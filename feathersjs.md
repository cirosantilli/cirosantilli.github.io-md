# FeathersJS

↑ **Parent:** [Node.js web framework](node-js-web-framework.md)

- [https://feathersjs.com](https://feathersjs.com)
- [https://github.com/feathersjs/feathers](https://github.com/feathersjs/feathers)
- [https://stackoverflow.com/questions/tagged/feathersjs](https://stackoverflow.com/questions/tagged/feathersjs)

Looks interesting.

It seems to abstract the part about the client messaging the backend, which focuses on being able to easily plug in a number of [Front-end web framework](front-end-web-framework.md) to manage client state.

Has the "main web [API](application-programming-interface.md) is the same as the REST API" focus, which is fundamental 2020-nowadays.

Uses [Socket.IO](socket-io.md), which allows the client Javascript to register callbacks when data is updated to achieve [Socket.IO](socket-io.md), e.g. their default chat app does:
```
client.service('messages').on('created', addMessage);
```
so that message appear immediately as they are sent.

Their standard template from `feathers generate app` on `@feathersjs/cli@4.5.0` includes:
- several authentication methods, including [OAuth](oauth.md)
- testing
- backend [database](database.md) with one of several [object-relational mapping](object-relational-mapping.md)! However, they don't abstract across them. E.g., the default Chat example uses NeDB, but a real app will likely use [Sequelize](sequelize-split.md), and a [port](porting.md) is needed
which looks promising! They don't have a default template for a [Front-end web framework](front-end-web-framework.md) however unfortunately: [https://docs.feathersjs.com/guides/frameworks.html#the-feathers-chat](https://docs.feathersjs.com/guides/frameworks.html#the-feathers-chat) lists a few chat app versions, which is their [hello world](hello-world-program.md):
- [Front-end web framework](front-end-web-framework.md): not built-in on generator, but there are some sample repos pointed from the documentation, and they did work out-of-box:
  - [feathers-chat-react](feathers-chat-react.md)
But it is in itself a completely boring app with a single splash page, and no database interaction, so not a good showcase. The actual showcase app is [feathersjs/feathers-chat](feathersjs-feathers-chat.md).

And there is no official example of the chat app that is immediately deployable to [Heroku](heroku.md): [FeathersJS Heroku deployment](feathersjs-heroku-deployment.md), all setups require thinking.

Global source entry point: determine on `package.json` as usual, defaults to `src/index.js`.

**Table of contents**

- [FeatherJS demo apps](featherjs-demo-apps.md)
  - [feathersjs/feathers-chat](feathersjs-feathers-chat.md)
    - [feathers-chat PostgreSQL](feathers-chat-postgresql.md)
    - [feathers-chat-react](feathers-chat-react.md)
  - [Codaisseur/feathersjs-react-redux-ssr](codaisseur-feathersjs-react-redux-ssr.md)
  - [randyscotsmithey/feathers-realworld-example-app](randyscotsmithey-feathers-realworld-example-app.md)
- [FeathersJS Heroku deployment](feathersjs-heroku-deployment.md)
- [FeathersJS signup email verification](feathersjs-signup-email-verification.md)

## ↑ Ancestors (11)

1. [Node.js web framework](node-js-web-framework.md)
2. [Node.js](node-js-split.md)
3. [JavaScript](javascript.md)
4. [List of programming languages](list-of-programming-languages.md)
5. [Programming language](programming-language-split.md)
6. [Software](software-split.md)
7. [Computer](computer-split.md)
8. [Information technology](information-technology.md)
9. [Area of technology](area-of-technology.md)
10. [Technology](technology-split.md)
11. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (4)

- [A blog in every web framework](a-blog-in-every-web-framework.md)
- [feathersjs/feathers-chat](feathersjs-feathers-chat.md)
- [Meteor (web framework)](meteor-web-framework.md)
- [Randyscotsmithey/feathers-realworld-example-app](randyscotsmithey-feathers-realworld-example-app.md)
