<h1 id="_file/c/inc_loop_asm.c">c/inc_loop_asm.c</h1>

↑ **Parent:** [CPU microbenchmark](../../cpu-microbenchmark.md)

This is the only way that we've managed to reliably get a single `inc` instruction loop, by using [inline assembly](../../inline-assembly.md), e.g. on we do [x86](../../x86.md):
```
loop:
  inc %[i];
  cmp %[max], %[i];
  jb loop;
```

For 1s on [P14s](../../ciro-santilli-s-hardware/lenovo-thinkpad-p14s-gen4-amd.md) [Ubuntu 25.04](../../ubuntu-25-04.md) GCC 14.2 -O0 x86\_64 we need about 5 billion:
```
time ./inc_loop_asm.out 5000000000
```

## ↑ Ancestors (9)

1. [CPU microbenchmark](../../cpu-microbenchmark.md)
2. [Microarchitectural benchmark](../../microarchitectural-benchmark.md)
3. [Microarchitecture](../../microarchitecture.md)
4. [Computer hardware](../../computer-hardware-split.md)
5. [Computer](../../computer-split.md)
6. [Information technology](../../information-technology.md)
7. [Area of technology](../../area-of-technology.md)
8. [Technology](../../technology-split.md)
9. [Ciro Santilli's Homepage](../../split.md)
