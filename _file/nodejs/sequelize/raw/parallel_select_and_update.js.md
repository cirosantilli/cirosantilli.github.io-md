<h1 id="_file/nodejs/sequelize/raw/parallel_select_and_update.js">nodejs/sequelize/raw/parallel_select_and_update.js</h1>

↑ **Parent:** [SQL parallel update example](../../../../sql-parallel-update-example.md)

This example is similar to [nodejs/sequelize/raw/parallel_update_async.js](parallel_update_async.js.md), but now we are doing a separate SELECT, later followed by an update:
- `SELECT FROM` to get i
- update on Js code `newI = i + 1`
- `UPDATE SET` the `newI`

Although this specific example is useless in itself, as we could just use `UPDATE "MyInt" SET i = i + 1` as in [nodejs/sequelize/raw/parallel_update_async.js](parallel_update_async.js.md), which automatically solves any concurrency issue, this kind of code could be required for example if the update was a complex function not suitably implemented in SQL, or if the update depends on some external data source.

Sample execution:
```
node --unhandled-rejections=strict ./parallel_select_and_update.js p 2 10 'READ COMMITTED'
```
which does:
- [PostgreSQL](../../../../postgresql.md), see other databases options at [SQL example](../../../../sql-example.md)
- 2 threads
- 10 increments on each thread

Another one:
```
node --unhandled-rejections=strict ./parallel_select_and_update.js p 2 10 'READ COMMITTED' 'FOR UPDATE'
```
this will run [SELECT FOR UPDATE](../../../../select-for-update.md) rather than just [SELECT](../../../../select-sql.md)

Observed behaviour under different [SQL transaction isolation levels](../../../../sql-transaction-isolation-level.md):
- `READ COMMITTED`: fails. Nothing in this case prevents:
  - thread 1: SELECT, obtains i = 0
  - thread 2: SELECT, obtains i = 0
  - thread 2: newI = 1
  - thread 2: UPDATE i = 1
  - thread 1: newI = 1
  - thread 1: UPDATE i = 1
- `REPEATABLE READ`: works. the manual mentions that if multiple concurrent updates would happen, only the first commit succeeds, and the following ones fail and rollback and retry, therefore preventing the loss of an update.
- `READ COMMITTED` + `SELECT FOR UPDATE`: works. And does not do rollbacks, which probably makes it faster. With `p 10 100`, `REPEATABLE READ` was about 4.2s and `READ COMMITTED` + `SELECT FOR UPDATE` 3.2s on [Lenovo ThinkPad P51 (2017)](../../../../ciro-santilli-s-hardware/lenovo-thinkpad-p51-2017.md).

  `SELECT FOR UPDATE` should be enough as mentioned at: [https://www.postgresql.org/docs/13/explicit-locking.html#LOCKING-ROWS](https://www.postgresql.org/docs/13/explicit-locking.html#LOCKING-ROWS)

  > FOR UPDATE causes the rows retrieved by the SELECT statement to be locked as though for update. This prevents them from being locked, modified or deleted by other transactions until the current transaction ends. That is, other transactions that attempt UPDATE, DELETE, SELECT FOR UPDATE, SELECT FOR NO KEY UPDATE, SELECT FOR SHARE or SELECT FOR KEY SHARE of these rows will be blocked until the current transaction ends; conversely, SELECT FOR UPDATE will wait for a concurrent transaction that has run any of those commands on the same row, and will then lock and return the updated row (or no row, if the row was deleted). Within a REPEATABLE READ or SERIALIZABLE transaction, however, an error will be thrown if a row to be locked has changed since the transaction started. For further discussion see Section 13.4.

A non-raw version of this example can be seen at: [nodejs/sequelize/parallel\_select\_and\_update.js](../parallel_select_and_update.js.md).

## ↑ Ancestors (16)

1. [SQL parallel update example](../../../../sql-parallel-update-example.md)
2. [SQL isolation level example](../../../../sql-isolation-level-example.md)
3. [SQL transaction isolation level](../../../../sql-transaction-isolation-level.md)
4. [SQL transaction](../../../../sql-transaction.md)
5. [SQL feature](../../../../sql-feature.md)
6. [SQL](../../../../sql-split.md)
7. [Relational database management system](../../../../relational-database-management-system.md)
8. [Relational database](../../../../relational-database.md)
9. [Type of database](../../../../type-of-database.md)
10. [Database](../../../../database.md)
11. [Software](../../../../software-split.md)
12. [Computer](../../../../computer-split.md)
13. [Information technology](../../../../information-technology.md)
14. [Area of technology](../../../../area-of-technology.md)
15. [Technology](../../../../technology-split.md)
16. [Ciro Santilli's Homepage](../../../../split.md)

## ← Incoming links (2)

- [Nodejs/sequelize/parallel\_select\_and\_update.js](../parallel_select_and_update.js.md)
- [SELECT FOR UPDATE](../../../../select-for-update.md)
