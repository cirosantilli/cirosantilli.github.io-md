<h1 id="next-js">Next.js</h1>

↑ **Parent:** [React](react-split.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Next.js)

Framework built on top of [React](react-split.md).

Officially recommended by [React](react-split.md)[https://reactjs.org/docs/create-a-new-react-app.html](https://reactjs.org/docs/create-a-new-react-app.html):

> Recommended Toolchains
> 
> If you’re building a server-rendered website with Node.js, try Next.js.

[gothinkster/realworld](gothinkster-realworld.md) blog example by [Ciro Santilli](ciro-santilli-split.md): [node Express Sequelize Next.js realworld example app](node-express-sequelize-next-js-realworld-example-app.md).

Basically what this does is to get [server-side rendering](server-side-rendering.md) just working by [React](react-split.md), including hydration, which is a good thing.

Next.js sends the first pre-rendered HTML page along with the JavaScript code. Then, JavaScript page switches just load the API data.

Next.js does this nicely by forcing you to provide page data in a serialized JSON format, even when rendering server-side (e.g. the return value of `getServerSideProps`). This way, it is also able to provide either the full HTML, or just the JSON.

Some general downsides:
- it does feel like they don't document deployment very well however, especially non-Vercel options, which is the company behind Next.js. I'm unable to find how to use a non Vercel CDN with ISR supposing that is possible.
- Next.js is very opinionated, and like any opinionated library it is sometimes hard to know why something is/isn't happening, and sometimes it is hard/impossible to do what you want with it unless they add support. They have done good progress, but even as of 2022, some aspects just feel so immature, some major-looking use cases are not very well done.

In theory, Next.js could be the "ultimate frontend framework". It does have a lot of development difficulties that need to be ironed out, but the general concepts, and things it tries to integrate, including e.g. [webpack](webpack-split.md), [TypeScript](typescript-split.md), etc. are good. Maybe the question is when will someone put it together with an amazing backend library and dominate and finally put an end to the infinite number of Js Frameworks!

In-tree examples at: [https://github.com/vercel/next.js/tree/canary/examples](https://github.com/vercel/next.js/tree/canary/examples)

`canary` is their `master`: [https://github.com/vercel/next.js/issues/3211](https://github.com/vercel/next.js/issues/3211)

In order to offer its amazing features, Next.js is also extremely opinionated, which means that if something wasn't designed to be possible, it basically isn't.

No prerender with custom [server](server-computing.md)? It forces you to write your API with next as well? Or does it mean something else?
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

"Module not found: Can't resolve 'fs'" [Hell](hell.md). The main reason this happens seems to be the that in a higher order component, [webpack](webpack-split.md) can't determine if callbacks use the require or not to remove it from frontend code. Fully investigated and solved at:
- [https://stackoverflow.com/questions/64926174/module-not-found-cant-resolve-fs-in-next-js-application/70363153#70363153](https://stackoverflow.com/questions/64926174/module-not-found-cant-resolve-fs-in-next-js-application/70363153#70363153)

Overviews:
- [https://www.reddit.com/r/reactjs/comments/8evy5d/what_are_the_downsides_to_nextjs/](https://www.reddit.com/r/reactjs/comments/8evy5d/what_are_the_downsides_to_nextjs/) 2017 What are the downsides to Next.js?

TODO answer:
- [https://stackoverflow.com/questions/59674496/how-to-pass-pageprops-in-next-js-from-a-child-component-to-app-js](https://stackoverflow.com/questions/59674496/how-to-pass-pageprops-in-next-js-from-a-child-component-to-app-js)

**Table of contents**

- [Next.js example](next-js-example.md)
  - [nodejs/next/posts](_file/nodejs/next/posts.md)
  - [nodejs/next/ref-twice](_file/nodejs/next/ref-twice.md)
  - [nodejs/next/inject-into-static](_file/nodejs/next/inject-into-static.md)
- [Node Express Sequelize Next.js realworld example app](node-express-sequelize-next-js-realworld-example-app.md)

## ↑ Ancestors (11)

1. [React](react-split.md)
2. [List of front-end web frameworks](list-of-front-end-web-frameworks.md)
3. [Front-end web framework](front-end-web-framework.md)
4. [Web framework](web-framework.md)
5. [Web technology](web-technology-split.md)
6. [Software](software-split.md)
7. [Computer](computer-split.md)
8. [Information technology](information-technology.md)
9. [Area of technology](area-of-technology.md)
10. [Technology](technology-split.md)
11. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (6)

- [react/ref-twice.html](_file/react/ref-twice.html.md)
- [Leanpub](leanpub.md)
- [OurBigBook.com](ourbigbook-com-top-project.md)
- [React](react-split.md)
- [Further improvements to the website's base technology](sponsor/updates/4/further-improvements-to-the-website-s-base-technology.md)
- [How the tech improved](updates/ourbigbook-project-update-march-2025/how-the-tech-improved.md)
