<h1 id="_file/qiskit/qft.py">qiskit/qft.py</h1>

↑ **Parent:** [Qiskit example](../../qiskit-example.md)  
🏷️ **Tags:** [Quantum Fourier transform](../../quantum-fourier-transform.md)

This is an example of the `qiskit.circuit.library.QFT` implementation of the [Quantum Fourier transform](../../quantum-fourier-transform.md) function which is documented at: [https://docs.quantum.ibm.com/api/qiskit/0.44/qiskit.circuit.library.QFT](https://docs.quantum.ibm.com/api/qiskit/0.44/qiskit.circuit.library.QFT)

Output:
```
init: [1, 0, 0, 0, 0, 0, 0, 0]
qc
     ┌──────────────────────────────┐┌──────┐
q_0: ┤0                             ├┤0     ├
     │                              ││      │
q_1: ┤1 Initialize(1,0,0,0,0,0,0,0) ├┤1 QFT ├
     │                              ││      │
q_2: ┤2                             ├┤2     ├
     └──────────────────────────────┘└──────┘
transpiled qc
     ┌──────────────────────────────┐                                     ┌───┐   
q_0: ┤0                             ├────────────────────■────────■───────┤ H ├─X─
     │                              │              ┌───┐ │        │P(π/2) └───┘ │ 
q_1: ┤1 Initialize(1,0,0,0,0,0,0,0) ├──────■───────┤ H ├─┼────────■─────────────┼─
     │                              │┌───┐ │P(π/2) └───┘ │P(π/4)                │ 
q_2: ┤2                             ├┤ H ├─■─────────────■──────────────────────X─
     └──────────────────────────────┘└───┘
Statevector([0.35355339+0.j, 0.35355339+0.j, 0.35355339+0.j,
             0.35355339+0.j, 0.35355339+0.j, 0.35355339+0.j,
             0.35355339+0.j, 0.35355339+0.j],
            dims=(2, 2, 2))

init: [0.0, 0.35355339059327373, 0.5, 0.3535533905932738, 6.123233995736766e-17, -0.35355339059327373, -0.5, -0.35355339059327384]
Statevector([ 7.71600526e-17+5.22650714e-17j,
              1.86749130e-16+7.07106781e-01j,
             -6.10667421e-18+6.10667421e-18j,
              1.13711443e-16-1.11022302e-16j,
              2.16489014e-17-8.96726857e-18j,
             -5.68557215e-17-1.11022302e-16j,
             -6.10667421e-18-4.94044770e-17j,
             -3.30200457e-16-7.07106781e-01j],
            dims=(2, 2, 2))
```
So this also serves as a more interesting example of [quantum compilation](../../quantum-compilation.md), mapping the `QFT` gate to [Qiskit Aer](../../qiskit-aer.md) primitives.

If we don't `transpile` in this example, then running blows up with:
```
qiskit_aer.aererror.AerError: 'unknown instruction: QFT'
```

The second input is:

$$
x_i = \frac{1}{2} sin(2 * \pi * i / 8)
$$

and the output of that approximately:
```
[0, 1j/sqrt(2), 0, 0, 0, 0, 0, 1j/sqrt(2)]
```
which can be defined simply as the [normalized DFT](../../normalized-dft.md) of the input [quantum state vector](../../quantum-state-vector.md).

From this we see that the [Quantum Fourier transform](../../quantum-fourier-transform.md) is equivalent to a direct [discrete Fourier transform](../../discrete-fourier-transform.md) on the [quantum state vector](../../quantum-state-vector.md), related: [https://physics.stackexchange.com/questions/110073/how-to-derive-quantum-fourier-transform-from-discrete-fourier-transform-dft](https://physics.stackexchange.com/questions/110073/how-to-derive-quantum-fourier-transform-from-discrete-fourier-transform-dft)

## ↑ Ancestors (11)

1. [Qiskit example](../../qiskit-example.md)
2. [Qiskit](../../qiskit.md)
3. [Quantum programming framework](../../quantum-programming-framework.md)
4. [Quantum software](../../quantum-software.md)
5. [Quantum computing](../../quantum-computing-split.md)
6. [Quantum information](../../quantum-information.md)
7. [Information](../../information.md)
8. [Information technology](../../information-technology.md)
9. [Area of technology](../../area-of-technology.md)
10. [Technology](../../technology-split.md)
11. [Ciro Santilli's Homepage](../../split.md)

## ← Incoming links (2)

- [`qiskit.transpile()`](../../qiskit-transpile.md)
- [Quantum Fourier transform](../../quantum-fourier-transform.md)
