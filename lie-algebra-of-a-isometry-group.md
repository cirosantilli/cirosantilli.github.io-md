# Lie algebra of a isometry group

↑ **Parent:** [Isometry group](isometry-group.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Lie_algebra_of_a_isometry_group)

We can almost reach the [Lie algebra](lie-algebra.md) of any [isometry group](isometry-group.md) in a single go. For every $X$ in the [Lie algebra](lie-algebra.md) we must have:

$$
\forall v, w \in V, t \in \R (e^{tX}v|e^{tX}w) = (v|w)
$$

because $e^{tX}$ has to be in the isometry group by definition as shown at [Section "Lie algebra of a matrix Lie group"](lie-algebra-of-a-matrix-lie-group.md).

Then:

$$
\evalat{\dv{(e^{tX}v|e^{tX}w)}{t}}{0} = 0
\implies
\evalat{(Xe^{tX}v|e^{tX}w) + (e^{tX}v|Xe^{tX}w)}{0} = 0
\implies
(Xv|w) + (v|Xw) = 0
$$

so we reach:

$$
\forall v, w \in V (Xv|w) = -(v|Xw)
$$

With this relation, we can easily determine the [Lie algebra](lie-algebra.md) of common isometries:
- [Lie algebra of $O(n)$](lie-algebra-of-o-n.md)

Bibliography:
- [An Introduction to Tensors and Group Theory for Physicists by Nadir Jeevanjee (2011)](an-introduction-to-tensors-and-group-theory-for-physicists-by-nadir-jeevanjee-2011.md) page 151

## ↑ Ancestors (8)

1. [Isometry group](isometry-group.md)
2. [Important Lie group](important-lie-group.md)
3. [Lie group](lie-group.md)
4. [Differential geometry](differential-geometry.md)
5. [Geometry](geometry-split.md)
6. [Area of mathematics](area-of-mathematics.md)
7. [Mathematics](mathematics-split.md)
8. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (1)

- [Lie algebra of $O(n)$](lie-algebra-of-o-n.md)
