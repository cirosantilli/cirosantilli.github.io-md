# Generate random text in PostgreSQL

↑ **Parent:** [PostgreSQL create test data](postgresql-create-test-data.md)

This one is good: [https://stackoverflow.com/questions/36533429/generate-random-string-in-postgresql/44200391#44200391](https://stackoverflow.com/questions/36533429/generate-random-string-in-postgresql/44200391#44200391) as it also describes how to generate multiple values.
```
with symbols(characters) as (VALUES ('ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789'))
select string_agg(substr(characters, (random() * (length(characters) - 1) + 1)::INTEGER, 1), '')
from symbols
join generate_series(1,8) as word(chr_idx) on 1 = 1 -- word length
join generate_series(1,10000) as words(idx) on 1 = 1 -- # of words
group by idx;
```

Then you can insert it into a row with:
```
create table tmp(s text);
insert into tmp(s)
  select s from
  (
    with symbols(characters) as (VALUES ('ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789'))
    select string_agg(substr(characters, (random() * (length(characters) - 1) + 1)::INTEGER, 1), '') as asdf
    from symbols
    join generate_series(1,8) as word(chr_idx) on 1 = 1 -- word length
    join generate_series(1,10000) as words(idx) on 1 = 1 -- # of words
    group by idx
  ) as sub(s);
```

A more convenient approach is likely to define the function:
```
CREATE OR REPLACE FUNCTION random_string(int) RETURNS TEXT as $$
select
  string_agg(substr(characters, (random() * length(characters) + 1)::integer, 1), '') as random_word
from (values('ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789    --')) as symbols(characters)
  join generate_series(1, $1) on 1 = 1
$$ language sql;
```

And then:
```
create table tmp(s text, t text);
insert into tmp(s) select random_string(10) from generate_series(10);
```

## ↑ Ancestors (16)

1. [PostgreSQL create test data](postgresql-create-test-data.md)
2. [PostgreSQL HOWTO](postgresql-howto.md)
3. [PostgreSQL getting started](postgresql-getting-started.md)
4. [PostgreSQL](postgresql.md)
5. [SQL implementation](sql-implementation.md)
6. [SQL](sql-split.md)
7. [Relational database management system](relational-database-management-system.md)
8. [Relational database](relational-database.md)
9. [Type of database](type-of-database.md)
10. [Database](database.md)
11. [Software](software-split.md)
12. [Computer](computer-split.md)
13. [Information technology](information-technology.md)
14. [Area of technology](area-of-technology.md)
15. [Technology](technology-split.md)
16. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (1)

- [PostgreSQL `generate_series`](postgresql-generate-series.md)
