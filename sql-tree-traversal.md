# SQL tree traversal

↑ **Parent:** [SQL application](sql-application.md)  
🏷️ **Tags:** [Tree traversal](tree-traversal.md)

Example: [nodejs/sequelize/raw/tree.js](nodejs/sequelize/raw/tree.js)

- Implementation agnostic
  - [https://stackoverflow.com/questions/192220/what-is-the-most-efficient-elegant-way-to-parse-a-flat-table-into-a-tree](https://stackoverflow.com/questions/192220/what-is-the-most-efficient-elegant-way-to-parse-a-flat-table-into-a-tree)
  - [https://stackoverflow.com/questions/5508985/recursive-query-for-adjacency-list-to-preorder-tree-traversal-in-sql](https://stackoverflow.com/questions/5508985/recursive-query-for-adjacency-list-to-preorder-tree-traversal-in-sql) DBMS agnostic specifically asking not to modify [adjacency list](adjacency-list.md) data structure
- [Postgres](postgresql.md)
  - [https://stackoverflow.com/questions/67848017/simple-recursive-sql-query](https://stackoverflow.com/questions/67848017/simple-recursive-sql-query)
  - [https://stackoverflow.com/questions/28688264/how-to-traverse-a-hierarchical-tree-structure-structure-backwards-using-recursiv](https://stackoverflow.com/questions/28688264/how-to-traverse-a-hierarchical-tree-structure-structure-backwards-using-recursiv)
  - [https://stackoverflow.com/questions/51822070/how-can-postgres-represent-a-tree-of-row-ids](https://stackoverflow.com/questions/51822070/how-can-postgres-represent-a-tree-of-row-ids)
  - depth first
    - uspecified depth first variant
      - [https://stackoverflow.com/questions/50098759/postgres-nested-records-in-a-recursive-query-in-depth-first-manner](https://stackoverflow.com/questions/50098759/postgres-nested-records-in-a-recursive-query-in-depth-first-manner)
      - [https://stackoverflow.com/questions/59463176/how-to-perform-depth-first-search-in-postgresql](https://stackoverflow.com/questions/59463176/how-to-perform-depth-first-search-in-postgresql)
      - [https://stackoverflow.com/questions/30336265/postgresql-recursive-cte-results-ordering](https://stackoverflow.com/questions/30336265/postgresql-recursive-cte-results-ordering)
    - [preorder DFS](pre-order-depth-first-search.md)
      - [https://dba.stackexchange.com/questions/63153/how-do-i-sort-the-results-of-a-recursive-query-in-an-expanded-tree-like-fashion](https://dba.stackexchange.com/questions/63153/how-do-i-sort-the-results-of-a-recursive-query-in-an-expanded-tree-like-fashion)
      - [https://stackoverflow.com/questions/65247873/preorder-tree-traversal-using-recursive-ctes-in-sql/77276675#77276675](https://stackoverflow.com/questions/65247873/preorder-tree-traversal-using-recursive-ctes-in-sql/77276675#77276675)
  - [breadth-first](breadth-first-search.md) [https://stackoverflow.com/questions/3709292/select-rows-from-table-using-tree-order](https://stackoverflow.com/questions/3709292/select-rows-from-table-using-tree-order)
- [MySQL](mysql.md)
  - [https://stackoverflow.com/questions/8252323/mysql-closure-table-hierarchical-database-how-to-pull-information-out-in-the-c](https://stackoverflow.com/questions/8252323/mysql-closure-table-hierarchical-database-how-to-pull-information-out-in-the-c) asks how to use a specific order ([preorder DFS](pre-order-depth-first-search.md)) with [closure table](closure-table.md)
- [Microsoft SQL Server](microsoft-sql-server.md)
  - [https://stackoverflow.com/questions/14274942/sql-server-cte-and-recursion-example](https://stackoverflow.com/questions/14274942/sql-server-cte-and-recursion-example)

**Table of contents**

- [Closure table](closure-table.md)
- [Nested set model in SQL](nested-set-model-in-sql.md)

## ↑ Ancestors (12)

1. [SQL application](sql-application.md)
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

## ← Incoming links (1)

- [SQL RECURSIVE query](sql-recursive-query.md)
