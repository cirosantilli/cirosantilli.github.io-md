# Cycler Turing machine

↑ **Parent:** [Turing machine decider](turing-machine-decider.md)

Bibliography: [https://discuss.bbchallenge.org/t/decider-cyclers/33](https://discuss.bbchallenge.org/t/decider-cyclers/33)

Example: [https://bbchallenge.org/279081](https://bbchallenge.org/279081).

These are very simple, they just check for exact state repetitions, which obviously imply that they will run forever.

Unfortunately, cyclers may need to run through an initial setup phase before reaching the initial cycle point, which is not very elegant.

Also, we have no way of knowing the initial setup length of the actual cycle length, so we just need an arbitrary cutoff value.

And unfortunately, this can lead to misses, e.g. [Skelet machine \#1](skelet-machine-1.md), a 5 state machine, has a (translated) cycle that starts at around 50-200M steps, and takes 8 trillion steps to repeat.

## ↑ Ancestors (10)

1. [Turing machine decider](turing-machine-decider.md)
2. [Halting problem](halting-problem.md)
3. [Decision problem](decision-problem.md)
4. [Computational problem](computational-problem.md)
5. [Computer science](computer-science-split.md)
6. [Computer](computer-split.md)
7. [Information technology](information-technology.md)
8. [Area of technology](area-of-technology.md)
9. [Technology](technology-split.md)
10. [Ciro Santilli's Homepage](split.md)
