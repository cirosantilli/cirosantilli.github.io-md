# Derivation of the Klein-Gordon equation

↑ **Parent:** [Klein-Gordon equation](klein-gordon-equation.md)

The Klein-Gordon equation directly uses a more naive [relativistic energy](relativistic-energy.md) guess of $p^2 + m^2$ squared.

But since this is [quantum mechanics](quantum-mechanics-split.md), we feel like making $p$ into the "[momentum operator](momentum-operator.md)", just like in the [Schrödinger equation](schrodinger-equation.md).

But we don't really know how to apply the momentum operator twice, because it is a [gradient](gradient.md), so the first application goes from a scalar field to the vector field, and the second one...

So we just cheat and try to use the [laplace operator](laplace-operator.md) instead because there's some squares on it:

$$
H = \laplacian{} + m^2
$$

But then, we have to avoid taking the square root to reach a first derivative in time, because we don't know how to take the square root of that operator expression.

So the Klein-Gordon equation just takes the approach of using this squared Hamiltonian instead.

Since it is a Hamiltonian, and comparing it to the [Schrödinger equation](schrodinger-equation.md) which looks like:

$$
H \psi = i \pdv{\psi}{t}
$$

taking the Hamiltonian twice leads to:

$$
H^2 \psi = - \pdv{^2 \psi}{^2 t}
$$

We can contrast this with the [Dirac equation](dirac-equation.md), which instead attempts to explicitly construct an operator which squared coincides with the relativistic formula: [derivation of the Dirac equation](derivation-of-the-dirac-equation.md).

## ↑ Ancestors (9)

1. [Klein-Gordon equation](klein-gordon-equation.md)
2. [Dirac equation](dirac-equation.md)
3. [Relativistic quantum mechanics](relativistic-quantum-mechanics-split.md)
4. [Quantum mechanics](quantum-mechanics-split.md)
5. [Particle physics](particle-physics-split.md)
6. [Physics](physics-split.md)
7. [Natural science](natural-science.md)
8. [Science](science-split.md)
9. [Ciro Santilli's Homepage](split.md)
