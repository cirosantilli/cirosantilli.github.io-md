# Linear algebra

↑ **Parent:** [Algebra](algebra.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Linear_algebra)

**Table of contents**

- [Linear function](#linear-function)
- [Linear map](#linear-map)
  - [Form (mathematics)](#form-mathematics)
  - [Linear form](#linear-form)
    - [Matrix representation of a linear form](#matrix-representation-of-a-linear-form)
    - [Dual space](#dual-space)
      - [Dual vector](#dual-vector)
  - [Linear operator](#linear-operator)
    - [Adjoint operator](#adjoint-operator)
  - [Self-adjoint operator](#self-adjoint-operator)
  - [Multilinear map](#multilinear-map)
    - [Bilinear map](#bilinear-map)
    - [Bilinear form](#bilinear-form)
      - [Matrix representation of a bilinear form](#matrix-representation-of-a-bilinear-form)
        - [Effect of a change of basis on the matrix of a bilinear form](#effect-of-a-change-of-basis-on-the-matrix-of-a-bilinear-form)
    - [Multilinear form](#multilinear-form)
    - [Symmetric bilinear map](#symmetric-bilinear-map)
      - [Symmetric bilinear form](#symmetric-bilinear-form)
        - [Matrix representation of a symmetric bilinear form](#matrix-representation-of-a-symmetric-bilinear-form)
      - [Hermitian form](#hermitian-form)
        - [Matrix representation of a Hermitian form](#matrix-representation-of-a-hermitian-form)
      - [Quadratic form](#quadratic-form)
      - [Positive definite symmetric bilinear form](#positive-definite-symmetric-bilinear-form)
        - [Matrix representation of a positive definite symmetric bilinear form](#matrix-representation-of-a-positive-definite-symmetric-bilinear-form)
      - [Skew-symmetric bilinear map](#skew-symmetric-bilinear-map)
      - [Skew-symmetric bilinear form](#skew-symmetric-bilinear-form)
    - [Symmetric multilinear map](#symmetric-multilinear-map)
      - [Antisymmetric multilinear map](#antisymmetric-multilinear-map)
    - [Alternating multilinear map](#alternating-multilinear-map)
- [Dot product](#dot-product)
  - [Orthogonality](#orthogonality)
    - [Orthonormality](#orthonormality)
  - [Angle](#angle)
- [Cross product](#cross-product)
  - [Jacobi identity](#jacobi-identity)
- [Index picking function](#index-picking-function)
  - [Kronecker delta](#kronecker-delta)
  - [Levi-Civita symbol](#levi-civita-symbol)
    - [Levi-Civita symbol as a tensor](#levi-civita-symbol-as-a-tensor)
- [Projection (mathematics)](#projection-mathematics)
- [Matrix](#matrix)
  - [Matrix operation](#matrix-operation)
    - [Determinant](#determinant)
    - [Matrix inverse](#matrix-inverse)
      - [Invertible matrix](#invertible-matrix)
    - [Transpose](#transpose)
      - [Transpose of a matrix multiplication](#transpose-of-a-matrix-multiplication)
      - [Inverse of the transpose](#inverse-of-the-transpose)
  - [Matrix multiplication](#matrix-multiplication)
    - [System of linear equations](#system-of-linear-equations)
      - [Application of systems of linear equations](#application-of-systems-of-linear-equations)
      - [System of linear equations algorithm](#system-of-linear-equations-algorithm)
        - [LINPACK benchmarks](#linpack-benchmarks)
        - [Conjugate gradient method](#conjugate-gradient-method)
    - [Application of matrix multiplication](#application-of-matrix-multiplication)
    - [Matrix multiplication algorithm](#matrix-multiplication-algorithm)
      - [General matrix matrix multiplication](#general-matrix-matrix-multiplication)
        - [Strassen algorithm](#strassen-algorithm)
      - [Multiplication of matrices of specific size](#multiplication-of-matrices-of-specific-size)
        - [Commutative matrix multiplication algorithm](#commutative-matrix-multiplication-algorithm)
        - [2x2 matrix multiplication](#2x2-matrix-multiplication)
        - [3x3 matrix multiplication](#3x3-matrix-multiplication)
    - [Matrix decomposition](#matrix-decomposition)
  - [Eigenvalues and eigenvectors](#eigenvalues-and-eigenvectors)
    - [Applications of eigenvalues and eigenvectors](#applications-of-eigenvalues-and-eigenvectors)
    - [Characteristic polynomial](#characteristic-polynomial)
    - [Eigenvalue](#eigenvalue)
      - [Spectrum (functional analysis)](#spectrum-functional-analysis)
        - [Continuous spectrum (functional analysis)](#continuous-spectrum-functional-analysis)
    - [Eigendecomposition of a matrix](#eigendecomposition-of-a-matrix)
      - [Eigendecomposition of a real symmetric matrix](#eigendecomposition-of-a-real-symmetric-matrix)
      - [Sylvester's law of inertia](#sylvester-s-law-of-inertia)
        - [Congruent matrix](#congruent-matrix)
          - [Matrix congruence can be seen as the change of basis of a bilinear form](#matrix-congruence-can-be-seen-as-the-change-of-basis-of-a-bilinear-form)
        - [Matrix similarity](#matrix-similarity)
        - [Metric signature](#metric-signature)
          - [Metric signature matrix](#metric-signature-matrix)
    - [Eigenvector](#eigenvector)
    - [Eigenvectors and eigenvalues of the identity matrix](#eigenvectors-and-eigenvalues-of-the-identity-matrix)
    - [Spectral theorem](#spectral-theorem)
      - [Hermitian matrix](#hermitian-matrix)
        - [Hermitian operator](#hermitian-operator)
          - [Riesz representation theorem](#riesz-representation-theorem)
  - [Kronecker product](#kronecker-product)
  - [Named matrix](#named-matrix)
    - [Dense and sparse matrices](#dense-and-sparse-matrices)
      - [Dense matrix](#dense-matrix)
      - [Sparse matrix](#sparse-matrix)
    - [Diagonal matrix](#diagonal-matrix)
      - [Scalar matrix](#scalar-matrix)
        - [Identity matrix](#identity-matrix)
    - [Square matrix](#square-matrix)
      - [Matrix ring](#matrix-ring)
    - [Orthogonal matrix](#orthogonal-matrix)
      - [Unitary matrix](#unitary-matrix)
    - [Triangular matrix](#triangular-matrix)
    - [Symmetric matrix](#symmetric-matrix)
      - [Definite matrix](#definite-matrix)
        - [Positive definite matrix](#positive-definite-matrix)
      - [Skew-symmetric matrix](#skew-symmetric-matrix)
        - [Skew-symmetric form](#skew-symmetric-form)
- [Vector space](#vector-space)
  - [Basis (linear algebra)](#basis-linear-algebra)
    - [Change of basis](#change-of-basis)
      - [Change of basis matrix](#change-of-basis-matrix)
      - [Change of basis between symmetric matrices](#change-of-basis-between-symmetric-matrices)
    - [Linear independence](#linear-independence)
  - [Classification of vector spaces](#classification-of-vector-spaces)
  - [Underlying field of a vector space](#underlying-field-of-a-vector-space)
  - [Tensor product](#tensor-product)
  - [Vector (mathematics)](#vector-mathematics)
    - [Scalar (mathematics)](#scalar-mathematics)
- [Tensor](#tensor)
  - [A linear map is a (1,1) tensor](#a-linear-map-is-a-1-1-tensor)
  - [Tensor space](#tensor-space)
    - [Order of a tensor](#order-of-a-tensor)
  - [Einstein notation](#einstein-notation)
    - [Raised and lowered indices](#raised-and-lowered-indices)
      - [Raised index](#raised-index)
      - [Lowered index](#lowered-index)
      - [Raising and lowering indices](#raising-and-lowering-indices)
    - [Implicit metric signature in Einstein notation](#implicit-metric-signature-in-einstein-notation)
    - [Einstein notation for partial derivatives](#einstein-notation-for-partial-derivatives)
      - [Divergence in Einstein notation](#divergence-in-einstein-notation)
      - [Laplacian in Einstein notation](#laplacian-in-einstein-notation)
        - [d'Alembert operator in Einstein notation](#d-alembert-operator-in-einstein-notation)
          - [Klein-Gordon equation in Einstein notation](#klein-gordon-equation-in-einstein-notation)
    - [Covariance and contravariance of vectors](#covariance-and-contravariance-of-vectors)
      - [Covariant vector](#covariant-vector)
      - [Contravariant vector](#contravariant-vector)
- [Linear algebra bibliography](#linear-algebra-bibliography)
  - [Interactive Linear Algebra by Margalit and Rabinoff](#interactive-linear-algebra-by-margalit-and-rabinoff)

## Linear function

↑ **Parent:** [Linear algebra](linear-algebra.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Linear_function)

The term is not very clear, as it could either mean:
- a [real number](formalization-of-mathematics.md#real-number) function whose graph is a line, i.e.:$$
  f(x) = ax + b
  $$

  or for higher dimensions, a [hyperplane](geometry.md#hyperplane):$$
  f(x_1, x_2, \ldots, x_n) = c_1 x_1 + c_2 x_2 + \ldots + c_n x_n + b
  $$
- a [linear map](#linear-map). Note that the above linear functions are not linear maps unless $b = 0$ (known as the homogeneous case), because e.g.:$$
  f(x + y) = ax + ay + b
  $$

  but$$
  f(x) + f(y) = ax + b + ay + b
  $$

  For this reason, it is better never to refer to linear maps as linear functions.

## Linear map

↑ **Parent:** [Linear algebra](linear-algebra.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Linear_map)

A linear map is a function $f : V_1(F) \to V_2(F)$ where $V_1(F)$ and $V_2(F)$ are two vector spaces over [underlying fields](#underlying-field-of-a-vector-space) $F$ such that:

$$
\forall v_{1}, v_{2} \in V_1, c_{1}, c_{2} \in F \\
f(c_{1} v_{1} + c_{2} v_{2}) = c_{1} f(v_{1}) + c_{2} f(v_{2})
$$

A common case is $F = \R$, $V_1 = \R_m$ and $V_2 = \R_n$.

One thing that makes such functions particularly simple is that they can be fully specified by specifyin how they act on all possible combinations of input basis vectors: they are therefore specified by only a finite number of elements of $F$.

Every linear map in [finite dimension](calculus.md#finite-dimensional) can be represented by a [matrix](#matrix), the points of the [domain](formalization-of-mathematics.md#domain-of-a-function) being represented as [vectors](#vector-mathematics).

As such, when we say "linear map", we can think of a generalization of [matrix multiplication](#matrix-multiplication) that makes sense in [infinite dimensional](calculus.md#infinite-dimensional) spaces like [Hilbert spaces](calculus.md#hilbert-space), since calling such infinite dimensional maps "matrices" is stretching it a bit, since we would need to specify infinitely many rows and columns.

The prototypical building block of [infinite dimensional](calculus.md#infinite-dimensional) linear map is the [derivative](calculus.md#derivative). In that case, the vectors being operated upon are [functions](formalization-of-mathematics.md#function-mathematics), which cannot therefore be specified by a finite number of parameters, e.g. 

For example, the left side of the [time-independent Schrödinger equation](quantum-mechanics.md#time-independent-schrodinger-equation) is a linear map. And the [time-independent Schrödinger equation](quantum-mechanics.md#time-independent-schrodinger-equation) can be seen as a [eigenvalue](#eigenvalue) problem.

### Form (mathematics)

↑ **Parent:** [Linear map](#linear-map)

A form is a [function](formalization-of-mathematics.md#function-mathematics) from a [vector space](#vector-space) to elements of the [underlying field of the vector space](#underlying-field-of-a-vector-space).

Examples:
- [linear form](#linear-form)
- [bilinear form](#bilinear-form)
- [multilinear form](#multilinear-form)

### Linear form

↑ **Parent:** [Linear map](#linear-map)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Linear_form)

A [Linear map](#linear-map) where the [image](formalization-of-mathematics.md#image-mathematics) is the [underlying field of the vector space](#underlying-field-of-a-vector-space), e.g. $\R^n \to \R$.

The set of all [linear forms](#linear-form) over a [vector space](#vector-space) forms another vector space called the [dual space](#dual-space).

#### Matrix representation of a linear form

↑ **Parent:** [Linear form](#linear-form)

For the typical case of a linear form over [$\R^n$](calculus.md#real-coordinate-space), the form can be seen just as a row vector with n elements, the full form being specified by the value of each of the [basis vectors](#basis-linear-algebra).

#### Dual space

↑ **Parent:** [Linear form](#linear-form)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Dual_space)

The dual space of a [vector space](#vector-space) $V$, sometimes denoted $V^*$, is the vector space of all [linear forms](#linear-form) over $V$ with the obvious addition and scalar multiplication operations defined.

Since a linear form is completely determined by how it acts on a [basis](#basis-linear-algebra), and since for each basis element it is specified by a scalar, at least in finite dimension, the dimension of the dual space is the same as the $V$, and so they are isomorphic because [all vector spaces of the same dimension on a given field are isomorphic](#classification-of-vector-spaces), and so the dual is quite a boring concept in the context of finite dimension.

Infinite dimension seems more interesting however, see: [https://en.wikipedia.org/w/index.php?title=Dual_space&oldid=1046421278#Infinite-dimensional_case](https://en.wikipedia.org/w/index.php?title=Dual_space&oldid=1046421278#Infinite-dimensional_case)

One place where duals are different from the non-duals however is when dealing with [tensors](#tensor), because they transform differently than vectors from the base space $V$.

##### Dual vector

↑ **Parent:** [Dual space](#dual-space)

Dual vectors are the members of a [dual space](#dual-space).

In the context of [tensors](#tensor) , we use raised indices to refer to members of the dual basis vs the underlying basis:

$$
\begin{aligned}
e_1 & \in V \\
e_2 & \in V \\
e_3 & \in V \\
e^1 & \in V^* \\
e^2 & \in V^* \\
e^3 & \in V^* \\
\end{aligned}
$$

The dual basis vectors $e^i$ are defined to "pick the corresponding coordinate" out of elements of V. E.g.:

$$
\begin{aligned}
e^1 (4, -3, 6) & =  4 \\
e^2 (4, -3, 6) & = -3 \\
e^3 (4, -3, 6) & =  6 \\
\end{aligned}
$$

By expanding into the basis, we can put this more succinctly with the [Kronecker delta](#kronecker-delta) as:

$$
e^i(e_j) = \delta_{ij}
$$

Note that in [Einstein notation](#einstein-notation), the components of a dual vector have lower indices. This works well with the upper case indices of the dual vectors, allowing us to write a dual vector $f$ as:

$$
f = f_i e^i
$$

In the context of [quantum mechanics](quantum-mechanics.md), the [bra](quantum-mechanics.md#bra-ket-notation) notation is also used for dual vectors.

### Linear operator

↑ **Parent:** [Linear map](#linear-map)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Linear_operator)

We define it as a [linear map](#linear-map) where the [domain](formalization-of-mathematics.md#domain-of-a-function) is the same as the [image](formalization-of-mathematics.md#image-mathematics), i.e. an [endofunction](formalization-of-mathematics.md#endofunction).

Examples:
- a 2x2 matrix can represent a [linear map](#linear-map) from [$\R^2$](calculus.md#real-plane) to [$\R^2$](calculus.md#real-plane), so which is a linear operator
- the [derivative](calculus.md#derivative) is a [linear map](#linear-map) from [$C^{\infty}$](calculus.md#infinitely-differentiable-function) to [$C^{\infty}$](calculus.md#infinitely-differentiable-function), so which is also a linear operator

#### Adjoint operator

↑ **Parent:** [Linear operator](#linear-operator)

Given a [linear operator](#linear-operator) $A$ over a space $S$ that has a [inner product](calculus.md#inner-product) defined, we define the adjoint operator $A^\dagger$ (the $\dagger$ symbol is called "dagger") as the unique operator that satisfies:

$$
\forall v, w \in S, <Av, w> = <v, A^{\dagger} w>
$$

### Self-adjoint operator

↑ **Parent:** [Linear map](#linear-map)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Self-adjoint_operator)

### Multilinear map

↑ **Parent:** [Linear map](#linear-map)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Multilinear_map)

#### Bilinear map

↑ **Parent:** [Multilinear map](#multilinear-map)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Bilinear_map)

[Linear map](#linear-map) of two variables.

More formally, given 3 [vector spaces](#vector-space) X, Y, Z over a single [field](group.md#field-mathematics), a bilinear map is a function from:

$$
f : X \times Y \to Z
$$

that is linear on the first two arguments from X and Y, i.e.:

$$
f(a_1\vec{x_1} + a_2\vec{x_2}, \vec{y}) = a_1f(\vec{x_1}, \vec{y}) + a_2f(\vec{x_2}, \vec{y})
$$

Note that the definition only makes sense if all three vector spaces are over the same field, because linearity can mix up each of them.

The most important example by far is the [dot product](#dot-product) from $\R^n \times \R^n \to \R$, which is more specifically also a [symmetric bilinear form](#symmetric-bilinear-form).

#### Bilinear form

↑ **Parent:** [Multilinear map](#multilinear-map)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Bilinear_form)

Analogous to a [linear form](#linear-form), a bilinear form is a [Bilinear map](#bilinear-map) where the [image](formalization-of-mathematics.md#image-mathematics) is the [underlying field of the vector space](#underlying-field-of-a-vector-space), e.g. $\R^n \times \R^m \to \R$.

Some definitions require both of the input spaces to be the same, e.g. $\R^n \times \R^n \to \R$, but it doesn't make much different in general.

The most important example of a bilinear form is the [dot product](#dot-product). It is only defined if both the input spaces are the same.

##### Matrix representation of a bilinear form

↑ **Parent:** [Bilinear form](#bilinear-form)

As usual, it is useful to think about how a [bilinear form](#bilinear-form) looks like in terms of [vectors](#vector-mathematics) and [matrices](#matrix).

Unlike a [linear form](#linear-form), which [was a vector](#matrix-representation-of-a-linear-form), because it has two inputs, the bilinear form is represented by a matrix $M$ which encodes the value for each possible pair of [basis vectors](#basis-linear-algebra).

In terms of that [matrix](#matrix), the form $B(x,y)$ is then given by:

$$
B(x,y) = x^T M y
$$

###### Effect of a change of basis on the matrix of a bilinear form

↑ **Parent:** [Matrix representation of a bilinear form](#matrix-representation-of-a-bilinear-form)

If $C$ is the [change of basis matrix](#change-of-basis-matrix), then the [matrix representation of a bilinear form](#matrix-representation-of-a-bilinear-form) $M$ that looked like:

$$
B(x,y) = x^T M y
$$

then the matrix in the new basis is:

$$
C^T M C
$$

[Sylvester's law of inertia](#sylvester-s-law-of-inertia) then tells us that the number of positive, negative and 0 eigenvalues of both of those matrices is the same.

Proof: the value of a given bilinear form cannot change due to a [change of basis](#change-of-basis), since the bilinear form is just a [function](formalization-of-mathematics.md#function-mathematics), and does not depend on the choice of basis. The only thing that change is the matrix representation of the form. Therefore, we must have:

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

#### Multilinear form

↑ **Parent:** [Multilinear map](#multilinear-map)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Multilinear_form)

See [form](#form-mathematics).

Analogous to a [linear form](#linear-form), a multilinear form is a [Multilinear map](#multilinear-map) where the [image](formalization-of-mathematics.md#image-mathematics) is the [underlying field of the vector space](#underlying-field-of-a-vector-space), e.g. $\R^{n_1} \times \R^{n_2} \times \R^{n_2} \to \R$.

#### Symmetric bilinear map

↑ **Parent:** [Multilinear map](#multilinear-map)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Symmetric_bilinear_map)

Subcase of [symmetric multilinear map](#symmetric-multilinear-map):

$$
f(x, y) = f(y, x)
$$

Requires the two inputs $x$ and $y$ to be in the same [vector space](#vector-space) of course.

The most important example is the [dot product](#dot-product), which is also a [positive definite symmetric bilinear form](#positive-definite-symmetric-bilinear-form).

##### Symmetric bilinear form

↑ **Parent:** [Symmetric bilinear map](#symmetric-bilinear-map)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Symmetric_bilinear_form)

[symmetric bilinear maps](#symmetric-bilinear-map) that is also a [bilinear form](#bilinear-form).

###### Matrix representation of a symmetric bilinear form

↑ **Parent:** [Symmetric bilinear form](#symmetric-bilinear-form)

Like the [matrix representation of a bilinear form](#matrix-representation-of-a-bilinear-form), it is a [matrix](#matrix), but now the matrix has to be a [symmetric matrix](#symmetric-matrix).

We can then immediately see that the matrix is symmetric, then so is the form. We have:

$$
B(x,y) = x^T M y
$$

But because $B(x,y)$ is a [scalar](#scalar-mathematics), we have:

$$
B(x,y) = B(x,y)^T
$$

and:

$$
B(x,y) = B(x,y)^T = (x^T M y)^T = y^T M^T x = y^T M^T x = y^T M x = B(y,x)
$$

##### Hermitian form

↑ **Parent:** [Symmetric bilinear map](#symmetric-bilinear-map)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Hermitian_form)

The [complex number](formalization-of-mathematics.md#complex-number) analogue of a [symmetric bilinear form](#symmetric-bilinear-form).

The prototypical example of it is the [complex dot product](calculus.md#complex-dot-product).

Note that this form is neither strictly [symmetric](#symmetric-bilinear-map), it satisfies:

$$
<x, y> = \overline{<y, x>}
$$

where the over bar indicates the [complex conjugate](formalization-of-mathematics.md#complex-conjugate), nor is it linear for complex scalar multiplication on the second argument.

Bibliography:
- [https://mathworld.wolfram.com/HermitianForm.html](https://mathworld.wolfram.com/HermitianForm.html)

###### Matrix representation of a Hermitian form

↑ **Parent:** [Hermitian form](#hermitian-form)

;

A [Hermitian matrix](#hermitian-matrix).

##### Quadratic form

↑ **Parent:** [Symmetric bilinear map](#symmetric-bilinear-map)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Quadratic_form)

[Multivariate polynomial](formalization-of-mathematics.md#multivariate-polynomial) where each term has degree 2, e.g.:

$$
f(x,y) = 2y^2 + 10yx + x^2
$$

is a quadratic form because each term has degree 2:
- $y^2$
- $xy$
- $x^2$
but e.g.:

$$
f(x,y) = 2y^2 + 10yx + x^3
$$

is not because the term $x^3$ has degree 3.

More generally for any number of variables it can be written as:

$$
f(x_1, x_2, \ldots, x_n) = \sum_{i,j} a_i a_j x_i x_j
$$

There is a [1-to-1](formalization-of-mathematics.md#bijection) relationship between [quadratic forms](#quadratic-form) and [symmetric bilinear forms](#symmetric-bilinear-form). In matrix representation, this can be written as:

$$
\vec{x}^T B \vec{x}
$$

where $\vec{x}$ contains each of the variabes of the form, e.g. for 2 variables:

$$
\vec{x} = [x, y]
$$

Strictly speaking, the associated [bilinear form](#bilinear-form) would not need to be a [symmetric bilinear form](#symmetric-bilinear-form), at least for the [real numbers](formalization-of-mathematics.md#real-number) or [complex numbers](formalization-of-mathematics.md#complex-number) which are [commutative](group.md#commutative-property). E.g.:

$$
\begin{bmatrix}x y\end{bmatrix}
\begin{bmatrix}0 & 1 \\ 2 & 0 \\ \end{bmatrix}
\begin{bmatrix}x \\ y \\ \end{bmatrix}
=
\begin{bmatrix}x y\end{bmatrix}
\begin{bmatrix}y \\ 2x \\\end{bmatrix}
= xy + 2yx
= 3xy
$$

But that same matrix could also be written in symmetric form as:

$$
\begin{bmatrix}0 & 1.5 \\ 1.5 & 0 \\ \end{bmatrix}
$$

so why not I guess, its simpler/more restricted.

##### Positive definite symmetric bilinear form

↑ **Parent:** [Symmetric bilinear map](#symmetric-bilinear-map)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Positive_definite_symmetric_bilinear_form)

[Symmetric bilinear form](#symmetric-bilinear-form) that is also [positive definite](#positive-definite-matrix), i.e.:

$$
\forall x, B(x, x) > 0
$$

###### Matrix representation of a positive definite symmetric bilinear form

↑ **Parent:** [Positive definite symmetric bilinear form](#positive-definite-symmetric-bilinear-form)

A [positive definite matrix](#positive-definite-matrix) that is also a [symmetric matrix](#symmetric-matrix).

##### Skew-symmetric bilinear map

↑ **Parent:** [Symmetric bilinear map](#symmetric-bilinear-map)

Subcase of [antisymmetric multilinear map](#antisymmetric-multilinear-map):

$$
f(x, y) = -f(y, x)
$$

##### Skew-symmetric bilinear form

↑ **Parent:** [Symmetric bilinear map](#symmetric-bilinear-map)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Skew-symmetric_bilinear_form)

[Skew-symmetric bilinear map](#skew-symmetric-bilinear-map) that is also a [bilinear form](#bilinear-form).

#### Symmetric multilinear map

↑ **Parent:** [Multilinear map](#multilinear-map)

Same value if you swap any input arguments.

##### Antisymmetric multilinear map

↑ **Parent:** [Symmetric multilinear map](#symmetric-multilinear-map)

Change sign if you swap two input values.

#### Alternating multilinear map

↑ **Parent:** [Multilinear map](#multilinear-map)

Implies [antisymmetric multilinear map](#antisymmetric-multilinear-map).

## Dot product

↑ **Parent:** [Linear algebra](linear-algebra.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Dot_product)

The definition of the "dot product" of a general space varies quite a lot with different contexts.

Most definitions tend to be [bilinear forms](#bilinear-form).

We use the unqualified generally refers to the dot product of [Real coordinate spaces](calculus.md#real-coordinate-space), which is a [positive definite symmetric bilinear form](#positive-definite-symmetric-bilinear-form). Other important examples include:
- the [complex dot product](calculus.md#complex-dot-product), which is not strictly [symmetric](#symmetric-bilinear-map) nor [linear](#linear-function), but it is [positive definite](#positive-definite-matrix)
- [Minkowski inner product](relativity.md#minkowski-inner-product), sometimes called" "Minkowski dot product is not [positive definite](#positive-definite-matrix)
The rest of this section is about the [$\R^n$](calculus.md#real-coordinate-space) case.

The [positive definite](#positive-definite-matrix) part of the definition likely comes in because we are so familiar with [metric spaces](calculus.md#metric-space), which requires a positive [norm](calculus.md#norm-mathematics) in the [norm induced by an inner product](calculus.md#norm-induced-by-an-inner-product).

The default [Euclidean space](calculus.md#euclidean-space) definition, we use the [matrix representation of a symmetric bilinear form](#matrix-representation-of-a-symmetric-bilinear-form) as the identity matrix, e.g. in [$\R^3$](calculus.md#real-coordinate-space-of-dimension-three):

$$
M =
\begin{bmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1 \\
\end{bmatrix}
$$

so that:

$$
\vec{x} \cdot \vec{y}
=
\begin{bmatrix}
x_1 & x_2 & x_3 \\
\end{bmatrix}
\begin{bmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1 \\
\end{bmatrix}
\begin{bmatrix}
y_1 \\
y_2 \\
y_3 \\
\end{bmatrix}
=
x_1y_1 + x_2y_2 + x_3y_3
$$

### Orthogonality

↑ **Parent:** [Dot product](#dot-product)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Orthogonality)

#### Orthonormality

↑ **Parent:** [Orthogonality](#orthogonality)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Orthonormality)

### Angle

↑ **Parent:** [Dot product](#dot-product)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Angle)

## Cross product

↑ **Parent:** [Linear algebra](linear-algebra.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Cross_product)

### Jacobi identity

↑ **Parent:** [Cross product](#cross-product)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Jacobi_identity)

## Index picking function

↑ **Parent:** [Linear algebra](linear-algebra.md)

### Kronecker delta

↑ **Parent:** [Index picking function](#index-picking-function)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Kronecker_delta)

### Levi-Civita symbol

↑ **Parent:** [Index picking function](#index-picking-function)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Levi-Civita_symbol)

Denoted by the [Greek letter epsilon](linguistics.md#epsilon-letter) with `\varepsilon` encoding in [LaTeX](computer.md#latex).

Definition:
- [odd permutation](group.md#odd-permutation): -1
- [even permutation](group.md#even-permutation): 1
- not a [permutation](group.md#permutation): 0. This happens iff two more more indices are repeated

#### Levi-Civita symbol as a tensor

↑ **Parent:** [Levi-Civita symbol](#levi-civita-symbol)  
🏷️ **Tags:** [Tensor](#tensor)

[An Introduction to Tensors and Group Theory for Physicists by Nadir Jeevanjee (2011)](geometry.md#an-introduction-to-tensors-and-group-theory-for-physicists-by-nadir-jeevanjee-2011) shows that this is a [tensor](#tensor) that represents the [volume of a parallelepiped](geometry.md#volume-of-the-parallelepiped).

It takes as input three vectors, and outputs one real number, the volume. And it is linear on each vector. This perfectly satisfied the definition of a tensor of [order](#order-of-a-tensor) (3,0).

Given a basis $(e_i, e_j, e_k)$ and a function that return the volume of a parallelepiped given by three vectors $V(v_1, v_2, v_3)$, $\varepsilon_{ikj} = V(e_i, e_j, e_k)$.

## Projection (mathematics)

↑ **Parent:** [Linear algebra](linear-algebra.md)

## Matrix

↑ **Parent:** [Linear algebra](linear-algebra.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Matrix)

### Matrix operation

↑ **Parent:** [Matrix](#matrix)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Matrix_operation)

#### Determinant

↑ **Parent:** [Matrix operation](#matrix-operation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Determinant)

Name origin: likely because it "determines" if a matrix is [invertible](#invertible-matrix) or not, as a matrix is invertible iff determinant is not zero.

#### Matrix inverse

↑ **Parent:** [Matrix operation](#matrix-operation)

When it exists, which is not for all matrices, only [invertible matrix](#invertible-matrix), the inverse is denoted:

$$
M^{-1}
$$

##### Invertible matrix

↑ **Parent:** [Matrix inverse](#matrix-inverse)  
🏷️ **Tags:** [Named matrix](#named-matrix)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Invertible_matrix)

The set of all [invertible matrices](#invertible-matrix) forms a [group](group.md): the [general linear group](geometry.md#general-linear-group) with [matrix multiplication](#matrix-multiplication). Non-invertible matrices don't form a group due to the lack of inverse.

#### Transpose

↑ **Parent:** [Matrix operation](#matrix-operation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Transpose)

##### Transpose of a matrix multiplication

↑ **Parent:** [Transpose](#transpose)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Transpose_of_a_matrix_multiplication)

When it distributes it inverts the order of the [matrix multiplication](#matrix-multiplication):

$$
(MN)^T = N^T M^T
$$

##### Inverse of the transpose

↑ **Parent:** [Transpose](#transpose)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Inverse_of_the_transpose)

The [transpose](#transpose) and [matrix inverse](#matrix-inverse) commute:

$$
(M^T)-1 = (M^{-1})^T
$$

### Matrix multiplication

↑ **Parent:** [Matrix](#matrix)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Matrix_multiplication)

Since a [matrix](#matrix) $M$ can be seen as a [linear map](#linear-map) $f_M(\vec{x})$, the product of two matrices $MN$ can be seen as the composition of two [linear maps](#linear-map):

$$
f_M(f_N(\vec{x}))
$$

One cool thing about linear functions is that we can easily pre-calculate this product only once to obtain a new matrix, and so we don't have to do both multiplications separately each time.

#### System of linear equations

↑ **Parent:** [Matrix multiplication](#matrix-multiplication)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/System_of_linear_equations)

##### Application of systems of linear equations

↑ **Parent:** [System of linear equations](#system-of-linear-equations)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Application_of_systems_of_linear_equations)

No 2x2 examples please. I'm talking about large matrices that would be used in [supercomputers](computer-hardware.md#supercomputer).

##### System of linear equations algorithm

↑ **Parent:** [System of linear equations](#system-of-linear-equations)

###### LINPACK benchmarks

↑ **Parent:** [System of linear equations algorithm](#system-of-linear-equations-algorithm)  
🏷️ **Tags:** [Benchmark](software.md#benchmark)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/LINPACK_benchmarks)

###### Conjugate gradient method

↑ **Parent:** [System of linear equations algorithm](#system-of-linear-equations-algorithm)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Conjugate_gradient_method)

For [positive definite matrices](#positive-definite-matrix) only.

TODO application.

TODO speedup over algorithm for general matrices.

[https://www.studentclustercompetition.us/](https://www.studentclustercompetition.us/) comments:

> The HPCG benchmark uses a preconditioned conjugate gradient (PCG) algorithm to measure the performance of HPC platforms with respect to frequently observed but challenging patterns of computing, communication, and memory access. While HPL provides an optimistic performance target for applications, HPCG can be considered as a lower bound on performance. Many of the top 500 supercomputers also provide their HPCG performance as a reference.

#### Application of matrix multiplication

↑ **Parent:** [Matrix multiplication](#matrix-multiplication)

[https://math.stackexchange.com/questions/41706/practical-uses-of-matrix-multiplication/4647422#4647422](https://math.stackexchange.com/questions/41706/practical-uses-of-matrix-multiplication/4647422#4647422) highlights [deep learning](machine-learning.md#deep-learning) applications.

#### Matrix multiplication algorithm

↑ **Parent:** [Matrix multiplication](#matrix-multiplication)  
🏷️ **Tags:** [Computational problem](computer-science.md#computational-problem)

[https://math.stackexchange.com/questions/30330/fast-algorithm-for-solving-system-of-linear-equations/259372#259372](https://math.stackexchange.com/questions/30330/fast-algorithm-for-solving-system-of-linear-equations/259372#259372)

##### General matrix matrix multiplication

↑ **Parent:** [Matrix multiplication algorithm](#matrix-multiplication-algorithm)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/General_matrix_matrix_multiplication)

The terminology [GEMM](#general-matrix-matrix-multiplication) is present on [BLAS](software.md#basic-linear-algebra-subprograms), and has stuck pretty much.

###### Strassen algorithm

↑ **Parent:** [General matrix matrix multiplication](#general-matrix-matrix-multiplication)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Strassen_algorithm)

##### Multiplication of matrices of specific size

↑ **Parent:** [Matrix multiplication algorithm](#matrix-multiplication-algorithm)

[DeepMind](artificial-intelligence.md#deepmind) likes coming up with new improved algorithms for these more specific cases, e.g. it was announced in 2025 that [AlphaEvolve](software.md#alphaevolve) found a novel 4x4 [complex](formalization-of-mathematics.md#complex-number) valued algorithm that uses 48 multiplications.

Bibliography:
- [https://fmm.univ-lille.fr/](https://fmm.univ-lille.fr/) attempts to keep an up-to-date list for various sizes

###### Commutative matrix multiplication algorithm

↑ **Parent:** [Multiplication of matrices of specific size](#multiplication-of-matrices-of-specific-size)

A "commutative matrix multiplication algorithm" is a matrix multiplication algorithm that requires the ring to be commutative. Such algorithms are inferior because you cannot use them to create more efficient algorithms for [general matrix matrix multiplication](#general-matrix-matrix-multiplication) by decomposing the bigger matrix into smaller ones.

For example, the [Strassen algorithm](#strassen-algorithm) is based on reduction to non-commutative [2x2 matrix multiplication](#2x2-matrix-multiplication) optimized to be done in 7 multiplications rather than 8 as in the native algorithm.

For [3x3 matrix multiplication](#3x3-matrix-multiplication), the best algorithms as of 2025 are:
- commutative: 21 multiplications
- non-commutative: 23 multiplications
and beating the [Strassen algorithm](#strassen-algorithm) using 3x3 matrices would require a non-commutative algorithm with 21 multiplications.

Bibliography:
- [https://stackoverflow.com/questions/10827209/ladermans-3x3-matrix-multiplication-with-only-23-multiplications-is-it-worth-i](https://stackoverflow.com/questions/10827209/ladermans-3x3-matrix-multiplication-with-only-23-multiplications-is-it-worth-i)

###### 2x2 matrix multiplication

↑ **Parent:** [Multiplication of matrices of specific size](#multiplication-of-matrices-of-specific-size)

###### 3x3 matrix multiplication

↑ **Parent:** [Multiplication of matrices of specific size](#multiplication-of-matrices-of-specific-size)

- [https://stackoverflow.com/questions/10827209/ladermans-3x3-matrix-multiplication-with-only-23-multiplications-is-it-worth-i#:~:text=Take%20the%20product%20of%20two,them%20in%20the%20right%20way.](https://stackoverflow.com/questions/10827209/ladermans-3x3-matrix-multiplication-with-only-23-multiplications-is-it-worth-i#:~:text=Take%20the%20product%20of%20two,them%20in%20the%20right%20way.)
- [https://www.reddit.com/r/math/comments/p7xr66/til_that_we_dont_know_what_is_the_fastest_way_to/](https://www.reddit.com/r/math/comments/p7xr66/til_that_we_dont_know_what_is_the_fastest_way_to/)
- [https://arxiv.org/abs/1905.10192](https://arxiv.org/abs/1905.10192)

#### Matrix decomposition

↑ **Parent:** [Matrix multiplication](#matrix-multiplication)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Matrix_decomposition)

### Eigenvalues and eigenvectors

↑ **Parent:** [Matrix](#matrix)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors)

#### Applications of eigenvalues and eigenvectors

↑ **Parent:** [Eigenvalues and eigenvectors](#eigenvalues-and-eigenvectors)

- [https://math.stackexchange.com/questions/23312/what-is-the-importance-of-eigenvalues-eigenvectors/3503875#3503875](https://math.stackexchange.com/questions/23312/what-is-the-importance-of-eigenvalues-eigenvectors/3503875#3503875)
- [https://math.stackexchange.com/questions/1520832/real-life-examples-for-eigenvalues-eigenvectors](https://math.stackexchange.com/questions/1520832/real-life-examples-for-eigenvalues-eigenvectors)
- [https://matheducators.stackexchange.com/questions/520/what-is-a-good-motivation-showcase-for-a-student-for-the-study-of-eigenvalues](https://matheducators.stackexchange.com/questions/520/what-is-a-good-motivation-showcase-for-a-student-for-the-study-of-eigenvalues)

#### Characteristic polynomial

↑ **Parent:** [Eigenvalues and eigenvectors](#eigenvalues-and-eigenvectors)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Characteristic_polynomial)

#### Eigenvalue

↑ **Parent:** [Eigenvalues and eigenvectors](#eigenvalues-and-eigenvectors)

See: [eigenvalues and eigenvectors](#eigenvalues-and-eigenvectors).

##### Spectrum (functional analysis)

↑ **Parent:** [Eigenvalue](#eigenvalue)

Set of [eigenvalues](#eigenvalue) of a [linear operator](#linear-operator).

###### Continuous spectrum (functional analysis)

↑ **Parent:** [Spectrum (functional analysis)](#spectrum-functional-analysis)

Unlike the simple case of a [matrix](#matrix), in [infinite dimensional](calculus.md#infinite-dimensional) vector spaces, the spectrum may be continuous.

The quintessential example of that is the spectrum of the [position operator](quantum-mechanics.md#position-operator) in [quantum mechanics](quantum-mechanics.md), in which any [real number](formalization-of-mathematics.md#real-number) is a possible [eigenvalue](#eigenvalue), since the particle may be found in any position. The associated [eigenvectors](#eigenvector) are the corresponding [Dirac delta functions](calculus.md#dirac-delta-function).

#### Eigendecomposition of a matrix

↑ **Parent:** [Eigenvalues and eigenvectors](#eigenvalues-and-eigenvectors)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Eigendecomposition_of_a_matrix)

Every [invertible matrix](#invertible-matrix) $M$ can be written as:

$$
M = QDQ^{-1}
$$

where:
- $D$ is a [diagonal matrix](#diagonal-matrix) containing the [eigenvalues](#eigenvalue) of $M$
- columns of $Q$ are [eigenvectors](#eigenvector) of $M$
Note therefore that this decomposition is unique up to swapping the order of eigenvectors. We could fix a canonical form by sorting eigenvectors from smallest to largest in the case of a [real number](formalization-of-mathematics.md#real-number).

Intuitively, Note that this is just the [change of basis](#change-of-basis) formula, and so:
- $Q^{-1}$ changes basis to align to the eigenvectors
- $D$ multiplies eigenvectors simply by eigenvalues
- $Q$ changes back to the original basis

##### Eigendecomposition of a real symmetric matrix

↑ **Parent:** [Eigendecomposition of a matrix](#eigendecomposition-of-a-matrix)

The general result from [eigendecomposition of a matrix](#eigendecomposition-of-a-matrix):

$$
M = QDQ^{-1}
$$

becomes:

$$
M = ODO^T
$$

where $O$ is an [orthogonal matrix](#orthogonal-matrix), and therefore has $O^{-1} = O^T$.

<h5 id="sylvester-s-law-of-inertia">Sylvester's law of inertia</h5>

↑ **Parent:** [Eigendecomposition of a matrix](#eigendecomposition-of-a-matrix)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Sylvester's_law_of_inertia)

The main interest of this theorem is in [classifying](mathematics.md#classification-mathematics) the [indefinite orthogonal groups](geometry.md#indefinite-orthogonal-group), which in turn is fundamental because the [Lorentz group](geometry.md#lorentz-group) is an [indefinite orthogonal groups](geometry.md#indefinite-orthogonal-group), see: [all indefinite orthogonal groups of matrices of equal metric signature are isomorphic](geometry.md#all-indefinite-orthogonal-groups-of-matrices-of-equal-metric-signature-are-isomorphic).

It also tells us that a [change of basis](#change-of-basis) does not the alter the [metric signature](#metric-signature) of a [bilinear form](#bilinear-form), see [matrix congruence can be seen as the change of basis of a bilinear form](#matrix-congruence-can-be-seen-as-the-change-of-basis-of-a-bilinear-form).

The theorem states that the number of 0, 1 and -1 in the [metric signature](#metric-signature) is the same for two [symmetric matrices](#symmetric-matrix) that are [congruent matrices](#congruent-matrix).

For example, consider:

$$
A = \begin{bmatrix}2 & \sqrt{2} \\ \sqrt{2} & 3 \\\end{bmatrix}
$$

The [eigenvalues](#eigenvalue) of $A$ are $1$ and $4$, and the associated eigenvectors are:

$$
v_1 = [-\sqrt{2}, 1]^T
v_4 = [\sqrt{2}/2, 1]^T
$$

[symPy](software.md#sympy) code:
```
A = Matrix([[2, sqrt(2)], [sqrt(2), 3]])
A.eigenvects()
```
and from the [eigendecomposition of a real symmetric matrix](#eigendecomposition-of-a-real-symmetric-matrix) we know that:

$$
A = PDP^T =
\begin{bmatrix}-\sqrt{2} & \sqrt{2}/2 \\ 1 & 1\\\end{bmatrix}
\begin{bmatrix}1 & 0 \\ 0 & 4\\\end{bmatrix}
\begin{bmatrix}-\sqrt{2} & 1 \\ \sqrt{2}/2 & 1\\\end{bmatrix}
$$

Now, instead of $P$, we could use $PE$, where $E$ is an arbitrary [diagonal matrix](#diagonal-matrix) of type:

$$
\begin{bmatrix}e_1 & 0 \\ 0 & e_2\\\end{bmatrix}
$$

With this, would reach a new matrix $B$:

$$
B = (PE)D(PE)^T = P(EDE^T)P^T = P(EED)P^T
$$

Therefore, with this congruence, we are able to multiply the eigenvalues of $A$ by any positive number $e_1^2$ and $e_2^2$. Since we are multiplying by two arbitrary positive numbers, we cannot change the signs of the original eigenvalues, and so the [metric signature](#metric-signature) is maintained, but respecting that any value can be reached.

Note that the [matrix congruence](#congruent-matrix) relation looks a bit like the [eigendecomposition of a matrix](#eigendecomposition-of-a-matrix):

$$
D = SMS^T
$$

but note that $D$ does not have to contain [eigenvalues](#eigenvalue), unlike the [eigendecomposition of a matrix](#eigendecomposition-of-a-matrix). This is because here $S$ is not fixed to having [eigenvectors](#eigenvector) in its columns.

But because the matrix is symmetric however, we could always choose $S$ to actually diagonalize as mentioned at [eigendecomposition of a real symmetric matrix](#eigendecomposition-of-a-real-symmetric-matrix). Therefore, the [metric signature](#metric-signature) can be seen directly from [eigenvalues](#eigenvalue).

Also, because $D$ is a [diagonal matrix](#diagonal-matrix), and thus symmetric, it must be that:

$$
S^T = S^{-1}
$$

What this does represent, is a general [change of basis](#change-of-basis) that maintains the matrix a [symmetric matrix](#symmetric-matrix).

Related:
- [https://math.stackexchange.com/questions/1817906/sylvesters-law-of-inertia](https://math.stackexchange.com/questions/1817906/sylvesters-law-of-inertia)
- [https://math.stackexchange.com/questions/1284601/what-is-the-lie-group-that-leaves-this-matrix-invariant](https://math.stackexchange.com/questions/1284601/what-is-the-lie-group-that-leaves-this-matrix-invariant)
- [https://physics.stackexchange.com/questions/24495/metric-signature-explanation](https://physics.stackexchange.com/questions/24495/metric-signature-explanation)

###### Congruent matrix

↑ **Parent:** [Sylvester's law of inertia](#sylvester-s-law-of-inertia)

Two [symmetric matrices](#symmetric-matrix) $A$ and $B$ are defined to be congruent if there exists an $S$ in [$GL(n)$](geometry.md#general-linear-group) such that:

$$
A = S B S^T
$$

###### Matrix congruence can be seen as the change of basis of a bilinear form

↑ **Parent:** [Congruent matrix](#congruent-matrix)

From [effect of a change of basis on the matrix of a bilinear form](#effect-of-a-change-of-basis-on-the-matrix-of-a-bilinear-form), remember that a change of basis $C$ modifies the [matrix representation of a bilinear form](#matrix-representation-of-a-bilinear-form) as:

$$
C^T M C
$$

So, by taking $S = C^T$, we understand that two matrices being congruent means that they can both correspond to the same [bilinear form](#bilinear-form) in different bases.

###### Matrix similarity

↑ **Parent:** [Sylvester's law of inertia](#sylvester-s-law-of-inertia)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Matrix_similarity)

###### Metric signature

↑ **Parent:** [Sylvester's law of inertia](#sylvester-s-law-of-inertia)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Metric_signature)

###### Metric signature matrix

↑ **Parent:** [Metric signature](#metric-signature)

#### Eigenvector

↑ **Parent:** [Eigenvalues and eigenvectors](#eigenvalues-and-eigenvectors)

See: [eigenvalues and eigenvectors](#eigenvalues-and-eigenvectors).

#### Eigenvectors and eigenvalues of the identity matrix

↑ **Parent:** [Eigenvalues and eigenvectors](#eigenvalues-and-eigenvectors)

[https://math.stackexchange.com/questions/1507290/linear-algebra-identity-matrix-and-its-relation-to-eigenvalues-and-eigenvectors/3934023#3934023](https://math.stackexchange.com/questions/1507290/linear-algebra-identity-matrix-and-its-relation-to-eigenvalues-and-eigenvectors/3934023#3934023)

#### Spectral theorem

↑ **Parent:** [Eigenvalues and eigenvectors](#eigenvalues-and-eigenvectors)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Spectral_theorem)

- [https://math.stackexchange.com/questions/1557878/do-infinite-dimensional-hermitian-operators-admit-a-complete-basis-of-eigenvecto](https://math.stackexchange.com/questions/1557878/do-infinite-dimensional-hermitian-operators-admit-a-complete-basis-of-eigenvecto)
- [https://mathoverflow.net/questions/45426/diagonalization-of-infinite-hermitian-matrices](https://mathoverflow.net/questions/45426/diagonalization-of-infinite-hermitian-matrices)

##### Hermitian matrix

↑ **Parent:** [Spectral theorem](#spectral-theorem)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Hermitian_matrix)

###### Hermitian operator

↑ **Parent:** [Hermitian matrix](#hermitian-matrix)

This is the possibly infinite dimensional version of a [Hermitian matrix](#hermitian-matrix), since [linear operators](#linear-operator) are the possibly infinite dimensional version of [matrices](#matrix).

There's a catch though: now we don't have explicit matrix indices here however in general, the generalized definition is shown at: [https://en.wikipedia.org/w/index.php?title=Hermitian_adjoint&oldid=1032475701#Definition_for_bounded_operators_between_Hilbert_spaces](https://en.wikipedia.org/w/index.php?title=Hermitian_adjoint&oldid=1032475701#Definition_for_bounded_operators_between_Hilbert_spaces)

###### Riesz representation theorem

↑ **Parent:** [Hermitian operator](#hermitian-operator)

### Kronecker product

↑ **Parent:** [Matrix](#matrix)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Kronecker_product)

### Named matrix

↑ **Parent:** [Matrix](#matrix)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/List_of_named_matrices)

#### Dense and sparse matrices

↑ **Parent:** [Named matrix](#named-matrix)

A good definition is that the [sparse matrix](#sparse-matrix) has non-zero entries proportional the number of rows. Therefore this is [Big O notation](computer-science.md#big-o-notation) less than something that has $N^2$ non zero entries. Of course, this only makes sense when generalizing to larger and larger matrices, otherwise we could take the constant of proportionality very high for one specific matrix.

Of course, this only makes sense when generalizing to larger and larger matrices, otherwise we could take the constant of proportionality very high for one specific matrix.

##### Dense matrix

↑ **Parent:** [Dense and sparse matrices](#dense-and-sparse-matrices)

##### Sparse matrix

↑ **Parent:** [Dense and sparse matrices](#dense-and-sparse-matrices)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Sparse_matrix)

#### Diagonal matrix

↑ **Parent:** [Named matrix](#named-matrix)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Diagonal_matrix)

Forms a [normal subgroup](group.md#normal-subgroup) of the [general linear group](geometry.md#general-linear-group).

##### Scalar matrix

↑ **Parent:** [Diagonal matrix](#diagonal-matrix)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Diagonal_matrix#Scalar_matrix)

Forms a [normal subgroup](group.md#normal-subgroup) of the [general linear group](geometry.md#general-linear-group).

###### Identity matrix

↑ **Parent:** [Scalar matrix](#scalar-matrix)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Identity_matrix)

#### Square matrix

↑ **Parent:** [Named matrix](#named-matrix)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Square_matrix)

##### Matrix ring

↑ **Parent:** [Square matrix](#square-matrix)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Matrix_ring)

The matrix ring of degree n $M_n$ is the set of all n-by-n square matrices together with the usual [vector space](#vector-space) and [matrix multiplication](#matrix-multiplication) operations.

This set forms a [ring](group.md#ring-mathematics).

Related terminology:
- [https://math.stackexchange.com/questions/412200/what-is-the-notation-for-the-set-of-all-m-times-n-matrices](https://math.stackexchange.com/questions/412200/what-is-the-notation-for-the-set-of-all-m-times-n-matrices)

#### Orthogonal matrix

↑ **Parent:** [Named matrix](#named-matrix)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Orthogonal_matrix)

Members of the [orthogonal group](geometry.md#orthogonal-group).

##### Unitary matrix

↑ **Parent:** [Orthogonal matrix](#orthogonal-matrix)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Unitary_matrix)

[Complex](formalization-of-mathematics.md#complex-number) analogue of [orthogonal matrix](#orthogonal-matrix).

Applications:
- in [quantum computers](quantum-computing.md) programming basically comes down to creating one big unitary matrix as explained at: [quantum computing is just matrix multiplication](quantum-computing.md#programmer-s-model-of-quantum-computers)

#### Triangular matrix

↑ **Parent:** [Named matrix](#named-matrix)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Triangular_matrix)

#### Symmetric matrix

↑ **Parent:** [Named matrix](#named-matrix)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Symmetric_matrix)

A [matrix](#matrix) that equals its [transpose](#transpose):

$$
M = M^T
$$

Can represent a [symmetric bilinear form](#symmetric-bilinear-form) as shown at [matrix representation of a symmetric bilinear form](#matrix-representation-of-a-symmetric-bilinear-form), or a [quadratic form](#quadratic-form).

##### Definite matrix

↑ **Parent:** [Symmetric matrix](#symmetric-matrix)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Definite_matrix)

The definition implies that this is also a [symmetric matrix](#symmetric-matrix).

###### Positive definite matrix

↑ **Parent:** [Definite matrix](#definite-matrix)

The [dot product](#dot-product) is a [positive definite matrix](#positive-definite-matrix), and so we see that those will have an important link to familiar [geometry](geometry.md).

##### Skew-symmetric matrix

↑ **Parent:** [Symmetric matrix](#symmetric-matrix)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Skew-symmetric_matrix)

WTF is a skew? "Antisymmetric" is just such a better name! And it also appears in other definitions such as [antisymmetric multilinear map](#antisymmetric-multilinear-map).

###### Skew-symmetric form

↑ **Parent:** [Skew-symmetric matrix](#skew-symmetric-matrix)

## Vector space

↑ **Parent:** [Linear algebra](linear-algebra.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Vector_space)

### Basis (linear algebra)

↑ **Parent:** [Vector space](#vector-space)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Basis_(linear_algebra))

#### Change of basis

↑ **Parent:** [Basis (linear algebra)](#basis-linear-algebra)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Change_of_basis)



$$
N = BMB^{-1}
$$

where:
- $M$: matrix in the old basis
- $N$: matrix in the new basis
- $B$: change of basis matrix

##### Change of basis matrix

↑ **Parent:** [Change of basis](#change-of-basis)

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

The answer is that we simply have to calculate the [matrix inverse](#matrix-inverse) of $M$:

$$
\vec{x_{old}} =  M^{-1}\vec{x_{new}}
$$

That $M^{-1}$ is the matrix inverse.

##### Change of basis between symmetric matrices

↑ **Parent:** [Change of basis](#change-of-basis)

When we have a [symmetric matrix](#symmetric-matrix), a [change of basis](#change-of-basis) keeps symmetry iff it is done by an [orthogonal matrix](#orthogonal-matrix), in which case:

$$
N = BMB^{-1} = OMO^T
$$

#### Linear independence

↑ **Parent:** [Basis (linear algebra)](#basis-linear-algebra)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Linear_independence)

### Classification of vector spaces

↑ **Parent:** [Vector space](#vector-space)

[https://en.wikipedia.org/wiki/Dimension_(vector_space)#Facts](https://en.wikipedia.org/wiki/Dimension_(vector_space)#Facts)

### Underlying field of a vector space

↑ **Parent:** [Vector space](#vector-space)

Every vector space is defined over a [field](group.md#field-mathematics).

E.g. in $\R^3$, the underlying [field](group.md#field-mathematics) is $\R$, the [real numbers](formalization-of-mathematics.md#real-number). And in $\C^2$ the underlying field is $\C$, the [complex numbers](formalization-of-mathematics.md#complex-number).

Any field can be used, including [finite field](group.md#finite-field). But the underlying thing has to be a field, because the definitions of a vector need all field properties to hold to make sense.

Elements of the underlying field of a vector space are known as [scalar](#scalar-mathematics).

### Tensor product

↑ **Parent:** [Vector space](#vector-space)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Tensor_product)

### Vector (mathematics)

↑ **Parent:** [Vector space](#vector-space)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Vector (mathematics and physics))

#### Scalar (mathematics)

↑ **Parent:** [Vector (mathematics)](#vector-mathematics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Scalar_(mathematics))

A member of the [underlying field of a vector space](#underlying-field-of-a-vector-space). E.g. in $\R^3$, the underlying field is $\R$, and a scalar is a member of $\R$, i.e. a [real number](formalization-of-mathematics.md#real-number).

## Tensor

↑ **Parent:** [Linear algebra](linear-algebra.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Tensor)

A [multilinear form](#multilinear-form) with a [domain](formalization-of-mathematics.md#domain-of-a-function) that looks like:

$$
V^m \times {V*}^n \to \R
$$

where $V*$ is the [dual space](#dual-space).

Because a tensor is a [multilinear form](#multilinear-form), it can be fully specified by how it act on all combinations of basis sets, which can be done in terms of components. We refer to each component as:

$$
T_{i_1 \ldots i_m}^{j_1 \ldots j_n} = T(e_{i_1}, \ldots, e_{i_m}, e^{j_1}, \ldots, e^{j_m})
$$

where we remember that the raised indices refer [dual vector](#dual-vector).

Some examples:
- [Levi-Civita symbol as a tensor](#levi-civita-symbol-as-a-tensor)
- [a linear map is a (1,1) tensor](#a-linear-map-is-a-1-1-tensor)

Explain it properly bibliography:
- [https://www.reddit.com/r/Physics/comments/7lfleo/intuitive_understanding_of_tensors/](https://www.reddit.com/r/Physics/comments/7lfleo/intuitive_understanding_of_tensors/)
- [https://www.reddit.com/r/askscience/comments/sis3j2/what_exactly_are_tensors/](https://www.reddit.com/r/askscience/comments/sis3j2/what_exactly_are_tensors/)
- [https://math.stackexchange.com/questions/10282/an-introduction-to-tensors?noredirect=1&lq=1](https://math.stackexchange.com/questions/10282/an-introduction-to-tensors?noredirect=1&lq=1)
- [https://math.stackexchange.com/questions/2398177/question-about-the-physical-intuition-behind-tensors](https://math.stackexchange.com/questions/2398177/question-about-the-physical-intuition-behind-tensors)
- [https://math.stackexchange.com/questions/657494/what-exactly-is-a-tensor](https://math.stackexchange.com/questions/657494/what-exactly-is-a-tensor)
- [https://physics.stackexchange.com/questions/715634/what-is-a-tensor-intuitively](https://physics.stackexchange.com/questions/715634/what-is-a-tensor-intuitively)

<h3 id="a-linear-map-is-a-1-1-tensor">A linear map is a (1,1) tensor</h3>

↑ **Parent:** [Tensor](#tensor)

A linear map $A$ can be seen as a (1,1) [tensor](#tensor) because:

$$
T(w, v*) = v* A w
$$

is a number, $v*$. is a [dual vector](#dual-vector), and [W](linguistics.md#w) is a [vector](#vector-mathematics). Furthermoe, $T$ is linear in both $v*$ and $w$. All of this makes $T$ fullfill the definition of a (1,1) tensor.

### Tensor space

↑ **Parent:** [Tensor](#tensor)

Bibliography:
- [https://mathworld.wolfram.com/TensorSpace.html](https://mathworld.wolfram.com/TensorSpace.html)

#### Order of a tensor

↑ **Parent:** [Tensor space](#tensor-space)

$T^{(m, n)}$ has order $(m, n)$

### Einstein notation

↑ **Parent:** [Tensor](#tensor)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Einstein_notation)

The [Wikipedia page](https://en.wikipedia.org/w/index.php?title=Einstein_notation&oldid=1021244532) of this article is basically a masterclass why [Wikipedia is useless for learning technical subjects](ourbigbook-com.md#wikipedia). They are not even able to teach such a simple subject properly there!

Bibliography:
- [https://www.maths.cam.ac.uk/postgrad/part-iii/files/misc/index-notation.pdf](https://www.maths.cam.ac.uk/postgrad/part-iii/files/misc/index-notation.pdf) gives a definition that does not consider upper and lower indexes, it only counts how many times the indices appear

  Their definition of the [Laplacian](calculus.md#laplace-operator) is a bit wrong as only one $i$ appears in it, they likely meant to have written $\pdv{}{x_i}\pdv{F}{x_i}$ instead of $\pdv{^2 F}{x_i^2}$, related: 

#### Raised and lowered indices

↑ **Parent:** [Einstein notation](#einstein-notation)

TODO what is the point of them? Why not just sum over every index that appears twice, regardless of where it is, as mentioned at: [https://www.maths.cam.ac.uk/postgrad/part-iii/files/misc/index-notation.pdf](https://www.maths.cam.ac.uk/postgrad/part-iii/files/misc/index-notation.pdf).

Vectors with the index on top such as $x^i$ are the "regular vectors", they are called [covariant vectors](#covariant-vector).

Those in indices on bottom are called [contravariant vectors](#contravariant-vector).

It is possible to change between them by [Raising and lowering indices](#raising-and-lowering-indices).

The values are different only when the [metric signature matrix](#metric-signature-matrix) is different from the [identity matrix](#identity-matrix).

##### Raised index

↑ **Parent:** [Raised and lowered indices](#raised-and-lowered-indices)

##### Lowered index

↑ **Parent:** [Raised and lowered indices](#raised-and-lowered-indices)

##### Raising and lowering indices

↑ **Parent:** [Raised and lowered indices](#raised-and-lowered-indices)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Raising_and_lowering_indices)

#### Implicit metric signature in Einstein notation

↑ **Parent:** [Einstein notation](#einstein-notation)

Then a specific [metric](calculus.md#metric-mathematics) is involved, sometimes we want to automatically add it to products.

E.g., in a context considering the common [Minkowski inner product matrix](relativity.md#minkowski-inner-product-matrix) where the $\eta$ 4x4 matrix and $\mu$ is a vector in [$\R^4$](calculus.md#real-coordinate-space-of-dimension-four)

$$
x^{\mu} x_{\mu} = x^{\mu} \eta_{\mu \nu} x^{\nu} = -x_0^2 + x_1^2 + x_2^2 + x_3^2;
$$

which leads to the change of sign of some terms.

#### Einstein notation for partial derivatives

↑ **Parent:** [Einstein notation](#einstein-notation)

The [Einstein summation convention](#einstein-notation) works will with [partial derivatives](calculus.md#partial-derivative) and it is widely used in [particle physics](particle-physics.md).

In particular, the [divergence](calculus.md#divergence) and the [Laplacian](calculus.md#laplace-operator) can be succinctly expressed in this notation:
- [Section "Divergence in Einstein notation"](#divergence-in-einstein-notation)
- [Section "Laplacian in Einstein notation"](#laplacian-in-einstein-notation)

In order to express partial derivatives, we must use what [Ciro Santilli](ciro-santilli.md) calls the "[partial index partial derivative notation](calculus.md#partial-index-partial-derivative-notation)", which refers to variables with indices such as $x_0$, $x_1$, $x_2$, $\partial_0$, $\partial_1$ and $\partial_2$  instead of the usual letters $x$, $y$ and $z$.

##### Divergence in Einstein notation

↑ **Parent:** [Einstein notation for partial derivatives](#einstein-notation-for-partial-derivatives)

First we write a [vector field](group.md#vector-field) as:

$$
F(x_0, x_1, x_2) = (F^0(x_0, x_1, x_2), F^1(x_0, x_1, x_2), F^2(x_0, x_1, x_2)) : \R^3 \to \R^3
$$

Note how we are denoting each component of $F$ as $F^i$ with a [raised index](#raised-index).

Then, the [divergence](calculus.md#divergence) can be written in [Einstein notation](#einstein-notation) as:

$$
\div{F} = \pdv{F^0(x_0, x_1, x_2)}{x_0} + \pdv{F^1(x_0, x_1, x_2)}{x_1} + \pdv{F^2(x_0, x_1, x_2)}{x_2} = \partial_i F^i(x_0, x_1, x_2) = \pdv{F^i(x_0, x_1, x_2)}{x^i}
$$

It is common to just omit the variables of the function, so we tend to just say:

$$
\div{F} = \partial_i F^i
$$

or equivalently when referring just to the [operator](#linear-operator):

$$
\div{} = \partial_i
$$

##### Laplacian in Einstein notation

↑ **Parent:** [Einstein notation for partial derivatives](#einstein-notation-for-partial-derivatives)  
🏷️ **Tags:** [Laplacian](calculus.md#laplace-operator)

Consider a real valued function of three variables:

$$
F(x_0, x_1, x_2) \colon \R^3 \to \R
$$

Its [Laplacian](calculus.md#laplace-operator) can be written as:

$$
\laplacian{F(x_0, x_1, x_2)} = \\
\partial_0^2 F(x_0, x_1, x_2) + \partial_1^2 F(x_0, x_1, x_2) + \partial_2^2 F(x_0, x_1, x_2) = \\
\partial_0 \partial^0 F(x_0, x_1, x_2) + \partial_1 \partial^1 F(x_0, x_1, x_2) + \partial_2 \partial^2 F(x_0, x_1, x_2) = \\
\partial_i \partial^i F(x_0, x_1, x_2)
$$

It is common to just omit the variables of the function, so we tend to just say:

$$
\laplacian{F} = \partial_i \partial^i F
$$

or equivalently when referring just to the [operator](#linear-operator):

$$
\laplacian{} = \partial_i \partial^i
$$

<h6 id="d-alembert-operator-in-einstein-notation">d'Alembert operator in Einstein notation</h6>

↑ **Parent:** [Laplacian in Einstein notation](#laplacian-in-einstein-notation)

Given the function $\psi$:

$$
\psi : \R^4 \to \C
$$

the operator can be written in [Planck units](system-of-units.md#planck-units) as:

$$
\partial_i \partial^i \psi(x_0, x_1, x_2, x_3) - m^2 \psi(x_0, x_1, x_2, x_3) = 0
$$

often written without function arguments as:

$$
\partial_i \partial^i \psi
$$

Note how this looks just like the [Laplacian in Einstein notation](#laplacian-in-einstein-notation),  since the [d'Alembert operator](calculus.md#d-alembert-operator) is just a generalization of the [laplace operator](calculus.md#laplace-operator) to [Minkowski space](relativity.md#minkowski-space).

###### Klein-Gordon equation in Einstein notation

↑ **Parent:** [d'Alembert operator in Einstein notation](#d-alembert-operator-in-einstein-notation)

The [Klein-Gordon equation](relativistic-quantum-mechanics.md#klein-gordon-equation) can be written in terms of the [d'Alembert operator](calculus.md#d-alembert-operator) as:

$$
\Box \psi + m^2 \psi = 0
$$

so we can expand the [d'Alembert operator in Einstein notation](#d-alembert-operator-in-einstein-notation) to:

$$
\partial_i \partial^i \psi - m^2 \psi = 0
$$

#### Covariance and contravariance of vectors

↑ **Parent:** [Einstein notation](#einstein-notation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Covariance_and_contravariance_of_vectors)

##### Covariant vector

↑ **Parent:** [Covariance and contravariance of vectors](#covariance-and-contravariance-of-vectors)

##### Contravariant vector

↑ **Parent:** [Covariance and contravariance of vectors](#covariance-and-contravariance-of-vectors)

## Linear algebra bibliography

↑ **Parent:** [Linear algebra](linear-algebra.md)

### Interactive Linear Algebra by Margalit and Rabinoff

↑ **Parent:** [Linear algebra bibliography](#linear-algebra-bibliography)  
🏷️ **Tags:** [GNU Free Documentation License](law.md#gnu-free-documentation-license), [Visual math HTML book](mathematics.md#visual-math-html-book)

[https://textbooks.math.gatech.edu/ila/index.html](https://textbooks.math.gatech.edu/ila/index.html)

Source: [https://github.com/QBobWatson/ila](https://github.com/QBobWatson/ila).

Written in [MathBook XML](computer.md#mathbook-xml).

## ↑ Ancestors (4)

1. [Algebra](algebra.md)
2. [Area of mathematics](mathematics.md#area-of-mathematics)
3. [Mathematics](mathematics.md)
4. [Ciro Santilli's Homepage](README.md)

## ← Incoming links (1)

- [SymPy](software.md#sympy)
