# Matrix multiplication

↑ **Parent:** [Matrix](matrix.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Matrix_multiplication)

Since a [matrix](matrix.md) $M$ can be seen as a [linear map](linear-map.md) $f_M(\vec{x})$, the product of two matrices $MN$ can be seen as the composition of two [linear maps](linear-map.md):

$$
f_M(f_N(\vec{x}))
$$

One cool thing about linear functions is that we can easily pre-calculate this product only once to obtain a new matrix, and so we don't have to do both multiplications separately each time.

**Table of contents**

- [System of linear equations](system-of-linear-equations.md)
  - [Application of systems of linear equations](application-of-systems-of-linear-equations.md)
  - [System of linear equations algorithm](system-of-linear-equations-algorithm.md)
    - [LINPACK benchmarks](linpack-benchmarks.md)
    - [Conjugate gradient method](conjugate-gradient-method.md)
- [Application of matrix multiplication](application-of-matrix-multiplication.md)
- [Matrix multiplication algorithm](matrix-multiplication-algorithm.md)
  - [General matrix matrix multiplication](general-matrix-matrix-multiplication.md)
    - [Strassen algorithm](strassen-algorithm.md)
  - [Multiplication of matrices of specific size](multiplication-of-matrices-of-specific-size.md)
    - [Commutative matrix multiplication algorithm](commutative-matrix-multiplication-algorithm.md)
    - [2x2 matrix multiplication](2x2-matrix-multiplication.md)
    - [3x3 matrix multiplication](3x3-matrix-multiplication.md)
- [Matrix decomposition](matrix-decomposition.md)

## ↑ Ancestors (6)

1. [Matrix](matrix.md)
2. [Linear algebra](linear-algebra-split.md)
3. [Algebra](algebra-split.md)
4. [Area of mathematics](area-of-mathematics.md)
5. [Mathematics](mathematics-split.md)
6. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (9)

- [Python/pytorch/matmul.py](_file/python/pytorch/matmul.py.md)
- [General linear group](general-linear-group.md)
- [Invertible matrix](invertible-matrix.md)
- [Lie algebra of a matrix Lie group](lie-algebra-of-a-matrix-lie-group.md)
- [Linear map](linear-map.md)
- [Matrix ring](matrix-ring.md)
- [Programmer's model of quantum computers](programmer-s-model-of-quantum-computers.md)
- [Transpose of a matrix multiplication](transpose-of-a-matrix-multiplication.md)
- [Understanding the state of 3x3 matrix multiplication](updates/understanding-the-state-of-3x3-matrix-multiplication.md)
