<h1 id="sylvester-s-law-of-inertia">Sylvester's law of inertia</h1>

↑ **Parent:** [Eigendecomposition of a matrix](eigendecomposition-of-a-matrix.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Sylvester's_law_of_inertia)

The main interest of this theorem is in [classifying](classification-mathematics.md) the [indefinite orthogonal groups](indefinite-orthogonal-group.md), which in turn is fundamental because the [Lorentz group](lorentz-group.md) is an [indefinite orthogonal groups](indefinite-orthogonal-group.md), see: [all indefinite orthogonal groups of matrices of equal metric signature are isomorphic](all-indefinite-orthogonal-groups-of-matrices-of-equal-metric-signature-are-isomorphic.md).

It also tells us that a [change of basis](change-of-basis.md) does not the alter the [metric signature](metric-signature.md) of a [bilinear form](bilinear-form.md), see [matrix congruence can be seen as the change of basis of a bilinear form](matrix-congruence-can-be-seen-as-the-change-of-basis-of-a-bilinear-form.md).

The theorem states that the number of 0, 1 and -1 in the [metric signature](metric-signature.md) is the same for two [symmetric matrices](symmetric-matrix.md) that are [congruent matrices](congruent-matrix.md).

For example, consider:

$$
A = \begin{bmatrix}2 & \sqrt{2} \\ \sqrt{2} & 3 \\\end{bmatrix}
$$

The [eigenvalues](eigenvalue.md) of $A$ are $1$ and $4$, and the associated eigenvectors are:

$$
v_1 = [-\sqrt{2}, 1]^T
v_4 = [\sqrt{2}/2, 1]^T
$$

[symPy](sympy.md) code:
```
A = Matrix([[2, sqrt(2)], [sqrt(2), 3]])
A.eigenvects()
```
and from the [eigendecomposition of a real symmetric matrix](eigendecomposition-of-a-real-symmetric-matrix.md) we know that:

$$
A = PDP^T =
\begin{bmatrix}-\sqrt{2} & \sqrt{2}/2 \\ 1 & 1\\\end{bmatrix}
\begin{bmatrix}1 & 0 \\ 0 & 4\\\end{bmatrix}
\begin{bmatrix}-\sqrt{2} & 1 \\ \sqrt{2}/2 & 1\\\end{bmatrix}
$$

Now, instead of $P$, we could use $PE$, where $E$ is an arbitrary [diagonal matrix](diagonal-matrix.md) of type:

$$
\begin{bmatrix}e_1 & 0 \\ 0 & e_2\\\end{bmatrix}
$$

With this, would reach a new matrix $B$:

$$
B = (PE)D(PE)^T = P(EDE^T)P^T = P(EED)P^T
$$

Therefore, with this congruence, we are able to multiply the eigenvalues of $A$ by any positive number $e_1^2$ and $e_2^2$. Since we are multiplying by two arbitrary positive numbers, we cannot change the signs of the original eigenvalues, and so the [metric signature](metric-signature.md) is maintained, but respecting that any value can be reached.

Note that the [matrix congruence](congruent-matrix.md) relation looks a bit like the [eigendecomposition of a matrix](eigendecomposition-of-a-matrix.md):

$$
D = SMS^T
$$

but note that $D$ does not have to contain [eigenvalues](eigenvalue.md), unlike the [eigendecomposition of a matrix](eigendecomposition-of-a-matrix.md). This is because here $S$ is not fixed to having [eigenvectors](eigenvector.md) in its columns.

But because the matrix is symmetric however, we could always choose $S$ to actually diagonalize as mentioned at [eigendecomposition of a real symmetric matrix](eigendecomposition-of-a-real-symmetric-matrix.md). Therefore, the [metric signature](metric-signature.md) can be seen directly from [eigenvalues](eigenvalue.md).

Also, because $D$ is a [diagonal matrix](diagonal-matrix.md), and thus symmetric, it must be that:

$$
S^T = S^{-1}
$$

What this does represent, is a general [change of basis](change-of-basis.md) that maintains the matrix a [symmetric matrix](symmetric-matrix.md).

Related:
- [https://math.stackexchange.com/questions/1817906/sylvesters-law-of-inertia](https://math.stackexchange.com/questions/1817906/sylvesters-law-of-inertia)
- [https://math.stackexchange.com/questions/1284601/what-is-the-lie-group-that-leaves-this-matrix-invariant](https://math.stackexchange.com/questions/1284601/what-is-the-lie-group-that-leaves-this-matrix-invariant)
- [https://physics.stackexchange.com/questions/24495/metric-signature-explanation](https://physics.stackexchange.com/questions/24495/metric-signature-explanation)

**Table of contents**

- [Congruent matrix](congruent-matrix.md)
  - [Matrix congruence can be seen as the change of basis of a bilinear form](matrix-congruence-can-be-seen-as-the-change-of-basis-of-a-bilinear-form.md)
- [Matrix similarity](matrix-similarity.md)
- [Metric signature](metric-signature.md)
  - [Metric signature matrix](metric-signature-matrix.md)

## ↑ Ancestors (8)

1. [Eigendecomposition of a matrix](eigendecomposition-of-a-matrix.md)
2. [Eigenvalues and eigenvectors](eigenvalues-and-eigenvectors.md)
3. [Matrix](matrix.md)
4. [Linear algebra](linear-algebra-split.md)
5. [Algebra](algebra-split.md)
6. [Area of mathematics](area-of-mathematics.md)
7. [Mathematics](mathematics-split.md)
8. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (3)

- [Definition of the indefinite orthogonal group](definition-of-the-indefinite-orthogonal-group.md)
- [Effect of a change of basis on the matrix of a bilinear form](effect-of-a-change-of-basis-on-the-matrix-of-a-bilinear-form.md)
- [What happens to the definition of the orthogonal group if we choose other types of symmetric bilinear forms](what-happens-to-the-definition-of-the-orthogonal-group-if-we-choose-other-types-of-symmetric-bilinear-forms.md)
