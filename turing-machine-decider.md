# Turing machine decider

↑ **Parent:** [Halting problem](halting-problem.md)

A [Turing machine](turing-machine.md) decider is a program that decides if one or more [Turing machines](turing-machine.md) halts of not.

Of course, because what we know about the [halting problem](halting-problem.md), there cannot exist a single decider that decides all [Turing machines](turing-machine.md).

E.g. [The Busy Beaver Challenge](busy-beaver-challenge.md) has a set of deciders clearly published, which decide a large part of [BB(5)](bb-5.md). Their proposed deciders are listed at: [https://discuss.bbchallenge.org/c/deciders/5](https://discuss.bbchallenge.org/c/deciders/5) and actually applied ones at: [https://bbchallenge.org](https://bbchallenge.org).

But there are deciders that can decide large classes of turing machines.

Many (all/most?) deciders are based on simulation of machines with arbitrary cutoff [hyperparameters](hyperparameter.md), e.g. the cutoff space/time of a [Turing machine cycler decider](cycler-turing-machine.md).

The simplest and most obvious example is the [Turing machine cycler decider](cycler-turing-machine.md)

**Table of contents**

- [Turing machine regex tape notation](turing-machine-regex-tape-notation.md)
- [Cycler Turing machine](cycler-turing-machine.md)
- [Translated cycler Turing machine](translated-cycler-turing-machine.md)
- [Closed Tape Language decider](closed-tape-language-decider.md)

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

## ← Incoming links (2)

- [Automated theorem proving by halting problem reduction](automated-theorem-proving-by-halting-problem-reduction.md)
- [Busy beaver scale](busy-beaver-scale.md)
