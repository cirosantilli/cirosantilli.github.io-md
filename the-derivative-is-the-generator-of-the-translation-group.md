# The derivative is the generator of the translation group

↑ **Parent:** [Translation group](translation-group.md)

Take the group of all [Translation](translation-geometry.md) in [$\R^1$](real-line.md).

Let's see how the [generator](generator-of-a-lie-algebra.md) of this group is the [derivative](derivative.md) [operator](linear-operator.md):

$$
\pdv{}{x}
$$

The way to think about this is:
- the translation group operates on the argument of a function $f(x)$
- the generator is an [operator](linear-operator.md) that operates on $f$ itself

So let's take the [exponential map](exponential-map-lie-theory.md):

$$
e^{x_0\pdv{}{x}}f(x) = \left( 1 + x_0 \pdv{}{x} + x_0^2 \pdv{^2}{x^2} + \ldots\right)f(x)
$$

and we notice that this is exactly the [Taylor series](taylor-series.md) of $f(x)$ around the identity element of the translation group, which is 0! Therefore, if $f(x)$ behaves nicely enough, within some [radius of convergence](radius-of-convergence.md) around the origin we have for finite $x_0$:

$$
e^{x_0\pdv{}{x}}f(x) = f(x + x_0)
$$

This example shows clearly how the [exponential map](exponential-map-lie-theory.md) applied to a (differential) [operator](linear-operator.md) can generate finite (non-infinitesimal) [Translation](translation-geometry.md)!

## ↑ Ancestors (11)

1. [Translation group](translation-group.md)
2. [Translation (geometry)](translation-geometry.md)
3. [Galilean transformation](galilean-transformation.md)
4. [Poincaré group](poincare-group.md)
5. [Important Lie group](important-lie-group.md)
6. [Lie group](lie-group.md)
7. [Differential geometry](differential-geometry.md)
8. [Geometry](geometry-split.md)
9. [Area of mathematics](area-of-mathematics.md)
10. [Mathematics](mathematics-split.md)
11. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (1)

- [Exponential map (Lie theory)](exponential-map-lie-theory.md)
