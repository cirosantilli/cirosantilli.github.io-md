# CNOT gate

↑ **Parent:** [Controlled quantum gate](controlled-quantum-gate.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Controlled_NOT_gate)

The [CNOT gate](cnot-gate.md) is a [controlled quantum gate](controlled-quantum-gate.md) that operates on two [qubits](qubit.md), flipping the second (operand) [qubit](qubit.md) if the first (control) [qubit](qubit.md) is set.

This gate is the first example of a [controlled quantum gate](controlled-quantum-gate.md) that you should study.

<a id="equation-cnot-gate-matrix"></a>
$$
\begin{bmatrix}
1 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 \\
0 & 0 & 0 & 1 \\
0 & 0 & 1 & 0
\end{bmatrix}
$$

<a id="image-cnot-gate-symbol"></a>
![](https://upload.wikimedia.org/wikipedia/commons/4/4e/CNOT_gate.svg)

**[Figure 4](#image-cnot-gate-symbol). CNOT gate symbol**. [Source](https://commons.wikimedia.org/wiki/File:CNOT_gate.svg). The symbol follow the generic symbol convention for [controlled quantum gates](controlled-quantum-gate.md) shown at [Figure 3. "Generic controlled quantum gate symbol"](controlled-quantum-gate.md#image-generic-controlled-quantum-gate-symbol), but replacing the generic "U" with the [Figure 2. "Quantum NOT gate symbol"](pauli-x-gate.md#image-quantum-not-gate-symbol).

To understand why the gate is called a CNOT gate, you should think as follows.

First let's produce a generic [quantum state](quantum-state.md) vector where the control qubit is certain to be 0.

On the standard basis:

$$
\ket{00} \\
\ket{01} \\
\ket{10} \\
\ket{11} \\
$$

we see that this means that only $\ket{00}$ and $\ket{01}$ should be possible. Therefore, the state must be of the form:

$$
\begin{bmatrix}
x \\
y \\
0 \\
0
\end{bmatrix}
$$

where $x$ and $y$ are two [complex numbers](complex-number.md) such that $|x| + |y| = 1.0$

If we operate the [CNOT gate](cnot-gate.md) on that state, we obtain:

$$
\begin{bmatrix}
1 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 \\
0 & 0 & 0 & 1 \\
0 & 0 & 1 & 0
\end{bmatrix}

\times

\begin{bmatrix}
x \\
y \\
0 \\
0
\end{bmatrix}

=

\begin{bmatrix}
x \\
y \\
0 \\
0
\end{bmatrix}
$$

and so the input is unchanged as desired, because the control qubit is 0.

If however we take only states where the control qubit is for sure 1:

$$
\begin{bmatrix}
1 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 \\
0 & 0 & 0 & 1 \\
0 & 0 & 1 & 0
\end{bmatrix}

\times

\begin{bmatrix}
0 \\
0 \\
x \\
y
\end{bmatrix}

=

\begin{bmatrix}
0 \\
0 \\
y \\
x
\end{bmatrix}
$$

Therefore, in that case, what happened is that the probabilities of $\ket{10}$ and $\ket{11}$ were swapped from $x$ and $y$ to $y$ and $x$ respectively, which is exactly what the [quantum NOT gate](pauli-x-gate.md) does.

So from this we understand more concretely what "the gate only operates if the first [qubit](qubit.md) is set to one" means.

Now go and study the [Bell state](bell-state.md) and understand intuitively how this gate is used to produce it.

## ↑ Ancestors (16)

1. [Controlled quantum gate](controlled-quantum-gate.md)
2. [Multi-qubit gate](multi-qubit-gate.md)
3. [Single-qubit gate](single-qubit-gate.md)
4. [Quantum logic gate](quantum-logic-gate.md)
5. [Digital quantum computer](digital-quantum-computer.md)
6. [Analog and digital quantum computers](analog-and-digital-quantum-computers.md)
7. [Model of quantum computing](model-of-quantum-computing.md)
8. [Quantum computer type](quantum-computer-type.md)
9. [Quantum computing hardware](quantum-computing-hardware.md)
10. [Quantum computing](quantum-computing-split.md)
11. [Quantum information](quantum-information.md)
12. [Information](information.md)
13. [Information technology](information-technology.md)
14. [Area of technology](area-of-technology.md)
15. [Technology](technology-split.md)
16. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (9)

- [qiskit/hello.py](_file/qiskit/hello.py.md)
- [Bell circuit](bell-circuit.md)
- [CNOT gate](cnot-gate.md)
- [Controlled quantum gate](controlled-quantum-gate.md)
- [Introduction to quantum computing](introduction-to-quantum-computing.md)
- [Photonic quantum computer](photonic-quantum-computer.md)
- [qiskit/initialize.py](qiskit-initialize-py.md)
- [Quantum logic gates are needed for physical implementation](quantum-logic-gates-are-needed-for-physical-implementation.md)
- [Tensor product in quantum computing](tensor-product-in-quantum-computing.md)
