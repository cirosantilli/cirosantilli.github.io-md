# Busy beaver

↑ **Parent:** [Halting problem](halting-problem.md)  
🏷️ **Tags:** [Function problem](function-problem.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Busy_beaver)

The busy beaver game consists in finding, for a given $n$, the turing machine with $n$ states that writes the largest possible number of 1's on a tape initially filled with 0's. In other words, computing the [busy beaver function](busy-beaver-function.md) for a given $n$.

There are only finitely many Turing machines with $n$ states, so we are certain that there exists such a maximum. Computing the [Busy beaver function](busy-beaver-function.md) for a given $n$ then comes down to solving the halting problem for every single machine with $n$ states.

Some variant definitions define it as the number of time steps taken by the machine instead. Wikipedia talks about their relationship, but no patience right now.

The Busy Beaver problem is cool because it puts the [halting problem](halting-problem.md) in a more precise numerical light, e.g.:
- the [Busy beaver function](busy-beaver-function.md) is the most obvious [uncomputable function](uncomputable-function.md) one can come up with starting from the [halting problem](halting-problem.md)
- the [Busy beaver scale](busy-beaver-scale.md) allows us to gauge the difficulty of proving certain (yet unproven!) mathematical [conjectures](conjecture.md)

Bibliography:
- [https://www.scottaaronson.com/blog/?p=4916](https://www.scottaaronson.com/blog/?p=4916)
- [https://www.quantamagazine.org/the-busy-beaver-game-illuminates-the-fundamental-limits-of-math-20201210](https://www.quantamagazine.org/the-busy-beaver-game-illuminates-the-fundamental-limits-of-math-20201210)

**Table of contents**

- [Step busy beaver](step-busy-beaver.md)
- [Busy beaver function](busy-beaver-function.md)
  - [Specific values of the Busy beaver function](specific-values-of-the-busy-beaver-function.md)
    - [Turing machine acceleration](turing-machine-acceleration.md)
    - [Busy Beaver Challenge](busy-beaver-challenge.md)
    - [BB(5)](bb-5.md)
      - [Marxen-Buntrock machine](marxen-buntrock-machine.md)
      - [Skelet’s machines](skelet%E2%80%99s-machines.md)
        - [Skelet machine \#1](skelet-machine-1.md)
          - [Skelet machine \#1 is infinite](skelet-machine-1-is-infinite.md)
    - [BB(6)](bb-6.md)
      - [BB(6) is hard](bb-6-is-hard.md)
        - [Antihydra](antihydra.md)
          - [Antihydra in Magic: The Gathering](antihydra-in-magic-the-gathering.md)
          - [Antihydra GMP implementation](antihydra-gmp-implementation.md)
          - [gmp/antihydra.c](_file/gmp/antihydra.c.md)
- [Busy beaver scale](busy-beaver-scale.md)
  - [Turing machine compiler](turing-machine-compiler.md)
  - [Automated theorem proving by halting problem reduction](automated-theorem-proving-by-halting-problem-reduction.md)
    - [Conjecture reduction to a halting problem](conjecture-reduction-to-a-halting-problem.md)
      - [Turing machine that halts if and only if the Goldbach conjecture is false](turing-machine-that-halts-if-and-only-if-the-goldbach-conjecture-is-false.md)
      - [Turing machine that halts if and only if Collatz conjecture is false](turing-machine-that-halts-if-and-only-if-collatz-conjecture-is-false.md)

## ↑ Ancestors (9)

1. [Halting problem](halting-problem.md)
2. [Decision problem](decision-problem.md)
3. [Computational problem](computational-problem.md)
4. [Computer science](computer-science-split.md)
5. [Computer](computer-split.md)
6. [Information technology](information-technology.md)
7. [Area of technology](area-of-technology.md)
8. [Technology](technology-split.md)
9. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (1)

- [Marxen-Buntrock machine](marxen-buntrock-machine.md)
