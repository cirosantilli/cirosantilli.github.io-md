# Change of basis matrix

↑ **Parent:** [Change of basis](change-of-basis.md)

The change of basis matrix $C$ is the matrix that allows us to express the new basis in an old basis:

$$
x_{old} = Cx_{new}
$$

Mnemonic is as follows: consider we have an initial basis $(x_{old}, y_{old})$. Now, we define the new basis in terms of the old basis, e.g.:

$$
\begin{aligned}
x_{new} &= 1x_{old} + 2y_{old} \\
y_{new} &= 3x_{old} + 4y_{old} \\
\end{aligned}
$$

which can be written in matrix form as:

$$
\begin{bmatrix}x_{new} \\ y_{new} \\\end{bmatrix} =
\begin{bmatrix}1 && 2 \\ 3 && 4 \\\end{bmatrix}
\begin{bmatrix}x_{old} \\ y_{old} \\\end{bmatrix}
$$

and so if we set:

$$
M = \begin{bmatrix}1 && 2 \\ 3 && 4 \\\end{bmatrix}
$$

we have:

$$
\vec{x_{new}} = M\vec{x_{old}}
$$

The usual question then is: given a vector in the new basis, how do we represent it in the old basis?

The answer is that we simply have to calculate the [matrix inverse](matrix-inverse.md) of $M$:

$$
\vec{x_{old}} =  M^{-1}\vec{x_{new}}
$$

That $M^{-1}$ is the matrix inverse.

## ↑ Ancestors (8)

1. [Change of basis](change-of-basis.md)
2. [Basis (linear algebra)](basis-linear-algebra.md)
3. [Vector space](vector-space.md)
4. [Linear algebra](linear-algebra-split.md)
5. [Algebra](algebra-split.md)
6. [Area of mathematics](area-of-mathematics.md)
7. [Mathematics](mathematics-split.md)
8. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (1)

- [Effect of a change of basis on the matrix of a bilinear form](effect-of-a-change-of-basis-on-the-matrix-of-a-bilinear-form.md)
