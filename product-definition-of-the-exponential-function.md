# Product definition of the exponential function

↑ **Parent:** [Definition of the exponential function](definition-of-the-exponential-function.md)

$$
e^x = \lim_{n\to\infty} \left(1+\frac x n \right)^n
$$

The basic intuition for this is to start from the origin and make small changes to the function based on its known derivative at the origin.

More precisely, we know that for any base b, [exponentiation](exponentiation.md) satisfies:
- $b^{x + y} = b^x b^y$.
- $b^{0} = 1$.
And we also know that for $b = e$ in particular that we satisfy the [exponential function differential equation](exponential-function-differential-equation.md) and so:

$$
\dv{e^x}{x}(0) = 1
$$

One interesting fact is that the only thing we use from the [exponential function differential equation](exponential-function-differential-equation.md) is the value around $x = 0$, which is quite little information! This idea is basically what is behind the importance of the ralationship between [Lie group-Lie algebra correspondence](lie-group-lie-algebra-correspondence.md) via the [exponential map](exponential-map.md). In the more general settings of groups and [manifolds](manifold.md), restricting ourselves to be near the origin is a huge advantage.

Now suppose that we want to calculate $e^1$. The idea is to start from $e^0$ and then then to use the first order of the [Taylor series](taylor-series.md) to extend the known value of $e^0$ to $e^1$.

E.g., if we split into 2 parts, we know that:

$$
e^1 = e^{1/2}e^{1/2}
$$

or in three parts:

$$
e^1 = e^{1/3}e^{1/3}e^{1/3}
$$

so we can just use arbitrarily many parts $e^{1/n}$ that are arbitrarily close to $x = 0$:

$$
e^1 = (e^{1/n})^n
$$

and more generally for any $x$ we have:

$$
e^x = (e^{x/n})^n
$$

Let's see what happens with the Taylor series. We have near $y = 0$ in [little-o notation](little-o-notation.md):

$$
e^y = 1 + y + o(y)
$$

Therefore, for $y = x/n$, which is near $y = 0$ for any fixed $x$:

$$
e^{x/n} = 1 + x/n + o(1/n)
$$

and therefore:

$$
e^x = (e^{x/n})^n = (1 + x/n + o(1/n))^n
$$

which is basically the formula tha we wanted. We just have to convince ourselves that at $\lim_{n \to \infty}$, the $o(1/n)$ disappears, i.e.:

$$
(1 + x/n + o(1/n))^n = (1 + x/n)^n
$$

To do that, let's multiply $e^y$ by itself once:

$$
e^y e^y = (1 + y + o(y))(1 + y + o(y)) = 1 + 2y + o(y)
$$

and multiplying a third time:

$$
e^y e^y e^y = (1 + 2y + o(y))(1 + y + o(y)) = 1 + 3y + o(y)
$$

TODO conclude.

## ↑ Ancestors (10)

1. [Definition of the exponential function](definition-of-the-exponential-function.md)
2. [Exponential function](exponential-function.md)
3. [Exponentiation](exponentiation.md)
4. [Numeric function](numeric-function.md)
5. [Function by signature](function-by-signature.md)
6. [Function (mathematics)](function-mathematics.md)
7. [Formalization of mathematics](formalization-of-mathematics-split.md)
8. [Area of mathematics](area-of-mathematics.md)
9. [Mathematics](mathematics-split.md)
10. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (1)

- [Exponential map (Lie theory)](exponential-map-lie-theory.md)
