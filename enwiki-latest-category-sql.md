<h1 id="enwiki-latest-category-sql">enwiki-latest-category.sql</h1>

↑ **Parent:** [Wikipedia dumps](wikipedia-dumps.md)

[https://dumps.wikimedia.org/enwiki/latest/enwiki-latest-category.sql.gz](https://dumps.wikimedia.org/enwiki/latest/enwiki-latest-category.sql.gz) contains a list of categories. It only contains the categories and some counts, but it doesn't contain the subcategories and pages under each category, so it is a bit pointless.

The schema is listed at: [https://www.mediawiki.org/wiki/Manual:Category_table](https://www.mediawiki.org/wiki/Manual:Category_table)

The SQL first defines the table:
```
CREATE TABLE `category` (
  `cat_id` int(10) unsigned NOT NULL AUTO_INCREMENT,
  `cat_title` varbinary(255) NOT NULL DEFAULT '',
  `cat_pages` int(11) NOT NULL DEFAULT 0,
  `cat_subcats` int(11) NOT NULL DEFAULT 0,
  `cat_files` int(11) NOT NULL DEFAULT 0,
  PRIMARY KEY (`cat_id`),
  UNIQUE KEY `cat_title` (`cat_title`),
  KEY `cat_pages` (`cat_pages`)
) ENGINE=InnoDB AUTO_INCREMENT=249228235 DEFAULT CHARSET=binary ROW_FORMAT=COMPRESSED;
```
followed by a few humongous inserts:
```
INSERT INTO `category` VALUES (2,'Unprintworthy_redirects',1597224,20,0),(3,'Computer_storage_devices',88,11,0)
```
which we can see at: [https://en.wikipedia.org/wiki/Category:Computer_storage_devices](https://en.wikipedia.org/wiki/Category:Computer_storage_devices)

Se see that [https://en.wikipedia.org/wiki/Category:Computer_storage_devices_by_company](https://en.wikipedia.org/wiki/Category:Computer_storage_devices_by_company)
- [https://en.wikipedia.org/wiki/Category:Computer_storage_devices](https://en.wikipedia.org/wiki/Category:Computer_storage_devices) is a subcategory of that category and it appears in that file.
- [https://en.wikipedia.org/wiki/Acronis_Secure_Zone](https://en.wikipedia.org/wiki/Acronis_Secure_Zone) is a page of the category, and it does not appear
so it contains only categories.

We can check this with:
```
sed -s 's/),/\n/g' enwiki-latest-category.sql | grep Computer_storage_devices
```
and it shows:
```
(3,'Computer_storage_devices',88,11,0
(521773,'Computer_storage_devices_by_company',6,6,0
```
There doesn't seem to be any interlink between the categories, only page and subcategory counts therefore.

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
