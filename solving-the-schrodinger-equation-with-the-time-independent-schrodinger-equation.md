<h1 id="solving-the-schrodinger-equation-with-the-time-independent-schrodinger-equation">Solving the Schrodinger equation with the time-independent Schrödinger equation</h1>

↑ **Parent:** [Time-independent Schrödinger equation](time-independent-schrodinger-equation.md)

Before reading any further, you _must_ understand [heat equation solution with Fourier series](heat-equation-solution-with-fourier-series.md), which uses [separation of variables](separation-of-variables.md).

Once that example is clear, we see that the exact same [separation of variables](separation-of-variables.md) can be done to the [Schrödinger equation](schrodinger-equation.md). If we name the constant of the separation of variables $E$ for energy, we get:
- a time-only part that does not depend on space and does not depend on the [Hamiltonian](hamiltonian-mechanics.md) at all. The solution for this part is therefore always the same exponentials for any problem, and this part is therefore "boring":$$
  \psi_t(E, t) = e^{-iEt/\hbar}
  $$
- a space-only part that does not depend on time, bud does depend on the Hamiltonian:

  $$
  \hat{H}[\psi_x(E, \vv{x})] = E \psi_x{\vv{x}}
  $$

  Since this is the only non-trivial part, unlike the time part which is trivial, this spacial part is just called "the time-independent Schrodinger equation".

  Note that the $\psi$ here is not the same as the $\psi$ in the [time-dependent Schrodinger equation](schrodinger-equation.md#equation-schrodinger-equation) of course, as that psi is the result of the multiplication of the time and space parts. This is a bit of imprecise terminology, but hey, physics.

Because the time part of the equation is always the same and always trivial to solve, all we have to do to actually solve the Schrodinger equation is to solve the time independent one, and then we can construct the full solution trivially.

Once we've solved the time-independent part for each possible $E$, we can construct a solution exactly as we did in [heat equation solution with Fourier series](heat-equation-solution-with-fourier-series.md): we make a weighted sum over all possible $E$ to match the initial condition, which is analogous to the [Fourier series](fourier-series.md) in the case of the heat equation to reach a final full solution:
- if there are only discretely many possible values of $E$, each possible energy $E_i$. we proceed <a id="equation-solution-of-the-schrodinger-equation-in-terms-of-the-time-independent-and-time-dependent-parts"></a>
  $$
  \sum_{i=0}^{\infty} =  \psi_t(E_i, t) \psi_x(E_i, x) = e^{-iE_i t/\hbar} \psi_x(E_i, x)
  $$

  and this is a solution by selecting $E_i$ such that at time $t = 0$ we match the initial condition:$$
  \sum_{i=0}^{\infty} e^{-iE0/\hbar} E_i\psi_i(x) = \sum_{i=0}^{\infty} E_i\psi_i(x) = initial condition
  $$

  A finite spectrum shows up in many incredibly important cases:
  - [particle in a box](particle-in-a-box.md)
  - [quantum harmonic oscillator](quantum-harmonic-oscillator.md)
  - [Schrödinger equation solution for the hydrogen atom](schrodinger-equation-solution-for-the-hydrogen-atom.md)
- if there are infinitely many values of E, we do something analogous but with an integral instead of a sum. This is called the [continuous spectrum](continuous-spectrum-functional-analysis.md). One notable

The fact that this approximation of the initial condition is always possible from is mathematically proven by some version of the [spectral theorem](spectral-theorem.md) based on the fact that [The Schrodinger equation Hamiltonian has to be Hermitian](the-schrodinger-equation-hamiltonian-has-to-be-hermitian.md) and therefore behaves nicely.

It is interesting to note that solving the time-independent Schrodinger equation can also be seen exactly as an [eigenvalue](eigenvalue.md) equation where:
- the [Hamiltonian](hamiltonian-mechanics.md) is a linear operator
- the value of the energy `E` is an [eigenvalue](eigenvalue.md)
The only difference from usual [matrix](matrix.md) [eigenvectors](eigenvector.md) is that we are now dealing with an [infinite dimensional](infinite-dimensional.md) vector space.

Furthermore:
- we immediately see from the equation that the time-independent solutions are states of deterministic energy because the energy is an [eigenvalue](eigenvalue.md) of the Hamiltonian operator
- by looking at [Equation 11. "Solution of the Schrodinger equation in terms of the time-independent and time dependent parts"](#equation-solution-of-the-schrodinger-equation-in-terms-of-the-time-independent-and-time-dependent-parts), it is obvious that if we take an energy measurement, the probability of each result never changes with time, because it is only multiplied by a constant

Bibliography:
- [https://quantummechanics.ucsd.edu/ph130a/130_notes/node124.html](https://quantummechanics.ucsd.edu/ph130a/130_notes/node124.html) from [quantum physics by Jim Branson (2003)](quantum-physics-by-jim-branson-2003.md)

## ↑ Ancestors (9)

1. [Time-independent Schrödinger equation](time-independent-schrodinger-equation.md)
2. [Schrödinger equation](schrodinger-equation.md)
3. [Non-relativistic quantum mechanics](non-relativistic-quantum-mechanics.md)
4. [Quantum mechanics](quantum-mechanics-split.md)
5. [Particle physics](particle-physics-split.md)
6. [Physics](physics-split.md)
7. [Natural science](natural-science.md)
8. [Science](science-split.md)
9. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (2)

- [Schrödinger equation for a free one dimensional particle](schrodinger-equation-for-a-free-one-dimensional-particle.md)
- [Time-independent Schrödinger equation](time-independent-schrodinger-equation.md)
