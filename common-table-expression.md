# Common Table Expression

↑ **Parent:** [SQL subquery](sql-subquery.md)

Similar to [SQL subquery](sql-subquery.md), but with some differences: [https://stackoverflow.com/questions/706972/difference-between-cte-and-subquery](https://stackoverflow.com/questions/706972/difference-between-cte-and-subquery)

```
rm -f tmp.sqlite
sqlite3 tmp.sqlite 'create table t(i integer)'
sqlite3 tmp.sqlite 'insert into t values (1), (2)'
sqlite3 tmp.sqlite 'with mycte as ( select * from t ) delete from mycte where i = 1'
sqlite3 tmp.sqlite 'select * from t'
```

**Table of contents**

- [CTE insert values](cte-insert-values.md)

## ↑ Ancestors (13)

1. [SQL subquery](sql-subquery.md)
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
