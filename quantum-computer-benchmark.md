# Quantum computer benchmark

↑ **Parent:** [Quantum computing](quantum-computing-split.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Quantum_computer_benchmark)

One important area of research and development of [quantum computing](quantum-computing-split.md) is the development of benchmarks that allow us to compare different quantum computers to decide which one is more powerful than the other.

Ideally, we would like to be able to have a single number that predicts which computer is more powerful than the other for a wide range of algorithms.

However, much like in [CPU](central-processing-unit.md) benchmarking, this is a very complex problem, since different algorithms might perform differently in different architectures, making it very hard to sum up the architecture's capabilities to a single number as we would like.

The only thing that is directly comparable across computers is how two machines perform for a single algorithm, but we want a single number that is representative of many algorithms.

For example, the number of qubits would be a simple naive choice of such performance predictor number. But it is very imprecise, since other factors are also very important:
- qubit error rate
- [coherence time](coherence-time.md), which determines the maximum circuit depth
- qubit connectivity. Can you only connect to 4 neighbouring qubits in a 2D plane? Or to every other qubit equally as well?

[Quantum volume](quantum-volume.md) is another less naive attempt at such metric.

**Table of contents**

- [Comparison of quantum computing hardware](comparison-of-quantum-computing-hardware.md)
- [Algorithmic qubits](algorithmic-qubits.md)
- [Coherence time](coherence-time.md)
- [Depth of a quantum circuit](depth-of-a-quantum-circuit.md)
- [Quantum volume](quantum-volume.md)
- [Random circuit sampling](random-circuit-sampling.md)

## ↑ Ancestors (7)

1. [Quantum computing](quantum-computing-split.md)
2. [Quantum information](quantum-information.md)
3. [Information](information.md)
4. [Information technology](information-technology.md)
5. [Area of technology](area-of-technology.md)
6. [Technology](technology-split.md)
7. [Ciro Santilli's Homepage](split.md)
