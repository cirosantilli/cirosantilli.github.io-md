# SQL

↑ **Parent:** [Relational database management system](software.md#relational-database-management-system)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/SQL)

**Table of contents**

- [SQL example](#sql-example)
- [SQL implementation](#sql-implementation)
  - [IBM Db2](#ibm-db2)
  - [MySQL](#mysql)
    - [mysqldump](#mysqldump)
      - [mysqldump to CSV](#mysqldump-to-csv)
    - [MariaDB](#mariadb)
  - [PostgreSQL](#postgresql)
    - [PostgreSQL getting started](#postgresql-getting-started)
      - [PostgreSQL HOWTO](#postgresql-howto)
        - [PostgreSQL create test data](#postgresql-create-test-data)
          - [Generate random text in PostgreSQL](#generate-random-text-in-postgresql)
        - [PostgreSQL full-text search](#postgresql-full-text-search)
    - [Create a test user in PostgreSQL](#create-a-test-user-in-postgresql)
    - [Peer authentication](#peer-authentication)
    - [PostgreSQL logging](#postgresql-logging)
    - [PostgreSQL serialization failure](#postgresql-serialization-failure)
    - [PostgreSQL function](#postgresql-function)
      - [PostgreSQL `generate_series`](#postgresql-generate-series)
      - [`to_tsvector`](#to-tsvector)
  - [Microsoft SQL Server](#microsoft-sql-server)
    - [Transact-SQL](#transact-sql)
  - [Oracle Database](#oracle-database)
  - [SQLite](#sqlite)
    - [SQLite import CSV](#sqlite-import-csv)
      - [SQLite import CSV from stdin](#sqlite-import-csv-from-stdin)
    - [SQLite import JSON](#sqlite-import-json)
    - [SQLite benchmark](#sqlite-benchmark)
    - [SQLite C extension](#sqlite-c-extension)
    - [SQLite isolation levels](#sqlite-isolation-levels)
    - [Node.js SQLite bindings](#node-js-sqlite-bindings)
      - [`sqlite3` Node.js package](#sqlite3-node-js-package)
      - [`better-sqlite3` Node.js package](#better-sqlite3-node-js-package)
- [SQL function](#sql-function)
  - [SQL set returning function](#sql-set-returning-function)
    - [SQL `genenerate_series`](#sql-genenerate-series)
  - [SQL aggregate function](#sql-aggregate-function)
    - [SQL `COUNT` function](#sql-count-function)
- [SQL keyword](#sql-keyword)
  - [SQL CASCADE](#sql-cascade)
  - [DELETE (SQL)](#delete-sql)
    - [Delete all duplicate rows in SQL](#delete-all-duplicate-rows-in-sql)
  - [GROUP BY (SQL)](#group-by-sql)
    - [HAVING (SQL)](#having-sql)
      - [HAVING vs WHERE](#having-vs-where)
  - [INSERT (SQL)](#insert-sql)
    - [Upsert](#upsert)
      - [Upsert with `NOT NULL` column](#upsert-with-not-null-column)
  - [JOIN (SQL)](#join-sql)
    - [SQL prefix column names with the table they came from](#sql-prefix-column-names-with-the-table-they-came-from)
    - [INNER JOIN](#inner-join)
    - [OUTER JOIN](#outer-join)
  - [LIKE (SQL)](#like-sql)
  - [SELECT (SQL)](#select-sql)
    - [SELECT FOR UPDATE](#select-for-update)
  - [SQL stored procedure](#sql-stored-procedure)
    - [SQL FUNCTION keyword](#sql-function-keyword)
    - [SQL PROCEDURE](#sql-procedure)
  - [SQL TRIGGER](#sql-trigger)
  - [ISO SQL TRIGGER syntax](#iso-sql-trigger-syntax)
    - [nodejs/sequelize/raw/trigger\_count.js](#_file/nodejs/sequelize/raw/trigger_count.js)
  - [UNION (SQL)](#union-sql)
  - [UPDATE (SQL)](#update-sql)
    - [Update multiple rows with different values in a single SQL query](#update-multiple-rows-with-different-values-in-a-single-sql-query)
    - [UPDATE with JOIN (SQL)](#update-with-join-sql)
      - [DELETE with JOIN (SQL)](#delete-with-join-sql)
- [SQL standard](#sql-standard)
  - [SQL standard version](#sql-standard-version)
    - [SQL:1999](#sql-1999)
- [SQL application](#sql-application)
  - [SQL histogram](#sql-histogram)
    - [SQL 2D histogram](#sql-2d-histogram)
  - [SQL tree traversal](#sql-tree-traversal)
    - [Closure table](#closure-table)
    - [Nested set model in SQL](#nested-set-model-in-sql)
- [SQL feature](#sql-feature)
  - [Generated column](#generated-column)
  - [SQL RECURSIVE query](#sql-recursive-query)
    - [SQL RECURSIVE prevent infinite recursion](#sql-recursive-prevent-infinite-recursion)
  - [SQL spatial index](#sql-spatial-index)
    - [PostgreSQL spatial index](#postgresql-spatial-index)
      - [PostgreSQL GIST](#postgresql-gist)
      - [PostGIS](#postgis)
  - [SQL subquery](#sql-subquery)
    - [Common Table Expression](#common-table-expression)
      - [CTE insert values](#cte-insert-values)
  - [SQL transaction](#sql-transaction)
    - [SQL transaction isolation level](#sql-transaction-isolation-level)
      - [SQL READ UNCOMMITTED isolation level](#sql-read-uncommitted-isolation-level)
      - [SQL READ COMMITTED isolation level](#sql-read-committed-isolation-level)
      - [SQL REPEATABLE READ isolation level](#sql-repeatable-read-isolation-level)
      - [SQL SERIALIZABLE isolation level](#sql-serializable-isolation-level)
      - [SQL isolation level example](#sql-isolation-level-example)
        - [SQL parallel update example](#sql-parallel-update-example)
          - [nodejs/sequelize/raw/parallel\_update\_async.js](#_file/nodejs/sequelize/raw/parallel_update_async.js)
          - [nodejs/sequelize/raw/parallel\_select\_and\_update.js](#_file/nodejs/sequelize/raw/parallel_select_and_update.js)
          - [nodejs/sequelize/raw/parallel\_select\_and\_update\_deterministic.js](#_file/nodejs/sequelize/raw/parallel_select_and_update_deterministic.js)
          - [nodejs/sequelize/raw/parallel\_create\_delete\_empty\_tag.js](#_file/nodejs/sequelize/raw/parallel_create_delete_empty_tag.js)
  - [Window function (SQL)](#window-function-sql)
    - [`ROW_NUMBER`](#row-number)
    - [SQL window `RANGE`](#sql-window-range)
    - [SQL contiguous ranges](#sql-contiguous-ranges)

## SQL example

↑ **Parent:** [SQL](sql.md)

We have some runnable [SQL](sql.md) examples with [assertion](software.md#assertion-software-development) under the `sequelize/raw` directory.

These examples are written in the [Sequelize](sequelize.md) library using raw queries.

Sequelize is used minimally, just to feed raw queries in transparently to any underlying database, and get minimally parsed results out for us, which we then assert with standard [JavaScript](programming-language.md#javascript). The queries themselves are all written by hand.

By default the examples run on [SQLite](#sqlite). Just like the examples from [sequelize example](sequelize.md#sequelize-example), you can set the database at runtime as:
- `./index.js` or `./index.js l`: [SQLite](#sqlite)
- `./index.js p`: [PostgreSQL](#postgresql). You must manually create a database called `tmp` and ensure that peer authentication works for it

Here we list only examples which we believe are standard SQL, and should therefore work across different SQL implementations:
- [nodejs/sequelize/raw/index.js](nodejs/sequelize/raw/index.js): basic hello world to demonstrate the setup and very simple functionality
- [nodejs/sequelize/raw/many_to_many.js](nodejs/sequelize/raw/many_to_many.js): illustrates [many-to-many relations](software.md#many-to-many) with [JOIN](#join-sql). Contains:
- [SQL transaction](#sql-transaction) examples:
  - [nodejs/sequelize/raw/commit_error.js](nodejs/sequelize/raw/commit_error.js): [https://stackoverflow.com/questions/27245101/why-should-we-use-rollback-in-sql-explicitly/27245234#27245234](https://stackoverflow.com/questions/27245101/why-should-we-use-rollback-in-sql-explicitly/27245234#27245234) and [https://stackoverflow.com/questions/48277519/how-to-use-commit-and-rollback-in-a-postgresql-function/48277708#48277708](https://stackoverflow.com/questions/48277519/how-to-use-commit-and-rollback-in-a-postgresql-function/48277708#48277708) suggest that on [PostgreSQL](#postgresql), once something fails inside a transaction, all queries in the current transaction are ignored, and `COMMIT` simply does a `ROLLBACK`. Let's check. Yup, true for Postgres, but false for [SQLite](#sqlite), SQLite just happily runs anything it can, you really need `ROLLBACK` for it.
  - [SQL isolation level example](#sql-isolation-level-example)
- [GROUP BY](#group-by-sql) and [SQL aggregate functions](#sql-aggregate-function):
  - [nodejs/sequelize/raw/group_by_extra_column.js](nodejs/sequelize/raw/group_by_extra_column.js): let's see if it blows up or not on different DB systems, [`sqlite3` Node.js package](#sqlite3-node-js-package) allows it:
    - [https://github.com/sequelize/sequelize/issues/5481#issuecomment-964387232](https://github.com/sequelize/sequelize/issues/5481#issuecomment-964387232)
    - [https://dba.stackexchange.com/questions/141594/how-select-column-does-not-list-in-group-by-clause/141600](https://dba.stackexchange.com/questions/141594/how-select-column-does-not-list-in-group-by-clause/141600) says that it was allowed in [SQL:1999](#sql-1999) when there are no ambiguities due to constraints, e.g. when grouping by unique columns
    - [https://github.com/postgres/postgres/blob/REL_13_5/src/test/regress/sql/functional_deps.sql#L27](https://github.com/postgres/postgres/blob/REL_13_5/src/test/regress/sql/functional_deps.sql#L27) shows that [PostgreSQL](#postgresql) wants it to work for `UNIQUE NOT NULL`, but they just haven't implemented it as of 13.5, where it only works if you group by `PRIMARY KEY`
    - [https://dba.stackexchange.com/questions/158015/why-can-i-select-all-fields-when-grouping-by-primary-key-but-not-when-grouping-b](https://dba.stackexchange.com/questions/158015/why-can-i-select-all-fields-when-grouping-by-primary-key-but-not-when-grouping-b) also says that `UNIQUE NOT NULL` doesn't work. Dan Lenski then points to a rationale mailing list thread.
  - [nodejs/sequelize/raw/group_by_max_full_row.js](nodejs/sequelize/raw/group_by_max_full_row.js): here we try to get the full row of each group at which a given column reaches the max of the group
    - [Postgres](#postgresql): has `SELECT DISCINTCT ON` which works perfectly if you only want one row in case of multiple rows attaining the max. `ON` is an extension to the standard unfortunately: [https://www.postgresql.org/docs/9.3/sql-select.html#SQL-DISTINCT](https://www.postgresql.org/docs/9.3/sql-select.html#SQL-DISTINCT) Docs specify that it always respects `ORDER BY` when selecting the row.
      - [https://stackoverflow.com/questions/586781/postgresql-fetch-the-row-which-has-the-max-value-for-a-column](https://stackoverflow.com/questions/586781/postgresql-fetch-the-row-which-has-the-max-value-for-a-column) asks it without the multiple matches use case
        - [https://stackoverflow.com/questions/586781/postgresql-fetch-the-rows-which-have-the-max-value-for-a-column-in-each-group/587209#587209](https://stackoverflow.com/questions/586781/postgresql-fetch-the-rows-which-have-the-max-value-for-a-column-in-each-group/587209#587209) also present in simpler form at [https://stackoverflow.com/questions/121387/fetch-the-rows-which-have-the-max-value-for-a-column-for-each-distinct-value-of/123481#123481](https://stackoverflow.com/questions/121387/fetch-the-rows-which-have-the-max-value-for-a-column-for-each-distinct-value-of/123481#123481) gives a very nice [OUTER JOIN](#outer-join) only solution! Incredible, very elegant.
      - [https://dba.stackexchange.com/questions/171938/get-only-rows-with-max-group-value](https://dba.stackexchange.com/questions/171938/get-only-rows-with-max-group-value) asks specifically the case of multiple matches to the max
    - [SQLite](#sqlite):
      - [https://stackoverflow.com/questions/48326957/row-with-max-value-per-group-sqlite](https://stackoverflow.com/questions/48326957/row-with-max-value-per-group-sqlite)
        - [https://stackoverflow.com/questions/48326957/row-with-max-value-per-group-sqlite/48328243#48328243](https://stackoverflow.com/questions/48326957/row-with-max-value-per-group-sqlite/48328243#48328243) teaches us that in SQLite min and max are magic and guarantee that the matching row is returned
        - [https://stackoverflow.com/questions/48326957/row-with-max-value-per-group-sqlite/72996649#72996649](https://stackoverflow.com/questions/48326957/row-with-max-value-per-group-sqlite/72996649#72996649) [Ciro Santilli](ciro-santilli.md) uses the magic of `ROW_NUMBER`
      - [https://stackoverflow.com/questions/17277152/sqlite-select-distinct-of-one-column-and-get-the-others/71924314#71924314](https://stackoverflow.com/questions/17277152/sqlite-select-distinct-of-one-column-and-get-the-others/71924314#71924314) get any full row without specifying which, we teach how to specify
      - [https://code.djangoproject.com/ticket/22696](https://code.djangoproject.com/ticket/22696) WONTFIXed `DISTINCT ON`
        - [https://stackoverflow.com/questions/50846722/what-is-the-difference-between-postgres-distinct-vs-distinct-on/72997494#72997494](https://stackoverflow.com/questions/50846722/what-is-the-difference-between-postgres-distinct-vs-distinct-on/72997494#72997494) `DISTINCT` vs `DISTINCT ON`, somewhat related question
    - [https://stackoverflow.com/questions/5803032/group-by-to-return-entire-row](https://stackoverflow.com/questions/5803032/group-by-to-return-entire-row) asks how to take the top N with distinct after order limit. I don't know how to do it in Postgres
  - [nodejs/sequelize/raw/most_frequent.js](nodejs/sequelize/raw/most_frequent.js): illustrates a few variants of findind the [mode](mathematics.md#mode-statistics), including across GROUP
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

## SQL implementation

↑ **Parent:** [SQL](sql.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/SQL_implementation)

### IBM Db2

↑ **Parent:** [SQL implementation](#sql-implementation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/IBM_Db2)

### MySQL

↑ **Parent:** [SQL implementation](#sql-implementation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/MySQL)

Login without password: [https://askubuntu.com/questions/915585/how-to-login-mysql-shell-when-mysql-have-no-password](https://askubuntu.com/questions/915585/how-to-login-mysql-shell-when-mysql-have-no-password)
```
sudo mysql
```
works on [Ubuntu](systems-programming.md#ubuntu) 20.10.

Create user for further logins without `sudo` [https://askubuntu.com/questions/915585/how-to-login-mysql-shell-when-mysql-have-no-password/1325689#1325689](https://askubuntu.com/questions/915585/how-to-login-mysql-shell-when-mysql-have-no-password/1325689#1325689):
```
sudo mysql -e "CREATE USER $USER"
```

Run command from CLI [https://stackoverflow.com/questions/1602904/how-do-you-run-a-single-query-through-mysql-from-the-command-line](https://stackoverflow.com/questions/1602904/how-do-you-run-a-single-query-through-mysql-from-the-command-line)
```
mysql -e 'SHOW DATABASES'
```

Create test user with password:
```
sudo mysql -e 'CREATE USER user0 IDENTIFIED WITH mysql_native_password BY "a"'
sudo mysql -e 'GRANT ALL PRIVILEGES ON database_name.* TO "user0"'
```
and login as that user:
```
mysql -u user0 -p
```
Login with password given on the command line:
```
mysql -u user0 -pmypassword
```
The `IDENTIFIED WITH mysql_native_password` part is to overcome "Client does not support authentication protocol requested by server" when connecting from [Node.js](node-js.md).

List users:
```
sudo mysql -e 'SELECT * FROM mysql.user'
```

View permissions for each user on each DB: [https://serverfault.com/questions/263868/how-to-know-all-the-users-that-can-access-a-database-mysql](https://serverfault.com/questions/263868/how-to-know-all-the-users-that-can-access-a-database-mysql)
```
sudo mysql -e 'SELECT * FROM mysql.db'
```

List databases:
```
sudo mysql -e 'SHOW DATABASES'
```

Create database:
```
sudo mysql -e 'CREATE DATABASE mydb0'
```

Destroy database:
```
sudo mysql -e 'DROP DATABASE mydb0'
```

Show tables in database:
```
sudo mysql -e 'SHOW TABLES' mydb0
```
or:
```
sudo mysql -e 'SHOW TABLES FROM mydb0'
```

#### mysqldump

↑ **Parent:** [MySQL](#mysql)

[https://dev.mysql.com/doc/refman/8.0/en/mysqldump.html](https://dev.mysql.com/doc/refman/8.0/en/mysqldump.html)

##### mysqldump to CSV

↑ **Parent:** [mysqldump](#mysqldump)

Related: [https://stackoverflow.com/questions/32026398/transform-sql-insert-script-into-csv-format](https://stackoverflow.com/questions/32026398/transform-sql-insert-script-into-csv-format)

#### MariaDB

↑ **Parent:** [MySQL](#mysql)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/MariaDB)

Dude's a legend. Sells company for a few million. Then forks the open source project next year. Love it.

### PostgreSQL

↑ **Parent:** [SQL implementation](#sql-implementation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/PostgreSQL)

PostgreSQL feels good.

Its feature set is insanely large! Just look at stuff like: [https://stackoverflow.com/questions/1986491/sql-split-string-by-space-into-table-in-postgresql/1993058#1993058](https://stackoverflow.com/questions/1986491/sql-split-string-by-space-into-table-in-postgresql/1993058#1993058)

Had a look at the source tree, and also felt good.

If [Oracle](software.md#oracle-corporation) is the [Microsoft](microsoft.md) of database, Postgres is the [Linux](systems-programming.md#linux), and [MySQL](#mysql) (or more precisely [MariaDB](#mariadb)) is the [FreeBSD](systems-programming.md#freebsd) (i.e. the one that got delayed by legal issues). Except that their [software licenses](law.md#software-license) were accidentally swapped.

The only problem with Postgres is its name. PostgreSQL is so unpronounceable and so untypeable that you should just call it "Postgres" like everyone else.

#### PostgreSQL getting started

↑ **Parent:** [PostgreSQL](#postgresql)

On Ubuntu 20.10 PostgreSQL 12.6, login with `psql` on my default username without [sudo](software.md#sudo) fails with: [https://stackoverflow.com/questions/11919391/postgresql-error-fatal-role-username-does-not-exist](https://stackoverflow.com/questions/11919391/postgresql-error-fatal-role-username-does-not-exist)

This is the one that worked on [Ubuntu 21.04](systems-programming.md#ubuntu-21-04): [https://stackoverflow.com/questions/11919391/postgresql-error-fatal-role-username-does-not-exist/38444152#38444152](https://stackoverflow.com/questions/11919391/postgresql-error-fatal-role-username-does-not-exist/38444152#38444152)
```
sudo -u postgres createuser -s $(whoami)
createdb $(whoami)
```
Explanation:
- `sudo -u postgres` uses the `postgres` user via [peer authentication](#peer-authentication)
- `-s` in `createuser -s`: make it a superuser
- `createdb`: TODO why do we have to create a table with the same name as the user? Otherwise login fails.

You can now run `psql` without any password. This works without password due to peer authentication:
```
sudo cat /etc/postgresql/12/main/pg_hba.conf
```
shows that peer authentication is available to all users apparently:
```
local   all             postgres                                peer

# TYPE  DATABASE        USER            ADDRESS                 METHOD

# "local" is for Unix domain socket connections only
local   all             all                                     peer
```

List users:
```
psql -c '\du'
```
output:
```
                                    List of roles
  Role name  |                         Attributes                         | Member of
-------------+------------------------------------------------------------+-----------
 ciro        | Superuser, Create role, Create DB                          | {}
 owning_user |                                                            | {}
 postgres    | Superuser, Create role, Create DB, Replication, Bypass RLS | {}
```

Delete user later on:
```
psql -c 'DROP USER username;'
```

Create a database:
```
createdb testdb0
```

Help toplevel:
```
help
```

Get help for Postgres commands such as `\h` and so on:
```
\?
```

List supported SQL commands:
```
\h
```

Show syntax for one type of command:
```
\h SELECT
```

List all databases:
```
psql -c '\l'
```
which shows:
```
    Name     |  Owner   | Encoding |   Collate   |    Ctype    |   Access privileges
-------------+----------+----------+-------------+-------------+-----------------------
 ciro        | postgres | UTF8     | en_GB.UTF-8 | en_GB.UTF-8 |
 postgres    | postgres | UTF8     | en_GB.UTF-8 | en_GB.UTF-8 |
 template0   | postgres | UTF8     | en_GB.UTF-8 | en_GB.UTF-8 | =c/postgres          +
             |          |          |             |             | postgres=CTc/postgres
 template1   | postgres | UTF8     | en_GB.UTF-8 | en_GB.UTF-8 | =c/postgres          +
             |          |          |             |             | postgres=CTc/postgres
 testdb0     | postgres | UTF8     | en_GB.UTF-8 | en_GB.UTF-8 |
(6 rows)
```

Delete a database:
```
psql -c 'DROP DATABASE "testdb0";'
```

If you didn't give a database from the command line e.g.:
```
psql
```
you can do that afterwards with:
```
\c testdb0
```

Let's create a table and test that it is working:
```
psql testdb0 -c 'CREATE TABLE table0 (int0 INT, char0 CHAR(16));'
```

List tables, no special tables:
```
psql testdb0 -c '\dt'
```
gives:
```
        List of relations
 Schema |  Name  | Type  | Owner
--------+--------+-------+-------
 public | table0 | table | ciro
(1 row)
```

View table schema: [https://stackoverflow.com/questions/109325/postgresql-describe-table](https://stackoverflow.com/questions/109325/postgresql-describe-table)
```
psql testdb0 -c '\d+ table0'
```
output:
```
                                      Table "public.table0"
 Column |     Type      | Collation | Nullable | Default | Storage  | Stats target | Description
--------+---------------+-----------+----------+---------+----------+--------------+-------------
 int0   | integer       |           |          |         | plain    |              |
 char0  | character(16) |           |          |         | extended |              |
```

Insert some data into it and get the data out:
```
psql testdb0 -c "INSERT INTO table0 (int0, char0) VALUES (2, 'two'), (3, 'three'), (5, 'five'), (7, 'seven');"
psql testdb0 -c 'SELECT * FROM table0;'
```
output:
```
 int0 |      char0
------+------------------
    2 | two
    3 | three
    5 | five
    7 | seven
(4 rows)
```

Delete the table:
```
psql testdb0 -c 'DROP TABLE table0;'
```

##### PostgreSQL HOWTO

↑ **Parent:** [PostgreSQL getting started](#postgresql-getting-started)

- output one column per line: [https://stackoverflow.com/questions/9604723/alternate-output-format-for-psql-showing-one-column-per-line-with-column-name](https://stackoverflow.com/questions/9604723/alternate-output-format-for-psql-showing-one-column-per-line-with-column-name)
- PostgreSQL does not automatically index foreign keys! [https://stackoverflow.com/questions/970562/postgres-and-indexes-on-foreign-keys-and-primary-keys](https://stackoverflow.com/questions/970562/postgres-and-indexes-on-foreign-keys-and-primary-keys)

###### PostgreSQL create test data

↑ **Parent:** [PostgreSQL HOWTO](#postgresql-howto)

- [https://stackoverflow.com/questions/3371503/sql-populate-table-with-random-data](https://stackoverflow.com/questions/3371503/sql-populate-table-with-random-data)
- [https://stackoverflow.com/questions/24841142/how-can-i-generate-big-data-sample-for-postgresql-using-generate-series-and-rand](https://stackoverflow.com/questions/24841142/how-can-i-generate-big-data-sample-for-postgresql-using-generate-series-and-rand)

###### Generate random text in PostgreSQL

↑ **Parent:** [PostgreSQL create test data](#postgresql-create-test-data)

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

###### PostgreSQL full-text search

↑ **Parent:** [PostgreSQL HOWTO](#postgresql-howto)  
🏷️ **Tags:** [Full-text search](software.md#full-text-search)

This section was tested on [Ubuntu 24.10](systems-programming.md#ubuntu-24-10), [PostgreSQL](#postgresql) 16.6.

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

We aimed to create a test table of size around 10 GB, as in practice it is around that order of size that index speedups start to become very obvious on a [SSD](computer-hardware.md#solid-state-storage)-based system.

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

Now let's create the index. First we create a [generated column](#generated-column) that splits the strings with [`to_tsvector`](#to-tsvector), and then we index that split column:
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

The next thing that we need to understand is how [`to_tsvector`](#to-tsvector) [tokenizes](https://ourbigbook.com/go/topic/tokenizes) strings for the `english` language. For example running:
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
On [Ubuntu 24.10](systems-programming.md#ubuntu-24-10), the list contains major world languages, plus the special `simple` configuration such that:
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

#### Create a test user in PostgreSQL

↑ **Parent:** [PostgreSQL](#postgresql)

In order to create a test user with password instead of [peer authentication](#peer-authentication), let's create test user:
```
createuser -P user0
createdb user0
```
`-P` makes it prompt for the users password.

Alternatively, to create the password non-interactively [https://stackoverflow.com/questions/42419559/postgres-createuser-with-password-from-terminal](https://stackoverflow.com/questions/42419559/postgres-createuser-with-password-from-terminal):
```
psql -c "create role NewRole with login password 'secret'"
```
Can't find a way using the `createuser` helper.

We can then login with that password with:
```
psql -U user0 -h localhost
```
which asks for the password we've just set, because the `-h` option turns off peer authentication, and turns off password authentication.

The password can be given non-interactively as shown at [https://stackoverflow.com/questions/6405127/how-do-i-specify-a-password-to-psql-non-interactively](https://stackoverflow.com/questions/6405127/how-do-i-specify-a-password-to-psql-non-interactively) with the `PGPASSWORD` [environment variable](systems-programming.md#environment-variable):
```
PGPASSWORD=a psql -U user0 -h localhost
```

Now let's create a test database which `user0` can access with an existing superuser account:
```
createdb user0db0
psql -c 'GRANT ALL PRIVILEGES ON DATABASE user0db0 TO user0'
```

We can check this permission with:
```
psql -c '\l'
```
which now contains:
```
                                  List of databases
   Name    |  Owner   | Encoding |   Collate   |    Ctype    |   Access privileges
-----------+----------+----------+-------------+-------------+-----------------------
 user0db0  | ciro     | UTF8     | en_GB.UTF-8 | en_GB.UTF-8 | =Tc/ciro             +
           |          |          |             |             | ciro=CTc/ciro        +
           |          |          |             |             | user0=CTc/ciro
```
The permission letters are explained at:
- [https://www.postgresql.org/docs/13/ddl-priv.html](https://www.postgresql.org/docs/13/ddl-priv.html)
- [https://stackoverflow.com/questions/25691037/postgresql-permissions-explained/25691587](https://stackoverflow.com/questions/25691037/postgresql-permissions-explained/25691587)

`user0` can now do the usual table operations on that table:
```
PGPASSWORD=a psql -U user0 -h localhost user0db0 -c 'CREATE TABLE table0 (int0 INT, char0 CHAR(16));'
PGPASSWORD=a psql -U user0 -h localhost user0db0 -c "INSERT INTO table0 (int0, char0) VALUES (2, 'two'), (3, 'three'), (5, 'five'), (7, 'seven');"
PGPASSWORD=a psql -U user0 -h localhost user0db0 -c 'SELECT * FROM table0;'
```

#### Peer authentication

↑ **Parent:** [PostgreSQL](#postgresql)

[https://www.postgresql.org/docs/13/auth-peer.html](https://www.postgresql.org/docs/13/auth-peer.html)

Uses the name of the current [Linux](systems-programming.md#linux) user to login without a [password](software.md#password).

#### PostgreSQL logging

↑ **Parent:** [PostgreSQL](#postgresql)

[https://stackoverflow.com/questions/722221/how-to-log-postgresql-queries](https://stackoverflow.com/questions/722221/how-to-log-postgresql-queries)

[Ubuntu 21.10](systems-programming.md#ubuntu-21-10) has a certain default level of logging by default to:
```
/var/log/postgresql/postgresql-13-main.log
```
but it does not log everything, only/mostly errors it seems.

Setting:
```
log_statement = 'all'
```
under:
```
/etc/postgresql/13/main/postgresql.conf
```
and then restarting the server:
```
sudo service restart postgresql
```
just works.

Realtime monitoring for long queries instead: [https://stackoverflow.com/questions/8597516/app-to-monitor-postgresql-queries-in-real-time](https://stackoverflow.com/questions/8597516/app-to-monitor-postgresql-queries-in-real-time)

#### PostgreSQL serialization failure

↑ **Parent:** [PostgreSQL](#postgresql)

When using [SQL REPEATABLE READ isolation level](#sql-repeatable-read-isolation-level) and [SQL SERIALIZABLE isolation level](#sql-serializable-isolation-level), concurrent transactions may fail with a serialization failure, and then you might need to retry them. You server code or your ORM must always account for that.

A good way to explore when it happens is to use the example

Related questions:
- [https://stackoverflow.com/questions/7705273/what-are-the-conditions-for-encountering-a-serialization-failure](https://stackoverflow.com/questions/7705273/what-are-the-conditions-for-encountering-a-serialization-failure)
- [https://stackoverflow.com/questions/59351109/error-could-not-serialize-access-due-to-concurrent-update](https://stackoverflow.com/questions/59351109/error-could-not-serialize-access-due-to-concurrent-update)
- [https://stackoverflow.com/questions/50797097/postgres-could-not-serialize-access-due-to-concurrent-update/51932824](https://stackoverflow.com/questions/50797097/postgres-could-not-serialize-access-due-to-concurrent-update/51932824)

#### PostgreSQL function

↑ **Parent:** [PostgreSQL](#postgresql)  
🏷️ **Tags:** [SQL function](#sql-function)

[https://www.postgresql.org/docs/17/functions-srf.html](https://www.postgresql.org/docs/17/functions-srf.html)

<h5 id="postgresql-generate-series">PostgreSQL <code>generate_series</code></h5>

↑ **Parent:** [PostgreSQL function](#postgresql-function)

[https://www.postgresql.org/docs/17/functions-srf.html](https://www.postgresql.org/docs/17/functions-srf.html)

Pattern you always want to generate [Generate random text in PostgreSQL](#generate-random-text-in-postgresql):
```
CREATE TABLE "mytable" ("i" INTEGER, "j" INTEGER);
INSERT INTO "mytable" SELECT i, i*2 FROM generate_series(1, 10) as s(i);
```

<h5 id="to-tsvector"><code>to_tsvector</code></h5>

↑ **Parent:** [PostgreSQL function](#postgresql-function)

[https://www.postgresql.org/docs/17/textsearch-controls.html](https://www.postgresql.org/docs/17/textsearch-controls.html)

### Microsoft SQL Server

↑ **Parent:** [SQL implementation](#sql-implementation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Microsoft_SQL_Server)

#### Transact-SQL

↑ **Parent:** [Microsoft SQL Server](#microsoft-sql-server)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Transact-SQL)

### Oracle Database

↑ **Parent:** [SQL implementation](#sql-implementation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Oracle_Database)

Often known simply as SQL Server, a terrible thing that makes it impossible to find portable SQL answers on [Google](google.md)! You just have to Google by specific [SQL implementation](#sql-implementation) unfortunately to find anything about the open source ones.

### SQLite

↑ **Parent:** [SQL implementation](#sql-implementation)  
🏷️ **Tags:** [Good](cirism.md#good)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/SQLite)

The minimalism, serverlessness/lack of temporary caches/lack of permission management, Hipp's religious obsession with efficiency, the use of their own pure Fossil [version control](software.md#version-control)[https://sqlite.org/whynotgit.html](https://sqlite.org/whynotgit.html). Wait, scrap that last one. Pure beauty!

![](https://upload.wikimedia.org/wikipedia/commons/thumb/3/38/SQLite370.svg/500px-SQLite370.svg.png)

**[Figure 1](#_275)** [Source](https://commons.wikimedia.org/wiki/File:SQLite370.svg.png).

Official [Git](software.md#git) mirror: [https://github.com/sqlite/sqlite](https://github.com/sqlite/sqlite)

Create a table
```
sqlite3 db.sqlite3 "
CREATE TABLE 'IntegerNames' (int0 INT, char0 CHAR(16));
INSERT INTO 'IntegerNames' (int0, char0) VALUES (2, 'two'), (3, 'three'), (5, 'five'), (7, 'seven');
"
```

List tables:
```
sqlite3 db.sqlite3 '.tables'
```
output:
```
IntegerNames
```

Show schema of a table:
```
sqlite3 db.sqlite3 '.schema IntegerNames'
```
outputs the query that would generate that table:
```
CREATE TABLE IF NOT EXISTS 'IntegerNames' (int0 INT, char0 CHAR(16));
```

Show all data in a table:
```
sqlite3 db.sqlite3 'SELECT * FROM IntegerNames'
```
output:
```
2|two
3|three
5|five
7|seven
```

#### [SQLite](#sqlite) import [CSV](computer.md#comma-separated-values)

↑ **Parent:** [SQLite](#sqlite)

##### [SQLite](#sqlite) import [CSV](computer.md#comma-separated-values) from [stdin](systems-programming.md#standard-input)

↑ **Parent:** [SQLite import CSV](#sqlite-import-csv)

#### [SQLite](#sqlite) import [JSON](computer.md#json)

↑ **Parent:** [SQLite](#sqlite)

- [https://stackoverflow.com/questions/46407770/how-to-convert-a-json-file-to-an-sqlite-database](https://stackoverflow.com/questions/46407770/how-to-convert-a-json-file-to-an-sqlite-database)

#### SQLite benchmark

↑ **Parent:** [SQLite](#sqlite)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/SQLite_benchmark)

Python sequence test data generation: [https://stackoverflow.com/questions/18219779/bulk-insert-huge-data-into-sqlite-using-python/76659706#76659706](https://stackoverflow.com/questions/18219779/bulk-insert-huge-data-into-sqlite-using-python/76659706#76659706)

#### [SQLite](#sqlite) C extension

↑ **Parent:** [SQLite](#sqlite)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/SQLite_C_extension)

Example: [sqlite/ip.c](sqlite/ip.c), adapted from [https://www.sqlite.org/loadext.html](https://www.sqlite.org/loadext.html), also mentioned explained at: [https://stackoverflow.com/questions/7638238/sqlite-ip-address-storage/76520885#76520885](https://stackoverflow.com/questions/7638238/sqlite-ip-address-storage/76520885#76520885).

Sample usage in the test program: [sqlite/test.sh](sqlite/test.sh).

Docs: [https://www.sqlite.org/loadext.html](https://www.sqlite.org/loadext.html)

#### [SQLite](#sqlite) isolation levels

↑ **Parent:** [SQLite](#sqlite)  
🏷️ **Tags:** [SQL transaction isolation level](#sql-transaction-isolation-level)

[https://www.sqlite.org/pragma.html#pragma_read_uncommitted](https://www.sqlite.org/pragma.html#pragma_read_uncommitted) mentions:

> The default isolation level for SQLite is SERIALIZABLE

It does not appear possible to achieve the other two levels besides SERIALIZABLE and READ UNCOMMITED

[https://www.sqlite.org/isolation.html](https://www.sqlite.org/isolation.html)

<h4 id="node-js-sqlite-bindings"><a href="node-js.html">Node.js</a> <a href="#sqlite">SQLite</a> bindings</h4>

↑ **Parent:** [SQLite](#sqlite)

<h5 id="sqlite3-node-js-package"><code>sqlite3</code> Node.js package</h5>

↑ **Parent:** [Node.js SQLite bindings](#node-js-sqlite-bindings)

- [https://github.com/mapbox/node-sqlite3](https://github.com/mapbox/node-sqlite3)
- [https://www.npmjs.com/package/sqlite3](https://www.npmjs.com/package/sqlite3)

Includes its own copy of sqlite3, you don't use the system one, which is good to ensure compatibility. The version is shown at: [https://github.com/mapbox/node-sqlite3/blob/918052b538b0effe6c4a44c74a16b2749c08a0d2/deps/common-sqlite.gypi#L3](https://github.com/mapbox/node-sqlite3/blob/918052b538b0effe6c4a44c74a16b2749c08a0d2/deps/common-sqlite.gypi#L3) [SQLite](#sqlite) source is tracked compressed in-tree: [https://github.com/mapbox/node-sqlite3/blob/918052b538b0effe6c4a44c74a16b2749c08a0d2/deps/sqlite-autoconf-3360000.tar.gz](https://github.com/mapbox/node-sqlite3/blob/918052b538b0effe6c4a44c74a16b2749c08a0d2/deps/sqlite-autoconf-3360000.tar.gz) horrendous. This explains why it takes forever to clone that repository. People who don't believe in git submodules, there's even an official Git mirror at: [https://github.com/sqlite/sqlite](https://github.com/sqlite/sqlite)

It appears to spawn its own [threads](computer.md#thread-computing) via its [C](programming-language.md#c-programming-language) extension (since [JavaScript is single threaded](programming-language.md#javascript-is-single-threaded) and and [SQLite](#sqlite) is not [server](computer.md#server-computing)-based), which allows for parallel queries using multiple threads: [https://github.com/mapbox/node-sqlite3/blob/v5.0.2/src/threading.h](https://github.com/mapbox/node-sqlite3/blob/v5.0.2/src/threading.h)

Hello world example: [nodejs/node-sqlite3/index.js](nodejs/node-sqlite3/index.js).

As of 2021, this had slumped back a bit, as maintainers got tired. Unmerged pull requests started piling more, and [`better-sqlite3` Node.js package](#better-sqlite3-node-js-package) started pulling ahead a little.
- [https://github.com/mapbox/node-sqlite3/issues/1381](https://github.com/mapbox/node-sqlite3/issues/1381) `FATAL ERROR: Error::ThrowAsJavaScriptException napi_throw` with [Node.js `worker_threads`](node-js.md#node-js-worker-threads) vs [`better-sqlite3` Node.js package](#better-sqlite3-node-js-package) [https://github.com/JoshuaWise/better-sqlite3/issues/237](https://github.com/JoshuaWise/better-sqlite3/issues/237)

<h5 id="better-sqlite3-node-js-package"><code>better-sqlite3</code> Node.js package</h5>

↑ **Parent:** [Node.js SQLite bindings](#node-js-sqlite-bindings)

As claimed on their README, their operation truly appears to be 10x faster than the node-sqlite package!! It is insane!! How can that other package still exist at all?

The only big problem was the lack of [ORM](software.md#object-relational-mapping), but people are looking into that by adding it to [Sequelize](sequelize.md):
- [https://github.com/JoshuaWise/better-sqlite3/issues/23](https://github.com/JoshuaWise/better-sqlite3/issues/23)
- [https://github.com/sequelize/sequelize/issues/11400](https://github.com/sequelize/sequelize/issues/11400)

## SQL function

↑ **Parent:** [SQL](sql.md)

### SQL set returning function

↑ **Parent:** [SQL function](#sql-function)

[PostgreSQL](#postgresql): [https://www.postgresql.org/docs/current/functions-srf.html](https://www.postgresql.org/docs/current/functions-srf.html)

<h4 id="sql-genenerate-series">SQL <code>genenerate_series</code></h4>

↑ **Parent:** [SQL set returning function](#sql-set-returning-function)

### SQL aggregate function

↑ **Parent:** [SQL function](#sql-function)

#### SQL `COUNT` function

↑ **Parent:** [SQL aggregate function](#sql-aggregate-function)

Have a look at some interesting examples under [nodejs/sequelize/raw/many_to_many.js](nodejs/sequelize/raw/many_to_many.js).

## SQL keyword

↑ **Parent:** [SQL](sql.md)

### SQL CASCADE

↑ **Parent:** [SQL keyword](#sql-keyword)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/SQL_CASCADE)

[https://stackoverflow.com/questions/59297/when-why-to-use-cascading-in-sql-server](https://stackoverflow.com/questions/59297/when-why-to-use-cascading-in-sql-server)

### DELETE (SQL)

↑ **Parent:** [SQL keyword](#sql-keyword)

#### Delete all duplicate rows in SQL

↑ **Parent:** [DELETE (SQL)](#delete-sql)

- [SQLite](#sqlite) with `rowid`: [https://stackoverflow.com/questions/8190541/deleting-duplicate-rows-from-sqlite-database](https://stackoverflow.com/questions/8190541/deleting-duplicate-rows-from-sqlite-database)
  - [PostgreSQL](#postgresql) is `ctid`: [https://stackoverflow.com/questions/14626481/rowid-equivalent-in-postgres-9-2](https://stackoverflow.com/questions/14626481/rowid-equivalent-in-postgres-9-2)
- [SQL Server](#oracle-database) has crazy "CTEs" change backing table extension: [https://stackoverflow.com/questions/18390574/how-to-delete-duplicate-rows-in-sql-server](https://stackoverflow.com/questions/18390574/how-to-delete-duplicate-rows-in-sql-server)

### GROUP BY (SQL)

↑ **Parent:** [SQL keyword](#sql-keyword)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Group_by_(SQL))

#### HAVING (SQL)

↑ **Parent:** [GROUP BY (SQL)](#group-by-sql)

##### HAVING vs WHERE

↑ **Parent:** [HAVING (SQL)](#having-sql)

- [https://www.reddit.com/r/SQL/comments/o3jeis/having_and_where_difference/](https://www.reddit.com/r/SQL/comments/o3jeis/having_and_where_difference/)
- [https://stackoverflow.com/questions/9253244/sql-having-vs-where](https://stackoverflow.com/questions/9253244/sql-having-vs-where)

### INSERT (SQL)

↑ **Parent:** [SQL keyword](#sql-keyword)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Insert_(SQL))

#### Upsert

↑ **Parent:** [INSERT (SQL)](#insert-sql)

`UPSERT` is extremely handy, and reduces the number of find, check on server, update loops. But `RETURNING` is a fundamental part of that (to get the updated/existing) ID. Can't believe SQL hasn't standardized it yet as of 2022. But both [SQLite](#sqlite) and [Postgres](#postgresql) support it with similar syntax thankfully.

[nodejs/sequelize/raw/upsert.js](nodejs/sequelize/raw/upsert.js)

- [https://www.postgresql.org/docs/14/sql-insert.html#SQL-ON-CONFLICT](https://www.postgresql.org/docs/14/sql-insert.html#SQL-ON-CONFLICT)
- [https://www.sqlite.org/lang_returning.html](https://www.sqlite.org/lang_returning.html)

##### Upsert with `NOT NULL` column

↑ **Parent:** [Upsert](#upsert)

Attempt at [nodejs/sequelize/raw/upsert.js](nodejs/sequelize/raw/upsert.js):
- [https://stackoverflow.com/questions/48816629/on-conflict-do-nothing-in-postgres-with-a-not-null-constraint](https://stackoverflow.com/questions/48816629/on-conflict-do-nothing-in-postgres-with-a-not-null-constraint) OP unable to provide a minimal exampe, but it is likely the problem
- [https://dba.stackexchange.com/questions/292428/postgresql-upsert-issue-with-not-null-columns](https://dba.stackexchange.com/questions/292428/postgresql-upsert-issue-with-not-null-columns)

Related on more complex constraints:
- [https://dba.stackexchange.com/questions/175182/on-conflict-on-two-columns-where-one-can-be-null](https://dba.stackexchange.com/questions/175182/on-conflict-on-two-columns-where-one-can-be-null)
- [https://dba.stackexchange.com/questions/292428/postgresql-upsert-issue-with-not-null-columns](https://dba.stackexchange.com/questions/292428/postgresql-upsert-issue-with-not-null-columns)

### JOIN (SQL)

↑ **Parent:** [SQL keyword](#sql-keyword)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Join_(SQL))

#### SQL prefix column names with the table they came from

↑ **Parent:** [JOIN (SQL)](#join-sql)

It is mind blowing that this is not possible... the only way to avoid ambiguity in JOINs with column name conflicts is to give aliases to each column...

- [https://stackoverflow.com/questions/329931/sql-select-join-is-it-possible-to-prefix-all-columns-as-prefix](https://stackoverflow.com/questions/329931/sql-select-join-is-it-possible-to-prefix-all-columns-as-prefix)
- [https://stackoverflow.com/questions/13153344/in-a-join-how-to-prefix-all-column-names-with-the-table-it-came-from](https://stackoverflow.com/questions/13153344/in-a-join-how-to-prefix-all-column-names-with-the-table-it-came-from)

#### INNER JOIN

↑ **Parent:** [JOIN (SQL)](#join-sql)

#### OUTER JOIN

↑ **Parent:** [JOIN (SQL)](#join-sql)

### LIKE (SQL)

↑ **Parent:** [SQL keyword](#sql-keyword)

### SELECT (SQL)

↑ **Parent:** [SQL keyword](#sql-keyword)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Select_(SQL))

#### SELECT FOR UPDATE

↑ **Parent:** [SELECT (SQL)](#select-sql)

An example where `SELECT FOR UPDATE` is a good solution to an use case can be seen at: [nodejs/sequelize/raw/parallel_select_and_update.js](#_file/nodejs/sequelize/raw/parallel_select_and_update.js).

`SELECT FOR UPDATE` vs/together with the [SQL transaction isolation level](#sql-transaction-isolation-level) is commented at: [https://stackoverflow.com/questions/10935850/when-to-use-select-for-update](https://stackoverflow.com/questions/10935850/when-to-use-select-for-update).

### SQL stored procedure

↑ **Parent:** [SQL keyword](#sql-keyword)  
🏷️ **Tags:** [Stored procedure](software.md#stored-procedure)

#### SQL FUNCTION keyword

↑ **Parent:** [SQL stored procedure](#sql-stored-procedure)

#### SQL PROCEDURE

↑ **Parent:** [SQL stored procedure](#sql-stored-procedure)

### SQL TRIGGER

↑ **Parent:** [SQL keyword](#sql-keyword)  
🏷️ **Tags:** [Database trigger](software.md#database-trigger)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/SQL_TRIGGER)

[SQL](sql.md)'s implementation of [database triggers](software.md#database-trigger).

This feature is really cool, as it allows you to keep caches up to date!

In particular, everything that happens in a trigger happens as if it were in a transaction. This way, you can do less explicit transactions when you use triggers. It is a bit like the advantages of [SQL CASCADE](#sql-cascade).

[DBMS](software.md#database-management-system):
- [PostgreSQL](#postgresql):
  - [https://stackoverflow.com/questions/24870416/counter-cache-column-in-postgresql](https://stackoverflow.com/questions/24870416/counter-cache-column-in-postgresql)
- [SQLite](#sqlite)
  - [https://stackoverflow.com/questions/35255304/sqlite-create-trigger-for-insert-or-update](https://stackoverflow.com/questions/35255304/sqlite-create-trigger-for-insert-or-update)

[ORM](software.md#object-relational-mapping):
- [Sequelize](sequelize.md): [SQL TRIGGER in Sequelize](sequelize.md#sql-trigger-in-sequelize)

### ISO SQL TRIGGER syntax

↑ **Parent:** [SQL keyword](#sql-keyword)  
🏷️ **Tags:** [Database trigger](software.md#database-trigger), [SQL standard](#sql-standard)

TODO what is the standard compliant syntax?

[PostgreSQL](#postgresql) requires you to define a [SQL stored procedure](#sql-stored-procedure): [https://stackoverflow.com/questions/28149494/is-it-possible-to-create-trigger-without-execute-procedure-in-postgresql](https://stackoverflow.com/questions/28149494/is-it-possible-to-create-trigger-without-execute-procedure-in-postgresql) Their syntax may be standard compliant, not sure about the `EXECUTE` part. Their docs: [https://www.postgresql.org/docs/current/sql-createtrigger.html](https://www.postgresql.org/docs/current/sql-createtrigger.html)

[SQLite](#sqlite) does not support [SQL stored procedures](#sql-stored-procedure) at all, so maybe that's why they can't be standard compliant here: [https://stackoverflow.com/questions/3335162/creating-stored-procedure-in-sqlite](https://stackoverflow.com/questions/3335162/creating-stored-procedure-in-sqlite)

[SQL:1999](#sql-1999) 11.38 covers "Trigger definition". The [Abstract syntax tree](computer-science.md#abstract-syntax-tree) starts with the `CREATE TRIGGER` and ends in:
```
<triggered SQL statement> ::=
  <SQL procedure statement>
```

This is defined at 13.5 "SQL procedure statement", but that is humongous and I'm not sure what it is at all.

<h4 id="_file/nodejs/sequelize/raw/trigger_count.js">nodejs/sequelize/raw/trigger_count.js</h4>

↑ **Parent:** [ISO SQL TRIGGER syntax](#iso-sql-trigger-syntax)

In this example we cache track the number of posts per user on a cache column.

### UNION (SQL)

↑ **Parent:** [SQL keyword](#sql-keyword)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Set_operations_(SQL)#UNION_operator)

Basic example tested on [SQLite](#sqlite) 3.40.1, [Ubuntu 23.04](systems-programming.md#ubuntu-23-04):
```
sqlite3 :memory: 'select 1 union select 2'
```
output:
```
1
2
```

Two columns two rows:
```
sqlite3 :memory: <<EOF
select * from (values (1, 2), (2, 3))
union
select * from (values (2, 3), (3, 4))
EOF
```
output:
```
1|2
2|3
3|4
```

Note how duplicates are removed, to keep them we `UNION ALL` instead:
```
sqlite3 :memory: <<EOF
select * from (values (1, 2), (2, 3))
union all
select * from (values (2, 3), (3, 4))
EOF
```
output:
```
1|2
2|3
2|3
3|4
```

### UPDATE (SQL)

↑ **Parent:** [SQL keyword](#sql-keyword)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Update_(SQL))

#### Update multiple rows with different values in a single SQL query

↑ **Parent:** [UPDATE (SQL)](#update-sql)

This happens when you calculate a bunch of values on your program, and then want to save the to SQL.

[Upsert](#upsert) is an option, but it fails if you have a `NOT NULL` column: [Upsert with `NOT NULL` column](#upsert-with-not-null-column)

Bibliography:
- [https://stackoverflow.com/questions/11563869/update-multiple-rows-with-different-values-in-a-single-sql-query](https://stackoverflow.com/questions/11563869/update-multiple-rows-with-different-values-in-a-single-sql-query)
- [https://dba.stackexchange.com/questions/69269/updating-multiple-rows-with-different-values-in-one-query](https://dba.stackexchange.com/questions/69269/updating-multiple-rows-with-different-values-in-one-query)

#### UPDATE with JOIN (SQL)

↑ **Parent:** [UPDATE (SQL)](#update-sql)

Dumping examples under [nodejs/sequelize/raw/many_to_many.js](nodejs/sequelize/raw/many_to_many.js).

Not possible without subqueries in the standard syntax, a huge shame: [https://stackoverflow.com/questions/1293330/how-can-i-do-an-update-statement-with-join-in-sql-server](https://stackoverflow.com/questions/1293330/how-can-i-do-an-update-statement-with-join-in-sql-server)

The `UPDATE` + `FROM` extension exists in a few [DBMS](software.md#database-management-system)s:
- [PostgreSQL](#postgresql): [https://stackoverflow.com/questions/7869592/how-to-do-an-update-join-in-postgresql](https://stackoverflow.com/questions/7869592/how-to-do-an-update-join-in-postgresql)
- [SQLite](#sqlite): [https://stackoverflow.com/questions/19270259/update-with-join-in-sqlite/69831549#69831549](https://stackoverflow.com/questions/19270259/update-with-join-in-sqlite/69831549#69831549)

[ORM](software.md#object-relational-mapping):
- [Sequelize](sequelize.md): [UPDATE with JOIN in Sequelize](sequelize.md#update-with-join-in-sequelize)

##### DELETE with JOIN (SQL)

↑ **Parent:** [UPDATE with JOIN (SQL)](#update-with-join-sql)  
🏷️ **Tags:** [DELETE (SQL)](#delete-sql)

Demo under: [nodejs/sequelize/raw/many_to_many.js](nodejs/sequelize/raw/many_to_many.js).

NO way in the [SQL standard](#sql-standard) apparently, but you'd hope that implementation status would be similar to [UPDATE with JOIN](#update-with-join-sql), but not even!
- [PostgreSQL](#postgresql): possible with `DELETE FROM USING`: [https://stackoverflow.com/questions/11753904/postgresql-delete-with-inner-join](https://stackoverflow.com/questions/11753904/postgresql-delete-with-inner-join)
- [SQLite](#sqlite): not possible without subqueries as of 3.35 far: [https://stackoverflow.com/questions/24511153/how-delete-table-inner-join-with-other-table-in-sqlite](https://stackoverflow.com/questions/24511153/how-delete-table-inner-join-with-other-table-in-sqlite), Does not appear to have any relevant features at: [https://www.sqlite.org/lang_delete.html](https://www.sqlite.org/lang_delete.html)

[ORM](software.md#object-relational-mapping)
- [Sequelize](sequelize.md): no support of course: [https://stackoverflow.com/questions/40890131/sequelize-destroy-record-with-join](https://stackoverflow.com/questions/40890131/sequelize-destroy-record-with-join)

## SQL standard

↑ **Parent:** [SQL](sql.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/SQL_standard)

A quick look at [PostgreSQL](#postgresql)'s compliance notes: [https://www.postgresql.org/docs/13/features.html](https://www.postgresql.org/docs/13/features.html) shows the complete utter mess that this standard is. Multiple compliance levels that no one fully implements and optional features everywhere.

### SQL standard version

↑ **Parent:** [SQL standard](#sql-standard)

<h4 id="sql-1999">SQL:1999</h4>

↑ **Parent:** [SQL standard version](#sql-standard-version)

## SQL application

↑ **Parent:** [SQL](sql.md)

### SQL histogram

↑ **Parent:** [SQL application](#sql-application)

OK, there's a billion questions:
- [SQL Server](#oracle-database)
  - [https://stackoverflow.com/questions/485409/generating-a-histogram-from-column-values-in-a-database](https://stackoverflow.com/questions/485409/generating-a-histogram-from-column-values-in-a-database) OP did not know the difference between count and histogram :-) But it's the number one Google result.
  - [https://stackoverflow.com/questions/19103991/create-range-bins-from-sql-server-table-for-histograms](https://stackoverflow.com/questions/19103991/create-range-bins-from-sql-server-table-for-histograms) has a minor extra group by twist, but otherwise fine
  - [https://stackoverflow.com/questions/16268441/generate-histogram-in-sql-server](https://stackoverflow.com/questions/16268441/generate-histogram-in-sql-server)
- [SQLite](#sqlite)
  - [https://stackoverflow.com/questions/67514208/how-to-optimise-creating-histogram-bins-in-sqlite](https://stackoverflow.com/questions/67514208/how-to-optimise-creating-histogram-bins-in-sqlite) perf only, benchmarking would be needed. [SQLite](#sqlite).
  - [https://stackoverflow.com/questions/32155449/create-a-histogram-with-a-dynamic-number-of-partitions-in-sqlite](https://stackoverflow.com/questions/32155449/create-a-histogram-with-a-dynamic-number-of-partitions-in-sqlite) variable bin size, same number of entries per bin
  - [https://stackoverflow.com/questions/60348109/histogram-for-time-periods-using-sqlite-regular-buckets-1h-wide](https://stackoverflow.com/questions/60348109/histogram-for-time-periods-using-sqlite-regular-buckets-1h-wide) time
- [MySQL](#mysql): [https://stackoverflow.com/questions/1764881/getting-data-for-histogram-plot](https://stackoverflow.com/questions/1764881/getting-data-for-histogram-plot) MySQL appears to extend `ROUND` to also round by integers: `ROUND(numeric_value, -2)`, but this is not widely portable which is a shame
- [https://stackoverflow.com/questions/72367652/populating-empty-bins-in-a-histogram-generated-using-sql](https://stackoverflow.com/questions/72367652/populating-empty-bins-in-a-histogram-generated-using-sql) specifically asks about empty bins, which is amazing. [Amazon Redshift](computer-hardware.md#amazon-redshift) dialect unfortunately, but answer provided works widely, and Redshift was forked from [PostgreSQL](#postgresql), so there's hope. Those newb [open source](software.md#open-source-software) server focused projects that don't use [AGPL](law.md#affero-general-public-license)!

Let's try it on [SQLite](#sqlite) 3.40.1, [Ubuntu 23.04](systems-programming.md#ubuntu-23-04). Data setup:
```
sqlite3 tmp.sqlite 'create table t(x integer)'
sqlite3 tmp.sqlite <<EOF
insert into t values (
  0,
  2,
  2,
  3,

  5,
  6,
  6,
  8,
  9,

  17,
)
EOF
sqlite3 tmp.sqlite 'create index tx on t(x)'
```

For a bin size of 5 ignoring empty ranges we can:
```
sqlite3 tmp.sqlite <<EOF
select floor(x/5)*5 as x,
       count(*) as cnt
from t
group by 1
order by 1
EOF
```
which produces the desired:
```
0|4
5|5
15|1
```

And to consider empty ranges we can use [SQL `genenerate_series`](#sql-genenerate-series) + as per [https://stackoverflow.com/questions/72367652/populating-empty-bins-in-a-histogram-generated-using-sql](https://stackoverflow.com/questions/72367652/populating-empty-bins-in-a-histogram-generated-using-sql):
```
sqlite3 tmp.sqlite <<EOF
select x, sum(cnt) from (
  select floor(x/5)*5 as x,
         count(*) as cnt
    from t
    group by 1
  union
  select *, 0 as cnt from generate_series(0, 15, 5)
)
group by x
EOF
```
which outputs the desired:
```
0|4
5|5
10|0
15|1
```

#### SQL 2D histogram

↑ **Parent:** [SQL histogram](#sql-histogram)

Let's try it on [SQLite](#sqlite) 3.40.1, [Ubuntu 23.04](systems-programming.md#ubuntu-23-04). Data setup:
```
sqlite3 tmp.sqlite 'create table t(x integer, y integer)'
sqlite3 tmp.sqlite <<EOF
insert into t values
  (0, 0),
  (1, 1),
  (2, 2),
  (3, 3),
  (4, 4),
  (5, 5),
  (6, 6),
  (7, 7),
  (8, 8),
  (9, 9),
  (10, 10),
  (11, 11),
  (12, 12),
  (13, 13),
  (14, 14),
  (15, 15),
  (16, 16),
  (17, 17),
  (18, 18),
  (19, 19),

  (2, 18)
EOF
sqlite3 tmp.sqlite 'create index txy on t(x, y)'
```

For a bin size of 5 ignoring empty ranges we can:
```
sqlite3 tmp.sqlite <<EOF
select
  floor(x/5)*5 as x,
  floor(y/5)*5 as y,
  count(*) as cnt
from t
group by 1, 2
order by 1, 2
EOF
```
which produces the desired:
```
0|0|5
0|15|1
5|5|5
10|10|5
15|15|5
```

And to consider empty ranges we can use [SQL `genenerate_series`](#sql-genenerate-series) + as per [https://stackoverflow.com/questions/72367652/populating-empty-bins-in-a-histogram-generated-using-sql](https://stackoverflow.com/questions/72367652/populating-empty-bins-in-a-histogram-generated-using-sql):
```
sqlite3 tmp.sqlite <<EOF
select x, y, sum(cnt) from (
  select
      floor(x/5)*5 as x,
      floor(y/5)*5 as y,
      count(*) as cnt
    from t
    group by 1, 2
  union
  select *, 0 as cnt from generate_series(0, 15, 5) inner join (select * from generate_series(0, 15, 5))
)
group by x, y
EOF
```
which outputs the desired:
```
0|0|5
0|5|0
0|10|0
0|15|1
5|0|0
5|5|5
5|10|0
5|15|0
10|0|0
10|5|0
10|10|5
10|15|0
15|0|0
15|5|0
15|10|0
15|15|5
```

### SQL tree traversal

↑ **Parent:** [SQL application](#sql-application)  
🏷️ **Tags:** [Tree traversal](mathematics.md#tree-traversal)

Example: [nodejs/sequelize/raw/tree.js](nodejs/sequelize/raw/tree.js)

- Implementation agnostic
  - [https://stackoverflow.com/questions/192220/what-is-the-most-efficient-elegant-way-to-parse-a-flat-table-into-a-tree](https://stackoverflow.com/questions/192220/what-is-the-most-efficient-elegant-way-to-parse-a-flat-table-into-a-tree)
  - [https://stackoverflow.com/questions/5508985/recursive-query-for-adjacency-list-to-preorder-tree-traversal-in-sql](https://stackoverflow.com/questions/5508985/recursive-query-for-adjacency-list-to-preorder-tree-traversal-in-sql) DBMS agnostic specifically asking not to modify [adjacency list](mathematics.md#adjacency-list) data structure
- [Postgres](#postgresql)
  - [https://stackoverflow.com/questions/67848017/simple-recursive-sql-query](https://stackoverflow.com/questions/67848017/simple-recursive-sql-query)
  - [https://stackoverflow.com/questions/28688264/how-to-traverse-a-hierarchical-tree-structure-structure-backwards-using-recursiv](https://stackoverflow.com/questions/28688264/how-to-traverse-a-hierarchical-tree-structure-structure-backwards-using-recursiv)
  - [https://stackoverflow.com/questions/51822070/how-can-postgres-represent-a-tree-of-row-ids](https://stackoverflow.com/questions/51822070/how-can-postgres-represent-a-tree-of-row-ids)
  - depth first
    - uspecified depth first variant
      - [https://stackoverflow.com/questions/50098759/postgres-nested-records-in-a-recursive-query-in-depth-first-manner](https://stackoverflow.com/questions/50098759/postgres-nested-records-in-a-recursive-query-in-depth-first-manner)
      - [https://stackoverflow.com/questions/59463176/how-to-perform-depth-first-search-in-postgresql](https://stackoverflow.com/questions/59463176/how-to-perform-depth-first-search-in-postgresql)
      - [https://stackoverflow.com/questions/30336265/postgresql-recursive-cte-results-ordering](https://stackoverflow.com/questions/30336265/postgresql-recursive-cte-results-ordering)
    - [preorder DFS](mathematics.md#pre-order-depth-first-search)
      - [https://dba.stackexchange.com/questions/63153/how-do-i-sort-the-results-of-a-recursive-query-in-an-expanded-tree-like-fashion](https://dba.stackexchange.com/questions/63153/how-do-i-sort-the-results-of-a-recursive-query-in-an-expanded-tree-like-fashion)
      - [https://stackoverflow.com/questions/65247873/preorder-tree-traversal-using-recursive-ctes-in-sql/77276675#77276675](https://stackoverflow.com/questions/65247873/preorder-tree-traversal-using-recursive-ctes-in-sql/77276675#77276675)
  - [breadth-first](mathematics.md#breadth-first-search) [https://stackoverflow.com/questions/3709292/select-rows-from-table-using-tree-order](https://stackoverflow.com/questions/3709292/select-rows-from-table-using-tree-order)
- [MySQL](#mysql)
  - [https://stackoverflow.com/questions/8252323/mysql-closure-table-hierarchical-database-how-to-pull-information-out-in-the-c](https://stackoverflow.com/questions/8252323/mysql-closure-table-hierarchical-database-how-to-pull-information-out-in-the-c) asks how to use a specific order ([preorder DFS](mathematics.md#pre-order-depth-first-search)) with [closure table](#closure-table)
- [Microsoft SQL Server](#microsoft-sql-server)
  - [https://stackoverflow.com/questions/14274942/sql-server-cte-and-recursion-example](https://stackoverflow.com/questions/14274942/sql-server-cte-and-recursion-example)

#### Closure table

↑ **Parent:** [SQL tree traversal](#sql-tree-traversal)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Closure_table)

#### Nested set model in SQL

↑ **Parent:** [SQL tree traversal](#sql-tree-traversal)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Nested_set_model_in_SQL)

How to implement [Nested set model](mathematics.md#nested-set-model) in [SQL](sql.md):
- [https://stackoverflow.com/questions/192220/what-is-the-most-efficient-elegant-way-to-parse-a-flat-table-into-a-tree/42781302#42781302](https://stackoverflow.com/questions/192220/what-is-the-most-efficient-elegant-way-to-parse-a-flat-table-into-a-tree/42781302#42781302) contains the correct left/size representation and update queries, which makes it much easier to maintain the tree without having to worry about the sizes of siblings which are constant
- [https://stackoverflow.com/questions/192220/what-is-the-most-efficient-elegant-way-to-parse-a-flat-table-into-a-tree/194031#194031](https://stackoverflow.com/questions/192220/what-is-the-most-efficient-elegant-way-to-parse-a-flat-table-into-a-tree/194031#194031) amazing ASCII art representations of the structure. Unfortunately uses a wonky left/right representation, rather than the much more natural left/size representation from the other post

## SQL feature

↑ **Parent:** [SQL](sql.md)

### Generated column

↑ **Parent:** [SQL feature](#sql-feature)

### SQL RECURSIVE query

↑ **Parent:** [SQL feature](#sql-feature)

Minimal example: [nodejs/sequelize/raw/recursive.js](nodejs/sequelize/raw/recursive.js)

More advanced [SQL tree traversal](#sql-tree-traversal) examples: [nodejs/sequelize/raw/tree.js](nodejs/sequelize/raw/tree.js)

[PostgreSQL](#postgresql) docs: [https://www.postgresql.org/docs/16/queries-with.html#QUERIES-WITH-RECURSIVE](https://www.postgresql.org/docs/16/queries-with.html#QUERIES-WITH-RECURSIVE)

#### SQL RECURSIVE prevent infinite recursion

↑ **Parent:** [SQL RECURSIVE query](#sql-recursive-query)

Example under: [nodejs/sequelize/raw/tree.js](nodejs/sequelize/raw/tree.js)

- [https://stackoverflow.com/questions/31739150/to-find-infinite-recursive-loop-in-cte](https://stackoverflow.com/questions/31739150/to-find-infinite-recursive-loop-in-cte) Canon.
- [PostgreSQL](#postgresql)
  - [https://stackoverflow.com/questions/26671612/prevent-and-or-detect-cycles-in-postgres?noredirect=1&lq=1](https://stackoverflow.com/questions/26671612/prevent-and-or-detect-cycles-in-postgres?noredirect=1&lq=1)
  - [https://stackoverflow.com/questions/39555616/detect-cycles-using-sql](https://stackoverflow.com/questions/39555616/detect-cycles-using-sql)
- [SQLite](#sqlite):
  - [https://dba.stackexchange.com/questions/310874/check-a-record-exists-already-and-stop-the-loop-in-a-recursive-query](https://dba.stackexchange.com/questions/310874/check-a-record-exists-already-and-stop-the-loop-in-a-recursive-query)
  - [https://stackoverflow.com/questions/66866542/sqlite-avoiding-cycles-in-depth-limited-recursive-cte](https://stackoverflow.com/questions/66866542/sqlite-avoiding-cycles-in-depth-limited-recursive-cte)
- [SQL Server](#oracle-database):
  - [https://stackoverflow.com/questions/58326847/sql-recursion-cte-infinite-loop](https://stackoverflow.com/questions/58326847/sql-recursion-cte-infinite-loop)
  - [https://dba.stackexchange.com/questions/215426/simple-recursive-cte-stuck-in-infinite-loop](https://dba.stackexchange.com/questions/215426/simple-recursive-cte-stuck-in-infinite-loop)
  - [https://stackoverflow.com/questions/13718168/infinite-loop-in-cte-when-parsing-self-referencing-table](https://stackoverflow.com/questions/13718168/infinite-loop-in-cte-when-parsing-self-referencing-table)

### SQL spatial index

↑ **Parent:** [SQL feature](#sql-feature)

#### PostgreSQL spatial index

↑ **Parent:** [SQL spatial index](#sql-spatial-index)

##### PostgreSQL GIST

↑ **Parent:** [PostgreSQL spatial index](#postgresql-spatial-index)

- [https://www.postgresql.org/docs/15/gist.html](https://www.postgresql.org/docs/15/gist.html)
- [https://www.postgresql.org/docs/15/datatype-geometric.html](https://www.postgresql.org/docs/15/datatype-geometric.html)
- [https://medium.com/postgres-professional/indexes-in-postgresql-5-gist-86e19781b5db](https://medium.com/postgres-professional/indexes-in-postgresql-5-gist-86e19781b5db) the only example on the net!

The highly underdocumented built-in module, that supports [SQL spatial index](#sql-spatial-index) and a lot more.

Quite horrendous as it only seems to work on geometric types and not existing columns. But why.

And it uses custom operatores, where standard operators would have been just fine for points...

Minimal runnable example with points:
```
set -x
time psql -c 'drop table if exists t'
time psql -c 'create table t(p point)'
time psql -c "insert into t select (point ('(' || generate_series || ',' || generate_series || ')')) from generate_series(1, 10000000)"
time psql -c 'create index on t using gist(p)'
time psql -c "select count(*) from t where p <@ box '(1000000,1000000),(9000000,2000000)'"
```
The index creation unfortunately took 100s, so it will not scale to 1B points very well whic his a shame.

Some sources about it:
- [https://stackoverflow.com/questions/28292198/how-to-port-simple-spatial-index-using-sqlite-r-trees-to-postgres](https://stackoverflow.com/questions/28292198/how-to-port-simple-spatial-index-using-sqlite-r-trees-to-postgres)

##### PostGIS

↑ **Parent:** [PostgreSQL spatial index](#postgresql-spatial-index)

[http://postgis.net/](http://postgis.net/)

The third part module, which clutters up any serches you make for the built-in one.

### SQL subquery

↑ **Parent:** [SQL feature](#sql-feature)

#### Common Table Expression

↑ **Parent:** [SQL subquery](#sql-subquery)

Similar to [SQL subquery](#sql-subquery), but with some differences: [https://stackoverflow.com/questions/706972/difference-between-cte-and-subquery](https://stackoverflow.com/questions/706972/difference-between-cte-and-subquery)

```
rm -f tmp.sqlite
sqlite3 tmp.sqlite 'create table t(i integer)'
sqlite3 tmp.sqlite 'insert into t values (1), (2)'
sqlite3 tmp.sqlite 'with mycte as ( select * from t ) delete from mycte where i = 1'
sqlite3 tmp.sqlite 'select * from t'
```

##### CTE insert values

↑ **Parent:** [Common Table Expression](#common-table-expression)

Useful for testing: [https://stackoverflow.com/questions/21819183/how-to-use-ctes-with-update-delete-on-sqlite](https://stackoverflow.com/questions/21819183/how-to-use-ctes-with-update-delete-on-sqlite)

```
sqlite3 :memory: 'WITH t (i, j) AS (VALUES (1, -1), (2, -2)) SELECT * FROM t'
```

### SQL transaction

↑ **Parent:** [SQL feature](#sql-feature)

#### SQL transaction isolation level

↑ **Parent:** [SQL transaction](#sql-transaction)

Each transaction isolation level specifies what can or cannot happen when two queries are being run in parallel, i.e.: the [memory semantics](computer.md#memory-semantics) of the system.

Remember that queries can affects thousands of rows, and database systems like [PostgreSQL](#postgresql) can run multiple such queries at the same time.

Good summary on the [PostgreSQL](#postgresql) page: [https://www.postgresql.org/docs/14/transaction-iso.html](https://www.postgresql.org/docs/14/transaction-iso.html)

Implementation specifics:
- [SQLite isolation levels](#sqlite-isolation-levels)

##### SQL READ UNCOMMITTED isolation level

↑ **Parent:** [SQL transaction isolation level](#sql-transaction-isolation-level)

##### SQL READ COMMITTED isolation level

↑ **Parent:** [SQL transaction isolation level](#sql-transaction-isolation-level)

Example where this level is sufficient: [nodejs/sequelize/raw/parallel_update_async.js](#_file/nodejs/sequelize/raw/parallel_update_async.js).

##### SQL REPEATABLE READ isolation level

↑ **Parent:** [SQL transaction isolation level](#sql-transaction-isolation-level)

Vs [SQL SERIALIZABLE isolation level](#sql-serializable-isolation-level) on [PostgreSQL](#postgresql): [https://dba.stackexchange.com/questions/284744/postgres-repeatable-read-vs-serializable](https://dba.stackexchange.com/questions/284744/postgres-repeatable-read-vs-serializable)

[nodejs/sequelize/raw/parallel_create_delete_empty_tag.js](#_file/nodejs/sequelize/raw/parallel_create_delete_empty_tag.js) is an example which experimentally seems to be solved by `REAPEATABLE READ`, although we are not sure that this is truly the case and why. What is clear is that that example is not solved by the [SQL READ COMMITTED isolation level](#sql-read-committed-isolation-level).

In [PostgreSQL](#postgresql), this is the first isolation level which can lead to [postgreSQL serialization failures](#postgresql-serialization-failure), this does not happen to [SQL READ COMMITTED isolation level](#sql-read-committed-isolation-level) in that [DBMS](software.md#database-management-system). You then have to retry the transaction.

##### SQL SERIALIZABLE isolation level

↑ **Parent:** [SQL transaction isolation level](#sql-transaction-isolation-level)

##### SQL isolation level example

↑ **Parent:** [SQL transaction isolation level](#sql-transaction-isolation-level)

###### SQL parallel update example

↑ **Parent:** [SQL isolation level example](#sql-isolation-level-example)

<h6 id="_file/nodejs/sequelize/raw/parallel_update_async.js">nodejs/sequelize/raw/parallel_update_async.js</h6>

↑ **Parent:** [SQL parallel update example](#sql-parallel-update-example)

[nodejs/sequelize/raw/parallel_update_worker_threads.js](nodejs/sequelize/raw/parallel_update_worker_threads.js) contains a base example that can be used to test what can happen when queries are being run in parallel. But it is broken due to a [`sqlite3` Node.js package](#sqlite3-node-js-package) bug: [https://github.com/mapbox/node-sqlite3/issues/1381](https://github.com/mapbox/node-sqlite3/issues/1381)...

[nodejs/sequelize/raw/parallel_update_async.js](nodejs/sequelize/raw/parallel_update_async.js) is an [`async`](programming-language.md#async-javascript) version of it. It should be just parallel enough to allow observing the same effects.

This is an example of a transaction where the [SQL READ COMMITTED isolation level](#sql-read-committed-isolation-level) if sufficient.

These examples run queries of type:
```
UPDATE "MyInt" SET i = i + 1
```

Sample execution:
```
node --unhandled-rejections=strict ./parallel_update_async.js p 10 100
```
which does:
- [PostgreSQL](#postgresql), see other databases options at [SQL example](#sql-example)
- 10 threads
- 100 increments on each thread

The fear then is that of a classic [read-modify-write](computer.md#read-modify-write) failure.

But as [https://www.postgresql.org/docs/14/transaction-iso.html](https://www.postgresql.org/docs/14/transaction-iso.html) page makes very clear, including with an explicit example of type `UPDATE accounts SET balance = balance + 100.00 WHERE acctnum = 12345;`, that the default isolation level, [SQL READ COMMITTED isolation level](#sql-read-committed-isolation-level), already prevents any problems with this, as the update always re-reads selected rows in case they were previously modified.

> If the first updater commits, the second updater will ignore the row if the first updater deleted it, otherwise it will attempt to apply its operation to the updated version of the row

Since in [PostgreSQL](#postgresql) "Read uncommitted" appears to be effectively the same as "Read committed", we won't be able to observe any failures on that database system for this example.

[nodejs/sequelize/raw/parallel_create_delete_empty_tag.js](#_file/nodejs/sequelize/raw/parallel_create_delete_empty_tag.js) contains an example where things can actually blow up in read committed.

<h6 id="_file/nodejs/sequelize/raw/parallel_select_and_update.js">nodejs/sequelize/raw/parallel_select_and_update.js</h6>

↑ **Parent:** [SQL parallel update example](#sql-parallel-update-example)

This example is similar to [nodejs/sequelize/raw/parallel_update_async.js](#_file/nodejs/sequelize/raw/parallel_update_async.js), but now we are doing a separate SELECT, later followed by an update:
- `SELECT FROM` to get i
- update on Js code `newI = i + 1`
- `UPDATE SET` the `newI`

Although this specific example is useless in itself, as we could just use `UPDATE "MyInt" SET i = i + 1` as in [nodejs/sequelize/raw/parallel_update_async.js](#_file/nodejs/sequelize/raw/parallel_update_async.js), which automatically solves any concurrency issue, this kind of code could be required for example if the update was a complex function not suitably implemented in SQL, or if the update depends on some external data source.

Sample execution:
```
node --unhandled-rejections=strict ./parallel_select_and_update.js p 2 10 'READ COMMITTED'
```
which does:
- [PostgreSQL](#postgresql), see other databases options at [SQL example](#sql-example)
- 2 threads
- 10 increments on each thread

Another one:
```
node --unhandled-rejections=strict ./parallel_select_and_update.js p 2 10 'READ COMMITTED' 'FOR UPDATE'
```
this will run [SELECT FOR UPDATE](#select-for-update) rather than just [SELECT](#select-sql)

Observed behaviour under different [SQL transaction isolation levels](#sql-transaction-isolation-level):
- `READ COMMITTED`: fails. Nothing in this case prevents:
  - thread 1: SELECT, obtains i = 0
  - thread 2: SELECT, obtains i = 0
  - thread 2: newI = 1
  - thread 2: UPDATE i = 1
  - thread 1: newI = 1
  - thread 1: UPDATE i = 1
- `REPEATABLE READ`: works. the manual mentions that if multiple concurrent updates would happen, only the first commit succeeds, and the following ones fail and rollback and retry, therefore preventing the loss of an update.
- `READ COMMITTED` + `SELECT FOR UPDATE`: works. And does not do rollbacks, which probably makes it faster. With `p 10 100`, `REPEATABLE READ` was about 4.2s and `READ COMMITTED` + `SELECT FOR UPDATE` 3.2s on [Lenovo ThinkPad P51 (2017)](ciro-santilli-s-hardware.md#lenovo-thinkpad-p51-2017).

  `SELECT FOR UPDATE` should be enough as mentioned at: [https://www.postgresql.org/docs/13/explicit-locking.html#LOCKING-ROWS](https://www.postgresql.org/docs/13/explicit-locking.html#LOCKING-ROWS)

  > FOR UPDATE causes the rows retrieved by the SELECT statement to be locked as though for update. This prevents them from being locked, modified or deleted by other transactions until the current transaction ends. That is, other transactions that attempt UPDATE, DELETE, SELECT FOR UPDATE, SELECT FOR NO KEY UPDATE, SELECT FOR SHARE or SELECT FOR KEY SHARE of these rows will be blocked until the current transaction ends; conversely, SELECT FOR UPDATE will wait for a concurrent transaction that has run any of those commands on the same row, and will then lock and return the updated row (or no row, if the row was deleted). Within a REPEATABLE READ or SERIALIZABLE transaction, however, an error will be thrown if a row to be locked has changed since the transaction started. For further discussion see Section 13.4.

A non-raw version of this example can be seen at: [nodejs/sequelize/parallel\_select\_and\_update.js](sequelize.md#_file/nodejs/sequelize/parallel_select_and_update.js).

<h6 id="_file/nodejs/sequelize/raw/parallel_select_and_update_deterministic.js">nodejs/sequelize/raw/parallel_select_and_update_deterministic.js</h6>

↑ **Parent:** [SQL parallel update example](#sql-parallel-update-example)

This example contains a deterministic demo of when [postgreSQL serialization failures](#postgresql-serialization-failure) may happen.

Tested on [PostgreSQL](#postgresql) 13.5.

<h6 id="_file/nodejs/sequelize/raw/parallel_create_delete_empty_tag.js">nodejs/sequelize/raw/parallel_create_delete_empty_tag.js</h6>

↑ **Parent:** [SQL parallel update example](#sql-parallel-update-example)

In this example, posts have tags. When a post is deleted, we check to see if there are now any empty tags, and now we want to delete any empty tags that the post deletion may have created.

If we are creating and deleting posts concurrently, a naive implementation might wrongly delete the tags of a newly created post.

This could be due to a concurrency issue of the following types.

Failure case 1:
- thread 2: delete old post
- thread 2: find all tags with 0 posts. Finds `tag0` from the deleted old post which is now empty.
- thread 1: create new post, which we want to have tag `tag0`
- thread 1: try to create a new tag `tag0`, but don't because it already exists, this is done using [SQLite](#sqlite)'s `INSERT OR IGNORE INTO` or [PostgreSQL](#postgresql)'s `INSERT ... ON CONFLICT DO NOTHING`
- thread 1: assign `tag0` to the new post by adding an entry to the join table
- thread 2: delete all tags with 0 posts. It still sees from its previous search that `tag0` is empty, and deletes it, which then cascades into the join table
which would result in the new post incorrectly not having the `tag0`.

Failure case 2:
- thread 2: delete old post
- thread 2: find all tags with 0 posts
- thread 1: create new post
- thread 1: try to create a new tag `tag0`, but don't because it already exists
- thread 2: delete all tags with 0 posts. It still sees from its previous search that `tag0` is empty, and deletes it
- thread 1: assign `tag0` to the new post
which leads to a foreign key failure, because the tag does not exist anymore when the assignment happens.

Failure case 3:
- thread 2: delete old post
- thread 1: create new post, which we want to have tag `tag0`
- thread 1: try to create a new tag `tag0`, and succeed because it wasn't present
- thread 2: find all tags with 0 posts, finds the tag that was just created
- thread 2: delete all tags with 0 posts, deleting the new tag
- thread 1: assign `tag0` to the new post
which leads to a foreign key failure, because the tag does not exist anymore when the assignment happens.

Sample executions:
- `node --unhandled-rejections=strict ./parallel_create_delete_empty_tag.js p 9 1000 'READ COMMITTED'`: [PostgreSQL](#postgresql), 9 tags, DELETE/CREATE the `tag0` test tag 1000 times, use `READ COMMITTED`

  Execution often fails, although not always. The failure is always:
  ```
  error: insert or update on table "PostTag" violates foreign key constraint "PostTag_tagId_fkey"
  ```
  because the:
  ```
  INSERT INTO "PostTag"
  ```
  tries to insert a tag that was deleted in the other thread, as it didn't have any corresponding posts, so this is the foreign key failure.

  TODO: we've never managed to observe the failure case in which `tag0` is deleted. Is it truly possible? And if not, by which guarantee?
- `node --unhandled-rejections=strict ./parallel_create_delete_empty_tag.js p 9 1000 'READ COMMITTED' 'FOR UPDATE'`: do a `SELECT ... FOR UPDATE` before trying to `INSERT`.

  This is likely correct and the fastest correct method according to our quick benchmarking, about 20% faster than `REPEATABLE READ`.

  We are just now 100% sure it is corret becase we can't find out if the `SELECT` in the `DELETE` subquery could first select some rows, which are then locked by the tag creator, and only then locked by `DELETE` after selection. Or does it re-evaludate the `SELECT` even though it is in a subquery?
- `node --unhandled-rejections=strict ./parallel_create_delete_empty_tag.js p 9 1000 'REPEATABLE READ'`: repeatable read

  We've never observed any failures with this level. This should likely fix the foreign key issue according to the PostgreSQL docs, since:
  - the `DELETE "Post"` commit cannot start to be seen only in the middle of the thread 1 transaction
  - and then if DELETE happened, the thread 1 transaction will detect it, ROLLBACK, and re-run. TODO how does it detect the need rollback? Is it because of the foreign key? It is very hard to be sure about this kind of thing, just can't find the information. Related: [postgreSQL serialization failure](#postgresql-serialization-failure).
- `node --unhandled-rejections=strict ./parallel_create_delete_empty_tag.js p 9 1000 'SERIALIZABLE'`: serializable
- `node --unhandled-rejections=strict ./parallel_create_delete_empty_tag.js p 9 1000 'NONE'`: magic value, don't use any transaction. Can blow up of course, since even less restrictions than `READ COMMITTED`
All executions use 2 threads.

Some theoretical notes:
- Failure case 3 is averted by a `READ COMMITTED` transaction, because thread 2 won't see the uncommitted tag that thread 1 created, and therefore won't be able to delete it

[https://stackoverflow.com/questions/10935850/when-to-use-select-for-update](https://stackoverflow.com/questions/10935850/when-to-use-select-for-update) from [SELECT FOR UPDATE](#select-for-update) also talks about a similar example, and has relevant answers.

### Window function (SQL)

↑ **Parent:** [SQL feature](#sql-feature)

<h4 id="row-number"><code>ROW_NUMBER</code></h4>

↑ **Parent:** [Window function (SQL)](#window-function-sql)


```
sqlite3 ':memory:'  'WITH t (i) AS (VALUES (-1), (-1), (-2)) SELECT *, row_number() over () FROM t'
```
Possible output:
```
-1|1
-1|2
-2|3
```
Gives them unique IDs.

With a `partition by`:
```
sqlite3 ':memory:'  'WITH t (i) AS (VALUES (-1), (-1), (-2)) SELECT *, row_number() over ( partition by i ) FROM t'
```
possible output:
```
-2|1
-1|1
-1|2
```

#### SQL window `RANGE`

↑ **Parent:** [Window function (SQL)](#window-function-sql)

- [SQLite](#sqlite): [https://www.sqlite.org/windowfunctions.html#exprrange](https://www.sqlite.org/windowfunctions.html#exprrange)

```
rm -f tmp.sqlite
sqlite3 tmp.sqlite "create table t (id integer, val integer)"
sqlite3 tmp.sqlite <<EOF
insert into t values
  (0, 0),
  (1, 5),
  (2, 10),
  (3, 14),
  (4, 15),
  (5, 16),
  (6, 20),
  (7, 25),
  (8, 29),
  (9, 30),
  (10, 30),
  (11, 31),
  (12, 35),
  (13, 40)
EOF
```

Show how many neighbours each column has with `val` between `val - 2` and `val + 2` inclusive:
```
sqlite3 tmp.sqlite <<EOF
SELECT id, val, COUNT(*) OVER (
  ORDER BY val RANGE BETWEEN 2 PRECEDING AND 2 FOLLOWING
) FROM t;
EOF
```
Output:
```
0|0|1
1|5|1
2|10|1
3|14|3
4|15|3
5|16|3
6|20|1
7|25|1
8|29|4
9|30|4
10|30|4
11|31|4
12|35|1
13|40|1
```

`val - 1` and `val + 1` inclusive instead:
```
sqlite3 tmp.sqlite <<EOF
SELECT id, val, COUNT(*) OVER (
  ORDER BY val RANGE BETWEEN 1 PRECEDING AND 1 FOLLOWING
) FROM t;
EOF
```
Output:
```
0|0|1
1|5|1
2|10|1
3|14|2
4|15|3
5|16|2
6|20|1
7|25|1
8|29|3
9|30|4
10|30|4
11|31|3
12|35|1
13|40|1
```

There seems to be no analogue to [HAVING](#having-sql) for window functions, so we can just settle for a subquery for once, e.g.:
```
sqlite3 tmp.sqlite <<EOF
SELECT * FROM (
  SELECT id, val, COUNT(*) OVER (
    ORDER BY val RANGE BETWEEN 1 PRECEDING AND 1 FOLLOWING
  ) as c FROM t
) WHERE c > 2
EOF
```
which outputs:
```
4|15|3
8|29|3
9|30|4
10|30|4
11|31|3
```

#### SQL contiguous ranges

↑ **Parent:** [Window function (SQL)](#window-function-sql)

[https://stackoverflow.com/questions/17046204/how-to-find-the-boundaries-of-groups-of-contiguous-sequential-numbers/17046749#17046749](https://stackoverflow.com/questions/17046204/how-to-find-the-boundaries-of-groups-of-contiguous-sequential-numbers/17046749#17046749) just works, even in [SQLite](#sqlite) which supports all quoting types known to man including `[]` for compatibility with insane [RDBMSs](software.md#relational-database-management-system)!

Here's a slightly saner version:
```
rm -f tmp.sqlite
sqlite3 tmp.sqlite "create table mytable (id integer primary key autoincrement, number integer, status integer)"
sqlite3 tmp.sqlite <<EOF
insert into mytable(number, status) values
  (100,0),
  (101,0),
  (102,0),
  (103,0),
  (104,1),
  (105,1),
  (106,0),
  (107,0),
  (1014,0),
  (1015,0),
  (1016,1),
  (1017,0)
EOF
sqlite3 tmp.sqlite <<EOF
SELECT
  MIN(id) AS "id",
  MIN(number) AS "from",
  MAX(number) AS "to"
FROM (
  SELECT ROW_NUMBER() OVER (ORDER BY number) - number AS grp, id, number
  FROM mytable
  WHERE status = 0
)
GROUP BY grp
ORDER BY MIN(number)
EOF
```

output:

```
1|100|103
7|106|107
9|1014|1015
12|1017|1017
```

To get only groups of length greater than 1:
```
sqlite3 tmp.sqlite <<EOF
SELECT "id", "from", "to", "to" - "from" + 1 as "len" FROM (
  SELECT
    MIN("id") AS "id",
    MIN(number) AS "from",
    MAX(number) AS "to"
  FROM (
    SELECT ROW_NUMBER() OVER (ORDER BY "number") - "number" AS "grp", "id", "number"
    FROM "mytable"
    WHERE "status" = 0
  )
  GROUP BY "grp"
  ORDER BY MIN("number")
) WHERE "len" > 1
EOF
```

Output:
```
1|100|103|4
7|106|107|2
9|1014|1015|2
```

## ↑ Ancestors (10)

1. [Relational database management system](software.md#relational-database-management-system)
2. [Relational database](software.md#relational-database)
3. [Type of database](software.md#type-of-database)
4. [Database](software.md#database)
5. [Software](software.md)
6. [Computer](computer.md)
7. [Information technology](technology.md#information-technology)
8. [Area of technology](technology.md#area-of-technology)
9. [Technology](technology.md)
10. [Ciro Santilli's Homepage](README.md)

## ← Incoming links (15)

- [etchablock.com](cool-data-embedded-in-the-bitcoin-blockchain.md#etchablock-com)
- [Database management system](software.md#database-management-system)
- [Gordon Linoff](stack-overflow.md#gordon-linoff)
- [How to decide if an ORM is good?](software.md#how-to-decide-if-an-orm-is-good)
- [IBM](computer.md#ibm)
- [Isolation (database systems)](software.md#isolation-database-systems)
- [Nested set model](mathematics.md#nested-set-model)
- [Nested set model in SQL](#nested-set-model-in-sql)
- [Oracle Corporation](software.md#oracle-corporation)
- [Sequelize raw query](sequelize.md#sequelize-raw-query)
- [List topics on home page](sponsor/updates/8.md#list-topics-on-home-page)
- [SQL example](#sql-example)
- [SQL TRIGGER](#sql-trigger)
- [Stack Exchange Data Explorer](stack-overflow.md#stack-exchange-data-explorer)
- [Metrics and rationales](updates.md#ourbigbook-project-update-march-2025/metrics-and-rationales)
