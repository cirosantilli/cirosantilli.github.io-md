# Elliptic curve point addition

↑ **Parent:** [Elliptic curve group](elliptic-curve-group.md)

[Elliptic curve point addition](elliptic-curve-point-addition.md) is the [group operation](group-operation.md) of an [elliptic curve group](elliptic-curve-group.md), i.e. it is a [function](function-mathematics.md) that takes two points of an [elliptic curve](elliptic-curve.md) as input, and returns a third point of the [elliptic curve](elliptic-curve.md) as its output, while obeying the [group axioms](group-axiom.md).

The operation is defined e.g. at [https://en.wikipedia.org/w/index.php?title=Elliptic_curve_point_multiplication&oldid=1168754060#Point_operations](https://en.wikipedia.org/w/index.php?title=Elliptic_curve_point_multiplication&oldid=1168754060#Point_operations). For example, consider the most common case for two different points different.  If the two points are given in coordinates:

$$
\begin{aligned}
P &+ Q &= R \\
(x_p, y_p) &+ (x_q, y_q) &= (x_r, y_r) \\
\end{aligned}
$$

then the addition is defined in the general case as:

$$
\begin{aligned}
\lambda &= \frac{y_q - y_p}{x_q - x_p} \\
x_r &= \lambda^2 - x_p - x_q \\
y_r &= \lambda(x_p - x_r) - y_p \\
\end{aligned}
$$

with some slightly different definitions for point doubling $P + P$ and the identity point.

This definition relies only on operations that we know how to do on arbitrary [fields](field-mathematics.md):
- [addition](addition.md) $+$
- [multiplication](multiplication.md) $\times$
and it therefore works for [elliptic curves](elliptic-curve.md) defined over any field.

Just remember that:

$$
x/y
$$

means:

$$
x \times y^{-1}
$$

and that $y^{-1}$ always exists because it is the [inverse element](inverse-element.md), which is guaranteed to exist for multiplication due to the [group axioms](group-axiom.md) it obeys.

The group function is usually called [elliptic curve point addition](elliptic-curve-point-addition.md), and repeated addition as done for [DHKE](diffie-hellman-key-exchange.md) is called [elliptic curve point multiplication](elliptic-curve-point-multiplication.md).

<a id="image-visualisation-of-elliptic-curve-point-addition"></a>
![](https://upload.wikimedia.org/wikipedia/commons/a/ae/ECClines-2.svg)

**[Figure 2](#image-visualisation-of-elliptic-curve-point-addition). Visualisation of elliptic curve point addition**. [Source](https://commons.wikimedia.org/wiki/File:ECClines-2.svg).

## ↑ Ancestors (7)

1. [Elliptic curve group](elliptic-curve-group.md)
2. [Elliptic curve](elliptic-curve.md)
3. [Algebraic geometry](algebraic-geometry.md)
4. [Algebra](algebra-split.md)
5. [Area of mathematics](area-of-mathematics.md)
6. [Mathematics](mathematics-split.md)
7. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (3)

- [Elliptic curve group](elliptic-curve-group.md)
- [Elliptic curve over a finite field](elliptic-curve-over-a-finite-field.md)
- [Elliptic curve point addition](elliptic-curve-point-addition.md)
