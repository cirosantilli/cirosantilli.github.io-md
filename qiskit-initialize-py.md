<h1 id="qiskit-initialize-py">qiskit/initialize.py</h1>

↑ **Parent:** [Qiskit example](qiskit-example.md)

In this example we will initialize a quantum circuit with a single [CNOT gate](cnot-gate.md) and see the output values.

By default, [Qiskit](qiskit.md) initializes every [qubit](qubit.md) to 0 as shown in the [qiskit/hello.py](_file/qiskit/hello.py.md). But we can also initialize to arbitrary values as would be done when computing the output for various different inputs.

Output:
```
     ┌──────────────────────┐
q_0: ┤0                     ├──■──
     │  Initialize(1,0,0,0) │┌─┴─┐
q_1: ┤1                     ├┤ X ├
     └──────────────────────┘└───┘
c: 2/═════════════════════════════

init: [1, 0, 0, 0]
probs: [1. 0. 0. 0.]

init: [0, 1, 0, 0]
probs: [0. 0. 0. 1.]

init: [0, 0, 1, 0]
probs: [0. 0. 1. 0.]

init: [0, 0, 0, 1]
probs: [0. 1. 0. 0.]

     ┌──────────────────────────────────┐
q_0: ┤0                                 ├──■──
     │  Initialize(0.70711,0,0,0.70711) │┌─┴─┐
q_1: ┤1                                 ├┤ X ├
     └──────────────────────────────────┘└───┘
c: 2/═════════════════════════════════════════

init: [0.7071067811865475, 0, 0, 0.7071067811865475]
probs: [0.5 0.5 0.  0. ]
```
which we should all be able to understand intuitively given our understanding of the [CNOT gate](cnot-gate.md) and [quantum state vectors](quantum-state-vector.md).

[https://quantumcomputing.stackexchange.com/questions/13202/qiskit-initializing-n-qubits-with-binary-values-0s-and-1s](https://quantumcomputing.stackexchange.com/questions/13202/qiskit-initializing-n-qubits-with-binary-values-0s-and-1s) describes how to initialize circuits qubits only with binary 0 or 1 to avoid dealing with the exponential number of elements of the [quantum state vector](quantum-state-vector.md).

## ↑ Ancestors (11)

1. [Qiskit example](qiskit-example.md)
2. [Qiskit](qiskit.md)
3. [Quantum programming framework](quantum-programming-framework.md)
4. [Quantum software](quantum-software.md)
5. [Quantum computing](quantum-computing-split.md)
6. [Quantum information](quantum-information.md)
7. [Information](information.md)
8. [Information technology](information-technology.md)
9. [Area of technology](area-of-technology.md)
10. [Technology](technology-split.md)
11. [Ciro Santilli's Homepage](split.md)
