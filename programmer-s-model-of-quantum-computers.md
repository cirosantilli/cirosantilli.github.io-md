<h1 id="programmer-s-model-of-quantum-computers">Programmer's model of quantum computers</h1>

↑ **Parent:** [Quantum computing](quantum-computing-split.md)  
🏷️ **Tags:** [The best articles by Ciro Santilli](articles-split.md)

This is a quick tutorial on how a [quantum computer](quantum-computing-split.md) programmer thinks about how a quantum computer works. If you know:
- what a [complex number](complex-number.md) is
- how to do [matrix multiplication](matrix-multiplication.md)
- what is a [probability](probability.md)
a concrete and precise [hello world](hello-world-program.md) operation can be understood in 30 minutes.

Although there are several [types of quantum computer](quantum-computer-physical-implementation.md) under development, there exists a single high level model that represents what most of those computers can do, and we are going to explain that model here. This model is the is the [digital quantum computer](digital-quantum-computer.md) model, which uses a [quantum circuit](quantum-circuit.md), that is made up of many [quantum gates](quantum-logic-gate.md).

Beyond that basic model, programmers only may have to consider the [imperfections of their hardware](quantum-logic-gates-are-needed-for-physical-implementation.md), but the starting point will almost always be this basic model, and tooling that automates mapping the high level model to real hardware considering those imperfections (i.e. [quantum compilers](quantum-compilation.md)) is already getting better and better.

The way quantum programmers think about a quantum computer in order to program can be described as follows:
- the input of a N qubit quantum computer is a vector of dimension N containing classic bits 0 and 1
- the quantum program, also known as circuit, is a $2^n \times 2^n$ [unitary matrix](unitary-matrix.md) of [complex numbers](complex-number.md) $Q \in \C^{2^n} \times \C^{2^n}$ that operates on the input to generate the output
- the output of a N qubit computer is also a vector of dimension N containing classic bits 0 and 1

To operate a quantum computer, you follow the [step of operation of a quantum computer](step-of-operation-of-a-quantum-computer.md):
- set the input [qubits](qubit.md) to classic input bits ([state initialization](state-initialization-quantum-computing.md))
- press a big red "RUN" button
- read the classic output bits ([readout](readout-quantum-computing.md))

Each time you do this, you are literally conducting a physical experiment of the specific [physical implementation](quantum-computer-physical-implementation.md) of the computer:
- setup your physical system to represent the classical 0/1 inputs
- let the state evolve for long enough
- measure the classical output back out
and each run as the above can is simply called "an experiment" or "a measurement".

The output comes out "instantly" in the sense that it is physically impossible to observe any intermediate state of the system, i.e. there are no clocks like in classical computers, further discussion at: [quantum circuits vs classical circuits](quantum-circuits-vs-classical-circuits.md). Setting up, running the experiment and taking the does take some time however, and this is important because you have to run the same experiment multiple times because results are probabilistic as mentioned below.

Unlike in a classical computer, the output of a quantum computer is not deterministic however.

But the each output is not equally likely either, otherwise the computer would be useless except as [random number generator](random-number-generation.md)!

This is because the probabilities of each output for a given input depends on the program ([unitary matrix](unitary-matrix.md)) it went through.

Therefore, what we have to do is to design the quantum circuit in a way that the right or better answers will come out more likely than the bad answers.

We then calculate the error bound for our circuit based on its design, and then determine how many times we have to run the experiment to reach the desired accuracy.

The probability of each output of a quantum computer is derived from the input and the circuit as follows.

First we take the classic input vector of dimension N of 0's and 1's and convert it to a "[quantum state vector](quantum-state-vector.md)" $\va{q_{in}}$ of dimension $2^n$:

$$
\va{q_{in}} \in \C^{2^n}
$$

We are after all going to multiply it by the program matrix, as you would expect, and that has dimension $2^n \times 2^n$!

Note that this initial transformation also transforms the discrete zeroes and ones into [complex numbers](complex-number.md).

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

Now that we finally have our quantum state vector, we just multiply it by the [unitary matrix](unitary-matrix.md) $Q$ of the quantum circuit, and obtain the $2^n$ dimensional output quantum state vector $\va{q_{out}}$:

$$
\va{q_{out}} = Q \: \va{q_{in}}
$$

And at long last, the probability of each classical outcome of the measurement is proportional to the square of the length of each entry in the quantum vector, analogously to what is done in the [Schrödinger equation](schrodinger-equation.md).

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

Keep in mind that the [quantum state vector](quantum-state-vector.md) can also contain [complex numbers because we are doing quantum mechanics](why-are-complex-numbers-used-in-the-schrodinger-equation.md), but we just take their magnitude in that case, e.g. the following quantum state would lead to the same probabilities as the previous one:

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

As we could see, this model is was simple to understand, being only marginally more complex than that of a classical computer, see also: [https://quantumcomputing.stackexchange.com/questions/6639/is-my-background-sufficient-to-start-quantum-computing/14317#14317](https://quantumcomputing.stackexchange.com/questions/6639/is-my-background-sufficient-to-start-quantum-computing/14317#14317) The situation of quantum computers today in the 2020's is somewhat analogous to that of the early days of classical circuits and computers in the 1950's and 1960's, before [CPU](central-processing-unit.md) came along and software ate the world. Even though the [exact physics of a classical computer](semiconductor-device-fabrication.md) might be hard to understand and vary across different types of [integrated circuits](integrated-circuit.md), those early hardware pioneers (and to this day modern CPU designers), can usefully view circuits from a higher level point of view, thinking only about concepts such as:
- [logic gates](logic-gate.md) like AND, NOR and NOT
- a clock + registers
as modelled at the [register transfer level](register-transfer-level.md), and only in a separate compilation step translated into actual chips. This high level understanding of how a classical computer works is what we can call "the programmer's model of a classical computer". So we are now going to describe the quantum analogue of it.

Bibliography:
- [https://arxiv.org/pdf/1804.03719.pdf](https://arxiv.org/pdf/1804.03719.pdf) Quantum Algorithm Implementations for Beginners by Abhijith et al. 2020

## ↑ Ancestors (7)

1. [Quantum computing](quantum-computing-split.md)
2. [Quantum information](quantum-information.md)
3. [Information](information.md)
4. [Information technology](information-technology.md)
5. [Area of technology](area-of-technology.md)
6. [Technology](technology-split.md)
7. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (1)

- [Introduction to quantum computing](introduction-to-quantum-computing.md)
