<h1 id="_file/webpack/no-js-inject">webpack/no-js-inject</h1>

↑ **Parent:** [webpack](../../webpack-split.md)

This example shows how you could manually include the `dist/index.js` that is output from webpack into your `index.html`.

This is generally not what you want to do, because what you actually want to do is to use a Js output name with a hash in it, so that browsers only need to refetch when the name changes.

And to do that, we have to let webpack dynamically inject that unpredictable hash as done in [webpack/template](template.md) with:
```
new HtmlWebpackPlugin({
  filename: 'index.html',
  // Inject the include to our hashed filename,
  // since it is not deterministic due to the hash.
  inject: true,
  template: path.resolve(__dirname, 'index.html'),
}),
```

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
