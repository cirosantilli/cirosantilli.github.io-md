# SQL window `RANGE`

↑ **Parent:** [Window function (SQL)](window-function-sql.md)

- [SQLite](sqlite.md): [https://www.sqlite.org/windowfunctions.html#exprrange](https://www.sqlite.org/windowfunctions.html#exprrange)

```
rm -f tmp.sqlite
sqlite3 tmp.sqlite "create table t (id integer, val integer)"
sqlite3 tmp.sqlite <<EOF
insert into t values
  (0, 0),
  (1, 5),
  (2, 10),
  (3, 14),
  (4, 15),
  (5, 16),
  (6, 20),
  (7, 25),
  (8, 29),
  (9, 30),
  (10, 30),
  (11, 31),
  (12, 35),
  (13, 40)
EOF
```

Show how many neighbours each column has with `val` between `val - 2` and `val + 2` inclusive:
```
sqlite3 tmp.sqlite <<EOF
SELECT id, val, COUNT(*) OVER (
  ORDER BY val RANGE BETWEEN 2 PRECEDING AND 2 FOLLOWING
) FROM t;
EOF
```
Output:
```
0|0|1
1|5|1
2|10|1
3|14|3
4|15|3
5|16|3
6|20|1
7|25|1
8|29|4
9|30|4
10|30|4
11|31|4
12|35|1
13|40|1
```

`val - 1` and `val + 1` inclusive instead:
```
sqlite3 tmp.sqlite <<EOF
SELECT id, val, COUNT(*) OVER (
  ORDER BY val RANGE BETWEEN 1 PRECEDING AND 1 FOLLOWING
) FROM t;
EOF
```
Output:
```
0|0|1
1|5|1
2|10|1
3|14|2
4|15|3
5|16|2
6|20|1
7|25|1
8|29|3
9|30|4
10|30|4
11|31|3
12|35|1
13|40|1
```

There seems to be no analogue to [HAVING](having-sql.md) for window functions, so we can just settle for a subquery for once, e.g.:
```
sqlite3 tmp.sqlite <<EOF
SELECT * FROM (
  SELECT id, val, COUNT(*) OVER (
    ORDER BY val RANGE BETWEEN 1 PRECEDING AND 1 FOLLOWING
  ) as c FROM t
) WHERE c > 2
EOF
```
which outputs:
```
4|15|3
8|29|3
9|30|4
10|30|4
11|31|3
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
