# Sequelize

↑ **Parent:** [Node.js ORM library](node-js-orm-library.md)

Source code: [https://github.com/sequelize/sequelize](https://github.com/sequelize/sequelize)

Some usage examples under: [Section "Sequelize example"](sequelize-example.md).

As of 2021, this library is extremely painful to use. It does feel semi-mature, but there are just too much horrible things going on;
- the documentation is a bit messy and misses a lot of stuff. The examples are often too short, and it is hard to understand what specific options they are talking about do because they lack clear input/expected output pairs. Examples:
  - [https://github.com/sequelize/sequelize/issues/5385#issuecomment-324479607](https://github.com/sequelize/sequelize/issues/5385#issuecomment-324479607)
  - [https://github.com/sequelize/sequelize/issues/1775#issuecomment-360028396](https://github.com/sequelize/sequelize/issues/1775#issuecomment-360028396)
- the implementation has several inelegant/unintuitive annoyances/requirements of code repetition that drive you mad.

  The association API feels notably bad, it took a few days for [Ciro Santilli](ciro-santilli-split.md) to learn to do what he considers "basic" association operations, knowledge which he dumped to: [https://stackoverflow.com/questions/22958683/how-to-implement-many-to-many-association-in-sequelize/67973948#67973948](https://stackoverflow.com/questions/22958683/how-to-implement-many-to-many-association-in-sequelize/67973948#67973948)

  See also: [how to decide if an ORM is good?](how-to-decide-if-an-orm-is-good.md).
- bugs are piling up. It appears that many key devs left, and current maintainers are just not being able to keep up.

  And they have setup a stupid bot that closes every thread automatically after a few days, what's the point... valid bugs are being closed due to this, and it is impossible to distinguish what is solved and what isn't since everything gets closed.

Some glaring issues are listed at [the horrors of Sequelize](the-horrors-of-sequelize.md).

**Table of contents**

- [The horrors of Sequelize](the-horrors-of-sequelize.md)
- [Sequelize example](sequelize-example.md)
  - [Sequelize raw query](sequelize-raw-query.md)
  - [UPDATE with JOIN in Sequelize](update-with-join-in-sequelize.md)
  - [Sequelize parallel example](sequelize-parallel-example.md)
    - [nodejs/sequelize/parallel\_select\_and\_update.js](_file/nodejs/sequelize/parallel_select_and_update.js.md)
- [Sequelize transaction retry](sequelize-transaction-retry.md)
- [SQL TRIGGER in Sequelize](sql-trigger-in-sequelize.md)

## ↑ Ancestors (12)

1. [Node.js ORM library](node-js-orm-library.md)
2. [Node.js library](node-js-library.md)
3. [Node.js](node-js-split.md)
4. [JavaScript](javascript.md)
5. [List of programming languages](list-of-programming-languages.md)
6. [Programming language](programming-language-split.md)
7. [Software](software-split.md)
8. [Computer](computer-split.md)
9. [Information technology](information-technology.md)
10. [Area of technology](area-of-technology.md)
11. [Technology](technology-split.md)
12. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (15)

- [nodejs/sequelize/parallel_select_and_update.js](_file/nodejs/sequelize/parallel_select_and_update.js.md)
- [`Better-sqlite3` Node.js package](better-sqlite3-node-js-package.md)
- [DELETE with JOIN (SQL)](delete-with-join-sql.md)
- [feathers-chat PostgreSQL](feathers-chat-postgresql.md)
- [FeathersJS](feathersjs.md)
- [How to decide if an ORM is good?](how-to-decide-if-an-orm-is-good.md)
- [OurBigBook.com](ourbigbook-com-top-project.md)
- [Sigoden/node-express-realworld-example-app](sigoden-node-express-realworld-example-app.md)
- [Further improvements to the website's base technology](sponsor/updates/4/further-improvements-to-the-website-s-base-technology.md)
- [SQL example](sql-example.md)
- [SQL TRIGGER](sql-trigger.md)
- [SQL TRIGGER in Sequelize](sql-trigger-in-sequelize.md)
- [UPDATE with JOIN (SQL)](update-with-join-sql.md)
- [Generating test data for full text search tests](updates/generating-test-data-for-full-text-search-tests.md)
- [webpack](webpack-split.md)
