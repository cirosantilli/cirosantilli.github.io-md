<h1 id="_file/webpack/template">webpack/template</h1>

↑ **Parent:** [webpack](../../webpack-split.md)

[webpack/template](webpack/template) contains a reasonable starter template.

This will produce, under `dist/` the following minimized files:
- `dist/index.html`: from [webpack/template/index.html](webpack/template/index.html). You can open it to see:
  ```
  Hello webpack
  ```

  show on the browser. This was added from [JavaScript](../../javascript.md).
- `dist/index.js`: from [webpack/template/index.js](webpack/template/index.js) and anything in its import tree, e.g.:
  - [webpack/template/main.scss](webpack/template/main.scss): [sass](../../sass-stylesheet-language.md) source. It gets embedded the the [JavaScript](../../javascript.md) output as a string, and the JavaScript then applies it to the page, making the font blue
  - `lodash` third party library

You can also run this test with the development server on [http://localhost:9000](http://localhost:9000):
```
npm start
```
which uses unminimized outptus, and automatically push reloads the page whenever you change any of the input files!

## ↑ Ancestors (9)

1. [webpack](../../webpack-split.md)
2. [Asset bundler](../../asset-bundler.md)
3. [Web technology](../../web-technology-split.md)
4. [Software](../../software-split.md)
5. [Computer](../../computer-split.md)
6. [Information technology](../../information-technology.md)
7. [Area of technology](../../area-of-technology.md)
8. [Technology](../../technology-split.md)
9. [Ciro Santilli's Homepage](../../split.md)

## ← Incoming links (1)

- [webpack/no-js-inject](no-js-inject.md)
