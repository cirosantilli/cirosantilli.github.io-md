<h1 id="_file/nodejs/next/posts">nodejs/next/posts</h1>

↑ **Parent:** [Next.js example](../../../next-js-example.md)

The goal of this example is to understand when states and effects happen when changing between different routes that use the same component.

Behavior is follows:
- visit: [http://localhost:3001/1](http://localhost:3001/1)
- click `count++`. This makes `count: 1`
- click "2" to visit [http://localhost:3001/2](http://localhost:3001/2)
- outcome: count is still 1

This is likely because in [React](../../../react-split.md) the state kept in the virtual DOM structure, and identical structure implies identical state. So when we change from post 1 to 2, we still have a `Post` object, and state is unchanged.

Next if we click:
- "Index" to go to [http://localhost:3000](http://localhost:3000)
- "1" to go to [http://localhost:3001/1](http://localhost:3001/1)
then the count is back to 0. This is because we changed the `Post` object in the DOM to `Index` and back, which resets everything.

This example also illustrates how to prevent this from happening with [`useEffect`](../../../useeffect.md).

Bibliography:
- [https://stackoverflow.com/questions/63143334/how-to-not-persist-state-between-next-js-dynamic-routes](https://stackoverflow.com/questions/63143334/how-to-not-persist-state-between-next-js-dynamic-routes)

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
