<h1 id="schrodinger-picture">Schrödinger picture</h1>

↑ **Parent:** [Mathematical formulation of quantum mechanics](mathematical-formulation-of-quantum-mechanics.md)

To better understand the discussion below, the best thing to do is to read it in parallel with the simplest possible example: [Schrödinger picture example: quantum harmonic oscillator](schrodinger-picture-example-quantum-harmonic-oscillator.md).

The state of a quantum system is a unit vector in a [Hilbert space](hilbert-space.md).

"Making a measurement" for an [observable](observable.md) means applying a [self-adjoint operator](self-adjoint-operator.md) to the state, and after a measurement is done:
- the state [collapses](wave-function-collapse.md) to an [eigenvector](eigenvector.md) of the self adjoint operator
- the result of the measurement is the [eigenvalue](eigenvalue.md) of the self adjoint operator
- the probability of a given result happening when the spectrum is [discrete](discrete.md) is proportional to the modulus of the projection on that eigenvector.

  For continuous spectra such as that of the [position operator](position-operator.md) in most systems, e.g. [Schrödinger equation for a free one dimensional particle](schrodinger-equation-for-a-free-one-dimensional-particle.md), the projection on each individual eigenvalue is zero, i.e. the probability of one absolutely exact position is zero. To get a non-zero result, measurement has to be done on a continuous range of eigenvectors (e.g. for position: "is the particle present between x=0 and x=1?"), and you have to integrate the probability over the projection on a continuous range of eigenvalues.

  In such continuous cases, the probability collapses to an uniform distribution on the range after measurement.

  The continuous position operator case is well illustrated at: [Video 9. "Visualization of Quantum Physics (Quantum Mechanics) by udiprod (2017)"](computational-quantum-mechanics.md#video-visualization-of-quantum-physics-quantum-mechanics-by-udiprod-2017)
Those last two rules are also known as the [Born rule](born-rule.md).

Self adjoint operators are chosen because they have the following key properties:
- their eigenvalues form an orthonormal basis
- they are diagonalizable

See also: [https://en.wikipedia.org/wiki/Measurement_in_quantum_mechanics](https://en.wikipedia.org/wiki/Measurement_in_quantum_mechanics)

Perhaps the easiest case to understand this for is that of [spin](spin-physics.md), which has only a finite number of eigenvalues. Although it is a shame that fully understanding that requires a [relativistic](special-relativity.md) quantum theory such as the [Dirac equation](dirac-equation.md).

The next steps are to look at simple 1D bound states such as [particle in a box](particle-in-a-box.md) and [quantum harmonic oscillator](quantum-harmonic-oscillator.md).

This naturally generalizes to [Schrödinger equation solution for the hydrogen atom](schrodinger-equation-solution-for-the-hydrogen-atom.md).

The solution to the [Schrödinger equation for a free one dimensional particle](schrodinger-equation-for-a-free-one-dimensional-particle.md) is a bit harder since the possible energies do not make up a [countable set](countable-set.md).

This formulation was apparently called more precisely [Dirac-von Neumann axioms](dirac-von-neumann-axioms.md), but it because so dominant we just call it "the" formulation.

[Quantum Field Theory lecture notes by David Tong (2007)](quantum-field-theory-lecture-notes-by-david-tong-2007.md) mentions that:

> if you were to write the wavefunction in quantum field theory, it would be a functional, that is a function of every possible configuration of the field $\phi$.

**Table of contents**

- [Schrödinger picture example: quantum harmonic oscillator](schrodinger-picture-example-quantum-harmonic-oscillator.md)
- [Wave function collapse](wave-function-collapse.md)
  - [Interpretations of quantum mechanics](interpretations-of-quantum-mechanics.md)
    - [Categorical quantum mechanics](categorical-quantum-mechanics.md)
    - [EPR paradox](epr-paradox.md)
    - [Many-worlds interpretation](many-worlds-interpretation.md)
      - [Universal wavefunction](universal-wavefunction.md)

## ↑ Ancestors (7)

1. [Mathematical formulation of quantum mechanics](mathematical-formulation-of-quantum-mechanics.md)
2. [Quantum mechanics](quantum-mechanics-split.md)
3. [Particle physics](particle-physics-split.md)
4. [Physics](physics-split.md)
5. [Natural science](natural-science.md)
6. [Science](science-split.md)
7. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (3)

- [Causality in quantum mechanics](causality-in-quantum-mechanics.md)
- [Mathematical formulation of quantum mechanics](mathematical-formulation-of-quantum-mechanics.md)
- [Schrödinger picture example: quantum harmonic oscillator](schrodinger-picture-example-quantum-harmonic-oscillator.md)
