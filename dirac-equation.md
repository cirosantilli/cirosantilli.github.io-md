# Dirac equation

↑ **Parent:** [Relativistic quantum mechanics](relativistic-quantum-mechanics-split.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Dirac_equation)

Adds [special relativity](special-relativity.md) to the [Schrödinger equation](schrodinger-equation.md), and the following conclusions come basically as a direct consequence of this!

Experiments explained:
- [spontaneous emission](spontaneous-emission.md) coefficients.
- [fine structure](fine-structure.md), notably for example [Dirac equation solution for the hydrogen atom](dirac-equation-solution-for-the-hydrogen-atom.md)
- [antimatter](antimatter.md)
- [particle creation and annihilation](particle-creation-and-annihilation.md)

Experiments not explained: those that [quantum electrodynamics](quantum-electrodynamics.md) explains like:
- [Lamb shift](lamb-shift.md)
- TODO: quantization of the electromagnetic field as [photons](photon-split.md)?
See also: [Dirac equation vs quantum electrodynamics](dirac-equation-vs-quantum-electrodynamics.md).

The Dirac equation is a set of 4 [partial differential equations](partial-differential-equation.md) on 4 [complex valued](complex-number.md) wave functions. The full explicit form in [Planck units](planck-units.md) is shown e.g. in [Video 2. "Quantum Mechanics 12a - Dirac Equation I by ViaScience (2015)"](#video-quantum-mechanics-12a-dirac-equation-i-by-viascience-2015) at [https://youtu.be/OCuaBmAzqek?t=1010](https://youtu.be/OCuaBmAzqek?t=1010):<a id="equation-expanded-dirac-equation-in-planck-units"></a>


$$
  i \partial_t \begin{bmatrix} \psi_1 \\  \psi_2 \\  \psi_3 \\  \psi_4 \end{bmatrix} =
- i \partial_x \begin{bmatrix} \psi_4 \\  \psi_3 \\  \psi_2 \\  \psi_1 \end{bmatrix}
+   \partial_y \begin{bmatrix}-\psi_4 \\  \psi_3 \\ -\psi_2 \\  \psi_1 \end{bmatrix}
- i \partial_z \begin{bmatrix} \psi_3 \\ -\psi_4 \\  \psi_1 \\ -\psi_2 \end{bmatrix}
+ m            \begin{bmatrix} \psi_1 \\  \psi_2 \\ -\psi_3 \\ -\psi_4 \end{bmatrix}
$$

Then as done at [https://physics.stackexchange.com/questions/32422/qm-without-complex-numbers/557600#557600](https://physics.stackexchange.com/questions/32422/qm-without-complex-numbers/557600#557600) from [why are complex numbers used in the Schrodinger equation?](why-are-complex-numbers-used-in-the-schrodinger-equation.md), we could further split those equations up into a system of 8 equations on 8 [real-valued](real-number.md) functions.

<a id="video-quantum-mechanics-12a-dirac-equation-i-by-viascience-2015"></a>
**[Video 2](#video-quantum-mechanics-12a-dirac-equation-i-by-viascience-2015). Quantum Mechanics 12a - Dirac Equation I by ViaScience (2015)** [Source](http://youtube.com/watch?v=OCuaBmAzqek).

<a id="video-phys-485-lecture-14-the-dirac-equation-by-roger-moore-2016"></a>
**[Video 3](#video-phys-485-lecture-14-the-dirac-equation-by-roger-moore-2016). PHYS 485 Lecture 14: The Dirac Equation by Roger Moore (2016)** [Source](https://www.youtube.com/watch?v=ajMaPc022VM).

**Table of contents**

- [Absorption, spontaneous and stimulated emission](absorption-spontaneous-and-stimulated-emission.md)
  - [Spontaneous emission](spontaneous-emission.md)
    - [Spontaneous emission defies causality](spontaneous-emission-defies-causality.md)
  - [Photon absorption](photon-absorption.md)
  - [Stimulated emission](stimulated-emission.md)
    - [History of stimulated emission](history-of-stimulated-emission.md)
      - [On the Quantum Theory of Radiation](on-the-quantum-theory-of-radiation.md)
  - [Einstein coefficients](einstein-coefficients.md)
- [The Dirac equation predicts spin](the-dirac-equation-predicts-spin.md)
- [Antimatter](antimatter.md)
- [Particle creation and annihilation](particle-creation-and-annihilation.md)
  - [Particle decay](particle-decay.md)
    - [Pair production](pair-production.md)
  - [Relativistic particle in a box thought experiment](relativistic-particle-in-a-box-thought-experiment.md)
- [The Dirac equation is consistent with special relativity](the-dirac-equation-is-consistent-with-special-relativity.md)
- [Derivation of the Dirac equation](derivation-of-the-dirac-equation.md)
- [Pauli equation](pauli-equation.md)
- [Klein-Gordon equation](klein-gordon-equation.md)
  - [Derivation of the Klein-Gordon equation](derivation-of-the-klein-gordon-equation.md)
- [Solutions of the Dirac equation](solutions-of-the-dirac-equation.md)
  - [Dirac equation solution for the hydrogen atom](dirac-equation-solution-for-the-hydrogen-atom.md)
- [Spin (physics)](spin-physics.md)
  - [Spin experiments](spin-experiments.md)
    - [Stern-Gerlach experiment](stern-gerlach-experiment.md)
      - [The Stern-Gerlach experiment needs an inhomogenous magnetic field](the-stern-gerlach-experiment-needs-an-inhomogenous-magnetic-field.md)
      - [Stern-Gerlach experiment paper](stern-gerlach-experiment-paper.md)
        - [The experimental proof of directional quantization in the magnetic field](the-experimental-proof-of-directional-quantization-in-the-magnetic-field.md)
    - [Spintronics](spintronics.md)
      - [Spin valve](spin-valve.md)
      - [Tunnel magnetoresistance](tunnel-magnetoresistance.md)
      - [Giant magnetoresistance](giant-magnetoresistance.md)
      - [Spin-transfer torque](spin-transfer-torque.md)
  - [Spin number of a field](spin-number-of-a-field.md)
    - [Spin 0](spin-0.md)
    - [Spin half](spin-half.md)
    - [Spin 1](spin-1.md)
      - [Proca equation](proca-equation.md)
    - [Spin 2](spin-2.md)
    - [Why is the spin of the electron half?](why-is-the-spin-of-the-electron-half.md)
  - [Pauli exclusion principle](pauli-exclusion-principle.md)
    - [Slater determinant](slater-determinant.md)
    - [Fermions, bosons and anyons](fermions-bosons-and-anyons.md)
      - [Fermion](fermion.md)
      - [Boson](boson.md)
      - [Anyon](anyon.md)
        - [Abelian an non abelian anyons](abelian-an-non-abelian-anyons.md)
          - [Abelian anyon](abelian-anyon.md)
          - [Non Abelian anyon](non-abelian-anyon.md)
    - [Spin-statistics theorem](spin-statistics-theorem.md)
    - [Electron degeneracy pressure](electron-degeneracy-pressure.md)
- [Dirac Lagrangian](dirac-lagrangian.md)
  - [Dirac adjoint](dirac-adjoint.md)
  - [Gamma matrices](gamma-matrices.md)
  - [Feynman slash notation](feynman-slash-notation.md)

## 🏷️ Tagged (1)

- [Dirac equation vs quantum electrodynamics](dirac-equation-vs-quantum-electrodynamics.md)

## ↑ Ancestors (7)

1. [Relativistic quantum mechanics](relativistic-quantum-mechanics-split.md)
2. [Quantum mechanics](quantum-mechanics-split.md)
3. [Particle physics](particle-physics-split.md)
4. [Physics](physics-split.md)
5. [Natural science](natural-science.md)
6. [Science](science-split.md)
7. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (34)

- [Antimatter](antimatter.md)
- [Atom 2007 Mini Series episode 3](atom-2007-mini-series-episode-3.md)
- [Derivation of the Dirac equation](derivation-of-the-dirac-equation.md)
- [Derivation of the Klein-Gordon equation](derivation-of-the-klein-gordon-equation.md)
- [Derivation of the quantum electrodynamics Lagrangian](derivation-of-the-quantum-electrodynamics-lagrangian.md)
- [Dirac equation](dirac-equation.md)
- [Dirac equation solution for the hydrogen atom](dirac-equation-solution-for-the-hydrogen-atom.md)
- [Dirac equation vs quantum electrodynamics](dirac-equation-vs-quantum-electrodynamics.md)
- [Dirac Lagrangian](dirac-lagrangian.md)
- [Fine structure](fine-structure.md)
- [Hyperfine structure](hyperfine-structure.md)
- [Internal and spacetime symmetries](internal-and-spacetime-symmetries.md)
- [Klein-Gordon equation](klein-gordon-equation.md)
- [Lamb-Retherford experiment](lamb-retherford-experiment.md)
- [Lamb shift](lamb-shift.md)
- [Mathematical formulation of quantum field theory](mathematical-formulation-of-quantum-field-theory.md)
- [Particle creation and annihilation](particle-creation-and-annihilation.md)
- [Particle physics](particle-physics-split.md)
- [Paul Dirac](paul-dirac.md)
- [Quantum electrodynamics](quantum-electrodynamics.md)
- [Quantum electrodynamics experiment](quantum-electrodynamics-experiment.md)
- [Quantum mechanics](quantum-mechanics-split.md)
- [Quantum physics by Jim Branson (2003)](quantum-physics-by-jim-branson-2003.md)
- [Relativistic quantum mechanics](relativistic-quantum-mechanics-split.md)
- [Schrödinger equation](schrodinger-equation.md)
- [Schrödinger picture](schrodinger-picture.md)
- [Solutions of the Schrodinger equation for two electrons](solutions-of-the-schrodinger-equation-for-two-electrons.md)
- [Spectral line](spectral-line.md)
- [Spin half](spin-half.md)
- [Spin (physics)](spin-physics.md)
- [Spontaneous emission](spontaneous-emission.md)
- [The Dirac equation does not work for more than one electron](the-dirac-equation-does-not-work-for-more-than-one-electron.md)
- [What does it mean that photons are force carriers for electromagnetism?](what-does-it-mean-that-photons-are-force-carriers-for-electromagnetism.md)
- [Why is the spin of the electron half?](why-is-the-spin-of-the-electron-half.md)
