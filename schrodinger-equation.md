<h1 id="schrodinger-equation">Schrödinger equation</h1>

↑ **Parent:** [Non-relativistic quantum mechanics](non-relativistic-quantum-mechanics.md)  
🏷️ **Tags:** [Important partial differential equation](important-partial-differential-equation.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Schrödinger_equation)

The [partial differential equation](partial-differential-equation.md) of [non-relativistic](special-relativity.md) [quantum mechanics](quantum-mechanics-split.md).

Experiments explained:
- via the [Schrödinger equation solution for the hydrogen atom](schrodinger-equation-solution-for-the-hydrogen-atom.md) it predicts:
  - [spectral line](spectral-line.md) basic lines, plus [Zeeman effect](zeeman-effect.md)
- [Schrödinger equation solution for the helium atom](schrodinger-equation-solution-for-the-helium-atom.md): perturbative solutions give good approximations to the energy levels
- [double-slit experiment](double-slit-experiment.md): I think we have a closed solution for the max and min probabilities on the measurement wall, and they match experiments

Experiments not explained: those that the [Dirac equation](dirac-equation.md) explains like:
- [fine structure](fine-structure.md)
- [spontaneous emission](spontaneous-emission.md) coefficients

To get some intuition on the equation on the consequences of the equation, have a look at:
- [Schrödinger equation simulations](computational-quantum-mechanics.md)
- [solutions of the Schrodinger equation](solutions-of-the-schrodinger-equation.md)

The easiest to understand case of the equation which you must have in mind initially that of the [Schrödinger equation for a free one dimensional particle](schrodinger-equation-for-a-free-one-dimensional-particle.md).

Then, with that in mind, the general form of the [Schrödinger equation](schrodinger-equation.md) is:<a id="equation-schrodinger-equation"></a>


$$
i\hbar\pdv{\psi(\vv{x}, t)}{t} = \hat{H}[\psi(\vv{x}, t)]
$$

where:
- $\hbar$ is the [reduced Planck constant](reduced-planck-constant.md)
- $\psi$ is the [wave function](wave-function.md)
- $t$ is the time
- $\hat{H}$ is a [linear operator](linear-operator.md) called the [Hamiltonian](hamiltonian-mechanics.md). It takes as input a function $\psi$, and returns another function. This plays a role analogous to the Hamiltonian in [classical mechanics](classical-mechanics.md): determining it determines what the physical system looks like, and how the system evolves in time, because we can just plug it into the equation and solve it. It basically encodes the total energy and forces of the system.

The $\vv{x}$ argument of $\psi$ could be anything, e.g.:
- we could have preferred [polar coordinates](polar-coordinate-system.md) instead of linear ones if the potential were symmetric around a point
- we could have more than one particle, e.g. [solutions of the Schrodinger equation for two electrons](solutions-of-the-schrodinger-equation-for-two-electrons.md), which would have e.g. $x_1$ and $x_2$ for different particles. No matter how many particles there are, we have just a single $\psi$, we just add more arguments to it.
- we could have even more generalized coordinates. This is much in the spirit of [Hamiltonian mechanics](hamiltonian-mechanics.md) or [generalized coordinates](generalized-coordinate.md)
Note however that there is always a single magical $t$ time variable. This is needed in particular because there is a time [partial derivative](partial-derivative.md) in the equation, so there must be a corresponding time variable in the function. This makes the equation explicitly [non-relativistic](relativity-split.md).

The general [Schrödinger equation](schrodinger-equation.md) can be broken up into a trivial time-dependent and a [time-independent Schrödinger equation](time-independent-schrodinger-equation.md) by separation of variables. So in practice, all we need to solve is the slightly simpler [time-independent Schrödinger equation](time-independent-schrodinger-equation.md), and the full equation comes out as a result.

