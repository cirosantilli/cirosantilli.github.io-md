# SQL transaction isolation level

↑ **Parent:** [SQL transaction](sql-transaction.md)

Each transaction isolation level specifies what can or cannot happen when two queries are being run in parallel, i.e.: the [memory semantics](memory-semantics.md) of the system.

Remember that queries can affects thousands of rows, and database systems like [PostgreSQL](postgresql.md) can run multiple such queries at the same time.

Good summary on the [PostgreSQL](postgresql.md) page: [https://www.postgresql.org/docs/14/transaction-iso.html](https://www.postgresql.org/docs/14/transaction-iso.html)

Implementation specifics:
- [SQLite isolation levels](sqlite-isolation-levels.md)

**Table of contents**

- [SQL READ UNCOMMITTED isolation level](sql-read-uncommitted-isolation-level.md)
- [SQL READ COMMITTED isolation level](sql-read-committed-isolation-level.md)
- [SQL REPEATABLE READ isolation level](sql-repeatable-read-isolation-level.md)
- [SQL SERIALIZABLE isolation level](sql-serializable-isolation-level.md)
- [SQL isolation level example](sql-isolation-level-example.md)
  - [SQL parallel update example](sql-parallel-update-example.md)
    - [nodejs/sequelize/raw/parallel\_update\_async.js](_file/nodejs/sequelize/raw/parallel_update_async.js.md)
    - [nodejs/sequelize/raw/parallel\_select\_and\_update.js](_file/nodejs/sequelize/raw/parallel_select_and_update.js.md)
    - [nodejs/sequelize/raw/parallel\_select\_and\_update\_deterministic.js](_file/nodejs/sequelize/raw/parallel_select_and_update_deterministic.js.md)
    - [nodejs/sequelize/raw/parallel\_create\_delete\_empty\_tag.js](_file/nodejs/sequelize/raw/parallel_create_delete_empty_tag.js.md)

## 🏷️ Tagged (1)

- [SQLite isolation levels](sqlite-isolation-levels.md)

## ↑ Ancestors (13)

1. [SQL transaction](sql-transaction.md)
2. [SQL feature](sql-feature.md)
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

## ← Incoming links (4)

- [nodejs/sequelize/raw/parallel_select_and_update.js](_file/nodejs/sequelize/raw/parallel_select_and_update.js.md)
- [Isolation (database systems)](isolation-database-systems.md)
- [Memory semantics](memory-semantics.md)
- [SELECT FOR UPDATE](select-for-update.md)
