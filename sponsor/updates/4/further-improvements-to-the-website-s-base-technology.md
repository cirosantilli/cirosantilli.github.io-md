<h1 id="further-improvements-to-the-website-s-base-technology">Further improvements to the website's base technology</h1>

↑ **Parent:** [Advances](advances.md)

<a id="_36"></a>
[https://github.com/cirosantilli/node-express-sequelize-nextjs-realworld-example-app](https://github.com/cirosantilli/node-express-sequelize-nextjs-realworld-example-app) contains the same baseline tech as OurBigBook, and I have been use to quickly test/benchmark new concepts for the website base.

<a id="_37"></a>
I'm almost proud about that project, as a reasonable template for a Next.js project. It is not perfect, notably see issues on the issue tracker, but it it quite reasonable.

<a id="_38"></a>
[The side effects of ambitious goals are often the most valuable thing achieved](../../../the-side-effects-of-ambitious-goals-are-often-the-most-valuable-thing-achieved.md) once again? I to actually make the project be more important thatn the side effects this time, but we'll see.

<a id="_39"></a>
Since the last update, I've made some major improvements to the baseline tech of the website, which I'll move little by little into OurBigBook. Some of the improvements actually started in OurBigBook.com. The improvements were:<a id="_40"></a>

<a id="_41"></a>
- got a satisfactorily comprehensive linting working at: [this commit](https://github.com/cirosantilli/node-express-sequelize-nextjs-realworld-example-app/commit/bf2eec3537a70e56b89e6e3cc3e546610cf8f51c). Nothing is easy, not even that! Part of the wisdom extracted to: [https://stackoverflow.com/questions/58233482/next-js-setting-up-eslint-for-nextjs/70519682#70519682](https://stackoverflow.com/questions/58233482/next-js-setting-up-eslint-for-nextjs/70519682#70519682).
<a id="_42"></a>
- fully rationalized directory structure to avoid nasty errors that show up in [Next.js](../../../next-js.md) when accidentally requiring backend stuff on the client. [Commit](https://github.com/cirosantilli/node-express-sequelize-nextjs-realworld-example-app/commit/67962af74b5c7e5efe9b3af168763d16a2e7c9f0). A detailed explanation of this was extracted to: [https://stackoverflow.com/questions/64926174/module-not-found-cant-resolve-fs-in-next-js-application/70363153#70363153](https://stackoverflow.com/questions/64926174/module-not-found-cant-resolve-fs-in-next-js-application/70363153#70363153).
<a id="_43"></a>
- create an extremely clean and rationalized way to do API tests from a simple `npm test`. These now actually start a clean server, and make full HTTP requests to that server. [Commit](https://github.com/cirosantilli/node-express-sequelize-nextjs-realworld-example-app/commit/9ee4962b04d75399bf8ab04ae0540e5d039cff45). Wisdom extracted to: [https://stackoverflow.com/questions/63762896/whats-the-best-way-to-test-express-js-api/70479940#70479940](https://stackoverflow.com/questions/63762896/whats-the-best-way-to-test-express-js-api/70479940#70479940).
<a id="_44"></a>
- greatly reduce the number of SQL queries, fully understood every problem <a id="_45"></a>

  <a id="_46"></a>
  - <a id="_47"></a>
    more intelligently using JOINs where I have managed to get [Sequelize](../../../sequelize-split.md) to do what I fucking want. This also led to several sequelize Stack Overflow answers as usual: [https://stackoverflow.com/search?tab=newest&q=user%3a895245%20%5bsequelize%5d](https://stackoverflow.com/search?tab=newest&q=user%3a895245%20%5bsequelize%5d)

    <a id="_48"></a>
    Everything that I didn't manage to do because of crappy sequelize is documented at: [https://github.com/cirosantilli/node-express-sequelize-nextjs-realworld-example-app/issues/5](https://github.com/cirosantilli/node-express-sequelize-nextjs-realworld-example-app/issues/5)
  <a id="_49"></a>
  - better understanding Next.js/React/useSWR do avoid doing double API queries

## ↑ Ancestors (7)

1. [Advances](advances.md)
2. [Ourbigbook.com](ourbigbook-com.md)
3. [Ciro's Edict \#4](../4-split.md)
4. [Sponsor updates](../../../sponsor-updates.md)
5. [Update from Ciro Santilli](../../../update-from-ciro-santilli.md)
6. [Ciro Santilli](../../../ciro-santilli-split.md)
7. [Ciro Santilli's Homepage](../../../split.md)

## ← Incoming links (1)

- [Ourbigbook.com](ourbigbook-com.md)
