# Skip ID extraction and rendering based on database timestamps

↑ **Parent:** [Advances](advances.md)

<a id="_10"></a>
Now that we can reliably split files at will with `\Include`, I finally added this feature.

<a id="_11"></a>
This means while developing a website locally with the [OurBigBook CLI](../../../ourbigbook-cli.md), if you have a bunch of files with an error in one of them, your first run will run slowly until the error:<a id="_12"></a>

```
extract_ids README.ciro
extract_ids README.ciro finished in 73.82836899906397 ms
extract_ids art.ciro
extract_ids art.ciro finished in 671.1738419979811 ms
extract_ids ciro-santilli.ciro
extract_ids ciro-santilli.ciro finished in 1009.6256089992821 ms
extract_ids science.ciro
error: science.ciro:13686:1: named argument "parent" given multiple times
extract_ids science.ciro finished in 1649.6193730011582 ms
```
but further runs will blast through the files that worked, skipping all files that have sucessfully converted:<a id="_13"></a>

```
extract_ids README.ciro
extract_ids README.ciro skipped by timestamp
extract_ids art.ciro
extract_ids art.ciro skipped by timestamp
extract_ids ciro-santilli.ciro
extract_ids ciro-santilli.ciro skipped by timestamp
extract_ids science.ciro
```
so you can fix file by file and move on quickly.

<a id="_14"></a>
More details at: [https://cirosantilli.com/ourbigbook#no-render-timestamp](https://cirosantilli.com/ourbigbook#no-render-timestamp)

<a id="_15"></a>
This was not fully trivial to implement because we had to rework how duplicate IDs are checked. Previously, we just nuked the DB every time on a directory conversion, and then repopulated everything. If a duplicated showed up on a file, it was a duplicate.

<a id="_16"></a>
But now that we are not necessarily extracing IDs from every file, we can't just nuke the database anymore, otherwise we'd lose the information. Therefore, what we have to do is to convert every file, and only at the end check the duplicates.

<a id="_17"></a>
Managed to do that with a single query as documented at: [https://stackoverflow.com/questions/71235548/how-to-find-all-rows-that-have-certain-columns-duplicated-in-sequelize/71235550#71235550](https://stackoverflow.com/questions/71235548/how-to-find-all-rows-that-have-certain-columns-duplicated-in-sequelize/71235550#71235550)

## ↑ Ancestors (7)

1. [Advances](advances.md)
2. [Ourbigbook.com](ourbigbook-com.md)
3. [Ciro's Edict \#5](../5-split.md)
4. [Sponsor updates](../../../sponsor-updates.md)
5. [Update from Ciro Santilli](../../../update-from-ciro-santilli.md)
6. [Ciro Santilli](../../../ciro-santilli-split.md)
7. [Ciro Santilli's Homepage](../../../split.md)
