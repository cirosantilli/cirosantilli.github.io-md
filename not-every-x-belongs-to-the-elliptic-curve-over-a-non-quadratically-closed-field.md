# Not every $x$ belongs to the elliptic curve over a non quadratically closed field

↑ **Parent:** [Domain of an elliptic curve](domain-of-an-elliptic-curve.md)

One major difference between the [elliptic curve over a finite field](elliptic-curve-over-a-finite-field.md) or the [elliptic curve over the rational numbers](elliptic-curve-over-the-rational-numbers.md) the [elliptic curve over the real numbers](elliptic-curve-over-the-real-numbers.md) is that not every possible $x$ generates a member of the curve.

This is because on the [Equation 1. "Definition of the elliptic curves"](elliptic-curve.md#equation-definition-of-the-elliptic-curves) we see that given an $x$, we calculate $x^3 + ax + b$, which always produces an element $y^2$.

But then we are not necessarily able to find an $y$ for the $y^2$, because not all [fields](field-mathematics.md) are not [quadratically closed fields](quadratically-closed-field.md).

For example: with $a = 1$ and $b = 1$, taking $x = 1$ gives:

$$
y^2 = 1^3 + 1 \times 1 + 1 = 3
$$

and therefore there is no $y \in \Q$ that satisfies the equation. So $x = 1$ is not on the curve if we consider this [elliptic curve over the rational numbers](elliptic-curve-over-the-rational-numbers.md).

That $x$ would also not belong to [Elliptic curve over the finite field](elliptic-curve-over-a-finite-field.md) $\F_4$, because doing everything $\mod 4$ we have:

$$
\begin{aligned}
0*0 &= 0 &    &\mod 4 \\
1*1 &= 1 &    &\mod 4 \\
2*2 &= 4 &= 0 &\mod 4 \\
3*3 &= 9 &= 1 &\mod 4 \\
\end{aligned}
$$

Therefore, there is no element $y \in \F_4$ such that $y \times y = 2$ or $y \times y = 3$, i.e. $2$ and $3$ don't have a [multiplicative inverse](multiplicative-inverse.md).

For the [real numbers](real-number.md), it would work however, because the [real numbers](real-number.md) are a [quadratically closed field](quadratically-closed-field.md), and $\sqrt{3} \in \R$.

For this reason, it is not necessarily trivial to determine the [number of elements of an elliptic curve](number-of-elements-of-an-elliptic-curve.md).

**Table of contents**

- [Number of elements of an elliptic curve](number-of-elements-of-an-elliptic-curve.md)

## ↑ Ancestors (7)

1. [Domain of an elliptic curve](domain-of-an-elliptic-curve.md)
2. [Elliptic curve](elliptic-curve.md)
3. [Algebraic geometry](algebraic-geometry.md)
4. [Algebra](algebra-split.md)
5. [Area of mathematics](area-of-mathematics.md)
6. [Mathematics](mathematics-split.md)
7. [Ciro Santilli's Homepage](split.md)
