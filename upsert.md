# Upsert

↑ **Parent:** [INSERT (SQL)](insert-sql.md)

`UPSERT` is extremely handy, and reduces the number of find, check on server, update loops. But `RETURNING` is a fundamental part of that (to get the updated/existing) ID. Can't believe SQL hasn't standardized it yet as of 2022. But both [SQLite](sqlite.md) and [Postgres](postgresql.md) support it with similar syntax thankfully.

[nodejs/sequelize/raw/upsert.js](nodejs/sequelize/raw/upsert.js)

- [https://www.postgresql.org/docs/14/sql-insert.html#SQL-ON-CONFLICT](https://www.postgresql.org/docs/14/sql-insert.html#SQL-ON-CONFLICT)
- [https://www.sqlite.org/lang_returning.html](https://www.sqlite.org/lang_returning.html)

**Table of contents**

- [Upsert with `NOT NULL` column](upsert-with-not-null-column.md)

## ↑ Ancestors (13)

1. [INSERT (SQL)](insert-sql.md)
2. [SQL keyword](sql-keyword.md)
3. [SQL](sql-split.md)
4. [Relational database management system](relational-database-management-system.md)
5. [Relational database](relational-database.md)
6. [Type of database](type-of-database.md)
7. [Database](database.md)
8. [Software](software-split.md)
9. [Computer](computer-split.md)
10. [Information technology](information-technology.md)
11. [Area of technology](area-of-technology.md)
12. [Technology](technology-split.md)
13. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (2)

- [Sequelize example](sequelize-example.md)
- [Update multiple rows with different values in a single SQL query](update-multiple-rows-with-different-values-in-a-single-sql-query.md)
