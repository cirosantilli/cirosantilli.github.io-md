<h1 id="next-js-example">Next.js example</h1>

↑ **Parent:** [Next.js](next-js.md)

Our examples are located under [nodejs/next](nodejs/next):
- [nodejs/next/hello-world](nodejs/next/hello-world): a hello world. There's an in-tree one at: [https://github.com/vercel/next.js/tree/e75361fd03872b097e817634c049b3185f24cf56/examples/hello-world](https://github.com/vercel/next.js/tree/e75361fd03872b097e817634c049b3185f24cf56/examples/hello-world), but ours is truly minimal
- [nodejs/next/hoc](nodejs/next/hoc): shows how to use a higher order component (HOC) to factor out `getStaticProps` across two pages: [nodejs/next/hoc/pages/index.js](nodejs/next/hoc/pages/index.js) and [nodejs/next/hoc/pages/notindex.js](nodejs/next/hoc/pages/notindex.js)
- [nodejs/next/typescript](nodejs/next/typescript): simple [TypeScript](typescript-split.md) example, minimized from: [https://github.com/vercel/next.js/tree/d61b0761efae09bd9cb1201ff134ed8950d9deca/examples/with-typescript](https://github.com/vercel/next.js/tree/d61b0761efae09bd9cb1201ff134ed8950d9deca/examples/with-typescript)

  Notably, that shows how `require` errors are avoided in that case as mentioned at: [https://stackoverflow.com/questions/64926174/module-not-found-cant-resolve-fs-in-next-js-application/70363153#70363153](https://stackoverflow.com/questions/64926174/module-not-found-cant-resolve-fs-in-next-js-application/70363153#70363153)
- [nodejs/next/localStorage](nodejs/next/localStorage): a counter that is persistent across page reloads by using `localStorage`. Used in: [https://stackoverflow.com/questions/54819721/next-js-access-localstorage-before-rendering-page/68136224#68136224](https://stackoverflow.com/questions/54819721/next-js-access-localstorage-before-rendering-page/68136224#68136224)

Solved ones:
- solved by [preview mode](https://nextjs.org/docs/advanced-features/preview-mode) in Next.js 12:
  - ISR was basically unusable for CRUD websites because you can't force a one-off immediate page update:
    - [https://github.com/vercel/next.js/discussions/25677](https://github.com/vercel/next.js/discussions/25677)

**Table of contents**

- [nodejs/next/posts](_file/nodejs/next/posts.md)
- [nodejs/next/ref-twice](_file/nodejs/next/ref-twice.md)
- [nodejs/next/inject-into-static](_file/nodejs/next/inject-into-static.md)

## ↑ Ancestors (12)

1. [Next.js](next-js.md)
2. [React](react-split.md)
3. [List of front-end web frameworks](list-of-front-end-web-frameworks.md)
4. [Front-end web framework](front-end-web-framework.md)
5. [Web framework](web-framework.md)
6. [Web technology](web-technology-split.md)
7. [Software](software-split.md)
8. [Computer](computer-split.md)
9. [Information technology](information-technology.md)
10. [Area of technology](area-of-technology.md)
11. [Technology](technology-split.md)
12. [Ciro Santilli's Homepage](split.md)
