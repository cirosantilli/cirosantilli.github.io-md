# Quantum computing

↑ **Parent:** [Quantum information](technology.md#quantum-information)  
🏷️ **Tags:** [Computer physical principle of operation](computer.md#computer-physical-principle-of-operation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Quantum_computing)

Quantum is getting hot in 2019, and even [Ciro Santilli](ciro-santilli.md) got a bit excited: [quantum computing could be the next big thing](ciro-santilli.md#quantum-computing-could-be-the-next-big-thing).

No useful algorithm has been economically accelerated by quantum yet as of 2019, only [useless ones](#quantum-supremacy), but [the bets are on, big time](#quantum-computing-player).

To get a feeling of this, just have a look at the insane number of startups that are already developing [quantum algorithms](#quantum-algorithm) for hardware that doesn't/barely exists! [https://quantumcomputingreport.com/players/privatestartup](https://quantumcomputingreport.com/players/privatestartup) ([archive](https://web.archive.org/web/20191223175204/https://quantumcomputingreport.com/players/privatestartup/)). Some feared we might be in a bubble: [Are we in a quantum computing bubble?](#are-we-in-a-quantum-computing-bubble)

To get a basic idea of what programming a quantum computer looks like start by reading: [Section "Quantum computing is just matrix multiplication"](#programmer-s-model-of-quantum-computers).

Some people [have their doubts](#quantum-computing-skepticism), and that is not unreasonable, it might truly not work out. We could be on the verge of an [AI winter](artificial-intelligence.md#ai-winter) of quantum computing. But [Ciro Santilli](ciro-santilli.md) feels that it is genuinely impossible to tell as of 2020 if something will work out or not. We really just have to try it out and see. There must have been skeptics before every single [next big thing](ciro-santilli.md#the-next-big-thing).

**Table of contents**

- [Introduction to quantum computing](#introduction-to-quantum-computing)
- [Programmer's model of quantum computers](#programmer-s-model-of-quantum-computers)
- [Timeline of quantum computing](#timeline-of-quantum-computing)
- [Quantum algorithm](#quantum-algorithm)
  - [Quantum computers are not expected to solve NP-complete problems](#quantum-computers-are-not-expected-to-solve-np-complete-problems)
  - [Quantum Algorithm Zoo](#quantum-algorithm-zoo)
  - [Quantum algorithm vs quantum gate vs quantum circuit](#quantum-algorithm-vs-quantum-gate-vs-quantum-circuit)
  - [Quantum algorithm by problem](#quantum-algorithm-by-problem)
    - [Quantum matrix multiplication](#quantum-matrix-multiplication)
    - [Quantum algorithm for linear systems of equations](#quantum-algorithm-for-linear-systems-of-equations)
      - [HHL algorithm](#hhl-algorithm)
  - [List of quantum algorithms](#list-of-quantum-algorithms)
    - [Bernstein-Vazirani algorithm](#bernstein-vazirani-algorithm)
    - [Grover's algorithm](#grover-s-algorithm)
    - [Hidden shift algorithm](#hidden-shift-algorithm)
      - [Hidden shift problem](#hidden-shift-problem)
    - [Quantum Fourier transform](#quantum-fourier-transform)
    - [Shor's algorithm](#shor-s-algorithm)
      - [How many logical qubits are needed to run Shor's algorithm?](#how-many-logical-qubits-are-needed-to-run-shor-s-algorithm)
      - [Integer factorization algorithms better than Shor's algorithm](#integer-factorization-algorithms-better-than-shor-s-algorithm)
- [Quantum compilation](#quantum-compilation)
  - [Quantum compiler benchmark](#quantum-compiler-benchmark)
  - [Quantum Intermediate Representation](#quantum-intermediate-representation)
  - [Quantum error correction](#quantum-error-correction)
    - [Quantum error correction code](#quantum-error-correction-code)
      - [Surface code](#surface-code)
    - [Quantum threshold theorem](#quantum-threshold-theorem)
      - [Noisy intermediate-scale quantum era](#noisy-intermediate-scale-quantum-era)
        - [NISQ algorithm](#nisq-algorithm)
          - [Variational quantum eigensolver](#variational-quantum-eigensolver)
          - [Quantum optimization algorithm](#quantum-optimization-algorithm)
            - [Quantum approximate optimization algorithm](#quantum-approximate-optimization-algorithm)
            - [Quadratic unconstrained binary optimization](#quadratic-unconstrained-binary-optimization)
  - [High level quantum synthesis](#high-level-quantum-synthesis)
    - [Classiq](#classiq)
- [Quantum computing player](#quantum-computing-player)
  - [Quantum computing player in Brazil](#quantum-computing-player-in-brazil)
  - [Quantum computing company](#quantum-computing-company)
  - [Quantum computing research institute](#quantum-computing-research-institute)
    - [QuTech](#qutech)
      - [QuTech Academy](#qutech-academy)
  - [Organization developing quantum hardware](#organization-developing-quantum-hardware)
    - [D-Wave Systems](#d-wave-systems)
    - [ColdQuanta](#coldquanta)
  - [Organization developing quantum software](#organization-developing-quantum-software)
    - [Haiqu](#haiqu)
    - [Quantum Computing Inc.](#quantum-computing-inc)
    - [Microsoft Quantum](#microsoft-quantum)
    - [Phasecraft](#phasecraft)
- [Quantum computing paradigm](#quantum-computing-paradigm)
- [Quantum computing hardware](#quantum-computing-hardware)
  - [Step of operation of a quantum computer](#step-of-operation-of-a-quantum-computer)
    - [State initialization (quantum computing)](#state-initialization-quantum-computing)
    - [Readout (quantum computing)](#readout-quantum-computing)
  - [Quantum computers as experiments that are hard to predict outcomes](#quantum-computers-as-experiments-that-are-hard-to-predict-outcomes)
  - [Quantum computing is hard because we want long coherence but fast control](#quantum-computing-is-hard-because-we-want-long-coherence-but-fast-control)
  - [Quantum computer type](#quantum-computer-type)
    - [Model of quantum computing](#model-of-quantum-computing)
      - [Measurement and circuit based quantum computers](#measurement-and-circuit-based-quantum-computers)
        - [Circuit-based quantum computer](#circuit-based-quantum-computer)
        - [Measurement-based quantum computer](#measurement-based-quantum-computer)
      - [Analog and digital quantum computers](#analog-and-digital-quantum-computers)
        - [Digital quantum computer](#digital-quantum-computer)
          - [Quantum circuit](#quantum-circuit)
            - [Quantum state vector](#quantum-state-vector)
            - [Tensor product in quantum computing](#tensor-product-in-quantum-computing)
            - [Quantum circuits vs classical circuits](#quantum-circuits-vs-classical-circuits)
          - [Quantum logic gate](#quantum-logic-gate)
            - [Quantum logic gates are needed because you can't compute the matrix explicitly as it grows exponentially](#quantum-logic-gates-are-needed-because-you-can-t-compute-the-matrix-explicitly-as-it-grows-exponentially)
            - [Quantum logic gates are needed for physical implementation](#quantum-logic-gates-are-needed-for-physical-implementation)
            - [Universal quantum gates](#universal-quantum-gates)
            - [Single-qubit gate](#single-qubit-gate)
              - [Hadamard gate](#hadamard-gate)
              - [Pauli gate](#pauli-gate)
                - [Pauli-X gate](#pauli-x-gate)
                - [Pauli-Y gate](#pauli-y-gate)
                - [Pauli-Z gate](#pauli-z-gate)
              - [Phase shift gate](#phase-shift-gate)
              - [Multi-qubit gate](#multi-qubit-gate)
                - [Controlled quantum gate](#controlled-quantum-gate)
                  - [Empty circle control qubit notation](#empty-circle-control-qubit-notation)
                  - [CNOT gate](#cnot-gate)
                  - [CZ gate](#cz-gate)
                - [Toffoli gate](#toffoli-gate)
            - [Clifford gates](#clifford-gates)
              - [Clifford plus T](#clifford-plus-t)
              - [Gottesman-Knill theorem](#gottesman-knill-theorem)
            - [List of quantum logic gates](#list-of-quantum-logic-gates)
        - [Analog quantum computer](#analog-quantum-computer)
          - [Continuous-variable quantum information](#continuous-variable-quantum-information)
  - [Quantum computer physical implementation](#quantum-computer-physical-implementation)
    - [Carbon nanotube spin quantum computer](#carbon-nanotube-spin-quantum-computer)
      - [Organization developing carbon nanotube spin quantum computer](#organization-developing-carbon-nanotube-spin-quantum-computer)
        - [C12 Quantum Electronics](#c12-quantum-electronics)
          - [UCL Quantum Devices Group](#ucl-quantum-devices-group)
    - [Diamond vacancy quantum computer](#diamond-vacancy-quantum-computer)
      - [N-V center quantum computer](#n-v-center-quantum-computer)
      - [Nitrogen-vacancy center](#nitrogen-vacancy-center)
    - [Electron on helium quantum computer](#electron-on-helium-quantum-computer)
      - [Organization developing electron on helium quantum computer](#organization-developing-electron-on-helium-quantum-computer)
        - [EeroQ](#eeroq)
    - [Nuclear magnetic resonance quantum computer](#nuclear-magnetic-resonance-quantum-computer)
      - [Organization developing nuclear magnetic resonance quantum computer](#organization-developing-nuclear-magnetic-resonance-quantum-computer)
        - [Silicon Quantum Computing](#silicon-quantum-computing)
          - [Kane quantum computer](#kane-quantum-computer)
          - [Diraq](#diraq)
    - [Quantum dot quantum computer](#quantum-dot-quantum-computer)
      - [Organization developing quantum dot quantum computer](#organization-developing-quantum-dot-quantum-computer)
        - [Quantum Motion](#quantum-motion)
      - [Intel quantum computer](#intel-quantum-computer)
    - [Superconducting quantum computing](#superconducting-quantum-computing)
      - [Superconducting quantum computer need non-linear components](#superconducting-quantum-computer-need-non-linear-components)
      - [Superconducting qubit](#superconducting-qubit)
        - [Pros and cons of superconducting qubits](#pros-and-cons-of-superconducting-qubits)
          - [Con of superconducting qubits](#con-of-superconducting-qubits)
            - [Superconducting qubits are bad because it is harder to ensure that they are all the same](#superconducting-qubits-are-bad-because-it-is-harder-to-ensure-that-they-are-all-the-same)
          - [Pro of superconducting qubits](#pro-of-superconducting-qubits)
            - [Superconducting qubits are good because superconductivity is macroscopic](#superconducting-qubits-are-good-because-superconductivity-is-macroscopic)
            - [Superconducting qubits are bad because of fabrication variation](#superconducting-qubits-are-bad-because-of-fabrication-variation)
        - [Superconducting qubit type](#superconducting-qubit-type)
          - [Flux qubit](#flux-qubit)
          - [Transmon](#transmon)
            - [An Introduction to the Transmon Qubit for Electromagnetic Engineers](#an-introduction-to-the-transmon-qubit-for-electromagnetic-engineers)
            - [Rabi cycle](#rabi-cycle)
            - [The Hardware of a Quantum Computer by TU Delft](#the-hardware-of-a-quantum-computer-by-tu-delft)
      - [Organization developing superconducting quantum computer](#organization-developing-superconducting-quantum-computer)
        - [Alice&Bob](#alice-and-bob)
          - [Cat qubit](#cat-qubit)
        - [Google Quantum AI](#google-quantum-ai)
          - [Google Quantum Campus](#google-quantum-campus)
          - [Google Quantum AI employee](#google-quantum-ai-employee)
            - [Daniel Sank](#daniel-sank)
            - [Julian Kelly](#julian-kelly)
            - [John M. Martinis](#john-m-martinis)
          - [Google Quantum AI hardware](#google-quantum-ai-hardware)
            - [Sycamore processor](#sycamore-processor)
            - [Willow (quantum computer)](#willow-quantum-computer)
        - [IBM Quantum Computing](#ibm-quantum-computing)
          - [IBM quantum computer](#ibm-quantum-computer)
        - [IQM](#iqm)
        - [OpenSuperQ](#opensuperq)
        - [Oxford Quantum Circuits](#oxford-quantum-circuits)
          - [Ilana Wisby](#ilana-wisby)
        - [Rigetti Computing](#rigetti-computing)
    - [Topological quantum computer](#topological-quantum-computer)
    - [Trapped ion quantum computer](#trapped-ion-quantum-computer)
      - [Cirac–Zoller controlled-NOT gate](#cirac-zoller-controlled-not-gate)
      - [Ion trap](#ion-trap)
      - [Modular trapped ion quantum computer](#modular-trapped-ion-quantum-computer)
      - [Organization developing trapped ion quantum computer](#organization-developing-trapped-ion-quantum-computer)
        - [IonQ](#ionq)
        - [NQIT](#nqit)
        - [Oxford Ionics](#oxford-ionics)
        - [Quantinuum](#quantinuum)
          - [Quantinuum hardware](#quantinuum-hardware)
            - [Quantinuum H1](#quantinuum-h1)
            - [Quantinuum H1-2](#quantinuum-h1-2)
          - [Cambridge Quantum Computing](#cambridge-quantum-computing)
            - [tket](#tket)
          - [Honeywell Quantum Solutions](#honeywell-quantum-solutions)
        - [Universal Quantum](#universal-quantum)
    - [Neutral atom quantum computer](#neutral-atom-quantum-computer)
      - [Organization developing neutral atom quantum computer](#organization-developing-neutral-atom-quantum-computer)
        - [Atom Computing](#atom-computing)
        - [Infleqtion](#infleqtion)
        - [QuEra](#quera)
        - [Pasqal](#pasqal)
    - [Photonic quantum computer](#photonic-quantum-computer)
      - [Organization developing photonic quantum computer](#organization-developing-photonic-quantum-computer)
        - [Quandela](#quandela)
          - [Prometheus single photon source](#prometheus-single-photon-source)
        - [ORCA Computing](#orca-computing)
        - [PsiQuantum](#psiquantum)
          - [Jeremy O'Brien](#jeremy-o-brien)
          - [PsiQuantum founding myth](#psiquantum-founding-myth)
        - [Xanadu Quantum Technologies](#xanadu-quantum-technologies)
  - [Quantum computing hardware bibliography](#quantum-computing-hardware-bibliography)
    - [Hardware for Quantum Computing by Chuck Easttom](#hardware-for-quantum-computing-by-chuck-easttom)
      - [Chuck Easttom](#chuck-easttom)
- [Quantum interconnect](#quantum-interconnect)
  - [Quantum interconnect company](#quantum-interconnect-company)
    - [Welinq](#welinq)
- [Quantum computer simulator](#quantum-computer-simulator)
- [Quantum software](#quantum-software)
  - [Quantum programming framework](#quantum-programming-framework)
    - [Cirq](#cirq)
    - [PennyLane](#pennylane)
    - [Qiskit](#qiskit)
      - [Qiskit example](#qiskit-example)
        - [Qiskit hello world](#qiskit-hello-world)
          - [qiskit/hello.py](#_file/qiskit/hello.py)
        - [qiskit/initialize.py](#qiskit-initialize-py)
        - [qiskit/qft.py](#_file/qiskit/qft.py)
      - [Qiskit component](#qiskit-component)
        - [`qiskit.transpile()`](#qiskit-transpile)
        - [Qiskit Aer](#qiskit-aer)
          - [AerError: 'unknown instruction](#aererror-unknown-instruction)
  - [Quantum circuit description language](#quantum-circuit-description-language)
  - [OpenQASM](#openqasm)
  - [Quantum control system](#quantum-control-system)
    - [Quantum control systems use FPGAs](#quantum-control-systems-use-fpgas)
    - [Organization developing quantum control systems](#organization-developing-quantum-control-systems)
      - [ParityQC](#parityqc)
      - [Q-CTRL](#q-ctrl)
      - [QuantrolOx](#quantrolox)
      - [Quantum Machines](#quantum-machines)
      - [M-Labs](#m-labs)
        - [ARTIQ](#artiq)
          - [Duke ARTIQ extensions](#duke-artiq-extensions)
      - [Riverlane](#riverlane)
        - [Deltaflow.OS](#deltaflow-os)
      - [Zurich Instruments](#zurich-instruments)
    - [List of quantum control systems](#list-of-quantum-control-systems)
      - [Pulser (quantum control)](#pulser-quantum-control)
- [Classical computer](#classical-computer)
- [ZX-calculus](#zx-calculus)
  - [ZX-calculus biliography](#zx-calculus-biliography)
    - [Picturing Quantum Processes](#picturing-quantum-processes)
  - [PyZX](#pyzx)
- [Quantum state](#quantum-state)
  - [Bell state](#bell-state)
    - [Bell circuit](#bell-circuit)
  - [Greenberger-Horne-Zeilinger state](#greenberger-horne-zeilinger-state)
  - [Quantum memory](#quantum-memory)
- [Quantum supremacy](#quantum-supremacy)
  - [Google's 2019 quantum supremacy claim](#google-s-2019-quantum-supremacy-claim)
  - [Quantum advantage](#quantum-advantage)
- [Qubit](#qubit)
- [Quantum computer benchmark](#quantum-computer-benchmark)
  - [Comparison of quantum computing hardware](#comparison-of-quantum-computing-hardware)
  - [Algorithmic qubits](#algorithmic-qubits)
  - [Coherence time](#coherence-time)
  - [Depth of a quantum circuit](#depth-of-a-quantum-circuit)
  - [Quantum volume](#quantum-volume)
  - [Random circuit sampling](#random-circuit-sampling)
- [Quantum computing market](#quantum-computing-market)
  - [Quantum computing skepticism](#quantum-computing-skepticism)
    - [Are we in a quantum computing bubble?](#are-we-in-a-quantum-computing-bubble)
- [Post-quantum cryptography](#post-quantum-cryptography)
  - [Post-quantum cryptography company](#post-quantum-cryptography-company)
    - [CryptoNext](#cryptonext)
    - [PQShield](#pqshield)
  - [NIST Post-Quantum Cryptography Standardization](#nist-post-quantum-cryptography-standardization)
  - [Provably quantum secure encryption algorithm](#provably-quantum-secure-encryption-algorithm)
  - [Quantum resistant cryptosystem](#quantum-resistant-cryptosystem)
    - [Lattice-based cryptography](#lattice-based-cryptography)
- [Quantum computing outreach](#quantum-computing-outreach)
  - [Quantum computing scholarship](#quantum-computing-scholarship)
- [Quantum computing certification](#quantum-computing-certification)
- [Quantum computing bibliography](#quantum-computing-bibliography)
  - [Quantum computing report](#quantum-computing-report)
  - [Quantum computing news](#quantum-computing-news)
    - [The Quantum Insider](#the-quantum-insider)
  - [Quantum computing book](#quantum-computing-book)
    - [Quantum Computation and Quantum Information by Nielsen and Chuang](#quantum-computation-and-quantum-information-by-nielsen-and-chuang)
  - [Quantum computing university course](#quantum-computing-university-course)

## Introduction to quantum computing

↑ **Parent:** [Quantum computing](quantum-computing.md)

Course plan:
- [Section "Programmer's model of quantum computers"](#programmer-s-model-of-quantum-computers)
- look at a [Qiskit hello world](#qiskit-hello-world)
  - e.g. ours: [qiskit/hello.py](#_file/qiskit/hello.py)
- learn about [quantum circuits](#quantum-circuit).
  - [tensor product in quantum computing](#tensor-product-in-quantum-computing)
  - First we learn some [quantum logic gates](#quantum-logic-gate). This shows an alternative, and extremely important view of a quantum computer besides a matrix multiplication: as a circuit. Fundamental subsections:
    - [Section "Quantum logic gates are needed because you can't compute the matrix explicitly as it grows exponentially"](#quantum-logic-gates-are-needed-because-you-can-t-compute-the-matrix-explicitly-as-it-grows-exponentially)
    - [Section "Quantum logic gates are needed for physical implementation"](#quantum-logic-gates-are-needed-for-physical-implementation)
    - [Section "Universal quantum gates"](#universal-quantum-gates)
    - [Section "Quantum circuits vs classical circuits"](#quantum-circuits-vs-classical-circuits)
    - Examples of specific gates:
      - [Single-qubit gates](#single-qubit-gate):
        - [Pauli gate](#pauli-gate)
          - [Pauli-X gate](#pauli-x-gate)
        - [Hadamard gate](#hadamard-gate)
      - [Controlled quantum gate](#controlled-quantum-gate)
        - [CNOT gate](#cnot-gate)
      - [Bell state](#bell-state)
        - [Bell circuit](#bell-circuit)
  - [quantum algorithms](#quantum-algorithm)
    - [Section "Quantum Fourier transform"](#quantum-fourier-transform)
    - [Section "Shor's algorithm"](#shor-s-algorithm)

<a id="video-but-what-is-quantum-computing-by-3blue1brown"></a>
**[Video 1](#video-but-what-is-quantum-computing-by-3blue1brown). But what is quantum computing? by 3Blue1Brown.** [Source](https://www.youtube.com/watch?v=RQWpF2Gb-gU).

<h2 id="programmer-s-model-of-quantum-computers">Programmer's model of quantum computers</h2>

↑ **Parent:** [Quantum computing](quantum-computing.md)  
🏷️ **Tags:** [The best articles by Ciro Santilli](articles.md)

This is a quick tutorial on how a [quantum computer](quantum-computing.md) programmer thinks about how a quantum computer works. If you know:
- what a [complex number](formalization-of-mathematics.md#complex-number) is
- how to do [matrix multiplication](linear-algebra.md#matrix-multiplication)
- what is a [probability](mathematics.md#probability)
a concrete and precise [hello world](software.md#hello-world-program) operation can be understood in 30 minutes.

Although there are several [types of quantum computer](#quantum-computer-physical-implementation) under development, there exists a single high level model that represents what most of those computers can do, and we are going to explain that model here. This model is the is the [digital quantum computer](#digital-quantum-computer) model, which uses a [quantum circuit](#quantum-circuit), that is made up of many [quantum gates](#quantum-logic-gate).

Beyond that basic model, programmers only may have to consider the [imperfections of their hardware](#quantum-logic-gates-are-needed-for-physical-implementation), but the starting point will almost always be this basic model, and tooling that automates mapping the high level model to real hardware considering those imperfections (i.e. [quantum compilers](#quantum-compilation)) is already getting better and better.

The way quantum programmers think about a quantum computer in order to program can be described as follows:
- the input of a N qubit quantum computer is a vector of dimension N containing classic bits 0 and 1
- the quantum program, also known as circuit, is a $2^n \times 2^n$ [unitary matrix](linear-algebra.md#unitary-matrix) of [complex numbers](formalization-of-mathematics.md#complex-number) $Q \in \C^{2^n} \times \C^{2^n}$ that operates on the input to generate the output
- the output of a N qubit computer is also a vector of dimension N containing classic bits 0 and 1

To operate a quantum computer, you follow the [step of operation of a quantum computer](#step-of-operation-of-a-quantum-computer):
- set the input [qubits](#qubit) to classic input bits ([state initialization](#state-initialization-quantum-computing))
- press a big red "RUN" button
- read the classic output bits ([readout](#readout-quantum-computing))

Each time you do this, you are literally conducting a physical experiment of the specific [physical implementation](#quantum-computer-physical-implementation) of the computer:
- setup your physical system to represent the classical 0/1 inputs
- let the state evolve for long enough
- measure the classical output back out
and each run as the above can is simply called "an experiment" or "a measurement".

The output comes out "instantly" in the sense that it is physically impossible to observe any intermediate state of the system, i.e. there are no clocks like in classical computers, further discussion at: [quantum circuits vs classical circuits](#quantum-circuits-vs-classical-circuits). Setting up, running the experiment and taking the does take some time however, and this is important because you have to run the same experiment multiple times because results are probabilistic as mentioned below.

Unlike in a classical computer, the output of a quantum computer is not deterministic however.

But the each output is not equally likely either, otherwise the computer would be useless except as [random number generator](cryptography.md#random-number-generation)!

This is because the probabilities of each output for a given input depends on the program ([unitary matrix](linear-algebra.md#unitary-matrix)) it went through.

Therefore, what we have to do is to design the quantum circuit in a way that the right or better answers will come out more likely than the bad answers.

We then calculate the error bound for our circuit based on its design, and then determine how many times we have to run the experiment to reach the desired accuracy.

The probability of each output of a quantum computer is derived from the input and the circuit as follows.

First we take the classic input vector of dimension N of 0's and 1's and convert it to a "[quantum state vector](#quantum-state-vector)" $\va{q_{in}}$ of dimension $2^n$:

$$
\va{q_{in}} \in \C^{2^n}
$$

We are after all going to multiply it by the program matrix, as you would expect, and that has dimension $2^n \times 2^n$!

Note that this initial transformation also transforms the discrete zeroes and ones into [complex numbers](formalization-of-mathematics.md#complex-number).

For example, in a 3 qubit computer, the quantum state vector has dimension $2^3 = 8$ and the following shows all 8 possible conversions from the classic input to the quantum state vector:
```
000 -> 1000 0000 == (1.0, 0.0, 0.0, 0.0,  0.0, 0.0, 0.0, 0.0)
001 -> 0100 0000 == (0.0, 1.0, 0.0, 0.0,  0.0, 0.0, 0.0, 0.0)
010 -> 0010 0000 == (0.0, 0.0, 1.0, 0.0,  0.0, 0.0, 0.0, 0.0)
011 -> 0001 0000 == (0.0, 0.0, 0.0, 1.0,  0.0, 0.0, 0.0, 0.0)
100 -> 0000 1000 == (0.0, 0.0, 0.0, 0.0,  1.0, 0.0, 0.0, 0.0)
101 -> 0000 0100 == (0.0, 0.0, 0.0, 0.0,  0.0, 1.0, 0.0, 0.0)
110 -> 0000 0010 == (0.0, 0.0, 0.0, 0.0,  0.0, 0.0, 1.0, 0.0)
111 -> 0000 0001 == (0.0, 0.0, 0.0, 0.0,  0.0, 0.0, 0.0, 1.0)
```

This can be intuitively interpreted as:
- if the classic input is `000`, then we are certain that all three bits are 0.

  Therefore, the probability of all three 0's is 1.0, and all other possible combinations have 0 probability.
- if the classic input is `001`, then we are certain that bit one and two are 0, and bit three is 1. The probability of that is 1.0, and all others are zero.
- and so on

Now that we finally have our quantum state vector, we just multiply it by the [unitary matrix](linear-algebra.md#unitary-matrix) $Q$ of the quantum circuit, and obtain the $2^n$ dimensional output quantum state vector $\va{q_{out}}$:

$$
\va{q_{out}} = Q \: \va{q_{in}}
$$

And at long last, the probability of each classical outcome of the measurement is proportional to the square of the length of each entry in the quantum vector, analogously to what is done in the [Schrödinger equation](quantum-mechanics.md#schrodinger-equation).

For example, suppose that the 3 qubit output were:

$$
\begin{aligned}
\va{q_{out}} &=
\begin{bmatrix}
\frac{\sqrt{3}}{2} \\
0.0 \\
\frac{1}{2} \\
0.0 \\
0.0 \\
0.0 \\
0.0 \\
0.0
\end{bmatrix}
\end{aligned}
$$

Then, the probability of each possible outcomes would be the length of each component squared:

$$
\begin{aligned}
P(000) &= \left|\frac{\sqrt{3}}{2}\right|^2 &= \frac{\sqrt{3}}{2}^2 &= \frac{3}{4} \\
P(001) &= \left|0\right|^2                  &= 0^2 &= 0 \\
P(010) &= \left|\frac{\sqrt{1}}{2}\right|^2 &= \frac{\sqrt{1}}{2}^2 &= \frac{1}{4} \\
P(011) &= \left|0\right|^2                  &= 0^2 &= 0 \\
P(100) &= \left|0\right|^2                  &= 0^2 &= 0 \\
P(101) &= \left|0\right|^2                  &= 0^2 &= 0 \\
P(110) &= \left|0\right|^2                  &= 0^2 &= 0 \\
P(111) &= \left|0\right|^2                  &= 0^2 &= 0 \\
\end{aligned}
$$

i.e. 75% for the first, and 25% for the third outcomes, where just like for the input:
- first outcome means `000`: all output bits are zero
- third outcome means `010`: the first and third bits are zero, but the second one is 1

All other outcomes have probability 0 and cannot occur, e.g.: `001` is impossible.

Keep in mind that the [quantum state vector](#quantum-state-vector) can also contain [complex numbers because we are doing quantum mechanics](quantum-mechanics.md#why-are-complex-numbers-used-in-the-schrodinger-equation), but we just take their magnitude in that case, e.g. the following quantum state would lead to the same probabilities as the previous one:

$$
\begin{aligned}
\abs{\frac{1 + \sqrt{2}i}{2}}^2 &= \frac{1^2 + \sqrt{2^2}}{2^2} &= \frac{3}{4} \\
\abs{\frac{i}{2}}^2             &= \frac{1^2}{2^2}              &= \frac{1}{4}
\end{aligned}
$$

This interpretation of the quantum state vector clarifies a few things:
- the input quantum state is just a simple state where we are certain of the value of each classic input bit
- the matrix has to be unitary because the total probability of all possible outcomes must be 1.0

  This is true for the input matrix, and unitary matrices have the probability of maintaining that property after multiplication.

  Unitary matrices are a bit analogous to [self-adjoint operators](https://en.wikipedia.org/wiki/Self-adjoint_operator) in general quantum mechanics (self-adjoint in finite dimensions implies is stronger)

  This also allows us to understand intuitively why quantum computers may be capable of accelerating certain algorithms exponentially: that is because the quantum computer is able to quickly do an unitary matrix multiplication of a humongous $2^{N}$ sized matrix.

  If we are able to encode our algorithm in that matrix multiplication, considering the probabilistic interpretation of the output, then we stand a chance of getting that speedup.

As we could see, this model is was simple to understand, being only marginally more complex than that of a classical computer, see also: [https://quantumcomputing.stackexchange.com/questions/6639/is-my-background-sufficient-to-start-quantum-computing/14317#14317](https://quantumcomputing.stackexchange.com/questions/6639/is-my-background-sufficient-to-start-quantum-computing/14317#14317) The situation of quantum computers today in the 2020's is somewhat analogous to that of the early days of classical circuits and computers in the 1950's and 1960's, before [CPU](computer-hardware.md#central-processing-unit) came along and software ate the world. Even though the [exact physics of a classical computer](computer-hardware.md#semiconductor-device-fabrication) might be hard to understand and vary across different types of [integrated circuits](computer-hardware.md#integrated-circuit), those early hardware pioneers (and to this day modern CPU designers), can usefully view circuits from a higher level point of view, thinking only about concepts such as:
- [logic gates](computer-hardware.md#logic-gate) like AND, NOR and NOT
- a clock + registers
as modelled at the [register transfer level](computer-hardware.md#register-transfer-level), and only in a separate compilation step translated into actual chips. This high level understanding of how a classical computer works is what we can call "the programmer's model of a classical computer". So we are now going to describe the quantum analogue of it.

Bibliography:
- [https://arxiv.org/pdf/1804.03719.pdf](https://arxiv.org/pdf/1804.03719.pdf) Quantum Algorithm Implementations for Beginners by Abhijith et al. 2020

## Timeline of quantum computing

↑ **Parent:** [Quantum computing](quantum-computing.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Timeline_of_quantum_computing)

## Quantum algorithm

↑ **Parent:** [Quantum computing](quantum-computing.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Quantum_algorithm)

This is the true key question: what are the most important algorithms that would be accelerated by quantum computing?

Some candidates:
- [Shor's algorithm](#shor-s-algorithm): this one will actually make humanity worse off, as we will be forced into [post-quantum cryptography](#post-quantum-cryptography) that will likely be less efficient than existing classical [cryptography](cryptography.md) to implement
- [quantum algorithm for linear systems of equations](#quantum-algorithm-for-linear-systems-of-equations), and related [application of systems of linear equations](linear-algebra.md#application-of-systems-of-linear-equations)
- [Grover's algorithm](#grover-s-algorithm): speedup not exponential. Still useful for anything?
- [Quantum Fourier transform](https://en.wikipedia.org/wiki/Quantum_Fourier_transform): TODO is the speedup exponential or not?
- Deutsch: solves an useless problem
- [NISQ algorithms](#nisq-algorithm)

Do you have proper optimization or [quantum chemistry](physics.md#quantum-chemistry) algorithms that will make trillions?

Maybe there is some room for doubt because some applications might be way better in some [implementations](#quantum-computer-physical-implementation), but we should at least have a good general idea.

However, clear information on this really hard to come by, not sure why.

Whenever asked e.g. at: [https://physics.stackexchange.com/questions/3390/can-anybody-provide-a-simple-example-of-a-quantum-computer-algorithm/3407](https://physics.stackexchange.com/questions/3390/can-anybody-provide-a-simple-example-of-a-quantum-computer-algorithm/3407) on [Physics Stack Exchange](stack-overflow.md#physics-stack-exchange) people say the infinite mantra:

Lists:
- [Quantum Algorithm Zoo](#quantum-algorithm-zoo): the leading list as of 2020
- [quantum computing computational chemistry algorithms](physics.md#quantum-computing-computational-chemistry-algorithms) is the area that Ciro and many people are te most excited about is 
- [https://cstheory.stackexchange.com/questions/3888/np-intermediate-problems-with-efficient-quantum-solutions](https://cstheory.stackexchange.com/questions/3888/np-intermediate-problems-with-efficient-quantum-solutions)
- [https://mathoverflow.net/questions/33597/are-there-any-known-quantum-algorithms-that-clearly-fall-outside-a-few-narrow-cla](https://mathoverflow.net/questions/33597/are-there-any-known-quantum-algorithms-that-clearly-fall-outside-a-few-narrow-cla)

### Quantum computers are not expected to solve NP-complete problems

↑ **Parent:** [Quantum algorithm](#quantum-algorithm)

Only [NP-intermediate](computer-science.md#np-intermediate), which includes notably [integer factorization](computer-science.md#integer-factorization):
- [https://quantumcomputing.stackexchange.com/questions/16506/can-quantum-computer-solve-np-complete-problems](https://quantumcomputing.stackexchange.com/questions/16506/can-quantum-computer-solve-np-complete-problems)
- [https://www.cs.virginia.edu/~robins/The_Limits_of_Quantum_Computers.pdf](https://www.cs.virginia.edu/~robins/The_Limits_of_Quantum_Computers.pdf) by [Scott Aaronson](computer-science.md#scott-aaronson)
- [https://cs.stackexchange.com/questions/130470/can-quantum-computing-help-solve-np-complete-problems](https://cs.stackexchange.com/questions/130470/can-quantum-computing-help-solve-np-complete-problems)
- [https://www.quora.com/How-can-quantum-computing-help-to-solve-NP-hard-problems](https://www.quora.com/How-can-quantum-computing-help-to-solve-NP-hard-problems)

### Quantum Algorithm Zoo

↑ **Parent:** [Quantum algorithm](#quantum-algorithm)

[https://quantumalgorithmzoo.org/](https://quantumalgorithmzoo.org/)

Source on [GitHub](software.md#github): [https://github.com/stephenjordan/stephenjordan.github.io](https://github.com/stephenjordan/stephenjordan.github.io)

The most comprehensive list is the amazing curated and commented list of [quantum algorithms](#quantum-algorithm) as of 2020.

### Quantum algorithm vs quantum gate vs quantum circuit

↑ **Parent:** [Quantum algorithm](#quantum-algorithm)

There is no fundamental difference between them, a [quantum algorithm](#quantum-algorithm) is a [quantum circuit](#quantum-circuit), which can be seen as a super complicated [quantum gate](#quantum-logic-gate).

Perhaps the greats practical difference is that algorithms tend to be defined for an arbitrary number of N qubits, i.e. as a [function](formalization-of-mathematics.md#function-mathematics) for that each N produces a specific [quantum circuit](#quantum-circuit) with N [qubits](#qubit) solving the problem. Most named gates on the other hand have fixed small sizes.

### Quantum algorithm by problem

↑ **Parent:** [Quantum algorithm](#quantum-algorithm)

#### Quantum matrix multiplication

↑ **Parent:** [Quantum algorithm by problem](#quantum-algorithm-by-problem)

[https://cstheory.stackexchange.com/questions/2951/quantum-matrix-multiplication](https://cstheory.stackexchange.com/questions/2951/quantum-matrix-multiplication)

#### Quantum algorithm for linear systems of equations

↑ **Parent:** [Quantum algorithm by problem](#quantum-algorithm-by-problem)  
🏷️ **Tags:** [System of linear equations algorithm](linear-algebra.md#system-of-linear-equations-algorithm)

##### HHL algorithm

↑ **Parent:** [Quantum algorithm for linear systems of equations](#quantum-algorithm-for-linear-systems-of-equations)

### List of quantum algorithms

↑ **Parent:** [Quantum algorithm](#quantum-algorithm)

#### Bernstein-Vazirani algorithm

↑ **Parent:** [List of quantum algorithms](#list-of-quantum-algorithms)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Bernstein–Vazirani algorithm)

Toy/test/tought experiment algorithm.

<h4 id="grover-s-algorithm">Grover's algorithm</h4>

↑ **Parent:** [List of quantum algorithms](#list-of-quantum-algorithms)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Grover's_algorithm)

#### Hidden shift algorithm

↑ **Parent:** [List of quantum algorithms](#list-of-quantum-algorithms)

##### Hidden shift problem

↑ **Parent:** [Hidden shift algorithm](#hidden-shift-algorithm)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Hidden_shift_problem)

#### Quantum Fourier transform

↑ **Parent:** [List of quantum algorithms](#list-of-quantum-algorithms)  
🏷️ **Tags:** [Discrete Fourier transform](calculus.md#discrete-fourier-transform)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Quantum_Fourier_transform)

Sample implementations:
- [Qiskit](#qiskit): [qiskit/qft.py](#_file/qiskit/qft.py)

<h4 id="shor-s-algorithm">Shor's algorithm</h4>

↑ **Parent:** [List of quantum algorithms](#list-of-quantum-algorithms)  
🏷️ **Tags:** [Integer factorization algorithm](computer-science.md#integer-factorization-algorithm)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Shor's_algorithm)

<a id="video-shor-s-algorithm-explained-by-minutephysics-2019"></a>
**[Video 2](#video-shor-s-algorithm-explained-by-minutephysics-2019). Shor's algorithm Explained by minutephysics (2019)** [Source](https://www.youtube.com/watch?v=lvTqbM5Dq4Q).

<h5 id="how-many-logical-qubits-are-needed-to-run-shor-s-algorithm">How many logical qubits are needed to run Shor's algorithm?</h5>

↑ **Parent:** [Shor's algorithm](#shor-s-algorithm)

[https://quantumcomputing.stackexchange.com/questions/5048/how-many-logical-qubits-are-needed-to-run-shors-algorithm-efficiently-on-large](https://quantumcomputing.stackexchange.com/questions/5048/how-many-logical-qubits-are-needed-to-run-shors-algorithm-efficiently-on-large)

<h5 id="integer-factorization-algorithms-better-than-shor-s-algorithm">Integer factorization algorithms better than Shor's algorithm</h5>

↑ **Parent:** [Shor's algorithm](#shor-s-algorithm)


- 2023 [https://www.schneier.com/blog/archives/2023/01/breaking-rsa-with-a-quantum-computer.html](https://www.schneier.com/blog/archives/2023/01/breaking-rsa-with-a-quantum-computer.html) comments on "Factoring integers with sublinear resources on a superconducting quantum processor” [https://arxiv.org/pdf/2212.12372.pdf](https://arxiv.org/pdf/2212.12372.pdf)


> A group of Chinese researchers have just published a paper claiming that they can—although they have not yet done so—break 2048-bit RSA. This is something to take seriously. It might not be correct, but it’s not obviously wrong.
> 
> We have long known from Shor’s algorithm that factoring with a quantum computer is easy. But it takes a big quantum computer, on the orders of millions of qbits, to factor anything resembling the key sizes we use today. What the researchers have done is combine classical lattice reduction factoring techniques with a quantum approximate optimization algorithm. This means that they only need a quantum computer with 372 qbits, which is well within what’s possible today. (The IBM Osprey is a 433-qbit quantum computer, for example. Others are on their way as well.)

## Quantum compilation

↑ **Parent:** [Quantum computing](quantum-computing.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Quantum_compilation)

Software that maps higher level languages like [Qiskit](#qiskit) into actual quantum circuits.

### Quantum compiler benchmark

↑ **Parent:** [Quantum compilation](#quantum-compilation)

These appear to be benchmarks that don't involve running anything concretely, just compiling and likely then counting [gates](#quantum-logic-gate):
- [https://github.com/ArlineQ/arline_benchmarks](https://github.com/ArlineQ/arline_benchmarks)

### Quantum Intermediate Representation

↑ **Parent:** [Quantum compilation](#quantum-compilation)  
🏷️ **Tags:** [LLVM Intermediate Representation](software.md#llvm-intermediate-representation)

[https://devblogs.microsoft.com/qsharp/introducing-quantum-intermediate-representation-qir/](https://devblogs.microsoft.com/qsharp/introducing-quantum-intermediate-representation-qir/)

Used e.g. by [Oxford Quantum Circuits](#oxford-quantum-circuits), [https://www.linkedin.com/in/john-dumbell-627454121/](https://www.linkedin.com/in/john-dumbell-627454121/) mentions:

> Using [LLVM](software.md#llvm) to consume QIR and run optimization, scheduling and then outputting hardware-specific instructions.

Presumably the point of it is to allow simulation in [classical computers](#classical-computer)?

### Quantum error correction

↑ **Parent:** [Quantum compilation](#quantum-compilation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Quantum_error_correction)

Technique that uses multiple non-[ideal](science.md#idealism) qubits (physical qubits) to simulate/produce one perfect qubit (logical).

One is philosophically reminded of classical [error correction codes](technology.md#error-correction-code), where we also have multiple input bits per actual information bit.

TODO understand in detail. This appears to be a fundamental technique since all physical systems we can manufacture are imperfect.

Part of the fundamental interest of this technique is due to the [quantum threshold theorem](#quantum-threshold-theorem).

For example, when [PsiQuantum raised 215M in 2020](https://www.bloomberg.com/news/articles/2020-04-06/quantum-computing-startup-raises-215-million-for-faster-device), they announced that they intended to reach 1 million physical qubits, which would achieve between 100 and 300 logical qubits.

[Video 43. "Jeremy O'Brien: "Quantum Technologies" by GoogleTechTalks (2014)"](#video-jeremy-o-brien-quantum-technologies-by-googletechtalks-2014) [https://youtu.be/7wCBkAQYBZA?t=2778](https://youtu.be/7wCBkAQYBZA?t=2778) describes an error correction approach for a [photonic quantum computer](#photonic-quantum-computer).

Bibliography:
- [https://errorcorrectionzoo.org/domain/quantum_domain](https://errorcorrectionzoo.org/domain/quantum_domain)

#### Quantum error correction code

↑ **Parent:** [Quantum error correction](#quantum-error-correction)  
🏷️ **Tags:** [Error correction code](technology.md#error-correction-code)

##### Surface code

↑ **Parent:** [Quantum error correction code](#quantum-error-correction-code)

- [https://www.nature.com/articles/s41586-022-05434-1](https://www.nature.com/articles/s41586-022-05434-1)
- [https://www.qutube.nl/quantum-computer-12/surface-codes](https://www.qutube.nl/quantum-computer-12/surface-codes)
- [https://quantumcomputing.stackexchange.com/questions/2106/what-is-the-surface-code-in-the-context-of-quantum-error-correction](https://quantumcomputing.stackexchange.com/questions/2106/what-is-the-surface-code-in-the-context-of-quantum-error-correction)

#### Quantum threshold theorem

↑ **Parent:** [Quantum error correction](#quantum-error-correction)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Quantum_threshold_theorem)

This theorem roughly states that states that for every [quantum algorithm](#quantum-algorithm), once we reach a certain level of physical error rate small enough (where small enough is algorithm dependant), then we can _perfectly_ error correct.

This algorithm provides the conceptual division between [noisy intermediate-scale quantum era](#noisy-intermediate-scale-quantum-era) and post-NISQ.

##### Noisy intermediate-scale quantum era

↑ **Parent:** [Quantum threshold theorem](#quantum-threshold-theorem)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Noisy_intermediate-scale_quantum_era)

Era of [quantum computing](quantum-computing.md) before we reach physical errors small enough to do perfect [quantum error correction](#quantum-error-correction) as demonstrated by the [quantum threshold theorem](#quantum-threshold-theorem).

###### NISQ algorithm

↑ **Parent:** [Noisy intermediate-scale quantum era](#noisy-intermediate-scale-quantum-era)  
🏷️ **Tags:** [Quantum algorithm](#quantum-algorithm)

A [quantum algorithm](#quantum-algorithm) that is thought to be more likely to be useful in the [NISQ](#noisy-intermediate-scale-quantum-era) era of [quantum computing](quantum-computing.md).

###### Variational quantum eigensolver

↑ **Parent:** [NISQ algorithm](#nisq-algorithm)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Variational_quantum_eigensolver)

TODO clear example of the [computational problem](computer-science.md#computational-problem) that it solves.

###### Quantum optimization algorithm

↑ **Parent:** [NISQ algorithm](#nisq-algorithm)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Quantum_optimization_algorithms)

###### Quantum approximate optimization algorithm

↑ **Parent:** [Quantum optimization algorithm](#quantum-optimization-algorithm)

TODO clear example of the [computational problem](computer-science.md#computational-problem) that it solves.

###### Quadratic unconstrained binary optimization

↑ **Parent:** [Quantum optimization algorithm](#quantum-optimization-algorithm)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Quadratic_unconstrained_binary_optimization)

### High level quantum synthesis

↑ **Parent:** [Quantum compilation](#quantum-compilation)

This is a term "invented" by [Ciro Santilli](ciro-santilli.md) to refer to quantum compilers that are able to convert non-specifically-quantum ([functional](programming-language.md#functional-programming), since there is no state in quantum software) programs into [quantum circuit](#quantum-circuit).

The term is made by adding "quantum" to the more "classical" concept of "[high-level synthesis](computer-hardware.md#high-level-synthesis)", which refers to software that converts an [imperative program](programming-language.md#imperative-programming) into [register transfer level](computer-hardware.md#register-transfer-level) hardware, typicially for [FPGA](computer-hardware.md#field-programmable-gate-array) applications.

#### Classiq

↑ **Parent:** [High level quantum synthesis](#high-level-quantum-synthesis)  
🏷️ **Tags:** [Organization developing quantum software](#organization-developing-quantum-software)

[https://www.classiq.io](https://www.classiq.io)

## Quantum computing player

↑ **Parent:** [Quantum computing](quantum-computing.md)

It is hard to beat the list present at [Quantum computing report](#quantum-computing-report): [https://quantumcomputingreport.com/players/](https://quantumcomputingreport.com/players/).

The much less-complete Wikipedia page is also of interest: [https://en.wikipedia.org/wiki/List_of_companies_involved_in_quantum_computing_or_communication](https://en.wikipedia.org/wiki/List_of_companies_involved_in_quantum_computing_or_communication) It has the merit of having a few extra columns compared to [Quantum computing report](#quantum-computing-report).

Also of interest: [https://quantumzeitgeist.com/interactive-map-of-quantum-computing-companies-from-around-the-globe/](https://quantumzeitgeist.com/interactive-map-of-quantum-computing-companies-from-around-the-globe/)

### Quantum computing player in Brazil

↑ **Parent:** [Quantum computing player](#quantum-computing-player)

- Paulo Nussenzveig physics researcher at [University of São Paulo](university.md#university-of-sao-paulo). Laboratory page: [http://portal.if.usp.br/lmcal/pt-br/node/323](http://portal.if.usp.br/lmcal/pt-br/node/323): LMCAL, laboratory of coherent manipulation of atoms and light. [Google Scholar](education.md#google-scholar): [https://scholar.google.com/citations?user=FbGL0BEAAAAJ](https://scholar.google.com/citations?user=FbGL0BEAAAAJ)
- Brazil Quantum: interest group created by students. Might be a software consultancy: [https://www.terra.com.br/noticias/tecnologia/inovacao/pesquisadores-paulistas-tentam-colocar-brasil-no-mapa-da-computacao-quantica,2efe660fbae16bc8901b1d00d139c8d2sz31cgc9.html](https://www.terra.com.br/noticias/tecnologia/inovacao/pesquisadores-paulistas-tentam-colocar-brasil-no-mapa-da-computacao-quantica,2efe660fbae16bc8901b1d00d139c8d2sz31cgc9.html)
- DOBSLIT [https://dobslit.com/en/the-company/](https://dobslit.com/en/the-company/) company in São Carlos, as of 2022 a quantum software consultancy with 3 people: [https://www.linkedin.com/search/results/people/?currentCompany=%5B%2272433615%22%5D&origin=COMPANY_PAGE_CANNED_SEARCH&sid=TAj](https://www.linkedin.com/search/results/people/?currentCompany=%5B%2272433615%22%5D&origin=COMPANY_PAGE_CANNED_SEARCH&sid=TAj) two of them from the [Federal University of São Carlos](university.md#federal-university-of-sao-carlos)
- [https://computacaoquanticabrasil.com/](https://computacaoquanticabrasil.com/) Website half broken as of 2022. Mentions a certain Lagrange Foundation, but their website is down.
- QuInTec academic interest group
  - [https://www.terra.com.br/noticias/tecnologia/inovacao/pesquisadores-paulistas-tentam-colocar-brasil-no-mapa-da-computacao-quantica,2efe660fbae16bc8901b1d00d139c8d2sz31cgc9.html](https://www.terra.com.br/noticias/tecnologia/inovacao/pesquisadores-paulistas-tentam-colocar-brasil-no-mapa-da-computacao-quantica,2efe660fbae16bc8901b1d00d139c8d2sz31cgc9.html) mentions 6 professors, 3 from [USP](university.md#university-of-sao-paulo) 3 from [UNICAMP](university.md#university-of-campinas) interest group:
  - [https://drive.google.com/file/d/1geGaRuCpRHeuLH2MLnLoxEJ1iOz4gNa9/view](https://drive.google.com/file/d/1geGaRuCpRHeuLH2MLnLoxEJ1iOz4gNa9/view) white paper gives all names
    - Celso Villas-Bôas
    - Frederico Brito
    - Gustavo Wiederhecker
    - Marcelo Terra Cunha
    - Paulo Nussenzveig
    - Philippe Courteille
  - [https://sites.google.com/unicamp.br/quintec/home](https://sites.google.com/unicamp.br/quintec/home) their website.
  - a 2021 symposium they organized: [http://www.saocarlos.usp.br/dia-09-quintec-quantum-engineering-workshop/](http://www.saocarlos.usp.br/dia-09-quintec-quantum-engineering-workshop/) some people of interest:
    - Samuraí Brito [https://www.linkedin.com/in/samuraí-brito-4a57a847/](https://www.linkedin.com/in/samuraí-brito-4a57a847/) at Itaú Unibanco, a Brazilian bank
    - [https://www.linkedin.com/in/dario-sassi-thober-5ba2923/](https://www.linkedin.com/in/dario-sassi-thober-5ba2923/) from [https://wvblabs.com.br/](https://wvblabs.com.br/)
    - [https://www.linkedin.com/in/roberto-panepucci-phd](https://www.linkedin.com/in/roberto-panepucci-phd) from [https://en.wikipedia.org/wiki/Centro_de_Pesquisas_Renato_Archer](https://en.wikipedia.org/wiki/Centro_de_Pesquisas_Renato_Archer) in Campinas
- Quanby quantum software in Florianópolis, founder Eduardo Duzzioni
- [https://thequantumhubs.com/category/quantum-brazil-news/](https://thequantumhubs.com/category/quantum-brazil-news/) good links
- [http://qubit.lncc.br/?lang=en](http://qubit.lncc.br/?lang=en) Quantum Computing Group of the National Laboratory for Scientific Computing: [https://pt.wikipedia.org/wiki/Laboratório_Nacional_de_Computação_Científica](https://pt.wikipedia.org/wiki/Laboratório_Nacional_de_Computação_Científica) in Rio. The principal researcher seems to be [https://www.lncc.br/~portugal/](https://www.lncc.br/~portugal/). He knows what [GitHub](software.md#github) is: [https://github.com/programaquantica/tutoriais](https://github.com/programaquantica/tutoriais), PDF without .tex though.
- [https://quantum-latino.com/](https://quantum-latino.com/) conference. E.g. 2022: [https://www.canva.com/design/DAFErjU3Wvk/2xo25nEuqv9O7RbCPLNEkw/view](https://www.canva.com/design/DAFErjU3Wvk/2xo25nEuqv9O7RbCPLNEkw/view)

### Quantum computing company

↑ **Parent:** [Quantum computing player](#quantum-computing-player)

### Quantum computing research institute

↑ **Parent:** [Quantum computing player](#quantum-computing-player)

#### QuTech

↑ **Parent:** [Quantum computing research institute](#quantum-computing-research-institute)  
🏷️ **Tags:** [Delft University of Technology](university.md#delft-university-of-technology)

##### QuTech Academy

↑ **Parent:** [QuTech](#qutech)  
🏷️ **Tags:** [Quantum computing outreach](#quantum-computing-outreach)

One of their learning sites: [https://www.qutube.nl/](https://www.qutube.nl/)

The educational/outreach branch of [QuTech](#qutech).

[https://qutechacademy.nl/](https://qutechacademy.nl/)

[https://www.youtube.com/@QuTechAcademy](https://www.youtube.com/@QuTechAcademy)

### Organization developing quantum hardware

↑ **Parent:** [Quantum computing player](#quantum-computing-player)

#### D-Wave Systems

↑ **Parent:** [Organization developing quantum hardware](#organization-developing-quantum-hardware)  
🏷️ **Tags:** [Company](company.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/D-Wave_Systems)

[Vaporware](computer.md#vaporware)?

#### ColdQuanta

↑ **Parent:** [Organization developing quantum hardware](#organization-developing-quantum-hardware)  
🏷️ **Tags:** [American company](company.md#american-company)

Not a [quantum computing](quantum-computing.md) pure-play, they also do sensing.

### Organization developing quantum software

↑ **Parent:** [Quantum computing player](#quantum-computing-player)

#### Haiqu

↑ **Parent:** [Organization developing quantum software](#organization-developing-quantum-software)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Haiqu)

[https://haiqu.ai](https://haiqu.ai)

#### Quantum Computing Inc.

↑ **Parent:** [Organization developing quantum software](#organization-developing-quantum-software)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Quantum_Computing_Inc.)

Really weird and obscure company, good coverage: [https://thequantuminsider.com/2020/02/06/quantum-computing-incorporated-the-first-publicly-traded-quantum-computing-stock/](https://thequantuminsider.com/2020/02/06/quantum-computing-incorporated-the-first-publicly-traded-quantum-computing-stock/)

Publicly traded in 2007, but only pivoted to [quantum computing](quantum-computing.md) much later.

Social media:
- [https://www.youtube.com/@quantumcomputinginc6758/videos](https://www.youtube.com/@quantumcomputinginc6758/videos)
- [https://twitter.com/QciQuantum?ref_src=twsrc%5Egoogle%7Ctwcamp%5Eserp%7Ctwgr%5Eauthor](https://twitter.com/QciQuantum?ref_src=twsrc%5Egoogle%7Ctwcamp%5Eserp%7Ctwgr%5Eauthor)
- [https://www.quantumcomputinginc.com/](https://www.quantumcomputinginc.com/)

#### Microsoft Quantum

↑ **Parent:** [Organization developing quantum software](#organization-developing-quantum-software)  
🏷️ **Tags:** [Microsoft](microsoft.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Microsoft_Quantum)

#### Phasecraft

↑ **Parent:** [Organization developing quantum software](#organization-developing-quantum-software)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Phasecraft)

[https://www.phasecraft.io](https://www.phasecraft.io)

The co-founder's name, Toby Cubitt, is the mos awesome thing ever (Cubitt -\> [qubit](#qubit)). From [UCL](university.md#university-college-london).

Funding:
- 2023: £13m: [https://www.uktech.news/deep-tech/phasecraft-quantum-computing-20230816](https://www.uktech.news/deep-tech/phasecraft-quantum-computing-20230816)

## Quantum computing paradigm

↑ **Parent:** [Quantum computing](quantum-computing.md)

## Quantum computing hardware

↑ **Parent:** [Quantum computing](quantum-computing.md)

### Step of operation of a quantum computer

↑ **Parent:** [Quantum computing hardware](#quantum-computing-hardware)

#### State initialization (quantum computing)

↑ **Parent:** [Step of operation of a quantum computer](#step-of-operation-of-a-quantum-computer)

#### Readout (quantum computing)

↑ **Parent:** [Step of operation of a quantum computer](#step-of-operation-of-a-quantum-computer)

### Quantum computers as experiments that are hard to predict outcomes

↑ **Parent:** [Quantum computing hardware](#quantum-computing-hardware)

One possibly interesting and possibly obvious point of view, is that a quantum computer is an experimental device that executes a quantum probabilistic experiment for which the probabilities cannot be calculated theoretically efficiently by a [nuclear weapon](nuclear-weapon.md).

This is how quantum computing was originally theorized by the likes of [Richard Feynman](richard-feynman.md): they noticed that "Hey, here's a well formulated [quantum mechanics](quantum-mechanics.md) problem, which I know the algorithm to solve (calculate the probability of outcomes), but it would take exponential time on the problem size".

The converse is then of course that if you were able to encode useful problems in such an experiment, then you have a computer that allows for exponential speedups.

This can be seen very directly by studying one specific quantum computer implementation. E.g. if you take the simplest to understand one, [photonic quantum computer](#photonic-quantum-computer), you can make systems for which you need exponential time to calculate the probabilities that photons will exit through certain holes and not others.

The obvious aspect of this idea is by coming from [quantum logic gates are needed because you can't compute the matrix explicitly as it grows exponentially](#quantum-logic-gates-are-needed-because-you-can-t-compute-the-matrix-explicitly-as-it-grows-exponentially): knowing the full explicit matrix is impossible in practice, and knowing the matrix is equivalent to knowing the probabilities of every outcome.

### Quantum computing is hard because we want long coherence but fast control

↑ **Parent:** [Quantum computing hardware](#quantum-computing-hardware)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Quantum_computing_is_hard_because_we_want_long_coherence_but_fast_control)

Mentioned e.g. at:
- [https://youtu.be/t5nxusm_Umk?t=176](https://youtu.be/t5nxusm_Umk?t=176)
- [https://youtu.be/xjlGL4Mvq7A?t=169](https://youtu.be/xjlGL4Mvq7A?t=169)

These are two conflicting constraints:
- long [coherence times](#coherence-time): require isolation from external world, otherwise observation destroys quantum state
- [fast control](#state-initialization-quantum-computing) and [readout](#readout-quantum-computing): require coupling with external world

### Quantum computer type

↑ **Parent:** [Quantum computing hardware](#quantum-computing-hardware)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Quantum_computer_type)

#### Model of quantum computing

↑ **Parent:** [Quantum computer type](#quantum-computer-type)

##### Measurement and circuit based quantum computers

↑ **Parent:** [Model of quantum computing](#model-of-quantum-computing)

###### Circuit-based quantum computer

↑ **Parent:** [Measurement and circuit based quantum computers](#measurement-and-circuit-based-quantum-computers)

Synonym to [gate-based quantum computer](#digital-quantum-computer)/[digital quantum computer](#digital-quantum-computer)?

###### Measurement-based quantum computer

↑ **Parent:** [Measurement and circuit based quantum computers](#measurement-and-circuit-based-quantum-computers)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/One-way quantum computer)

TODO confirm: apparently in the paradigm you can choose to measure only certain output [qubits](#qubit).

This makes things irreversible (TODO what does reversibility mean in this random context?), as opposed to [Circuit-based quantum computer](#circuit-based-quantum-computer) where you measure all output qubits at once.

TODO what is the advantage?

##### Analog and digital quantum computers

↑ **Parent:** [Model of quantum computing](#model-of-quantum-computing)

###### Digital quantum computer

↑ **Parent:** [Analog and digital quantum computers](#analog-and-digital-quantum-computers)

As of 2022, this tends to be the more "default" when you talk about a quantum computer.

But there are some serious [analog quantum computer](#analog-quantum-computer) contestants in the field as well.

###### Quantum circuit

↑ **Parent:** [Digital quantum computer](#digital-quantum-computer)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Quantum_circuit)

A [quantum circuit](#quantum-circuit) is a [graph](mathematics.md#graph-discrete-mathematics) of [quantum logic gates](#quantum-logic-gate).

[Quantum circuits](#quantum-circuit) are the prevailing [model of quantum computing](#model-of-quantum-computing) as of the 2010's - 2020's

###### Quantum state vector

↑ **Parent:** [Quantum circuit](#quantum-circuit)

###### Tensor product in quantum computing

↑ **Parent:** [Quantum circuit](#quantum-circuit)  
🏷️ **Tags:** [Tensor product](linear-algebra.md#tensor-product)

We don't need to understand a super generalized version of [tensor products](linear-algebra.md#tensor-product) to know what they mean in basic [quantum computing](quantum-computing.md)!

Intuitively, taking a [tensor product](linear-algebra.md#tensor-product) of two [qubits](#qubit) simply means putting them together on the same quantum system/computer.

When we write the [bra-ket notation](quantum-mechanics.md#bra-ket-notation): $\ket{00}$ that is the same as $\ket{0} \otimes \ket{0}$.

The tensor product is called a "product" because it distributes over addition.

E.g. consider:

$$
(\frac{\ket{0} + \ket{1}}{\sqrt{2}}) \otimes \ket{0} =
\frac{\ket{0} \otimes \ket{0} + \ket{1} \otimes \ket{0}}{\sqrt{2}} =
\frac{\ket{00} + \ket{10}}{\sqrt{2}}
$$

Intuitively, in this operation we just put a [Hadamard gate](#hadamard-gate) qubit together with a second pure $\ket{0}$ qubit.

And the outcome still has the second qubit as always 0, because we haven't made them interact.

The [quantum state](#quantum-state) $\frac{\ket{00} + \ket{10}}{\sqrt{2}}$ is called a [separable state](quantum-mechanics.md#separable-state), because it can be written as a single product of two different qubits. We have simply brought two qubits together, without making them interact.

If we then add a [CNOT gate](#cnot-gate) to make a [Bell state](#bell-state):

$$
\frac{\ket{00} + \ket{11}}{\sqrt{2}} =
\frac{\ket{0} \otimes \ket{0} + \ket{1} \otimes \ket{1}}{\sqrt{2}}
$$

we can now see that the [Bell state](#bell-state) is [non-separable](quantum-mechanics.md#separable-state): we've made the two qubits interact, and there is no way to write this state with a single [tensor product](linear-algebra.md#tensor-product). The qubits are fundamentally [entangled](quantum-mechanics.md#quantum-entanglement).

###### Quantum circuits vs classical circuits

↑ **Parent:** [Quantum circuit](#quantum-circuit)

Just like a classic [programmer](software.md#software-engineer) does not need to understand the intricacies of how transistors are implemented and [CMOS](electronics.md#cmos) semiconductors, the quantum programmer does not understand physical intricacies of the underlying [physical implementation](#quantum-computer-physical-implementation).

The main difference to keep in mind is that quantum computers cannot [save and observe intermediate quantum state](https://en.wikipedia.org/wiki/Observer_effect_(physics)), so programming a quantum computer is basically like programming a combinatorial-like circuit with gates that operate on (qu)bits:
- [https://quantumcomputing.stackexchange.com/questions/8441/does-a-quantum-computer-have-a-clock-signal-and-if-yes-how-big-is-it/9383#9383](https://quantumcomputing.stackexchange.com/questions/8441/does-a-quantum-computer-have-a-clock-signal-and-if-yes-how-big-is-it/9383#9383)
- [https://quantumcomputing.stackexchange.com/questions/8849/quantum-circuits-explain-algorithms-why-didnt-classical-circuits/8869#8869](https://quantumcomputing.stackexchange.com/questions/8849/quantum-circuits-explain-algorithms-why-didnt-classical-circuits/8869#8869)

For this reason programming a quantum computer is much like programming a classical combinatorial circuit as you would do with [SPICE](https://en.wikipedia.org/wiki/SPICE), [verilog-or-vhdl](computer-hardware.md#register-transfer-level), in which you are basically describing a graph of gates that goes from the input to the output

For this reason, we can use the words "program" and "circuit" interchangeably to refer to a quantum program

Also remember that and there is no no clocks in combinatorial circuits because there are no registers to drive; and so there is no analogue of clock in the quantum system either,

Another consequence of this is that programming quantum computers does not look like programming the more "common" procedural programming languages such as C or Python, since those fundamentally rely on processor register / memory state all the time.

Quantum programmers can however use classic languages to help describe their quantum programs more easily, for example this is what happens in [Qiskit](#qiskit), where you write a Python program that makes Qiskit library calls that describe the quantum program.

###### Quantum logic gate

↑ **Parent:** [Digital quantum computer](#digital-quantum-computer)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Quantum_logic_gate)

At [Section "Quantum computing is just matrix multiplication"](#programmer-s-model-of-quantum-computers) we saw that making a quantum circuit actually comes down to designing one big [unitary matrix](linear-algebra.md#unitary-matrix).

We have to say though that that was a bit of a lie.

Quantum programmers normally don't just produce those big matrices manually from scratch.

Instead, they use [quantum logic gates](#quantum-logic-gate).

The following are the main reasons for that:
- [Section "Quantum logic gates are needed because you can't compute the matrix explicitly as it grows exponentially"](#quantum-logic-gates-are-needed-because-you-can-t-compute-the-matrix-explicitly-as-it-grows-exponentially)
- [Section "Quantum logic gates are needed for physical implementation"](#quantum-logic-gates-are-needed-for-physical-implementation)

<h6 id="quantum-logic-gates-are-needed-because-you-can-t-compute-the-matrix-explicitly-as-it-grows-exponentially">Quantum logic gates are needed because you can't compute the matrix explicitly as it grows exponentially</h6>

↑ **Parent:** [Quantum logic gate](#quantum-logic-gate)

One key insight, is that the matrix of a non-trivial quantum circuit is going to be huge, and won't fit into any amount classical memory that can be present in this universe.

This is because the matrix is exponential in the number qubits, and $2^{100}$ is more than the number of atoms in the universe!

Therefore, off the bat we know that we cannot possibly describe those matrices in an explicit form, but rather must use some kind of shorthand.

But it gets worse.

Even if we had enough memory, the act of explicitly computing the matrix is not generally possible.

This is because knowing the matrix, basically means knowing the probability result for all possible $2^{N}$ outputs for each of the $2^{N}$ possible inputs.

But if we had those probabilities, our algorithmic problem would already be solved in the first place! We would "just" go over each of those output probabilities (OK, there are $2^{N}$ of those, which is also an insurmountable problem in itself), and the largest probability would be the answer.

So if we could calculate those probabilities on a classical machine, we would also be able to simulate the quantum computer on the classical machine, and quantum computing would not be able to give exponential speedups, which we know it does.

To see this, consider that for a given input, say `000` on a 3 qubit machine, the corresponding 8-sized quantum state looks like:
```
000 -> 1000 0000 == (1.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0)
```
and therefore when you multiply it by the unitary matrix of the quantum circuit, what you get is the first column of the unitary matrix of the quantum circuit. And `001`, gives the second column and so on.

As a result, to prove that a quantum algorithm is correct, we need to be a bit smarter than "just calculate the full matrix".

Which is why you should now go and read: [Section "Quantum algorithm"](#quantum-algorithm).

This type of thinking links back to how physical experiments relate to quantum computing: a quantum computer realizes a physical experiment to which we cannot calculate the probabilities of outcomes without exponential time.

So for example in the case of a [photonic quantum computer](#photonic-quantum-computer), you are not able to calculate from theory the probability that photons will show up on certain wires or not.

###### Quantum logic gates are needed for physical implementation

↑ **Parent:** [Quantum logic gate](#quantum-logic-gate)

One direct practical reason is that we need to map the matrix to real quantum hardware somehow, and all quantum hardware designs so far and likely in the future are gate-based: you manipulate a small number of qubits at a time (2) and add more and more of such operations.

While there are "[quantum compilers](#quantum-compilation)" to increase the portability of quantum programs, it is to be expected that programs manually crafted for a specific hardware will be more efficient just like in classic computers.

TODO: is there any clear reason why computers can't beat humans in approximating any unitary matrix with a gate set?

This is analogous to what classic circuit programmers will do, by using smaller [logic gates](computer-hardware.md#logic-gate) to create complex circuits, rather than directly creating one huge [truth table](computer-hardware.md#truth-table).

The most commonly considered quantum gates take 1, 2, or 3 qubits as input.

The gates themselves are just unitary matrices that operate on the input qubits and produce the same number of output qubits.

For example, the matrix for the [CNOT gate](#cnot-gate), which takes 2 qubits as input is:
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

TODO lazy to properly learn right now. Apparently you have to use the [Kronecker product](https://en.wikipedia.org/wiki/Kronecker_product) by the identity matrix. Also, [zX-calculus](#zx-calculus) appears to provide a powerful alternative method in some/all cases.

Bibliography:
- [https://quantumcomputing.stackexchange.com/questions/2299/how-to-interpret-a-quantum-circuit-as-a-matrix](https://quantumcomputing.stackexchange.com/questions/2299/how-to-interpret-a-quantum-circuit-as-a-matrix)

###### Universal quantum gates

↑ **Parent:** [Quantum logic gate](#quantum-logic-gate)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Quantum_logic_gate#Universal_quantum_gates)

Just [like as for classic gates](https://en.wikipedia.org/wiki/Functional_completeness), we would like to be able to select [quantum computer physical implementations](#quantum-computer-physical-implementation) that can represent one or a few gates that can be used to create _any_ quantum circuit.

Unfortunately, in the case of quantum circuits this is obviously impossible, since the space of N x N unitary matrices is infinite and continuous.

Therefore, when we say that certain gates form a "set of universal quantum gates", we actually mean that "any unitary matrix can be approximated to arbitrary precision with enough of these gates".

Or if you like fancy Mathy words, you can say that the subgroup of the [unitary group](geometry.md#unitary-group) [generated by](group.md#subgroup-generated-by-a-group) our basic gate set is a [dense subset](calculus.md#dense-set) of the unitary group.

###### Single-qubit gate

↑ **Parent:** [Quantum logic gate](#quantum-logic-gate)

The first two that you should study are:
- [Quantum NOT gate](#pauli-x-gate)
- [Hadamard gate](#hadamard-gate)
- [Phase shift gate](#phase-shift-gate)

###### Hadamard gate

↑ **Parent:** [Single-qubit gate](#single-qubit-gate)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Quantum_logic_gate#Hadamard_gate)

The [Hadamard gate](#hadamard-gate) takes $\ket{0}$ or $\ket{1}$ ([quantum states](#quantum-state) with probability 1.0 of measuring either 0 or 1), and produces states that have equal probability of 0 or 1.

<a id="equation-hadamard-gate-matrix"></a>
$$
H = \frac{1}{\sqrt{2}} \begin{bmatrix} 1 & 1 \\ 1 & -1 \end{bmatrix}
$$

<a id="image-hadamard-gate-symbol"></a>
![](https://upload.wikimedia.org/wikipedia/commons/1/1a/Hadamard_gate.svg)

**[Figure 1](#image-hadamard-gate-symbol). Hadamard gate symbol**. [Source](https://commons.wikimedia.org/wiki/File:Hadamard_gate.svg).

###### Pauli gate

↑ **Parent:** [Single-qubit gate](#single-qubit-gate)

###### Pauli-X gate

↑ **Parent:** [Pauli gate](#pauli-gate)

The [quantum NOT gate](#pauli-x-gate) swaps the state of $\ket{0}$ and $\ket{1}$, i.e. it maps:

$$
x \ket{0} + y \ket{y} \to y \ket{0} + x \ket{y}
$$

As a result, this gate also inverts the probability of measuring 0 or 1, e.g.
- if the old probability of 0 was 0, then it becomes 1
- if the old probability of 0 was 0.2, then it becomes 0.8

<a id="equation-quantum-not-gate-matrix"></a>
$$
\begin{bmatrix}
0 & 1 \\
1 & 0 \\
\end{bmatrix}
$$

<a id="image-quantum-not-gate-symbol"></a>
![](https://upload.wikimedia.org/wikipedia/commons/9/91/Qcircuit_CNOT.svg)

**[Figure 2](#image-quantum-not-gate-symbol). Quantum NOT gate symbol**. [Source](https://commons.wikimedia.org/wiki/File:Qcircuit_CNOT.svg).

###### Pauli-Y gate

↑ **Parent:** [Pauli gate](#pauli-gate)

###### Pauli-Z gate

↑ **Parent:** [Pauli gate](#pauli-gate)

###### Phase shift gate

↑ **Parent:** [Single-qubit gate](#single-qubit-gate)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Quantum_logic_gate#Phase_shift_gates)

###### Multi-qubit gate

↑ **Parent:** [Single-qubit gate](#single-qubit-gate)

The most common way to construct [multi-qubit gates](#multi-qubit-gate) is to use [single-qubit gates](#single-qubit-gate) as part of a [controlled quantum gate](#controlled-quantum-gate).

###### Controlled quantum gate

↑ **Parent:** [Multi-qubit gate](#multi-qubit-gate)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Quantum_logic_gate#Controlled_gates)

[Controlled quantum gates](#controlled-quantum-gate) are gates that have two types of input qubits:
- control [qubits](#qubit)
- operand [qubits](#qubit) (terminology made up by [Ciro Santilli](ciro-santilli.md) just now)
These gates can be understood as doing a certain [unitary operation](linear-algebra.md#unitary-matrix) only if the control qubits are enabled or disabled.

The first example to look at is the [CNOT gate](#cnot-gate).

<a id="image-generic-controlled-quantum-gate-symbol"></a>
![](https://upload.wikimedia.org/wikipedia/commons/d/dc/Controlled_gate.svg)

**[Figure 3](#image-generic-controlled-quantum-gate-symbol). Generic controlled quantum gate symbol**. [Source](https://commons.wikimedia.org/wiki/File:Controlled_gate.svg). The black dot means "control qubit", and "U" means an arbitrary [Unitary operation](linear-algebra.md#unitary-matrix).

When the operand has a conventional symbol, e.g. the [Figure 2. "Quantum NOT gate symbol"](#image-quantum-not-gate-symbol) for the [quantum NOT gate](#pauli-x-gate) to form the [CNOT gate](#cnot-gate), that symbol is used in the operand instead.

---

###### Empty circle control qubit notation

↑ **Parent:** [Controlled quantum gate](#controlled-quantum-gate)

Some authors use the convention of:
- filled black circle: conventional [controlled quantum gate](#controlled-quantum-gate), i.e. operate if control qubit is active
- empty (White) circle: operate if control qubit is inactive

###### CNOT gate

↑ **Parent:** [Controlled quantum gate](#controlled-quantum-gate)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Controlled_NOT_gate)

The [CNOT gate](#cnot-gate) is a [controlled quantum gate](#controlled-quantum-gate) that operates on two [qubits](#qubit), flipping the second (operand) [qubit](#qubit) if the first (control) [qubit](#qubit) is set.

This gate is the first example of a [controlled quantum gate](#controlled-quantum-gate) that you should study.

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

**[Figure 4](#image-cnot-gate-symbol). CNOT gate symbol**. [Source](https://commons.wikimedia.org/wiki/File:CNOT_gate.svg). The symbol follow the generic symbol convention for [controlled quantum gates](#controlled-quantum-gate) shown at [Figure 3. "Generic controlled quantum gate symbol"](#image-generic-controlled-quantum-gate-symbol), but replacing the generic "U" with the [Figure 2. "Quantum NOT gate symbol"](#image-quantum-not-gate-symbol).

To understand why the gate is called a CNOT gate, you should think as follows.

First let's produce a generic [quantum state](#quantum-state) vector where the control qubit is certain to be 0.

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

where $x$ and $y$ are two [complex numbers](formalization-of-mathematics.md#complex-number) such that $|x| + |y| = 1.0$

If we operate the [CNOT gate](#cnot-gate) on that state, we obtain:

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

Therefore, in that case, what happened is that the probabilities of $\ket{10}$ and $\ket{11}$ were swapped from $x$ and $y$ to $y$ and $x$ respectively, which is exactly what the [quantum NOT gate](#pauli-x-gate) does.

So from this we understand more concretely what "the gate only operates if the first [qubit](#qubit) is set to one" means.

Now go and study the [Bell state](#bell-state) and understand intuitively how this gate is used to produce it.

###### CZ gate

↑ **Parent:** [Controlled quantum gate](#controlled-quantum-gate)  
🏷️ **Tags:** [Pauli-Z gate](#pauli-z-gate)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Controlled_NOT_gate)

###### Toffoli gate

↑ **Parent:** [Multi-qubit gate](#multi-qubit-gate)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Toffoli_gate)

###### Clifford gates

↑ **Parent:** [Quantum logic gate](#quantum-logic-gate)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Clifford_gates)

This gate set alone is not a set of [universal quantum gates](#universal-quantum-gates).

Notably, circuits containing those gates alone can be fully simulated by classical computers according to the [Gottesman-Knill theorem](#gottesman-knill-theorem), so there's no way they could be universal.

This means that if we add any number of Clifford gates to a quantum circuit, we haven't really increased the complexity of the algorithm, which can be useful as a transformational device.

A popular set of [universal quantum gates](#universal-quantum-gates) derived from [Clifford gates](#clifford-gates) is [Clifford plus T](#clifford-plus-t).

###### Clifford plus T

↑ **Parent:** [Clifford gates](#clifford-gates)  
🏷️ **Tags:** [Universal quantum gates](#universal-quantum-gates)

Set of [quantum logic gate](#quantum-logic-gate) composed of the [Clifford gates](#clifford-gates) plus the [Toffoli gate](#toffoli-gate). It forms a set of [universal quantum gates](#universal-quantum-gates).

###### Gottesman-Knill theorem

↑ **Parent:** [Clifford gates](#clifford-gates)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Gottesman-Knill_theorem)

###### List of quantum logic gates

↑ **Parent:** [Quantum logic gate](#quantum-logic-gate)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/List_of_quantum_logic_gates)

###### Analog quantum computer

↑ **Parent:** [Analog and digital quantum computers](#analog-and-digital-quantum-computers)  
🏷️ **Tags:** [Analog and digital computers](computer.md#analog-and-digital-computers), [Analog computer](computer.md#analog-computer)

- [https://quantumtech.blog/2023/01/17/quantum-computing-with-neutral-atoms/](https://quantumtech.blog/2023/01/17/quantum-computing-with-neutral-atoms/) OK this one hits it:> As Alex Keesling, CEO of [QuEra](#quera) told me, "... whereas in gate-based \[digital\] quantum computing the focus is on the sequence of the gates, in analog quantum processing it's more about the position of the atoms and where you place them so they can mirror real life problems. We arrange the atoms and define the forces that drive them and then measure the result... so it’s a geometric encoding of the problem itself."

  So we understand that it is truly like the [classical computer](#classical-computer) analog vs digital case.
- [https://thequantuminsider.com/2022/06/28/why-analog-neutral-atoms-quantum-computing-is-a-promising-direction-for-early-quantum-advantage](https://thequantuminsider.com/2022/06/28/why-analog-neutral-atoms-quantum-computing-is-a-promising-direction-for-early-quantum-advantage) on [The Quantum Insider](#the-quantum-insider) useless article mostly by [Pasqal](#pasqal)

<a id="video-tensorflow-quantum-by-masoud-mohseni-2020"></a>
**[Video 3](#video-tensorflow-quantum-by-masoud-mohseni-2020). TensorFlow quantum by Masoud Mohseni (2020)** [Source](https://youtu.be/-o9AhIz1uvo?t=295). At the timestamp, Masoud gives a [thought experiment](science.md#thought-experiment) example of the perhaps simplest to understand [analog quantum computer](#analog-quantum-computer): chained [double-slit experiments](quantum-mechanics.md#double-slit-experiment) with carefully calculated distances between slits. Calulating the final propability distribution of that grows exponentially.

###### Continuous-variable quantum information

↑ **Parent:** [Analog quantum computer](#analog-quantum-computer)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Continuous-variable_quantum_information)

TODO synonym to [analog quantum computer](#analog-quantum-computer)?

It is also possible to carry out [quantum computing](quantum-computing.md) without [qubits](#qubit) using processes with a [continuous spectrum](linear-algebra.md#continuous-spectrum-functional-analysis) of measurement.

As of 2020, these approaches seem less developed/promising, but who knows.

These computers can be seen as analogous to classical non-quantum [analog computers](computer.md#analog-computer).

### Quantum computer physical implementation

↑ **Parent:** [Quantum computing hardware](#quantum-computing-hardware)

Lists of the most promising implementations:
- [https://en.wikipedia.org/wiki/Quantum_computing#Physical_realizations](https://en.wikipedia.org/wiki/Quantum_computing#Physical_realizations)
- [https://quantumcomputingreport.com/scorecards/qubit-count/](https://quantumcomputingreport.com/scorecards/qubit-count/), see also: [Section "Quantum computing player"](#quantum-computing-player).

As of 2020, the hottest by far are:
- [superconducting quantum computer](#superconducting-quantum-computing)
- [trapped ion quantum computer](#trapped-ion-quantum-computer)
- [photonic quantum computer](#photonic-quantum-computer)

<a id="video-how-to-build-a-quantum-computer-by-lukas-s-lab-2023"></a>
**[Video 4](#video-how-to-build-a-quantum-computer-by-lukas-s-lab-2023). How To Build A Quantum Computer by Lukas's Lab (2023)** [Source](https://www.youtube.com/watch?v=N06hC1GL1ns). Super quick overview of the main types of [quantum computer physical implementations](#quantum-computer-physical-implementation), so doesn't any much to a quick [Google](google.md).

He says he's going to make a series about it, so then something useful might actually come out. The first one was: [Video 12. "How to Turn Superconductors Into A Quantum Computer by Lukas's Lab (2023)"](#video-how-to-turn-superconductors-into-a-quantum-computer-by-lukas-s-lab-2023), but it is still too basic.

The author's full name is Lukas Baker, [https://www.linkedin.com/in/lukasbaker1331/](https://www.linkedin.com/in/lukasbaker1331/), found with [Google reverse image search](google.md#google-reverse-image-search), even though the LinkedIn image is very slightly different from the YouTube one.

As of 2023 he was a [PhD](education.md#doctor-of-philosophy) student at [NYU](university.md#new-york-university).

---

#### Carbon nanotube spin quantum computer

↑ **Parent:** [Quantum computer physical implementation](#quantum-computer-physical-implementation)

[https://www.ucl.ac.uk/quantum-devices/carbon-nanotube-spin-qubits](https://www.ucl.ac.uk/quantum-devices/carbon-nanotube-spin-qubits)

##### Organization developing carbon nanotube spin quantum computer

↑ **Parent:** [Carbon nanotube spin quantum computer](#carbon-nanotube-spin-quantum-computer)  
🏷️ **Tags:** [Organization developing quantum hardware](#organization-developing-quantum-hardware)

###### C12 Quantum Electronics

↑ **Parent:** [Organization developing carbon nanotube spin quantum computer](#organization-developing-carbon-nanotube-spin-quantum-computer)  
🏷️ **Tags:** [French company](company.md#french-company)

Official website: [https://www.c12qe.com/](https://www.c12qe.com/)

2024 address: 26 rue des Fossés Saint-Jacques, 75005 [Paris](continent.md#paris)

[https://www.c12qe.com/articles/la-deeptech-c12-inaugure-sa-premiere-ligne-de-production-de-puces-quantiques-a-paris](https://www.c12qe.com/articles/la-deeptech-c12-inaugure-sa-premiere-ligne-de-production-de-puces-quantiques-a-paris) explains their choice of address: there is a hill in the [5th arrondissement of Paris](https://ourbigbook.com/go/topic/5th-arrondissement-of-paris), and they have a lab in a deep basement, which helps reduce vibrations from the external environment. Interesting.

[Crunchbase](website.md#crunchbase) entry: [https://www.crunchbase.com/organization/c12-quantum-electronics](https://www.crunchbase.com/organization/c12-quantum-electronics)

Founed by two twin brothers who both studied at [École Polytechnique](ecole-polytechnique.md): [Pierre Desjardins](https://ourbigbook.com/go/topic/pierre-desjardins) and [Matthieu Desjardins](https://ourbigbook.com/go/topic/matthieu-desjardins).

Funding:
- 2024-06-19: [€](social-technology.md#euro)18m
  - [https://techcrunch.com/2024/06/19/c12-the-french-quantum-computing-startup-founded-by-two-twin-brothers-raises-194-million/](https://techcrunch.com/2024/06/19/c12-the-french-quantum-computing-startup-founded-by-two-twin-brothers-raises-194-million/)
  - [https://sifted.eu/articles/c12-quantum-startup-round-news](https://sifted.eu/articles/c12-quantum-startup-round-news)
- 2021: [€](social-technology.md#euro)9m
  - [https://sifted.eu/articles/c12-quantum-startup-round-news](https://sifted.eu/articles/c12-quantum-startup-round-news)

###### UCL Quantum Devices Group

↑ **Parent:** [C12 Quantum Electronics](#c12-quantum-electronics)  
🏷️ **Tags:** [UCL research group](university.md#ucl-research-group)

[https://www.ucl.ac.uk/quantum-devices/carbon-nanotube-spin-qubits](https://www.ucl.ac.uk/quantum-devices/carbon-nanotube-spin-qubits) As mentioned in this link, they collaborate with [C12 Quantum Electronics](#c12-quantum-electronics).

#### Diamond vacancy quantum computer

↑ **Parent:** [Quantum computer physical implementation](#quantum-computer-physical-implementation)

[https://thequantuminsider.com/2022/03/31/5-quantum-computing-companies-working-with-nv-centre-in-diamond-technology/](https://thequantuminsider.com/2022/03/31/5-quantum-computing-companies-working-with-nv-centre-in-diamond-technology/) on [The Quantum Insider](#the-quantum-insider)

[Principal investigator](education.md#principal-investigator): [Mark Buitelaar](https://ourbigbook.com/go/topic/mark-buitelaar)

##### N-V center quantum computer

↑ **Parent:** [Diamond vacancy quantum computer](#diamond-vacancy-quantum-computer)

##### Nitrogen-vacancy center

↑ **Parent:** [Diamond vacancy quantum computer](#diamond-vacancy-quantum-computer)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Nitrogen-vacancy_center)

#### Electron on helium quantum computer

↑ **Parent:** [Quantum computer physical implementation](#quantum-computer-physical-implementation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Electron-on-helium qubit)

##### Organization developing electron on helium quantum computer

↑ **Parent:** [Electron on helium quantum computer](#electron-on-helium-quantum-computer)

###### EeroQ

↑ **Parent:** [Organization developing electron on helium quantum computer](#organization-developing-electron-on-helium-quantum-computer)

[https://eeroq.com/](https://eeroq.com/)

#### Nuclear magnetic resonance quantum computer

↑ **Parent:** [Quantum computer physical implementation](#quantum-computer-physical-implementation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Nuclear_magnetic_resonance_quantum_computer)

##### Organization developing nuclear magnetic resonance quantum computer

↑ **Parent:** [Nuclear magnetic resonance quantum computer](#nuclear-magnetic-resonance-quantum-computer)

###### Silicon Quantum Computing

↑ **Parent:** [Organization developing nuclear magnetic resonance quantum computer](#organization-developing-nuclear-magnetic-resonance-quantum-computer)  
🏷️ **Tags:** [Australian company](company.md#australian-company)

- [https://sqc.com.au/](https://sqc.com.au/)
- [https://www.crunchbase.com/organization/silicon-quantum-computing](https://www.crunchbase.com/organization/silicon-quantum-computing) on [Crunchbase](website.md#crunchbase)

[https://sqc.com.au/2024/02/08/silicon-quantum-computing-demonstrates-high-fidelity-initialisation-of-nuclear-spins-in-a-4-qubit-device/](https://sqc.com.au/2024/02/08/silicon-quantum-computing-demonstrates-high-fidelity-initialisation-of-nuclear-spins-in-a-4-qubit-device/) points to one of their papers: [https://www.nature.com/articles/s41565-023-01596-9](https://www.nature.com/articles/s41565-023-01596-9) High-fidelity initialization and control of electron and [nuclear spins](particle-physics.md#nuclear-magnetic-moment) in a four-qubit register

Their approach seems to be more precisely called: [Kane quantum computer](#kane-quantum-computer) and uses [phosphorus](chemistry.md#phosphorus) embedded in [silicon](chemistry.md#silicon).

They come from the [University of New South Wales](university.md#university-of-new-south-wales).

###### Kane quantum computer

↑ **Parent:** [Silicon Quantum Computing](#silicon-quantum-computing)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Kane_quantum_computer)

![](https://upload.wikimedia.org/wikipedia/commons/1/15/Kane_QC.png)

**[Figure 5](#_445)** [Source](https://commons.wikimedia.org/wiki/File:Kane_QC.png).

Through the company [Silicon Quantum Computing](#silicon-quantum-computing), this has been [Australia](continent.md#australia)'s national quantum computing focus.

###### Diraq

↑ **Parent:** [Silicon Quantum Computing](#silicon-quantum-computing)  
🏷️ **Tags:** [Australian company](company.md#australian-company)

Another [Australian company](company.md#australian-company) and using a similar approach as [Silicon Quantum Computing](#silicon-quantum-computing):
- [https://diraq.com/](https://diraq.com/)
- [https://www.linkedin.com/company/diraq/?originalSubdomain=au](https://www.linkedin.com/company/diraq/?originalSubdomain=au)
Some coverage at: [https://www.afr.com/technology/start-up-says-it-will-have-a-quantum-computer-by-2028-20240219-p5f64k](https://www.afr.com/technology/start-up-says-it-will-have-a-quantum-computer-by-2028-20240219-p5f64k)

#### Quantum dot quantum computer

↑ **Parent:** [Quantum computer physical implementation](#quantum-computer-physical-implementation)  
🏷️ **Tags:** [Quantum dot](condensed-matter-physics.md#quantum-dot)

##### Organization developing quantum dot quantum computer

↑ **Parent:** [Quantum dot quantum computer](#quantum-dot-quantum-computer)

###### Quantum Motion

↑ **Parent:** [Organization developing quantum dot quantum computer](#organization-developing-quantum-dot-quantum-computer)

- [https://www.crunchbase.com/organization/quantum-motion-technologies](https://www.crunchbase.com/organization/quantum-motion-technologies)
- [https://quantummotion.tech/](https://quantummotion.tech/)

Funding:
- 2023: [£](social-technology.md#pound-sterling)42m (~[$](social-technology.md#dollar)50m) [https://www.uktech.news/deep-tech/quantum-motion-raises-42m-20230221](https://www.uktech.news/deep-tech/quantum-motion-raises-42m-20230221)

##### Intel quantum computer

↑ **Parent:** [Quantum dot quantum computer](#quantum-dot-quantum-computer)

<a id="video-architecture-all-access-quantum-computing-by-james-clarke-2021"></a>
**[Video 5](#video-architecture-all-access-quantum-computing-by-james-clarke-2021). Architecture All Access: Quantum Computing by James Clarke (2021)** [Source](https://www.youtube.com/watch?v=-5fKVn1GR9Y).

#### Superconducting quantum computing

↑ **Parent:** [Quantum computer physical implementation](#quantum-computer-physical-implementation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Superconducting_quantum_computing)

Based on the [Josephson effect](condensed-matter-physics.md#josephson-effect). Yet another application of that phenomenal phenomena!

Philosophically, [superconducting qubits are good because superconductivity is macroscopic](#superconducting-qubits-are-good-because-superconductivity-is-macroscopic).

It is fun to see that the representation of information in the QC basically uses an [LC circuit](electronics.md#lc-circuit), which is a very classical resonator circuit.

As mentioned at [https://en.wikipedia.org/wiki/Superconducting_quantum_computing#Qubit_archetypes](https://en.wikipedia.org/wiki/Superconducting_quantum_computing#Qubit_archetypes) there are actually a few different types of superconducting qubits:
- flux
- charge
- phase

and hybridizations of those such as:
- [transmon](#transmon)

Input:
- [microwave](photon.md#microwave) radiation to excite circuit, or do nothing and wait for it to fall to 0 spontaneously
- interaction: TODO
- readout: TODO

<a id="video-quantum-computing-with-superconducting-qubits-by-alexandre-blais-2012"></a>
**[Video 6](#video-quantum-computing-with-superconducting-qubits-by-alexandre-blais-2012). Quantum Computing with Superconducting Qubits by Alexandre Blais (2012)** [Source](http://youtube.com/watch?v=t5nxusm_Umk). - [https://youtu.be/t5nxusm_Umk?t=176](https://youtu.be/t5nxusm_Umk?t=176) [quantum computing is hard because we want long coherence but fast control](#quantum-computing-is-hard-because-we-want-long-coherence-but-fast-control)
- [https://youtu.be/t5nxusm_Umk?t=784](https://youtu.be/t5nxusm_Umk?t=784) [superconducting quantum computer need non-linear components](#superconducting-quantum-computer-need-non-linear-components)

---

<a id="video-quantum-transport-lecture-16-superconducting-qubits-by-sergey-frolov-2013"></a>
**[Video 7](#video-quantum-transport-lecture-16-superconducting-qubits-by-sergey-frolov-2013). Quantum Transport, Lecture 16: Superconducting qubits by Sergey Frolov (2013)** [Source](http://youtube.com/watch?v=Kz6mhh1A_mU). [https://youtu.be/Kz6mhh1A_mU?t=1171](https://youtu.be/Kz6mhh1A_mU?t=1171) describes several possible realizations: charge, flux, charge/flux and phase.

<a id="video-building-a-quantum-computer-with-superconducting-qubits-by-daniel-sank-2019"></a>
**[Video 8](#video-building-a-quantum-computer-with-superconducting-qubits-by-daniel-sank-2019). Building a quantum computer with superconducting qubits by Daniel Sank (2019)** [Source](https://www.youtube.com/watch?v=uPw9nkJAwDY). Daniel wears a "Google SB" t-shirt, which either means [shabi](linguistics.md#shabi) in [Chinese](linguistics.md#chinese-language), or [Santa Barbara](united-states.md#santa-barbara). [Google Quantum AI](#google-quantum-ai) is based in [Santa Barbara](united-states.md#santa-barbara), with links to [UCSB](university.md#university-of-california-santa-barbara).
- [https://youtu.be/uPw9nkJAwDY?t=293](https://youtu.be/uPw9nkJAwDY?t=293) [superconducting qubits are good because superconductivity is macroscopic](#superconducting-qubits-are-good-because-superconductivity-is-macroscopic). Explains how in non superconducting metal, each electron moves separatelly, and can hit atoms and leak vibration/photos, which lead to observation and quantum error
- [https://youtu.be/uPw9nkJAwDY?t=429](https://youtu.be/uPw9nkJAwDY?t=429) made of [aluminium](chemistry.md#aluminium)
- [https://youtu.be/uPw9nkJAwDY?t=432](https://youtu.be/uPw9nkJAwDY?t=432) shows the [circuit diagram](electronics.md#circuit-diagram), and notes that the thing is basically a [LC circuit](electronics.md#lc-circuit)
  ```
  +-----+
  |     |
  |   +-+-+
  |   |   |
  C   X   X
  |   |   |
  |   +-+-+
  |     |
  +-----+
  ```

  using the newly created just now [Ciro's ASCII art circuit diagram notation](electronics.md#ciro-s-ascii-art-circuit-diagram-notation). Note that the block on the right is a [SQUID device](condensed-matter-physics.md#squid-device).
- [https://youtu.be/uPw9nkJAwDY?t=471](https://youtu.be/uPw9nkJAwDY?t=471) mentions that the frequency between states 0 and 1 is chosen to be 6 GHz:
  - higher frequencies would be harder/more expensive to generate
  - lower frequencies would mean less energy according to the [Planck relation](quantum-mechanics.md#planck-einstein-relation). And less energy means that thermal energy would matter more, and introduce more noise.

    6 GHz is about $6^9 \times h = 6 \times 10^9 \times 6.62 \times 10^{-34} \approx 4\e{-24} J$

    From the definition of the [Boltzmann constant](statistical-physics.md#boltzmann-constant), the temperature which has that average energe of particles is of the order of:

    $$
    T = E/k_b = 4\e{-24}/1.38\e{-23} \approx 0.3K
    $$

  This explains why we need to go to much lower temperatures than simply the [superconducting temperature of aluminum](chemistry.md#superconducting-temperature-of-aluminum)!

---

<a id="video-a-brief-history-of-superconducting-quantum-computing-by-steven-girvin-2021"></a>
**[Video 9](#video-a-brief-history-of-superconducting-quantum-computing-by-steven-girvin-2021). A Brief History of Superconducting quantum computing by Steven Girvin (2021)** [Source](https://www.youtube.com/watch?v=xjlGL4Mvq7A). - [https://youtu.be/xjlGL4Mvq7A?t=138](https://youtu.be/xjlGL4Mvq7A?t=138) [superconducting quantum computer need non-linear components](#superconducting-quantum-computer-need-non-linear-components) (too brief if you don't know what he means in advance)
- [https://youtu.be/xjlGL4Mvq7A?t=169](https://youtu.be/xjlGL4Mvq7A?t=169) [quantum computing is hard because we want long coherence but fast control](#quantum-computing-is-hard-because-we-want-long-coherence-but-fast-control)

---

<a id="video-superconducting-qubits-i-part-1-by-zlatko-minev-2020"></a>
**[Video 10](#video-superconducting-qubits-i-part-1-by-zlatko-minev-2020). Superconducting Qubits I Part 1 by Zlatko Minev (2020)** [Source](https://www.youtube.com/watch?v=eZJjQGu85Ps). The Q&A in the middle of talking is a bit annoying.


- [https://youtu.be/eZJjQGu85Ps?t=2443](https://youtu.be/eZJjQGu85Ps?t=2443) the first actually useful part, shows a [transmon](#transmon) diagram with some useful formulas on it

---

<a id="video-superconducting-qubits-i-part-2-by-zlatko-minev-2020"></a>
**[Video 11](#video-superconducting-qubits-i-part-2-by-zlatko-minev-2020). Superconducting Qubits I Part 2 by Zlatko Minev (2020)** [Source](https://www.youtube.com/watch?v=SDiiFOham6Y).

<a id="video-how-to-turn-superconductors-into-a-quantum-computer-by-lukas-s-lab-2023"></a>
**[Video 12](#video-how-to-turn-superconductors-into-a-quantum-computer-by-lukas-s-lab-2023). How to Turn Superconductors Into A Quantum Computer by Lukas's Lab (2023)** [Source](https://www.youtube.com/watch?v=xsdleM-f0i8). This video is just the introduction, too basic. But if he goes through with the followups he promisses, then something might actually come out of it.

##### Superconducting quantum computer need non-linear components

↑ **Parent:** [Superconducting quantum computing](#superconducting-quantum-computing)

Non-linearity is needed otherwise the input energy would just make the state go to higher and higher energy levels, e.g. from 1 to 2. But we only want to use levels 0 and 1.

The way this is modelled in by starting from a pure [LC circuit](electronics.md#lc-circuit), which is an harmonic oscillator, see also [quantum LC circuit](quantum-mechanics.md#quantum-lc-circuit), and then replacing the linear [inductor](electronics.md#inductor) with a [SQUID device](condensed-matter-physics.md#squid-device), e.g. mentioned at: [https://youtu.be/eZJjQGu85Ps?t=1655](https://youtu.be/eZJjQGu85Ps?t=1655) [Video 10. "Superconducting Qubits I Part 1 by Zlatko Minev (2020)"](#video-superconducting-qubits-i-part-1-by-zlatko-minev-2020).

##### Superconducting qubit

↑ **Parent:** [Superconducting quantum computing](#superconducting-quantum-computing)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Superconducting_qubit)

###### Pros and cons of superconducting qubits

↑ **Parent:** [Superconducting qubit](#superconducting-qubit)

###### Con of superconducting qubits

↑ **Parent:** [Pros and cons of superconducting qubits](#pros-and-cons-of-superconducting-qubits)

- requires intense refrigeration to 15mK in [dilution refrigerator](statistical-physics.md#dilution-refrigerator). Note that this is much lower than the actual [superconducting temperature](condensed-matter-physics.md#superconducting-temperature) of the metal, we have to go even lower to reduce noise enough, see e.g. [https://youtu.be/uPw9nkJAwDY?t=471](https://youtu.be/uPw9nkJAwDY?t=471) from [Video 8. "Building a quantum computer with superconducting qubits by Daniel Sank (2019)"](#video-building-a-quantum-computer-with-superconducting-qubits-by-daniel-sank-2019)
- less connectivity, normally limited to 4 nearest neighbours, or maybe 6 for 3D approaches, e.g. compared to [trapped ion quantum computers](#trapped-ion-quantum-computer), where each trapped ion can be entangled with every other on the same chip

###### Superconducting qubits are bad because it is harder to ensure that they are all the same

↑ **Parent:** [Con of superconducting qubits](#con-of-superconducting-qubits)

This is unlike atomic systems like [trapped ion quantum computers](#trapped-ion-quantum-computer), where each atom is necessarily exactly the same as the other.

###### Pro of superconducting qubits

↑ **Parent:** [Pros and cons of superconducting qubits](#pros-and-cons-of-superconducting-qubits)

###### Superconducting qubits are good because superconductivity is macroscopic

↑ **Parent:** [Pro of superconducting qubits](#pro-of-superconducting-qubits)

Superconducting qubits are regarded as promising because superconductivity is a [macroscopic quantum phenomena](quantum-mechanics.md#macroscopic-quantum-phenomena) of [Bose Einstein condensation](condensed-matter-physics.md#bose-einstein-condensate), and so as a macroscopic phenomena, it is easier to control and observe.

This is mentioned e.g. in this relatively early: [https://physicsworld.com/a/superconducting-quantum-bits/](https://physicsworld.com/a/superconducting-quantum-bits/). While most quantum phenomena is observed at the atomic scale, [superconducting qubits](#superconducting-qubit) are micrometer scale, which is huge!

> Physicists are comfortable with the use of quantum mechanics to describe atomic and subatomic particles. However, in recent years we have discovered that micron-sized objects that have been produced using standard semiconductor-fabrication techniques – objects that are small on everyday scales but large compared with atoms – can also behave as quantum particles.

###### Superconducting qubits are bad because of fabrication variation

↑ **Parent:** [Pro of superconducting qubits](#pro-of-superconducting-qubits)

Atom-based [qubits](#qubit) like [trapped ion quantum computers](#trapped-ion-quantum-computer) have parameters fixed by the laws of physics.

However superconducting qubits have a limit on how precise their parameters can be set based on how well we can fabricate devices. This may require per-device characterisation.

###### Superconducting qubit type

↑ **Parent:** [Superconducting qubit](#superconducting-qubit)

###### Flux qubit

↑ **Parent:** [Superconducting qubit type](#superconducting-qubit-type)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Flux_qubit)

In [Ciro's ASCII art circuit diagram notation](electronics.md#ciro-s-ascii-art-circuit-diagram-notation), it is a loop with three [Josephson junctions](condensed-matter-physics.md#josephson-junction):
```
+----X-----+
|          |
|          |
|          |
+--X----X--+
```

![](https://upload.wikimedia.org/wikipedia/en/0/04/Flux_Qubit_-_Holloway.jpg)

<a id="video-superconducting-qubit-by-ntt-scl-2015"></a>
**[Video 13](#video-superconducting-qubit-by-ntt-scl-2015). Superconducting Qubit by NTT SCL (2015)** [Source](https://www.youtube.com/watch?v=daQJMwvxC_U). Offers an interesting interpretation of [superposition](quantum-mechanics.md#quantum-superposition) in that type of device (TODO precise name, seems to be a [flux qubit](#flux-qubit)): current going clockwise or current going counter clockwise at the same time. [https://youtu.be/xjlGL4Mvq7A?t=1348](https://youtu.be/xjlGL4Mvq7A?t=1348) clarifies that this is just one of the types of qubits, and that it was developed by [Hans Mooij](https://ourbigbook.com/go/topic/hans-mooij) et. al., with a proposal in 1999 and experiments in 2000. The other type is dual to this one, and the [superposition](quantum-mechanics.md#quantum-superposition) of the other type is between N and N + 1 copper pairs stored in a box.

Their circuit is a loop with three [Josephson junctions](condensed-matter-physics.md#josephson-junction), in [Ciro's ASCII art circuit diagram notation](electronics.md#ciro-s-ascii-art-circuit-diagram-notation):
```
+----X-----+
|          |
|          |
|          |
+--X----X--+
```

They name the clockwise and counter clockwise states $\ket{L}$ and $\ket{R}$ (named for Left and Right).

When half the [magnetic flux quantum](condensed-matter-physics.md#magnetic-flux-quantum) is applied as [microwaves](photon.md#microwave), this produces the ground state:

$$
\ket{0} = \ket{L} + \ket{R}
$$

where $L$ and $R$ cancel each other out. And the first excited state $\ket{1}$ is:

$$
\ket{0} = \ket{L} - \ket{R}
$$

Then he mentions that:
- to go from 0 to 1, they apply the difference in energy
- if the duration is reduced by half, it creates a superposition of $\ket{0} + \ket{1}$.

---

###### Transmon

↑ **Parent:** [Superconducting qubit type](#superconducting-qubit-type)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Transmon)

Used e.g. in the [Sycamore processor](#sycamore-processor).

The most basic type of transmon is in [Ciro's ASCII art circuit diagram notation](electronics.md#ciro-s-ascii-art-circuit-diagram-notation), an [LC circuit](electronics.md#lc-circuit) e.g. as mentioned at [https://youtu.be/cb_f9KpYipk?t=180](https://youtu.be/cb_f9KpYipk?t=180) from [Video 16. "The transmon qubit by Leo Di Carlo (2018)"](#video-the-transmon-qubit-by-leo-di-carlo-2018):
```
+----------+
| Island 1 |
+----------+
   |   |
   X   C
   |   |
+----------+
| Island 2 |
+----------+
```

[https://youtu.be/eZJjQGu85Ps?t=2443](https://youtu.be/eZJjQGu85Ps?t=2443) from [Video 10. "Superconducting Qubits I Part 1 by Zlatko Minev (2020)"](#video-superconducting-qubits-i-part-1-by-zlatko-minev-2020) describes a (possibly simplified) physical model of it, as two superconducting metal islands linked up by a [Josephson junction](condensed-matter-physics.md#josephson-junction) marked as `X` in the diagram as per-[Ciro's ASCII art circuit diagram notation](electronics.md#ciro-s-ascii-art-circuit-diagram-notation):
```
+-------+       +-------+
|       |       |       |
| Q_1() |---X---| Q_2() |
|       |       |       |
+-------+       +-------+
```
The circuit is then analogous to a [LC circuit](electronics.md#lc-circuit), with the islands being the [capacitor](electronics.md#capacitor). The [Josephson junction](condensed-matter-physics.md#josephson-junction) functions as a non-linear [inductor](electronics.md#inductor).

Others define it with a [SQUID device](condensed-matter-physics.md#squid-device) instead: [https://youtu.be/cb_f9KpYipk?t=328](https://youtu.be/cb_f9KpYipk?t=328) from [Video 16. "The transmon qubit by Leo Di Carlo (2018)"](#video-the-transmon-qubit-by-leo-di-carlo-2018). He mentions that this allows tuning the inductive element without creating a new device.

<a id="video-the-superconducting-transmon-qubit-as-a-microwave-resonator-by-daniel-sank-2021"></a>
**[Video 14](#video-the-superconducting-transmon-qubit-as-a-microwave-resonator-by-daniel-sank-2021). The superconducting transmon qubit as a microwave resonator by Daniel Sank (2021)** [Source](https://www.youtube.com/watch?v=dKTNBN99xLw).

<a id="video-calibration-of-transmon-superconducting-qubits-by-stefan-titus-2021"></a>
**[Video 15](#video-calibration-of-transmon-superconducting-qubits-by-stefan-titus-2021). Calibration of Transmon Superconducting Qubits by Stefan Titus (2021)** [Source](https://www.youtube.com/watch?v=5ggYJJjlw8o). Possibly this [Keysight](electronics.md#keysight) which would make sense.

###### An Introduction to the Transmon Qubit for Electromagnetic Engineers

↑ **Parent:** [Transmon](#transmon)  
🏷️ **Tags:** [Review article](education.md#review-article)

[https://arxiv.org/abs/2106.11352](https://arxiv.org/abs/2106.11352)

This is a good [review article](education.md#review-article).

###### Rabi cycle

↑ **Parent:** [Transmon](#transmon)

###### The Hardware of a Quantum Computer by TU Delft

↑ **Parent:** [Transmon](#transmon)  
🏷️ **Tags:** [TU Delft](university.md#delft-university-of-technology)

[EdX](website.md#edx) course. Meh! Just give me the [YouTube](website.md#youtube) list!!

But seriously, this is a valuable little list.

The course is basically exclusively about [transmons](#transmon).

<a id="video-the-transmon-qubit-by-leo-di-carlo-2018"></a>
**[Video 16](#video-the-transmon-qubit-by-leo-di-carlo-2018). The transmon qubit by Leo Di Carlo (2018)** [Source](https://www.youtube.com/watch?v=cb_f9KpYipk). Via [QuTech Academy](#qutech-academy).

<a id="video-circuit-qed-by-leo-di-carlo-2018"></a>
**[Video 17](#video-circuit-qed-by-leo-di-carlo-2018). Circuit QED by Leo Di Carlo (2018)** [Source](https://www.youtube.com/watch?v=JmnpcWEuMJY). Via [QuTech Academy](#qutech-academy).

<a id="video-measurements-on-transmon-qubits-by-niels-bultink-2018"></a>
**[Video 18](#video-measurements-on-transmon-qubits-by-niels-bultink-2018). Measurements on transmon qubits by Niels Bultink (2018)** [Source](https://www.youtube.com/watch?v=KDANvtOkEc4). Via [QuTech Academy](#qutech-academy). I wish someone would show some actual equipment running! But this is of interest.

<a id="video-single-qubit-gate-by-brian-taraskinki-2018"></a>
**[Video 19](#video-single-qubit-gate-by-brian-taraskinki-2018). Single-qubit gate by Brian Taraskinki (2018)** [Source](https://www.youtube.com/watch?v=_MfABBLtBd0). Good video! Basically you make a phase rotation by controlling the envelope of a pulse.

<a id="video-two-qubit-gates-by-adriaan-rol-2018"></a>
**[Video 20](#video-two-qubit-gates-by-adriaan-rol-2018). Two qubit gates by Adriaan Rol (2018)** [Source](https://www.youtube.com/watch?v=vwjlEdwi2LU).

<a id="video-assembling-a-quantum-processor-by-leo-di-carlo-2018"></a>
**[Video 21](#video-assembling-a-quantum-processor-by-leo-di-carlo-2018). Assembling a Quantum Processor by Leo Di Carlo (2018)** [Source](https://www.youtube.com/watch?v=BA5thMaxkyY). Via [QuTech Academy](#qutech-academy).

##### Organization developing superconducting quantum computer

↑ **Parent:** [Superconducting quantum computing](#superconducting-quantum-computing)  
🏷️ **Tags:** [Organization developing quantum hardware](#organization-developing-quantum-hardware)

<h6 id="alice-and-bob">Alice&amp;Bob</h6>

↑ **Parent:** [Organization developing superconducting quantum computer](#organization-developing-superconducting-quantum-computer)  
🏷️ **Tags:** [French company](company.md#french-company)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Alice&Bob)

- [https://alice-bob.com](https://alice-bob.com)
- [https://www.crunchbase.com/organization/alice-bob](https://www.crunchbase.com/organization/alice-bob)

Funding rounds:
- January 2025: 100M Euros[https://alice-bob.com/newsroom/alice-bob-100m-series-b-fundraising-press-release/](https://alice-bob.com/newsroom/alice-bob-100m-series-b-fundraising-press-release/)
- March 2022: 27M Euros

About their [qubit](#qubit):
- [https://alice-bob.com/2023/02/15/computing-256-bit-elliptic-curve-logarithm-in-9-hours-with-126133-cat-qubits/](https://alice-bob.com/2023/02/15/computing-256-bit-elliptic-curve-logarithm-in-9-hours-with-126133-cat-qubits/) Computing 256-bit elliptic curve logarithm in 9 hours with 126,133 cat qubits (2023). This describes their "[cat qubit](#cat-qubit)".

<a id="video-cat-qubits-and-ldpc-codes-a-new-step-towards-quantum-error-correction-by-alice-and-bob"></a>
**[Video 22](#video-cat-qubits-and-ldpc-codes-a-new-step-towards-quantum-error-correction-by-alice-and-bob). Cat Qubits and LDPC Codes, a New Step Towards Quantum Error Correction by Alice&Bob.** [Source](https://www.youtube.com/watch?v=nI0Yg-QRAns).

<a id="video-behind-the-tech-cryostats-by-alice-and-bob"></a>
**[Video 23](#video-behind-the-tech-cryostats-by-alice-and-bob). Behind The Tech : Cryostats by Alice&Bob.** [Source](https://www.youtube.com/watch?v=QbMVJdbHGrs). Showcasing their [Bluefors](statistical-physics.md#bluefors) [dilution refrigerators](statistical-physics.md#dilution-refrigerator). They are named after [Asterix](https://ourbigbook.com/go/topic/asterix) characters.

###### Cat qubit

↑ **Parent:** [Alice&Bob](#alice-and-bob)

###### Google Quantum AI

↑ **Parent:** [Organization developing superconducting quantum computer](#organization-developing-superconducting-quantum-computer)  
🏷️ **Tags:** [Google project](google.md#google-project)

- [https://quantumai.google/](https://quantumai.google/)
- [https://quantumai.google/hardware/our-lab](https://quantumai.google/hardware/our-lab)

[Google](google.md)'s quantum hardware/software effort.

The "AI" part is just prerequisite buzzword of the [AI boom](artificial-intelligence.md#ai-boom) era for any project and completely bullshit.

According to job postings such as: [https://archive.ph/wip/Fdgsv](https://archive.ph/wip/Fdgsv) their center is in Goleta, [California](united-states.md#california), near [Santa Barbara](united-states.md#santa-barbara). Though Google tends to promote it more as Santa Barbara, see e.g. Daniel's t-shirt at [Video 8. "Building a quantum computer with superconducting qubits by Daniel Sank (2019)"](#video-building-a-quantum-computer-with-superconducting-qubits-by-daniel-sank-2019).

<a id="video-control-of-transmon-qubits-using-a-cryogenic-cmos-integrated-circuit-quantumcasts-by-google-2020"></a>
**[Video 24](#video-control-of-transmon-qubits-using-a-cryogenic-cmos-integrated-circuit-quantumcasts-by-google-2020). Control of transmon qubits using a cryogenic CMOS integrated circuit (QuantumCasts) by Google (2020)** [Source](https://youtube.com/watch?v=VA2HEUmkrKo). Fantastic video, good photos of the [Google Quantum AI](#google-quantum-ai) setup!

###### Google Quantum Campus

↑ **Parent:** [Google Quantum AI](#google-quantum-ai)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Google_Quantum_Campus)

Built 2021. TODO address. Located in [Santa Barbara](united-states.md#santa-barbara), which has long been the epycenter of [Google](google.md)'s AI efforts. Apparently contains fabrication facilities.

Announcement: [https://blog.google/technology/ai/unveiling-our-new-quantum-ai-campus/](https://blog.google/technology/ai/unveiling-our-new-quantum-ai-campus/)

<img src="https://web.archive.org/web/20241118231832im_/https://storage.googleapis.com/gweb-uniblog-publish-prod/images/1_294_R01_1.width-1200.format-webp.webp" alt="" height="500">

**[Figure 6](#_559)** [Source](https://quantumai.google/learn/lab).

<a id="video-take-a-tour-of-google-s-quantum-ai-lab-by-google-quantum-ai"></a>
**[Video 25](#video-take-a-tour-of-google-s-quantum-ai-lab-by-google-quantum-ai). Take a tour of Google's Quantum AI Lab by Google Quantum AI.** [Source](https://www.youtube.com/watch?v=Ay8qp92V33s). 2023

###### Google Quantum AI employee

↑ **Parent:** [Google Quantum AI](#google-quantum-ai)

###### Daniel Sank

↑ **Parent:** [Google Quantum AI employee](#google-quantum-ai-employee)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Daniel_Sank)

- [https://www.linkedin.com/in/daniel-sank-a3679a92/](https://www.linkedin.com/in/daniel-sank-a3679a92/)
- [https://github.com/DanielSank](https://github.com/DanielSank)

Cool dude. Uses [Stack Exchange](stack-overflow.md#stack-exchange): [https://physics.stackexchange.com/users/31790/danielsank](https://physics.stackexchange.com/users/31790/danielsank)

Started at [Google Quantum AI](#google-quantum-ai) in 2014.

Has his [LaTeX](computer.md#latex) notes at: [https://github.com/DanielSank/theory](https://github.com/DanielSank/theory). One day he will convert to [OurBigBook.com](ourbigbook-com.md). Interesting to see that he is able to continue his notes despite being at Google.

###### Julian Kelly

↑ **Parent:** [Google Quantum AI employee](#google-quantum-ai-employee)

- [https://www.linkedin.com/in/julianskelly/](https://www.linkedin.com/in/julianskelly/)
- [https://research.google/people/105027/](https://research.google/people/105027/)

Timeline:
- 2015: joined [Google](google.md) as a [Google Quantum AI employee](#google-quantum-ai-employee)
- 2010: [UCSB](university.md#university-of-california-santa-barbara) Physics [PhD](education.md#doctor-of-philosophy). His thesis was "Fault-tolerant [superconducting qubits](#superconducting-qubit)" and the PDF can be downloaded from: [https://alexandria.ucsb.edu/lib/ark:/48907/f3b56gwb](https://alexandria.ucsb.edu/lib/ark:/48907/f3b56gwb).
- 2006: [UCSB](university.md#university-of-california-santa-barbara) Physics undergrad. In 2008 he joined [John Martinis](#john-m-martinis)' lab during his undergrad itself.
He went pretty much in a straight line into the [quantum computing](quantum-computing.md) boom! Well done.

![](https://web.archive.org/web/20241210115504if_/https://media.licdn.com/dms/image/v2/C5603AQFihwLgo2lsAg/profile-displayphoto-shrink_200_200/profile-displayphoto-shrink_200_200/0/1629342596573?e=1739404800&amp;v=beta&amp;t=s2XXlNtkmRNrnlKNTPy8PI6VuyW--8-JAl7YS1iY-e8)

**[Figure 7](#_574)** [Source](https://www.linkedin.com/in/julianskelly/).

###### John M. Martinis

↑ **Parent:** [Google Quantum AI employee](#google-quantum-ai-employee)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/John_M._Martinis)

Timeline:
- 2020: left Google after he was demoted apparently, and joined [Silicon Quantum Computing](#silicon-quantum-computing).
- 2014: he and the entire lab were hired by [Google](google.md)

<img src="https://web.archive.org/web/20241206185437im_/https://media.wired.com/photos/593245d858b0d64bb35d09c8/master/w_1920,c_limit/Martinis1.jpg" alt="" height="600">

**[Figure 8](#_579)** [Source](https://www.wired.com/2014/09/martinis/).

###### Google Quantum AI hardware

↑ **Parent:** [Google Quantum AI](#google-quantum-ai)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Google_Quantum_AI_hardware)

###### Sycamore processor

↑ **Parent:** [Google Quantum AI hardware](#google-quantum-ai-hardware)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Sycamore_processor)

This is a good read: [https://quantumai.google/hardware/datasheet/weber.pdf](https://quantumai.google/hardware/datasheet/weber.pdf) May 14, 2021. Their topology is so weird, not just a rectangle, one wonders why! You get different error rates in different qubits, it's mad.

<a id="image-google-sycamore-weber-quantum-computer-connectivity-graph"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/Google_Sycamore_Weber_quantum_computer_connectivity_graph.png)

**[Figure 9](#image-google-sycamore-weber-quantum-computer-connectivity-graph). Google Sycamore Weber quantum computer connectivity graph**. Weber is a specific processor of the Sycamore family. From this we see it clearly that qubits are connected to at most 4 other qubits, and that the full topology is not just a simple rectangle.

###### Willow (quantum computer)

↑ **Parent:** [Google Quantum AI hardware](#google-quantum-ai-hardware)

<a id="video-meet-willow-quantum-computer-our-state-of-the-art-quantum-chip-by-google-quantum-ai"></a>
**[Video 26](#video-meet-willow-quantum-computer-our-state-of-the-art-quantum-chip-by-google-quantum-ai). Meet Willow, our state-of-the-art quantum chip by Google Quantum AI.** [Source](https://www.youtube.com/watch?v=W7ppd_RY-UE). 2024 public presentation of their then new chip.

Related blog post: [https://blog.google/technology/research/google-willow-quantum-chip/](https://blog.google/technology/research/google-willow-quantum-chip/)

---

###### IBM Quantum Computing

↑ **Parent:** [Organization developing superconducting quantum computer](#organization-developing-superconducting-quantum-computer)  
🏷️ **Tags:** [IBM](computer.md#ibm)

The term "IBM Q" has been used in some promotional material as of 2020, e.g.: [https://www.ibm.com/mysupport/s/topic/0TO50000000227pGAA/ibm-q-quantum-computing?language=en_US](https://www.ibm.com/mysupport/s/topic/0TO50000000227pGAA/ibm-q-quantum-computing?language=en_US) though the fuller form "IBM Quantum Computing" is somewhat more widely used.

They also internally named an division as "IBM Q": [https://sg.news.yahoo.com/ibm-thinks-ready-turn-quantum-050100574.html](https://sg.news.yahoo.com/ibm-thinks-ready-turn-quantum-050100574.html)

###### IBM quantum computer

↑ **Parent:** [IBM Quantum Computing](#ibm-quantum-computing)

###### IQM

↑ **Parent:** [Organization developing superconducting quantum computer](#organization-developing-superconducting-quantum-computer)

Homepage: [https://meetiqm.com/](https://meetiqm.com/)

###### OpenSuperQ

↑ **Parent:** [Organization developing superconducting quantum computer](#organization-developing-superconducting-quantum-computer)

[Open source](software.md#open-source-software) superconducting quantum computer hardware design!

<a id="video-opensuperq-intro-by-quantum-flagship-2021"></a>
**[Video 27](#video-opensuperq-intro-by-quantum-flagship-2021). OpenSuperQ intro by Quantum Flagship (2021)** [Source](https://www.youtube.com/watch?v=2cU2PA4Q0Bw). - [https://youtu.be/2cU2PA4Q0Bw?t=61](https://youtu.be/2cU2PA4Q0Bw?t=61): [Dilution refrigerator](statistical-physics.md#dilution-refrigerator) by [Bluefors](statistical-physics.md#bluefors)

---

###### Oxford Quantum Circuits

↑ **Parent:** [Organization developing superconducting quantum computer](#organization-developing-superconducting-quantum-computer)  
🏷️ **Tags:** [British company](company.md#british-company), [University of Oxford spinout company](university-of-oxford.md#university-of-oxford-spinout-company)

[https://oxfordquantumcircuits.com/](https://oxfordquantumcircuits.com/)

Their main innovation seems to be their 3D design which they call "Coaxmon".

Funding:
- 2023: [$](social-technology.md#dollar)1m (869,000 pounds) for [Japan](japan.md) expansion: [https://www.uktech.news/deep-tech/oqc-funding-japan-20230203](https://www.uktech.news/deep-tech/oqc-funding-japan-20230203)
- 2022: [$](social-technology.md#dollar)47m (38M pounds) [https://techcrunch.com/2022/07/04/uks-oxford-quantum-circuits-snaps-up-47m-for-quantum-computing-as-a-service/](https://techcrunch.com/2022/07/04/uks-oxford-quantum-circuits-snaps-up-47m-for-quantum-computing-as-a-service/)
- 2017: [$](social-technology.md#dollar)2.7m [https://globalventuring.com/university/oxford-quantum-calculates-2-7m/](https://globalventuring.com/university/oxford-quantum-calculates-2-7m/)

<a id="video-the-coaxmon-by-oxford-quantum-circuits-2022"></a>
**[Video 28](#video-the-coaxmon-by-oxford-quantum-circuits-2022). The Coaxmon by Oxford Quantum Circuits (2022)** [Source](https://www.youtube.com/watch?v=dPtsOmdofnA).

###### Ilana Wisby

↑ **Parent:** [Oxford Quantum Circuits](#oxford-quantum-circuits)

Founding CEO of [Oxford Quantum Circuits](#oxford-quantum-circuits).

As mentioned at [https://www.investmentmonitor.ai/tech/innovation/in-conversation-with-oxford-quantum-circuits-ilana-wisby](https://www.investmentmonitor.ai/tech/innovation/in-conversation-with-oxford-quantum-circuits-ilana-wisby) she is not the original tech person:

> she was finally headhunted by Oxford Science and Innovation to become the founding CEO of OQC. The company was spun out of Oxford University's physics department in 2017, at which point Wisby was handed "a laptop and a patent".

Did they mean [Oxford Sciences Enterprises](university-of-oxford.md#oxford-sciences-enterprises)? There's nothing called "Oxford Science and Innovation" on [Google](google.md). Yes, it is just a typo [https://oxfordscienceenterprises.com/news/meet-the-founder-ilana-wisby-ceo-of-oxford-quantum-circuits/](https://oxfordscienceenterprises.com/news/meet-the-founder-ilana-wisby-ceo-of-oxford-quantum-circuits/) says it clearly:

> I was headhunted by [Oxford Sciences Enterprises](university-of-oxford.md#oxford-sciences-enterprises) to be the founding CEO of OQC.

[https://oxfordquantumcircuits.com/story](https://oxfordquantumcircuits.com/story) mentions that the core patent was by Dr. Peter Leek: [https://www.linkedin.com/in/peter-leek-00954b62/](https://www.linkedin.com/in/peter-leek-00954b62/)

###### Rigetti Computing

↑ **Parent:** [Organization developing superconducting quantum computer](#organization-developing-superconducting-quantum-computer)  
🏷️ **Tags:** [Company](company.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Rigetti_Computing)

<a id="video-forest-an-operating-system-for-quantum-computing-by-guen-prawiroatmodjo-2017"></a>
**[Video 29](#video-forest-an-operating-system-for-quantum-computing-by-guen-prawiroatmodjo-2017). Forest: an Operating System for Quantum Computing by Guen Prawiroatmodjo (2017)** [Source](https://www.youtube.com/watch?v=SDQXGv1V2dc). The title of the talk is innapropriate, this is a very basic overview of the entire [Rigetti Computing](#rigetti-computing) stack. Still some fine mentions. Her name is so long, TODO origin? She later moved to [Microsoft Quantum](#microsoft-quantum): [https://www.linkedin.com/in/gueneverep/](https://www.linkedin.com/in/gueneverep/).

#### Topological quantum computer

↑ **Parent:** [Quantum computer physical implementation](#quantum-computer-physical-implementation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Topological_quantum_computer)

<a id="video-topological-quantum-computer-by-professor-john-preskill"></a>
**[Video 30](#video-topological-quantum-computer-by-professor-john-preskill). Topological Quantum Computer by Professor John Preskill.** [Source](https://www.youtube.com/watch?v=igPXzKjqrNg).

<a id="video-topological-quantum-computation-by-jason-alicea-2021"></a>
**[Video 31](#video-topological-quantum-computation-by-jason-alicea-2021). Topological Quantum Computation by Jason Alicea (2021)** [Source](https://www.youtube.com/watch?v=CnsQRValXdk).

<a id="video-anyons-by-yuly-billig-2022"></a>
**[Video 32](#video-anyons-by-yuly-billig-2022). Anyons by Yuly Billig (2022)** [Source](https://www.youtube.com/watch?v=LRrRgGmEeqA).

#### Trapped ion quantum computer

↑ **Parent:** [Quantum computer physical implementation](#quantum-computer-physical-implementation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Trapped_ion_quantum_computer)

TODO understand.

<a id="video-trapping-ions-for-quantum-computing-by-diana-craik-2019"></a>
**[Video 33](#video-trapping-ions-for-quantum-computing-by-diana-craik-2019). Trapping Ions for Quantum Computing by Diana Craik (2019)** [Source](https://www.youtube.com/watch?v=j1SKprQIkyE). A basic introduction, but very concrete, with only a bit of math it might be amazing:
- [https://youtu.be/j1SKprQIkyE?t=217](https://youtu.be/j1SKprQIkyE?t=217) you need [ultra-high vacuum](statistical-physics.md#ultra-high-vacuum)
- [https://youtu.be/j1SKprQIkyE?t=257](https://youtu.be/j1SKprQIkyE?t=257) you put the [Calcium](chemistry.md#calcium) on a "calcium oven", heat it up, and make it evaporates a little bit
- [https://youtu.be/j1SKprQIkyE?t=289](https://youtu.be/j1SKprQIkyE?t=289) you need [lasers](condensed-matter-physics.md#laser). You shine the laser on the calcium atom to eject one of the two valence electrons from it. Though e.g. [Universal Quantum](#universal-quantum) is trying to do away with them, because alignment for thousands or millions of particles would be difficult.
- [https://youtu.be/j1SKprQIkyE?t=518](https://youtu.be/j1SKprQIkyE?t=518) keeping all surrounding electrodes positive would be unstable. So they instead alternate electrode quickly between plus and minus
- [https://youtu.be/j1SKprQIkyE?t=643](https://youtu.be/j1SKprQIkyE?t=643) talks about the alternative, of doing it just with electrodes on a chip, which is easier to manufacture. They fly at about 100 microns above the trap. And you can have multiple ions per chip.
- [https://youtu.be/j1SKprQIkyE?t=1165](https://youtu.be/j1SKprQIkyE?t=1165) using [microwaves](photon.md#microwave) you can flip the [spin](relativistic-quantum-mechanics.md#spin-physics) of the [electron](standard-model.md#electron), or put it into a superposition. From more reading, we understand that she is talking about a [hyperfine transition](quantum-mechanics.md#hyperfine-structure), which often happen in the [microwave](photon.md#microwave) area.
- [https://youtu.be/j1SKprQIkyE?t=1210](https://youtu.be/j1SKprQIkyE?t=1210) talks about making [quantum gates](#quantum-logic-gate). You have to put the ions into a [magnetic field](electromagnetism.md#magnetic-field) at one of the two [resonance frequencies](calculus.md#resonance) of the system. Presumably what is meant is an inhomogenous magnetic field as in the [Stern-Gerlach experiment](relativistic-quantum-mechanics.md#stern-gerlach-experiment).

  This is the hard and interesting part. It is not clear why the atoms become coupled in any way. Is it due to electric repulsion?

  She is presumably describing the [Cirac–Zoller CNOT gate](#cirac-zoller-controlled-not-gate).
Sounds complicated, several technologies need to work together for that to work! Videos of ions moving are from [https://www.physics.ox.ac.uk/research/group/ion-trap-quantum-computing](https://www.physics.ox.ac.uk/research/group/ion-trap-quantum-computing).

A major flaw of this presentation is not explaining the [readout](#readout-quantum-computing) process.

---

<a id="video-how-to-trap-particles-in-a-particle-accelerator-by-the-royal-institution-2016"></a>
**[Video 34](#video-how-to-trap-particles-in-a-particle-accelerator-by-the-royal-institution-2016). How To Trap Particles in a Particle Accelerator by the Royal Institution (2016)** [Source](https://www.youtube.com/watch?v=LR_aNOcnH0Q). Demonstrates trapping pollen particles in an alternating field.

<a id="video-ion-trapping-and-quantum-gates-by-wolfgang-ketterle-2013"></a>
**[Video 35](#video-ion-trapping-and-quantum-gates-by-wolfgang-ketterle-2013). Ion trapping and quantum gates by Wolfgang Ketterle (2013)** [Source](https://www.youtube.com/watch?v=lJOuPmI--5c). - [https://youtu.be/lJOuPmI--5c?t=1601](https://youtu.be/lJOuPmI--5c?t=1601) [Cirac–Zoller CNOT gate](#cirac-zoller-controlled-not-gate) was the first 2 qubit gate. Explains it more or less.

---

<a id="video-introduction-to-quantum-optics-by-peter-zoller-2018"></a>
**[Video 36](#video-introduction-to-quantum-optics-by-peter-zoller-2018). Introduction to quantum optics by Peter Zoller (2018)** [Source](https://www.youtube.com/watch?v=W3l0QPEnaq0). THE Zoller from [Cirac–Zoller CNOT gate](#cirac-zoller-controlled-not-gate) talks about his gate.
- [https://www.youtube.com/watch?v=W3l0QPEnaq0&t=427s](https://www.youtube.com/watch?v=W3l0QPEnaq0&t=427s) shows that the state is split between two options: center of mass mode (ions move in same direction), and strechmode (atoms move in opposite directions)
- [https://youtu.be/W3l0QPEnaq0?t=658](https://youtu.be/W3l0QPEnaq0?t=658) shows a schematic of the experiment

---

<h5 id="cirac-zoller-controlled-not-gate">Cirac–Zoller controlled-NOT gate</h5>

↑ **Parent:** [Trapped ion quantum computer](#trapped-ion-quantum-computer)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Cirac–Zoller_controlled-NOT_gate)

##### Ion trap

↑ **Parent:** [Trapped ion quantum computer](#trapped-ion-quantum-computer)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Ion_trap)

##### Modular trapped ion quantum computer

↑ **Parent:** [Trapped ion quantum computer](#trapped-ion-quantum-computer)

Trapped ion people acknowledge that they can't put a million qubits in on chip (TODO why) so they are already thinking of ways to entangle separate chips. Thinking is maybe the key word here. One of the propoesd approaches inolves optical links. [Universal Quantum](#universal-quantum) for example explicitly rejects that idea in favor of electric field link modularity.

##### Organization developing trapped ion quantum computer

↑ **Parent:** [Trapped ion quantum computer](#trapped-ion-quantum-computer)  
🏷️ **Tags:** [Organization developing quantum hardware](#organization-developing-quantum-hardware)

###### IonQ

↑ **Parent:** [Organization developing trapped ion quantum computer](#organization-developing-trapped-ion-quantum-computer)  
🏷️ **Tags:** [Company](company.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/IonQ)

<a id="video-quantum-simulation-and-computation-with-trapped-ions-by-christopher-monroe-2021"></a>
**[Video 37](#video-quantum-simulation-and-computation-with-trapped-ions-by-christopher-monroe-2021). Quantum Simulation and Computation with Trapped Ions by Christopher Monroe (2021)** [Source](https://www.youtube.com/watch?v=LEqPlDrMXjs).

<a id="video-quantum-computing-with-trapped-ions-by-christopher-monroe-2018"></a>
**[Video 38](#video-quantum-computing-with-trapped-ions-by-christopher-monroe-2018). Quantum Computing with Trapped Ions by Christopher Monroe (2018)** [Source](https://www.youtube.com/watch?v=9aOLwjUZLm0). Co-founder of [IonQ](#ionq). Cool dude. Starts with basic background we already know now. Mentions that there is some relationship between [atomic clocks](system-of-units.md#atomic-clock) and [trapped ion quantum computers](#trapped-ion-quantum-computer), which is interesting. Then he goes into turbo mode, and you get lost unless you're an expert! [Video 37. "Quantum Simulation and Computation with Trapped Ions by Christopher Monroe (2021)"](#video-quantum-simulation-and-computation-with-trapped-ions-by-christopher-monroe-2021) is perhaps a better watch.
- [https://youtu.be/9aOLwjUZLm0?t=1216](https://youtu.be/9aOLwjUZLm0?t=1216) [superconducting qubits are bad because it is harder to ensure that they are all the same](#superconducting-qubits-are-bad-because-it-is-harder-to-ensure-that-they-are-all-the-same)
- [https://youtu.be/9aOLwjUZLm0?t=1270](https://youtu.be/9aOLwjUZLm0?t=1270) our wires are provided by [lasers](condensed-matter-physics.md#laser). Gives example of [ytterbium](chemistry.md#ytterbium)$^{+1}$, which has nice frequencies for practical [laser](condensed-matter-physics.md#laser) choice. Ytterbium ends in 6s2 5d1, so they must remove the 5d1 electron? But then you are left with 2 electrons in 6s2, can you just change their spins at will without problem?
- [https://youtu.be/9aOLwjUZLm0?t=1391](https://youtu.be/9aOLwjUZLm0?t=1391) a single atom actually reflects 1% of the input laser, not bad!
- [https://youtu.be/9aOLwjUZLm0?t=1475](https://youtu.be/9aOLwjUZLm0?t=1475) a transition that they want to drive in Ytterbium has 355 nm, which is easy to generate TODO why.
- [https://youtu.be/9aOLwjUZLm0?t=1520](https://youtu.be/9aOLwjUZLm0?t=1520) mentions that 351 would be much harder, e.g. as used in inertially confied fusion, takes up a room
- [https://youtu.be/9aOLwjUZLm0?t=1539](https://youtu.be/9aOLwjUZLm0?t=1539) what they use: a [pulsed laser](condensed-matter-physics.md#pulsed-laser). It is made primarily for [photolithography](computer-hardware.md#photolithography), [Coherent, Inc.](condensed-matter-physics.md#coherent-inc) makes 200 of them a year, so it is reliable stuff and easy to operate. At [https://www.coherent.com/lasers/nanosecond/avia-nx](https://www.coherent.com/lasers/nanosecond/avia-nx) we can see some of their 355 offers. [https://archive.ph/wip/JKuHI](https://archive.ph/wip/JKuHI) shows a used system going for 4500 USD.
- [https://youtu.be/9aOLwjUZLm0?t=1584](https://youtu.be/9aOLwjUZLm0?t=1584) Cirac and Zoller proposed the idea of using entangled ions soon after they heard about [Shor's algorithm](#shor-s-algorithm) in 1995
- [https://youtu.be/9aOLwjUZLm0?t=1641](https://youtu.be/9aOLwjUZLm0?t=1641) you use [optical tweezers](condensed-matter-physics.md#optical-tweezers) to move the pairs of ions you want to entangle. This means shining a [laser](condensed-matter-physics.md#laser) on two ions at the same time. Their movement depends on their [spin](relativistic-quantum-mechanics.md#spin-physics), which is already in a superposition. If both move up, their distance stats the same, so the [Coulomb interaction](electromagnetism.md#coulomb-s-law) is unchanged. But if they are different, then one goes up and the other down, distance increases due to the diagonal, and energy is lower.
- [https://youtu.be/9aOLwjUZLm0?t=1939](https://youtu.be/9aOLwjUZLm0?t=1939) S. Debnah 2016 Nature experiment with a pentagon. Well, it is not a pentagon, they are just in a linear chain, the pentagon is just to convey the full connectivity. Maybe also [Satanism](religion.md#satanism). Anyways. This point also mentions usage of an [acousto-optic modulator](photon.md#acousto-optic-modulator) to select which atoms we want to act on. On the other side, a simpler wide laser is used that hits all atoms ([optical tweezers](condensed-matter-physics.md#optical-tweezers) are literally like tweezers in the sense that you use two lasers). Later on mentions that the modulator is from Harris, later merged with L3, so: [https://www.l3harris.com/all-capabilities/acousto-optic-solutions](https://www.l3harris.com/all-capabilities/acousto-optic-solutions)
- [https://youtu.be/9aOLwjUZLm0?t=2119](https://youtu.be/9aOLwjUZLm0?t=2119) [Bernstein-Vazirani algorithm](#bernstein-vazirani-algorithm). This to illustrate better connectivity of their ion approach compared to an [IBM quantum computer](#ibm-quantum-computer), which is a [superconducting quantum computer](#superconducting-quantum-computing)
- [https://youtu.be/9aOLwjUZLm0?t=2354](https://youtu.be/9aOLwjUZLm0?t=2354) [hidden shift algorithm](#hidden-shift-algorithm)
- [https://youtu.be/9aOLwjUZLm0?t=2740](https://youtu.be/9aOLwjUZLm0?t=2740) Zhang et al. Nature 2017 paper about a 53 ion system that calculates something that cannot be classically calculated. Not fully controllable though, so more of a [continuous-variable quantum information](#continuous-variable-quantum-information) operation.
- [https://youtu.be/9aOLwjUZLm0?t=2923](https://youtu.be/9aOLwjUZLm0?t=2923) usage of cooling to 4 K to get lower pressures on top of vacuum. Before this point all experiments were room temperature. Shows image of refrigerator labelled Janis cooler, presumably something like: [https://qd-uki.co.uk/cryogenics/janis-recirculating-gas-coolers/](https://qd-uki.co.uk/cryogenics/janis-recirculating-gas-coolers/)
- [https://youtu.be/9aOLwjUZLm0?t=2962](https://youtu.be/9aOLwjUZLm0?t=2962) qubit vs gates plot by H. Neven
- [https://youtu.be/9aOLwjUZLm0?t=3108](https://youtu.be/9aOLwjUZLm0?t=3108) [modular trapped ion quantum computer](#modular-trapped-ion-quantum-computer) ideas. Mentions experiment with 2 separate systems with optical link. Miniaturization and their black box. Mentions again that their chip is from [Sandia](research-institute.md#sandia-national-laboratories). Amazing how you pronounce that.

---

###### NQIT

↑ **Parent:** [Organization developing trapped ion quantum computer](#organization-developing-trapped-ion-quantum-computer)  
🏷️ **Tags:** [UKRI](united-kingdom.md#uk-research-and-innovation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/NQIT)

<a id="video-quantum-computing-with-networked-ion-traps-by-nqit-2018"></a>
**[Video 39](#video-quantum-computing-with-networked-ion-traps-by-nqit-2018). Quantum Computing with Networked Ion traps by NQIT (2018)** [Source](https://www.youtube.com/watch?v=aV1wL5jsfRU). The video is a bit useless. But it does show the networked approach proposal a little bit. [Universal Quantum](#universal-quantum)'s homepage particularly rejects that.

###### Oxford Ionics

↑ **Parent:** [Organization developing trapped ion quantum computer](#organization-developing-trapped-ion-quantum-computer)  
🏷️ **Tags:** [British company](company.md#british-company), [University of Oxford spinout company](university-of-oxford.md#university-of-oxford-spinout-company)

- [https://www.oxionics.com/](https://www.oxionics.com/)
- [https://www.crunchbase.com/organization/oxford-ionics](https://www.crunchbase.com/organization/oxford-ionics)

This job announcement from 2022 gives a good idea about their tech stack: [https://web.archive.org/web/20220920114810/https://oxfordionics.bamboohr.com/jobs/view.php?id=32&source=aWQ9MTA%3D](https://web.archive.org/web/20220920114810/https://oxfordionics.bamboohr.com/jobs/view.php?id=32&source=aWQ9MTA%3D). Notably, they use [ARTIQ](#artiq).

Funding:
- 2023: [$](social-technology.md#dollar)36m [https://www.forbes.com/sites/gilpress/2023/01/09/36-million-oxford-ionics-funding-to-jump-start-quantum-computing-in-2023/?sh=6af75e7a6ccb](https://www.forbes.com/sites/gilpress/2023/01/09/36-million-oxford-ionics-funding-to-jump-start-quantum-computing-in-2023/?sh=6af75e7a6ccb)

###### Quantinuum

↑ **Parent:** [Organization developing trapped ion quantum computer](#organization-developing-trapped-ion-quantum-computer)  
🏷️ **Tags:** [Company](company.md)

Merger between [Cambridge Quantum Computing](#cambridge-quantum-computing), which does [quantum software](#quantum-software), and [Honeywell Quantum Solutions](#honeywell-quantum-solutions), which does the hardware.

###### Quantinuum hardware

↑ **Parent:** [Quantinuum](#quantinuum)

###### Quantinuum H1

↑ **Parent:** [Quantinuum hardware](#quantinuum-hardware)

###### Quantinuum H1-2

↑ **Parent:** [Quantinuum hardware](#quantinuum-hardware)

E.g.: [https://www.quantinuum.com/pressrelease/demonstrating-benefits-of-quantum-upgradable-design-strategy-system-model-h1-2-first-to-prove-2-048-quantum-volume](https://www.quantinuum.com/pressrelease/demonstrating-benefits-of-quantum-upgradable-design-strategy-system-model-h1-2-first-to-prove-2-048-quantum-volume) from 2021.

###### Cambridge Quantum Computing

↑ **Parent:** [Quantinuum](#quantinuum)  
🏷️ **Tags:** [Organization developing quantum software](#organization-developing-quantum-software), [University of Cambridge spinout company](university.md#university-of-cambridge-spinout-company)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Cambridge_Quantum_Computing)

In 2015, they got a 50 million investment from Grupo Arcano, led by Alberto Chang-Rajii, who is a really shady character who fled from justice for 2 years:
- [http://web.archive.org/web/20160320064944/http://www.cambridgequantum.com/index.php?page=team](http://web.archive.org/web/20160320064944/http://www.cambridgequantum.com/index.php?page=team) Alberto on the board
- [https://theshiftnews.com/2018/10/25/wanted-chilean-businessman-in-hiding-in-malta-for-two-years/](https://theshiftnews.com/2018/10/25/wanted-chilean-businessman-in-hiding-in-malta-for-two-years/)
- [https://www.techbritannia.co.uk/2015/09/cambridge-quantum-computing-receives-50m-funding-from-grupo-arcano/](https://www.techbritannia.co.uk/2015/09/cambridge-quantum-computing-receives-50m-funding-from-grupo-arcano/)
Merged into [Quantinuum](#quantinuum) later on in 2021.

###### tket

↑ **Parent:** [Cambridge Quantum Computing](#cambridge-quantum-computing)  
🏷️ **Tags:** [Quantum compiler](#quantum-compilation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/tket)

[https://github.com/CQCL/tket](https://github.com/CQCL/tket)

TODO vs all the others?

###### Honeywell Quantum Solutions

↑ **Parent:** [Quantinuum](#quantinuum)  
🏷️ **Tags:** [Honeywell](company.md#honeywell)

###### Universal Quantum

↑ **Parent:** [Organization developing trapped ion quantum computer](#organization-developing-trapped-ion-quantum-computer)  
🏷️ **Tags:** [British company](company.md#british-company)

As of 2021, their location is a small business park in Haywards Heath, about 15 minutes north of [Brighton](united-kingdom.md#brighton)[https://www.midsussex.gov.uk/about-us/press-releases-and-publications/cutting-edge-tech-company-invests-in-mid-sussex/](https://www.midsussex.gov.uk/about-us/press-releases-and-publications/cutting-edge-tech-company-invests-in-mid-sussex/)

Funding rounds:
- 2022:
  - 67m euro contract with the [German](continent.md#germany) government: [https://www.uktech.news/deep-tech/universal-quantum-german-contract-20221102](https://www.uktech.news/deep-tech/universal-quantum-german-contract-20221102) Both co-founders are German. They then immediatly announced several jobs in Hamburg: [https://apply.workable.com/universalquantum/?lng=en#jobs](https://apply.workable.com/universalquantum/?lng=en#jobs) so presumably linked to the Hamburg University of Technology campus of the German Aerospace Center.
  - [https://medium.com/@universalquantum/universal-quantum-wins-67m-contract-to-build-the-fully-scalable-trapped-ion-quantum-computer-16eba31b869e](https://medium.com/@universalquantum/universal-quantum-wins-67m-contract-to-build-the-fully-scalable-trapped-ion-quantum-computer-16eba31b869e)
- 2021: $10M (7.5M GBP) grant from the [British Government](united-kingdom.md#government-of-the-united-kingdom): [https://www.uktech.news/news/brighton-universal-quantum-wins-grant-20211105](https://www.uktech.news/news/brighton-universal-quantum-wins-grant-20211105)

  This grant is very secretive, very hard to find any other information about it! Most investment trackers are not listing it.

  The article reads:

  > Universal Quantum will lead a consortium that includes Rolls-Royce, quantum developer [Riverlane](#riverlane), and world-class researchers from [Imperial College London](university.md#imperial-college-london) and The [University of Sussex](university.md#university-of-sussex), among others.

  Interesting!

  A but further down the article gives some more information of partners, from which some of the hardware vendors can be deduced:

  > The consortium includes end-user [Rolls-Royce](mechanics.md#rolls-royce) supported by the [Science and Technology Facilities Council](united-kingdom.md#science-and-technology-facilities-council) (STFC) Hartree Centre, quantum software developer [Riverlane](#riverlane), supply chain partners Edwards, [TMD Technologies](https://www.tmd.co.uk/) (now acquired by Communications & Power Industries (CPI)) and [Diamond Microwave](https://www.diamondmic.com/)


  - Edwards is presumably [Edwards Vacuum](statistical-physics.md#edwards-vacuum), since we know that [trapped ion quantum computers](#trapped-ion-quantum-computer) rely heavily on good vacuum systems. Edwards Vacuum is also located quite close to Universal Quantum as of 2022, a few minutes drive.
  - TMD Technologies is a [microwave](photon.md#microwave) technology vendor amongst other things, and we know that microwaves are used e.g. to initialize the spin states of the ions
  - Diamond Microwave is another microwave stuff vendor

  The money comes from UK's "Industrial Strategy Challenge Fund".

  [https://www.riverlane.com/news/2021/12/riverlane-joins-7-5-million-consortium-to-build-error-corrected-quantum-processor/](https://www.riverlane.com/news/2021/12/riverlane-joins-7-5-million-consortium-to-build-error-corrected-quantum-processor/) gives some more details on the use case provided by Rolls Royce:

  > The work with Rolls Royce will explore how quantum computers can develop practical applications toward the development of more sustainable and efficient jet engines.  
  > 
  > This starts by applying quantum algorithms to take steps to toward a greater understanding of how liquids and gases flow, a field known as '[fluid dynamics](mechanics.md#fluid-dynamics)'. Simulating such flows accurately is beyond the computational capacity of even the most powerful classical computers today.

  This funding was part of a larger quantum push by the [UKNQTP](united-kingdom.md#uk-national-quantum-technologies-programme): [https://www.ukri.org/news/50-million-in-funding-for-uk-quantum-industrial-projects/](https://www.ukri.org/news/50-million-in-funding-for-uk-quantum-industrial-projects/)
- 2020: $4.5M (3.5M GBP) [https://www.crunchbase.com/organization/universal-quantum](https://www.crunchbase.com/organization/universal-quantum). Just out of stealth.

Co-founders:
- Sebastian Weidt. He is [German](continent.md#germany), right? Yes at [https://youtu.be/SwHaJXVYIeI?t=1078](https://youtu.be/SwHaJXVYIeI?t=1078) from [Video 42. "Fireside Chat with with Sebastian Weidt by Startup Grind Brighton (2022)"](#video-fireside-chat-with-with-sebastian-weidt-by-startup-grind-brighton-2022). The company was founded by two Germans from Essex!
- Winfried Hensinger: if you saw him on the street, you'd think he plays in a punk-rock band. That West Berlin feeling.

Homepage says only needs cooling to 70 K. So it doesn't work with [liquid nitrogen](chemistry.md#liquid-nitrogen) which is 77 K?

Homepage points to foundational paper: [https://www.science.org/doi/10.1126/sciadv.1601540](https://www.science.org/doi/10.1126/sciadv.1601540)

<a id="video-universal-quantum-emerges-out-of-stealth-by-university-of-sussex-2020"></a>
**[Video 40](#video-universal-quantum-emerges-out-of-stealth-by-university-of-sussex-2020). Universal Quantum emerges out of stealth by University of Sussex (2020)** [Source](https://www.youtube.com/watch?v=rYe9TXz35B8). Explains that a more "traditional" [trapped ion quantum computer](#trapped-ion-quantum-computer) would user "pairs of [lasers](condensed-matter-physics.md#laser)", which would require a lot of lasers. Their approach is to try and do it by applying voltages to a microchip instead.
- [https://youtu.be/rYe9TXz35B8?t=127](https://youtu.be/rYe9TXz35B8?t=127) shows some 3D models. It shows how [piezoelectric actuators](condensed-matter-physics.md#piezoelectric-actuator) are used to align or misalign some plates, which presumably then determine conductivity

---

<a id="video-quantum-computing-webinar-with-sebastian-weidt-by-green-lemon-company-2020"></a>
**[Video 41](#video-quantum-computing-webinar-with-sebastian-weidt-by-green-lemon-company-2020). Quantum Computing webinar with Sebastian Weidt by Green Lemon Company (2020)** [Source](https://www.youtube.com/watch?v=WhredTaZvTs). The sound quality is to bad to stop and listen to, but it presumaby shows the coding office in the background.

<a id="video-fireside-chat-with-with-sebastian-weidt-by-startup-grind-brighton-2022"></a>
**[Video 42](#video-fireside-chat-with-with-sebastian-weidt-by-startup-grind-brighton-2022). Fireside Chat with with Sebastian Weidt by Startup Grind Brighton (2022)** [Source](https://www.youtube.com/watch?v=SwHaJXVYIeI). Very basic target audience:
- [https://youtu.be/SwHaJXVYIeI?t=680](https://youtu.be/SwHaJXVYIeI?t=680) we are not at a point where you can buy victory. There is too much uncertainty involved across different approaches.
- [https://youtu.be/SwHaJXVYIeI?t=949](https://youtu.be/SwHaJXVYIeI?t=949) his background
- [https://youtu.be/SwHaJXVYIeI?t=1277](https://youtu.be/SwHaJXVYIeI?t=1277) difference between [venture capitalists](company.md#venture-capitalist) in different countries
- [https://youtu.be/SwHaJXVYIeI?t=1535](https://youtu.be/SwHaJXVYIeI?t=1535) they are 33 people now. They've just setup their office in Haywards Heath, north of Bristol.

---

#### Neutral atom quantum computer

↑ **Parent:** [Quantum computer physical implementation](#quantum-computer-physical-implementation)

- [https://quantumtech.blog/2023/01/17/quantum-computing-with-neutral-atoms/](https://quantumtech.blog/2023/01/17/quantum-computing-with-neutral-atoms/)

##### Organization developing neutral atom quantum computer

↑ **Parent:** [Neutral atom quantum computer](#neutral-atom-quantum-computer)  
🏷️ **Tags:** [Organization developing quantum hardware](#organization-developing-quantum-hardware)

###### Atom Computing

↑ **Parent:** [Organization developing neutral atom quantum computer](#organization-developing-neutral-atom-quantum-computer)  
🏷️ **Tags:** [American company](company.md#american-company), [Organization developing nuclear magnetic resonance quantum computer](#organization-developing-nuclear-magnetic-resonance-quantum-computer)

These people are cool.

They use [optical tweezers](condensed-matter-physics.md#optical-tweezers) to place individual atoms floating in midair, and then do stuff to entangle their [nuclear spins](particle-physics.md#nuclear-magnetic-moment).

###### Infleqtion

↑ **Parent:** [Organization developing neutral atom quantum computer](#organization-developing-neutral-atom-quantum-computer)

[https://infleqtion.com/](https://infleqtion.com/)

###### QuEra

↑ **Parent:** [Organization developing neutral atom quantum computer](#organization-developing-neutral-atom-quantum-computer)  
🏷️ **Tags:** [American company](company.md#american-company), [Analog quantum computer](#analog-quantum-computer)

- [https://www.quera.com/about](https://www.quera.com/about)
- [https://mobile.twitter.com/queracomputing](https://mobile.twitter.com/queracomputing)

###### Pasqal

↑ **Parent:** [Organization developing neutral atom quantum computer](#organization-developing-neutral-atom-quantum-computer)  
🏷️ **Tags:** [Analog quantum computer](#analog-quantum-computer), [French company](company.md#french-company)

[https://pasqal.io/](https://pasqal.io/)

Funding:
- 2023: [$](social-technology.md#dollar)100m [https://techcrunch.com/2023/01/23/pasqal-raises-100m-to-build-a-neutral-atom-based-quantum-computer/](https://techcrunch.com/2023/01/23/pasqal-raises-100m-to-build-a-neutral-atom-based-quantum-computer/)

#### Photonic quantum computer

↑ **Parent:** [Quantum computer physical implementation](#quantum-computer-physical-implementation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Linear optical quantum computing)

- [https://en.wikipedia.org/wiki/Linear_optical_quantum_computing](https://en.wikipedia.org/wiki/Linear_optical_quantum_computing)
- [https://en.wikipedia.org/wiki/KLM_protocol](https://en.wikipedia.org/wiki/KLM_protocol)

Uses [photons](photon.md)!

The key experiment/phenomena that sets the basis for photonic quantum computing is the [two photon interference experiment](photon.md#two-photon-interference-experiment).

The physical representation of the information encoding is very easy to understand:
- input: we choose to put or not photons into certain wires or no
- interaction: two wires pass very nearby at some point, and photons travelling on either of them can jump to the other one and interact with the other photons
- output: the probabilities that photos photons will go out through one wire or another

<a id="video-jeremy-o-brien-quantum-technologies-by-googletechtalks-2014"></a>
**[Video 43](#video-jeremy-o-brien-quantum-technologies-by-googletechtalks-2014). Jeremy O'Brien: "Quantum Technologies" by GoogleTechTalks (2014)** [Source](http://youtube.com/watch?v=7wCBkAQYBZA). This is a good introduction to a [photonic quantum computer](#photonic-quantum-computer). Highly recommended.
- [https://youtube.com/watch?v=7wCBkAQYBZA&t=1285](https://youtube.com/watch?v=7wCBkAQYBZA&t=1285) shows an experimental curve for a [two photon interference experiment](photon.md#two-photon-interference-experiment) by Hong, Ou, Mandel (1987)
- [https://youtube.com/watch?v=7wCBkAQYBZA&t=1440](https://youtube.com/watch?v=7wCBkAQYBZA&t=1440) shows a KLM [CNOT gate](#cnot-gate)
- [https://youtube.com/watch?v=7wCBkAQYBZA&t=2831](https://youtube.com/watch?v=7wCBkAQYBZA&t=2831) discusses the [quantum error correction](#quantum-error-correction) scheme for photonic QC based on the idea of the "Raussendorf unit cell"

---

##### Organization developing photonic quantum computer

↑ **Parent:** [Photonic quantum computer](#photonic-quantum-computer)  
🏷️ **Tags:** [Organization developing quantum hardware](#organization-developing-quantum-hardware)

###### Quandela

↑ **Parent:** [Organization developing photonic quantum computer](#organization-developing-photonic-quantum-computer)  
🏷️ **Tags:** [French company](company.md#french-company)

[https://www.quandela.com](https://www.quandela.com)

One interesting aspect of this company is that they are trying to sell not only full [quantum computers](quantum-computing.md), but also components that could be used by competitors, such as 

###### Prometheus single photon source

↑ **Parent:** [Quandela](#quandela)

[https://www.quandela.com/prometheus/](https://www.quandela.com/prometheus/) ([2024 archive](https://web.archive.org/web/20240110044019/https://www.quandela.com/prometheus/))

###### ORCA Computing

↑ **Parent:** [Organization developing photonic quantum computer](#organization-developing-photonic-quantum-computer)  
🏷️ **Tags:** [British company](company.md#british-company)

[https://www.orcacomputing.com/](https://www.orcacomputing.com/)

- 2022: $15 million [https://www.orcacomputing.com/blog/orca-computing-completes-15-million-series-a-funding-round](https://www.orcacomputing.com/blog/orca-computing-completes-15-million-series-a-funding-round)
- 2021: $14.5 million for an [Innovate UK](united-kingdom.md#innovate-uk) project

###### PsiQuantum

↑ **Parent:** [Organization developing photonic quantum computer](#organization-developing-photonic-quantum-computer)  
🏷️ **Tags:** [Company](company.md)

CEO: [Jeremy O'Brien](#jeremy-o-brien)

Raised 215M in 2020: [https://www.bloomberg.com/news/articles/2020-04-06/quantum-computing-startup-raises-215-million-for-faster-device](https://www.bloomberg.com/news/articles/2020-04-06/quantum-computing-startup-raises-215-million-for-faster-device)

Good talk by CEO before starting the company which gives insight on what they are very likely doing: [Video 43. "Jeremy O'Brien: "Quantum Technologies" by GoogleTechTalks (2014)"](#video-jeremy-o-brien-quantum-technologies-by-googletechtalks-2014)

PsiQuantum appears to be particularly secretive, even more than other startups in the field.

They want to reuse classical [semiconductor fabrication technologies](computer-hardware.md#semiconductor-device-fabrication), notably they have close ties to [GlobalFoundries](computer-hardware.md#globalfoundries).

So he went to the [US](united-states.md) and raised N times more from the [American](united-states.md) [military-industrial complex](science.md#military-industrial-complex).

<h6 id="jeremy-o-brien">Jeremy O'Brien</h6>

↑ **Parent:** [PsiQuantum](#psiquantum)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Jeremy_O'Brien)

[https://www.linkedin.com/in/jeremy-o-brien-39482631](https://www.linkedin.com/in/jeremy-o-brien-39482631)

###### PsiQuantum founding myth

↑ **Parent:** [PsiQuantum](#psiquantum)

Once upon a time, the [British Government](united-kingdom.md#government-of-the-united-kingdom) decided to invest some 80 million into [quantum computing](quantum-computing.md).

[Jeremy O'Brien](#jeremy-o-brien) told his peers that he had the best tech, and that he should get it all.

Some well connected peers from well known universities did not agree however, and also bid for the money, and won.

Jeremy was defeated. And pissed.

So he moved to [Palo Alto](united-states.md#palo-alto) and raised a total of $665 million instead as of 2021. The end.

Makes for a reasonable [the old man lost his horse](china.md#the-old-man-lost-his-horse).

[https://www.ft.com/content/afc27836-9383-11e9-aea1-2b1d33ac3271](https://www.ft.com/content/afc27836-9383-11e9-aea1-2b1d33ac3271) British quantum computing experts leave for Silicon Valley talks a little bit about them leaving, but nothing too juicy. They were called PsiQ previously apparently.

> The departure of some of the UK’s leading experts in a potentially revolutionary new field of technology will raise fresh concerns over the country’s ability to develop industrial champions in the sector.

More interestingly, the article mentions that this was party advised by early investor [Hermann Hauser](company.md#hermann-hauser), who is known to be preoccupied about UK's ability to create companies. Of course, [European Tower of Babel](cirism.md#european-tower-of-babel).

###### Xanadu Quantum Technologies

↑ **Parent:** [Organization developing photonic quantum computer](#organization-developing-photonic-quantum-computer)  
🏷️ **Tags:** [Company](company.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Xanadu_Quantum_Technologies)

Rounds:
- 2022-11: 100m USD [https://www.prnewswire.com/news-releases/xanadu-closes-100m-usd-series-c-to-accelerate-development-of-fault-tolerant-quantum-computers-301672611.html](https://www.prnewswire.com/news-releases/xanadu-closes-100m-usd-series-c-to-accelerate-development-of-fault-tolerant-quantum-computers-301672611.html)

[https://www.youtube.com/watch?v=v7iAqcFCTQQ](https://www.youtube.com/watch?v=v7iAqcFCTQQ) shows their base technology:
- [laser](condensed-matter-physics.md#laser) beam comes in
- input set via of [optical ring resonators](photon.md#optical-ring-resonator) that form a [squeezed state of light](photon.md#squeezed-state-of-light). Does not seem to rely on [single photon production and detection experiments](photon.md#single-photon-production-and-detection)?

### Quantum computing hardware bibliography

↑ **Parent:** [Quantum computing hardware](#quantum-computing-hardware)

Lists:
- [https://www.reddit.com/r/QuantumComputing/comments/j2rcbm/books_on_the_physical_design_of_quantum_computers/](https://www.reddit.com/r/QuantumComputing/comments/j2rcbm/books_on_the_physical_design_of_quantum_computers/)

#### Hardware for Quantum Computing by Chuck Easttom

↑ **Parent:** [Quantum computing hardware bibliography](#quantum-computing-hardware-bibliography)

This book is mostly a failure unfortunately, as it glosses far too quickly over the physical implementations.

##### Chuck Easttom

↑ **Parent:** [Hardware for Quantum Computing by Chuck Easttom](#hardware-for-quantum-computing-by-chuck-easttom)

Author of [hardware for Quantum Computing by Chuck Easttom](#hardware-for-quantum-computing-by-chuck-easttom).

On [Amazon](amazon.md): [https://www.amazon.com/dp/3031664760](https://www.amazon.com/dp/3031664760)

ISBN: 3031664760.

Certainly he looks after his image very strictly, endlessly saying how good he is. And he is definitely a [high flying bird](mathematics.md#high-flying-bird-vs-gophers). Perhaps [it is hard to differentiate genius from mad](brain.md#it-is-hard-to-differentiate-genius-from-mad) applies.

<a id="video-ec-council-certified-encryption-specialist-eces-with-chuck-easttom"></a>
**[Video 44](#video-ec-council-certified-encryption-specialist-eces-with-chuck-easttom). EC-Council Certified Encryption Specialist (ECES) with Chuck Easttom.** [Source](https://www.youtube.com/watch?v=ZLuz60ImHuM). Check saying how amazing he is.

## Quantum interconnect

↑ **Parent:** [Quantum computing](quantum-computing.md)

"Quantum interconnect" refers to methods for linking up smaller quantum processors into a larger system.

As of 2024, seemingly few [organizations developing quantum hardware](#organization-developing-quantum-hardware) had actually integrated multiple chips in interconnects as part of their main current roadmap. But many acknowledged that this would be an essential step towards scalable compuation.

The name "quantum interconnect" is likely partly a throwback to [classical computer](#classical-computer)'s "[chip interconnect](computer-hardware.md#interconnect-integrated-circuits)".

Sample usages of the term:
- [https://news.mit.edu/2023/quantum-interconnects-photon-emission-0105](https://news.mit.edu/2023/quantum-interconnects-photon-emission-0105)> Researchers have demonstrated directional photon emission, the first step toward extensible **quantum interconnects**
- [https://qpl.ece.ucsb.edu/research/quantum-interconnects](https://qpl.ece.ucsb.edu/research/quantum-interconnects)

<a id="video-gerhard-rempe-quantum-dynamics-by-max-planck-institute-of-quantum-optics"></a>
**[Video 45](#video-gerhard-rempe-quantum-dynamics-by-max-planck-institute-of-quantum-optics). Gerhard Rempe - Quantum Dynamics by Max Planck Institute of Quantum Optics.** [Source](https://www.youtube.com/watch?v=PzZJmujw71s). No technical details of course, but they do show off their [optical tables](photon.md#optical-table) quite a bit!

### Quantum interconnect company

↑ **Parent:** [Quantum interconnect](#quantum-interconnect)

#### Welinq

↑ **Parent:** [Quantum interconnect company](#quantum-interconnect-company)  
🏷️ **Tags:** [French company](company.md#french-company)

Funding:
- 2023-01-23 €5 Million
  - [https://thequantuminsider.com/2023/01/23/welinq-closes-e5-million-pre-seed-round/](https://thequantuminsider.com/2023/01/23/welinq-closes-e5-million-pre-seed-round/)

## Quantum computer simulator

↑ **Parent:** [Quantum computing](quantum-computing.md)

Other good lists:
- [https://quantumcomputingreport.com/resources/tools/](https://quantumcomputingreport.com/resources/tools/) is hard to beat as usual.
- [https://www.quantiki.org/wiki/list-qc-simulators](https://www.quantiki.org/wiki/list-qc-simulators)

- [JavaScript](programming-language.md#javascript)
  - [https://algassert.com/quirk](https://algassert.com/quirk) demo: [https://github.com/Strilanc/Quirk](https://github.com/Strilanc/Quirk) drag-and-drop, by a 2019-quantum-computing-[Googler](google.md), impressive. You can create gates. State store in URL.
  - [https://github.com/stewdio/q.js/](https://github.com/stewdio/q.js/) demo: [https://quantumjavascript.app/](https://quantumjavascript.app/)

Bibliography:
- [https://www.epcc.ed.ac.uk/whats-happening/articles/energy-efficient-quantum-computing-simulations](https://www.epcc.ed.ac.uk/whats-happening/articles/energy-efficient-quantum-computing-simulations) mentions two types of [quantum computer simulation](#quantum-computer-simulator):
  - > The most common approach to quantum simulations is to store the whole state in memory and to modify it with gates in a given order
  - > However, there is a completely different approach that can sometimes eliminate this issue - tensor networks

## Quantum software

↑ **Parent:** [Quantum computing](quantum-computing.md)

### Quantum programming framework

↑ **Parent:** [Quantum software](#quantum-software)

#### Cirq

↑ **Parent:** [Quantum programming framework](#quantum-programming-framework)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Cirq)

#### PennyLane

↑ **Parent:** [Quantum programming framework](#quantum-programming-framework)  
🏷️ **Tags:** [Python library](programming-language.md#python-library)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/PennyLane)

By [Xanadu](#xanadu-quantum-technologies).

Apparently meant to be higher level.

Homepage: [https://pennylane.ai/](https://pennylane.ai/)

[Source code](software.md#source-code): [https://github.com/PennyLaneAI/pennylane](https://github.com/PennyLaneAI/pennylane)

#### Qiskit

↑ **Parent:** [Quantum programming framework](#quantum-programming-framework)  
🏷️ **Tags:** [Python library](programming-language.md#python-library)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Qiskit)

[Python](programming-language.md#python-programming-language) library, claims multiple backends, including [simulation](#quantum-computer-simulator) and real [IBM quantum computer](#ibm-quantum-computer).

##### Qiskit example

↑ **Parent:** [Qiskit](#qiskit)

###### Qiskit hello world

↑ **Parent:** [Qiskit example](#qiskit-example)  
🏷️ **Tags:** [Hello world](software.md#hello-world-program)

The official [hello world](software.md#hello-world-program) is documented at: [https://qiskit.org/documentation/intro_tutorial1.html](https://qiskit.org/documentation/intro_tutorial1.html) and contains a [Bell state circuit](#bell-circuit).

Our version at [qiskit/hello.py](#_file/qiskit/hello.py).

<h6 id="_file/qiskit/hello.py">qiskit/hello.py</h6>

↑ **Parent:** [Qiskit hello world](#qiskit-hello-world)

Our example uses a [Bell state circuit](#bell-circuit) to illustrate all the fundamental [Qiskit](#qiskit) basics.

Sample program output, `counts` are randomized each time.

First we take the [quantum state vector](#quantum-state-vector) immediately after the $\ket{00}$ input.
```
input:
state:
Statevector([1.+0.j, 0.+0.j, 0.+0.j, 0.+0.j],
            dims=(2, 2))
probs:
[1. 0. 0. 0.]
```
We understand that the first element of `Statevector` is $\ket{00}$, and has probability of 1.0.

Next we take the state after a [Hadamard gate](#hadamard-gate) on the first [qubit](#qubit):
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

Then we apply the [CNOT gate](#cnot-gate):
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

And finally we [compile](#quantum-compilation) the circuit and do some sample measurements:
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

<h6 id="qiskit-initialize-py">qiskit/initialize.py</h6>

↑ **Parent:** [Qiskit example](#qiskit-example)

In this example we will initialize a quantum circuit with a single [CNOT gate](#cnot-gate) and see the output values.

By default, [Qiskit](#qiskit) initializes every [qubit](#qubit) to 0 as shown in the [qiskit/hello.py](#_file/qiskit/hello.py). But we can also initialize to arbitrary values as would be done when computing the output for various different inputs.

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
which we should all be able to understand intuitively given our understanding of the [CNOT gate](#cnot-gate) and [quantum state vectors](#quantum-state-vector).

[https://quantumcomputing.stackexchange.com/questions/13202/qiskit-initializing-n-qubits-with-binary-values-0s-and-1s](https://quantumcomputing.stackexchange.com/questions/13202/qiskit-initializing-n-qubits-with-binary-values-0s-and-1s) describes how to initialize circuits qubits only with binary 0 or 1 to avoid dealing with the exponential number of elements of the [quantum state vector](#quantum-state-vector).

<h6 id="_file/qiskit/qft.py">qiskit/qft.py</h6>

↑ **Parent:** [Qiskit example](#qiskit-example)  
🏷️ **Tags:** [Quantum Fourier transform](#quantum-fourier-transform)

This is an example of the `qiskit.circuit.library.QFT` implementation of the [Quantum Fourier transform](#quantum-fourier-transform) function which is documented at: [https://docs.quantum.ibm.com/api/qiskit/0.44/qiskit.circuit.library.QFT](https://docs.quantum.ibm.com/api/qiskit/0.44/qiskit.circuit.library.QFT)

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
So this also serves as a more interesting example of [quantum compilation](#quantum-compilation), mapping the `QFT` gate to [Qiskit Aer](#qiskit-aer) primitives.

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
which can be defined simply as the [normalized DFT](calculus.md#normalized-dft) of the input [quantum state vector](#quantum-state-vector).

From this we see that the [Quantum Fourier transform](#quantum-fourier-transform) is equivalent to a direct [discrete Fourier transform](calculus.md#discrete-fourier-transform) on the [quantum state vector](#quantum-state-vector), related: [https://physics.stackexchange.com/questions/110073/how-to-derive-quantum-fourier-transform-from-discrete-fourier-transform-dft](https://physics.stackexchange.com/questions/110073/how-to-derive-quantum-fourier-transform-from-discrete-fourier-transform-dft)

##### Qiskit component

↑ **Parent:** [Qiskit](#qiskit)

<h6 id="qiskit-transpile"><code>qiskit.transpile()</code></h6>

↑ **Parent:** [Qiskit component](#qiskit-component)

This function does [quantum compilation](#quantum-compilation). Shown e.g. at [qiskit/qft.py](#_file/qiskit/qft.py).

###### Qiskit Aer

↑ **Parent:** [Qiskit component](#qiskit-component)  
🏷️ **Tags:** [Quantum computer simulator](#quantum-computer-simulator)

[https://github.com/Qiskit/qiskit-aer](https://github.com/Qiskit/qiskit-aer)

###### AerError: 'unknown instruction

↑ **Parent:** [Qiskit Aer](#qiskit-aer)

You get an error like this if you forget to call [`qiskit.transpile()`](#qiskit-transpile):
```
qiskit_aer.aererror.AerError: 'unknown instruction: QFT'
```
Related: [https://quantumcomputing.stackexchange.com/questions/34396/aererror-unknown-instruction-c-unitary-while-using-control-unitary-operator/35132#35132](https://quantumcomputing.stackexchange.com/questions/34396/aererror-unknown-instruction-c-unitary-while-using-control-unitary-operator/35132#35132)

### Quantum circuit description language

↑ **Parent:** [Quantum software](#quantum-software)

These are a bit like the [Verilog](computer-hardware.md#verilog) of [quantum computing](quantum-computing.md).

One would hope that they are not [Turing complete](computer-science.md#turing-complete), this way they may serve as a way to pass on data in such a way that the receiver knows they will only be doing so much computation in advance to unpack the circuit. So it would be like [JSON](computer.md#json) is for [JavaScript](programming-language.md#javascript).

### OpenQASM

↑ **Parent:** [Quantum software](#quantum-software)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/OpenQASM)

On [Qiskit](#qiskit) `qiskit==0.44.1`:
```
qc.qasm()
```

E.g. with our [qiskit/hello.py](#_file/qiskit/hello.py), we obtain the [Bell state circuit](#bell-circuit):
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

### Quantum control system

↑ **Parent:** [Quantum software](#quantum-software)

Some people call it "operating System".

The main parts of those systems are:
- sending multiple signals at very precise times to the system
- reading out some [quantum error correction](#quantum-error-correction) bits and sending error correcting signals back in a control loop

#### Quantum control systems use FPGAs

↑ **Parent:** [Quantum control system](#quantum-control-system)  
🏷️ **Tags:** [FPGA](computer-hardware.md#field-programmable-gate-array)

It seems that all/almost all of them do. Quite cool.

<a id="video-fpga-architecture-of-the-quantum-control-system-by-keysight-2022"></a>
**[Video 46](#video-fpga-architecture-of-the-quantum-control-system-by-keysight-2022). FPGA Architecture of the Quantum Control System by Keysight (2022)** [Source](https://www.youtube.com/watch?v=0262IFOdUV0). They actually have a dedicated quantum team! Cool.

<a id="video-fpga-based-servo-system-by-atoms-and-laser-2018"></a>
**[Video 47](#video-fpga-based-servo-system-by-atoms-and-laser-2018). FPGA based servo system by Atoms & Laser (2018)** [Source](https://www.youtube.com/watch?v=qjjuWSqEPQ8). The Indian lady is hardcore.

#### Organization developing quantum control systems

↑ **Parent:** [Quantum control system](#quantum-control-system)  
🏷️ **Tags:** [Organization developing quantum software](#organization-developing-quantum-software)

[https://github.com/m-labs/artiq](https://github.com/m-labs/artiq)

##### ParityQC

↑ **Parent:** [Organization developing quantum control systems](#organization-developing-quantum-control-systems)

[https://parityqc.com](https://parityqc.com)

##### Q-CTRL

↑ **Parent:** [Organization developing quantum control systems](#organization-developing-quantum-control-systems)  
🏷️ **Tags:** [Australian company](company.md#australian-company)

[https://q-ctrl.com/](https://q-ctrl.com/)

Someone attempted a [Wikipedia](website.md#wikipedia) page apparently: [https://en.wikipedia.org/wiki/Q-CTRL](https://en.wikipedia.org/wiki/Q-CTRL). [Nice try, nice try](website.md#deletionism-on-wikipedia).

##### QuantrolOx

↑ **Parent:** [Organization developing quantum control systems](#organization-developing-quantum-control-systems)  
🏷️ **Tags:** [University of Oxford spinout company](university-of-oxford.md#university-of-oxford-spinout-company)

[https://q-ctrl.com/](https://q-ctrl.com/)

##### Quantum Machines

↑ **Parent:** [Organization developing quantum control systems](#organization-developing-quantum-control-systems)  
🏷️ **Tags:** [Israeli company](company.md#israeli-company)

##### M-Labs

↑ **Parent:** [Organization developing quantum control systems](#organization-developing-quantum-control-systems)  
🏷️ **Tags:** [French company](company.md#french-company)

###### ARTIQ

↑ **Parent:** [M-Labs](#m-labs)  
🏷️ **Tags:** [List of quantum control systems](#list-of-quantum-control-systems), [Open source software](software.md#open-source-software)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/ARTIQ)

###### Duke ARTIQ extensions

↑ **Parent:** [ARTIQ](#artiq)

[https://gitlab.com/duke-artiq/dax](https://gitlab.com/duke-artiq/dax)

##### Riverlane

↑ **Parent:** [Organization developing quantum control systems](#organization-developing-quantum-control-systems)  
🏷️ **Tags:** [British company](company.md#british-company), [University of Cambridge spinout company](university.md#university-of-cambridge-spinout-company)

[https://www.riverlane.com/](https://www.riverlane.com/)

When you fail a HR interview, then you know you've reached rock bottom.

Investments:
- 2024: 75m GBP
- 2023-04: 15m GBP: [https://www.uktech.news/deep-tech/riverlane-series-b-20230424](https://www.uktech.news/deep-tech/riverlane-series-b-20230424) At 100 employeed on LinkedIn, this should keep them going for two more years.
- 2022 500k GBP: [https://www.uktech.news/deep-tech/riverlane-rigetti-quantum-innovate-uk-20220628](https://www.uktech.news/deep-tech/riverlane-rigetti-quantum-innovate-uk-20220628) by [Innovate UK](united-kingdom.md#innovate-uk) for joing project with [Rigetti Computing](#rigetti-computing) to work on [quantum error correction](#quantum-error-correction)

<a id="video-the-operating-system-for-quantum-computing-by-steve-brierley-2021"></a>
**[Video 48](#video-the-operating-system-for-quantum-computing-by-steve-brierley-2021). The Operating System for Quantum Computing by Steve Brierley (2021)** [Source](https://www.youtube.com/watch?v=ugzWnw1LTBE). Founding CEO. He seems nice. You might as well just start watching at: [https://youtu.be/ugzWnw1LTBE?t=1166](https://youtu.be/ugzWnw1LTBE?t=1166) where more specific things start to come out.

<h6 id="deltaflow-os">Deltaflow.OS</h6>

↑ **Parent:** [Riverlane](#riverlane)

A "quantum computer operating system". Or in English, control system + [quantum error correction](#quantum-error-correction).

[https://uknqt.ukri.org/wp-content/uploads/2021/10/UKNQTP-Strategic-Intent-2020.pdf](https://uknqt.ukri.org/wp-content/uploads/2021/10/UKNQTP-Strategic-Intent-2020.pdf) page 24 mentions [UKNQTP](united-kingdom.md#uk-national-quantum-technologies-programme) investment and gives an overview of some layers.

##### Zurich Instruments

↑ **Parent:** [Organization developing quantum control systems](#organization-developing-quantum-control-systems)  
🏷️ **Tags:** [French company](company.md#french-company)

[https://www.zhinst.com/europe/en/quantum-computing-systems/qccs](https://www.zhinst.com/europe/en/quantum-computing-systems/qccs)

#### List of quantum control systems

↑ **Parent:** [Quantum control system](#quantum-control-system)  
🏷️ **Tags:** [Organization developing quantum software](#organization-developing-quantum-software)

##### Pulser (quantum control)

↑ **Parent:** [List of quantum control systems](#list-of-quantum-control-systems)

[https://github.com/pasqal-io/Pulser](https://github.com/pasqal-io/Pulser)

This is the one by [Pasqal](#pasqal).

## Classical computer

↑ **Parent:** [Quantum computing](quantum-computing.md)

In the context of [quantum computing](quantum-computing.md) of the 2020's, a "classical computer" is a [computer](computer.md) that is not "quantum", i.e., the then dominating [CMOS](electronics.md#cmos) computers.

## ZX-calculus

↑ **Parent:** [Quantum computing](quantum-computing.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/ZX-calculus)

As [https://en.wikipedia.org/w/index.php?title=ZX-calculus&oldid=1071329204#Diagram_rewriting](https://en.wikipedia.org/w/index.php?title=ZX-calculus&oldid=1071329204#Diagram_rewriting) tries to explain [but fails to deliver as usual](ourbigbook-com.md#wikipedia) consider the [GHZ state](#quantum-memory) represented as a quantum circuit.

How can we easily prove that that quantum circuit equals the state:

$$
\frac{|000> + |111>}{\sqrt{2}}
$$

?

The naive way would be to just do the matrix multiplication as explained at [Section "Quantum computing is just matrix multiplication"](#programmer-s-model-of-quantum-computers).

However, ZX-calculus provides a simpler way.

And even more importantly, sometimes it is the only way, because in a real circuit, we would not be able to do the matrix multiplication 

What we do in ZX-calculus is we first transform the original quantum circuit into a ZX graph.

This is always possible, because we can describe how to do the conversion simply for any of the [Clifford plus T](#clifford-plus-t) gates, which is a set of [universal quantum gates](#universal-quantum-gates).

Then, after we do this transformation, we can start applying further transformations that simplify the circuit.

It has already been proven that there is no efficient algorithm for this (TODO source, someone said P-sharp complete best case)

But it has been proven in 2017 that any possible equivalence between quantum circuits can be reached by modifying ZX-calculus circuits.

There are only 7 transformation rules that we need, and all others can be derived from those, universality.

So, we can apply those rules to do [the transformation shown in Wikipedia](https://en.wikipedia.org/w/index.php?title=ZX-calculus&oldid=1071329204#Diagram_rewriting):

<a id="image-ghz-circuit-as-zx-diagram"></a>
<img src="https://upload.wikimedia.org/wikipedia/commons/0/05/GHZ_circuit_as_ZX-diagram.svg" alt="" height="500">

**[Figure 10](#image-ghz-circuit-as-zx-diagram). GHZ circuit as ZX-diagram**. [Source](https://commons.wikimedia.org/wiki/File:GHZ_circuit_as_ZX-diagram.svg).

and one of those rules finally tells us that that last graph means our desired state:

$$
\frac{|000> + |111>}{\sqrt{2}}
$$

because it is a Z spider with $m = 3$ and $n = 1$.

<a id="video-working-with-pyzx-by-aleks-kissinger-2019"></a>
**[Video 49](#video-working-with-pyzx-by-aleks-kissinger-2019). Working with PyZX by Aleks Kissinger (2019)** [Source](https://www.youtube.com/watch?v=JafI_LZts2g). This video appears to give amazing motivation on why you should care about [ZX-calculus](#zx-calculus), it mentions
- [quantum compilation](#quantum-compilation)
- [quantum computer simulation](#quantum-computer-simulator)

---

Bibliography:
- [https://quantumcomputing.stackexchange.com/questions/9774/what-are-some-applications-of-the-zx-calculus](https://quantumcomputing.stackexchange.com/questions/9774/what-are-some-applications-of-the-zx-calculus)
- [https://github.com/zxcalc/book](https://github.com/zxcalc/book) Picturing Quantum Software by [Aleks Kissinger](https://ourbigbook.com/go/topic/aleks-kissinger) and [John van de Wetering](https://ourbigbook.com/go/topic/john-van-de-wetering) (2024), [CC BY-NC-SA](law.md#cc-by-nc-sa).

### ZX-calculus biliography

↑ **Parent:** [ZX-calculus](#zx-calculus)

#### Picturing Quantum Processes

↑ **Parent:** [ZX-calculus biliography](#zx-calculus-biliography)

- [https://www.amazon.co.uk/Picturing-Quantum-Processes-Diagrammatic-Reasoning/dp/110710422X](https://www.amazon.co.uk/Picturing-Quantum-Processes-Diagrammatic-Reasoning/dp/110710422X)
- [https://www.cambridge.org/core/books/picturing-quantum-processes/1119568B3101F3A685BE832FEEC53E52](https://www.cambridge.org/core/books/picturing-quantum-processes/1119568B3101F3A685BE832FEEC53E52)
- [ISBN](literature.md#isbn)-13: 978-1107104228

### PyZX

↑ **Parent:** [ZX-calculus](#zx-calculus)

[https://github.com/Quantomatic/pyzx](https://github.com/Quantomatic/pyzx)

## Quantum state

↑ **Parent:** [Quantum computing](quantum-computing.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Quantum_state)

### Bell state

↑ **Parent:** [Quantum state](#quantum-state)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Bell_state)

One of the four following states:

$$
\begin{aligned}
\ket{\Phi^+} &= \frac{1}{\sqrt{2}} (\ket{00} &+ \ket{11})
\ket{\Phi^-} &= \frac{1}{\sqrt{2}} (\ket{00} &- \ket{11})
\ket{\Psi^+} &= \frac{1}{\sqrt{2}} (\ket{01} &+ \ket{10})
\ket{\Psi^-} &= \frac{1}{\sqrt{2}} (\ket{01} &- \ket{10})
\end{aligned}
$$

When unqualified as in "the Bell state", it generally just means $\ket{\Phi^+}$.

The Bell states are entangled and [non-separable](quantum-mechanics.md#separable-state). Intuitively, we can see that when we measure that state, the values of the first and second bit are strictly correlated. This is the hallmark of [quantum computation](quantum-computing.md): making up states where qubits are highly correlated to match a specific algorithmic answer, and opposed to uniformly random noise. For example, the [Bell state circuit](#bell-circuit) is a common [hello world](software.md#hello-world-program), e.g. it is used in the official [Qiskit hello world](#qiskit-hello-world).

#### Bell circuit

↑ **Parent:** [Bell state](#bell-state)  
🏷️ **Tags:** [Quantum circuit](#quantum-circuit)

A [quantum circuit](#quantum-circuit) which when fed with input $\ket{00}$ produces the [Bell state](#bell-state).

In [Qiskit](#qiskit) at: [qiskit/hello.py](#_file/qiskit/hello.py).

<a id="image-quantum-circuit-that-generates-the-bell-state"></a>
![](https://upload.wikimedia.org/wikipedia/commons/f/fc/The_Hadamard-CNOT_transform_on_the_zero-state.png)

**[Figure 11](#image-quantum-circuit-that-generates-the-bell-state). Quantum circuit that generates the Bell state**. [Source](https://commons.wikimedia.org/wiki/File:The_Hadamard-CNOT_transform_on_the_zero-state.png). The fundamental intuition for this circuit is as follows.

First the [Hadamard gate](#hadamard-gate) makes the first [qubit](#qubit) be in a 50/50 state.

Then, the [CNOT gate](#cnot-gate) gets controlled by that 50/50 value, and the controlled qubit also gets 50/50 chance as a result.

However, both qubits are now [entangled](quantum-mechanics.md#quantum-entanglement): the result of the second qubit depends on the result of the first one. Because:
- if the first qubit is 0, cnot is not active, and so the second qubit remains 0 as its input
- if the first qubit is 1, cnot is active, and so the second qubit is flipped to 1

---

### Greenberger-Horne-Zeilinger state

↑ **Parent:** [Quantum state](#quantum-state)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Greenberger–Horne–Zeilinger_state)

### Quantum memory

↑ **Parent:** [Quantum state](#quantum-state)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Quantum_memory)

TODO clear example and application.

[https://www.quantamagazine.org/quantum-memory-proves-exponentially-powerful-20241016/](https://www.quantamagazine.org/quantum-memory-proves-exponentially-powerful-20241016/) from [Quanta Magazine](science.md#quanta-magazine) has an incomprehensible news of something that sounds cool

## Quantum supremacy

↑ **Parent:** [Quantum computing](quantum-computing.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Quantum_supremacy)

<h3 id="google-s-2019-quantum-supremacy-claim">Google's 2019 quantum supremacy claim</h3>

↑ **Parent:** [Quantum supremacy](#quantum-supremacy)

### Quantum advantage

↑ **Parent:** [Quantum supremacy](#quantum-supremacy)

Similar to [quantum supremacy](#quantum-supremacy), but add the goal that the computation must be useful, i.e. make money or solve some open [mathematical](mathematics.md) problem, [Ciro Santilli's wife](ciro-santilli.md#ciro-santilli-s-wife) was quite excited about the possibility of finding some counter examples in [number theory](mathematics.md#number-theory) with quantum computers.

## Qubit

↑ **Parent:** [Quantum computing](quantum-computing.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Qubit)

## Quantum computer benchmark

↑ **Parent:** [Quantum computing](quantum-computing.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Quantum_computer_benchmark)

One important area of research and development of [quantum computing](quantum-computing.md) is the development of benchmarks that allow us to compare different quantum computers to decide which one is more powerful than the other.

Ideally, we would like to be able to have a single number that predicts which computer is more powerful than the other for a wide range of algorithms.

However, much like in [CPU](computer-hardware.md#central-processing-unit) benchmarking, this is a very complex problem, since different algorithms might perform differently in different architectures, making it very hard to sum up the architecture's capabilities to a single number as we would like.

The only thing that is directly comparable across computers is how two machines perform for a single algorithm, but we want a single number that is representative of many algorithms.

For example, the number of qubits would be a simple naive choice of such performance predictor number. But it is very imprecise, since other factors are also very important:
- qubit error rate
- [coherence time](#coherence-time), which determines the maximum circuit depth
- qubit connectivity. Can you only connect to 4 neighbouring qubits in a 2D plane? Or to every other qubit equally as well?

[Quantum volume](#quantum-volume) is another less naive attempt at such metric.

### Comparison of quantum computing hardware

↑ **Parent:** [Quantum computer benchmark](#quantum-computer-benchmark)

| System | Announcement date | [Type](#quantum-computer-physical-implementation) | Qubits | Average connectivity | [Coherence time](#coherence-time) | Measurements per second | Single qubit error | [CZ](#cz-gate) error |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| [Willow](#willow-quantum-computer) | 2024-12 | [superconducting](#superconducting-quantum-computing) | 105[Video 26. "Meet Willow, our state-of-the-art quantum chip by Google Quantum AI"](#video-meet-willow-quantum-computer-our-state-of-the-art-quantum-chip-by-google-quantum-ai) | 3.47[Video 26. "Meet Willow, our state-of-the-art quantum chip by Google Quantum AI"](#video-meet-willow-quantum-computer-our-state-of-the-art-quantum-chip-by-google-quantum-ai) | 68 μs[Video 26. "Meet Willow, our state-of-the-art quantum chip by Google Quantum AI"](#video-meet-willow-quantum-computer-our-state-of-the-art-quantum-chip-by-google-quantum-ai) | 63 k[Video 26. "Meet Willow, our state-of-the-art quantum chip by Google Quantum AI"](#video-meet-willow-quantum-computer-our-state-of-the-art-quantum-chip-by-google-quantum-ai) | 0.035%[Video 26. "Meet Willow, our state-of-the-art quantum chip by Google Quantum AI"](#video-meet-willow-quantum-computer-our-state-of-the-art-quantum-chip-by-google-quantum-ai) | 0.33%[Video 26. "Meet Willow, our state-of-the-art quantum chip by Google Quantum AI"](#video-meet-willow-quantum-computer-our-state-of-the-art-quantum-chip-by-google-quantum-ai) |

Other comparisons:
- [https://terra-docs.s3.us-east-2.amazonaws.com/IJHSR/Articles/volume6-issue8/IJHSR_2024_68_52.pdf](https://terra-docs.s3.us-east-2.amazonaws.com/IJHSR/Articles/volume6-issue8/IJHSR_2024_68_52.pdf) Comparison Between Different Qubit Designs for Quantum Computing by Zaichen Hao (2024)

### Algorithmic qubits

↑ **Parent:** [Quantum computer benchmark](#quantum-computer-benchmark)

Metric created by [IonQ](#ionq).

### Coherence time

↑ **Parent:** [Quantum computer benchmark](#quantum-computer-benchmark)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Coherence_time)

It takes time for the quantum state to evolve. So in order to have a deep [quantum circuit](#quantum-circuit), we need longer [coherence times](#coherence-time).

### Depth of a quantum circuit

↑ **Parent:** [Quantum computer benchmark](#quantum-computer-benchmark)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Depth_of_a_quantum_circuit)

This is an important metric, because it takes some time for the quantum operations to propagate, and so the depth of a circuit gives you an idea of how long the [coherence time](#coherence-time) a hardware needs to support a given circuit.

Bibliography:
- [https://quantumcomputing.stackexchange.com/questions/14431/whats-meant-by-the-depth-of-a-quantum-circuit](https://quantumcomputing.stackexchange.com/questions/14431/whats-meant-by-the-depth-of-a-quantum-circuit)
- [https://quantumcomputing.stackexchange.com/questions/5769/how-to-calculate-circuit-depth-properly](https://quantumcomputing.stackexchange.com/questions/5769/how-to-calculate-circuit-depth-properly)

![](https://github.com/Qiskit/qiskit/blob/0.45.1/docs/source_images/depth.gif?raw=true)

**[Figure 12](#_996)** [Source](https://github.com/Qiskit/qiskit/blob/0.45.1/docs/source\_images/depth.gif).

### Quantum volume

↑ **Parent:** [Quantum computer benchmark](#quantum-computer-benchmark)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Quantum_volume)

### Random circuit sampling

↑ **Parent:** [Quantum computer benchmark](#quantum-computer-benchmark)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Random_circuit_sampling)

[https://quantumcomputing.stackexchange.com/questions/4005/what-exactly-is-random-circuit-sampling](https://quantumcomputing.stackexchange.com/questions/4005/what-exactly-is-random-circuit-sampling)

## Quantum computing market

↑ **Parent:** [Quantum computing](quantum-computing.md)

### Quantum computing skepticism

↑ **Parent:** [Quantum computing market](#quantum-computing-market)

#### Are we in a quantum computing bubble?

↑ **Parent:** [Quantum computing skepticism](#quantum-computing-skepticism)

[https://www.reddit.com/r/QuantumComputing/comments/lf1vp2/comment/ibuukcq/?utm_source=reddit&utm_medium=web2x&context=3](https://www.reddit.com/r/QuantumComputing/comments/lf1vp2/comment/ibuukcq/?utm_source=reddit&utm_medium=web2x&context=3)

## Post-quantum cryptography

↑ **Parent:** [Quantum computing](quantum-computing.md)  
🏷️ **Tags:** [Cryptography](cryptography.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Post-quantum_cryptography)

[Encryption algorithms](cryptography.md#cryptosystem) that run on [classical computers](#classical-computer) that are expected to be resistant to [quantum computers](quantum-computing.md).

This is notably not the case of the dominant 2020 algorithms, [RSA](cryptography.md#rsa-cryptosystem) and [elliptic curve cryptography](cryptography.md#elliptic-curve-cryptography), which are provably broken by [Grover's algorithm](#grover-s-algorithm).

However, as of 2020, we [don't have any proof that any symmetric or public key algorithm is quantum resistant](#provably-quantum-secure-encryption-algorithm).

Post-quantum cryptography is the very first quantum computing thing at which people have to put money into.

The reason is that attackers would be able to store captured [ciphertext](cryptography.md#ciphertext), and then retroactively break them once and if [quantum computing](quantum-computing.md) power becomes available in the future.

There isn't a shade of a doubt that [intelligence agencies](science.md#intelligence-agency) are actively doing this as of 2020. They must have a database of how interesting a given source is, and then store as much as they can given some ammount of storage budget they have available.

A good way to explain this to [quantum computing skeptics](#quantum-computing-skepticism) is to ask them:

> If I told you there is a 5% chance that I will be able to decrypt everything you write online starting today in 10 years. Would you give me a dollar to reduce that chance to 0.5%?

Post-quantum cryptography is simply not a choice. It must be done now. Even if the risk is low, the cost would be way too great.

### Post-quantum cryptography company

↑ **Parent:** [Post-quantum cryptography](#post-quantum-cryptography)

#### CryptoNext

↑ **Parent:** [Post-quantum cryptography company](#post-quantum-cryptography-company)  
🏷️ **Tags:** [French company](company.md#french-company)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/CryptoNext)

[https://www.cryptonext-security.com/en/](https://www.cryptonext-security.com/en/)

#### PQShield

↑ **Parent:** [Post-quantum cryptography company](#post-quantum-cryptography-company)  
🏷️ **Tags:** [University of Oxford spinout company](university-of-oxford.md#university-of-oxford-spinout-company)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/PQShield)

They seem to be doing hardware acceleration for [post-quantum cryptography](#post-quantum-cryptography) algorithm.

One has to feel bad for them as they likely threw out entire chip designs over [NIST Post-Quantum Cryptography Standardization](#nist-post-quantum-cryptography-standardization) algorithm breakeges.

- 2024-06: $37M [https://techcrunch.com/2024/06/20/pqshield-secures-37m-more-for-quantum-resistant-cryptography/](https://techcrunch.com/2024/06/20/pqshield-secures-37m-more-for-quantum-resistant-cryptography/)
- 2022-01: $20M [https://techcrunch.com/2022/01/25/pqshield-raises-20m-for-its-quantum-ready-future-proof-cryptographic-security-solutions/](https://techcrunch.com/2022/01/25/pqshield-raises-20m-for-its-quantum-ready-future-proof-cryptographic-security-solutions/)

### NIST Post-Quantum Cryptography Standardization

↑ **Parent:** [Post-quantum cryptography](#post-quantum-cryptography)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/NIST_Post-Quantum_Cryptography_Standardization)

This [post-quantum cryptography](#post-quantum-cryptography) competition by [NIST](research-institute.md#national-institute-of-standards-and-technology) is a huge milestone of the field.

It was mind blowing when in 2022, after several years of selection, one of the 7 finalists was broken on a [classical computer](#classical-computer), not even in a quantum computer! [https://news.ycombinator.com/item?id=30466063](https://news.ycombinator.com/item?id=30466063) | [https://eprint.iacr.org/2022/214](https://eprint.iacr.org/2022/214) Breaking Rainbow Takes a Weekend on a Laptop by Ward Beullens. Dude announced he had a break a few days before submission: [https://twitter.com/WardBeullens/status/1492780462028300290](https://twitter.com/WardBeullens/status/1492780462028300290) On [Twitter](social-technology.md#twitter). He's so young. Epic.

Edit: and then, after the third round, things were a bit unclear, so they made a fourth round with 4 choices out of the 7 from round 3, and in August 2022 one of the four was broken again on a classic CPU!!! OMG: [https://arstechnica.com/information-technology/2022/08/sike-once-a-post-quantum-encryption-contender-is-koed-in-nist-smackdown/](https://arstechnica.com/information-technology/2022/08/sike-once-a-post-quantum-encryption-contender-is-koed-in-nist-smackdown/)

### Provably quantum secure encryption algorithm

↑ **Parent:** [Post-quantum cryptography](#post-quantum-cryptography)

None known as of 2020.

### Quantum resistant cryptosystem

↑ **Parent:** [Post-quantum cryptography](#post-quantum-cryptography)

#### Lattice-based cryptography

↑ **Parent:** [Quantum resistant cryptosystem](#quantum-resistant-cryptosystem)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Lattice-based_cryptography)

Bibliography:
- on [Quanta Magazine](science.md#quanta-magazine): [https://www.quantamagazine.org/cryptographys-future-will-be-quantum-safe-heres-how-it-will-work-20221109/](https://www.quantamagazine.org/cryptographys-future-will-be-quantum-safe-heres-how-it-will-work-20221109/) "[Cryptography](cryptography.md)’s Future Will Be Quantum-Safe. Here’s How It Will Work." (2024)

## Quantum computing outreach

↑ **Parent:** [Quantum computing](quantum-computing.md)

- [https://qosf.org](https://qosf.org)
- [https://www.qubitbyqubit.org/](https://www.qubitbyqubit.org/)
- [https://www.qsium.com/](https://www.qsium.com/)> Qsium is a student-led initiative that aims to democratise education in quantum computing. With the focus of raising 'quantum literacy' and creating a thriving quantum ecosystem through our Quantum Youth Network, we support [STEM](education.md#science-technology-engineering-and-mathematics) students in the [UK](united-kingdom.md). 
- [https://qworld.net](https://qworld.net)

### Quantum computing scholarship

↑ **Parent:** [Quantum computing outreach](#quantum-computing-outreach)

- [https://unitary.fund](https://unitary.fund)

## Quantum computing certification

↑ **Parent:** [Quantum computing](quantum-computing.md)

- [https://qworld.net/qsilver/](https://qworld.net/qsilver/)

## Quantum computing bibliography

↑ **Parent:** [Quantum computing](quantum-computing.md)

### Quantum computing report

↑ **Parent:** [Quantum computing bibliography](#quantum-computing-bibliography)

[https://quantumcomputingreport.com/](https://quantumcomputingreport.com/)

They have some amazingly long market analysis lists/tables there e.g.:
- [quantum computing players](#quantum-computing-player): [https://quantumcomputingreport.com/players/](https://quantumcomputingreport.com/players/)
- [quantum computer](quantum-computing.md) parameters: [https://quantumcomputingreport.com/qubit-count/](https://quantumcomputingreport.com/qubit-count/). TODO I think this was open in the past, but as of 2024 it was paywalled.

Some of their resources are open, others closed.

### Quantum computing news

↑ **Parent:** [Quantum computing bibliography](#quantum-computing-bibliography)

#### The Quantum Insider

↑ **Parent:** [Quantum computing news](#quantum-computing-news)

[https://thequantuminsider.com/](https://thequantuminsider.com/)

Good publication.

### Quantum computing book

↑ **Parent:** [Quantum computing bibliography](#quantum-computing-bibliography)

#### Quantum Computation and Quantum Information by Nielsen and Chuang

↑ **Parent:** [Quantum computing book](#quantum-computing-book)

[https://www.amazon.com/dp/1107002176](https://www.amazon.com/dp/1107002176)

### Quantum computing university course

↑ **Parent:** [Quantum computing bibliography](#quantum-computing-bibliography)

## 🏷️ Tagged (1)

- [TensorFlow quantum](machine-learning.md#tensorflow-quantum)

## ↑ Ancestors (6)

1. [Quantum information](technology.md#quantum-information)
2. [Information](technology.md#information)
3. [Information technology](technology.md#information-technology)
4. [Area of technology](technology.md#area-of-technology)
5. [Technology](technology.md)
6. [Ciro Santilli's Homepage](README.md)

## ← Incoming links (38)

- [Ciro Santilli's Homepage](README.md)
- [Andy Matuschak](education.md#andy-matuschak)
- [Applications of Josephson Junctions](condensed-matter-physics.md#applications-of-josephson-junctions)
- [The best articles by Ciro Santilli](articles.md)
- [BQP](computer-science.md#bqp)
- [Chemistry](chemistry.md)
- [Classical computer](#classical-computer)
- [ColdQuanta](#coldquanta)
- [Continuous-variable quantum information](#continuous-variable-quantum-information)
- [Deep tech](technology.md#deep-tech)
- [Fusion power](technology.md#fusion-power)
- [Introduction to quantum computing](#introduction-to-quantum-computing)
- [Job application by Ciro Santilli](ciro-santilli.md#job-application-by-ciro-santilli)
- [Julian Kelly](#julian-kelly)
- [Michael Nielsen](artificial-intelligence.md#michael-nielsen)
- [Microsoft](microsoft.md)
- [Microwave](photon.md#microwave)
- [Molecular biology technologies](ciro-santilli.md#molecular-biology-technologies)
- [NISQ algorithm](#nisq-algorithm)
- [Noisy intermediate-scale quantum era](#noisy-intermediate-scale-quantum-era)
- [Optical tweezers](condensed-matter-physics.md#optical-tweezers)
- [Post-quantum cryptography](#post-quantum-cryptography)
- [PsiQuantum founding myth](#psiquantum-founding-myth)
- [Quantum circuit description language](#quantum-circuit-description-language)
- [Quantum computer benchmark](#quantum-computer-benchmark)
- [Quantum computing could be the next big thing](ciro-santilli.md#quantum-computing-could-be-the-next-big-thing)
- [Quantum Computing Inc.](#quantum-computing-inc)
- [Quantum mechanics](quantum-mechanics.md)
- [Silicon photonics](photon.md#silicon-photonics)
- [Why you should give money to Ciro Santilli](sponsor.md#why-you-should-give-money-to-ciro-santilli)
- [Telecommunication](telecommunication.md)
- [Tensor product in quantum computing](#tensor-product-in-quantum-computing)
- [Two-state quantum system](quantum-mechanics.md#two-state-quantum-system)
- [OurBigBook Project Update March 2025](updates.md#ourbigbook-project-update-march-2025)
- [I ended up doing tech rather than content as usual](updates.md#ourbigbook-project-update-march-2025/i-ended-up-doing-tech-rather-than-content-as-usual)
- [Post OurBigBook job search round 2025](updates.md#post-ourbigbook-job-search-round-2025)
- [Pick few good bets and invest enough on them](what-poor-countries-have-to-do-to-get-richer.md#pick-few-good-bets)
- [Why it is hard to simulate quantum systems?](quantum-mechanics.md#why-it-is-hard-to-simulate-quantum-systems)
