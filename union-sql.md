# UNION (SQL)

↑ **Parent:** [SQL keyword](sql-keyword.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Set_operations_(SQL)#UNION_operator)

Basic example tested on [SQLite](sqlite.md) 3.40.1, [Ubuntu 23.04](ubuntu-23-04.md):
```
sqlite3 :memory: 'select 1 union select 2'
```
output:
```
1
2
```

Two columns two rows:
```
sqlite3 :memory: <<EOF
select * from (values (1, 2), (2, 3))
union
select * from (values (2, 3), (3, 4))
EOF
```
output:
```
1|2
2|3
3|4
```

Note how duplicates are removed, to keep them we `UNION ALL` instead:
```
sqlite3 :memory: <<EOF
select * from (values (1, 2), (2, 3))
union all
select * from (values (2, 3), (3, 4))
EOF
```
output:
```
1|2
2|3
2|3
3|4
```

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