Existence and uniqueness: [https://mathoverflow.net/questions/212913/existence-and-uniqueness-for-two-dimensional-time-dependent-schr%C3%B6dinger-equation](https://mathoverflow.net/questions/212913/existence-and-uniqueness-for-two-dimensional-time-dependent-schr%C3%B6dinger-equation)

**Table of contents**

- [Time-independent Schrödinger equation](time-independent-schrodinger-equation.md)
  - [Solving the Schrodinger equation with the time-independent Schrödinger equation](solving-the-schrodinger-equation-with-the-time-independent-schrodinger-equation.md)
- [Derivation of the Schrodinger equation](derivation-of-the-schrodinger-equation.md)
  - [Why are complex numbers used in the Schrodinger equation?](why-are-complex-numbers-used-in-the-schrodinger-equation.md)
- [Schrodinger equation Hamiltonian](schrodinger-equation-hamiltonian.md)
- [The Schrodinger equation Hamiltonian has to be Hermitian](the-schrodinger-equation-hamiltonian-has-to-be-hermitian.md)
- [Solutions of the Schrodinger equation](solutions-of-the-schrodinger-equation.md)
  - [Computational quantum mechanics](computational-quantum-mechanics.md)
    - [Why it is hard to simulate quantum systems?](why-it-is-hard-to-simulate-quantum-systems.md)
    - [Computational quantum mechanics software](computational-quantum-mechanics-software.md)
      - [Quantum ESPRESSO](quantum-espresso.md)
      - [QuTiP](qutip.md)
  - [Schrödinger equation for a one dimensional particle](schrodinger-equation-for-a-one-dimensional-particle.md)
  - [Schrödinger equation for a free one dimensional particle](schrodinger-equation-for-a-free-one-dimensional-particle.md)
    - [Plane wave function](plane-wave-function.md)
    - [Time-independent Schrödinger equation for a free one dimensional particle](time-independent-schrodinger-equation-for-a-free-one-dimensional-particle.md)
  - [Particle in a box](particle-in-a-box.md)
    - [Quantum well](quantum-well.md)
  - [Quantum harmonic oscillator](quantum-harmonic-oscillator.md)
    - [Quantum LC circuit](quantum-lc-circuit.md)
    - [Hermite polynomials](hermite-polynomials.md)
      - [Hermite functions](hermite-functions.md)
    - [Ladder operator](ladder-operator.md)
  - [Quantum tunnelling](quantum-tunnelling.md)
  - [Schrödinger equation solution for the hydrogen atom](schrodinger-equation-solution-for-the-hydrogen-atom.md)
    - [Atomic orbital](atomic-orbital.md)
    - [Quantum number](quantum-number.md)
      - [Principal quantum number](principal-quantum-number.md)
      - [Azimuthal quantum number](azimuthal-quantum-number.md)
        - [s-orbital](s-orbital.md)
        - [p-orbital](p-orbital.md)
        - [d-orbital](d-orbital.md)
        - [f-orbital](f-orbital.md)
      - [Magnetic quantum number](magnetic-quantum-number.md)
      - [Spin quantum number](spin-quantum-number.md)
        - [Spectroscopic notation](spectroscopic-notation.md)
  - [Solutions for the Schrodinger equation with multiple particles](solutions-for-the-schrodinger-equation-with-multiple-particles.md)
    - [Separable state](separable-state.md)
    - [Solutions of the Schrodinger equation for two electrons](solutions-of-the-schrodinger-equation-for-two-electrons.md)
    - [Orbital approximation](orbital-approximation.md)
    - [Schrödinger equation solution for the helium atom](schrodinger-equation-solution-for-the-helium-atom.md)
    - [Hartree-Fock method](hartree-fock-method.md)
      - [Hartree-Fock method for the helium atom](hartree-fock-method-for-the-helium-atom.md)
      - [Why do multiple electrons occupy the same orbital if electrons repel each other?](why-do-multiple-electrons-occupy-the-same-orbital-if-electrons-repel-each-other.md)
      - [Aufbau principle](aufbau-principle.md)
        - [Electron configuration](electron-configuration.md)
        - [Electron configuration notation](electron-configuration-notation.md)
        - [Why does 2s have less energy than 1s if they have the same principal quantum number?](why-does-2s-have-less-energy-than-1s-if-they-have-the-same-principal-quantum-number.md)
        - [Madelung energy ordering rule](madelung-energy-ordering-rule.md)
          - [Exception to the Madelung energy ordering rule](exception-to-the-madelung-energy-ordering-rule.md)
        - [Term symbol](term-symbol.md)
          - [Hund's rules](hund-s-rules.md)
            - [Hund's first rule](hund-s-first-rule.md)
            - [Hund's second rule](hund-s-second-rule.md)
    - [Term symbols for carbon ground state](term-symbols-for-carbon-ground-state.md)
    - [Schrödinger equation solution for molecule](schrodinger-equation-solution-for-molecule.md)
      - [Schrödinger equation solution for the hydrogen molecule](schrodinger-equation-solution-for-the-hydrogen-molecule.md)
      - [Chemical bond](chemical-bond.md)
        - [Molecule](molecule.md)
          - [Molecule representation](molecule-representation.md)
            - [Ball-and-stick model](ball-and-stick-model.md)
          - [Isomer](isomer.md)
            - [Cis-trans isomerism](cis-trans-isomerism.md)
            - [Enantiomer](enantiomer.md)
            - [Polymorphism (materials science)](polymorphism-materials-science.md)
            - [Stereochemistry](stereochemistry.md)
        - [Covalent bond](covalent-bond.md)
          - [Sigma bond](sigma-bond.md)
          - [Pi bond](pi-bond.md)
            - [Double bond](double-bond.md)
            - [Triple bond](triple-bond.md)
        - [Ionic bond](ionic-bond.md)
        - [Octet rule](octet-rule.md)
  - [Two-state quantum system](two-state-quantum-system.md)
    - [Bloch sphere](bloch-sphere.md)
    - [Pauli matrix](pauli-matrix.md)
- [Born-Oppenheimer approximation](born-oppenheimer-approximation.md)
- [Uncertainty principle](uncertainty-principle.md)
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
- [Conservation laws in Schrodinger equations](conservation-laws-in-schrodinger-equations.md)
  - [Conservation of the square amplitude in the Schrodinger equation](conservation-of-the-square-amplitude-in-the-schrodinger-equation.md)
    - [Probability current](probability-current.md)
- [Wave function](wave-function.md)
  - [Matter wave](matter-wave.md)
    - [Electron diffraction experiment](electron-diffraction-experiment.md)
      - [Diffraction of Cathode Rays by a Thin Film by Thomson and Reid (1927)](diffraction-of-cathode-rays-by-a-thin-film-by-thomson-and-reid-1927.md)
      - [Davisson-Germer experiment](davisson-germer-experiment.md)
    - [de Broglie relations](de-broglie-relations.md)

## 🏷️ Tagged (1)

- [The Schrödinger equation is not relativistic](the-schrodinger-equation-is-not-relativistic.md)

## ↑ Ancestors (7)

1. [Non-relativistic quantum mechanics](non-relativistic-quantum-mechanics.md)
2. [Quantum mechanics](quantum-mechanics-split.md)
3. [Particle physics](particle-physics-split.md)
4. [Physics](physics-split.md)
5. [Natural science](natural-science.md)
6. [Science](science-split.md)
7. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (38)

- [Causality in quantum mechanics](causality-in-quantum-mechanics.md)
- [Conservation of the square amplitude in the Schrodinger equation](conservation-of-the-square-amplitude-in-the-schrodinger-equation.md)
- [Derivation of the Klein-Gordon equation](derivation-of-the-klein-gordon-equation.md)
- [Dirac equation](dirac-equation.md)
- [Energy operator](energy-operator.md)
- [History of quantum mechanics](history-of-quantum-mechanics.md)
- [Hund's rules](hund-s-rules.md)
- [Important partial differential equation](important-partial-differential-equation.md)
- [Klein-Gordon equation](klein-gordon-equation.md)
- [Lagrangian mechanics](lagrangian-mechanics.md)
- [Matrix mechanics](matrix-mechanics.md)
- [Non-relativistic quantum mechanics](non-relativistic-quantum-mechanics.md)
- [Particle physics](particle-physics-split.md)
- [Planck constant](planck-constant.md)
- [Planck's law](planck-s-law.md)
- [Plane wave function](plane-wave-function.md)
- [Programmer's model of quantum computers](programmer-s-model-of-quantum-computers.md)
- [Quantization as an Eigenvalue Problem](quantization-as-an-eigenvalue-problem.md)
- [Quantum electrodynamics](quantum-electrodynamics.md)
- [Quantum jump](quantum-jump.md)
- [Quantum mechanical re-interpretation of kinematic and mechanical relations by Heisenberg (1925)](quantum-mechanical-re-interpretation-of-kinematic-and-mechanical-relations-by-heisenberg-1925.md)
- [Quantum mechanics](quantum-mechanics-split.md)
- [Quantum number](quantum-number.md)
- [Reduced Planck constant](reduced-planck-constant.md)
- [Schrödinger equation](schrodinger-equation.md)
- [Schrödinger equation for a one dimensional particle](schrodinger-equation-for-a-one-dimensional-particle.md)
- [Separation of variables](separation-of-variables.md)
- [Solving the Schrodinger equation with the time-independent Schrödinger equation](solving-the-schrodinger-equation-with-the-time-independent-schrodinger-equation.md)
- [Spectral line](spectral-line.md)
- [Spin (physics)](spin-physics.md)
- [Spontaneous emission](spontaneous-emission.md)
- [System of partial differential equations](system-of-partial-differential-equations.md)
- [The Schrodinger equation Hamiltonian has to be Hermitian](the-schrodinger-equation-hamiltonian-has-to-be-hermitian.md)
- [Time-independent Schrödinger equation](time-independent-schrodinger-equation.md)
- [Wave function collapse](wave-function-collapse.md)
- [Why are complex numbers used in the Schrodinger equation?](why-are-complex-numbers-used-in-the-schrodinger-equation.md)
- [Why does 2s have less energy than 1s if they have the same principal quantum number?](why-does-2s-have-less-energy-than-1s-if-they-have-the-same-principal-quantum-number.md)
- [Zeeman effect](zeeman-effect.md)
