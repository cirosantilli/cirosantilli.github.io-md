# webpack Sass import

↑ **Parent:** [webpack](webpack-split.md)

This shows how to produce a minimized fully embedded CSS file with webpack from a [sass](sass-stylesheet-language.md):
```
cd webpack/sass
npm install
npm run build
xdg-open index.html
```
That example produces a `dist/main.css` file which is a compresesd combination of:
- [webpack/sass/main.scss](webpack/sass/main.scss)
- [normalize.css](https://necolas.github.io/normalize.css/), added to the project as a regular `node_modules` package

## ↑ Ancestors (9)

1. [webpack](webpack-split.md)
2. [Asset bundler](asset-bundler.md)
3. [Web technology](web-technology-split.md)
4. [Software](software-split.md)
5. [Computer](computer-split.md)
6. [Information technology](information-technology.md)
7. [Area of technology](area-of-technology.md)
8. [Technology](technology-split.md)
9. [Ciro Santilli's Homepage](split.md)
