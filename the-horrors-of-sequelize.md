# The horrors of Sequelize

↑ **Parent:** [Sequelize](sequelize-split.md)

- foreign keys are capitalized:
  - [https://stackoverflow.com/questions/55273091/why-use-the-uppercase-key-when-creating-association-model-in-sequelize](https://stackoverflow.com/questions/55273091/why-use-the-uppercase-key-when-creating-association-model-in-sequelize)
  - [https://github.com/sequelize/sequelize/issues/5828](https://github.com/sequelize/sequelize/issues/5828)
- you must give `foreignKey` when using aliases, otherwise it fails subtely. That would be derived automatically.
- [https://stackoverflow.com/questions/41502699/return-flat-object-from-sequelize-with-association](https://stackoverflow.com/questions/41502699/return-flat-object-from-sequelize-with-association) can't auto-flatten to reuse the database's `ORDER`
- `limit` and `offset` don't work without `subQuery: false` when doing includes! It is just too buggy. Examples of this can be found e.g. under [nodejs/sequelize/many_to_many_same_model.js](nodejs/sequelize/many_to_many_same_model.js).
- [https://stackoverflow.com/questions/34059081/how-do-i-reference-an-association-when-creating-a-row-in-sequelize-without-assum](https://stackoverflow.com/questions/34059081/how-do-i-reference-an-association-when-creating-a-row-in-sequelize-without-assum) hard to not duplicate foreign keys values everywhere
- stack traces permanently broken or requiring non-obvious configs:
  - [https://github.com/sequelize/sequelize/issues/8199#issuecomment-863943835](https://github.com/sequelize/sequelize/issues/8199#issuecomment-863943835)
  - [https://github.com/sequelize/sequelize/issues/12044](https://github.com/sequelize/sequelize/issues/12044)
  - [https://stackoverflow.com/questions/28231970/bluebird-shows-broken-stacktrace-when-using-with-sequelize-mysql](https://stackoverflow.com/questions/28231970/bluebird-shows-broken-stacktrace-when-using-with-sequelize-mysql)
- does not automatically update fields on hooks: [https://github.com/sequelize/sequelize/issues/8586#issuecomment-422877555](https://github.com/sequelize/sequelize/issues/8586#issuecomment-422877555)
- cannot change columns when other columns have constraints due to the backup table?
  - [https://stackoverflow.com/questions/64533732/process-of-changing-a-table-with-sequelize-migration-if-foreign-key-constraint-i](https://stackoverflow.com/questions/64533732/process-of-changing-a-table-with-sequelize-migration-if-foreign-key-constraint-i)
- you have to use `.get()` for `attribute` aliased fields, why? [https://stackoverflow.com/questions/32649218/how-do-i-select-a-column-using-an-alias/69890944#69890944](https://stackoverflow.com/questions/32649218/how-do-i-select-a-column-using-an-alias/69890944#69890944)
- `.id` gets added to `SELECT` no matter what, breaking `GROUP BY` unless you do horrible workarounds:
  - [https://github.com/sequelize/sequelize/issues/3256](https://github.com/sequelize/sequelize/issues/3256)
  - [https://github.com/sequelize/sequelize/issues/5481](https://github.com/sequelize/sequelize/issues/5481)
- no simple built-in mechanism for transaction retries: [Sequelize transaction retries](sequelize-transaction-retry.md)
- impossible to do subqueries in general. Docs just tell you to use literals. This in particular prevents single query deletes with join as done at [nodejs/sequelize/raw/many_to_many.js](nodejs/sequelize/raw/many_to_many.js):
  - [https://sequelize.org/master/manual/sub-queries.html](https://sequelize.org/master/manual/sub-queries.html): the docs actually just tell you to use literals, lol
  - [https://stackoverflow.com/questions/45354001/nodejs-sequelize-delete-with-nested-select-query](https://stackoverflow.com/questions/45354001/nodejs-sequelize-delete-with-nested-select-query)

  Also, you can't get query strings either: [https://github.com/sequelize/sequelize/issues/2325](https://github.com/sequelize/sequelize/issues/2325)
- migrations. Generally speaking, anything but the simplest migrations are exceedingly hard to get right, as you have to go very low level when doing migrations. Syntax can be very different from regular DB operations.
  - no way to do (non-raw) queries during migrations, e.g. to update fields based on other fields in a complex way?
    - [https://github.com/sequelize/cli/issues/862](https://github.com/sequelize/cli/issues/862)
    - [https://stackoverflow.com/questions/18742962/add-data-in-sequelize-migration-script](https://stackoverflow.com/questions/18742962/add-data-in-sequelize-migration-script)
    - [https://stackoverflow.com/questions/38671483/sequelize-migration-update-model-after-updating-column-attributes](https://stackoverflow.com/questions/38671483/sequelize-migration-update-model-after-updating-column-attributes)
    - [https://stackoverflow.com/questions/38998397/can-i-use-sequelize-models-in-migration-scripts](https://stackoverflow.com/questions/38998397/can-i-use-sequelize-models-in-migration-scripts)
    - [https://stackoverflow.com/questions/45286429/custom-query-on-sequelize-seeder](https://stackoverflow.com/questions/45286429/custom-query-on-sequelize-seeder)
    `queryInterface.sequelize.models` contains only `SequelizeMeta`. Not sure why they have this limitation.

    Edit: actually things will likely just work if immediately after making table changes you just instantiate a new sequelize and do any data changes.
  - [https://stackoverflow.com/questions/56043246/node-js-sequelize-no-primary-keys-when-migrating/56046101#56046101](https://stackoverflow.com/questions/56043246/node-js-sequelize-no-primary-keys-when-migrating/56046101#56046101)
  - [SQLite](sqlite.md) `changeColumn` migrations do on delete cascades of other tables. SQLite does not have change column statements, so they have to drop and recreate tables, but they don't temporarily remove cascades, so you lose data: [https://stackoverflow.com/questions/62667269/sequelize-js-how-do-we-change-column-type-in-migration/70486686#70486686](https://stackoverflow.com/questions/62667269/sequelize-js-how-do-we-change-column-type-in-migration/70486686#70486686)
  - associations require full explicit index construction: [https://stackoverflow.com/questions/39651853/how-to-create-join-table-with-foreign-keys-with-sequelize-or-sequelize-cli](https://stackoverflow.com/questions/39651853/how-to-create-join-table-with-foreign-keys-with-sequelize-or-sequelize-cli)
- ability to iterate over a large result without blowing up memory and without using limit + offset (which is inneficient e.g. when looping over recursive queries). This is also known as cursor or streaming interfaces:
  - stack overflow
    - [https://stackoverflow.com/questions/28787889/how-can-i-set-up-sequelize-js-to-stream-data-instead-of-a-promise-callback](https://stackoverflow.com/questions/28787889/how-can-i-set-up-sequelize-js-to-stream-data-instead-of-a-promise-callback)
    - [https://stackoverflow.com/questions/43964067/how-to-implement-cursor-pagination-using-sequelize](https://stackoverflow.com/questions/43964067/how-to-implement-cursor-pagination-using-sequelize)
    - [https://stackoverflow.com/questions/57164242/perform-sequelize-findall-in-a-huge-array](https://stackoverflow.com/questions/57164242/perform-sequelize-findall-in-a-huge-array)
    - [https://stackoverflow.com/questions/55191891/how-to-loop-through-result-in-sequelize](https://stackoverflow.com/questions/55191891/how-to-loop-through-result-in-sequelize) generic loop
  - issue tracker
    - [https://github.com/sequelize/sequelize/issues/15827](https://github.com/sequelize/sequelize/issues/15827)
    - [https://github.com/sequelize/sequelize/issues/10347](https://github.com/sequelize/sequelize/issues/10347)
    - [https://github.com/sequelize/sequelize/issues/4286](https://github.com/sequelize/sequelize/issues/4286)
    - [https://github.com/sequelize/sequelize/issues/2454](https://github.com/sequelize/sequelize/issues/2454)

  E.g. the [Python](python-programming-language.md) [SQLite](sqlite.md) interface supports this just fine: [https://stackoverflow.com/questions/29582736/python3-is-there-a-way-to-iterate-row-by-row-over-a-very-large-sqlite-table-wi](https://stackoverflow.com/questions/29582736/python3-is-there-a-way-to-iterate-row-by-row-over-a-very-large-sqlite-table-wi)
- empty `attributes: []` breaks some nested queries: [https://github.com/sequelize/sequelize/issues/16436](https://github.com/sequelize/sequelize/issues/16436)
- does not expose a iteration API that supports large arrays?
  - [https://github.com/sequelize/sequelize/issues/8550](https://github.com/sequelize/sequelize/issues/8550)
  - [https://stackoverflow.com/questions/57164242/perform-sequelize-findall-in-a-huge-array](https://stackoverflow.com/questions/57164242/perform-sequelize-findall-in-a-huge-array)

  E.g. [Python](python-programming-language.md) [SQLite](sqlite.md) does: [https://stackoverflow.com/questions/29582736/python3-is-there-a-way-to-iterate-row-by-row-over-a-very-large-sqlite-table-wi](https://stackoverflow.com/questions/29582736/python3-is-there-a-way-to-iterate-row-by-row-over-a-very-large-sqlite-table-wi)

## ↑ Ancestors (13)

1. [Sequelize](sequelize-split.md)
2. [Node.js ORM library](node-js-orm-library.md)
3. [Node.js library](node-js-library.md)
4. [Node.js](node-js-split.md)
5. [JavaScript](javascript.md)
6. [List of programming languages](list-of-programming-languages.md)
7. [Programming language](programming-language-split.md)
8. [Software](software-split.md)
9. [Computer](computer-split.md)
10. [Information technology](information-technology.md)
11. [Area of technology](area-of-technology.md)
12. [Technology](technology-split.md)
13. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (1)

- [Sequelize](sequelize-split.md)
