# Lagrangian density

↑ **Parent:** [Lagrangian (field theory)](lagrangian-field-theory.md)

When we particles particles, the [action](action-physics.md) is obtained by integrating the [Lagrangian](lagrangian.md) over time:

$$
Action = \int_{t_0}^{t} L(x(t), \pdv{x(t)}{t}, t) dt
$$

In the case of [field](field-mathematics.md) however, we can expand the Lagrangian out further, to also integrate over the space coordinates and their derivatives.

Since we are now working with something that gets integrated over space to obtain the total action, much like [density](density.md) would be integrated over space to obtain a total mass, the name "Lagrangian density" is fitting.

E.g. for a 2-dimensional field $f(x, y, t)$:

$$
Action = \int_{t_0}^{t} L(f(x, y, t), \pdv{f(x, y, t)}{x}, \pdv{f(x, y, t)}{y}, \pdv{f(x, y, t)}{t}, x, y, t) dx dy dt
$$

Of course, if we were to write it like that all the time we would go mad, so we can just write a much more condensed [vectorized](vector-mathematics.md) version using the [gradient](gradient.md) with $x \in \R^2$:

$$
Action = \int_{t_0}^{t} L(f(x, t), \grad{f(x, t)}, x, t) dx dt
$$

And in the context of [special relativity](special-relativity.md), people condense that even further by adding $t$ to the spacetime [Four-vector](four-vector.md) as well, so you don't even need to write that separate pesky $t$.

The main point of talking about the Lagrangian density instead of a Lagrangian for fields is likely that it treats space and time in a more uniform way, which is a basic requirement of [special relativity](special-relativity.md): we have to be able to mix them up somehow to do [Lorentz transformations](lorentz-transformation.md). Notably, this is a key ingredient in a/the formulation of [quantum field theory](quantum-field-theory-split.md).

## ↑ Ancestors (8)

1. [Lagrangian (field theory)](lagrangian-field-theory.md)
2. [Lagrangian](lagrangian.md)
3. [Lagrangian mechanics](lagrangian-mechanics.md)
4. [Mechanics](mechanics-split.md)
5. [Physics](physics-split.md)
6. [Natural science](natural-science.md)
7. [Science](science-split.md)
8. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (1)

- [Yang-Mills existence and mass gap](yang-mills-existence-and-mass-gap.md)
