# Flux qubit

↑ **Parent:** [Superconducting qubit type](superconducting-qubit-type.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Flux_qubit)

In [Ciro's ASCII art circuit diagram notation](ciro-s-ascii-art-circuit-diagram-notation.md), it is a loop with three [Josephson junctions](josephson-junction.md):
```
+----X-----+
|          |
|          |
|          |
+--X----X--+
```

![](https://upload.wikimedia.org/wikipedia/en/0/04/Flux_Qubit_-_Holloway.jpg)

<a id="video-superconducting-qubit-by-ntt-scl-2015"></a>
**[Video 13](#video-superconducting-qubit-by-ntt-scl-2015). Superconducting Qubit by NTT SCL (2015)** [Source](https://www.youtube.com/watch?v=daQJMwvxC_U). Offers an interesting interpretation of [superposition](quantum-superposition.md) in that type of device (TODO precise name, seems to be a [flux qubit](flux-qubit.md)): current going clockwise or current going counter clockwise at the same time. [https://youtu.be/xjlGL4Mvq7A?t=1348](https://youtu.be/xjlGL4Mvq7A?t=1348) clarifies that this is just one of the types of qubits, and that it was developed by [Hans Mooij](https://ourbigbook.com/go/topic/hans-mooij) et. al., with a proposal in 1999 and experiments in 2000. The other type is dual to this one, and the [superposition](quantum-superposition.md) of the other type is between N and N + 1 copper pairs stored in a box.

Their circuit is a loop with three [Josephson junctions](josephson-junction.md), in [Ciro's ASCII art circuit diagram notation](ciro-s-ascii-art-circuit-diagram-notation.md):
```
+----X-----+
|          |
|          |
|          |
+--X----X--+
```

They name the clockwise and counter clockwise states $\ket{L}$ and $\ket{R}$ (named for Left and Right).

When half the [magnetic flux quantum](magnetic-flux-quantum.md) is applied as [microwaves](microwave.md), this produces the ground state:

$$
\ket{0} = \ket{L} + \ket{R}
$$

where $L$ and $R$ cancel each other out. And the first excited state $\ket{1}$ is:

$$
\ket{0} = \ket{L} - \ket{R}
$$

Then he mentions that:
- to go from 0 to 1, they apply the difference in energy
- if the duration is reduced by half, it creates a superposition of $\ket{0} + \ket{1}$.

---

## ↑ Ancestors (12)

1. [Superconducting qubit type](superconducting-qubit-type.md)
2. [Superconducting qubit](superconducting-qubit.md)
3. [Superconducting quantum computing](superconducting-quantum-computing.md)
4. [Quantum computer physical implementation](quantum-computer-physical-implementation.md)
5. [Quantum computing hardware](quantum-computing-hardware.md)
6. [Quantum computing](quantum-computing-split.md)
7. [Quantum information](quantum-information.md)
8. [Information](information.md)
9. [Information technology](information-technology.md)
10. [Area of technology](area-of-technology.md)
11. [Technology](technology-split.md)
12. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (1)

- [Flux qubit](flux-qubit.md)
