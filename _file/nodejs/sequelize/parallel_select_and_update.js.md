<h1 id="_file/nodejs/sequelize/parallel_select_and_update.js">nodejs/sequelize/parallel_select_and_update.js</h1>

↑ **Parent:** [Sequelize parallel example](../../../sequelize-parallel-example.md)

This example is the same as [nodejs/sequelize/raw/parallel\_select\_and\_update.js](raw/parallel_select_and_update.js.md), but going through [Sequelize](../../../sequelize-split.md) rather than with [Sequelize raw queries](../../../sequelize-raw-query.md). `NONE` is not supported for now to not have a transaction at all because lazy.

The examples illustrates: [https://stackoverflow.com/questions/55452441/for-share-and-for-update-statements-in-sequelize](https://stackoverflow.com/questions/55452441/for-share-and-for-update-statements-in-sequelize)

Sample invocation:
```
node --unhandled-rejections=strict ./parallel_select_and_update.js p 10 100 READ_COMMITTED UPDATE
```
where:
- `READ_COMMITTED`: one of the keys documented at: [https://sequelize.org/master/class/lib/transaction.js~Transaction.html](https://sequelize.org/master/class/lib/transaction.js~Transaction.html) which correspond to the standard [sQL isolation levels](../../../sql-transaction-isolation-level.md). It not given, don't set one, defaulting to the database's/sequelize's default level.
- `UPDATE`: one of the keys documented at: [https://sequelize.org/master/class/lib/transaction.js~Transaction.html#static-get-LOCK](https://sequelize.org/master/class/lib/transaction.js~Transaction.html#static-get-LOCK). Update generates a `SELECT FOR UPDATE` in [PostgreSQL](../../../postgresql.md) for example. If not given, don't use any `FOR xxx` explicit locking.

Other examples:
- `node --unhandled-rejections=strict ./parallel_select_and_update.js p 10 100 READ_COMMITTED UPDATE`

Then, the outcome is exactly as described at: [nodejs/sequelize/raw/parallel\_select\_and\_update.js](raw/parallel_select_and_update.js.md):
- `READ_COMMITTED`: fails
- `READ_COMMITTED UPDATE`: works
- `REPEATABLE_READ`: works, but is a bit slower, as it does rollbacks

  This case also illustrates [Sequelize transaction retries](../../../sequelize-transaction-retry.md), since in this transaction isolation level transactions may fail:
  - [https://stackoverflow.com/questions/68427796/sequelize-transaction-retry-doenst-work-as-expected](https://stackoverflow.com/questions/68427796/sequelize-transaction-retry-doenst-work-as-expected)
  - [https://github.com/sequelize/sequelize/issues/1478](https://github.com/sequelize/sequelize/issues/1478)
  - [https://github.com/sequelize/sequelize/issues/8294](https://github.com/sequelize/sequelize/issues/8294)

## ↑ Ancestors (15)

1. [Sequelize parallel example](../../../sequelize-parallel-example.md)
2. [Sequelize example](../../../sequelize-example.md)
3. [Sequelize](../../../sequelize-split.md)
4. [Node.js ORM library](../../../node-js-orm-library.md)
5. [Node.js library](../../../node-js-library.md)
6. [Node.js](../../../node-js-split.md)
7. [JavaScript](../../../javascript.md)
8. [List of programming languages](../../../list-of-programming-languages.md)
9. [Programming language](../../../programming-language-split.md)
10. [Software](../../../software-split.md)
11. [Computer](../../../computer-split.md)
12. [Information technology](../../../information-technology.md)
13. [Area of technology](../../../area-of-technology.md)
14. [Technology](../../../technology-split.md)
15. [Ciro Santilli's Homepage](../../../split.md)

## ← Incoming links (1)

- [Nodejs/sequelize/raw/parallel\_select\_and\_update.js](raw/parallel_select_and_update.js.md)
