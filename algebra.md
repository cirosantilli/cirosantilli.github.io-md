# Algebra

↑ **Parent:** [Area of mathematics](mathematics.md#area-of-mathematics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Algebra)

Not to be confused with [algebra over a field](group.md#algebra-over-a-field), which is a particular [algebraic structure](#algebraic-structure) studied within algebra.

**Table of contents**

- [Abstract algebra](#abstract-algebra)
- [Algebraic structure](#algebraic-structure)
  - [Commutator](#commutator)
  - [Identity element](#identity-element)
    - [Inverse element](#inverse-element)
      - [Invertible](#invertible)
  - [Order (algebra)](#order-algebra)
    - [Degree (algebra)](#degree-algebra)
    - [Finite algebraic structure](#finite-algebraic-structure)
- [Linear algebra](linear-algebra.md)
  - [Linear function](linear-algebra.md#linear-function)
  - [Linear map](linear-algebra.md#linear-map)
    - [Form (mathematics)](linear-algebra.md#form-mathematics)
    - [Linear form](linear-algebra.md#linear-form)
      - [Matrix representation of a linear form](linear-algebra.md#matrix-representation-of-a-linear-form)
      - [Dual space](linear-algebra.md#dual-space)
        - [Dual vector](linear-algebra.md#dual-vector)
    - [Linear operator](linear-algebra.md#linear-operator)
      - [Adjoint operator](linear-algebra.md#adjoint-operator)
    - [Self-adjoint operator](linear-algebra.md#self-adjoint-operator)
    - [Multilinear map](linear-algebra.md#multilinear-map)
      - [Bilinear map](linear-algebra.md#bilinear-map)
      - [Bilinear form](linear-algebra.md#bilinear-form)
        - [Matrix representation of a bilinear form](linear-algebra.md#matrix-representation-of-a-bilinear-form)
          - [Effect of a change of basis on the matrix of a bilinear form](linear-algebra.md#effect-of-a-change-of-basis-on-the-matrix-of-a-bilinear-form)
      - [Multilinear form](linear-algebra.md#multilinear-form)
      - [Symmetric bilinear map](linear-algebra.md#symmetric-bilinear-map)
        - [Symmetric bilinear form](linear-algebra.md#symmetric-bilinear-form)
          - [Matrix representation of a symmetric bilinear form](linear-algebra.md#matrix-representation-of-a-symmetric-bilinear-form)
        - [Hermitian form](linear-algebra.md#hermitian-form)
          - [Matrix representation of a Hermitian form](linear-algebra.md#matrix-representation-of-a-hermitian-form)
        - [Quadratic form](linear-algebra.md#quadratic-form)
        - [Positive definite symmetric bilinear form](linear-algebra.md#positive-definite-symmetric-bilinear-form)
          - [Matrix representation of a positive definite symmetric bilinear form](linear-algebra.md#matrix-representation-of-a-positive-definite-symmetric-bilinear-form)
        - [Skew-symmetric bilinear map](linear-algebra.md#skew-symmetric-bilinear-map)
        - [Skew-symmetric bilinear form](linear-algebra.md#skew-symmetric-bilinear-form)
      - [Symmetric multilinear map](linear-algebra.md#symmetric-multilinear-map)
        - [Antisymmetric multilinear map](linear-algebra.md#antisymmetric-multilinear-map)
      - [Alternating multilinear map](linear-algebra.md#alternating-multilinear-map)
  - [Dot product](linear-algebra.md#dot-product)
    - [Orthogonality](linear-algebra.md#orthogonality)
      - [Orthonormality](linear-algebra.md#orthonormality)
    - [Angle](linear-algebra.md#angle)
  - [Cross product](linear-algebra.md#cross-product)
    - [Jacobi identity](linear-algebra.md#jacobi-identity)
  - [Index picking function](linear-algebra.md#index-picking-function)
    - [Kronecker delta](linear-algebra.md#kronecker-delta)
    - [Levi-Civita symbol](linear-algebra.md#levi-civita-symbol)
      - [Levi-Civita symbol as a tensor](linear-algebra.md#levi-civita-symbol-as-a-tensor)
  - [Projection (mathematics)](linear-algebra.md#projection-mathematics)
  - [Matrix](linear-algebra.md#matrix)
    - [Matrix operation](linear-algebra.md#matrix-operation)
      - [Determinant](linear-algebra.md#determinant)
      - [Matrix inverse](linear-algebra.md#matrix-inverse)
        - [Invertible matrix](linear-algebra.md#invertible-matrix)
      - [Transpose](linear-algebra.md#transpose)
        - [Transpose of a matrix multiplication](linear-algebra.md#transpose-of-a-matrix-multiplication)
        - [Inverse of the transpose](linear-algebra.md#inverse-of-the-transpose)
    - [Matrix multiplication](linear-algebra.md#matrix-multiplication)
      - [System of linear equations](linear-algebra.md#system-of-linear-equations)
        - [Application of systems of linear equations](linear-algebra.md#application-of-systems-of-linear-equations)
        - [System of linear equations algorithm](linear-algebra.md#system-of-linear-equations-algorithm)
          - [LINPACK benchmarks](linear-algebra.md#linpack-benchmarks)
          - [Conjugate gradient method](linear-algebra.md#conjugate-gradient-method)
      - [Application of matrix multiplication](linear-algebra.md#application-of-matrix-multiplication)
      - [Matrix multiplication algorithm](linear-algebra.md#matrix-multiplication-algorithm)
        - [General matrix matrix multiplication](linear-algebra.md#general-matrix-matrix-multiplication)
          - [Strassen algorithm](linear-algebra.md#strassen-algorithm)
        - [Multiplication of matrices of specific size](linear-algebra.md#multiplication-of-matrices-of-specific-size)
          - [Commutative matrix multiplication algorithm](linear-algebra.md#commutative-matrix-multiplication-algorithm)
          - [2x2 matrix multiplication](linear-algebra.md#2x2-matrix-multiplication)
          - [3x3 matrix multiplication](linear-algebra.md#3x3-matrix-multiplication)
      - [Matrix decomposition](linear-algebra.md#matrix-decomposition)
    - [Eigenvalues and eigenvectors](linear-algebra.md#eigenvalues-and-eigenvectors)
      - [Applications of eigenvalues and eigenvectors](linear-algebra.md#applications-of-eigenvalues-and-eigenvectors)
      - [Characteristic polynomial](linear-algebra.md#characteristic-polynomial)
      - [Eigenvalue](linear-algebra.md#eigenvalue)
        - [Spectrum (functional analysis)](linear-algebra.md#spectrum-functional-analysis)
          - [Continuous spectrum (functional analysis)](linear-algebra.md#continuous-spectrum-functional-analysis)
      - [Eigendecomposition of a matrix](linear-algebra.md#eigendecomposition-of-a-matrix)
        - [Eigendecomposition of a real symmetric matrix](linear-algebra.md#eigendecomposition-of-a-real-symmetric-matrix)
        - [Sylvester's law of inertia](linear-algebra.md#sylvester-s-law-of-inertia)
          - [Congruent matrix](linear-algebra.md#congruent-matrix)
            - [Matrix congruence can be seen as the change of basis of a bilinear form](linear-algebra.md#matrix-congruence-can-be-seen-as-the-change-of-basis-of-a-bilinear-form)
          - [Matrix similarity](linear-algebra.md#matrix-similarity)
          - [Metric signature](linear-algebra.md#metric-signature)
            - [Metric signature matrix](linear-algebra.md#metric-signature-matrix)
      - [Eigenvector](linear-algebra.md#eigenvector)
      - [Eigenvectors and eigenvalues of the identity matrix](linear-algebra.md#eigenvectors-and-eigenvalues-of-the-identity-matrix)
      - [Spectral theorem](linear-algebra.md#spectral-theorem)
        - [Hermitian matrix](linear-algebra.md#hermitian-matrix)
          - [Hermitian operator](linear-algebra.md#hermitian-operator)
            - [Riesz representation theorem](linear-algebra.md#riesz-representation-theorem)
    - [Kronecker product](linear-algebra.md#kronecker-product)
    - [Named matrix](linear-algebra.md#named-matrix)
      - [Dense and sparse matrices](linear-algebra.md#dense-and-sparse-matrices)
        - [Dense matrix](linear-algebra.md#dense-matrix)
        - [Sparse matrix](linear-algebra.md#sparse-matrix)
      - [Diagonal matrix](linear-algebra.md#diagonal-matrix)
        - [Scalar matrix](linear-algebra.md#scalar-matrix)
          - [Identity matrix](linear-algebra.md#identity-matrix)
      - [Square matrix](linear-algebra.md#square-matrix)
        - [Matrix ring](linear-algebra.md#matrix-ring)
      - [Orthogonal matrix](linear-algebra.md#orthogonal-matrix)
        - [Unitary matrix](linear-algebra.md#unitary-matrix)
      - [Triangular matrix](linear-algebra.md#triangular-matrix)
      - [Symmetric matrix](linear-algebra.md#symmetric-matrix)
        - [Definite matrix](linear-algebra.md#definite-matrix)
          - [Positive definite matrix](linear-algebra.md#positive-definite-matrix)
        - [Skew-symmetric matrix](linear-algebra.md#skew-symmetric-matrix)
          - [Skew-symmetric form](linear-algebra.md#skew-symmetric-form)
  - [Vector space](linear-algebra.md#vector-space)
    - [Basis (linear algebra)](linear-algebra.md#basis-linear-algebra)
      - [Change of basis](linear-algebra.md#change-of-basis)
        - [Change of basis matrix](linear-algebra.md#change-of-basis-matrix)
        - [Change of basis between symmetric matrices](linear-algebra.md#change-of-basis-between-symmetric-matrices)
      - [Linear independence](linear-algebra.md#linear-independence)
    - [Classification of vector spaces](linear-algebra.md#classification-of-vector-spaces)
    - [Underlying field of a vector space](linear-algebra.md#underlying-field-of-a-vector-space)
    - [Tensor product](linear-algebra.md#tensor-product)
    - [Vector (mathematics)](linear-algebra.md#vector-mathematics)
      - [Scalar (mathematics)](linear-algebra.md#scalar-mathematics)
  - [Tensor](linear-algebra.md#tensor)
    - [A linear map is a (1,1) tensor](linear-algebra.md#a-linear-map-is-a-1-1-tensor)
    - [Tensor space](linear-algebra.md#tensor-space)
      - [Order of a tensor](linear-algebra.md#order-of-a-tensor)
    - [Einstein notation](linear-algebra.md#einstein-notation)
      - [Raised and lowered indices](linear-algebra.md#raised-and-lowered-indices)
        - [Raised index](linear-algebra.md#raised-index)
        - [Lowered index](linear-algebra.md#lowered-index)
        - [Raising and lowering indices](linear-algebra.md#raising-and-lowering-indices)
      - [Implicit metric signature in Einstein notation](linear-algebra.md#implicit-metric-signature-in-einstein-notation)
      - [Einstein notation for partial derivatives](linear-algebra.md#einstein-notation-for-partial-derivatives)
        - [Divergence in Einstein notation](linear-algebra.md#divergence-in-einstein-notation)
        - [Laplacian in Einstein notation](linear-algebra.md#laplacian-in-einstein-notation)
          - [d'Alembert operator in Einstein notation](linear-algebra.md#d-alembert-operator-in-einstein-notation)
            - [Klein-Gordon equation in Einstein notation](linear-algebra.md#klein-gordon-equation-in-einstein-notation)
      - [Covariance and contravariance of vectors](linear-algebra.md#covariance-and-contravariance-of-vectors)
        - [Covariant vector](linear-algebra.md#covariant-vector)
        - [Contravariant vector](linear-algebra.md#contravariant-vector)
  - [Linear algebra bibliography](linear-algebra.md#linear-algebra-bibliography)
    - [Interactive Linear Algebra by Margalit and Rabinoff](linear-algebra.md#interactive-linear-algebra-by-margalit-and-rabinoff)
- [Group](group.md)
  - [Center (group theory)](group.md#center-group-theory)
  - [Group axiom](group.md#group-axiom)
    - [Commutative property](group.md#commutative-property)
      - [Abelian group](group.md#abelian-group)
        - [Non-commutative](group.md#non-commutative)
  - [Symmetry](group.md#symmetry)
    - [Symmetry breaking](group.md#symmetry-breaking)
  - [Important mathematical group](group.md#important-mathematical-group)
    - [Important discrete mathematical group](group.md#important-discrete-mathematical-group)
      - [Cyclic group](group.md#cyclic-group)
      - [The direct product of two cyclic groups of coprime order is another cyclic group](group.md#the-direct-product-of-two-cyclic-groups-of-coprime-order-is-another-cyclic-group)
      - [Permutation](group.md#permutation)
        - [Cycle notation](group.md#cycle-notation)
        - [Parity of a permutation](group.md#parity-of-a-permutation)
          - [Odd permutation](group.md#odd-permutation)
          - [Even permutation](group.md#even-permutation)
        - [Permutation group](group.md#permutation-group)
          - [Stabilizer (group)](group.md#stabilizer-group)
          - [Symmetric group](group.md#symmetric-group)
            - [All groups are isomorphic to a subgroup of the symmetric group](group.md#all-groups-are-isomorphic-to-a-subgroup-of-the-symmetric-group)
          - [Alternating group](group.md#alternating-group)
            - [Alternating group of degree 5](group.md#alternating-group-of-degree-5)
              - [The alternating groups of degree 5 or greater are simple](group.md#the-alternating-groups-of-degree-5-or-greater-are-simple)
      - [Dihedral group](group.md#dihedral-group)
      - [Wallpaper group](group.md#wallpaper-group)
      - [Space group](group.md#space-group)
      - [Klein four-group](group.md#klein-four-group)
  - [Finite group](group.md#finite-group)
    - [Classification of finite groups](group.md#classification-of-finite-groups)
      - [List of finite groups](group.md#list-of-finite-groups)
        - [GroupNames](group.md#groupnames)
      - [Classification of finite simple groups](group.md#classification-of-finite-simple-groups)
        - [Group of Lie type](group.md#group-of-lie-type)
          - [Chevalley group](group.md#chevalley-group)
            - [Chevalley groups $A_n(q)$](group.md#chevalley-groups-a-n-q)
        - [Sporadic group](group.md#sporadic-group)
          - [Mathieu group](group.md#mathieu-group)
            - [k-transitive group](group.md#k-transitive-group)
              - [Classification of k-transitive groups](group.md#classification-of-k-transitive-groups)
                - [2-transitive group](group.md#2-transitive-group)
                  - [Classification of 2-transitive groups](group.md#classification-of-2-transitive-groups)
                - [Classification of 3-transitive groups](group.md#classification-of-3-transitive-groups)
                - [Classification of 4-transitive groups](group.md#classification-of-4-transitive-groups)
                - [Classification of 5-transitive groups](group.md#classification-of-5-transitive-groups)
                - [Classification of 6-transitive groups](group.md#classification-of-6-transitive-groups)
            - [Mathieu group $M_{11}$](group.md#mathieu-group-m-11)
            - [Mathieu group $M_{12}$](group.md#mathieu-group-m-12)
            - [Mathieu group $M_{22}$](group.md#mathieu-group-m-22)
            - [Mathieu group $M_{23}$](group.md#mathieu-group-m-23)
            - [Mathieu group $M_{24}$](group.md#mathieu-group-m-24)
          - [Janko group](group.md#janko-group)
          - [Monster group](group.md#monster-group)
            - [Monstrous moonshine](group.md#monstrous-moonshine)
        - [Jordan-Holder Theorem](group.md#jordan-holder-theorem)
        - [Composition series](group.md#composition-series)
      - [Group extension problem](group.md#group-extension-problem)
  - [Group operation](group.md#group-operation)
  - [Group isomorphism](group.md#group-isomorphism)
    - [Isomorphism](group.md#isomorphism)
    - [Group homomorphism](group.md#group-homomorphism)
      - [Fundamental theorem on homomorphisms](group.md#fundamental-theorem-on-homomorphisms)
      - [Kernel (algebra)](group.md#kernel-algebra)
  - [Generating set of a group](group.md#generating-set-of-a-group)
    - [Finitely generated group](group.md#finitely-generated-group)
    - [Rank of a group](group.md#rank-of-a-group)
    - [Cayley graph](group.md#cayley-graph)
      - [Cycle graph (algebra)](group.md#cycle-graph-algebra)
    - [Cycle of an element of a group](group.md#cycle-of-an-element-of-a-group)
      - [Order of an element of a group](group.md#order-of-an-element-of-a-group)
  - [Direct product of groups](group.md#direct-product-of-groups)
    - [Product of group subsets](group.md#product-of-group-subsets)
    - [Semidirect product](group.md#semidirect-product)
  - [Subgroup](group.md#subgroup)
    - [Subgroup generated by a group](group.md#subgroup-generated-by-a-group)
    - [Quotient group](group.md#quotient-group)
      - [Subquotient](group.md#subquotient)
      - [Relationship between the quotient group and direct products](group.md#relationship-between-the-quotient-group-and-direct-products)
      - [Normal subgroup](group.md#normal-subgroup)
        - [Simple group](group.md#simple-group)
          - [How to show that a group is simple](group.md#how-to-show-that-a-group-is-simple)
  - [Ring (mathematics)](group.md#ring-mathematics)
    - [Commutative ring](group.md#commutative-ring)
    - [Division ring](group.md#division-ring)
    - [Finite ring](group.md#finite-ring)
      - [Classification of finite rings](group.md#classification-of-finite-rings)
    - [Field (mathematics)](group.md#field-mathematics)
      - [Multiplicative inverse](group.md#multiplicative-inverse)
      - [Distributive property](group.md#distributive-property)
      - [Finite field](group.md#finite-field)
        - [Classification of finite fields](group.md#classification-of-finite-fields)
        - [Finite field of non-prime order](group.md#finite-field-of-non-prime-order)
        - [GF(2)](group.md#gf-2)
        - [GF(4)](group.md#gf-4)
      - [Quadratically closed field](group.md#quadratically-closed-field)
      - [Vector field](group.md#vector-field)
        - [Algebra over a field](group.md#algebra-over-a-field)
          - [Division algebra](group.md#division-algebra)
            - [Frobenius theorem (real division algebras)](group.md#frobenius-theorem-real-division-algebras)
- [Associative property](#associative-property)
- [Algebraic geometry](#algebraic-geometry)
  - [The beauty of algebraic geometry](#the-beauty-of-algebraic-geometry)
  - [Algebraic curve](#algebraic-curve)
  - [Elliptic curve](#elliptic-curve)
    - [Elliptic curve group](#elliptic-curve-group)
      - [Elliptic curve point addition](#elliptic-curve-point-addition)
      - [Elliptic curve point multiplication](#elliptic-curve-point-multiplication)
    - [Domain of an elliptic curve](#domain-of-an-elliptic-curve)
      - [Not every $x$ belongs to the elliptic curve over a non quadratically closed field](#not-every-x-belongs-to-the-elliptic-curve-over-a-non-quadratically-closed-field)
        - [Number of elements of an elliptic curve](#number-of-elements-of-an-elliptic-curve)
      - [Elliptic curve over the real numbers](#elliptic-curve-over-the-real-numbers)
      - [Elliptic curve over the rational numbers](#elliptic-curve-over-the-rational-numbers)
        - [Number of elements of an elliptic curve over the rational numbers](#number-of-elements-of-an-elliptic-curve-over-the-rational-numbers)
          - [Mordell's theorem](#mordell-s-theorem)
            - [Rank of an elliptic curve over the rational numbers](#rank-of-an-elliptic-curve-over-the-rational-numbers)
              - [Largest known ranks of an elliptic curve over the rational numbers](#largest-known-ranks-of-an-elliptic-curve-over-the-rational-numbers)
        - [Reduction of an elliptic curve over the rational numbers to an elliptic curve over a finite field mod p](#reduction-of-an-elliptic-curve-over-the-rational-numbers-to-an-elliptic-curve-over-a-finite-field-mod-p)
        - [Birch and Swinnerton-Dyer conjecture](#birch-and-swinnerton-dyer-conjecture)
          - [BSD conjecture bibliography](#bsd-conjecture-bibliography)
            - [Birch and Swinnerton-Dyer conjecture in two minutes by Ciro Santilli](#birch-and-swinnerton-dyer-conjecture-in-two-minutes-by-ciro-santilli)
            - [Notes on Elliptic Curves (II) by BSD](#notes-on-elliptic-curves-ii-by-bsd)
      - [Elliptic curve over a finite field](#elliptic-curve-over-a-finite-field)
        - [Number of elements of an elliptic curve over a finite field](#number-of-elements-of-an-elliptic-curve-over-a-finite-field)
          - [Schoof's algorithm](#schoof-s-algorithm)
    - [Elliptic curve bibliography](#elliptic-curve-bibliography)
      - [Elliptic curve university course](#elliptic-curve-university-course)

## Abstract algebra

↑ **Parent:** [Algebra](algebra.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Abstract_algebra)

We just use "Abstract algebra" as a synonym for [algebra](algebra.md).

## Algebraic structure

↑ **Parent:** [Algebra](algebra.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Algebraic_structure)

A [set](formalization-of-mathematics.md#set-mathematics) $S$ plus any number of functions $f_i : S \times S \to S$, such that each $f_i$ satisfies some properties of choice.

Key examples:
- [group](group.md): one function
- [field](group.md#field-mathematics): two functions
- [ring](group.md#ring-mathematics): also two functions, but with less restrictive properties

### Commutator

↑ **Parent:** [Algebraic structure](#algebraic-structure)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Commutator)

### Identity element

↑ **Parent:** [Algebraic structure](#algebraic-structure)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Identity_element)

#### Inverse element

↑ **Parent:** [Identity element](#identity-element)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Inverse_element)

Some specific examples:
- [invertible matrix](linear-algebra.md#invertible-matrix)

##### Invertible

↑ **Parent:** [Inverse element](#inverse-element)

### Order (algebra)

↑ **Parent:** [Algebraic structure](#algebraic-structure)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Order_(algebra))

The order of a [algebraic structure](#algebraic-structure) is just its [cardinality](formalization-of-mathematics.md#cardinality).

Sometimes, especially in the case of structures with an [infinite](calculus.md#infinity) number of elements, it is often more convenient to talk in terms of some parameter that characterizes the structure, and that parameter is usually called the [degree](#degree-algebra).

#### Degree (algebra)

↑ **Parent:** [Order (algebra)](#order-algebra)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Degree_(algebra))

The degree of some [algebraic structure](#algebraic-structure) is some parameter that describes the structure. There is no universal definition valid for all structures, it is a per structure type thing.

This is particularly useful when talking about structures with an [infinite](calculus.md#infinity) number of elements, but it is sometimes also used for finite structures.

Examples:
- the [dihedral group](group.md#dihedral-group) of degree n acts on n elements, and has order 2n
- the parameter $n$ that characterizes the size of the [general linear group](geometry.md#general-linear-group) $GL(n)$ is called the degree of that group, i.e. the dimension of the underlying matrices

#### Finite algebraic structure

↑ **Parent:** [Order (algebra)](#order-algebra)

Examples:
- [finite group](group.md#finite-group)
- [finite field](group.md#finite-field)

## Linear algebra

↑ **Parent:** [Algebra](algebra.md)

[This section is present in another page, follow this link to view it.](linear-algebra.md)

## Group

↑ **Parent:** [Algebra](algebra.md)

[This section is present in another page, follow this link to view it.](group.md)

## Associative property

↑ **Parent:** [Algebra](algebra.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Associative_property)

## Algebraic geometry

↑ **Parent:** [Algebra](algebra.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Algebraic_geometry)

### The beauty of algebraic geometry

↑ **Parent:** [Algebraic geometry](#algebraic-geometry)  
🏷️ **Tags:** [The beauty of mathematics](mathematics.md#the-beauty-of-mathematics)

[https://mathoverflow.net/questions/20112/interesting-results-in-algebraic-geometry-accessible-to-3rd-year-undergraduates](https://mathoverflow.net/questions/20112/interesting-results-in-algebraic-geometry-accessible-to-3rd-year-undergraduates) Interesting results in algebraic geometry accessible to 3rd year undergraduates

### Algebraic curve

↑ **Parent:** [Algebraic geometry](#algebraic-geometry)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Algebraic_curve)

### Elliptic curve

↑ **Parent:** [Algebraic geometry](#algebraic-geometry)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Elliptic_curve)

An elliptic curve is defined by numbers $a$ and $b$. The curve is the set of all points $(x, y)$ of the [real plane](calculus.md#real-plane) that satisfy the [Equation 1. "Definition of the elliptic curves"](#equation-definition-of-the-elliptic-curves)

<a id="equation-definition-of-the-elliptic-curves"></a>
$$
y^2 = x^3 + ax + b
$$

<a id="image-plots-of-real-elliptic-curves-for-various-values-of-a-and-b"></a>
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/d/db/EllipticCurveCatalog.svg/960px-EllipticCurveCatalog.svg.png" alt="" height="800">

**[Figure 1](#image-plots-of-real-elliptic-curves-for-various-values-of-a-and-b). Plots of real elliptic curves for various values of $a$ and $b$**. [Source](https://commons.wikimedia.org/wiki/File:EllipticCurveCatalog.svg.png).

[Equation 1. "Definition of the elliptic curves"](#equation-definition-of-the-elliptic-curves) definies [elliptic curves](#elliptic-curve) over any [field](group.md#field-mathematics), it doesn't have to the [real numbers](formalization-of-mathematics.md#real-number). Notably, the definition also works for [finite fields](group.md#finite-field), leading to [elliptic curve over a finite fields](#elliptic-curve-over-a-finite-field), which are the ones used in [Elliptic-curve Diffie-Hellman](cryptography.md#elliptic-curve-diffie-hellman) cyprotgraphy.

#### Elliptic curve group

↑ **Parent:** [Elliptic curve](#elliptic-curve)

The [elliptic curve group](#elliptic-curve-group) of an [elliptic curve](#elliptic-curve) is a group in which the elements of the group are points on an [elliptic curve](#elliptic-curve).

The [group operation](group.md#group-operation) is called [elliptic curve point addition](#elliptic-curve-point-addition).

Bibliography:
- [https://mathoverflow.net/questions/6870/why-is-an-elliptic-curve-a-group](https://mathoverflow.net/questions/6870/why-is-an-elliptic-curve-a-group)

##### Elliptic curve point addition

↑ **Parent:** [Elliptic curve group](#elliptic-curve-group)

[Elliptic curve point addition](#elliptic-curve-point-addition) is the [group operation](group.md#group-operation) of an [elliptic curve group](#elliptic-curve-group), i.e. it is a [function](formalization-of-mathematics.md#function-mathematics) that takes two points of an [elliptic curve](#elliptic-curve) as input, and returns a third point of the [elliptic curve](#elliptic-curve) as its output, while obeying the [group axioms](group.md#group-axiom).

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

This definition relies only on operations that we know how to do on arbitrary [fields](group.md#field-mathematics):
- [addition](formalization-of-mathematics.md#addition) $+$
- [multiplication](formalization-of-mathematics.md#multiplication) $\times$
and it therefore works for [elliptic curves](#elliptic-curve) defined over any field.

Just remember that:

$$
x/y
$$

means:

$$
x \times y^{-1}
$$

and that $y^{-1}$ always exists because it is the [inverse element](#inverse-element), which is guaranteed to exist for multiplication due to the [group axioms](group.md#group-axiom) it obeys.

The group function is usually called [elliptic curve point addition](#elliptic-curve-point-addition), and repeated addition as done for [DHKE](cryptography.md#diffie-hellman-key-exchange) is called [elliptic curve point multiplication](#elliptic-curve-point-multiplication).

<a id="image-visualisation-of-elliptic-curve-point-addition"></a>
![](https://upload.wikimedia.org/wikipedia/commons/a/ae/ECClines-2.svg)

**[Figure 2](#image-visualisation-of-elliptic-curve-point-addition). Visualisation of elliptic curve point addition**. [Source](https://commons.wikimedia.org/wiki/File:ECClines-2.svg).

##### Elliptic curve point multiplication

↑ **Parent:** [Elliptic curve group](#elliptic-curve-group)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Elliptic_curve_point_multiplication)

#### Domain of an elliptic curve

↑ **Parent:** [Elliptic curve](#elliptic-curve)

##### Not every $x$ belongs to the elliptic curve over a non quadratically closed field

↑ **Parent:** [Domain of an elliptic curve](#domain-of-an-elliptic-curve)

One major difference between the [elliptic curve over a finite field](#elliptic-curve-over-a-finite-field) or the [elliptic curve over the rational numbers](#elliptic-curve-over-the-rational-numbers) the [elliptic curve over the real numbers](#elliptic-curve-over-the-real-numbers) is that not every possible $x$ generates a member of the curve.

This is because on the [Equation 1. "Definition of the elliptic curves"](#equation-definition-of-the-elliptic-curves) we see that given an $x$, we calculate $x^3 + ax + b$, which always produces an element $y^2$.

But then we are not necessarily able to find an $y$ for the $y^2$, because not all [fields](group.md#field-mathematics) are not [quadratically closed fields](group.md#quadratically-closed-field).

For example: with $a = 1$ and $b = 1$, taking $x = 1$ gives:

$$
y^2 = 1^3 + 1 \times 1 + 1 = 3
$$

and therefore there is no $y \in \Q$ that satisfies the equation. So $x = 1$ is not on the curve if we consider this [elliptic curve over the rational numbers](#elliptic-curve-over-the-rational-numbers).

That $x$ would also not belong to [Elliptic curve over the finite field](#elliptic-curve-over-a-finite-field) $\F_4$, because doing everything $\mod 4$ we have:

$$
\begin{aligned}
0*0 &= 0 &    &\mod 4 \\
1*1 &= 1 &    &\mod 4 \\
2*2 &= 4 &= 0 &\mod 4 \\
3*3 &= 9 &= 1 &\mod 4 \\
\end{aligned}
$$

Therefore, there is no element $y \in \F_4$ such that $y \times y = 2$ or $y \times y = 3$, i.e. $2$ and $3$ don't have a [multiplicative inverse](group.md#multiplicative-inverse).

For the [real numbers](formalization-of-mathematics.md#real-number), it would work however, because the [real numbers](formalization-of-mathematics.md#real-number) are a [quadratically closed field](group.md#quadratically-closed-field), and $\sqrt{3} \in \R$.

For this reason, it is not necessarily trivial to determine the [number of elements of an elliptic curve](#number-of-elements-of-an-elliptic-curve).

###### Number of elements of an elliptic curve

↑ **Parent:** [Not every $x$ belongs to the elliptic curve over a non quadratically closed field](#not-every-x-belongs-to-the-elliptic-curve-over-a-non-quadratically-closed-field)

##### Elliptic curve over the real numbers

↑ **Parent:** [Domain of an elliptic curve](#domain-of-an-elliptic-curve)  
🏷️ **Tags:** [Real number](formalization-of-mathematics.md#real-number)

##### Elliptic curve over the rational numbers

↑ **Parent:** [Domain of an elliptic curve](#domain-of-an-elliptic-curve)  
🏷️ **Tags:** [Rational number](formalization-of-mathematics.md#rational-number)

###### Number of elements of an elliptic curve over the rational numbers

↑ **Parent:** [Elliptic curve over the rational numbers](#elliptic-curve-over-the-rational-numbers)  
🏷️ **Tags:** [Number of elements of an elliptic curve](#number-of-elements-of-an-elliptic-curve)

Can be finite or infinite! TODO examples. But it is always a [finitely generated group](group.md#finitely-generated-group).

<h6 id="mordell-s-theorem">Mordell's theorem</h6>

↑ **Parent:** [Number of elements of an elliptic curve over the rational numbers](#number-of-elements-of-an-elliptic-curve-over-the-rational-numbers)

The [elliptic curve group](#elliptic-curve-group) of all [elliptic curve over the rational numbers](#elliptic-curve-over-the-rational-numbers) is always a [finitely generated group](group.md#finitely-generated-group).

The number of points may be either finite or infinite. But when infinite, it is still a [finitely generated group](group.md#finitely-generated-group).

For this reason, the [rank of an elliptic curve over the rational numbers](#rank-of-an-elliptic-curve-over-the-rational-numbers) is always defined.

TODO example.

###### Rank of an elliptic curve over the rational numbers

↑ **Parent:** [Mordell's theorem](#mordell-s-theorem)  
🏷️ **Tags:** [Rank of a group](group.md#rank-of-a-group)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Rank_of_an_elliptic_curve)

[Mordell's theorem](#mordell-s-theorem) guarantees that [the rank](group.md#rank-of-a-group) (number of elements in the [generating set of the group](group.md#generating-set-of-a-group)) is always well defined for an [elliptic curve over the rational numbers](#elliptic-curve-over-the-rational-numbers). But as of 2023 there is no known algorithm which calculates the rank of any curve!

It is not even known if there are elliptic curves of every rank or not: [Largest known ranks of an elliptic curve over the rational numbers](#largest-known-ranks-of-an-elliptic-curve-over-the-rational-numbers), and it has proven extremely hard to find new ones over time.

TODO list of known values and algorithms? The [Birch and Swinnerton-Dyer conjecture](#birch-and-swinnerton-dyer-conjecture) would immediately provide a stupid algorithm for it.

###### Largest known ranks of an elliptic curve over the rational numbers

↑ **Parent:** [Rank of an elliptic curve over the rational numbers](#rank-of-an-elliptic-curve-over-the-rational-numbers)

[https://web.math.pmf.unizg.hr/~duje/tors/rankhist.html](https://web.math.pmf.unizg.hr/~duje/tors/rankhist.html) gives a list with Elkies (2006) on top with:

$$
y^2 + xy + y = x^3 - x^2 - 20067762415575526585033208209338542750930230312178956502 x + 34481611795030556467032985690390720374855944359319180361266008296291939448732243429
$$

TODO why this non standard formulation?

###### Reduction of an elliptic curve over the rational numbers to an elliptic curve over a finite field mod p

↑ **Parent:** [Elliptic curve over the rational numbers](#elliptic-curve-over-the-rational-numbers)

This construction takes as input:
- [elliptic curve over the rational numbers](#elliptic-curve-over-the-rational-numbers)
- a prime number $p$
and it produces an [elliptic curve over a finite field](#elliptic-curve-over-a-finite-field) of order $p$ as output.

The constructions is used in the [Birch and Swinnerton-Dyer conjecture](#birch-and-swinnerton-dyer-conjecture).

To do it, we just convert the coefficients $a$ and $b$ from the [Equation 1. "Definition of the elliptic curves"](#equation-definition-of-the-elliptic-curves) from [rational numbers](formalization-of-mathematics.md#rational-number) to elements of the [finite field](group.md#finite-field).

For example, suppose we have $a = 3/4$ and we are using $p = 11$.

For the [denominator](formalization-of-mathematics.md#denominator) $4$, we just use the [multiplicative inverse](group.md#multiplicative-inverse), e.g. supposing we have

$$
\frac{3}{4} \to 3 \times 4^{-1} \mod 11 = 3 \times 3 \mod 11 = 9 \mod 11
$$

where $4^{-1} = 3 \mod 11$ because $4 \times 3 = 1 \mod 11$, related: [https://math.stackexchange.com/questions/1204034/elliptic-curve-reduction-modulo-p](https://math.stackexchange.com/questions/1204034/elliptic-curve-reduction-modulo-p)

###### Birch and Swinnerton-Dyer conjecture

↑ **Parent:** [Elliptic curve over the rational numbers](#elliptic-curve-over-the-rational-numbers)  
🏷️ **Tags:** [Millennium Prize Problems](mathematics.md#millennium-prize-problems)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Birch_and_Swinnerton-Dyer_conjecture)

The BSD conjecture states that if your name is long enough, it will always count as two letters on a famous conjecture.

Maybe also insert a joke about [BSD Operating Systems](systems-programming.md#berkeley-software-distribution) if you're into that kind of stuff.

The conjecture states that [Equation 10. "BSD conjecture"](#equation-bsd-conjecture) holds for every [elliptic curve over the rational numbers](#elliptic-curve-over-the-rational-numbers) (which is defined by its  constants $a$ and $b$)

<a id="equation-bsd-conjecture"></a>
$$
\lim_{x \to \infty} \prod_{p \leq x} \frac{N_p}{p} = C \log(x)^r
$$

The conjecture, if true, provides a (possibly inefficient) way to calculate the [rank of an elliptic curve over the rational numbers](#rank-of-an-elliptic-curve-over-the-rational-numbers), since we can calculate the [number of elements of an elliptic curve over a finite field](#number-of-elements-of-an-elliptic-curve-over-a-finite-field) by [Schoof's algorithm](#schoof-s-algorithm) in [polynomial time](computer-science.md#p-complexity). So it is just a matter of calculating $N_p$ like that up to some point at which we are quite certain about $r$.

The [Wikipedia page of the this conecture](https://en.wikipedia.org/wiki/Birch_and_Swinnerton-Dyer_conjecture) is the perfect example of why [it is not possible to teach natural sciences on Wikipedia](website.md#it-is-not-possible-to-teach-natural-sciences-on-wikipedia). A [million dollar problem](mathematics.md#millennium-prize-problems), and the page is thoroughly incomprehensible unless you already know everything!

<a id="image-lim-x-to-infty-prod-p-leq-x-frac-n-p-p-as-a-function-of-p-for-the-elliptic-curve-y-2-x-3-5x"></a>
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/62/BSD_data_plot_for_elliptic_curve_800h1.svg/500px-BSD_data_plot_for_elliptic_curve_800h1.svg.png" alt="" height="400">

**[Figure 3](#image-lim-x-to-infty-prod-p-leq-x-frac-n-p-p-as-a-function-of-p-for-the-elliptic-curve-y-2-x-3-5x). $\lim_{x \to \infty} \prod_{p \leq x} \frac{N_p}{p}$ as a function of $p$ for the elliptic curve $y^2 = x^3 - 5x$**. [Source](https://commons.wikimedia.org/wiki/File:BSD_data_plot_for_elliptic_curve_800h1.svg.png). The curve is known to have [rank](#rank-of-an-elliptic-curve-over-the-rational-numbers) 1, and the logarithmic plot tends more and more to a line of slope 1 as expected from the conjecture, matching the rank.

<a id="video-birch-and-swinnerton-dyer-conjecture-by-kinertia-2020"></a>
**[Video 1](#video-birch-and-swinnerton-dyer-conjecture-by-kinertia-2020). Birch and Swinnerton-Dyer conjecture by Kinertia (2020)** [Source](https://www.youtube.com/watch?v=R9FKN9MIHlE).

<a id="video-the-1-000-000-birch-and-swinnerton-dyer-conjecture-by-absolutely-uniformly-confused-2022"></a>
**[Video 2](#video-the-1-000-000-birch-and-swinnerton-dyer-conjecture-by-absolutely-uniformly-confused-2022). The $1,000,000 Birch and Swinnerton-Dyer conjecture by Absolutely Uniformly Confused (2022)** [Source](https://www.youtube.com/watch?v=tjnwEGBUOLI). A respectable 1 minute attempt. But will be too fast for most people. The sweet spot is likely 2 minutes.

###### BSD conjecture bibliography

↑ **Parent:** [Birch and Swinnerton-Dyer conjecture](#birch-and-swinnerton-dyer-conjecture)

###### Birch and Swinnerton-Dyer conjecture in two minutes by Ciro Santilli

↑ **Parent:** [BSD conjecture bibliography](#bsd-conjecture-bibliography)

Summary:
- overview of the formula of the [BSD conjecture](#birch-and-swinnerton-dyer-conjecture)
- definition of [elliptic curve](#elliptic-curve)
- [domain of an elliptic curve](#domain-of-an-elliptic-curve). Prerequisite: [field](group.md#field-mathematics)
- [elliptic curve group](#elliptic-curve-group). Prerequisite: [group](group.md)
- [Mordell's theorem](#mordell-s-theorem) lets us define the [rank of an elliptic curve over the rational numbers](#rank-of-an-elliptic-curve-over-the-rational-numbers), which is the $r$. Prerequisite: [generating set of a group](group.md#generating-set-of-a-group)
- [reduction of an elliptic curve from $E(\Q)$ to $E(\F_p) \mod p$](#reduction-of-an-elliptic-curve-over-the-rational-numbers-to-an-elliptic-curve-over-a-finite-field-mod-p) lets us define $N_r$ as the number of elements of the generated finite group

**[Video 3](#_105)** [Source](https://www.youtube.com/watch?v=84ig5cih4kI).

###### Notes on Elliptic Curves (II) by BSD

↑ **Parent:** [BSD conjecture bibliography](#bsd-conjecture-bibliography)

The paper that states the [BSD conjecture](#birch-and-swinnerton-dyer-conjecture).

Likely [paywalled](education.md#closed-access-academic-journals-are-evil) at: [https://www.degruyter.com/document/doi/10.1515/crll.1965.218.79/html](https://www.degruyter.com/document/doi/10.1515/crll.1965.218.79/html). One illegal upload at: [http://virtualmath1.stanford.edu/~conrad/BSDseminar/refs/BSDorigin.pdf](http://virtualmath1.stanford.edu/~conrad/BSDseminar/refs/BSDorigin.pdf).

##### Elliptic curve over a finite field

↑ **Parent:** [Domain of an elliptic curve](#domain-of-an-elliptic-curve)  
🏷️ **Tags:** [Finite field](group.md#finite-field)

The [Equation 1. "Definition of the elliptic curves"](#equation-definition-of-the-elliptic-curves) and definitions on [elliptic curve point addition](#elliptic-curve-point-addition) both hold directly.

###### Number of elements of an elliptic curve over a finite field

↑ **Parent:** [Elliptic curve over a finite field](#elliptic-curve-over-a-finite-field)  
🏷️ **Tags:** [Number of elements of an elliptic curve](#number-of-elements-of-an-elliptic-curve)

<h6 id="schoof-s-algorithm">Schoof's algorithm</h6>

↑ **Parent:** [Number of elements of an elliptic curve over a finite field](#number-of-elements-of-an-elliptic-curve-over-a-finite-field)  
🏷️ **Tags:** [Polynomial time algorithm](computer-science.md#polynomial-time-algorithm)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Schoof's_algorithm)

#### Elliptic curve bibliography

↑ **Parent:** [Elliptic curve](#elliptic-curve)

- [https://www.cantorsparadise.com/another-math-problem-that-will-earn-you-a-million-dollars-for-solving-it-95546d4841cc](https://www.cantorsparadise.com/another-math-problem-that-will-earn-you-a-million-dollars-for-solving-it-95546d4841cc)

##### Elliptic curve university course

↑ **Parent:** [Elliptic curve bibliography](#elliptic-curve-bibliography)

## ↑ Ancestors (3)

1. [Area of mathematics](mathematics.md#area-of-mathematics)
2. [Mathematics](mathematics.md)
3. [Ciro Santilli's Homepage](README.md)

## ← Incoming links (2)

- [Abstract algebra](#abstract-algebra)
- [Field (mathematics)](group.md#field-mathematics)
