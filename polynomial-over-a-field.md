# Polynomial over a field

↑ **Parent:** [Domain of a polynomial](domain-of-a-polynomial.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Polynomial_over_a_field)

By default, we think of polynomials over the [real numbers](real-number.md) or [complex numbers](complex-number.md).

However, a polynomial can be defined over any other field just as well, the most notable example being that of a polynomial over a [finite field](finite-field.md).

For example, given the finite field of [order](order-algebra.md) 9, $GP(3)$ and with elements $\{0, 1, 2\}$, we can denote polynomials over that ring as

$$
GP(3)[x]
$$

where $x$ is the variable name.

For example, one such polynomial could be:

$$
P(x) = 2x^4 + x^2 + 2
$$

and another one:

$$
Q(X) = x^3 + 2x^2 + 2
$$

Note how all the coefficients are members of the finite field we chose.

Given this, we could evaluate the polynomial for any element of the field, e.g.:

$$
P(0) = 2 (0 \times 0 \times 0 \times 0) + (0 \times 0) + 2 = 2
P(1) = 2 (1 \times 1 \times 1 \times 1) + (1 \times 1) + 2 = 2 (1) + 1 + 2 = 2
P(2) = 2 (2 \times 2 \times 2 \times 2) + (2 \times 2) + 2 = 2 (16 % 3) + (4 % 3) + 2 = 2 + 1 + 2 = 2
$$

and so on.

We can also add polynomials as usual over the field:

$$
P(x) + Q(x) = 2x^4 + x^3 + (1+2)x^2 + (2 + 2) = 2x^4 + x^3 + (0)x^2 + 1 = 2x^4 + x^3 + 1
$$

and multiplication works analogously.

## ↑ Ancestors (9)

1. [Domain of a polynomial](domain-of-a-polynomial.md)
2. [Polynomial](polynomial.md)
3. [Numeric function](numeric-function.md)
4. [Function by signature](function-by-signature.md)
5. [Function (mathematics)](function-mathematics.md)
6. [Formalization of mathematics](formalization-of-mathematics-split.md)
7. [Area of mathematics](area-of-mathematics.md)
8. [Mathematics](mathematics-split.md)
9. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (2)

- [Finite field of non-prime order](finite-field-of-non-prime-order.md)
- [Polynomial over a ring](polynomial-over-a-ring.md)
