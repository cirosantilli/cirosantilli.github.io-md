# Connected components of the orthogonal group

↑ **Parent:** [Topology of the orthogonal group](topology-of-the-orthogonal-group.md)

The [orthogonal group](orthogonal-group.md) has 2 [connected components](connected-component.md):
- one with determinant +1, which is itself a [subgroup](subgroup.md) known as the [special orthogonal group](special-orthogonal-group.md). These are pure [rotations](special-orthogonal-group.md) without a reflection.
- the other with determinant -1. This is not a [subgroup](subgroup.md) as it does not contain the origin. It represents [rotations](special-orthogonal-group.md) with a reflection.

It is instructive to visualize how the $\pm1$ looks like in [$SO(3)$](3d-rotation-group.md):
- you take the first basis vector and move it to any other. You have therefore two angular parameters.
- you take the second one, and move it to be orthogonal to the first new vector. (you can choose a circle around the first new vector, and so you have another angular parameter.
- at last, for the last one, there are only two choices that are orthogonal to both previous ones, one in each direction. It is this directio, relative to the others, that determines the "has a reflection or not" thing

As a result it is [isomorphic](group-isomorphism.md) to the [direct product](direct-product-of-groups.md) of the special orthogonal group by the [cyclic group](cyclic-group.md) of [order](order-algebra.md) 2:

$$
O(n) \cong SO(n) \times C_2
$$

A low dimensional example:

$$
O(1) \cong SO(2) \times C_2
$$

because you can only do two things: to flip or not to flip the line around zero.

Note that having the determinant plus or minus 1 is not a definition: there are non-orthogonal groups with determinant plus or minus 1. This is just a property. E.g.:

$$
M = \begin{bmatrix} 2 & 3 \\ 1 & 2 \\ \end{bmatrix}
$$

has determinant 1, but:

$$
M^TM = \begin{bmatrix} 5 & 8 \\ 8 & 11 \\ \end{bmatrix}
$$

so $M$ is not orthogonal.

## ↑ Ancestors (9)

1. [Topology of the orthogonal group](topology-of-the-orthogonal-group.md)
2. [Orthogonal group](orthogonal-group.md)
3. [Important Lie group](important-lie-group.md)
4. [Lie group](lie-group.md)
5. [Differential geometry](differential-geometry.md)
6. [Geometry](geometry-split.md)
7. [Area of mathematics](area-of-mathematics.md)
8. [Mathematics](mathematics-split.md)
9. [Ciro Santilli's Homepage](split.md)
