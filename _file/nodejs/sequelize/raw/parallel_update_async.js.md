<h1 id="_file/nodejs/sequelize/raw/parallel_update_async.js">nodejs/sequelize/raw/parallel_update_async.js</h1>

↑ **Parent:** [SQL parallel update example](../../../../sql-parallel-update-example.md)

[nodejs/sequelize/raw/parallel_update_worker_threads.js](nodejs/sequelize/raw/parallel_update_worker_threads.js) contains a base example that can be used to test what can happen when queries are being run in parallel. But it is broken due to a [`sqlite3` Node.js package](../../../../sqlite3-node-js-package.md) bug: [https://github.com/mapbox/node-sqlite3/issues/1381](https://github.com/mapbox/node-sqlite3/issues/1381)...

[nodejs/sequelize/raw/parallel_update_async.js](nodejs/sequelize/raw/parallel_update_async.js) is an [`async`](../../../../async-javascript.md) version of it. It should be just parallel enough to allow observing the same effects.

This is an example of a transaction where the [SQL READ COMMITTED isolation level](../../../../sql-read-committed-isolation-level.md) if sufficient.

These examples run queries of type:
```
UPDATE "MyInt" SET i = i + 1
```

Sample execution:
```
node --unhandled-rejections=strict ./parallel_update_async.js p 10 100
```
which does:
- [PostgreSQL](../../../../postgresql.md), see other databases options at [SQL example](../../../../sql-example.md)
- 10 threads
- 100 increments on each thread

The fear then is that of a classic [read-modify-write](../../../../read-modify-write.md) failure.

But as [https://www.postgresql.org/docs/14/transaction-iso.html](https://www.postgresql.org/docs/14/transaction-iso.html) page makes very clear, including with an explicit example of type `UPDATE accounts SET balance = balance + 100.00 WHERE acctnum = 12345;`, that the default isolation level, [SQL READ COMMITTED isolation level](../../../../sql-read-committed-isolation-level.md), already prevents any problems with this, as the update always re-reads selected rows in case they were previously modified.

> If the first updater commits, the second updater will ignore the row if the first updater deleted it, otherwise it will attempt to apply its operation to the updated version of the row

Since in [PostgreSQL](../../../../postgresql.md) "Read uncommitted" appears to be effectively the same as "Read committed", we won't be able to observe any failures on that database system for this example.

[nodejs/sequelize/raw/parallel_create_delete_empty_tag.js](parallel_create_delete_empty_tag.js.md) contains an example where things can actually blow up in read committed.

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

- [nodejs/sequelize/raw/parallel_select_and_update.js](parallel_select_and_update.js.md)
- [SQL READ COMMITTED isolation level](../../../../sql-read-committed-isolation-level.md)
