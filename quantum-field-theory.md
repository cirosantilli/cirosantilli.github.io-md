# Quantum field theory

↑ **Parent:** [Relativistic quantum mechanics](relativistic-quantum-mechanics.md)  
🏷️ **Tags:** [Ciro Santilli's fetishes](ciro-santilli-s-psychology-and-physiology.md#ciro-santilli-s-fetishes)

Theoretical framework on which quantum field theories are based, theories based on framework include:
- [quantum electrodynamics](#quantum-electrodynamics)
- [quantum chromodynamics](#quantum-chromodynamics)
so basically the entire [Standard Model](standard-model.md)

The basic idea is that there is a field for each particle particle type.

E.g. in QED, one for the [electron](standard-model.md#electron) and one for the [photon](photon.md): [https://physics.stackexchange.com/questions/166709/are-electron-fields-and-photon-fields-part-of-the-same-field-in-qed](https://physics.stackexchange.com/questions/166709/are-electron-fields-and-photon-fields-part-of-the-same-field-in-qed).

And then those fields interact with some [Lagrangian](mechanics.md#lagrangian).

One way to look at QFT is to split it into two parts:
- deriving the Lagrangians of the [Standard Model](standard-model.md): [S](linguistics.md#s). This is the easier part, since the lagrangians themselves can be understood with not very advanced mathematics, and derived beautifully from symmetry constraints
- the qantization of fields. This is the hard part [Ciro Santilli](ciro-santilli.md) is unable to understand, TODO [mathematical formulation of quantum field theory](#mathematical-formulation-of-quantum-field-theory).
Then interwined with those two is the part "OK, how to solve the equations, if they are solvable at all", which is an open problem: [Yang-Mills existence and mass gap](#yang-mills-existence-and-mass-gap).

There appear to be two main equivalent formulations of quantum field theory:
- [second quantization](#second-quantization)
- [path integral formulation](#path-integral-formulation)

<a id="video-quantum-field-theory-visualized-by-scienceclic-english-2020"></a>
**[Video 1](#video-quantum-field-theory-visualized-by-scienceclic-english-2020). Quantum Field Theory visualized by ScienceClic English (2020)** [Source](https://www.youtube.com/watch?v=MmG2ah5Df4g). Gives one piece of possibly OK intuition: quantum theories kind of model all possible evolutions of the system at the same time, but with different probabilities. QFT is no different in that aspect.
- [https://youtu.be/MmG2ah5Df4g?t=209](https://youtu.be/MmG2ah5Df4g?t=209) describes how the [spin number of a field](relativistic-quantum-mechanics.md#spin-number-of-a-field) is directly related to how much you have to rotate an element to reach the original position
- [https://youtu.be/MmG2ah5Df4g?t=480](https://youtu.be/MmG2ah5Df4g?t=480) explains which particles are modelled by which spin number

---

<a id="video-quantum-fields-the-real-building-blocks-of-the-universe-by-david-tong-2017"></a>
**[Video 2](#video-quantum-fields-the-real-building-blocks-of-the-universe-by-david-tong-2017). Quantum Fields: The Real Building Blocks of the Universe by David Tong (2017)** [Source](https://youtu.be/zNVQfWC_evg). Boring, does not give anything except the usual blabla everyone knows from Googling:
- [https://youtu.be/zNVQfWC_evg?t=1335](https://youtu.be/zNVQfWC_evg?t=1335) shows [https://www.youtube.com/watch?v=9TJe1Pr5c9Q](https://www.youtube.com/watch?v=9TJe1Pr5c9Q) from [quantum field theory simulations](#quantum-field-theory-simulations)
- [https://youtu.be/zNVQfWC_evg?t=1522](https://youtu.be/zNVQfWC_evg?t=1522) alludes to the [Birch and Swinnerton-Dyer conjecture](algebra.md#birch-and-swinnerton-dyer-conjecture)

---

<a id="video-quantum-field-theory-what-is-a-particle-by-physics-explained-2021"></a>
**[Video 3](#video-quantum-field-theory-what-is-a-particle-by-physics-explained-2021). Quantum Field Theory: What is a particle? by Physics Explained (2021)** [Source](https://www.youtube.com/watch?v=QPAxzr6ihu8). Gives some high level analogies between high level principles of [non-relativistic quantum mechanics](quantum-mechanics.md#non-relativistic-quantum-mechanics) and [special relativity](relativity.md#special-relativity) in to suggest that there is a minimum quanta of a relativistic quantum field.

**Table of contents**

- [Quantum field](#quantum-field)
- [Mathematical formulation of quantum field theory](#mathematical-formulation-of-quantum-field-theory)
  - [Gauge theory](#gauge-theory)
    - [Lattice gauge theory](#lattice-gauge-theory)
    - [Gauge field](#gauge-field)
    - [Gauge symmetry](#gauge-symmetry)
  - [Fock space](#fock-space)
  - [Second quantization](#second-quantization)
    - [Canonical quantization](#canonical-quantization)
  - [Path integral formulation](#path-integral-formulation)
    - [Quantum particles take all possible paths](#quantum-particles-take-all-possible-paths)
    - [Propagator](#propagator)
    - [Infinitely many slits thought experiment](#infinitely-many-slits-thought-experiment)
  - [Renormalization](#renormalization)
    - [Mass renormalization](#mass-renormalization)
    - [Renormalization group](#renormalization-group)
    - [Cutoff energy](#cutoff-energy)
    - [Effective field theory](#effective-field-theory)
    - [Yang-Mills theory](#yang-mills-theory)
      - [Yang-Mills existence and mass gap](#yang-mills-existence-and-mass-gap)
        - [Wightman axioms](#wightman-axioms)
- [Quantum electrodynamics](#quantum-electrodynamics)
  - [Quantum electrodynamics experiment](#quantum-electrodynamics-experiment)
    - [Lamb shift](#lamb-shift)
      - [Lamb-Retherford experiment](#lamb-retherford-experiment)
    - [Electron magnetic moment](#electron-magnetic-moment)
      - [Anomalous magnetic dipole moment](#anomalous-magnetic-dipole-moment)
        - [Anomalous magnetic dipole moment of the electron](#anomalous-magnetic-dipole-moment-of-the-electron)
          - [The Magnetic Moment of the Electron by Kusch and Foley (1948)](#the-magnetic-moment-of-the-electron-by-kusch-and-foley-1948)
    - [Dirac equation vs quantum electrodynamics](#dirac-equation-vs-quantum-electrodynamics)
      - [The Dirac equation does not work for more than one electron](#the-dirac-equation-does-not-work-for-more-than-one-electron)
  - [Applications of quantum electrodynamics](#applications-of-quantum-electrodynamics)
  - [Quantum electrodynamics Lagrangian](#quantum-electrodynamics-lagrangian)
    - [Derivation of the quantum electrodynamics Lagrangian](#derivation-of-the-quantum-electrodynamics-lagrangian)
  - [What does it mean that photons are force carriers for electromagnetism?](#what-does-it-mean-that-photons-are-force-carriers-for-electromagnetism)
  - [Photon field](#photon-field)
  - [Schwinger effect](#schwinger-effect)
  - [Feynman diagram](#feynman-diagram)
    - [Feynman diagram solver](#feynman-diagram-solver)
    - [Does the exact position of vertices matter in Feynman diagrams?](#does-the-exact-position-of-vertices-matter-in-feynman-diagrams)
  - [Wheeler-Feynman absorber theory](#wheeler-feynman-absorber-theory)
  - [Cavity quantum electrodynamics](#cavity-quantum-electrodynamics)
    - [Circuit quantum electrodynamics](#circuit-quantum-electrodynamics)
  - [Positrons are electrons travelling back in time](#positrons-are-electrons-travelling-back-in-time)
  - [Quantum electrodynamics bibliography](#quantum-electrodynamics-bibliography)
    - [Quantum Theory of Radiation by Fermi (1932)](#quantum-theory-of-radiation-by-fermi-1932)
    - [Advanced quantum mechanics by Freeman Dyson (1951)](#advanced-quantum-mechanics-by-freeman-dyson-1951)
    - [Selected Papers on Quantum Electrodynamics by Julian Schwinger (1958)](#selected-papers-on-quantum-electrodynamics-by-julian-schwinger-1958)
    - [Richard Feynman Quantum Electrodynamics Lecture at University of Auckland (1979)](#richard-feynman-quantum-electrodynamics-lecture-at-university-of-auckland-1979)
      - [Quantum Mechanical View of Reality by Richard Feynman (1983)](#quantum-mechanical-view-of-reality-by-richard-feynman-1983)
    - [Quantum electrodynamics by Lifshitz et al. 2nd edition (1982)](#quantum-electrodynamics-by-lifshitz-et-al-2nd-edition-1982)
    - [Physics 253a by Sidney Coleman (1986)](#physics-253a-by-sidney-coleman-1986)
    - [QED and the men who made it: Dyson, Feynman, Schwinger, and Tomonaga by Silvan Schweber (1994)](#qed-and-the-men-who-made-it-dyson-feynman-schwinger-and-tomonaga-by-silvan-schweber-1994)
    - [Advanced quantum mechanics II by Douglas Gingrich (2004)](#advanced-quantum-mechanics-ii-by-douglas-gingrich-2004)
- [Weak interaction](#weak-interaction)
  - [Electroweak interaction](#electroweak-interaction)
  - [Parity violation](#parity-violation)
    - [Wu experiment](#wu-experiment)
    - [CP Violation](#cp-violation)
      - [CPT symmetry](#cpt-symmetry)
      - [Strong CP problem](#strong-cp-problem)
  - [Weak charge](#weak-charge)
  - [W boson](#w-boson)
  - [Z boson](#z-boson)
- [Quantum chromodynamics](#quantum-chromodynamics)
  - [Quark](#quark)
    - [Down quark](#down-quark)
    - [Up quark](#up-quark)
      - [Why do the up ad down quarks have different masses?](#why-do-the-up-ad-down-quarks-have-different-masses)
  - [Strange quark](#strange-quark)
  - [Gluon](#gluon)
    - [Glueball](#glueball)
  - [Proton decay](#proton-decay)
  - [Strong interaction](#strong-interaction)
  - [Color charge](#color-charge)
  - [Color confinement](#color-confinement)
- [Quantum field theory simulations](#quantum-field-theory-simulations)
  - [Nielsen-Ninomiya theorem](#nielsen-ninomiya-theorem)
- [Infinities in quantum field theory](#infinities-in-quantum-field-theory)
  - [Mathematical consistency of quantum field theory](#mathematical-consistency-of-quantum-field-theory)
- [Internal and spacetime symmetries](#internal-and-spacetime-symmetries)
  - [Internal symmetry](#internal-symmetry)
  - [Spacetime symmetry](#spacetime-symmetry)
- [Quantum field theory bibliography](#quantum-field-theory-bibliography)
  - [Quantum field theory lecture notes](#quantum-field-theory-lecture-notes)
    - [An Introduction to QED and QCD by Jeff Forshaw (1997)](#an-introduction-to-qed-and-qcd-by-jeff-forshaw-1997)
    - [Quantum Field Theory lecture notes by David Tong (2007)](#quantum-field-theory-lecture-notes-by-david-tong-2007)
    - [Quantum Field Theory book by Mark Srednicki (2006)](#quantum-field-theory-book-by-mark-srednicki-2006)
  - [Quantum field theory lectures](#quantum-field-theory-lectures)
    - [Relativistic Quantum Mechanics by Apoorva D Patel (2014)](#relativistic-quantum-mechanics-by-apoorva-d-patel-2014)
    - [New Revolutions in Particle Physics by Leonard Susskind (2009)](#new-revolutions-in-particle-physics-by-leonard-susskind-2009)
    - [David Tong's 2009 Quantum Field Theory lectures at the Perimeter Institute](#david-tong-s-2009-quantum-field-theory-lectures-at-the-perimeter-institute)
      - [Lecture 1](#david-tong-s-2009-quantum-field-theory-lectures-at-the-perimeter-institute/lecture-1)
    - [Quantum field theory courses by Tobias Osborne](#quantum-field-theory-courses-by-tobias-osborne)
      - [Quantum field theory lecture by Tobias Osborne (2017)](#quantum-field-theory-lecture-by-tobias-osborne-2017)
        - [Lecture 1](#quantum-field-theory-lecture-by-tobias-osborne-2017/lecture-1)
        - [Lecture 2](#quantum-field-theory-lecture-by-tobias-osborne-2017/lecture-2)
        - [Lecture 3](#quantum-field-theory-lecture-by-tobias-osborne-2017/lecture-3)
        - [Lecture 4](#quantum-field-theory-lecture-by-tobias-osborne-2017/lecture-4)
        - [Lecture 5](#quantum-field-theory-lecture-by-tobias-osborne-2017/lecture-5)
        - [Lecture 8](#quantum-field-theory-lecture-by-tobias-osborne-2017/lecture-8)
        - [Lecture 9](#quantum-field-theory-lecture-by-tobias-osborne-2017/lecture-9)
        - [Lecture 14](#quantum-field-theory-lecture-by-tobias-osborne-2017/lecture-14)
        - [Lecture 15](#quantum-field-theory-lecture-by-tobias-osborne-2017/lecture-15)
      - [Advanced quantum field theory lecture by Tobias Osborne (2017)](#advanced-quantum-field-theory-lecture-by-tobias-osborne-2017)
        - [Lecture 2](#advanced-quantum-field-theory-lecture-by-tobias-osborne-2017/lecture-2)
  - [Quantum field theory book](#quantum-field-theory-book)
    - [No-Nonsense Quantum Field Theory by Jakob Schwichtenberg (2020)](#no-nonsense-quantum-field-theory-by-jakob-schwichtenberg-2020)
    - [Quantum Field Theory for The Gifted Amateur by Tom Lancaster (2015)](#quantum-field-theory-for-the-gifted-amateur-by-tom-lancaster-2015)
    - [Student Friendly Quantum Field Theory by Robert D Klauber (2013)](#student-friendly-quantum-field-theory-by-robert-d-klauber-2013)
    - [Quantum field theory in a nutshell by Anthony Zee (2010)](#quantum-field-theory-in-a-nutshell-by-anthony-zee-2010)
    - [Problem Book in Quantum Field Theory by Voja Radovanovic (2008)](#problem-book-in-quantum-field-theory-by-voja-radovanovic-2008)
    - [Quantum Field Theory Demystified by David McMahon (2008)](#quantum-field-theory-demystified-by-david-mcmahon-2008)
    - [An Introduction To Quantum Field Theory by Peskin and Schroeder (1995)](#an-introduction-to-quantum-field-theory-by-peskin-and-schroeder-1995)

## Quantum field

↑ **Parent:** [Quantum field theory](quantum-field-theory.md)

## Mathematical formulation of quantum field theory

↑ **Parent:** [Quantum field theory](quantum-field-theory.md)

TODO holy crap, even this is hard to understand/find a clear definition of.

The [Dirac equation](relativistic-quantum-mechanics.md#dirac-equation), OK, is a [partial differential equation](calculus.md#partial-differential-equation), so we can easily understand its definition with basic calculus. We may not be able to solve it efficiently, but at least we understand it.

But what the heck is the mathematical model for a quantum field theory? TODO someone was saying it is equivalent to an infinite set of PDEs somehow. Investigate. Related:
- [https://www.reddit.com/r/AskPhysics/comments/74qeag/what_is_so_hard_about_qft_after_all/](https://www.reddit.com/r/AskPhysics/comments/74qeag/what_is_so_hard_about_qft_after_all/)
- [https://physics.stackexchange.com/questions/337423/what-are-quantum-fields-mathematically](https://physics.stackexchange.com/questions/337423/what-are-quantum-fields-mathematically)
- [https://physics.stackexchange.com/questions/155608/what-is-a-quantum-field](https://physics.stackexchange.com/questions/155608/what-is-a-quantum-field)

The [path integral formulation](#path-integral-formulation) might actually be the most understandable formulation, as shown at [Richard Feynman Quantum Electrodynamics Lecture at University of Auckland (1979)](#richard-feynman-quantum-electrodynamics-lecture-at-university-of-auckland-1979).

The formulation of QFT also appears to be a form of infinite-dimentional calculus.

[Quantum electrodynamics by Lifshitz et al. 2nd edition (1982)](#quantum-electrodynamics-by-lifshitz-et-al-2nd-edition-1982) chapter 1. "The uncertainty principle in the relativistic case" contains an interesting idea:

> The foregoing discussion suggests that the theory will not consider the time dependence of particle interaction processes. It will show that in these processes there are no characteristics precisely definable (even within the usual limitations of quantum mechanics); the description of such a process as occurring in the course of time is therefore just as unreal as the classical paths are in non-relativistic quantum mechanics. The only observable quantities are the properties (momenta,  
> polarizations) of free particles: the initial particles which come into interaction, and the final particles which result from the process.

### Gauge theory

↑ **Parent:** [Mathematical formulation of quantum field theory](#mathematical-formulation-of-quantum-field-theory)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Gauge_theory)

The term and idea was first introduced initialized by [Hermann Weyl](physicist.md#hermann-weyl) when he was working on combining [electromagnetism](electromagnetism.md) and [general relativity](relativity.md#general-relativity) to formulate [Maxwell's equations in curved spacetime](relativity.md#maxwell-s-equations-in-curved-spacetime) in 1918 and published as [Gravity and electricity by Hermann Weyl (1918)](physicist.md#gravity-and-electricity-by-hermann-weyl-1918). Based on perception that [$U(1)$](geometry.md#unitary-group-of-degree-1) symmetry implies [charge conservation](electromagnetism.md#charge-conservation). The same idea was later adapted for [quantum electrodynamics](#quantum-electrodynamics), a context in which is has even more impact.

#### Lattice gauge theory

↑ **Parent:** [Gauge theory](#gauge-theory)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Lattice_gauge_theory)

#### Gauge field

↑ **Parent:** [Gauge theory](#gauge-theory)

A random field you add to make something transform locally the way you want. See e.g.: [Video 17. "Deriving the qED Lagrangian by Dietterich Labs (2018)"](#video-deriving-the-qed-lagrangian-by-dietterich-labs-2018).

#### Gauge symmetry

↑ **Parent:** [Gauge theory](#gauge-theory)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Gauge_symmetry_(mathematics))

<a id="video-lawrence-krauss-explains-gauge-symmetry-by-joe-rogan-2017"></a>
**[Video 4](#video-lawrence-krauss-explains-gauge-symmetry-by-joe-rogan-2017). Lawrence Krauss explains Gauge symmetry by Joe Rogan (2017)** [Source](https://www.youtube.com/watch?v=YP-tPE7WO64). While most of this is useless as you would expect from the channel, it does give one key idea: you can change charge locally, but things somehow still work out.

And this has something to do with the general intuition of [special relativity](relativity.md#special-relativity) that only local measures make much sense, as evidenced by [Einstein synchronization](relativity.md#einstein-synchronization).

---

### Fock space

↑ **Parent:** [Mathematical formulation of quantum field theory](#mathematical-formulation-of-quantum-field-theory)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Fock_space)

Yup, this one Focks you up.

<a id="video-what-s-a-fock-space-by-physics-duck-2023"></a>
**[Video 5](#video-what-s-a-fock-space-by-physics-duck-2023). What's a Fock space? by Physics Duck (2023)** [Source](https://www.youtube.com/watch?v=NchdNEo5a48).

### Second quantization

↑ **Parent:** [Mathematical formulation of quantum field theory](#mathematical-formulation-of-quantum-field-theory)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Second_quantization)

[https://www.quora.com/How-are-quantum-fields-quantized-to-describe-particles](https://www.quora.com/How-are-quantum-fields-quantized-to-describe-particles)

Second quantization also appears to be useful not only for [relativistic quantum mechanics](relativistic-quantum-mechanics.md), but also for [condensed matter physics](condensed-matter-physics.md). The reason is that the basis idea is to use the number occupation basis. This basis is:
- convenient for [quantum field theory](quantum-field-theory.md) because of [particle creation and annihilation](relativistic-quantum-mechanics.md#particle-creation-and-annihilation) changes the number of particles all the time
- convenient for [condensed matter physics](condensed-matter-physics.md) because there you have a gazillion particles occupying entire [energy bands](condensed-matter-physics.md#electronic-band-theory)

Bibliography:

- [https://www.youtube.com/watch?v=MVqOfEYzwFY](https://www.youtube.com/watch?v=MVqOfEYzwFY) "How to Visualize Quantum Field Theory" by ZAP Physics (2020). Has [1D simulations](#quantum-field-theory-simulations) on a circle. Starts towards the right direction, but is a bit lacking unfortunately, could go deeper.

#### Canonical quantization

↑ **Parent:** [Second quantization](#second-quantization)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Canonical_quantization)

Basically a synonym for [second quantization](#second-quantization).

### Path integral formulation

↑ **Parent:** [Mathematical formulation of quantum field theory](#mathematical-formulation-of-quantum-field-theory)  
🏷️ **Tags:** [Equivalent alternatives to the Schrodinger equation](quantum-mechanics.md#equivalent-alternatives-to-the-schrodinger-equation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Path_integral_formulation)

This one might actually be understandable! It is what [Richard Feynman](richard-feynman.md) starts to explain at: [Richard Feynman Quantum Electrodynamics Lecture at University of Auckland (1979)](#richard-feynman-quantum-electrodynamics-lecture-at-university-of-auckland-1979).

The difficulty is then proving that the total probability remains at 1, and maybe causality is hard too.

The path integral formulation can be seen as a generalization of the [double-slit experiment](quantum-mechanics.md#double-slit-experiment) to infinitely many slits.

Feynman first stared working it out for [non-relativistic quantum mechanics](quantum-mechanics.md#non-relativistic-quantum-mechanics), with the relativistic goal in mind, and only later on he attained the relativistic goal.

TODO why intuitively did he take that approach? Likely is makes it easier to add [special relativity](relativity.md#special-relativity).

This approach more directly suggests the idea that [quantum particles take all possible paths](#quantum-particles-take-all-possible-paths).

#### Quantum particles take all possible paths

↑ **Parent:** [Path integral formulation](#path-integral-formulation)

As mentioned at: [https://physics.stackexchange.com/questions/212726/a-quantum-particle-moving-from-a-to-b-will-take-every-possible-path-from-a-to-b/212790#212790](https://physics.stackexchange.com/questions/212726/a-quantum-particle-moving-from-a-to-b-will-take-every-possible-path-from-a-to-b/212790#212790), classical [Gravity waves](mechanics.md#gravity-wave) for example also "take all possible paths". This is just what waves look like they are doing.

#### Propagator

↑ **Parent:** [Path integral formulation](#path-integral-formulation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Propagator)

#### Infinitely many slits thought experiment

↑ **Parent:** [Path integral formulation](#path-integral-formulation)

Thought experiment that illustrates the [path integral formulation](#path-integral-formulation) of [quantum field theory](quantum-field-theory.md).

Mentioned for example in [quantum field theory in a nutshell by Anthony Zee (2010)](#quantum-field-theory-in-a-nutshell-by-anthony-zee-2010) page 8.

### Renormalization

↑ **Parent:** [Mathematical formulation of quantum field theory](#mathematical-formulation-of-quantum-field-theory)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Renormalization)

- [https://www.quora.com/What-is-renormalization-in-quantum-theory-explained-to-graduated-only-not-doctors/answer/Paul-Mainwood](https://www.quora.com/What-is-renormalization-in-quantum-theory-explained-to-graduated-only-not-doctors/answer/Paul-Mainwood) covers the simpler [Ising model](condensed-matter-physics.md#ising-model) case

<a id="video-the-biggest-ideas-in-the-universe-11-renormalization-by-sean-carroll-2020"></a>
**[Video 6](#video-the-biggest-ideas-in-the-universe-11-renormalization-by-sean-carroll-2020). The Biggest Ideas in the Universe | 11. Renormalization by Sean Carroll (2020)** [Source](https://www.youtube.com/watch?v=Nm8DRUgmjZc). Gives a very quick and high level overview of [renormalization](#renormalization). It is not enough to satisfy [Ciro Santilli](ciro-santilli.md) as usual for other Sean Carroll videos, but it goes some way.

#### Mass renormalization

↑ **Parent:** [Renormalization](#renormalization)

#### Renormalization group

↑ **Parent:** [Renormalization](#renormalization)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Renormalization_group)

#### Cutoff energy

↑ **Parent:** [Renormalization](#renormalization)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Cutoff_energy)

#### Effective field theory

↑ **Parent:** [Renormalization](#renormalization)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Effective_field_theory)

[https://www.youtube.com/watch?v=WB8r7CU7clk&list=PLUl4u3cNGP60TvpbO5toEWC8y8w51dtvm](https://www.youtube.com/watch?v=WB8r7CU7clk&list=PLUl4u3cNGP60TvpbO5toEWC8y8w51dtvm) by Iain Stewart. Basically starts by explaining how [quantum field theory](quantum-field-theory.md) is so generic that it is hard to get any numerical results out of it :-)

But in particular, we want to describe those subtheories in a way that we can reach arbitrary precision of the full theory if desired.

#### Yang-Mills theory

↑ **Parent:** [Renormalization](#renormalization)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Yang–Mills_theory)

##### Yang-Mills existence and mass gap

↑ **Parent:** [Yang-Mills theory](#yang-mills-theory)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Yang–Mills_existence_and_mass_gap)

- [https://www.youtube.com/watch?v=-_qNKbwM_eE](https://www.youtube.com/watch?v=-_qNKbwM_eE) Unsolved: Yang-Mills existence and mass gap by J Knudsen (2019). Gives 10 key points, but the truly hard ones are too quick. He knows the thing though.

<a id="video-yang-mills-1-by-david-metzler-2011"></a>


**[Video 7](#video-yang-mills-1-by-david-metzler-2011). Yang-Mills 1 by David Metzler (2011)** [Source](https://www.youtube.com/watch?v=j3fsPHnrgLg). Playlist: [https://www.youtube.com/watch?v=j3fsPHnrgLg&list=PL613A31A706529585&index=13](https://www.youtube.com/watch?v=j3fsPHnrgLg&list=PL613A31A706529585&index=13)

A bit disappointing, too high level, with very few nuggests that are not Googleable withing 5 minutes.

Breakdown:
- 1 [https://www.youtube.com/watch?v=j3fsPHnrgLg](https://www.youtube.com/watch?v=j3fsPHnrgLg): too basic
- 2 [https://www.youtube.com/watch?v=br6OxCLyqAI?t=569](https://www.youtube.com/watch?v=br6OxCLyqAI?t=569): mentions [groups of Lie type](group.md#group-of-lie-type) in the context of [classification of finite simple groups](group.md#classification-of-finite-simple-groups). Each group has a little diagram.
- 3 [https://youtu.be/1baiIxKKQlQ?list=PL613A31A706529585&t=728](https://youtu.be/1baiIxKKQlQ?list=PL613A31A706529585&t=728) the original example of a [local symmetry](geometry.md#local-symmetry) was [general relativity](relativity.md#general-relativity), and that in that context it can be clearly seen that the local symmetry is what causes "forces" to appear
  - [https://youtu.be/1baiIxKKQlQ?list=PL613A31A706529585&t=933](https://youtu.be/1baiIxKKQlQ?list=PL613A31A706529585&t=933) [local symmetry](geometry.md#local-symmetry) gives a conserved current. In the case of [electromagnetism](electromagnetism.md), this is electrical current. This was the only worthwhile thing he sad to 2021 Ciro. Summarized at: [local symmetries of the Lagrangian imply conserved currents](geometry.md#local-symmetries-of-the-lagrangian-imply-conserved-currents).
- 4 [https://youtu.be/5ljKcWm7hoU?list=PL613A31A706529585&t=427](https://youtu.be/5ljKcWm7hoU?list=PL613A31A706529585&t=427) [electromagnetism](electromagnetism.md) has both a global symmetry ([special relativity](relativity.md#special-relativity)) but also [local symmetry](geometry.md#local-symmetry), which leads to the conservation of charge current and forces.

  [lecture 3](#quantum-field-theory-lecture-by-tobias-osborne-2017/lecture-3) properly defines a [local symmetry](geometry.md#local-symmetry) in terms of the context of the [lagrangian density](mechanics.md#lagrangian-density), and explains that the conservation of currents there is basically the statement of [Noether's theorem](mechanics.md#noether-s-theorem) in that context.

---

<a id="video-millennium-prize-problem-yang-mills-theory-by-david-gross-2018"></a>


**[Video 8](#video-millennium-prize-problem-yang-mills-theory-by-david-gross-2018). Millennium Prize Problem: Yang Mills Theory by David Gross (2018)** [Source](https://www.youtube.com/watch?v=vMiY7zlBOFI). 2 hour talk at the [Kavli Institute for Theoretical Physics](university.md#kavli-institute-for-theoretical-physics). Too mathematical, 2021 Ciro can't make much out of it.

<a id="video-lorenzo-sadun-on-the-yang-mills-and-mass-gap-millennium-problem"></a>
**[Video 9](#video-lorenzo-sadun-on-the-yang-mills-and-mass-gap-millennium-problem). Lorenzo Sadun on the "Yang-Mills and Mass Gap" Millennium problem.** [Source](https://www.youtube.com/watch?v=pCQ9GIqpGBI). Unknown year. He almost gets there, he's good. Just needed to be a little bit deeper.

###### Wightman axioms

↑ **Parent:** [Yang-Mills existence and mass gap](#yang-mills-existence-and-mass-gap)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Wightman_axioms)

## Quantum electrodynamics

↑ **Parent:** [Quantum field theory](quantum-field-theory.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Quantum_electrodynamics)

Theory that describes [electrons](standard-model.md#electron) and [photons](photon.md) really well, and [as Feynman puts it](#richard-feynman-quantum-electrodynamics-lecture-at-university-of-auckland-1979) "accounts very precisely for all physical phenomena we have ever observed, except for gravity and nuclear physics" ("including the laughter of the crowd" ;-)).

Learning it is one of [Ciro Santilli](ciro-santilli.md)'s main intellectual [fetishes](brain.md#fetish).

While Ciro acknowledges that QED is intrinsically challenging due to the wide range or requirements ([quantum mechanics](quantum-mechanics.md), [special relativity](relativity.md#special-relativity) and [electromagnetism](electromagnetism.md)), Ciro feels that there is a glaring gap in this moneyless market for a learning material that follows the [Middle Way](religion.md#middle-way) as mentioned at: [the missing link between basic and advanced](ciro-santilli.md#the-missing-link-between-basic-and-advanced). [Richard Feynman Quantum Electrodynamics Lecture at University of Auckland (1979)](#richard-feynman-quantum-electrodynamics-lecture-at-university-of-auckland-1979) is one of the best attempts so far, but it falls a bit too close to the superficial side of things, if only Feynman hadn't assumed that the audience doesn't know any mathematics...

The funny thing is that when [Ciro Santilli's mother](ciro-santilli.md#ciro-santilli-s-mother) retired, learning it (or as she put it: "how photons and electrons interact") was also one of her retirement plans. She is a pharmacist by training, and doesn't know much [mathematics](mathematics.md), and her [English](linguistics.md#english-language) was [somewhat limited](cirism.md#having-more-than-one-natural-language-is-bad-for-the-world). Oh, she also wanted to learn how [photosynthesis](taxonomy.md#photosynthesis) works (possibly not fully understood by science as that time, 2020). Ambitious old lady!!!

Experiments: [quantum electrodynamics experiments](#quantum-electrodynamics-experiment).

Combines [special relativity](relativity.md#special-relativity) with more classical [quantum mechanics](quantum-mechanics.md), but further generalizing the [Dirac equation](relativistic-quantum-mechanics.md#dirac-equation), which also does that: [Dirac equation vs quantum electrodynamics](#dirac-equation-vs-quantum-electrodynamics). The name "relativistic" likely doesn't need to appear on the title of QED because [Maxwell's equations require special relativity](relativity.md#maxwell-s-equations-require-special-relativity), so just having "electro-" in the title is enough.

Before QED, the most advanced theory was that of the [Dirac equation](relativistic-quantum-mechanics.md#dirac-equation), which was already relativistic but TODO what was missing there exactly?

As summarized at: [https://youtube.com/watch?v=_AZdvtf6hPU?t=305](https://youtube.com/watch?v=_AZdvtf6hPU?t=305) Quantum Field Theory lecture at the African Summer Theory Institute 1 of 4 by Anthony Zee (2004):
- classical mechanics describes large and slow objects
- special relativity describes large and fast objects (they are getting close to the speed of light, so we have to consider relativity)
- classical [quantum mechanics](quantum-mechanics.md) describes small and slow objects.
- QED describes objects that are both small and fast

That video also mentions the interesting idea that:
- in special relativity, we have the [mass-energy equivalence](relativity.md#mass-energy-equivalence)
- in quantum mechanics, thinking along the [time-energy uncertainty principle](quantum-mechanics.md#time-energy-uncertainty-principle), $\Delta E \sim \frac{1}{\Delta t}$
Therefore, for small timescales, energy can vary a lot. But mass is equivalent to energy. Therefore, for small time scale, particles can appear and disappear wildly.

QED is the first [quantum field theory](quantum-field-theory.md) fully developed. That framework was later extended to also include the [weak interaction](#weak-interaction) and [strong interaction](#strong-interaction). As a result, it is perhaps easier to just [Google](google.md) for "Quantum Field Theory" if you want to learn QED, since QFT is more general and has more resources available generally.

Like in more general quantum field theory, there is on field for each particle type. In quantum field theory, there are only two fields to worry about:
- [photon](photon.md) field
- [electromagnetism](electromagnetism.md) field

<a id="video-lecture-01-overview-of-quantum-field-theory-by-markus-luty-2013"></a>
**[Video 10](#video-lecture-01-overview-of-quantum-field-theory-by-markus-luty-2013). Lecture 01 | Overview of Quantum Field Theory by Markus Luty (2013)** [Source](https://www.youtube.com/watch?v=EzfFklLqDjA). This takes quite a direct approach, one cool thing he says is how we have to be careful with adding special relativity to the [Schrödinger equation](quantum-mechanics.md#schrodinger-equation) to avoid faster-than-light information.

### Quantum electrodynamics experiment

↑ **Parent:** [Quantum electrodynamics](#quantum-electrodynamics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Quantum_electrodynamics_experiment)

Experiments explained by QED but not by the [Dirac equation](relativistic-quantum-mechanics.md#dirac-equation):
- [Lamb shift](#lamb-shift): by far the most famous one
- [hyperfine structure](quantum-mechanics.md#hyperfine-structure) TODO confirm
- [anomalous magnetic dipole moment of the electron](#anomalous-magnetic-dipole-moment-of-the-electron)

#### Lamb shift

↑ **Parent:** [Quantum electrodynamics experiment](#quantum-electrodynamics-experiment)  
🏷️ **Tags:** [The most important physics experiments](physics.md#the-most-important-physics-experiments)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Lamb_shift)

2s/2p energy split in the [hydrogen emission spectrum](quantum-mechanics.md#hydrogen-emission-spectrum), not predicted by the [Dirac equation](relativistic-quantum-mechanics.md#dirac-equation), but explained by [quantum electrodynamics](#quantum-electrodynamics), which is one of the first great triumphs of that theory.

Note that for atoms with multiple electrons, 2s/2p shifts are expected: [Why does 2s have less energy than 1s if they have the same principal quantum number?](quantum-mechanics.md#why-does-2s-have-less-energy-than-1s-if-they-have-the-same-principal-quantum-number). The surprise was observing that on [hydrogen](chemistry.md#hydrogen) which only has one [electron](standard-model.md#electron). 

Initial experiment: [Lamb-Retherford experiment](#lamb-retherford-experiment).

On the return from the train from  the [Shelter Island Conference](physics.md#shelter-island-conference) in [New York](united-states.md#new-york), [Hans Bethe](physicist.md#hans-bethe) managed to do a [non-relativistic](relativity.md) calculation of the [Lamb shift](#lamb-shift). He then published as The Electromagnetic Shift of Energy Levels by Hans Bethe (1947) which is still paywalled as of 2021, [fuck me](education.md#academic-publishing): [https://journals.aps.org/pr/abstract/10.1103/PhysRev.72.339](https://journals.aps.org/pr/abstract/10.1103/PhysRev.72.339) by [Physical Review](physics.md#physical-review).

The Electromagnetic Shift of Energy Levels [Freeman Dyson](physicist.md#freeman-dyson) (1948) published on  [Physical Review](physics.md#physical-review) is apparently a [relativistic](relativity.md) analysis of the same: [https://journals.aps.org/pr/abstract/10.1103/PhysRev.73.617](https://journals.aps.org/pr/abstract/10.1103/PhysRev.73.617) also paywalled as of 2021.

TODO how do the infinities show up, and how did people solve them?

<a id="video-lamb-shift-by-dr-nissar-ahmad-2020"></a>
**[Video 11](#video-lamb-shift-by-dr-nissar-ahmad-2020). Lamb shift by Dr. Nissar Ahmad (2020)** [Source](https://www.youtube.com/watch?v=jPKEuiUNJIk). Whiteboard Lecture about the phenomena, includes description of the experiment. Seems quite good.

<a id="video-murray-gell-mann-the-race-to-calculate-the-relativistic-lamb-shift-by-web-of-stories-1997"></a>
**[Video 12](#video-murray-gell-mann-the-race-to-calculate-the-relativistic-lamb-shift-by-web-of-stories-1997). Murray Gell-Mann - The race to calculate the relativistic Lamb shift by Web of Stories (1997)** [Source](https://www.youtube.com/watch?v=WcyMfgj9psQ). Quick historical overview. Mentions that [Richard Feynman](richard-feynman.md) and [Julian Schwinger](physicist.md#julian-schwinger) were using [mass renormalization](#mass-renormalization) and cancellation if infinities. He says that French and  Weisskopf actually managed to do the correct calculations first with a less elegant method.

[https://www.mdpi.com/2624-8174/2/2/8/pdf](https://www.mdpi.com/2624-8174/2/2/8/pdf) History and Some Aspects of the Lamb Shift by G. Jordan Maclay (2019)

<a id="video-freeman-dyson-the-lamb-shift-by-web-of-stories-1998"></a>
**[Video 13](#video-freeman-dyson-the-lamb-shift-by-web-of-stories-1998). Freeman Dyson - The Lamb shift by Web of Stories (1998)** [Source](https://www.youtube.com/watch?v=062GN3RdH1c). Mentions that he moved to the [USA](united-states.md) from the [United Kingdom](united-kingdom.md) specifically because great experiments were being carried at [Columbia University](university.md#columbia-university), which is where the [Lamb-Retherford experiment](#lamb-retherford-experiment) was done, and that [Isidor Isaac Rabi](physicist.md#isidor-isaac-rabi) was the head at the time.

He then explains [mass renormalization](#mass-renormalization) briefly: instead of calculating from scratch, you just compare the raw electron to the bound electron and take the difference. Both of those have infinities in them, but the difference between them cancels out those infinities.

---

<a id="video-hans-bethe-the-lamb-shift-1996"></a>
**[Video 14](#video-hans-bethe-the-lamb-shift-1996). Hans Bethe - The Lamb shift (1996)** [Source](https://www.youtube.com/watch?v=YP6TGj-yL7Y). Ahh, Hans is so old in that video, it is sad to see. He did live a lot tough. Mentions that the shift is of about 1000 MHz.

The following video: [https://www.youtube.com/watch?v=vZvQg3bkV7s](https://www.youtube.com/watch?v=vZvQg3bkV7s) Hans Bethe - Calculating the Lamb shift.

---

<a id="video-lamb-shift-by-vidya-mitra-2018"></a>
**[Video 15](#video-lamb-shift-by-vidya-mitra-2018). Lamb shift by Vidya-mitra (2018)** [Source](https://www.youtube.com/watch?v=-0DDUyR0200).

##### Lamb-Retherford experiment

↑ **Parent:** [Lamb shift](#lamb-shift)  
🏷️ **Tags:** [1955 Nobel Prize in Physics](nobel-prize.md#1955-nobel-prize-in-physics)

Published as "Fine Structure of the Hydrogen Atom by a Microwave Method" by [Willis Lamb](physicist.md#willis-lamb) and Robert Retherford (1947) on [Physical Review](physics.md#physical-review). This one actually has [open accesses](education.md#open-access) as of 2021, miracle! [https://journals.aps.org/pr/pdf/10.1103/PhysRev.72.241](https://journals.aps.org/pr/pdf/10.1103/PhysRev.72.241)

[Microwave](photon.md#microwave) technology was developed in [World War II](science.md#world-war-ii) for [radar](telecommunication.md#radar), notably at the [MIT Radiation Laboratory](university.md#mit-radiation-laboratory). Before that, people were using much higher frequencies such as the [visible spectrum](photon.md#visible-spectrum). But to detect small energy differences, you need to look into longer wavelengths.

This experiment was fundamental to the development of [quantum electrodynamics](#quantum-electrodynamics). As mentioned at [Genius: Richard Feynman and Modern Physics by James Gleick (1994)](genius-richard-feynman-and-modern-physics-by-james-gleick-1994.md) chapter "Shrinking the infinities", before the experiment, people already knew that trying to add [electromagnetism](electromagnetism.md) to the [Dirac equation](relativistic-quantum-mechanics.md#dirac-equation) led to [infinities](#infinities-in-quantum-field-theory) using previous methods, and something needed to change urgently. However for the first time now the theorists had one precise number to try and hack their formulas to reach, not just a philosophical debate about infinities, and this led to major breakthroughs. The same book also describes the experiment briefly as:

> Willis Lamb had just shined a beam of microwaves onto a hot wisp of hydrogen blowing from an oven.

It is two pages and a half long.

They were at [Columbia University](university.md#columbia-university) in the [Columbia Radiation Laboratory](university.md#columbia-radiation-laboratory). Robert was Willis' graduate student.

Previous less experiments had already hinted at this effect, but they were too imprecise to be sure.

#### Electron magnetic moment

↑ **Parent:** [Quantum electrodynamics experiment](#quantum-electrodynamics-experiment)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Electron_magnetic_moment)

##### Anomalous magnetic dipole moment

↑ **Parent:** [Electron magnetic moment](#electron-magnetic-moment)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Anomalous_magnetic_dipole_moment)

###### Anomalous magnetic dipole moment of the electron

↑ **Parent:** [Anomalous magnetic dipole moment](#anomalous-magnetic-dipole-moment)  
🏷️ **Tags:** [1955 Nobel Prize in Physics](nobel-prize.md#1955-nobel-prize-in-physics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Anomalous_magnetic_dipole_moment#Electron)

[Richard Feynman Quantum Electrodynamics Lecture at University of Auckland (1979)](#richard-feynman-quantum-electrodynamics-lecture-at-university-of-auckland-1979) mentions it several times.

This was one of the first two great successes of [quantum electrodynamics](#quantum-electrodynamics), the other one being the [Lamb shift](#lamb-shift).

In [https://youtu.be/UKbp85zpdcY?t=52](https://youtu.be/UKbp85zpdcY?t=52) from [freeman Dyson Web of Stories interview (1998)](physicist.md#freeman-dyson-web-of-stories-interview-1998) Dyson mentions that the original key experiment was from Kusch and Foley from [Columbia University](university.md#columbia-university), and that in 1948, [Julian Schwinger](physicist.md#julian-schwinger) reached the correct value from his calculations.

Apparently first published at [The Magnetic Moment of the Electron by Kusch and Foley (1948)](#the-magnetic-moment-of-the-electron-by-kusch-and-foley-1948).

Bibliography:
- [https://www.youtube.com/watch?v=Ix-3LQhElvU](https://www.youtube.com/watch?v=Ix-3LQhElvU) Anomalous Magnetic Moment Of The Electron | One Loop Quantum Correction | Quantum Electrodynamics by [Dietterich Labs](particle-physics.md#dietterich-labs) (2019)

###### The Magnetic Moment of the Electron by Kusch and Foley (1948)

↑ **Parent:** [Anomalous magnetic dipole moment of the electron](#anomalous-magnetic-dipole-moment-of-the-electron)  
🏷️ **Tags:** [1955 Nobel Prize in Physics](nobel-prize.md#1955-nobel-prize-in-physics)

Published on [Physical Review](physics.md#physical-review) by [Polykarp Kusch](physicist.md#polykarp-kusch) and Foley.

[https://journals.aps.org/pr/abstract/10.1103/PhysRev.74.250](https://journals.aps.org/pr/abstract/10.1103/PhysRev.74.250), paywall as of 2021.

#### Dirac equation vs quantum electrodynamics

↑ **Parent:** [Quantum electrodynamics experiment](#quantum-electrodynamics-experiment)  
🏷️ **Tags:** [Dirac equation](relativistic-quantum-mechanics.md#dirac-equation)

TODO: in high level terms, why is QED more general than just solving the [Dirac equation](relativistic-quantum-mechanics.md#dirac-equation), and therefore explaining [quantum electrodynamics experiments](#quantum-electrodynamics-experiment)?

Also, is it just a bunch of [differential equation](calculus.md#differential-equation) (like the [Dirac equation](relativistic-quantum-mechanics.md#dirac-equation) itself), or does it have some other more complicated mathematical formulation, as seems to be the case? Why do we need something more complicated than 

The main high level insight seems to be that [The Dirac equation does not work for more than one electron](#the-dirac-equation-does-not-work-for-more-than-one-electron).

Bibliography:
- [https://physics.stackexchange.com/questions/101307/dirac-equation-in-qft-vs-relativistic-qm](https://physics.stackexchange.com/questions/101307/dirac-equation-in-qft-vs-relativistic-qm)
- [https://physics.stackexchange.com/questions/44188/what-is-the-relativistic-particle-in-a-box/44309#44309](https://physics.stackexchange.com/questions/44188/what-is-the-relativistic-particle-in-a-box/44309#44309) says:> By several reasons explained in textbooks, the Dirac equation is not a valid wavefunction equation. You can solve it and find solutions, but those solutions cannot be interpreted as wavefunctions for a particle
- [https://physics.stackexchange.com/questions/64206/why-is-the-dirac-equation-not-used-for-calculations](https://physics.stackexchange.com/questions/64206/why-is-the-dirac-equation-not-used-for-calculations)
- [https://www.physicsforums.com/threads/is-diracs-equation-still-useful-after-qed-is-developed.663994/](https://www.physicsforums.com/threads/is-diracs-equation-still-useful-after-qed-is-developed.663994/)

##### The Dirac equation does not work for more than one electron

↑ **Parent:** [Dirac equation vs quantum electrodynamics](#dirac-equation-vs-quantum-electrodynamics)

TODO understand in detail.

[Advanced quantum mechanics by Freeman Dyson (1951)](#advanced-quantum-mechanics-by-freeman-dyson-1951) mentions:

> A Relativistic Quantum Theory of a Finite Number of Particles is Impossible.

[Atom 2007 Mini Series episode 3](science.md#atom-2007-mini-series-episode-3):

> \[The [Dirac equation](relativistic-quantum-mechanics.md#dirac-equation)\] could only describe a single electron. It fails completely to explain what happens when there is more than one electron present. What was needed was a new theory. A theory which explains how electrons interact with each other. 

### Applications of quantum electrodynamics

↑ **Parent:** [Quantum electrodynamics](#quantum-electrodynamics)

- [https://www.quora.com/What-are-some-engineering-applications-of-QED-or-QCD-quantum-field-theories](https://www.quora.com/What-are-some-engineering-applications-of-QED-or-QCD-quantum-field-theories)
- [relativistic quantum chemistry](physics.md#relativistic-quantum-chemistry)

### Quantum electrodynamics Lagrangian

↑ **Parent:** [Quantum electrodynamics](#quantum-electrodynamics)



$$
\mathcal{L}_{\mathrm{QED}} = \bar \psi (i\hbar c {D}\!\!\!\!/\ - mc^2) \psi - {1 \over 4\mu_0} F_{\mu \nu} F^{\mu \nu}
$$

where:
- $F$ is the [electromagnetic tensor](electromagnetism.md#electromagnetic-tensor)

Note that this is the sum of the:
- [Dirac Lagrangian](relativistic-quantum-mechanics.md#dirac-lagrangian), which  only describes the "inertia of bodies" part of the equation
- the [electromagnetic](electromagnetism.md) interaction term ${1 \over 4\mu_0} F_{\mu \nu} F^{\mu \nu}$, which describes term describes forces
Note that the relationship between $\psi$ and $F$ is not explicit. However, if we knew what type of particle we were talking about, e.g. [electron](standard-model.md#electron), then the knowledge of [psi](linguistics.md#psi-greek) would also give the charge distribution and therefore $F$

As mentioned at the beginning of [Quantum Field Theory lecture notes by David Tong (2007)](#quantum-field-theory-lecture-notes-by-david-tong-2007):
- by "[Lagrangian](mechanics.md#lagrangian)" we mean Lagrangian density
- the [generalized coordinates](mechanics.md#generalized-coordinate) of the Lagrangian are fields

<a id="video-particle-physics-is-founded-on-this-principle-by-physics-with-elliot-2022"></a>
**[Video 16](#video-particle-physics-is-founded-on-this-principle-by-physics-with-elliot-2022). Particle Physics is Founded on This Principle! by Physics with Elliot (2022)** [Source](https://www.youtube.com/watch?v=I4CjewbJgRQ).

#### Derivation of the quantum electrodynamics Lagrangian

↑ **Parent:** [Quantum electrodynamics Lagrangian](#quantum-electrodynamics-lagrangian)

Like the rest of the [Standard Model Lagrangian](standard-model.md#standard-model-lagrangian), this can be split into two parts:
- [spacetime symmetry](#spacetime-symmetry): reaches the [derivation of the Dirac equation](relativistic-quantum-mechanics.md#derivation-of-the-dirac-equation), but has no interactions
- add the [$U(1)$](geometry.md#unitary-group-of-degree-1) [internal symmetry](#internal-symmetry) to add interactions, which reaches the full equation

<a id="video-deriving-the-qed-lagrangian-by-dietterich-labs-2018"></a>
**[Video 17](#video-deriving-the-qed-lagrangian-by-dietterich-labs-2018). Deriving the qED Lagrangian by Dietterich Labs (2018)** [Source](https://www.youtube.com/watch?v=IFRyN3fQMO8). As mentioned at the start of the video, he starts with the [Dirac equation](relativistic-quantum-mechanics.md#dirac-equation) Lagrangian derived in a previous video. It has nothing to do with [electromagnetism](electromagnetism.md) specifically.

He notes that that [Dirac Lagrangian](relativistic-quantum-mechanics.md#dirac-lagrangian), besides being globally [Lorentz invariant](relativity.md#lorentz-invariant), it also also has a global [$U(1)$](geometry.md#unitary-group-of-degree-1) invariance.

However, it does not have a local invariance if the [$U(1)$](geometry.md#unitary-group-of-degree-1) transformation depends on the point in spacetime.

He doesn't mention it, but I think this is highly desirable, because in general [local symmetries of the Lagrangian imply conserved currents](geometry.md#local-symmetries-of-the-lagrangian-imply-conserved-currents), and in this case we want conservation of charges.

To fix that, he adds an extra [gauge field](#gauge-field) $A_\mu$ (a field of $4 \times 4$ matrices) to the regular derivative, and the resulting derivative has a fancy name: the [covariant derivative](calculus.md#covariant-derivative).

Then finally he notes that this [gauge field](#gauge-field) he had to add has to transform exactly like the [electromagnetic four-potential](electromagnetism.md#electromagnetic-four-potential)!

So he uses that as the gauge, and also adds in the [Maxwell Lagrangian](relativity.md#maxwell-lagrangian) in the same go. It is kind of a guess, but it is a natural guess, and it turns out to be correct.

[https://www.youtube.com/watch?v=IFRyN3fQMO8&lc=UgzNGkLXdwcSl7z8Lap4AaABAg](https://www.youtube.com/watch?v=IFRyN3fQMO8&lc=UgzNGkLXdwcSl7z8Lap4AaABAg)

---

### What does it mean that photons are force carriers for electromagnetism?

↑ **Parent:** [Quantum electrodynamics](#quantum-electrodynamics)

[https://physics.stackexchange.com/questions/61095/photon-as-the-carrier-of-the-electromagnetic-force](https://physics.stackexchange.com/questions/61095/photon-as-the-carrier-of-the-electromagnetic-force)

TODO find/create decent answer.

I think the best answer is something along:
- [local symmetries of the Lagrangian imply conserved currents](geometry.md#local-symmetries-of-the-lagrangian-imply-conserved-currents). $U(1)$ gives conserved charges.
- OK now. We want a local $U(1)$ symmetry. And we also want:
  - [Dirac equation](relativistic-quantum-mechanics.md#dirac-equation): quantum relativistic Newton's laws that specify what forces do to the fields
  - [electromagnetism](electromagnetism.md): specifies what causes forces based on currents. But not what it does to masses.

  Given all of that, the most obvious and direct thing we reach a guess at the [quantum electrodynamics Lagrangian](#quantum-electrodynamics-lagrangian) is [Video 17. "Deriving the qED Lagrangian by Dietterich Labs (2018)"](#video-deriving-the-qed-lagrangian-by-dietterich-labs-2018)

A basic non-precise intuition is that a good model of reality is that electrons do not "interact with one another directly via the electromagnetic field".

A better model happens to be the [quantum field theory](quantum-field-theory.md) view that the electromagnetic field interacts with the photon field but not directly with itself, and then the photon field interacts with parts of the electromagnetic field further away.

The more precise statement is that the [photon field](#photon-field) is a gauge field of the electromagnetic force under local U(1) symmetry, which is described by a [Lie group](geometry.md#lie-group). TODO understand.

This idea was first applied in [general relativity](relativity.md#general-relativity), where [Einstein](physicist.md#albert-einstein) understood that the "force of [gravity](relativity.md#gravity)" can be understood just in terms of symmetry and curvature of space. This was later applied o [quantum electrodynamics](#quantum-electrodynamics) and the entire [Standard Model](standard-model.md).

From [Video 9. "Lorenzo Sadun on the "Yang-Mills and Mass Gap" Millennium problem"](#video-lorenzo-sadun-on-the-yang-mills-and-mass-gap-millennium-problem):
- [https://www.youtube.com/watch?v=pCQ9GIqpGBI&t=1663s](https://www.youtube.com/watch?v=pCQ9GIqpGBI&t=1663s) mentions this idea first came about from [Hermann Weyl](physicist.md#hermann-weyl).
- [https://youtu.be/pCQ9GIqpGBI?t=2827](https://youtu.be/pCQ9GIqpGBI?t=2827) mentions that in that case the curvature is given by the [electromagnetic tensor](electromagnetism.md#electromagnetic-tensor).

Bibliography:
- [https://www.youtube.com/watch?v=qtf6U3FfDNQ](https://www.youtube.com/watch?v=qtf6U3FfDNQ) Symmetry and Quantum Electrodynamics (The Standard Model Part 1) by ZAP Physics (2021)
- [https://www.youtube.com/watch?v=OQF7kkWjVWM](https://www.youtube.com/watch?v=OQF7kkWjVWM) The Symmetry and Simplicity of the Laws of Nature and the Higgs Boson by Juan Maldacena (2012). [Meh](linguistics.md#meh), also too basic.

### Photon field

↑ **Parent:** [Quantum electrodynamics](#quantum-electrodynamics)

### Schwinger effect

↑ **Parent:** [Quantum electrodynamics](#quantum-electrodynamics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Schwinger_effect)

### Feynman diagram

↑ **Parent:** [Quantum electrodynamics](#quantum-electrodynamics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Feynman_diagram)

I think they are a tool to calculate the probability of different types of particle decays and particle collision outcomes. TODO Minimal example of that.

And they can be derived from a more complete [quantum electrodynamics](#quantum-electrodynamics) formulation via [perturbation theory](mathematics.md#perturbation-theory).

Can be used for all of [quantum electrodynamics](#quantum-electrodynamics), [weak interaction](#weak-interaction) and [quantum chromodynamics](#quantum-chromodynamics).

At [Richard Feynman Quantum Electrodynamics Lecture at University of Auckland (1979)](#richard-feynman-quantum-electrodynamics-lecture-at-university-of-auckland-1979), an intuitive explanation of them in termes of sum of products of [propagators](#propagator) is given.

- [https://www.youtube.com/watch?v=fG52mXN-uWI](https://www.youtube.com/watch?v=fG52mXN-uWI) The Secrets of Feynman Diagrams | Space Time by [PBS Space Time](particle-physics.md#pbs-space-time) (2017)

#### Feynman diagram solver

↑ **Parent:** [Feynman diagram](#feynman-diagram)

[https://physics.stackexchange.com/questions/96510/software-for-calculating-feynman-diagrams](https://physics.stackexchange.com/questions/96510/software-for-calculating-feynman-diagrams)

#### Does the exact position of vertices matter in Feynman diagrams?

↑ **Parent:** [Feynman diagram](#feynman-diagram)

No, but why?

- [https://physics.stackexchange.com/questions/297004/feynman-diagram-and-uncertainty/297006](https://physics.stackexchange.com/questions/297004/feynman-diagram-and-uncertainty/297006)

### Wheeler-Feynman absorber theory

↑ **Parent:** [Quantum electrodynamics](#quantum-electrodynamics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Wheeler–Feynman absorber theory)

What they presented on [richard Feynman's first seminar in 1941](richard-feynman-s-first-seminar-in-1941.md). Does not include [quantum mechanics](quantum-mechanics.md) it seems.

### Cavity quantum electrodynamics

↑ **Parent:** [Quantum electrodynamics](#quantum-electrodynamics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Cavity_quantum_electrodynamics)

#### Circuit quantum electrodynamics

↑ **Parent:** [Cavity quantum electrodynamics](#cavity-quantum-electrodynamics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Circuit_quantum_electrodynamics)

### Positrons are electrons travelling back in time

↑ **Parent:** [Quantum electrodynamics](#quantum-electrodynamics)

TODO understand this stuff:
- [https://physics.stackexchange.com/questions/144607/are-all-positrons-electrons-traveling-back-in-time](https://physics.stackexchange.com/questions/144607/are-all-positrons-electrons-traveling-back-in-time)
- [https://www.quora.com/Is-a-positron-just-an-electron-going-backwards-in-time?share=1](https://www.quora.com/Is-a-positron-just-an-electron-going-backwards-in-time?share=1)

### Quantum electrodynamics bibliography

↑ **Parent:** [Quantum electrodynamics](#quantum-electrodynamics)

[http://fafnir.phyast.pitt.edu/py3765/](http://fafnir.phyast.pitt.edu/py3765/) Phys3765 Advanced Quantum Mechanics -- QFT-I Fall 2012 by E.S. Swanson mentions several milestone texts including:
- [Advanced quantum mechanics by Freeman Dyson (1951)](#advanced-quantum-mechanics-by-freeman-dyson-1951)

#### Quantum Theory of Radiation by Fermi (1932)

↑ **Parent:** [Quantum electrodynamics bibliography](#quantum-electrodynamics-bibliography)

#### Advanced quantum mechanics by Freeman Dyson (1951)

↑ **Parent:** [Quantum electrodynamics bibliography](#quantum-electrodynamics-bibliography)  
🏷️ **Tags:** [Work by Freeman Dyson](physicist.md#work-by-freeman-dyson)

[https://arxiv.org/abs/quant-ph/0608140v1](https://arxiv.org/abs/quant-ph/0608140v1)

Lecture notes that were apparently very popular at [Cornell University](university.md#cornell-university). In this period he was actively synthesizing the revolutionary bullshit [Richard Feynman](richard-feynman.md) and [Julian Schwinger](physicist.md#julian-schwinger) were writing and making it understandable to the more general [physicist](physicist.md) audience, so it might be a good reading.



> We shall not develop straightaway a correct theory including many particles. Instead we follow the historical development. We try to make a relativistic quantum theory of one particle, find out how far we can go and where we get into trouble.

Oh yes, see also: [Dirac equation vs quantum electrodynamics](#dirac-equation-vs-quantum-electrodynamics).

#### Selected Papers on Quantum Electrodynamics by Julian Schwinger (1958)

↑ **Parent:** [Quantum electrodynamics bibliography](#quantum-electrodynamics-bibliography)

Recommended by [Ron Maimon](stack-overflow.md#ron-maimon) at [https://physics.stackexchange.com/questions/18632/good-book-on-the-history-of-quantum-mechanics/18643#18643](https://physics.stackexchange.com/questions/18632/good-book-on-the-history-of-quantum-mechanics/18643#18643).

[Julian Schwinger](physicist.md#julian-schwinger)'s selection of [academic papers](education.md#academic-paper) by himself and others.

#### Richard Feynman Quantum Electrodynamics Lecture at University of Auckland (1979)

↑ **Parent:** [Quantum electrodynamics bibliography](#quantum-electrodynamics-bibliography)  
🏷️ **Tags:** [Work by Richard Feynman](work-by-richard-feynman.md)

Talk title shown on intro: "Today's Answers to Newton's Queries about Light".

6 hour lecture, where he tries to explain it to an audience that does not know any modern physics. This is a noble effort.

Part of The Douglas Robb Memorial Lectures lecture series.

Feynman apparently also made a book adaptation: [QED: The Strange Theory of Light and Matter](https://en.wikipedia.org/wiki/QED:_The_Strange_Theory_of_Light_and_Matter). That book is basically word by word the same as the presentation, including the diagrams.

According to [http://www.feynman.com/science/qed-lectures-in-new-zealand/](http://www.feynman.com/science/qed-lectures-in-new-zealand/) the official upload is at [http://www.vega.org.uk/video/subseries/8](http://www.vega.org.uk/video/subseries/8) and Vega does show up as a watermark on the video (though it is too pixilated to guess without knowing it), a project that has been discontinued and has has a non-permissive license. Newbs.

4 parts:
- Part 1: is saying "[photons](photon.md) exist"
- Part 2: is amazing, and describes how photons move as a sum of all possible paths, not sure if it is relativistic at all though, and suggests that something is minimized in that calculation (the [action](mechanics.md#action-physics))
- Part 3: is where he hopelessly tries to explain the crucial part of how electrons join the picture in a similar manner to how photons do.

  He does make the link to light, saying that there is a function $P(A, B)$ which gives the amplitude for a photon going from A to B, where A and B are spacetime events.

  And then he mentions that there is a similar function $E(A, B)$ for an electron to go from A to B, but says that that function is too complicated, and gives no intuition unlike the photon one.

  He does not mention it, but P and E are the so called [propagators](#propagator).

  This is likely the [path integral formulation](#path-integral-formulation) of QED.

  On [Quantum Mechanical View of Reality by Richard Feynman (1983)](#quantum-mechanical-view-of-reality-by-richard-feynman-1983) he mentions that $E$ is a [Bessel function](calculus.md#bessel-function), without giving further detail.

  And also mentions that:

  $$
  E = f(1, 2, m) \\
  P = f(1, 2, 0)
  $$

  where `m` is basically a scale factor.  
  such that both are very similar. And that something similar holds for many other particles.

  And then, when you draw a [Feynman diagram](#feynman-diagram), e.g. electron emits photon and both are detected at given positions, you sum over all the possibilities, each amplitude is given by:

  $$
  c \times E(A, D) \times E(D, B) \times P(B, C)
  $$

  summed over all possible $D$ [Spacetime](relativity.md#spacetime) points.

  This is basically well said at: [https://youtu.be/rZvgGekvHes?t=3349](https://youtu.be/rZvgGekvHes?t=3349) from [Quantum Mechanical View of Reality by Richard Feynman (1983)](#quantum-mechanical-view-of-reality-by-richard-feynman-1983).

  TODO: how do electron velocities affect where they are likely to end up? $E(A, D)$ suggests the probability only depends on the spacetime points.

  Also, this clarifies why computations in QED are so insane: you have to sum over every possible point in space!!! TODO but then how do we calculate anything at all in practice?
- Part 4: known problems with QED and thoughts on QCD. Boring.
This talk has the merit of being very experiment oriented on part 2, big kudos: [how to teach and learn physics](physics.md#how-to-teach-and-learn-physics)

<a id="video-richard-feynman-quantum-electrodynamics-lecture-at-university-of-auckland-1979-uploaded-by-trev-m-2015"></a>
**[Video 18](#video-richard-feynman-quantum-electrodynamics-lecture-at-university-of-auckland-1979-uploaded-by-trev-m-2015). Richard Feynman Quantum Electrodynamics Lecture at University of Auckland (1979) uploaded by Trev M (2015)** [Source](https://www.youtube.com/watch?v=Alj6q4Y0TNE). Single upload version. Let's use this one for the timestamps I guess.
- [https://youtu.be/Alj6q4Y0TNE?t=2217](https://youtu.be/Alj6q4Y0TNE?t=2217): [photomultiplier tube](photon.md#photomultiplier-tube)
- [https://youtu.be/Alj6q4Y0TNE?t=2410](https://youtu.be/Alj6q4Y0TNE?t=2410): [local hidden-variable theory](quantum-mechanics.md#local-hidden-variable-theory)
- [https://youtu.be/Alj6q4Y0TNE?t=6444](https://youtu.be/Alj6q4Y0TNE?t=6444): mirror experiment shown at [https://en.wikipedia.org/w/index.php?title=Quantum_electrodynamics&oldid=991301352#Probability_amplitudes](https://en.wikipedia.org/w/index.php?title=Quantum_electrodynamics&oldid=991301352#Probability_amplitudes)
- [https://youtu.be/Alj6q4Y0TNE?t=7309](https://youtu.be/Alj6q4Y0TNE?t=7309): mirror experiment with a [diffraction grating](photon.md#diffraction-grating) pattern painted black leads to reflection at a weird angle
- [https://youtu.be/Alj6q4Y0TNE?t=7627](https://youtu.be/Alj6q4Y0TNE?t=7627): detector under water to explain [refraction](calculus.md#refraction)
- [https://youtu.be/Alj6q4Y0TNE?t=8050](https://youtu.be/Alj6q4Y0TNE?t=8050): explains [biconvex spherical lens](photon.md#biconvex-spherical-lens) in terms of minimal times
- [https://youtu.be/Alj6q4Y0TNE?t=8402](https://youtu.be/Alj6q4Y0TNE?t=8402): mentions that for events in a series, you multiply the complex number of each step
- [https://youtu.be/Alj6q4Y0TNE?t=9270](https://youtu.be/Alj6q4Y0TNE?t=9270): mentions that the up to this point, ignored:
  - amplitude shrinks down with distance
  - [photon polarization](photon.md#photon-polarization)

  but it should not be too hard to add those
- [https://youtu.be/Alj6q4Y0TNE?t=11697](https://youtu.be/Alj6q4Y0TNE?t=11697): finally starts electron interaction. First point is to add time of event detection.
- [https://youtu.be/Alj6q4Y0TNE?t=13704](https://youtu.be/Alj6q4Y0TNE?t=13704): electron between plates, and mentions the word [action](mechanics.md#action-physics), without giving a clear enough idea of what it is unfortunately
- [https://youtu.be/Alj6q4Y0TNE?t=14467](https://youtu.be/Alj6q4Y0TNE?t=14467): mentions [positrons](standard-model.md#positron) going back in time, but does not clarify it well enough
- [https://youtu.be/Alj6q4Y0TNE?t=16614](https://youtu.be/Alj6q4Y0TNE?t=16614): on the fourth part, half is about frontiers in [quantum electrodynamics](#quantum-electrodynamics), and half full blown [theory of everything](standard-model.md#theory-of-everything). The QED part goes into [renormalization](#renormalization) and the large number of parameters of the [Standard Model](standard-model.md)

---

<a id="video-richard-feynman-lecture-on-quantum-electrodynamics-1-8"></a>
**[Video 19](#video-richard-feynman-lecture-on-quantum-electrodynamics-1-8). Richard Feynman Lecture on Quantum Electrodynamics 1/8.** [Source](https://www.youtube.com/watch?v=LPDP_8X5Hug).

##### Quantum Mechanical View of Reality by Richard Feynman (1983)

↑ **Parent:** [Richard Feynman Quantum Electrodynamics Lecture at University of Auckland (1979)](#richard-feynman-quantum-electrodynamics-lecture-at-university-of-auckland-1979)

Sample playlist: [https://www.youtube.com/playlist?list=PLW_HsOU6YZRkdhFFznHNEfua9NK3deBQy](https://www.youtube.com/playlist?list=PLW_HsOU6YZRkdhFFznHNEfua9NK3deBQy)

Basically the same content as: [Richard Feynman Quantum Electrodynamics Lecture at University of Auckland (1979)](#richard-feynman-quantum-electrodynamics-lecture-at-university-of-auckland-1979), but maybe there is some merit to this talk, as it is a bit more direct in some points. This is consistent with what is mentioned at [http://www.feynman.com/science/qed-lectures-in-new-zealand/](http://www.feynman.com/science/qed-lectures-in-new-zealand/) that the Auckland lecture was the first attempt.

Some more information at: [https://iucat.iu.edu/iub/5327621](https://iucat.iu.edu/iub/5327621)

By Mill Valley, CA based producer "Sound Photosynthesis", some info on their website: [http://sound.photosynthesis.com/Richard_Feynman.html](http://sound.photosynthesis.com/Richard_Feynman.html)

They are mostly a [New Age](religion.md#new-age) production company it seems, which highlights Feynman's absolute cult status. E.g. on the last video, he's not wearing shoes, like a proper guru.

Feynman liked to meet all kinds of weird people, and at some point he got interested in the [New Age](religion.md#new-age) [Esalen Institute](religion.md#esalen-institute). [Surely You're Joking, Mr. Feynman](surely-you-re-joking-mr-feynman.md) this kind of experience a bit, there was nude bathing on a pool that oversaw the sea, and a guy offered to give a massage to the he nude girl and the accepted.

[https://youtu.be/rZvgGekvHest=5105](https://youtu.be/rZvgGekvHest=5105) actually talks about [spin](relativistic-quantum-mechanics.md#spin-physics), notably that the endpoint events also have a spin, and that the transition rules take spin into account by rotating thing, and that the transition rules take spin into account by rotating things.

#### Quantum electrodynamics by Lifshitz et al. 2nd edition (1982)

↑ **Parent:** [Quantum electrodynamics bibliography](#quantum-electrodynamics-bibliography)

#### Physics 253a by Sidney Coleman (1986)

↑ **Parent:** [Quantum electrodynamics bibliography](#quantum-electrodynamics-bibliography)

#### QED and the men who made it: Dyson, Feynman, Schwinger, and Tomonaga by Silvan Schweber (1994)

↑ **Parent:** [Quantum electrodynamics bibliography](#quantum-electrodynamics-bibliography)

Available for [free](economy.md#free) [online](computer.md#internet) [rent](economy.md#renting) on the [Internet Archive](website.md#internet-archive): [https://archive.org/details/qedmenwhomadeitd0000schw](https://archive.org/details/qedmenwhomadeitd0000schw)

This book has formulas on it, which is quite cool!! And the formulas are basically not understandable unless you know the subject pretty well already in advance. It is however possible to skip over them and get back to the little personal stories.

#### Advanced quantum mechanics II by Douglas Gingrich (2004)

↑ **Parent:** [Quantum electrodynamics bibliography](#quantum-electrodynamics-bibliography)

[https://sites.ualberta.ca/~gingrich/courses/phys512/phys512.html](https://sites.ualberta.ca/~gingrich/courses/phys512/phys512.html)

From [University of Alberta](university.md#university-of-alberta).

## Weak interaction

↑ **Parent:** [Quantum field theory](quantum-field-theory.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Weak_interaction)

Explains [beta decay](particle-physics.md#beta-decay). TODO why/how.

Maybe a good view of why this force was needed given [beta decay](particle-physics.md#beta-decay) experiments is: in beta decay, a [neutron](standard-model.md#neutron) is getting split up into an [electron](standard-model.md#electron) and a [proton](standard-model.md#proton). Therefore, those charges must be contained inside the neutron somehow to start with. But then what could possibly make a positive and a negative particle separate?
- the [electromagnetic force](electromagnetism.md) should hold them together
- the [strong force](#strong-interaction) seems to hold positive charges together. Could it then be pushing opposite-charges apart? Why not? In any case this force doesn't seem to act on [electrons](standard-model.md#electron), only [quarks](#quark).
- [gravity](relativity.md#gravity) is too weak

[http://www.thestargarden.co.uk/Weak-nuclear-force.html](http://www.thestargarden.co.uk/Weak-nuclear-force.html) gives a quick and dirty:

> Beta decay could not be explained by the strong nuclear force, the force that's responsible for holding the atomic nucleus together, because this force doesn't affect electrons. It couldn't be explained by the electromagnetic force, because this does not affect [neutrons](standard-model.md#neutron), and the force of [gravity](relativity.md#gravity) is far too weak to be responsible. Since this new atomic force was not as strong as the strong nuclear force, it was dubbed the weak nuclear force.

Also interesting:

> While the photon 'carries' charge, and therefore mediates the [electromagnetic force](electromagnetism.md), the [Z](#z-boson) and [W](#w-boson) [bosons](relativistic-quantum-mechanics.md#boson) are said to carry a property known as 'weak isospin'. [W bosons](#w-boson) mediate the weak force when particles with charge are involved, and [Z bosons](#z-boson) mediate the weak force when neutral particles are involved.

<a id="video-weak-nuclear-force-and-standard-model-of-particle-physics-by-physics-videos-by-eugene-khutoryansky-2018"></a>
**[Video 20](#video-weak-nuclear-force-and-standard-model-of-particle-physics-by-physics-videos-by-eugene-khutoryansky-2018). Weak Nuclear Force and Standard Model of particle physics by Physics Videos by Eugene Khutoryansky (2018)** [Source](https://www.youtube.com/watch?v=iIWTRwJlrGo). Some decent visualizations of the field lines.

Bibliography:
- [https://physics.stackexchange.com/questions/562319/what-exactly-does-the-weak-force-do](https://physics.stackexchange.com/questions/562319/what-exactly-does-the-weak-force-do)
- [https://www.reddit.com/r/AskPhysics/comments/fnjziz/what_exactly_is_the_weak_interactionforce/](https://www.reddit.com/r/AskPhysics/comments/fnjziz/what_exactly_is_the_weak_interactionforce/)

### Electroweak interaction

↑ **Parent:** [Weak interaction](#weak-interaction)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Electroweak_interaction)

<a id="video-electroweak-theory-and-the-origin-of-the-fundamental-forces-by-pbs-space-time-2020"></a>
**[Video 21](#video-electroweak-theory-and-the-origin-of-the-fundamental-forces-by-pbs-space-time-2020). Electroweak Theory and the Origin of the Fundamental Forces by PBS Space Time (2020)** [Source](https://www.youtube.com/watch?v=qKVpknSKgE0). [Unsatisfactory](ciro-santilli.md#the-missing-link-between-basic-and-advanced), as usual.

### Parity violation

↑ **Parent:** [Weak interaction](#weak-interaction)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Parity_violation)

This is quite [mind blowing](brain.md#mind-blown). The [laws of physics](physics.md#law-of-physics) actually differentiate between particles and [antiparticles](relativistic-quantum-mechanics.md#antimatter) moving in opposite directions!!!

Only the [weak interaction](#weak-interaction) however does it of the [fundamental interactions](standard-model.md#fundamental-interaction).

Some historical remarks on [Surely You're Joking, Mr. Feynman](surely-you-re-joking-mr-feynman.md) section "The 7 Percent Solution".

It gets worse of course with [CP Violation](#cp-violation).

<a id="video-this-particle-breaks-time-symmetry-by-veritasium"></a>
**[Video 22](#video-this-particle-breaks-time-symmetry-by-veritasium). This Particle Breaks Time Symmetry by Veritasium.** [Source](https://www.youtube.com/watch?v=yArprk0q9eE).

#### Wu experiment

↑ **Parent:** [Parity violation](#parity-violation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Wu_experiment)

#### CP Violation

↑ **Parent:** [Parity violation](#parity-violation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/CP_Violation)

##### CPT symmetry

↑ **Parent:** [CP Violation](#cp-violation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/CPT_symmetry)

##### Strong CP problem

↑ **Parent:** [CP Violation](#cp-violation)  
🏷️ **Tags:** [Unsolved physics problem](physics.md#unsolved-physics-problem)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Strong_CP_problem)

### Weak charge

↑ **Parent:** [Weak interaction](#weak-interaction)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Weak_charge)

### W boson

↑ **Parent:** [Weak interaction](#weak-interaction)  
🏷️ **Tags:** [Elementary particle](standard-model.md#elementary-particle)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/W_boson)

### Z boson

↑ **Parent:** [Weak interaction](#weak-interaction)  
🏷️ **Tags:** [Elementary particle](standard-model.md#elementary-particle)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Z_boson)

## Quantum chromodynamics

↑ **Parent:** [Quantum field theory](quantum-field-theory.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Quantum_chromodynamics)

Formulated as a [quantum field theory](quantum-field-theory.md).

<a id="video-quarks-gluon-flux-tubes-strong-nuclear-force-and-quantum-chromodynamics-by-physics-videos-by-eugene-khutoryansky-2018"></a>
**[Video 23](#video-quarks-gluon-flux-tubes-strong-nuclear-force-and-quantum-chromodynamics-by-physics-videos-by-eugene-khutoryansky-2018). Quarks, Gluon flux tubes, Strong Nuclear Force, & Quantum Chromodynamics by Physics Videos by Eugene Khutoryansky (2018)** [Source](http://youtube.com/watch?v=FoR3hq5b5yE). Some decent visualizations of how the field lines don't expand out like they do in [electromagnetism](electromagnetism.md), suggesting [color confinement](#color-confinement).

<a id="video-phys-485-lecture-6-feynman-diagrams-by-roger-moore-2016"></a>
**[Video 24](#video-phys-485-lecture-6-feynman-diagrams-by-roger-moore-2016). PHYS 485 Lecture 6: Feynman Diagrams by Roger Moore (2016)** [Source](https://www.youtube.com/watch?v=LqUgzxJ8Jss). Despite the title, this is mostly about QCD.

### Quark

↑ **Parent:** [Quantum chromodynamics](#quantum-chromodynamics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Quark)

TODO experimental discovery.

#### Down quark

↑ **Parent:** [Quark](#quark)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Down_quark)

#### Up quark

↑ **Parent:** [Quark](#quark)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Up_quark)

##### Why do the up ad down quarks have different masses?

↑ **Parent:** [Up quark](#up-quark)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Why_do_the_up_ad_down_quarks_have_different_masses?)

[https://www.quora.com/Why-do-up-quarks-and-down-quarks-have-different-charges](https://www.quora.com/Why-do-up-quarks-and-down-quarks-have-different-charges)

### Strange quark

↑ **Parent:** [Quantum chromodynamics](#quantum-chromodynamics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Strange_quark)

### Gluon

↑ **Parent:** [Quantum chromodynamics](#quantum-chromodynamics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Gluon)

Force carrier of [quantum chromodynamics](#quantum-chromodynamics), like the [photon](photon.md) is the force carrier of [quantum electrodynamics](#quantum-electrodynamics).

One big difference is that it carrier itself [color charge](#color-charge).

#### Glueball

↑ **Parent:** [Gluon](#gluon)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Glueball)

### Proton decay

↑ **Parent:** [Quantum chromodynamics](#quantum-chromodynamics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Proton_decay)

### Strong interaction

↑ **Parent:** [Quantum chromodynamics](#quantum-chromodynamics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Strong_interaction)

### Color charge

↑ **Parent:** [Quantum chromodynamics](#quantum-chromodynamics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Color_charge)

### Color confinement

↑ **Parent:** [Quantum chromodynamics](#quantum-chromodynamics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Color_confinement)

Can be thought as being produced from [gluon](#gluon)-gluon lines of the [Feynman diagrams](#feynman-diagram) of [quantum chromodynamics](#quantum-chromodynamics). This is in contrast to [quantum electrodynamics](#quantum-electrodynamics), in which there are no [photon](photon.md)-photon vertices, because the photon does not have charge unlike gluons.

This phenomena makes the strong force be very very different from electromagnetism.

## Quantum field theory simulations

↑ **Parent:** [Quantum field theory](quantum-field-theory.md)

TODO why is it so hard to find anything non perturbative :-(

- [https://www.youtube.com/channel/UCPHFUHiwbpMqC8ONxEICCiQ](https://www.youtube.com/channel/UCPHFUHiwbpMqC8ONxEICCiQ) NanoNebula using raw [Perl](programming-language.md#perl-programming-language) PDFL [https://en.wikipedia.org/wiki/Perl_Data_Language](https://en.wikipedia.org/wiki/Perl_Data_Language) (the Perl [NumPy](programming-language.md#numpy))
- [https://www.youtube.com/watch?v=9TJe1Pr5c9Q](https://www.youtube.com/watch?v=9TJe1Pr5c9Q) "Interplay of Quantum Electrodynamics and Quantum Chromodynamics in the Nontrivial Vacuum" by CSSM Visualisation (2019)

On a [quantum computer](quantum-computing.md)...:
- [https://www.cornell.edu/video/john-preskill-simulating-quantum-field-theory-with-quantum-computer](https://www.cornell.edu/video/john-preskill-simulating-quantum-field-theory-with-quantum-computer) Simulating Quantum Field Theory with a Quantum Computer by John Preskill (2019)
- [https://www.youtube.com/watch?v=Lln-C21u0U8](https://www.youtube.com/watch?v=Lln-C21u0U8) Quantum Simulation from Quantum Chemistry to Quantum Field Theory by Peter Love (2019)

<a id="video-are-we-living-in-the-matrix-by-david-tong-2020"></a>
**[Video 25](#video-are-we-living-in-the-matrix-by-david-tong-2020). Are we living in the matrix? by David Tong (2020)** [Source](https://www.youtube.com/watch?v=QPMn7SuiHP8). Talks about how the [Nielsen-Ninomiya theorem](#nielsen-ninomiya-theorem) means it is impossible to simulate [QFT](quantum-field-theory.md) on a computer in the case of a [lattice gauge theory](#lattice-gauge-theory).

### Nielsen-Ninomiya theorem

↑ **Parent:** [Quantum field theory simulations](#quantum-field-theory-simulations)  
🏷️ **Tags:** [No-go theorem](quantum-mechanics.md#no-go-theorem)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Nielsen–Ninomiya_theorem)

As mentioned at [Video 25. "Are we living in the matrix? by David Tong (2020)"](#video-are-we-living-in-the-matrix-by-david-tong-2020) somehow implies that it is difficult or impossible to simulate physics on a computer. Big news!!!

## Infinities in quantum field theory

↑ **Parent:** [Quantum field theory](quantum-field-theory.md)

TODO concrete example, please...
- [https://physics.stackexchange.com/questions/310496/what-is-the-infinity-that-strikes-quantum-field-theory](https://physics.stackexchange.com/questions/310496/what-is-the-infinity-that-strikes-quantum-field-theory)
- [QED and the men who made it: Dyson, Feynman, Schwinger, and Tomonaga by Silvan Schweber (1994)](#qed-and-the-men-who-made-it-dyson-feynman-schwinger-and-tomonaga-by-silvan-schweber-1994) chapter 2.5 "The Divergences" contains a specific example by [Pascual Jordan](physicist.md#pascual-jordan)

### Mathematical consistency of quantum field theory

↑ **Parent:** [Infinities in quantum field theory](#infinities-in-quantum-field-theory)

[https://physics.stackexchange.com/questions/16142/is-qft-mathematically-self-consistent](https://physics.stackexchange.com/questions/16142/is-qft-mathematically-self-consistent)

## Internal and spacetime symmetries

↑ **Parent:** [Quantum field theory](quantum-field-theory.md)

[https://physics.stackexchange.com/questions/106392/internal-and-spacetime-symmetries](https://physics.stackexchange.com/questions/106392/internal-and-spacetime-symmetries)

The different only shows up for [field](physics.md#field-physics), not with particles. For fields, there are two types of changes that we can make that can keep the [Lagrangian](mechanics.md#lagrangian) unchanged as mentioned at [Physics from Symmetry by Jakob Schwichtenberg (2015)](physicist.md#physics-from-symmetry-by-jakob-schwichtenberg-2015) chapter "4.5.2 Noether's Theorem for Field Theories - Spacetime":
- [spacetime symmetry](#spacetime-symmetry): act with the [Poincaré group](geometry.md#poincare-group) on the [Four-vector](relativity.md#four-vector) spacetime inputs of the field itself, i.e. transforming $L(\Phi(x), \partial \Phi(x), dx)$ into $L(\Phi'(x'), \partial \Phi'(x'), x')$
- [internal symmetry](#internal-symmetry): act on the output of the  field, i.e.: $L(\Phi(x) + \delta \Phi(x), \partial (\Phi(x) + \delta \Phi(x)), x)$

From [defining properties of elementary particles](standard-model.md#defining-properties-of-elementary-particles):
- spacetime:
  - [mass](mechanics.md#mass)
  - [spin](relativistic-quantum-mechanics.md#spin-physics)
- internal
  - [electric charge](electromagnetism.md#electric-charge)
  - [Weak charge](#weak-charge)
  - [color charge](#color-charge)

From the spacetime theory alone, we can derive the [Lagrangian](mechanics.md#lagrangian) for the free theories for each [spin](relativistic-quantum-mechanics.md#spin-physics):
- [spin 0](relativistic-quantum-mechanics.md#spin-0): [Klein-Gordon equation](relativistic-quantum-mechanics.md#klein-gordon-equation)
- [spin half](relativistic-quantum-mechanics.md#spin-half): [Dirac equation](relativistic-quantum-mechanics.md#dirac-equation)
- [spin 1](relativistic-quantum-mechanics.md#spin-1): [Proca equation](relativistic-quantum-mechanics.md#proca-equation)
Then the internal symmetries are what add the interaction part of the [Lagrangian](mechanics.md#lagrangian), which then completes the [Standard Model Lagrangian](standard-model.md#standard-model-lagrangian).

### Internal symmetry

↑ **Parent:** [Internal and spacetime symmetries](#internal-and-spacetime-symmetries)

See: [internal and spacetime symmetries](#internal-and-spacetime-symmetries).

### Spacetime symmetry

↑ **Parent:** [Internal and spacetime symmetries](#internal-and-spacetime-symmetries)

See: [internal and spacetime symmetries](#internal-and-spacetime-symmetries).

## Quantum field theory bibliography

↑ **Parent:** [Quantum field theory](quantum-field-theory.md)

[Ciro Santilli](ciro-santilli.md)'s favorites so far:
- [Physics from Symmetry by Jakob Schwichtenberg (2015)](physicist.md#physics-from-symmetry-by-jakob-schwichtenberg-2015)

Bibliography of the biliograpy:
- [https://physics.stackexchange.com/questions/8441/what-is-a-complete-book-for-introductory-quantum-field-theory](https://physics.stackexchange.com/questions/8441/what-is-a-complete-book-for-introductory-quantum-field-theory) "What is a complete book for introductory quantum field theory?"
- [https://www.quora.com/What-is-the-best-book-to-learn-quantum-field-theory-on-your-own](https://www.quora.com/What-is-the-best-book-to-learn-quantum-field-theory-on-your-own) on [Quora](website.md#quora)
- [https://www.amazon.co.uk/Lectures-Quantum-Field-Theory-Ashok-ebook/dp/B07CL8Y3KY](https://www.amazon.co.uk/Lectures-Quantum-Field-Theory-Ashok-ebook/dp/B07CL8Y3KY)

Recommendations by friend P. C.:
- The Global Approach to Quantum Field Theory
- Lecture Notes | Geometry and Quantum Field Theory | Mathematics [https://ocw.mit.edu/courses/mathematics/18-238-geometry-and-quantum-field-theory-fall-2002/lecture-notes/](https://ocw.mit.edu/courses/mathematics/18-238-geometry-and-quantum-field-theory-fall-2002/lecture-notes/)
- Towards the mathematics of quantum field theory (Frederic Paugam)
- Path Integrals in Quantum Mechanics (J. Zinn–Justin)
- (B.Hall) Quantum Theory for Mathematicians (B.Hall)
- Quantum Field Theory and the Standard Model (Schwartz)
- The Algebra of Grand Unified Theories ([John C. Baez](physicist.md#john-c-baez))
- [quantum Field Theory for The Gifted Amateur by Tom Lancaster (2015)](#quantum-field-theory-for-the-gifted-amateur-by-tom-lancaster-2015)

### Quantum field theory lecture notes

↑ **Parent:** [Quantum field theory bibliography](#quantum-field-theory-bibliography)

Lecture notes found by [Googling](google.md) "quantum field theory pdf":
- [https://www.ppd.stfc.ac.uk/Pages/Dasgupta_08_Intro_to_QFT.pdf](https://www.ppd.stfc.ac.uk/Pages/Dasgupta_08_Intro_to_QFT.pdf) "An Introduction to Quantum Field Theory" by Mrinal Dasgupta from the University of Manchester (2008). 48 pages.
- [https://www.thphys.uni-heidelberg.de/~weigand/QFT2-14/SkriptQFT2.pdf](https://www.thphys.uni-heidelberg.de/~weigand/QFT2-14/SkriptQFT2.pdf) "Quantum Field Theory I + II" by Timo Weigand from the Heidelberg University. Unknown year, references up to 2008.
- [https://edu.itp.phys.ethz.ch/hs12/qft1/](https://edu.itp.phys.ethz.ch/hs12/qft1/) Quantum Field Theory 1 by Niklas Beisert

#### An Introduction to QED and QCD by Jeff Forshaw (1997)

↑ **Parent:** [Quantum field theory lecture notes](#quantum-field-theory-lecture-notes)

[http://www.hep.man.ac.uk/u/forshaw/NorthWest/QED.pdf](http://www.hep.man.ac.uk/u/forshaw/NorthWest/QED.pdf) [https://web.archive.org/web/20200824083133/http://www.hep.man.ac.uk/u/forshaw/NorthWest/QED.pdf](https://web.archive.org/web/20200824083133/http://www.hep.man.ac.uk/u/forshaw/NorthWest/QED.pdf)

These seem very direct and not ultra advanced, good read.

#### Quantum Field Theory lecture notes by David Tong (2007)

↑ **Parent:** [Quantum field theory lecture notes](#quantum-field-theory-lecture-notes)  
🏷️ **Tags:** [David Tong](physicist.md#david-tong)

[https://www.damtp.cam.ac.uk/user/tong/qft/qft.pdf](https://www.damtp.cam.ac.uk/user/tong/qft/qft.pdf)

Author: [David Tong](physicist.md#david-tong).

Number of pages circa 2021: 155.

It should also be noted that those notes are still being updated circa 2020 much after original publication. But without [Git](software.md#git) to track the [LaTeX](computer.md#latex), it is hard to be sure how much. [We'll get there one day, one day](ourbigbook-com.md).

Likely used at: [David Tong's 2009 Quantum Field Theory lectures at the Perimeter Institute](#david-tong-s-2009-quantum-field-theory-lectures-at-the-perimeter-institute).

Some quotes self describing the work:
- > [an Introduction To Quantum Field Theory by Peskin and Schroeder (1995)](#an-introduction-to-quantum-field-theory-by-peskin-and-schroeder-1995)
  > 
  > This is a very clear and comprehensive book, covering everything in this course at the right level. To a large extent, our course will follow the first section of this book.

  Perhaps for this reason [Ciro Santilli](ciro-santilli.md) was not able to get as much as he'd out of those notes either. This is not to say that the notes are bad, just not what Ciro needed, much like P&S:
  - [the missing link between basic and advanced](ciro-santilli.md#the-missing-link-between-basic-and-advanced)
  - [doing physics means calculating a number](physics.md#doing-physics-means-calculating-a-number)
- > In this course we will not discuss [path integral methods](#path-integral-formulation), and focus instead on [canonical quantization](#canonical-quantization).

A follow up course in the [University of Cambridge](university.md#university-of-cambridge) seems to be the "Advanced QFT course" (AQFT, Quantum field theory II) by David Skinner: [http://www.damtp.cam.ac.uk/user/dbs26/AQFT.html](http://www.damtp.cam.ac.uk/user/dbs26/AQFT.html)

#### Quantum Field Theory book by Mark Srednicki (2006)

↑ **Parent:** [Quantum field theory lecture notes](#quantum-field-theory-lecture-notes)

Free to view draft: [https://web.physics.ucsb.edu/~mark/ms-qft-DRAFT.pdf](https://web.physics.ucsb.edu/~mark/ms-qft-DRAFT.pdf) Page presenting it: [http://web.physics.ucsb.edu/~mark/qft.html](http://web.physics.ucsb.edu/~mark/qft.html)

Author affiliation: University of California, Santa Barbara.

Number of pages: 616!

Don't redistribute clause, and final version by Cambridge University Press, alas, so corrections will never be merged back: [http://web.physics.ucsb.edu/~mark/qft.html](http://web.physics.ucsb.edu/~mark/qft.html). But at least he's collecing erratas for the published (and therefore draft) versions there.

The book is top-level organized in spin 0, spin half, and spin 1. Quite ominous, really.

The preface states that one of its pedagogical philosophies is to "Illustration of the basic concepts with the simplest examples.", so maybe there is hope after all.

### Quantum field theory lectures

↑ **Parent:** [Quantum field theory bibliography](#quantum-field-theory-bibliography)

#### Relativistic Quantum Mechanics by Apoorva D Patel (2014)

↑ **Parent:** [Quantum field theory lectures](#quantum-field-theory-lectures)

[https://www.youtube.com/playlist?list=PLbMVogVj5nJTDMhThY9xu2Tvg0u1RPuxO](https://www.youtube.com/playlist?list=PLbMVogVj5nJTDMhThY9xu2Tvg0u1RPuxO)

45 1 hour lessons. The Indian traditional music opening is the best.

#### New Revolutions in Particle Physics by Leonard Susskind (2009)

↑ **Parent:** [Quantum field theory lectures](#quantum-field-theory-lectures)  
🏷️ **Tags:** [Lecture by Leonard Susskind](physicist.md#lecture-by-leonard-susskind)

[https://www.youtube.com/playlist?list=PL138995FAC49F5FB4](https://www.youtube.com/playlist?list=PL138995FAC49F5FB4)

10 2-hour lessons.

Lecturer: [Leonard Susskind](physicist.md#leonard-susskind).

<h4 id="david-tong-s-2009-quantum-field-theory-lectures-at-the-perimeter-institute">David Tong's 2009 Quantum Field Theory lectures at the Perimeter Institute</h4>

↑ **Parent:** [Quantum field theory lectures](#quantum-field-theory-lectures)  
🏷️ **Tags:** [David Tong](physicist.md#david-tong)

<a id="david-tong-s-2009-quantum-field-theory-lectures-at-the-perimeter-institute/_405"></a>
[https://www.youtube.com/playlist?list=PLaNkJORnlhZlVkrpQVvCTVvGAMIlXL88Y](https://www.youtube.com/playlist?list=PLaNkJORnlhZlVkrpQVvCTVvGAMIlXL88Y)

<a id="david-tong-s-2009-quantum-field-theory-lectures-at-the-perimeter-institute/_406"></a>
Lecture notes: [Quantum Field Theory lecture notes by David Tong (2007)](#quantum-field-theory-lecture-notes-by-david-tong-2007).

<a id="david-tong-s-2009-quantum-field-theory-lectures-at-the-perimeter-institute/_407"></a>
By [David Tong](physicist.md#david-tong).

<a id="david-tong-s-2009-quantum-field-theory-lectures-at-the-perimeter-institute/_408"></a>
14 1 hours 20 minute lectures.

<a id="david-tong-s-2009-quantum-field-theory-lectures-at-the-perimeter-institute/_409"></a>
The video resolution is extremely low, with images glued as he moves away from what he wrote :-) The beauty of the early [Internet](computer.md#internet).

<h5 id="david-tong-s-2009-quantum-field-theory-lectures-at-the-perimeter-institute/lecture-1">Lecture 1</h5>

↑ **Parent:** [David Tong's 2009 Quantum Field Theory lectures at the Perimeter Institute](#david-tong-s-2009-quantum-field-theory-lectures-at-the-perimeter-institute)

<a id="david-tong-s-2009-quantum-field-theory-lectures-at-the-perimeter-institute/_410"></a>
[https://www.youtube.com/watch?v=H3AFzbrqH68](https://www.youtube.com/watch?v=H3AFzbrqH68)

#### Quantum field theory courses by Tobias Osborne

↑ **Parent:** [Quantum field theory lectures](#quantum-field-theory-lectures)  
🏷️ **Tags:** [Tobias J. Osborne](physicist.md#tobias-j-osborne)

##### Quantum field theory lecture by Tobias Osborne (2017)

↑ **Parent:** [Quantum field theory courses by Tobias Osborne](#quantum-field-theory-courses-by-tobias-osborne)

<a id="quantum-field-theory-lecture-by-tobias-osborne-2017/_412"></a>
[https://www.youtube.com/playlist?list=PLDfPUNusx1EpRs-wku83aqYSKfR5fFmfS](https://www.youtube.com/playlist?list=PLDfPUNusx1EpRs-wku83aqYSKfR5fFmfS)

<a id="quantum-field-theory-lecture-by-tobias-osborne-2017/_413"></a>
This is a bit "[formal hocus pocus first, action later](physics.md#how-to-teach-and-learn-physics)". But withing that category, it is just barely basic enough that 2021 Ciro can understand something.

<a id="quantum-field-theory-lecture-by-tobias-osborne-2017/_414"></a>
By: [Tobias J. Osborne](physicist.md#tobias-j-osborne).

<a id="quantum-field-theory-lecture-by-tobias-osborne-2017/_415"></a>
Lecture notes transcribed by a student: [https://github.com/avstjohn/qft](https://github.com/avstjohn/qft)

<a id="quantum-field-theory-lecture-by-tobias-osborne-2017/_416"></a>
18 1h30 lectures.

<a id="quantum-field-theory-lecture-by-tobias-osborne-2017/_417"></a>
Followup course: [Advanced quantum field theory lecture by Tobias Osborne (2017)](#advanced-quantum-field-theory-lecture-by-tobias-osborne-2017).

<h6 id="quantum-field-theory-lecture-by-tobias-osborne-2017/lecture-1">Lecture 1</h6>

↑ **Parent:** [Quantum field theory lecture by Tobias Osborne (2017)](#quantum-field-theory-lecture-by-tobias-osborne-2017)

<a id="quantum-field-theory-lecture-by-tobias-osborne-2017/_418"></a>
[https://www.youtube.com/watch?v=T58H6ofIOpE](https://www.youtube.com/watch?v=T58H6ofIOpE)

<a id="quantum-field-theory-lecture-by-tobias-osborne-2017/_419"></a>
Bibliography review:<a id="quantum-field-theory-lecture-by-tobias-osborne-2017/_420"></a>

<a id="quantum-field-theory-lecture-by-tobias-osborne-2017/_421"></a>
- [Quantum Field Theory lecture notes by David Tong (2007)](#quantum-field-theory-lecture-notes-by-david-tong-2007) is the course basis
<a id="quantum-field-theory-lecture-by-tobias-osborne-2017/_422"></a>
- [quantum field theory in a nutshell by Anthony Zee (2010)](#quantum-field-theory-in-a-nutshell-by-anthony-zee-2010) is a good quick and dirty book to start

<a id="quantum-field-theory-lecture-by-tobias-osborne-2017/_423"></a>
Course outline given:<a id="quantum-field-theory-lecture-by-tobias-osborne-2017/_424"></a>

<a id="quantum-field-theory-lecture-by-tobias-osborne-2017/_425"></a>
- classical field theory
<a id="quantum-field-theory-lecture-by-tobias-osborne-2017/_426"></a>
- quantum scalar field. Covers [bosons](relativistic-quantum-mechanics.md#boson), and is simpler to get intuition about.
<a id="quantum-field-theory-lecture-by-tobias-osborne-2017/_427"></a>
- quantum Dirac field. Covers [fermions](relativistic-quantum-mechanics.md#fermion)
<a id="quantum-field-theory-lecture-by-tobias-osborne-2017/_428"></a>
- interacting fields
<a id="quantum-field-theory-lecture-by-tobias-osborne-2017/_429"></a>
- [perturbation theory](mathematics.md#perturbation-theory)
<a id="quantum-field-theory-lecture-by-tobias-osborne-2017/_430"></a>
- [renormalization](#renormalization)

<a id="quantum-field-theory-lecture-by-tobias-osborne-2017/_431"></a>
Non-relativistic [QFT](quantum-field-theory.md) is a limit of relativistic QFT, and can be used to describe for example [condensed matter physics](condensed-matter-physics.md) systems at very low temperature. But it is still very hard to make accurate measurements even in those experiments.

<a id="quantum-field-theory-lecture-by-tobias-osborne-2017/_432"></a>
Defines "relativistic" as: "the [Lagrangian](mechanics.md#lagrangian) is symmetric under the [Poincaré group](geometry.md#poincare-group)".

<a id="quantum-field-theory-lecture-by-tobias-osborne-2017/_433"></a>
Mentions that "QFT is hard" because (a finite list follows???):<a id="quantum-field-theory-lecture-by-tobias-osborne-2017/_434"></a>


> There are no nontrivial finite-dimensional unitary [representations](geometry.md#representation-theory) of the [Poincaré group](geometry.md#poincare-group).

But I guess that if you fully understand what that means precisely, QTF won't be too hard for you!

<a id="quantum-field-theory-lecture-by-tobias-osborne-2017/_435"></a>
Notably, this is stark contrast with rotation symmetry groups ([SO(3)](geometry.md#special-orthogonal-group)) which appears in space rotations present in [non-relativistic quantum mechanics](quantum-mechanics.md#non-relativistic-quantum-mechanics).

<a id="quantum-field-theory-lecture-by-tobias-osborne-2017/_436"></a>
[https://www.youtube.com/watch?v=T58H6ofIOpE&t=5097](https://www.youtube.com/watch?v=T58H6ofIOpE&t=5097) describes the [relativistic particle in a box thought experiment](relativistic-quantum-mechanics.md#relativistic-particle-in-a-box-thought-experiment) with shrinking walls

<h6 id="quantum-field-theory-lecture-by-tobias-osborne-2017/lecture-2">Lecture 2</h6>

↑ **Parent:** [Quantum field theory lecture by Tobias Osborne (2017)](#quantum-field-theory-lecture-by-tobias-osborne-2017)

<a id="quantum-field-theory-lecture-by-tobias-osborne-2017/_437"></a>
[https://www.youtube.com/watch?v=bTcFOE5vpOA&list=PLDfPUNusx1EpRs-wku83aqYSKfR5fFmfS&index=2](https://www.youtube.com/watch?v=bTcFOE5vpOA&list=PLDfPUNusx1EpRs-wku83aqYSKfR5fFmfS&index=2)

<a id="quantum-field-theory-lecture-by-tobias-osborne-2017/_438"></a>
<a id="quantum-field-theory-lecture-by-tobias-osborne-2017/_439"></a>
- the advantage of using [Lagrangian mechanics](mechanics.md#lagrangian-mechanics) instead of directly trying to work out the equations of motion is that it is easier to guess the Lagrangian correctly, while still imposing some fundamental constraints
<a id="quantum-field-theory-lecture-by-tobias-osborne-2017/_440"></a>
- [https://youtu.be/bTcFOE5vpOA?list=PLDfPUNusx1EpRs-wku83aqYSKfR5fFmfS&t=3375](https://youtu.be/bTcFOE5vpOA?list=PLDfPUNusx1EpRs-wku83aqYSKfR5fFmfS&t=3375)<a id="quantum-field-theory-lecture-by-tobias-osborne-2017/_441"></a>

  <a id="quantum-field-theory-lecture-by-tobias-osborne-2017/_442"></a>
  - [Lagrangian mechanics](mechanics.md#lagrangian-mechanics) is better for [path integral formulation](#path-integral-formulation). But the [mathematics](mathematics.md) of that is fuzzy, so not going in that path.
  <a id="quantum-field-theory-lecture-by-tobias-osborne-2017/_443"></a>
  - [Hamiltonian mechanics](mechanics.md#hamiltonian-mechanics) is better for non-[path integral formulation](#path-integral-formulation)
<a id="quantum-field-theory-lecture-by-tobias-osborne-2017/_444"></a>
- [https://youtu.be/bTcFOE5vpOA?list=PLDfPUNusx1EpRs-wku83aqYSKfR5fFmfS&t=3449](https://youtu.be/bTcFOE5vpOA?list=PLDfPUNusx1EpRs-wku83aqYSKfR5fFmfS&t=3449) Hamiltonian formalism requires finding conjugate pairs, and doing a 

<h6 id="quantum-field-theory-lecture-by-tobias-osborne-2017/lecture-3">Lecture 3</h6>

↑ **Parent:** [Quantum field theory lecture by Tobias Osborne (2017)](#quantum-field-theory-lecture-by-tobias-osborne-2017)

<a id="quantum-field-theory-lecture-by-tobias-osborne-2017/_445"></a>
[https://www.youtube.com/watch?v=cj-QpsZsDDY&list=PLDfPUNusx1EpRs-wku83aqYSKfR5fFmfS&index=3](https://www.youtube.com/watch?v=cj-QpsZsDDY&list=PLDfPUNusx1EpRs-wku83aqYSKfR5fFmfS&index=3)

<a id="quantum-field-theory-lecture-by-tobias-osborne-2017/_446"></a>
<a id="quantum-field-theory-lecture-by-tobias-osborne-2017/_447"></a>
- symmetry in classical field theory
<a id="quantum-field-theory-lecture-by-tobias-osborne-2017/_448"></a>
- from Lagrangian density we can algorithmically get equations of motion, but the Lagrangian density is a more compact way of representing the equations of motion
<a id="quantum-field-theory-lecture-by-tobias-osborne-2017/_449"></a>
- definition of symmetry in context: keeps Lagrangian unchanged up to a total derivative
<a id="quantum-field-theory-lecture-by-tobias-osborne-2017/_450"></a>
- [Noether's theorem](mechanics.md#noether-s-theorem)
<a id="quantum-field-theory-lecture-by-tobias-osborne-2017/_451"></a>
- [https://youtu.be/cj-QpsZsDDY?list=PLDfPUNusx1EpRs-wku83aqYSKfR5fFmfS&t=3062](https://youtu.be/cj-QpsZsDDY?list=PLDfPUNusx1EpRs-wku83aqYSKfR5fFmfS&t=3062) Lagrangian and conservation example under translations
<a id="quantum-field-theory-lecture-by-tobias-osborne-2017/_452"></a>
- [https://youtu.be/cj-QpsZsDDY?list=PLDfPUNusx1EpRs-wku83aqYSKfR5fFmfS&t=3394](https://youtu.be/cj-QpsZsDDY?list=PLDfPUNusx1EpRs-wku83aqYSKfR5fFmfS&t=3394) same but for [Poincaré transformations](geometry.md#poincare-group) But now things are harder, because it is harder to describe general infinitesimal Poincare transforms than it was to describe the translations. Using constraints/definition of Lorentz transforms, also constricts the allowed infinitesimal symmetries to 6 independent parameters
<a id="quantum-field-theory-lecture-by-tobias-osborne-2017/_453"></a>
- <a id="quantum-field-theory-lecture-by-tobias-osborne-2017/_454"></a>
  [https://youtu.be/cj-QpsZsDDY?list=PLDfPUNusx1EpRs-wku83aqYSKfR5fFmfS&t=4525](https://youtu.be/cj-QpsZsDDY?list=PLDfPUNusx1EpRs-wku83aqYSKfR5fFmfS&t=4525) brings out [Poisson brackets](mechanics.md#poisson-bracket), and concludes that each conserved current maps to a [generator of the Lie algebra](geometry.md#generator-of-a-lie-algebra)

  <a id="quantum-field-theory-lecture-by-tobias-osborne-2017/_455"></a>
  This allows you to build the symmetry back from the conserved charges, just as you can determine conserved charges starting from the symmetry.

<h6 id="quantum-field-theory-lecture-by-tobias-osborne-2017/lecture-4">Lecture 4</h6>

↑ **Parent:** [Quantum field theory lecture by Tobias Osborne (2017)](#quantum-field-theory-lecture-by-tobias-osborne-2017)

<a id="quantum-field-theory-lecture-by-tobias-osborne-2017/_456"></a>
[https://www.youtube.com/watch?v=fnMcaq6QqTY&list=PLDfPUNusx1EpRs-wku83aqYSKfR5fFmfS&index=4](https://www.youtube.com/watch?v=fnMcaq6QqTY&list=PLDfPUNusx1EpRs-wku83aqYSKfR5fFmfS&index=4)

<a id="quantum-field-theory-lecture-by-tobias-osborne-2017/_457"></a>
<a id="quantum-field-theory-lecture-by-tobias-osborne-2017/_458"></a>
- quantization. Uses a more or less standard way to guess the quantized system from the classical one using [Hamiltonian mechanics](mechanics.md#hamiltonian-mechanics).
<a id="quantum-field-theory-lecture-by-tobias-osborne-2017/_459"></a>
- [https://youtu.be/fnMcaq6QqTY?t=1179](https://youtu.be/fnMcaq6QqTY?t=1179) remembers how to solve the non-field [quantum harmonic oscillator](quantum-mechanics.md#quantum-harmonic-oscillator)
<a id="quantum-field-theory-lecture-by-tobias-osborne-2017/_460"></a>
- [https://youtu.be/fnMcaq6QqTY?t=2008](https://youtu.be/fnMcaq6QqTY?t=2008) puts hats on everything to make the field version of things. With the [Klein-Gordon equation](relativistic-quantum-mechanics.md#klein-gordon-equation) [Hamiltonian](mechanics.md#hamiltonian-mechanics), everything is analogous to the harmonic oscilator

<h6 id="quantum-field-theory-lecture-by-tobias-osborne-2017/lecture-5">Lecture 5</h6>

↑ **Parent:** [Quantum field theory lecture by Tobias Osborne (2017)](#quantum-field-theory-lecture-by-tobias-osborne-2017)

<a id="quantum-field-theory-lecture-by-tobias-osborne-2017/_461"></a>
[https://www.youtube.com/watch?v=fnMcaq6QqTY&list=PLDfPUNusx1EpRs-wku83aqYSKfR5fFmfS&index=5](https://www.youtube.com/watch?v=fnMcaq6QqTY&list=PLDfPUNusx1EpRs-wku83aqYSKfR5fFmfS&index=5)

<a id="quantum-field-theory-lecture-by-tobias-osborne-2017/_462"></a>
<a id="quantum-field-theory-lecture-by-tobias-osborne-2017/_463"></a>
- something about finding a unitary representation of the poincare group

<h6 id="quantum-field-theory-lecture-by-tobias-osborne-2017/lecture-8">Lecture 8</h6>

↑ **Parent:** [Quantum field theory lecture by Tobias Osborne (2017)](#quantum-field-theory-lecture-by-tobias-osborne-2017)

<a id="quantum-field-theory-lecture-by-tobias-osborne-2017/_464"></a>
[https://www.youtube.com/watch?v=ARes2YJNFds&list=PLDfPUNusx1EpRs-wku83aqYSKfR5fFmfS&index=8](https://www.youtube.com/watch?v=ARes2YJNFds&list=PLDfPUNusx1EpRs-wku83aqYSKfR5fFmfS&index=8)

<a id="quantum-field-theory-lecture-by-tobias-osborne-2017/_465"></a>
Interactions.

<h6 id="quantum-field-theory-lecture-by-tobias-osborne-2017/lecture-9">Lecture 9</h6>

↑ **Parent:** [Quantum field theory lecture by Tobias Osborne (2017)](#quantum-field-theory-lecture-by-tobias-osborne-2017)

<a id="quantum-field-theory-lecture-by-tobias-osborne-2017/_466"></a>
[https://www.youtube.com/watch?v=zSSjgG9AbgM&list=PLDfPUNusx1EpRs-wku83aqYSKfR5fFmfS&index=9](https://www.youtube.com/watch?v=zSSjgG9AbgM&list=PLDfPUNusx1EpRs-wku83aqYSKfR5fFmfS&index=9)

<a id="quantum-field-theory-lecture-by-tobias-osborne-2017/_467"></a>
[Feynman diagram](#feynman-diagram).

<h6 id="quantum-field-theory-lecture-by-tobias-osborne-2017/lecture-14">Lecture 14</h6>

↑ **Parent:** [Quantum field theory lecture by Tobias Osborne (2017)](#quantum-field-theory-lecture-by-tobias-osborne-2017)

<a id="quantum-field-theory-lecture-by-tobias-osborne-2017/_468"></a>
[https://www.youtube.com/watch?v=zSSjgG9AbgM&list=PLDfPUNusx1EpRs-wku83aqYSKfR5fFmfS&index=9](https://www.youtube.com/watch?v=zSSjgG9AbgM&list=PLDfPUNusx1EpRs-wku83aqYSKfR5fFmfS&index=9)

<a id="quantum-field-theory-lecture-by-tobias-osborne-2017/_469"></a>
Dirac field.

<h6 id="quantum-field-theory-lecture-by-tobias-osborne-2017/lecture-15">Lecture 15</h6>

↑ **Parent:** [Quantum field theory lecture by Tobias Osborne (2017)](#quantum-field-theory-lecture-by-tobias-osborne-2017)

<a id="quantum-field-theory-lecture-by-tobias-osborne-2017/_470"></a>
[https://www.youtube.com/watch?v=J2lV8uNx0LU&list=PLDfPUNusx1EpRs-wku83aqYSKfR5fFmfS&index=15](https://www.youtube.com/watch?v=J2lV8uNx0LU&list=PLDfPUNusx1EpRs-wku83aqYSKfR5fFmfS&index=15)

<a id="quantum-field-theory-lecture-by-tobias-osborne-2017/_471"></a>
Dirac equation.

##### Advanced quantum field theory lecture by Tobias Osborne (2017)

↑ **Parent:** [Quantum field theory courses by Tobias Osborne](#quantum-field-theory-courses-by-tobias-osborne)  
🏷️ **Tags:** [Tobias J. Osborne](physicist.md#tobias-j-osborne)

<a id="advanced-quantum-field-theory-lecture-by-tobias-osborne-2017/_473"></a>
[https://www.youtube.com/playlist?list=PLDfPUNusx1ErSu1JDVV1KKGQkJQCkzL9u](https://www.youtube.com/playlist?list=PLDfPUNusx1ErSu1JDVV1KKGQkJQCkzL9u)

<a id="advanced-quantum-field-theory-lecture-by-tobias-osborne-2017/_474"></a>
Followup to [Quantum field theory lecture by Tobias Osborne (2017)](#quantum-field-theory-lecture-by-tobias-osborne-2017).

<a id="advanced-quantum-field-theory-lecture-by-tobias-osborne-2017/_475"></a>
When the word "advanced" precedes QFT, you know that the brainrape is imminent!!!

<a id="advanced-quantum-field-theory-lecture-by-tobias-osborne-2017/_476"></a>
Big goal: explain the [Standard Model](standard-model.md).

<h6 id="advanced-quantum-field-theory-lecture-by-tobias-osborne-2017/lecture-2">Lecture 2</h6>

↑ **Parent:** [Advanced quantum field theory lecture by Tobias Osborne (2017)](#advanced-quantum-field-theory-lecture-by-tobias-osborne-2017)

<a id="advanced-quantum-field-theory-lecture-by-tobias-osborne-2017/_477"></a>
[https://www.youtube.com/watch?v=hapYr6rX4JM&list=PLDfPUNusx1ErSu1JDVV1KKGQkJQCkzL9u&index=2](https://www.youtube.com/watch?v=hapYr6rX4JM&list=PLDfPUNusx1ErSu1JDVV1KKGQkJQCkzL9u&index=2)

<a id="advanced-quantum-field-theory-lecture-by-tobias-osborne-2017/_478"></a>
Gaussian path integrals.

### Quantum field theory book

↑ **Parent:** [Quantum field theory bibliography](#quantum-field-theory-bibliography)

- [https://web.archive.org/web/20150623011722/http://users.physik.fu-berlin.de/~kleinert/b6/psfiles/qft.pdf](https://web.archive.org/web/20150623011722/http://users.physik.fu-berlin.de/~kleinert/b6/psfiles/qft.pdf) by [Hagen Kleinert](https://en.wikipedia.org/wiki/Hagen_Kleinert) (2015). 1500 pages!
- The Quantum Theory of Fields by Steven Weinberg (2013) [https://www.cambridge.org/core/books/quantum-theory-of-fields/22986119910BF6A2EFE42684801A3BDF](https://www.cambridge.org/core/books/quantum-theory-of-fields/22986119910BF6A2EFE42684801A3BDF) 
- Quantum Field Theory by Lewis H. Ryder 2nd edition (1996) [https://www.amazon.co.uk/Quantum-Field-Theory-Lewis-Ryder/dp/0521478146](https://www.amazon.co.uk/Quantum-Field-Theory-Lewis-Ryder/dp/0521478146)
- Lectures of Quantum Field Theory by Ashok Das (2018) [https://www.amazon.co.uk/Lectures-Quantum-Field-Theory-Ashok-ebook/dp/B07CL8Y3KY](https://www.amazon.co.uk/Lectures-Quantum-Field-Theory-Ashok-ebook/dp/B07CL8Y3KY)
- A Modern Introduction to Quantum Field Theory by Michele Maggiore (2005) [https://www.amazon.co.uk/Modern-Introduction-Quantum-Theory-Physics/dp/0198520743](https://www.amazon.co.uk/Modern-Introduction-Quantum-Theory-Physics/dp/0198520743)

#### No-Nonsense Quantum Field Theory by Jakob Schwichtenberg (2020)

↑ **Parent:** [Quantum field theory book](#quantum-field-theory-book)  
🏷️ **Tags:** [Jakob Schwichtenberg](physicist.md#jakob-schwichtenberg)

[https://www.amazon.com/No-Nonsense-Quantum-Field-Theory-Student-Friendly/dp/3948763011](https://www.amazon.com/No-Nonsense-Quantum-Field-Theory-Student-Friendly/dp/3948763011)

This book really tries to recall basic things to ensure that the reader will be able to understand the more advanced ones.

Sometimes it goes a little bit overboard, like defining what a [function](formalization-of-mathematics.md#function-mathematics) does several times.

But [Ciro Santilli](ciro-santilli.md) really prefers it when authors error on the side of obvious.

#### Quantum Field Theory for The Gifted Amateur by Tom Lancaster (2015)

↑ **Parent:** [Quantum field theory book](#quantum-field-theory-book)

[https://www.amazon.co.uk/Quantum-Field-Theory-Gifted-Amateur/dp/019969933X](https://www.amazon.co.uk/Quantum-Field-Theory-Gifted-Amateur/dp/019969933X)

People are mostly saying you have to be a more of a genius amateur to read it.

#### Student Friendly Quantum Field Theory by Robert D Klauber (2013)

↑ **Parent:** [Quantum field theory book](#quantum-field-theory-book)

[http://www.quantumfieldtheory.info/](http://www.quantumfieldtheory.info/)

[https://www.quora.com/Whats-an-expert-opinion-on-Robert-Klaubers-Student-Friendly-Quantum-Field-Theory](https://www.quora.com/Whats-an-expert-opinion-on-Robert-Klaubers-Student-Friendly-Quantum-Field-Theory)

[https://www.amazon.co.uk/Student-Friendly-Quantum-Field-Theory/dp/0984513957](https://www.amazon.co.uk/Student-Friendly-Quantum-Field-Theory/dp/0984513957)

#### Quantum field theory in a nutshell by Anthony Zee (2010)

↑ **Parent:** [Quantum field theory book](#quantum-field-theory-book)

Author: [https://en.wikipedia.org/wiki/Anthony_Zee](https://en.wikipedia.org/wiki/Anthony_Zee) from [University of California, Santa Barbara](university.md#university-of-california-santa-barbara).

ISBN-13: 978-0691140346

[Amazon](amazon.md): [https://www.amazon.com/dp/0691140340](https://www.amazon.com/dp/0691140340)

[lecture 1](#quantum-field-theory-lecture-by-tobias-osborne-2017/lecture-1) mentions that this book is quick and dirty, as one might guess from the title. [Ciro Santilli](ciro-santilli.md) thinks he's gonna like this one.

First edition: from 2003, [https://www.amazon.com/dp/0691010196](https://www.amazon.com/dp/0691010196), ISBN-13: 978-0691010199.

Summary:
- page 8: [infinitely many slits thought experiment](#infinitely-many-slits-thought-experiment)

#### Problem Book in Quantum Field Theory by Voja Radovanovic (2008)

↑ **Parent:** [Quantum field theory book](#quantum-field-theory-book)

[https://www.springer.com/gp/book/9783540770138](https://www.springer.com/gp/book/9783540770138)

#### Quantum Field Theory Demystified by David McMahon (2008)

↑ **Parent:** [Quantum field theory book](#quantum-field-theory-book)

This didn't really deliver. It does start from the basics, but it is often hard to link those basics to more interesting or deeper points. Also like many other [Quantum field theory book](#quantum-field-theory-book), it does not seem to contain a single comparison between a theoretical result and an experiment.

#### An Introduction To Quantum Field Theory by Peskin and Schroeder (1995)

↑ **Parent:** [Quantum field theory book](#quantum-field-theory-book)

[https://www.amazon.co.uk/Introduction-Quantum-Theory-Frontiers-Physics/dp/0201503972](https://www.amazon.co.uk/Introduction-Quantum-Theory-Frontiers-Physics/dp/0201503972)

This is very widely used in courses as of 2020, it became kind of the default book.

Unfortunately, this approach bores [Ciro Santilli](ciro-santilli.md) to death. Or perhaps is too [just advanced for him to appreciate](ciro-santilli.md#the-missing-link-between-basic-and-advanced). Either of those.

800+ pages.

## ↑ Ancestors (7)

1. [Relativistic quantum mechanics](relativistic-quantum-mechanics.md)
2. [Quantum mechanics](quantum-mechanics.md)
3. [Particle physics](particle-physics.md)
4. [Physics](physics.md)
5. [Natural science](science.md#natural-science)
6. [Science](science.md)
7. [Ciro Santilli's Homepage](README.md)

## ← Incoming links (21)

- [Coursera](website.md#coursera)
- [David Tong](physicist.md#david-tong)
- [EdX](website.md#edx)
- [Effective field theory](#effective-field-theory)
- [Generalized coordinate](mechanics.md#generalized-coordinate)
- [Infinitely many slits thought experiment](#infinitely-many-slits-thought-experiment)
- [Jazz fusion](music.md#jazz-fusion)
- [Lagrangian density](mechanics.md#lagrangian-density)
- [Lagrangian mechanics](mechanics.md#lagrangian-mechanics)
- [Luxury goods](art.md#luxury-goods)
- [Millennium Prize Problems](mathematics.md#millennium-prize-problems)
- [Perturbation theory](mathematics.md#perturbation-theory)
- [Physics education needs more focus on understanding experiments and their history](physics.md#physics-education-needs-more-focus-on-understanding-experiments-and-their-history)
- [Quantization of a real scalar field](quantum-mechanics.md#quantization-of-a-real-scalar-field)
- [Quantum chromodynamics](#quantum-chromodynamics)
- [Quantum electrodynamics](#quantum-electrodynamics)
- [Quantum Mechanics for Engineers by Leon van Dommelen (2011)](quantum-mechanics.md#quantum-mechanics-for-engineers-by-leon-van-dommelen-2011)
- [Second quantization](#second-quantization)
- [Solutions of the Schrodinger equation for two electrons](quantum-mechanics.md#solutions-of-the-schrodinger-equation-for-two-electrons)
- [The wave equation can be seen as infinitely many infinitesimal coupled oscillators](calculus.md#the-wave-equation-can-be-seen-as-infinitely-many-infinitesimal-coupled-oscillators)
- [What does it mean that photons are force carriers for electromagnetism?](#what-does-it-mean-that-photons-are-force-carriers-for-electromagnetism)
