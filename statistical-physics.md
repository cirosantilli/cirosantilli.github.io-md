# Statistical physics

↑ **Parent:** [Physics](physics.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Statistical_physics)

**Table of contents**

- [Statistical mechanics](#statistical-mechanics)
  - [Kinetic theory of gases](#kinetic-theory-of-gases)
  - [Statistical mechanics model](#statistical-mechanics-model)
    - [Percolation](#percolation)
      - [Percolation theory](#percolation-theory)
- [Sedimentation](#sedimentation)
- [Maxwell-Boltzmann vs Bose-Einstein vs Fermi-Dirac statistics](#maxwell-boltzmann-vs-bose-einstein-vs-fermi-dirac-statistics)
  - [Maxwell-Boltzmann distribution](#maxwell-boltzmann-distribution)
    - [Maxwell-Boltzmann statistics](#maxwell-boltzmann-statistics)
    - [Experimental verification of the Maxwell-Boltzmann distribution](#experimental-verification-of-the-maxwell-boltzmann-distribution)
      - [Zartman Ko experiment](#zartman-ko-experiment)
        - [Stern-Zartman experiment](#stern-zartman-experiment)
      - [Application of the Maxwell-Boltzmann distribution](#application-of-the-maxwell-boltzmann-distribution)
  - [Quantum statistics](#quantum-statistics)
    - [Bose-Einstein statistics](#bose-einstein-statistics)
    - [Fermi-Dirac statistics](#fermi-dirac-statistics)
      - [Quantum statistical mechanics](#quantum-statistical-mechanics)
- [Thermodynamics](#thermodynamics)
  - [Boltzmann constant](#boltzmann-constant)
  - [Equipartition theorem](#equipartition-theorem)
  - [Thermodynamic potential](#thermodynamic-potential)
    - [Enthalpy](#enthalpy)
    - [Gibbs free energy](#gibbs-free-energy)
      - [Chemical equilibrium](#chemical-equilibrium)
      - [Reversible reaction](#reversible-reaction)
  - [Equation of state](#equation-of-state)
    - [Ideal gas law](#ideal-gas-law)
      - [Monatomic gas](#monatomic-gas)
  - [Entropy](#entropy)
    - [Clausius entropy](#clausius-entropy)
      - [Carnot cycle](#carnot-cycle)
    - [Second law of thermodynamics](#second-law-of-thermodynamics)
      - [Time reversibility](#time-reversibility)
        - [Arrow of time](#arrow-of-time)
        - [Time reversibility of classical mechanics](#time-reversibility-of-classical-mechanics)
        - [Time reversibility of gravity](#time-reversibility-of-gravity)
  - [Phase (matter)](#phase-matter)
    - [List of phase transitions](#list-of-phase-transitions)
      - [Evaporation](#evaporation)
      - [Sublimation](#sublimation)
    - [Phase transition](#phase-transition)
      - [Phase diagram](#phase-diagram)
        - [Type of phase diagram](#type-of-phase-diagram)
          - [Temperature-pressure phase diagram](#temperature-pressure-phase-diagram)
          - [Composition phase diagram](#composition-phase-diagram)
            - [Temperature-composition phase diagram](#temperature-composition-phase-diagram)
        - [Triple point](#triple-point)
        - [Critical point (thermodynamics)](#critical-point-thermodynamics)
      - [Second-order phase transition](#second-order-phase-transition)
  - [Refrigerator](#refrigerator)
    - [Dilution refrigerator](#dilution-refrigerator)
      - [Cryogen-free dilution refrigerator](#cryogen-free-dilution-refrigerator)
      - [Dilution refrigerator manufacturer](#dilution-refrigerator-manufacturer)
        - [Bluefors](#bluefors)
  - [Temperature](#temperature)
    - [Standard temperature and pressure](#standard-temperature-and-pressure)
    - [Scale of temperature](#scale-of-temperature)
      - [Kelvin](#kelvin)
    - [Thermometer](#thermometer)
      - [Mercury-in-glass thermometer](#mercury-in-glass-thermometer)
  - [Vacuum](#vacuum)
    - [Vacuum engineering](#vacuum-engineering)
      - [Vacuum vendor](#vacuum-vendor)
        - [Edwards Vacuum](#edwards-vacuum)
      - [Ultra-high vacuum](#ultra-high-vacuum)

## Statistical mechanics

↑ **Parent:** [Statistical physics](statistical-physics.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Statistical_mechanics)

### Kinetic theory of gases

↑ **Parent:** [Statistical mechanics](#statistical-mechanics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Kinetic_theory_of_gases)

Theory that gases are made up of a bunch of small billiard balls that don't interact with each other.

This theory attempts to deduce/explain properties of matter such as the [equation of state](#equation-of-state) in terms of [classical mechanics](mechanics.md#classical-mechanics).

### Statistical mechanics model

↑ **Parent:** [Statistical mechanics](#statistical-mechanics)

#### Percolation

↑ **Parent:** [Statistical mechanics model](#statistical-mechanics-model)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Percolation)

##### Percolation theory

↑ **Parent:** [Percolation](#percolation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Percolation_theory)

This field is likely both ugly and useless.

OK, in 2D they've achieved some cute [rational number](formalization-of-mathematics.md#rational-number) results. But still.

## Sedimentation

↑ **Parent:** [Statistical physics](statistical-physics.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Sedimentation)

## Maxwell-Boltzmann vs Bose-Einstein vs Fermi-Dirac statistics

↑ **Parent:** [Statistical physics](statistical-physics.md)

[Maxwell-Boltzmann statistics](#maxwell-boltzmann-statistics), [Bose-Einstein statistics](#bose-einstein-statistics) and [Fermi-Dirac statistics](#fermi-dirac-statistics) all describe how energy is distributed in different physical systems at a given temperature.

For example, [Maxwell-Boltzmann statistics](#maxwell-boltzmann-statistics) describes how the speeds of particles are distributed in an [ideal gas](#ideal-gas-law).

The [temperature](#temperature) of a gas is only a statistical average of the total [energy](physics.md#energy) of the gas. But at a given temperature, not all particles have the exact same speed as the average: some are higher and others lower than the average.

For a large number of particles however, the fraction of particles that will have a given speed at a given temperature is highly deterministic, and it is this that the distributions determine.

One of the main interest of learning those statistics is determining the probability, and therefore average speed, at which some event that requires a minimum energy to happen happens. For example, for a [chemical reaction](chemistry.md#chemical-reaction) to happen, both input molecules need a certain speed to overcome the [potential barrier](physics.md#potential-barrier) of the reaction. Therefore, if we know how many particles have energy above some threshold, then we can estimate the speed of the reaction at a given temperature.

The three distributions can be summarized as:
- [Maxwell-Boltzmann statistics](#maxwell-boltzmann-statistics): statistics without considering [quantum](quantum-mechanics.md) statistics. It is therefore only an approximation. The other two statistics are the more precise quantum versions of [Maxwell-Boltzmann](#maxwell-boltzmann-statistics) and tend to it at high [temperatures](#temperature) or low concentration. Therefore this one works well at high temperatures or low concentrations.
- [Bose-Einstein statistics](#bose-einstein-statistics): [quantum](quantum-mechanics.md) version of [Maxwell-Boltzmann statistics](#maxwell-boltzmann-statistics) for [bosons](relativistic-quantum-mechanics.md#boson)
- [Fermi-Dirac statistics](#fermi-dirac-statistics): [quantum](quantum-mechanics.md) version of [Maxwell-Boltzmann statistics](#maxwell-boltzmann-statistics) for [fermions](relativistic-quantum-mechanics.md#fermion). Sample system: electrons in a metal, which creates the [free electron model](electronics.md#free-electron-model). Compared to [Maxwell-Boltzmann statistics](#maxwell-boltzmann-statistics), this explained many important experimental observations such as the [specific heat capacity](condensed-matter-physics.md#specific-heat-capacity) of metals. A very cool and concrete example can be seen at [https://youtu.be/5V8VCFkAd0A?t=1187](https://youtu.be/5V8VCFkAd0A?t=1187) from [Video "Using a Photomultiplier to Detect single photons by Huygens Optics"](photon.md#video-using-a-photomultiplier-to-detect-single-photons-by-huygens-optics) where spontaneous [field electron emission](condensed-matter-physics.md#field-electron-emission) would follow [Fermi-Dirac statistics](#fermi-dirac-statistics). In this case, the electrons with enough energy are undesired and a source of [noise](technology.md#signal-to-noise-ratio) in the experiment.

<a id="image-maxwell-boltzmann-vs-bose-einstein-vs-fermi-dirac-statistics"></a>
![](https://upload.wikimedia.org/wikipedia/commons/d/d8/Quantum_and_classical_statistics.png)

**[Figure 1](#image-maxwell-boltzmann-vs-bose-einstein-vs-fermi-dirac-statistics). Maxwell-Boltzmann vs Bose-Einstein vs Fermi-Dirac statistics**. [Source](https://commons.wikimedia.org/wiki/File:Quantum_and_classical_statistics.png).

A good conceptual starting point is to like the example that is mentioned at [The Harvest of a Century by Siegmund Brandt (2008)](particle-physics.md#the-harvest-of-a-century-by-siegmund-brandt-2008).

Consider a system with 2 particles and 3 states. Remember that:
- in [quantum statistics](#quantum-statistics) ([Bose-Einstein statistics](#bose-einstein-statistics) and [Fermi-Dirac statistics](#fermi-dirac-statistics)), particles are indistinguishable, therefore, we might was well call both of them `A`, as opposed to `A` and `B` from non-quantum statistics
- in [Bose-Einstein statistics](#bose-einstein-statistics), two particles may occupy the same state. In [Fermi-Dirac statistics](#fermi-dirac-statistics)

Therefore, all the possible way to put those two particles in three states are for:
- [Maxwell-Boltzmann distribution](#maxwell-boltzmann-distribution): both A and B can go anywhere:| State 1 | State 2 | State 3 |
  | --- | --- | --- |
  | AB |  |  |
  |  | AB |  |
  |  |  | AB |
  | A | B |  |
  | B | A |  |
  | A |  | B |
  | B |  | A |
  |  | A | B |
  |  | B | A |
- [Bose-Einstein statistics](#bose-einstein-statistics): because A and B are indistinguishable, there is now only 1 possibility for the states where A and B would be in different states.| State 1 | State 2 | State 3 |
  | --- | --- | --- |
  | AA |  |  |
  |  | AA |  |
  |  |  | AA |
  | A | A |  |
  | A |  | A |
  |  | A | A |
- [Fermi-Dirac statistics](#fermi-dirac-statistics): now states with two particles in the same state are not possible anymore:| State 1 | State 2 | State 3 |
  | --- | --- | --- |
  | A | A |  |
  | A |  | A |
  |  | A | A |

### Maxwell-Boltzmann distribution

↑ **Parent:** [Maxwell-Boltzmann vs Bose-Einstein vs Fermi-Dirac statistics](#maxwell-boltzmann-vs-bose-einstein-vs-fermi-dirac-statistics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Maxwell–Boltzmann_distribution)

<a id="image-maxwell-boltzmann-distribution-for-three-different-temperatures"></a>
![](https://en.wikipedia.org/wiki/File:Maxwell-Boltzmann_distribution_1.png)

**[Figure 2](#image-maxwell-boltzmann-distribution-for-three-different-temperatures). Maxwell-Boltzmann distribution for three different temperatures**.

#### Maxwell-Boltzmann statistics

↑ **Parent:** [Maxwell-Boltzmann distribution](#maxwell-boltzmann-distribution)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Maxwell-Boltzmann_statistics)

#### Experimental verification of the Maxwell-Boltzmann distribution

↑ **Parent:** [Maxwell-Boltzmann distribution](#maxwell-boltzmann-distribution)

Most [applications of the Maxwell-Boltzmann distribution](#application-of-the-maxwell-boltzmann-distribution) confirm the theory, but don't give a very direct proof of its curve.

Here we will try to gather some that do.

##### Zartman Ko experiment

↑ **Parent:** [Experimental verification of the Maxwell-Boltzmann distribution](#experimental-verification-of-the-maxwell-boltzmann-distribution)  
🏷️ **Tags:** [Physics experiment without a decent modern video](physics.md#physics-experiment-without-a-decent-modern-video)

Measured particle speeds with a rotation barrel! OMG, pre [electromagnetism](electromagnetism.md) equipment?
- [https://bingweb.binghamton.edu/~suzuki/GeneralPhysNote_PDF/LN19v7.pdf](https://bingweb.binghamton.edu/~suzuki/GeneralPhysNote_PDF/LN19v7.pdf)
- [https://chem.libretexts.org/Bookshelves/Physical_and_Theoretical_Chemistry_Textbook_Maps/Book%3A_Thermodynamics_and_Chemical_Equilibrium_(Ellgen)/04%3A_The_Distribution_of_Gas_Velocities/4.07%3A_Experimental_Test_of_the_Maxwell-Boltzmann_Probability_Density](https://chem.libretexts.org/Bookshelves/Physical_and_Theoretical_Chemistry_Textbook_Maps/Book%3A_Thermodynamics_and_Chemical_Equilibrium_(Ellgen)/04%3A_The_Distribution_of_Gas_Velocities/4.07%3A_Experimental_Test_of_the_Maxwell-Boltzmann_Probability_Density)

###### Stern-Zartman experiment

↑ **Parent:** [Zartman Ko experiment](#zartman-ko-experiment)

Is it the same as [Zartman Ko experiment](#zartman-ko-experiment)? TODO find the relevant papers.
- [https://encyclopedia2.thefreedictionary.com/Stern-Zartman+Experiment](https://encyclopedia2.thefreedictionary.com/Stern-Zartman+Experiment)

##### Application of the Maxwell-Boltzmann distribution

↑ **Parent:** [Experimental verification of the Maxwell-Boltzmann distribution](#experimental-verification-of-the-maxwell-boltzmann-distribution)

[https://edisciplinas.usp.br/pluginfile.php/48089/course/section/16461/qsp_chapter7-boltzman.pdf](https://edisciplinas.usp.br/pluginfile.php/48089/course/section/16461/qsp_chapter7-boltzman.pdf) mentions
- [sedimentation](#sedimentation)
- [reaction rate](chemistry.md#reaction-rate) as it calculates how likely it is for particles to overcome the [activation energy](chemistry.md#activation-energy)

### Quantum statistics

↑ **Parent:** [Maxwell-Boltzmann vs Bose-Einstein vs Fermi-Dirac statistics](#maxwell-boltzmann-vs-bose-einstein-vs-fermi-dirac-statistics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Particle_statistics#Quantum_statistics)

#### Bose-Einstein statistics

↑ **Parent:** [Quantum statistics](#quantum-statistics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Bose–Einstein_statistics)

Start by looking at: [Maxwell-Boltzmann vs Bose-Einstein vs Fermi-Dirac statistics](#maxwell-boltzmann-vs-bose-einstein-vs-fermi-dirac-statistics).

#### Fermi-Dirac statistics

↑ **Parent:** [Quantum statistics](#quantum-statistics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Fermi–Dirac_statistics)

Start by looking at: [Maxwell-Boltzmann vs Bose-Einstein vs Fermi-Dirac statistics](#maxwell-boltzmann-vs-bose-einstein-vs-fermi-dirac-statistics).

##### Quantum statistical mechanics

↑ **Parent:** [Fermi-Dirac statistics](#fermi-dirac-statistics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Quantum_statistical_mechanics)

Bibliography:
- [https://stanford.edu/~jeffjar/statmech/lec3.html](https://stanford.edu/~jeffjar/statmech/lec3.html)

## Thermodynamics

↑ **Parent:** [Statistical physics](statistical-physics.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Thermodynamics)

### Boltzmann constant

↑ **Parent:** [Thermodynamics](#thermodynamics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Boltzmann_constant)

This is not a truly "fundamental" constant of nature like say the [speed of light](photon.md#speed-of-light) or the [Planck constant](quantum-mechanics.md#planck-constant).

Rather, it is just a definition of our [Kelvin](#kelvin) temperature scale, linking average microscopic energy to our macroscopic temperature scale.

The way to think about that link is, at 1 [Kelvin](#kelvin), each particle has average energy:

$$
1/2 kT
$$

per degree of freedom.

This is why the units of the Boltzmann constant are [Joules](physics.md#joule) per [Kelvin](#kelvin).

For an ideal [monatomic gas](#monatomic-gas), say [helium](chemistry.md#helium), there are 3 degrees of freedom. so each helium atom has average energy:

$$
3/2 k_B T
$$

If we have 2 atoms at 1 K, they will have average energy $6/2 k_B J$, and so on.

Another conclusion is that this defines [temperature](#temperature) as being proportional to the total energy. E.g. if we had 1 helium atom at 2 K then we would have about $6/2 k_B J$ energy, 3 K $9/2 k_B J$ and so on.

This energy is of course just an average: some particles have more, and others less, following the [Maxwell-Boltzmann distribution](#maxwell-boltzmann-distribution).

### Equipartition theorem

↑ **Parent:** [Thermodynamics](#thermodynamics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Equipartition_theorem)

### Thermodynamic potential

↑ **Parent:** [Thermodynamics](#thermodynamics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Thermodynamic_potential)

[https://chemistry.stackexchange.com/questions/7696/how-do-i-distinguish-between-internal-energy-and-enthalpy/7700#7700](https://chemistry.stackexchange.com/questions/7696/how-do-i-distinguish-between-internal-energy-and-enthalpy/7700#7700) has a good insight:

> To summarize, internal energy and enthalpy are used to estimate the thermodynamic potential of the system. There are other such estimates, like the Gibbs free energy G. Which one you choose is determined by the conditions and how easy it is to determine pressure and volume changes.

#### Enthalpy

↑ **Parent:** [Thermodynamic potential](#thermodynamic-potential)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Enthalpy)

Adds up chemical energy and kinetic energy.

Wikipedia mentions however that the kinetic energy is often negligible, even for gases.

The sum is of interest when thinking about reactions because chemical reactions can change the number of molecules involved, and therefore the pressure.

To predict if a reaction is spontaneous or not, negative enthalpy is not enough, we must also consider [entropy](#entropy) via [Gibbs free energy](#gibbs-free-energy).

Bibliography:
- [https://chemistry.stackexchange.com/questions/7696/how-do-i-distinguish-between-internal-energy-and-enthalpy](https://chemistry.stackexchange.com/questions/7696/how-do-i-distinguish-between-internal-energy-and-enthalpy)

#### Gibbs free energy

↑ **Parent:** [Thermodynamic potential](#thermodynamic-potential)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Gibbs_free_energy)

TODO understand more intuitively how that determines if a reaction happens or not.

$$
\Delta G = \Delta H - T \Delta S
$$

At least from the formula we see that:
- the more exothermic, the more likely it is to occur
- if the entropy increases, the higher the temperature, the more likely it is to occur
  - otherwise, the lower the temperature the more likely it is to occur

A prototypical example of reaction that is exothermic but does not happen at any temperature is combustion.

<a id="video-lab-7-gibbs-free-energy-by-mj-billman-2020"></a>
**[Video 1](#video-lab-7-gibbs-free-energy-by-mj-billman-2020). Lab 7 - Gibbs Free Energy by MJ Billman (2020)** [Source](https://www.youtube.com/watch?v=DKiBA35Nqp4). Shows the shift of equilibrium due to temperature change with a color change in a HCl CoCl reaction. Unfortunately there are no conclusions because its student's homework.

##### Chemical equilibrium

↑ **Parent:** [Gibbs free energy](#gibbs-free-energy)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Chemical_equilibrium)

##### Reversible reaction

↑ **Parent:** [Gibbs free energy](#gibbs-free-energy)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Reversible_reaction)

I think these are the ones where $\Delta H \times \Delta S > 0$, i.e. [enthalpy](#enthalpy) and [entropy](#entropy) push the reaction in different directions. And so we can use temperature to move the [Chemical equilibrium](#chemical-equilibrium) back and forward.

<a id="video-demonstration-of-a-reversible-reaction-by-rugby-school-chemistry-2020"></a>
**[Video 2](#video-demonstration-of-a-reversible-reaction-by-rugby-school-chemistry-2020). Demonstration of a Reversible Reaction by Rugby School Chemistry (2020)** [Source](https://www.youtube.com/watch?v=NMIoon-kuQ4). Hydrated copper(ii) sulfate.

### Equation of state

↑ **Parent:** [Thermodynamics](#thermodynamics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Equation_of_state)

#### Ideal gas law

↑ **Parent:** [Equation of state](#equation-of-state)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Ideal_gas_law)

##### Monatomic gas

↑ **Parent:** [Ideal gas law](#ideal-gas-law)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Monatomic_gas)

### Entropy

↑ **Parent:** [Thermodynamics](#thermodynamics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Entropy)

OK, can someone please just stop the philosophy and give numerical predictions of how entropy helps you predict the future?

The original notion of entropy, and the first one you should study, is the [Clausius entropy](#clausius-entropy).

For entropy in chemistry see: [entropy of a chemical reaction](chemistry.md#entropy-of-a-chemical-reaction).

<a id="video-the-unexpected-side-of-entropy-by-daan-frenkel"></a>
**[Video 3](#video-the-unexpected-side-of-entropy-by-daan-frenkel). The Unexpected Side of Entropy by Daan Frenkel.** [Source](https://www.youtube.com/watch?v=0-yhZFDxBh8). 2021.

<a id="video-the-biggest-ideas-in-the-universe-20-entropy-and-information-by-sean-carroll-2020"></a>
**[Video 4](#video-the-biggest-ideas-in-the-universe-20-entropy-and-information-by-sean-carroll-2020). The Biggest Ideas in the Universe | 20. Entropy and Information by Sean Carroll (2020)** [Source](https://www.youtube.com/watch?v=rBPPOI5UIe0). In usual [Sean Carroll](physicist.md#sean-m-carroll) fashion, it glosses over the subject. This one might be worth watching. It mentions 4 possible definitions of entropy: Boltzmann, Gibbs, Shannon ([information theory](technology.md#information-theory)) and [John von Neumann](physicist.md#john-von-neumann) ([quantum mechanics](quantum-mechanics.md)).

- [https://www.quantamagazine.org/what-is-entropy-a-measure-of-just-how-little-we-really-know-20241213/](https://www.quantamagazine.org/what-is-entropy-a-measure-of-just-how-little-we-really-know-20241213/) What Is Entropy? A Measure of Just How Little We Really Know. on [Quanta Magazine](science.md#quanta-magazine) attempts to make the point that entropy is observer dependant. TODO details on that.

#### Clausius entropy

↑ **Parent:** [Entropy](#entropy)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Entropy_(classical_thermodynamics))

##### Carnot cycle

↑ **Parent:** [Clausius entropy](#clausius-entropy)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Carnot_cycle)

TODO why it is optimal: [https://physics.stackexchange.com/questions/149214/why-is-the-carnot-engine-the-most-efficient](https://physics.stackexchange.com/questions/149214/why-is-the-carnot-engine-the-most-efficient)

#### Second law of thermodynamics

↑ **Parent:** [Entropy](#entropy)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Second_law_of_thermodynamics)

[Subtle is the Lord by Abraham Pais (1982)](physicist.md#subtle-is-the-lord-by-abraham-pais-1982) chapter 4 "Entropy and Probability" mentions well how [Boltzmann](physicist.md#ludwig-boltzmann) first thought that the second law was an actual base physical law of the universe while he was calculating numerical stuff for it, including as late as 1872.

But then he saw an argument by [Johann Joseph Loschmidt](chemistry.md#johann-joseph-loschmidt) that given the [time reversibility of classical mechanics](#time-reversibility-of-classical-mechanics), and because they were thinking of atoms as classical balls as in the [kinetic theory of gases](#kinetic-theory-of-gases), then there always exist a valid physical state where entropy decreases, by just reversing the direction of time and all particle speeds.

So from this he understood that the second law can only be probabilistic, and not a fundamental law of physics, which he published clearly in 1877.

##### Time reversibility

↑ **Parent:** [Second law of thermodynamics](#second-law-of-thermodynamics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Time_reversibility)

###### Arrow of time

↑ **Parent:** [Time reversibility](#time-reversibility)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Arrow_of_time)

###### Time reversibility of classical mechanics

↑ **Parent:** [Time reversibility](#time-reversibility)

Considering e.g. [Newton's laws of motion](mechanics.md#newton-s-laws-of-motion), you take a system that is a function of time $f(t)$, e.g. the position of many point particles, and then you reverse the speeds of all particles, then $f(-t)$ is a solution to that.

###### Time reversibility of gravity

↑ **Parent:** [Time reversibility](#time-reversibility)

[https://physics.stackexchange.com/questions/288339/does-gravity-break-time-reversibility-on-the-microlevel](https://physics.stackexchange.com/questions/288339/does-gravity-break-time-reversibility-on-the-microlevel)

I guess you also have to change the sign of the [gravitational constant](relativity.md#gravitational-constant)?

### Phase (matter)

↑ **Parent:** [Thermodynamics](#thermodynamics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Phase_(matter))

#### List of phase transitions

↑ **Parent:** [Phase (matter)](#phase-matter)

##### Evaporation

↑ **Parent:** [List of phase transitions](#list-of-phase-transitions)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Evaporation)

##### Sublimation

↑ **Parent:** [List of phase transitions](#list-of-phase-transitions)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Sublimation_(phase_transition))

#### Phase transition

↑ **Parent:** [Phase (matter)](#phase-matter)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Phase_transition)

TODO can anything interesting and deep be said about "why phase transition happens?" [https://physics.stackexchange.com/questions/29128/what-causes-a-phase-transition](https://physics.stackexchange.com/questions/29128/what-causes-a-phase-transition) on [Physics Stack Exchange](stack-overflow.md#physics-stack-exchange)

##### Phase diagram

↑ **Parent:** [Phase transition](#phase-transition)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Phase_diagram)

###### Type of phase diagram

↑ **Parent:** [Phase diagram](#phase-diagram)

###### Temperature-pressure phase diagram

↑ **Parent:** [Type of phase diagram](#type-of-phase-diagram)

This is the most classical type of phase diagram, widely used when considering a [substance](chemistry.md#chemical-substance) at a fixed composition.

###### Composition phase diagram

↑ **Parent:** [Type of phase diagram](#type-of-phase-diagram)

Composition phase diagrams are [phase diagrams](#phase-diagram) that also consider variations in composition of a mixture. The most classic of such diagrams are [temperature-composition phase diagrams](#temperature-composition-phase-diagram) for [binary alloys](condensed-matter-physics.md#binary-alloy).

###### Temperature-composition phase diagram

↑ **Parent:** [Composition phase diagram](#composition-phase-diagram)

###### Triple point

↑ **Parent:** [Phase diagram](#phase-diagram)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Triple_point)

###### Critical point (thermodynamics)

↑ **Parent:** [Phase diagram](#phase-diagram)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Critical_point_(thermodynamics))

##### Second-order phase transition

↑ **Parent:** [Phase transition](#phase-transition)

Mentioned at: [https://en.wikipedia.org/wiki/Phase_transition#Modern_classifications](https://en.wikipedia.org/wiki/Phase_transition#Modern_classifications)

The more familiar transitions we are familiar with like liquid [water](chemistry.md#water) into solid water happen at constant temperature.

However, other types of phase transitions we are less familiar in our daily lives happen across a continuum of such "state variables", notably:
- [superfluidity](condensed-matter-physics.md#superfluidity) and its related manifestation, [superconductivity](condensed-matter-physics.md#superconductivity)
- [ferromagnetism](condensed-matter-physics.md#ferromagnetism)

### Refrigerator

↑ **Parent:** [Thermodynamics](#thermodynamics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Refrigerator)

<a id="video-refrigerator-how-does-it-work-by-curiosity-show"></a>
**[Video 5](#video-refrigerator-how-does-it-work-by-curiosity-show). Refrigerator - How Does It Work? by Curiosity Show.** [Source](https://www.youtube.com/watch?v=se1XZ8D_fCM).

#### Dilution refrigerator

↑ **Parent:** [Refrigerator](#refrigerator)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Dilution_refrigerator)

Reaches 2 mK[https://en.wikipedia.org/wiki/Dilution_refrigerator](https://en.wikipedia.org/wiki/Dilution_refrigerator). [https://youtu.be/upw9nkjawdy?t=487](https://youtu.be/upw9nkjawdy?t=487) from [Video "Building a quantum computer with superconducting qubits by Daniel Sank (2019)"](quantum-computing.md#video-building-a-quantum-computer-with-superconducting-qubits-by-daniel-sank-2019) mentions that 15 mK are widely available.

Used for example in some times of [quantum computers](quantum-computing.md), notably [superconducting quantum computers](quantum-computing.md#superconducting-quantum-computing). As mentioned at: [https://youtu.be/uPw9nkJAwDY?t=487](https://youtu.be/uPw9nkJAwDY?t=487), in that case we need to go so low to reduce thermal noise.
- [D-Wave Systems](quantum-computing.md#d-wave-systems): [https://www.dwavesys.com/tutorials/background-reading-series/introduction-d-wave-quantum-hardware#h2-5](https://www.dwavesys.com/tutorials/background-reading-series/introduction-d-wave-quantum-hardware#h2-5) (15mK)

<a id="video-this-is-what-a-helium-dilution-refrigerator-is-by-dietterich-labs-2019"></a>
**[Video 6](#video-this-is-what-a-helium-dilution-refrigerator-is-by-dietterich-labs-2019). This Is What A Helium Dilution refrigerator Is by Dietterich Labs (2019)** [Source](https://www.youtube.com/watch?v=j0s3uqqXZlc).

##### Cryogen-free dilution refrigerator

↑ **Parent:** [Dilution refrigerator](#dilution-refrigerator)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Dilution_refrigerator#Cryogen-free_dilution_refrigerators)

##### Dilution refrigerator manufacturer

↑ **Parent:** [Dilution refrigerator](#dilution-refrigerator)

###### Bluefors

↑ **Parent:** [Dilution refrigerator manufacturer](#dilution-refrigerator-manufacturer)

Users:
- [https://www.insidequantumtechnology.com/news-archive/ibm-bluefors-partnership-promises-really-cool-quantum-future/](https://www.insidequantumtechnology.com/news-archive/ibm-bluefors-partnership-promises-really-cool-quantum-future/)

### Temperature

↑ **Parent:** [Thermodynamics](#thermodynamics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Temperature)

For scales from absolute 0 like [Kelvin](#kelvin), is proportional to the total kinetic energy of the material.

The [Boltzmann constant](#boltzmann-constant) tells us how much energy that is, i.e. gives the slope.

#### Standard temperature and pressure

↑ **Parent:** [Temperature](#temperature)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Standard_temperature_and_pressure)

#### Scale of temperature

↑ **Parent:** [Temperature](#temperature)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Scale_of_temperature)

##### Kelvin

↑ **Parent:** [Scale of temperature](#scale-of-temperature)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Kelvin)

#### Thermometer

↑ **Parent:** [Temperature](#temperature)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Thermometer)

##### Mercury-in-glass thermometer

↑ **Parent:** [Thermometer](#thermometer)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Mercury-in-glass_thermometer)

### Vacuum

↑ **Parent:** [Thermodynamics](#thermodynamics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Vacuum)

#### Vacuum engineering

↑ **Parent:** [Vacuum](#vacuum)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Vacuum_engineering)

<a id="video-air-tight-vs-vacuum-tight-by-alphaphoenix-2020"></a>
**[Video 7](#video-air-tight-vs-vacuum-tight-by-alphaphoenix-2020). Air-tight vs. Vacuum-tight by AlphaPhoenix (2020)** [Source](https://www.youtube.com/watch?v=VD69crOFx10). Shows how to debug a leak in an [ultra-high vacuum](#ultra-high-vacuum) system. Like every other area of engineering, you basically bisect the machine! :-) By [Brian Haidet](https://www.materials.ucsb.edu/people/graduate-student/brian-haidet), a PhD at [University of California, Santa Barbara](university.md#university-of-california-santa-barbara).

##### Vacuum vendor

↑ **Parent:** [Vacuum engineering](#vacuum-engineering)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Vacuum_vendor)

###### Edwards Vacuum

↑ **Parent:** [Vacuum vendor](#vacuum-vendor)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Edwards_Vacuum)

##### Ultra-high vacuum

↑ **Parent:** [Vacuum engineering](#vacuum-engineering)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Ultra-high_vacuum)

## ↑ Ancestors (4)

1. [Physics](physics.md)
2. [Natural science](science.md#natural-science)
3. [Science](science.md)
4. [Ciro Santilli's Homepage](README.md)
