# Sequelize example

↑ **Parent:** [Sequelize](sequelize-split.md)

To run examples on a specific database:
- `./index.js` or `./index.js l`: [SQLite](sqlite.md)
- `./index.js p`: [PostgreSQL](postgresql.md). You must manually create a database called `tmp` and ensure that peer authentication works for it
All examples can be tested on all databases with:
```
cd sequelize
./test
```

Overview of the examples:
- [nodejs/sequelize/index.js](nodejs/sequelize/index.js): a bunch of basic examples
- [nodejs/sequelize/update.js](nodejs/sequelize/update.js): This file is also where we are storing our expression-foo for now, e.g. how to do stuff like `col1 + col2`. Such knowledge can however be used basically anywhere else however, e.g. in `AS` or `WHERE` clauses, not just in `UPDATE`.
  - [https://stackoverflow.com/questions/54898994/bulkupdate-in-sequelize-orm/69044138#69044138](https://stackoverflow.com/questions/54898994/bulkupdate-in-sequelize-orm/69044138#69044138)
  - [https://stackoverflow.com/questions/55646233/updating-with-calculated-values-in-sequelize](https://stackoverflow.com/questions/55646233/updating-with-calculated-values-in-sequelize)
- [nodejs/sequelize/count.js](nodejs/sequelize/count.js): a simplified single-table count example. In practice, this will be usually done together with [JOIN](join-sql.md) queries across multiple tables. Answers: [https://stackoverflow.com/questions/22627258/how-does-group-by-works-in-sequelize/69896449#69896449](https://stackoverflow.com/questions/22627258/how-does-group-by-works-in-sequelize/69896449#69896449)
- [nodejs/sequelize/date.js](nodejs/sequelize/date.js): automatic date typecasts
- [nodejs/sequelize/like.js](nodejs/sequelize/like.js): [LIKE](like-sql.md)
- [nodejs/sequelize/camel_case.js](nodejs/sequelize/camel_case.js): trying to get everything in the database camel cased, columns starting with lowercase, and tables starting with uppercase. The defaults documented on getting started documentation do uppercase foreign keys, and lowercase non-foreign keys. It's a mess.
- [nodejs/sequelize/ignore_duplicates.js](nodejs/sequelize/ignore_duplicates.js): ignore query on unique violation with `ignoreDuplicates: true` which does [SQLite](sqlite.md) `INSERT OR IGNORE INTO` or [PostgreSQL](postgresql.md) `ON CONFLICT DO NOTHING`. Closely related [Upsert](upsert.md) versions:
  - [Upsert](upsert.md)
    - [nodejs/sequelize/upsert.js](nodejs/sequelize/upsert.js): `.upsert` selects the conflict column automatically by unique columns. Both [SQLite](sqlite.md) and [PostgreSQL](postgresql.md) do `INSERT INTO ON CONFLICT`. PostgreSQL uses `RETURNING`, which was added too recently to SQLite: [https://www.sqlite.org/lang_returning.html](https://www.sqlite.org/lang_returning.html)

      At [nodejs/sequelize/composite_index.js](nodejs/sequelize/composite_index.js) we have a `.upsert` test with a composite index. Works just fine as you'd expect with a composite `ON CONFLICT`. Well done.
    - [nodejs/sequelize/update_on_duplicate.js](nodejs/sequelize/update_on_duplicate.js): `.bulkCreate({}, { updateOnDuplicate: ['col1', col2'] }`. Produces queries analogous to `.upsert`. This method is cool because it can upsert multiple columns at once. But it is annoying that you have to specify all fields to be updated one by one manually.
    - [https://stackoverflow.com/questions/29063232/how-to-get-the-id-of-an-inserted-or-updated-record-in-sequelize-upsert/72092277#72092277](https://stackoverflow.com/questions/29063232/how-to-get-the-id-of-an-inserted-or-updated-record-in-sequelize-upsert/72092277#72092277)
    - [https://stackoverflow.com/questions/55531860/sequelize-bulkcreate-updateonduplicate-for-postgresql](https://stackoverflow.com/questions/55531860/sequelize-bulkcreate-updateonduplicate-for-postgresql)
- [nodejs/sequelize/inc.js](nodejs/sequelize/inc.js): demonstrate the `increment` method. In [SQLite](sqlite.md), it produces a statement of type:
  ```
  UPDATE `IntegerNames` SET `value`=`value`+ 1,`updatedAt`='2021-11-03 10:23:45.409 +00:00' WHERE `id` = 3
  ```
- [nodejs/sequelize/sync_alter.js](nodejs/sequelize/sync_alter.js): illustrates `Model.sync({alter: true})` to modify a table definition, answers: [https://stackoverflow.com/questions/54898994/bulkupdate-in-sequelize-orm/69044138#69044138](https://stackoverflow.com/questions/54898994/bulkupdate-in-sequelize-orm/69044138#69044138)
- [nodejs/sequelize/truncate_key.js](nodejs/sequelize/truncate_key.js)
- [nodejs/sequelize/validation.js](nodejs/sequelize/validation.js): is handled by a third-party library: [https://github.com/validatorjs/validator.js](https://github.com/validatorjs/validator.js). They then add a few extra validators on top of that.

  The `args: true` thing is explained at: [https://stackoverflow.com/questions/58522387/unhandled-rejection-sequelizevalidationerror-validation-error-cannot-create-pr/70263032#70263032](https://stackoverflow.com/questions/58522387/unhandled-rejection-sequelizevalidationerror-validation-error-cannot-create-pr/70263032#70263032)
- [nodejs/sequelize/composite_index.js](nodejs/sequelize/composite_index.js): [https://stackoverflow.com/questions/34664853/sequelize-composite-unique-constraint](https://stackoverflow.com/questions/34664853/sequelize-composite-unique-constraint)
- [nodejs/sequelize/indent_log.js](nodejs/sequelize/indent_log.js): [https://stackoverflow.com/questions/34664853/sequelize-composite-unique-constraint](https://stackoverflow.com/questions/34664853/sequelize-composite-unique-constraint)
- association examples:
  - [nodejs/sequelize/one_to_many.js](nodejs/sequelize/one_to_many.js): basic [one-to-many](one-to-many.md) examples.
    - [nodejs/sequelize/one_to_many_custom_column_name.js](nodejs/sequelize/one_to_many_custom_column_name.js):
      - [https://stackoverflow.com/questions/43025861/sequelize-association-is-referencing-to-wrong-foreignkey-column-name](https://stackoverflow.com/questions/43025861/sequelize-association-is-referencing-to-wrong-foreignkey-column-name)
      - [https://stackoverflow.com/questions/49818406/sequelize-targetkey-not-working/59953948#59953948](https://stackoverflow.com/questions/49818406/sequelize-targetkey-not-working/59953948#59953948)
  - [nodejs/sequelize/many_to_many.js](nodejs/sequelize/many_to_many.js): basic [many-to-many](many-to-many.md) examples, each user can like multiple posts. Answers: [https://stackoverflow.com/questions/22958683/how-to-implement-many-to-many-association-in-sequelize/67973948#67973948](https://stackoverflow.com/questions/22958683/how-to-implement-many-to-many-association-in-sequelize/67973948#67973948)
    - ORDER BY include:
      - [https://github.com/sequelize/sequelize/issues/4553](https://github.com/sequelize/sequelize/issues/4553)
      - [https://stackoverflow.com/questions/66984410/why-the-sequelize-include-order-does-not-work](https://stackoverflow.com/questions/66984410/why-the-sequelize-include-order-does-not-work)
    - [nodejs/sequelize/many_to_many_custom_table.js](nodejs/sequelize/many_to_many_custom_table.js): [many-to-many](many-to-many.md) example, but where we craft our own table which can hold extra data. In our case, users can like posts, but likes have a integer weight associated with them. Related threads:
      - [https://stackoverflow.com/questions/22958683/how-to-implement-many-to-many-association-in-sequelize/67973948#67973948](https://stackoverflow.com/questions/22958683/how-to-implement-many-to-many-association-in-sequelize/67973948#67973948)
      - [https://stackoverflow.com/questions/30308217/sequelize-find-by-association-through-manually-defined-join-table/69899876#69899876](https://stackoverflow.com/questions/30308217/sequelize-find-by-association-through-manually-defined-join-table/69899876#69899876)
    - [nodejs/sequelize/many_to_many_same_model.js](nodejs/sequelize/many_to_many_same_model.js): association between a model and itself: users can follow other users. Related:
      - [https://stackoverflow.com/questions/43152180/node-sequelize-followering-following-relationship](https://stackoverflow.com/questions/43152180/node-sequelize-followering-following-relationship)
      - [https://stackoverflow.com/questions/27065154/how-to-get-all-children-or-parents-in-a-many-to-many-association-if-one-model-re/72951602#72951602](https://stackoverflow.com/questions/27065154/how-to-get-all-children-or-parents-in-a-many-to-many-association-if-one-model-re/72951602#72951602)
      - [https://github.com/sequelize/sequelize/issues/8263](https://github.com/sequelize/sequelize/issues/8263)
    - [nodejs/sequelize/many_to_many_same_model_super.js](nodejs/sequelize/many_to_many_same_model_super.js)
      - [nodejs/sequelize/find_duplicates.js](nodejs/sequelize/find_duplicates.js): [https://stackoverflow.com/questions/71235548/how-to-find-all-rows-that-have-certain-columns-duplicated-in-sequelize/71235550#71235550](https://stackoverflow.com/questions/71235548/how-to-find-all-rows-that-have-certain-columns-duplicated-in-sequelize/71235550#71235550)
    - [nodejs/sequelize/many_to_many_super.js](nodejs/sequelize/many_to_many_super.js): "Super many to many": [https://sequelize.org/master/manual/advanced-many-to-many.html](https://sequelize.org/master/manual/advanced-many-to-many.html) This should not exist and shows how bad this library is for associations, you need all that boilerplate in order to expose certain relationships that aren't otherwise exposed by a direct `hasMany` with implicit join table.
  - nested includes to produce queries with multiple [JOIN](join-sql.md):
    - [nodejs/sequelize/nested_include.js](nodejs/sequelize/nested_include.js): find all posts by users that a given user follows. Answers: [https://stackoverflow.com/questions/42632943/sequelize-multiple-where-clause/68018083#68018083](https://stackoverflow.com/questions/42632943/sequelize-multiple-where-clause/68018083#68018083)
    - [nodejs/sequelize/nested_include_super.js](nodejs/sequelize/nested_include_super.js): like [nodejs/sequelize/nested_include.js](nodejs/sequelize/nested_include.js) but with a super many to many. We should move this to [nodejs/sequelize/many_to_many_super.js](nodejs/sequelize/many_to_many_super.js).
  - two relationships between two specific tables: we need to use `as:` to disambiguate them
    - [nodejs/sequelize/many_to_many_double.js](nodejs/sequelize/many_to_many_double.js): users can both follow and like posts
    - [nodejs/sequelize/one_to_many_double.js](nodejs/sequelize/one_to_many_double.js): posts have the author and a mandatory reviewer
- hooks
  - [nodejs/sequelize/before_validate_modify.js](nodejs/sequelize/before_validate_modify.js):
    - [https://github.com/sequelize/sequelize/issues/3534](https://github.com/sequelize/sequelize/issues/3534)
    - [https://github.com/sequelize/sequelize/issues/8586](https://github.com/sequelize/sequelize/issues/8586)
  - [nodejs/sequelize/hook_in_transaction.js](nodejs/sequelize/hook_in_transaction.js):
    - [https://stackoverflow.com/questions/35014679/sequelize-hook-depending-on-transaction](https://stackoverflow.com/questions/35014679/sequelize-hook-depending-on-transaction)
  - [nodejs/sequelize/hook_abort.js](nodejs/sequelize/hook_abort.js): aborting updates from hooks: [https://stackoverflow.com/questions/64362298/how-to-abort-an-update-operation-with-beforeupdate-hook-sequelize/71308632#71308632](https://stackoverflow.com/questions/64362298/how-to-abort-an-update-operation-with-beforeupdate-hook-sequelize/71308632#71308632)
- internals:
  - [nodejs/sequelize/common.js](nodejs/sequelize/common.js): common utilities used across examples, most notably:
    - to easily setup different DBRM
  - [nodejs/sequelize/min_nocommon.js](nodejs/sequelize/min_nocommon.js): to copy paste to [Stack Overflow](stack-overflow-split.md)
  - [nodejs/sequelize/min.js](nodejs/sequelize/min.js): template for new exapmles in the folder

**Table of contents**

- [Sequelize raw query](sequelize-raw-query.md)
- [UPDATE with JOIN in Sequelize](update-with-join-in-sequelize.md)
- [Sequelize parallel example](sequelize-parallel-example.md)
  - [nodejs/sequelize/parallel\_select\_and\_update.js](_file/nodejs/sequelize/parallel_select_and_update.js.md)

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

## ← Incoming links (2)

- [Sequelize](sequelize-split.md)
- [SQL example](sql-example.md)
