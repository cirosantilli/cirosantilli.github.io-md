# Quadratic form

↑ **Parent:** [Symmetric bilinear map](symmetric-bilinear-map.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Quadratic_form)

[Multivariate polynomial](multivariate-polynomial.md) where each term has degree 2, e.g.:

$$
f(x,y) = 2y^2 + 10yx + x^2
$$

is a quadratic form because each term has degree 2:
- $y^2$
- $xy$
- $x^2$
but e.g.:

$$
f(x,y) = 2y^2 + 10yx + x^3
$$

is not because the term $x^3$ has degree 3.

More generally for any number of variables it can be written as:

$$
f(x_1, x_2, \ldots, x_n) = \sum_{i,j} a_i a_j x_i x_j
$$

There is a [1-to-1](bijection.md) relationship between [quadratic forms](quadratic-form.md) and [symmetric bilinear forms](symmetric-bilinear-form.md). In matrix representation, this can be written as:

$$
\vec{x}^T B \vec{x}
$$

where $\vec{x}$ contains each of the variabes of the form, e.g. for 2 variables:

$$
\vec{x} = [x, y]
$$

Strictly speaking, the associated [bilinear form](bilinear-form.md) would not need to be a [symmetric bilinear form](symmetric-bilinear-form.md), at least for the [real numbers](real-number.md) or [complex numbers](complex-number.md) which are [commutative](commutative-property.md). E.g.:

$$
\begin{bmatrix}x y\end{bmatrix}
\begin{bmatrix}0 & 1 \\ 2 & 0 \\ \end{bmatrix}
\begin{bmatrix}x \\ y \\ \end{bmatrix}
=
\begin{bmatrix}x y\end{bmatrix}
\begin{bmatrix}y \\ 2x \\\end{bmatrix}
= xy + 2yx
= 3xy
$$

But that same matrix could also be written in symmetric form as:

$$
\begin{bmatrix}0 & 1.5 \\ 1.5 & 0 \\ \end{bmatrix}
$$

so why not I guess, its simpler/more restricted.

## ↑ Ancestors (8)

1. [Symmetric bilinear map](symmetric-bilinear-map.md)
2. [Multilinear map](multilinear-map.md)
3. [Linear map](linear-map.md)
4. [Linear algebra](linear-algebra-split.md)
5. [Algebra](algebra-split.md)
6. [Area of mathematics](area-of-mathematics.md)
7. [Mathematics](mathematics-split.md)
8. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (2)

- [Quadratic form](quadratic-form.md)
- [Symmetric matrix](symmetric-matrix.md)
