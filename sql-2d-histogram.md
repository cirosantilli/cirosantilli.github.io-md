# SQL 2D histogram

↑ **Parent:** [SQL histogram](sql-histogram.md)

Let's try it on [SQLite](sqlite.md) 3.40.1, [Ubuntu 23.04](ubuntu-23-04.md). Data setup:
```
sqlite3 tmp.sqlite 'create table t(x integer, y integer)'
sqlite3 tmp.sqlite <<EOF
insert into t values
  (0, 0),
  (1, 1),
  (2, 2),
  (3, 3),
  (4, 4),
  (5, 5),
  (6, 6),
  (7, 7),
  (8, 8),
  (9, 9),
  (10, 10),
  (11, 11),
  (12, 12),
  (13, 13),
  (14, 14),
  (15, 15),
  (16, 16),
  (17, 17),
  (18, 18),
  (19, 19),

  (2, 18)
EOF
sqlite3 tmp.sqlite 'create index txy on t(x, y)'
```

For a bin size of 5 ignoring empty ranges we can:
```
sqlite3 tmp.sqlite <<EOF
select
  floor(x/5)*5 as x,
  floor(y/5)*5 as y,
  count(*) as cnt
from t
group by 1, 2
order by 1, 2
EOF
```
which produces the desired:
```
0|0|5
0|15|1
5|5|5
10|10|5
15|15|5
```

And to consider empty ranges we can use [SQL `genenerate_series`](sql-genenerate-series.md) + as per [https://stackoverflow.com/questions/72367652/populating-empty-bins-in-a-histogram-generated-using-sql](https://stackoverflow.com/questions/72367652/populating-empty-bins-in-a-histogram-generated-using-sql):
```
sqlite3 tmp.sqlite <<EOF
select x, y, sum(cnt) from (
  select
      floor(x/5)*5 as x,
      floor(y/5)*5 as y,
      count(*) as cnt
    from t
    group by 1, 2
  union
  select *, 0 as cnt from generate_series(0, 15, 5) inner join (select * from generate_series(0, 15, 5))
)
group by x, y
EOF
```
which outputs the desired:
```
0|0|5
0|5|0
0|10|0
0|15|1
5|0|0
5|5|5
5|10|0
5|15|0
10|0|0
10|5|0
10|10|5
10|15|0
15|0|0
15|5|0
15|10|0
15|15|5
```

## ↑ Ancestors (13)

1. [SQL histogram](sql-histogram.md)
2. [SQL application](sql-application.md)
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
