<h1 id="gothinkster-realworld">gothinkster/realworld</h1>

↑ **Parent:** [A blog in every web framework](a-blog-in-every-web-framework.md)

[https://github.com/gothinkster/realworld](https://github.com/gothinkster/realworld)

[Ciro Santilli](ciro-santilli-split.md)'s implementation: [node Express Sequelize Next.js realworld example app](node-express-sequelize-next-js-realworld-example-app.md).

Ahh, you [can't have new ideas anymore](a-blog-in-every-web-framework.md)!

Basically puts together every backend with [Front-end web framework](front-end-web-framework.md) to create the exact same website.

The reference live demo can be found at: [https://demo.realworld.io/#/](https://demo.realworld.io/#/) It is based on [Angular.js](angular-js.md) as it links to: [https://github.com/gothinkster/angularjs-realworld-example-app](https://github.com/gothinkster/angularjs-realworld-example-app) TODO backend?

There are however also live demos of other frontends, e.g.:
- [React](react-split.md): [https://react-redux.realworld.io](https://react-redux.realworld.io). But note that tag addition at post creation is broken there as of March 2021, but not on master: [https://github.com/gothinkster/react-redux-realworld-example-app/issues/151#issuecomment-808417846](https://github.com/gothinkster/react-redux-realworld-example-app/issues/151#issuecomment-808417846) so they forgot to update the live [server](server-computing.md).
- [Vue.js](vue-js.md): [https://vue-vuex-realworld.netlify.app](https://vue-vuex-realworld.netlify.app)
Note that all those frontends communicate with the same backend.

As of 2021 Devs are seemed a bit too focused on monetizing the project through their "how to use this project" premium tutorial, and documentation could be better: just getting the [hello world](hello-world-program.md) of the most popular backend with the most popular frontend is not easy... come on.

[https://github.com/gothinkster/realworld/issues/578](https://github.com/gothinkster/realworld/issues/578) asks for community support, as devs have moved on since unfortunately.

Remember:
- by default, the frontends hardcode the upstream public data [API](application-programming-interface.md): `https://conduit.productionready.io/api` so you have to hack their code to match the port of the backend. And each backend can have a different port.
- when you switch between backends, you must first manually [clear client-side storage](clear-client-side-storage.md) cookies/local new run will fail due to authentication issues!

Important missing things from the minimum base app:
- [server-side rendering](server-side-rendering.md):
  - [https://github.com/arrlancore/nextjs-ssr-real-world-app-example](https://github.com/arrlancore/nextjs-ssr-real-world-app-example). As advertised, that global instance does render with [JavaScript](javascript.md) disabled! Proposed for upstream at: [https://github.com/gothinkster/realworld/issues/423](https://github.com/gothinkster/realworld/issues/423)
  - [https://github.com/gothinkster/realworld/issues/266](https://github.com/gothinkster/realworld/issues/266)
- no [javaScript bi-directional communication library](javascript-bi-directional-communication-library.md) built-in... come on: [https://github.com/gothinkster/realworld/issues/107](https://github.com/gothinkster/realworld/issues/107)
- [email](email.md) notifications however as tested on the live demo: [https://demo.realworld.io/#/](https://demo.realworld.io/#/)
- error handling is broken/missing/inconsistent across apps

First you should the most popular backend/frontend combination running, which is the most likely to be working. We managed to run on [Ubuntu](ubuntu.md) 20.10, [React](react-split.md) + [Node.js](node-js-split.md) [Express.js](express-js.md) as described at [https://github.com/gothinkster/node-express-realworld-example-app/pull/116](https://github.com/gothinkster/node-express-realworld-example-app/pull/116):
- [https://github.com/cirosantilli/node-express-realworld-example-app/tree/mongo4](https://github.com/cirosantilli/node-express-realworld-example-app/tree/mongo4) which has a simple patch on top of [https://github.com/gothinkster/node-express-realworld-example-app/tree/ba04b70c31af81ca7935096740a6e083563b3a4a](https://github.com/gothinkster/node-express-realworld-example-app/tree/ba04b70c31af81ca7935096740a6e083563b3a4a) for MongoDB 4 support

  This requires you to first [install MongoDB on Ubuntu](install-mongodb-on-ubuntu.md) and ensure you can login to it from the command line.
- [https://github.com/gothinkster/react-redux-realworld-example-app/tree/9186292054dc37567e707602a15a0884d6bdae35](https://github.com/gothinkster/react-redux-realworld-example-app/tree/9186292054dc37567e707602a15a0884d6bdae35) patched to use the correct server host/port `localhost:3000`:
  ```
  diff --git a/src/agent.js b/src/agent.js
  index adfbd72..e3cdc7f 100644
  --- a/src/agent.js
  +++ b/src/agent.js
  @@ -3,7 +3,7 @@ import _superagent from 'superagent';

   const superagent = superagentPromise(_superagent, global.Promise);

  -const API_ROOT = 'https://conduit.productionready.io/api';
  +const API_ROOT = 'http://localhost:3030/api';

   const encode = encodeURIComponent;
   const responseBody = res => res.body;
  ```
Then just:
```
npm install
npm start
```
on both [server](server-computing.md) and [client](client-computing.md), and then visit the client URL: [http://localhost:4100/](http://localhost:4100/)

You have to hit the Enter key to add tags, it's terrible: [https://github.com/gothinkster/react-redux-realworld-example-app/issues/151#issuecomment-808417846](https://github.com/gothinkster/react-redux-realworld-example-app/issues/151#issuecomment-808417846)

One cool thing is that the main repo has unified backend API tests:
```
git clone https://github.com/gothinkster/realworld
cd realworld
git checkout e7adc6b06b459e578d7d4a6738c1c050598ba431
cd api
APIURL=http://localhost:3000/api USERNAME="u$(date +%s)" ./run-api-tests.sh
```
so the per-repository tests are basically useless, and that single test can test everything for any backend! There is no frontend testing however: [https://github.com/gothinkster/realworld/issues/269](https://github.com/gothinkster/realworld/issues/269) so newb.

**Table of contents**

- [gothinkster/realworld implementation](gothinkster-realworld-implementation.md)

## ↑ Ancestors (10)

1. [A blog in every web framework](a-blog-in-every-web-framework.md)
2. [Hello world website](hello-world-website.md)
3. [Web framework](web-framework.md)
4. [Web technology](web-technology-split.md)
5. [Software](software-split.md)
6. [Computer](computer-split.md)
7. [Information technology](information-technology.md)
8. [Area of technology](area-of-technology.md)
9. [Technology](technology-split.md)
10. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (8)

- [How to decide if an ORM is good?](how-to-decide-if-an-orm-is-good.md)
- [lujakob/nestjs-realworld-example-app](lujakob-nestjs-realworld-example-app.md)
- [Next.js](next-js.md)
- [Randyscotsmithey/feathers-realworld-example-app](randyscotsmithey-feathers-realworld-example-app.md)
- [Realworld app written in Express](realworld-app-written-in-express.md)
- [Shakacode/react\_on\_rails](shakacode-react-on-rails.md)
- [TodoMVC](todomvc.md)
- [Web framework](web-framework.md)
