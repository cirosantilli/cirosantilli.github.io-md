# Commutative matrix multiplication algorithm

↑ **Parent:** [Multiplication of matrices of specific size](multiplication-of-matrices-of-specific-size.md)

A "commutative matrix multiplication algorithm" is a matrix multiplication algorithm that requires the ring to be commutative. Such algorithms are inferior because you cannot use them to create more efficient algorithms for [general matrix matrix multiplication](general-matrix-matrix-multiplication.md) by decomposing the bigger matrix into smaller ones.

For example, the [Strassen algorithm](strassen-algorithm.md) is based on reduction to non-commutative [2x2 matrix multiplication](2x2-matrix-multiplication.md) optimized to be done in 7 multiplications rather than 8 as in the native algorithm.

For [3x3 matrix multiplication](3x3-matrix-multiplication.md), the best algorithms as of 2025 are:
- commutative: 21 multiplications
- non-commutative: 23 multiplications
and beating the [Strassen algorithm](strassen-algorithm.md) using 3x3 matrices would require a non-commutative algorithm with 21 multiplications.

Bibliography:
- [https://stackoverflow.com/questions/10827209/ladermans-3x3-matrix-multiplication-with-only-23-multiplications-is-it-worth-i](https://stackoverflow.com/questions/10827209/ladermans-3x3-matrix-multiplication-with-only-23-multiplications-is-it-worth-i)

## ↑ Ancestors (9)

1. [Multiplication of matrices of specific size](multiplication-of-matrices-of-specific-size.md)
2. [Matrix multiplication algorithm](matrix-multiplication-algorithm.md)
3. [Matrix multiplication](matrix-multiplication.md)
4. [Matrix](matrix.md)
5. [Linear algebra](linear-algebra-split.md)
6. [Algebra](algebra-split.md)
7. [Area of mathematics](area-of-mathematics.md)
8. [Mathematics](mathematics-split.md)
9. [Ciro Santilli's Homepage](split.md)
