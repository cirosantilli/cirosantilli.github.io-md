# Divergence in Einstein notation

↑ **Parent:** [Einstein notation for partial derivatives](einstein-notation-for-partial-derivatives.md)

First we write a [vector field](vector-field.md) as:

$$
F(x_0, x_1, x_2) = (F^0(x_0, x_1, x_2), F^1(x_0, x_1, x_2), F^2(x_0, x_1, x_2)) : \R^3 \to \R^3
$$

Note how we are denoting each component of $F$ as $F^i$ with a [raised index](raised-index.md).

Then, the [divergence](divergence.md) can be written in [Einstein notation](einstein-notation.md) as:

$$
\div{F} = \pdv{F^0(x_0, x_1, x_2)}{x_0} + \pdv{F^1(x_0, x_1, x_2)}{x_1} + \pdv{F^2(x_0, x_1, x_2)}{x_2} = \partial_i F^i(x_0, x_1, x_2) = \pdv{F^i(x_0, x_1, x_2)}{x^i}
$$

It is common to just omit the variables of the function, so we tend to just say:

$$
\div{F} = \partial_i F^i
$$

or equivalently when referring just to the [operator](linear-operator.md):

$$
\div{} = \partial_i
$$

## ↑ Ancestors (8)

1. [Einstein notation for partial derivatives](einstein-notation-for-partial-derivatives.md)
2. [Einstein notation](einstein-notation.md)
3. [Tensor](tensor.md)
4. [Linear algebra](linear-algebra-split.md)
5. [Algebra](algebra-split.md)
6. [Area of mathematics](area-of-mathematics.md)
7. [Mathematics](mathematics-split.md)
8. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (1)

- [Einstein notation for partial derivatives](einstein-notation-for-partial-derivatives.md)
