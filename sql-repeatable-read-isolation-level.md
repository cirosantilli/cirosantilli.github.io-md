# SQL REPEATABLE READ isolation level

↑ **Parent:** [SQL transaction isolation level](sql-transaction-isolation-level.md)

Vs [SQL SERIALIZABLE isolation level](sql-serializable-isolation-level.md) on [PostgreSQL](postgresql.md): [https://dba.stackexchange.com/questions/284744/postgres-repeatable-read-vs-serializable](https://dba.stackexchange.com/questions/284744/postgres-repeatable-read-vs-serializable)

[nodejs/sequelize/raw/parallel_create_delete_empty_tag.js](_file/nodejs/sequelize/raw/parallel_create_delete_empty_tag.js.md) is an example which experimentally seems to be solved by `REAPEATABLE READ`, although we are not sure that this is truly the case and why. What is clear is that that example is not solved by the [SQL READ COMMITTED isolation level](sql-read-committed-isolation-level.md).

In [PostgreSQL](postgresql.md), this is the first isolation level which can lead to [postgreSQL serialization failures](postgresql-serialization-failure.md), this does not happen to [SQL READ COMMITTED isolation level](sql-read-committed-isolation-level.md) in that [DBMS](database-management-system.md). You then have to retry the transaction.

## ↑ Ancestors (14)

1. [SQL transaction isolation level](sql-transaction-isolation-level.md)
2. [SQL transaction](sql-transaction.md)
3. [SQL feature](sql-feature.md)
4. [SQL](sql-split.md)
5. [Relational database management system](relational-database-management-system.md)
6. [Relational database](relational-database.md)
7. [Type of database](type-of-database.md)
8. [Database](database.md)
9. [Software](software-split.md)
10. [Computer](computer-split.md)
11. [Information technology](information-technology.md)
12. [Area of technology](area-of-technology.md)
13. [Technology](technology-split.md)
14. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (1)

- [PostgreSQL serialization failure](postgresql-serialization-failure.md)
