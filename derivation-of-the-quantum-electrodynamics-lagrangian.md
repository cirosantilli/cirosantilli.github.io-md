# Derivation of the quantum electrodynamics Lagrangian

↑ **Parent:** [Quantum electrodynamics Lagrangian](quantum-electrodynamics-lagrangian.md)

Like the rest of the [Standard Model Lagrangian](standard-model-lagrangian.md), this can be split into two parts:
- [spacetime symmetry](spacetime-symmetry.md): reaches the [derivation of the Dirac equation](derivation-of-the-dirac-equation.md), but has no interactions
- add the [$U(1)$](unitary-group-of-degree-1.md) [internal symmetry](internal-symmetry.md) to add interactions, which reaches the full equation

<a id="video-deriving-the-qed-lagrangian-by-dietterich-labs-2018"></a>
**[Video 17](#video-deriving-the-qed-lagrangian-by-dietterich-labs-2018). Deriving the qED Lagrangian by Dietterich Labs (2018)** [Source](https://www.youtube.com/watch?v=IFRyN3fQMO8). As mentioned at the start of the video, he starts with the [Dirac equation](dirac-equation.md) Lagrangian derived in a previous video. It has nothing to do with [electromagnetism](electromagnetism-split.md) specifically.

He notes that that [Dirac Lagrangian](dirac-lagrangian.md), besides being globally [Lorentz invariant](lorentz-invariant.md), it also also has a global [$U(1)$](unitary-group-of-degree-1.md) invariance.

However, it does not have a local invariance if the [$U(1)$](unitary-group-of-degree-1.md) transformation depends on the point in spacetime.

He doesn't mention it, but I think this is highly desirable, because in general [local symmetries of the Lagrangian imply conserved currents](local-symmetries-of-the-lagrangian-imply-conserved-currents.md), and in this case we want conservation of charges.

To fix that, he adds an extra [gauge field](gauge-field.md) $A_\mu$ (a field of $4 \times 4$ matrices) to the regular derivative, and the resulting derivative has a fancy name: the [covariant derivative](covariant-derivative.md).

Then finally he notes that this [gauge field](gauge-field.md) he had to add has to transform exactly like the [electromagnetic four-potential](electromagnetic-four-potential.md)!

So he uses that as the gauge, and also adds in the [Maxwell Lagrangian](maxwell-lagrangian.md) in the same go. It is kind of a guess, but it is a natural guess, and it turns out to be correct.

[https://www.youtube.com/watch?v=IFRyN3fQMO8&lc=UgzNGkLXdwcSl7z8Lap4AaABAg](https://www.youtube.com/watch?v=IFRyN3fQMO8&lc=UgzNGkLXdwcSl7z8Lap4AaABAg)

---

## ↑ Ancestors (10)

1. [Quantum electrodynamics Lagrangian](quantum-electrodynamics-lagrangian.md)
2. [Quantum electrodynamics](quantum-electrodynamics.md)
3. [Quantum field theory](quantum-field-theory-split.md)
4. [Relativistic quantum mechanics](relativistic-quantum-mechanics-split.md)
5. [Quantum mechanics](quantum-mechanics-split.md)
6. [Particle physics](particle-physics-split.md)
7. [Physics](physics-split.md)
8. [Natural science](natural-science.md)
9. [Science](science-split.md)
10. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (1)

- [Why do symmetries such as SU(3), SU(2) and U(1) matter in particle physics?](why-do-symmetries-such-as-su-3-su-2-and-u-1-matter-in-particle-physics.md)
