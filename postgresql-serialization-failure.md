# PostgreSQL serialization failure

↑ **Parent:** [PostgreSQL](postgresql.md)

When using [SQL REPEATABLE READ isolation level](sql-repeatable-read-isolation-level.md) and [SQL SERIALIZABLE isolation level](sql-serializable-isolation-level.md), concurrent transactions may fail with a serialization failure, and then you might need to retry them. You server code or your ORM must always account for that.

A good way to explore when it happens is to use the example

Related questions:
- [https://stackoverflow.com/questions/7705273/what-are-the-conditions-for-encountering-a-serialization-failure](https://stackoverflow.com/questions/7705273/what-are-the-conditions-for-encountering-a-serialization-failure)
- [https://stackoverflow.com/questions/59351109/error-could-not-serialize-access-due-to-concurrent-update](https://stackoverflow.com/questions/59351109/error-could-not-serialize-access-due-to-concurrent-update)
- [https://stackoverflow.com/questions/50797097/postgres-could-not-serialize-access-due-to-concurrent-update/51932824](https://stackoverflow.com/questions/50797097/postgres-could-not-serialize-access-due-to-concurrent-update/51932824)

## ↑ Ancestors (13)

1. [PostgreSQL](postgresql.md)
2. [SQL implementation](sql-implementation.md)
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

## ← Incoming links (3)

- [nodejs/sequelize/raw/parallel_create_delete_empty_tag.js](_file/nodejs/sequelize/raw/parallel_create_delete_empty_tag.js.md)
- [nodejs/sequelize/raw/parallel_select_and_update_deterministic.js](_file/nodejs/sequelize/raw/parallel_select_and_update_deterministic.js.md)
- [SQL REPEATABLE READ isolation level](sql-repeatable-read-isolation-level.md)
