# PostgreSQL full-text search

↑ **Parent:** [PostgreSQL HOWTO](postgresql-howto.md)  
🏷️ **Tags:** [Full-text search](full-text-search.md)

This section was tested on [Ubuntu 24.10](ubuntu-24-10.md), [PostgreSQL](postgresql.md) 16.6.

Let's create some test data like this:
```
time psql tmp -c 'DROP TABLE IF EXISTS fts;'
time psql tmp -c 'CREATE TABLE fts(s TEXT, i INTEGER);'
time psql tmp <<'EOF'
INSERT INTO fts SELECT
  i::text || ' ' ||
    (i * 2  )::text || ' ' ||
    (i * 5  )::text || ' ' ||
    (i * 7  )::text || ' ' ||
    (i * 11 )::text || ' ' ||
    (i * 13 )::text || ' ' ||
    (i * 17 )::text || ' ' ||
    (i * 23 )::text || ' ' ||
    (i * 29 )::text || ' ' ||
    (i * 31 )::text
  ,
  i % 100
FROM generate_series(1::bigint, 100000000::bigint) AS s(i);
EOF
```

The creation time was 2m13s, and the final size was:
```
    table_name    | pg_size_pretty | pg_total_relation_size
------------------+----------------+------------------------
 fts              | 13 GB          |            14067326976
```

This test data will be simple to predict what each line contains so we can make educated queries, while also posing some difficulty to the RDMS. As per:
```
time psql tmp -c 'SELECT * FROM fts LIMIT 10;'
```
the first columns look like:
```
                  s                  | i
-------------------------------------+----
 1 2 5 7 11 13 17 23 29 31           |  1
 2 4 10 14 22 26 34 46 58 62         |  2
 3 6 15 21 33 39 51 69 87 93         |  3
 4 8 20 28 44 52 68 92 116 124       |  4
 5 10 25 35 55 65 85 115 145 155     |  5
 6 12 30 42 66 78 102 138 174 186    |  6
 7 14 35 49 77 91 119 161 203 217    |  7
 8 16 40 56 88 104 136 184 232 248   |  8
 9 18 45 63 99 117 153 207 261 279   |  9
 10 20 50 70 110 130 170 230 290 310 | 10
```

We aimed to create a test table of size around 10 GB, as in practice it is around that order of size that index speedups start to become very obvious on a [SSD](solid-state-storage.md)-based system.

Before we create the index, let's see if our non-indexed queries are slow enough for our tests:
```
time psql tmp -c "SELECT * FROM fts WHERE s LIKE '% 50000000 %';"
```
which gives:
```
                                                 s                                                 | i
---------------------------------------------------------------------------------------------------+---
 10000000 20000000 50000000 70000000 110000000 130000000 170000000 230000000 290000000 310000000   | 0
 25000000 50000000 125000000 175000000 275000000 325000000 425000000 575000000 725000000 775000000 | 0
(2 rows)


real    0m11.758s
user    0m0.017s
sys     0m0.008s
```
so it should be enough to observe the index speedup.

Now let's create the index. First we create a [generated column](generated-column.md) that splits the strings with [`to_tsvector`](to-tsvector.md), and then we index that split column:
```
time psql tmp <<'EOF'
ALTER TABLE fts ADD COLUMN s_ts tsvector
  GENERATED ALWAYS AS (to_tsvector('english', s)) STORED;
EOF
time psql tmp -c 'CREATE INDEX s_ts_gin_idx ON fts USING GIN (s_ts);'
```
These commands took 8m51s and 40m8s and the DB size went up about 5x:
```
    table_name    | pg_size_pretty | pg_total_relation_size
------------------+----------------+------------------------
 fts              | 69 GB          |            74487758848
```

And finally let's try out the index:
```
time psql tmp -c "SELECT s, i FROM fts WHERE s_ts @@ to_tsquery('english', '50000000');"
```
which "instantly" gives us in 0m0.129s:
```
                                                   s                                                   | i
-------------------------------------------------------------------------------------------------------+---
 10000000 20000000 50000000 70000000 110000000 130000000 170000000 230000000 290000000 310000000       | 0
 25000000 50000000 125000000 175000000 275000000 325000000 425000000 575000000 725000000 775000000     | 0
 50000000 100000000 250000000 350000000 550000000 650000000 850000000 1150000000 1450000000 1550000000 | 0
```
so the index worked!

We understand from this that it only find exact word hits.

