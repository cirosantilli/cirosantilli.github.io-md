# Electromagnetism

↑ **Parent:** [Particle physics](particle-physics.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Electromagnetism)

As of the 20th century, this can be described well as "the phenomena described by [Maxwell's equations](#maxwell-s-equations)".

Back [through its history however](physics.md#physics-education-needs-more-focus-on-understanding-experiments-and-their-history), that was not at all clear. This highlights how big of an achievement [Maxwell's equations](#maxwell-s-equations) are.

**Table of contents**

- [Maxwell's equations](#maxwell-s-equations)
  - [Faraday's law of induction](#faraday-s-law-of-induction)
    - [Electromagnetic induction](#electromagnetic-induction)
      - [Inductive sensor](#inductive-sensor)
  - [Lorentz force](#lorentz-force)
    - [Ampère's force law](#ampere-s-force-law)
  - [Explicit scalar form of the Maxwell's equations](#explicit-scalar-form-of-the-maxwell-s-equations)
    - [Overdetermination of Maxwell's equations](#overdetermination-of-maxwell-s-equations)
  - [Coulomb's law](#coulomb-s-law)
  - [Solutions of Maxwell's equations](#solutions-of-maxwell-s-equations)
    - [Maxwell's equations with pointlike particles](#maxwell-s-equations-with-pointlike-particles)
  - [Maxwell's equations in 2D](#maxwell-s-equations-in-2d)
  - [Existence and uniqueness of solutions to Maxwell's equations](#existence-and-uniqueness-of-solutions-to-maxwell-s-equations)
  - [Electric field](#electric-field)
    - [Electric charge](#electric-charge)
      - [Electric charge measure unit](#electric-charge-measure-unit)
        - [Coulomb](#coulomb)
      - [Charge conservation](#charge-conservation)
      - [Electric current](#electric-current)
    - [Electric potential](#electric-potential)
      - [Volt](#volt)
        - [Voltmeter](#voltmeter)
          - [Electrometer](#electrometer)
          - [Nanovoltmeter](#nanovoltmeter)
        - [Voltage](#voltage)
        - [Electronvolt](#electronvolt)
  - [Hall effect](#hall-effect)
    - [Hall resistance](#hall-resistance)
    - [Charge carrier density](#charge-carrier-density)
    - [Hall effect sensor](#hall-effect-sensor)
  - [Electromagnetic four-potential](#electromagnetic-four-potential)
    - [Electromagnetic tensor](#electromagnetic-tensor)
    - [Four-current](#four-current)
    - [Lorentz gauge condition](#lorentz-gauge-condition)
      - [Coulomb gauge](#coulomb-gauge)
- [Magnetism](#magnetism)
  - [Magnetic field](#magnetic-field)
    - [Magnetic B and H field](#magnetic-b-and-h-field)
    - [Tesla (unit)](#tesla-unit)
  - [Magnetic moment](#magnetic-moment)
  - [Magnetometer](#magnetometer)
  - [Magnetic flux](#magnetic-flux)
  - [Magnetic vector potential](#magnetic-vector-potential)

<h2 id="maxwell-s-equations">Maxwell's equations</h2>

↑ **Parent:** [Electromagnetism](electromagnetism.md)  
🏷️ **Tags:** [Important partial differential equation](calculus.md#important-partial-differential-equation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Maxwell's_equations)

Unified all previous electro-magnetism theories into one equation.

Explains the propagation of light as a wave, and matches the previously known relationship between the [speed of light](photon.md#speed-of-light) and electromagnetic constants.

The equations are a limit case of the more complete [quantum electrodynamics](quantum-field-theory.md#quantum-electrodynamics), and unlike that more general theory account for the quantization of [photon](photon.md).

The equations are a system of [partial differential equation](calculus.md#partial-differential-equation).

The system consists of 6 unknown functions that map 4 variables: time t and the x, y and z positions in space, to a real number:
- $E_x(t, x,y,z)$, $E_y(t, x,y,z)$, $E_z(t, x,y,z)$: directions of the electric field $\E : \R^4 \to \R^3$
- $B_x(t, x,y,z)$, $B_y(t, x,y,z)$, $B_z(t, x,y,z)$: directions of the magnetic field $\B : \R^4 \to \R^3$
and two known input functions:
- $\rho : \R^3\ to \R$: density of charges in space
- $\J : \R^3 \to \R^3$: current vector in space. This represents the strength of moving charges in space.

Due to the [conservation of charge](#charge-conservation) however, those input functions have the following restriction:<a id="equation-charge-conservation"></a>


$$
\pdv{\rho}{t} + \div{\mathbf{\J}} = 0
$$

Also consider the following cases:
- if a spherical charge is moving, then this of course means that $\rho$ is changing with time, and at the same time that a current exists
- in an [ideal](science.md#idealism) infinite cylindrical wire however, we can have constant $\rho$ in the wire, but there can still be a current because those charges are moving

  Such infinite cylindrical wire is of course an ideal case, but one which is a good approximation to the huge number of electrons that travel in a actual wire.

The goal of finding $\E$ and $\B$ is that those fields allow us to determine the force that gets applied to a charge via the [Equation 6. "Lorentz force"](#equation-lorentz-force), and then to find the force we just need to integrate over the entire body.

Finally, now that we have defined all terms involved in the Maxwell equations, let's see the equations:

<a id="equation-gauss-law"></a>
$$
div{\E} = \frac{\rho}{\vacuumPermittivity}
$$

<a id="equation-gauss-s-law-for-magnetism"></a>
$$
div{\B} = 0
$$

<a id="equation-faraday-s-law"></a>
$$
\curl{\E} = -\pdv{\B}{t}
$$

<a id="equation-ampere-s-circuital-law"></a>
$$
\curl{\B} = \vacuumPermeability \left(\J + \vacuumPermittivity \pdv{E}{t} \right)
$$

You should also review the intuitive interpretation of [divergence](calculus.md#divergence) and [curl](calculus.md#curl-mathematics).

<h3 id="faraday-s-law-of-induction">Faraday's law of induction</h3>

↑ **Parent:** [Maxwell's equations](#maxwell-s-equations)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Faraday's_law_of_induction)

#### Electromagnetic induction

↑ **Parent:** [Faraday's law of induction](#faraday-s-law-of-induction)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Electromagnetic_induction)

##### Inductive sensor

↑ **Parent:** [Electromagnetic induction](#electromagnetic-induction)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Inductive_sensor)

### Lorentz force

↑ **Parent:** [Maxwell's equations](#maxwell-s-equations)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Lorentz_force)

<a id="equation-lorentz-force"></a>
$$
\text{force\_density} = \rho \E + \J \times \B
$$

A little suspicious that it bears the name of Lorentz, who is famous for [special relativity](relativity.md#special-relativity), isn't it? See: [Maxwell's equations require special relativity](relativity.md#maxwell-s-equations-require-special-relativity).

<h4 id="ampere-s-force-law">Ampère's force law</h4>

↑ **Parent:** [Lorentz force](#lorentz-force)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Ampère's_force_law)

Force between two wires carrying an [electric current](#electric-current).

Caused by the [Lorentz force](#lorentz-force).

<h3 id="explicit-scalar-form-of-the-maxwell-s-equations">Explicit scalar form of the Maxwell's equations</h3>

↑ **Parent:** [Maxwell's equations](#maxwell-s-equations)

For numerical algorithms and to get a more low level understanding of the equations, we can expand all terms to the simpler and more explicit form:<a id="equation-maxwells-equation-explicit"></a>


$$
\pdv{E_x}{x} + \pdv{E_y}{x} +
\pdv{E_z}{x} =
\frac{\rho}{\vacuumPermittivity}
\\

\pdv{B_x}{x} +
\pdv{B_y}{x} +
\pdv{B_z}{x} =
0
\\

\pdv{E_z}{y} - \pdv{E_y}{z} = -\pdv{B_x}{t} \\
\pdv{E_x}{z} - \pdv{E_z}{x} = -\pdv{B_y}{t} \\
\pdv{E_y}{x} - \pdv{E_x}{y} = -\pdv{B_z}{t} \\

\pdv{B_z}{y} - \pdv{B_y}{z} = \vacuumPermeability \left(J_x + \vacuumPermittivity \pdv{E_x}{t} \right) \\
\pdv{B_x}{z} - \pdv{B_z}{x} = \vacuumPermeability \left(J_y + \vacuumPermittivity \pdv{E_y}{t} \right) \\
\pdv{B_y}{x} - \pdv{B_x}{y} = \vacuumPermeability \left(J_z + \vacuumPermittivity \pdv{E_z}{t} \right) \\
$$

<h4 id="overdetermination-of-maxwell-s-equations">Overdetermination of Maxwell's equations</h4>

↑ **Parent:** [Explicit scalar form of the Maxwell's equations](#explicit-scalar-form-of-the-maxwell-s-equations)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Maxwell's_equations#Overdetermination_of_Maxwell's_equations)

As seen from [explicit scalar form of the Maxwell's equations](#explicit-scalar-form-of-the-maxwell-s-equations), this expands to 8 equations, so the question arises if the system is over-determined because it only has 6 functions to be determined.

As explained on the Wikipedia page  however, this is not the case, because if the first two equations hold for the initial condition, then the othe six equations imply that they also hold for all time, so they can be essentially omitted.

It is also worth noting that the first two equations don't involve time derivatives. Therefore, they can be seen as spacial constraints.

TODO: the [electric field](#electric-field) and [magnetic field](#magnetic-field) can be expressed in terms of the [electric potential](#electric-potential) and [magnetic vector potential](#magnetic-vector-potential). So then we only need 4 variables?

Bibliography:
- [https://physics.stackexchange.com/questions/20071/do-maxwells-equations-overdetermine-the-electric-and-magnetic-fields](https://physics.stackexchange.com/questions/20071/do-maxwells-equations-overdetermine-the-electric-and-magnetic-fields)

<h3 id="coulomb-s-law">Coulomb's law</h3>

↑ **Parent:** [Maxwell's equations](#maxwell-s-equations)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Coulomb's_law)

Static case of Maxwell's law for electricity only.

Is implied by Gauss' law if [Maxwell's equations](#maxwell-s-equations): [https://physics.stackexchange.com/questions/44418/are-the-maxwells-equations-enough-to-derive-the-law-of-coulomb](https://physics.stackexchange.com/questions/44418/are-the-maxwells-equations-enough-to-derive-the-law-of-coulomb)

The "static" part is important: if this law were true for moving charges, we would be able to transmit information instantly at infinite distances. This is basically where the idea of [field](physics.md#field-physics) comes in.

<a id="video-coulomb-s-law-experiment-with-torsion-balance-with-a-mirror-on-the-balance-to-amplify-rotations-by-uclaphysics-2010"></a>
**[Video 1](#video-coulomb-s-law-experiment-with-torsion-balance-with-a-mirror-on-the-balance-to-amplify-rotations-by-uclaphysics-2010). Coulomb's Law experiment with torsion balance with a mirror on the balance to amplify rotations by uclaphysics (2010)** [Source](https://www.youtube.com/watch?v=B5LVoU_a08c).

<h3 id="solutions-of-maxwell-s-equations">Solutions of Maxwell's equations</h3>

↑ **Parent:** [Maxwell's equations](#maxwell-s-equations)

<a id="video-understanding-electromagnetic-radiation-by-learn-engineering-2019"></a>
**[Video 2](#video-understanding-electromagnetic-radiation-by-learn-engineering-2019). Understanding Electromagnetic Radiation! by Learn Engineering (2019)** [Source](https://www.youtube.com/watch?v=FWCN_uI5ygY). Shows animations of a [dipole antenna](telecommunication.md#dipole-antenna) which illustrates well how radiation is emitted from moving charges and travels at the [speed of light](photon.md#speed-of-light).

<h4 id="maxwell-s-equations-with-pointlike-particles">Maxwell's equations with pointlike particles</h4>

↑ **Parent:** [Solutions of Maxwell's equations](#solutions-of-maxwell-s-equations)

In the standard formulation of [Maxwell's equations](#maxwell-s-equations), the [electric current](#electric-current) is a convient but magic input.

Would it be possible to use [Maxwell's equations](#maxwell-s-equations) to solve a system of [pointlike particles](mechanics.md#point-particle) such as electrons instead?

The following suggest no, or only for certain subcases less general than [Maxwell's equations](#maxwell-s-equations):
- [https://physics.stackexchange.com/questions/498892/solution-to-maxwell-lorentz-equations](https://physics.stackexchange.com/questions/498892/solution-to-maxwell-lorentz-equations)
- [https://physics.stackexchange.com/questions/380741/complete-classical-description-of-two-interacting-charges](https://physics.stackexchange.com/questions/380741/complete-classical-description-of-two-interacting-charges)
This is the type of thing where the probability aspect of [quantum mechanics](quantum-mechanics.md) seems it could "help".

<h3 id="maxwell-s-equations-in-2d">Maxwell's equations in 2D</h3>

↑ **Parent:** [Maxwell's equations](#maxwell-s-equations)

TODO it would be awesome if we could de-generalize the equations in 2D and do a [JavaScript](programming-language.md#javascript) demo of it!

Not sure it is possible though because the [curl](calculus.md#curl-mathematics) appears in the equations:
- [https://physics.stackexchange.com/questions/104008/maxwells-equations-of-electromagnetism-in-21-spacetime-dimensions](https://physics.stackexchange.com/questions/104008/maxwells-equations-of-electromagnetism-in-21-spacetime-dimensions)
- [https://www.reed.edu/physics/faculty/wheeler/documents/Electrodynamics/Miscellaneous%20Essays/E&M%20in%202%20Dimensions.pdf](https://www.reed.edu/physics/faculty/wheeler/documents/Electrodynamics/Miscellaneous%20Essays/E&M%20in%202%20Dimensions.pdf)

<h3 id="existence-and-uniqueness-of-solutions-to-maxwell-s-equations">Existence and uniqueness of solutions to Maxwell's equations</h3>

↑ **Parent:** [Maxwell's equations](#maxwell-s-equations)

TODO: I'm surprised that the Wiki page barely talks about it, and there are few [Google](google.md) hits too! A sample one: [https://www.researchgate.net/publication/228928756_On_the_existence_and_uniqueness_of_Maxwell's_equations_in_bounded_domains_with_application_to_magnetotellurics](https://www.researchgate.net/publication/228928756_On_the_existence_and_uniqueness_of_Maxwell's_equations_in_bounded_domains_with_application_to_magnetotellurics)

### Electric field

↑ **Parent:** [Maxwell's equations](#maxwell-s-equations)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Electric_field)

#### Electric charge

↑ **Parent:** [Electric field](#electric-field)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Electric_charge)

##### Electric charge measure unit

↑ **Parent:** [Electric charge](#electric-charge)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Electric_charge_measure_unit)

###### Coulomb

↑ **Parent:** [Electric charge measure unit](#electric-charge-measure-unit)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Coulomb)

##### Charge conservation

↑ **Parent:** [Electric charge](#electric-charge)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Charge_conservation)

##### Electric current

↑ **Parent:** [Electric charge](#electric-charge)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Electric_current)

In the context of [Maxwell's equations](#maxwell-s-equations), it is [vector field](group.md#vector-field) that is one of the inputs of the equation.

[Section "Maxwell's equations with pointlike particles"](#maxwell-s-equations-with-pointlike-particles) asks if the theory would work for pointlike particles in order to predict the evolution of this field as part of the equations themselves rather than as an external element.

Measured in [amperes](system-of-units.md#ampere) in the [International System of Units](system-of-units.md#international-system-of-units).

#### Electric potential

↑ **Parent:** [Electric field](#electric-field)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Electric_potential)

##### Volt

↑ **Parent:** [Electric potential](#electric-potential)  
🏷️ **Tags:** [International System of Units](system-of-units.md#international-system-of-units)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Volt)

###### Voltmeter

↑ **Parent:** [Volt](#volt)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Voltmeter)

###### Electrometer

↑ **Parent:** [Voltmeter](#voltmeter)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Electrometer)

This can be used to detect the [ionization of air by radiation ](photon.md#ionization-of-air-by-radiation), see e.g. [https://youtu.be/CZ7DoLLwW04?t=76](https://youtu.be/CZ7DoLLwW04?t=76) from [Video "Ions produced by radiation carry a current by Institute of Physics"](photon.md#video-ions-produced-by-radiation-carry-a-current-by-institute-of-physics).

###### Nanovoltmeter

↑ **Parent:** [Voltmeter](#voltmeter)

###### Voltage

↑ **Parent:** [Volt](#volt)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Voltage)

###### Electronvolt

↑ **Parent:** [Volt](#volt)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Electronvolt)

After the [2019 redefinition of the SI base units](system-of-units.md#2019-redefinition-of-the-si-base-units) it is by definition exactly $1.602 176 634 10^{-19}$ [Joules](physics.md#joule).

### Hall effect

↑ **Parent:** [Maxwell's equations](#maxwell-s-equations)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Hall_effect)

The voltage changes perpendicular to the current when magnetic field is applied.

<a id="image-hall-effect-experimental-diagram"></a>
![](https://upload.wikimedia.org/wikipedia/commons/1/19/Hall_Effect_Measurement_Setup_for_Electrons.png)

**[Figure 1](#image-hall-effect-experimental-diagram). Hall effect experimental diagram**. [Source](https://commons.wikimedia.org/wiki/File:Hall_Effect_Measurement_Setup_for_Electrons.png). The [Hall effect](#hall-effect) refers to the produced voltage $V_H$, AKA $V_y$ on this setup.

An intuitive video is:

**[Video 3](#_64)** [Source](https://commons.wikimedia.org/wiki/File:Hall_Sensor.webm).

The key formula for it is:

$$
V_{H} = \frac{I_x B_z}{n t e}
$$

where:
- $I_x$: current on x direction, which we can control by changing the voltage $V_x$
- $B_z$: strength of transversal [magnetic field](#magnetic-field) applied
- $n$: [charge carrier density](#charge-carrier-density), a property of the material used
- $t$: height of the plate
- $e$: [electron charge](standard-model.md#elementary-charge)

Applications:
- the direction of the effect proves that electric currents in common electrical conductors are made up of negative charged particles
- [measure magnetic fields](#magnetometer), TODO vs other methods

Other more precise non-classical versions:
- [quantum Hall effect](quantum-mechanics.md#quantum-hall-effect)

Bibliography:
- [http://hyperphysics.phy-astr.gsu.edu/hbase/magnetic/Hall.html](http://hyperphysics.phy-astr.gsu.edu/hbase/magnetic/Hall.html)

#### Hall resistance

↑ **Parent:** [Hall effect](#hall-effect)

In some contexts, we want to observe what happens for a given fixed [magnetic field](#magnetic-field) strength on a specific plate (thus $t$ and $n$ are also fixed).

In those cases, it can be useful to talk about the "Hall resistance" defined as:

$$
R_{xy} = \frac{V_y}{I_x}
$$

So note that it is not a "regular resistance", it just has the same dimensions, and is more usefully understood as a proportionality constant for the voltage given an input $I_x$ current:

$$
V_y = R_{xy} I_x
$$

This notion can be useful because everything else being equal, if we increase the current $I_x$, then $V_y$ also increases proportionally, making this a way to talk about the voltage in a current independent manner.

And this is particularly the case for the [quantum Hall effect](quantum-mechanics.md#quantum-hall-effect), where $R_{xy}$ is constant for wide ranges of applied [magnetic field](#magnetic-field) and TODO presumably the height $t$ can be made to a single molecular layer with [chemical vapor deposition](computer-hardware.md#chemical-vapor-deposition) of the like, and if therefore fixed.

#### Charge carrier density

↑ **Parent:** [Hall effect](#hall-effect)

#### Hall effect sensor

↑ **Parent:** [Hall effect](#hall-effect)

### Electromagnetic four-potential

↑ **Parent:** [Maxwell's equations](#maxwell-s-equations)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Electromagnetic_four-potential)

A different and more elegant way to express [Maxwell's equations](#maxwell-s-equations) by using the:
- [magnetic vector potential](#magnetic-vector-potential)
- [electric potential](#electric-potential)
instead of the:
- [magnetic field](#magnetic-field)
- [electric field](#electric-field)

#### Electromagnetic tensor

↑ **Parent:** [Electromagnetic four-potential](#electromagnetic-four-potential)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Electromagnetic_tensor)

#### Four-current

↑ **Parent:** [Electromagnetic four-potential](#electromagnetic-four-potential)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Four-current)

#### Lorentz gauge condition

↑ **Parent:** [Electromagnetic four-potential](#electromagnetic-four-potential)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Lorentz_gauge_condition)

There are several choices of [electromagnetic four-potential](#electromagnetic-four-potential) that lead to the same physics.

E.g. thinking about the [electric potential](#electric-potential) alone, you could set the zero anywhere, and everything would remain be the same.

The Lorentz gauge is just one such choice. It is however a very popular one, because it is also manifestly [Lorentz invariant](relativity.md#lorentz-invariant).

##### Coulomb gauge

↑ **Parent:** [Lorentz gauge condition](#lorentz-gauge-condition)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Coulomb_gauge)

Alternative to the [Lorentz gauge](#lorentz-gauge-condition), but less used in general as it is not as nice for [relativity](relativity.md) invariance.

## Magnetism

↑ **Parent:** [Electromagnetism](electromagnetism.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Magnetism)

### Magnetic field

↑ **Parent:** [Magnetism](#magnetism)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Magnetic_field)

#### Magnetic B and H field

↑ **Parent:** [Magnetic field](#magnetic-field)

[https://electronics.stackexchange.com/questions/94744/what-is-the-difference-between-the-magnetic-h-field-and-the-b-field](https://electronics.stackexchange.com/questions/94744/what-is-the-difference-between-the-magnetic-h-field-and-the-b-field)

#### Tesla (unit)

↑ **Parent:** [Magnetic field](#magnetic-field)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Tesla_(unit))

### Magnetic moment

↑ **Parent:** [Magnetism](#magnetism)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Magnetic_moment)

### Magnetometer

↑ **Parent:** [Magnetism](#magnetism)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Magnetometer)

Implementations:
- [Hall effect](#hall-effect) based, i.e. a [Hall effect sensor](#hall-effect-sensor)
- [SQUID device](condensed-matter-physics.md#squid-device)

### Magnetic flux

↑ **Parent:** [Magnetism](#magnetism)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Magnetic_flux)

### Magnetic vector potential

↑ **Parent:** [Magnetism](#magnetism)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Magnetic_vector_potential)

## ↑ Ancestors (5)

1. [Particle physics](particle-physics.md)
2. [Physics](physics.md)
3. [Natural science](science.md#natural-science)
4. [Science](science.md)
5. [Ciro Santilli's Homepage](README.md)

## ← Incoming links (11)

- [Aharonov-Bohm effect](physics.md#aharonov-bohm-effect)
- [Derivation of the quantum electrodynamics Lagrangian](quantum-field-theory.md#derivation-of-the-quantum-electrodynamics-lagrangian)
- [Gauge theory](quantum-field-theory.md#gauge-theory)
- [General relativity](relativity.md#general-relativity)
- [Lamb-Retherford experiment](quantum-field-theory.md#lamb-retherford-experiment)
- [Maxwell's equations in curved spacetime](relativity.md#maxwell-s-equations-in-curved-spacetime)
- [Quantum chromodynamics](quantum-field-theory.md#quantum-chromodynamics)
- [Quantum electrodynamics](quantum-field-theory.md#quantum-electrodynamics)
- [What does it mean that photons are force carriers for electromagnetism?](quantum-field-theory.md#what-does-it-mean-that-photons-are-force-carriers-for-electromagnetism)
- [Yang-Mills existence and mass gap](quantum-field-theory.md#yang-mills-existence-and-mass-gap)
- [Zartman Ko experiment](statistical-physics.md#zartman-ko-experiment)
