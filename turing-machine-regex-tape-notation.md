# Turing machine regex tape notation

↑ **Parent:** [Turing machine decider](turing-machine-decider.md)

[Turing machine regex tape notation](turing-machine-regex-tape-notation.md) is [Ciro Santilli](ciro-santilli-split.md)'s made up name for the notation used e.g. at:
- [https://www.sligocki.com/2023/02/02/skelet-34.html](https://www.sligocki.com/2023/02/02/skelet-34.html)
- [https://www.sligocki.com/2022/06/10/ctl.html](https://www.sligocki.com/2022/06/10/ctl.html)
Most of it is just regular [regular expression](regular-expression.md) notation, with a few differences:
- $0^{\inf}$ denotes the right or left edge of the (zero initialized) tape. It is often omitted as we always just assume it is always present on both sides of every regex
- `A`, `B`, `C`, `D` and `E` denotes the current machine state. This is especially common notation in the context of the [BB(5)](bb-5.md) problem
- `<` and `>` next to the state indicate if the head is on top of the left or right element. E.g.:
  ```
  11 (01)^n <A 00 (0011)^{n+2}
  ```

  indicates that the head `A` is on top of the last `1` of the last sequence of n `01`s to the left of the head.

This notation is very useful, as it helps compress long repeated sequences of [Turing machine](turing-machine.md) tape and extract higher level patterns from them, which is how you go about understanding a Turing machine in order to apply [Turing machine acceleration](turing-machine-acceleration.md).

## ↑ Ancestors (10)

1. [Turing machine decider](turing-machine-decider.md)
2. [Halting problem](halting-problem.md)
3. [Decision problem](decision-problem.md)
4. [Computational problem](computational-problem.md)
5. [Computer science](computer-science-split.md)
6. [Computer](computer-split.md)
7. [Information technology](information-technology.md)
8. [Area of technology](area-of-technology.md)
9. [Technology](technology-split.md)
10. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (1)

- [Turing machine regex tape notation](turing-machine-regex-tape-notation.md)
