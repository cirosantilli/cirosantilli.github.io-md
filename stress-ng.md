# stress-ng

↑ **Parent:** [Computer benchmark](computer-benchmark.md)

The interface is a bit annoying, but the tool is really cool.

100 cycles of `matrixprod`:
```
stress-ng -c1 --cpu-ops 100 --cpu-method matrixprod
```
`man stress-ng` gives the list of possible `--cpu-method`. It documents `matrixprod` as:

> [matrix product](matrix-multiplication.md) of two 128 × 128 matrices of double floats. Testing on 64 bit [x86](x86.md) hardware shows that this is provides a good mix of memory, cache and floating point operations and is probably the best CPU method to use to make a CPU run hot.

If you don't specify the `--cpu-method` it apparently loops through every method one by one.

Limit time to 1s instead of limiting cycles:
```
stress-ng -c1 -t1 --cpu-method matrixprod
```

## ↑ Ancestors (6)

1. [Computer benchmark](computer-benchmark.md)
2. [Computer](computer-split.md)
3. [Information technology](information-technology.md)
4. [Area of technology](area-of-technology.md)
5. [Technology](technology-split.md)
6. [Ciro Santilli's Homepage](split.md)
