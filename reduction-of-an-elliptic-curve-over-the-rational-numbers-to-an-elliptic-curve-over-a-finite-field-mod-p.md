# Reduction of an elliptic curve over the rational numbers to an elliptic curve over a finite field mod p

↑ **Parent:** [Elliptic curve over the rational numbers](elliptic-curve-over-the-rational-numbers.md)

This construction takes as input:
- [elliptic curve over the rational numbers](elliptic-curve-over-the-rational-numbers.md)
- a prime number $p$
and it produces an [elliptic curve over a finite field](elliptic-curve-over-a-finite-field.md) of order $p$ as output.

The constructions is used in the [Birch and Swinnerton-Dyer conjecture](birch-and-swinnerton-dyer-conjecture.md).

To do it, we just convert the coefficients $a$ and $b$ from the [Equation 1. "Definition of the elliptic curves"](elliptic-curve.md#equation-definition-of-the-elliptic-curves) from [rational numbers](rational-number.md) to elements of the [finite field](finite-field.md).

For example, suppose we have $a = 3/4$ and we are using $p = 11$.

For the [denominator](denominator.md) $4$, we just use the [multiplicative inverse](multiplicative-inverse.md), e.g. supposing we have

$$
\frac{3}{4} \to 3 \times 4^{-1} \mod 11 = 3 \times 3 \mod 11 = 9 \mod 11
$$

where $4^{-1} = 3 \mod 11$ because $4 \times 3 = 1 \mod 11$, related: [https://math.stackexchange.com/questions/1204034/elliptic-curve-reduction-modulo-p](https://math.stackexchange.com/questions/1204034/elliptic-curve-reduction-modulo-p)

## ↑ Ancestors (8)

1. [Elliptic curve over the rational numbers](elliptic-curve-over-the-rational-numbers.md)
2. [Domain of an elliptic curve](domain-of-an-elliptic-curve.md)
3. [Elliptic curve](elliptic-curve.md)
4. [Algebraic geometry](algebraic-geometry.md)
5. [Algebra](algebra-split.md)
6. [Area of mathematics](area-of-mathematics.md)
7. [Mathematics](mathematics-split.md)
8. [Ciro Santilli's Homepage](split.md)
