# Dot product

↑ **Parent:** [Linear algebra](linear-algebra-split.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Dot_product)

The definition of the "dot product" of a general space varies quite a lot with different contexts.

Most definitions tend to be [bilinear forms](bilinear-form.md).

We use the unqualified generally refers to the dot product of [Real coordinate spaces](real-coordinate-space.md), which is a [positive definite symmetric bilinear form](positive-definite-symmetric-bilinear-form.md). Other important examples include:
- the [complex dot product](complex-dot-product.md), which is not strictly [symmetric](symmetric-bilinear-map.md) nor [linear](linear-function.md), but it is [positive definite](positive-definite-matrix.md)
- [Minkowski inner product](minkowski-inner-product.md), sometimes called" "Minkowski dot product is not [positive definite](positive-definite-matrix.md)
The rest of this section is about the [$\R^n$](real-coordinate-space.md) case.

The [positive definite](positive-definite-matrix.md) part of the definition likely comes in because we are so familiar with [metric spaces](metric-space.md), which requires a positive [norm](norm-mathematics.md) in the [norm induced by an inner product](norm-induced-by-an-inner-product.md).

The default [Euclidean space](euclidean-space.md) definition, we use the [matrix representation of a symmetric bilinear form](matrix-representation-of-a-symmetric-bilinear-form.md) as the identity matrix, e.g. in [$\R^3$](real-coordinate-space-of-dimension-three.md):

$$
M =
\begin{bmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1 \\
\end{bmatrix}
$$

so that:

$$
\vec{x} \cdot \vec{y}
=
\begin{bmatrix}
x_1 & x_2 & x_3 \\
\end{bmatrix}
\begin{bmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1 \\
\end{bmatrix}
\begin{bmatrix}
y_1 \\
y_2 \\
y_3 \\
\end{bmatrix}
=
x_1y_1 + x_2y_2 + x_3y_3
$$

**Table of contents**

- [Orthogonality](orthogonality.md)
  - [Orthonormality](orthonormality.md)
- [Angle](angle.md)

## ↑ Ancestors (5)

1. [Linear algebra](linear-algebra-split.md)
2. [Algebra](algebra-split.md)
3. [Area of mathematics](area-of-mathematics.md)
4. [Mathematics](mathematics-split.md)
5. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (13)

- [Bilinear form](bilinear-form.md)
- [Bilinear map](bilinear-map.md)
- [Bra-ket notation](bra-ket-notation.md)
- [Complex dot product](complex-dot-product.md)
- [Definition of the indefinite orthogonal group](definition-of-the-indefinite-orthogonal-group.md)
- [Dirac Lagrangian](dirac-lagrangian.md)
- [Inner product](inner-product.md)
- [Minkowski space](minkowski-space.md)
- [One-form](one-form.md)
- [Positive definite matrix](positive-definite-matrix.md)
- [Symmetric bilinear map](symmetric-bilinear-map.md)
- [The orthogonal group is the group of all matrices that preserve the dot product](the-orthogonal-group-is-the-group-of-all-matrices-that-preserve-the-dot-product.md)
- [What happens to the definition of the orthogonal group if we choose other types of symmetric bilinear forms](what-happens-to-the-definition-of-the-orthogonal-group-if-we-choose-other-types-of-symmetric-bilinear-forms.md)
