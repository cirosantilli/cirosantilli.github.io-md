# Lorentz transform consequence: everyone sees the same speed of light

↑ **Parent:** [Lorentz transformation](lorentz-transformation.md)

OK, so let's verify the main desired consequence of the [Lorentz transformation](lorentz-transformation.md): that everyone observes the same [speed of light](speed-of-light.md).

Observers will measure the speed of light by calculating how long it takes the light going towards $+x$ cross a rod of length $L = x_2 - x_1$ laid in the x axis at position $X1$.

TODO image.

Each observer will observe two events:
- $(t_1, x_1, y_1, z_1)$: the light touches the left side of the rod
- $(t_2, x_2, y_2, z_2)$: the light touches the right side of the rod

Supposing that the standing observer measures the speed of light as $c$ and that light hits the left side of the rod at time $T1$, then he observes the coordinates:

$$
\begin{aligned}
t_1 & = T1 \\
x_1 & = X1 \\
t_2 & = \frac{L}{c} \\
x_2 & = X1 + L \\
\end{aligned}
$$

Now, if we transform for the moving observer:

$$
\begin{aligned}
t_1' & = \gamma \left( t_1 - \frac{v x_1}{c^2} \right) \\
x_1' & = \gamma \left( x_1 - v t_1             \right) \\
t_2' & = \gamma \left( t_2 - \frac{v x_2}{c^2} \right) \\
x_2' & = \gamma \left( x_2 - v t_2             \right) \\
\end{aligned}
$$

and so the moving observer measures the speed of light as:

$$
\begin{aligned}
c' & = \frac{x_2' - x_1'}{t_2' - t_1'} \\
   & = \frac{(x_2 - v t_2) - (x_1 - v t_1)}{(t_2 - \frac{v x_2}{c^2}) - (t_1 - \frac{v x_1}{c^2})} \\
   & = \frac{(x_2 - x_1) - v (t_2 - t_1)}{(t_2 - t_1) - \frac{v}{c^2} (x_2 - x_1)} \\
   & = \frac{\frac{x_2 - x_1}{t_2 - t_1} - v}{1 - \frac{v}{c^2} \frac{x_2 -x_1}{t_2 - t_1}} \\
   & = \frac{c - v}{1 - \frac{v}{c^2} c} \\
   & = \frac{c - v}{\frac{c - v}{c}} \\
   & = c \\
\end{aligned}
$$

## ↑ Ancestors (8)

1. [Lorentz transformation](lorentz-transformation.md)
2. [Special relativity](special-relativity.md)
3. [Relativity](relativity-split.md)
4. [Particle physics](particle-physics-split.md)
5. [Physics](physics-split.md)
6. [Natural science](natural-science.md)
7. [Science](science-split.md)
8. [Ciro Santilli's Homepage](split.md)
