# MySQL

↑ **Parent:** [SQL implementation](sql-implementation.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/MySQL)

Login without password: [https://askubuntu.com/questions/915585/how-to-login-mysql-shell-when-mysql-have-no-password](https://askubuntu.com/questions/915585/how-to-login-mysql-shell-when-mysql-have-no-password)
```
sudo mysql
```
works on [Ubuntu](ubuntu.md) 20.10.

Create user for further logins without `sudo` [https://askubuntu.com/questions/915585/how-to-login-mysql-shell-when-mysql-have-no-password/1325689#1325689](https://askubuntu.com/questions/915585/how-to-login-mysql-shell-when-mysql-have-no-password/1325689#1325689):
```
sudo mysql -e "CREATE USER $USER"
```

Run command from CLI [https://stackoverflow.com/questions/1602904/how-do-you-run-a-single-query-through-mysql-from-the-command-line](https://stackoverflow.com/questions/1602904/how-do-you-run-a-single-query-through-mysql-from-the-command-line)
```
mysql -e 'SHOW DATABASES'
```

Create test user with password:
```
sudo mysql -e 'CREATE USER user0 IDENTIFIED WITH mysql_native_password BY "a"'
sudo mysql -e 'GRANT ALL PRIVILEGES ON database_name.* TO "user0"'
```
and login as that user:
```
mysql -u user0 -p
```
Login with password given on the command line:
```
mysql -u user0 -pmypassword
```
The `IDENTIFIED WITH mysql_native_password` part is to overcome "Client does not support authentication protocol requested by server" when connecting from [Node.js](node-js-split.md).

List users:
```
sudo mysql -e 'SELECT * FROM mysql.user'
```

View permissions for each user on each DB: [https://serverfault.com/questions/263868/how-to-know-all-the-users-that-can-access-a-database-mysql](https://serverfault.com/questions/263868/how-to-know-all-the-users-that-can-access-a-database-mysql)
```
sudo mysql -e 'SELECT * FROM mysql.db'
```

List databases:
```
sudo mysql -e 'SHOW DATABASES'
```

Create database:
```
sudo mysql -e 'CREATE DATABASE mydb0'
```

Destroy database:
```
sudo mysql -e 'DROP DATABASE mydb0'
```

Show tables in database:
```
sudo mysql -e 'SHOW TABLES' mydb0
```
or:
```
sudo mysql -e 'SHOW TABLES FROM mydb0'
```

**Table of contents**

- [mysqldump](mysqldump.md)
  - [mysqldump to CSV](mysqldump-to-csv.md)
- [MariaDB](mariadb.md)

## ↑ Ancestors (12)

1. [SQL implementation](sql-implementation.md)
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

## ← Incoming links (5)

- [Database management system](database-management-system.md)
- [Download all Wikipedia categories](download-all-wikipedia-categories.md)
- [PostgreSQL](postgresql.md)
- [SQL histogram](sql-histogram.md)
- [SQL tree traversal](sql-tree-traversal.md)
