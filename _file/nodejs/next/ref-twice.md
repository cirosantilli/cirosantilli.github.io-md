<h1 id="_file/nodejs/next/ref-twice">nodejs/next/ref-twice</h1>

↑ **Parent:** [Next.js example](../../../next-js-example.md)

This is a minimal reproducible example for the terrible problem of external effects applying twice to refs for effects that are not idempotent and thus blowup if applied twice.

The issue is currently discussed at: [https://react.dev/learn/synchronizing-with-effects#step-3-add-cleanup-if-needed](https://react.dev/learn/synchronizing-with-effects#step-3-add-cleanup-if-needed) ([archive](https://web.archive.org/web/20240720100401/https://react.dev/learn/synchronizing-with-effects#step-3-add-cleanup-if-needed)) which says "you need to cleanup the thing yourself". [https://web.archive.org/web/20240720100401/https://react.dev/learn/synchronizing-with-effects#subscribing-to-events](https://web.archive.org/web/20240720100401/https://react.dev/learn/synchronizing-with-effects#subscribing-to-events) is also says that for the specific case of `addEventListener`.

But that's annoying! Can't we just somehow tell if we applied twice or not to avoid having to implement a cleanup? What if a third party system does not provide a cleanup at all?

Is the correct solution to just just have a [`useEffect`](../../../useeffect.md) with empty dependency list? Seems to be good according to posts and to [ESLint](../../../eslint.md)!

Tried to do a [React](../../../react-split.md) only reproduction at: [react/ref-twice.html](../../react/ref-twice.html.md).

Bibliography:
- [https://github.com/facebook/react/issues/8619](https://github.com/facebook/react/issues/8619)
- [https://github.com/vercel/next.js/tree/276fd521d04b6c228d5637ce359220ffa8f62a2f/examples/with-three-js](https://github.com/vercel/next.js/tree/276fd521d04b6c228d5637ce359220ffa8f62a2f/examples/with-three-js)
- [https://www.reddit.com/r/reactjs/comments/tbt2z8/comment/lizezgd/](https://www.reddit.com/r/reactjs/comments/tbt2z8/comment/lizezgd/)

[Ciro Santilli](../../../ciro-santilli-split.md)'s questions:
- [https://stackoverflow.com/questions/78891187/how-to-prevent-a-react-useeffect-from-running-twice-in-strictmode-development-wi](https://stackoverflow.com/questions/78891187/how-to-prevent-a-react-useeffect-from-running-twice-in-strictmode-development-wi)
- [https://www.reddit.com/r/reactjs/comments/1ewprza/how_to_prevent_a_react_useeffect_from_running/](https://www.reddit.com/r/reactjs/comments/1ewprza/how_to_prevent_a_react_useeffect_from_running/)

## ↑ Ancestors (13)

1. [Next.js example](../../../next-js-example.md)
2. [Next.js](../../../next-js.md)
3. [React](../../../react-split.md)
4. [List of front-end web frameworks](../../../list-of-front-end-web-frameworks.md)
5. [Front-end web framework](../../../front-end-web-framework.md)
6. [Web framework](../../../web-framework.md)
7. [Web technology](../../../web-technology-split.md)
8. [Software](../../../software-split.md)
9. [Computer](../../../computer-split.md)
10. [Information technology](../../../information-technology.md)
11. [Area of technology](../../../area-of-technology.md)
12. [Technology](../../../technology-split.md)
13. [Ciro Santilli's Homepage](../../../split.md)

## ← Incoming links (1)

- [react/ref-twice.html](../../react/ref-twice.html.md)
