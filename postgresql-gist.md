# PostgreSQL GIST

↑ **Parent:** [PostgreSQL spatial index](postgresql-spatial-index.md)

- [https://www.postgresql.org/docs/15/gist.html](https://www.postgresql.org/docs/15/gist.html)
- [https://www.postgresql.org/docs/15/datatype-geometric.html](https://www.postgresql.org/docs/15/datatype-geometric.html)
- [https://medium.com/postgres-professional/indexes-in-postgresql-5-gist-86e19781b5db](https://medium.com/postgres-professional/indexes-in-postgresql-5-gist-86e19781b5db) the only example on the net!

The highly underdocumented built-in module, that supports [SQL spatial index](sql-spatial-index.md) and a lot more.

Quite horrendous as it only seems to work on geometric types and not existing columns. But why.

And it uses custom operatores, where standard operators would have been just fine for points...

Minimal runnable example with points:
```
set -x
time psql -c 'drop table if exists t'
time psql -c 'create table t(p point)'
time psql -c "insert into t select (point ('(' || generate_series || ',' || generate_series || ')')) from generate_series(1, 10000000)"
time psql -c 'create index on t using gist(p)'
time psql -c "select count(*) from t where p <@ box '(1000000,1000000),(9000000,2000000)'"
```
The index creation unfortunately took 100s, so it will not scale to 1B points very well whic his a shame.

Some sources about it:
- [https://stackoverflow.com/questions/28292198/how-to-port-simple-spatial-index-using-sqlite-r-trees-to-postgres](https://stackoverflow.com/questions/28292198/how-to-port-simple-spatial-index-using-sqlite-r-trees-to-postgres)

## ↑ Ancestors (14)

1. [PostgreSQL spatial index](postgresql-spatial-index.md)
2. [SQL spatial index](sql-spatial-index.md)
3. [SQL feature](sql-feature.md)
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
