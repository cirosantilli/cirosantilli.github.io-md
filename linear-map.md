# Linear map

↑ **Parent:** [Linear algebra](linear-algebra-split.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Linear_map)

A linear map is a function $f : V_1(F) \to V_2(F)$ where $V_1(F)$ and $V_2(F)$ are two vector spaces over [underlying fields](underlying-field-of-a-vector-space.md) $F$ such that:

$$
\forall v_{1}, v_{2} \in V_1, c_{1}, c_{2} \in F \\
f(c_{1} v_{1} + c_{2} v_{2}) = c_{1} f(v_{1}) + c_{2} f(v_{2})
$$

A common case is $F = \R$, $V_1 = \R_m$ and $V_2 = \R_n$.

One thing that makes such functions particularly simple is that they can be fully specified by specifyin how they act on all possible combinations of input basis vectors: they are therefore specified by only a finite number of elements of $F$.

Every linear map in [finite dimension](finite-dimensional.md) can be represented by a [matrix](matrix.md), the points of the [domain](domain-of-a-function.md) being represented as [vectors](vector-mathematics.md).

As such, when we say "linear map", we can think of a generalization of [matrix multiplication](matrix-multiplication.md) that makes sense in [infinite dimensional](infinite-dimensional.md) spaces like [Hilbert spaces](hilbert-space.md), since calling such infinite dimensional maps "matrices" is stretching it a bit, since we would need to specify infinitely many rows and columns.

The prototypical building block of [infinite dimensional](infinite-dimensional.md) linear map is the [derivative](derivative.md). In that case, the vectors being operated upon are [functions](function-mathematics.md), which cannot therefore be specified by a finite number of parameters, e.g. 

For example, the left side of the [time-independent Schrödinger equation](time-independent-schrodinger-equation.md) is a linear map. And the [time-independent Schrödinger equation](time-independent-schrodinger-equation.md) can be seen as a [eigenvalue](eigenvalue.md) problem.

**Table of contents**

- [Form (mathematics)](form-mathematics.md)
- [Linear form](linear-form.md)
  - [Matrix representation of a linear form](matrix-representation-of-a-linear-form.md)
  - [Dual space](dual-space.md)
    - [Dual vector](dual-vector.md)
- [Linear operator](linear-operator.md)
  - [Adjoint operator](adjoint-operator.md)
- [Self-adjoint operator](self-adjoint-operator.md)
- [Multilinear map](multilinear-map.md)
  - [Bilinear map](bilinear-map.md)
  - [Bilinear form](bilinear-form.md)
    - [Matrix representation of a bilinear form](matrix-representation-of-a-bilinear-form.md)
      - [Effect of a change of basis on the matrix of a bilinear form](effect-of-a-change-of-basis-on-the-matrix-of-a-bilinear-form.md)
  - [Multilinear form](multilinear-form.md)
  - [Symmetric bilinear map](symmetric-bilinear-map.md)
    - [Symmetric bilinear form](symmetric-bilinear-form.md)
      - [Matrix representation of a symmetric bilinear form](matrix-representation-of-a-symmetric-bilinear-form.md)
    - [Hermitian form](hermitian-form.md)
      - [Matrix representation of a Hermitian form](matrix-representation-of-a-hermitian-form.md)
    - [Quadratic form](quadratic-form.md)
    - [Positive definite symmetric bilinear form](positive-definite-symmetric-bilinear-form.md)
      - [Matrix representation of a positive definite symmetric bilinear form](matrix-representation-of-a-positive-definite-symmetric-bilinear-form.md)
    - [Skew-symmetric bilinear map](skew-symmetric-bilinear-map.md)
    - [Skew-symmetric bilinear form](skew-symmetric-bilinear-form.md)
  - [Symmetric multilinear map](symmetric-multilinear-map.md)
    - [Antisymmetric multilinear map](antisymmetric-multilinear-map.md)
  - [Alternating multilinear map](alternating-multilinear-map.md)

## ↑ Ancestors (5)

1. [Linear algebra](linear-algebra-split.md)
2. [Algebra](algebra-split.md)
3. [Area of mathematics](area-of-mathematics.md)
4. [Mathematics](mathematics-split.md)
5. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (7)

- [Bilinear map](bilinear-map.md)
- [General linear group](general-linear-group.md)
- [Linear form](linear-form.md)
- [Linear function](linear-function.md)
- [Linear operator](linear-operator.md)
- [Matrix multiplication](matrix-multiplication.md)
- [Representation theory](representation-theory.md)
