<h1 id="lie-algebra-of-so-3">Lie algebra of <span class="katex"><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:1em;vertical-align:-0.25em;"></span><span class="mord mathnormal" style="margin-right:0.02778em;">SO</span><span class="mopen">(</span><span class="mord">3</span><span class="mclose">)</span></span></span></span></h1>

↑ **Parent:** [Special orthogonal group](special-orthogonal-group.md)

We can reach it by taking the rotations in three directions, e.g. a rotation around the z axis:

$$
R_z(\theta)
=
\begin{bmatrix}
cos(\theta) & -sin(\theta) & 0 \\
sin(\theta) & cos(\theta) & 0 \\
0 & 0 & 1 \\
\end{bmatrix}
$$

then we derive and evaluate at 0:

$$
L_z
=
\evalat{\dv{R_z(\theta)}{\theta}}{0}
=
\evalat{\begin{bmatrix}
-sin(\theta) & -cos(\theta) & 0 \\
cos(\theta) & -sin(\theta) & 0 \\
0 & 0 & 1 \\
\end{bmatrix}}{0}
=
\begin{bmatrix}
0 & -1 & 0 \\
1 & 0 & 0 \\
0 & 0 & 0 \\
\end{bmatrix}
$$

$L_z$ therefore represents the infinitesimal rotation.

Note that the [exponential map](exponential-map.md) reverses this and gives a finite rotation around the Z axis back from the [infinitesimal generator](infinitesimal-generator.md) $L_z$:

$$
e^{\theta L_z} = R_z(\theta)
$$

Repeating the same process for the other directions gives:

$$
L_x = TODO
L_y = TODO
$$

We have now found 3 [linearly independent](linear-independence.md) elements of the Lie algebra, and since $SO(3)$ has dimension 3, we are done.

**Table of contents**

- [Lie bracket of the rotation group](lie-bracket-of-the-rotation-group.md)

## ↑ Ancestors (9)

1. [Special orthogonal group](special-orthogonal-group.md)
2. [Orthogonal group](orthogonal-group.md)
3. [Important Lie group](important-lie-group.md)
4. [Lie group](lie-group.md)
5. [Differential geometry](differential-geometry.md)
6. [Geometry](geometry-split.md)
7. [Area of mathematics](area-of-mathematics.md)
8. [Mathematics](mathematics-split.md)
9. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (3)

- [Lie algebra of a matrix Lie group](lie-algebra-of-a-matrix-lie-group.md)
- [Lie bracket of the rotation group](lie-bracket-of-the-rotation-group.md)
- [One parameter subgroup](one-parameter-subgroup.md)
