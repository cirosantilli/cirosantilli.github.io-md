# Condensed matter physics

↑ **Parent:** [Physics](physics.md)  
🏷️ **Tags:** [Emergence](science.md#emergence)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Condensed_matter_physics)

[Condensed matter physics](condensed-matter-physics.md) is one of the best examples of [emergence](science.md#emergence). We start with a bunch of small elements which we understand fully at the required level ([atoms](chemistry.md#atom), [electrons](standard-model.md#electron), [quantum mechanics](quantum-mechanics.md)) but then there are complex properties that show up when we put a bunch of them together.

Includes fun things like:
- [superconductivity](#superconductivity) and [superfluidity](#superfluidity)
- [semiconductors](#semiconductor)

As of 2020, this is the other "fundamental branch of physics" besides to [particle physics](particle-physics.md)/[nuclear physics](particle-physics.md#nuclear-physics).

Condensed matter is basically [chemistry](chemistry.md) but without reactions: you study a fixed state of matter, not a reaction in which compositions change with time.

Just like in chemistry, you end up getting some very well defined substance properties due to the incredibly large number of atoms.

Just like chemistry, the ultimate goal is to do de-novo [computational chemistry](physics.md#computational-chemistry) to predict those properties.

And just like chemistry, what we can actually is actually very limited in part due to the exponential nature of [quantum mechanics](quantum-mechanics.md).

Also since chemistry involves reactions, chemistry puts a huge focus on liquids and solutions, which is the simplest state of matter to do reactions in.

Condensed matter however can put a lot more emphasis on solids than chemistry, notably because solids are what we generally want in end products, no one likes stuff leaking right?

But it also studies liquids, e.g. notably [superfluidity](#superfluidity).

One thing condensed matter is particularly obsessed with is the fascinating phenomena of [phase transition](statistical-physics.md#phase-transition).

<a id="image-xkcd-2933-elementary-physics-paths"></a>
![](https://web.archive.org/web/20241202062559im_/https://imgs.xkcd.com/comics/elementary_physics_paths.png)

**[Figure 1](#image-xkcd-2933-elementary-physics-paths). xkcd 2933: Elementary Physics Paths**.

<a id="video-what-is-condensed-matter-physics-by-erica-calman"></a>
**[Video 1](#video-what-is-condensed-matter-physics-by-erica-calman). What Is Condensed matter physics? by Erica Calman.** [Source](https://www.youtube.com/watch?v=CY5V0q3K0zc). Cute. Overview of the main fields of physics research. Quick mention of his field, [quantum wells](quantum-mechanics.md#quantum-well), but not enough details.

**Table of contents**

- [Atomic, Molecular and Optical Physics](#atomic-molecular-and-optical-physics)
  - [Molecular beam](#molecular-beam)
- [Solid-state physics](#solid-state-physics)
  - [Crystallography](#crystallography)
    - [Crystal system](#crystal-system)
    - [Point group](#point-group)
      - [Point groups in two dimensions](#point-groups-in-two-dimensions)
      - [Point groups in three dimensions](#point-groups-in-three-dimensions)
      - [Crystallographic restriction theorem](#crystallographic-restriction-theorem)
    - [Bravais lattice](#bravais-lattice)
    - [Crystal](#crystal)
  - [Topological insulator](#topological-insulator)
    - [Topology in condensed matter](#topology-in-condensed-matter)
- [Electronic band theory](#electronic-band-theory)
  - [Direct and indirect band gaps](#direct-and-indirect-band-gaps)
- [Electrical resistivity and conductivity](#electrical-resistivity-and-conductivity)
  - [Electrical reactance](#electrical-reactance)
    - [Electrical impedance](#electrical-impedance)
  - [Four-terminal sensing](#four-terminal-sensing)
  - [Dependence of electrical resistivity on tempreature](#dependence-of-electrical-resistivity-on-tempreature)
    - [Kondo effect](#kondo-effect)
  - [Semiconductor](#semiconductor)
    - [Doping (semiconductor)](#doping-semiconductor)
    - [Type of semiconductor](#type-of-semiconductor)
      - [III-V semiconductor](#iii-v-semiconductor)
  - [Superconductivity](#superconductivity)
    - [Superconductor resistivity experiment video](#superconductor-resistivity-experiment-video)
    - [Superconductor coil experiment video](#superconductor-coil-experiment-video)
    - [Superconductivity is a a form of superfluidity](#superconductivity-is-a-a-form-of-superfluidity)
    - [Cooper pair](#cooper-pair)
    - [Superconducting temperature](#superconducting-temperature)
    - [Superconducting phase diagram](#superconducting-phase-diagram)
    - [Type of superconductor](#type-of-superconductor)
      - [Type-I superconductor](#type-i-superconductor)
      - [Type-II superconductor](#type-ii-superconductor)
      - [High-temperature superconductivity](#high-temperature-superconductivity)
        - [Room temperature superconductor](#room-temperature-superconductor)
          - [Resonating valence bond theory](#resonating-valence-bond-theory)
          - [Room temperature and pressure superconductor](#room-temperature-and-pressure-superconductor)
            - [LK-99](#lk-99)
        - [List of High-temperature superconductors](#list-of-high-temperature-superconductors)
          - [Yttrium barium copper oxide](#yttrium-barium-copper-oxide)
          - [Bismuth strontium calcium copper oxide](#bismuth-strontium-calcium-copper-oxide)
    - [Superconducting material](#superconducting-material)
    - [Applications of superconductivity](#applications-of-superconductivity)
      - [Most important superconductor material](#most-important-superconductor-material)
    - [Superconductor I-V curve](#superconductor-i-v-curve)
      - [Do superconductors carry infinite current?](#do-superconductors-carry-infinite-current)
    - [BCS Theory](#bcs-theory)
    - [Josephson effect](#josephson-effect)
      - [History of the Josephson effect](#history-of-the-josephson-effect)
        - [Possible new effects in superconductive tunnelling](#possible-new-effects-in-superconductive-tunnelling)
        - [Probable observation of the Josephson superconducting tunneling effect](#probable-observation-of-the-josephson-superconducting-tunneling-effect)
      - [Josephson effect regime](#josephson-effect-regime)
        - [DC Josephson effect](#dc-josephson-effect)
        - [AC Josephson effect](#ac-josephson-effect)
        - [Inverse AC Josephson effect](#inverse-ac-josephson-effect)
          - [Shapiro steps](#shapiro-steps)
      - [Josephson equations](#josephson-equations)
        - [Josephson current](#josephson-current)
        - [Josephson phase](#josephson-phase)
      - [Josephson junction](#josephson-junction)
        - [Pi Josephson junction](#pi-josephson-junction)
      - [Magnetic flux quantum](#magnetic-flux-quantum)
        - [Experimental Evidence for Quantized Flux in Superconducting Cylinders](#experimental-evidence-for-quantized-flux-in-superconducting-cylinders)
        - [Josephson constant](#josephson-constant)
      - [Symmetry breaking in superconductors](#symmetry-breaking-in-superconductors)
      - [Applications of Josephson Junctions](#applications-of-josephson-junctions)
        - [Josephson voltage standard](#josephson-voltage-standard)
        - [SQUID device](#squid-device)
          - [DC SQUID](#dc-squid)
- [Superconducting tunnel junction](#superconducting-tunnel-junction)
- [Superfluidity](#superfluidity)
- [State of matter](#state-of-matter)
  - [High pressure](#high-pressure)
- [List of states of matter](#list-of-states-of-matter)
  - [Solid](#solid)
  - [Liquid](#liquid)
  - [Gas](#gas)
    - [Fermi gas](#fermi-gas)
      - [Electron gas](#electron-gas)
        - [Two-dimensional electron gas](#two-dimensional-electron-gas)
          - [Laughlin wavefunction](#laughlin-wavefunction)
      - [1D Fermi gas](#1d-fermi-gas)
        - [Impenetrable Bose Gas](#impenetrable-bose-gas)
  - [Bose-Einstein condensate](#bose-einstein-condensate)
- [Materials science](#materials-science)
  - [Type of material](#type-of-material)
    - [Glass](#glass)
    - [Quantum dot](#quantum-dot)
      - [Quantum dot single photon source](#quantum-dot-single-photon-source)
    - [Metal](#metal)
      - [Field electron emission](#field-electron-emission)
      - [Alloy](#alloy)
        - [Binary alloy](#binary-alloy)
      - [Metallurgy](#metallurgy)
        - [Ingot](#ingot)
    - [Polymer](#polymer)
      - [Plastic](#plastic)
  - [Material property](#material-property)
    - [Material property database](#material-property-database)
      - [Open material property database](#open-material-property-database)
        - [The Materials Project](#the-materials-project)
    - [Density](#density)
    - [Magnet](#magnet)
      - [Permanent magnet](#permanent-magnet)
        - [Curie temperature](#curie-temperature)
        - [Ferromagnetism](#ferromagnetism)
          - [Magnetic hysteresis](#magnetic-hysteresis)
            - [Saturation magnetisation](#saturation-magnetisation)
      - [Electromagnet](#electromagnet)
        - [Electromagnetic coil](#electromagnetic-coil)
        - [Solenoid](#solenoid)
        - [Lifting electromagnet](#lifting-electromagnet)
          - [Breaking Bad magnet scene](#breaking-bad-magnet-scene)
      - [Ising model](#ising-model)
        - [Solution of the Ising model](#solution-of-the-ising-model)
        - [1D Ising model](#1d-ising-model)
        - [2D Ising model](#2d-ising-model)
        - [3D Ising model](#3d-ising-model)
      - [Magnetic dipole](#magnetic-dipole)
        - [Magnetic dipole moment](#magnetic-dipole-moment)
        - [Interaction between a magnetic dipole and a magnetic field](#interaction-between-a-magnetic-dipole-and-a-magnetic-field)
          - [Interaction between a magnetic dipole and a homogenous magnetic field](#interaction-between-a-magnetic-dipole-and-a-homogenous-magnetic-field)
          - [Magnetic dipole in an inhomogenous magnetic field](#magnetic-dipole-in-an-inhomogenous-magnetic-field)
      - [Compass](#compass)
        - [Water compass](#water-compass)
      - [Superconducting magnet](#superconducting-magnet)
        - [Superconducting magnet vendor](#superconducting-magnet-vendor)
          - [Oxford Instruments](#oxford-instruments)
        - [High temperature superconductor superconducting magnet](#high-temperature-superconductor-superconducting-magnet)
    - [Optical material property](#optical-material-property)
      - [Black-body radiation](#black-body-radiation)
        - [Planck's law](#planck-s-law)
          - [Wien approximation](#wien-approximation)
          - [Rayleigh-Jeans law](#rayleigh-jeans-law)
        - [Black-body radiation experiment](#black-body-radiation-experiment)
        - [Ultraviolet catastrophe](#ultraviolet-catastrophe)
      - [Transparency (electromagnetic radiation)](#transparency-electromagnetic-radiation)
        - [Absorption (electromagnetic radiation)](#absorption-electromagnetic-radiation)
    - [Piezoelectricity](#piezoelectricity)
      - [Piezoelectric actuator](#piezoelectric-actuator)
        - [Piezoelectric motor](#piezoelectric-motor)
      - [Piezo ignition](#piezo-ignition)
    - [Photoluminescence](#photoluminescence)
      - [Fluorescence](#fluorescence)
        - [Fluorometer](#fluorometer)
        - [Phosphorescence](#phosphorescence)
    - [Specific heat capacity](#specific-heat-capacity)
      - [Einstein solid](#einstein-solid)
        - [Dulong-Petit law](#dulong-petit-law)
      - [Debye model](#debye-model)
    - [Viscosity](#viscosity)
      - [Pitch drop experiment](#pitch-drop-experiment)
- [Laser](#laser)
  - [History of the laser](#history-of-the-laser)
    - [The History of the Laser by Mario Bertolotti](#the-history-of-the-laser-by-mario-bertolotti)
  - [Laser spectrum](#laser-spectrum)
    - [Laser linewidth](#laser-linewidth)
    - [Laser gain curve](#laser-gain-curve)
  - [Lasers vs other light sources](#lasers-vs-other-light-sources)
    - [Lasers emit a narrow spectrum](#lasers-emit-a-narrow-spectrum)
      - [Laser spectrum vs LED spectrum](#laser-spectrum-vs-led-spectrum)
    - [Why can't you collimate incoherent light as well as a laser?](#why-can-t-you-collimate-incoherent-light-as-well-as-a-laser)
  - [Type of laser](#type-of-laser)
    - [Maser](#maser)
    - [Fiber laser](#fiber-laser)
    - [Gas laser](#gas-laser)
    - [Laser diode](#laser-diode)
      - [Laser pointer](#laser-pointer)
    - [Three-level laser](#three-level-laser)
    - [Four-level laser](#four-level-laser)
  - [Are lasers polarized](#are-lasers-polarized)
  - [Optical tweezers](#optical-tweezers)
    - [Laser cooling](#laser-cooling)
  - [Population inversion](#population-inversion)
  - [Pulsed laser](#pulsed-laser)
  - [Laser vendor](#laser-vendor)
    - [Coherent, Inc.](#coherent-inc)
- [Quasiparticle](#quasiparticle)
  - [Quasiparticles vs elementary particles](#quasiparticles-vs-elementary-particles)
- [History of condensed matter physics](#history-of-condensed-matter-physics)
- [Condensed matter Physics bibliography](#condensed-matter-physics-bibliography)
  - [Condensed matter university course](#condensed-matter-university-course)
    - [Theories of Quantum Matter by Austen Lamacraft](theories-of-quantum-matter-by-austen-lamacraft.md)
      - [Many Body Wavefunctions](theories-of-quantum-matter-by-austen-lamacraft.md#many-body-wavefunctions)
        - [Bosons and Fermions](theories-of-quantum-matter-by-austen-lamacraft.md#many-body-wavefunctions/bosons-and-fermions)
          - [Two Particles](theories-of-quantum-matter-by-austen-lamacraft.md#many-body-wavefunctions/two-particles)
          - [Product States](theories-of-quantum-matter-by-austen-lamacraft.md#many-body-wavefunctions/product-states)
        - [The 1D Fermi Gas](theories-of-quantum-matter-by-austen-lamacraft.md#many-body-wavefunctions/the-1d-fermi-gas)
          - [Ground State](theories-of-quantum-matter-by-austen-lamacraft.md#many-body-wavefunctions/1d-fermi-gas-ground-state)
          - [Density; Density Matrix; Pair Distribution](theories-of-quantum-matter-by-austen-lamacraft.md#many-body-wavefunctions/1d-fermi-gas-density)
          - [Impenetrable Bose Gas](theories-of-quantum-matter-by-austen-lamacraft.md#many-body-wavefunctions/impenetrable-bose-gas)
      - [Quantum Hall Effect](theories-of-quantum-matter-by-austen-lamacraft.md#quantum-hall-effect)
        - [Fractional Quantum Hall Effect](theories-of-quantum-matter-by-austen-lamacraft.md#quantum-hall-effect/fractional-quantum-hall-effect)
          - [Landau Levels](theories-of-quantum-matter-by-austen-lamacraft.md#quantum-hall-effect/landau-levels)
            - [Lowest Landau level](theories-of-quantum-matter-by-austen-lamacraft.md#quantum-hall-effect/lowest-landau-level)
              - [Filled LLL of Fermions](theories-of-quantum-matter-by-austen-lamacraft.md#quantum-hall-effect/filled-lll-of-fermions)
          - [The Laughlin Wavefunction](theories-of-quantum-matter-by-austen-lamacraft.md#quantum-hall-effect/the-laughlin-wavefunction)
          - [The Plasma Analogy](theories-of-quantum-matter-by-austen-lamacraft.md#quantum-hall-effect/the-plasma-analogy)
          - [Fractional Charge](theories-of-quantum-matter-by-austen-lamacraft.md#quantum-hall-effect/fractional-charge)
          - [Fractional Statistics](theories-of-quantum-matter-by-austen-lamacraft.md#quantum-hall-effect/fractional-statistics)
        - [Appendix](theories-of-quantum-matter-by-austen-lamacraft.md#quantum-hall-effect/quantum-hall-effect-appendix)
          - [Sampling from a complex wavefunction](theories-of-quantum-matter-by-austen-lamacraft.md#quantum-hall-effect/sampling-from-a-complex-wavefunction)
      - [The Elastic Chain](theories-of-quantum-matter-by-austen-lamacraft.md#the-elastic-chain)
        - [The Classical System](theories-of-quantum-matter-by-austen-lamacraft.md#the-elastic-chain/the-classical-system)
          - [Equations of Motion](theories-of-quantum-matter-by-austen-lamacraft.md#the-elastic-chain/equations-of-motion)
          - [Hamiltonian Formulation](theories-of-quantum-matter-by-austen-lamacraft.md#the-elastic-chain/hamiltonian-formulation)
          - [Complex Coordinates](theories-of-quantum-matter-by-austen-lamacraft.md#the-elastic-chain/complex-coordinates)
        - [Quantum Oscillators](theories-of-quantum-matter-by-austen-lamacraft.md#the-elastic-chain/quantum-oscillators)
          - [The Quantum Chain](theories-of-quantum-matter-by-austen-lamacraft.md#the-elastic-chain/the-quantum-chain)
          - [Oscillator Quanta are Bosons!](theories-of-quantum-matter-by-austen-lamacraft.md#the-elastic-chain/oscillator-quanta-are-bosons)
          - [Thermodynamic ($N \to \infty$) limit](theories-of-quantum-matter-by-austen-lamacraft.md#the-elastic-chain/thermodynamic-n-to-infty-limit)
          - [Finite Temperature](theories-of-quantum-matter-by-austen-lamacraft.md#the-elastic-chain/finite-temperature)
          - [Position Fluctuations](theories-of-quantum-matter-by-austen-lamacraft.md#the-elastic-chain/position-fluctuations)
          - [Density Fluctuations](theories-of-quantum-matter-by-austen-lamacraft.md#the-elastic-chain/density-fluctuations)
        - [Appendix](theories-of-quantum-matter-by-austen-lamacraft.md#the-elastic-chain/appendix)
          - [Fourier review](theories-of-quantum-matter-by-austen-lamacraft.md#the-elastic-chain/fourier-review)
          - [Discrete Fourier Transform](theories-of-quantum-matter-by-austen-lamacraft.md#the-elastic-chain/discrete-fourier-transform)
          - [Properties of the Fourier Transform](theories-of-quantum-matter-by-austen-lamacraft.md#the-elastic-chain/properties-of-the-fourier-transform)
          - [Higher dimensions](theories-of-quantum-matter-by-austen-lamacraft.md#the-elastic-chain/higher-dimensions)
          - [Evaluating (56)](theories-of-quantum-matter-by-austen-lamacraft.md#the-elastic-chain/evaluating-56)
    - [Course: Quantum Many-Body Physics in Condensed Matter by Luis Gregorio Dias (2020)](#course-quantum-many-body-physics-in-condensed-matter-by-luis-gregorio-dias-2020)

## Atomic, Molecular and Optical Physics

↑ **Parent:** [Condensed matter physics](condensed-matter-physics.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Atomic,_Molecular_and_Optical_Physics)

AMO is a slightly more general area than [condensed matter physics](condensed-matter-physics.md), including related phenomena with smaller numbers atoms and optics. The two terms are however sometimes used as synonyms. The term AMO has gained wide usage and acceptability, see e.g.:
- [https://www.sussex.ac.uk/amo/](https://www.sussex.ac.uk/amo/) at [University of Sussex](university.md#university-of-sussex)

If Ciro had had greater foresight, [this might have been what he studied at university](university.md#when-in-doubt-choose-the-course-that-has-the-most-experimental-work)!

### Molecular beam

↑ **Parent:** [Atomic, Molecular and Optical Physics](#atomic-molecular-and-optical-physics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Molecular_beam)

[Molecular beams](#molecular-beam) are cool because they create a one dimensional flow of [molecules](quantum-mechanics.md#molecule), which makes it easier to observe certain single-molecule effects, as it removes the multi-particle issues from experiments.

Key [molecular beam](#molecular-beam) experiments include:
- [Stern-Gerlach experiment](relativistic-quantum-mechanics.md#stern-gerlach-experiment), which confirmed the existence of [spin](relativistic-quantum-mechanics.md#spin-physics)
- [Rabi's NMR experiment](particle-physics.md#rabi-s-nmr-experiment), which confirmed the existence of [nuclear spin](particle-physics.md#nuclear-magnetic-moment)

The center piece of the control system of [atomic clocks](system-of-units.md#atomic-clock) is a [molecular beam](#molecular-beam).

## Solid-state physics

↑ **Parent:** [Condensed matter physics](condensed-matter-physics.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Solid-state_physics)

### Crystallography

↑ **Parent:** [Solid-state physics](#solid-state-physics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Crystallography)

#### Crystal system

↑ **Parent:** [Crystallography](#crystallography)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Crystal_system)

#### Point group

↑ **Parent:** [Crystallography](#crystallography)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Point_group)

##### Point groups in two dimensions

↑ **Parent:** [Point group](#point-group)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Point_groups_in_two_dimensions)

##### Point groups in three dimensions

↑ **Parent:** [Point group](#point-group)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Point_groups_in_three_dimensions)

##### Crystallographic restriction theorem

↑ **Parent:** [Point group](#point-group)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Crystallographic_restriction_theorem)

#### Bravais lattice

↑ **Parent:** [Crystallography](#crystallography)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Bravais_lattice)

#### Crystal

↑ **Parent:** [Crystallography](#crystallography)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Crystal)

### Topological insulator

↑ **Parent:** [Solid-state physics](#solid-state-physics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Topological_insulator)

Bibliography:

#### Topology in condensed matter

↑ **Parent:** [Topological insulator](#topological-insulator)  
🏷️ **Tags:** [GitHub book repo](software.md#github-book-repo)

[https://topocondmat.org/](https://topocondmat.org/)

Previously on [EdX](website.md#edx): [https://www.edx.org/learn/quantum-physics-mechanics/delft-university-of-technology-topology-in-condensed-matter-tying-quantum-knots](https://www.edx.org/learn/quantum-physics-mechanics/delft-university-of-technology-topology-in-condensed-matter-tying-quantum-knots) "DelftX: Topology in Condensed Matter: Tying Quantum Knots".

But then they regained their sanity and put the source code on [GitHub](software.md#github): [https://github.com/topocm/topocm_content](https://github.com/topocm/topocm_content) and is [CC BY-SA](law.md#cc-by-sa).

Uses an ungodly combination of [Jupyter](programming-language.md#jupyter-notebook) notebooks and [Pelican](website.md#pelican-static-site-generator).

## Electronic band theory

↑ **Parent:** [Condensed matter physics](condensed-matter-physics.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Electronic_band_theory)

How are the bands measured experimentally?

Why are there gaps? Why aren't bands infinite? What determines the width of gaps?

Bibliography:
- [Applications of Quantum Mechanics by David Tong (2017)](quantum-mechanics.md#applications-of-quantum-mechanics-by-david-tong-2017) Chapter 2 "Band Structure"

### Direct and indirect band gaps

↑ **Parent:** [Electronic band theory](#electronic-band-theory)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Direct_and_indirect_band_gaps)

## Electrical resistivity and conductivity

↑ **Parent:** [Condensed matter physics](condensed-matter-physics.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Electrical_resistivity_and_conductivity)

### Electrical reactance

↑ **Parent:** [Electrical resistivity and conductivity](#electrical-resistivity-and-conductivity)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Electrical_reactance)

#### Electrical impedance

↑ **Parent:** [Electrical reactance](#electrical-reactance)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Electrical_impedance)

[Ciro Santilli](ciro-santilli.md) distinctly remembers being taught that at basic [electrical engineering](electronics.md#electrical-engineer) school during [Ciro Santilli's undergrad studies at the University of São Paulo](ciro-santilli.md#ciro-santilli-s-undergrad-studies-at-the-university-of-sao-paulo).

It really allows you to do [alternating current](electronics.md#alternating-current) calculations much as you'd do DC calculations with resistors, quite poweful. It must have been all the rage in the 1950s.

### Four-terminal sensing

↑ **Parent:** [Electrical resistivity and conductivity](#electrical-resistivity-and-conductivity)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Four-terminal_sensing)

### Dependence of electrical resistivity on tempreature

↑ **Parent:** [Electrical resistivity and conductivity](#electrical-resistivity-and-conductivity)

#### Kondo effect

↑ **Parent:** [Dependence of electrical resistivity on tempreature](#dependence-of-electrical-resistivity-on-tempreature)

If you adda bit of impurities to certain materials, at low temperatures of a few [Kelvin](statistical-physics.md#kelvin) their [resistivity](#electrical-resistivity-and-conductivity) actually starts increasing if you go below a certain critical temperature.

<a id="image-kondo-effect-graph-for-gold-with-added-impurities"></a>
![](https://upload.wikimedia.org/wikipedia/commons/4/4a/Classickondo.png)

**[Figure 2](#image-kondo-effect-graph-for-gold-with-added-impurities). Kondo effect graph for gold with added impurities**. [Source](https://commons.wikimedia.org/wiki/File:Classickondo.png).

### Semiconductor

↑ **Parent:** [Electrical resistivity and conductivity](#electrical-resistivity-and-conductivity)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Semiconductor)

The basis of 1970-20XX [computers](computer.md), gotta understand them I guess?

#### Doping (semiconductor)

↑ **Parent:** [Semiconductor](#semiconductor)

#### Type of semiconductor

↑ **Parent:** [Semiconductor](#semiconductor)

##### III-V semiconductor

↑ **Parent:** [Type of semiconductor](#type-of-semiconductor)

Most notable example: [gallium arsenide](chemistry.md#gallium-arsenide), see also: [gallium arsenide vs silicon](chemistry.md#gallium-arsenide-vs-silicon).

An important class of [semiconductors](#semiconductor), e.g. there is a dedicated III-V lab at: [École Polytechnique](ecole-polytechnique.md): [http://www.3-5lab.fr/contactus.php](http://www.3-5lab.fr/contactus.php)

### Superconductivity

↑ **Parent:** [Electrical resistivity and conductivity](#electrical-resistivity-and-conductivity)  
🏷️ **Tags:** [Second-order phase transition](statistical-physics.md#second-order-phase-transition)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Superconductivity)

Experiments:
- "An introduction to superconductivity" by Alfred Leitner originally published in 1965, source: [http://www.alfredleitner.com/](http://www.alfredleitner.com/)
- Isotope effect on the critical temperature. [http://hyperphysics.phy-astr.gsu.edu/hbase/Solids/coop.html](http://hyperphysics.phy-astr.gsu.edu/hbase/Solids/coop.html) mentions that:

  > If electrical conduction in mercury were purely electronic, there should be no dependence upon the nuclear masses. This dependence of the critical temperature for superconductivity upon isotopic mass was the first direct evidence for interaction between the electrons and the lattice. This supported the [BCS Theory](#bcs-theory) of lattice coupling of electron pairs.

<a id="video-20-fermi-gases-bec-bcs-crossover-by-wolfgang-ketterle-2014"></a>
**[Video 2](#video-20-fermi-gases-bec-bcs-crossover-by-wolfgang-ketterle-2014). 20. Fermi gases, BEC-BCS crossover by Wolfgang Ketterle (2014)** [Source](http://youtube.com/watch?v=O_zjGYvP4Ps). Part of the "Atomic and Optical Physics" series, uploaded by [MIT OpenCourseWare](university.md#mit-opencourseware).

Actually goes into the equations.

Notably, [https://youtu.be/O_zjGYvP4Ps?t=3278](https://youtu.be/O_zjGYvP4Ps?t=3278) describes extremely briefly an experimental setup that more directly observes pair condensation.

<a id="video-superconductivity-and-quantum-mechanics-at-the-macro-scale-1-of-2-by-steven-kivelson-2016"></a>
**[Video 3](#video-superconductivity-and-quantum-mechanics-at-the-macro-scale-1-of-2-by-steven-kivelson-2016). Superconductivity and Quantum Mechanics at the Macro-Scale - 1 of 2 by Steven Kivelson (2016)** [Source](http://youtube.com/watch?v=Yx666k2XH8E). For the Stanford Institute for Theoretical Physics. Gives a reasonable basis overview, but does not go into the meat of BCS it at the end.

<a id="video-the-map-of-superconductivity-by-domain-of-science"></a>
**[Video 4](#video-the-map-of-superconductivity-by-domain-of-science). The Map of Superconductivity by Domain of Science.** [Source](https://www.youtube.com/watch?v=bD2M7P6dTVA). Lacking as usual, but this one is particularly good as the author used to work on the area as he mentions in the video.

Lecture notes:
- [https://austen.uk/courses/tqm/superconductivity/](https://austen.uk/courses/tqm/superconductivity/)

Media:
- [http://www.supraconductivite.fr/en/index.php#supra-explication](http://www.supraconductivite.fr/en/index.php#supra-explication)

  Cool CNRS video showing the condensed wave function, and mentioning that "every pair moves at the same speed". To change the speed of one pair, you need to change the speed of all others. That's why there's not energy loss.

Transition into superconductivity can be seen as a [phase transition](statistical-physics.md#phase-transition), which happens to be a [second-order phase transition](statistical-physics.md#second-order-phase-transition).

#### Superconductor resistivity experiment video

↑ **Parent:** [Superconductivity](#superconductivity)

[https://andor.oxinst.com/learning/view/article/measuring-resistance-of-a-superconducting-sample-with-a-dry-cryostat](https://andor.oxinst.com/learning/view/article/measuring-resistance-of-a-superconducting-sample-with-a-dry-cryostat) Not a video, but well done, by [Oxford Instruments](#oxford-instruments).

<a id="video-superconductor-4-probe-measurement-by-frederiksen-scientific-a-s-2015"></a>
**[Video 5](#video-superconductor-4-probe-measurement-by-frederiksen-scientific-a-s-2015). Superconductor, 4-probe measurement by Frederiksen Scientific A/S (2015)** [Source](https://www.youtube.com/watch?v=8gMKuy-gDQc). OK experiment, illustrates the educational kit they sell. No temperature control, just dumps [liquid nitrogen](chemistry.md#liquid-nitrogen) into conductor and watches it drop. But not too bad either. The kit sale link is broken (obviously, enterprise stuff), but there are no archives unfortunately. But it must be some [High-temperature superconductor](#high-temperature-superconductivity)

#### Superconductor coil experiment video

↑ **Parent:** [Superconductivity](#superconductivity)  
🏷️ **Tags:** [Videos of all key physics experiments](todo.md#videos-of-all-key-physics-experiments)

TODO!!! Even this is hard to find! A clean and minimal one! Why! All we can find are shittly levitating [YBCO](#yttrium-barium-copper-oxide) samples in [liquid nitrogen](chemistry.md#liquid-nitrogen)! Maybe because [liquid helium](chemistry.md#liquid-helium) is expensive?

[https://physics.stackexchange.com/questions/69222/how-can-i-put-a-permanent-current-into-a-superconducting-loop](https://physics.stackexchange.com/questions/69222/how-can-i-put-a-permanent-current-into-a-superconducting-loop)

<a id="video-first-10t-tape-coil-by-mark-benz"></a>
**[Video 6](#video-first-10t-tape-coil-by-mark-benz). First 10T Tape Coil by Mark Benz.** [Source](https://www.youtube.com/watch?v=ba9zUW2Xf8Y). Dr. Mark Benz describes the first commercially sold superconducting magnet made by him and colleagues in 1965. The 10 Tesla magnet was made at GE Schenectady and they sold magnets to research facilities world wide before the team formed Intermagnetics General.  IGC and Carl Rosner went on to pioneer MRI technology.

#### Superconductivity is a a form of superfluidity

↑ **Parent:** [Superconductivity](#superconductivity)

We know that [superfluidity](#superfluidity) happens more easily in [bosons](relativistic-quantum-mechanics.md#boson), and so electrons joins in [Cooper pairs](#cooper-pair) to form [bosons](relativistic-quantum-mechanics.md#boson), making a superfluid of [Cooper pairs](#cooper-pair)!

Isn't that awesome!

#### Cooper pair

↑ **Parent:** [Superconductivity](#superconductivity)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Cooper_pair)

#### Superconducting temperature

↑ **Parent:** [Superconductivity](#superconductivity)

#### Superconducting phase diagram

↑ **Parent:** [Superconductivity](#superconductivity)  
🏷️ **Tags:** [Phase transition](statistical-physics.md#phase-transition)

There are various possibilities for the axes, but some common ones:
- temperature (T) vs magnetic field strength (B)
- temperature (T) vs proportion of each [chemical element](chemistry.md#chemical-element) of a [binary alloy](#binary-alloy)
- temperature (T) vs pressure

<a id="image-sketch-of-the-typical-superconducting-phase-diagram-of-a-type-i-superconductor-superconducting-phase-diagram"></a>
![](https://upload.wikimedia.org/wikipedia/commons/5/51/Phase_diagram_superconductor_type_I.svg)

**[Figure 3](#image-sketch-of-the-typical-superconducting-phase-diagram-of-a-type-i-superconductor-superconducting-phase-diagram). Sketch of the typical superconducting phase diagram of a Type-I superconductor**. [Source](https://commons.wikimedia.org/wiki/File:Phase_diagram_superconductor_type_I.svg).

<a id="image-sketch-of-the-typical-superconducting-phase-diagram-of-a-type-ii-superconductor-superconducting-phase-diagram"></a>
![](https://upload.wikimedia.org/wikipedia/commons/thumb/6/6c/Superconductor_interactions_with_magnetic_field.png/500px-Superconductor_interactions_with_magnetic_field.png)

**[Figure 4](#image-sketch-of-the-typical-superconducting-phase-diagram-of-a-type-ii-superconductor-superconducting-phase-diagram). Sketch of the typical superconducting phase diagram of a Type-II superconductor**. [Source](https://commons.wikimedia.org/wiki/File:Superconductor_interactions_with_magnetic_field.png).

#### Type of superconductor

↑ **Parent:** [Superconductivity](#superconductivity)

##### Type-I superconductor

↑ **Parent:** [Type of superconductor](#type-of-superconductor)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Type-I_superconductor)

<a id="image-sketch-of-the-typical-superconducting-phase-diagram-of-a-type-i-superconductor"></a>
![](https://upload.wikimedia.org/wikipedia/commons/5/51/Phase_diagram_superconductor_type_I.svg)

**[Figure 5](#image-sketch-of-the-typical-superconducting-phase-diagram-of-a-type-i-superconductor). Sketch of the typical superconducting phase diagram of a Type-I superconductor**. [Source](https://commons.wikimedia.org/wiki/File:Phase_diagram_superconductor_type_I.svg).

##### Type-II superconductor

↑ **Parent:** [Type of superconductor](#type-of-superconductor)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Type-II_superconductor)

<a id="image-sketch-of-the-typical-superconducting-phase-diagram-of-a-type-ii-superconductor"></a>
![](https://upload.wikimedia.org/wikipedia/commons/thumb/6/6c/Superconductor_interactions_with_magnetic_field.png/500px-Superconductor_interactions_with_magnetic_field.png)

**[Figure 6](#image-sketch-of-the-typical-superconducting-phase-diagram-of-a-type-ii-superconductor). Sketch of the typical superconducting phase diagram of a Type-II superconductor**. [Source](https://commons.wikimedia.org/wiki/File:Superconductor_interactions_with_magnetic_field.png).

##### High-temperature superconductivity

↑ **Parent:** [Type of superconductor](#type-of-superconductor)  
🏷️ **Tags:** [1987 Nobel Prize in Physics](nobel-prize.md#1987-nobel-prize-in-physics), [Unsolved physics problem](physics.md#unsolved-physics-problem)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/High-temperature_superconductivity)

As of 2020, basically means "[liquid nitrogen](chemistry.md#liquid-nitrogen) temperature", which is much cheaper than [liquid helium](chemistry.md#liquid-helium).

The dream of course being [room temperature and pressure superconductor](#room-temperature-and-pressure-superconductor).

<a id="image-timeline-of-superconductivity-from-1900-to-2015"></a>
<img src="https://upload.wikimedia.org/wikipedia/commons/b/bb/Timeline_of_Superconductivity_from_1900_to_2015.svg" alt="" height="600">

**[Figure 7](#image-timeline-of-superconductivity-from-1900-to-2015). Timeline of superconductivity from 1900 to 2015**. [Source](https://commons.wikimedia.org/wiki/File:Timeline_of_Superconductivity_from_1900_to_2015.svg).

###### Room temperature superconductor

↑ **Parent:** [High-temperature superconductivity](#high-temperature-superconductivity)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Room_temperature_superconductor)

###### Resonating valence bond theory

↑ **Parent:** [Room temperature superconductor](#room-temperature-superconductor)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Resonating_valence_bond_theory)

###### Room temperature and pressure superconductor

↑ **Parent:** [Room temperature superconductor](#room-temperature-superconductor)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Room_temperature_and_pressure_superconductor)

LK-99:
- [https://www.tomshardware.com/news/superconductor-breakthrough-replicated-twice](https://www.tomshardware.com/news/superconductor-breakthrough-replicated-twice)

###### LK-99

↑ **Parent:** [Room temperature and pressure superconductor](#room-temperature-and-pressure-superconductor)

###### List of High-temperature superconductors

↑ **Parent:** [High-temperature superconductivity](#high-temperature-superconductivity)  
🏷️ **Tags:** [Superconducting material](#superconducting-material)

###### Yttrium barium copper oxide

↑ **Parent:** [List of High-temperature superconductors](#list-of-high-temperature-superconductors)  
🏷️ **Tags:** [Barium compound](chemistry.md#barium-compound), [Copper compound](chemistry.md#copper-compound)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Yttrium_barium_copper_oxide)

Upside: superconducting above 92K, which is above the 77K of [liquid nitrogen](chemistry.md#liquid-nitrogen), and therefore much much cheaper to obtain and maintain than liquid helium.

Downside: it is brittle, so how do you make wires out of it? Still, can already be used in certain circuits, e.g. high temperature [SQUID devices](#squid-device).

###### Bismuth strontium calcium copper oxide

↑ **Parent:** [List of High-temperature superconductors](#list-of-high-temperature-superconductors)  
🏷️ **Tags:** [Bismuth compound](chemistry.md#bismuth-compound), [Copper compound](chemistry.md#copper-compound)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Bismuth_strontium_calcium_copper_oxide)

Discovered in 1988, the first [high-temperature superconductor](#high-temperature-superconductivity) which did not contain a rare-earth element.

#### Superconducting material

↑ **Parent:** [Superconductivity](#superconductivity)

#### Applications of superconductivity

↑ **Parent:** [Superconductivity](#superconductivity)

Superconductivity is one of the key advances of 21st century technology:
- produce powerful magnetic fields with [superconducting magnets](#superconducting-magnet)
- the [Josephson effect](#josephson-effect), applications listed at: [Section "Applications of Josephson Junctions"](#applications-of-josephson-junctions)

Bibliography:
- [https://en.wikipedia.org/wiki/Technological_applications_of_superconductivity](https://en.wikipedia.org/wiki/Technological_applications_of_superconductivity)

##### Most important superconductor material

↑ **Parent:** [Applications of superconductivity](#applications-of-superconductivity)

As of 2023 the most important ones economicaly were:
- [Nb-Ti](chemistry.md#niobium-titanium): the most widely used one. Used e.g. to create the [magnetic fields](electromagnetism.md#magnetic-field) of the [Large Hadron Collider](particle-physics.md#large-hadron-collider) Up to 15 [T](electromagnetism.md#tesla-unit).
- [Nb-Sn](chemistry.md#niobium-tin): more expensive than [Nb-Ti](chemistry.md#niobium-titanium), but can reach up to 30 [T](electromagnetism.md#tesla-unit).
The main application is [magnetic resonance imaging](particle-physics.md#magnetic-resonance-imaging). Both of these are have to be [Liquid helium](chemistry.md#liquid-helium), i.e. they are not "[high-temperature superconductor](#high-temperature-superconductivity)" which is a pain. One big strength they have is that they are [metallic](#metal), and therefore can made into wires, which is crucial to be able to make [electromagnetic coils](#electromagnetic-coil) out of them.

#### Superconductor I-V curve

↑ **Parent:** [Superconductivity](#superconductivity)

TODO, come on, [Internet](computer.md#internet)!

Bibliography.

##### Do superconductors carry infinite current?

↑ **Parent:** [Superconductor I-V curve](#superconductor-i-v-curve)

No, see: [superconductor I-V curve](#superconductor-i-v-curve).

Bibliography:
- [https://physics.stackexchange.com/questions/62664/how-can-ohms-law-be-correct-if-superconductors-have-0-resistivity](https://physics.stackexchange.com/questions/62664/how-can-ohms-law-be-correct-if-superconductors-have-0-resistivity) on [Physics Stack Exchange](stack-overflow.md#physics-stack-exchange)
- [https://physics.stackexchange.com/questions/69222/how-can-i-put-a-permanent-current-into-a-superconducting-loop](https://physics.stackexchange.com/questions/69222/how-can-i-put-a-permanent-current-into-a-superconducting-loop)
- [https://www.quora.com/Do-superconductors-produce-infinite-current-I-V-R-R-0-How-do-they-fit-into-quantum-theory](https://www.quora.com/Do-superconductors-produce-infinite-current-I-V-R-R-0-How-do-they-fit-into-quantum-theory)
- [https://www.reddit.com/r/askscience/comments/dcgdf/does_superconductivity_imply_infinite_current/](https://www.reddit.com/r/askscience/comments/dcgdf/does_superconductivity_imply_infinite_current/)
- [https://www.reddit.com/r/askscience/comments/7xhb46/what_would_happen_if_a_voltage_was_applied_to_a/](https://www.reddit.com/r/askscience/comments/7xhb46/what_would_happen_if_a_voltage_was_applied_to_a/)

<a id="video-superconducting-short-circuits-across-batteries-by-eugene-khutoryansky-2020"></a>
**[Video 7](#video-superconducting-short-circuits-across-batteries-by-eugene-khutoryansky-2020). Superconducting Short Circuits across Batteries by Eugene Khutoryansky (2020)** [Source](https://www.youtube.com/watch?v=v8iD_waF_kM). Well, internal battery resistance acts as the only resistor, and voltage drops to zero immediately outside of the battery. And you get a huge current.

#### BCS Theory

↑ **Parent:** [Superconductivity](#superconductivity)  
🏷️ **Tags:** [1972 Nobel Prize in Physics](nobel-prize.md#1972-nobel-prize-in-physics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/BCS_Theory)

Main theory to explain Type I superconductors very successfully.

TODO can someone please just give the final predictions of BCS, and how they compare to experiments, first of all? Then derive them.

High level concepts:
- the wave functions of pairs of electrons (fermions) get together to form bosons. This is a [phase transition](statistical-physics.md#phase-transition) effect, thus the specific sudden transition temperature.
- the pairs form a [Bose-Einstein condensate](#bose-einstein-condensate)
- once this new state is reached, all pairs are somehow entangled into one big wave function, and you so individual lattice imperfections can't move just one single electron off trajectory and make it lose energy

#### Josephson effect

↑ **Parent:** [Superconductivity](#superconductivity)  
🏷️ **Tags:** [1973 Nobel Prize in Physics](nobel-prize.md#1973-nobel-prize-in-physics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Josephson_effect)

[Discrete](calculus.md#discrete) [quantum](quantum-mechanics.md) effect observed in [superconductors](#superconductivity) with a small insulating layer, a device known as a [Josephson junction](#josephson-junction).

To understand the behaviour effect, it is important to look at the [Josephson equations](#josephson-equations) consider the following [Josephson effect regimes](#josephson-effect-regime) separately:
- [DC Josephson effect](#dc-josephson-effect)
- [AC Josephson effect](#ac-josephson-effect)
- [Inverse AC Josephson effect](#inverse-ac-josephson-effect)

A good summary from Wikipedia by physicist Andrew Whitaker:

> at a junction of two superconductors, a current will flow even if there is no drop in voltage; that when there is a voltage drop, the current should oscillate at a frequency related to the drop in voltage; and that there is a dependence on any magnetic field

Bibliography:
- [https://www.youtube.com/watch?v=cnZ6exn2CkE](https://www.youtube.com/watch?v=cnZ6exn2CkE) "Superconductivity: Professor [Brian Josephson](physicist.md#brian-josephson)". Several random excerpts from Cambridge people talking about the Josephson effect

##### History of the Josephson effect

↑ **Parent:** [Josephson effect](#josephson-effect)  
🏷️ **Tags:** [History of condensed matter physics](#history-of-condensed-matter-physics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Josephson_effect#History)

In 1962 [Brian Josephson](physicist.md#brian-josephson) published his inaugural paper predicting the effect as [Section "Possible new effects in superconductive tunnelling"](#possible-new-effects-in-superconductive-tunnelling).

In 1963 [Philip W. Anderson](physicist.md#philip-w-anderson) and [John M. Rowell](physicist.md#john-rowell) published their paper that first observed the effect as [Section "Possible new effects in superconductive tunnelling"](#possible-new-effects-in-superconductive-tunnelling).

Some golden notes can be found at [True Genius: The Life and Science of John Bardeen](physicist.md#true-genius-the-life-and-science-of-john-bardeen) page 224 and around. [Philip W. Anderson](physicist.md#philip-w-anderson) commented:

> We were all - [Josephson](physicist.md#brian-josephson), Pippard and myself, as well as various other people who also habitually sat at the [Mond](university.md#mond-laboratory) tea and participated in the discussions of the next few weeks - very much puzzled by the meaning of the fact that the [current](electromagnetism.md#electric-current) depends on the [phase](#josephson-phase)

As part of the course Anderson had introduced the concept of broken symmetry in superconductors. Josephson "was fascinated by the idea of broken symmetry, and wondered whether there could be any way of observing it experimentally."

###### Possible new effects in superconductive tunnelling

↑ **Parent:** [History of the Josephson effect](#history-of-the-josephson-effect)  
🏷️ **Tags:** [Physical Review Letters](physics.md#physical-review-letters)

The inaugural that predicted the [Josephson effect](#josephson-effect).

Published on [Physics Letters](physics.md#physics-letters), then a new journal, before they split into [Physics Letters A](physics.md#physics-letters-a) and [Physics Letters B](physics.md#physics-letters-b). [True Genius: The Life and Science of John Bardeen](physicist.md#true-genius-the-life-and-science-of-john-bardeen) mentions that this choice was made rather than the more prestigious [Physical Review Letters](physics.md#physical-review-letters) because they were not yet so confident about the results.

[Paywalled](education.md#closed-access-academic-journals-are-evil) by [Elsevier](education.md#elsevier) as of 2023 at: [https://www.sciencedirect.com/science/article/abs/pii/0031916362913690](https://www.sciencedirect.com/science/article/abs/pii/0031916362913690)

###### Probable observation of the Josephson superconducting tunneling effect

↑ **Parent:** [History of the Josephson effect](#history-of-the-josephson-effect)  
🏷️ **Tags:** [Physical Review Letters](physics.md#physical-review-letters)

Paper by [Philip W. Anderson](physicist.md#philip-w-anderson) and [John M. Rowell](physicist.md#john-rowell) that first (?) experimentally observed the [Josephson effect](#josephson-effect).

[Paywalled](education.md#closed-access-academic-journals-are-evil) by the [American Physical Society](education.md#american-physical-society) as of 2023 at: [https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.10.230](https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.10.230)

[DOI](literature.md#digital-object-identifier): [https://doi.org/10.1103/PhysRevLett.10.230](https://doi.org/10.1103/PhysRevLett.10.230)

TODO understand the graphs in detail.

They used [tin](chemistry.md#tin)-oxide-[lead](chemistry.md#lead) tunnel at 1.5 K. TODO oxide of what? Why two different metals? They say that both films are 200 nm thick, so maybe it is:
```
   -----+------+------+-----
...  Sn | SnO2 | PbO2 | Pb  ...
   -----+------+------------
          100nm 100nm
```

A reconstruction of their circuit in [Ciro's ASCII art circuit diagram notation](electronics.md#ciro-s-ascii-art-circuit-diagram-notation) TODO:
```
DC---R_10---X---G
```

There are not details of the physical construction of course. [Reproducibility](science.md#reproducibility) lol.

<a id="image-figure-1-of-probable-observation-of-the-josephson-superconducting-tunneling-effect"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/probable-observation-of-the-josephson-superconducting-tunneling-effect/1.png)

**[Figure 8](#image-figure-1-of-probable-observation-of-the-josephson-superconducting-tunneling-effect). Figure 1 of Probable observation of the Josephson superconducting tunneling effect**. TODO what do the dotted lines mean?

<a id="image-figure-2-of-probable-observation-of-the-josephson-superconducting-tunneling-effect"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/probable-observation-of-the-josephson-superconducting-tunneling-effect/1.png)

**[Figure 9](#image-figure-2-of-probable-observation-of-the-josephson-superconducting-tunneling-effect). Figure 2 of Probable observation of the Josephson superconducting tunneling effect**.

##### Josephson effect regime

↑ **Parent:** [Josephson effect](#josephson-effect)

###### DC Josephson effect

↑ **Parent:** [Josephson effect regime](#josephson-effect-regime)

###### AC Josephson effect

↑ **Parent:** [Josephson effect regime](#josephson-effect-regime)

This is what happens when you apply a [DC voltage](electronics.md#direct-current) across a [Josephson junction](#josephson-junction).

It is called "AC effect" because when we apply a [DC voltage](electronics.md#direct-current), it produces an [alternating current](electronics.md#alternating-current) on the device.

By looking at the [Josephson equations](#josephson-equations), we see that $V(t) = k$ a positive constant, then $\varphi$ just increases linearly without bound.

Therefore, from the first equation:

$$
I(t) = I_c \sin (\varphi (t))
$$

we see that the current will just vary sinusoidally between $\pm I_c$.

This meas that we can use a [Josephson junction](#josephson-junction) as a perfect voltage to frequency converter.

Wikipedia mentions that this frequency is $484 GHz/mV$, so it is very very high, so we are not able to view individual points of the sine curve separately with our instruments.

Also it is likely not going to be very useful for many practical applications in this mode.

An [I-V curve](electronics.md#current-voltage-characteristic) can also be seen at: [Figure 12. "Electron microscope image of a Josephson junction its I-V curve"](#image-electron-microscope-image-of-a-josephson-junction-its-i-v-curve).

<a id="image-i-v-curve-of-the-ac-josephson-effect"></a>
![](https://upload.wikimedia.org/wikipedia/commons/d/dd/I-V_characteristics_of_Josephson_Junction.JPG)

**[Figure 10](#image-i-v-curve-of-the-ac-josephson-effect). I-V curve of the AC Josephson effect**. [Source](https://commons.wikimedia.org/wiki/File:I-V_characteristics_of_Josephson_Junction.JPG). Voltage is horizontal, current vertical. The vertical bar in the middle is the effect of interest: the current is going up and down very quickly between $\pm I_c$, the [Josephson current](#josephson-current) of the device. Because it is too quick for the [oscilloscope](electronics.md#oscilloscope), we just see a solid vertical bar.

The non vertical curves at right and left are just other effects we are not interested in.

TODO what does it mean that there is no line at all near the central vertical line? What happens at those voltages?

---

<a id="video-superconducting-transition-of-josephson-junction-by-christina-wicker-2016"></a>
**[Video 8](#video-superconducting-transition-of-josephson-junction-by-christina-wicker-2016). Superconducting Transition of Josephson junction by Christina Wicker (2016)** [Source](https://www.youtube.com/watch?v=FYnDcWFYyVA). Amazing video that presumably shows the screen of a digital [oscilloscope](electronics.md#oscilloscope) doing a voltage sweep as temperature is reduced and superconductivity is reached.

<a id="image-i-v-curve-of-a-superconducting-tunnel-junction"></a>
![](https://upload.wikimedia.org/wikipedia/en/6/6b/STJ_IV_Curve.jpg?20110816180152)

**[Figure 11](#image-i-v-curve-of-a-superconducting-tunnel-junction). I-V curve of a superconducting tunnel junction**. So it appears that there is a zero current between $V=0$ and $V=2\Delta/e$. Why doesn't it show up on the [oscilloscope](electronics.md#oscilloscope) sweeps, e.g. [Video 8. "Superconducting Transition of Josephson junction by Christina Wicker (2016)"](#video-superconducting-transition-of-josephson-junction-by-christina-wicker-2016)?

###### Inverse AC Josephson effect

↑ **Parent:** [Josephson effect regime](#josephson-effect-regime)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Josephson_effect#The_inverse_AC_Josephson_effect)

If you shine [microwave](photon.md#microwave) radiation on a Josephson junction, it produces a fixed average voltage that depends only on the frequency of the microwave. TODO how is that done more precisely? How to you produce and inject microwaves into the thing?

It acts therefore as a perfect frequency to voltage converter.

The Wiki page gives the formula: [https://en.wikipedia.org/wiki/Josephson_effect#The_inverse_AC_Josephson_effect](https://en.wikipedia.org/wiki/Josephson_effect#The_inverse_AC_Josephson_effect) You get several sinusoidal harmonics, so the output is not a perfect sine. But the infinite sum of the harmonics has a fixed average voltage value.

And [https://en.wikipedia.org/wiki/Josephson_voltage_standard#Josephson_effect](https://en.wikipedia.org/wiki/Josephson_voltage_standard#Josephson_effect) mentions that the effect is independent of the junction material, physical dimension or temperature.

All of the above, compounded with the fact that we are able to generate microwaves with extremely precise frequency with an [atomic clock](system-of-units.md#atomic-clock), makes this phenomenon perfect as a [Volt](electromagnetism.md#volt) standard, the [Josephson voltage standard](#josephson-voltage-standard).

TODO understand how/why it works better.

###### Shapiro steps

↑ **Parent:** [Inverse AC Josephson effect](#inverse-ac-josephson-effect)

##### Josephson equations

↑ **Parent:** [Josephson effect](#josephson-effect)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Josephson_equations)

Two equations derived [from first principles](science.md#from-first-principles) by [Brian Josephson](physicist.md#brian-josephson) that characterize the device, somewhat like an [I-V curve](electronics.md#current-voltage-characteristic):

$$
I(t) = I_c \sin (\varphi (t)) \\
\dv{\varphi(t)}{t} = \frac{2 e V(t)}{\hbar}
$$

where:
- $I_c$: [Josephson current](#josephson-current)
- $\varphi$: the [Josephson phase](#josephson-phase), a function $\R \to \R$ defined by the second equation plus initial conditions
- $V(t)$: input voltage of the system
- $I(t)$: current across the junction, determined by the input voltage

Note how these equations are not a typical [I-V curve](electronics.md#current-voltage-characteristic), as they are not an instantaneous dependency between voltage and current: the history of the voltage matters! Or in other words, the system has an internal state, represented by the [Josephson phase](#josephson-phase) at a given point in time.

To understand them better, it is important to look at some important cases separately:
- [AC Josephson effect](#ac-josephson-effect): V is a fixed [DC voltage](electronics.md#direct-current)

###### Josephson current

↑ **Parent:** [Josephson equations](#josephson-equations)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Josephson_current)

Maximum current that can flow across a [Josephson junction](#josephson-junction), as can be directly seen from the [Josephson equations](#josephson-equations).

Is a fixed characteristic value of the physical construction of the junction.

###### Josephson phase

↑ **Parent:** [Josephson equations](#josephson-equations)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Josephson_phase)

A function $\R \to \R$ defined by the second of the [Josephson equations](#josephson-equations) plus initial conditions.

It represents an internal state of the junction.

##### Josephson junction

↑ **Parent:** [Josephson effect](#josephson-effect)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Josephson_junction)

A device that exhibits the [Josephson effect](#josephson-effect).

<a id="image-electron-microscope-image-of-a-josephson-junction-its-i-v-curve"></a>
![](https://web.archive.org/web/20220615163007im_/https://www.researchgate.net/publication/330223210/figure/fig9/AS:606819705688070@1521688500497/FIG-S2-Josephson-junction-of-a-second-sample-a-Scanning-electron-micrograph-of-sample.png)

**[Figure 12](#image-electron-microscope-image-of-a-josephson-junction-its-i-v-curve). Electron microscope image of a Josephson junction its I-V curve**. [Source](https://www.researchgate.net/figure/FIG-S2-Josephson-junction-of-a-second-sample-a-Scanning-electron-micrograph-of-sample\_fig9\_330223210).

###### Pi Josephson junction

↑ **Parent:** [Josephson junction](#josephson-junction)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Pi_Josephson_junction)

##### Magnetic flux quantum

↑ **Parent:** [Josephson effect](#josephson-effect)  
🏷️ **Tags:** [Physical Review Letters article](physics.md#physical-review-letters-article)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Magnetic_flux_quantum)

TODO is there any relationship between this and the [Josephson effect](#josephson-effect)?

Experimental observation published as [Experimental Evidence for Quantized Flux in Superconducting Cylinders](#experimental-evidence-for-quantized-flux-in-superconducting-cylinders).

This appears to happen to any superconducting loop, because the superconducting wave function has to be continuous.

[Video "Superconducting Qubit by NTT SCL (2015)"](quantum-computing.md#video-superconducting-qubit-by-ntt-scl-2015) suggests that anything in between gets cancelled out by a [superposition](quantum-mechanics.md#quantum-superposition) of current in both directions.

###### Experimental Evidence for Quantized Flux in Superconducting Cylinders

↑ **Parent:** [Magnetic flux quantum](#magnetic-flux-quantum)  
🏷️ **Tags:** [Physical Review Letters article](physics.md#physical-review-letters-article)

Paywalled at: [https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.7.43](https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.7.43)

The first published experimental observation of the [magnetic flux quantum](#magnetic-flux-quantum).

The paper that follows it in the journal is also of interest, "Theoretical Considerations Concerning Quantized Magnetic Flux In Superconducting Cylinders" by N. Byers and C. N. Yang, it starts:

> In a recent experiment, the magnetic flux through a superconducting ring has been found to be quantized in units of ch/2e. Quantization in twice this unit has been briefly discussed by London' and by Onsager. ' Onsager' has also considered the possibility of quantization in units ch/2e due to pairs of electrons forming quasi-bosons.

So there was some previous confusion about the flux quantum due to the presence of [Cooper pairs](#cooper-pair) or not.

Dumping the fitures at: [https://archive.org/details/experimental-evidence-for-quantized-flux-in-superconducting-cylinders](https://archive.org/details/experimental-evidence-for-quantized-flux-in-superconducting-cylinders) One day we can also dump the paper scans when it goes into the public domain in 2056! [Public domain scientific paper by year](law.md#public-domain-scientific-paper-by-year).

<a id="image-figure-1-of-experimental-evidence-for-quantized-flux-in-superconducting-cylinders"></a>
![](https://archive.org/download/experimental-evidence-for-quantized-flux-in-superconducting-cylinders-fig.-1/Experimental%20Evidence%20for%20Quantized%20Flux%20in%20Superconducting%20Cylinders%20Fig.%201.png)

**[Figure 13](#image-figure-1-of-experimental-evidence-for-quantized-flux-in-superconducting-cylinders). Figure 1 of Experimental Evidence for Quantized Flux in Superconducting Cylinders**. The legend reads:> (Upper) Trapped flux in cylinder No. 1 as a function of magnetic field in which the cylinder was cooled below the superconducting transition. temperature. The open circles are individual data points. The solid circles represent th, e average value of all data points at a particular value of applied field including all the points plotted and additional data which could not be plotted due to severe overlapping of points. Approximately two hundred data points are represented. The lines are drawn at multiples of hc/2e.
> 
> (Lower) Net flux in cylinder No. 1 before turning off the applied field in which it was cooled as a function of the applied field. Open and solid circles have the same significance as above. The lower line is the diamagnetic calibration to which all runs have been normalized. The other lines are translated vertically by successive steps of hc/2e.

---

<a id="image-figure-2-of-experimental-evidence-for-quantized-flux-in-superconducting-cylinders"></a>
![](https://archive.org/download/experimental-evidence-for-quantized-flux-in-superconducting-cylinders-fig.-1/Experimental%20Evidence%20for%20Quantized%20Flux%20in%20Superconducting%20Cylinders%20Fig.%202.png)

**[Figure 14](#image-figure-2-of-experimental-evidence-for-quantized-flux-in-superconducting-cylinders). Figure 2 of Experimental Evidence for Quantized Flux in Superconducting Cylinders**. The legend reads:> (Upper) Trapped flux in cylinder No. 2 as a function of magnetic field in which the cylinder was cooled below the superconducting transition temperature. The circles and triangles indicate points for oppositely directed applied fields. Lines are drawn at multiples of hc/2e.
> 
> (Lower) Net flux in cylinder No. 2 before turning off the applied field as a function of the applied field. The circles and triangles are points for oppositely directed applied fields. The lower line is the diamagnetic calibration to which all runs have The other been normalized. lines are translated vertically by successive steps of hc/2e.

---

###### Josephson constant

↑ **Parent:** [Magnetic flux quantum](#magnetic-flux-quantum)

The inverse of the [magnetic flux quantum](#magnetic-flux-quantum).

##### Symmetry breaking in superconductors

↑ **Parent:** [Josephson effect](#josephson-effect)

[https://physics.stackexchange.com/questions/133780/superconductor-symmetry-breaking](https://physics.stackexchange.com/questions/133780/superconductor-symmetry-breaking)

As mentioned in [True Genius: The Life and Science of John Bardeen](physicist.md#true-genius-the-life-and-science-of-john-bardeen) page 224, the idea of [symmetry breaking](group.md#symmetry-breaking) was a major motivation in Josephson's study of the [Josephson effect](#josephson-effect).

##### Applications of Josephson Junctions

↑ **Parent:** [Josephson effect](#josephson-effect)

- the basis for the most promising 2019 [quantum computing](quantum-computing.md) implementation: [superconducting quantum computer](quantum-computing.md#superconducting-quantum-computing)
- [Josephson voltage standard](#josephson-voltage-standard): the most practical/precise [Volt](electromagnetism.md#volt) standard, which motivated the definition of the [ampere in the 2019 redefinition of the SI base units](system-of-units.md#ampere-in-the-2019-redefinition-of-the-si-base-units)
- [SQUID devices](#squid-device), which are:
  - very precise [magnetometer](electromagnetism.md#magnetometer)
  - the basis for [superconducting quantum computers](quantum-computing.md#superconducting-quantum-computing)

###### Josephson voltage standard

↑ **Parent:** [Applications of Josephson Junctions](#applications-of-josephson-junctions)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Josephson_voltage_standard)

The most practical/precise volt standard.

It motivated the definition of the [ampere in the 2019 redefinition of the SI base units](system-of-units.md#ampere-in-the-2019-redefinition-of-the-si-base-units)

Good [NIST](research-institute.md#national-institute-of-standards-and-technology) articles about it:
- [A Primary Voltage Standard for the Whole World](https://www.nist.gov/news-events/news/2013/04/primary-voltage-standard-whole-world)  
   (2013)
 ([archive](https://web.archive.org/web/20190410011041/https://www.nist.gov/news-events/news/2013/04/primary-voltage-standard-whole-world))
- [History of NIST Quantum Voltage Standards (2011-2022)](https://www.nist.gov/pml/history-nist-quantum-voltage-standards)

The wiki page [https://en.wikipedia.org/wiki/Josephson_voltage_standard](https://en.wikipedia.org/wiki/Josephson_voltage_standard) contains amazing schematics of the device, apparently made by the [US Government](united-states.md#united-states-government).

<a id="image-schematic-of-a-typical-josephson-voltage-standard-chip"></a>
<img src="https://upload.wikimedia.org/wikipedia/commons/2/2b/Layout_and_Schematic_of_JVS_Chip.jpg" alt="" height="600">

**[Figure 15](#image-schematic-of-a-typical-josephson-voltage-standard-chip). Schematic of a typical Josephson voltage standard chip**. [Source](https://commons.wikimedia.org/wiki/File:Layout_and_Schematic_of_JVS_Chip.jpg).

<a id="image-sam-benz-demonstrating-the-equipment-required-the-voltage-standard"></a>
<img src="https://web.archive.org/web/20241201074611im_/https://www.nist.gov/sites/default/files/styles/480_x_480_limit/public/images/pml/div686/devices/sam-switch900.png?itok=OyCJl26y" alt="" height="600">

**[Figure 16](#image-sam-benz-demonstrating-the-equipment-required-the-voltage-standard). Sam Benz demonstrating the equipment required the voltage standard**. [Source](https://www.nist.gov/news-events/news/2013/04/primary-voltage-standard-whole-world).

<a id="video-the-evolution-of-voltage-metrology-to-the-latest-generation-of-jvss-by-alain-rufenacht"></a>
**[Video 9](#video-the-evolution-of-voltage-metrology-to-the-latest-generation-of-jvss-by-alain-rufenacht). The evolution of voltage metrology to the latest generation of JVSs by Alain Rüfenacht.** [Source](https://www.youtube.com/watch?v=VoRab8U2eS0). Talk given in 2023. The speaker is from [NIST](research-institute.md#national-institute-of-standards-and-technology), and the talk was hosted by the [BIPM](system-of-units.md#international-bureau-of-weights-and-measures). Fantastic talk.
- [https://youtu.be/VoRab8U2eS0?t=354](https://youtu.be/VoRab8U2eS0?t=354) the desired output voltage is 10V
- [https://youtu.be/VoRab8U2eS0?t=475](https://youtu.be/VoRab8U2eS0?t=475) lists the three most commonly used 10V implementations currently:
  - [Japanese](japan.md) one by [AIST](research-institute.md#national-institute-of-advanced-industrial-science-and-technology)
  - [American](united-states.md) one by [NIST](research-institute.md#national-institute-of-standards-and-technology)
  - [German](continent.md#germany) one by [PTB](research-institute.md#physikalisch-technische-bundesanstalt)

---

<a id="video-technical-aspects-of-realizing-the-dc-volt-in-the-laboratory-with-a-jvs-by-stephane-solve"></a>
**[Video 10](#video-technical-aspects-of-realizing-the-dc-volt-in-the-laboratory-with-a-jvs-by-stephane-solve). Technical aspects of realizing the DC volt in the laboratory with a JVS by Stéphane Solve.** [Source](https://www.youtube.com/watch?v=VoRab8U2eS0). Talk given in 2023. The speaker is from [BIPM](system-of-units.md#international-bureau-of-weights-and-measures), and the talk was hosted by the [BIPM](system-of-units.md#international-bureau-of-weights-and-measures). Fantastic talk.
- [https://youtu.be/6pgGNJby1lw?t=296](https://youtu.be/6pgGNJby1lw?t=296) gives the experimental setup used to compare two different references. Notably it involves a [nanovoltmeter](electromagnetism.md#nanovoltmeter)

---

###### SQUID device

↑ **Parent:** [Applications of Josephson Junctions](#applications-of-josephson-junctions)  
🏷️ **Tags:** [Electronic component](electronics.md#electronic-component), [Magnetometer](electromagnetism.md#magnetometer)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/SQUID)

Can be used as a very precise [magnetometer](electromagnetism.md#magnetometer).

There are high temperature [yttrium barium copper oxide](#yttrium-barium-copper-oxide) ones that work on [liquid nitrogen](chemistry.md#liquid-nitrogen).

<a id="video-superconducting-quantum-interference-device-by-felipe-contipelli-2019"></a>
**[Video 11](#video-superconducting-quantum-interference-device-by-felipe-contipelli-2019). Superconducting Quantum Interference Device by Felipe Contipelli (2019)** [Source](https://www.youtube.com/watch?v=d_vrhzX3VcE). Good intuiotionistic video. Some points deserved a bit more detail.

<a id="video-mishmash-of-squid-interviews-and-talks-by-bartek-glowaki"></a>
**[Video 12](#video-mishmash-of-squid-interviews-and-talks-by-bartek-glowaki). Mishmash of SQUID interviews and talks by Bartek Glowaki.** [Source](https://www.youtube.com/watch?v=0kl3ucjh2Uw). The videos come from: [https://www.ascg.msm.cam.ac.uk/lectures/](https://www.ascg.msm.cam.ac.uk/lectures/). Vintage.

Mentions that the [SQUID device](#squid-device) is analogous to a [double-slit experiment](quantum-mechanics.md#double-slit-experiment).

One of the segments is by John Clarke.

---

<a id="video-superconducting-quantum-interference-devices-by-unsw-physics-2020"></a>
**[Video 13](#video-superconducting-quantum-interference-devices-by-unsw-physics-2020). Superconducting Quantum Interference Devices by UNSW Physics (2020)** [Source](https://www.youtube.com/watch?v=ql2Yo5LgU8M). An experimental lab video for [COVID-19](taxonomy.md#covid-19) lockdown. Thanks, [COVID-19](taxonomy.md#covid-19). Presented by a cute and awkward Adam Stewart.

Uses a [SQUID device](#squid-device) and control system made by [STAR Cryoelectronics](electronics.md#star-cryoelectronics). We can see [Mr. SQUID](electronics.md#mr-squid) EB-03 written on the probe and control box, that is their educational product.

As mentioned on the Mr. SQUID specs, it is a [high-temperature superconductor](#high-temperature-superconductivity), so [liquid nitrogen](chemistry.md#liquid-nitrogen) is used.

He then measures the [I-V curve](electronics.md#current-voltage-characteristic) on an [Agilent Technologies oscilloscope](electronics.md#agilent-technologies-oscilloscope).

Unfortunately, the video doesn't explain very well what is happening behind the scenes, e.g. with a [circuit diagram](electronics.md#circuit-diagram). That is the curse of university laboratory videos: some of them assume that students will have material from other internal sources.


- [https://youtu.be/ql2Yo5LgU8M?t=211](https://youtu.be/ql2Yo5LgU8M?t=211) shows the classic voltage oscillations, presumably on a magnetic field sweep, and then he puts a [magnet](#magnet) next to the device from outside the [Dewar](technology.md#vacuum-flask)
- [https://youtu.be/ql2Yo5LgU8M?t=253](https://youtu.be/ql2Yo5LgU8M?t=253) demonstrates the formation of [Shapiro steps](#shapiro-steps). Inserts a [Rohde & Schwarz](electronics.md#rohde-and-schwarz) signal generator into the Dewar to vary the flux. The result is not amazing, but they are visible somewhat.

---

<a id="video-the-ubiquitous-squid-by-john-clarke-2018"></a>
**[Video 14](#video-the-ubiquitous-squid-by-john-clarke-2018). The Ubiquitous SQUID by John Clarke (2018)** [Source](https://www.youtube.com/watch?v=7PJguB3Y8L8).

###### DC SQUID

↑ **Parent:** [SQUID device](#squid-device)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/SQUID#DC_SQUID)

Two parallel [Josephson junctions](#josephson-junction).

In [Ciro's ASCII art circuit diagram notation](electronics.md#ciro-s-ascii-art-circuit-diagram-notation):
```
  |
+-+-+
|   |
X   X
|   |
+-+-+
  |
```

## Superconducting tunnel junction

↑ **Parent:** [Condensed matter physics](condensed-matter-physics.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Superconducting_tunnel_junction)

Specific type of [Josephson junction](#josephson-junction). Probably can be made tiny and in huge numbers through [photolithography](computer-hardware.md#photolithography).

<a id="image-illustration-of-a-thin-film-superconducting-tunnel-junction-stj"></a>
![](https://web.archive.org/web/20210124093431im_/https://upload.wikimedia.org/wikipedia/commons/thumb/8/81/Superconducting_tunnel_junction.svg/735px-Superconducting_tunnel_junction.svg.png)

**[Figure 17](#image-illustration-of-a-thin-film-superconducting-tunnel-junction-stj). Illustration of a thin-film superconducting tunnel junction (STJ)** [Source](https://upload.wikimedia.org/wikipedia/commons/8/81/Superconducting\_tunnel\_junction.svg). The superconducting material is light blue, the insulating tunnel barrier is black, and the substrate is green.

<a id="video-quantum-transport-lecture-14-josephson-effects-by-sergey-frolov-2013"></a>
**[Video 15](#video-quantum-transport-lecture-14-josephson-effects-by-sergey-frolov-2013). Quantum Transport, Lecture 14: Josephson effects by Sergey Frolov (2013)** [Source](http://youtube.com/watch?v=-HUVGWTfaSI). [https://youtu.be/-HUVGWTfaSI?t=878](https://youtu.be/-HUVGWTfaSI?t=878) mentions [maskless electron beam lithography](https://en.wikipedia.org/wiki/Electron-beam_lithography) being used to produce STJs.

## Superfluidity

↑ **Parent:** [Condensed matter physics](condensed-matter-physics.md)  
🏷️ **Tags:** [Second-order phase transition](statistical-physics.md#second-order-phase-transition)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Superfluidity)

<a id="video-alfred-leitner-liquid-helium-ii-the-superfluid-by-alfred-leitner-1963"></a>
**[Video 16](#video-alfred-leitner-liquid-helium-ii-the-superfluid-by-alfred-leitner-1963). Alfred Leitner - Liquid Helium II the Superfluid by Alfred Leitner (1963)** [Source](http://youtube.com/watch?v=7eZlF6IToQs). Original source: [http://www.alfredleitner.com](http://www.alfredleitner.com).

<a id="video-ben-miller-experiments-with-superfluid-helium-by-bbc-2011"></a>
**[Video 17](#video-ben-miller-experiments-with-superfluid-helium-by-bbc-2011). Ben Miller experiments with superfluid helium by BBC (2011)** [Source](http://youtube.com/watch?v=9FudzqfpLLs). Just quickly shows the superfluid helium climbing out o the cup, no detailed setup. With [professor Robert Taylor](https://www2.physics.ox.ac.uk/contacts/people/rtaylor) from the [University of Oxford](university-of-oxford.md).

## State of matter

↑ **Parent:** [Condensed matter physics](condensed-matter-physics.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/State_of_matter)

### High pressure

↑ **Parent:** [State of matter](#state-of-matter)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/High_pressure)

<a id="video-something-weird-happens-when-you-keep-squeezing-by-vox-2023"></a>
**[Video 18](#video-something-weird-happens-when-you-keep-squeezing-by-vox-2023). Something weird happens when you keep squeezing by Vox (2023)** [Source](https://www.youtube.com/watch?v=NqabT21d8VM). [Sodium](chemistry.md#sodium) becomes liquid when you compress it. Weird.

## List of states of matter

↑ **Parent:** [Condensed matter physics](condensed-matter-physics.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/List_of_states_of_matter)

### Solid

↑ **Parent:** [List of states of matter](#list-of-states-of-matter)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Solid)

### Liquid

↑ **Parent:** [List of states of matter](#list-of-states-of-matter)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Liquid)

### Gas

↑ **Parent:** [List of states of matter](#list-of-states-of-matter)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Gas)

#### Fermi gas

↑ **Parent:** [Gas](#gas)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Fermi_gas)

##### Electron gas

↑ **Parent:** [Fermi gas](#fermi-gas)

###### Two-dimensional electron gas

↑ **Parent:** [Electron gas](#electron-gas)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Two-dimensional_electron_gas)

###### Laughlin wavefunction

↑ **Parent:** [Two-dimensional electron gas](#two-dimensional-electron-gas)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Laughlin_wavefunction)

##### 1D Fermi gas

↑ **Parent:** [Fermi gas](#fermi-gas)

###### Impenetrable Bose Gas

↑ **Parent:** [1D Fermi gas](#1d-fermi-gas)

### Bose-Einstein condensate

↑ **Parent:** [List of states of matter](#list-of-states-of-matter)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Bose–Einstein_condensate)

[Inward Bound by Abraham Pais (1988)](particle-physics.md#inward-bound-by-abraham-pais-1988) page 282 shows how this can be generalized from the [Maxwell-Boltzmann distribution](statistical-physics.md#maxwell-boltzmann-distribution)

## Materials science

↑ **Parent:** [Condensed matter physics](condensed-matter-physics.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Materials_science)

### Type of material

↑ **Parent:** [Materials science](#materials-science)

#### Glass

↑ **Parent:** [Type of material](#type-of-material)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Glass)

#### Quantum dot

↑ **Parent:** [Type of material](#type-of-material)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Quantum_dot)

TODO WTF is this? How is it built? What is special about it?

Mentioned a lot in the context of [superconducting quantum computers](quantum-computing.md#superconducting-quantum-computing), e.g. [https://youtu.be/t5nxusm_Umk?t=268](https://youtu.be/t5nxusm_Umk?t=268) from [Video "Quantum Computing with Superconducting Qubits by Alexandre Blais (2012)"](quantum-computing.md#video-quantum-computing-with-superconducting-qubits-by-alexandre-blais-2012),

##### Quantum dot single photon source

↑ **Parent:** [Quantum dot](#quantum-dot)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Quantum_dot_single_photon_source)

Mentioned at: [Video "Quantum Computing with Light by Quantum Light University of Sheffield (2015)"](photon.md#video-quantum-computing-with-light-by-quantum-light-university-of-sheffield-2015) [https://youtu.be/nyK-vhoOBpE?t=185](https://youtu.be/nyK-vhoOBpE?t=185).

#### Metal

↑ **Parent:** [Type of material](#type-of-material)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Metal)

##### Field electron emission

↑ **Parent:** [Metal](#metal)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Field_electron_emission)

##### Alloy

↑ **Parent:** [Metal](#metal)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Alloy)

###### Binary alloy

↑ **Parent:** [Alloy](#alloy)

Bibliography: [https://phys.libretexts.org/Bookshelves/Thermodynamics_and_Statistical_Mechanics/Heat_and_Thermodynamics_(Tatum)/17%3A_Chemical_Thermodynamics/17.09%3A_Binary_Alloys](https://phys.libretexts.org/Bookshelves/Thermodynamics_and_Statistical_Mechanics/Heat_and_Thermodynamics_(Tatum)/17%3A_Chemical_Thermodynamics/17.09%3A_Binary_Alloys)

##### Metallurgy

↑ **Parent:** [Metal](#metal)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Metallurgy)

###### Ingot

↑ **Parent:** [Metallurgy](#metallurgy)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Ingot)

#### Polymer

↑ **Parent:** [Type of material](#type-of-material)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Polymer)

##### Plastic

↑ **Parent:** [Polymer](#polymer)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Plastic)

[https://www.youtube.com/watch?v=PbuiIhr0LVA](https://www.youtube.com/watch?v=PbuiIhr0LVA) 7 Different Types of Plastic and Their Uses by Orange Plastics Academy (2018) Does not mention packaging foams.

### Material property

↑ **Parent:** [Materials science](#materials-science)

#### Material property database

↑ **Parent:** [Material property](#material-property)  
🏷️ **Tags:** [Database](software.md#database)

##### Open material property database

↑ **Parent:** [Material property database](#material-property-database)

###### The Materials Project

↑ **Parent:** [Open material property database](#open-material-property-database)

[https://next-gen.materialsproject.org/](https://next-gen.materialsproject.org/)

Signup required for any search, bastards. But it's free. Once you have a URL however it is visible without login, so you could just [Google](google.md) it too.

#### Density

↑ **Parent:** [Material property](#material-property)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Density)

#### Magnet

↑ **Parent:** [Material property](#material-property)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Magnet)

##### Permanent magnet

↑ **Parent:** [Magnet](#magnet)

###### Curie temperature

↑ **Parent:** [Permanent magnet](#permanent-magnet)  
🏷️ **Tags:** [Phase transition](statistical-physics.md#phase-transition)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Curie_temperature)

<a id="image-variation-of-saturation-magnetisation-with-temperature-for-nickel"></a>
![](https://web.archive.org/web/20231130040035im_/https://www.doitpoms.ac.uk/tlplib/ferromagnetic/images/FigureJ.gif)

**[Figure 18](#image-variation-of-saturation-magnetisation-with-temperature-for-nickel). Variation of saturation magnetisation with temperature for Nickel**. [Source](https://www.doitpoms.ac.uk/tlplib/ferromagnetic/hysteresis.php). This graph shows what happens when you approach the [Curie temperature](#curie-temperature) from below.

###### Ferromagnetism

↑ **Parent:** [Permanent magnet](#permanent-magnet)  
🏷️ **Tags:** [Second-order phase transition](statistical-physics.md#second-order-phase-transition)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Ferromagnetism)

The wiki comments: [https://en.wikipedia.org/w/index.php?title=Ferromagnetism&oldid=965600553#Explanation](https://en.wikipedia.org/w/index.php?title=Ferromagnetism&oldid=965600553#Explanation)

> The Bohr-van Leeuwen theorem, discovered in the 1910s, showed that classical physics theories are unable to account for any form of magnetism, including ferromagnetism. Magnetism is now regarded as a purely quantum mechanical effect. Ferromagnetism arises due to two effects from quantum mechanics: spin and the Pauli exclusion principle.

###### Magnetic hysteresis

↑ **Parent:** [Ferromagnetism](#ferromagnetism)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Magnetic_hysteresis)

To understand the graph, first learn/remember the difference between the [magnetic B and H field](electromagnetism.md#magnetic-b-and-h-field).

The interest of the [magnetic hysteresis](#magnetic-hysteresis) graph is that it serves as an important characterization of a :
- its area gives you the hysteresis loss of the [transformer](electronics.md#transformer), which is a major cause of efficiency loss of the component
- some key points of the curve give important characterizations of the core/material:
  - [Saturation magnetisation](#saturation-magnetisation)
  - magnetization strength without field
  - how much field you need to demagnetize it
This curve will also tell you how many turns of the coil will be needed to reach the required field.

<a id="image-theoretical-magnetic-hysteresis-plot"></a>
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/c/c3/StonerWohlfarthMainLoop.svg/500px-StonerWohlfarthMainLoop.svg.png" alt="" height="600">

**[Figure 19](#image-theoretical-magnetic-hysteresis-plot). Theoretical magnetic hysteresis plot**. [Source](https://commons.wikimedia.org/wiki/File:StonerWohlfarthMainLoop.svg.png).

<a id="video-measurement-of-b-h-characteristic"></a>
**[Video 19](#video-measurement-of-b-h-characteristic). Measurement of B-H characteristic.** [Source](https://www.youtube.com/watch?v=pXukVix5Pcw). 1989. 1989 and they were making such awesome materials. It is hard to understand why university still exists given this.

Shows how you can obtain the [magnetic hysteresis](#magnetic-hysteresis) curve with an [AC source](electronics.md#alternating-current-source) plus an [oscilloscope in XY mode](electronics.md#oscilloscope-xy-mode). [https://youtu.be/pXukVix5Pcw?t=193](https://youtu.be/pXukVix5Pcw?t=193) clearly shows the measurement circuit.

---

<a id="video-magnetic-hysteresis-experiment-by-unsw-physics"></a>
**[Video 20](#video-magnetic-hysteresis-experiment-by-unsw-physics). Magnetic hysteresis experiment by UNSW Physics.** [Source](https://www.youtube.com/watch?v=YiKFPyfC1HY). 2020, thanks [COVID-19](taxonomy.md#covid-19). Like other [UNSW Physics YouTube channel](physics.md#unsw-physics-youtube-channel) videos, the experimental setup could be made clearer with diagrams.

But this video does have one merit: it shows that the hysteresis plot can be obtained directly with the [oscilloscope XY mode](electronics.md#oscilloscope-xy-mode) by using an [AC source](electronics.md#alternating-current-source). The Y axis is just a measure of the total magnetic field induced by the primary coil + the magnetization of the material itself.

---

###### Saturation magnetisation

↑ **Parent:** [Magnetic hysteresis](#magnetic-hysteresis)

##### Electromagnet

↑ **Parent:** [Magnet](#magnet)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Electromagnet)

[Electromagnets](#electromagnet) allow us to create controllable [magnetic fields](electromagnetism.md#magnetic-field), i.e.: they act as [magnets](#magnet) that we can turn on and off as we please but controlling an input [voltage](electromagnetism.md#voltage).

Compare them to [permanent magnet](#permanent-magnet): on a magnet, you always have a fixed generated magnetic field. But with an [electromagnet](#electromagnet) you can control the field, and even turn it off entirely.

This type of "useful looking thing that can be controlled by a voltage" tends to be of huge importance in [electrical engineering](electronics.md#electrical-engineer), the [transistor](electronics.md#transistor) being another example.

###### Electromagnetic coil

↑ **Parent:** [Electromagnet](#electromagnet)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Electromagnetic_coil)

###### Solenoid

↑ **Parent:** [Electromagnet](#electromagnet)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Solenoid)

[Solenoids](#solenoid) are a type of [electromagnet coil](#electromagnetic-coil) of [helical](https://ourbigbook.com/go/topic/helical) shape.

Solenoid means "tubular" in [Greek](linguistics.md#greek-language).

Solenoids are simpler to build as they don't require [insulated wire](https://ourbigbook.com/go/topic/insulated-wire) as in modern [electrical cable](electronics.md#electrical-cable) because as the [electromagnetic coils](#electromagnetic-coil) don't touch one another.

As such it is perhaps the reason why some early electromagnetism experiments were carried out with solenoids, which [André-Marie Ampère](https://ourbigbook.com/go/topic/andre-marie-ampere) named in 1823.

But the downside of this is that the [magnetic field](electromagnetism.md#magnetic-field) they can generate is less strong.

<a id="image-illustration-of-a-solenoid"></a>
![](https://en.wikipedia.org/wiki/File:Solenoid-1.png)

**[Figure 20](#image-illustration-of-a-solenoid). Illustration of a solenoid**.

<a id="image-magnetic-field-lines-around-a-solenoid-cross-section"></a>
![](https://en.wikipedia.org/wiki/File:VFPt_Solenoid_correct2.svg)

**[Figure 21](#image-magnetic-field-lines-around-a-solenoid-cross-section). Magnetic field lines around a solenoid cross-section**. TODO accurate simulation or not?

###### Lifting electromagnet

↑ **Parent:** [Electromagnet](#electromagnet)

<a id="video-easy-to-build-electromagnet-lifts-over-50-lbs-by-dorian-mcintire"></a>
**[Video 21](#video-easy-to-build-electromagnet-lifts-over-50-lbs-by-dorian-mcintire). Easy-to-Build Electromagnet lifts over 50 lbs by Dorian McIntire.** [Source](https://www.youtube.com/watch?v=SGoOu8cPmeM). Fun, but zero reproducibility.

###### Breaking Bad magnet scene

↑ **Parent:** [Lifting electromagnet](#lifting-electromagnet)  
🏷️ **Tags:** [Breaking Bad](television-series.md#breaking-bad)

Is it realistic?
- [https://www.reddit.com/r/breakingbad/comments/wqyn4/spoilers_the_hard_drive_was_solid_state_the/](https://www.reddit.com/r/breakingbad/comments/wqyn4/spoilers_the_hard_drive_was_solid_state_the/)
- [https://www.quora.com/How-realistic-is-Breaking-Bads-portrayal-of-magnets-in-season-5s-premiere](https://www.quora.com/How-realistic-is-Breaking-Bads-portrayal-of-magnets-in-season-5s-premiere)

<a id="video-yeah-bitch-magnets-scene-from-breaking-bad"></a>
**[Video 22](#video-yeah-bitch-magnets-scene-from-breaking-bad). Yeah, bitch! Magnets! scene from Breaking Bad.** [Source](https://www.youtube.com/watch?v=vJ7vEZIrfPo).

<a id="video-police-evidence-magnet-scene-from-breaking-bad"></a>
**[Video 23](#video-police-evidence-magnet-scene-from-breaking-bad). Police evidence magnet scene from Breaking Bad.** [Source](https://www.youtube.com/watch?v=xVEj36ABsVU).

##### Ising model

↑ **Parent:** [Magnet](#magnet)  
🏷️ **Tags:** [Statistical mechanics model](statistical-physics.md#statistical-mechanics-model)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Ising_model)

Toy model of matter that exhibits [phase transition](statistical-physics.md#phase-transition) in dimension 2 and greater. It does not provide numerically exact results by itself, but can serve as a tool to theorize existing and new [phase transitions](statistical-physics.md#phase-transition).

Each point in the lattice has two possible states: TODO insert image.

As mentioned at: [https://stanford.edu/~jeffjar/statmech/intro4.html](https://stanford.edu/~jeffjar/statmech/intro4.html) some systems which can be seen as modelled by it include:
- the spins direction (up or down) of atoms in a [magnet](#magnet), which can undergo phase transitions depending on temperature as that characterized by the [Curie temperature](#curie-temperature) and an externally applied magnetic field

  Neighboring spins like to align, which lowers the total system energy.
- the type of atom at a lattice point in a 2-metal [alloy](#alloy), e.g. [Fe-C](chemistry.md#fe-c) (e.g. [steel](chemistry.md#steel)). TODO: intuition for the neighbor interaction? What likes to be with what? And aren't different phases in different crystal structures?

Also has some funky relations to [renormalization](quantum-field-theory.md#renormalization) TODO.

Bibliography:
- [https://stanford.edu/~jeffjar/statmech/intro4.html](https://stanford.edu/~jeffjar/statmech/intro4.html)

<a id="video-the-ising-model-in-python-by-mr-p-solver"></a>
**[Video 24](#video-the-ising-model-in-python-by-mr-p-solver). The Ising Model in Python by Mr. P Solver.** [Source](https://www.youtube.com/watch?v=K--1hlv9yv0). The dude is crushing it on a [Jupyter Notebook](programming-language.md#jupyter-notebook).

###### Solution of the Ising model

↑ **Parent:** [Ising model](#ising-model)

TODO what it means to solve an Ising model in general?

[https://stanford.edu/~jeffjar/statmech/lec4.html](https://stanford.edu/~jeffjar/statmech/lec4.html) gives some good notions:
- $<\sigma_i>$ is the [expectation value](mathematics.md#expectation-value) of the value. It is therefore a number between -1.0 an and 1.0, -1.0 means everything is always down, 0.0 means half up half down, and 1.0 means all up
- $<\sigma_i \sigma_j>$: correlation between neighboring states. TODO.

###### 1D Ising model

↑ **Parent:** [Ising model](#ising-model)

Bibliography:
- [https://stanford.edu/~jeffjar/statmech/intro4.html](https://stanford.edu/~jeffjar/statmech/intro4.html)
- [https://stanford.edu/~jeffjar/statmech/lec4.html](https://stanford.edu/~jeffjar/statmech/lec4.html)

###### 2D Ising model

↑ **Parent:** [Ising model](#ising-model)

###### 3D Ising model

↑ **Parent:** [Ising model](#ising-model)

##### Magnetic dipole

↑ **Parent:** [Magnet](#magnet)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Magnetic_dipole)

A tiny idealized magnet! It is a very good model if you have a small strong magnet interacting with objects that are far away, notably other [magnetic dipoles](#magnetic-dipole) or a constant magnetic field.

The cool thing about this model is that we have simple explicit formulas for the [magnetic field](electromagnetism.md#magnetic-field) it produces, and for how this little magnet is affected by a magnetic field or by another [magnetic dipole](#magnetic-dipole).

This is the perfect model for [electron](standard-model.md#electron) [spin](relativistic-quantum-mechanics.md#spin-physics), but it can also be representative of macroscopic systems in the right circumstances.

The intuition for the name is likely that "dipole" means "both poles are on the same spot".

<a id="image-different-macroscopic-magnets-can-be-approximated-by-a-magnetic-dipole-when-shrunk-seen-from-far-away"></a>
![](https://upload.wikimedia.org/wikipedia/commons/thumb/7/76/VFPt_dipoles_magnetic.svg/500px-VFPt_dipoles_magnetic.svg.png)

**[Figure 22](#image-different-macroscopic-magnets-can-be-approximated-by-a-magnetic-dipole-when-shrunk-seen-from-far-away). Different macroscopic magnets can be approximated by a magnetic dipole when shrunk seen from far away**. [Source](https://commons.wikimedia.org/wiki/File:VFPt_dipoles_magnetic.svg.png).

###### Magnetic dipole moment

↑ **Parent:** [Magnetic dipole](#magnetic-dipole)

###### Interaction between a magnetic dipole and a magnetic field

↑ **Parent:** [Magnetic dipole](#magnetic-dipole)

###### Interaction between a magnetic dipole and a homogenous magnetic field

↑ **Parent:** [Interaction between a magnetic dipole and a magnetic field](#interaction-between-a-magnetic-dipole-and-a-magnetic-field)

Produces [torque](mechanics.md#torque) but no [force](mechanics.md#force). For example:

###### Magnetic dipole in an inhomogenous magnetic field

↑ **Parent:** [Interaction between a magnetic dipole and a magnetic field](#interaction-between-a-magnetic-dipole-and-a-magnetic-field)

- [https://physics.stackexchange.com/questions/218953/what-makes-the-magnetic-field-inhomogeneous-in-the-stern-gerlach-experiment](https://physics.stackexchange.com/questions/218953/what-makes-the-magnetic-field-inhomogeneous-in-the-stern-gerlach-experiment)

##### Compass

↑ **Parent:** [Magnet](#magnet)

###### Water compass

↑ **Parent:** [Compass](#compass)

We define a "water compass" as a compass made by placing a magnet floating on a water surface to reduce friction and allow it to align with the [Earth's magnetic field](astronomy.md#earth-s-magnetic-field). This is a common children's scientific experiment.

<a id="video-bar-magnet-aligns-with-earth-s-magnetic-axis-by-kclasssciencechannel"></a>
**[Video 25](#video-bar-magnet-aligns-with-earth-s-magnetic-axis-by-kclasssciencechannel). Bar magnet aligns with Earth's magnetic axis by KClassScienceChannel.** [Source](https://www.youtube.com/watch?v=5FQCEJ8XQYc).

##### Superconducting magnet

↑ **Parent:** [Magnet](#magnet)  
🏷️ **Tags:** [Applications of superconductivity](#applications-of-superconductivity), [Superconductivity](#superconductivity)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Superconducting_magnet)

Applications: produce high [magnetic fields](electromagnetism.md#magnetic-field) for
- [magnetic resonance imaging](particle-physics.md#magnetic-resonance-imaging), the most important commercial application as of the early 2020s
- more researchy applications as of the early 2020s:
  - [magnetic confinement fusion](technology.md#magnetic-confinement-fusion)
  - [particle accelerators](particle-physics.md#particle-accelerator)
As of the early 2020s, [superconducting magnets](#superconducting-magnet) predominantly use low temperature superconductors [Nb-Ti](chemistry.md#niobium-titanium) and [Nb-Sn](chemistry.md#niobium-tin), see also [most important superconductor materials](#most-important-superconductor-material), but there were efforts underway to create practical [high-temperature superconductor](#high-temperature-superconductivity)-based magnets as well: [Section "High temperature superconductor superconducting magnet"](#high-temperature-superconductor-superconducting-magnet).

Wikipedia has done well for once:

> The current to the coil windings is provided by a high current, very low voltage [DC power supply](electronics.md#direct-current-source), since in steady state the only voltage across the magnet is due to the resistance of the feeder wires. Any change to the current through the magnet must be done very slowly, first because electrically the magnet is a large inductor and an abrupt current change will result in a large voltage spike across the windings, and more importantly because fast changes in current can cause eddy currents and mechanical stresses in the windings that can precipitate a quench (see below). So the power supply is usually [microprocessor](computer-hardware.md#microprocessor)-controlled, programmed to accomplish current changes gradually, in gentle ramps. It usually takes several minutes to energize or de-energize a laboratory-sized magnet.

<a id="video-superconductivity-magnetic-separation-by-university-of-cambridge"></a>
**[Video 26](#video-superconductivity-magnetic-separation-by-university-of-cambridge). Superconductivity: magnetic separation by University of Cambridge.** [Source](https://www.youtube.com/watch?v=pKnIUYhEmnw).

###### Superconducting magnet vendor

↑ **Parent:** [Superconducting magnet](#superconducting-magnet)

###### Oxford Instruments

↑ **Parent:** [Superconducting magnet vendor](#superconducting-magnet-vendor)  
🏷️ **Tags:** [University of Oxford spinout company](university-of-oxford.md#university-of-oxford-spinout-company)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Oxford_Instruments)

They are pioneers in making [superconducting magnets](#superconducting-magnet), [physicist](physicist.md) from the university taking obsolete equipment from the uni to his garage and making a startup kind of situation. This was particularly notable for this time and place.

They became a major supplier for [magnetic resonance imaging](particle-physics.md#magnetic-resonance-imaging) applications.

###### High temperature superconductor superconducting magnet

↑ **Parent:** [Superconducting magnet](#superconducting-magnet)

- [https://home.cern/news/series/superconductors/20-tesla-and-beyond-high-temperature-superconductors](https://home.cern/news/series/superconductors/20-tesla-and-beyond-high-temperature-superconductors)
- [https://www.tokamakenergy.co.uk/magnets/](https://www.tokamakenergy.co.uk/magnets/)
- [https://www.bnl.gov/magnets/hts-magnet-program.php](https://www.bnl.gov/magnets/hts-magnet-program.php)

#### Optical material property

↑ **Parent:** [Material property](#material-property)

##### Black-body radiation

↑ **Parent:** [Optical material property](#optical-material-property)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Black-body_radiation)

<h6 id="planck-s-law">Planck's law</h6>

↑ **Parent:** [Black-body radiation](#black-body-radiation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Planck's_law)

Used to explain the [black-body radiation experiment](#black-body-radiation-experiment).

Published as: [On the Theory of the Energy Distribution Law of the Normal Spectrum by Max Planck (1900)](physicist.md#on-the-law-of-distribution-of-energy-in-the-normal-spectrum).

[The Quantum Story by Jim Baggott (2011)](quantum-mechanics.md#the-quantum-story-by-jim-baggott-2011) page 9 mentions that Planck apparently immediately recognized that [Planck constant](quantum-mechanics.md#planck-constant) was a new fundamental [physical constant](system-of-units.md#physical-constant), and could have potential applications in the definition of the [system of units](system-of-units.md) (TODO where was that published):

> [Planck](physicist.md#max-planck) wrote that the constants offered: 'the possibility of establishing units of length, mass, time and temperature which are independent of speciﬁc bodies or materials and which necessarily maintain their meaning for all time and for all civilizations, even those which are extraterrestrial and nonhuman, constants which therefore can be called "fundamental physical units of measurement".'

This was a visionary insight, and was finally realized in the [2019 redefinition of the SI base units](system-of-units.md#2019-redefinition-of-the-si-base-units).

TODO how can it be derived from theoretical principles alone? There is one derivation at; [https://en.wikipedia.org/wiki/Planck%27s_law#Derivation](https://en.wikipedia.org/wiki/Planck%27s_law#Derivation) but it does not seem to mention the [Schrödinger equation](quantum-mechanics.md#schrodinger-equation) at all.
- [https://physics.stackexchange.com/questions/22075/deriving-plancks-radiation-law-from-microscopic-considerations](https://physics.stackexchange.com/questions/22075/deriving-plancks-radiation-law-from-microscopic-considerations)
- [https://physics.stackexchange.com/questions/4816/is-there-a-fully-quantum-field-theoretic-treatise-of-plancks-law-for-black-body](https://physics.stackexchange.com/questions/4816/is-there-a-fully-quantum-field-theoretic-treatise-of-plancks-law-for-black-body)

<a id="video-quantum-mechanics-2-photons-by-viascience-2012"></a>
**[Video 27](#video-quantum-mechanics-2-photons-by-viascience-2012). Quantum Mechanics 2 - Photons by ViaScience (2012)** [Source](https://youtube.com/watch?v=KabPQLIXLw4). Contains a good explanation of how [discretization](calculus.md#discretization) + [energy](physics.md#energy) increases with frequency explains the [black-body radiation experiment](#black-body-radiation-experiment) curve: you need more and more energy for small wavelengths, each time higher above the average energy available.

###### Wien approximation

↑ **Parent:** [Planck's law](#planck-s-law)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Wien_approximation)

###### Rayleigh-Jeans law

↑ **Parent:** [Planck's law](#planck-s-law)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Rayleigh-Jeans_law)

Derived [from classical first principles](science.md#from-first-principles), matches [Planck's law](#planck-s-law) for low frequencies, but diverges at higher frequencies.

###### Black-body radiation experiment

↑ **Parent:** [Black-body radiation](#black-body-radiation)  
🏷️ **Tags:** [Quantum mechanics experiment](quantum-mechanics.md#quantum-mechanics-experiment)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Black-body_radiation_experiment)

- [The Quantum Story by Jim Baggott (2011)](quantum-mechanics.md#the-quantum-story-by-jim-baggott-2011) page 10 mentions:> Early examples of such cavities included rather expensive closed cylinders made from porcelain and platinum.

  and the footnote comments:> The study of cavity radiation was not just about establishing theoretical principles, however. It was also of interest to the German Bureau of Standards as a reference for rating electric lamps.
- 1859-60 Gustav Kirchhoff demonstrated that the ratio of emitted to absorbed energy depends only on the frequency of the radiation and the temperature inside the cavity
- 1896 [Wien approximation](#wien-approximation) seems to explain existing curves well
- 1900 expriments by Otto Lummer and Ernst Pringsheim show [Wien approximation](#wien-approximation) is bad for lower frequencies
- 1900-10-07 Heinrich Rubens visits Planck in Planck's villa in the Berlin suburb of Grünewald and informs him about new experimental he and Ferdinand Kurlbaum obtained, still showing that [Wien approximation](#wien-approximation) is bad
- 1900 [Planck's law](#planck-s-law) matches Lummer and Pringsheim's experiments well. Planck forced to make the "desperate" postulate that energy is exchanged in quantized lumps. Not clear that light itself is quantized however, he thinks it might be something to do with allowed vibration modes of the atoms of the cavity rather.
- 1900 [Rayleigh-Jeans law](#rayleigh-jeans-law) derived [from classical first principles](science.md#from-first-principles) matches [Planck's law](#planck-s-law) for low frequencies, but diverges at higher frequencies.

<a id="video-black-body-radiation-experiment-by-sciencesolution-2008"></a>
**[Video 28](#video-black-body-radiation-experiment-by-sciencesolution-2008). Black-body Radiation Experiment by sciencesolution (2008)** [Source](https://youtube.com/watch?v=HnBZf1RfB-w). A modern version of the experiment with a PASCO scientific EX-9920 setup.

###### Ultraviolet catastrophe

↑ **Parent:** [Black-body radiation](#black-body-radiation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Ultraviolet_catastrophe)

<a id="video-what-is-the-ultraviolet-catastrophe-by-physics-explained-2020"></a>
**[Video 29](#video-what-is-the-ultraviolet-catastrophe-by-physics-explained-2020). What is the Ultraviolet Catastrophe? by Physics Explained (2020)** [Source](https://www.youtube.com/watch?v=rCfPQLVzus4).

##### Transparency (electromagnetic radiation)

↑ **Parent:** [Optical material property](#optical-material-property)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Transparency_(electromagnetic_radiation))

[https://physics.stackexchange.com/questions/300551/how-can-wifi-penetrate-through-walls-when-visible-light-cant](https://physics.stackexchange.com/questions/300551/how-can-wifi-penetrate-through-walls-when-visible-light-cant)

###### Absorption (electromagnetic radiation)

↑ **Parent:** [Transparency (electromagnetic radiation)](#transparency-electromagnetic-radiation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Absorption_(electromagnetic_radiation))

#### Piezoelectricity

↑ **Parent:** [Material property](#material-property)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Piezoelectricity)

##### Piezoelectric actuator

↑ **Parent:** [Piezoelectricity](#piezoelectricity)  
🏷️ **Tags:** [Actuator](robotics.md#actuator)

###### Piezoelectric motor

↑ **Parent:** [Piezoelectric actuator](#piezoelectric-actuator)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Piezoelectric_motor)

##### Piezo ignition

↑ **Parent:** [Piezoelectricity](#piezoelectricity)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Piezo_ignition)

#### Photoluminescence

↑ **Parent:** [Material property](#material-property)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Photoluminescence)

##### Fluorescence

↑ **Parent:** [Photoluminescence](#photoluminescence)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Fluorescence)

###### Fluorometer

↑ **Parent:** [Fluorescence](#fluorescence)  
🏷️ **Tags:** [Photonics equipment](photon.md#photonics-equipment)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Fluorometer)

<a id="video-time-correlated-single-photon-counting-tcspc-with-the-fluorolog-fluorimeter-by-yale-cbic-2011"></a>
**[Video 30](#video-time-correlated-single-photon-counting-tcspc-with-the-fluorolog-fluorimeter-by-yale-cbic-2011). Time-Correlated Single Photon Counting (TCSPC) with the Fluorolog Fluorimeter by Yale CBIC (2011)** [Source](https://www.youtube.com/watch?v=BbqsNDfCPQU).

###### Phosphorescence

↑ **Parent:** [Fluorescence](#fluorescence)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Phosphorescence)

#### Specific heat capacity

↑ **Parent:** [Material property](#material-property)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Specific_heat_capacity)

##### Einstein solid

↑ **Parent:** [Specific heat capacity](#specific-heat-capacity)  
🏷️ **Tags:** [Quantum mechanics experiment](quantum-mechanics.md#quantum-mechanics-experiment)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Einstein_solid)

One important [quantum mechanics experiment](quantum-mechanics.md#quantum-mechanics-experiment), which using quantum effects explain the dependency of [specific heat capacity](#specific-heat-capacity) on temperature, an effect which is not present in the [Dulong-Petit law](#dulong-petit-law).

This is the [solid-state](#solid-state-physics) analogue to the [black-body radiation](#black-body-radiation) problem. It is also therefore a [quantum mechanics](quantum-mechanics.md)-specific phenomenon.

###### Dulong-Petit law

↑ **Parent:** [Einstein solid](#einstein-solid)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Dulong-Petit_law)

Observation that all solids appear to have the same constant heat capacity per [mole](chemistry.md#mole-unit).

It can be seen as the limit case of an [Einstein solid](#einstein-solid) at high temperatures. At lower temperatures, the heat capacity depends on temperature.

##### Debye model

↑ **Parent:** [Specific heat capacity](#specific-heat-capacity)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Debye_model)

Wikipedia mentions that it is completely analogous to [Planck's law](#planck-s-law).

#### Viscosity

↑ **Parent:** [Material property](#material-property)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Viscosity)

##### Pitch drop experiment

↑ **Parent:** [Viscosity](#viscosity)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Pitch_drop_experiment)

## Laser

↑ **Parent:** [Condensed matter physics](condensed-matter-physics.md)  
🏷️ **Tags:** [Light source](photon.md#light-source)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Laser)

What makes lasers so special: [Lasers vs other light sources](#lasers-vs-other-light-sources).

<a id="video-how-lasers-work-by-scientized-2017"></a>
**[Video 31](#video-how-lasers-work-by-scientized-2017). How Lasers Work by Scientized (2017)** [Source](https://www.youtube.com/watch?v=_JOchLyNO_w). An extremely good overview of how lasers work. Clearly explains the electron/photon exchange processes involved, notably [spontaneous emission](relativistic-quantum-mechanics.md#spontaneous-emission).

Talks about the importance of the metastable state to achieve [population inversion](#population-inversion).

Also briefly explains the imperfections that lead to the slightly imperfect non punctual spectrum seen in a real laser.


- [https://youtu.be/_JOchLyNO_w?t=188](https://youtu.be/_JOchLyNO_w?t=188) says [LED](electronics.md#light-emitting-diode) is "also monochromatic", but that is not strictly true, it has way way larger frequency band than a laser. Only narrower compared to other sources such as [incandescent light bulbs](https://ourbigbook.com/go/topic/incandescent-light-bulbs).
- [https://youtu.be/_JOchLyNO_w?t=517](https://youtu.be/_JOchLyNO_w?t=517) [stimulated emission](relativistic-quantum-mechanics.md#stimulated-emission). This is the key to laser formation as it produces coherent photons.
- [https://youtu.be/_JOchLyNO_w?t=581](https://youtu.be/_JOchLyNO_w?t=581) [spontaneous emission](relativistic-quantum-mechanics.md#spontaneous-emission) happens too fast (100 ns), which is not enough time for [stimulated emission](relativistic-quantum-mechanics.md#stimulated-emission) to happen. [Metastable electrons](quantum-mechanics.md#metastable-electron) to the rescue.
- [https://youtu.be/_JOchLyNO_w?t=832](https://youtu.be/_JOchLyNO_w?t=832) the parallel mirrors select perpendicular photons preferentially

---

<a id="video-laser-fundamentals-i-by-shaoul-ezekiel"></a>
**[Video 32](#video-laser-fundamentals-i-by-shaoul-ezekiel). Laser Fundamentals I by Shaoul Ezekiel.** [Source](https://www.youtube.com/watch?v=saVE7pMhaxk). 2008, [MIT](university.md#massachusetts-institute-of-technology). Many more great videos in this series.

Bibliography:
- [https://phys.libretexts.org/Courses/University_of_California_Davis/UCD%3A_Physics_9HE_-_Modern_Physics/06%3A_Emission_and_Absorption_of_Photons/6.3%3A_Lasers](https://phys.libretexts.org/Courses/University_of_California_Davis/UCD%3A_Physics_9HE_-_Modern_Physics/06%3A_Emission_and_Absorption_of_Photons/6.3%3A_Lasers) His [Rate My Professors](website.md#rate-my-professors) is amazing: [https://www.ratemyprofessors.com/ShowRatings.jsp?tid=1783467](https://www.ratemyprofessors.com/ShowRatings.jsp?tid=1783467)

### History of the laser

↑ **Parent:** [Laser](#laser)  
🏷️ **Tags:** [History of condensed matter physics](#history-of-condensed-matter-physics)

#### The History of the Laser by Mario Bertolotti

↑ **Parent:** [History of the laser](#history-of-the-laser)

On [Internet Archive Open Library](website.md#internet-archive-open-library): [https://archive.org/details/historyoflaser0000bert_d2f3](https://archive.org/details/historyoflaser0000bert_d2f3)

### Laser spectrum

↑ **Parent:** [Laser](#laser)

<a id="video-spectrum-of-laser-light-by-shaoul-ezekiel"></a>
**[Video 33](#video-spectrum-of-laser-light-by-shaoul-ezekiel). Spectrum of laser light by Shaoul Ezekiel.** [Source](https://www.youtube.com/watch?v=--Zi_cn4kPE). 2008, [MIT](university.md#massachusetts-institute-of-technology).

#### Laser linewidth

↑ **Parent:** [Laser spectrum](#laser-spectrum)  
🏷️ **Tags:** [Spectral coherence](photon.md#spectral-coherence)

<a id="video-laser-linewidth-measurement-and-explanation-by-your-favourite-ta"></a>
**[Video 34](#video-laser-linewidth-measurement-and-explanation-by-your-favourite-ta). Laser linewidth - measurement and explanation by Your Favourite TA.** [Source](https://www.youtube.com/watch?v=efSk-l-7aTQ).

#### Laser gain curve

↑ **Parent:** [Laser spectrum](#laser-spectrum)

TODO why it exists:
- [https://www.reddit.com/r/askscience/comments/6y1rac/why_is_there_a_laser_gain_curve/](https://www.reddit.com/r/askscience/comments/6y1rac/why_is_there_a_laser_gain_curve/)
- [https://physics.stackexchange.com/questions/355223/laser-gain-curve](https://physics.stackexchange.com/questions/355223/laser-gain-curve)

### Lasers vs other light sources

↑ **Parent:** [Laser](#laser)

The key advantages of lasers over other [light sources](photon.md#light-source) are:
- [lasers emit a narrow spectrum](#lasers-emit-a-narrow-spectrum)
- it can be efficient collimated, while still emitting a lot of output power: [Section "Why can't you collimate incoherent light as well as a laser?"](#why-can-t-you-collimate-incoherent-light-as-well-as-a-laser)
- can be phase and polarization coherent, though it is not always the case? TODO.

One cool thing about [lasers](#laser) is that they rely on one specific atomic energy level transition to produce light. This is why they are able to to be so monchromatic. Compare this to:
- incandescent bulbs: wide [black-body radiation](#black-body-radiation) spectrum
- [LED](electronics.md#light-emitting-diode): has a wider spectrum fundamentally related to an energy distribution, related: [Why aren't LEDs monochromatic](electronics.md#why-aren-t-leds-monochromatic)
- TODO think a bit about [fluorescent lamps](photon.md#fluorescent-lamp). These also rely on atomic energy transitions, but many of them are present at once, which makes the spectrum very noisy. But would individual lines be very narrow?
As such, lasers manage to largely overcome "temperature distribution-like" effects that create wider wave spectrum

<a id="video-crazy-difference-between-5w-laser-and-5w-led-by-brainiac75"></a>
**[Video 35](#video-crazy-difference-between-5w-laser-and-5w-led-by-brainiac75). Crazy difference between 5W laser and 5W LED by Brainiac75.** [Source](https://www.youtube.com/watch?v=vUwP7SY0Ajs). Baseic but good. Uses a [laser](#laser) [photometer](photon.md#photometer).

#### Lasers emit a narrow spectrum

↑ **Parent:** [Lasers vs other light sources](#lasers-vs-other-light-sources)  
🏷️ **Tags:** [Laser spectrum](#laser-spectrum)

It emits a very narrow range of frequencies (small linewidth), which for many purposes can be considered a single frequency.

It does however have a small range of frequencies. The smaller the range, the better the laser quality.

##### Laser spectrum vs LED spectrum

↑ **Parent:** [Lasers emit a narrow spectrum](#lasers-emit-a-narrow-spectrum)

[https://electronics.stackexchange.com/questions/477264/spectrum-of-leds](https://electronics.stackexchange.com/questions/477264/spectrum-of-leds) claims cheap [LEDs](electronics.md#light-emitting-diode) have 20 nm width at 50% from peak, and cheap lasers can be 1 nm or much less

<h4 id="why-can-t-you-collimate-incoherent-light-as-well-as-a-laser">Why can't you collimate incoherent light as well as a laser?</h4>

↑ **Parent:** [Lasers vs other light sources](#lasers-vs-other-light-sources)

[https://physics.stackexchange.com/questions/252393/why-cant-incoherent-light-be-collimated-as-well-as-laser-light-e-g-in-a-laser](https://physics.stackexchange.com/questions/252393/why-cant-incoherent-light-be-collimated-as-well-as-laser-light-e-g-in-a-laser)

You could put an [LED](electronics.md#light-emitting-diode) in a cavity with a thin long hole but then, most rays, which are not aligned with the hole, will just bounce inside forever producing heat.

So you would have a very hot device, and very little efficiency on the light output. This heat might also behave like a [black-body radiation](#black-body-radiation) source, so you would not have a single frequency.

The beauty of lasers is the laser cavity (two parallel mirrors around the medium) selects parallel motion preferentially, see e.g.: [https://youtu.be/_JOchLyNO_w?t=832](https://youtu.be/_JOchLyNO_w?t=832) from [Video 31. "How Lasers Work by Scientized (2017)"](#video-how-lasers-work-by-scientized-2017)

### Type of laser

↑ **Parent:** [Laser](#laser)

#### Maser

↑ **Parent:** [Type of laser](#type-of-laser)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Maser)

<a id="video-principles-of-the-optical-maser-by-bell-labs"></a>
**[Video 36](#video-principles-of-the-optical-maser-by-bell-labs). Principles of the Optical Maser by Bell Labs.** [Source](https://www.youtube.com/watch?v=vuORqMb481k). Date: 1963.

#### Fiber laser

↑ **Parent:** [Type of laser](#type-of-laser)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Fiber_laser)

Closely related to [optical amplifiers](photon.md#optical-amplifier).

#### Gas laser

↑ **Parent:** [Type of laser](#type-of-laser)  
🏷️ **Tags:** [Gas](#gas)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Gas_laser)

#### Laser diode

↑ **Parent:** [Type of laser](#type-of-laser)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Laser_diode)

This is by far the most important type of [laser](#laser) commercially, as it can be made relatively cheaply, and it doesn't break easily as it ends up being a single [crystal](#crystal).

Compare them for example to the earlier [gas lasers](#gas-laser).

This is the type of laser that you would get in a simple [laser pointer](#laser-pointer).

But the real mega aplications are:
- [fiber-optic communication](photon.md#fiber-optic-communication), where [laser diodes](#laser-diode) are one of the most commonly used methods to generate the light that goes in the fiber. This makes [laser diodes](#laser-diode) one of the most important inventions of the 20th centure without doubt.
- [optical storage](computer-hardware.md#optical-storage). But as of the 2020s its usefulness was much diminished by a combination of [solid-state storage](computer-hardware.md#solid-state-storage) + faster [Internet](computer.md#internet) due largely to [fiber-optic communication](photon.md#fiber-optic-communication). So it is partly a matter of [laser diodes](#laser-diode) beating [laser diodes](#laser-diode)!

##### Laser pointer

↑ **Parent:** [Laser diode](#laser-diode)

<a id="video-laser-pointer-by-shahzadi"></a>
**[Video 37](#video-laser-pointer-by-shahzadi). Laser pointer by shahzadi.** [Source](https://www.youtube.com/watch?v=-SMhy4KZldA).

#### Three-level laser

↑ **Parent:** [Type of laser](#type-of-laser)

The type of laser described at: [Video 31. "How Lasers Work by Scientized (2017)"](#video-how-lasers-work-by-scientized-2017), notably [https://youtu.be/_JOchLyNO_w?t=581](https://youtu.be/_JOchLyNO_w?t=581). Mentioned at: [https://youtu.be/_JOchLyNO_w?t=759](https://youtu.be/_JOchLyNO_w?t=759) That point also mentions that 4-level lasers also exist and are more efficient. TODO dominance? Alternatives?

<a id="video-three-level-laser-system-by-dr-nissar-ahmad-2021"></a>
**[Video 38](#video-three-level-laser-system-by-dr-nissar-ahmad-2021). Three-level laser system by Dr. Nissar Ahmad (2021)** [Source](https://www.youtube.com/watch?v=6c89tsJHuWc).

Bibliography:
- [https://www.britannica.com/technology/three-level-laser](https://www.britannica.com/technology/three-level-laser)

#### Four-level laser

↑ **Parent:** [Type of laser](#type-of-laser)

### Are lasers polarized

↑ **Parent:** [Laser](#laser)

[https://physics.stackexchange.com/questions/183216/is-the-output-of-a-laser-pointer-polarized-or-not](https://physics.stackexchange.com/questions/183216/is-the-output-of-a-laser-pointer-polarized-or-not)

### Optical tweezers

↑ **Parent:** [Laser](#laser)  
🏷️ **Tags:** [2018 Nobel Prize in Physics](nobel-prize.md#2018-nobel-prize-in-physics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Optical_tweezers)

Sample usages:
- [quantum computing](quantum-computing.md) startup [Atom Computing](quantum-computing.md#atom-computing) uses them to hold dozens of individual atoms midair separately, to later entangle their nuclei

<a id="video-optical-tweezers-experiment-by-alexis-bishop"></a>
**[Video 39](#video-optical-tweezers-experiment-by-alexis-bishop). Optical Tweezers Experiment by Alexis Bishop.** [Source](https://www.youtube.com/watch?v=3SJiKr8LbP8). Setup on a [optical table](photon.md#optical-table). He drags a 1 micron ball of polystyrene immersed in water around with the laser. You look through the [microscope](microscopy.md) and move the stage. [Brownian motion](chemistry.md#brownian-motion) is also clearly visible when the laster is not holding the ball.

#### Laser cooling

↑ **Parent:** [Optical tweezers](#optical-tweezers)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Laser_cooling)

### Population inversion

↑ **Parent:** [Laser](#laser)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Population_inversion)

### Pulsed laser

↑ **Parent:** [Laser](#laser)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Pulsed_laser)

### Laser vendor

↑ **Parent:** [Laser](#laser)

#### Coherent, Inc.

↑ **Parent:** [Laser vendor](#laser-vendor)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Coherent,_Inc.)

## Quasiparticle

↑ **Parent:** [Condensed matter physics](condensed-matter-physics.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Quasiparticle)

The opposite of [elementary particle](standard-model.md#elementary-particle).

### Quasiparticles vs elementary particles

↑ **Parent:** [Quasiparticle](#quasiparticle)

As a phisicist once amazingly put it in a talk Ciro watched:

> It all depends on how much energy you have to probe nature with. Previously, we thought [protons](standard-model.md#proton) were [elementary particles](standard-model.md#elementary-particle). But then we used more energy and found that they aren't.
> 
> If some [alien](taxonomy.md#extraterrestrial-life) race had even less energy, they might not know about [electrons](standard-model.md#electron) at all, and could think that [anyons](relativistic-quantum-mechanics.md#anyon) are actually elementary.
> 
> Being an "elementary particle" is always a possibly temporary label.

Bibliography:
- [https://physics.stackexchange.com/questions/21954/are-elementary-particles-actually-more-elementary-than-quasiparticles](https://physics.stackexchange.com/questions/21954/are-elementary-particles-actually-more-elementary-than-quasiparticles)

## History of condensed matter physics

↑ **Parent:** [Condensed matter physics](condensed-matter-physics.md)  
🏷️ **Tags:** [History of science](science.md#history-of-science)

Bibliography:
- [https://www.reddit.com/r/AskPhysics/comments/acupnt/any_book_suggestions_about_history_of_condensed/](https://www.reddit.com/r/AskPhysics/comments/acupnt/any_book_suggestions_about_history_of_condensed/)
- [https://hsm.stackexchange.com/questions/14262/are-there-any-good-books-on-the-history-of-condensed-matter](https://hsm.stackexchange.com/questions/14262/are-there-any-good-books-on-the-history-of-condensed-matter)

## Condensed matter Physics bibliography

↑ **Parent:** [Condensed matter physics](condensed-matter-physics.md)

- When [condensed matter physics](condensed-matter-physics.md) became king by Joseph D. Martin (2019): [https://physicstoday.scitation.org/doi/10.1063/PT.3.4110](https://physicstoday.scitation.org/doi/10.1063/PT.3.4110)
- [https://www.youtube.com/watch?v=RImqF8z91fU&list=PLtTPtV8SRcxi91n9Mni2xcQX4KhjX91xp](https://www.youtube.com/watch?v=RImqF8z91fU&list=PLtTPtV8SRcxi91n9Mni2xcQX4KhjX91xp) Solid State Physics" course by Sergey Frolov taught at the University of Pittsburgh in the Fall 2015 semester

### Condensed matter university course

↑ **Parent:** [Condensed matter Physics bibliography](#condensed-matter-physics-bibliography)

#### Theories of Quantum Matter by Austen Lamacraft

↑ **Parent:** [Condensed matter university course](#condensed-matter-university-course)

[This section is present in another page, follow this link to view it.](theories-of-quantum-matter-by-austen-lamacraft.md)

#### Course: Quantum Many-Body Physics in Condensed Matter by Luis Gregorio Dias (2020)

↑ **Parent:** [Condensed matter university course](#condensed-matter-university-course)

[https://www.youtube.com/playlist?list=PL6FyrZIBwD8LMWizZW1FUN2dS_l44yuiy](https://www.youtube.com/playlist?list=PL6FyrZIBwD8LMWizZW1FUN2dS_l44yuiy)

Affiliation: [University of São Paulo](university.md#university-of-sao-paulo).

## ↑ Ancestors (4)

1. [Physics](physics.md)
2. [Natural science](science.md#natural-science)
3. [Science](science.md)
4. [Ciro Santilli's Homepage](README.md)

## ← Incoming links (7)

- [Atomic, Molecular and Optical Physics](#atomic-molecular-and-optical-physics)
- [Condensed matter physics](condensed-matter-physics.md)
- [Condensed matter Physics bibliography](#condensed-matter-physics-bibliography)
- [Physics](physics.md)
- [Lecture 1](quantum-field-theory.md#quantum-field-theory-lecture-by-tobias-osborne-2017/lecture-1)
- [Second quantization](quantum-field-theory.md#second-quantization)
- [Why you should give money to Ciro Santilli](sponsor.md#why-you-should-give-money-to-ciro-santilli)
