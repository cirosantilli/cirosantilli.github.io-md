# SQL histogram

↑ **Parent:** [SQL application](sql-application.md)

OK, there's a billion questions:
- [SQL Server](oracle-database.md)
  - [https://stackoverflow.com/questions/485409/generating-a-histogram-from-column-values-in-a-database](https://stackoverflow.com/questions/485409/generating-a-histogram-from-column-values-in-a-database) OP did not know the difference between count and histogram :-) But it's the number one Google result.
  - [https://stackoverflow.com/questions/19103991/create-range-bins-from-sql-server-table-for-histograms](https://stackoverflow.com/questions/19103991/create-range-bins-from-sql-server-table-for-histograms) has a minor extra group by twist, but otherwise fine
  - [https://stackoverflow.com/questions/16268441/generate-histogram-in-sql-server](https://stackoverflow.com/questions/16268441/generate-histogram-in-sql-server)
- [SQLite](sqlite.md)
  - [https://stackoverflow.com/questions/67514208/how-to-optimise-creating-histogram-bins-in-sqlite](https://stackoverflow.com/questions/67514208/how-to-optimise-creating-histogram-bins-in-sqlite) perf only, benchmarking would be needed. [SQLite](sqlite.md).
  - [https://stackoverflow.com/questions/32155449/create-a-histogram-with-a-dynamic-number-of-partitions-in-sqlite](https://stackoverflow.com/questions/32155449/create-a-histogram-with-a-dynamic-number-of-partitions-in-sqlite) variable bin size, same number of entries per bin
  - [https://stackoverflow.com/questions/60348109/histogram-for-time-periods-using-sqlite-regular-buckets-1h-wide](https://stackoverflow.com/questions/60348109/histogram-for-time-periods-using-sqlite-regular-buckets-1h-wide) time
- [MySQL](mysql.md): [https://stackoverflow.com/questions/1764881/getting-data-for-histogram-plot](https://stackoverflow.com/questions/1764881/getting-data-for-histogram-plot) MySQL appears to extend `ROUND` to also round by integers: `ROUND(numeric_value, -2)`, but this is not widely portable which is a shame
- [https://stackoverflow.com/questions/72367652/populating-empty-bins-in-a-histogram-generated-using-sql](https://stackoverflow.com/questions/72367652/populating-empty-bins-in-a-histogram-generated-using-sql) specifically asks about empty bins, which is amazing. [Amazon Redshift](amazon-redshift.md) dialect unfortunately, but answer provided works widely, and Redshift was forked from [PostgreSQL](postgresql.md), so there's hope. Those newb [open source](open-source-software.md) server focused projects that don't use [AGPL](affero-general-public-license.md)!

Let's try it on [SQLite](sqlite.md) 3.40.1, [Ubuntu 23.04](ubuntu-23-04.md). Data setup:
```
sqlite3 tmp.sqlite 'create table t(x integer)'
sqlite3 tmp.sqlite <<EOF
insert into t values (
  0,
  2,
  2,
  3,

  5,
  6,
  6,
  8,
  9,

  17,
)
EOF
sqlite3 tmp.sqlite 'create index tx on t(x)'
```

For a bin size of 5 ignoring empty ranges we can:
```
sqlite3 tmp.sqlite <<EOF
select floor(x/5)*5 as x,
       count(*) as cnt
from t
group by 1
order by 1
EOF
```
which produces the desired:
```
0|4
5|5
15|1
```

And to consider empty ranges we can use [SQL `genenerate_series`](sql-genenerate-series.md) + as per [https://stackoverflow.com/questions/72367652/populating-empty-bins-in-a-histogram-generated-using-sql](https://stackoverflow.com/questions/72367652/populating-empty-bins-in-a-histogram-generated-using-sql):
```
sqlite3 tmp.sqlite <<EOF
select x, sum(cnt) from (
  select floor(x/5)*5 as x,
         count(*) as cnt
    from t
    group by 1
  union
  select *, 0 as cnt from generate_series(0, 15, 5)
)
group by x
EOF
```
which outputs the desired:
```
0|4
5|5
10|0
15|1
```

**Table of contents**

- [SQL 2D histogram](sql-2d-histogram.md)

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
