# Create a test user in PostgreSQL

↑ **Parent:** [PostgreSQL](postgresql.md)

In order to create a test user with password instead of [peer authentication](peer-authentication.md), let's create test user:
```
createuser -P user0
createdb user0
```
`-P` makes it prompt for the users password.

Alternatively, to create the password non-interactively [https://stackoverflow.com/questions/42419559/postgres-createuser-with-password-from-terminal](https://stackoverflow.com/questions/42419559/postgres-createuser-with-password-from-terminal):
```
psql -c "create role NewRole with login password 'secret'"
```
Can't find a way using the `createuser` helper.

We can then login with that password with:
```
psql -U user0 -h localhost
```
which asks for the password we've just set, because the `-h` option turns off peer authentication, and turns off password authentication.

The password can be given non-interactively as shown at [https://stackoverflow.com/questions/6405127/how-do-i-specify-a-password-to-psql-non-interactively](https://stackoverflow.com/questions/6405127/how-do-i-specify-a-password-to-psql-non-interactively) with the `PGPASSWORD` [environment variable](environment-variable.md):
```
PGPASSWORD=a psql -U user0 -h localhost
```

Now let's create a test database which `user0` can access with an existing superuser account:
```
createdb user0db0
psql -c 'GRANT ALL PRIVILEGES ON DATABASE user0db0 TO user0'
```

We can check this permission with:
```
psql -c '\l'
```
which now contains:
```
                                  List of databases
   Name    |  Owner   | Encoding |   Collate   |    Ctype    |   Access privileges
-----------+----------+----------+-------------+-------------+-----------------------
 user0db0  | ciro     | UTF8     | en_GB.UTF-8 | en_GB.UTF-8 | =Tc/ciro             +
           |          |          |             |             | ciro=CTc/ciro        +
           |          |          |             |             | user0=CTc/ciro
```
The permission letters are explained at:
- [https://www.postgresql.org/docs/13/ddl-priv.html](https://www.postgresql.org/docs/13/ddl-priv.html)
- [https://stackoverflow.com/questions/25691037/postgresql-permissions-explained/25691587](https://stackoverflow.com/questions/25691037/postgresql-permissions-explained/25691587)

`user0` can now do the usual table operations on that table:
```
PGPASSWORD=a psql -U user0 -h localhost user0db0 -c 'CREATE TABLE table0 (int0 INT, char0 CHAR(16));'
PGPASSWORD=a psql -U user0 -h localhost user0db0 -c "INSERT INTO table0 (int0, char0) VALUES (2, 'two'), (3, 'three'), (5, 'five'), (7, 'seven');"
PGPASSWORD=a psql -U user0 -h localhost user0db0 -c 'SELECT * FROM table0;'
```

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
