<h1 id="quantum-logic-gates-are-needed-because-you-can-t-compute-the-matrix-explicitly-as-it-grows-exponentially">Quantum logic gates are needed because you can't compute the matrix explicitly as it grows exponentially</h1>

↑ **Parent:** [Quantum logic gate](quantum-logic-gate.md)

One key insight, is that the matrix of a non-trivial quantum circuit is going to be huge, and won't fit into any amount classical memory that can be present in this universe.

This is because the matrix is exponential in the number qubits, and $2^{100}$ is more than the number of atoms in the universe!

Therefore, off the bat we know that we cannot possibly describe those matrices in an explicit form, but rather must use some kind of shorthand.

But it gets worse.

Even if we had enough memory, the act of explicitly computing the matrix is not generally possible.

This is because knowing the matrix, basically means knowing the probability result for all possible $2^{N}$ outputs for each of the $2^{N}$ possible inputs.

But if we had those probabilities, our algorithmic problem would already be solved in the first place! We would "just" go over each of those output probabilities (OK, there are $2^{N}$ of those, which is also an insurmountable problem in itself), and the largest probability would be the answer.

So if we could calculate those probabilities on a classical machine, we would also be able to simulate the quantum computer on the classical machine, and quantum computing would not be able to give exponential speedups, which we know it does.

To see this, consider that for a given input, say `000` on a 3 qubit machine, the corresponding 8-sized quantum state looks like:
```
000 -> 1000 0000 == (1.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0)
```
and therefore when you multiply it by the unitary matrix of the quantum circuit, what you get is the first column of the unitary matrix of the quantum circuit. And `001`, gives the second column and so on.

As a result, to prove that a quantum algorithm is correct, we need to be a bit smarter than "just calculate the full matrix".

Which is why you should now go and read: [Section "Quantum algorithm"](quantum-algorithm.md).

This type of thinking links back to how physical experiments relate to quantum computing: a quantum computer realizes a physical experiment to which we cannot calculate the probabilities of outcomes without exponential time.

So for example in the case of a [photonic quantum computer](photonic-quantum-computer.md), you are not able to calculate from theory the probability that photons will show up on certain wires or not.

## ↑ Ancestors (13)

1. [Quantum logic gate](quantum-logic-gate.md)
2. [Digital quantum computer](digital-quantum-computer.md)
3. [Analog and digital quantum computers](analog-and-digital-quantum-computers.md)
4. [Model of quantum computing](model-of-quantum-computing.md)
5. [Quantum computer type](quantum-computer-type.md)
6. [Quantum computing hardware](quantum-computing-hardware.md)
7. [Quantum computing](quantum-computing-split.md)
8. [Quantum information](quantum-information.md)
9. [Information](information.md)
10. [Information technology](information-technology.md)
11. [Area of technology](area-of-technology.md)
12. [Technology](technology-split.md)
13. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (3)

- [Introduction to quantum computing](introduction-to-quantum-computing.md)
- [Quantum computers as experiments that are hard to predict outcomes](quantum-computers-as-experiments-that-are-hard-to-predict-outcomes.md)
- [Quantum logic gate](quantum-logic-gate.md)
