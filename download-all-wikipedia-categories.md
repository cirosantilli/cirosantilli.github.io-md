# Download all Wikipedia categories

↑ **Parent:** [Wikipedia HOWTO](wikipedia-howto.md)

Our WIP script: [wikipedia/import-categories.sh](wikipedia/import-categories.sh).

Related:
- [https://opendata.stackexchange.com/questions/1533/download-wikipedia-articles-from-a-specific-category](https://opendata.stackexchange.com/questions/1533/download-wikipedia-articles-from-a-specific-category)
- [https://webapps.stackexchange.com/questions/16359/is-there-a-way-to-download-a-list-of-all-wikipedia-categories/172480#172480](https://webapps.stackexchange.com/questions/16359/is-there-a-way-to-download-a-list-of-all-wikipedia-categories/172480#172480)
- [https://stackoverflow.com/questions/40119322/how-to-download-all-pages-inside-a-category-in-wikipedia](https://stackoverflow.com/questions/40119322/how-to-download-all-pages-inside-a-category-in-wikipedia)
- category tree on Stack Overflow
  - [https://stackoverflow.com/questions/17432254/wikipedia-category-hierarchy-from-dumps/77313490#77313490](https://stackoverflow.com/questions/17432254/wikipedia-category-hierarchy-from-dumps/77313490#77313490) Canon but no good answers.
  - [https://stackoverflow.com/questions/12227134/how-to-fetch-category-tree-of-wiki](https://stackoverflow.com/questions/12227134/how-to-fetch-category-tree-of-wiki)
  - [https://stackoverflow.com/questions/21782410/finding-subcategories-of-a-wikipedia-category-using-category-and-categorylinks-t](https://stackoverflow.com/questions/21782410/finding-subcategories-of-a-wikipedia-category-using-category-and-categorylinks-t). Actually explains it: [https://stackoverflow.com/questions/21782410/finding-subcategories-of-a-wikipedia-category-using-category-and-categorylinks-t/21798259#21798259](https://stackoverflow.com/questions/21782410/finding-subcategories-of-a-wikipedia-category-using-category-and-categorylinks-t/21798259#21798259)
  - [https://stackoverflow.com/questions/27279649/how-to-build-wikipedia-category-hierarchy](https://stackoverflow.com/questions/27279649/how-to-build-wikipedia-category-hierarchy)
- [https://mdkzaman.com/knowledge-graph-from-wikipedia-category-hierarchy/](https://mdkzaman.com/knowledge-graph-from-wikipedia-category-hierarchy/)

Consider:
- [https://en.wikipedia.org/wiki/Category:Computer_storage_devices](https://en.wikipedia.org/wiki/Category:Computer_storage_devices)
- [https://en.wikipedia.org/wiki/Category:Computer_data_storage](https://en.wikipedia.org/wiki/Category:Computer_data_storage)
- [https://en.wikipedia.org/wiki/Computer_storage_devices](https://en.wikipedia.org/wiki/Computer_storage_devices) which redirects to: [https://en.wikipedia.org/wiki/Computer_data_storage](https://en.wikipedia.org/wiki/Computer_data_storage)

Jewish\_physicists

Let's observe them in [MySQL](mysql.md):
```
mysql enwiki -e "select page_id, page_namespace, page_title, page_is_redirect from page where page_namespace in (0, 14) and page_title in ('Computer_storage_devices', 'Computer_data_storage')"
```
outputs:
```
+----------+----------------+--------------------------+------------------+
| page_id  | page_namespace | page_title               | page_is_redirect |
+----------+----------------+--------------------------+------------------+
|     5300 |              0 | Computer_data_storage    |                0 |
| 42371130 |              0 | Computer_storage_devices |                1 |
|   711721 |             14 | Computer_data_storage    |                0 |
|   895945 |             14 | Computer_storage_devices |                0 |
+----------+----------------+--------------------------+------------------+
```


```
mysql enwiki -e "select cl_from, cl_to from categorylinks where cl_from in (5300, 711721, 895945, 42371130)"
```
gives:
```
+----------+-----------------------------------------------------------------------+
| cl_from  | cl_to                                                                 |
+----------+-----------------------------------------------------------------------+
|     5300 | All_articles_containing_potentially_dated_statements                  |
|     5300 | Articles_containing_potentially_dated_statements_from_2009            |
|     5300 | Articles_containing_potentially_dated_statements_from_2011            |
|     5300 | Articles_with_GND_identifiers                                         |
|     5300 | Articles_with_NKC_identifiers                                         |
|     5300 | Articles_with_short_description                                       |
|     5300 | Computer_architecture                                                 |
|     5300 | Computer_data_storage                                                 |
|     5300 | Short_description_matches_Wikidata                                    |
|     5300 | Use_dmy_dates_from_June_2020                                          |
|     5300 | Wikipedia_articles_incorporating_text_from_the_Federal_Standard_1037C |
|   711721 | Computer_architecture                                                 |
|   711721 | Computer_data                                                         |
|   711721 | Computer_hardware_by_type                                             |
|   711721 | Data_storage                                                          |
|   895945 | Computer_data_storage                                                 |
|   895945 | Computer_peripherals                                                  |
|   895945 | Recording_devices                                                     |
| 42371130 | Redirects_from_alternative_names                                      |
+----------+-----------------------------------------------------------------------+
```

So we see that `cl_from` encodes the parent categories:
- parent categories of categories:
  - [https://en.wikipedia.org/wiki/Category:Computer_data_storage](https://en.wikipedia.org/wiki/Category:Computer_data_storage), which has ID `711721`, has parent categories: "Computer hardware by type", "Computer data", "Data storage", "Computer architecture". This matches exactly on the database. These are all encoded on the source code of the page:
    ```
    {{DEFAULTSORT:Storage}}
    [[Category:Computer hardware by type]]
    [[Category:Computer data|Storage]]
    [[Category:Data storage|Computer]]
    [[Category:Computer architecture]]
    ```
  - [https://en.wikipedia.org/wiki/Category:Computer_storage_devices](https://en.wikipedia.org/wiki/Category:Computer_storage_devices) has parent categories: "Computer data storage", "Recording devices", "Computer peripherals". This matches exactly on the database.
- parent categories of pages:
  - [https://en.wikipedia.org/wiki/Computer_storage_devices](https://en.wikipedia.org/wiki/Computer_storage_devices) whish is a redirect gets the magic category "Redirects\_from\_alternative\_names", a humongous placeholder with many thousands of pages: [https://en.wikipedia.org/wiki/Category:Redirects_from_alternative_names](https://en.wikipedia.org/wiki/Category:Redirects_from_alternative_names)
  - [https://en.wikipedia.org/wiki/Computer_data_storage](https://en.wikipedia.org/wiki/Computer_data_storage) shows only two categories onthe web UI: "Computer data storage" and "Computer architecture". Both of these are present on the database and at the end of the source code:
    ```
    {{DEFAULTSORT:Computer Data Storage}}
    [[Category:Computer data storage| ]]
    [[Category:Computer architecture]]
    ```

    The others appear to be more magic. Two of them we can guess from the templates:
    ```
    {{short description|Storage of digital data readable by computers}}
    {{Use dmy dates|date=June 2020}}
    ```

    are likely `Use_dmy_dates_from_June_2020` and `Articles_with_short_description` but the rest is more magic and not necessarily present in-source.

So to find all articls and categories under a given category title, say [https://en.wikipedia.org/wiki/Category:Mathematics](https://en.wikipedia.org/wiki/Category:Mathematics) we can run:
```
mariadb enwiki -e "select cl_from, cl_to, page_namespace, page_title from categorylinks inner join page on page_namespace in (0, 14) and cl_from = page_id and cl_to = 'Mathematics'"
```

## ↑ Ancestors (9)

1. [Wikipedia HOWTO](wikipedia-howto.md)
2. [Wikipedia](wikipedia.md)
3. [List of Wikis](list-of-wikis.md)
4. [Wiki](wiki.md)
5. [Collaborative writing platform](collaborative-writing-platform.md)
6. [Website genre](website-genre.md)
7. [Website](website-split.md)
8. [Art](art-split.md)
9. [Ciro Santilli's Homepage](split.md)
