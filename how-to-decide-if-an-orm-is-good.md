# How to decide if an ORM is good?

↑ **Parent:** [Object-relational mapping](object-relational-mapping.md)

How to decide if an ORM is decent? Just try to replicate every [SQL](sql-split.md) query from [nodejs/sequelize/raw/many_to_many.js](nodejs/sequelize/raw/many_to_many.js) on [PostgreSQL](postgresql.md) and [SQLite](sqlite.md).

There is only a very finite number of possible reasonable queries on a two table many to many relationship with a join table. A decent ORM _has_ to be able to do them all.

If it can do all those queries, then the ORM can actually do a good subset of SQL and is decent. If not, it can't, and this will make you suffer. E.g. [Sequelize](sequelize-split.md) v5 is such an ORM that makes you suffer.

The next thing to check are transactions.

Basically, all of those come up if you try to implement a blog [hello world](hello-world-program.md) world such as [gothinkster/realworld](gothinkster-realworld.md) _correctly_, i.e. without unnecessary inefficiencies due to your ORM on top of underlying SQL, and dealing with concurrency.

## ↑ Ancestors (8)

1. [Object-relational mapping](object-relational-mapping.md)
2. [Database](database.md)
3. [Software](software-split.md)
4. [Computer](computer-split.md)
5. [Information technology](information-technology.md)
6. [Area of technology](area-of-technology.md)
7. [Technology](technology-split.md)
8. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (1)

- [Sequelize](sequelize-split.md)
