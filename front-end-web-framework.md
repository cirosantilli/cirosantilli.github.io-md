# Front-end web framework

↑ **Parent:** [Web framework](web-framework.md)

You need those because it is hard to do the following:
- client [JavaScript](javascript.md) sends a request to [server](server-computing.md)
- server sends back data
- client updates what the user sees

This is hard to do notably because when the update happens, several things might need to change on the webpage at the same time.

Notably, new elements might need to be added to the webpage, which in turn means that new bindings such as button clicks have to be added to those, in a way that keeps the page working.

The only way to do this basically is to have a functional dependency graph that keeps everything in the page in working state as updates come.

**Table of contents**

- [Single page application](single-page-application.md)
  - [Isomorphic JavaScript](isomorphic-javascript.md)
    - [Server-side rendering](server-side-rendering.md)
- [List of front-end web frameworks](list-of-front-end-web-frameworks.md)
  - [Angular.js](angular-js.md)
  - [React](react.md)
    - [React JSX](react.md#react-jsx)
    - [React error](react.md#react-error)
      - [Cannot update a component while rendering a different component warning in React](react.md#cannot-update-a-component-while-rendering-a-different-component-warning-in-react)
    - [React example](react.md#react-example)
      - [react/hello.html](react.md#_file/react/hello.html)
      - [react/ref-twice.html](react.md#_file/react/ref-twice.html)
    - [React DOM manipulation](react.md#react-dom-manipulation)
      - [react/ref-click-counter.html](react.md#_file/react/ref-click-counter.html)
      - [react/ref-click-counter-func.html](react.md#_file/react/ref-click-counter-func.html)
    - [React class vs function component](react.md#react-class-vs-function-component)
      - [React class component](react.md#react-class-component)
      - [React function component](react.md#react-function-component)
        - [React hook](react.md#react-hook)
          - [`useEffect`](react.md#useeffect)
          - [`useRef`](react.md#useref)
          - [`useCallback`](react.md#usecallback)
    - [Next.js](react.md#next-js)
      - [Next.js example](react.md#next-js-example)
        - [nodejs/next/posts](react.md#_file/nodejs/next/posts)
        - [nodejs/next/ref-twice](react.md#_file/nodejs/next/ref-twice)
        - [nodejs/next/inject-into-static](react.md#_file/nodejs/next/inject-into-static)
      - [Node Express Sequelize Next.js realworld example app](react.md#node-express-sequelize-next-js-realworld-example-app)
  - [Vue.js](vue-js.md)
    - [Nuxt.js](nuxt-js.md)

## ↑ Ancestors (8)

1. [Web framework](web-framework.md)
2. [Web technology](web-technology-split.md)
3. [Software](software-split.md)
4. [Computer](computer-split.md)
5. [Information technology](information-technology.md)
6. [Area of technology](area-of-technology.md)
7. [Technology](technology-split.md)
8. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (7)

- [FeathersJS](feathersjs.md)
- [feathersjs/feathers-chat](feathersjs-feathers-chat.md)
- [Gothinkster/realworld](gothinkster-realworld.md)
- [Meteor (web framework)](meteor-web-framework.md)
- [Nest.js](nest-js.md)
- [Sails.js](sails-js.md)
- [TodoMVC](todomvc.md)
