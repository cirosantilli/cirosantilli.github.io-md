# CPython JIT

↑ **Parent:** [CPython](cpython.md)

Added in [CPython 3.13](cpython-3-13.md).

To enable tested on [Ubuntu 25.04](ubuntu-25-04.md):
```
git clone https://github.com/python/cpython
cd cpython
git checkout v3.13.7
./configure --enable-experimental-jit
make -j
```

However, the JIT appears to be useless tested as of this Python version, lol:
- [https://news.ycombinator.com/item?id=44476023](https://news.ycombinator.com/item?id=44476023)
- [https://devclass.com/2025/07/09/despite-30-months-work-core-developer-says-pythons-jit-compiler-is-often-slower-than-the-interpreter/](https://devclass.com/2025/07/09/despite-30-months-work-core-developer-says-pythons-jit-compiler-is-often-slower-than-the-interpreter/)
- [https://fidget-spinner.github.io/posts/jit-reflections.html](https://fidget-spinner.github.io/posts/jit-reflections.html)

We can try to test it with [python/inc_loop.py](python/inc_loop.py):
```
time ./python python/inc_loop.py 10000000
```
but the result is just as pathetic as without JIT currently, taking about 1 second for only 10m loops.

This can be compared with the optimal assembly from [c/inc_loop_asm.c](c/inc_loop_asm.c):
```
time ./inc_loop_asm.out 1000000000
```
which does 1 billion loops in about half a second on [P14s](ciro-santilli-s-hardware/lenovo-thinkpad-p14s-gen4-amd.md).

For comparison, [PyPy](pypy.md) actually speeds things up and does 1 billion loops in about a second, so only 2x worse than native.

TODO triple check that JIT is enabled. Many threads say the command is:
```
./python -c 'import sysconfig; sysconfig.get_config_var("JIT_DEPS")'
```
but that fails with:
```
ModuleNotFoundError: No module named '_sysconfigdata__linux_x86_64-linux-gnu'
```

For comparison with a properly implemented dynamic language JIT running [nodejs/inc_loop.js](nodejs/inc_loop.js) does 1 billion loops in 0.6s on v22.14.0, close to native.

[https://tonybaloney.github.io/posts/python-gets-a-jit.html](https://tonybaloney.github.io/posts/python-gets-a-jit.html) documents what the initial "JIT" implementation does. It is just an extremely naive concatenation of instructions that avoids a for + switch. No wonder it doesn't speed things up much at all.

## ↑ Ancestors (11)

1. [CPython](cpython.md)
2. [Python implementation](python-implementation.md)
3. [Python (programming language)](python-programming-language.md)
4. [List of programming languages](list-of-programming-languages.md)
5. [Programming language](programming-language-split.md)
6. [Software](software-split.md)
7. [Computer](computer-split.md)
8. [Information technology](information-technology.md)
9. [Area of technology](area-of-technology.md)
10. [Technology](technology-split.md)
11. [Ciro Santilli's Homepage](split.md)
