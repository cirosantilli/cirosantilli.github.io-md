<h1 id="_file/react/ref-click-counter.html">react/ref-click-counter.html</h1>

↑ **Parent:** [React DOM manipulation](../../react-dom-manipulation.md)

Dummy example of using a [React `ref`](../../react-dom-manipulation.md) This example is useless and to the end user seems functionally equivalent to [react/hello.html](hello.html.md).

It does however serve as a good example of what react does that is useful: it provides a "clear" separation between state and render code (which becomes once again much less clear in [React function components](../../react-function-component.md).

Notably, this example is insane because at:
```
<button onClick={() => {
  elem.innerHTML = (parseInt(elem.innerHTML) + 1).toString()
```
we are extracing state from some random HTML string rather than having a clean [JavaScript](../../javascript.md) variable containing that value.

In this case we managed to get away with it, but this is in general not easy/possible.

## ↑ Ancestors (12)

1. [React DOM manipulation](../../react-dom-manipulation.md)
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

## ← Incoming links (1)

- [react/ref-click-counter-func.html](ref-click-counter-func.html.md)
