# Maxwell-Boltzmann vs Bose-Einstein vs Fermi-Dirac statistics

↑ **Parent:** [Statistical physics](statistical-physics-split.md)

[Maxwell-Boltzmann statistics](maxwell-boltzmann-statistics.md), [Bose-Einstein statistics](bose-einstein-statistics.md) and [Fermi-Dirac statistics](fermi-dirac-statistics.md) all describe how energy is distributed in different physical systems at a given temperature.

For example, [Maxwell-Boltzmann statistics](maxwell-boltzmann-statistics.md) describes how the speeds of particles are distributed in an [ideal gas](ideal-gas-law.md).

The [temperature](temperature.md) of a gas is only a statistical average of the total [energy](energy.md) of the gas. But at a given temperature, not all particles have the exact same speed as the average: some are higher and others lower than the average.

For a large number of particles however, the fraction of particles that will have a given speed at a given temperature is highly deterministic, and it is this that the distributions determine.

One of the main interest of learning those statistics is determining the probability, and therefore average speed, at which some event that requires a minimum energy to happen happens. For example, for a [chemical reaction](chemical-reaction.md) to happen, both input molecules need a certain speed to overcome the [potential barrier](potential-barrier.md) of the reaction. Therefore, if we know how many particles have energy above some threshold, then we can estimate the speed of the reaction at a given temperature.

The three distributions can be summarized as:
- [Maxwell-Boltzmann statistics](maxwell-boltzmann-statistics.md): statistics without considering [quantum](quantum-mechanics-split.md) statistics. It is therefore only an approximation. The other two statistics are the more precise quantum versions of [Maxwell-Boltzmann](maxwell-boltzmann-statistics.md) and tend to it at high [temperatures](temperature.md) or low concentration. Therefore this one works well at high temperatures or low concentrations.
- [Bose-Einstein statistics](bose-einstein-statistics.md): [quantum](quantum-mechanics-split.md) version of [Maxwell-Boltzmann statistics](maxwell-boltzmann-statistics.md) for [bosons](boson.md)
- [Fermi-Dirac statistics](fermi-dirac-statistics.md): [quantum](quantum-mechanics-split.md) version of [Maxwell-Boltzmann statistics](maxwell-boltzmann-statistics.md) for [fermions](fermion.md). Sample system: electrons in a metal, which creates the [free electron model](free-electron-model.md). Compared to [Maxwell-Boltzmann statistics](maxwell-boltzmann-statistics.md), this explained many important experimental observations such as the [specific heat capacity](specific-heat-capacity.md) of metals. A very cool and concrete example can be seen at [https://youtu.be/5V8VCFkAd0A?t=1187](https://youtu.be/5V8VCFkAd0A?t=1187) from [Video "Using a Photomultiplier to Detect single photons by Huygens Optics"](photomultiplier-tube.md#video-using-a-photomultiplier-to-detect-single-photons-by-huygens-optics) where spontaneous [field electron emission](field-electron-emission.md) would follow [Fermi-Dirac statistics](fermi-dirac-statistics.md). In this case, the electrons with enough energy are undesired and a source of [noise](signal-to-noise-ratio.md) in the experiment.

<a id="image-maxwell-boltzmann-vs-bose-einstein-vs-fermi-dirac-statistics"></a>
![](https://upload.wikimedia.org/wikipedia/commons/d/d8/Quantum_and_classical_statistics.png)

**[Figure 1](#image-maxwell-boltzmann-vs-bose-einstein-vs-fermi-dirac-statistics). Maxwell-Boltzmann vs Bose-Einstein vs Fermi-Dirac statistics**. [Source](https://commons.wikimedia.org/wiki/File:Quantum_and_classical_statistics.png).

A good conceptual starting point is to like the example that is mentioned at [The Harvest of a Century by Siegmund Brandt (2008)](the-harvest-of-a-century-by-siegmund-brandt-2008.md).

Consider a system with 2 particles and 3 states. Remember that:
- in [quantum statistics](quantum-statistics.md) ([Bose-Einstein statistics](bose-einstein-statistics.md) and [Fermi-Dirac statistics](fermi-dirac-statistics.md)), particles are indistinguishable, therefore, we might was well call both of them `A`, as opposed to `A` and `B` from non-quantum statistics
- in [Bose-Einstein statistics](bose-einstein-statistics.md), two particles may occupy the same state. In [Fermi-Dirac statistics](fermi-dirac-statistics.md)

Therefore, all the possible way to put those two particles in three states are for:
- [Maxwell-Boltzmann distribution](maxwell-boltzmann-distribution.md): both A and B can go anywhere:| State 1 | State 2 | State 3 |
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
- [Bose-Einstein statistics](bose-einstein-statistics.md): because A and B are indistinguishable, there is now only 1 possibility for the states where A and B would be in different states.| State 1 | State 2 | State 3 |
  | --- | --- | --- |
  | AA |  |  |
  |  | AA |  |
  |  |  | AA |
  | A | A |  |
  | A |  | A |
  |  | A | A |
- [Fermi-Dirac statistics](fermi-dirac-statistics.md): now states with two particles in the same state are not possible anymore:| State 1 | State 2 | State 3 |
  | --- | --- | --- |
  | A | A |  |
  | A |  | A |
  |  | A | A |

**Table of contents**

- [Maxwell-Boltzmann distribution](maxwell-boltzmann-distribution.md)
  - [Maxwell-Boltzmann statistics](maxwell-boltzmann-statistics.md)
  - [Experimental verification of the Maxwell-Boltzmann distribution](experimental-verification-of-the-maxwell-boltzmann-distribution.md)
    - [Zartman Ko experiment](zartman-ko-experiment.md)
      - [Stern-Zartman experiment](stern-zartman-experiment.md)
    - [Application of the Maxwell-Boltzmann distribution](application-of-the-maxwell-boltzmann-distribution.md)
- [Quantum statistics](quantum-statistics.md)
  - [Bose-Einstein statistics](bose-einstein-statistics.md)
  - [Fermi-Dirac statistics](fermi-dirac-statistics.md)
    - [Quantum statistical mechanics](quantum-statistical-mechanics.md)

## ↑ Ancestors (5)

1. [Statistical physics](statistical-physics-split.md)
2. [Physics](physics-split.md)
3. [Natural science](natural-science.md)
4. [Science](science-split.md)
5. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (2)

- [Bose-Einstein statistics](bose-einstein-statistics.md)
- [Fermi-Dirac statistics](fermi-dirac-statistics.md)
