# Computational quantum mechanics

↑ **Parent:** [Solutions of the Schrodinger equation](solutions-of-the-schrodinger-equation.md)

- [https://www.youtube.com/watch?v=1Z9wo2CzJO8](https://www.youtube.com/watch?v=1Z9wo2CzJO8) "Schrodinger equation solved numerically in 3D" by Tetsuya Matsuno. 3D hydrogen atom, code may be hidden in some paper, maybe
- [https://www.youtube.com/playlist?list=PLdCdV2GBGyXM0j66zrpDy2aMXr6cgrBJA](https://www.youtube.com/playlist?list=PLdCdV2GBGyXM0j66zrpDy2aMXr6cgrBJA) "Computational Quantum Mechanics" by Let's Code Physics. Uses a 1D trinket.io.
- [https://www.youtube.com/watch?v=BBt8EugN03Q](https://www.youtube.com/watch?v=BBt8EugN03Q) Simulating Quantum Systems \[Split Operator Method\] by LeiosOS (2018)
- [https://www.youtube.com/watch?v=86x0_-JGlGQ](https://www.youtube.com/watch?v=86x0_-JGlGQ) Simulating the Quantum World on a [Classical Computer](classical-computer.md) by Garnet Chan (2016) discusses how modeling only local [entanglement](quantum-entanglement.md) can make certain simulations feasible

<a id="video-simulation-of-the-time-dependent-schrodinger-equation-javascript-animation-by-coding-physics-2019"></a>
**[Video 7](#video-simulation-of-the-time-dependent-schrodinger-equation-javascript-animation-by-coding-physics-2019). Simulation of the time-dependent Schrodinger equation (JavaScript Animation) by Coding Physics (2019)** [Source](http://youtube.com/watch?v=g4wuSgwLT9I). Source code: [https://github.com/CodingPhysics/Schroedinger](https://github.com/CodingPhysics/Schroedinger). One dimensional potentials, non-interacting particles. The code is clean, graphics based on [https://github.com/processing/p5.js](https://github.com/processing/p5.js), and all maths from scratch. Source organization and comments are typical of numerical code, the anonymous author is was likely a Fortran user in the past.

A potential change patch in `sketch.js`:
```
-   potential:     x => 2E+4*Math.pow((4*x - 1)*(4*x - 3),2),
+ potential:     x => 4*Math.pow(x - 0.5, 2),
```

---

<a id="video-quantum-mechanics-5b-schrodinger-equation-ii-by-viascience-2013"></a>
**[Video 8](#video-quantum-mechanics-5b-schrodinger-equation-ii-by-viascience-2013). Quantum Mechanics 5b - Schrödinger Equation II by ViaScience (2013)** [Source](http://youtube.com/watch?v=ee4LqXRlQmE). 2D non-interacting particle in a box, description says using [Scilab](scilab.md) and points to source. Has a double slit simulation.

<a id="video-visualization-of-quantum-physics-quantum-mechanics-by-udiprod-2017"></a>
**[Video 9](#video-visualization-of-quantum-physics-quantum-mechanics-by-udiprod-2017). Visualization of Quantum Physics (Quantum Mechanics) by udiprod (2017)** [Source](https://www.youtube.com/watch?v=p7bzE1E5PMY). Closed source, but a fantastic visualization and explanation of a 1D free wave packet, including how measurement snaps position to the measured range, [position and momentum space](position-and-momentum-space.md) and the [uncertainty principle](uncertainty-principle.md).

**Table of contents**

- [Why it is hard to simulate quantum systems?](why-it-is-hard-to-simulate-quantum-systems.md)
- [Computational quantum mechanics software](computational-quantum-mechanics-software.md)
  - [Quantum ESPRESSO](quantum-espresso.md)
  - [QuTiP](qutip.md)

## ↑ Ancestors (9)

1. [Solutions of the Schrodinger equation](solutions-of-the-schrodinger-equation.md)
2. [Schrödinger equation](schrodinger-equation.md)
3. [Non-relativistic quantum mechanics](non-relativistic-quantum-mechanics.md)
4. [Quantum mechanics](quantum-mechanics-split.md)
5. [Particle physics](particle-physics-split.md)
6. [Physics](physics-split.md)
7. [Natural science](natural-science.md)
8. [Science](science-split.md)
9. [Ciro Santilli's Homepage](split.md)
