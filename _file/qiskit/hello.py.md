<h1 id="_file/qiskit/hello.py">qiskit/hello.py</h1>

↑ **Parent:** [Qiskit hello world](../../qiskit-hello-world.md)

Our example uses a [Bell state circuit](../../bell-circuit.md) to illustrate all the fundamental [Qiskit](../../qiskit.md) basics.

Sample program output, `counts` are randomized each time.

First we take the [quantum state vector](../../quantum-state-vector.md) immediately after the $\ket{00}$ input.
```
input:
state:
Statevector([1.+0.j, 0.+0.j, 0.+0.j, 0.+0.j],
            dims=(2, 2))
probs:
[1. 0. 0. 0.]
```
We understand that the first element of `Statevector` is $\ket{00}$, and has probability of 1.0.

Next we take the state after a [Hadamard gate](../../hadamard-gate.md) on the first [qubit](../../qubit.md):
```
h:
state:
Statevector([0.70710678+0.j, 0.70710678+0.j, 0.        +0.j,
             0.        +0.j],
            dims=(2, 2))
probs:
[0.5 0.5 0.  0. ]
```
We now understand that the second element of the `Statevector` is $\ket{01}$, and now we have a 50/50 propabability split for the first bit.

Then we apply the [CNOT gate](../../cnot-gate.md):
```
cx:
state:
Statevector([0.70710678+0.j, 0.        +0.j, 0.        +0.j,
             0.70710678+0.j],
            dims=(2, 2))
probs:
[0.5 0.  0.  0.5]
```
which leaves us with the final $\frac{\ket{00} + \ket{11}}{\sqrt{2}}$.

Then we print the circuit a bit:
```
qc without measure:
     ┌───┐
q_0: ┤ H ├──■──
     └───┘┌─┴─┐
q_1: ─────┤ X ├
          └───┘
c: 2/══════════

qc with measure:
     ┌───┐     ┌─┐
q_0: ┤ H ├──■──┤M├───
     └───┘┌─┴─┐└╥┘┌─┐
q_1: ─────┤ X ├─╫─┤M├
          └───┘ ║ └╥┘
c: 2/═══════════╩══╩═
                0  1
qasm:
OPENQASM 2.0;
include "qelib1.inc";
qreg q[2];
creg c[2];
h q[0];
cx q[0],q[1];
measure q[0] -> c[0];
measure q[1] -> c[1];
```

And finally we [compile](../../quantum-compilation.md) the circuit and do some sample measurements:
```
qct:
     ┌───┐     ┌─┐
q_0: ┤ H ├──■──┤M├───
     └───┘┌─┴─┐└╥┘┌─┐
q_1: ─────┤ X ├─╫─┤M├
          └───┘ ║ └╥┘
c: 2/═══════════╩══╩═
                0  1
counts={'11': 484, '00': 516}
counts={'11': 493, '00': 507}
```

## ↑ Ancestors (12)

1. [Qiskit hello world](../../qiskit-hello-world.md)
2. [Qiskit example](../../qiskit-example.md)
3. [Qiskit](../../qiskit.md)
4. [Quantum programming framework](../../quantum-programming-framework.md)
5. [Quantum software](../../quantum-software.md)
6. [Quantum computing](../../quantum-computing-split.md)
7. [Quantum information](../../quantum-information.md)
8. [Information](../../information.md)
9. [Information technology](../../information-technology.md)
10. [Area of technology](../../area-of-technology.md)
11. [Technology](../../technology-split.md)
12. [Ciro Santilli's Homepage](../../split.md)

## ← Incoming links (5)

- [Bell circuit](../../bell-circuit.md)
- [Introduction to quantum computing](../../introduction-to-quantum-computing.md)
- [OpenQASM](../../openqasm.md)
- [Qiskit hello world](../../qiskit-hello-world.md)
- [qiskit/initialize.py](../../qiskit-initialize-py.md)
