<h1 id="row-number"><code>ROW_NUMBER</code></h1>

↑ **Parent:** [Window function (SQL)](window-function-sql.md)


```
sqlite3 ':memory:'  'WITH t (i) AS (VALUES (-1), (-1), (-2)) SELECT *, row_number() over () FROM t'
```
Possible output:
```
-1|1
-1|2
-2|3
```
Gives them unique IDs.

With a `partition by`:
```
sqlite3 ':memory:'  'WITH t (i) AS (VALUES (-1), (-1), (-2)) SELECT *, row_number() over ( partition by i ) FROM t'
```
possible output:
```
-2|1
-1|1
-1|2
```

## ↑ Ancestors (13)

1. [Window function (SQL)](window-function-sql.md)
2. [SQL feature](sql-feature.md)
3. [SQL](sql-split.md)
4. [Relational database management system](relational-database-management-system.md)
5. [Relational database](relational-database.md)
6. [Type of database](type-of-database.md)
7. [Database](database.md)
8. [Software](software-split.md)
9. [Computer](computer-split.md)
10. [Information technology](information-technology.md)
11. [Area of technology](area-of-technology.md)
12. [Technology](technology-split.md)
13. [Ciro Santilli's Homepage](split.md)
