# Uncertainty principle

↑ **Parent:** [Schrödinger equation](schrodinger-equation.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Uncertainty_principle)

The wave equation contains the entire state of a particle.

From [mathematical formulation of quantum mechanics](mathematical-formulation-of-quantum-mechanics.md) remember that the wave equation is a vector in [Hilbert space](hilbert-space.md).

And a single vector can be represented in many different ways in different basis, and two of those ways happen to be the position and the momentum representations.

More importantly, position and momentum are first and foremost operators associated with observables: the [position operator](position-operator.md) and the [momentum operator](momentum-operator.md). And both of their eigenvalue sets form a basis of the [Hilbert space](hilbert-space.md) according to the [spectral theorem](spectral-theorem.md).

When you represent a wave equation as a function, you have to say what the variable of the function means. And depending on weather you say "it means position" or "it means momentum", the position and momentum operators will be written differently.

This is well shown at: [Video 9. "Visualization of Quantum Physics (Quantum Mechanics) by udiprod (2017)"](computational-quantum-mechanics.md#video-visualization-of-quantum-physics-quantum-mechanics-by-udiprod-2017).

Furthermore, the position and momentum representations are equivalent: one is the [Fourier transform](fourier-transform.md) of the other: [position and momentum space](position-and-momentum-space.md). Remember that notably we can always take the Fourier transform of a function in [$\LTwo$](l2.md) due to [Carleson's theorem](carleson-s-theorem.md).

Then the uncertainty principle follows immediately from a general property of the Fourier transform: [https://en.wikipedia.org/w/index.php?title=Fourier_transform&oldid=961707157#Uncertainty_principle](https://en.wikipedia.org/w/index.php?title=Fourier_transform&oldid=961707157#Uncertainty_principle)

In precise terms, the [uncertainty principle](uncertainty-principle.md) talks about the [standard deviation](standard-deviation.md) of two measures.

We can visualize the uncertainty principle more intuitively by thinking of a [wave function](wave-function.md) that is a [real](real-number.md) [flat top bump function](flat-top-bump-function.md) with a flat top in [1D](real-line.md). We can then change the width of the support, but when we do that, the top goes higher to keep probability equal to 1. The momentum is 0 everywhere, except in the edges of the support. Then:
- to localize the wave in space at position 0 to reduce the space uncertainty, we have to reduce the support. However, doing so makes the momentum variation on the edges more and more important, as the slope will go up and down faster (higher top, and less x space for descent), leading to a larger variance (note that average momentum is still 0, due to to symmetry of the bump function)
- to localize the momentum as much as possible at 0, we can make the support wider and wider. This makes the bumps at the edges smaller and smaller. However, this also obviously delocalises the wave function more and more, increasing the variance of x

Bibliography:
- [https://www.youtube.com/watch?v=bIIjIZBKgtI&list=PL54DF0652B30D99A4&index=59](https://www.youtube.com/watch?v=bIIjIZBKgtI&list=PL54DF0652B30D99A4&index=59) "K2. Heisenberg Uncertainty Relation" by doctorphys (2011)
- [https://physics.stackexchange.com/questions/132111/uncertainty-principle-intuition](https://physics.stackexchange.com/questions/132111/uncertainty-principle-intuition) Uncertainty Principle Intuition on [Physics Stack Exchange](physics-stack-exchange.md)

**Table of contents**

- [Position and momentum space](position-and-momentum-space.md)
  - [Position representation](position-representation.md)
  - [Position operator](position-operator.md)
  - [Momentum operator](momentum-operator.md)
  - [Squeezed coherent state](squeezed-coherent-state.md)
- [Energy operator](energy-operator.md)
  - [Time-energy uncertainty principle](time-energy-uncertainty-principle.md)
- [Angular momentum operator](angular-momentum-operator.md)
  - [Total angular momentum operator](total-angular-momentum-operator.md)
- [Complementarity (physics)](complementarity-physics.md)

## ↑ Ancestors (8)

1. [Schrödinger equation](schrodinger-equation.md)
2. [Non-relativistic quantum mechanics](non-relativistic-quantum-mechanics.md)
3. [Quantum mechanics](quantum-mechanics-split.md)
4. [Particle physics](particle-physics-split.md)
5. [Physics](physics-split.md)
6. [Natural science](natural-science.md)
7. [Science](science-split.md)
8. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (7)

- [Angular momentum operator](angular-momentum-operator.md)
- [Computational quantum mechanics](computational-quantum-mechanics.md)
- [GitHub](ourbigbook-com/github.md)
- [Plane wave function](plane-wave-function.md)
- [Quantum superposition](quantum-superposition.md)
- [Time-energy uncertainty principle](time-energy-uncertainty-principle.md)
- [Uncertainty principle](uncertainty-principle.md)
