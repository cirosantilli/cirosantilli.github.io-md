# Euler-Lagrange equation

↑ **Parent:** [Calculus of variations](calculus-of-variations.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Euler–Lagrange equation)

Let's start with the one dimensional case. Let the $q : \R \to \R$ and a [Functional](functional.md) $I$ defined by a function of three variables $F : \R^3 \to \R$:

$$
I(q) = \int_{t_0}^{t} F(t, q(t), \dot{q}(t)) dt
$$

Then, the [Euler-Lagrange equation](euler-lagrange-equation.md) gives the [maxima and minima](maxima-and-minima.md) of the that type of functional. Note that this type of functional is just one very specific type of functional amongst all possible functionals that one might come up with. However, it turns out to be enough to do most of physics, so we are happy with with it.

Given $F$, the Euler-Lagrange equations are a system of [ordinary differential equations](ordinary-differential-equation.md) constructed from that $F$ such that the solutions to that system are the maxima/minima.

In the one dimensional case, the system has a single ordinary differential equation:

$$
\pdv{F(t, q(t), \dot{q}(t))}{q} - \dv{}{t} \pdv{F(t, q(t), \dot{q}(t))}{\dot{q}} = 0
$$

By $\pdv{F}{q}$ and $\pdv{F}{\dot{q}}$ we simply mean "the [partial derivative](partial-derivative.md) of $F$ with respect to its second and third arguments". The notation is a bit confusing at first, but that's all it means.

Therefore, that expression ends up being at most a [second order](order-of-a-differential-equation.md) [ordinary differential equation](ordinary-differential-equation.md) where $q$ is the unknown, since:
- the term $\pdv{F(t, q(t), \dot{q}(t))}{q}$ is a function of $t, q(t), \dot{q}(t)$
- the term $\pdv{F(t, q(t), \dot{q}(t))}{\dot{q}}$ is a function of $t, q(t), \dot{q}(t)$. And so it's derivative with respect to time will contain only up to $\ddot{q}$

Now let's think about the multi-dimensional case. Instead of having $q : \R \to \R$, we now have $q : \R \to \R^n$. Think about the [Lagrangian mechanics](lagrangian-mechanics.md) motivation of a [double pendulum](double-pendulum.md) where for a given time we have two angles.

Let's do the 2-dimensional case then. In that case, $F$ is going to be a function of 5 variables $F : \R^5 \to \R$ rather than 3 as in the one dimensional case, and the functional looks like:

$$
I(q) = \int_{t_0}^{t} F(t, q_1(t), q_2(t), \dot{q_1}(t), \dot{q_2})(t) dt
$$

This time, the Euler-Lagrange equations are going to be a system of two [ordinary differential equations](ordinary-differential-equation.md) on two unknown functions $q_1$ and $q_2$ of order up to 2 in both variables:

$$
\pdv{F(t, q_1(t), q_2(t), \dot{q_1}(t), \dot{q_2}(t))}{q_1} - \dv{}{t} \pdv{F(t, q_1(t), q_2(t), \dot{q_1}(t), \dot{q_2}(t)}{\dot{q_1}} = 0 \\
\pdv{F(t, q_1(t), q_2(t), \dot{q_1}(t), \dot{q_2}(t))}{q_2} - \dv{}{t} \pdv{F(t, q_1(t), q_2(t), \dot{q_1}(t), \dot{q_2}(t)}{\dot{q_2}} = 0 \\
$$

At this point, notation is getting a bit clunky, so people will often condense the $q_i$ vector

$$
\pdv{F(t, \mathbf{q}(t), \dot{\mathbf{q}}(t))}{q_1} - \dv{}{t} \pdv{F(t, \mathbf{q}(t), \dot{\mathbf{q}}(t))}{\dot{q_1}} = 0 \\
\pdv{F(t, \mathbf{q}(t), \dot{\mathbf{q}}(t))}{q_2} - \dv{}{t} \pdv{F(t, \mathbf{q}(t), \dot{\mathbf{q}}(t))}{\dot{q_2}} = 0 \\
$$

or just omit the arguments of $F$ entirely:

$$
\pdv{F}{q_i} - \dv{}{t} \pdv{F}{\dot{q_i}} = 0
$$

<a id="video-calculus-of-variations-ft-flammable-maths-by-vcubingx-2020"></a>
**[Video 3](#video-calculus-of-variations-ft-flammable-maths-by-vcubingx-2020). Calculus of Variations ft. Flammable Maths by vcubingx (2020)** [Source](https://www.youtube.com/watch?v=SQLxrr9N8zM).

**Table of contents**

- [Equations of motion](equations-of-motion.md)

## ↑ Ancestors (9)

1. [Calculus of variations](calculus-of-variations.md)
2. [Stationary action principle](stationary-action-principle.md)
3. [Action (physics)](action-physics.md)
4. [Lagrangian mechanics](lagrangian-mechanics.md)
5. [Mechanics](mechanics-split.md)
6. [Physics](physics-split.md)
7. [Natural science](natural-science.md)
8. [Science](science-split.md)
9. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (5)

- [Dirac Lagrangian](dirac-lagrangian.md)
- [Equations of motion](equations-of-motion.md)
- [Euler-Lagrange equation](euler-lagrange-equation.md)
- [Hamilton's equations](hamilton-s-equations.md)
- [Lagrangian mechanics](lagrangian-mechanics.md)
