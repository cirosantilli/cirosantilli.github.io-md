# MongoDB

↑ **Parent:** [NoSQL](nosql.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/MongoDB)

List databases:
```
echo 'show dbs' | mongo
```

Delete database:
```
use mydb
db.dropDatabase()
```
or:
```
echo 'db.dropDatabase()' | mongo mydb
```

View collections within a database:
```
echo 'db.getCollectionNames()' | mongo mydb
```

Show all data from one of the collections: [https://stackoverflow.com/questions/24985684/mongodb-show-all-contents-from-all-collections](https://stackoverflow.com/questions/24985684/mongodb-show-all-contents-from-all-collections)
```
echo 'db.collectionName.find()' | mongo mydb
```

**Table of contents**

- [Install MongoDB on Ubuntu](install-mongodb-on-ubuntu.md)

## ↑ Ancestors (9)

1. [NoSQL](nosql.md)
2. [Type of database](type-of-database.md)
3. [Database](database.md)
4. [Software](software-split.md)
5. [Computer](computer-split.md)
6. [Information technology](information-technology.md)
7. [Area of technology](area-of-technology.md)
8. [Technology](technology-split.md)
9. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (3)

- [Randyscotsmithey/feathers-realworld-example-app](randyscotsmithey-feathers-realworld-example-app.md)
- [Server Side Public License](server-side-public-license.md)
- [The Math Genome Project](the-math-genome-project.md)
