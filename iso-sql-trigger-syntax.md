# ISO SQL TRIGGER syntax

↑ **Parent:** [SQL keyword](sql-keyword.md)  
🏷️ **Tags:** [Database trigger](database-trigger.md), [SQL standard](sql-standard.md)

TODO what is the standard compliant syntax?

[PostgreSQL](postgresql.md) requires you to define a [SQL stored procedure](sql-stored-procedure.md): [https://stackoverflow.com/questions/28149494/is-it-possible-to-create-trigger-without-execute-procedure-in-postgresql](https://stackoverflow.com/questions/28149494/is-it-possible-to-create-trigger-without-execute-procedure-in-postgresql) Their syntax may be standard compliant, not sure about the `EXECUTE` part. Their docs: [https://www.postgresql.org/docs/current/sql-createtrigger.html](https://www.postgresql.org/docs/current/sql-createtrigger.html)

[SQLite](sqlite.md) does not support [SQL stored procedures](sql-stored-procedure.md) at all, so maybe that's why they can't be standard compliant here: [https://stackoverflow.com/questions/3335162/creating-stored-procedure-in-sqlite](https://stackoverflow.com/questions/3335162/creating-stored-procedure-in-sqlite)

[SQL:1999](sql-1999.md) 11.38 covers "Trigger definition". The [Abstract syntax tree](abstract-syntax-tree.md) starts with the `CREATE TRIGGER` and ends in:
```
<triggered SQL statement> ::=
  <SQL procedure statement>
```

This is defined at 13.5 "SQL procedure statement", but that is humongous and I'm not sure what it is at all.

**Table of contents**

- [nodejs/sequelize/raw/trigger\_count.js](_file/nodejs/sequelize/raw/trigger_count.js.md)

## ↑ Ancestors (12)

1. [SQL keyword](sql-keyword.md)
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
