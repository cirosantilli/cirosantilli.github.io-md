# Generating test data for full text search tests

↑ **Parent:** [Updates](../updates-split.md)

<a id="_509"></a>
I've been thinking lightly about adding full text search to [OurBigBook](../ourbigbook.md).

<a id="_510"></a>
For example, at [https://docs.ourbigbook.com/news/article-and-topic-id-prefix-search](https://docs.ourbigbook.com/news/article-and-topic-id-prefix-search) article search was added, but it only finds if you search something that appears right at the start of a title, e.g. for:<a id="_511"></a>

```
Fundamental theorem of calculus
```
you'd get a hit for:<a id="_512"></a>

```
fundamental
```
but not for<a id="_513"></a>

```
calculus
```

<a id="_514"></a>
To do this efficiently, we need full text search, which [PostgreSQL](../postgresql.md) implements.

<a id="_515"></a>
But finding a clean way to generate test data for testing out the speedup was not so easy and exploration into this led me to publishing a few new slightly improved methods where Googlers can now find them:<a id="_516"></a>

<a id="_517"></a>
- <a id="_518"></a>
  [https://unix.stackexchange.com/questions/97160/is-there-something-like-a-lorem-ipsum-generator/787733#787733](https://unix.stackexchange.com/questions/97160/is-there-something-like-a-lorem-ipsum-generator/787733#787733) I propose a neat random "sentence" generator using common CLI tools like [`grep`](../grep.md) and [`sed`](../sed.md) and the pre-installed Ubuntu dictionary `/usr/share/dict/american-english`:<a id="_519"></a>

  ```
  grep -v "'" /usr/share/dict/american-english |
  shuf -r |
  paste -d ' ' $(printf "%4s" | sed 's/ /- /g') |
  sed -e 's/^\(.\)/\U\1/;s/$/./' |
  head -n10000000 \
  > lorem.txt
  ```

  <a id="_520"></a>

  <a id="_521"></a>
  - to achieve that, I also proposed two superior "join every N lines" method for the CLI: [https://stackoverflow.com/questions/25973140/joining-every-group-of-n-lines-into-one-with-bash/79257780#79257780](https://stackoverflow.com/questions/25973140/joining-every-group-of-n-lines-into-one-with-bash/79257780#79257780), notably this [awk](../awk.md) poem:<a id="_522"></a>

    ```
    seq 10 | awk '{ printf("%s%s", NR  == 1 ? "" : NR % 3 == 1 ? "\n" : " ", $0 ) } END { printf("\n") }'
    ```
<a id="_523"></a>
- [https://stackoverflow.com/questions/3371503/sql-populate-table-with-random-data/79255281#79255281](https://stackoverflow.com/questions/3371503/sql-populate-table-with-random-data/79255281#79255281) I propose:<a id="_524"></a>

  <a id="_525"></a>
  - a clean [PostgreSQL](../postgresql.md) random string stored procedure that picks random characters from an allowed character list<a id="_526"></a>

    ```
    CREATE OR REPLACE FUNCTION random_string(int) RETURNS TEXT as $$
    select
    string_agg(substr(characters, (random() * length(characters) + 1)::integer, 1), '') as random_word
    from (values('ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789-    ')) as symbols(characters)
    join generate_series(1, $1) on 1 = 1
    $$ language sql;
    ```
  <a id="_527"></a>
  - first generating [PostgreSQL](../postgresql.md) data as [CSV](../comma-separated-values.md), and then importing the CSV into PostgreSQL as a more flexible method. This can also be done in a streaming fashion from stdin which is neat.<a id="_528"></a>

    ```
    python generate_data.py 10 | psql mydb -c '\copy "mytable" FROM STDIN'
    ```
<a id="_529"></a>
- [https://stackoverflow.com/questions/16020164/psqlexception-error-syntax-error-in-tsquery/79437030#79437030](https://stackoverflow.com/questions/16020164/psqlexception-error-syntax-error-in-tsquery/79437030#79437030) regarding the safe generation of prefix search `tsquery` from user inputs without query errors, I've learned about `websearch_to_tsquery` and further highlighted a possible `tsquery -> text -> tsquery` approach that might be correct for prefix searches
<a id="_530"></a>
- [https://stackoverflow.com/questions/67438575/fulltext-search-using-sequelize-postgres/79439253#79439253](https://stackoverflow.com/questions/67438575/fulltext-search-using-sequelize-postgres/79439253#79439253) I put everything together into a minimal [Sequelize](../sequelize-split.md) example, read for usage in [OurBigBook](../ourbigbook.md)

<a id="_531"></a>
Finally I did a writeup summarizing PostgreSQL full text search: [Section "PostgreSQL full-text search"](../postgresql-full-text-search.md) and also dumped it at: [https://www.reddit.com/r/PostgreSQL/comments/12yld1o/is_it_worth_using_postgres_builtin_fulltext/](https://www.reddit.com/r/PostgreSQL/comments/12yld1o/is_it_worth_using_postgres_builtin_fulltext/) for good measure.

## ↑ Ancestors (3)

1. [Updates](../updates-split.md)
2. [Ciro Santilli](../ciro-santilli-split.md)
3. [Ciro Santilli's Homepage](../split.md)
