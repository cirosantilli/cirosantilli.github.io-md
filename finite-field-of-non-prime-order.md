# Finite field of non-prime order

↑ **Parent:** [Finite field](finite-field.md)

As per [classification of finite fields](classification-of-finite-fields.md) those must be of [prime power](prime-power.md) order.

[Video 4. "Finite fields made easy by Randell Heyman (2015)"](finite-field.md#video-finite-fields-made-easy-by-randell-heyman-2015) at [https://youtu.be/z9bTzjy4SCg?t=159](https://youtu.be/z9bTzjy4SCg?t=159) shows how for order $9 = 3 \times 3$. Basically, for order $p^n$, we take:
- each element is a polynomial in $GF(p)[x]$, $GF(p)[x]$, the [polynomial ring over the finite field $GF(p)$](polynomial-over-a-field.md) with degree smaller than $n$. We've just seen how to construct $GF(p)$ for prime $p$ above, so we're good there.
- addition works element-wise modulo on $GF(p)$
- multiplication is done modulo an [irreducible polynomial](irreducible-polynomial.md) of order $n$
For a worked out example, see: [GF(4)](gf-4.md).

## ↑ Ancestors (8)

1. [Finite field](finite-field.md)
2. [Field (mathematics)](field-mathematics.md)
3. [Ring (mathematics)](ring-mathematics.md)
4. [Group](group-split.md)
5. [Algebra](algebra-split.md)
6. [Area of mathematics](area-of-mathematics.md)
7. [Mathematics](mathematics-split.md)
8. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (2)

- [Finite field](finite-field.md)
- [GF(4)](gf-4.md)
