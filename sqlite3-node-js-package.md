<h1 id="sqlite3-node-js-package"><code>sqlite3</code> Node.js package</h1>

↑ **Parent:** [Node.js SQLite bindings](node-js-sqlite-bindings.md)

- [https://github.com/mapbox/node-sqlite3](https://github.com/mapbox/node-sqlite3)
- [https://www.npmjs.com/package/sqlite3](https://www.npmjs.com/package/sqlite3)

Includes its own copy of sqlite3, you don't use the system one, which is good to ensure compatibility. The version is shown at: [https://github.com/mapbox/node-sqlite3/blob/918052b538b0effe6c4a44c74a16b2749c08a0d2/deps/common-sqlite.gypi#L3](https://github.com/mapbox/node-sqlite3/blob/918052b538b0effe6c4a44c74a16b2749c08a0d2/deps/common-sqlite.gypi#L3) [SQLite](sqlite.md) source is tracked compressed in-tree: [https://github.com/mapbox/node-sqlite3/blob/918052b538b0effe6c4a44c74a16b2749c08a0d2/deps/sqlite-autoconf-3360000.tar.gz](https://github.com/mapbox/node-sqlite3/blob/918052b538b0effe6c4a44c74a16b2749c08a0d2/deps/sqlite-autoconf-3360000.tar.gz) horrendous. This explains why it takes forever to clone that repository. People who don't believe in git submodules, there's even an official Git mirror at: [https://github.com/sqlite/sqlite](https://github.com/sqlite/sqlite)

It appears to spawn its own [threads](thread-computing.md) via its [C](c-programming-language.md) extension (since [JavaScript is single threaded](javascript-is-single-threaded.md) and and [SQLite](sqlite.md) is not [server](server-computing.md)-based), which allows for parallel queries using multiple threads: [https://github.com/mapbox/node-sqlite3/blob/v5.0.2/src/threading.h](https://github.com/mapbox/node-sqlite3/blob/v5.0.2/src/threading.h)

Hello world example: [nodejs/node-sqlite3/index.js](nodejs/node-sqlite3/index.js).

As of 2021, this had slumped back a bit, as maintainers got tired. Unmerged pull requests started piling more, and [`better-sqlite3` Node.js package](better-sqlite3-node-js-package.md) started pulling ahead a little.
- [https://github.com/mapbox/node-sqlite3/issues/1381](https://github.com/mapbox/node-sqlite3/issues/1381) `FATAL ERROR: Error::ThrowAsJavaScriptException napi_throw` with [Node.js `worker_threads`](node-js-worker-threads.md) vs [`better-sqlite3` Node.js package](better-sqlite3-node-js-package.md) [https://github.com/JoshuaWise/better-sqlite3/issues/237](https://github.com/JoshuaWise/better-sqlite3/issues/237)

## ↑ Ancestors (14)

1. [Node.js SQLite bindings](node-js-sqlite-bindings.md)
2. [SQLite](sqlite.md)
3. [SQL implementation](sql-implementation.md)
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

## ← Incoming links (2)

- [nodejs/sequelize/raw/parallel_update_async.js](_file/nodejs/sequelize/raw/parallel_update_async.js.md)
- [SQL example](sql-example.md)
