<h1 id="_file/react/hello.html">react/hello.html</h1>

↑ **Parent:** [React example](../../react-example.md)

Minimal React hello world example. As you click:
- one counter increments every time
- the other increments every two clicks
By opening a web inspector, you can see that only modified elements get updated. So we understand that [JSX](../../react-jsx.md) parses its "HTML-like" into a tree, and then propagates updates on that tree.

By looking at the terminal, we see that `render()` does get called every time the button is clicked, so the tree of elements does get recreated every time. But then React diffes thing out and only updates things in the DOM where needed.

## ↑ Ancestors (12)

1. [React example](../../react-example.md)
2. [React](../../react-split.md)
3. [List of front-end web frameworks](../../list-of-front-end-web-frameworks.md)
4. [Front-end web framework](../../front-end-web-framework.md)
5. [Web framework](../../web-framework.md)
6. [Web technology](../../web-technology-split.md)
7. [Software](../../software-split.md)
8. [Computer](../../computer-split.md)
9. [Information technology](../../information-technology.md)
10. [Area of technology](../../area-of-technology.md)
11. [Technology](../../technology-split.md)
12. [Ciro Santilli's Homepage](../../split.md)

## ← Incoming links (2)

- [react/ref-click-counter.html](ref-click-counter.html.md)
- [React](../../react-split.md)
