<h1 id="postgresql-generate-series">PostgreSQL <code>generate_series</code></h1>

↑ **Parent:** [PostgreSQL function](postgresql-function.md)

[https://www.postgresql.org/docs/17/functions-srf.html](https://www.postgresql.org/docs/17/functions-srf.html)

Pattern you always want to generate [Generate random text in PostgreSQL](generate-random-text-in-postgresql.md):
```
CREATE TABLE "mytable" ("i" INTEGER, "j" INTEGER);
INSERT INTO "mytable" SELECT i, i*2 FROM generate_series(1, 10) as s(i);
```

## ↑ Ancestors (14)

1. [PostgreSQL function](postgresql-function.md)
2. [PostgreSQL](postgresql.md)
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
