# How to convert `async` to sync in JavaScript

↑ **Parent:** [`Async` (JavaScript)](async-javascript.md)

[God](god.md), it's impossible! You just have to convert the entire fucking call stack all the way up to async functions. It could mean refactoring hundreds of functions.

To be fair, there is a logic to this, if you put yourself within the crappiness of the [JavaScript](javascript.md) threading model. And [Python](python-programming-language.md) is not that much better with its [Global Interpreter Lock](global-interpreter-lock.md).

The problem is that async was introduced relatively late, previously we just had to use infinitely deep callback [trees](tree-data-structure.md), which was worse:
```
myAsync().then(ret => myAsync2(ret).then(ret2 => myAsync3(re3)))
```
compared to the new infinitely more readable:
```
ret = await myAsync()
ret2 = await myAsync2(ret)
ret3 = await myAsync3(ret3)
```
But now we are in an endless period of transition between both worlds.

It is also worth mentioning that callbacks are still inescapable if you really want to fan out into a non-linear dependency graph, usually with `Promise.all`:
```
await Promise.all([
  myAsync(1).then(ret => myAsync2(ret)),
  myAsync(2).then(ret => myAsync2(ret)),
])
```

Bibliography:
- [https://stackoverflow.com/questions/21819858/how-to-wrap-async-function-calls-into-a-sync-function-in-node-js-or-javascript](https://stackoverflow.com/questions/21819858/how-to-wrap-async-function-calls-into-a-sync-function-in-node-js-or-javascript)
- [https://stackoverflow.com/questions/9121902/call-an-asynchronous-javascript-function-synchronously](https://stackoverflow.com/questions/9121902/call-an-asynchronous-javascript-function-synchronously)
- [https://stackoverflow.com/questions/47227550/using-await-inside-non-async-function](https://stackoverflow.com/questions/47227550/using-await-inside-non-async-function)
- [https://stackoverflow.com/questions/43832490/is-it-possible-to-use-await-without-async-in-js](https://stackoverflow.com/questions/43832490/is-it-possible-to-use-await-without-async-in-js)
- [https://stackoverflow.com/questions/6921895/synchronous-delay-in-code-execution](https://stackoverflow.com/questions/6921895/synchronous-delay-in-code-execution)

And then, after many many hours of this work, you might notice that the new code is way, way way slower than before, because making small functions `async` has a large performance impact: [https://madelinemiller.dev/blog/javascript-promise-overhead/](https://madelinemiller.dev/blog/javascript-promise-overhead/). Real world case with a 4x slowdown: [https://github.com/ourbigbook/ourbigbook/tree/async-slow](https://github.com/ourbigbook/ourbigbook/tree/async-slow).

Anyways, since you Googled here, you might as well learn the standard pattern to convert callbacks functions into async functions using a promise: [https://stackoverflow.com/questions/4708787/get-password-from-input-using-node-js/71868483#71868483](https://stackoverflow.com/questions/4708787/get-password-from-input-using-node-js/71868483#71868483)

<a id="image-async-function-teletubbies-meme"></a>
<img src="https://web.archive.org/web/20241129001302im_/https://miro.medium.com/v2/resize:fit:828/format:webp/0*-sXUj7txIyw9LX_F" alt="" height="800">

**[Figure 3](#image-async-function-teletubbies-meme). async function Teletubbies meme**. [Source](https://andrewzuo.com/async-await-is-the-worst-thing-to-happen-to-programming-9b8f5150ba74). TODO find original source.

## ↑ Ancestors (11)

1. [`Async` (JavaScript)](async-javascript.md)
2. [JavaScript language](javascript-language.md)
3. [JavaScript](javascript.md)
4. [List of programming languages](list-of-programming-languages.md)
5. [Programming language](programming-language-split.md)
6. [Software](software-split.md)
7. [Computer](computer-split.md)
8. [Information technology](information-technology.md)
9. [Area of technology](area-of-technology.md)
10. [Technology](technology-split.md)
11. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (2)

- [`Async` (JavaScript)](async-javascript.md)
- [Node.js](node-js-split.md)
