# Quantum logic gates are needed for physical implementation

↑ **Parent:** [Quantum logic gate](quantum-logic-gate.md)

One direct practical reason is that we need to map the matrix to real quantum hardware somehow, and all quantum hardware designs so far and likely in the future are gate-based: you manipulate a small number of qubits at a time (2) and add more and more of such operations.

While there are "[quantum compilers](quantum-compilation.md)" to increase the portability of quantum programs, it is to be expected that programs manually crafted for a specific hardware will be more efficient just like in classic computers.

TODO: is there any clear reason why computers can't beat humans in approximating any unitary matrix with a gate set?

This is analogous to what classic circuit programmers will do, by using smaller [logic gates](logic-gate.md) to create complex circuits, rather than directly creating one huge [truth table](truth-table.md).

The most commonly considered quantum gates take 1, 2, or 3 qubits as input.

The gates themselves are just unitary matrices that operate on the input qubits and produce the same number of output qubits.

For example, the matrix for the [CNOT gate](cnot-gate.md), which takes 2 qubits as input is:
```
1 0 0 0
0 1 0 0
0 0 0 1
0 0 1 0
```

The final question is then: if I have a 2 qubit gate but an input with more qubits, say 3 qubits, then what does the 2 qubit gate (4x4 matrix) do for the final big 3 qubit matrix (8x8)? In order words, how do we scale quantum gates up to match the total number of qubits?

The intuitive answer is simple: we "just" extend the small matrix with a larger identity matrix so that the sum of the probabilities third bit is unaffected.

More precisely, we likely have to extend the matrix in a way such that the [partial measurement](https://cs.stackexchange.com/questions/71462/how-are-partial-measurements-performed-on-a-n-qubit-quantum-circuit) of the original small gate qubits leaves all other qubits unaffected.

For example, if the circuit were made up of a CNOT gate operating on the first and second qubits as in:
```
0 ----+----- 0
      |
1 ---CNOT--- 1

2 ---------- 2
```

then we would just extend the 2x2 CNOT gate to:

TODO lazy to properly learn right now. Apparently you have to use the [Kronecker product](https://en.wikipedia.org/wiki/Kronecker_product) by the identity matrix. Also, [zX-calculus](zx-calculus.md) appears to provide a powerful alternative method in some/all cases.

Bibliography:
- [https://quantumcomputing.stackexchange.com/questions/2299/how-to-interpret-a-quantum-circuit-as-a-matrix](https://quantumcomputing.stackexchange.com/questions/2299/how-to-interpret-a-quantum-circuit-as-a-matrix)

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
- [Programmer's model of quantum computers](programmer-s-model-of-quantum-computers.md)
- [Quantum logic gate](quantum-logic-gate.md)
