<h1 id="_file/c/inc_loop_asm_n.sh">c/inc_loop_asm_n.sh</h1>

↑ **Parent:** [CPU microbenchmark](../../cpu-microbenchmark.md)

This is a quick [Microarchitectural benchmark](../../microarchitectural-benchmark.md) to try and determine how many [functional units](../../cpu-functional-unit.md) our CPU has that can do an `inc` instruction at the same time due to [superscalar architecture](../../superscalar-processor.md).

The generated programs do loops like:
```
loop:
  inc %[i0];
  inc %[i1];
  inc %[i2];
  ...
  inc %[i_n];
  cmp %[max], %[i0];
  jb loop;
```
with different numbers of inc instructions.

<a id="image-c-inc-loop-asm-n-sh-results-for-a-few-cpus"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/refs/heads/master/c/inc_loop_asm_n_manual.png" alt="" height="480">

**[Figure 2](#image-c-inc-loop-asm-n-sh-results-for-a-few-cpus). c/inc_loop_asm_n.sh results for a few CPUs**. Quite clearly:
- [AMD 7840U](../../amd-7840u.md) can run INC on 4 functional units
- [Intel i7-7820HQ](../../intel-i7-7820hq.md) can run INC on 2 functional units
and both have low instruction count effects that destroy performance, AMD at 3 and Intel at 3 and 5. TODO it would be cool to understand those better.

Data from multiple CPUs manually collated and plotted manually with [c/inc_loop_asm_n_manual.sh](c/inc_loop_asm_n_manual.sh).

---

Announced at:
- [https://mastodon.social/@cirosantilli/114698665154298332](https://mastodon.social/@cirosantilli/114698665154298332)
- [https://x.com/cirosantilli/status/1934950348663214211](https://x.com/cirosantilli/status/1934950348663214211)
- [https://www.linkedin.com/feed/update/urn:li:ugcPost:7340716961170898944/](https://www.linkedin.com/feed/update/urn:li:ugcPost:7340716961170898944/)

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

## ← Incoming links (1)

- [c/inc_loop_asm_n.sh](inc_loop_asm_n.sh.md)
