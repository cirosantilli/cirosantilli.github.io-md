# feathers-chat-react

↑ **Parent:** [feathersjs/feathers-chat](feathersjs-feathers-chat.md)

[https://github.com/feathersjs-ecosystem/feathers-chat-react](https://github.com/feathersjs-ecosystem/feathers-chat-react)

Last updated 2018 as of 2021, but still just worked.

Also uses [webpack](webpack-split.md) which is fantastic.

Gotta run [https://github.com/feathersjs/feathers-chat](https://github.com/feathersjs/feathers-chat) first: [https://github.com/feathersjs-ecosystem/feathers-chat-react/issues/5](https://github.com/feathersjs-ecosystem/feathers-chat-react/issues/5), then it worked:
```
git clone https://github.com/feathersjs/feathers-chat
cd feathers-chat
git checkout fd729a47c57f9e6170cc1fa23cee0c84a004feb5
npm install
npm start
```
and on the other terminal:
```
git clone https://github.com/feathersjs-ecosystem/feathers-chat-react
cd feathers-chat-react
git checkout 36d56cbe80bbd5596f6a108b1de9db343b33dac3
npm install
npm start
```
then visit [http://localhost:3000/](http://localhost:3000/) and you can create an account and login, tested on Ubuntu 20.10. Data is stored on persistently.

TODO how to merge those two repos into a single repo.

If you [disable JavaScript on Chromium](disable-javascript-on-chromium.md), it stops working completely. There is a section on how to solve that at: [https://docs.feathersjs.com/cookbook/express/view-engine.html](https://docs.feathersjs.com/cookbook/express/view-engine.html) but it does not cover React specifically. [Codaisseur/feathersjs-react-redux-ssr](codaisseur-feathersjs-react-redux-ssr.md) might be good to look into.

## ↑ Ancestors (14)

1. [feathersjs/feathers-chat](feathersjs-feathers-chat.md)
2. [FeatherJS demo apps](featherjs-demo-apps.md)
3. [FeathersJS](feathersjs.md)
4. [Node.js web framework](node-js-web-framework.md)
5. [Node.js](node-js-split.md)
6. [JavaScript](javascript.md)
7. [List of programming languages](list-of-programming-languages.md)
8. [Programming language](programming-language-split.md)
9. [Software](software-split.md)
10. [Computer](computer-split.md)
11. [Information technology](information-technology.md)
12. [Area of technology](area-of-technology.md)
13. [Technology](technology-split.md)
14. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (2)

- [FeathersJS](feathersjs.md)
- [feathersjs/feathers-chat](feathersjs-feathers-chat.md)
