# React

↑ **Parent:** [List of front-end web frameworks](list-of-front-end-web-frameworks.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/React_(JavaScript library))

Website: [https://reactjs.org](https://reactjs.org)

React officially recommends that you use [Next.js](next-js.md)[https://reactjs.org/docs/create-a-new-react-app.html#recommended-toolchains](https://reactjs.org/docs/create-a-new-react-app.html#recommended-toolchains), so just do it. It just sets up obvious missing functionality from raw React.

React feels like a good. But it also feels impossible to use/learn sometimes.

Its main design goal is to reduce DOM changes to improve rendering times.

And an important side effect of that is that it becomes easier to do stuff of the type:
- user creates a new comment that appears on screen without page reload
- comment has a delete button, which is JavaScript callback activated
and then the new comment easily gets the callback attached to it.

And it also ends up naturally doubling as a template engine.

But React can also be extremely hard to use. It can be very hard to know what you can and cannot do sometimes, then you have to stop and try to understand how react works things better:
- [cannot update a component while rendering a different component warning in React](cannot-update-a-component-while-rendering-a-different-component-warning-in-react.md)
- Rendered more hooks than during the previous render.
- cannot use hooks from helpers:
  - [https://www.benmvp.com/blog/helper-functions-react-useeffect-hook/](https://www.benmvp.com/blog/helper-functions-react-useeffect-hook/)
  - [https://stackoverflow.com/questions/68273638/using-hooks-inside-helper-functions](https://stackoverflow.com/questions/68273638/using-hooks-inside-helper-functions)
  - [https://stackoverflow.com/questions/64689409/helper-function-using-hooks-inside-a-functional-component](https://stackoverflow.com/questions/64689409/helper-function-using-hooks-inside-a-functional-component)
The biggest problem is that it is hard to automatically detect such errors, but perhaps this is the same for other frontend stuff. Though when doing [server-side rendering](server-side-rendering.md), the setup should really tell you about such errors, so you don't just discover them in production later on.

Is is also very difficult to understand precisely why hooks run a certain number of times.

Examples under: [react](react).
- [react/hello.html](_file/react/hello.html.md)
- [react/hello-func.html](react/hello-func.html): Hello World with a [React function component](react-function-component.md) instead of classes. At page load console shows:
  ```
  Main
  ```

  and then after each click:
  ```
  onClick
  Main
  ```

  so we understand that `Main` insanely functions both as the constructor and as the render function in [React function components](react-function-component.md).
- [react/hello-func-use-callback.html](react/hello-func-use-callback.html): same as [react/hello-func.html](react/hello-func.html) but with useCallback. TODO no advantages in this case? When does it help?
- [react/hello-without-jsx.html](react/hello-without-jsx.html): Hello World in pure [JavaScript](javascript.md), without [JSX](react-jsx.md). Exactly equivalent to [react/hello.html](react/hello.html). Documented at: [https://reactjs.org/docs/react-without-jsx.html](https://reactjs.org/docs/react-without-jsx.html) Understanding this is fundamental to understanding React.
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

- [React JSX](react-jsx.md)
- [React error](react-error.md)
  - [Cannot update a component while rendering a different component warning in React](cannot-update-a-component-while-rendering-a-different-component-warning-in-react.md)
- [React example](react-example.md)
  - [react/hello.html](_file/react/hello.html.md)
  - [react/ref-twice.html](_file/react/ref-twice.html.md)
- [React DOM manipulation](react-dom-manipulation.md)
  - [react/ref-click-counter.html](_file/react/ref-click-counter.html.md)
  - [react/ref-click-counter-func.html](_file/react/ref-click-counter-func.html.md)
- [React class vs function component](react-class-vs-function-component.md)
  - [React class component](react-class-component.md)
  - [React function component](react-function-component.md)
    - [React hook](react-hook.md)
      - [`useEffect`](useeffect.md)
      - [`useRef`](useref.md)
      - [`useCallback`](usecallback.md)
- [Next.js](next-js.md)
  - [Next.js example](next-js-example.md)
    - [nodejs/next/posts](_file/nodejs/next/posts.md)
    - [nodejs/next/ref-twice](_file/nodejs/next/ref-twice.md)
    - [nodejs/next/inject-into-static](_file/nodejs/next/inject-into-static.md)
  - [Node Express Sequelize Next.js realworld example app](node-express-sequelize-next-js-realworld-example-app.md)

## ↑ Ancestors (10)

1. [List of front-end web frameworks](list-of-front-end-web-frameworks.md)
2. [Front-end web framework](front-end-web-framework.md)
3. [Web framework](web-framework.md)
4. [Web technology](web-technology-split.md)
5. [Software](software-split.md)
6. [Computer](computer-split.md)
7. [Information technology](information-technology.md)
8. [Area of technology](area-of-technology.md)
9. [Technology](technology-split.md)
10. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (12)

- [nodejs/next/inject-into-static](_file/nodejs/next/inject-into-static.md)
- [nodejs/next/posts](_file/nodejs/next/posts.md)
- [nodejs/next/ref-twice](_file/nodejs/next/ref-twice.md)
- [Django (web-framework)](django-web-framework.md)
- [Gothinkster/realworld](gothinkster-realworld.md)
- [Gothinkster/realworld implementation](gothinkster-realworld-implementation.md)
- [Meteor (web framework)](meteor-web-framework.md)
- [Randyscotsmithey/feathers-realworld-example-app](randyscotsmithey-feathers-realworld-example-app.md)
- [Ruby on Rails React integration](ruby-on-rails-react-integration.md)
- [Sails.js](sails-js.md)
- [How the tech improved](updates/ourbigbook-project-update-march-2025/how-the-tech-improved.md)
- [`UseEffect`](useeffect.md)
