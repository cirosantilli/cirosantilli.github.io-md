# PostgreSQL logging

↑ **Parent:** [PostgreSQL](postgresql.md)

[https://stackoverflow.com/questions/722221/how-to-log-postgresql-queries](https://stackoverflow.com/questions/722221/how-to-log-postgresql-queries)

[Ubuntu 21.10](ubuntu-21-10.md) has a certain default level of logging by default to:
```
/var/log/postgresql/postgresql-13-main.log
```
but it does not log everything, only/mostly errors it seems.

Setting:
```
log_statement = 'all'
```
under:
```
/etc/postgresql/13/main/postgresql.conf
```
and then restarting the server:
```
sudo service restart postgresql
```
just works.

Realtime monitoring for long queries instead: [https://stackoverflow.com/questions/8597516/app-to-monitor-postgresql-queries-in-real-time](https://stackoverflow.com/questions/8597516/app-to-monitor-postgresql-queries-in-real-time)

## ↑ Ancestors (13)

1. [PostgreSQL](postgresql.md)
2. [SQL implementation](sql-implementation.md)
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
