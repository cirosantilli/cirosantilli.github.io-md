# Dual vector

↑ **Parent:** [Dual space](dual-space.md)

Dual vectors are the members of a [dual space](dual-space.md).

In the context of [tensors](tensor.md) , we use raised indices to refer to members of the dual basis vs the underlying basis:

$$
\begin{aligned}
e_1 & \in V \\
e_2 & \in V \\
e_3 & \in V \\
e^1 & \in V^* \\
e^2 & \in V^* \\
e^3 & \in V^* \\
\end{aligned}
$$

The dual basis vectors $e^i$ are defined to "pick the corresponding coordinate" out of elements of V. E.g.:

$$
\begin{aligned}
e^1 (4, -3, 6) & =  4 \\
e^2 (4, -3, 6) & = -3 \\
e^3 (4, -3, 6) & =  6 \\
\end{aligned}
$$

By expanding into the basis, we can put this more succinctly with the [Kronecker delta](kronecker-delta.md) as:

$$
e^i(e_j) = \delta_{ij}
$$

Note that in [Einstein notation](einstein-notation.md), the components of a dual vector have lower indices. This works well with the upper case indices of the dual vectors, allowing us to write a dual vector $f$ as:

$$
f = f_i e^i
$$

In the context of [quantum mechanics](quantum-mechanics-split.md), the [bra](bra-ket-notation.md) notation is also used for dual vectors.

## ↑ Ancestors (8)

1. [Dual space](dual-space.md)
2. [Linear form](linear-form.md)
3. [Linear map](linear-map.md)
4. [Linear algebra](linear-algebra-split.md)
5. [Algebra](algebra-split.md)
6. [Area of mathematics](area-of-mathematics.md)
7. [Mathematics](mathematics-split.md)
8. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (3)

- [A linear map is a (1,1) tensor](a-linear-map-is-a-1-1-tensor.md)
- [Bra-ket notation](bra-ket-notation.md)
- [Tensor](tensor.md)
