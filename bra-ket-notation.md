# Bra-ket notation

↑ **Parent:** [Mathematical formulation of quantum mechanics](mathematical-formulation-of-quantum-mechanics.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Bra–ket_notation)

Notation used in [quantum mechanics](quantum-mechanics-split.md).

Ket is just a [vector](vector-mathematics.md). Though generally in the context of [quantum mechanics](quantum-mechanics-split.md), this is an infinite dimensional vector in a [Hilbert space](hilbert-space.md) like [$\LTwo$](l2.md).

Bra is just the [dual vector](dual-vector.md) corresponding to a ket, or in other words [projection](projection-mathematics.md) [linear operator](linear-operator.md), i.e. a linear function which can act on a given vector and returns a single [complex number](complex-number.md). Also known as... [dot product](dot-product.md).

For example:

$$
(a{x}) \ket{y}
$$

is basically a fancy way of saying:

$$
x \cdot y
$$

that is: we are taking the projection of $y$ along the $x$ direction. Note that in the ordinary dot product notation however, we don't differentiate as clearly what is a vector and what is an operator, while the bra-ket notation makes it clear.

The projection operator is completely specified by the vector that we are projecting it on. This is why the bracket notation makes sense.

It also has the merit of clearly differentiating vectors from operators. E.g. it is not very clear in $x \cdot y$ that $x$ is an operator and $y$ is a vector, except due to the relative position to the dot. This is especially bad when we start manipulating operators by themselves without vectors.

This notation is widely used in [quantum mechanics](quantum-mechanics-split.md) because calculating the [probability](probability.md) of getting a certain outcome for an experiment is calculated by taking the projection of a state on one an [eigenvalue](eigenvalue.md) basis vector as explained at: [Section "Mathematical formulation of quantum mechanics"](mathematical-formulation-of-quantum-mechanics.md).

Making the projection operator "look like a thing" (the bra) is nice because we can add and multiply them much like we can for vectors (they also form a [vector space](vector-space.md)), e.g.:

$$
a{x} + a{y}
$$

just means taking the projection along the $x + y$ direction.

[Ciro Santilli](ciro-santilli-split.md) thinks that this notation is a bit over-engineered. Notably the bra's are just vectors, which we should just write as usual with $\va{v}$... the bra thing makes it look scarier than it needs to be. And then we should just find a different notation for the projection part.

Maybe [Dirac](paul-dirac.md) chose it because of the appeal of the women's piece of clothing: [bra](bra.md), in an irresistible call from [British humour](british-humour.md).

But in any case, alas, we are now stuck with it.

## ↑ Ancestors (7)

1. [Mathematical formulation of quantum mechanics](mathematical-formulation-of-quantum-mechanics.md)
2. [Quantum mechanics](quantum-mechanics-split.md)
3. [Particle physics](particle-physics-split.md)
4. [Physics](physics-split.md)
5. [Natural science](natural-science.md)
6. [Science](science-split.md)
7. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (3)

- [Photon polarization](photon-polarization.md)
- [Polarizer](polarizer.md)
- [Tensor product in quantum computing](tensor-product-in-quantum-computing.md)
