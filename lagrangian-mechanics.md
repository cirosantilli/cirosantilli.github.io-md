# Lagrangian mechanics

↑ **Parent:** [Mechanics](mechanics-split.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Lagrangian_mechanics)

Originally it was likely created to study constrained mechanical systems where you want to use some "custom convenient" variables to parametrize things instead of global x, y, z. Classical examples that you must have in mind include:
- [compound Atwood machine](compound-atwood-machine.md). Here, we can use the coordinates as the heights of masses relative to the [axles](axle.md) rather than absolute heights relative to the ground
- [double pendulum](double-pendulum.md), using two angles. The Lagrangian approach is simpler than using Newton's laws
  - [pendulum](pendulum.md), use angle instead of x/y
- [two-body problem](two-body-problem.md), use the distance between the bodies
[lagrangian mechanics lectures by Michel van Biezen (2017)](lagrangian-mechanics-lectures-by-michel-van-biezen-2017.md) is a good starting point.

When doing lagrangian mechanics, we just lump together all generalized coordinates into a single vector $\va{q}(t) : \R \to \R^n$ that maps time to the full state:

$$
\va{q}(t) = [q_1(t), q_2(t), q_3(t), ..., q_n(t)]
$$

where each component can be anything, either the x/y/z coordinates relative to the ground of different particles, or angles, or nay other crazy thing we want.

The [Lagrangian](lagrangian.md) is a function $\R^n \times \R^n \times \R \to \R$ that maps:

$$
L(\va{q}(t), \dot{\va{q}}(t), t)
$$

to a real number.

Then, the [stationary action principle](stationary-action-principle.md) says that the actual path taken obeys the [Euler-Lagrange equation](euler-lagrange-equation.md):

$$
\pdv{L(\va{q}(t), \dot{\va{q}}(t), t)}{q_i} - \dv{}{t}\pdv{L(\va{q}(t), \dot{\va{q}}(t), t)}{\dot{q_i}} = 0
$$

This produces a [system of partial differential equations](system-of-partial-differential-equations.md) with:
- $n$ equations
- $n$ unknown functions $q_i$
- at most second order derivatives of $q_i$. Those appear because of the chain rule on the second term.

The mixture of so many derivatives is a bit mind mending, so we can clarify them a bit further. At:

$$
\pdv{L(\va{q}(t), \dot{\va{q}}(t), t)}{q_i}
$$

the $q_i$ is just identifying which argument of the Lagrangian we are differentiating by: the i-th according to the order of our definition of the Lagrangian. It is not the actual function, just a mnemonic.

Then at:

$$
\dv{}{t}\pdv{L(\va{q}(t), \dot{\va{q}}(t), t)}{\dot{q_i}}
$$


- the $\pdv{}{\dot{q_i}}$ part is just like the previous term, $\dot{q_i}$ just identifies the argument with index $n + i$ ($n$ because we have the $n$ non derivative arguments)
- after the partial derivative is taken and returns a new function $\pdv{L(\va{q}(t), \dot{\va{q}}(t), t)}{\dot{q_i}}$, then the [multivariable chain rule](multivariable-chain-rule.md) comes in and expands everything into $2n + 1$ terms

However, people later noticed that the Lagrangian had some nice properties related to [Lie group](lie-group.md) continuous symmetries.

Basically it seems that the easiest way to come up with new [quantum field theory](quantum-field-theory-split.md) models is to first find the Lagrangian, and then derive the equations of motion from them.

For every [continuous symmetry](continuous-symmetry.md) in the system (modelled by a [Lie group](lie-group.md)), there is a corresponding conservation law: [local symmetries of the Lagrangian imply conserved currents](local-symmetries-of-the-lagrangian-imply-conserved-currents.md).  
[Genius: Richard Feynman and Modern Physics by James Gleick (1994)](genius-richard-feynman-and-modern-physics-by-james-gleick-1994.md) chapter "The Best Path" mentions that [Richard Feynman](richard-feynman-split.md) didn't like the [Lagrangian mechanics](lagrangian-mechanics.md) approach when he started university at [MIT](massachusetts-institute-of-technology.md), because he felt it was too magical. The reason is that the Lagrangian approach basically starts from the principle that "nature minimizes the action across time globally". This implies that things that will happen in the future are also taken into consideration when deciding what has to happen before them! Much like the lifeguard in the [lifegard problem](lifegard-problem.md) making global decisions about the future. However, chapter "Least Action in Quantum Mechanics" comments that Feynman later notice that this was indeed necessary while developping [Wheeler-Feynman absorber theory](wheeler-feynman-absorber-theory.md) into [quantum electrodynamics](quantum-electrodynamics.md), because they felt that it would make more sense to consider things that way while playing with ideas such as [positrons are electrons travelling back in time](positrons-are-electrons-travelling-back-in-time.md). This is in contrast with [Hamiltonian mechanics](hamiltonian-mechanics.md), where the idea of time moving foward is more directly present, e.g. as in the [Schrödinger equation](schrodinger-equation.md).

Furthermore, given the symmetry, we can calculate the derived conservation law, and vice versa.

