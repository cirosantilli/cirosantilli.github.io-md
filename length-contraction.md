# Length contraction

↑ **Parent:** [Lorentz transformation](lorentz-transformation.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Length_contraction)

Suppose that a rod has is length $L$ measured on a rest frame $S$ (or maybe even better: two identical rulers were manufactured, and one is taken on a spaceship, a bit like the [twin paradox](twin-paradox.md)).

Question: what is the length $L'$ than an observer in frame $S'$ moving relative to $S$ as speed $v$ observe the rod to be?

The key idea is that there are two events to consider in each frame, which we call 1 and 2:
- the left end of the rod is an observation event at a given position at a given time: $x_1$ and $t_1$ for $S$ or $x'_1$ and $t'_1$ for $S'$
- the right end of the rod is an observation event at a given position at a given time : $x_2$ and $t_2$ for $S$ or $x'_2$ and $t'_2$ for $S'$
Note that what you visually observe on a photograph is a different measurement to the more precise/easy to calculate two event measurement. On a photograph, it seems you might not even see the contraction in some cases as mentioned at [https://en.wikipedia.org/wiki/Terrell_rotation](https://en.wikipedia.org/wiki/Terrell_rotation)

Measuring a length means to measure the $x_2 - x_1$ difference for a single point in time in your frame ($t2 = t1$).

So what we want to obtain is $x'_2 - x'_1$ for any given time $t'2 = t'1$.

In summary, we have:

$$
\begin{aligned}
L  &= x_2  &- x_1 \\
L' &= x'_2 &- x'_1
t'_2 = t'_1
\end{aligned}
$$

By plugging those values into the [Lorentz transformation](lorentz-transformation.md), we can eliminate $t_2 and t_1$, and conclude that for any $t'_2 = t'_1$, the length contraction relation holds:

$$
L' = \frac{L}{\gamma}
$$

The key question that needs intuitive clarification then is: but how can this be symmetric? How can both observers see each other's rulers shrink?

And the key answer is: because to the second observer, the measurements made by the first observer are not simultaneous. Notably, the two measurement events are obviously [spacelike-separated events](spacelike-separated-event.md) by looking at the [light cone](light-cone.md), and therefore can be measured even in different orders by different observers.

**Table of contents**

- [Terrell rotation](terrell-rotation.md)

## ↑ Ancestors (8)

1. [Lorentz transformation](lorentz-transformation.md)
2. [Special relativity](special-relativity.md)
3. [Relativity](relativity-split.md)
4. [Particle physics](particle-physics-split.md)
5. [Physics](physics-split.md)
6. [Natural science](natural-science.md)
7. [Science](science-split.md)
8. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (4)

- [Moving magnet and conductor problem](moving-magnet-and-conductor-problem.md)
- [Special relativity](special-relativity.md)
- [Terrell rotation](terrell-rotation.md)
- [Transversal time dilation](transversal-time-dilation.md)
