# Big O notation

↑ **Parent:** [Big O notation family](big-o-notation-family.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Big_O_notation)

Module bound above, possibly multiplied by a constant:

$$
f(x) = O(g(x))
$$

is defined as:

$$
\exists M > 0 \exists x_0  \forall x > x_0 \colon |f(x)| \leq M g(x)
$$

E.g.:
- $\forall c \in \R x + c = O(x)$. For $c < 0$, $M = 1$ is enough. Otherwise, any $M > 1$ will do, the bottom line will always catch up to the top one eventually.

## ↑ Ancestors (9)

1. [Big O notation family](big-o-notation-family.md)
2. [Complexity class](complexity-class.md)
3. [Computational problem](computational-problem.md)
4. [Computer science](computer-science-split.md)
5. [Computer](computer-split.md)
6. [Information technology](information-technology.md)
7. [Area of technology](area-of-technology.md)
8. [Technology](technology-split.md)
9. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (3)

- [Big O notation family](big-o-notation-family.md)
- [Dense and sparse matrices](dense-and-sparse-matrices.md)
- [Little-o notation](little-o-notation.md)
