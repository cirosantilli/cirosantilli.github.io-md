# SQL contiguous ranges

↑ **Parent:** [Window function (SQL)](window-function-sql.md)

[https://stackoverflow.com/questions/17046204/how-to-find-the-boundaries-of-groups-of-contiguous-sequential-numbers/17046749#17046749](https://stackoverflow.com/questions/17046204/how-to-find-the-boundaries-of-groups-of-contiguous-sequential-numbers/17046749#17046749) just works, even in [SQLite](sqlite.md) which supports all quoting types known to man including `[]` for compatibility with insane [RDBMSs](relational-database-management-system.md)!

Here's a slightly saner version:
```
rm -f tmp.sqlite
sqlite3 tmp.sqlite "create table mytable (id integer primary key autoincrement, number integer, status integer)"
sqlite3 tmp.sqlite <<EOF
insert into mytable(number, status) values
  (100,0),
  (101,0),
  (102,0),
  (103,0),
  (104,1),
  (105,1),
  (106,0),
  (107,0),
  (1014,0),
  (1015,0),
  (1016,1),
  (1017,0)
EOF
sqlite3 tmp.sqlite <<EOF
SELECT
  MIN(id) AS "id",
  MIN(number) AS "from",
  MAX(number) AS "to"
FROM (
  SELECT ROW_NUMBER() OVER (ORDER BY number) - number AS grp, id, number
  FROM mytable
  WHERE status = 0
)
GROUP BY grp
ORDER BY MIN(number)
EOF
```

output:

```
1|100|103
7|106|107
9|1014|1015
12|1017|1017
```

To get only groups of length greater than 1:
```
sqlite3 tmp.sqlite <<EOF
SELECT "id", "from", "to", "to" - "from" + 1 as "len" FROM (
  SELECT
    MIN("id") AS "id",
    MIN(number) AS "from",
    MAX(number) AS "to"
  FROM (
    SELECT ROW_NUMBER() OVER (ORDER BY "number") - "number" AS "grp", "id", "number"
    FROM "mytable"
    WHERE "status" = 0
  )
  GROUP BY "grp"
  ORDER BY MIN("number")
) WHERE "len" > 1
EOF
```

Output:
```
1|100|103|4
7|106|107|2
9|1014|1015|2
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
