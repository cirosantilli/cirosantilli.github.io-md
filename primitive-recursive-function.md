# Primitive recursive function

↑ **Parent:** [Complexity class](complexity-class.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Primitive_recursive_function)

In intuitive terms it consists of all integer functions, possibly with multiple input arguments, that can be written only with a sequence of:
- variable assignments
- addition and subtraction
- integer comparisons and if/else
- [for loops](for-loop.md)

```
for (i = 0; i < n; i++)
```
and such that `n` does not change inside the loop body, i.e. no [while loops](while-loop.md) with arbitrary conditions.

`n` does not have to be a constant, it may come from previous calculations. But it must not change inside the loop body.

[Primitive recursive functions](primitive-recursive-function.md) basically include every integer function that comes up in practice. Primitive recursive functions can have huge complexity, and it strictly contains [EXPTIME](exptime.md). As such, they mostly only come up in [foundation of mathematics](formalization-of-mathematics-split.md) contexts.

The cool thing about [primitive recursive functions](primitive-recursive-function.md) is that the number of iterations is always bound, so we are certain that they terminate and are therefore [computable](computable-problem.md).

This also means that there are necessarily functions which are not [primitive recursive](primitive-recursive-function.md), as we know that there must exist [uncomputable](computable-problem.md) functions, e.g. the [busy beaver function](busy-beaver-function.md).

Adding unbounded [while loops](while-loop.md) of course enables us to simulate arbitrary [Turing machines](turing-machine.md), and therefore increases the [complexity class](complexity-class.md).

More finely, there are [non-primitive total recursive functions](non-primitive-total-recursive-function.md), e.g. most famously the [Ackermann function](ackermann-function.md).

**Table of contents**

- [Non-primitive total recursive function](non-primitive-total-recursive-function.md)
  - [Ackermann function](ackermann-function.md)

## ↑ Ancestors (8)

1. [Complexity class](complexity-class.md)
2. [Computational problem](computational-problem.md)
3. [Computer science](computer-science-split.md)
4. [Computer](computer-split.md)
5. [Information technology](information-technology.md)
6. [Area of technology](area-of-technology.md)
7. [Technology](technology-split.md)
8. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (2)

- [For loop](for-loop.md)
- [Primitive recursive function](primitive-recursive-function.md)
