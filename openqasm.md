# OpenQASM

↑ **Parent:** [Quantum software](quantum-software.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/OpenQASM)

On [Qiskit](qiskit.md) `qiskit==0.44.1`:
```
qc.qasm()
```

E.g. with our [qiskit/hello.py](_file/qiskit/hello.py.md), we obtain the [Bell state circuit](bell-circuit.md):
```
OPENQASM 2.0;
include "qelib1.inc";
qreg q[2];
creg c[2];
h q[0];
cx q[0],q[1];
measure q[0] -> c[0];
measure q[1] -> c[1];
```

## ↑ Ancestors (8)

1. [Quantum software](quantum-software.md)
2. [Quantum computing](quantum-computing-split.md)
3. [Quantum information](quantum-information.md)
4. [Information](information.md)
5. [Information technology](information-technology.md)
6. [Area of technology](area-of-technology.md)
7. [Technology](technology-split.md)
8. [Ciro Santilli's Homepage](split.md)
