# Busy beaver scale

↑ **Parent:** [Busy beaver](busy-beaver.md)

The [Busy beaver scale](busy-beaver-scale.md) allows us to gauge the difficulty of proving certain (yet unproven!) mathematical [conjectures](conjecture.md)!

To to this, people have reduced certain mathematical problems to deciding the [halting problem](halting-problem.md) of a specific [Turing machine](turing-machine.md).

A good example is perhaps the [Goldbach's conjecture](goldbach-s-conjecture.md). We just make a [Turing machine](turing-machine.md) that successively checks for each even number of it is a sum of two primes by naively looping down and trying every possible pair. Let the machine halt if the check fails. So this machine halts [iff](if-and-only-if.md) the [Goldbach's conjecture](goldbach-s-conjecture.md) is false! See also [Conjecture reduction to a halting problem](conjecture-reduction-to-a-halting-problem.md).

Therefore, if we were able to compute $BB(n)$, we would be able to prove those conjectures automatically, by letting the machine run up to $BB(n)$, and if it hadn't halted by then, we would know that it would never halt.

Of course, in practice, $BB$ is generally [uncomputable](computable-problem.md), so we will never know it. And furthermore, even if it were computable, it would take a lot longer than the age of the universe to compute any of it, so it would be useless.

However, philosophically speaking at least, the number of states of the equivalent [Turing machine](turing-machine.md) gives us a philosophical idea of the complexity of the problem.

The [busy beaver scale](busy-beaver-scale.md) is likely mostly useless, since we are able to prove that many non-trivial [Turing machines](turing-machine.md) do halt, often by reducing problems to simpler known cases. But still, it is cute.

But maybe, just maybe, reduction to Turing machine form could be useful. E.g. [The Busy Beaver Challenge](busy-beaver-challenge.md) and other attempts to solve [BB(5)](bb-5.md) have come up with large number of automated (usually parametrized up to a certain threshold) [Turing machine decider](turing-machine-decider.md) programs that automatically determine if certain (often large numbers of) Turing machines run forever.

So it it not impossible that after some reduction to a standard [Turing machine](turing-machine.md) form, some conjecture just gets automatically brute-forced by one of the deciders, this is a path to

**Table of contents**

- [Turing machine compiler](turing-machine-compiler.md)
- [Automated theorem proving by halting problem reduction](automated-theorem-proving-by-halting-problem-reduction.md)
  - [Conjecture reduction to a halting problem](conjecture-reduction-to-a-halting-problem.md)
    - [Turing machine that halts if and only if the Goldbach conjecture is false](turing-machine-that-halts-if-and-only-if-the-goldbach-conjecture-is-false.md)
    - [Turing machine that halts if and only if Collatz conjecture is false](turing-machine-that-halts-if-and-only-if-collatz-conjecture-is-false.md)

## ↑ Ancestors (10)

1. [Busy beaver](busy-beaver.md)
2. [Halting problem](halting-problem.md)
3. [Decision problem](decision-problem.md)
4. [Computational problem](computational-problem.md)
5. [Computer science](computer-science-split.md)
6. [Computer](computer-split.md)
7. [Information technology](information-technology.md)
8. [Area of technology](area-of-technology.md)
9. [Technology](technology-split.md)
10. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (5)

- [Automated theorem proving by halting problem reduction](automated-theorem-proving-by-halting-problem-reduction.md)
- [BB(5)](bb-5.md)
- [Busy beaver](busy-beaver.md)
- [Busy beaver scale](busy-beaver-scale.md)
- [Erdős' conjecture on powers of 2](erdos-conjecture-on-powers-of-2.md)
