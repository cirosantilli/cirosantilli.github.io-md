# Quantum mechanics

↑ **Parent:** [Particle physics](particle-physics.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Quantum_mechanics)

Quantum mechanics is quite a broad term. Perhaps it is best to start approaching it from the division into:
- [non-relativistic quantum mechanics](#non-relativistic-quantum-mechanics): obviously the simpler one, and where you should start
- [relativistic quantum mechanics](relativistic-quantum-mechanics.md): more advanced, and arguably "less useful"

Key experiments that could not work without quantum mechanics: [Section "Quantum mechanics experiment"](#quantum-mechanics-experiment).

Mathematics: there are a few models of increasing precision which could all be called "quantum mechanics":
- [Schrödinger equation](#schrodinger-equation)
- [Dirac equation](relativistic-quantum-mechanics.md#dirac-equation)
- [quantum electrodynamics](quantum-field-theory.md#quantum-electrodynamics)

[Ciro Santilli](ciro-santilli.md) feels that the [largest technological revolutions since the 1950's have been quantum related](technology.md#deep-tech), and will continue to be for a while, from deeper understanding of chemistry and materials to [quantum computing](quantum-computing.md), understanding and controlling quantum systems is where the most interesting frontier of technology lies.

**Table of contents**

- [Quantum mechanics experiment](#quantum-mechanics-experiment)
  - [Emission spectrum](#emission-spectrum)
    - [Spectral line](#spectral-line)
      - [NIST Atomic Spectra Database](#nist-atomic-spectra-database)
      - [Forbidden mechanism](#forbidden-mechanism)
        - [Selection rule](#selection-rule)
          - [Metastable electron](#metastable-electron)
            - [Triplet state](#triplet-state)
      - [Rydberg atom](#rydberg-atom)
      - [Hydrogen emission spectrum](#hydrogen-emission-spectrum)
        - [Gross hydrogen emission spectrum](#gross-hydrogen-emission-spectrum)
          - [Hydrogen 1-2 spectral line](#hydrogen-1-2-spectral-line)
        - [Rydberg formula](#rydberg-formula)
          - [Balmer series](#balmer-series)
        - [Hydrogen spectral series](#hydrogen-spectral-series)
          - [Pickering series](#pickering-series)
      - [Fine structure](#fine-structure)
        - [Fine structure constant](#fine-structure-constant)
        - [Hyperfine structure](#hyperfine-structure)
          - [Hydrogen line](#hydrogen-line)
      - [Zeeman effect](#zeeman-effect)
        - [Anomalous Zeeman effect](#anomalous-zeeman-effect)
  - [Double-slit experiment](#double-slit-experiment)
    - [Single particle double slit experiment](#single-particle-double-slit-experiment)
      - [Single electron double slit experiment](#single-electron-double-slit-experiment)
    - [Are particles bounced by the first wall in the double slit experiment?](#are-particles-bounced-by-the-first-wall-in-the-double-slit-experiment)
  - [Franck-Hertz experiment](#franck-hertz-experiment)
  - [Quantum Hall effect](#quantum-hall-effect)
    - [Integer quantum Hall effect](#integer-quantum-hall-effect)
    - [Fractional quantum Hall effect](#fractional-quantum-hall-effect)
      - [Fractional quantum Hall effect for $\nu = 1/m$](#fractional-quantum-hall-effect-for-nu-1-m)
      - [Fractional quantum Hall effect for $\nu \ne 1/m$](#fractional-quantum-hall-effect-for-nu-ne-1-m)
        - [Fractional quantum Hall effect 5/2](#fractional-quantum-hall-effect-5-2)
    - [Spin Hall effect](#spin-hall-effect)
  - [Macroscopic quantum phenomena](#macroscopic-quantum-phenomena)
- [History of quantum mechanics](#history-of-quantum-mechanics)
  - [Timeline of quantum mechanics](#timeline-of-quantum-mechanics)
  - [Old quantum theory](#old-quantum-theory)
- [History of quantum mechanics bibliography](#history-of-quantum-mechanics-bibliography)
  - [The Quantum Story by Jim Baggott (2011)](#the-quantum-story-by-jim-baggott-2011)
  - [The Old Quantum Theory by Dirk ter Haar (1967)](#the-old-quantum-theory-by-dirk-ter-haar-1967)
- [Quantum mechanics bibliography](#quantum-mechanics-bibliography)
  - [Introductory Quantum Mechanics by Richard Fitzpatrick (2020)](#introductory-quantum-mechanics-by-richard-fitzpatrick-2020)
  - [The Principles of Quantum Mechanics by Paul Dirac (1930)](#the-principles-of-quantum-mechanics-by-paul-dirac-1930)
    - [The Principles of Quantum Mechanics by Paul Dirac revised fourth edition (1967)](#the-principles-of-quantum-mechanics-by-paul-dirac-revised-fourth-edition-1967)
  - [MIT 8.06 Quantum Physics III, Spring 2018 by Barton Zwiebach](#mit-8-06-quantum-physics-iii-spring-2018-by-barton-zwiebach)
  - [Applications of Quantum Mechanics by David Tong (2017)](#applications-of-quantum-mechanics-by-david-tong-2017)
  - [Quantum Mechanics for Engineers by Leon van Dommelen (2011)](#quantum-mechanics-for-engineers-by-leon-van-dommelen-2011)
  - [Quantum physics by Jim Branson (2003)](#quantum-physics-by-jim-branson-2003)
- [Mathematical formulation of quantum mechanics](#mathematical-formulation-of-quantum-mechanics)
  - [Schrödinger picture](#schrodinger-picture)
    - [Schrödinger picture example: quantum harmonic oscillator](#schrodinger-picture-example-quantum-harmonic-oscillator)
    - [Wave function collapse](#wave-function-collapse)
      - [Interpretations of quantum mechanics](#interpretations-of-quantum-mechanics)
        - [Categorical quantum mechanics](#categorical-quantum-mechanics)
        - [EPR paradox](#epr-paradox)
        - [Many-worlds interpretation](#many-worlds-interpretation)
          - [Universal wavefunction](#universal-wavefunction)
  - [Born rule](#born-rule)
  - [Bra-ket notation](#bra-ket-notation)
  - [Dirac-von Neumann axioms](#dirac-von-neumann-axioms)
  - [Linearity of quantum mechanics](#linearity-of-quantum-mechanics)
  - [Observable](#observable)
  - [Phase-space formulation](#phase-space-formulation)
- [Non-relativistic quantum mechanics](#non-relativistic-quantum-mechanics)
  - [Schrödinger equation](#schrodinger-equation)
    - [Time-independent Schrödinger equation](#time-independent-schrodinger-equation)
      - [Solving the Schrodinger equation with the time-independent Schrödinger equation](#solving-the-schrodinger-equation-with-the-time-independent-schrodinger-equation)
    - [Derivation of the Schrodinger equation](#derivation-of-the-schrodinger-equation)
      - [Why are complex numbers used in the Schrodinger equation?](#why-are-complex-numbers-used-in-the-schrodinger-equation)
    - [Schrodinger equation Hamiltonian](#schrodinger-equation-hamiltonian)
    - [The Schrodinger equation Hamiltonian has to be Hermitian](#the-schrodinger-equation-hamiltonian-has-to-be-hermitian)
    - [Solutions of the Schrodinger equation](#solutions-of-the-schrodinger-equation)
      - [Computational quantum mechanics](#computational-quantum-mechanics)
        - [Why it is hard to simulate quantum systems?](#why-it-is-hard-to-simulate-quantum-systems)
        - [Computational quantum mechanics software](#computational-quantum-mechanics-software)
          - [Quantum ESPRESSO](#quantum-espresso)
          - [QuTiP](#qutip)
      - [Schrödinger equation for a one dimensional particle](#schrodinger-equation-for-a-one-dimensional-particle)
      - [Schrödinger equation for a free one dimensional particle](#schrodinger-equation-for-a-free-one-dimensional-particle)
        - [Plane wave function](#plane-wave-function)
        - [Time-independent Schrödinger equation for a free one dimensional particle](#time-independent-schrodinger-equation-for-a-free-one-dimensional-particle)
      - [Particle in a box](#particle-in-a-box)
        - [Quantum well](#quantum-well)
      - [Quantum harmonic oscillator](#quantum-harmonic-oscillator)
        - [Quantum LC circuit](#quantum-lc-circuit)
        - [Hermite polynomials](#hermite-polynomials)
          - [Hermite functions](#hermite-functions)
        - [Ladder operator](#ladder-operator)
      - [Quantum tunnelling](#quantum-tunnelling)
      - [Schrödinger equation solution for the hydrogen atom](#schrodinger-equation-solution-for-the-hydrogen-atom)
        - [Atomic orbital](#atomic-orbital)
        - [Quantum number](#quantum-number)
          - [Principal quantum number](#principal-quantum-number)
          - [Azimuthal quantum number](#azimuthal-quantum-number)
            - [s-orbital](#s-orbital)
            - [p-orbital](#p-orbital)
            - [d-orbital](#d-orbital)
            - [f-orbital](#f-orbital)
          - [Magnetic quantum number](#magnetic-quantum-number)
          - [Spin quantum number](#spin-quantum-number)
            - [Spectroscopic notation](#spectroscopic-notation)
      - [Solutions for the Schrodinger equation with multiple particles](#solutions-for-the-schrodinger-equation-with-multiple-particles)
        - [Separable state](#separable-state)
        - [Solutions of the Schrodinger equation for two electrons](#solutions-of-the-schrodinger-equation-for-two-electrons)
        - [Orbital approximation](#orbital-approximation)
        - [Schrödinger equation solution for the helium atom](#schrodinger-equation-solution-for-the-helium-atom)
        - [Hartree-Fock method](#hartree-fock-method)
          - [Hartree-Fock method for the helium atom](#hartree-fock-method-for-the-helium-atom)
          - [Why do multiple electrons occupy the same orbital if electrons repel each other?](#why-do-multiple-electrons-occupy-the-same-orbital-if-electrons-repel-each-other)
          - [Aufbau principle](#aufbau-principle)
            - [Electron configuration](#electron-configuration)
            - [Electron configuration notation](#electron-configuration-notation)
            - [Why does 2s have less energy than 1s if they have the same principal quantum number?](#why-does-2s-have-less-energy-than-1s-if-they-have-the-same-principal-quantum-number)
            - [Madelung energy ordering rule](#madelung-energy-ordering-rule)
              - [Exception to the Madelung energy ordering rule](#exception-to-the-madelung-energy-ordering-rule)
            - [Term symbol](#term-symbol)
              - [Hund's rules](#hund-s-rules)
                - [Hund's first rule](#hund-s-first-rule)
                - [Hund's second rule](#hund-s-second-rule)
        - [Term symbols for carbon ground state](#term-symbols-for-carbon-ground-state)
        - [Schrödinger equation solution for molecule](#schrodinger-equation-solution-for-molecule)
          - [Schrödinger equation solution for the hydrogen molecule](#schrodinger-equation-solution-for-the-hydrogen-molecule)
          - [Chemical bond](#chemical-bond)
            - [Molecule](#molecule)
              - [Molecule representation](#molecule-representation)
                - [Ball-and-stick model](#ball-and-stick-model)
              - [Isomer](#isomer)
                - [Cis-trans isomerism](#cis-trans-isomerism)
                - [Enantiomer](#enantiomer)
                - [Polymorphism (materials science)](#polymorphism-materials-science)
                - [Stereochemistry](#stereochemistry)
            - [Covalent bond](#covalent-bond)
              - [Sigma bond](#sigma-bond)
              - [Pi bond](#pi-bond)
                - [Double bond](#double-bond)
                - [Triple bond](#triple-bond)
            - [Ionic bond](#ionic-bond)
            - [Octet rule](#octet-rule)
      - [Two-state quantum system](#two-state-quantum-system)
        - [Bloch sphere](#bloch-sphere)
        - [Pauli matrix](#pauli-matrix)
    - [Born-Oppenheimer approximation](#born-oppenheimer-approximation)
    - [Uncertainty principle](#uncertainty-principle)
      - [Position and momentum space](#position-and-momentum-space)
        - [Position representation](#position-representation)
        - [Position operator](#position-operator)
        - [Momentum operator](#momentum-operator)
        - [Squeezed coherent state](#squeezed-coherent-state)
      - [Energy operator](#energy-operator)
        - [Time-energy uncertainty principle](#time-energy-uncertainty-principle)
      - [Angular momentum operator](#angular-momentum-operator)
        - [Total angular momentum operator](#total-angular-momentum-operator)
      - [Complementarity (physics)](#complementarity-physics)
    - [Conservation laws in Schrodinger equations](#conservation-laws-in-schrodinger-equations)
      - [Conservation of the square amplitude in the Schrodinger equation](#conservation-of-the-square-amplitude-in-the-schrodinger-equation)
        - [Probability current](#probability-current)
    - [Wave function](#wave-function)
      - [Matter wave](#matter-wave)
        - [Electron diffraction experiment](#electron-diffraction-experiment)
          - [Diffraction of Cathode Rays by a Thin Film by Thomson and Reid (1927)](#diffraction-of-cathode-rays-by-a-thin-film-by-thomson-and-reid-1927)
          - [Davisson-Germer experiment](#davisson-germer-experiment)
        - [de Broglie relations](#de-broglie-relations)
  - [Equivalent alternatives to the Schrodinger equation](#equivalent-alternatives-to-the-schrodinger-equation)
    - [Matrix mechanics](#matrix-mechanics)
      - [Quantum mechanical re-interpretation of kinematic and mechanical relations by Heisenberg (1925)](#quantum-mechanical-re-interpretation-of-kinematic-and-mechanical-relations-by-heisenberg-1925)
      - [Heisenberg picture](#heisenberg-picture)
    - [De Broglie-Bohm theory](#de-broglie-bohm-theory)
- [Planck-Einstein relation](#planck-einstein-relation)
  - [Planck constant](#planck-constant)
    - [Reduced Planck constant](#reduced-planck-constant)
- [Relativistic quantum mechanics](relativistic-quantum-mechanics.md)
  - [The Schrödinger equation is not relativistic](relativistic-quantum-mechanics.md#the-schrodinger-equation-is-not-relativistic)
  - [Dirac equation](relativistic-quantum-mechanics.md#dirac-equation)
    - [Absorption, spontaneous and stimulated emission](relativistic-quantum-mechanics.md#absorption-spontaneous-and-stimulated-emission)
      - [Spontaneous emission](relativistic-quantum-mechanics.md#spontaneous-emission)
        - [Spontaneous emission defies causality](relativistic-quantum-mechanics.md#spontaneous-emission-defies-causality)
      - [Photon absorption](relativistic-quantum-mechanics.md#photon-absorption)
      - [Stimulated emission](relativistic-quantum-mechanics.md#stimulated-emission)
        - [History of stimulated emission](relativistic-quantum-mechanics.md#history-of-stimulated-emission)
          - [On the Quantum Theory of Radiation](relativistic-quantum-mechanics.md#on-the-quantum-theory-of-radiation)
      - [Einstein coefficients](relativistic-quantum-mechanics.md#einstein-coefficients)
    - [The Dirac equation predicts spin](relativistic-quantum-mechanics.md#the-dirac-equation-predicts-spin)
    - [Antimatter](relativistic-quantum-mechanics.md#antimatter)
    - [Particle creation and annihilation](relativistic-quantum-mechanics.md#particle-creation-and-annihilation)
      - [Particle decay](relativistic-quantum-mechanics.md#particle-decay)
        - [Pair production](relativistic-quantum-mechanics.md#pair-production)
      - [Relativistic particle in a box thought experiment](relativistic-quantum-mechanics.md#relativistic-particle-in-a-box-thought-experiment)
    - [The Dirac equation is consistent with special relativity](relativistic-quantum-mechanics.md#the-dirac-equation-is-consistent-with-special-relativity)
    - [Derivation of the Dirac equation](relativistic-quantum-mechanics.md#derivation-of-the-dirac-equation)
    - [Pauli equation](relativistic-quantum-mechanics.md#pauli-equation)
    - [Klein-Gordon equation](relativistic-quantum-mechanics.md#klein-gordon-equation)
      - [Derivation of the Klein-Gordon equation](relativistic-quantum-mechanics.md#derivation-of-the-klein-gordon-equation)
    - [Solutions of the Dirac equation](relativistic-quantum-mechanics.md#solutions-of-the-dirac-equation)
      - [Dirac equation solution for the hydrogen atom](relativistic-quantum-mechanics.md#dirac-equation-solution-for-the-hydrogen-atom)
    - [Spin (physics)](relativistic-quantum-mechanics.md#spin-physics)
      - [Spin experiments](relativistic-quantum-mechanics.md#spin-experiments)
        - [Stern-Gerlach experiment](relativistic-quantum-mechanics.md#stern-gerlach-experiment)
          - [The Stern-Gerlach experiment needs an inhomogenous magnetic field](relativistic-quantum-mechanics.md#the-stern-gerlach-experiment-needs-an-inhomogenous-magnetic-field)
          - [Stern-Gerlach experiment paper](relativistic-quantum-mechanics.md#stern-gerlach-experiment-paper)
            - [The experimental proof of directional quantization in the magnetic field](relativistic-quantum-mechanics.md#the-experimental-proof-of-directional-quantization-in-the-magnetic-field)
        - [Spintronics](relativistic-quantum-mechanics.md#spintronics)
          - [Spin valve](relativistic-quantum-mechanics.md#spin-valve)
          - [Tunnel magnetoresistance](relativistic-quantum-mechanics.md#tunnel-magnetoresistance)
          - [Giant magnetoresistance](relativistic-quantum-mechanics.md#giant-magnetoresistance)
          - [Spin-transfer torque](relativistic-quantum-mechanics.md#spin-transfer-torque)
      - [Spin number of a field](relativistic-quantum-mechanics.md#spin-number-of-a-field)
        - [Spin 0](relativistic-quantum-mechanics.md#spin-0)
        - [Spin half](relativistic-quantum-mechanics.md#spin-half)
        - [Spin 1](relativistic-quantum-mechanics.md#spin-1)
          - [Proca equation](relativistic-quantum-mechanics.md#proca-equation)
        - [Spin 2](relativistic-quantum-mechanics.md#spin-2)
        - [Why is the spin of the electron half?](relativistic-quantum-mechanics.md#why-is-the-spin-of-the-electron-half)
      - [Pauli exclusion principle](relativistic-quantum-mechanics.md#pauli-exclusion-principle)
        - [Slater determinant](relativistic-quantum-mechanics.md#slater-determinant)
        - [Fermions, bosons and anyons](relativistic-quantum-mechanics.md#fermions-bosons-and-anyons)
          - [Fermion](relativistic-quantum-mechanics.md#fermion)
          - [Boson](relativistic-quantum-mechanics.md#boson)
          - [Anyon](relativistic-quantum-mechanics.md#anyon)
            - [Abelian an non abelian anyons](relativistic-quantum-mechanics.md#abelian-an-non-abelian-anyons)
              - [Abelian anyon](relativistic-quantum-mechanics.md#abelian-anyon)
              - [Non Abelian anyon](relativistic-quantum-mechanics.md#non-abelian-anyon)
        - [Spin-statistics theorem](relativistic-quantum-mechanics.md#spin-statistics-theorem)
        - [Electron degeneracy pressure](relativistic-quantum-mechanics.md#electron-degeneracy-pressure)
    - [Dirac Lagrangian](relativistic-quantum-mechanics.md#dirac-lagrangian)
      - [Dirac adjoint](relativistic-quantum-mechanics.md#dirac-adjoint)
      - [Gamma matrices](relativistic-quantum-mechanics.md#gamma-matrices)
      - [Feynman slash notation](relativistic-quantum-mechanics.md#feynman-slash-notation)
  - [Quantum field theory](quantum-field-theory.md)
    - [Quantum field](quantum-field-theory.md#quantum-field)
    - [Mathematical formulation of quantum field theory](quantum-field-theory.md#mathematical-formulation-of-quantum-field-theory)
      - [Gauge theory](quantum-field-theory.md#gauge-theory)
        - [Lattice gauge theory](quantum-field-theory.md#lattice-gauge-theory)
        - [Gauge field](quantum-field-theory.md#gauge-field)
        - [Gauge symmetry](quantum-field-theory.md#gauge-symmetry)
      - [Fock space](quantum-field-theory.md#fock-space)
      - [Second quantization](quantum-field-theory.md#second-quantization)
        - [Canonical quantization](quantum-field-theory.md#canonical-quantization)
      - [Path integral formulation](quantum-field-theory.md#path-integral-formulation)
        - [Quantum particles take all possible paths](quantum-field-theory.md#quantum-particles-take-all-possible-paths)
        - [Propagator](quantum-field-theory.md#propagator)
        - [Infinitely many slits thought experiment](quantum-field-theory.md#infinitely-many-slits-thought-experiment)
      - [Renormalization](quantum-field-theory.md#renormalization)
        - [Mass renormalization](quantum-field-theory.md#mass-renormalization)
        - [Renormalization group](quantum-field-theory.md#renormalization-group)
        - [Cutoff energy](quantum-field-theory.md#cutoff-energy)
        - [Effective field theory](quantum-field-theory.md#effective-field-theory)
        - [Yang-Mills theory](quantum-field-theory.md#yang-mills-theory)
          - [Yang-Mills existence and mass gap](quantum-field-theory.md#yang-mills-existence-and-mass-gap)
            - [Wightman axioms](quantum-field-theory.md#wightman-axioms)
    - [Quantum electrodynamics](quantum-field-theory.md#quantum-electrodynamics)
      - [Quantum electrodynamics experiment](quantum-field-theory.md#quantum-electrodynamics-experiment)
        - [Lamb shift](quantum-field-theory.md#lamb-shift)
          - [Lamb-Retherford experiment](quantum-field-theory.md#lamb-retherford-experiment)
        - [Electron magnetic moment](quantum-field-theory.md#electron-magnetic-moment)
          - [Anomalous magnetic dipole moment](quantum-field-theory.md#anomalous-magnetic-dipole-moment)
            - [Anomalous magnetic dipole moment of the electron](quantum-field-theory.md#anomalous-magnetic-dipole-moment-of-the-electron)
              - [The Magnetic Moment of the Electron by Kusch and Foley (1948)](quantum-field-theory.md#the-magnetic-moment-of-the-electron-by-kusch-and-foley-1948)
        - [Dirac equation vs quantum electrodynamics](quantum-field-theory.md#dirac-equation-vs-quantum-electrodynamics)
          - [The Dirac equation does not work for more than one electron](quantum-field-theory.md#the-dirac-equation-does-not-work-for-more-than-one-electron)
      - [Applications of quantum electrodynamics](quantum-field-theory.md#applications-of-quantum-electrodynamics)
      - [Quantum electrodynamics Lagrangian](quantum-field-theory.md#quantum-electrodynamics-lagrangian)
        - [Derivation of the quantum electrodynamics Lagrangian](quantum-field-theory.md#derivation-of-the-quantum-electrodynamics-lagrangian)
      - [What does it mean that photons are force carriers for electromagnetism?](quantum-field-theory.md#what-does-it-mean-that-photons-are-force-carriers-for-electromagnetism)
      - [Photon field](quantum-field-theory.md#photon-field)
      - [Schwinger effect](quantum-field-theory.md#schwinger-effect)
      - [Feynman diagram](quantum-field-theory.md#feynman-diagram)
        - [Feynman diagram solver](quantum-field-theory.md#feynman-diagram-solver)
        - [Does the exact position of vertices matter in Feynman diagrams?](quantum-field-theory.md#does-the-exact-position-of-vertices-matter-in-feynman-diagrams)
      - [Wheeler-Feynman absorber theory](quantum-field-theory.md#wheeler-feynman-absorber-theory)
      - [Cavity quantum electrodynamics](quantum-field-theory.md#cavity-quantum-electrodynamics)
        - [Circuit quantum electrodynamics](quantum-field-theory.md#circuit-quantum-electrodynamics)
      - [Positrons are electrons travelling back in time](quantum-field-theory.md#positrons-are-electrons-travelling-back-in-time)
      - [Quantum electrodynamics bibliography](quantum-field-theory.md#quantum-electrodynamics-bibliography)
        - [Quantum Theory of Radiation by Fermi (1932)](quantum-field-theory.md#quantum-theory-of-radiation-by-fermi-1932)
        - [Advanced quantum mechanics by Freeman Dyson (1951)](quantum-field-theory.md#advanced-quantum-mechanics-by-freeman-dyson-1951)
        - [Selected Papers on Quantum Electrodynamics by Julian Schwinger (1958)](quantum-field-theory.md#selected-papers-on-quantum-electrodynamics-by-julian-schwinger-1958)
        - [Richard Feynman Quantum Electrodynamics Lecture at University of Auckland (1979)](quantum-field-theory.md#richard-feynman-quantum-electrodynamics-lecture-at-university-of-auckland-1979)
          - [Quantum Mechanical View of Reality by Richard Feynman (1983)](quantum-field-theory.md#quantum-mechanical-view-of-reality-by-richard-feynman-1983)
        - [Quantum electrodynamics by Lifshitz et al. 2nd edition (1982)](quantum-field-theory.md#quantum-electrodynamics-by-lifshitz-et-al-2nd-edition-1982)
        - [Physics 253a by Sidney Coleman (1986)](quantum-field-theory.md#physics-253a-by-sidney-coleman-1986)
        - [QED and the men who made it: Dyson, Feynman, Schwinger, and Tomonaga by Silvan Schweber (1994)](quantum-field-theory.md#qed-and-the-men-who-made-it-dyson-feynman-schwinger-and-tomonaga-by-silvan-schweber-1994)
        - [Advanced quantum mechanics II by Douglas Gingrich (2004)](quantum-field-theory.md#advanced-quantum-mechanics-ii-by-douglas-gingrich-2004)
    - [Weak interaction](quantum-field-theory.md#weak-interaction)
      - [Electroweak interaction](quantum-field-theory.md#electroweak-interaction)
      - [Parity violation](quantum-field-theory.md#parity-violation)
        - [Wu experiment](quantum-field-theory.md#wu-experiment)
        - [CP Violation](quantum-field-theory.md#cp-violation)
          - [CPT symmetry](quantum-field-theory.md#cpt-symmetry)
          - [Strong CP problem](quantum-field-theory.md#strong-cp-problem)
      - [Weak charge](quantum-field-theory.md#weak-charge)
      - [W boson](quantum-field-theory.md#w-boson)
      - [Z boson](quantum-field-theory.md#z-boson)
    - [Quantum chromodynamics](quantum-field-theory.md#quantum-chromodynamics)
      - [Quark](quantum-field-theory.md#quark)
        - [Down quark](quantum-field-theory.md#down-quark)
        - [Up quark](quantum-field-theory.md#up-quark)
          - [Why do the up ad down quarks have different masses?](quantum-field-theory.md#why-do-the-up-ad-down-quarks-have-different-masses)
      - [Strange quark](quantum-field-theory.md#strange-quark)
      - [Gluon](quantum-field-theory.md#gluon)
        - [Glueball](quantum-field-theory.md#glueball)
      - [Proton decay](quantum-field-theory.md#proton-decay)
      - [Strong interaction](quantum-field-theory.md#strong-interaction)
      - [Color charge](quantum-field-theory.md#color-charge)
      - [Color confinement](quantum-field-theory.md#color-confinement)
    - [Quantum field theory simulations](quantum-field-theory.md#quantum-field-theory-simulations)
      - [Nielsen-Ninomiya theorem](quantum-field-theory.md#nielsen-ninomiya-theorem)
    - [Infinities in quantum field theory](quantum-field-theory.md#infinities-in-quantum-field-theory)
      - [Mathematical consistency of quantum field theory](quantum-field-theory.md#mathematical-consistency-of-quantum-field-theory)
    - [Internal and spacetime symmetries](quantum-field-theory.md#internal-and-spacetime-symmetries)
      - [Internal symmetry](quantum-field-theory.md#internal-symmetry)
      - [Spacetime symmetry](quantum-field-theory.md#spacetime-symmetry)
    - [Quantum field theory bibliography](quantum-field-theory.md#quantum-field-theory-bibliography)
      - [Quantum field theory lecture notes](quantum-field-theory.md#quantum-field-theory-lecture-notes)
        - [An Introduction to QED and QCD by Jeff Forshaw (1997)](quantum-field-theory.md#an-introduction-to-qed-and-qcd-by-jeff-forshaw-1997)
        - [Quantum Field Theory lecture notes by David Tong (2007)](quantum-field-theory.md#quantum-field-theory-lecture-notes-by-david-tong-2007)
        - [Quantum Field Theory book by Mark Srednicki (2006)](quantum-field-theory.md#quantum-field-theory-book-by-mark-srednicki-2006)
      - [Quantum field theory lectures](quantum-field-theory.md#quantum-field-theory-lectures)
        - [Relativistic Quantum Mechanics by Apoorva D Patel (2014)](quantum-field-theory.md#relativistic-quantum-mechanics-by-apoorva-d-patel-2014)
        - [New Revolutions in Particle Physics by Leonard Susskind (2009)](quantum-field-theory.md#new-revolutions-in-particle-physics-by-leonard-susskind-2009)
        - [David Tong's 2009 Quantum Field Theory lectures at the Perimeter Institute](quantum-field-theory.md#david-tong-s-2009-quantum-field-theory-lectures-at-the-perimeter-institute)
          - [Lecture 1](quantum-field-theory.md#david-tong-s-2009-quantum-field-theory-lectures-at-the-perimeter-institute/lecture-1)
        - [Quantum field theory courses by Tobias Osborne](quantum-field-theory.md#quantum-field-theory-courses-by-tobias-osborne)
          - [Quantum field theory lecture by Tobias Osborne (2017)](quantum-field-theory.md#quantum-field-theory-lecture-by-tobias-osborne-2017)
            - [Lecture 1](quantum-field-theory.md#quantum-field-theory-lecture-by-tobias-osborne-2017/lecture-1)
            - [Lecture 2](quantum-field-theory.md#quantum-field-theory-lecture-by-tobias-osborne-2017/lecture-2)
            - [Lecture 3](quantum-field-theory.md#quantum-field-theory-lecture-by-tobias-osborne-2017/lecture-3)
            - [Lecture 4](quantum-field-theory.md#quantum-field-theory-lecture-by-tobias-osborne-2017/lecture-4)
            - [Lecture 5](quantum-field-theory.md#quantum-field-theory-lecture-by-tobias-osborne-2017/lecture-5)
            - [Lecture 8](quantum-field-theory.md#quantum-field-theory-lecture-by-tobias-osborne-2017/lecture-8)
            - [Lecture 9](quantum-field-theory.md#quantum-field-theory-lecture-by-tobias-osborne-2017/lecture-9)
            - [Lecture 14](quantum-field-theory.md#quantum-field-theory-lecture-by-tobias-osborne-2017/lecture-14)
            - [Lecture 15](quantum-field-theory.md#quantum-field-theory-lecture-by-tobias-osborne-2017/lecture-15)
          - [Advanced quantum field theory lecture by Tobias Osborne (2017)](quantum-field-theory.md#advanced-quantum-field-theory-lecture-by-tobias-osborne-2017)
            - [Lecture 2](quantum-field-theory.md#advanced-quantum-field-theory-lecture-by-tobias-osborne-2017/lecture-2)
      - [Quantum field theory book](quantum-field-theory.md#quantum-field-theory-book)
        - [No-Nonsense Quantum Field Theory by Jakob Schwichtenberg (2020)](quantum-field-theory.md#no-nonsense-quantum-field-theory-by-jakob-schwichtenberg-2020)
        - [Quantum Field Theory for The Gifted Amateur by Tom Lancaster (2015)](quantum-field-theory.md#quantum-field-theory-for-the-gifted-amateur-by-tom-lancaster-2015)
        - [Student Friendly Quantum Field Theory by Robert D Klauber (2013)](quantum-field-theory.md#student-friendly-quantum-field-theory-by-robert-d-klauber-2013)
        - [Quantum field theory in a nutshell by Anthony Zee (2010)](quantum-field-theory.md#quantum-field-theory-in-a-nutshell-by-anthony-zee-2010)
        - [Problem Book in Quantum Field Theory by Voja Radovanovic (2008)](quantum-field-theory.md#problem-book-in-quantum-field-theory-by-voja-radovanovic-2008)
        - [Quantum Field Theory Demystified by David McMahon (2008)](quantum-field-theory.md#quantum-field-theory-demystified-by-david-mcmahon-2008)
        - [An Introduction To Quantum Field Theory by Peskin and Schroeder (1995)](quantum-field-theory.md#an-introduction-to-quantum-field-theory-by-peskin-and-schroeder-1995)
- [Quantization (physics)](#quantization-physics)
  - [Quantization of a real scalar field](#quantization-of-a-real-scalar-field)
- [Quantum superposition](#quantum-superposition)
- [Quantum entanglement](#quantum-entanglement)
  - [Bell's theorem](#bell-s-theorem)
    - [Bell test experiment](#bell-test-experiment)
      - [Loopholes in Bell test experiments](#loopholes-in-bell-test-experiments)
    - [Local hidden-variable theory](#local-hidden-variable-theory)
- [No-go theorem](#no-go-theorem)

## Quantum mechanics experiment

↑ **Parent:** [Quantum mechanics](quantum-mechanics.md)

Atoms exist and last for a long time, while in [classical electromagnetic theory punctual](electromagnetism.md#maxwell-s-equations) orbiting electrons should emit radiation quickly and fall into the nucleus: [https://physics.stackexchange.com/questions/20003/why-dont-electrons-crash-into-the-nuclei-they-orbit](https://physics.stackexchange.com/questions/20003/why-dont-electrons-crash-into-the-nuclei-they-orbit)

In other sections:
- [black-body radiation experiment](condensed-matter-physics.md#black-body-radiation-experiment)
  - [Einstein solid](condensed-matter-physics.md#einstein-solid) experiments, which are analogous to black body radiation experiments
- [emission spectrum](#emission-spectrum)
- [electron diffraction experiments](#electron-diffraction-experiment) such as:
  - [Davisson-Germer experiment](#davisson-germer-experiment)

Bibliography:
- [http://web.mit.edu/course/5/5.73/oldwww/Fall04/notes/Experimental_Evidence_for_Quantum_Mechanics.pdf](http://web.mit.edu/course/5/5.73/oldwww/Fall04/notes/Experimental_Evidence_for_Quantum_Mechanics.pdf) Experimental Evidence for Quantum Mechanics

### Emission spectrum

↑ **Parent:** [Quantum mechanics experiment](#quantum-mechanics-experiment)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Emission_spectrum)

#### Spectral line

↑ **Parent:** [Emission spectrum](#emission-spectrum)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Spectral_line)

A single line in the [emission spectrum](#emission-spectrum).

So precise, so [discrete](calculus.md#discrete), which makes no sense in [classical mechanics](mechanics.md#classical-mechanics)!

Has been the leading motivation of the development of [quantum mechanics](quantum-mechanics.md), all the way from the:
- [Schrödinger equation](#schrodinger-equation): major lines predicted, including [Zeeman effect](#zeeman-effect), but not finer line splits like [fine structure](#fine-structure)
- [Dirac equation](relativistic-quantum-mechanics.md#dirac-equation): explains [fine structure](#fine-structure) 2p spin split due to electron spin/orbit interactions, but not [Lamb shift](quantum-field-theory.md#lamb-shift)
- [quantum electrodynamics](quantum-field-theory.md#quantum-electrodynamics): explains [Lamb shift](quantum-field-theory.md#lamb-shift)
- [hyperfine structure](#hyperfine-structure): due to electron/nucleus spin interactions, offers a window into [nuclear spin](particle-physics.md#nuclear-magnetic-moment)

##### NIST Atomic Spectra Database

↑ **Parent:** [Spectral line](#spectral-line)

[NIST](research-institute.md#national-institute-of-standards-and-technology) database for [spectral line](#spectral-line): [https://physics.nist.gov/PhysRefData/ASD/lines_form.html](https://physics.nist.gov/PhysRefData/ASD/lines_form.html)

Let's do a sanity check.

Searching for "H" for [hydrogen](chemistry.md#hydrogen) leads to: [https://physics.nist.gov/cgi-bin/ASD/lines1.pl?spectra=H&limits_type=0&low_w=&upp_w=&unit=1&submit=Retrieve+Data&de=0&format=0&line_out=0&en_unit=0&output=0&bibrefs=1&page_size=15&show_obs_wl=1&show_calc_wl=1&unc_out=1&order_out=0&max_low_enrg=&show_av=2&max_upp_enrg=&tsb_value=0&min_str=&A_out=0&intens_out=on&max_str=&allowed_out=1&forbid_out=1&min_accur=&min_intens=&conf_out=on&term_out=on&enrg_out=on&J_out=on](https://physics.nist.gov/cgi-bin/ASD/lines1.pl?spectra=H&limits_type=0&low_w=&upp_w=&unit=1&submit=Retrieve+Data&de=0&format=0&line_out=0&en_unit=0&output=0&bibrefs=1&page_size=15&show_obs_wl=1&show_calc_wl=1&unc_out=1&order_out=0&max_low_enrg=&show_av=2&max_upp_enrg=&tsb_value=0&min_str=&A_out=0&intens_out=on&max_str=&allowed_out=1&forbid_out=1&min_accur=&min_intens=&conf_out=on&term_out=on&enrg_out=on&J_out=on)

From there we can see for example the 1 to 2 lines:
- 1s to 2p: 121.5673644608 nm
- 1s to 2: 121.56701 nm TODO what does that $2$ mean?
- 1s to 2s: 121.5673123130200 TODO what does that mean?

We see that the table is sorted from lower from level first and then by upper level second.

So it is good to see that we are in the same 121nm ballpark as mentioned at [hydrogen spectral line](#hydrogen-emission-spectrum).

TODO why I can't see 2s to 2p transitions there to get the [fine structure](#fine-structure)?

##### Forbidden mechanism

↑ **Parent:** [Spectral line](#spectral-line)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Forbidden_mechanism)

Bibliography:
- [https://phys.libretexts.org/Bookshelves/Quantum_Mechanics/Introductory_Quantum_Mechanics_(Fitzpatrick)/12%3A_Time-Dependent_Perturbation_Theory/12.13%3A_Forbidden_Transitions](https://phys.libretexts.org/Bookshelves/Quantum_Mechanics/Introductory_Quantum_Mechanics_(Fitzpatrick)/12%3A_Time-Dependent_Perturbation_Theory/12.13%3A_Forbidden_Transitions) from [Introductory Quantum Mechanics by Richard Fitzpatrick (2020)](#introductory-quantum-mechanics-by-richard-fitzpatrick-2020)

###### Selection rule

↑ **Parent:** [Forbidden mechanism](#forbidden-mechanism)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Selection_rule)

[https://phys.libretexts.org/Courses/University_of_California_Davis/UCD%3A_Physics_9HE_-_Modern_Physics/06%3A_Emission_and_Absorption_of_Photons/6.2%3A_Selection_Rules_and_Transition_Times](https://phys.libretexts.org/Courses/University_of_California_Davis/UCD%3A_Physics_9HE_-_Modern_Physics/06%3A_Emission_and_Absorption_of_Photons/6.2%3A_Selection_Rules_and_Transition_Times) has some very good mentions:

> So it appears that if a hydrogen atom emits a photon, it not only has to transition between two states whose energy difference matches the energy of the photon, but it is restricted in other ways as well, if its mode of radiation is to be dipole. For example, a hydrogen atom in its 3p state must drop to either the n=1 or n=2 energy level, to make the energy available to the photon. The n=2 energy level is 4-fold degenerate, and including the single n=1 state, the atom has five different states to which it can transition. But three of the states in the n=2 energy level have l=1 (the 2p states), so transitioning to these states does not involve a change in the angular momentum quantum number, and the dipole mode is not available.
> 
> So what's the big deal? Why doesn't the hydrogen atom just use a quadrupole or higher-order mode for this transition? It can, but the characteristic time for the dipole mode is so much shorter than that for the higher-order modes, that by the time the atom gets around to transitioning through a higher-order mode, it has usually already done so via dipole. All of this is statistical, of course, meaning that in a large collection of hydrogen atoms, many different modes of transitions will occur, but the vast majority of these will be dipole.
> 
> It turns out that examining details of these restrictions introduces a couple more. These come about from the conservation of angular momentum. It turns out that photons have an intrinsic angular momentum (spin) magnitude of $\hbar$, which means whenever a photon (emitted or absorbed) causes a transition in a hydrogen atom, the value of l must change (up or down) by exactly 1. This in turn restricts the changes that can occur to the magnetic quantum number: $m_l$ can change by no more than 1 (it can stay the same). We have dubbed these transition restrictions selection rules, which we summarize as:
> 
> $$
> \Delta l = \pm 1, \Delta m_l = 0, \pm 1
> $$

###### Metastable electron

↑ **Parent:** [Selection rule](#selection-rule)  
🏷️ **Tags:** [Selection rule](#selection-rule)

A fundamental component of [three-level lasers](condensed-matter-physics.md#three-level-laser).

As mentioned at [https://youtu.be/_JOchLyNO_w?t=581](https://youtu.be/_JOchLyNO_w?t=581) from [Video "How Lasers Work by Scientized (2017)"](condensed-matter-physics.md#video-how-lasers-work-by-scientized-2017), they stay in that state for a long time compared to non [spontaneous emission](relativistic-quantum-mechanics.md#spontaneous-emission) of metastable states!

[https://phys.libretexts.org/Courses/University_of_California_Davis/UCD%3A_Physics_9HE_-_Modern_Physics/06%3A_Emission_and_Absorption_of_Photons/6.3%3A_Lasers](https://phys.libretexts.org/Courses/University_of_California_Davis/UCD%3A_Physics_9HE_-_Modern_Physics/06%3A_Emission_and_Absorption_of_Photons/6.3%3A_Lasers) mentions that they are kept in that excited state due to [selection rules](#selection-rule).

This is also one of mechanisms behind [phosphorescence](condensed-matter-physics.md#phosphorescence) with [triplet states](#triplet-state).

###### Triplet state

↑ **Parent:** [Metastable electron](#metastable-electron)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Triplet_state)

![](https://upload.wikimedia.org/wikipedia/commons/7/7e/Spin_multiplicity_diagram.svg)

**[Figure 1](#_58)** [Source](https://commons.wikimedia.org/wiki/File:Spin_multiplicity_diagram.svg).

##### Rydberg atom

↑ **Parent:** [Spectral line](#spectral-line)

##### Hydrogen emission spectrum

↑ **Parent:** [Spectral line](#spectral-line)

###### Gross hydrogen emission spectrum

↑ **Parent:** [Hydrogen emission spectrum](#hydrogen-emission-spectrum)

One reasonable and memorable approximation excluding any [fine structure](#fine-structure) is:<a id="equation-hydrogen-spectral-series-mnemonic"></a>


$$
E_n = -\frac{13.6eV}{n^2}
$$

see for example example: [hydrogen 1-2 spectral line](#hydrogen-1-2-spectral-line).

###### Hydrogen 1-2 spectral line

↑ **Parent:** [Gross hydrogen emission spectrum](#gross-hydrogen-emission-spectrum)

[Equation 2. "Hydrogen spectral series mnemonic"](#equation-hydrogen-spectral-series-mnemonic) gives for example from [principal quantum number](#principal-quantum-number) 1 to 2 a difference:

$$
E_n = -13.6eV\left[\frac{1}{2^2} - \frac{1}{1^2}\right] = 10.2 eV
$$

which with [Planck-Einstein relation](#planck-einstein-relation) gives about 121.6 [nm](system-of-units.md#nanometer) ($2.47 \times 10^15$ [Hz](system-of-units.md#hertz)), which is a reasonable match with the value of 121.567... from the [NIST Atomic Spectra Database](#nist-atomic-spectra-database).

###### Rydberg formula

↑ **Parent:** [Hydrogen emission spectrum](#hydrogen-emission-spectrum)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Rydberg_formula)

###### Balmer series

↑ **Parent:** [Rydberg formula](#rydberg-formula)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Balmer_series)

###### Hydrogen spectral series

↑ **Parent:** [Hydrogen emission spectrum](#hydrogen-emission-spectrum)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Hydrogen_spectral_series)

Kind of a synonym for [hydrogen emission spectrum](#hydrogen-emission-spectrum) not very clear if [fine structure](#fine-structure) is considered by this term or not.

A line set for [hydrogen spectral line](#hydrogen-emission-spectrum).

Formula discovered in 1885, was it the first set to have an empirical formula?

###### Pickering series

↑ **Parent:** [Hydrogen spectral series](#hydrogen-spectral-series)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Pickering_series)

##### Fine structure

↑ **Parent:** [Spectral line](#spectral-line)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Fine_structure)

Split in energy levels due to interaction between electron up or down [spin](relativistic-quantum-mechanics.md#spin-physics) and the electron orbitals.

Numerically explained by the [Dirac equation](relativistic-quantum-mechanics.md#dirac-equation) when [solving it for the hydrogen atom](relativistic-quantum-mechanics.md#dirac-equation-solution-for-the-hydrogen-atom), and it is one of the main triumphs of the theory.

###### Fine structure constant

↑ **Parent:** [Fine structure](#fine-structure)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Fine_structure_constant)

###### Hyperfine structure

↑ **Parent:** [Fine structure](#fine-structure)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Hyperfine_structure)

Small splits present in all levels due to interaction between the electron spin and the [nuclear spin](particle-physics.md#nuclear-magnetic-moment) if it is present, i.e. the nucleus has an even number of nucleons.

As the name suggests, this energy split is very small, since the influence of the nucleus spin on the electron spin is relatively small compared to other [fine structure](#fine-structure).

TODO confirm: does it need [quantum electrodynamics](quantum-field-theory.md#quantum-electrodynamics) or is the [Dirac equation](relativistic-quantum-mechanics.md#dirac-equation) enough?

The most important examples:
- [hydrogen line](#hydrogen-line) useful in astronomy, and also the simplest possible case between 1s
- [caesium standard](system-of-units.md#caesium-standard), which is used to define the [second](system-of-units.md#second) in the [International System of Units](system-of-units.md#international-system-of-units) since 1967.

###### Hydrogen line

↑ **Parent:** [Hyperfine structure](#hyperfine-structure)  
🏷️ **Tags:** [Hydrogen emission spectrum](#hydrogen-emission-spectrum)

21 cm is very long and very low energy, because he energy split is very small!

Compare it e.g. with the [hydrogen 1-2 spectral line](#hydrogen-1-2-spectral-line) which is 121.6 nm!

##### Zeeman effect

↑ **Parent:** [Spectral line](#spectral-line)  
🏷️ **Tags:** [1902 Nobel Prize in Physics](nobel-prize.md#1902-nobel-prize-in-physics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Zeeman_effect)

Split in the [spectral line](#spectral-line) when a [magnetic field](electromagnetism.md#magnetic-field) is applied.

Non-anomalous: number of splits matches predictions of the [Schrödinger equation](#schrodinger-equation) about the number of possible states with a given angular momentum. TODO does it make numerical predictions?

[Anomalous](#anomalous-zeeman-effect): evidence of [spin](relativistic-quantum-mechanics.md#spin-physics).

[http://www.pas.rochester.edu/~blackman/ast104/zeeman-split.html](http://www.pas.rochester.edu/~blackman/ast104/zeeman-split.html) contains the hello world that everyone should know: 2p splits into 3 energy levels, so you see 3 spectral lines from 1s to 2p rather than just one.

p splits into 3, d into 5, f into 7 and so on, i.e. one for each possible [azimuthal quantum number](#azimuthal-quantum-number).

It also mentions that polarization effects become visible from this: each line is polarized in a different way. TODO more details as in an experiment to observe this.

Well explained at: [Video 19. "Quantum Mechanics 7a - Angular Momentum I by ViaScience (2013)"](#video-quantum-mechanics-7a-angular-momentum-i-by-viascience-2013).

<a id="video-experimental-physics-iv-22-zeeman-effect-by-lehrportal-uni-gottingen-2020"></a>
**[Video 1](#video-experimental-physics-iv-22-zeeman-effect-by-lehrportal-uni-gottingen-2020). Experimental physics - IV: 22 - Zeeman effect by Lehrportal Uni Gottingen (2020)** [Source](https://www.youtube.com/watch?v=ZmObNFAqkBE). This one is decent. Uses a [cadmium](chemistry.md#cadmium) lamp and an [etalon](photon.md#fabry-perot-interferometer) on an [optical table](photon.md#optical-table). They see a more or less clear 3-split in a circular [interference pattern](calculus.md#interference-pattern),

They filter out all but the transition of interest.


- [https://youtu.be/ZmObNFAqkBE?t=165](https://youtu.be/ZmObNFAqkBE?t=165) passes the lines through a [polarizer](photon.md#polarizer), which shows how orbital angular momentum is carried by [photon polarization](photon.md#photon-polarization)
- [https://youtu.be/ZmObNFAqkBE?t=370](https://youtu.be/ZmObNFAqkBE?t=370) says they are looking at 1D2 to 1P1 changes.

---

<a id="video-zeeman-effect-control-light-with-magnetic-fields-by-applied-science-youtube-channel-2018"></a>
**[Video 2](#video-zeeman-effect-control-light-with-magnetic-fields-by-applied-science-youtube-channel-2018). Zeeman Effect - Control light with magnetic fields by Applied Science (2018)** [Source](https://www.youtube.com/watch?v=OzkcB1lkgGU). Does not appear to achieve a crystal clear split unfortunately.

###### Anomalous Zeeman effect

↑ **Parent:** [Zeeman effect](#zeeman-effect)

### Double-slit experiment

↑ **Parent:** [Quantum mechanics experiment](#quantum-mechanics-experiment)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Double-slit_experiment)

Amazingly confirms the wave particle duality of [quantum mechanics](quantum-mechanics.md).

The effect is even more remarkable when done with individual particles such individual [photons](photon.md) or [electrons](standard-model.md#electron).

[Richard Feynman](richard-feynman.md) liked to stress how this experiment can illustrate the core ideas of [quantum mechanics](quantum-mechanics.md). Notably, he night have created the [infinitely many slits thought experiment](quantum-field-theory.md#infinitely-many-slits-thought-experiment) which illustrates the [path integral formulation](quantum-field-theory.md#path-integral-formulation).

#### Single particle double slit experiment

↑ **Parent:** [Double-slit experiment](#double-slit-experiment)

This experiment seems to be really hard to do, and so there aren't many super clear demonstration videos with full experimental setup description out there unfortunately.

Wikipedia has a good summary at: [https://en.wikipedia.org/wiki/Double-slit_experiment#Overview](https://en.wikipedia.org/wiki/Double-slit_experiment#Overview)

For single-[photon](photon.md) non-[double-slit experiments](#double-slit-experiment) see: [single photon production and detection experiments](photon.md#single-photon-production-and-detection). Those are basically a pre-requisite to this.

[photon](photon.md) experiments:
- [https://aapt.scitation.org/doi/full/10.1119/1.4955173](https://aapt.scitation.org/doi/full/10.1119/1.4955173) "Video recording true single-photon double-slit interference" by Aspden and Padgetta (2016). Abstract says using [spontaneous parametric down-conversion](photon.md#spontaneous-parametric-down-conversion) detection of the second photon to know when to turn the camera on

[electron](standard-model.md#electron) experiments: [single electron double slit experiment](#single-electron-double-slit-experiment).

Non-[elementary particle](standard-model.md#elementary-particle):
- 2019-10-08: 25,000 Daltons
- [https://interactive.quantumnano.at/letsgo/](https://interactive.quantumnano.at/letsgo/) awesome interactive demo that allows you to control many parameters on a lab. Written in Flash unfortunately, in 2015... what a lack of future proofing!

<a id="video-single-photon-interference-by-veritasium-2013"></a>
**[Video 3](#video-single-photon-interference-by-veritasium-2013). Single Photon Interference by Veritasium (2013)** [Source](https://www.youtube.com/watch?v=GzbKb59my3U). Claims to do exactly what we want, but does not describe the setup precisely well enough. Notably, does not justify how he knows that single photons are being produced.

##### Single electron double slit experiment

↑ **Parent:** [Single particle double slit experiment](#single-particle-double-slit-experiment)  
🏷️ **Tags:** [Electron diffraction experiment](#electron-diffraction-experiment)

<a id="video-electron-interference-by-the-italian-national-research-council-1976"></a>
**[Video 4](#video-electron-interference-by-the-italian-national-research-council-1976). Electron Interference by the Italian National Research Council (1976)** [Source](https://www.youtube.com/watch?v=zc-iyjpzzGQ). Institutional video about the 1974 single electron experiment by Merli, Missiroli, Pozzi from the [University of Bologna](https://en.wikipedia.org/wiki/University_of_Bologna).

Uses an electron biprism as in [electron holography](microscopy.md#electron-holography) inside a [transmission electron microscope](microscopy.md#transmission-electron-microscopy).

Shows them manually making the biprism by drawing a fine glass wire and coating it with gold.

Then actually show the result live on a television screen, where you see the interference patterns only at higher electron currents, and then on photographic film.

This was elected "the most beautiful experiment" by readers of Physics World in 2002.

Accompanying website: [http://l-esperimento-piu-bello-della-fisica.bo.imm.cnr.it/english/index.html](http://l-esperimento-piu-bello-della-fisica.bo.imm.cnr.it/english/index.html).

Italian title: "Interferenza di elettroni". Goddammit, those Italian cinematographers can make even [physics](physics.md) look exciting!

---

#### Are particles bounced by the first wall in the double slit experiment?

↑ **Parent:** [Double-slit experiment](#double-slit-experiment)

[https://physics.stackexchange.com/questions/443358/in-the-double-slit-experiment-why-is-it-never-shown-that-particles-may-hit-the/573455#573455](https://physics.stackexchange.com/questions/443358/in-the-double-slit-experiment-why-is-it-never-shown-that-particles-may-hit-the/573455#573455)

It would be amazing to answer this with [single particle double slit experiment](#single-particle-double-slit-experiment) measurements!

### Franck-Hertz experiment

↑ **Parent:** [Quantum mechanics experiment](#quantum-mechanics-experiment)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Franck–Hertz_experiment)

### Quantum Hall effect

↑ **Parent:** [Quantum mechanics experiment](#quantum-mechanics-experiment)  
🏷️ **Tags:** [Hall effect](electromagnetism.md#hall-effect), [Physics experiment without a decent modern video](physics.md#physics-experiment-without-a-decent-modern-video)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Quantum_Hall_effect)

Quantum version of the [Hall effect](electromagnetism.md#hall-effect).

As you increase the [magnetic field](electromagnetism.md#magnetic-field), you can see the [Hall resistance](electromagnetism.md#hall-resistance) increase, but it does so in discrete steps.

<a id="image-hall-resistance-as-a-function-of-the-applied-magnetic-field-showing-the-quantum-hall-effect"></a>
![](https://upload.wikimedia.org/wikipedia/commons/3/38/Rhoxy.jpg)

**[Figure 2](#image-hall-resistance-as-a-function-of-the-applied-magnetic-field-showing-the-quantum-hall-effect). Hall resistance as a function of the applied magnetic field showing the Quantum Hall effect**. [Source](https://commons.wikimedia.org/wiki/File:Rhoxy.jpg). As we can see, the blue line of the [Hall resistance](electromagnetism.md#hall-resistance)  TODO material, temperature, etc. It is unclear if this is just

Gotta understand this because the name sounds cool. Maybe also because it is used to define the [fucking](biology.md#sexual-intercourse) [ampere in the 2019 redefinition of the SI base units](system-of-units.md#ampere-in-the-2019-redefinition-of-the-si-base-units).

At least the experiment description itself is easy to understand. The hard part is the physical theory behind.

TODO [experiment video](todo.md#videos-of-all-key-physics-experiments).

The effect can be separated into two modes:
- [Integer quantum Hall effect](#integer-quantum-hall-effect): easier to explain from first principles
- [Fractional quantum Hall effect](#fractional-quantum-hall-effect): harder to explain from first principles
  - [Fractional quantum Hall effect for $\nu = 1/m$](#fractional-quantum-hall-effect-for-nu-1-m): [1998 Nobel Prize in Physics](nobel-prize.md#1998-nobel-prize-in-physics)
  - [Fractional quantum Hall effect for $\nu \ne 1/m$](#fractional-quantum-hall-effect-for-nu-ne-1-m): one of the most important [unsolved physics problems](physics.md#unsolved-physics-problem) as of 2023

<a id="video-integer-and-fractional-quantum-hall-effects-by-matthew-a-grayson"></a>
**[Video 5](#video-integer-and-fractional-quantum-hall-effects-by-matthew-a-grayson). Integer and fractional quantum Hall effects by Matthew A. Grayson.** [Source](https://www.youtube.com/watch?v=UNyNjZeG1wc). Presented 2015. This dude did good.

#### Integer quantum Hall effect

↑ **Parent:** [Quantum Hall effect](#quantum-hall-effect)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Integer_quantum_Hall_effect)

![](https://upload.wikimedia.org/wikipedia/commons/3/38/Rhoxy.jpg)

**[Figure 3](#_137)** [Source](https://commons.wikimedia.org/wiki/File:Rhoxy.jpg).

#### Fractional quantum Hall effect

↑ **Parent:** [Quantum Hall effect](#quantum-hall-effect)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Fractional_quantum_Hall_effect)

TODO original experiment?

Laughlin paper: 1981 Quantized Hall conductivity in two dimensions.

Shows a cool new type of matter: [Abelian anyons](relativistic-quantum-mechanics.md#abelian-anyon).

<h5 id="fractional-quantum-hall-effect-for-nu-1-m">Fractional quantum Hall effect for <span class="katex"><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:0.4306em;"></span><span class="mord mathnormal" style="margin-right:0.06366em;">ν</span><span class="mspace" style="margin-right:0.2778em;"></span><span class="mrel">=</span><span class="mspace" style="margin-right:0.2778em;"></span></span><span class="base"><span class="strut" style="height:1em;vertical-align:-0.25em;"></span><span class="mord">1/</span><span class="mord mathnormal">m</span></span></span></span></h5>

↑ **Parent:** [Fractional quantum Hall effect](#fractional-quantum-hall-effect)  
🏷️ **Tags:** [1998 Nobel Prize in Physics](nobel-prize.md#1998-nobel-prize-in-physics)

<h5 id="fractional-quantum-hall-effect-for-nu-ne-1-m">Fractional quantum Hall effect for <span class="katex"><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:0.8889em;vertical-align:-0.1944em;"></span><span class="mord mathnormal" style="margin-right:0.06366em;">ν</span><span class="mspace" style="margin-right:0.2778em;"></span><span class="mrel"><span class="mrel"><span class="mord vbox"><span class="thinbox"><span class="rlap"><span class="strut" style="height:0.8889em;vertical-align:-0.1944em;"></span><span class="inner"><span class="mord"><span class="mrel"></span></span></span><span class="fix"></span></span></span></span></span><span class="mrel">=</span></span><span class="mspace" style="margin-right:0.2778em;"></span></span><span class="base"><span class="strut" style="height:1em;vertical-align:-0.25em;"></span><span class="mord">1/</span><span class="mord mathnormal">m</span></span></span></span></h5>

↑ **Parent:** [Fractional quantum Hall effect](#fractional-quantum-hall-effect)

<h6 id="fractional-quantum-hall-effect-5-2">Fractional quantum Hall effect 5/2</h6>

↑ **Parent:** [Fractional quantum Hall effect for $\nu \ne 1/m$](#fractional-quantum-hall-effect-for-nu-ne-1-m)  
🏷️ **Tags:** [Unsolved physics problem](physics.md#unsolved-physics-problem)

#### Spin Hall effect

↑ **Parent:** [Quantum Hall effect](#quantum-hall-effect)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Spin_Hall_effect)

### Macroscopic quantum phenomena

↑ **Parent:** [Quantum mechanics experiment](#quantum-mechanics-experiment)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Macroscopic_quantum_phenomena)

## History of quantum mechanics

↑ **Parent:** [Quantum mechanics](quantum-mechanics.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/History_of_quantum_mechanics)

The discovery of the [photon](photon.md) was one of the major initiators of quantum mechanics.

Light was very well known to be a wave through [diffraction](calculus.md#diffraction) experiments. So how could it also be a particle???

This was a key development for people to eventually notice that the [electron](standard-model.md#electron) is also a wave.

This process "started" in 1900 with [Planck's law](condensed-matter-physics.md#planck-s-law) which was based on discrete energy packets being exchanged as exposed at [On the Theory of the Energy Distribution Law of the Normal Spectrum by Max Planck (1900)](physicist.md#on-the-law-of-distribution-of-energy-in-the-normal-spectrum).

This ideas was reinforced by [Einstein](physicist.md#albert-einstein)'s explanation of the [photoelectric effect](physics.md#photoelectric-effect) in 1905 in terms of [photon](photon.md).

In the next big development was the [Bohr model](chemistry.md#bohr-model) in 1913, which supposed non-[classical physics](mechanics.md#classical-physics) new quantization rules for the [electron](standard-model.md#electron) which explained the [hydrogen emission spectrum](#hydrogen-emission-spectrum). The quantization rule used made use of the [Planck constant](#planck-constant), and so served an initial link between the emerging quantized nature of [light](photon.md#light), and that of the [electron](standard-model.md#electron).

The final phase started in 1923, when [Louis de Broglie](physicist.md#louis-de-broglie) proposed that in analogy to photons, [electrons](standard-model.md#electron) might also be waves, a statement made more precise through the [de Broglie relations](#de-broglie-relations).

This event opened the floodgates, and soon [matrix mechanics](#matrix-mechanics) was published in [quantum mechanical re-interpretation of kinematic and mechanical relations by Heisenberg (1925)](#quantum-mechanical-re-interpretation-of-kinematic-and-mechanical-relations-by-heisenberg-1925), as the first coherent formulation of [quantum mechanics](quantum-mechanics.md).

It was followed by the [Schrödinger equation](#schrodinger-equation) in 1926, which proposed an equivalent [partial differential equation](calculus.md#partial-differential-equation) formulation to [matrix mechanics](#matrix-mechanics), a mathematical formulation that was more familiar to [physicists](physicist.md) than the matrix ideas of Heisenberg.

[Inward Bound by Abraham Pais (1988)](particle-physics.md#inward-bound-by-abraham-pais-1988) summarizes his views of the main developments of the subjectit:

> 
> - Planck's on the discovery of the quantum theory (1900);
> - Einstein's on the light-quantum (1905);
> - [Bohr's on the hydrogen atom](chemistry.md#bohr-model) (1913);
> - Bose's on what came to be called quantum statistics (1924);
> - Heisenberg's on what came to be known as [matrix mechanics](#matrix-mechanics) (1925);
> - and Schroedinger's on wave mechanics (1926).

Bibliography:
- [https://physics.stackexchange.com/questions/18632/good-book-on-the-history-of-quantum-mechanics](https://physics.stackexchange.com/questions/18632/good-book-on-the-history-of-quantum-mechanics) on [Physics Stack Exchange](stack-overflow.md#physics-stack-exchange)
- [https://www.youtube.com/watch?v=5hVmeOCJjOU](https://www.youtube.com/watch?v=5hVmeOCJjOU) A Brief History of Quantum Mechanics by [Sean Carroll](physicist.md#sean-m-carroll) (2020) Given at the [Royal Institution](science.md#royal-institution).

### Timeline of quantum mechanics

↑ **Parent:** [History of quantum mechanics](#history-of-quantum-mechanics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Timeline_of_quantum_mechanics)

- 1859-1900: see [Section "Black-body radiation experiment"](condensed-matter-physics.md#black-body-radiation-experiment). Continuously improving  culminating in [Planck's law](condensed-matter-physics.md#planck-s-law) [black-body radiation](condensed-matter-physics.md#black-body-radiation) and [Planck's law](condensed-matter-physics.md#planck-s-law)
- 1905 [photoelectric effect](physics.md#photoelectric-effect) and the [photon](photon.md)
  - TODO experiments
  - 1905 Einstein's photoelectric effect paper. Planck was intially thinking that light was continuous, but the atoms vibrated in a discrete way. Einstein's explanation of the photoelectric effect throws that out of the window, and considers the photon discrete.
- 1913 [atomic spectra](#emission-spectrum) and the [Bohr model](chemistry.md#bohr-model)
  - 1885 [Balmer series](#balmer-series), an [empirical formula](science.md#empirical-formula) describes some of the lines of the [hydrogen emission spectrum](#hydrogen-emission-spectrum)
  - 1888 [Rydberg formula](#rydberg-formula) generalizes the [Balmer series](#balmer-series)
  - 1896 [Pickering series](#pickering-series) makes it look like a star has some new kind of hydrogen that produces half-integer entries in the [Pickering series](#pickering-series)
  - 1911 Bohr visits [J. J. Thomson](physicist.md#j-j-thomson) in the [University of Cambridge](university.md#university-of-cambridge) for his postdoc, but they don't get along well
    - Bohr visits [Rutherford](physicist.md#ernest-rutherford) at the [University of Manchester](university.md#university-of-manchester) and decides to transfer there. During this stay he becomes interested in problems of the electronic structure of the atom.

      Bohr was forced into a quantization postulate because spinning electrons must radiate energy and collapse, so he postulated that electrons must somehow magically stay in orbits without classically spinning.
  - 1913 february: young physics professor Hans Hansen tells Bohr about the [Balmer series](#balmer-series). This is one of the final elements Bohr needed.
  - 1913 [Bohr model](chemistry.md#bohr-model) published predicts atomic spectral lines in terms of the [Planck constant](#planck-constant) and other [physical constant](system-of-units.md#physical-constant).
    - explains the [Pickering series](#pickering-series) as belonging to inoized [helium](chemistry.md#helium) that has a single [electron](standard-model.md#electron). The half term in the spectral lines of this species come from the nucleus having twice the charge of hydrogen.
    - 1913 March: during review before publication, Rutherford points out that [instantaneous quantum jumps don't seem to play well with causality](physics.md#causality-and-quantum-jumps-are-incompatible).
  - 1916 [Bohr-Sommerfeld model](chemistry.md#bohr-sommerfeld-model) introduces [angular momentum](mechanics.md#angular-momentum) to explain why some lines are not observed, as they would violate the conservation of angular momentum.

### Old quantum theory

↑ **Parent:** [History of quantum mechanics](#history-of-quantum-mechanics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Old_quantum_theory)

## History of quantum mechanics bibliography

↑ **Parent:** [Quantum mechanics](quantum-mechanics.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/History_of_quantum_mechanics_bibliography)

### The Quantum Story by Jim Baggott (2011)

↑ **Parent:** [History of quantum mechanics bibliography](#history-of-quantum-mechanics-bibliography)

[https://archive.org/details/quantumstoryhist0000bagg](https://archive.org/details/quantumstoryhist0000bagg) on the [Internet Archive Open Library](website.md#internet-archive-open-library).

### The Old Quantum Theory by Dirk ter Haar (1967)

↑ **Parent:** [History of quantum mechanics bibliography](#history-of-quantum-mechanics-bibliography)

## Quantum mechanics bibliography

↑ **Parent:** [Quantum mechanics](quantum-mechanics.md)

### Introductory Quantum Mechanics by Richard Fitzpatrick (2020)

↑ **Parent:** [Quantum mechanics bibliography](#quantum-mechanics-bibliography)

[https://phys.libretexts.org/Bookshelves/Quantum_Mechanics/Introductory_Quantum_Mechanics_(Fitzpatrick)](https://phys.libretexts.org/Bookshelves/Quantum_Mechanics/Introductory_Quantum_Mechanics_(Fitzpatrick))

This [LibreTexts](social-technology.md#libretexts) book does have some interest!

### The Principles of Quantum Mechanics by Paul Dirac (1930)

↑ **Parent:** [Quantum mechanics bibliography](#quantum-mechanics-bibliography)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/The_Principles_of_Quantum_Mechanics_by_Paul_Dirac_(1930))

#### The Principles of Quantum Mechanics by Paul Dirac revised fourth edition (1967)

↑ **Parent:** [The Principles of Quantum Mechanics by Paul Dirac (1930)](#the-principles-of-quantum-mechanics-by-paul-dirac-1930)

<h3 id="mit-8-06-quantum-physics-iii-spring-2018-by-barton-zwiebach">MIT 8.06 Quantum Physics III, Spring 2018 by Barton Zwiebach</h3>

↑ **Parent:** [Quantum mechanics bibliography](#quantum-mechanics-bibliography)  
🏷️ **Tags:** [Barton Zwiebach](physicist.md#barton-zwiebach)

[https://www.youtube.com/playlist?list=PLUl4u3cNGP60Zcz8LnCDFI8RPqRhJbb4L](https://www.youtube.com/playlist?list=PLUl4u3cNGP60Zcz8LnCDFI8RPqRhJbb4L)

100 10-20 minute videos properly split by topic, good resource!

Instructor: [Barton Zwiebach](physicist.md#barton-zwiebach).

Free material from university courses:
- [https://physics.weber.edu/schroeder/quantum/QuantumBook.pdf](https://physics.weber.edu/schroeder/quantum/QuantumBook.pdf)  ([archive](https://web.archive.org/web/20191230193450/https://physics.weber.edu/schroeder/quantum/QuantumBook.pdf)) "Notes on Quantum Mechanics" pusbliehd by Daniel V. Schroeder (2019) The author is from from Weber State University.

### Applications of Quantum Mechanics by David Tong (2017)

↑ **Parent:** [Quantum mechanics bibliography](#quantum-mechanics-bibliography)  
🏷️ **Tags:** [David Tong](physicist.md#david-tong)

- [http://www.damtp.cam.ac.uk/user/tong/aqm/aqm.pdf](http://www.damtp.cam.ac.uk/user/tong/aqm/aqm.pdf)
- [https://web.archive.org/web/20200215103215/http://www.damtp.cam.ac.uk/user/tong/aqm/aqm.pdf](https://web.archive.org/web/20200215103215/http://www.damtp.cam.ac.uk/user/tong/aqm/aqm.pdf)

Author: [David Tong](physicist.md#david-tong).

Summary:
- Chapter 2 "Band Structure" covers [electronic band theory](condensed-matter-physics.md#electronic-band-theory)

### Quantum Mechanics for Engineers by Leon van Dommelen (2011)

↑ **Parent:** [Quantum mechanics bibliography](#quantum-mechanics-bibliography)

- [http://www.eng.fsu.edu/~dommelen/quantum/style_a/index.html](http://www.eng.fsu.edu/~dommelen/quantum/style_a/index.html)
- [https://web.archive.org/web/20200220003741/http://www.eng.fsu.edu/~dommelen/quantum/style_a/index.html](https://web.archive.org/web/20200220003741/http://www.eng.fsu.edu/~dommelen/quantum/style_a/index.html)

Looks very impressive! Last update marked 2011 as of 2020.

Goes up to "A.15 [quantum field theory](quantum-field-theory.md) in a Nanoshell", Ciro have to review it to see if there's anything worthwhile in that section.

Personal page says he retired as of 2020: [http://www.eng.fsu.edu/~dommelen/](http://www.eng.fsu.edu/~dommelen/) But hopefully he has more time for these notes!

And he appears to have his own lightweight markup language that [transpiles](software.md#source-to-source-compiler) to [LaTeX](computer.md#latex) called l2h: [http://www.eng.fsu.edu/~dommelen/l2h/](http://www.eng.fsu.edu/~dommelen/l2h/)

### Quantum physics by Jim Branson (2003)

↑ **Parent:** [Quantum mechanics bibliography](#quantum-mechanics-bibliography)

[https://quantummechanics.ucsd.edu/ph130a/130_notes/130_notes.html](https://quantummechanics.ucsd.edu/ph130a/130_notes/130_notes.html)

For the [UCSD](university.md#university-of-california-san-diego) Physics 130 course.

Last updated: 2013.

Very good! Goes up to the [Dirac equation](relativistic-quantum-mechanics.md#dirac-equation).

There were apparently some lecture videos at: [https://web.archive.org/web/20030604194654/http://physicsstream.ucsd.edu/courses/spring2003/physics130a/](https://web.archive.org/web/20030604194654/http://physicsstream.ucsd.edu/courses/spring2003/physics130a/) as pointed out by [Matthew Heaney](google.md#matthew-heaney)[https://github.com/cirosantilli/cirosantilli.github.io/discussions/116#discussioncomment-7572926](https://github.com/cirosantilli/cirosantilli.github.io/discussions/116#discussioncomment-7572926), .mov files can be found at: [https://web.archive.org/web/*/http://physicsstream.ucsd.edu/courses/spring2003/physics130a/*](https://web.archive.org/web/*/http://physicsstream.ucsd.edu/courses/spring2003/physics130a/*), but we were yet unable to open them, related:
- [https://unix.stackexchange.com/questions/331977/how-to-view-and-play-mov-files-on-ubuntu-16-04-lts](https://unix.stackexchange.com/questions/331977/how-to-view-and-play-mov-files-on-ubuntu-16-04-lts)
- [https://askubuntu.com/questions/1695/watch-quicktime-videos-in-the-browser](https://askubuntu.com/questions/1695/watch-quicktime-videos-in-the-browser)

## Mathematical formulation of quantum mechanics

↑ **Parent:** [Quantum mechanics](quantum-mechanics.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Mathematical_formulation_of_quantum_mechanics)

These are the key mathematical ideas to understand!!

There are actually a few formulations out there. By far the dominant one as of 2020 has been the [Schrödinger picture](#schrodinger-picture), which contrasts notably with the [Heisenberg picture](#heisenberg-picture).

Another well known one is the [de Broglie-Bohm theory](#de-broglie-bohm-theory), which is deterministic, but [non-local](physics.md#principle-of-locality).

<h3 id="schrodinger-picture">Schrödinger picture</h3>

↑ **Parent:** [Mathematical formulation of quantum mechanics](#mathematical-formulation-of-quantum-mechanics)

To better understand the discussion below, the best thing to do is to read it in parallel with the simplest possible example: [Schrödinger picture example: quantum harmonic oscillator](#schrodinger-picture-example-quantum-harmonic-oscillator).

The state of a quantum system is a unit vector in a [Hilbert space](calculus.md#hilbert-space).

"Making a measurement" for an [observable](#observable) means applying a [self-adjoint operator](linear-algebra.md#self-adjoint-operator) to the state, and after a measurement is done:
- the state [collapses](#wave-function-collapse) to an [eigenvector](linear-algebra.md#eigenvector) of the self adjoint operator
- the result of the measurement is the [eigenvalue](linear-algebra.md#eigenvalue) of the self adjoint operator
- the probability of a given result happening when the spectrum is [discrete](calculus.md#discrete) is proportional to the modulus of the projection on that eigenvector.

  For continuous spectra such as that of the [position operator](#position-operator) in most systems, e.g. [Schrödinger equation for a free one dimensional particle](#schrodinger-equation-for-a-free-one-dimensional-particle), the projection on each individual eigenvalue is zero, i.e. the probability of one absolutely exact position is zero. To get a non-zero result, measurement has to be done on a continuous range of eigenvectors (e.g. for position: "is the particle present between x=0 and x=1?"), and you have to integrate the probability over the projection on a continuous range of eigenvalues.

  In such continuous cases, the probability collapses to an uniform distribution on the range after measurement.

  The continuous position operator case is well illustrated at: [Video 9. "Visualization of Quantum Physics (Quantum Mechanics) by udiprod (2017)"](#video-visualization-of-quantum-physics-quantum-mechanics-by-udiprod-2017)
Those last two rules are also known as the [Born rule](#born-rule).

Self adjoint operators are chosen because they have the following key properties:
- their eigenvalues form an orthonormal basis
- they are diagonalizable

See also: [https://en.wikipedia.org/wiki/Measurement_in_quantum_mechanics](https://en.wikipedia.org/wiki/Measurement_in_quantum_mechanics)

Perhaps the easiest case to understand this for is that of [spin](relativistic-quantum-mechanics.md#spin-physics), which has only a finite number of eigenvalues. Although it is a shame that fully understanding that requires a [relativistic](relativity.md#special-relativity) quantum theory such as the [Dirac equation](relativistic-quantum-mechanics.md#dirac-equation).

The next steps are to look at simple 1D bound states such as [particle in a box](#particle-in-a-box) and [quantum harmonic oscillator](#quantum-harmonic-oscillator).

This naturally generalizes to [Schrödinger equation solution for the hydrogen atom](#schrodinger-equation-solution-for-the-hydrogen-atom).

The solution to the [Schrödinger equation for a free one dimensional particle](#schrodinger-equation-for-a-free-one-dimensional-particle) is a bit harder since the possible energies do not make up a [countable set](formalization-of-mathematics.md#countable-set).

This formulation was apparently called more precisely [Dirac-von Neumann axioms](#dirac-von-neumann-axioms), but it because so dominant we just call it "the" formulation.

[Quantum Field Theory lecture notes by David Tong (2007)](quantum-field-theory.md#quantum-field-theory-lecture-notes-by-david-tong-2007) mentions that:

> if you were to write the wavefunction in quantum field theory, it would be a functional, that is a function of every possible configuration of the field $\phi$.

<h4 id="schrodinger-picture-example-quantum-harmonic-oscillator">Schrödinger picture example: quantum harmonic oscillator</h4>

↑ **Parent:** [Schrödinger picture](#schrodinger-picture)

TODO: use the results from the [quantum harmonic oscillator](#quantum-harmonic-oscillator) solution to precisely illustrate the discussion at [Schrödinger picture](#schrodinger-picture) with a concrete example.

#### Wave function collapse

↑ **Parent:** [Schrödinger picture](#schrodinger-picture)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Wave_function_collapse)

Similar to [quantum jump](chemistry.md#quantum-jump) in the [Bohr model](chemistry.md#bohr-model), but for the [Schrödinger equation](#schrodinger-equation).

The idea the the wave function of a small observed system collapses "obviously" cannot be the full physical truth, only a very useful approximation of reality.

Because then are are hard pressed to determine the boundary between what collapses and what doesn't, and there isn't such a boundary, as everything is interacting, including the observer.

The [many-worlds interpretation](#many-worlds-interpretation) is an elegant explanation for this. Though it does feel a bit sad and superfluous.

##### Interpretations of quantum mechanics

↑ **Parent:** [Wave function collapse](#wave-function-collapse)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Interpretations_of_quantum_mechanics)

###### Categorical quantum mechanics

↑ **Parent:** [Interpretations of quantum mechanics](#interpretations-of-quantum-mechanics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Categorical_quantum_mechanics)

[https://quantumcomputing.stackexchange.com/questions/1988/what-is-the-use-of-categorical-quantum-mechanics](https://quantumcomputing.stackexchange.com/questions/1988/what-is-the-use-of-categorical-quantum-mechanics)

###### EPR paradox

↑ **Parent:** [Interpretations of quantum mechanics](#interpretations-of-quantum-mechanics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/EPR_paradox)

###### Many-worlds interpretation

↑ **Parent:** [Interpretations of quantum mechanics](#interpretations-of-quantum-mechanics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Many-worlds_interpretation)

One single [universal wavefunction](#universal-wavefunction), and every possible outcomes happens in some alternate universe. Does feel a bit sad and superfluous, but also does give some sense to perceived "[wave function collapse](#wave-function-collapse)".

###### Universal wavefunction

↑ **Parent:** [Many-worlds interpretation](#many-worlds-interpretation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Universal_wavefunction)

### Born rule

↑ **Parent:** [Mathematical formulation of quantum mechanics](#mathematical-formulation-of-quantum-mechanics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Born_rule)

### Bra-ket notation

↑ **Parent:** [Mathematical formulation of quantum mechanics](#mathematical-formulation-of-quantum-mechanics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Bra–ket_notation)

Notation used in [quantum mechanics](quantum-mechanics.md).

Ket is just a [vector](linear-algebra.md#vector-mathematics). Though generally in the context of [quantum mechanics](quantum-mechanics.md), this is an infinite dimensional vector in a [Hilbert space](calculus.md#hilbert-space) like [$\LTwo$](calculus.md#l2).

Bra is just the [dual vector](linear-algebra.md#dual-vector) corresponding to a ket, or in other words [projection](linear-algebra.md#projection-mathematics) [linear operator](linear-algebra.md#linear-operator), i.e. a linear function which can act on a given vector and returns a single [complex number](formalization-of-mathematics.md#complex-number). Also known as... [dot product](linear-algebra.md#dot-product).

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

This notation is widely used in [quantum mechanics](quantum-mechanics.md) because calculating the [probability](mathematics.md#probability) of getting a certain outcome for an experiment is calculated by taking the projection of a state on one an [eigenvalue](linear-algebra.md#eigenvalue) basis vector as explained at: [Section "Mathematical formulation of quantum mechanics"](#mathematical-formulation-of-quantum-mechanics).

Making the projection operator "look like a thing" (the bra) is nice because we can add and multiply them much like we can for vectors (they also form a [vector space](linear-algebra.md#vector-space)), e.g.:

$$
a{x} + a{y}
$$

just means taking the projection along the $x + y$ direction.

[Ciro Santilli](ciro-santilli.md) thinks that this notation is a bit over-engineered. Notably the bra's are just vectors, which we should just write as usual with $\va{v}$... the bra thing makes it look scarier than it needs to be. And then we should just find a different notation for the projection part.

Maybe [Dirac](physicist.md#paul-dirac) chose it because of the appeal of the women's piece of clothing: [bra](technology.md#bra), in an irresistible call from [British humour](comedy.md#british-humour).

But in any case, alas, we are now stuck with it.

### Dirac-von Neumann axioms

↑ **Parent:** [Mathematical formulation of quantum mechanics](#mathematical-formulation-of-quantum-mechanics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Dirac–von_Neumann_axioms)

This is basically what became the dominant formulation as of 2020 (and much earlier), and so we just call it the "[mathematical formulation of quantum mechanics](#mathematical-formulation-of-quantum-mechanics)".

### Linearity of quantum mechanics

↑ **Parent:** [Mathematical formulation of quantum mechanics](#mathematical-formulation-of-quantum-mechanics)

- [https://physics.stackexchange.com/questions/1201/linearity-of-quantum-mechanics-and-nonlinearity-of-macroscopic-physics](https://physics.stackexchange.com/questions/1201/linearity-of-quantum-mechanics-and-nonlinearity-of-macroscopic-physics)
- [https://physics.stackexchange.com/questions/134503/what-is-the-physical-reason-behind-linearity-of-schrodingers-equation](https://physics.stackexchange.com/questions/134503/what-is-the-physical-reason-behind-linearity-of-schrodingers-equation)
- [https://physics.stackexchange.com/questions/33344/is-the-universe-linear-if-so-why](https://physics.stackexchange.com/questions/33344/is-the-universe-linear-if-so-why)

### Observable

↑ **Parent:** [Mathematical formulation of quantum mechanics](#mathematical-formulation-of-quantum-mechanics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Observable)

### Phase-space formulation

↑ **Parent:** [Mathematical formulation of quantum mechanics](#mathematical-formulation-of-quantum-mechanics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Phase-space_formulation)

An "alternative" formulation of [quantum mechanics](quantum-mechanics.md) that does not involve operators.

## Non-relativistic quantum mechanics

↑ **Parent:** [Quantum mechanics](quantum-mechanics.md)

The first [quantum mechanics](quantum-mechanics.md) theories developed.

Their most popular formulation has been the [Schrödinger equation](#schrodinger-equation).

<h3 id="schrodinger-equation">Schrödinger equation</h3>

↑ **Parent:** [Non-relativistic quantum mechanics](#non-relativistic-quantum-mechanics)  
🏷️ **Tags:** [Important partial differential equation](calculus.md#important-partial-differential-equation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Schrödinger_equation)

The [partial differential equation](calculus.md#partial-differential-equation) of [non-relativistic](relativity.md#special-relativity) [quantum mechanics](quantum-mechanics.md).

Experiments explained:
- via the [Schrödinger equation solution for the hydrogen atom](#schrodinger-equation-solution-for-the-hydrogen-atom) it predicts:
  - [spectral line](#spectral-line) basic lines, plus [Zeeman effect](#zeeman-effect)
- [Schrödinger equation solution for the helium atom](#schrodinger-equation-solution-for-the-helium-atom): perturbative solutions give good approximations to the energy levels
- [double-slit experiment](#double-slit-experiment): I think we have a closed solution for the max and min probabilities on the measurement wall, and they match experiments

Experiments not explained: those that the [Dirac equation](relativistic-quantum-mechanics.md#dirac-equation) explains like:
- [fine structure](#fine-structure)
- [spontaneous emission](relativistic-quantum-mechanics.md#spontaneous-emission) coefficients

To get some intuition on the equation on the consequences of the equation, have a look at:
- [Schrödinger equation simulations](#computational-quantum-mechanics)
- [solutions of the Schrodinger equation](#solutions-of-the-schrodinger-equation)

The easiest to understand case of the equation which you must have in mind initially that of the [Schrödinger equation for a free one dimensional particle](#schrodinger-equation-for-a-free-one-dimensional-particle).

Then, with that in mind, the general form of the [Schrödinger equation](#schrodinger-equation) is:<a id="equation-schrodinger-equation"></a>


$$
i\hbar\pdv{\psi(\vv{x}, t)}{t} = \hat{H}[\psi(\vv{x}, t)]
$$

where:
- $\hbar$ is the [reduced Planck constant](#reduced-planck-constant)
- $\psi$ is the [wave function](#wave-function)
- $t$ is the time
- $\hat{H}$ is a [linear operator](linear-algebra.md#linear-operator) called the [Hamiltonian](mechanics.md#hamiltonian-mechanics). It takes as input a function $\psi$, and returns another function. This plays a role analogous to the Hamiltonian in [classical mechanics](mechanics.md#classical-mechanics): determining it determines what the physical system looks like, and how the system evolves in time, because we can just plug it into the equation and solve it. It basically encodes the total energy and forces of the system.

The $\vv{x}$ argument of $\psi$ could be anything, e.g.:
- we could have preferred [polar coordinates](calculus.md#polar-coordinate-system) instead of linear ones if the potential were symmetric around a point
- we could have more than one particle, e.g. [solutions of the Schrodinger equation for two electrons](#solutions-of-the-schrodinger-equation-for-two-electrons), which would have e.g. $x_1$ and $x_2$ for different particles. No matter how many particles there are, we have just a single $\psi$, we just add more arguments to it.
- we could have even more generalized coordinates. This is much in the spirit of [Hamiltonian mechanics](mechanics.md#hamiltonian-mechanics) or [generalized coordinates](mechanics.md#generalized-coordinate)
Note however that there is always a single magical $t$ time variable. This is needed in particular because there is a time [partial derivative](calculus.md#partial-derivative) in the equation, so there must be a corresponding time variable in the function. This makes the equation explicitly [non-relativistic](relativity.md).

The general [Schrödinger equation](#schrodinger-equation) can be broken up into a trivial time-dependent and a [time-independent Schrödinger equation](#time-independent-schrodinger-equation) by separation of variables. So in practice, all we need to solve is the slightly simpler [time-independent Schrödinger equation](#time-independent-schrodinger-equation), and the full equation comes out as a result.

Existence and uniqueness: [https://mathoverflow.net/questions/212913/existence-and-uniqueness-for-two-dimensional-time-dependent-schr%C3%B6dinger-equation](https://mathoverflow.net/questions/212913/existence-and-uniqueness-for-two-dimensional-time-dependent-schr%C3%B6dinger-equation)

<h4 id="time-independent-schrodinger-equation">Time-independent Schrödinger equation</h4>

↑ **Parent:** [Schrödinger equation](#schrodinger-equation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Schrödinger_equation#Time-independent_equation)

The [time-independent Schrödinger equation](#time-independent-schrodinger-equation) is a variant of the [Schrödinger equation](#schrodinger-equation) defined as:<a id="equation-time-independent-schrodinger-equation"></a>


$$
\hat{H}[\psi_x(E, \vv{x})] = E \psi_x{\vv{x}}
$$

So we see that for any [Schrödinger equation](#schrodinger-equation), which is fully defined by the [Hamiltonian](mechanics.md#hamiltonian-mechanics) $\hat{H}$, there is a corresponding [time-independent Schrödinger equation](#time-independent-schrodinger-equation), which is also uniquely defined by the same [Hamiltonian](mechanics.md#hamiltonian-mechanics).

The cool thing about the [Time-independent Schrödinger equation](#time-independent-schrodinger-equation) is that we can always reduce solving the full [Schrödinger equation](#schrodinger-equation) to solving this slightly simpler time-independent version, as described at: [Section "Solving the Schrodinger equation with the time-independent Schrödinger equation"](#solving-the-schrodinger-equation-with-the-time-independent-schrodinger-equation).

Because this method is fully general, and it simplifies the initial time-dependent problem to a time independent one, it is the approach that we will always take [when solving the Schrodinger equation](#solutions-of-the-schrodinger-equation), see e.g. [quantum harmonic oscillator](#quantum-harmonic-oscillator).

<h5 id="solving-the-schrodinger-equation-with-the-time-independent-schrodinger-equation">Solving the Schrodinger equation with the time-independent Schrödinger equation</h5>

↑ **Parent:** [Time-independent Schrödinger equation](#time-independent-schrodinger-equation)

Before reading any further, you _must_ understand [heat equation solution with Fourier series](calculus.md#heat-equation-solution-with-fourier-series), which uses [separation of variables](calculus.md#separation-of-variables).

Once that example is clear, we see that the exact same [separation of variables](calculus.md#separation-of-variables) can be done to the [Schrödinger equation](#schrodinger-equation). If we name the constant of the separation of variables $E$ for energy, we get:
- a time-only part that does not depend on space and does not depend on the [Hamiltonian](mechanics.md#hamiltonian-mechanics) at all. The solution for this part is therefore always the same exponentials for any problem, and this part is therefore "boring":$$
  \psi_t(E, t) = e^{-iEt/\hbar}
  $$
- a space-only part that does not depend on time, bud does depend on the Hamiltonian:

  $$
  \hat{H}[\psi_x(E, \vv{x})] = E \psi_x{\vv{x}}
  $$

  Since this is the only non-trivial part, unlike the time part which is trivial, this spacial part is just called "the time-independent Schrodinger equation".

  Note that the $\psi$ here is not the same as the $\psi$ in the [time-dependent Schrodinger equation](#equation-schrodinger-equation) of course, as that psi is the result of the multiplication of the time and space parts. This is a bit of imprecise terminology, but hey, physics.

Because the time part of the equation is always the same and always trivial to solve, all we have to do to actually solve the Schrodinger equation is to solve the time independent one, and then we can construct the full solution trivially.

Once we've solved the time-independent part for each possible $E$, we can construct a solution exactly as we did in [heat equation solution with Fourier series](calculus.md#heat-equation-solution-with-fourier-series): we make a weighted sum over all possible $E$ to match the initial condition, which is analogous to the [Fourier series](calculus.md#fourier-series) in the case of the heat equation to reach a final full solution:
- if there are only discretely many possible values of $E$, each possible energy $E_i$. we proceed <a id="equation-solution-of-the-schrodinger-equation-in-terms-of-the-time-independent-and-time-dependent-parts"></a>
  $$
  \sum_{i=0}^{\infty} =  \psi_t(E_i, t) \psi_x(E_i, x) = e^{-iE_i t/\hbar} \psi_x(E_i, x)
  $$

  and this is a solution by selecting $E_i$ such that at time $t = 0$ we match the initial condition:$$
  \sum_{i=0}^{\infty} e^{-iE0/\hbar} E_i\psi_i(x) = \sum_{i=0}^{\infty} E_i\psi_i(x) = initial condition
  $$

  A finite spectrum shows up in many incredibly important cases:
  - [particle in a box](#particle-in-a-box)
  - [quantum harmonic oscillator](#quantum-harmonic-oscillator)
  - [Schrödinger equation solution for the hydrogen atom](#schrodinger-equation-solution-for-the-hydrogen-atom)
- if there are infinitely many values of E, we do something analogous but with an integral instead of a sum. This is called the [continuous spectrum](linear-algebra.md#continuous-spectrum-functional-analysis). One notable

The fact that this approximation of the initial condition is always possible from is mathematically proven by some version of the [spectral theorem](linear-algebra.md#spectral-theorem) based on the fact that [The Schrodinger equation Hamiltonian has to be Hermitian](#the-schrodinger-equation-hamiltonian-has-to-be-hermitian) and therefore behaves nicely.

It is interesting to note that solving the time-independent Schrodinger equation can also be seen exactly as an [eigenvalue](linear-algebra.md#eigenvalue) equation where:
- the [Hamiltonian](mechanics.md#hamiltonian-mechanics) is a linear operator
- the value of the energy `E` is an [eigenvalue](linear-algebra.md#eigenvalue)
The only difference from usual [matrix](linear-algebra.md#matrix) [eigenvectors](linear-algebra.md#eigenvector) is that we are now dealing with an [infinite dimensional](calculus.md#infinite-dimensional) vector space.

Furthermore:
- we immediately see from the equation that the time-independent solutions are states of deterministic energy because the energy is an [eigenvalue](linear-algebra.md#eigenvalue) of the Hamiltonian operator
- by looking at [Equation 11. "Solution of the Schrodinger equation in terms of the time-independent and time dependent parts"](#equation-solution-of-the-schrodinger-equation-in-terms-of-the-time-independent-and-time-dependent-parts), it is obvious that if we take an energy measurement, the probability of each result never changes with time, because it is only multiplied by a constant

Bibliography:
- [https://quantummechanics.ucsd.edu/ph130a/130_notes/node124.html](https://quantummechanics.ucsd.edu/ph130a/130_notes/node124.html) from [quantum physics by Jim Branson (2003)](#quantum-physics-by-jim-branson-2003)

#### Derivation of the Schrodinger equation

↑ **Parent:** [Schrödinger equation](#schrodinger-equation)

Where derivation == "intuitive routes", since a "law of physics" cannot be derived, only observed right or wrong.

TODO also comment on [why are complex numbers used in the Schrodinger equation?](#why-are-complex-numbers-used-in-the-schrodinger-equation).

Some approaches:
- [https://en.wikipedia.org/w/index.php?title=Schr%C3%B6dinger_equation&oldid=964460597#Derivation](https://en.wikipedia.org/w/index.php?title=Schr%C3%B6dinger_equation&oldid=964460597#Derivation): holy crap, this just goes all in into a [Lie group](geometry.md#lie-group) approach, nice
- [Richard Feynman](richard-feynman.md)'s derivation of the Schrodinger equation:
  - [https://physics.stackexchange.com/questions/263990/feynmans-derivation-of-the-schrödinger-equation](https://physics.stackexchange.com/questions/263990/feynmans-derivation-of-the-schrödinger-equation)
  - [https://www.youtube.com/watch?v=xQ1d0M19LsM](https://www.youtube.com/watch?v=xQ1d0M19LsM) "Class Y. Feynman's Derivation of the Schrödinger Equation" by doctorphys (2020)
- [https://www.youtube.com/watch?v=zC_gYfAqjZY&list=PL54DF0652B30D99A4&index=53](https://www.youtube.com/watch?v=zC_gYfAqjZY&list=PL54DF0652B30D99A4&index=53) "I5. Derivation of the Schrödinger Equation" by doctorphys

##### Why are complex numbers used in the Schrodinger equation?

↑ **Parent:** [Derivation of the Schrodinger equation](#derivation-of-the-schrodinger-equation)

[Ciro](ciro-santilli.md)'s 10 cents: [https://physics.stackexchange.com/questions/32422/qm-without-complex-numbers/557600#557600](https://physics.stackexchange.com/questions/32422/qm-without-complex-numbers/557600#557600)

Why is there a [complex number](formalization-of-mathematics.md#complex-number) in the equation? Intuitively and mathematically:
- [https://physics.stackexchange.com/questions/8062/about-the-complex-nature-of-the-wave-function](https://physics.stackexchange.com/questions/8062/about-the-complex-nature-of-the-wave-function)
- [https://physics.stackexchange.com/questions/32422/qm-without-complex-numbers/557600#557600](https://physics.stackexchange.com/questions/32422/qm-without-complex-numbers/557600#557600)
- [https://physics.stackexchange.com/questions/292947/is-it-possible-to-formulate-the-schr%C3%B6dinger-equation-in-a-manner-that-excludes-i](https://physics.stackexchange.com/questions/292947/is-it-possible-to-formulate-the-schr%C3%B6dinger-equation-in-a-manner-that-excludes-i)

Some ideas:
- [explicit scalar form of the Maxwell's equations](electromagnetism.md#explicit-scalar-form-of-the-maxwell-s-equations)

<a id="video-necessity-of-complex-numbers-in-the-schrodinger-equation-by-barton-zwiebach-2017"></a>
**[Video 6](#video-necessity-of-complex-numbers-in-the-schrodinger-equation-by-barton-zwiebach-2017). Necessity of complex numbers in the Schrödinger equation by Barton Zwiebach (2017)** [Source](https://www.youtube.com/watch?v=f079K1f2WQk). This useless video doesn't really explain anything, he just says "it's needed because the equation has an $i$ in it".

The real explanation is: they are not needed, they just allow us to write the equation in a shorter form, which is always a win: [https://physics.stackexchange.com/questions/32422/qm-without-complex-numbers/557600#557600](https://physics.stackexchange.com/questions/32422/qm-without-complex-numbers/557600#557600)

---

#### Schrodinger equation Hamiltonian

↑ **Parent:** [Schrödinger equation](#schrodinger-equation)  
🏷️ **Tags:** [Hamiltonian](mechanics.md#hamiltonian-mechanics)

#### The Schrodinger equation Hamiltonian has to be Hermitian

↑ **Parent:** [Schrödinger equation](#schrodinger-equation)

The [Schrödinger equation](#schrodinger-equation) Hamiltonian has to be a [Hermitian](linear-algebra.md#hermitian-operator) so we will have only positive energies I think: [https://quantumcomputing.stackexchange.com/questions/12113/why-does-a-hamiltonian-have-to-be-hermitian](https://quantumcomputing.stackexchange.com/questions/12113/why-does-a-hamiltonian-have-to-be-hermitian)

#### Solutions of the Schrodinger equation

↑ **Parent:** [Schrödinger equation](#schrodinger-equation)

[https://en.wikipedia.org/wiki/List_of_quantum-mechanical_systems_with_analytical_solutions](https://en.wikipedia.org/wiki/List_of_quantum-mechanical_systems_with_analytical_solutions)

As always, the best way to get some intuition about an equation is to solve it for some simple cases, so let's give that a try with different fixed potentials.

##### Computational quantum mechanics

↑ **Parent:** [Solutions of the Schrodinger equation](#solutions-of-the-schrodinger-equation)

- [https://www.youtube.com/watch?v=1Z9wo2CzJO8](https://www.youtube.com/watch?v=1Z9wo2CzJO8) "Schrodinger equation solved numerically in 3D" by Tetsuya Matsuno. 3D hydrogen atom, code may be hidden in some paper, maybe
- [https://www.youtube.com/playlist?list=PLdCdV2GBGyXM0j66zrpDy2aMXr6cgrBJA](https://www.youtube.com/playlist?list=PLdCdV2GBGyXM0j66zrpDy2aMXr6cgrBJA) "Computational Quantum Mechanics" by Let's Code Physics. Uses a 1D trinket.io.
- [https://www.youtube.com/watch?v=BBt8EugN03Q](https://www.youtube.com/watch?v=BBt8EugN03Q) Simulating Quantum Systems \[Split Operator Method\] by LeiosOS (2018)
- [https://www.youtube.com/watch?v=86x0_-JGlGQ](https://www.youtube.com/watch?v=86x0_-JGlGQ) Simulating the Quantum World on a [Classical Computer](quantum-computing.md#classical-computer) by Garnet Chan (2016) discusses how modeling only local [entanglement](#quantum-entanglement) can make certain simulations feasible

<a id="video-simulation-of-the-time-dependent-schrodinger-equation-javascript-animation-by-coding-physics-2019"></a>
**[Video 7](#video-simulation-of-the-time-dependent-schrodinger-equation-javascript-animation-by-coding-physics-2019). Simulation of the time-dependent Schrodinger equation (JavaScript Animation) by Coding Physics (2019)** [Source](http://youtube.com/watch?v=g4wuSgwLT9I). Source code: [https://github.com/CodingPhysics/Schroedinger](https://github.com/CodingPhysics/Schroedinger). One dimensional potentials, non-interacting particles. The code is clean, graphics based on [https://github.com/processing/p5.js](https://github.com/processing/p5.js), and all maths from scratch. Source organization and comments are typical of numerical code, the anonymous author is was likely a Fortran user in the past.

A potential change patch in `sketch.js`:
```
-   potential:     x => 2E+4*Math.pow((4*x - 1)*(4*x - 3),2),
+ potential:     x => 4*Math.pow(x - 0.5, 2),
```

---

<a id="video-quantum-mechanics-5b-schrodinger-equation-ii-by-viascience-2013"></a>
**[Video 8](#video-quantum-mechanics-5b-schrodinger-equation-ii-by-viascience-2013). Quantum Mechanics 5b - Schrödinger Equation II by ViaScience (2013)** [Source](http://youtube.com/watch?v=ee4LqXRlQmE). 2D non-interacting particle in a box, description says using [Scilab](mathematics.md#scilab) and points to source. Has a double slit simulation.

<a id="video-visualization-of-quantum-physics-quantum-mechanics-by-udiprod-2017"></a>
**[Video 9](#video-visualization-of-quantum-physics-quantum-mechanics-by-udiprod-2017). Visualization of Quantum Physics (Quantum Mechanics) by udiprod (2017)** [Source](https://www.youtube.com/watch?v=p7bzE1E5PMY). Closed source, but a fantastic visualization and explanation of a 1D free wave packet, including how measurement snaps position to the measured range, [position and momentum space](#position-and-momentum-space) and the [uncertainty principle](#uncertainty-principle).

###### Why it is hard to simulate quantum systems?

↑ **Parent:** [Computational quantum mechanics](#computational-quantum-mechanics)

This is basically how [quantum computing](quantum-computing.md) was first theorized by [Richard Feynman](richard-feynman.md): [quantum computers as experiments that are hard to predict outcomes](quantum-computing.md#quantum-computers-as-experiments-that-are-hard-to-predict-outcomes).

TODO answer that: [https://quantumcomputing.stackexchange.com/questions/5005/why-it-is-hard-to-simulate-a-quantum-device-by-a-classical-devices](https://quantumcomputing.stackexchange.com/questions/5005/why-it-is-hard-to-simulate-a-quantum-device-by-a-classical-devices). A good answer would be with a more physical example of [quantum entanglement](#quantum-entanglement), e.g. on a [photonic quantum computer](quantum-computing.md#photonic-quantum-computer).

###### Computational quantum mechanics software

↑ **Parent:** [Computational quantum mechanics](#computational-quantum-mechanics)

###### Quantum ESPRESSO

↑ **Parent:** [Computational quantum mechanics software](#computational-quantum-mechanics-software)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Quantum_ESPRESSO)

###### QuTiP

↑ **Parent:** [Computational quantum mechanics software](#computational-quantum-mechanics-software)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/QuTiP)

<h5 id="schrodinger-equation-for-a-one-dimensional-particle">Schrödinger equation for a one dimensional particle</h5>

↑ **Parent:** [Solutions of the Schrodinger equation](#solutions-of-the-schrodinger-equation)

We select for the general [Equation 7. "Schrodinger equation"](#equation-schrodinger-equation):
- $\vv{x} = x$, the linear [cartesian coordinate](calculus.md#cartesian-coordinate-system) in the x direction
- $\hat{H} = -\frac{\hbar^2}{2m}\pdv{^2}{x^2} + V(x, t)$, which analogous to the sum of [kinetic](physics.md#kinetic-energy) and [potential energy](physics.md#potential-energy) in [classical mechanics](mechanics.md#classical-mechanics)
giving the full explicit [partial differential equation](calculus.md#partial-differential-equation):<a id="equation-schrodinger-equation-for-a-one-dimensional-particle"></a>


$$
i\hbar\pdv{\psi(x, t)}{t} = \left[ -\frac{\hbar^2}{2m}\pdv{^2}{x^2} + V(x, t) \right]\psi(x, t)
$$

The corresponding [time-independent Schrödinger equation](#time-independent-schrodinger-equation) for this equation is:<a id="equation-time-independent-schrodinger-equation-for-a-one-dimensional-particle"></a>


$$
\left[-\frac{\hbar^2}{2m} \pdv{^2}{x^2} + V(x)\right]\psi(x) = E \psi(x)
$$

<h5 id="schrodinger-equation-for-a-free-one-dimensional-particle">Schrödinger equation for a free one dimensional particle</h5>

↑ **Parent:** [Solutions of the Schrodinger equation](#solutions-of-the-schrodinger-equation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Free_particle#Quantum_free_particle)

[Schrödinger equation for a one dimensional particle](#schrodinger-equation-for-a-one-dimensional-particle) with $V = 0$. The first step is to calculate the [time-independent Schrödinger equation for a free one dimensional particle](#time-independent-schrodinger-equation-for-a-free-one-dimensional-particle)

Then, for each energy $E$, from the discussion at [Section "Solving the Schrodinger equation with the time-independent Schrödinger equation"](#solving-the-schrodinger-equation-with-the-time-independent-schrodinger-equation), the solution is:

$$
\psi(x) = \int_{E=-\infty}^{\infty} e^{\frac{\sqrt{2mE} i x}{\hbar}} e^{-iE t/\hbar} = e^{i\frac{\sqrt{2mE}x - E t}{\hbar}}
$$

Therefore, we see that the solution is made up of infinitely many [plane wave functions](#plane-wave-function).

###### Plane wave function

↑ **Parent:** [Schrödinger equation for a free one dimensional particle](#schrodinger-equation-for-a-free-one-dimensional-particle)

In this solution of the [Schrödinger equation](#schrodinger-equation), by the [uncertainty principle](#uncertainty-principle), position is completely unknown (the particle could be anywhere in space), and momentum (and therefore, [energy](physics.md#energy)) is perfectly known.

The [plane wave function](#plane-wave-function) appears for example in the solution of the [Schrödinger equation for a free one dimensional particle](#schrodinger-equation-for-a-free-one-dimensional-particle). This makes sense, because when solving with the [time-independent Schrödinger equation](#time-independent-schrodinger-equation), we do separation of variable on fixed energy levels explicitly, and the plane wave solutions are exactly fixed energy level ones.

<h6 id="time-independent-schrodinger-equation-for-a-free-one-dimensional-particle">Time-independent Schrödinger equation for a free one dimensional particle</h6>

↑ **Parent:** [Schrödinger equation for a free one dimensional particle](#schrodinger-equation-for-a-free-one-dimensional-particle)



$$
\pdv{^2}{x^2} \psi(x) = -\frac{2mE}{\hbar^2} \psi(x)
$$

so the solution is:

$$
\psi(x) = e^{\frac{\sqrt{2mE} i x}{\hbar}}
$$

We notice that the solution has [continuous spectrum](linear-algebra.md#continuous-spectrum-functional-analysis), since any value of $E$ can provide a solution.

##### Particle in a box

↑ **Parent:** [Solutions of the Schrodinger equation](#solutions-of-the-schrodinger-equation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Particle_in_a_box)

###### Quantum well

↑ **Parent:** [Particle in a box](#particle-in-a-box)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Quantum_well)

![](https://upload.wikimedia.org/wikipedia/commons/4/45/Quantum_well.svg)

**[Figure 4](#_389)** [Source](https://commons.wikimedia.org/wiki/File:Quantum_well.svg).

##### Quantum harmonic oscillator

↑ **Parent:** [Solutions of the Schrodinger equation](#solutions-of-the-schrodinger-equation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Quantum_harmonic_oscillator)

This equation is a subcase of [Equation 13. "Schrödinger equation for a one dimensional particle"](#equation-schrodinger-equation-for-a-one-dimensional-particle) with $V(x) = x^2$.

We get the [time-independent Schrödinger equation](#time-independent-schrodinger-equation) by substituting this $V$ into [Equation 14. "time-independent Schrödinger equation for a one dimensional particle"](#equation-time-independent-schrodinger-equation-for-a-one-dimensional-particle):

$$
\left[- \frac{\hbar}{2m} \pdv{^2}{x} + x^2 \right]\psi = E \psi(x)
$$

Now, there are two ways to go about this.

The first is the stupid "here's a guess" + "hey this family of solutions forms a [complete basis](calculus.md#complete-basis)"! This is exactly how we solved the problem at [Section "Solving partial differential equations with the Fourier series"](calculus.md#solving-partial-differential-equations-with-the-fourier-series), except that now the complete basis are the [Hermite functions](#hermite-functions).

The second is the much celebrated [ladder operator](#ladder-operator) method.

###### Quantum LC circuit

↑ **Parent:** [Quantum harmonic oscillator](#quantum-harmonic-oscillator)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Quantum_LC_circuit)

A quantum version of the [LC circuit](electronics.md#lc-circuit)!

TODO are there experiments, or just theoretical?

###### Hermite polynomials

↑ **Parent:** [Quantum harmonic oscillator](#quantum-harmonic-oscillator)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Hermite_polynomials)

Show up in the solution of the [quantum harmonic oscillator](#quantum-harmonic-oscillator) after [separation of variables](calculus.md#separation-of-variables) leading into the [time-independent Schrödinger equation](#time-independent-schrodinger-equation), much like [solving partial differential equations with the Fourier series](calculus.md#solving-partial-differential-equations-with-the-fourier-series).

I.e.: they are both:
- solutions to the [time-independent Schrödinger equation](#time-independent-schrodinger-equation) for the [quantum harmonic oscillator](#quantum-harmonic-oscillator)
- a complete basis of that space

###### Hermite functions

↑ **Parent:** [Hermite polynomials](#hermite-polynomials)  
🏷️ **Tags:** [Complete basis](calculus.md#complete-basis)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Hermite_polynomials#Hermite_functions)

Not the same as [Hermite polynomials](#hermite-polynomials).

###### Ladder operator

↑ **Parent:** [Quantum harmonic oscillator](#quantum-harmonic-oscillator)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Ladder_operator)

[http://www.physics.udel.edu/~jim/PHYS424_17F/Class%20Notes/Class_5.pdf](http://www.physics.udel.edu/~jim/PHYS424_17F/Class%20Notes/Class_5.pdf) by James MacDonald shows it well.

The operators are a natural guess on the lines of "if p and x were integers".

And then we can prove the ladder properties easily.

The [commutator](algebra.md#commutator) appear in the middle of this analysis.

##### Quantum tunnelling

↑ **Parent:** [Solutions of the Schrodinger equation](#solutions-of-the-schrodinger-equation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Quantum_tunnelling)

Examples:
- [flash memory](computer-hardware.md#flash-memory) uses quantum tunneling as the basis for setting and resetting bits
- [alpha decay](particle-physics.md#alpha-decay) is understood as a quantum tunneling effect in the nucleus

<h5 id="schrodinger-equation-solution-for-the-hydrogen-atom">Schrödinger equation solution for the hydrogen atom</h5>

↑ **Parent:** [Solutions of the Schrodinger equation](#solutions-of-the-schrodinger-equation)

Is the only atom that has a closed form solution, which allows for very good predictions, and gives awesome intuition about the orbitals in general.

It is arguably the most important solution of the Schrodinger equation.

In particular, it predicts:
- the major [spectral line](#spectral-line) of the [hydrogen](chemistry.md#hydrogen) atom by taking the difference between energy levels

The explicit solution can be written in terms of [spherical harmonics](calculus.md#spherical-harmonic).

<a id="video-a-better-way-to-picture-atoms-by-minutephysics-2021"></a>
**[Video 10](#video-a-better-way-to-picture-atoms-by-minutephysics-2021). A Better Way To Picture Atoms by minutephysics (2021)** [Source](https://www.youtube.com/watch?v=W2Xb2GFK2yc). Renderings based on the exact [Schrödinger equation solution for the hydrogen atom](#schrodinger-equation-solution-for-the-hydrogen-atom) that depict [wave function](#wave-function) concentration by concentration of small balls, and [angular momentum](mechanics.md#angular-momentum) by how fast the balls rotate at each point. Mentions that the approach is inspired by [de Broglie-Bohm theory](#de-broglie-bohm-theory).

###### Atomic orbital

↑ **Parent:** [Schrödinger equation solution for the hydrogen atom](#schrodinger-equation-solution-for-the-hydrogen-atom)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Atomic_orbital)

In the case of the [Schrödinger equation solution for the hydrogen atom](#schrodinger-equation-solution-for-the-hydrogen-atom), each orbital is one [eigenvector](linear-algebra.md#eigenvector) of the solution.

Remember from [time-independent Schrödinger equation](#time-independent-schrodinger-equation) that the final solution is just the weighted sum of the eigenvector decomposition of the initial state, analogously to [solving partial differential equations with the Fourier series](calculus.md#solving-partial-differential-equations-with-the-fourier-series).

This is the table that you should have in mind to visualize them: [https://en.wikipedia.org/w/index.php?title=Atomic_orbital&oldid=1022865014#Orbitals_table](https://en.wikipedia.org/w/index.php?title=Atomic_orbital&oldid=1022865014#Orbitals_table)

###### Quantum number

↑ **Parent:** [Schrödinger equation solution for the hydrogen atom](#schrodinger-equation-solution-for-the-hydrogen-atom)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Quantum_number)

Quantum numbers appear directly in the [Schrödinger equation solution for the hydrogen atom](#schrodinger-equation-solution-for-the-hydrogen-atom).

However, it very cool that they are actually discovered before the [Schrödinger equation](#schrodinger-equation), and are present in the [Bohr model](chemistry.md#bohr-model) ([principal quantum number](#principal-quantum-number)) and the [Bohr-Sommerfeld model](chemistry.md#bohr-sommerfeld-model) ([azimuthal quantum number](#azimuthal-quantum-number) and [magnetic quantum number](#magnetic-quantum-number)) of the atom. This must be because they observed direct effects of those numbers in some experiments. TODO which experiments.

E.g. [The Quantum Story by Jim Baggott (2011)](#the-quantum-story-by-jim-baggott-2011) page 34 mentions:

> As the various lines in the spectrum were identified with different quantum jumps between different orbits, it was soon discovered that not all the possible jumps were appearing. Some lines were missing. For some reason certain jumps were forbidden. An elaborate scheme of ‘selection rules’ was established by Bohr and Sommerfeld to account for those jumps that were allowed and those that were forbidden.

This refers to [forbidden mechanism](#forbidden-mechanism). TODO concrete example, ideally the first one to be noticed. How can you notice this if the energy depends only on the [principal quantum number](#principal-quantum-number)?

<a id="video-quantum-numbers-atomic-orbitals-and-electron-configurations-by-professor-dave-explains-2015"></a>
**[Video 11](#video-quantum-numbers-atomic-orbitals-and-electron-configurations-by-professor-dave-explains-2015). Quantum Numbers, Atomic Orbitals, and Electron configurations by Professor Dave Explains (2015)** [Source](https://www.youtube.com/watch?v=Aoi4j8es4gQ). He does not say the key words "Eigenvalues of the [Schrödinger equation](#schrodinger-equation)" (Which solve it), but the summary of results is good enough.

###### Principal quantum number

↑ **Parent:** [Quantum number](#quantum-number)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Principal_quantum_number)

Determines energy. This comes out directly from the resolution of the [Schrödinger equation solution for the hydrogen atom](#schrodinger-equation-solution-for-the-hydrogen-atom) where we have to set some arbitrary values of energy by [separation of variables](calculus.md#separation-of-variables) just like we have to set some arbitrary numbers when [solving partial differential equations with the Fourier series](calculus.md#solving-partial-differential-equations-with-the-fourier-series). We then just happen to see that only certain integer values are possible to satisfy the equations.

###### Azimuthal quantum number

↑ **Parent:** [Quantum number](#quantum-number)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Azimuthal_quantum_number)

Fixed [total angular momentum](#total-angular-momentum-operator).

The direction however is not specified by this number.

To determine the [quantum angular momentum](#angular-momentum-operator), we need the [magnetic quantum number](#magnetic-quantum-number), which then selects which orbital exactly we are talking about.

###### s-orbital

↑ **Parent:** [Azimuthal quantum number](#azimuthal-quantum-number)

###### p-orbital

↑ **Parent:** [Azimuthal quantum number](#azimuthal-quantum-number)

###### d-orbital

↑ **Parent:** [Azimuthal quantum number](#azimuthal-quantum-number)

###### f-orbital

↑ **Parent:** [Azimuthal quantum number](#azimuthal-quantum-number)

###### Magnetic quantum number

↑ **Parent:** [Quantum number](#quantum-number)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Magnetic_quantum_number)

Fixed [quantum angular momentum](#angular-momentum-operator) in a given direction.

Can range between $\pm l$.

E.g. consider [gallium](chemistry.md#gallium) which is 1s2 2s2 2p6 3s2 3p6 4s2 3d10 4p1:
- the electrons in [s-orbitals](#s-orbital) such as 1s, 2d, and 3d are $l=0$, and so the only value for $m_l$ is 0
- the electrons in [p-orbitals](#p-orbital) such as 2p, 3p and 4p are $l=1$, and so the possible values for $m_l$ are -1, 0 and 1
- the electrons in [d-orbitals](#d-orbital) such as 2d are $l=2$, and so the possible values for $m_l$ are -2, -1, 0 and 1 and 2

The z component of the [quantum angular momentum](#angular-momentum-operator) is simply:

$$
L_z = m_l \hbar
$$

so e.g. again for gallium:
- [s-orbitals](#s-orbital): necessarily have 0 z angular momentum
- [p-orbitals](#p-orbital): have either 0, $- \hbar$ or $+ \hbar$ z angular momentum

Note that this direction is arbitrary, since for a fixed [azimuthal quantum number](#azimuthal-quantum-number) (and therefore fixed total angular momentum), we can only know one direction for sure. $z$ is normally used by convention.

###### Spin quantum number

↑ **Parent:** [Quantum number](#quantum-number)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Spin_quantum_number)

###### Spectroscopic notation

↑ **Parent:** [Spin quantum number](#spin-quantum-number)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Spectroscopic_notation)

This notation is cool as it gives the [spin quantum number](#spin-quantum-number), which is important e.g. when talking about [hyperfine structure](#hyperfine-structure).

But it is a bit crap that the spin is not given simply as $\pm 1/2$ but rather mixes up both the [azimuthal quantum number](#azimuthal-quantum-number) and spin. What is the reason?

<a id="video-spectroscopic-notation-by-andre-k-2014"></a>
**[Video 12](#video-spectroscopic-notation-by-andre-k-2014). Spectroscopic notation by Andre K (2014)** [Source](https://www.youtube.com/watch?v=aehyxwC0KC8).

##### Solutions for the Schrodinger equation with multiple particles

↑ **Parent:** [Solutions of the Schrodinger equation](#solutions-of-the-schrodinger-equation)

Bibliography:
- [Quantum Mechanics for Engineers by Leon van Dommelen (2011)](#quantum-mechanics-for-engineers-by-leon-van-dommelen-2011) "5. Multiple-Particle Systems"

###### Separable state

↑ **Parent:** [Solutions for the Schrodinger equation with multiple particles](#solutions-for-the-schrodinger-equation-with-multiple-particles)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Separable_state)

###### Solutions of the Schrodinger equation for two electrons

↑ **Parent:** [Solutions for the Schrodinger equation with multiple particles](#solutions-for-the-schrodinger-equation-with-multiple-particles)

TODO. Can't find it easily. Anyone?

This is closely linked to the [Pauli exclusion principle](relativistic-quantum-mechanics.md#pauli-exclusion-principle).

What does a particle even mean, right? Especially in [quantum field theory](quantum-field-theory.md), where two electrons are just vibrations of a single electron field.

Another issue is that if we consider [magnetism](electromagnetism.md#magnetism), things only make sense if we add [special relativity](relativity.md#special-relativity), since [Maxwell's equations require special relativity](relativity.md#maxwell-s-equations-require-special-relativity), so a non approximate solution for this will necessarily require full [quantum electrodynamics](quantum-field-theory.md#quantum-electrodynamics).

As mentioned at [lecture 1](quantum-field-theory.md#david-tong-s-2009-quantum-field-theory-lectures-at-the-perimeter-institute/lecture-1) [https://youtube.com/watch?video=H3AFzbrqH68&t=555](https://youtube.com/watch?video=H3AFzbrqH68&t=555), [relativistic](relativity.md#special-relativity) quantum mechanical theories like the [Dirac equation](relativistic-quantum-mechanics.md#dirac-equation) and [Klein-Gordon equation](relativistic-quantum-mechanics.md#klein-gordon-equation) make no sense for a "single particle": they must imply that particles can pop in out of existence.

Bibliography:
- [https://www.youtube.com/watch?v=Og13-bSF9kA&list=PLDfPUNusx1Eo60qx3Od2KLUL4b7VDPo9F](https://www.youtube.com/watch?v=Og13-bSF9kA&list=PLDfPUNusx1Eo60qx3Od2KLUL4b7VDPo9F) "Advanced quantum theory" by [Tobias J. Osborne](physicist.md#tobias-j-osborne) says that the course will essentially cover multi-particle quantum mechanics!
- [https://physics.stackexchange.com/questions/54854/equivalence-between-qft-and-many-particle-qm](https://physics.stackexchange.com/questions/54854/equivalence-between-qft-and-many-particle-qm) "Equivalence between QFT and many-particle QM"
- Course: Quantum Many-Body Physics in Condensed Matter by Luis Gregorio Dias (2020) from [course: Quantum Many-Body Physics in Condensed Matter by Luis Gregorio Dias (2020)](condensed-matter-physics.md#course-quantum-many-body-physics-in-condensed-matter-by-luis-gregorio-dias-2020) give a good introduction to non-interacting particles

###### Orbital approximation

↑ **Parent:** [Solutions for the Schrodinger equation with multiple particles](#solutions-for-the-schrodinger-equation-with-multiple-particles)

Just ignore the electron electron interactions.

Bibliography:
- [https://chem.libretexts.org/Bookshelves/Physical_and_Theoretical_Chemistry_Textbook_Maps/Book%3A_Quantum_States_of_Atoms_and_Molecules_(Zielinksi_et_al)/10%3A_Theories_of_Electronic_Molecular_Structure/10.02%3A_The_Orbital_Approximation_and_Orbital_Configurations](https://chem.libretexts.org/Bookshelves/Physical_and_Theoretical_Chemistry_Textbook_Maps/Book%3A_Quantum_States_of_Atoms_and_Molecules_(Zielinksi_et_al)/10%3A_Theories_of_Electronic_Molecular_Structure/10.02%3A_The_Orbital_Approximation_and_Orbital_Configurations)

<h6 id="schrodinger-equation-solution-for-the-helium-atom">Schrödinger equation solution for the helium atom</h6>

↑ **Parent:** [Solutions for the Schrodinger equation with multiple particles](#solutions-for-the-schrodinger-equation-with-multiple-particles)

No closed form solution, but good approximation that can be calculated by hand with the [Hartree-Fock method](#hartree-fock-method), see [hartree-Fock method for the helium atom](#hartree-fock-method-for-the-helium-atom).

Bibliography:
- [https://www.quora.com/Why-do-electrons-not-repel-each-other-on-their-orbits](https://www.quora.com/Why-do-electrons-not-repel-each-other-on-their-orbits)
- [https://physics.stackexchange.com/questions/224108/what-does-an-orbital-mean-in-atoms-with-multiple-electrons-what-do-the-orbitals](https://physics.stackexchange.com/questions/224108/what-does-an-orbital-mean-in-atoms-with-multiple-electrons-what-do-the-orbitals)

<a id="video-quantum-chemistry-9-2-helium-atom-energy-approximations-by-tmp-chem-2016"></a>
**[Video 13](#video-quantum-chemistry-9-2-helium-atom-energy-approximations-by-tmp-chem-2016). Quantum Chemistry 9.2 - Helium Atom Energy Approximations by TMP Chem (2016)** [Source](https://www.youtube.com/watch?v=tcfNNGGjS2o). Video gives the actual numerical value of various methods, second order [perturbation theory](mathematics.md#perturbation-theory) being very close. But it the says that in the following videos will only do [Hartree-Fock method](#hartree-fock-method).

###### Hartree-Fock method

↑ **Parent:** [Solutions for the Schrodinger equation with multiple particles](#solutions-for-the-schrodinger-equation-with-multiple-particles)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Hartree–Fock_method)

###### Hartree-Fock method for the helium atom

↑ **Parent:** [Hartree-Fock method](#hartree-fock-method)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Helium_atom#Hartree–Fock_method)

###### Why do multiple electrons occupy the same orbital if electrons repel each other?

↑ **Parent:** [Hartree-Fock method](#hartree-fock-method)

That is, two electrons per [atomic orbital](#atomic-orbital), each with a different [spin](relativistic-quantum-mechanics.md#spin-physics).

As shown at [Schrödinger equation solution for the helium atom](#schrodinger-equation-solution-for-the-helium-atom), they do repel each other, and that affects their measurable energy.

However, this energy is still lower than going up to the next orbital. TODO numbers.

Bibliography:
- [https://physics.stackexchange.com/questions/505263/do-electrons-in-the-same-orbital-but-different-spin-feel-each-others-coulomb-re](https://physics.stackexchange.com/questions/505263/do-electrons-in-the-same-orbital-but-different-spin-feel-each-others-coulomb-re)

This changes however at higher orbitals, notably as approximately described by the [aufbau principle](#aufbau-principle).

###### Aufbau principle

↑ **Parent:** [Hartree-Fock method](#hartree-fock-method)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Aufbau_principle)

Boring rule that says that less energetic atomic orbitals are filled first.

Much more interesting is actually determining that order, which the [Madelung energy ordering rule](#madelung-energy-ordering-rule) is a reasonable approximation to.

###### Electron configuration

↑ **Parent:** [Aufbau principle](#aufbau-principle)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Electron_configuration)

###### Electron configuration notation

↑ **Parent:** [Aufbau principle](#aufbau-principle)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Electron_configuration_notation)

We will sometimes just write them without superscript, as it saves typing and is useless.

###### Why does 2s have less energy than 1s if they have the same principal quantum number?

↑ **Parent:** [Aufbau principle](#aufbau-principle)

[https://chemistry.stackexchange.com/questions/152/why-is-the-2s-orbital-lower-in-energy-than-the-2p-orbital-when-the-electrons-in](https://chemistry.stackexchange.com/questions/152/why-is-the-2s-orbital-lower-in-energy-than-the-2p-orbital-when-the-electrons-in)

The [principal quantum number](#principal-quantum-number) thing fully determining energy is only true for the [hydrogen emission spectrum](#hydrogen-emission-spectrum) for which we can solve the [Schrödinger equation](#schrodinger-equation) explicitly.

For other atoms with more than one electron, the orbital names are just a very good approximation/perturbation, as we don't have an explicit solution. And the internal electrons do change energy levels.

Note however that due to the more complex effect of the [Lamb shift](quantum-field-theory.md#lamb-shift) from [QED](quantum-field-theory.md#quantum-electrodynamics), there is actually a very small 2p/2s shift even in hydrogen.

###### Madelung energy ordering rule

↑ **Parent:** [Aufbau principle](#aufbau-principle)

Looking at the energy level of the [Schrödinger equation solution for the hydrogen atom](#schrodinger-equation-solution-for-the-hydrogen-atom), you would guess that for multi-electron atoms that only the [principal quantum number](#principal-quantum-number) would matter, [azimuthal quantum number](#azimuthal-quantum-number) getting filled randomly.

However, orbitals energies for large atoms don't increase in energy like those of hydrogen due to [electron](standard-model.md#electron)-electron interactions.

In particular, the following would not be naively expected:
- 2s fills up before 2p. From the hydrogen solution, you might guess that they would randomly go into either one as they'd have the same energy
- $4s^1$ in [potassium](chemistry.md#potassium) fills up before 3d, even though it has a higher [principal quantum number](#principal-quantum-number)!

This rule is only an approximation, there exist [exceptions to the Madelung energy ordering rule](#exception-to-the-madelung-energy-ordering-rule).

Bibliography:
- [https://chemistry.stackexchange.com/questions/8357/why-does-the-3rd-electron-shell-start-filling-up-with-scandium](https://chemistry.stackexchange.com/questions/8357/why-does-the-3rd-electron-shell-start-filling-up-with-scandium)
- [https://www.quora.com/If-4s-orbitals-are-higher-in-energy-than-3d-orbitals-then-why-do-electrons-fill-up-in-4s-before-filling-up-in-3d](https://www.quora.com/If-4s-orbitals-are-higher-in-energy-than-3d-orbitals-then-why-do-electrons-fill-up-in-4s-before-filling-up-in-3d)

###### Exception to the Madelung energy ordering rule

↑ **Parent:** [Madelung energy ordering rule](#madelung-energy-ordering-rule)

The most notable exception is the borrowing of 3[d-orbital](#d-orbital) electrons to 4[s](#s-orbital) as in [chromium](chemistry.md#chromium), leading to a 3d5 4s1 configuration instead of the 3d4 4s2 we would have with the rule. TODO how is that observed observed experimentally?

###### Term symbol

↑ **Parent:** [Aufbau principle](#aufbau-principle)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Term_symbol)

This notation is so confusing! People often don't manage to explain the intuition behind it, why this is an useful notation. When you see Indian university entry exam level memorization classes about this, it makes you want to cry.

The key reason why term symbols matter are [Hund's rules](#hund-s-rules), which allow us to predict with some accuracy which [electron configurations](#electron-configuration) of those states has more energy than the other.

[https://web.chem.ucsb.edu/~devries/chem218/Term%20symbols.pdf](https://web.chem.ucsb.edu/~devries/chem218/Term%20symbols.pdf) puts it well: [electron configuration notation](#electron-configuration-notation) is not specific enough, as each such notation e.g. 1s2 2s2 2p2 contains several options of spins and z angular momentum. And those affect energy.

This is why those symbols are often used when talking about energy differences: they specify more precisely which levels you are talking about.

Basically, each term symbol appears to represent a group of possible electron configurations with a given [quantum angular momentum](#angular-momentum-operator).

We first fix the energy level by saying at which orbital each electron can be ([hyperfine structure](#hyperfine-structure) is ignored). It doesn't even have to be the ground state: we can make some electrons excited at will. 

The best thing to learn this is likely to draw out all the possible configurations explicitly, and then understand what is the term symbol for each possible configuration, see e.g. [term symbols for carbon ground state](#term-symbols-for-carbon-ground-state).

It also confusing how uppercase letters S, P and D are used, when they do not refer to orbitals s, p and d, but rather to states which have the same angular momentum as individual electrons in those states.

It is also very confusing how extremelly close it looks to [spectroscopic notation](#spectroscopic-notation)!

The form of the term symbol is:

$$
^{2S + 1}L_J
$$

The $2S + 1$ can be understood directly as the degeneracy, how many configurations we have in that state.

<a id="video-atomic-term-symbols-by-tmp-chem-2015"></a>
**[Video 14](#video-atomic-term-symbols-by-tmp-chem-2015). Atomic Term Symbols by TMP Chem (2015)** [Source](https://www.youtube.com/watch?v=dhARbw8cdDE).

<a id="video-atomic-term-symbols-by-t-daniel-crawford-2016"></a>
**[Video 15](#video-atomic-term-symbols-by-t-daniel-crawford-2016). Atomic Term Symbols by T. Daniel Crawford (2016)** [Source](https://www.youtube.com/watch?v=DAgEmLWpYjs). - [https://youtu.be/DAgEmLWpYjs?t=2675](https://youtu.be/DAgEmLWpYjs?t=2675) [term symbols for carbon ground state](#term-symbols-for-carbon-ground-state)

---

Bibliography:
- [https://chem.libretexts.org/Bookshelves/Physical_and_Theoretical_Chemistry_Textbook_Maps/Supplemental_Modules_(Physical_and_Theoretical_Chemistry)/Spectroscopy/Electronic_Spectroscopy/Spin-orbit_Coupling/Atomic_Term_Symbols](https://chem.libretexts.org/Bookshelves/Physical_and_Theoretical_Chemistry_Textbook_Maps/Supplemental_Modules_(Physical_and_Theoretical_Chemistry)/Spectroscopy/Electronic_Spectroscopy/Spin-orbit_Coupling/Atomic_Term_Symbols)
- [https://chem.libretexts.org/Courses/Pacific_Union_College/Quantum_Chemistry/08%3A_Multielectron_Atoms/8.08%3A_Term_Symbols_Gives_a_Detailed_Description_of_an_Electron_Configuration](https://chem.libretexts.org/Courses/Pacific_Union_College/Quantum_Chemistry/08%3A_Multielectron_Atoms/8.08%3A_Term_Symbols_Gives_a_Detailed_Description_of_an_Electron_Configuration) The PDF origin: [https://web.chem.ucsb.edu/~devries/chem218/Term%20symbols.pdf](https://web.chem.ucsb.edu/~devries/chem218/Term%20symbols.pdf)
- [https://chem.libretexts.org/Bookshelves/Inorganic_Chemistry/Inorganic_Coordination_Chemistry_(Landskron)/08%3A_Coordination_Chemistry_III_-_Electronic_Spectra/8.01%3A_Quantum_Numbers_of_Multielectron_Atoms](https://chem.libretexts.org/Bookshelves/Inorganic_Chemistry/Inorganic_Coordination_Chemistry_(Landskron)/08%3A_Coordination_Chemistry_III_-_Electronic_Spectra/8.01%3A_Quantum_Numbers_of_Multielectron_Atoms)
- [https://physics.stackexchange.com/questions/8567/how-do-electron-configuration-microstates-map-to-term-symbols](https://physics.stackexchange.com/questions/8567/how-do-electron-configuration-microstates-map-to-term-symbols) How do electron configuration microstates map to term symbols?

<h6 id="hund-s-rules">Hund's rules</h6>

↑ **Parent:** [Term symbol](#term-symbol)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Hund's_rules)

Allow us to determine with good approximation in a multi-electron atom which [electron configuration](#electron-configuration) have more energy. It is a bit like the [Aufbau principle](#aufbau-principle), but at a finer resolution.

Note that this is not trivial since there is no explicit solution to the [Schrödinger equation](#schrodinger-equation) for multi-electron atoms [like there is for hydrogen](#schrodinger-equation-solution-for-the-hydrogen-atom).

For example, consider carbon which has [electron configuration](#electron-configuration) 1s2 2s2 2p2.

If we were to populate the 3 [p-orbitals](#p-orbital) with two electrons with spins either up or down, which has more energy? E.g. of the following two:
```
m_L -1  0  1
    u_ u_ __
    u_ __ u_
    __ ud __
```

<h6 id="hund-s-first-rule">Hund's first rule</h6>

↑ **Parent:** [Hund's rules](#hund-s-rules)

Higher spin multiplicity means lower energy. I.e.: you want to keep all spins pointin in the same direction.

<h6 id="hund-s-second-rule">Hund's second rule</h6>

↑ **Parent:** [Hund's rules](#hund-s-rules)

###### Term symbols for carbon ground state

↑ **Parent:** [Solutions for the Schrodinger equation with multiple particles](#solutions-for-the-schrodinger-equation-with-multiple-particles)

This example covered for example at [Video 16. "Term Symbols Example 1 by TMP Chem (2015)"](#video-term-symbols-example-1-by-tmp-chem-2015).

[Carbon](chemistry.md#carbon) has electronic structure 1s2 2s2 2p2.

For term symbols we only care about unfilled layers, because in every filled layer the total z angular momentum is 0, as one electron necessarily cancels out each other:
- [magnetic quantum number](#magnetic-quantum-number) varies from -l to +l, each with z angular momentum $-l \hbar$ to $+l \hbar$ and so each cancels the other out
- [spin quantum number](#spin-quantum-number) is either + or minus half, and so each pair of electron cancels the other out

So in this case, we only care about the 2 electrons in 2p2. Let's list out all possible ways in which the 2p2 electrons can be.

There are 3 p orbitals, with three different [magnetic quantum numbers](#magnetic-quantum-number), each representing a different possible z [quantum angular momentum](#angular-momentum-operator).

We are going to distribute 2 electrons with 2 different spins across them. All the possible distributions that don't violate the [Pauli exclusion principle](relativistic-quantum-mechanics.md#pauli-exclusion-principle) are:

```
m_l  +1  0 -1  m_L  m_S
     u_ u_ __    1    1
     u_ __ u_    0    1
     __ u_ u_   -1    1
     d_ d_ __    1   -1
     d_ __ d_    0   -1
     __ d_ d_   -1   -1
     u_ d_ __    1    0
     d_ u_ __    1    0
     u_ __ d_    0    0
     d_ __ u_    0    0
     __ u_ d_   -1    0
     __ d_ u_   -1    0
     ud __ __    2    0
     __ ud __    0    0
     __ __ ud   -2    0
```

where:
- `m_l` is $m_l$, the [magnetic quantum number](#magnetic-quantum-number) of each electron. Remember that this gives a orbital (non-spin) [quantum angular momentum](#angular-momentum-operator) of $m_l \hbar$ to each such electron
- `m_L` with a capital L is the sum of the $m_l$ of each electron
- `m_S` with a capital S is the sum of the spin angular momentum of each electron

For example, on the first line:
```
m_l  +1  0 -1  m_L  m_S
     u_ u_ __    1    1
```
we have:
- one electron with $m_l = +1$, and so angular momentum $\hbar$
- one electron with $m_l = +0$, and so angular momentum 0
and so the sum of them has angular momentum $0 + 1 \hbar = 1 \hbar$. So the value of $m_L$ is 1, we just omit the $\hbar$.

TODO now I don't understand the logic behind the next steps... I understand how to mechanically do them, but what do they mean? Can you determine the [term symbol](#term-symbol) for individual microstates at all? Or do you have to group them to get the answer? Since there are multiple choices in some steps, it appears that you can't assign a specific term symbol to an individual microstate. And it has something to do with the [Slater determinant](relativistic-quantum-mechanics.md#slater-determinant). The previous lecture mentions it: [https://www.youtube.com/watch?v=7_8n1TS-8Y0](https://www.youtube.com/watch?v=7_8n1TS-8Y0) more precisely [https://youtu.be/7_8n1TS-8Y0?t=2268](https://youtu.be/7_8n1TS-8Y0?t=2268) about carbon.

[https://youtu.be/DAgEmLWpYjs?t=2675](https://youtu.be/DAgEmLWpYjs?t=2675) mentions that $^{3}D$ is not allowed because it would imply $L = 2, S = 1$, which would be a state `uu __ __` which violates the [Pauli exclusion principle](relativistic-quantum-mechanics.md#pauli-exclusion-principle), and so was not listed on our list of 15 states.

He then goes for $^{1}D$ and mentions:
- S = 1 so $m_S$ can only be 0
- L = 2 (D) so $m_L$ ranges in -2, -1, 0, 1, 2
and so that corresponds to states on our list:
```
ud __ __    2    0
u_ d_ __    1    0
u_ __ d_    0    0
__ u_ d_   -1    0
__ __ ud   -2    0
```
Note that for some we had a two choices, so we just pick any one of them and tick them off off from the table, which now looks like:
```
 +1  0 -1  m_L  m_S
 u_ u_ __    1    1
 u_ __ u_    0    1
 __ u_ u_   -1    1
 d_ d_ __    1   -1
 d_ __ d_    0   -1
 __ d_ d_   -1   -1
 d_ u_ __    1    0
 d_ __ u_    0    0
 __ d_ u_   -1    0
 __ ud __    0    0
```

Then for $^{3}P$ the choices are:
- S = 2 so $m_S$ is either -1, 0  or 1
- L = 1 (P) so $m_L$ ranges in -1, 0, 1
so we have 9 possibilities for both together. We again verify that 9 such states are left matching those criteria, and tick them off, and so on.

For the $m_S$, we have two electrons with spin up. The angular momentum of each electron is $1/2 \hbar$, and so given that we have two, the total is $1 \hbar$, so again we omit $\hbar$ and $m_S$ is 1.

<a id="video-term-symbols-example-1-by-tmp-chem-2015"></a>
**[Video 16](#video-term-symbols-example-1-by-tmp-chem-2015). Term Symbols Example 1 by TMP Chem (2015)** [Source](https://www.youtube.com/watch?v=doC9Z2S7lm8). Carbon atom.

Bibliography:
- [https://youtu.be/DAgEmLWpYjs?t=1962](https://youtu.be/DAgEmLWpYjs?t=1962) from [Video 15. "Atomic Term Symbols by T. Daniel Crawford (2016)"](#video-atomic-term-symbols-by-t-daniel-crawford-2016)

<h6 id="schrodinger-equation-solution-for-molecule">Schrödinger equation solution for molecule</h6>

↑ **Parent:** [Solutions for the Schrodinger equation with multiple particles](#solutions-for-the-schrodinger-equation-with-multiple-particles)

<h6 id="schrodinger-equation-solution-for-the-hydrogen-molecule">Schrödinger equation solution for the hydrogen molecule</h6>

↑ **Parent:** [Schrödinger equation solution for molecule](#schrodinger-equation-solution-for-molecule)

Can we make any ab initio predictions about it all?

A 2016 paper: [https://aip.scitation.org/doi/abs/10.1063/1.4948309](https://aip.scitation.org/doi/abs/10.1063/1.4948309)

<a id="video-quantum-chemistry-10-1-hydrogen-molecule-hamiltonian-by-tmp-chem-2016"></a>
**[Video 17](#video-quantum-chemistry-10-1-hydrogen-molecule-hamiltonian-by-tmp-chem-2016). Quantum Chemistry 10.1 - Hydrogen Molecule Hamiltonian by TMP Chem (2016)** [Source](https://www.youtube.com/watch?v=BBoE6NRRZ8k). Continued in the following videos, uses the [Born–Oppenheimer approximation](#born-oppenheimer-approximation). Does not give predictions vs experiment?

###### Chemical bond

↑ **Parent:** [Schrödinger equation solution for molecule](#schrodinger-equation-solution-for-molecule)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Chemical_bond)

###### Molecule

↑ **Parent:** [Chemical bond](#chemical-bond)  
🏷️ **Tags:** [Chemical compound](chemistry.md#chemical-compound)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Molecule)

###### Molecule representation

↑ **Parent:** [Molecule](#molecule)

###### Ball-and-stick model

↑ **Parent:** [Molecule representation](#molecule-representation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Ball-and-stick_model)

<a id="image-ball-and-stick-model-of-proline"></a>
![](https://upload.wikimedia.org/wikipedia/commons/c/ca/Proline_model.jpg)

**[Figure 5](#image-ball-and-stick-model-of-proline). Ball-and-stick model of proline**. [Source](https://commons.wikimedia.org/wiki/File:Proline_model.jpg).

###### Isomer

↑ **Parent:** [Molecule](#molecule)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Isomer)

Isomers were quite confusing for early chemists, before [atomic theory](chemistry.md#atom) was widely accepted, and people where thinking mostly in terms of proportions of equations, related: [Section "Isomers suggest that atoms exist"](chemistry.md#isomers-suggest-that-atoms-exist).

###### Cis-trans isomerism

↑ **Parent:** [Isomer](#isomer)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Cis–trans isomerism)

Exist because [double bonds](#double-bond) don't rotate freely. Have different properties of course, unlike [enantiomer](#enantiomer).

Bibliography:
- [https://chem.libretexts.org/Bookshelves/Organic_Chemistry/Map%3A_Essential_Organic_Chemistry_(Bruice)/06%3A_Isomers_and_Stereochemistry/5.01%3A_Cis-Trans_Isomers_Result_from_Restricted_Rotation](https://chem.libretexts.org/Bookshelves/Organic_Chemistry/Map%3A_Essential_Organic_Chemistry_(Bruice)/06%3A_Isomers_and_Stereochemistry/5.01%3A_Cis-Trans_Isomers_Result_from_Restricted_Rotation) from [LibreTexts](social-technology.md#libretexts)

###### Enantiomer

↑ **Parent:** [Isomer](#isomer)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Enantiomer)

Mirror images.

Key exmaple: [d and L amino acids](protein.md#d-and-l-amino-acids). Enantiomers have identical physico-chemical properties. But their biological roles can be very different, because an [enzyme](protein.md#enzyme) might only be able to act on one of them.

###### Polymorphism (materials science)

↑ **Parent:** [Isomer](#isomer)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Polymorphism_(materials_science))

TODO definition. Appears to be [isomers](#isomer)

Example:
- the three most table polymorphs of [calcium carbonate polymorphs](chemistry.md#calcium-carbonate-polymorph) are:
  - [calcite](chemistry.md#calcite)
  - [aragonite](chemistry.md#aragonite)
  - [vaterite](chemistry.md#vaterite)

###### Stereochemistry

↑ **Parent:** [Isomer](#isomer)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Stereochemistry)

Molecules that are the same if you just look at "what atom is linked to what atom", they are only different if you consider the relative spacial positions of atoms.

###### Covalent bond

↑ **Parent:** [Chemical bond](#chemical-bond)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Covalent_bond)

###### Sigma bond

↑ **Parent:** [Covalent bond](#covalent-bond)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Sigma_bond)

###### Pi bond

↑ **Parent:** [Covalent bond](#covalent-bond)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Pi_bond)

###### Double bond

↑ **Parent:** [Pi bond](#pi-bond)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Double_bond)

###### Triple bond

↑ **Parent:** [Pi bond](#pi-bond)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Triple_bond)

###### Ionic bond

↑ **Parent:** [Chemical bond](#chemical-bond)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Ionic_bond)

###### Octet rule

↑ **Parent:** [Chemical bond](#chemical-bond)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Octet_rule)

##### Two-state quantum system

↑ **Parent:** [Solutions of the Schrodinger equation](#solutions-of-the-schrodinger-equation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Two-state_quantum_system)

[Discrete](calculus.md#discrete) quantum system model that can model both [spin](relativistic-quantum-mechanics.md#spin-physics) in the [Stern-Gerlach experiment](relativistic-quantum-mechanics.md#stern-gerlach-experiment) or [photon polarization](photon.md#photon-polarization) in [polarizer](photon.md#polarizer).

Also known in [quantum computing](quantum-computing.md) as a qubit :-)

###### Bloch sphere

↑ **Parent:** [Two-state quantum system](#two-state-quantum-system)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Bloch_sphere)

[https://physics.stackexchange.com/questions/204090/understanding-the-bloch-sphere/598254#598254](https://physics.stackexchange.com/questions/204090/understanding-the-bloch-sphere/598254#598254)

A more concrete and easier to understand version of it is the more [photon](photon.md)-specific [Poincaré sphere](photon.md#poincare-sphere), have a look at that one first.

###### Pauli matrix

↑ **Parent:** [Two-state quantum system](#two-state-quantum-system)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Pauli_matrices)

[2D representation of $SU(2)$](geometry.md#2d-representation-of-su-2).

#### Born-Oppenheimer approximation

↑ **Parent:** [Schrödinger equation](#schrodinger-equation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Born–Oppenheimer_approximation)

#### Uncertainty principle

↑ **Parent:** [Schrödinger equation](#schrodinger-equation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Uncertainty_principle)

The wave equation contains the entire state of a particle.

From [mathematical formulation of quantum mechanics](#mathematical-formulation-of-quantum-mechanics) remember that the wave equation is a vector in [Hilbert space](calculus.md#hilbert-space).

And a single vector can be represented in many different ways in different basis, and two of those ways happen to be the position and the momentum representations.

More importantly, position and momentum are first and foremost operators associated with observables: the [position operator](#position-operator) and the [momentum operator](#momentum-operator). And both of their eigenvalue sets form a basis of the [Hilbert space](calculus.md#hilbert-space) according to the [spectral theorem](linear-algebra.md#spectral-theorem).

When you represent a wave equation as a function, you have to say what the variable of the function means. And depending on weather you say "it means position" or "it means momentum", the position and momentum operators will be written differently.

This is well shown at: [Video 9. "Visualization of Quantum Physics (Quantum Mechanics) by udiprod (2017)"](#video-visualization-of-quantum-physics-quantum-mechanics-by-udiprod-2017).

Furthermore, the position and momentum representations are equivalent: one is the [Fourier transform](calculus.md#fourier-transform) of the other: [position and momentum space](#position-and-momentum-space). Remember that notably we can always take the Fourier transform of a function in [$\LTwo$](calculus.md#l2) due to [Carleson's theorem](calculus.md#carleson-s-theorem).

Then the uncertainty principle follows immediately from a general property of the Fourier transform: [https://en.wikipedia.org/w/index.php?title=Fourier_transform&oldid=961707157#Uncertainty_principle](https://en.wikipedia.org/w/index.php?title=Fourier_transform&oldid=961707157#Uncertainty_principle)

In precise terms, the [uncertainty principle](#uncertainty-principle) talks about the [standard deviation](mathematics.md#standard-deviation) of two measures.

We can visualize the uncertainty principle more intuitively by thinking of a [wave function](#wave-function) that is a [real](formalization-of-mathematics.md#real-number) [flat top bump function](calculus.md#flat-top-bump-function) with a flat top in [1D](calculus.md#real-line). We can then change the width of the support, but when we do that, the top goes higher to keep probability equal to 1. The momentum is 0 everywhere, except in the edges of the support. Then:
- to localize the wave in space at position 0 to reduce the space uncertainty, we have to reduce the support. However, doing so makes the momentum variation on the edges more and more important, as the slope will go up and down faster (higher top, and less x space for descent), leading to a larger variance (note that average momentum is still 0, due to to symmetry of the bump function)
- to localize the momentum as much as possible at 0, we can make the support wider and wider. This makes the bumps at the edges smaller and smaller. However, this also obviously delocalises the wave function more and more, increasing the variance of x

Bibliography:
- [https://www.youtube.com/watch?v=bIIjIZBKgtI&list=PL54DF0652B30D99A4&index=59](https://www.youtube.com/watch?v=bIIjIZBKgtI&list=PL54DF0652B30D99A4&index=59) "K2. Heisenberg Uncertainty Relation" by doctorphys (2011)
- [https://physics.stackexchange.com/questions/132111/uncertainty-principle-intuition](https://physics.stackexchange.com/questions/132111/uncertainty-principle-intuition) Uncertainty Principle Intuition on [Physics Stack Exchange](stack-overflow.md#physics-stack-exchange)

##### Position and momentum space

↑ **Parent:** [Uncertainty principle](#uncertainty-principle)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Position_and_momentum_space)

One of the main reasons why physicists are obsessed by this topic is that position and momentum are mapped to the [phase space coordinates](mechanics.md#phase-space-coordinate) of [Hamiltonian mechanics](mechanics.md#hamiltonian-mechanics), which appear in the [matrix mechanics](#matrix-mechanics) formulation of [quantum mechanics](quantum-mechanics.md), which offers insight into the theory, particularly when generalizing to [relativistic quantum mechanics](relativistic-quantum-mechanics.md).

One way to think is: what is the definition of space space? It is a way to write the wave function $\psi_x(x)$ such that:
- the position operator is the multiplication by $x$
- the momentum operator is the derivative by $x$
And then, what is the definition of momentum space? It is of course a way to write the wave function $\psi_p(p)$ such that:
- the momentum operator is the multiplication by $p$

[https://physics.stackexchange.com/questions/39442/intuitive-explanation-of-why-momentum-is-the-fourier-transform-variable-of-posit/39508#39508](https://physics.stackexchange.com/questions/39442/intuitive-explanation-of-why-momentum-is-the-fourier-transform-variable-of-posit/39508#39508) gives the best idea intuitive idea: the [Fourier transform](calculus.md#fourier-transform) writes a function as a (continuous) sum of plane waves, and each plane wave has a fixed momentum.

Bibliography:
- [https://en.wikipedia.org/wiki/Position_and_momentum_space](https://en.wikipedia.org/wiki/Position_and_momentum_space)

###### Position representation

↑ **Parent:** [Position and momentum space](#position-and-momentum-space)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Position_representation)

A way to write the wavefunction $\psi(x)$ such that the [position operator](#position-operator) is:

$$
x
$$

i.e., a function that takes the wavefunction as input, and outputs another function:

$$
x \psi(x)
$$

If you believe that [mathematicians](mathematics.md#mathematician) took care of [continuous spectrum](linear-algebra.md#continuous-spectrum-functional-analysis) for us and that everything just works, the most concrete and direct thing that this representation tells us is that:

> the probability of finding a particle between $x_0$ and $x_1$ at time $t$

equals:

$$
\int_{x_0}^{x_1}x \psi{x, t} dx
$$

###### Position operator

↑ **Parent:** [Position and momentum space](#position-and-momentum-space)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Position_operator)

This operator case is surprisingly not necessarily mathematically trivial to describe formally because you often end up getting into the [Dirac delta functions](calculus.md#dirac-delta-function)/continuous spectrum: as mentioned at: [mathematical formulation of quantum mechanics](#mathematical-formulation-of-quantum-mechanics)

###### Momentum operator

↑ **Parent:** [Position and momentum space](#position-and-momentum-space)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Momentum_operator)

One dimension in [position representation](#position-representation):

$$
\hat{p} = - i \hbar \pdv{}{x}
$$

In three dimensions In position representation, we define it by using the [gradient](calculus.md#gradient), and so we see that 

$$
\hat{p} = - i \hbar \pdv{}{x}
$$

<a id="video-position-and-momentum-from-wavefunctions-by-faculty-of-khan-2018"></a>
**[Video 18](#video-position-and-momentum-from-wavefunctions-by-faculty-of-khan-2018). Position and Momentum from Wavefunctions by Faculty of Khan (2018)** [Source](https://www.youtube.com/watch?v=Egu4i8umpoM). Proves in detail why the [momentum operator](#momentum-operator) is $\pdv{}{x}$. The starting point is determining the time [derivative](calculus.md#derivative) of the [expectation value](mathematics.md#expectation-value) of the [position operator](#position-operator).

###### Squeezed coherent state

↑ **Parent:** [Position and momentum space](#position-and-momentum-space)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Squeezed_coherent_state)

##### Energy operator

↑ **Parent:** [Uncertainty principle](#uncertainty-principle)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Energy_operator)

Appears directly on [Schrödinger equation](#schrodinger-equation)! And in particular in the [time-independent Schrödinger equation](#time-independent-schrodinger-equation).

###### Time-energy uncertainty principle

↑ **Parent:** [Energy operator](#energy-operator)

There is also a time-energy [uncertainty principle](#uncertainty-principle), because those two operators are also [complementary](#complementarity-physics).

##### Angular momentum operator

↑ **Parent:** [Uncertainty principle](#uncertainty-principle)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Angular_momentum_operator)

Basically the operators are just analogous to the classical ones e.g. the classical:

$$
L_z = x p_y - y p_x
$$

becomes:

$$
\hat{L}_z = -i \hbar \left( x\pdv{}{y} - y\pdv{}{x} \right)
$$

Besides the angular momentum in each direction, we also have the [total angular momentum](#total-angular-momentum-operator):

$$
\hat{L}^2 = \hat{L}_x + \hat{L}_y + \hat{L}_z
$$

Then you have to understand what each one of those does to the each [atomic orbital](#atomic-orbital):
- total angular momentum: determined by the [azimuthal quantum number](#azimuthal-quantum-number)
- angular momentum in one direction ($z$ by convention): determined by the [magnetic quantum number](#magnetic-quantum-number)

There is an [uncertainty principle](#uncertainty-principle) between the x, y and z angular momentums, we can only measure one of them with certainty at a time. [Video 19. "Quantum Mechanics 7a - Angular Momentum I by ViaScience (2013)"](#video-quantum-mechanics-7a-angular-momentum-i-by-viascience-2013) justifies this intuitively by mentioning that this is analogous to [precession](mechanics.md#precession): if you try to measure electrons e.g. with the [Zeeman effect](#zeeman-effect) the precess on the other directions which you end up modifing.

TODO experiment. Likely [Zeeman effect](#zeeman-effect).

<a id="video-quantum-mechanics-7a-angular-momentum-i-by-viascience-2013"></a>
**[Video 19](#video-quantum-mechanics-7a-angular-momentum-i-by-viascience-2013). Quantum Mechanics 7a - Angular Momentum I by ViaScience (2013)** [Source](https://youtube.com/watch?v=NwbvTa2xV9k).

###### Total angular momentum operator

↑ **Parent:** [Angular momentum operator](#angular-momentum-operator)

See: [angular momentum operator](#angular-momentum-operator).

##### Complementarity (physics)

↑ **Parent:** [Uncertainty principle](#uncertainty-principle)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Complementarity_(physics))

#### Conservation laws in Schrodinger equations

↑ **Parent:** [Schrödinger equation](#schrodinger-equation)

[https://physics.stackexchange.com/questions/229885/energy-equation-in-quantum-mechanics](https://physics.stackexchange.com/questions/229885/energy-equation-in-quantum-mechanics)

TODO is there any good intuitive argument or proof of conservation of energy, momentum, angular momentum?

##### Conservation of the square amplitude in the Schrodinger equation

↑ **Parent:** [Conservation laws in Schrodinger equations](#conservation-laws-in-schrodinger-equations)

Proof that the probability 1 is conserved by the time evolution:

It can be derived directly from the [Schrödinger equation](#schrodinger-equation).

Bibliography:
- [https://quantummechanics.ucsd.edu/ph130a/130_notes/node127.html](https://quantummechanics.ucsd.edu/ph130a/130_notes/node127.html) from [quantum physics by Jim Branson (2003)](#quantum-physics-by-jim-branson-2003).

  That proof also mentions that if the potential `V` is not real, then there is no conservation of probability! Therefore the potential _must_ be real valued!

###### Probability current

↑ **Parent:** [Conservation of the square amplitude in the Schrodinger equation](#conservation-of-the-square-amplitude-in-the-schrodinger-equation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Probability_current)

#### Wave function

↑ **Parent:** [Schrödinger equation](#schrodinger-equation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Wave_function)

Contains the full state of the quantum system.

This is in contrast to classical mechanics where e.g. the state of mechanical system is given by two real functions: position and speed.

The wave equation in [position representation](#position-representation) on the other hand encodes speed in "how fast does the complex phase spin around", and direction in "does it spin clockwise or counterclockwise", as described well at: [Video 9. "Visualization of Quantum Physics (Quantum Mechanics) by udiprod (2017)"](#video-visualization-of-quantum-physics-quantum-mechanics-by-udiprod-2017). Then once you understand that, it is more compact to just view those graphs with the phase color coded as in [Video 7. "Simulation of the time-dependent Schrodinger equation (JavaScript Animation) by Coding Physics (2019)"](#video-simulation-of-the-time-dependent-schrodinger-equation-javascript-animation-by-coding-physics-2019).

##### Matter wave

↑ **Parent:** [Wave function](#wave-function)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Matter_wave)

###### Electron diffraction experiment

↑ **Parent:** [Matter wave](#matter-wave)

###### Diffraction of Cathode Rays by a Thin Film by Thomson and Reid (1927)

↑ **Parent:** [Electron diffraction experiment](#electron-diffraction-experiment)

[https://www.nature.com/articles/119890a0](https://www.nature.com/articles/119890a0)

###### Davisson-Germer experiment

↑ **Parent:** [Electron diffraction experiment](#electron-diffraction-experiment)  
🏷️ **Tags:** [1937 Nobel Prize in Physics](nobel-prize.md#1937-nobel-prize-in-physics), [Quantum mechanics experiment](#quantum-mechanics-experiment)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Davisson–Germer_experiment)

<a id="image-schematic-of-the-davisson-germer-experiment"></a>
![](https://upload.wikimedia.org/wikipedia/commons/thumb/4/4e/Davisson-Germer_experiment.svg/960px-Davisson-Germer_experiment.svg.png)

**[Figure 6](#image-schematic-of-the-davisson-germer-experiment). Schematic of the Davisson-Germer experiment**. [Source](https://commons.wikimedia.org/wiki/File:Davisson-Germer_experiment.svg.png).

###### de Broglie relations

↑ **Parent:** [Matter wave](#matter-wave)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Matter_wave#de_Broglie_relations)

Relates particle momentum and its wavelength, or equivalently, energy and frequency.

The wavelength relation is:

$$
\lambda = \frac{h}{p}
$$

but since:

$$
v = \lambda f
E = p v
$$

the wavelength relation implies:

$$
\frac{v}{f} = \frac{h}{p}
f = \frac{v p}{h}  = \frac{E}{h}
$$

Particle wavelength can be for example measured very directly on a [double-slit experiment](#double-slit-experiment).

So if we take for example electrons of different speeds, we should be able to see the diffraction pattern change accordingly.

### Equivalent alternatives to the Schrodinger equation

↑ **Parent:** [Non-relativistic quantum mechanics](#non-relativistic-quantum-mechanics)

#### Matrix mechanics

↑ **Parent:** [Equivalent alternatives to the Schrodinger equation](#equivalent-alternatives-to-the-schrodinger-equation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Matrix_mechanics)

Published by [Werner Heisenberg](physicist.md#werner-heisenberg) in 1925-07-25 as [quantum mechanical re-interpretation of kinematic and mechanical relations by Heisenberg (1925)](#quantum-mechanical-re-interpretation-of-kinematic-and-mechanical-relations-by-heisenberg-1925), it offered the first general formulation of quantum mechanics.

It is apparently more closely related to the [ladder operator](#ladder-operator) method, which is a more [algebraic](algebra.md) than the more [analytical](calculus.md#mathematical-analysis) [Schrödinger equation](#schrodinger-equation).

It appears that this formulation makes the importance of the [Poisson bracket](mechanics.md#poisson-bracket) clear, and explains why [physicists](physicist.md) are so obsessed with talking about [position and momentum space](#position-and-momentum-space). This point of view also apparently makes it clearer that [quantum mechanics](quantum-mechanics.md) can be seen as a generalization of [classical mechanics](mechanics.md#classical-mechanics) through the [Hamiltonian](mechanics.md#hamiltonian-mechanics).

[QED and the men who made it: Dyson, Feynman, Schwinger, and Tomonaga by Silvan Schweber (1994)](quantum-field-theory.md#qed-and-the-men-who-made-it-dyson-feynman-schwinger-and-tomonaga-by-silvan-schweber-1994) mentions however that [relativistic quantum mechanics](relativistic-quantum-mechanics.md) broke that analogy, because some 2x2 matrix had a different form, TODO find that again.

[Inward Bound by Abraham Pais (1988)](particle-physics.md#inward-bound-by-abraham-pais-1988) chapter 12 "Quantum mechanics, an essay" part (c) "A chronology" has some ultra brief, but worthwhile mentions of matrix mechanics and the [commutator](algebra.md#commutator).

##### Quantum mechanical re-interpretation of kinematic and mechanical relations by Heisenberg (1925)

↑ **Parent:** [Matrix mechanics](#matrix-mechanics)  
🏷️ **Tags:** [Paper by Werner Heisenberg](physicist.md#paper-by-werner-heisenberg)

This [Heisenberg](physicist.md#werner-heisenberg)'s breakthrough paper on [matrix mechanics](#matrix-mechanics) which later led to the [Schrödinger equation](#schrodinger-equation), see also: [history of quantum mechanics](#history-of-quantum-mechanics).

Published on the [Zeitschrift für Physik](education.md#zeitschrift-fur-physik) volume 33 page pages 879-893, [https://link.springer.com/article/10.1007%2FBF01328377](https://link.springer.com/article/10.1007%2FBF01328377)

Modern overview: [http://www.mat.unimi.it/users/galgani/arch/heisenberg25amer_j_phys.pdf](http://www.mat.unimi.it/users/galgani/arch/heisenberg25amer_j_phys.pdf)

##### Heisenberg picture

↑ **Parent:** [Matrix mechanics](#matrix-mechanics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Heisenberg_picture)

Basically the same as [matrix mechanics](#matrix-mechanics) it seems, just a bit more generalized.

#### De Broglie-Bohm theory

↑ **Parent:** [Equivalent alternatives to the Schrodinger equation](#equivalent-alternatives-to-the-schrodinger-equation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/De Broglie–Bohm theory)

Deterministic, but [non-local](physics.md#principle-of-locality).

## Planck-Einstein relation

↑ **Parent:** [Quantum mechanics](quantum-mechanics.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Planck–Einstein_relation)

Photon energy is proportional to its frequency:

$$
energy = (plancks \space constant) * (frequency)
$$

or with common weird variables:

$$
E = h * \nu
$$

This only makes sense if the [photon](photon.md) exists, there is no classical analogue, because the energy of classical waves depends only on their amplitude, not frequency.

Experiments that suggest this:
- [photoelectric effect](physics.md#photoelectric-effect)
- [Compton scattering](physics.md#compton-scattering)

### Planck constant

↑ **Parent:** [Planck-Einstein relation](#planck-einstein-relation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Planck_constant)

Proportionality factor in the [Planck-Einstein relation](#planck-einstein-relation) between light energy and frequency.

And analogously for matter, appears in the [de Broglie relations](#de-broglie-relations) relating momentum and frequency. Also appears in the [Schrödinger equation](#schrodinger-equation), basically as a consequence/cause of the de Broglie relations most likely.

Intuitively, the [Planck constant](#planck-constant) determines at what length scale do quantum effects start to show up for a given energy scale. It is because the Plank constant is very small that we don't perceive quantum effects on everyday energy/length/time scales. On the $\lim_{h \to 0}$, quantum mechanics disappears entirely.

A very direct way of thinking about it is to think about what would happen in a [double-slit experiment](#double-slit-experiment). TODO think more clearly what happens there.

Defined exactly in the [2019 redefinition of the SI base units](system-of-units.md#2019-redefinition-of-the-si-base-units) to:

$$
6.62607015 \times 10^{-34} J \cdot s
$$

#### Reduced Planck constant

↑ **Parent:** [Planck constant](#planck-constant)

Appears in the [Schrödinger equation](#schrodinger-equation).

Equals the quantum of [angular momentum](mechanics.md#angular-momentum) in the [Bohr model](chemistry.md#bohr-model).

## Relativistic quantum mechanics

↑ **Parent:** [Quantum mechanics](quantum-mechanics.md)

[This section is present in another page, follow this link to view it.](relativistic-quantum-mechanics.md)

## Quantization (physics)

↑ **Parent:** [Quantum mechanics](quantum-mechanics.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Quantization_(physics))

[Quantum field theory lecture by Tobias Osborne (2017)](quantum-field-theory.md#quantum-field-theory-lecture-by-tobias-osborne-2017) mentions that quantization is a guess.

### Quantization of a real scalar field

↑ **Parent:** [Quantization (physics)](#quantization-physics)

This is one of the first examples in most [quantum field theory](quantum-field-theory.md).

It usually does not involve any forces, just the interpretation of what the [quantum field](quantum-field-theory.md#quantum-field) is.

[https://www.youtube.com/watch?v=zv94slY6WqY&list=PLSpklniGdSfSsk7BSZjONcfhRGKNa2uou&index=2](https://www.youtube.com/watch?v=zv94slY6WqY&list=PLSpklniGdSfSsk7BSZjONcfhRGKNa2uou&index=2) Quantization Of A Free Real Scalar Field by Dietterich Labs (2019)

## Quantum superposition

↑ **Parent:** [Quantum mechanics](quantum-mechanics.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Quantum_superposition)

Quantum superposition is really weird because it is fundamentally different than "either definite state but I don't know which", because the superposition state leads to different measurements than the non-superposition state.

Examples:
- [https://www.youtube.com/watch?v=tt8gVXDsh7Q](https://www.youtube.com/watch?v=tt8gVXDsh7Q) "Interference in quantum mechanics" by [Looking Glass Universe](physics.md#looking-glass-universe) (2015) shows how a left-right [spin](relativistic-quantum-mechanics.md#spin-physics) measurement has a defined value for a superposed half up half down state, but not for a pure up state.

  TODO can this be conducted? As mentioned in the video, this is closely linked to the fact that you can describe the wave function in multiple different bases (up/down or left/right), which is also at the root of the [uncertainty principle](#uncertainty-principle).
- [Video "Quantum Mechanics 9b - Photon Spin and Schrodinger's Cat II by ViaScience (2013)"](photon.md#video-quantum-mechanics-9b-photon-spin-and-schrodinger-s-cat-ii-by-viascience-2013) gives a similar photon version
- it seems that the [single particle double slit experiment](#single-particle-double-slit-experiment) can also be thought of as in terms of a superposition of "the particle goes through the right" and "the particle goes through the right", although it is a bit harder to thing about as it is not a [discrete](calculus.md#discrete) process

## Quantum entanglement

↑ **Parent:** [Quantum mechanics](quantum-mechanics.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Quantum_entanglement)

Quantum entanglement is often called spooky/surprising/unintuitive, but they key question is to understand why.

To understand that, you have to understand why it is fundamentally impossible for the entangled particle pair be in a predefined state [according to experiments done](#bell-test-experiment) e.g. where one is deterministically yes and the other deterministically down.

In other words, why [local hidden-variable theory](#local-hidden-variable-theory) is not valid.

How to generate entangled particles:
- [particle decay](relativistic-quantum-mechanics.md#particle-decay), notably [pair production](relativistic-quantum-mechanics.md#pair-production)
- for [photons](photon.md), notably: [spontaneous parametric down-conversion](photon.md#spontaneous-parametric-down-conversion), e.g.: [https://www.youtube.com/watch?v=tn1sEaw1K2k](https://www.youtube.com/watch?v=tn1sEaw1K2k) "Shanni Prutchi Construction of an Entangled Photon Source" by HACKADAY (2015). Estimatd price: 5000 USD.

<a id="video-bell-s-theorem-the-quantum-venn-diagram-paradox-by-minutephysics-2017"></a>
**[Video 20](#video-bell-s-theorem-the-quantum-venn-diagram-paradox-by-minutephysics-2017). Bell's Theorem: The Quantum Venn Diagram Paradox by minutephysics (2017)** [Source](https://www.youtube.com/watch?v=zcqZHYo7ONs). Contains the clearest [Bell test experiment](#bell-test-experiment) description seen so far.

It clearly describes the [photon](photon.md)-based 22.5, 45 degree/85%/15% probability [photon polarization](photon.md#photon-polarization) experiment and its result conceptually.

It does not mention [spontaneous parametric down-conversion](photon.md#spontaneous-parametric-down-conversion) but that's what they likely hint at.

Done in Collaboration with [3Blue1Brown](mathematics.md#3blue1brown).

Question asking further clarification on why the 100/85/50 thing is surprising: [https://physics.stackexchange.com/questions/357039/why-is-the-quantum-venn-diagram-paradox-considered-a-paradox/597982#597982](https://physics.stackexchange.com/questions/357039/why-is-the-quantum-venn-diagram-paradox-considered-a-paradox/597982#597982)

---

<a id="video-bell-s-inequality-i-by-viascience-2014"></a>
**[Video 21](#video-bell-s-inequality-i-by-viascience-2014). Bell's Inequality I by ViaScience (2014)** [Source](https://www.youtube.com/watch?v=sAXxSKifgtU).

<a id="video-quantum-entanglement-and-spooky-action-at-a-distance-by-veritasium-2015"></a>
**[Video 22](#video-quantum-entanglement-and-spooky-action-at-a-distance-by-veritasium-2015). Quantum Entanglement & Spooky Action at a Distance by Veritasium (2015)** [Source](https://www.youtube.com/watch?v=ZuvK-od647c). Gives a clear explanation of a thought [Bell test experiments](#bell-test-experiment) with [electron](standard-model.md#electron) [spin](relativistic-quantum-mechanics.md#spin-physics) of electron pairs from photon decay with three 120-degree separated slits. The downside is that he does not clearly describe an experimental setup, it is quite generic.

<a id="video-quantum-mechanics-animation-explaining-quantum-physics-by-physics-videos-by-eugene-khutoryansky-2013"></a>
**[Video 23](#video-quantum-mechanics-animation-explaining-quantum-physics-by-physics-videos-by-eugene-khutoryansky-2013). Quantum Mechanics: Animation explaining quantum physics by Physics Videos by Eugene Khutoryansky (2013)** [Source](https://www.youtube.com/watch?v=iVpXrbZ4bnU). Usual Eugene, good animations, and not too precise explanations :-) [https://youtu.be/iVpXrbZ4bnU?t=922](https://youtu.be/iVpXrbZ4bnU?t=922) describes a conceptual spin entangled electron-positron [pair production](relativistic-quantum-mechanics.md#pair-production) [Stern-Gerlach experiment](relativistic-quantum-mechanics.md#stern-gerlach-experiment) as a [Bell test experiments](#bell-test-experiment). The 85% is mentioned, but not explained at all.

<a id="video-quantum-entanglement-spooky-action-at-a-distance-by-don-lincoln-2020"></a>
**[Video 24](#video-quantum-entanglement-spooky-action-at-a-distance-by-don-lincoln-2020). Quantum Entanglement: Spooky Action at a Distance by Don Lincoln (2020)** [Source](https://www.youtube.com/watch?v=JFozGfxmi8A). This only has two merits compared to [Video 22. "Quantum Entanglement & Spooky Action at a Distance by Veritasium (2015)"](#video-quantum-entanglement-and-spooky-action-at-a-distance-by-veritasium-2015): it mentions the [Aspect](physicist.md#alain-aspect) et al. (1982) [Bell test experiment](#bell-test-experiment), and it shows the continuous curve similar to [https://en.wikipedia.org/wiki/File:Bell.svg](https://en.wikipedia.org/wiki/File:Bell.svg). But it just does not clearly explain the bell test.

<a id="video-quantum-entanglement-lab-by-scientific-american-2013"></a>
**[Video 25](#video-quantum-entanglement-lab-by-scientific-american-2013). Quantum Entanglement Lab by Scientific American (2013)** [Source](https://www.youtube.com/watch?v=Z34ugMy1QaA). The hosts interview Professor Enrique Galvez of Colgate University who shows briefly the [optical table](photon.md#optical-table) setup without great details, and then moves to a whiteboard explanation. Treats the audience as stupid, doesn't say the keywords [spontaneous parametric down-conversion](photon.md#spontaneous-parametric-down-conversion) and [Bell's theorem](#bell-s-theorem) which they clearly allude to. You can even them showing a two second footage of the professor explaining the rotation experiments and the data for it, but that's all you get.

<h3 id="bell-s-theorem">Bell's theorem</h3>

↑ **Parent:** [Quantum entanglement](#quantum-entanglement)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Bell's_theorem)

Basically a precise statement of "[quantum entanglement](#quantum-entanglement) is spooky".

#### Bell test experiment

↑ **Parent:** [Bell's theorem](#bell-s-theorem)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Bell_test_experiments)

Some of the most remarkable ones seem to be:
- [Alain Aspect](physicist.md#alain-aspect) 1982
- Hensen et al., Giustina et al., Shalm et al. (2015): "[loophole](#loopholes-in-bell-test-experiments)-free" Bell tests

##### Loopholes in Bell test experiments

↑ **Parent:** [Bell test experiment](#bell-test-experiment)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Loopholes_in_Bell_test_experiments)

#### Local hidden-variable theory

↑ **Parent:** [Bell's theorem](#bell-s-theorem)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Local_hidden-variable_theory)

## No-go theorem

↑ **Parent:** [Quantum mechanics](quantum-mechanics.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/No-go_theorem)

## ↑ Ancestors (5)

1. [Particle physics](particle-physics.md)
2. [Physics](physics.md)
3. [Natural science](science.md#natural-science)
4. [Science](science.md)
5. [Ciro Santilli's Homepage](README.md)

## ← Incoming links (42)

- [Ampere in the 2019 redefinition of the SI base units](system-of-units.md#ampere-in-the-2019-redefinition-of-the-si-base-units)
- [Bra-ket notation](#bra-ket-notation)
- [Classical limit](mechanics.md#classical-limit)
- [Classical mechanics](mechanics.md#classical-mechanics)
- [Condensed matter physics](condensed-matter-physics.md)
- [Continuous spectrum (functional analysis)](linear-algebra.md#continuous-spectrum-functional-analysis)
- [Correspondence principle](mechanics.md#correspondence-principle)
- [Derivation of the Klein-Gordon equation](relativistic-quantum-mechanics.md#derivation-of-the-klein-gordon-equation)
- [Dirac delta function](calculus.md#dirac-delta-function)
- [Distribution (mathematics)](calculus.md#distribution-mathematics)
- [Double-slit experiment](#double-slit-experiment)
- [Dual vector](linear-algebra.md#dual-vector)
- [Einstein solid](condensed-matter-physics.md#einstein-solid)
- [Entropy](statistical-physics.md#entropy)
- [Half-life](particle-physics.md#half-life)
- [Hilbert space](calculus.md#hilbert-space)
- [History of quantum mechanics](#history-of-quantum-mechanics)
- [Inward Bound by Abraham Pais (1988)](particle-physics.md#inward-bound-by-abraham-pais-1988)
- [Lebesgue integral of $\LP$ is complete but Riemann isn't](calculus.md#lebesgue-integral-of-lp-is-complete-but-riemann-isn-t)
- [LibreTexts](social-technology.md#libretexts)
- [Matrix mechanics](#matrix-mechanics)
- [Maxwell's equations in curved spacetime](relativity.md#maxwell-s-equations-in-curved-spacetime)
- [Maxwell's equations with pointlike particles](electromagnetism.md#maxwell-s-equations-with-pointlike-particles)
- [Non-relativistic quantum mechanics](#non-relativistic-quantum-mechanics)
- [GitHub](ourbigbook-com.md#github)
- [Motivation](ourbigbook-com.md#motivation)
- [Perturbation theory](mathematics.md#perturbation-theory)
- [Phase-space formulation](#phase-space-formulation)
- [Position and momentum space](#position-and-momentum-space)
- [Quantum computers as experiments that are hard to predict outcomes](quantum-computing.md#quantum-computers-as-experiments-that-are-hard-to-predict-outcomes)
- [Quantum electrodynamics](quantum-field-theory.md#quantum-electrodynamics)
- [Quantum key distribution](technology.md#quantum-key-distribution)
- [Real world applications of the Lebesgue integral](calculus.md#real-world-applications-of-the-lebesgue-integral)
- [Relativistic quantum mechanics](relativistic-quantum-mechanics.md)
- [Richard Feynman](richard-feynman.md)
- [Schrödinger equation](#schrodinger-equation)
- [Spectral line](#spectral-line)
- [Why you should give money to Ciro Santilli](sponsor.md#why-you-should-give-money-to-ciro-santilli)
- [The Fourier transform is a bijection in $L^2$](calculus.md#the-fourier-transform-is-a-bijection-in-l-2)
- [Tobias J. Osborne](physicist.md#tobias-j-osborne)
- [ViaScience](particle-physics.md#viascience)
- [Wheeler-Feynman absorber theory](quantum-field-theory.md#wheeler-feynman-absorber-theory)
