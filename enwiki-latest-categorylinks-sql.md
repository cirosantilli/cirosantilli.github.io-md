<h1 id="enwiki-latest-categorylinks-sql">enwiki-latest-categorylinks.sql</h1>

↑ **Parent:** [Wikipedia dumps](wikipedia-dumps.md)

[https://dumps.wikimedia.org/enwiki/latest/enwiki-latest-categorylinks.sql.gz](https://dumps.wikimedia.org/enwiki/latest/enwiki-latest-categorylinks.sql.gz)

The schema is listed at: [https://www.mediawiki.org/wiki/Manual:Categorylinks_table](https://www.mediawiki.org/wiki/Manual:Categorylinks_table)

On the SQL:
```
CREATE TABLE `categorylinks` (
  `cl_from` int(8) unsigned NOT NULL DEFAULT 0,
  `cl_to` varbinary(255) NOT NULL DEFAULT '',
  `cl_sortkey` varbinary(230) NOT NULL DEFAULT '',
  `cl_timestamp` timestamp NOT NULL DEFAULT current_timestamp() ON UPDATE current_timestamp(),
  `cl_sortkey_prefix` varbinary(255) NOT NULL DEFAULT '',
  `cl_collation` varbinary(32) NOT NULL DEFAULT '',
  `cl_type` enum('page','subcat','file') NOT NULL DEFAULT 'page',
  PRIMARY KEY (`cl_from`,`cl_to`),
  KEY `cl_timestamp` (`cl_to`,`cl_timestamp`),
  KEY `cl_sortkey` (`cl_to`,`cl_type`,`cl_sortkey`,`cl_from`),
  KEY `cl_collation_ext` (`cl_collation`,`cl_to`,`cl_type`,`cl_from`)
) ENGINE=InnoDB DEFAULT CHARSET=binary ROW_FORMAT=COMPRESSED;
```

TODO what is `cl_from`? We've tried:
- `page_id`: nope, there is not `page_id` of 3

`cl_to` appears to always be a category string name.

The format appears to be described at: [https://www.mediawiki.org/wiki/Manual:Categorylinks_table](https://www.mediawiki.org/wiki/Manual:Categorylinks_table)

A sample INSERT entry is:
```
(3,'Computer_storage_devices',88,11,0)
```

## ↑ Ancestors (9)

1. [Wikipedia dumps](wikipedia-dumps.md)
2. [Wikipedia](wikipedia.md)
3. [List of Wikis](list-of-wikis.md)
4. [Wiki](wiki.md)
5. [Collaborative writing platform](collaborative-writing-platform.md)
6. [Website genre](website-genre.md)
7. [Website](website-split.md)
8. [Art](art-split.md)
9. [Ciro Santilli's Homepage](split.md)
