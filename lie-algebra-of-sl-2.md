<h1 id="lie-algebra-of-sl-2">Lie algebra of <span class="katex"><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:1em;vertical-align:-0.25em;"></span><span class="mord mathnormal" style="margin-right:0.05764em;">S</span><span class="mord mathnormal">L</span><span class="mopen">(</span><span class="mord">2</span><span class="mclose">)</span></span></span></span></h1>

↑ **Parent:** [Lie algebra of $SL(n)$](lie-algebra-of-sl-n.md)

This is a good first concrete example of a Lie algebra. Shown at [Lie Groups, Physics, and Geometry by Robert Gilmore (2008)](lie-groups-physics-and-geometry-by-robert-gilmore-2008.md) Chapter 4.2 "How to linearize a Lie Group" has an example.

We can use use the following parametrization of the [special linear group](special-linear-group.md) on variables $x$, $y$ and $z$:

$$
M =
\begin{bmatrix}
1 + x & y \\
z & (1 + yz)/(1 + x) \\
\end{bmatrix}
$$

Every element with this parametrization has [determinant](determinant.md) 1:

$$
det(M) = (1 + x)(1 + yz)/(1 + x) - yz = 1
$$

Furthermore, any element can be reached, because by independently settting $x$, $y$ and $z$, $M_{00}$, $M_{01}$ and $M_{10}$ can have any value, and once those three are set, $M_{11}$ is fixed by the determinant.

To find the elements of the [Lie algebra](lie-algebra.md), we evaluate the derivative on each parameter at 0:

$$
\begin{aligned}
M_x
&=
\evalat{\dv{M}{x}}{(x,y,z) = (0,0,0)}
&=
\evalat{
\begin{bmatrix}
1 & 0 \\
0 & -(1 + yz)/(1 + x)^2 \\
\end{bmatrix}
}{(x,y,z) = (0,0,0)}
&=
\begin{bmatrix}
1 & 0 \\
0 & -1 \\
\end{bmatrix}
\\

M_y
&=
\evalat{\dv{M}{y}}{(x,y,z) = (0,0,0)}
&=
\evalat{
\begin{bmatrix}
0 & 1 \\
0 & z/(1 + x) \\
\end{bmatrix}
}{(x,y,z) = (0,0,0)}
&=
\begin{bmatrix}
0 & 1 \\
0 & 0 \\
\end{bmatrix}
\\

M_z
&=
\evalat{\dv{M}{z}}{(x,y,z) = (0,0,0)}
&=
\evalat{
\begin{bmatrix}
0 & 0 \\
1 & y/(1 + x) \\
\end{bmatrix}
}{(x,y,z) = (0,0,0)}
&=
\begin{bmatrix}
0 & 0 \\
1 & 0 \\
\end{bmatrix}
\\

\end{aligned}
$$

Remembering that the [Lie bracket of a matrix Lie group](lie-bracket-of-a-matrix-lie-group.md) is really simple, we can then observe the following [Lie bracket](lie-bracket.md) relations between them:

$$
\begin{aligned}
[M_x, M_y] &= M_xM_y - M_yM_x &= \begin{bmatrix}0 & 1 \\  0 & 0 \\\end{bmatrix} &- \begin{bmatrix}0 & -1 \\ 0 & 0 \\\end{bmatrix} &= \begin{bmatrix}0 & 2 \\  0 &  0 \\\end{bmatrix} &=  2M_y\\
[M_x, M_z] &= M_xM_z - M_zM_x &= \begin{bmatrix}0 & 0 \\ -1 & 0 \\\end{bmatrix} &- \begin{bmatrix}0 &  0 \\ 1 & 0 \\\end{bmatrix} &= \begin{bmatrix}0 & 0 \\ -2 &  0 \\\end{bmatrix} &= -2M_z\\
[M_y, M_z] &= M_yM_z - M_zM_y &= \begin{bmatrix}1 & 0 \\  0 & 0 \\\end{bmatrix} &- \begin{bmatrix}0 &  0 \\ 0 & 1 \\\end{bmatrix} &= \begin{bmatrix}1 & 0 \\  0 & -1 \\\end{bmatrix} &=   M_x\\
\end{aligned}
$$

One key thing to note is that the specific matrices $M_x$, $M_y$ and $M_z$ are not really fundamental: we could easily have had different matrices if we had chosen any other parametrization of the group.

TODO confirm: however, no matter which parametrization we choose, the [Lie bracket](lie-bracket.md) relations between the three elements would always be the same, since it is the number of elements, and the definition of the [Lie bracket](lie-bracket.md), that is truly fundamental.

[Lie Groups, Physics, and Geometry by Robert Gilmore (2008)](lie-groups-physics-and-geometry-by-robert-gilmore-2008.md) Chapter 4.2 "How to linearize a Lie Group" then calculates the [exponential map](exponential-map.md) of the vector $xM_x + yM_y + zM_z$ as:

$$
I cosh(\theta) + M_x sinh(\theta)/\theta
$$

with:

$$
\theta^2 = x^2 + bc
$$

TODO now the natural question is: can we cover the entire Lie group with this exponential? [Lie Groups, Physics, and Geometry by Robert Gilmore (2008)](lie-groups-physics-and-geometry-by-robert-gilmore-2008.md) Chapter 7 "EXPonentiation" explains why not.

## ↑ Ancestors (9)

1. [Lie algebra of $SL(n)$](lie-algebra-of-sl-n.md)
2. [Special linear group](special-linear-group.md)
3. [Important Lie group](important-lie-group.md)
4. [Lie group](lie-group.md)
5. [Differential geometry](differential-geometry.md)
6. [Geometry](geometry-split.md)
7. [Area of mathematics](area-of-mathematics.md)
8. [Mathematics](mathematics-split.md)
9. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (1)

- [Lie algebra of a matrix Lie group](lie-algebra-of-a-matrix-lie-group.md)
