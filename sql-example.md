# SQL example

↑ **Parent:** [SQL](sql-split.md)

We have some runnable [SQL](sql-split.md) examples with [assertion](assertion-software-development.md) under the `sequelize/raw` directory.

These examples are written in the [Sequelize](sequelize-split.md) library using raw queries.

Sequelize is used minimally, just to feed raw queries in transparently to any underlying database, and get minimally parsed results out for us, which we then assert with standard [JavaScript](javascript.md). The queries themselves are all written by hand.

By default the examples run on [SQLite](sqlite.md). Just like the examples from [sequelize example](sequelize-example.md), you can set the database at runtime as:
- `./index.js` or `./index.js l`: [SQLite](sqlite.md)
- `./index.js p`: [PostgreSQL](postgresql.md). You must manually create a database called `tmp` and ensure that peer authentication works for it

Here we list only examples which we believe are standard SQL, and should therefore work across different SQL implementations:
- [nodejs/sequelize/raw/index.js](nodejs/sequelize/raw/index.js): basic hello world to demonstrate the setup and very simple functionality
- [nodejs/sequelize/raw/many_to_many.js](nodejs/sequelize/raw/many_to_many.js): illustrates [many-to-many relations](many-to-many.md) with [JOIN](join-sql.md). Contains:
- [SQL transaction](sql-transaction.md) examples:
  - [nodejs/sequelize/raw/commit_error.js](nodejs/sequelize/raw/commit_error.js): [https://stackoverflow.com/questions/27245101/why-should-we-use-rollback-in-sql-explicitly/27245234#27245234](https://stackoverflow.com/questions/27245101/why-should-we-use-rollback-in-sql-explicitly/27245234#27245234) and [https://stackoverflow.com/questions/48277519/how-to-use-commit-and-rollback-in-a-postgresql-function/48277708#48277708](https://stackoverflow.com/questions/48277519/how-to-use-commit-and-rollback-in-a-postgresql-function/48277708#48277708) suggest that on [PostgreSQL](postgresql.md), once something fails inside a transaction, all queries in the current transaction are ignored, and `COMMIT` simply does a `ROLLBACK`. Let's check. Yup, true for Postgres, but false for [SQLite](sqlite.md), SQLite just happily runs anything it can, you really need `ROLLBACK` for it.
  - [SQL isolation level example](sql-isolation-level-example.md)
- [GROUP BY](group-by-sql.md) and [SQL aggregate functions](sql-aggregate-function.md):
  - [nodejs/sequelize/raw/group_by_extra_column.js](nodejs/sequelize/raw/group_by_extra_column.js): let's see if it blows up or not on different DB systems, [`sqlite3` Node.js package](sqlite3-node-js-package.md) allows it:
    - [https://github.com/sequelize/sequelize/issues/5481#issuecomment-964387232](https://github.com/sequelize/sequelize/issues/5481#issuecomment-964387232)
    - [https://dba.stackexchange.com/questions/141594/how-select-column-does-not-list-in-group-by-clause/141600](https://dba.stackexchange.com/questions/141594/how-select-column-does-not-list-in-group-by-clause/141600) says that it was allowed in [SQL:1999](sql-1999.md) when there are no ambiguities due to constraints, e.g. when grouping by unique columns
    - [https://github.com/postgres/postgres/blob/REL_13_5/src/test/regress/sql/functional_deps.sql#L27](https://github.com/postgres/postgres/blob/REL_13_5/src/test/regress/sql/functional_deps.sql#L27) shows that [PostgreSQL](postgresql.md) wants it to work for `UNIQUE NOT NULL`, but they just haven't implemented it as of 13.5, where it only works if you group by `PRIMARY KEY`
    - [https://dba.stackexchange.com/questions/158015/why-can-i-select-all-fields-when-grouping-by-primary-key-but-not-when-grouping-b](https://dba.stackexchange.com/questions/158015/why-can-i-select-all-fields-when-grouping-by-primary-key-but-not-when-grouping-b) also says that `UNIQUE NOT NULL` doesn't work. Dan Lenski then points to a rationale mailing list thread.
  - [nodejs/sequelize/raw/group_by_max_full_row.js](nodejs/sequelize/raw/group_by_max_full_row.js): here we try to get the full row of each group at which a given column reaches the max of the group
    - [Postgres](postgresql.md): has `SELECT DISCINTCT ON` which works perfectly if you only want one row in case of multiple rows attaining the max. `ON` is an extension to the standard unfortunately: [https://www.postgresql.org/docs/9.3/sql-select.html#SQL-DISTINCT](https://www.postgresql.org/docs/9.3/sql-select.html#SQL-DISTINCT) Docs specify that it always respects `ORDER BY` when selecting the row.
      - [https://stackoverflow.com/questions/586781/postgresql-fetch-the-row-which-has-the-max-value-for-a-column](https://stackoverflow.com/questions/586781/postgresql-fetch-the-row-which-has-the-max-value-for-a-column) asks it without the multiple matches use case
        - [https://stackoverflow.com/questions/586781/postgresql-fetch-the-rows-which-have-the-max-value-for-a-column-in-each-group/587209#587209](https://stackoverflow.com/questions/586781/postgresql-fetch-the-rows-which-have-the-max-value-for-a-column-in-each-group/587209#587209) also present in simpler form at [https://stackoverflow.com/questions/121387/fetch-the-rows-which-have-the-max-value-for-a-column-for-each-distinct-value-of/123481#123481](https://stackoverflow.com/questions/121387/fetch-the-rows-which-have-the-max-value-for-a-column-for-each-distinct-value-of/123481#123481) gives a very nice [OUTER JOIN](outer-join.md) only solution! Incredible, very elegant.
      - [https://dba.stackexchange.com/questions/171938/get-only-rows-with-max-group-value](https://dba.stackexchange.com/questions/171938/get-only-rows-with-max-group-value) asks specifically the case of multiple matches to the max
    - [SQLite](sqlite.md):
      - [https://stackoverflow.com/questions/48326957/row-with-max-value-per-group-sqlite](https://stackoverflow.com/questions/48326957/row-with-max-value-per-group-sqlite)
        - [https://stackoverflow.com/questions/48326957/row-with-max-value-per-group-sqlite/48328243#48328243](https://stackoverflow.com/questions/48326957/row-with-max-value-per-group-sqlite/48328243#48328243) teaches us that in SQLite min and max are magic and guarantee that the matching row is returned
        - [https://stackoverflow.com/questions/48326957/row-with-max-value-per-group-sqlite/72996649#72996649](https://stackoverflow.com/questions/48326957/row-with-max-value-per-group-sqlite/72996649#72996649) [Ciro Santilli](ciro-santilli-split.md) uses the magic of `ROW_NUMBER`
      - [https://stackoverflow.com/questions/17277152/sqlite-select-distinct-of-one-column-and-get-the-others/71924314#71924314](https://stackoverflow.com/questions/17277152/sqlite-select-distinct-of-one-column-and-get-the-others/71924314#71924314) get any full row without specifying which, we teach how to specify
      - [https://code.djangoproject.com/ticket/22696](https://code.djangoproject.com/ticket/22696) WONTFIXed `DISTINCT ON`
        - [https://stackoverflow.com/questions/50846722/what-is-the-difference-between-postgres-distinct-vs-distinct-on/72997494#72997494](https://stackoverflow.com/questions/50846722/what-is-the-difference-between-postgres-distinct-vs-distinct-on/72997494#72997494) `DISTINCT` vs `DISTINCT ON`, somewhat related question
    - [https://stackoverflow.com/questions/5803032/group-by-to-return-entire-row](https://stackoverflow.com/questions/5803032/group-by-to-return-entire-row) asks how to take the top N with distinct after order limit. I don't know how to do it in Postgres
  - [nodejs/sequelize/raw/most_frequent.js](nodejs/sequelize/raw/most_frequent.js): illustrates a few variants of findind the [mode](mode-statistics.md), including across GROUP
    - [https://stackoverflow.com/questions/12235595/find-most-frequent-value-in-sql-column/72979899#72979899](https://stackoverflow.com/questions/12235595/find-most-frequent-value-in-sql-column/72979899#72979899)
  - [nodejs/sequelize/raw/group_by_max_n.js](nodejs/sequelize/raw/group_by_max_n.js): get the top N in each group
    - PostgreSQL
      - [https://stackoverflow.com/questions/1124603/grouped-limit-in-postgresql-show-the-first-n-rows-for-each-group](https://stackoverflow.com/questions/1124603/grouped-limit-in-postgresql-show-the-first-n-rows-for-each-group)
      - [https://stackoverflow.com/questions/7613785/postgresql-top-n-entries-per-item-in-same-table](https://stackoverflow.com/questions/7613785/postgresql-top-n-entries-per-item-in-same-table)
        - [https://dba.stackexchange.com/questions/247275/rank-used-in-where-returns-invalid-column-but-exists-in-results-set](https://dba.stackexchange.com/questions/247275/rank-used-in-where-returns-invalid-column-but-exists-in-results-set)
    - SQLite [https://stackoverflow.com/questions/28119176/select-top-n-record-from-each-group-sqlite](https://stackoverflow.com/questions/28119176/select-top-n-record-from-each-group-sqlite)
    - MySQL [https://stackoverflow.com/questions/2129693/using-limit-within-group-by-to-get-n-results-per-group](https://stackoverflow.com/questions/2129693/using-limit-within-group-by-to-get-n-results-per-group)
- order results in the same order as `IN`:
  - MysQL: [https://stackoverflow.com/questions/396748/ordering-by-the-order-of-values-in-a-sql-in-clause](https://stackoverflow.com/questions/396748/ordering-by-the-order-of-values-in-a-sql-in-clause)
  - PostgreSQL:
    - [https://stackoverflow.com/questions/866465/order-by-the-in-value-list](https://stackoverflow.com/questions/866465/order-by-the-in-value-list)
    - [https://dba.stackexchange.com/questions/59394/order-of-returned-rows-with-in-statement](https://dba.stackexchange.com/questions/59394/order-of-returned-rows-with-in-statement)
- LIMIT by a running total: TODO links

## ↑ Ancestors (11)

1. [SQL](sql-split.md)
2. [Relational database management system](relational-database-management-system.md)
3. [Relational database](relational-database.md)
4. [Type of database](type-of-database.md)
5. [Database](database.md)
6. [Software](software-split.md)
7. [Computer](computer-split.md)
8. [Information technology](information-technology.md)
9. [Area of technology](area-of-technology.md)
10. [Technology](technology-split.md)
11. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (3)

- [nodejs/sequelize/raw/parallel_select_and_update.js](_file/nodejs/sequelize/raw/parallel_select_and_update.js.md)
- [nodejs/sequelize/raw/parallel_update_async.js](_file/nodejs/sequelize/raw/parallel_update_async.js.md)
- [Sequelize raw query](sequelize-raw-query.md)
