<h1 id="gf-4">GF(4)</h1>

↑ **Parent:** [Finite field](finite-field.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/GF(4))

[Ciro Santilli](ciro-santilli-split.md) tried to [add this example to Wikipedia](https://en.wikipedia.org/w/index.php?title=Finite_field&type=revision&diff=1044934168&oldid=1044905041), but it was reverted, so here we are, see also: [Section "Deletionism on Wikipedia"](deletionism-on-wikipedia.md).

This is a good first example of a field of a [finite field of non-prime order](finite-field-of-non-prime-order.md), this one is a [prime power](prime-power.md) order instead.

$4 = 2^2$, so one way to represent the elements of the field will be the to use the 4 polynomials of degree 1 over [GF(2)](gf-2.md):
- 0X + 0
- 0X + 1
- 1X + 0
- 1X + 1

Note that we refer in this definition to anther field, but that is fine, because we only refer to fields of [prime](prime-number.md) order such as [GF(2)](gf-2.md), because we are dealing with [prime powers](prime-power.md) only. And we have already defined fields of prime order easily previously with [modular arithmetic](modular-arithmetic.md).

Over GF(2), there is only one [irreducible polynomial](irreducible-polynomial.md) of degree 2:

$$
X^2+X+1
$$

Addition is defined element-wise with [modular arithmetic](modular-arithmetic.md) modulo 2 as defined over GF(2), e.g.:

$$
(1X + 0) + (1X + 1) = (1 + 1)X + (0 + 1) = 0X + 1
$$

Multiplication is done modulo $X^2+X+1$, which ensures that the result is also of degree 1.

For example first we do a regular multiplication:

$$
(1X + 0) \times (1X + 1) = (1 \times 1)X^2 + (1 \times 1)X + (0 \times 1)X + (0 \times 1) = 1X^2 + 1X + 0
$$

Without modulo, that would not be one of the elements of the field anymore due to the $1X^2$!

So we take the modulo, we note that:

$$
1X^2 + 1X + 0 = 1(X^2+X+1) + (0X + 1)
$$

and by the definition of modulo:

$$
(1X^2 + 1X + 0) \mod (X^2+X+1) = (0X + 1)
$$

which is the final result of the multiplication.

TODO show how taking a reducible polynomial for modulo fails. Presumably it is for a similar reason to why things fail for the prime case.

## ↑ Ancestors (8)

1. [Finite field](finite-field.md)
2. [Field (mathematics)](field-mathematics.md)
3. [Ring (mathematics)](ring-mathematics.md)
4. [Group](group-split.md)
5. [Algebra](algebra-split.md)
6. [Area of mathematics](area-of-mathematics.md)
7. [Mathematics](mathematics-split.md)
8. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (1)

- [Finite field of non-prime order](finite-field-of-non-prime-order.md)
