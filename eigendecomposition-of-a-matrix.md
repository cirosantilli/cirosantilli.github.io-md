# Eigendecomposition of a matrix

↑ **Parent:** [Eigenvalues and eigenvectors](eigenvalues-and-eigenvectors.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Eigendecomposition_of_a_matrix)

Every [invertible matrix](invertible-matrix.md) $M$ can be written as:

$$
M = QDQ^{-1}
$$

where:
- $D$ is a [diagonal matrix](diagonal-matrix.md) containing the [eigenvalues](eigenvalue.md) of $M$
- columns of $Q$ are [eigenvectors](eigenvector.md) of $M$
Note therefore that this decomposition is unique up to swapping the order of eigenvectors. We could fix a canonical form by sorting eigenvectors from smallest to largest in the case of a [real number](real-number.md).

Intuitively, Note that this is just the [change of basis](change-of-basis.md) formula, and so:
- $Q^{-1}$ changes basis to align to the eigenvectors
- $D$ multiplies eigenvectors simply by eigenvalues
- $Q$ changes back to the original basis

**Table of contents**

- [Eigendecomposition of a real symmetric matrix](eigendecomposition-of-a-real-symmetric-matrix.md)
- [Sylvester's law of inertia](sylvester-s-law-of-inertia.md)
  - [Congruent matrix](congruent-matrix.md)
    - [Matrix congruence can be seen as the change of basis of a bilinear form](matrix-congruence-can-be-seen-as-the-change-of-basis-of-a-bilinear-form.md)
  - [Matrix similarity](matrix-similarity.md)
  - [Metric signature](metric-signature.md)
    - [Metric signature matrix](metric-signature-matrix.md)

## ↑ Ancestors (7)

1. [Eigenvalues and eigenvectors](eigenvalues-and-eigenvectors.md)
2. [Matrix](matrix.md)
3. [Linear algebra](linear-algebra-split.md)
4. [Algebra](algebra-split.md)
5. [Area of mathematics](area-of-mathematics.md)
6. [Mathematics](mathematics-split.md)
7. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (2)

- [Eigendecomposition of a real symmetric matrix](eigendecomposition-of-a-real-symmetric-matrix.md)
- [Sylvester's law of inertia](sylvester-s-law-of-inertia.md)
