# Bell circuit

↑ **Parent:** [Bell state](bell-state.md)  
🏷️ **Tags:** [Quantum circuit](quantum-circuit.md)

A [quantum circuit](quantum-circuit.md) which when fed with input $\ket{00}$ produces the [Bell state](bell-state.md).

In [Qiskit](qiskit.md) at: [qiskit/hello.py](_file/qiskit/hello.py.md).

<a id="image-quantum-circuit-that-generates-the-bell-state"></a>
![](https://upload.wikimedia.org/wikipedia/commons/f/fc/The_Hadamard-CNOT_transform_on_the_zero-state.png)

**[Figure 11](#image-quantum-circuit-that-generates-the-bell-state). Quantum circuit that generates the Bell state**. [Source](https://commons.wikimedia.org/wiki/File:The_Hadamard-CNOT_transform_on_the_zero-state.png). The fundamental intuition for this circuit is as follows.

First the [Hadamard gate](hadamard-gate.md) makes the first [qubit](qubit.md) be in a 50/50 state.

Then, the [CNOT gate](cnot-gate.md) gets controlled by that 50/50 value, and the controlled qubit also gets 50/50 chance as a result.

However, both qubits are now [entangled](quantum-entanglement.md): the result of the second qubit depends on the result of the first one. Because:
- if the first qubit is 0, cnot is not active, and so the second qubit remains 0 as its input
- if the first qubit is 1, cnot is active, and so the second qubit is flipped to 1

---

## ↑ Ancestors (9)

1. [Bell state](bell-state.md)
2. [Quantum state](quantum-state.md)
3. [Quantum computing](quantum-computing-split.md)
4. [Quantum information](quantum-information.md)
5. [Information](information.md)
6. [Information technology](information-technology.md)
7. [Area of technology](area-of-technology.md)
8. [Technology](technology-split.md)
9. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (1)

- [Introduction to quantum computing](introduction-to-quantum-computing.md)
