# Geometry

↑ **Parent:** [Area of mathematics](mathematics.md#area-of-mathematics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Geometry)

**Table of contents**

- [Minimum bounding box](#minimum-bounding-box)
- [Bounding box](#bounding-box)
- [Fractal](#fractal)
- [Point (geometry)](#point-geometry)
  - [Line (geometry)](#line-geometry)
  - [Hyperplane](#hyperplane)
    - [Plane (geometry)](#plane-geometry)
- [n-sphere](#n-sphere)
  - [Antipodal point](#antipodal-point)
  - [Diameter](#diameter)
    - [Radius](#radius)
  - [Circle](#circle)
    - [Squaring the circle](#squaring-the-circle)
    - [Tarski's circle-squaring problem](#tarski-s-circle-squaring-problem)
  - [Sphere](#sphere)
    - [Great circle](#great-circle)
  - [3-sphere](#3-sphere)
- [Projective geometry](#projective-geometry)
  - [Projective space](#projective-space)
    - [Projective plane](#projective-plane)
  - [Real projective space](#real-projective-space)
    - [Real projective line](#real-projective-line)
    - [Real projective plane](#real-projective-plane)
      - [Synthetic geometry of the real projective plane](#synthetic-geometry-of-the-real-projective-plane)
      - [Model of the real projective plane](#model-of-the-real-projective-plane)
        - [Lines through origin model of the real projective plane](#lines-through-origin-model-of-the-real-projective-plane)
        - [Spherical cap model of the real projective plane](#spherical-cap-model-of-the-real-projective-plane)
      - [The real projective plane is not simply connected](#the-real-projective-plane-is-not-simply-connected)
      - [Point at infinity](#point-at-infinity)
      - [Homogenous coordinates](#homogenous-coordinates)
- [Polytope](#polytope)
  - [Convex polytope](#convex-polytope)
  - [Regular polytope](#regular-polytope)
    - [Classification of regular polytopes](#classification-of-regular-polytopes)
      - [Simplex](#simplex)
      - [Hypercube](#hypercube)
        - [Hyperrectangle](#hyperrectangle)
      - [Cross polytope](#cross-polytope)
  - [Polygon](#polygon)
    - [Quadrilateral](#quadrilateral)
      - [Rectangle](#rectangle)
    - [Parallelogram](#parallelogram)
      - [Parallelepiped](#parallelepiped)
        - [Volume of the parallelepiped](#volume-of-the-parallelepiped)
    - [Regular polygon](#regular-polygon)
      - [Regular convex polygon](#regular-convex-polygon)
        - [Triangle](#triangle)
        - [Square](#square)
        - [Pentagon](#pentagon)
        - [Hexagon](#hexagon)
        - [Octagon](#octagon)
  - [Polyhedron](#polyhedron)
    - [Tetrahedron](#tetrahedron)
    - [Octahedron](#octahedron)
  - [Regular polyhedron](#regular-polyhedron)
    - [Platonic solid](#platonic-solid)
  - [4-polytope](#4-polytope)
    - [Regular 4-polytope](#regular-4-polytope)
      - [Tesseract](#tesseract)
- [Differential geometry](#differential-geometry)
  - [Lie group](#lie-group)
    - [Lie derivative](#lie-derivative)
    - [Applications of Lie groups to differential equations](#applications-of-lie-groups-to-differential-equations)
    - [Lie algebra](#lie-algebra)
      - [Infinitesimal generator](#infinitesimal-generator)
      - [Lie group-Lie algebra correspondence](#lie-group-lie-algebra-correspondence)
        - [Lie algebra exponential covering problem](#lie-algebra-exponential-covering-problem)
          - [A single exponential map is not enough to recover a simple Lie group from its algebra](#a-single-exponential-map-is-not-enough-to-recover-a-simple-lie-group-from-its-algebra)
          - [The product of a exponential of the compact algebra with that of the non-compact algebra recovers a simple Lie from its algebra](#the-product-of-a-exponential-of-the-compact-algebra-with-that-of-the-non-compact-algebra-recovers-a-simple-lie-from-its-algebra)
        - [Two different Lie groups can have the same Lie algebra](#two-different-lie-groups-can-have-the-same-lie-algebra)
          - [Every Lie algebra has a unique single corresponding simply connected Lie group](#every-lie-algebra-has-a-unique-single-corresponding-simply-connected-lie-group)
            - [Universal covering group](#universal-covering-group)
          - [Every Lie group that has a given Lie algebra is the image of an homomorphism from the universal cover group](#every-lie-group-that-has-a-given-lie-algebra-is-the-image-of-an-homomorphism-from-the-universal-cover-group)
      - [Lie bracket](#lie-bracket)
      - [Exponential map](#exponential-map)
        - [Exponential map (Lie theory)](#exponential-map-lie-theory)
      - [Baker-Campbell-Hausdorff formula](#baker-campbell-hausdorff-formula)
      - [Generator of a Lie algebra](#generator-of-a-lie-algebra)
      - [Generators of a Lie algebra](#generators-of-a-lie-algebra)
    - [Continuous symmetry](#continuous-symmetry)
      - [Local symmetry](#local-symmetry)
        - [Local symmetries of the Lagrangian imply conserved currents](#local-symmetries-of-the-lagrangian-imply-conserved-currents)
    - [Important Lie group](#important-lie-group)
      - [Matrix Lie group](#matrix-lie-group)
        - [Every closed subgroup of $GL(n, \C)$ is a Lie group](#every-closed-subgroup-of-gl-n-c-is-a-lie-group)
        - [Lie algebra of a matrix Lie group](#lie-algebra-of-a-matrix-lie-group)
          - [Lie bracket of a matrix Lie group](#lie-bracket-of-a-matrix-lie-group)
          - [One parameter subgroup](#one-parameter-subgroup)
      - [Classical group](#classical-group)
        - [Symplectic group](#symplectic-group)
          - [Symplectic matrix](#symplectic-matrix)
          - [Unitary symplectic group](#unitary-symplectic-group)
      - [General linear group](#general-linear-group)
        - [Finite general linear group](#finite-general-linear-group)
      - [Lie algebra of $GL(n)$](#lie-algebra-of-gl-n)
      - [Special linear group](#special-linear-group)
        - [Special linear group of dimension 2](#special-linear-group-of-dimension-2)
        - [Lie algebra of $SL(n)$](#lie-algebra-of-sl-n)
          - [Lie algebra of $SL(2)$](#lie-algebra-of-sl-2)
        - [Finite special general linear group](#finite-special-general-linear-group)
      - [Isometry group](#isometry-group)
        - [Lie algebra of a isometry group](#lie-algebra-of-a-isometry-group)
      - [Orthogonal group](#orthogonal-group)
        - [Definition of the orthogonal group](#definition-of-the-orthogonal-group)
          - [The orthogonal group is the group of all matrices that preserve the dot product](#the-orthogonal-group-is-the-group-of-all-matrices-that-preserve-the-dot-product)
            - [What happens to the definition of the orthogonal group if we choose other types of symmetric bilinear forms](#what-happens-to-the-definition-of-the-orthogonal-group-if-we-choose-other-types-of-symmetric-bilinear-forms)
          - [The orthogonal group is the group of all invertible matrices where the inverse is equal to the transpose](#the-orthogonal-group-is-the-group-of-all-invertible-matrices-where-the-inverse-is-equal-to-the-transpose)
            - [Elements of the orthogonal group have determinant plus or minus one](#elements-of-the-orthogonal-group-have-determinant-plus-or-minus-one)
          - [The orthogonal group is the group of all matrices with orthonormal rows and orthonormal columns](#the-orthogonal-group-is-the-group-of-all-matrices-with-orthonormal-rows-and-orthonormal-columns)
        - [Topology of the orthogonal group](#topology-of-the-orthogonal-group)
          - [The orthogonal group is compact](#the-orthogonal-group-is-compact)
          - [Connected components of the orthogonal group](#connected-components-of-the-orthogonal-group)
        - [Lie algebra of $O(n)$](#lie-algebra-of-o-n)
        - [Special orthogonal group](#special-orthogonal-group)
          - [Lie algebra of $SO(3)$](#lie-algebra-of-so-3)
            - [Lie bracket of the rotation group](#lie-bracket-of-the-rotation-group)
          - [3D rotation group](#3d-rotation-group)
        - [Unitary group](#unitary-group)
          - [Unitary group of degree 1](#unitary-group-of-degree-1)
          - [Unitary group of degree 2](#unitary-group-of-degree-2)
          - [Unit circle](#unit-circle)
          - [Special unitary group](#special-unitary-group)
            - [Special unitary of degree 2](#special-unitary-of-degree-2)
              - [Representations of $SU(2)$](#representations-of-su-2)
                - [Lie algebra of $SU(2)$](#lie-algebra-of-su-2)
                - [2D representation of $SU(2)$](#2d-representation-of-su-2)
      - [Projective linear group](#projective-linear-group)
        - [Finite projective linear group](#finite-projective-linear-group)
        - [Projective special linear group](#projective-special-linear-group)
          - [Finite projective special linear group](#finite-projective-special-linear-group)
            - [$PSL(2, p)$](#psl-2-p)
              - [PSL(2,7)](#psl-2-7)
      - [Poincaré group](#poincare-group)
        - [Galilean transformation](#galilean-transformation)
          - [Translation (geometry)](#translation-geometry)
            - [Translation group](#translation-group)
              - [The derivative is the generator of the translation group](#the-derivative-is-the-generator-of-the-translation-group)
          - [Galilean invariance](#galilean-invariance)
            - [Covariance](#covariance)
              - [Invariant vs covariant](#invariant-vs-covariant)
        - [Lorentz group](#lorentz-group)
          - [Representation theory of the Lorentz group](#representation-theory-of-the-lorentz-group)
            - [Representation of the Lorentz group](#representation-of-the-lorentz-group)
              - [Lie algebra of the Lorentz group](#lie-algebra-of-the-lorentz-group)
              - [Spinor](#spinor)
          - [Lorentz boost](#lorentz-boost)
          - [Indefinite orthogonal group](#indefinite-orthogonal-group)
            - [Definition of the indefinite orthogonal group](#definition-of-the-indefinite-orthogonal-group)
              - [All indefinite orthogonal groups of matrices of equal metric signature are isomorphic](#all-indefinite-orthogonal-groups-of-matrices-of-equal-metric-signature-are-isomorphic)
            - [Indefinite special orthogonal group](#indefinite-special-orthogonal-group)
    - [Representation theory](#representation-theory)
      - [Irreducible representation](#irreducible-representation)
        - [Casimir element](#casimir-element)
      - [Schur's lemma](#schur-s-lemma)
    - [Simple Lie group](#simple-lie-group)
      - [Classification of simple Lie groups](#classification-of-simple-lie-groups)
    - [Lie group bibliography](#lie-group-bibliography)
      - [An Introduction to Tensors and Group Theory for Physicists by Nadir Jeevanjee (2011)](#an-introduction-to-tensors-and-group-theory-for-physicists-by-nadir-jeevanjee-2011)
      - [Lie Groups, Physics, and Geometry by Robert Gilmore (2008)](#lie-groups-physics-and-geometry-by-robert-gilmore-2008)
      - [Naive Lie theory by John Stillwell (2008)](#naive-lie-theory-by-john-stillwell-2008)
      - [Lie Algebras In Particle Physics by Howard Georgi (1999)](#lie-algebras-in-particle-physics-by-howard-georgi-1999)
- [Tesselation](#tesselation)
  - [Aperiodic tiling](#aperiodic-tiling)
  - [Tiling of the plane](#tiling-of-the-plane)
    - [Aperiodic monotile](#aperiodic-monotile)
      - [Smith aperiodic monotile](#smith-aperiodic-monotile)
      - [Spectre aperiodic monotile](#spectre-aperiodic-monotile)

## Minimum bounding box

↑ **Parent:** [Geometry](geometry.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Minimum_bounding_box)

## Bounding box

↑ **Parent:** [Geometry](geometry.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Bounding_box)

## Fractal

↑ **Parent:** [Geometry](geometry.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Fractal)

## Point (geometry)

↑ **Parent:** [Geometry](geometry.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Point_(geometry))

### Line (geometry)

↑ **Parent:** [Point (geometry)](#point-geometry)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Line_(geometry))

### Hyperplane

↑ **Parent:** [Point (geometry)](#point-geometry)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Hyperplane)

Generalization of a [plane](#plane-geometry) for any number of dimensions.

Kind of the opposite of a line: the line has dimension 1, and the plane has dimension D-1.

In $D=2$, both happen to coincide, a boring example of an [exceptional isomorphism](mathematics.md#exceptional-isomorphism).

#### Plane (geometry)

↑ **Parent:** [Hyperplane](#hyperplane)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Plane_(geometry))

## n-sphere

↑ **Parent:** [Geometry](geometry.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/n-sphere)

### Antipodal point

↑ **Parent:** [N-sphere](#n-sphere)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Antipodal_point)

### Diameter

↑ **Parent:** [N-sphere](#n-sphere)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Diameter)

#### Radius

↑ **Parent:** [Diameter](#diameter)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Radius)

### Circle

↑ **Parent:** [N-sphere](#n-sphere)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Circle)

#### Squaring the circle

↑ **Parent:** [Circle](#circle)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Squaring_the_circle)

<h4 id="tarski-s-circle-squaring-problem">Tarski's circle-squaring problem</h4>

↑ **Parent:** [Circle](#circle)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Tarski's_circle-squaring_problem)

Does not require straight line cuts.

### Sphere

↑ **Parent:** [N-sphere](#n-sphere)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Sphere)

#### Great circle

↑ **Parent:** [Sphere](#sphere)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Great_circle)

### 3-sphere

↑ **Parent:** [N-sphere](#n-sphere)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/3-sphere)

Diffeomorphic to [$SU(2)$](#special-unitary-of-degree-2).

## Projective geometry

↑ **Parent:** [Geometry](geometry.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Projective_geometry)

### Projective space

↑ **Parent:** [Projective geometry](#projective-geometry)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Projective_space)

A [unique](formalization-of-mathematics.md#uniqueness) projective space can be defined for any [vector space](linear-algebra.md#vector-space).

The projective space associated with a given [vector space](linear-algebra.md#vector-space) $V$ is denoted $\projectiveSpace(V)$.

The definition is to take the vector space, remove the zero element, and identify all elements that lie on the same line, i.e. $\vec{v} = \lambda \vec{w}$

The most important initial example to study is the [real projective plane](#real-projective-plane).

#### Projective plane

↑ **Parent:** [Projective space](#projective-space)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Projective_plane)

### Real projective space

↑ **Parent:** [Projective geometry](#projective-geometry)

In those cases at least, it is possible to add a [metric](calculus.md#metric-mathematics) to the spaces, leading to [elliptic geometry](calculus.md#elliptic-geometry).

#### Real projective line

↑ **Parent:** [Real projective space](#real-projective-space)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Real_projective_line)

Just a [circle](#circle).

Take $\R^2$ with a line at $x = 0$. Identify all the points that an observer 

#### Real projective plane

↑ **Parent:** [Real projective space](#real-projective-space)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Real_projective_plane)

For some reason, [Ciro Santilli](ciro-santilli.md) is mildly obsessed with understanding and visualizing the real projective plane.

To see why this is called a plane, move he center of the sphere to $z=1$, and project each line passing on the center of the sphere on the x-y plane. This works for all points of the sphere, except those at the equator $z=1$. Those are the [points at infinity](#point-at-infinity). Note that there is one such point at infinity for each direction in the x-y plane.

##### Synthetic geometry of the real projective plane

↑ **Parent:** [Real projective plane](#real-projective-plane)

It good to think about how [Euclid's postulates](mathematics.md#euclid-s-postulates) look like in the real projective plane:
- two parallel lines on the plane meet at a point on the sphere!

  Since there is one point of infinity for each direction, there is one such point for every direction the two parallel lines might be at. The [parallel postulate](mathematics.md#parallel-postulate) does not hold, and is replaced with a simpler more elegant version: every two lines meet at exactly one point.

  One thing to note however is that ther [real projective plane](#real-projective-plane) does not have [angles](linear-algebra.md#angle) defined on it by definition. Those can be defined, forming [elliptic geometry](calculus.md#elliptic-geometry) through the [projective model of elliptic geometry](calculus.md#projective-elliptic-geometry), but we can interpret the "parallel lines" as "two lines that meet at a point at infinity"
- points in the real projective plane are lines in [$\R^3$](calculus.md#real-coordinate-space-of-dimension-three)
- lines in the real projective plane are planes in [$\R^3$](calculus.md#real-coordinate-space-of-dimension-three).

  For every two projective points there is a single projective line that passes through them.

  Since it is a plane in [$\R^3$](calculus.md#real-coordinate-space-of-dimension-three), it always intersects the real plane at a line.

  Note however that not all lines in the real plane correspond to a projective line: only lines tangent to a circle at zero do.

Unlike the [real projective line](#real-projective-line) which is [homotopic](calculus.md#homotopy) to the [circle](#circle), the [real projective plane](#real-projective-plane) is not [homotopic](calculus.md#homotopy) to the [sphere](#sphere).

The [topological](calculus.md#topology) difference bewteen the [sphere](#sphere) and the [real projective space](#real-projective-space) is that for the [sphere](#sphere) all those points in the x-y circle are identified to a single point.

One more generalized argument of this is the [classification of closed surfaces](calculus.md#classification-of-closed-surfaces), in which the [real projective plane](#real-projective-plane) is a [sphere](#sphere) with a hole cut and one [Möbius strip](calculus.md#mobius-strip) glued in.

##### Model of the real projective plane

↑ **Parent:** [Real projective plane](#real-projective-plane)

###### Lines through origin model of the real projective plane

↑ **Parent:** [Model of the real projective plane](#model-of-the-real-projective-plane)

This is the standard model.

###### Spherical cap model of the real projective plane

↑ **Parent:** [Model of the real projective plane](#model-of-the-real-projective-plane)

[Ciro Santilli](ciro-santilli.md)'s preferred visualization of the real projective plane is a small variant of the standard "lines through origin in [$\R^3$](calculus.md#real-coordinate-space-of-dimension-three)".

Take a open half [sphere](#sphere) e.g. a sphere but only the points with $z > 0$.

Each point in the half sphere identifies a unique line through the origin.

Then, the only lines missing are the lines in the x-y plane itself.

For those sphere points in the [circle](#circle) on the x-y plane, you should think of them as magic poins that are identified with the corresponding [antipodal point](#antipodal-point), also on the x-y, but on the other side of the origin. So basically you you can teleport from one of those to the other side, and you are still in the same point.

Ciro likes this model because then all the magic is confined just to the $z=0$ part of the model, and everything else looks exactly like the sphere.

It is useful to contrast this with the sphere itself. In the sphere, all points in the circle $z = 0$ are the same point. But this is not the case for the [projective plane](#projective-plane). You cannot instantly go to any other point on the $z=0$ by just moving a little bit, you have to walk around that circle.

<a id="image-spherical-cap-model-of-the-real-projective-plane"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/spherical-cap-model-of-the-real-projective-plane.svg)

**[Figure 1](#image-spherical-cap-model-of-the-real-projective-plane). Spherical cap model of the real projective plane**. On the x-y plane, you can magically travel immediately between [antipodal points](#antipodal-point) such as A/A', B/B' and C/C'. Or equivalently, those pairs are the same point. Every other point outside the x-y plane is just a regular point like a normal [sphere](#sphere).

##### The real projective plane is not simply connected

↑ **Parent:** [Real projective plane](#real-projective-plane)

To see that the [real projective plane](#real-projective-plane) is not [simply connected space](calculus.md#simply-connected-space), considering the [lines through origin model of the real projective plane](#lines-through-origin-model-of-the-real-projective-plane), take a [loop](calculus.md#loop-topology) that starts at $(1, 0, 0)$ and moves along the $y=0$ [great circle](#great-circle) ends at $(-1, 0, 0)$.

Note that both of those points are the same, so we have a loop.

Now try to shrink it to a point.

There's just no way!

##### Point at infinity

↑ **Parent:** [Real projective plane](#real-projective-plane)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Point_at_infinity)

##### Homogenous coordinates

↑ **Parent:** [Real projective plane](#real-projective-plane)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Homogenous_coordinates)

## Polytope

↑ **Parent:** [Geometry](geometry.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Polytope)

A [polygon](#polygon) is a 2-dimensional [polytope](#polytope), [polyhedra](#polyhedron) is a 3-dimensional [polytope](#polytope). 

### Convex polytope

↑ **Parent:** [Polytope](#polytope)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Convex_polytope)

### Regular polytope

↑ **Parent:** [Polytope](#polytope)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Regular_polytope)

TODO understand and explain definition.

#### Classification of regular polytopes

↑ **Parent:** [Regular polytope](#regular-polytope)  
🏷️ **Tags:** [Classification (mathematics)](mathematics.md#classification-mathematics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Regular_polytope#Classification_and_description)

The 3D regular convex polyhedrons are super famous, have the name: [Platonic solid](#platonic-solid), and have been known since antiquity. In particular, there are only 5 of them.

The counts per dimension are:<a id="table-number-of-regular-polytopes-per-dimension"></a>


| Dimension | Count |
| --- | --- |
| 2 | Infinite |
| 3 | 5 |
| 4 | 6 |
| \>4 | 3 |

The cool thing is that the 3 that exist in 5+ dimensions are all of one of the three families:
- [simplex](#simplex)
- [hypercube](#hypercube)
- [cross polytope](#cross-polytope)
Then, the 2 3D missing ones have 4D analogues and the sixth one in 4D does not have a 3D analogue: [the 24-cell](https://en.wikipedia.org/wiki/24-cell). Yes, this is the kind of irregular stuff [Ciro Santilli](ciro-santilli.md) lives [for](mathematics.md#the-beauty-of-mathematics).

##### Simplex

↑ **Parent:** [Classification of regular polytopes](#classification-of-regular-polytopes)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Simplex)

[Triangle](#triangle), [tetrahedron](#tetrahedron).

The name does not imply regular by default. For regular ones, you should say "regular polytope".

Non-regular description: take convex hull take D + 1 vertices that are not on a single D-plan.

##### Hypercube

↑ **Parent:** [Classification of regular polytopes](#classification-of-regular-polytopes)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Hypercube)

[square](#square), cube. 4D case known as [tesseract](#tesseract).

Convex hull of all $\{-1, 1\}^D$ ([Cartesian product](formalization-of-mathematics.md#cartesian-product) power) D-tuples, e.g. in [3D](calculus.md#real-coordinate-space-of-dimension-three):
```
( 1,  1,  1)
( 1,  1, -1)
( 1, -1,  1)
( 1, -1, -1)
(-1,  1,  1)
(-1,  1, -1)
(-1, -1,  1)
(-1, -1, -1)
```

From this we see that there are $2^D$ [vertices](mathematics.md#vertex).

Two [vertices](mathematics.md#vertex) are linked iff they differ by a single number. So each vertex has D neighbors.

###### Hyperrectangle

↑ **Parent:** [Hypercube](#hypercube)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Hyperrectangle)

The [non-regular](#regular-polytope) version of the [hypercube](#hypercube).

##### Cross polytope

↑ **Parent:** [Classification of regular polytopes](#classification-of-regular-polytopes)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Cross_polytope)

Examples: [square](#square), [octahedron](#octahedron).

Take $(0, 0, 0, \dots, 0)$ and flip one of 0's to $\pm 1$. Therefore has $2 \times D$ [vertices](mathematics.md#vertex).

Each edge E is linked to every other edge, except it's opposite -E.

### Polygon

↑ **Parent:** [Polytope](#polytope)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Polygon)

#### Quadrilateral

↑ **Parent:** [Polygon](#polygon)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Quadrilateral)

##### Rectangle

↑ **Parent:** [Quadrilateral](#quadrilateral)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Rectangle)

#### Parallelogram

↑ **Parent:** [Polygon](#polygon)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Parallelogram)

##### Parallelepiped

↑ **Parent:** [Parallelogram](#parallelogram)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Parallelepiped)

[3D](calculus.md#real-coordinate-space-of-dimension-three) [parallelogram](#parallelogram).

###### Volume of the parallelepiped

↑ **Parent:** [Parallelepiped](#parallelepiped)

#### Regular polygon

↑ **Parent:** [Polygon](#polygon)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Regular_polygon)

##### Regular convex polygon

↑ **Parent:** [Regular polygon](#regular-polygon)

###### Triangle

↑ **Parent:** [Regular convex polygon](#regular-convex-polygon)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Triangle)

###### Square

↑ **Parent:** [Regular convex polygon](#regular-convex-polygon)  
🏷️ **Tags:** [Rectangle](#rectangle)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Square)

###### Pentagon

↑ **Parent:** [Regular convex polygon](#regular-convex-polygon)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Pentagon)

###### Hexagon

↑ **Parent:** [Regular convex polygon](#regular-convex-polygon)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Hexagon)

###### Octagon

↑ **Parent:** [Regular convex polygon](#regular-convex-polygon)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Octagon)

### Polyhedron

↑ **Parent:** [Polytope](#polytope)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Polyhedron)

#### Tetrahedron

↑ **Parent:** [Polyhedron](#polyhedron)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Tetrahedron)

#### Octahedron

↑ **Parent:** [Polyhedron](#polyhedron)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Octahedron)

### Regular polyhedron

↑ **Parent:** [Polytope](#polytope)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Regular_polyhedron)

#### Platonic solid

↑ **Parent:** [Regular polyhedron](#regular-polyhedron)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Platonic_solid)

A [convex](#convex-polytope) [regular polyhedron](#regular-polyhedron).

Their [beauty is a classification type result](mathematics.md#the-beauty-of-mathematics) as stated at [classification of regular polytopes](#classification-of-regular-polytopes).

[https://en.wikipedia.org/wiki/Platonic_solid#Topological_proof](https://en.wikipedia.org/wiki/Platonic_solid#Topological_proof)

### 4-polytope

↑ **Parent:** [Polytope](#polytope)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/4-polytope)

#### Regular 4-polytope

↑ **Parent:** [4-polytope](#4-polytope)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Regular_4-polytope)

##### Tesseract

↑ **Parent:** [Regular 4-polytope](#regular-4-polytope)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Tesseract)

## Differential geometry

↑ **Parent:** [Geometry](geometry.md)

Bibliography:
- [https://maths-people.anu.edu.au/~andrews/DG/](https://maths-people.anu.edu.au/~andrews/DG/) Lectures on Differential Geometry by Ben Andrews

### Lie group

↑ **Parent:** [Differential geometry](#differential-geometry)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Lie_group)

The key and central motivation for studying Lie groups and their [Lie algebras](#lie-algebra) appears to be to characterize [symmetry](group.md#symmetry) in [Lagrangian mechanics](mechanics.md#lagrangian-mechanics) through [Noether's theorem](mechanics.md#noether-s-theorem), just start from there.

Notably [local symmetries](#local-symmetry) appear to map to forces, and local means "around the identity", notably: [local symmetries of the Lagrangian imply conserved currents](#local-symmetries-of-the-lagrangian-imply-conserved-currents).

More precisely: [local symmetries of the Lagrangian imply conserved currents](#local-symmetries-of-the-lagrangian-imply-conserved-currents).

TODO [Ciro Santilli](ciro-santilli.md) really wants to understand what all the fuss is about:
- [https://math.stackexchange.com/questions/1322206/lie-groups-lie-algebra-applications](https://math.stackexchange.com/questions/1322206/lie-groups-lie-algebra-applications)
- [https://mathoverflow.net/questions/58696/why-study-lie-algebras](https://mathoverflow.net/questions/58696/why-study-lie-algebras)
- [https://math.stackexchange.com/questions/405406/definition-of-lie-algebra](https://math.stackexchange.com/questions/405406/definition-of-lie-algebra)

Oh, there is a low dimensional classification! Ciro is [a sucker for classification theorems](mathematics.md#high-flying-bird-vs-gophers)! [https://en.wikipedia.org/wiki/Classification_of_low-dimensional_real_Lie_algebras](https://en.wikipedia.org/wiki/Classification_of_low-dimensional_real_Lie_algebras)

The fact that there are elements arbitrarily close to the identity, which is only possible due to the group being continuous, is the key factor that simplifies the treatment of Lie groups, and follows the philosophy of [continuous problems are simpler than discrete ones](calculus.md#continuous-problems-are-simpler-than-discrete-ones).

Bibliography:
- [https://youtu.be/kpeP3ioiHcw?t=2655](https://youtu.be/kpeP3ioiHcw?t=2655) "Particle Physics Topic 6: Lie Groups and Lie Algebras" by Alex Flournoy (2016). Good [SO(3)](#special-orthogonal-group) explicit exponential expansion example. Then next lecture shows why SU(2) is the representation of SO(3). Next ones appear to eventually get to the physical usefulness of the thing, but I lost patience. Not too far out though.
- [https://www.youtube.com/playlist?list=PLRlVmXqzHjURZO0fviJuyikvKlGS6rXrb](https://www.youtube.com/playlist?list=PLRlVmXqzHjURZO0fviJuyikvKlGS6rXrb) "Lie Groups and Lie Algebras" playlist by XylyXylyX (2018). Tutorial with infinitely many hours
- [http://www.staff.science.uu.nl/~hooft101/lectures/lieg07.pdf](http://www.staff.science.uu.nl/~hooft101/lectures/lieg07.pdf)
- [http://www.physics.drexel.edu/~bob/LieGroups.html](http://www.physics.drexel.edu/~bob/LieGroups.html)

<a id="video-what-is-lie-theory-by-mathemaniac-2023"></a>
**[Video 1](#video-what-is-lie-theory-by-mathemaniac-2023). What is Lie theory? by Mathemaniac 2023.** [Source](https://www.youtube.com/watch?v=ZRca3Ggpy_g).

#### Lie derivative

↑ **Parent:** [Lie group](#lie-group)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Lie_derivative)

Bibliography:
- [https://takeshimg92.github.io/posts/lie_derivatives.html](https://takeshimg92.github.io/posts/lie_derivatives.html)

#### Applications of Lie groups to differential equations

↑ **Parent:** [Lie group](#lie-group)  
🏷️ **Tags:** [Analytical method to solve a partial differential equation](calculus.md#analytical-method-to-solve-a-partial-differential-equation)

Solving [differential equations](calculus.md#differential-equation) was apparently Lie's original motivation for developing [Lie groups](#lie-group). It is therefore likely one of the most understandable ways to approach it.

It appears that Lie's goal was to understand when can a differential equation have an explicitly written solution, much like [Galois theory](formalization-of-mathematics.md#galois-theory) had done for [algebraic equations](formalization-of-mathematics.md#algebraic-equation). Both approaches use [symmetry](group.md#symmetry) as the key tool.

- [https://www.researchgate.net/profile/Michael_Frewer/publication/269465435_Lie-Groups_as_a_Tool_for_Solving_Differential_Equations/links/548cbf250cf214269f20e267/Lie-Groups-as-a-Tool-for-Solving-Differential-Equations.pdf](https://www.researchgate.net/profile/Michael_Frewer/publication/269465435_Lie-Groups_as_a_Tool_for_Solving_Differential_Equations/links/548cbf250cf214269f20e267/Lie-Groups-as-a-Tool-for-Solving-Differential-Equations.pdf) Lie-Groups as a Tool for Solving Differential Equations by Michael Frewer. Slides with good examples.

#### Lie algebra

↑ **Parent:** [Lie group](#lie-group)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Lie_algebra)

Like everything else in [Lie groups](#lie-group), first start with the [matrix](linear-algebra.md#matrix) as discussed at [Section "Lie algebra of a matrix Lie group"](#lie-algebra-of-a-matrix-lie-group).

Intuitively, a [Lie algebra](#lie-algebra) is a simpler object than a [Lie group](#lie-group). Without any extra structure, groups can be very complicated non-linear objects. But a [Lie algebra](#lie-algebra) is just an [algebra over a field](group.md#algebra-over-a-field), and one with a restricted [bilinear map](linear-algebra.md#bilinear-map) called the [Lie bracket](#lie-bracket), that has to also be [alternating](linear-algebra.md#alternating-multilinear-map) and satisfy the [Jacobi identity](linear-algebra.md#jacobi-identity).

Another important way to think about Lie algebras, is as [infinitesimal generators](#infinitesimal-generator).

Because of the [Lie group-Lie algebra correspondence](#lie-group-lie-algebra-correspondence), we know that there is almost a [bijection](formalization-of-mathematics.md#bijection) between each [Lie group](#lie-group) and the corresponding [Lie algebra](#lie-algebra). So it makes sense to try and study the algebra instead of the group itself whenever possible, to try and get insight and proofs in that simpler framework. This is the key reason why people study Lie algebras. One is philosophically reminded of how [normal subgroups](group.md#normal-subgroup) are a simpler representation of [group homomorphisms](group.md#group-homomorphism).

To make things even simpler, because [all vector spaces of the same dimension on a given field are isomorphic](linear-algebra.md#classification-of-vector-spaces), the only things we need to specify a [Lie group](#lie-group) through a [Lie algebra](#lie-algebra) are:
- the dimension
- the [Lie bracket](#lie-bracket)
Note that the [Lie bracket](#lie-bracket) can look different under different basis of the [Lie algebra](#lie-algebra) however. This is shown for example at [Physics from Symmetry by Jakob Schwichtenberg (2015)](physicist.md#physics-from-symmetry-by-jakob-schwichtenberg-2015) page 71 for the [Lorentz group](#lorentz-group).

As mentioned at [Lie Groups, Physics, and Geometry by Robert Gilmore (2008)](#lie-groups-physics-and-geometry-by-robert-gilmore-2008) Chapter 4 "Lie Algebras", taking the [Lie algebra](#lie-algebra) around the identity is mostly a convention, we could treat any other point, and things are more or less equivalent.

Bibliography:
- [https://physicstravelguide.com/advanced_tools/group_theory/lie_algebras#tab__concrete](https://physicstravelguide.com/advanced_tools/group_theory/lie_algebras#tab__concrete) on [Physics Travel Guide](physicist.md#physics-travel-guide)
- [http://jakobschwichtenberg.com/lie-algebra-able-describe-group/](http://jakobschwichtenberg.com/lie-algebra-able-describe-group/) by [Jakob Schwichtenberg](physicist.md#jakob-schwichtenberg)

##### Infinitesimal generator

↑ **Parent:** [Lie algebra](#lie-algebra)

Elements of a [Lie algebra](#lie-algebra) can (should!) be seen a continuous analogue to the [generating set of a group](group.md#generating-set-of-a-group) in finite groups.

For continuous groups however, we can't have a finite generating set in the strict sense, as a finite set won't ever cover every possible point.

But the [generator of a Lie algebra](#generator-of-a-lie-algebra) can be finite.

And just like in finite groups, where you can specify the full group by specifying only the relationships between generating elements, in the Lie algebra you can almost specify the full group by specifying the relationships between the elements of a [generator of the Lie algebra](#generators-of-a-lie-algebra).

This "specification of a relation" is done by defining the [Lie bracket](#lie-bracket).

The reason why the algebra works out well for continuous stuff is that by definition an [algebra over a field](group.md#algebra-over-a-field) is a [vector space](linear-algebra.md#vector-space) with some extra structure, and we know very well how to make infinitesimal elements in a vector space: just multiply its vectors by a constant $c$ that cana be arbitrarily small.

##### Lie group-Lie algebra correspondence

↑ **Parent:** [Lie algebra](#lie-algebra)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Lie_group–Lie_algebra_correspondence)

Every [Lie algebra](#lie-algebra) corresponds to a single [simply connected](calculus.md#simply-connected-space) [Lie group](#lie-group).

The [Baker-Campbell-Hausdorff formula](#baker-campbell-hausdorff-formula) basically defines how to map an algebra to the group.

Bibliography:
- [Lie Groups, Physics, and Geometry by Robert Gilmore (2008)](#lie-groups-physics-and-geometry-by-robert-gilmore-2008) Chapter 7 "EXPonentiation"

###### Lie algebra exponential covering problem

↑ **Parent:** [Lie group-Lie algebra correspondence](#lie-group-lie-algebra-correspondence)

[Lie Groups, Physics, and Geometry by Robert Gilmore (2008)](#lie-groups-physics-and-geometry-by-robert-gilmore-2008) 7.2 "The covering problem" gives some amazing intuition on the subject as usual.

###### A single exponential map is not enough to recover a simple Lie group from its algebra

↑ **Parent:** [Lie algebra exponential covering problem](#lie-algebra-exponential-covering-problem)

Example at: [Lie Groups, Physics, and Geometry by Robert Gilmore (2008)](#lie-groups-physics-and-geometry-by-robert-gilmore-2008) Chapter 7 "EXPonentiation".

###### The product of a exponential of the compact algebra with that of the non-compact algebra recovers a simple Lie from its algebra

↑ **Parent:** [Lie algebra exponential covering problem](#lie-algebra-exponential-covering-problem)

Example at: [Lie Groups, Physics, and Geometry by Robert Gilmore (2008)](#lie-groups-physics-and-geometry-by-robert-gilmore-2008) Chapter 7 "EXPonentiation".

Furthermore, the non-[compact](calculus.md#compact-space) part is always [isomorphic](group.md#isomorphism) to [$\R^n$](calculus.md#real-coordinate-space), only the non-compact part can have more interesting structure.

###### Two different Lie groups can have the same Lie algebra

↑ **Parent:** [Lie group-Lie algebra correspondence](#lie-group-lie-algebra-correspondence)

The most important example is perhaps [$SO(3)$](#3d-rotation-group) and [$SU(2)$](#special-unitary-of-degree-2), both of which have the same [Lie algebra](#lie-algebra), but are not isomorphic.

###### Every Lie algebra has a unique single corresponding simply connected Lie group

↑ **Parent:** [Two different Lie groups can have the same Lie algebra](#two-different-lie-groups-can-have-the-same-lie-algebra)

This [simply connected](calculus.md#simply-connected-space) is called the [universal covering group](#universal-covering-group).

E.g. in the case of [$SO(3)$](#3d-rotation-group) and [$SU(2)$](#special-unitary-of-degree-2), [$SU(2)$](#special-unitary-of-degree-2) is [simply connected](calculus.md#simply-connected-space), but [$SO(3)$](#3d-rotation-group) is not.

###### Universal covering group

↑ **Parent:** [Every Lie algebra has a unique single corresponding simply connected Lie group](#every-lie-algebra-has-a-unique-single-corresponding-simply-connected-lie-group)

The [unique](formalization-of-mathematics.md#uniqueness) group referred to at: [every Lie algebra has a unique single corresponding simply connected Lie group](#every-lie-algebra-has-a-unique-single-corresponding-simply-connected-lie-group).

###### Every Lie group that has a given Lie algebra is the image of an homomorphism from the universal cover group

↑ **Parent:** [Two different Lie groups can have the same Lie algebra](#two-different-lie-groups-can-have-the-same-lie-algebra)

##### Lie bracket

↑ **Parent:** [Lie algebra](#lie-algebra)

##### Exponential map

↑ **Parent:** [Lie algebra](#lie-algebra)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Exponential_map)

Most commonly refers to: [exponential map](#exponential-map-lie-theory).

###### Exponential map (Lie theory)

↑ **Parent:** [Exponential map](#exponential-map)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Exponential_map_(Lie_theory))

Like everything else in [Lie group](#lie-group) theory, you should first look at the [matrix](linear-algebra.md#matrix) version of this operation: the [matrix exponential](formalization-of-mathematics.md#matrix-exponential).

The [exponential map](#exponential-map) links small transformations around the origin (infinitely small) back to larger finite transformations, and small transformations around the origin are something we can deal with a [Lie algebra](#lie-algebra), so this map links the two worlds.

The idea is that we can decompose a finite transformation into infinitely arbitrarily small around the origin, and proceed just like the [product definition of the exponential function](formalization-of-mathematics.md#product-definition-of-the-exponential-function).

The definition of the exponential map is simply the same as that of the regular exponential function as given at [Taylor expansion definition of the exponential function](formalization-of-mathematics.md#taylor-expansion-definition-of-the-exponential-function), except that the argument $x$ can now be an operator instead of just a number.

Examples:
- [the derivative is the generator of the translation group](#the-derivative-is-the-generator-of-the-translation-group)

##### Baker-Campbell-Hausdorff formula

↑ **Parent:** [Lie algebra](#lie-algebra)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Baker–Campbell–Hausdorff formula)

Solution $Z$ for given $X$ and $Y$ of:

$$
e^Z = e^X e^Y
$$

where $e$ is the [exponential map](#exponential-map).

If we consider just [real number](formalization-of-mathematics.md#real-number), $Z = X + Y$, but when X and Y are [non-commutative](group.md#non-commutative), things are not so simple.

Furthermore, TODO confirm it is possible that a solution does not exist at all if $X$ and $Y$ aren't sufficiently small.

This formula is likely the basis for the [Lie group-Lie algebra correspondence](#lie-group-lie-algebra-correspondence). With it, we express the actual [group operation](group.md#group-operation) in terms of the Lie algebra operations.

Notably, remember that a [algebra over a field](group.md#algebra-over-a-field) is just a [vector space](linear-algebra.md#vector-space) with one extra product operation defined.

Vector spaces are simple because [all vector spaces of the same dimension on a given field are isomorphic](linear-algebra.md#classification-of-vector-spaces), so besides the dimension, once we define a [Lie bracket](#lie-bracket), we also define the corresponding [Lie group](#lie-group).

Since a group is basically defined by what the group operation does to two arbitrary elements, once we have that defined via the [Baker-Campbell-Hausdorff formula](#baker-campbell-hausdorff-formula), we are basically done defining the group in terms of the algebra.

##### Generator of a Lie algebra

↑ **Parent:** [Lie algebra](#lie-algebra)

##### Generators of a Lie algebra

↑ **Parent:** [Lie algebra](#lie-algebra)

Cardinality $\leq$ dimension of the vector space.

#### Continuous symmetry

↑ **Parent:** [Lie group](#lie-group)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Continuous_symmetry)

Basically a synonym for [Lie group](#lie-group) which is the way of modelling them.

##### Local symmetry

↑ **Parent:** [Continuous symmetry](#continuous-symmetry)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Local_symmetry)

Local symmetries appear to be a synonym to [internal symmetry](quantum-field-theory.md#internal-symmetry), see description at: [Section "Internal and spacetime symmetries"](quantum-field-theory.md#internal-and-spacetime-symmetries).

As mentioned at [Quote ](standard-model.md#quote-axelmaas-local-symmetry), local symmetries map to forces in the [Standard Model](standard-model.md).

Appears to be a synonym for: [gauge symmetry](quantum-field-theory.md#gauge-symmetry).

A local symmetry is a transformation that you apply a different transformation for each point, instead of a single transformation for every point.

TODO what's the point of a local symmetry?

Bibliography:
- [lecture 3](quantum-field-theory.md#quantum-field-theory-lecture-by-tobias-osborne-2017/lecture-3)
- [https://physics.stackexchange.com/questions/48188/local-and-global-symmetries](https://physics.stackexchange.com/questions/48188/local-and-global-symmetries)
- [https://www.physics.rutgers.edu/grad/618/lects/localsym.pdf](https://www.physics.rutgers.edu/grad/618/lects/localsym.pdf) by Joel Shapiro gives one nice high level intuitive idea:> In relativistic physics, global objects are awkward because the finite velocity with which effects can propagate is expressed naturally in terms of local objects. For this reason high energy physics is expressed in terms of a field theory.
- [Quora](website.md#quora):
  - [https://www.quora.com/What-does-a-local-symmetry-mean-in-physics](https://www.quora.com/What-does-a-local-symmetry-mean-in-physics)
  - [https://www.quora.com/What-is-the-difference-between-local-and-global-symmetries-in-physics](https://www.quora.com/What-is-the-difference-between-local-and-global-symmetries-in-physics)
  - [https://www.quora.com/What-is-the-difference-between-global-and-local-gauge-symmetry](https://www.quora.com/What-is-the-difference-between-global-and-local-gauge-symmetry)

###### Local symmetries of the Lagrangian imply conserved currents

↑ **Parent:** [Local symmetry](#local-symmetry)

TODO. I think this is the key point. Notably, [$U(1)$](#unitary-group-of-degree-1) symmetry implies [charge conservation](electromagnetism.md#charge-conservation).

More precisely, each [generator of the corresponding Lie algebra](#generator-of-a-lie-algebra) leads to one separate conserved current, such that a single symmetry can lead to multiple conserved currents.

This is basically the [local symmetry](#local-symmetry) version of [Noether's theorem](mechanics.md#noether-s-theorem).

Then to maintain charge conservation, we have to maintain [local symmetry](#local-symmetry), which in turn means we have to add a [gauge field](quantum-field-theory.md#gauge-field) as shown at [Video "Deriving the qED Lagrangian by Dietterich Labs (2018)"](quantum-field-theory.md#video-deriving-the-qed-lagrangian-by-dietterich-labs-2018).

Forces can then be seen as kind of a side effect of this.

Bibliography:
- [https://photonics101.com/relativistic-electrodynamics/gauge-invariance-action-charge-conservation#show-solution](https://photonics101.com/relativistic-electrodynamics/gauge-invariance-action-charge-conservation#show-solution) has a good explanation of the Gauge transformation. TODO how does that relate to [$U(1)$](#unitary-group-of-degree-1) symmetry?
- [https://physics.stackexchange.com/questions/57901/noether-theorem-gauge-symmetry-and-conservation-of-charge](https://physics.stackexchange.com/questions/57901/noether-theorem-gauge-symmetry-and-conservation-of-charge)

#### Important Lie group

↑ **Parent:** [Lie group](#lie-group)

##### Matrix Lie group

↑ **Parent:** [Important Lie group](#important-lie-group)

This important and common simple case has easy properties.

<h6 id="every-closed-subgroup-of-gl-n-c-is-a-lie-group">Every closed subgroup of <span class="katex"><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:1em;vertical-align:-0.25em;"></span><span class="mord mathnormal">G</span><span class="mord mathnormal">L</span><span class="mopen">(</span><span class="mord mathnormal">n</span><span class="mpunct">,</span><span class="mspace" style="margin-right:0.1667em;"></span><span class="mord mathbb">C</span><span class="mclose">)</span></span></span></span> is a Lie group</h6>

↑ **Parent:** [Matrix Lie group](#matrix-lie-group)

[S](linguistics.md#s) page 146.

###### Lie algebra of a matrix Lie group

↑ **Parent:** [Matrix Lie group](#matrix-lie-group)

For this sub-case, we can define the [Lie algebra](#lie-algebra) of a Lie group $G$ as the set of all matrices $M \in G$ such that for all $t \in \R$:

$$
e^{tM} \in G
$$

If we fix a given $M$ and vary $t$, we obtain a [subgroup](group.md#subgroup) of $G$. This type of subgroup is known as a [one parameter subgroup](#one-parameter-subgroup).

The immediate question is then if every element of $G$ can be reached in a unique way (i.e. is the exponential map a [bijection](formalization-of-mathematics.md#bijection)). By looking at the [matrix logarithm](formalization-of-mathematics.md#logarithm-of-a-matrix) however we conclude that this is not the case for [real](formalization-of-mathematics.md#real-number) matrices, but it is for [complex](formalization-of-mathematics.md#complex-number) matrices.

Examples:
- [Lie algebra of $GL(n)$](#lie-algebra-of-gl-n)
- [Lie algebra of $SL(2)$](#lie-algebra-of-sl-2)
- [Lie algebra of $SO(3)$](#lie-algebra-of-so-3)
- [Lie algebra of $SU(2)$](#lie-algebra-of-su-2)

TODO example it can be seen that the Lie algebra is not closed [matrix multiplication](linear-algebra.md#matrix-multiplication), even though the corresponding group is by definition. But it is closed under the [Lie bracket](#lie-bracket) operation.

###### Lie bracket of a matrix Lie group

↑ **Parent:** [Lie algebra of a matrix Lie group](#lie-algebra-of-a-matrix-lie-group)

$$
[X, Y] = XY - YX
$$

This makes it clear how the [Lie bracket](#lie-bracket) can be seen as a "measure of non-[commutativity](group.md#commutative-property)"

Because the [Lie bracket](#lie-bracket) has to be a bilinear map, all we need to do to specify it uniquely is to specify how it acts on every pair of some basis of the [Lie algebra](#lie-algebra).

Then, together with the [Baker-Campbell-Hausdorff formula](#baker-campbell-hausdorff-formula) and the [Lie group-Lie algebra correspondence](#lie-group-lie-algebra-correspondence), this forms an exceptionally compact description of a [Lie group](#lie-group).

###### One parameter subgroup

↑ **Parent:** [Lie algebra of a matrix Lie group](#lie-algebra-of-a-matrix-lie-group)

The one parameter subgroup of a [Lie group](#lie-group) for a given element $M$ of its [Lie algebra](#lie-algebra) is a [subgroup](group.md#subgroup) of $G$ given by:

$$
{ e^{tM} \in G | t \in \R }
$$

Intuitively, $M$ is a direction, and $t$ is how far we move along a given direction. This intuition is especially vivid in for example in the case of the [Lie algebra of $SO(3)$](#lie-algebra-of-so-3), the [rotation group](#special-orthogonal-group).

One parameter subgroups can be seen as the continuous analogue to the [cycle of an element of a group](group.md#cycle-of-an-element-of-a-group).

##### Classical group

↑ **Parent:** [Important Lie group](#important-lie-group)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Classical_group)

###### Symplectic group

↑ **Parent:** [Classical group](#classical-group)

Intuition, please? Example? [https://mathoverflow.net/questions/278641/intuition-for-symplectic-groups](https://mathoverflow.net/questions/278641/intuition-for-symplectic-groups) The key motivation seems to be related to [Hamiltonian mechanics](mechanics.md#hamiltonian-mechanics). The two arguments of the [bilinear form](linear-algebra.md#bilinear-form) correspond to each set of variables in Hamiltonian mechanics: the generalized positions and generalized momentums, which appear in the same number each.

Seems to be set of matrices that preserve a [skew-symmetric bilinear form](linear-algebra.md#skew-symmetric-bilinear-form), which is comparable to the [orthogonal group](#orthogonal-group), which preserves a [symmetric bilinear form](linear-algebra.md#symmetric-bilinear-form). More precisely, the orthogonal group has:

$$
O^T I O = I
$$

and its generalization the [indefinite orthogonal group](#indefinite-orthogonal-group) has:

$$
O^T S O = I
$$

where S is symmetric. So for the symplectic group we have matrices Y such as:

$$
Y^T A Y = I
$$

where A is antisymmetric. This is explained at: [https://www.ucl.ac.uk/~ucahad0/7302_handout_13.pdf](https://www.ucl.ac.uk/~ucahad0/7302_handout_13.pdf) They also explain there that unlike as in the analogous [orthogonal group](#orthogonal-group), that definition ends up excluding determinant -1 automatically.

Therefore, just like the [special orthogonal group](#special-orthogonal-group), the symplectic group is also a [subgroup](group.md#subgroup) of the [special linear group](#special-linear-group).

###### Symplectic matrix

↑ **Parent:** [Symplectic group](#symplectic-group)  
🏷️ **Tags:** [Named matrix](linear-algebra.md#named-matrix)

###### Unitary symplectic group

↑ **Parent:** [Symplectic group](#symplectic-group)

##### General linear group

↑ **Parent:** [Important Lie group](#important-lie-group)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/General_linear_group)

Invertible matrices. Or if you think a bit more generally, an invertible [linear map](linear-algebra.md#linear-map).

When the [field](group.md#field-mathematics) $F$ is not given, it defaults to the [real numbers](formalization-of-mathematics.md#real-number).

Non-invertible are excluded "because" otherwise it would not form a [group](group.md) (every element must have an inverse). This is therefore the largest possible group under [matrix multiplication](linear-algebra.md#matrix-multiplication), other matrix multiplication groups being subgroups of it.

###### Finite general linear group

↑ **Parent:** [General linear group](#general-linear-group)

[general linear group](#general-linear-group) over a [finite field](group.md#finite-field) of order $m$. Remember that due to the [classification of finite fields](group.md#classification-of-finite-fields), there is one single field for each [prime power](mathematics.md#prime-power) $m$.

Exactly as over the [real numbers](formalization-of-mathematics.md#real-number), you just put the finite field elements into a $n \times n$ matrix, and then take the invertible ones.

<h5 id="lie-algebra-of-gl-n">Lie algebra of <span class="katex"><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:1em;vertical-align:-0.25em;"></span><span class="mord mathnormal">G</span><span class="mord mathnormal">L</span><span class="mopen">(</span><span class="mord mathnormal">n</span><span class="mclose">)</span></span></span></span></h5>

↑ **Parent:** [Important Lie group](#important-lie-group)  
🏷️ **Tags:** [Lie algebra of a matrix Lie group](#lie-algebra-of-a-matrix-lie-group)

Is the [set of all n-by-y square matrices](linear-algebra.md#matrix-ring).

Because [$GL(n)$](#general-linear-group) is a [Lie group](#lie-group) we can use [Section "Lie algebra of a matrix Lie group"](#lie-algebra-of-a-matrix-lie-group).

For every matrix $x$ in the [set of all n-by-y square matrices](linear-algebra.md#matrix-ring) $M_n$, $e^x$ has inverse $e^-x$.

Note that this works even if $x$ is not [invertible](algebra.md#invertible), and therefore not in [$GL(n)$](#general-linear-group)!

Therefore, the Lie algebra of [$GL(n)$](#general-linear-group) is the entire [$M_n$](linear-algebra.md#matrix-ring).

##### Special linear group

↑ **Parent:** [Important Lie group](#important-lie-group)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Special_linear_group)

Specials sub case of the [general linear group](#general-linear-group) when the determinant equals exactly 1.

###### Special linear group of dimension 2

↑ **Parent:** [Special linear group](#special-linear-group)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/SL2(R))

<h6 id="lie-algebra-of-sl-n">Lie algebra of <span class="katex"><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:1em;vertical-align:-0.25em;"></span><span class="mord mathnormal" style="margin-right:0.05764em;">S</span><span class="mord mathnormal">L</span><span class="mopen">(</span><span class="mord mathnormal">n</span><span class="mclose">)</span></span></span></span></h6>

↑ **Parent:** [Special linear group](#special-linear-group)  
🏷️ **Tags:** [Lie algebra of a matrix Lie group](#lie-algebra-of-a-matrix-lie-group)

<h6 id="lie-algebra-of-sl-2">Lie algebra of <span class="katex"><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:1em;vertical-align:-0.25em;"></span><span class="mord mathnormal" style="margin-right:0.05764em;">S</span><span class="mord mathnormal">L</span><span class="mopen">(</span><span class="mord">2</span><span class="mclose">)</span></span></span></span></h6>

↑ **Parent:** [Lie algebra of $SL(n)$](#lie-algebra-of-sl-n)

This is a good first concrete example of a Lie algebra. Shown at [Lie Groups, Physics, and Geometry by Robert Gilmore (2008)](#lie-groups-physics-and-geometry-by-robert-gilmore-2008) Chapter 4.2 "How to linearize a Lie Group" has an example.

We can use use the following parametrization of the [special linear group](#special-linear-group) on variables $x$, $y$ and $z$:

$$
M =
\begin{bmatrix}
1 + x & y \\
z & (1 + yz)/(1 + x) \\
\end{bmatrix}
$$

Every element with this parametrization has [determinant](linear-algebra.md#determinant) 1:

$$
det(M) = (1 + x)(1 + yz)/(1 + x) - yz = 1
$$

Furthermore, any element can be reached, because by independently settting $x$, $y$ and $z$, $M_{00}$, $M_{01}$ and $M_{10}$ can have any value, and once those three are set, $M_{11}$ is fixed by the determinant.

To find the elements of the [Lie algebra](#lie-algebra), we evaluate the derivative on each parameter at 0:

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

Remembering that the [Lie bracket of a matrix Lie group](#lie-bracket-of-a-matrix-lie-group) is really simple, we can then observe the following [Lie bracket](#lie-bracket) relations between them:

$$
\begin{aligned}
[M_x, M_y] &= M_xM_y - M_yM_x &= \begin{bmatrix}0 & 1 \\  0 & 0 \\\end{bmatrix} &- \begin{bmatrix}0 & -1 \\ 0 & 0 \\\end{bmatrix} &= \begin{bmatrix}0 & 2 \\  0 &  0 \\\end{bmatrix} &=  2M_y\\
[M_x, M_z] &= M_xM_z - M_zM_x &= \begin{bmatrix}0 & 0 \\ -1 & 0 \\\end{bmatrix} &- \begin{bmatrix}0 &  0 \\ 1 & 0 \\\end{bmatrix} &= \begin{bmatrix}0 & 0 \\ -2 &  0 \\\end{bmatrix} &= -2M_z\\
[M_y, M_z] &= M_yM_z - M_zM_y &= \begin{bmatrix}1 & 0 \\  0 & 0 \\\end{bmatrix} &- \begin{bmatrix}0 &  0 \\ 0 & 1 \\\end{bmatrix} &= \begin{bmatrix}1 & 0 \\  0 & -1 \\\end{bmatrix} &=   M_x\\
\end{aligned}
$$

One key thing to note is that the specific matrices $M_x$, $M_y$ and $M_z$ are not really fundamental: we could easily have had different matrices if we had chosen any other parametrization of the group.

TODO confirm: however, no matter which parametrization we choose, the [Lie bracket](#lie-bracket) relations between the three elements would always be the same, since it is the number of elements, and the definition of the [Lie bracket](#lie-bracket), that is truly fundamental.

[Lie Groups, Physics, and Geometry by Robert Gilmore (2008)](#lie-groups-physics-and-geometry-by-robert-gilmore-2008) Chapter 4.2 "How to linearize a Lie Group" then calculates the [exponential map](#exponential-map) of the vector $xM_x + yM_y + zM_z$ as:

$$
I cosh(\theta) + M_x sinh(\theta)/\theta
$$

with:

$$
\theta^2 = x^2 + bc
$$

TODO now the natural question is: can we cover the entire Lie group with this exponential? [Lie Groups, Physics, and Geometry by Robert Gilmore (2008)](#lie-groups-physics-and-geometry-by-robert-gilmore-2008) Chapter 7 "EXPonentiation" explains why not.

###### Finite special general linear group

↑ **Parent:** [Special linear group](#special-linear-group)

Just like for the [finite general linear group](#finite-general-linear-group), the definition of special also works for finite fields, where 1 is the multiplicative identity!

Note that the definition of [orthogonal group](#orthogonal-group) may not have such a clear finite analogue on the other hand.

##### Isometry group

↑ **Parent:** [Important Lie group](#important-lie-group)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Isometry_group)

The [group](group.md) of all transformations that preserve some [bilinear form](linear-algebra.md#bilinear-form), notable examples:
- [orthogonal group](#orthogonal-group) preserves the [inner product](calculus.md#inner-product)
- [unitary group](#unitary-group) preserves a [Hermitian form](linear-algebra.md#hermitian-form)
- [Lorentz group](#lorentz-group) preserves the [Minkowski inner product](relativity.md#minkowski-inner-product)

###### Lie algebra of a isometry group

↑ **Parent:** [Isometry group](#isometry-group)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Lie_algebra_of_a_isometry_group)

We can almost reach the [Lie algebra](#lie-algebra) of any [isometry group](#isometry-group) in a single go. For every $X$ in the [Lie algebra](#lie-algebra) we must have:

$$
\forall v, w \in V, t \in \R (e^{tX}v|e^{tX}w) = (v|w)
$$

because $e^{tX}$ has to be in the isometry group by definition as shown at [Section "Lie algebra of a matrix Lie group"](#lie-algebra-of-a-matrix-lie-group).

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

With this relation, we can easily determine the [Lie algebra](#lie-algebra) of common isometries:
- [Lie algebra of $O(n)$](#lie-algebra-of-o-n)

Bibliography:
- [An Introduction to Tensors and Group Theory for Physicists by Nadir Jeevanjee (2011)](#an-introduction-to-tensors-and-group-theory-for-physicists-by-nadir-jeevanjee-2011) page 151

##### Orthogonal group

↑ **Parent:** [Important Lie group](#important-lie-group)  
🏷️ **Tags:** [Isometry group](#isometry-group)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Orthogonal_group)

###### Definition of the orthogonal group

↑ **Parent:** [Orthogonal group](#orthogonal-group)

Intuitive definition: real group of rotations + reflections.

Mathematical definition that most directly represents this: [the orthogonal group is the group of all matrices that preserve the dot product](#the-orthogonal-group-is-the-group-of-all-matrices-that-preserve-the-dot-product).

###### The orthogonal group is the group of all matrices that preserve the dot product

↑ **Parent:** [Definition of the orthogonal group](#definition-of-the-orthogonal-group)

When viewed as matrices, it is the group of all matrices that preserve the [dot product](linear-algebra.md#dot-product), i.e.:

$$
O(n) = { O \in M(n) | \forall x, y, x^Ty = (Ox)^T (Oy) }
$$

This implies that it also preserves important geometric notions such as [norm](calculus.md#norm-mathematics) (intuitively: distance between two points) and [angles](linear-algebra.md#angle).

This is perhaps the best "default definition".

###### What happens to the definition of the orthogonal group if we choose other types of symmetric bilinear forms

↑ **Parent:** [The orthogonal group is the group of all matrices that preserve the dot product](#the-orthogonal-group-is-the-group-of-all-matrices-that-preserve-the-dot-product)

We looking at the definition [the orthogonal group is the group of all matrices that preserve the dot product](#the-orthogonal-group-is-the-group-of-all-matrices-that-preserve-the-dot-product), we notice that the [dot product](linear-algebra.md#dot-product) is one example of [positive definite symmetric bilinear form](linear-algebra.md#positive-definite-symmetric-bilinear-form), which in turn can also be represented by a matrix as shown at: [Section "Matrix representation of a symmetric bilinear form"](linear-algebra.md#matrix-representation-of-a-symmetric-bilinear-form).

By looking at this more general point of view, we could ask ourselves what happens to the group if instead of the [dot product](linear-algebra.md#dot-product) we took a more general [bilinear form](linear-algebra.md#bilinear-form), e.g.:
- $I_2$: another [positive definite symmetric bilinear form](linear-algebra.md#positive-definite-symmetric-bilinear-form) such as $(x_1, x_2)^T(y_1, y_2) = 2 x_1 y_1 + x_2 y_2$?
- $I_-$ what if we drop the [positive definite](linear-algebra.md#positive-definite-matrix) requirement, e.g. $(x_1, x_2)^T(y_1, y_2) = - x_1 y_1 + x_2 y_2$?
The answers to those questions are given by the [Sylvester's law of inertia](linear-algebra.md#sylvester-s-law-of-inertia) at [Section "All indefinite orthogonal groups of matrices of equal metric signature are isomorphic"](#all-indefinite-orthogonal-groups-of-matrices-of-equal-metric-signature-are-isomorphic).

###### The orthogonal group is the group of all invertible matrices where the inverse is equal to the transpose

↑ **Parent:** [Definition of the orthogonal group](#definition-of-the-orthogonal-group)

Let's show that this definition is equivalent to [the orthogonal group is the group of all matrices that preserve the dot product](#the-orthogonal-group-is-the-group-of-all-matrices-that-preserve-the-dot-product).

Note that:

$$
x^Ty = (Ox)^T (Oy) = x^T O^T O y
$$

and for that to be true for all possible $x$ and $y$ then we must have:

$$
O^T O = I
$$

i.e. the [matrix inverse](linear-algebra.md#matrix-inverse) is equal to the [transpose](linear-algebra.md#transpose).

Conversely, if:

$$
O^T O = I
$$

is true, then

$$
(Ox)^T (Oy) = x^T (O^T O) y = x^Ty
$$

These matricese are called the [orthogonal matrices](linear-algebra.md#orthogonal-matrix).

TODO is there any more intuitive way to think about this?

###### Elements of the orthogonal group have determinant plus or minus one

↑ **Parent:** [The orthogonal group is the group of all invertible matrices where the inverse is equal to the transpose](#the-orthogonal-group-is-the-group-of-all-invertible-matrices-where-the-inverse-is-equal-to-the-transpose)

[the orthogonal group is the group of all invertible matrices where the inverse is equal to the transpose](#the-orthogonal-group-is-the-group-of-all-invertible-matrices-where-the-inverse-is-equal-to-the-transpose)

###### The orthogonal group is the group of all matrices with orthonormal rows and orthonormal columns

↑ **Parent:** [Definition of the orthogonal group](#definition-of-the-orthogonal-group)

Or equivalently, the set of rows is [orthonormal](linear-algebra.md#orthonormality), and so is the set of columns. TODO proof that it is equivalent to [the orthogonal group is the group of all matrices that preserve the dot product](#the-orthogonal-group-is-the-group-of-all-matrices-that-preserve-the-dot-product).

###### Topology of the orthogonal group

↑ **Parent:** [Orthogonal group](#orthogonal-group)

###### The orthogonal group is compact

↑ **Parent:** [Topology of the orthogonal group](#topology-of-the-orthogonal-group)

###### Connected components of the orthogonal group

↑ **Parent:** [Topology of the orthogonal group](#topology-of-the-orthogonal-group)

The [orthogonal group](#orthogonal-group) has 2 [connected components](calculus.md#connected-component):
- one with determinant +1, which is itself a [subgroup](group.md#subgroup) known as the [special orthogonal group](#special-orthogonal-group). These are pure [rotations](#special-orthogonal-group) without a reflection.
- the other with determinant -1. This is not a [subgroup](group.md#subgroup) as it does not contain the origin. It represents [rotations](#special-orthogonal-group) with a reflection.

It is instructive to visualize how the $\pm1$ looks like in [$SO(3)$](#3d-rotation-group):
- you take the first basis vector and move it to any other. You have therefore two angular parameters.
- you take the second one, and move it to be orthogonal to the first new vector. (you can choose a circle around the first new vector, and so you have another angular parameter.
- at last, for the last one, there are only two choices that are orthogonal to both previous ones, one in each direction. It is this directio, relative to the others, that determines the "has a reflection or not" thing

As a result it is [isomorphic](group.md#group-isomorphism) to the [direct product](group.md#direct-product-of-groups) of the special orthogonal group by the [cyclic group](group.md#cyclic-group) of [order](algebra.md#order-algebra) 2:

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

<h6 id="lie-algebra-of-o-n">Lie algebra of <span class="katex"><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:1em;vertical-align:-0.25em;"></span><span class="mord mathnormal" style="margin-right:0.02778em;">O</span><span class="mopen">(</span><span class="mord mathnormal">n</span><span class="mclose">)</span></span></span></span></h6>

↑ **Parent:** [Orthogonal group](#orthogonal-group)  
🏷️ **Tags:** [Lie algebra of a matrix Lie group](#lie-algebra-of-a-matrix-lie-group)

From [Section "Lie algebra of a isometry group"](#lie-algebra-of-a-isometry-group) we reach:

###### Special orthogonal group

↑ **Parent:** [Orthogonal group](#orthogonal-group)

Group of rotations of a rigid body.

Like [orthogonal group](#orthogonal-group) but without reflections. So it is a "special case" of the orthogonal group.

This is a subgroup of both the [orthogonal group](#orthogonal-group) and the [special linear group](#special-linear-group).

<h6 id="lie-algebra-of-so-3">Lie algebra of <span class="katex"><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:1em;vertical-align:-0.25em;"></span><span class="mord mathnormal" style="margin-right:0.02778em;">SO</span><span class="mopen">(</span><span class="mord">3</span><span class="mclose">)</span></span></span></span></h6>

↑ **Parent:** [Special orthogonal group](#special-orthogonal-group)

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

Note that the [exponential map](#exponential-map) reverses this and gives a finite rotation around the Z axis back from the [infinitesimal generator](#infinitesimal-generator) $L_z$:

$$
e^{\theta L_z} = R_z(\theta)
$$

Repeating the same process for the other directions gives:

$$
L_x = TODO
L_y = TODO
$$

We have now found 3 [linearly independent](linear-algebra.md#linear-independence) elements of the Lie algebra, and since $SO(3)$ has dimension 3, we are done.

###### Lie bracket of the rotation group

↑ **Parent:** [Lie algebra of $SO(3)$](#lie-algebra-of-so-3)

Based on the $L_x$,$L_y$ and $L_z$ derived at [Lie algebra of $SO(3)$](#lie-algebra-of-so-3) we can calculate the [Lie bracket](#lie-bracket) as:

$$
TODO
$$

###### 3D rotation group

↑ **Parent:** [Special orthogonal group](#special-orthogonal-group)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/3D_rotation_group)

Has [$SU(2)$](#special-unitary-of-degree-2) as a [double cover](calculus.md#double-cover).

###### Unitary group

↑ **Parent:** [Orthogonal group](#orthogonal-group)  
🏷️ **Tags:** [Isometry group](#isometry-group)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Unitary_group)

[Group](group.md) of the [unitary matrices](linear-algebra.md#unitary-matrix).

[Complex](formalization-of-mathematics.md#complex-number) analogue of the [orthogonal group](#orthogonal-group).

One notable difference from the orthogonal group however is that the unitary group is connected "because" its determinant is not fixed to two disconnected values 1/-1, but rather goes around in a continuous [unit circle](#unit-circle). $U(1)$ _is_ the unit circle.

###### Unitary group of degree 1

↑ **Parent:** [Unitary group](#unitary-group)

###### Unitary group of degree 2

↑ **Parent:** [Unitary group](#unitary-group)

Diffeomorphic to the 3 sphere.

###### Unit circle

↑ **Parent:** [Unitary group](#unitary-group)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Unit_circle)

The $U(1)$ [unitary group](#unitary-group) is one very over-generalized way of looking at it :-)

###### Special unitary group

↑ **Parent:** [Unitary group](#unitary-group)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Special_unitary_group)

The complex analogue of the [special orthogonal group](#special-orthogonal-group), i.e. the subgroup of the [unitary group](#unitary-group) with determinant equals exactly 1 instead of an arbitrary complex number with absolute value equal 1 as is the case for the unitary group.

###### Special unitary of degree 2

↑ **Parent:** [Special unitary group](#special-unitary-group)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Special_unitary_of_degree_2)

[https://en.wikipedia.org/wiki/Representation_theory_of_SU(2)](https://en.wikipedia.org/wiki/Representation_theory_of_SU(2))

[Double cover](calculus.md#double-cover) of [$SO(3)$](#3d-rotation-group).

[Isomorphic](group.md#isomorphism) to the [quaternions](formalization-of-mathematics.md#quaternion).

<h6 id="representations-of-su-2">Representations of <span class="katex"><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:1em;vertical-align:-0.25em;"></span><span class="mord mathnormal" style="margin-right:0.05764em;">S</span><span class="mord mathnormal" style="margin-right:0.10903em;">U</span><span class="mopen">(</span><span class="mord">2</span><span class="mclose">)</span></span></span></span></h6>

↑ **Parent:** [Special unitary of degree 2](#special-unitary-of-degree-2)

<h6 id="lie-algebra-of-su-2">Lie algebra of <span class="katex"><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:1em;vertical-align:-0.25em;"></span><span class="mord mathnormal" style="margin-right:0.05764em;">S</span><span class="mord mathnormal" style="margin-right:0.10903em;">U</span><span class="mopen">(</span><span class="mord">2</span><span class="mclose">)</span></span></span></span></h6>

↑ **Parent:** [Representations of $SU(2)$](#representations-of-su-2)  
🏷️ **Tags:** [Lie algebra of a matrix Lie group](#lie-algebra-of-a-matrix-lie-group)

Bibliography:
- [Physics from Symmetry by Jakob Schwichtenberg (2015)](physicist.md#physics-from-symmetry-by-jakob-schwichtenberg-2015) page 54.

<h6 id="2d-representation-of-su-2">2D representation of <span class="katex"><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:1em;vertical-align:-0.25em;"></span><span class="mord mathnormal" style="margin-right:0.05764em;">S</span><span class="mord mathnormal" style="margin-right:0.10903em;">U</span><span class="mopen">(</span><span class="mord">2</span><span class="mclose">)</span></span></span></span></h6>

↑ **Parent:** [Representations of $SU(2)$](#representations-of-su-2)

[Pauli matrix](quantum-mechanics.md#pauli-matrix).

##### Projective linear group

↑ **Parent:** [Important Lie group](#important-lie-group)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Projective_linear_group)

TODO motivation. Motivation. Motivation. Motivation. The definitin with [quotient group](group.md#quotient-group) is easy to understand.

###### Finite projective linear group

↑ **Parent:** [Projective linear group](#projective-linear-group)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Projective_linear_group#Finite_fields)

###### Projective special linear group

↑ **Parent:** [Projective linear group](#projective-linear-group)

###### Finite projective special linear group

↑ **Parent:** [Projective special linear group](#projective-special-linear-group)

<h6 id="psl-2-p"><span class="katex"><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:1em;vertical-align:-0.25em;"></span><span class="mord mathnormal" style="margin-right:0.05764em;">PS</span><span class="mord mathnormal">L</span><span class="mopen">(</span><span class="mord">2</span><span class="mpunct">,</span><span class="mspace" style="margin-right:0.1667em;"></span><span class="mord mathnormal">p</span><span class="mclose">)</span></span></span></span></h6>

↑ **Parent:** [Finite projective special linear group](#finite-projective-special-linear-group)

<h6 id="psl-2-7">PSL(2,7)</h6>

↑ **Parent:** [$PSL(2, p)$](#psl-2-p)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/PSL(2,7))

The second smallest non-[Abelian](group.md#abelian-group) finite [simple group](group.md#simple-group) after the [alternating group of degree 5](group.md#alternating-group-of-degree-5).

<h5 id="poincare-group">Poincaré group</h5>

↑ **Parent:** [Important Lie group](#important-lie-group)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Poincaré_group)

Full set of all possible [special relativity](relativity.md#special-relativity) symmetries:
- translations in space and time
- rotations in space
- [Lorentz boosts](#lorentz-boost)

In simple and concrete terms. Suppose you observe N particles following different trajectories in [Spacetime](relativity.md#spacetime).

There are two observers traveling at constant speed relative to each other, and so they see different trajectories for those particles:
- space and time shifts, because their space origin and time origin (time they consider 0, i.e. when they started their timers) are not synchronized. This can be modelled with a 4-vector addition.
- their space axes are rotated relative to one another. This can be modelled with a 4x4 matrix multiplication.
- and they are moving relative to each other, which leads to the usual spacetime interactions of [special relativity](relativity.md#special-relativity). Also modelled with a 4x4 matrix multiplication.
Note that the first two types of transformation are exactly the non-relativistic [Galilean transformations](#galilean-transformation).

The Poincare group is the set of all matrices such that such a relationship like this exists between two frames of reference.

###### Galilean transformation

↑ **Parent:** [Poincaré group](#poincare-group)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Galilean_transformation)

###### Translation (geometry)

↑ **Parent:** [Galilean transformation](#galilean-transformation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Translation_(geometry))

Subset of [Galilean transformation](#galilean-transformation) with speed equals 0.

###### Translation group

↑ **Parent:** [Translation (geometry)](#translation-geometry)

This is a good and simple first example of [Lie algebra](#lie-algebra) to look into.

###### The derivative is the generator of the translation group

↑ **Parent:** [Translation group](#translation-group)

Take the group of all [Translation](#translation-geometry) in [$\R^1$](calculus.md#real-line).

Let's see how the [generator](#generator-of-a-lie-algebra) of this group is the [derivative](calculus.md#derivative) [operator](linear-algebra.md#linear-operator):

$$
\pdv{}{x}
$$

The way to think about this is:
- the translation group operates on the argument of a function $f(x)$
- the generator is an [operator](linear-algebra.md#linear-operator) that operates on $f$ itself

So let's take the [exponential map](#exponential-map-lie-theory):

$$
e^{x_0\pdv{}{x}}f(x) = \left( 1 + x_0 \pdv{}{x} + x_0^2 \pdv{^2}{x^2} + \ldots\right)f(x)
$$

and we notice that this is exactly the [Taylor series](calculus.md#taylor-series) of $f(x)$ around the identity element of the translation group, which is 0! Therefore, if $f(x)$ behaves nicely enough, within some [radius of convergence](calculus.md#radius-of-convergence) around the origin we have for finite $x_0$:

$$
e^{x_0\pdv{}{x}}f(x) = f(x + x_0)
$$

This example shows clearly how the [exponential map](#exponential-map-lie-theory) applied to a (differential) [operator](linear-algebra.md#linear-operator) can generate finite (non-infinitesimal) [Translation](#translation-geometry)!

###### Galilean invariance

↑ **Parent:** [Galilean transformation](#galilean-transformation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Galilean_invariance)

A [law of physics](physics.md#law-of-physics) is Galilean invariant if the same formula works both when you are standing still on land, or when you are on a boat moving at constant velocity.

For example, if we were describing the movement of a [point particle](mechanics.md#point-particle), the exact same formulas that predict the evolution of $x_{land}(t)$ must also predict $x_{boat}(t)$, even though of course both of those $x(t)$ will have different values. 

It would be extremely unsatisfactory if the formulas of the [laws of physics](physics.md#law-of-physics) did not obey [Galilean invariance](#galilean-invariance). Especially if you remember that [Earth](astronomy.md#earth) is travelling extremelly fast relative to the [Sun](astronomy.md#sun). If there was no such invariance, that would mean for example that the [laws of physics](physics.md#law-of-physics) would be different in other [planets](astronomy.md#planet) that are moving at different speeds. That would be a strong sign that our laws of physics are not complete.

The consequence/cause of that is that you cannot know if you are moving at a constant speed or not.

[Lorentz invariance](relativity.md#lorentz-invariant) generalizes [Galilean invariance](#galilean-invariance) to also account for [special relativity](relativity.md#special-relativity), in which a more complicated invariant that also takes into account different times observed in different [inertial frames of reference](relativity.md#inertial-frame-of-reference) is also taken into account. But the fundamental desire for the [Lorentz invariance](relativity.md#lorentz-invariant) of the [laws of physics](physics.md#law-of-physics) remains the same.

###### Covariance

↑ **Parent:** [Galilean invariance](#galilean-invariance)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Covariance)

Generally means that he form of the equation $f(x)$ does not change if we transform $x$.

This is generally what we want from the laws of physics.

E.g. a [Galilean transformation](#galilean-transformation) generally changes the exact values of coordinates, but not the form of the laws of physics themselves.

[Lorentz covariance](relativity.md#lorentz-covariance) is the main context under which the word "covariant" appears, because we really don't want the form of the equations to change under [Lorentz transforms](relativity.md#lorentz-transformation), and "covariance" is often used as a synonym of "Lorentz covariance".

TODO some sources distinguish "invariant" from "covariant": [invariant vs covariant](#invariant-vs-covariant).

###### Invariant vs covariant

↑ **Parent:** [Covariance](#covariance)

Some sources distinguish "invariant" from "covariant" such that under some transformation (typically [Lie group](#lie-group)):
- invariant: the value of $f(x)$ does not change if we transform $x$
- covariant: the form of the equation $f(x)$ does not change if we transform $x$.
TODO examples.

Bibliography:
- [https://physics.stackexchange.com/questions/7700/definitions-and-usage-of-covariant-form-invariant-invariant](https://physics.stackexchange.com/questions/7700/definitions-and-usage-of-covariant-form-invariant-invariant)
- [https://physics.stackexchange.com/questions/270296/what-is-the-difference-between-lorentz-invariant-and-lorentz-covariant](https://physics.stackexchange.com/questions/270296/what-is-the-difference-between-lorentz-invariant-and-lorentz-covariant)

###### Lorentz group

↑ **Parent:** [Poincaré group](#poincare-group)  
🏷️ **Tags:** [Isometry group](#isometry-group)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Lorentz_group)

[Subgroup](group.md#subgroup) of the [Poincaré group](#poincare-group) without translations. Therefore, in those, the spacetime origin is always fixed.

Or in other words, it is as if two observers had their space and time origins at the exact same place. However, their space axes may be rotated, and one may be at a relative speed to the other to create a [Lorentz boost](#lorentz-boost). Note however that if they are at relative speeds to one another, then their axes will immediately stop being at the same location in the next moment of time, so things are only valid infinitesimally in that case.

This group is made up of matrix multiplication alone, no need to add the offset vector: space rotations and [Lorentz boost](#lorentz-boost) only spin around and bend things around the origin.

One definition: set of all 4x4 matrices that keep the [Minkowski inner product](relativity.md#minkowski-inner-product), mentioned at [Physics from Symmetry by Jakob Schwichtenberg (2015)](physicist.md#physics-from-symmetry-by-jakob-schwichtenberg-2015) page 63. This then implies:

$$
\Lambda ^ T \eta \Lambda = \eta
$$

###### Representation theory of the Lorentz group

↑ **Parent:** [Lorentz group](#lorentz-group)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Representation_theory_of_the_Lorentz_group)

[Physics from Symmetry by Jakob Schwichtenberg (2015)](physicist.md#physics-from-symmetry-by-jakob-schwichtenberg-2015) page 66 shows one in terms of 4x4 complex matrices.

More importantly though, are the representations of the [Lie algebra of the Lorentz group](#lie-algebra-of-the-lorentz-group), which are generally also just also called "Representation of the Lorentz group" since you can reach the representation from the algebra via the [exponential map](#exponential-map).

Bibliography:
- [Physics from Symmetry by Jakob Schwichtenberg (2015)](physicist.md#physics-from-symmetry-by-jakob-schwichtenberg-2015) chapter 3.7 "The Lorentz Group O (1, 3)"

###### Representation of the Lorentz group

↑ **Parent:** [Representation theory of the Lorentz group](#representation-theory-of-the-lorentz-group)

One of the representations of the [Lorentz group](#lorentz-group) that show up in the [Representation theory of the Lorentz group](#representation-theory-of-the-lorentz-group).

###### Lie algebra of the Lorentz group

↑ **Parent:** [Representation of the Lorentz group](#representation-of-the-lorentz-group)

###### Spinor

↑ **Parent:** [Representation of the Lorentz group](#representation-of-the-lorentz-group)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Spinor)

TODO understand a bit more intuitively.

- [Physics from Symmetry by Jakob Schwichtenberg (2015)](physicist.md#physics-from-symmetry-by-jakob-schwichtenberg-2015) page 72
- [https://physics.stackexchange.com/questions/172385/what-is-a-spinor](https://physics.stackexchange.com/questions/172385/what-is-a-spinor)
- [https://physics.stackexchange.com/questions/41211/what-is-the-difference-between-a-spinor-and-a-vector-or-a-tensor](https://physics.stackexchange.com/questions/41211/what-is-the-difference-between-a-spinor-and-a-vector-or-a-tensor)
- [https://physics.stackexchange.com/questions/74682/introduction-to-spinors-in-physics-and-their-relation-to-representations](https://physics.stackexchange.com/questions/74682/introduction-to-spinors-in-physics-and-their-relation-to-representations)
- [http://www.weylmann.com/spinor.pdf](http://www.weylmann.com/spinor.pdf)

<a id="video-the-mystery-of-spinors-by-richard-behiel"></a>
**[Video 2](#video-the-mystery-of-spinors-by-richard-behiel). The Mystery of Spinors by Richard Behiel.** [Source](https://www.youtube.com/watch?v=b7OIbMCIfs4).

###### Lorentz boost

↑ **Parent:** [Lorentz group](#lorentz-group)

Two observers travel at fixed speed relative to each other. They synchronize origins at x=0 and t=0, and their spacial axes are perfectly aligned. This is a subset of the [Lorentz group](#lorentz-group). TODO confirm it does not form a subgroup however.

###### Indefinite orthogonal group

↑ **Parent:** [Lorentz group](#lorentz-group)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Indefinite_orthogonal_group)

Generalization of [orthogonal group](#orthogonal-group) to preserve different [bilinear forms](linear-algebra.md#bilinear-form). Important because the [Lorentz group](#lorentz-group) is [$SO(1,3)$](#lorentz-group).

###### Definition of the indefinite orthogonal group

↑ **Parent:** [Indefinite orthogonal group](#indefinite-orthogonal-group)

Given a [matrix](linear-algebra.md#matrix) $A$ with [metric signature](linear-algebra.md#metric-signature) containing $m$ positive and $n$ negative entries, the [indefinite orthogonal group](#indefinite-orthogonal-group) is the set of all matrices that preserve the [associated bilinear form](linear-algebra.md#matrix-representation-of-a-bilinear-form), i.e.:

$$
O(m, n) = {O \in M(m + n) | \forall x, y x^T A y = (Ox)^T A (Oy)}
$$

Note that if $A = I$, we just have the standard [dot product](linear-algebra.md#dot-product), and that subcase corresponds to the following definition of the [orthogonal group](#orthogonal-group): [Section "The orthogonal group is the group of all matrices that preserve the dot product"](#the-orthogonal-group-is-the-group-of-all-matrices-that-preserve-the-dot-product).

As shown at [all indefinite orthogonal groups of matrices of equal metric signature are isomorphic](#all-indefinite-orthogonal-groups-of-matrices-of-equal-metric-signature-are-isomorphic), due to the [Sylvester's law of inertia](linear-algebra.md#sylvester-s-law-of-inertia), only the metric signature of $A$ matters. E.g., if we take two different matrices with the same metric signature such as:

$$
\begin{bmatrix}
1 0
0 -1
\end{bmatrix}
$$

and:

$$
\begin{bmatrix}
2 0
0 -3
\end{bmatrix}
$$

both produce [isomorphic](group.md#isomorphism) spaces. So it is customary to just always pick the matrix with only +1 and -1 as entries.

###### All indefinite orthogonal groups of matrices of equal metric signature are isomorphic

↑ **Parent:** [Definition of the indefinite orthogonal group](#definition-of-the-indefinite-orthogonal-group)

Following the [definition of the indefinite orthogonal group](#definition-of-the-indefinite-orthogonal-group), we want to show that only the [metric signature](linear-algebra.md#metric-signature) matters.

First we can observe that the exact matrices are different. For example, taking the standard matrix of $O(2)$:

$$
\begin{bmatrix}
1 0
0 1
\end{bmatrix}
$$

and:

$$
\begin{bmatrix}
2 0
0 1
\end{bmatrix}
$$

both have the same [metric signature](linear-algebra.md#metric-signature). However, we notice that a rotation of 90 degrees, which preserves the first form, does not preserve the second one! E.g. consider the vector $x = (1, 0)$, then $x \cdot x = 1$. But after a rotation of 90 degrees, it becomes $x_2 = (0, 1)$, and now $x_2 \cdot x_2 = 2$! Therefore, we have to search for an [isomorphism](group.md#isomorphism) between the two sets of matrices.

For example, consider the [orthogonal group](#orthogonal-group), which can be defined as shown at [the orthogonal group is the group of all matrices that preserve the dot product](#the-orthogonal-group-is-the-group-of-all-matrices-that-preserve-the-dot-product) can be defined as:

###### Indefinite special orthogonal group

↑ **Parent:** [Indefinite orthogonal group](#indefinite-orthogonal-group)

Like the [special orthogonal group](#special-orthogonal-group) is to the [orthogonal group](#orthogonal-group), [$SO(m,n)$](#indefinite-special-orthogonal-group) is the subset of [$O(m,n)$](#indefinite-orthogonal-group) with [determinant](linear-algebra.md#determinant) equal to exactly 1.

#### Representation theory

↑ **Parent:** [Lie group](#lie-group)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Representation_theory)

Basically, a "representation" means associating each group element as an invertible [matrices](linear-algebra.md#matrix), i.e. a matrix in (possibly some subset of) [$GL(n)$](#general-linear-group), that has the same properties as the group.

Or in other words, associating to the more abstract notion of a [group](group.md) more concrete objects with which we are familiar (e.g. a matrix). 

Each such matrix then represents one specific element of the group.

This is basically what everyone does (or should do!) when starting to study [Lie groups](#lie-group): we start looking at [matrix Lie groups](#matrix-lie-group), which are very concrete.

Or more precisely, mapping each group element to a [linear map](linear-algebra.md#linear-map) over some [vector field](group.md#vector-field) $V$ (which can be represented by a matrix infinite dimension), in a way that respects the group operations:

$$
R(g) : G \to GL(V)
$$

As shown at [Physics from Symmetry by Jakob Schwichtenberg (2015)](physicist.md#physics-from-symmetry-by-jakob-schwichtenberg-2015)
- page 51, a representation is not unique, we can even use matrices of different dimensions to represent the same group
- 3.6 classifies the [representations of $SU(2)$](#representations-of-su-2). There is only one possibility per dimension!
- 3.7 "The Lorentz Group O(1,3)" mentions that even for a "simple" group such as the [Lorentz group](#lorentz-group), not all representations can be described in terms of matrices, and that we can construct such representations with the help of [Lie group](#lie-group) theory, and that they have fundamental physical application

Motivation:
- [https://math.stackexchange.com/questions/1628464/what-is-representation-theory](https://math.stackexchange.com/questions/1628464/what-is-representation-theory)

Bibliography:
- [https://www.youtube.com/watch?v=9rDzaKASMTM](https://www.youtube.com/watch?v=9rDzaKASMTM) "RT1: Representation Theory Basics" by [MathDoctorBob](mathematics.md#mathdoctorbob) (2011). Too much theory, give me the motivation!
- [https://www.quantamagazine.org/the-useless-perspective-that-transformed-mathematics-20200609](https://www.quantamagazine.org/the-useless-perspective-that-transformed-mathematics-20200609) The "Useless" Perspective That Transformed Mathematics by [Quanta Magazine](science.md#quanta-magazine) (2020). Maybe there is something in there amidst the "the reader might not know what a [matrix](linear-algebra.md#matrix) is" stuff.

##### Irreducible representation

↑ **Parent:** [Representation theory](#representation-theory)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Irreducible_representation)

###### Casimir element

↑ **Parent:** [Irreducible representation](#irreducible-representation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Casimir_element)

<h5 id="schur-s-lemma">Schur's lemma</h5>

↑ **Parent:** [Representation theory](#representation-theory)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Schur's_lemma)

#### Simple Lie group

↑ **Parent:** [Lie group](#lie-group)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Simple_Lie_group)

##### Classification of simple Lie groups

↑ **Parent:** [Simple Lie group](#simple-lie-group)  
🏷️ **Tags:** [Classification (mathematics)](mathematics.md#classification-mathematics)

[https://en.wikipedia.org/wiki/Simple_Lie_group#List](https://en.wikipedia.org/wiki/Simple_Lie_group#List)

A bit like the [classification of simple finite groups](group.md#classification-of-finite-simple-groups), they also have a few [sporadic groups](group.md#sporadic-group)! Not as spectacular since as usual [continuous problems are simpler than discrete ones](calculus.md#continuous-problems-are-simpler-than-discrete-ones), but still, not bad.

#### Lie group bibliography

↑ **Parent:** [Lie group](#lie-group)

Recommended from [Physics from Symmetry by Jakob Schwichtenberg (2015)](physicist.md#physics-from-symmetry-by-jakob-schwichtenberg-2015) page 92:
- [An Introduction to Tensors and Group Theory for Physicists by Nadir Jeevanjee (2011)](#an-introduction-to-tensors-and-group-theory-for-physicists-by-nadir-jeevanjee-2011)
- [Naive Lie theory by John Stillwell (2008)](#naive-lie-theory-by-john-stillwell-2008)
- [Lie Algebras In Particle Physics by Howard Georgi (1999)](#lie-algebras-in-particle-physics-by-howard-georgi-1999)

##### An Introduction to Tensors and Group Theory for Physicists by Nadir Jeevanjee (2011)

↑ **Parent:** [Lie group bibliography](#lie-group-bibliography)

This does not seem to go deep into the [Standard Model](standard-model.md) as [Physics from Symmetry by Jakob Schwichtenberg (2015)](physicist.md#physics-from-symmetry-by-jakob-schwichtenberg-2015), appears to focus more on more basic applications.

But because it is more basic, it does explain some things quite well.

##### Lie Groups, Physics, and Geometry by Robert Gilmore (2008)

↑ **Parent:** [Lie group bibliography](#lie-group-bibliography)

The author seems to have uploaded the entire book by chapters at: [https://www.physics.drexel.edu/~bob/LieGroups.html](https://www.physics.drexel.edu/~bob/LieGroups.html)

And the author is the cutest: [https://www.physics.drexel.edu/~bob/Personal.html](https://www.physics.drexel.edu/~bob/Personal.html).

Overview:
- Chapter 3: gives a bunch of examples of important [matrix Lie groups](#matrix-lie-group). These are done by imposing certain types of constraints on the [general linear group](#general-linear-group), to obtain [subgroups](group.md#subgroup) of the general linear group. Feels like the start of a [classification](mathematics.md#classification-mathematics)
- Chapter 4: defines [Lie algebra](#lie-algebra). Does some basic examples with them, but not much of deep interest, that is mostl left for Chapter 7
- Chapter 5: calculates the [Lie algebra](#lie-algebra) for all examples from chapter 3
- Chapter 6: don't know
- Chapter 7: describes how the [exponential map](#exponential-map) links [Lie algebras](#lie-algebra) to [Lie groups](#lie-group)

##### Naive Lie theory by John Stillwell (2008)

↑ **Parent:** [Lie group bibliography](#lie-group-bibliography)

##### Lie Algebras In Particle Physics by Howard Georgi (1999)

↑ **Parent:** [Lie group bibliography](#lie-group-bibliography)

## Tesselation

↑ **Parent:** [Geometry](geometry.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Tesselation)

### Aperiodic tiling

↑ **Parent:** [Tesselation](#tesselation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Aperiodic_tiling)

[https://www.quantamagazine.org/nasty-geometry-breaks-decades-old-tiling-conjecture-20221215/](https://www.quantamagazine.org/nasty-geometry-breaks-decades-old-tiling-conjecture-20221215/)

### Tiling of the plane

↑ **Parent:** [Tesselation](#tesselation)

[https://math.libretexts.org/Bookshelves/Arithmetic_and_Basic_Math/Book%3A_Basic_Math_(Grade_6)/01%3A_Area_and_Surface_Area/01%3A_Lessons_Reasoning_to_Find_Area/1.01%3A_Tiling_the_Plane](https://math.libretexts.org/Bookshelves/Arithmetic_and_Basic_Math/Book%3A_Basic_Math_(Grade_6)/01%3A_Area_and_Surface_Area/01%3A_Lessons_Reasoning_to_Find_Area/1.01%3A_Tiling_the_Plane)

<a id="video-hexagons-are-the-bestagons-by-cgp-grey-2020"></a>
**[Video 3](#video-hexagons-are-the-bestagons-by-cgp-grey-2020). Hexagons are the Bestagons by CGP Grey (2020)** [Source](https://www.youtube.com/watch?v=thOifuHs6eY).

#### Aperiodic monotile

↑ **Parent:** [Tiling of the plane](#tiling-of-the-plane)

##### Smith aperiodic monotile

↑ **Parent:** [Aperiodic monotile](#aperiodic-monotile)

[Preprint](education.md#preprint): [https://arxiv.org/abs/2303.10798](https://arxiv.org/abs/2303.10798)

![](https://upload.wikimedia.org/wikipedia/commons/thumb/2/25/Smith_aperiodic_monotiling.svg/500px-Smith_aperiodic_monotiling.svg.png)

**[Figure 2](#_485)** [Source](https://commons.wikimedia.org/wiki/File:Smith_aperiodic_monotiling.svg.png).

##### Spectre aperiodic monotile

↑ **Parent:** [Aperiodic monotile](#aperiodic-monotile)

[https://aperiodical.com/2023/05/now-thats-what-i-call-an-aperiodic-monotile/](https://aperiodical.com/2023/05/now-thats-what-i-call-an-aperiodic-monotile/)

## ↑ Ancestors (3)

1. [Area of mathematics](mathematics.md#area-of-mathematics)
2. [Mathematics](mathematics.md)
3. [Ciro Santilli's Homepage](README.md)

## ← Incoming links (2)

- [Adolfo Amidei](physicist.md#adolfo-amidei)
- [Positive definite matrix](linear-algebra.md#positive-definite-matrix)
