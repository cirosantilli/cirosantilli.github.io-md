# React

↑ **Parent:** [List of front-end web frameworks](web-technology.md#list-of-front-end-web-frameworks)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/React_(JavaScript library))

Website: [https://reactjs.org](https://reactjs.org)

React officially recommends that you use [Next.js](#next-js)[https://reactjs.org/docs/create-a-new-react-app.html#recommended-toolchains](https://reactjs.org/docs/create-a-new-react-app.html#recommended-toolchains), so just do it. It just sets up obvious missing functionality from raw React.

React feels like a good. But it also feels impossible to use/learn sometimes.

Its main design goal is to reduce DOM changes to improve rendering times.

And an important side effect of that is that it becomes easier to do stuff of the type:
- user creates a new comment that appears on screen without page reload
- comment has a delete button, which is JavaScript callback activated
and then the new comment easily gets the callback attached to it.

And it also ends up naturally doubling as a template engine.

But React can also be extremely hard to use. It can be very hard to know what you can and cannot do sometimes, then you have to stop and try to understand how react works things better:
- [cannot update a component while rendering a different component warning in React](#cannot-update-a-component-while-rendering-a-different-component-warning-in-react)
- Rendered more hooks than during the previous render.
- cannot use hooks from helpers:
  - [https://www.benmvp.com/blog/helper-functions-react-useeffect-hook/](https://www.benmvp.com/blog/helper-functions-react-useeffect-hook/)
  - [https://stackoverflow.com/questions/68273638/using-hooks-inside-helper-functions](https://stackoverflow.com/questions/68273638/using-hooks-inside-helper-functions)
  - [https://stackoverflow.com/questions/64689409/helper-function-using-hooks-inside-a-functional-component](https://stackoverflow.com/questions/64689409/helper-function-using-hooks-inside-a-functional-component)
The biggest problem is that it is hard to automatically detect such errors, but perhaps this is the same for other frontend stuff. Though when doing [server-side rendering](web-technology.md#server-side-rendering), the setup should really tell you about such errors, so you don't just discover them in production later on.

Is is also very difficult to understand precisely why hooks run a certain number of times.

Examples under: [react](react).
- [react/hello.html](#_file/react/hello.html)
- [react/hello-func.html](react/hello-func.html): Hello World with a [React function component](#react-function-component) instead of classes. At page load console shows:
  ```
  Main
  ```

  and then after each click:
  ```
  onClick
  Main
  ```

  so we understand that `Main` insanely functions both as the constructor and as the render function in [React function components](#react-function-component).
- [react/hello-func-use-callback.html](react/hello-func-use-callback.html): same as [react/hello-func.html](react/hello-func.html) but with useCallback. TODO no advantages in this case? When does it help?
- [react/hello-without-jsx.html](react/hello-without-jsx.html): Hello World in pure [JavaScript](programming-language.md#javascript), without [JSX](#react-jsx). Exactly equivalent to [react/hello.html](react/hello.html). Documented at: [https://reactjs.org/docs/react-without-jsx.html](https://reactjs.org/docs/react-without-jsx.html) Understanding this is fundamental to understanding React.
- [react/prop-change.html](react/prop-change.html): shows what gets called as parameters flow down through the tree.

  By looking at the console, we see all `render` get called every time, even if `props` didn't change, but not the constructors.

  After page load the console contains:
  ```
  Main.constructor
  Main.render
  NotMain.constructor
  NotMain.render
  NotMain2.constructor
  NotMain2.render
  ```

  Then, every time we click the button it adds:
  ```
  handleClick
  Main.render
  NotMain.render
  NotMain2.render
  ```

  Note how the `props` of `NotMain` only change every other click, but `render` still gets called every time.

  In order to make `React` not re-render when there are not changes, you have to either:
  - define the `shouldComponentUpdate` method of class components
  - wrap functional components in `React.memo`

  Related:
  - [https://stackoverflow.com/questions/61301937/why-is-react-component-rerendering-when-props-has-not-changed](https://stackoverflow.com/questions/61301937/why-is-react-component-rerendering-when-props-has-not-changed)
  - [https://stackoverflow.com/questions/67214500/why-react-rerendres-components-even-if-props-didnt-changed](https://stackoverflow.com/questions/67214500/why-react-rerendres-components-even-if-props-didnt-changed)
- [react/prop-change-hook.html](react/prop-change-hook.html): same as [react/prop-change.html](react/prop-change.html), but using hooks. The notable difference is that functional components don't have a clear constructor/render separation, the function just gets called every time. Then React does some magic to ensure that `useState` returns the current state, except for the first render where they return the initial value.
- [react/prop-change-hook-use-memo.html](react/prop-change-hook-use-memo.html): TODO forgot if this example is useful, was tring to use `useMemo`
- [react/prop-change-child.html](react/prop-change-child.html): shows what child prop changes do not call render on parent, `Main` does not show up on console when you click under `NotMain`
- [react/hook-from-function-fail.html](react/hook-from-function-fail.html): TODO got some errors that seemed linked to this on a larger program, but failed to minimize them here
- [react/hook-different-number-of-times.html](react/hook-different-number-of-times.html): this illustrates one of the cardinal points of using hooks: you must always call them the same number of times, otherwise it fails with:> React has detected a change in the order of Hooks called by Main. This will lead to bugs and errors if not fixed.

  In the case of `useState`, we can kind of understand why this happens: React must use the order of calls to determine which state variable to return at each point in time.
- [react/hello-hook-use-effect.html](react/hello-hook-use-effect.html): just checking when it gets called. Happens after every render
  ```
  handleClick
  Main
  useEffect
  useEffect2
  ```
- TODO create a test `\a[react/img-broken.html]`
  - [https://stackoverflow.com/questions/34097560/react-js-replace-img-src-onerror](https://stackoverflow.com/questions/34097560/react-js-replace-img-src-onerror)
  - [https://stackoverflow.com/questions/36305805/how-to-hide-alt-text-using-css-when-the-image-is-not-present](https://stackoverflow.com/questions/36305805/how-to-hide-alt-text-using-css-when-the-image-is-not-present)

How React works bibliography:
- [https://www.netlify.com/blog/2019/03/11/deep-dive-how-do-react-hooks-really-work/](https://www.netlify.com/blog/2019/03/11/deep-dive-how-do-react-hooks-really-work/) shows how `uesState` works under the hood with crazy closures
- [https://medium.com/@gethylgeorge/how-virtual-dom-and-diffing-works-in-react-6fc805f9f84e](https://medium.com/@gethylgeorge/how-virtual-dom-and-diffing-works-in-react-6fc805f9f84e)

<a id="video-react-for-the-haters-in-100-seconds-by-fireship-2022"></a>
**[Video 1](#video-react-for-the-haters-in-100-seconds-by-fireship-2022). React for the Haters in 100 Seconds by Fireship (2022)** [Source](https://www.youtube.com/watch?v=HyWYpM_S-2c).

**Table of contents**

- [React JSX](#react-jsx)
- [React error](#react-error)
  - [Cannot update a component while rendering a different component warning in React](#cannot-update-a-component-while-rendering-a-different-component-warning-in-react)
- [React example](#react-example)
  - [react/hello.html](#_file/react/hello.html)
  - [react/ref-twice.html](#_file/react/ref-twice.html)
- [React DOM manipulation](#react-dom-manipulation)
  - [react/ref-click-counter.html](#_file/react/ref-click-counter.html)
  - [react/ref-click-counter-func.html](#_file/react/ref-click-counter-func.html)
- [React class vs function component](#react-class-vs-function-component)
  - [React class component](#react-class-component)
  - [React function component](#react-function-component)
    - [React hook](#react-hook)
      - [`useEffect`](#useeffect)
      - [`useRef`](#useref)
      - [`useCallback`](#usecallback)
- [Next.js](#next-js)
  - [Next.js example](#next-js-example)
    - [nodejs/next/posts](#_file/nodejs/next/posts)
    - [nodejs/next/ref-twice](#_file/nodejs/next/ref-twice)
    - [nodejs/next/inject-into-static](#_file/nodejs/next/inject-into-static)
  - [Node Express Sequelize Next.js realworld example app](#node-express-sequelize-next-js-realworld-example-app)

## React JSX

↑ **Parent:** [React](react.md)

## React error

↑ **Parent:** [React](react.md)

### Cannot update a component while rendering a different component warning in React

↑ **Parent:** [React error](#react-error)

Minimal reproduction: [https://stackoverflow.com/questions/62336340/cannot-update-a-component-while-rendering-a-different-component-warning/70317831#70317831](https://stackoverflow.com/questions/62336340/cannot-update-a-component-while-rendering-a-different-component-warning/70317831#70317831)

## React example

↑ **Parent:** [React](react.md)

<h3 id="_file/react/hello.html">react/hello.html</h3>

↑ **Parent:** [React example](#react-example)

Minimal React hello world example. As you click:
- one counter increments every time
- the other increments every two clicks
By opening a web inspector, you can see that only modified elements get updated. So we understand that [JSX](#react-jsx) parses its "HTML-like" into a tree, and then propagates updates on that tree.

By looking at the terminal, we see that `render()` does get called every time the button is clicked, so the tree of elements does get recreated every time. But then React diffes thing out and only updates things in the DOM where needed.

<h3 id="_file/react/ref-twice.html">react/ref-twice.html</h3>

↑ **Parent:** [React example](#react-example)

Failed attempt at minimizing [nodejs/next/ref-twice](#_file/nodejs/next/ref-twice) outside of [Next.js](#next-js).

## React DOM manipulation

↑ **Parent:** [React](react.md)

<h3 id="_file/react/ref-click-counter.html">react/ref-click-counter.html</h3>

↑ **Parent:** [React DOM manipulation](#react-dom-manipulation)

Dummy example of using a [React `ref`](#react-dom-manipulation) This example is useless and to the end user seems functionally equivalent to [react/hello.html](#_file/react/hello.html).

It does however serve as a good example of what react does that is useful: it provides a "clear" separation between state and render code (which becomes once again much less clear in [React function components](#react-function-component).

Notably, this example is insane because at:
```
<button onClick={() => {
  elem.innerHTML = (parseInt(elem.innerHTML) + 1).toString()
```
we are extracing state from some random HTML string rather than having a clean [JavaScript](programming-language.md#javascript) variable containing that value.

In this case we managed to get away with it, but this is in general not easy/possible.

<h3 id="_file/react/ref-click-counter-func.html">react/ref-click-counter-func.html</h3>

↑ **Parent:** [React DOM manipulation](#react-dom-manipulation)

[React function component](#react-function-component) version of [react/ref-click-counter.html](#_file/react/ref-click-counter.html) using [`useRef`](#useref).

## React class vs function component

↑ **Parent:** [React](react.md)

[React function components](#react-function-component) do produce shorter code. But they are also impossible to understand without knowing what is their corresponding class component.

Hooks were introduced much after classes, and just require less code, so everyone is using them now instead of classes.

### React class component

↑ **Parent:** [React class vs function component](#react-class-vs-function-component)

### React function component

↑ **Parent:** [React class vs function component](#react-class-vs-function-component)

#### React hook

↑ **Parent:** [React function component](#react-function-component)

##### `useEffect`

↑ **Parent:** [React hook](#react-hook)

This should only be used for things that happen outside of the state that [React](react.md) trackes, e.g. `window` event handlers.

Examples:
- [react/ref-click-counter-func.html](#_file/react/ref-click-counter-func.html)

##### `useRef`

↑ **Parent:** [React hook](#react-hook)

##### `useCallback`

↑ **Parent:** [React hook](#react-hook)

<h2 id="next-js">Next.js</h2>

↑ **Parent:** [React](react.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Next.js)

Framework built on top of [React](react.md).

Officially recommended by [React](react.md)[https://reactjs.org/docs/create-a-new-react-app.html](https://reactjs.org/docs/create-a-new-react-app.html):

> Recommended Toolchains
> 
> If you’re building a server-rendered website with Node.js, try Next.js.

[gothinkster/realworld](web-technology.md#gothinkster-realworld) blog example by [Ciro Santilli](ciro-santilli.md): [node Express Sequelize Next.js realworld example app](#node-express-sequelize-next-js-realworld-example-app).

Basically what this does is to get [server-side rendering](web-technology.md#server-side-rendering) just working by [React](react.md), including hydration, which is a good thing.

Next.js sends the first pre-rendered HTML page along with the JavaScript code. Then, JavaScript page switches just load the API data.

Next.js does this nicely by forcing you to provide page data in a serialized JSON format, even when rendering server-side (e.g. the return value of `getServerSideProps`). This way, it is also able to provide either the full HTML, or just the JSON.

Some general downsides:
- it does feel like they don't document deployment very well however, especially non-Vercel options, which is the company behind Next.js. I'm unable to find how to use a non Vercel CDN with ISR supposing that is possible.
- Next.js is very opinionated, and like any opinionated library it is sometimes hard to know why something is/isn't happening, and sometimes it is hard/impossible to do what you want with it unless they add support. They have done good progress, but even as of 2022, some aspects just feel so immature, some major-looking use cases are not very well done.

In theory, Next.js could be the "ultimate frontend framework". It does have a lot of development difficulties that need to be ironed out, but the general concepts, and things it tries to integrate, including e.g. [webpack](webpack.md), [TypeScript](typescript.md), etc. are good. Maybe the question is when will someone put it together with an amazing backend library and dominate and finally put an end to the infinite number of Js Frameworks!

In-tree examples at: [https://github.com/vercel/next.js/tree/canary/examples](https://github.com/vercel/next.js/tree/canary/examples)

`canary` is their `master`: [https://github.com/vercel/next.js/issues/3211](https://github.com/vercel/next.js/issues/3211)

In order to offer its amazing features, Next.js is also extremely opinionated, which means that if something wasn't designed to be possible, it basically isn't.

No prerender with custom [server](computer.md#server-computing)? It forces you to write your API with next as well? Or does it mean something else?
- [https://github.com/vercel/next.js/discussions/25394](https://github.com/vercel/next.js/discussions/25394)
- [https://nextjs.org/docs/advanced-features/custom-server](https://nextjs.org/docs/advanced-features/custom-server)

TODO can it statically generate pages that are created at runtime? E.g. if I create a new blog post, will it automatically upload a static page? It seems that yes, and that this is exactly what Incremental Static Regeneration means:
- [https://github.com/vercel/next.js/discussions/25410](https://github.com/vercel/next.js/discussions/25410)
- [https://vercel.com/docs/next.js/incremental-static-regeneration](https://vercel.com/docs/next.js/incremental-static-regeneration)
- [https://github.com/vercel/next.js/discussions/17711](https://github.com/vercel/next.js/discussions/17711)
- [https://www.reddit.com/r/nextjs/comments/mvvhym/a_complete_guide_to_incremental_static/](https://www.reddit.com/r/nextjs/comments/mvvhym/a_complete_guide_to_incremental_static/)
- [https://github.com/vercel/next.js/discussions/11552#discussioncomment-115595](https://github.com/vercel/next.js/discussions/11552#discussioncomment-115595)
- [https://stackoverflow.com/questions/62105756/how-to-use-aws-with-next-js](https://stackoverflow.com/questions/62105756/how-to-use-aws-with-next-js)
- [https://github.com/vercel/next.js/discussions/17080](https://github.com/vercel/next.js/discussions/17080)
- [https://github.com/vercel/next.js/discussions/16852](https://github.com/vercel/next.js/discussions/16852)
However, Ciro can't find any mention of how to specify where the pages are uploaded to... this is pat of the non-Vercel deployment problem.

Can't ISR prerenter by URL query parameters:
- [https://stackoverflow.com/questions/66133814/how-to-get-url-query-string-on-next-js-static-site-generation](https://stackoverflow.com/questions/66133814/how-to-get-url-query-string-on-next-js-static-site-generation)
- [https://github.com/vercel/next.js/discussions/17269](https://github.com/vercel/next.js/discussions/17269)
That plus the requirement to have one page per file under `pages/` leads to a lot of useless duplication, because then you are forced to place the URL parameters on the pathnames.

"Module not found: Can't resolve 'fs'" [Hell](religion.md#hell). The main reason this happens seems to be the that in a higher order component, [webpack](webpack.md) can't determine if callbacks use the require or not to remove it from frontend code. Fully investigated and solved at:
- [https://stackoverflow.com/questions/64926174/module-not-found-cant-resolve-fs-in-next-js-application/70363153#70363153](https://stackoverflow.com/questions/64926174/module-not-found-cant-resolve-fs-in-next-js-application/70363153#70363153)

Overviews:
- [https://www.reddit.com/r/reactjs/comments/8evy5d/what_are_the_downsides_to_nextjs/](https://www.reddit.com/r/reactjs/comments/8evy5d/what_are_the_downsides_to_nextjs/) 2017 What are the downsides to Next.js?

TODO answer:
- [https://stackoverflow.com/questions/59674496/how-to-pass-pageprops-in-next-js-from-a-child-component-to-app-js](https://stackoverflow.com/questions/59674496/how-to-pass-pageprops-in-next-js-from-a-child-component-to-app-js)

<h3 id="next-js-example">Next.js example</h3>

↑ **Parent:** [Next.js](#next-js)

Our examples are located under [nodejs/next](nodejs/next):
- [nodejs/next/hello-world](nodejs/next/hello-world): a hello world. There's an in-tree one at: [https://github.com/vercel/next.js/tree/e75361fd03872b097e817634c049b3185f24cf56/examples/hello-world](https://github.com/vercel/next.js/tree/e75361fd03872b097e817634c049b3185f24cf56/examples/hello-world), but ours is truly minimal
- [nodejs/next/hoc](nodejs/next/hoc): shows how to use a higher order component (HOC) to factor out `getStaticProps` across two pages: [nodejs/next/hoc/pages/index.js](nodejs/next/hoc/pages/index.js) and [nodejs/next/hoc/pages/notindex.js](nodejs/next/hoc/pages/notindex.js)
- [nodejs/next/typescript](nodejs/next/typescript): simple [TypeScript](typescript.md) example, minimized from: [https://github.com/vercel/next.js/tree/d61b0761efae09bd9cb1201ff134ed8950d9deca/examples/with-typescript](https://github.com/vercel/next.js/tree/d61b0761efae09bd9cb1201ff134ed8950d9deca/examples/with-typescript)

  Notably, that shows how `require` errors are avoided in that case as mentioned at: [https://stackoverflow.com/questions/64926174/module-not-found-cant-resolve-fs-in-next-js-application/70363153#70363153](https://stackoverflow.com/questions/64926174/module-not-found-cant-resolve-fs-in-next-js-application/70363153#70363153)
- [nodejs/next/localStorage](nodejs/next/localStorage): a counter that is persistent across page reloads by using `localStorage`. Used in: [https://stackoverflow.com/questions/54819721/next-js-access-localstorage-before-rendering-page/68136224#68136224](https://stackoverflow.com/questions/54819721/next-js-access-localstorage-before-rendering-page/68136224#68136224)

Solved ones:
- solved by [preview mode](https://nextjs.org/docs/advanced-features/preview-mode) in Next.js 12:
  - ISR was basically unusable for CRUD websites because you can't force a one-off immediate page update:
    - [https://github.com/vercel/next.js/discussions/25677](https://github.com/vercel/next.js/discussions/25677)

<h4 id="_file/nodejs/next/posts">nodejs/next/posts</h4>

↑ **Parent:** [Next.js example](#next-js-example)

The goal of this example is to understand when states and effects happen when changing between different routes that use the same component.

Behavior is follows:
- visit: [http://localhost:3001/1](http://localhost:3001/1)
- click `count++`. This makes `count: 1`
- click "2" to visit [http://localhost:3001/2](http://localhost:3001/2)
- outcome: count is still 1

This is likely because in [React](react.md) the state kept in the virtual DOM structure, and identical structure implies identical state. So when we change from post 1 to 2, we still have a `Post` object, and state is unchanged.

Next if we click:
- "Index" to go to [http://localhost:3000](http://localhost:3000)
- "1" to go to [http://localhost:3001/1](http://localhost:3001/1)
then the count is back to 0. This is because we changed the `Post` object in the DOM to `Index` and back, which resets everything.

This example also illustrates how to prevent this from happening with [`useEffect`](#useeffect).

Bibliography:
- [https://stackoverflow.com/questions/63143334/how-to-not-persist-state-between-next-js-dynamic-routes](https://stackoverflow.com/questions/63143334/how-to-not-persist-state-between-next-js-dynamic-routes)

<h4 id="_file/nodejs/next/ref-twice">nodejs/next/ref-twice</h4>

↑ **Parent:** [Next.js example](#next-js-example)

This is a minimal reproducible example for the terrible problem of external effects applying twice to refs for effects that are not idempotent and thus blowup if applied twice.

The issue is currently discussed at: [https://react.dev/learn/synchronizing-with-effects#step-3-add-cleanup-if-needed](https://react.dev/learn/synchronizing-with-effects#step-3-add-cleanup-if-needed) ([archive](https://web.archive.org/web/20240720100401/https://react.dev/learn/synchronizing-with-effects#step-3-add-cleanup-if-needed)) which says "you need to cleanup the thing yourself". [https://web.archive.org/web/20240720100401/https://react.dev/learn/synchronizing-with-effects#subscribing-to-events](https://web.archive.org/web/20240720100401/https://react.dev/learn/synchronizing-with-effects#subscribing-to-events) is also says that for the specific case of `addEventListener`.

But that's annoying! Can't we just somehow tell if we applied twice or not to avoid having to implement a cleanup? What if a third party system does not provide a cleanup at all?

Is the correct solution to just just have a [`useEffect`](#useeffect) with empty dependency list? Seems to be good according to posts and to [ESLint](programming-language.md#eslint)!

Tried to do a [React](react.md) only reproduction at: [react/ref-twice.html](#_file/react/ref-twice.html).

Bibliography:
- [https://github.com/facebook/react/issues/8619](https://github.com/facebook/react/issues/8619)
- [https://github.com/vercel/next.js/tree/276fd521d04b6c228d5637ce359220ffa8f62a2f/examples/with-three-js](https://github.com/vercel/next.js/tree/276fd521d04b6c228d5637ce359220ffa8f62a2f/examples/with-three-js)
- [https://www.reddit.com/r/reactjs/comments/tbt2z8/comment/lizezgd/](https://www.reddit.com/r/reactjs/comments/tbt2z8/comment/lizezgd/)

[Ciro Santilli](ciro-santilli.md)'s questions:
- [https://stackoverflow.com/questions/78891187/how-to-prevent-a-react-useeffect-from-running-twice-in-strictmode-development-wi](https://stackoverflow.com/questions/78891187/how-to-prevent-a-react-useeffect-from-running-twice-in-strictmode-development-wi)
- [https://www.reddit.com/r/reactjs/comments/1ewprza/how_to_prevent_a_react_useeffect_from_running/](https://www.reddit.com/r/reactjs/comments/1ewprza/how_to_prevent_a_react_useeffect_from_running/)

<h4 id="_file/nodejs/next/inject-into-static">nodejs/next/inject-into-static</h4>

↑ **Parent:** [Next.js example](#next-js-example)

In this example we attempt to inject [React](react.md) elements into statically rendered HTML coming from the server, and properly hydrate them.

Questions by [Ciro Santilli](ciro-santilli.md):
- [https://stackoverflow.com/questions/78892868/how-to-inject-a-react-component-inside-static-pre-rendered-html-coming-from-the](https://stackoverflow.com/questions/78892868/how-to-inject-a-react-component-inside-static-pre-rendered-html-coming-from-the)
- [https://www.reddit.com/r/nextjs/comments/1ewwea3/how_to_inject_a_react_component_inside_static/](https://www.reddit.com/r/nextjs/comments/1ewwea3/how_to_inject_a_react_component_inside_static/)
- [https://github.com/vercel/next.js/discussions/69099](https://github.com/vercel/next.js/discussions/69099)

Bibliography:
- [https://stackoverflow.com/questions/76489919/nextjs-custom-component-hydration](https://stackoverflow.com/questions/76489919/nextjs-custom-component-hydration)
- [https://stackoverflow.com/questions/67915232/how-to-use-domparser-in-next-js](https://stackoverflow.com/questions/67915232/how-to-use-domparser-in-next-js)

<h3 id="node-express-sequelize-next-js-realworld-example-app">Node Express Sequelize Next.js realworld example app</h3>

↑ **Parent:** [Next.js](#next-js)  
🏷️ **Tags:** [Gothinkster/realworld implementation](web-technology.md#gothinkster-realworld-implementation)

[https://github.com/cirosantilli/node-express-sequelize-nextjs-realworld-example-app](https://github.com/cirosantilli/node-express-sequelize-nextjs-realworld-example-app)

## ↑ Ancestors (10)

1. [List of front-end web frameworks](web-technology.md#list-of-front-end-web-frameworks)
2. [Front-end web framework](web-technology.md#front-end-web-framework)
3. [Web framework](web-technology.md#web-framework)
4. [Web technology](web-technology.md)
5. [Software](software.md)
6. [Computer](computer.md)
7. [Information technology](technology.md#information-technology)
8. [Area of technology](technology.md#area-of-technology)
9. [Technology](technology.md)
10. [Ciro Santilli's Homepage](README.md)

## ← Incoming links (12)

- [nodejs/next/inject-into-static](#_file/nodejs/next/inject-into-static)
- [nodejs/next/posts](#_file/nodejs/next/posts)
- [nodejs/next/ref-twice](#_file/nodejs/next/ref-twice)
- [Django (web-framework)](programming-language.md#django-web-framework)
- [Gothinkster/realworld](web-technology.md#gothinkster-realworld)
- [Gothinkster/realworld implementation](web-technology.md#gothinkster-realworld-implementation)
- [Meteor (web framework)](node-js.md#meteor-web-framework)
- [Randyscotsmithey/feathers-realworld-example-app](node-js.md#randyscotsmithey-feathers-realworld-example-app)
- [Ruby on Rails React integration](programming-language.md#ruby-on-rails-react-integration)
- [Sails.js](node-js.md#sails-js)
- [How the tech improved](updates.md#ourbigbook-project-update-march-2025/how-the-tech-improved)
- [`UseEffect`](#useeffect)
