# Representation theory

↑ **Parent:** [Lie group](lie-group.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Representation_theory)

Basically, a "representation" means associating each group element as an invertible [matrices](matrix.md), i.e. a matrix in (possibly some subset of) [$GL(n)$](general-linear-group.md), that has the same properties as the group.

Or in other words, associating to the more abstract notion of a [group](group-split.md) more concrete objects with which we are familiar (e.g. a matrix). 

Each such matrix then represents one specific element of the group.

This is basically what everyone does (or should do!) when starting to study [Lie groups](lie-group.md): we start looking at [matrix Lie groups](matrix-lie-group.md), which are very concrete.

Or more precisely, mapping each group element to a [linear map](linear-map.md) over some [vector field](vector-field.md) $V$ (which can be represented by a matrix infinite dimension), in a way that respects the group operations:

$$
R(g) : G \to GL(V)
$$

As shown at [Physics from Symmetry by Jakob Schwichtenberg (2015)](physics-from-symmetry-by-jakob-schwichtenberg-2015.md)
- page 51, a representation is not unique, we can even use matrices of different dimensions to represent the same group
- 3.6 classifies the [representations of $SU(2)$](representations-of-su-2.md). There is only one possibility per dimension!
- 3.7 "The Lorentz Group O(1,3)" mentions that even for a "simple" group such as the [Lorentz group](lorentz-group.md), not all representations can be described in terms of matrices, and that we can construct such representations with the help of [Lie group](lie-group.md) theory, and that they have fundamental physical application

Motivation:
- [https://math.stackexchange.com/questions/1628464/what-is-representation-theory](https://math.stackexchange.com/questions/1628464/what-is-representation-theory)

Bibliography:
- [https://www.youtube.com/watch?v=9rDzaKASMTM](https://www.youtube.com/watch?v=9rDzaKASMTM) "RT1: Representation Theory Basics" by [MathDoctorBob](mathdoctorbob.md) (2011). Too much theory, give me the motivation!
- [https://www.quantamagazine.org/the-useless-perspective-that-transformed-mathematics-20200609](https://www.quantamagazine.org/the-useless-perspective-that-transformed-mathematics-20200609) The "Useless" Perspective That Transformed Mathematics by [Quanta Magazine](quanta-magazine.md) (2020). Maybe there is something in there amidst the "the reader might not know what a [matrix](matrix.md) is" stuff.

**Table of contents**

- [Irreducible representation](irreducible-representation.md)
  - [Casimir element](casimir-element.md)
- [Schur's lemma](schur-s-lemma.md)

## ↑ Ancestors (6)

1. [Lie group](lie-group.md)
2. [Differential geometry](differential-geometry.md)
3. [Geometry](geometry-split.md)
4. [Area of mathematics](area-of-mathematics.md)
5. [Mathematics](mathematics-split.md)
6. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (2)

- [Lecture 1](quantum-field-theory-lecture-by-tobias-osborne-2017/lecture-1.md)
- [Spin number of a field](spin-number-of-a-field.md)