And partly due to the above observations, it was noticed that the easiest way to describe the fundamental laws of [particle physics](particle-physics-split.md) and make calculations with them is to first formulate their Lagrangian somehow: [S](s.md).

TODO advantages:
- [https://physics.stackexchange.com/questions/254266/advantages-of-lagrangian-mechanics-over-newtonian-mechanics](https://physics.stackexchange.com/questions/254266/advantages-of-lagrangian-mechanics-over-newtonian-mechanics) on [Physics Stack Exchange](physics-stack-exchange.md), [fucking](sexual-intercourse.md) closed question...
- [https://www.quora.com/Why-was-Lagrangian-formalism-needed-in-the-presence-of-Newtonian-formalism](https://www.quora.com/Why-was-Lagrangian-formalism-needed-in-the-presence-of-Newtonian-formalism) 
- [https://www.researchgate.net/post/What_is_the_advantage_of_Lagrangian_formalism_over_Hamiltonian_formalism_in_QFT](https://www.researchgate.net/post/What_is_the_advantage_of_Lagrangian_formalism_over_Hamiltonian_formalism_in_QFT)

Bibliography:
- [http://www.physics.usu.edu/torre/6010_Fall_2010/Lectures.html](http://www.physics.usu.edu/torre/6010_Fall_2010/Lectures.html) Physics 6010 Classical Mechanics lecture notes by Charles Torre from Utah State University published on 2010,
  - Classical physics only. The last lecture: [http://www.physics.usu.edu/torre/6010_Fall_2010/Lectures/12.pdf](http://www.physics.usu.edu/torre/6010_Fall_2010/Lectures/12.pdf) mentions [Lie algebra](lie-algebra.md) more or less briefly.
- [http://www.damtp.cam.ac.uk/user/tong/dynamics/two.pdf](http://www.damtp.cam.ac.uk/user/tong/dynamics/two.pdf) by [David Tong](david-tong.md)

<a id="video-euler-lagrange-equation-explained-intuitively-lagrangian-mechanics-by-physics-videos-by-eugene-khutoryansky-2018"></a>
**[Video 2](#video-euler-lagrange-equation-explained-intuitively-lagrangian-mechanics-by-physics-videos-by-eugene-khutoryansky-2018). Euler-Lagrange equation explained intuitively - Lagrangian Mechanics by Physics Videos by Eugene Khutoryansky (2018)** [Source](https://www.youtube.com/watch?v=EceVJJGAFFI). Well, unsurprisingly, it is exactly what you can expect from an Eugene Khutoryansky video.

**Table of contents**

- [Lagrangian mechanics lectures by Michel van Biezen (2017)](lagrangian-mechanics-lectures-by-michel-van-biezen-2017.md)
- [Action (physics)](action-physics.md)
  - [Stationary action principle](stationary-action-principle.md)
    - [Calculus of variations](calculus-of-variations.md)
      - [Functional](functional.md)
      - [Euler-Lagrange equation](euler-lagrange-equation.md)
        - [Equations of motion](equations-of-motion.md)
- [Lagrangian](lagrangian.md)
  - [Lagrangian (field theory)](lagrangian-field-theory.md)
    - [Lagrangian density](lagrangian-density.md)
  - [Generalized coordinate](generalized-coordinate.md)
- [Noether's theorem](noether-s-theorem.md)
  - [Time invariance implies energy conservation](time-invariance-implies-energy-conservation.md)
- [Spontaneous symmetry breaking](spontaneous-symmetry-breaking.md)
- [Hamiltonian mechanics](hamiltonian-mechanics.md)
  - [Lagrangian vs Hamiltonian](lagrangian-vs-hamiltonian.md)
  - [Phase space coordinate](phase-space-coordinate.md)
  - [Hamilton's equations](hamilton-s-equations.md)
  - [Poisson bracket](poisson-bracket.md)
- [Equivalence between Lagrangian and Hamiltonian formalisms](equivalence-between-lagrangian-and-hamiltonian-formalisms.md)
  - [Legendre transformation](legendre-transformation.md)

## ↑ Ancestors (5)

1. [Mechanics](mechanics-split.md)
2. [Physics](physics-split.md)
3. [Natural science](natural-science.md)
4. [Science](science-split.md)
5. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (11)

- [Compound Atwood machine](compound-atwood-machine.md)
- [Euler-Lagrange equation](euler-lagrange-equation.md)
- [Genius: Richard Feynman and Modern Physics by James Gleick (1994)](genius-richard-feynman-and-modern-physics-by-james-gleick-1994.md)
- [Hamilton's equations](hamilton-s-equations.md)
- [Hamiltonian mechanics](hamiltonian-mechanics.md)
- [Lagrangian](lagrangian.md)
- [Lagrangian mechanics](lagrangian-mechanics.md)
- [Lagrangian vs Hamiltonian](lagrangian-vs-hamiltonian.md)
- [Lie group](lie-group.md)
- [Lecture 2](quantum-field-theory-lecture-by-tobias-osborne-2017/lecture-2.md)
- [Two-body problem](two-body-problem.md)
