# Quantum circuits vs classical circuits

↑ **Parent:** [Quantum circuit](quantum-circuit.md)

Just like a classic [programmer](software-engineer.md) does not need to understand the intricacies of how transistors are implemented and [CMOS](cmos.md) semiconductors, the quantum programmer does not understand physical intricacies of the underlying [physical implementation](quantum-computer-physical-implementation.md).

The main difference to keep in mind is that quantum computers cannot [save and observe intermediate quantum state](https://en.wikipedia.org/wiki/Observer_effect_(physics)), so programming a quantum computer is basically like programming a combinatorial-like circuit with gates that operate on (qu)bits:
- [https://quantumcomputing.stackexchange.com/questions/8441/does-a-quantum-computer-have-a-clock-signal-and-if-yes-how-big-is-it/9383#9383](https://quantumcomputing.stackexchange.com/questions/8441/does-a-quantum-computer-have-a-clock-signal-and-if-yes-how-big-is-it/9383#9383)
- [https://quantumcomputing.stackexchange.com/questions/8849/quantum-circuits-explain-algorithms-why-didnt-classical-circuits/8869#8869](https://quantumcomputing.stackexchange.com/questions/8849/quantum-circuits-explain-algorithms-why-didnt-classical-circuits/8869#8869)

For this reason programming a quantum computer is much like programming a classical combinatorial circuit as you would do with [SPICE](https://en.wikipedia.org/wiki/SPICE), [verilog-or-vhdl](register-transfer-level.md), in which you are basically describing a graph of gates that goes from the input to the output

For this reason, we can use the words "program" and "circuit" interchangeably to refer to a quantum program

Also remember that and there is no no clocks in combinatorial circuits because there are no registers to drive; and so there is no analogue of clock in the quantum system either,

Another consequence of this is that programming quantum computers does not look like programming the more "common" procedural programming languages such as C or Python, since those fundamentally rely on processor register / memory state all the time.

Quantum programmers can however use classic languages to help describe their quantum programs more easily, for example this is what happens in [Qiskit](qiskit.md), where you write a Python program that makes Qiskit library calls that describe the quantum program.

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

## ← Incoming links (2)

- [Introduction to quantum computing](introduction-to-quantum-computing.md)
- [Programmer's model of quantum computers](programmer-s-model-of-quantum-computers.md)
