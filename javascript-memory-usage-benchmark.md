# JavaScript memory usage benchmark

↑ **Parent:** [Node.js example](node-js-example.md)

In this section we will use the file [nodejs/bench_mem.js](nodejs/bench_mem.js), tests are run on Node.js v16.14.2 from NVM, Ubuntu 21.10, on [Lenovo ThinkPad P51 (2017)](ciro-santilli-s-hardware/lenovo-thinkpad-p51-2017.md) which has 32 GB RAM.

Related answer: [https://stackoverflow.com/questions/12023359/what-do-the-return-values-of-node-js-process-memoryusage-stand-for/72043884#72043884](https://stackoverflow.com/questions/12023359/what-do-the-return-values-of-node-js-process-memoryusage-stand-for/72043884#72043884)

First using `topp` from [https://stackoverflow.com/questions/1221555/retrieve-cpu-usage-and-memory-usage-of-a-single-process-on-linux/40576129#40576129](https://stackoverflow.com/questions/1221555/retrieve-cpu-usage-and-memory-usage-of-a-single-process-on-linux/40576129#40576129) let's observe the memory usage of some baseline cases.

A C hello world with an infinite loop at the end has:
- 2.7 MB
- 770 KB

For a Node.js infinite loop [nodejs/infinite_loop.js](nodejs/infinite_loop.js)
```
topp infinite_loop.js
```
This gives approximately:
- RSS: 20 MB
- VSZ: 230 MB

Adding a single hello world to it as in [nodejs/infinite_hello.js](nodejs/infinite_hello.js) and running:
```
topp infinite_hello.js
```
leads to:
- RSS: 26 MB
- VSZ: 580 MB
We understand that Node.js preallocates VSZ wildly. No big deal, but it does mean that VSZ is a useless measure for Node.js.

Forcing garbage collection as in [nodejs/infinite_hello.js](nodejs/infinite_hello.js) brings it down to 20 MB however:
```
topp node --expose-gc infinite_hello_gc.js
```

Finally let's see a baseline for `process.memoryUsage` [nodejs/infinite_memoryusage.js](nodejs/infinite_memoryusage.js):
```
node --expose-gc infinite_memoryusage.js
```
which gives initially:
```
{
  rss: 23851008,
  heapTotal: 6987776,
  heapUsed: 3674696,
  external: 285296,
  arrayBuffers: 10422
}
```
but after a few seconds randomly jumps to:
```
{
  rss: 26005504,
  heapTotal: 9084928,
  heapUsed: 3761240,
  external: 285296,
  arrayBuffers: 10422
}
```
so we understand that
- `heapUsed` seems constant at 3.7 MB
- `heapTotal` is a very noisy, as it starts at 7 MB, but randomly jumps to 9 MB at one point without apparent reason

Now let's run our main test program.

First a baseline case with an array of length 1:
```
node --expose-gc bench_mem.js n 1
```
This gives the same results as `node --expose-gc infinite_memoryusage.js`. The same result is obtained by doing:
```
a = undefined
```
with:
```
node --expose-gc bench_mem.js dealloc
```

Not let's vary the size of `n` a bit with:
```
node --expose-gc bench_mem.js n N
```
which gives:

| N | `heapUsed` | `heapTotal` | `rss` | `heapUsed` per elem | `rss` per elem |
| --- | --- | --- | --- | --- | --- |
| 1 M | 14 MB | 48 MB | 56 MB | 10 | 30 |
| 10 M | 122 MB | 157 MB | 176 MB | 18 | 15 |
| 100 M | 906 MB | 940 MB | 960 MB | 9 | 9.3 |

"`rss` per elem" is calculated as: `rss` - 26 MB, where 26 MB is the baseline RSS seen on `n 1`.

Similarly "`heapUsed` per elem" deduces the 4 MB (approximation of the above 3.7 MB) seen on `n 1`.

Note that to reach [MAX\_SAFE\_INTEGER](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number/MAX_SAFE_INTEGER) we would need 8 bytes per elem worst case.

Everything below 100 million (8) is therefore very memory wasteful in terms of RSS.

If we use `Int32Array` typed array buffers instead of a simple `Array`:
```
node --expose-gc bench_mem.js array-buffer n N
```
we see that the memory is now, unsurprisingly, accounted for under `arrayBuffers`, e.g. for `N` 1 million:
```
{
  rss: 31776768,
  heapTotal: 6463488,
  heapUsed: 3674520,
  external: 4285296,
  arrayBuffers: 4010422
}
```
Results for different N:
```
|| N
|| `arrayBuffers`
|| `rss`
|| `rss` per elem

| 1 M
| 4 MB
| 31 MB
| 5

| 10 M
| 40 MB
| 67 MB
| 4.6

| 100 M
| 40 MB
| 427 MB
| 4
```
We see therefore that typed arrays are much closer to what they advertise (4 bytes per element), even for smaller element counts, as expected.

Now let's try one million objects of type `{ a: 1, b: -1 }`:
```
node --expose-gc bench_mem.js obj
```
gives:
```
{
  rss: 138969088,
  heapTotal: 105246720,
  heapUsed: 70103896,
  external: 285296,
  arrayBuffers: 10422
}
```
Disaster! Memory usage is up to 70 MB! Why?? We were expecting only about 24, 4 baseline + 2 \* 10 for each million int?!

And now an equivalent version using `class`:
```
node --expose-gc bench_mem.js class
```
gives the same result.

Let's try Array:
```
node --expose-gc bench_mem.js arr
```
is even worse at 78 MB!! OMG why.
```
{
  rss: 164597760,
  heapTotal: 129363968,
  heapUsed: 78117008,
  external: 285296,
  arrayBuffers: 10422
}
```

Let's change the number of fields on the object? First as a sanity check:
```
node --expose-gc bench_mem.js obj 2
```
produces as expected the smae result as:
```
node --expose-gc bench_mem.js obj
```
so adding properties one by one doesn't change anything from creating the literal all at once. Good.

Now:
```
node --expose-gc bench_mem.js obj N
```
gives `heapUsed`:
- 1: 70M
- 2: 70M
- 3: 70M
- 4: 70M
- 5: 110M
- 6: 110M
- 7: 110M
- 8: 134M
- 9: 134M
- 10: 134M
- 11: 158M

## ↑ Ancestors (11)

1. [Node.js example](node-js-example.md)
2. [Node.js](node-js-split.md)
3. [JavaScript](javascript.md)
4. [List of programming languages](list-of-programming-languages.md)
5. [Programming language](programming-language-split.md)
6. [Software](software-split.md)
7. [Computer](computer-split.md)
8. [Information technology](information-technology.md)
9. [Area of technology](area-of-technology.md)
10. [Technology](technology-split.md)
11. [Ciro Santilli's Homepage](split.md)
