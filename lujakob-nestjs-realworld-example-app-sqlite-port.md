<h1 id="lujakob-nestjs-realworld-example-app-sqlite-port">lujakob/nestjs-realworld-example-app SQLite port</h1>

↑ **Parent:** [lujakob/nestjs-realworld-example-app](lujakob-nestjs-realworld-example-app.md)

Tried a quick port to [SQLite](sqlite.md) to get rid of annoying local databases for development, but failed, at c1c2cc4e448b279ff083272df1ac50d20c3304fa
```
npm install sqlite3 --save-dev
```
and
```
{
  "type": "sqlite",
  "database": "db.sqlite3",
  "entities": ["src/**/**.entity{.ts,.js}"],
  "synchronize": true
}
```
then:
```
npm start
```
fails with:
```
DataTypeNotSupportedError: Data type "timestamp" in "ArticleEntity.created" is not supported by "sqlite" database.
```
Attempt to hack it:
```
--- a/src/article/article.entity.ts
+++ b/src/article/article.entity.ts
@@ -20,10 +20,10 @@ export class ArticleEntity {
   @Column({default: ''})
   body: string;

-  @Column({ type: 'timestamp', default: () => "CURRENT_TIMESTAMP"})
+  @Column({ default: () => "CURRENT_TIMESTAMP"})
   created: Date;

-  @Column({ type: 'timestamp', default: () => "CURRENT_TIMESTAMP"})
+  @Column({ default: () => "CURRENT_TIMESTAMP"})
   updated: Date;
```
and after that it seems to run.

I can signup and login, terrible error reporting as usual, make sure to use long enough usernames/passwords.

However, article creation fails with:
```
Unhandled Rejection (TypeError): Cannot read property 'slug' of undefined
```

## ↑ Ancestors (13)

1. [lujakob/nestjs-realworld-example-app](lujakob-nestjs-realworld-example-app.md)
2. [Nest.js](nest-js.md)
3. [Node.js web framework](node-js-web-framework.md)
4. [Node.js](node-js-split.md)
5. [JavaScript](javascript.md)
6. [List of programming languages](list-of-programming-languages.md)
7. [Programming language](programming-language-split.md)
8. [Software](software-split.md)
9. [Computer](computer-split.md)
10. [Information technology](information-technology.md)
11. [Area of technology](area-of-technology.md)
12. [Technology](technology-split.md)
13. [Ciro Santilli's Homepage](split.md)
