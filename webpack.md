# webpack

↑ **Parent:** [Asset bundler](web-technology.md#asset-bundler)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/webpack)

Webpack is like a magic hydra that can [eat](biology.md#eating) any type of file and bundle it into a single output: .js, [.ts](typescript.md), .ccs, .scss, .jsx, .tsx, `require`, `import`, `import` css from `.js`, it doesn't matter at all, it just digests all into the same [dump](molecular-biology.md#feces).

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
  - [Lodash](https://ourbigbook.com/go/topic/lodash), a common third-party helper library specified in the [package.json](node-js.md#package-json) and installed with [npm](node-js.md#npm)
- [webpack/node](webpack/node): produce [Node.js](node-js.md) output, as opposed to the default web output. To test it run:
  ```
  npm run build
  node dist/index.js
  ```

  Achieved simply with:
  ```
  target: 'node'Fatman in Robin,
  ```

  as documented at: [https://webpack.js.org/concepts/targets/](https://webpack.js.org/concepts/targets/)
- [webpack/sequelize](webpack/sequelize): attempts at getting [Sequelize](sequelize.md) to work with webpack. It's just not supported by [Sequelize](sequelize.md):
  - [https://github.com/sequelize/sequelize/issues/9489#issuecomment-486047783](https://github.com/sequelize/sequelize/issues/9489#issuecomment-486047783)
  - [https://github.com/sequelize/sequelize/issues/13169](https://github.com/sequelize/sequelize/issues/13169)

**Table of contents**

- [webpack/template](#_file/webpack/template)
- [webpack/sass](#_file/webpack/sass)
- [webpack/no-js-inject](#_file/webpack/no-js-inject)
- [webpack Sass import](#webpack-sass-import)
- [webpack CSS ignore font format](#webpack-css-ignore-font-format)

<h2 id="_file/webpack/template">webpack/template</h2>

↑ **Parent:** [webpack](webpack.md)

[webpack/template](webpack/template) contains a reasonable starter template.

This will produce, under `dist/` the following minimized files:
- `dist/index.html`: from [webpack/template/index.html](webpack/template/index.html). You can open it to see:
  ```
  Hello webpack
  ```

  show on the browser. This was added from [JavaScript](programming-language.md#javascript).
- `dist/index.js`: from [webpack/template/index.js](webpack/template/index.js) and anything in its import tree, e.g.:
  - [webpack/template/main.scss](webpack/template/main.scss): [sass](web-technology.md#sass-stylesheet-language) source. It gets embedded the the [JavaScript](programming-language.md#javascript) output as a string, and the JavaScript then applies it to the page, making the font blue
  - `lodash` third party library

You can also run this test with the development server on [http://localhost:9000](http://localhost:9000):
```
npm start
```
which uses unminimized outptus, and automatically push reloads the page whenever you change any of the input files!

<h2 id="_file/webpack/sass">webpack/sass</h2>

↑ **Parent:** [webpack](webpack.md)

This example shows how to use [Sass](web-technology.md#sass-stylesheet-language).

To make things simple, it generates a completely separate `dist/index.js` and `dist/main.css` which are manually included from `index.html`, and does not do any type of injection (neither Js into HTML nor CSS in Js).

<h2 id="_file/webpack/no-js-inject">webpack/no-js-inject</h2>

↑ **Parent:** [webpack](webpack.md)

This example shows how you could manually include the `dist/index.js` that is output from webpack into your `index.html`.

This is generally not what you want to do, because what you actually want to do is to use a Js output name with a hash in it, so that browsers only need to refetch when the name changes.

And to do that, we have to let webpack dynamically inject that unpredictable hash as done in [webpack/template](#_file/webpack/template) with:
```
new HtmlWebpackPlugin({
  filename: 'index.html',
  // Inject the include to our hashed filename,
  // since it is not deterministic due to the hash.
  inject: true,
  template: path.resolve(__dirname, 'index.html'),
}),
```

## webpack Sass import

↑ **Parent:** [webpack](webpack.md)

This shows how to produce a minimized fully embedded CSS file with webpack from a [sass](web-technology.md#sass-stylesheet-language):
```
cd webpack/sass
npm install
npm run build
xdg-open index.html
```
That example produces a `dist/main.css` file which is a compresesd combination of:
- [webpack/sass/main.scss](webpack/sass/main.scss)
- [normalize.css](https://necolas.github.io/normalize.css/), added to the project as a regular `node_modules` package

## webpack CSS ignore font format

↑ **Parent:** [webpack](webpack.md)

- [https://stackoverflow.com/questions/37667444/is-there-a-way-to-ignore-a-file-type-with-webpack/39886771#39886771](https://stackoverflow.com/questions/37667444/is-there-a-way-to-ignore-a-file-type-with-webpack/39886771#39886771)
- [https://stackoverflow.com/questions/71320578/how-to-ignore-exclude-certain-font-formats-font-face-in-css-with-webpack](https://stackoverflow.com/questions/71320578/how-to-ignore-exclude-certain-font-formats-font-face-in-css-with-webpack)
- [https://github.com/cherrry/ignore-loader/issues/8](https://github.com/cherrry/ignore-loader/issues/8)

## ↑ Ancestors (8)

1. [Asset bundler](web-technology.md#asset-bundler)
2. [Web technology](web-technology.md)
3. [Software](software.md)
4. [Computer](computer.md)
5. [Information technology](technology.md#information-technology)
6. [Area of technology](technology.md#area-of-technology)
7. [Technology](technology.md)
8. [Ciro Santilli's Homepage](README.md)

## ← Incoming links (4)

- [Codaisseur/feathersjs-react-redux-ssr](node-js.md#codaisseur-feathersjs-react-redux-ssr)
- [feathers-chat-react](node-js.md#feathers-chat-react)
- [Next.js](react.md#next-js)
- [Ruby on Rails React integration](programming-language.md#ruby-on-rails-react-integration)
