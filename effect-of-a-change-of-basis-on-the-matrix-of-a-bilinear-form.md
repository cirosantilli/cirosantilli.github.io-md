# Effect of a change of basis on the matrix of a bilinear form

↑ **Parent:** [Matrix representation of a bilinear form](matrix-representation-of-a-bilinear-form.md)

If $C$ is the [change of basis matrix](change-of-basis-matrix.md), then the [matrix representation of a bilinear form](matrix-representation-of-a-bilinear-form.md) $M$ that looked like:

$$
B(x,y) = x^T M y
$$

then the matrix in the new basis is:

$$
C^T M C
$$

[Sylvester's law of inertia](sylvester-s-law-of-inertia.md) then tells us that the number of positive, negative and 0 eigenvalues of both of those matrices is the same.

Proof: the value of a given bilinear form cannot change due to a [change of basis](change-of-basis.md), since the bilinear form is just a [function](function-mathematics.md), and does not depend on the choice of basis. The only thing that change is the matrix representation of the form. Therefore, we must have:

$$
x^T M y = x_{new}^T M_{new} y_{new}
$$

and in the new basis:

$$
x = C x_{new} \\
y = C y_{new} \\
x_{new}^T M_{new} y_{new} = x^T M y =  (Cx_{new})^T M (Cy_{new}) = x_{new}^T (C^T M C) y_{new} \\
$$

and so since:

$$
\forall x_{new}, y_{new} x_{new}^T M_{new} y_{new} = x_{new}^T (C^T M C) y_{new} \implies M_{new} = C^T M C \\
$$

Related:
- [https://proofwiki.org/wiki/Matrix_of_Bilinear_Form_Under_Change_of_Basis](https://proofwiki.org/wiki/Matrix_of_Bilinear_Form_Under_Change_of_Basis)

## ↑ Ancestors (9)

1. [Matrix representation of a bilinear form](matrix-representation-of-a-bilinear-form.md)
2. [Bilinear form](bilinear-form.md)
3. [Multilinear map](multilinear-map.md)
4. [Linear map](linear-map.md)
5. [Linear algebra](linear-algebra-split.md)
6. [Algebra](algebra-split.md)
7. [Area of mathematics](area-of-mathematics.md)
8. [Mathematics](mathematics-split.md)
9. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (1)

- [Matrix congruence can be seen as the change of basis of a bilinear form](matrix-congruence-can-be-seen-as-the-change-of-basis-of-a-bilinear-form.md)
