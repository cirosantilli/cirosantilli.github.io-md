# OurBigBook Library tested on PostgreSQL

↑ **Parent:** [Advances](advances.md)

<a id="_27"></a>
After something broke on the website due to SQLite vs PostgreSQL inconsistencies and took me a day to figure it out, I finally decided to update the test system so that `OURBIGBOOK_POSTGRES=true npm test` will run the tests on PostgreSQL.

<a id="_28"></a>
Originally, these were being run only on SQLite, which is the major use case for OurBigBook CLI, which came before the website.

<a id="_29"></a>
But the website runs on PostgreSQL, so it is fundamental to test things in PostgreSQL as well.

## ↑ Ancestors (7)

1. [Advances](advances.md)
2. [Ourbigbook.com](ourbigbook-com.md)
3. [Ciro's Edict \#5](../5-split.md)
4. [Sponsor updates](../../../sponsor-updates.md)
5. [Update from Ciro Santilli](../../../update-from-ciro-santilli.md)
6. [Ciro Santilli](../../../ciro-santilli-split.md)
7. [Ciro Santilli's Homepage](../../../split.md)
