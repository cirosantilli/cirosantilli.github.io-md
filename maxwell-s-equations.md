<h1 id="maxwell-s-equations">Maxwell's equations</h1>

↑ **Parent:** [Electromagnetism](electromagnetism-split.md)  
🏷️ **Tags:** [Important partial differential equation](important-partial-differential-equation.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Maxwell's_equations)

Unified all previous electro-magnetism theories into one equation.

Explains the propagation of light as a wave, and matches the previously known relationship between the [speed of light](speed-of-light.md) and electromagnetic constants.

The equations are a limit case of the more complete [quantum electrodynamics](quantum-electrodynamics.md), and unlike that more general theory account for the quantization of [photon](photon-split.md).

The equations are a system of [partial differential equation](partial-differential-equation.md).

The system consists of 6 unknown functions that map 4 variables: time t and the x, y and z positions in space, to a real number:
- $E_x(t, x,y,z)$, $E_y(t, x,y,z)$, $E_z(t, x,y,z)$: directions of the electric field $\E : \R^4 \to \R^3$
- $B_x(t, x,y,z)$, $B_y(t, x,y,z)$, $B_z(t, x,y,z)$: directions of the magnetic field $\B : \R^4 \to \R^3$
and two known input functions:
- $\rho : \R^3\ to \R$: density of charges in space
- $\J : \R^3 \to \R^3$: current vector in space. This represents the strength of moving charges in space.

Due to the [conservation of charge](charge-conservation.md) however, those input functions have the following restriction:<a id="equation-charge-conservation"></a>


$$
\pdv{\rho}{t} + \div{\mathbf{\J}} = 0
$$

Also consider the following cases:
- if a spherical charge is moving, then this of course means that $\rho$ is changing with time, and at the same time that a current exists
- in an [ideal](idealism.md) infinite cylindrical wire however, we can have constant $\rho$ in the wire, but there can still be a current because those charges are moving

  Such infinite cylindrical wire is of course an ideal case, but one which is a good approximation to the huge number of electrons that travel in a actual wire.

The goal of finding $\E$ and $\B$ is that those fields allow us to determine the force that gets applied to a charge via the [Equation 6. "Lorentz force"](lorentz-force.md#equation-lorentz-force), and then to find the force we just need to integrate over the entire body.

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

You should also review the intuitive interpretation of [divergence](divergence.md) and [curl](curl-mathematics.md).

**Table of contents**

- [Faraday's law of induction](faraday-s-law-of-induction.md)
  - [Electromagnetic induction](electromagnetic-induction.md)
    - [Inductive sensor](inductive-sensor.md)
- [Lorentz force](lorentz-force.md)
  - [Ampère's force law](ampere-s-force-law.md)
- [Explicit scalar form of the Maxwell's equations](explicit-scalar-form-of-the-maxwell-s-equations.md)
  - [Overdetermination of Maxwell's equations](overdetermination-of-maxwell-s-equations.md)
- [Coulomb's law](coulomb-s-law.md)
- [Solutions of Maxwell's equations](solutions-of-maxwell-s-equations.md)
  - [Maxwell's equations with pointlike particles](maxwell-s-equations-with-pointlike-particles.md)
- [Maxwell's equations in 2D](maxwell-s-equations-in-2d.md)
- [Existence and uniqueness of solutions to Maxwell's equations](existence-and-uniqueness-of-solutions-to-maxwell-s-equations.md)
- [Electric field](electric-field.md)
  - [Electric charge](electric-charge.md)
    - [Electric charge measure unit](electric-charge-measure-unit.md)
      - [Coulomb](coulomb.md)
    - [Charge conservation](charge-conservation.md)
    - [Electric current](electric-current.md)
  - [Electric potential](electric-potential.md)
    - [Volt](volt.md)
      - [Voltmeter](voltmeter.md)
        - [Electrometer](electrometer.md)
        - [Nanovoltmeter](nanovoltmeter.md)
      - [Voltage](voltage.md)
      - [Electronvolt](electronvolt.md)
- [Hall effect](hall-effect.md)
  - [Hall resistance](hall-resistance.md)
  - [Charge carrier density](charge-carrier-density.md)
  - [Hall effect sensor](hall-effect-sensor.md)
- [Electromagnetic four-potential](electromagnetic-four-potential.md)
  - [Electromagnetic tensor](electromagnetic-tensor.md)
  - [Four-current](four-current.md)
  - [Lorentz gauge condition](lorentz-gauge-condition.md)
    - [Coulomb gauge](coulomb-gauge.md)

## ↑ Ancestors (6)

1. [Electromagnetism](electromagnetism-split.md)
2. [Particle physics](particle-physics-split.md)
3. [Physics](physics-split.md)
4. [Natural science](natural-science.md)
5. [Science](science-split.md)
6. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (14)

- [Coulomb's law](coulomb-s-law.md)
- [Deriving magnetism from electricity and relativity](deriving-magnetism-from-electricity-and-relativity.md)
- [Electric current](electric-current.md)
- [Electromagnetic four-potential](electromagnetic-four-potential.md)
- [Electromagnetism](electromagnetism-split.md)
- [Important partial differential equation](important-partial-differential-equation.md)
- [Maxwell's equations require special relativity](maxwell-s-equations-require-special-relativity.md)
- [Maxwell's equations with pointlike particles](maxwell-s-equations-with-pointlike-particles.md)
- [Particle physics](particle-physics-split.md)
- [Polarization of light](polarization-of-light.md)
- [Quantum mechanics experiment](quantum-mechanics-experiment.md)
- [Special relativity experiment](special-relativity-experiment.md)
- [System of partial differential equations](system-of-partial-differential-equations.md)
- [Wave-particle duality](wave-particle-duality.md)
