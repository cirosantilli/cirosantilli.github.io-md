# SQLite

↑ **Parent:** [SQL implementation](sql-implementation.md)  
🏷️ **Tags:** [Good](good.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/SQLite)

The minimalism, serverlessness/lack of temporary caches/lack of permission management, Hipp's religious obsession with efficiency, the use of their own pure Fossil [version control](version-control.md)[https://sqlite.org/whynotgit.html](https://sqlite.org/whynotgit.html). Wait, scrap that last one. Pure beauty!

![](https://upload.wikimedia.org/wikipedia/commons/thumb/3/38/SQLite370.svg/500px-SQLite370.svg.png)

**[Figure 1](#_275)** [Source](https://commons.wikimedia.org/wiki/File:SQLite370.svg.png).

Official [Git](git.md) mirror: [https://github.com/sqlite/sqlite](https://github.com/sqlite/sqlite)

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

**Table of contents**

- [SQLite import CSV](sqlite-import-csv.md)
  - [SQLite import CSV from stdin](sqlite-import-csv-from-stdin.md)
- [SQLite import JSON](sqlite-import-json.md)
- [SQLite benchmark](sqlite-benchmark.md)
- [SQLite C extension](sqlite-c-extension.md)
- [SQLite isolation levels](sqlite-isolation-levels.md)
- [Node.js SQLite bindings](node-js-sqlite-bindings.md)
  - [`sqlite3` Node.js package](sqlite3-node-js-package.md)
  - [`better-sqlite3` Node.js package](better-sqlite3-node-js-package.md)

## 🏷️ Tagged (1)

- [D. Richard Hipp](d-richard-hipp.md)

## ↑ Ancestors (12)

1. [SQL implementation](sql-implementation.md)
2. [SQL](sql-split.md)
3. [Relational database management system](relational-database-management-system.md)
4. [Relational database](relational-database.md)
5. [Type of database](type-of-database.md)
6. [Database](database.md)
7. [Software](software-split.md)
8. [Computer](computer-split.md)
9. [Information technology](information-technology.md)
10. [Area of technology](area-of-technology.md)
11. [Technology](technology-split.md)
12. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (29)

- [nodejs/sequelize/raw/parallel_create_delete_empty_tag.js](_file/nodejs/sequelize/raw/parallel_create_delete_empty_tag.js.md)
- [Delete all duplicate rows in SQL](delete-all-duplicate-rows-in-sql.md)
- [DELETE with JOIN (SQL)](delete-with-join-sql.md)
- [Get Bitcoin transaction id from position in dat file](get-bitcoin-transaction-id-from-position-in-dat-file.md)
- [Good](good.md)
- [How to decide if an ORM is good?](how-to-decide-if-an-orm-is-good.md)
- [ISO SQL TRIGGER syntax](iso-sql-trigger-syntax.md)
- [LevelDB](leveldb.md)
- [Lujakob/nestjs-realworld-example-app SQLite port](lujakob-nestjs-realworld-example-app-sqlite-port.md)
- [Node.js SQLite bindings](node-js-sqlite-bindings.md)
- [Sequelize example](sequelize-example.md)
- [SQL 2D histogram](sql-2d-histogram.md)
- [SQL contiguous ranges](sql-contiguous-ranges.md)
- [SQL example](sql-example.md)
- [SQL histogram](sql-histogram.md)
- [SQL RECURSIVE prevent infinite recursion](sql-recursive-prevent-infinite-recursion.md)
- [SQL TRIGGER](sql-trigger.md)
- [SQL window `RANGE`](sql-window-range.md)
- [SQLite C extension](sqlite-c-extension.md)
- [SQLite import CSV](sqlite-import-csv.md)
- [SQLite import CSV from stdin](sqlite-import-csv-from-stdin.md)
- [SQLite import JSON](sqlite-import-json.md)
- [SQLite isolation levels](sqlite-isolation-levels.md)
- [`Sqlite3` Node.js package](sqlite3-node-js-package.md)
- [The horrors of Sequelize](the-horrors-of-sequelize.md)
- [The most awesome systems programmers](the-most-awesome-systems-programmers.md)
- [UNION (SQL)](union-sql.md)
- [UPDATE with JOIN (SQL)](update-with-join-sql.md)
- [Upsert](upsert.md)
