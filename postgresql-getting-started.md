# PostgreSQL getting started

↑ **Parent:** [PostgreSQL](postgresql.md)

On Ubuntu 20.10 PostgreSQL 12.6, login with `psql` on my default username without [sudo](sudo.md) fails with: [https://stackoverflow.com/questions/11919391/postgresql-error-fatal-role-username-does-not-exist](https://stackoverflow.com/questions/11919391/postgresql-error-fatal-role-username-does-not-exist)

This is the one that worked on [Ubuntu 21.04](ubuntu-21-04.md): [https://stackoverflow.com/questions/11919391/postgresql-error-fatal-role-username-does-not-exist/38444152#38444152](https://stackoverflow.com/questions/11919391/postgresql-error-fatal-role-username-does-not-exist/38444152#38444152)
```
sudo -u postgres createuser -s $(whoami)
createdb $(whoami)
```
Explanation:
- `sudo -u postgres` uses the `postgres` user via [peer authentication](peer-authentication.md)
- `-s` in `createuser -s`: make it a superuser
- `createdb`: TODO why do we have to create a table with the same name as the user? Otherwise login fails.

You can now run `psql` without any password. This works without password due to peer authentication:
```
sudo cat /etc/postgresql/12/main/pg_hba.conf
```
shows that peer authentication is available to all users apparently:
```
local   all             postgres                                peer

# TYPE  DATABASE        USER            ADDRESS                 METHOD

# "local" is for Unix domain socket connections only
local   all             all                                     peer
```

List users:
```
psql -c '\du'
```
output:
```
                                    List of roles
  Role name  |                         Attributes                         | Member of
-------------+------------------------------------------------------------+-----------
 ciro        | Superuser, Create role, Create DB                          | {}
 owning_user |                                                            | {}
 postgres    | Superuser, Create role, Create DB, Replication, Bypass RLS | {}
```

Delete user later on:
```
psql -c 'DROP USER username;'
```

Create a database:
```
createdb testdb0
```

Help toplevel:
```
help
```

Get help for Postgres commands such as `\h` and so on:
```
\?
```

List supported SQL commands:
```
\h
```

Show syntax for one type of command:
```
\h SELECT
```

List all databases:
```
psql -c '\l'
```
which shows:
```
    Name     |  Owner   | Encoding |   Collate   |    Ctype    |   Access privileges
-------------+----------+----------+-------------+-------------+-----------------------
 ciro        | postgres | UTF8     | en_GB.UTF-8 | en_GB.UTF-8 |
 postgres    | postgres | UTF8     | en_GB.UTF-8 | en_GB.UTF-8 |
 template0   | postgres | UTF8     | en_GB.UTF-8 | en_GB.UTF-8 | =c/postgres          +
             |          |          |             |             | postgres=CTc/postgres
 template1   | postgres | UTF8     | en_GB.UTF-8 | en_GB.UTF-8 | =c/postgres          +
             |          |          |             |             | postgres=CTc/postgres
 testdb0     | postgres | UTF8     | en_GB.UTF-8 | en_GB.UTF-8 |
(6 rows)
```

Delete a database:
```
psql -c 'DROP DATABASE "testdb0";'
```

If you didn't give a database from the command line e.g.:
```
psql
```
you can do that afterwards with:
```
\c testdb0
```

Let's create a table and test that it is working:
```
psql testdb0 -c 'CREATE TABLE table0 (int0 INT, char0 CHAR(16));'
```

List tables, no special tables:
```
psql testdb0 -c '\dt'
```
gives:
```
        List of relations
 Schema |  Name  | Type  | Owner
--------+--------+-------+-------
 public | table0 | table | ciro
(1 row)
```

View table schema: [https://stackoverflow.com/questions/109325/postgresql-describe-table](https://stackoverflow.com/questions/109325/postgresql-describe-table)
```
psql testdb0 -c '\d+ table0'
```
output:
```
                                      Table "public.table0"
 Column |     Type      | Collation | Nullable | Default | Storage  | Stats target | Description
--------+---------------+-----------+----------+---------+----------+--------------+-------------
 int0   | integer       |           |          |         | plain    |              |
 char0  | character(16) |           |          |         | extended |              |
```

Insert some data into it and get the data out:
```
psql testdb0 -c "INSERT INTO table0 (int0, char0) VALUES (2, 'two'), (3, 'three'), (5, 'five'), (7, 'seven');"
psql testdb0 -c 'SELECT * FROM table0;'
```
output:
```
 int0 |      char0
------+------------------
    2 | two
    3 | three
    5 | five
    7 | seven
(4 rows)
```

Delete the table:
```
psql testdb0 -c 'DROP TABLE table0;'
```

**Table of contents**

- [PostgreSQL HOWTO](postgresql-howto.md)
  - [PostgreSQL create test data](postgresql-create-test-data.md)
    - [Generate random text in PostgreSQL](generate-random-text-in-postgresql.md)
  - [PostgreSQL full-text search](postgresql-full-text-search.md)

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