Another important use case is to search for prefixes of words, e.g. as you'd want in a simple autocompletion system. This can be achieved by adding `:*` at the end of the search term as in:
```
time psql tmp -c "SELECT s, i FROM fts WHERE s_ts @@ to_tsquery('english', '50000000:*');"
```
This finishes in the same amount of time, and gives:
```
                                                     s                                                     | i
-----------------------------------------------------------------------------------------------------------+----
 10000000 20000000 50000000 70000000 110000000 130000000 170000000 230000000 290000000 310000000           |  0
 38461539 76923078 192307695 269230773 423076929 500000007 653846163 884615397 1115384631 1192307709       | 39
 45454546 90909092 227272730 318181822 500000006 590909098 772727282 1045454558 1318181834 1409090926      | 46
 50000000 100000000 250000000 350000000 550000000 650000000 850000000 1150000000 1450000000 1550000000     |  0
 71428572 142857144 357142860 500000004 785714292 928571436 1214285724 1642857156 2071428588 2214285732    | 72
 100000000 200000000 500000000 700000000 1100000000 1300000000 1700000000 2300000000 2900000000 3100000000 |  0
 29411765 58823530 147058825 205882355 323529415 382352945 500000005 676470595 852941185 911764715         | 65
 25000000 50000000 125000000 175000000 275000000 325000000 425000000 575000000 725000000 775000000         |  0
```
so now we have cool hits such as `500000000`, `500000004`, `500000005`, `500000007` and `500000006`. The syntax is also mentioned at:
- [https://www.postgresql.org/docs/17/textsearch-controls.html#TEXTSEARCH-PARSING-QUERIES](https://www.postgresql.org/docs/17/textsearch-controls.html#TEXTSEARCH-PARSING-QUERIES)

Next we can also try some other queries with multiple terms. Text must contain two words with `&`:
```
time psql tmp -c "SELECT s, i FROM fts WHERE s_ts @@ to_tsquery('english', '50000000 & 175000000');"
```
gives:
```
                                                   s                                                   | i
-------------------------------------------------------------------------------------------------------+---
 25000000 50000000 125000000 175000000 275000000 325000000 425000000 575000000 725000000 775000000     | 0
```

Text can contain either word with `|`:
```
time psql tmp -c "SELECT s, i FROM fts WHERE s_ts @@ to_tsquery('english', '50000000 | 175000000');"
```
gives:
```
                                                    s                                                    | i
---------------------------------------------------------------------------------------------------------+---
 10000000 20000000 50000000 70000000 110000000 130000000 170000000 230000000 290000000 310000000         | 0
 50000000 100000000 250000000 350000000 550000000 650000000 850000000 1150000000 1450000000 1550000000   | 0
 87500000 175000000 437500000 612500000 962500000 1137500000 1487500000 2012500000 2537500000 2712500000 | 0
 25000000 50000000 125000000 175000000 275000000 325000000 425000000 575000000 725000000 775000000       | 0
 35000000 70000000 175000000 245000000 385000000 455000000 595000000 805000000 1015000000 1085000000     | 0
```

Text can contain the given words sequentially:
```
time psql tmp -c "SELECT s, i FROM fts WHERE s_ts @@ to_tsquery('english', '50000000 <-> 125000000 <-> 175000000');"
```
gives:
```
                                                   s                                                   | i
-------------------------------------------------------------------------------------------------------+---
 25000000 50000000 125000000 175000000 275000000 325000000 425000000 575000000 725000000 775000000     | 0
```

We can also inspect how words were split by simply doing a `SELECT *` again:
```
             s              | i |                                 s_ts
----------------------------+---+----------------------------------------------------------------------
1 2 5 7 11 13 17 23 29 31   | 1 | '1':1 '11':5 '13':6 '17':7 '2':2 '23':8 '29':9 '31':10 '5':3 '7':4
2 4 10 14 22 26 34 46 58 62 | 2 | '10':3 '14':4 '2':1 '22':5 '26':6 '34':7 '4':2 '46':8 '58':9 '62':10
3 6 15 21 33 39 51 69 87 93 | 3 | '15':3 '21':4 '3':1 '33':5 '39':6 '51':7 '6':2 '69':8 '87':9 '93':10
```

Let's check if the index updates automatically when we do an insert and if insertion seems to have been significantly slowed down by the index:
```
time psql tmp -c "INSERT INTO fts VALUES ('abcd efgh', 99)"
```
finishes in:
```
real    0m0.043s
user    0m0.014s
sys     0m0.010s
```
so performance is OK. Presumably, the insertion time is proportional to the number of tokens, doing one logarithmic operation per token, so indexing short chunks of text like titles is easy. And then let's find it:
```
time psql tmp -c "SELECT s, i FROM fts WHERE s_ts @@ to_tsquery('english', 'efgh');"
```
which finds it with:
```
     s     | i
-----------+----
 abcd efgh | 99
```
so we are all good. Unfortunately, accurate performance benchmarking is a bit harder than that, as the index by default first collects a certain number of updates into memory into the "pending list", before actually inserting them all at once after a certain mass is reached, as documented at: [https://www.postgresql.org/docs/17/gin.html#GIN-IMPLEMENTATION](https://www.postgresql.org/docs/17/gin.html#GIN-IMPLEMENTATION). We are not going that deep today.

The next thing that we need to understand is how [`to_tsvector`](to-tsvector.md) [tokenizes](https://ourbigbook.com/go/topic/tokenizes) strings for the `english` language. For example running:
```
psql -c "select to_tsvector('english', 'A Dog run runs fast faster two Cats: b c to from 1 é befhyph-afthyph.')"
```
gives:
```
'1':13
'afthyph':17
'b':9
'befhyph':16
'befhyph-afthyph':15
'c':10
'cat':8
'dog':2
'fast':5
'faster':6
'run':3,4
'two':7
'é':14
```
so we understand some of the heuristic normalizations:
- prepositions like `to` and `from` are gone. These are called stopwords as documented at: [https://www.postgresql.org/docs/17/textsearch-controls.html#TEXTSEARCH-PARSING-DOCUMENTS](https://www.postgresql.org/docs/17/textsearch-controls.html#TEXTSEARCH-PARSING-DOCUMENTS)
- words are lowercased and singularized, e.g. `Cats` becomes `cat`
- hyphenated words are stored both in separate components and in the full hyphenated form:
  - `'afthyph':17`
  - `'befhyph':16`
  - `'befhyph-afthyph':15`

The full list of languages available can be obtained with:
```
psql -c '\dF'
```
On [Ubuntu 24.10](ubuntu-24-10.md), the list contains major world languages, plus the special `simple` configuration such that:
```
psql -c "select to_tsvector('simple', 'A Dog run runs fast faster two Cats: b c to from 1 é befhyph-afthyph.')"
```
gives:
```
'1':13
'a':1
'afthyph':17
'b':9
'befhyph':16
'befhyph-afthyph':15
'c':10
'cats':8
'dog':2
'fast':5
'faster':6
'from':12
'run':3
'runs':4
'to':11
'two':7
'é':14
```
so we understand that it is similar to `english` but it does not:
- seem to have any stopwords
- do singularization normalization

From the query side of things, if the query is going to be open to end users on a web interface, we need to understand `to_tsquery` better. The issue is that `to_tsquery` is quite brutal and happily throws errors for common things users might do e.g. spaces:
```
select to_tsquery('english', 'abc def');
```
giving:
```
ERROR:  syntax error in tsquery: "abc def"
```
To avoid such errors, we can use:
- `plainto_tsquery`: ANDs everything
- `websearch_to_tsquery`: supports `AND` with spaces, OR with `or`, word negation with `-word` and concatenation with `"my word"`. But it unfortunately does not support prefixing, which is what everyone and their mother wants for autocomplete: [https://stackoverflow.com/questions/14103880/escaping-special-characters-in-to-tsquery#comment78452351_41804957](https://stackoverflow.com/questions/14103880/escaping-special-characters-in-to-tsquery#comment78452351_41804957)
Bibliography:
- [https://stackoverflow.com/questions/16020164/psqlexception-error-syntax-error-in-tsquery/16020565#16020565](https://stackoverflow.com/questions/16020164/psqlexception-error-syntax-error-in-tsquery/16020565#16020565)
- [https://stackoverflow.com/questions/14103880/escaping-special-characters-in-to-tsquery](https://stackoverflow.com/questions/14103880/escaping-special-characters-in-to-tsquery)
- [https://www.reddit.com/r/rails/comments/1cmloa6/sanitizing_a_search_phrase_when_using_to_tsvector/](https://www.reddit.com/r/rails/comments/1cmloa6/sanitizing_a_search_phrase_when_using_to_tsvector/)
- [https://stackoverflow.com/questions/6735881/to-tsquery-validation](https://stackoverflow.com/questions/6735881/to-tsquery-validation)
- [https://dba.stackexchange.com/questions/135030/filtering-special-characters-in-to-tsquery](https://dba.stackexchange.com/questions/135030/filtering-special-characters-in-to-tsquery)

Also posted at:
- [https://www.reddit.com/r/PostgreSQL/comments/12yld1o/comment/m3l5nkv/](https://www.reddit.com/r/PostgreSQL/comments/12yld1o/comment/m3l5nkv/) "Is it worth using Postgres' builtin full-text search or should I go straight to Elastic?", high top Google result for "PostgreSQL full text search" as of 2024. Random, but it's there.

## ↑ Ancestors (15)

1. [PostgreSQL HOWTO](postgresql-howto.md)
2. [PostgreSQL getting started](postgresql-getting-started.md)
3. [PostgreSQL](postgresql.md)
4. [SQL implementation](sql-implementation.md)
5. [SQL](sql-split.md)
6. [Relational database management system](relational-database-management-system.md)
7. [Relational database](relational-database.md)
8. [Type of database](type-of-database.md)
9. [Database](database.md)
10. [Software](software-split.md)
11. [Computer](computer-split.md)
12. [Information technology](information-technology.md)
13. [Area of technology](area-of-technology.md)
14. [Technology](technology-split.md)
15. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (1)

- [Generating test data for full text search tests](updates/generating-test-data-for-full-text-search-tests.md)
