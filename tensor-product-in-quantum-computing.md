# Tensor product in quantum computing

↑ **Parent:** [Quantum circuit](quantum-circuit.md)  
🏷️ **Tags:** [Tensor product](tensor-product.md)

We don't need to understand a super generalized version of [tensor products](tensor-product.md) to know what they mean in basic [quantum computing](quantum-computing-split.md)!

Intuitively, taking a [tensor product](tensor-product.md) of two [qubits](qubit.md) simply means putting them together on the same quantum system/computer.

When we write the [bra-ket notation](bra-ket-notation.md): $\ket{00}$ that is the same as $\ket{0} \otimes \ket{0}$.

The tensor product is called a "product" because it distributes over addition.

E.g. consider:

$$
(\frac{\ket{0} + \ket{1}}{\sqrt{2}}) \otimes \ket{0} =
\frac{\ket{0} \otimes \ket{0} + \ket{1} \otimes \ket{0}}{\sqrt{2}} =
\frac{\ket{00} + \ket{10}}{\sqrt{2}}
$$

Intuitively, in this operation we just put a [Hadamard gate](hadamard-gate.md) qubit together with a second pure $\ket{0}$ qubit.

And the outcome still has the second qubit as always 0, because we haven't made them interact.

The [quantum state](quantum-state.md) $\frac{\ket{00} + \ket{10}}{\sqrt{2}}$ is called a [separable state](separable-state.md), because it can be written as a single product of two different qubits. We have simply brought two qubits together, without making them interact.

If we then add a [CNOT gate](cnot-gate.md) to make a [Bell state](bell-state.md):

$$
\frac{\ket{00} + \ket{11}}{\sqrt{2}} =
\frac{\ket{0} \otimes \ket{0} + \ket{1} \otimes \ket{1}}{\sqrt{2}}
$$

we can now see that the [Bell state](bell-state.md) is [non-separable](separable-state.md): we've made the two qubits interact, and there is no way to write this state with a single [tensor product](tensor-product.md). The qubits are fundamentally [entangled](quantum-entanglement.md).

## ↑ Ancestors (13)

1. [Quantum circuit](quantum-circuit.md)
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

## ← Incoming links (1)

- [Introduction to quantum computing](introduction-to-quantum-computing.md)
