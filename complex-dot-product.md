# Complex dot product

↑ **Parent:** [Complex coordinate space](complex-coordinate-space.md)

This section is about the definition of the [dot product](dot-product.md) over [$\C^n$](complex-coordinate-space.md), which extends the definition of the [dot product](dot-product.md) over [$\R^n$](real-coordinate-space.md).

Some motivation is discussed at: [https://math.stackexchange.com/questions/2459814/what-is-the-dot-product-of-complex-vectors/4300169#4300169](https://math.stackexchange.com/questions/2459814/what-is-the-dot-product-of-complex-vectors/4300169#4300169)

The complex dot product is defined as:

$$
\sum a_i \overline{b_i}
$$

E.g. in $\C^1$:

$$
(a + bi) \cdot (c + di) = (a + bi) (\overline{c + di}) = (a + bi) (c - di) = (ac + bd) + (bc - ad)i
$$

We can see therefore that this is a [form](form-mathematics.md), and a positive definite because:

$$
(a + bi) \cdot (a + bi) = (aa + bb) + (ba - ab)i = a^2 + b^2
$$

Just like the usual [dot product](dot-product.md), this will be a [positive definite symmetric bilinear form](positive-definite-symmetric-bilinear-form.md) by definition.

**Table of contents**

- [Norm induced by the complex dot product](norm-induced-by-the-complex-dot-product.md)

## ↑ Ancestors (7)

1. [Complex coordinate space](complex-coordinate-space.md)
2. [Real coordinate space](real-coordinate-space.md)
3. [Topology](topology.md)
4. [Calculus](calculus-split.md)
5. [Area of mathematics](area-of-mathematics.md)
6. [Mathematics](mathematics-split.md)
7. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (2)

- [Dot product](dot-product.md)
- [Hermitian form](hermitian-form.md)
