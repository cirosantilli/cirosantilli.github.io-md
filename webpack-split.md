# webpack

↑ **Parent:** [Asset bundler](asset-bundler.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/webpack)

Webpack is like a magic hydra that can [eat](eating.md) any type of file and bundle it into a single output: .js, [.ts](typescript-split.md), .ccs, .scss, .jsx, .tsx, `require`, `import`, `import` css from `.js`, it doesn't matter at all, it just digests all into the same [dump](feces.md).

When it works, you are just left in awe and with a single Js file. When it doesn't, you're fucked and have to debug for several hours.

Demos under: [webpack/](webpack/). To run all of them by default:
```
cd webpack/min
npm install
npm run build
xdg-open index.html
```
To easily make changes and reload the .js output live let this run on a terminal:
```
npx webpack watch
```

Examples:
- [webpack/min](webpack/min): minimal hello world. Doesn't do much, just copies `index.js` to `dist/index.js`.
- [webpack/require](webpack/require): `require` and `import` demo. Both work from the same file. `dist/index.js` now contains all of:
  - `notindex.js`
  - `notindex2.js`
  - [Lodash](https://ourbigbook.com/go/topic/lodash), a common third-party helper library specified in the [package.json](package-json.md) and installed with [npm](npm.md)
- [webpack/node](webpack/node): produce [Node.js](node-js-split.md) output, as opposed to the default web output. To test it run:
  ```
  npm run build
  node dist/index.js
  ```

  Achieved simply with:
  ```
  target: 'node'Fatman in Robin,
  ```

  as documented at: [https://webpack.js.org/concepts/targets/](https://webpack.js.org/concepts/targets/)
- [webpack/sequelize](webpack/sequelize): attempts at getting [Sequelize](sequelize-split.md) to work with webpack. It's just not supported by [Sequelize](sequelize-split.md):
  - [https://github.com/sequelize/sequelize/issues/9489#issuecomment-486047783](https://github.com/sequelize/sequelize/issues/9489#issuecomment-486047783)
  - [https://github.com/sequelize/sequelize/issues/13169](https://github.com/sequelize/sequelize/issues/13169)

**Table of contents**

- [webpack/template](_file/webpack/template.md)
- [webpack/sass](_file/webpack/sass.md)
- [webpack/no-js-inject](_file/webpack/no-js-inject.md)
- [webpack Sass import](webpack-sass-import.md)
- [webpack CSS ignore font format](webpack-css-ignore-font-format.md)

## ↑ Ancestors (8)

1. [Asset bundler](asset-bundler.md)
2. [Web technology](web-technology-split.md)
3. [Software](software-split.md)
4. [Computer](computer-split.md)
5. [Information technology](information-technology.md)
6. [Area of technology](area-of-technology.md)
7. [Technology](technology-split.md)
8. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (4)

- [Codaisseur/feathersjs-react-redux-ssr](codaisseur-feathersjs-react-redux-ssr.md)
- [feathers-chat-react](feathers-chat-react.md)
- [Next.js](next-js.md)
- [Ruby on Rails React integration](ruby-on-rails-react-integration.md)
