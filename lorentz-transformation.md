# Lorentz transformation

↑ **Parent:** [Special relativity](special-relativity.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Lorentz_transformation)

The equation that allows us to calculate stuff in [special relativity](special-relativity.md)!

Take two observers with identical rules and stopwatch, and aligned axes, but one is on a car moving at towards the $+x$ direction at speed $v$.

TODO image.

When both observe an event, if we denote:
- $(t, x, y, z)$ the observation of the standing observer
- $(t', x', y', z')$ the observation of the ending observer on a car
It is of course arbitrary who is standing and who is moving, we will just use the term "standing" for the one without primes.

Then the coordinates of the event observed by the observer on the car are:

$$
\begin{aligned}
t' & = \gamma \left( t - \frac{v x}{c^2} \right) \\
x' & = \gamma \left( x - v t \right) \\
y' & = y \\
z' & = z
\end{aligned}
$$

where:

$$
\gamma = \frac{1}{\sqrt{1 - \left(\frac{v}{c}\right)^2}}
$$

Note that if $\frac{v}{c}$ tends towards zero, then this reduces to the usual [Galilean transformations](galilean-transformation.md) which our intuition expects:

$$
\begin{aligned}
t' & = t
x' & = x - v t \\
y' & = y \\
z' & = z
\end{aligned}
$$

This explains why we don't observe special relativity in our daily lives: macroscopic objects move too slowly compared to light, and $\frac{v}{c}$ is almost zero.

**Table of contents**

- [Lorentz covariance](lorentz-covariance.md)
  - [Lorentz invariant](lorentz-invariant.md)
- [Lorentz transform consequence: everyone sees the same speed of light](lorentz-transform-consequence-everyone-sees-the-same-speed-of-light.md)
- [Length contraction](length-contraction.md)
  - [Terrell rotation](terrell-rotation.md)
- [Time dilation](time-dilation.md)
  - [Transversal time dilation](transversal-time-dilation.md)
  - [Transverse Doppler effect](transverse-doppler-effect.md)
- [Twin paradox](twin-paradox.md)

## ↑ Ancestors (7)

1. [Special relativity](special-relativity.md)
2. [Relativity](relativity-split.md)
3. [Particle physics](particle-physics-split.md)
4. [Physics](physics-split.md)
5. [Natural science](natural-science.md)
6. [Science](science-split.md)
7. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (5)

- [Lagrangian density](lagrangian-density.md)
- [Length contraction](length-contraction.md)
- [Lorentz covariance](lorentz-covariance.md)
- [Lorentz transform consequence: everyone sees the same speed of light](lorentz-transform-consequence-everyone-sees-the-same-speed-of-light.md)
- [Spacetime diagram](spacetime-diagram.md)
