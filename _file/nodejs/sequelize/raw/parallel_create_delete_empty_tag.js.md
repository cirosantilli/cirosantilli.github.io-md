<h1 id="_file/nodejs/sequelize/raw/parallel_create_delete_empty_tag.js">nodejs/sequelize/raw/parallel_create_delete_empty_tag.js</h1>

↑ **Parent:** [SQL parallel update example](../../../../sql-parallel-update-example.md)

In this example, posts have tags. When a post is deleted, we check to see if there are now any empty tags, and now we want to delete any empty tags that the post deletion may have created.

If we are creating and deleting posts concurrently, a naive implementation might wrongly delete the tags of a newly created post.

This could be due to a concurrency issue of the following types.

Failure case 1:
- thread 2: delete old post
- thread 2: find all tags with 0 posts. Finds `tag0` from the deleted old post which is now empty.
- thread 1: create new post, which we want to have tag `tag0`
- thread 1: try to create a new tag `tag0`, but don't because it already exists, this is done using [SQLite](../../../../sqlite.md)'s `INSERT OR IGNORE INTO` or [PostgreSQL](../../../../postgresql.md)'s `INSERT ... ON CONFLICT DO NOTHING`
- thread 1: assign `tag0` to the new post by adding an entry to the join table
- thread 2: delete all tags with 0 posts. It still sees from its previous search that `tag0` is empty, and deletes it, which then cascades into the join table
which would result in the new post incorrectly not having the `tag0`.

Failure case 2:
- thread 2: delete old post
- thread 2: find all tags with 0 posts
- thread 1: create new post
- thread 1: try to create a new tag `tag0`, but don't because it already exists
- thread 2: delete all tags with 0 posts. It still sees from its previous search that `tag0` is empty, and deletes it
- thread 1: assign `tag0` to the new post
which leads to a foreign key failure, because the tag does not exist anymore when the assignment happens.

Failure case 3:
- thread 2: delete old post
- thread 1: create new post, which we want to have tag `tag0`
- thread 1: try to create a new tag `tag0`, and succeed because it wasn't present
- thread 2: find all tags with 0 posts, finds the tag that was just created
- thread 2: delete all tags with 0 posts, deleting the new tag
- thread 1: assign `tag0` to the new post
which leads to a foreign key failure, because the tag does not exist anymore when the assignment happens.

Sample executions:
- `node --unhandled-rejections=strict ./parallel_create_delete_empty_tag.js p 9 1000 'READ COMMITTED'`: [PostgreSQL](../../../../postgresql.md), 9 tags, DELETE/CREATE the `tag0` test tag 1000 times, use `READ COMMITTED`

  Execution often fails, although not always. The failure is always:
  ```
  error: insert or update on table "PostTag" violates foreign key constraint "PostTag_tagId_fkey"
  ```
  because the:
  ```
  INSERT INTO "PostTag"
  ```
  tries to insert a tag that was deleted in the other thread, as it didn't have any corresponding posts, so this is the foreign key failure.

  TODO: we've never managed to observe the failure case in which `tag0` is deleted. Is it truly possible? And if not, by which guarantee?
- `node --unhandled-rejections=strict ./parallel_create_delete_empty_tag.js p 9 1000 'READ COMMITTED' 'FOR UPDATE'`: do a `SELECT ... FOR UPDATE` before trying to `INSERT`.

  This is likely correct and the fastest correct method according to our quick benchmarking, about 20% faster than `REPEATABLE READ`.

  We are just now 100% sure it is corret becase we can't find out if the `SELECT` in the `DELETE` subquery could first select some rows, which are then locked by the tag creator, and only then locked by `DELETE` after selection. Or does it re-evaludate the `SELECT` even though it is in a subquery?
- `node --unhandled-rejections=strict ./parallel_create_delete_empty_tag.js p 9 1000 'REPEATABLE READ'`: repeatable read

  We've never observed any failures with this level. This should likely fix the foreign key issue according to the PostgreSQL docs, since:
  - the `DELETE "Post"` commit cannot start to be seen only in the middle of the thread 1 transaction
  - and then if DELETE happened, the thread 1 transaction will detect it, ROLLBACK, and re-run. TODO how does it detect the need rollback? Is it because of the foreign key? It is very hard to be sure about this kind of thing, just can't find the information. Related: [postgreSQL serialization failure](../../../../postgresql-serialization-failure.md).
- `node --unhandled-rejections=strict ./parallel_create_delete_empty_tag.js p 9 1000 'SERIALIZABLE'`: serializable
- `node --unhandled-rejections=strict ./parallel_create_delete_empty_tag.js p 9 1000 'NONE'`: magic value, don't use any transaction. Can blow up of course, since even less restrictions than `READ COMMITTED`
All executions use 2 threads.

Some theoretical notes:
- Failure case 3 is averted by a `READ COMMITTED` transaction, because thread 2 won't see the uncommitted tag that thread 1 created, and therefore won't be able to delete it

[https://stackoverflow.com/questions/10935850/when-to-use-select-for-update](https://stackoverflow.com/questions/10935850/when-to-use-select-for-update) from [SELECT FOR UPDATE](../../../../select-for-update.md) also talks about a similar example, and has relevant answers.

## ↑ Ancestors (16)

1. [SQL parallel update example](../../../../sql-parallel-update-example.md)
2. [SQL isolation level example](../../../../sql-isolation-level-example.md)
3. [SQL transaction isolation level](../../../../sql-transaction-isolation-level.md)
4. [SQL transaction](../../../../sql-transaction.md)
5. [SQL feature](../../../../sql-feature.md)
6. [SQL](../../../../sql-split.md)
7. [Relational database management system](../../../../relational-database-management-system.md)
8. [Relational database](../../../../relational-database.md)
9. [Type of database](../../../../type-of-database.md)
10. [Database](../../../../database.md)
11. [Software](../../../../software-split.md)
12. [Computer](../../../../computer-split.md)
13. [Information technology](../../../../information-technology.md)
14. [Area of technology](../../../../area-of-technology.md)
15. [Technology](../../../../technology-split.md)
16. [Ciro Santilli's Homepage](../../../../split.md)

## ← Incoming links (2)

- [nodejs/sequelize/raw/parallel_update_async.js](parallel_update_async.js.md)
- [SQL REPEATABLE READ isolation level](../../../../sql-repeatable-read-isolation-level.md)
