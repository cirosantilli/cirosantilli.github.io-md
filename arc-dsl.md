# ARC-DSL

↑ **Parent:** [ARC-AGI implementation](arc-agi-implementation.md)

[https://github.com/michaelhodel/arc-dsl](https://github.com/michaelhodel/arc-dsl)

This interesting repo defines a set of input transformations that can be composed together into programs to generate the solve ARC problems.

It does not appear to have any [program synthesis](automatic-programming.md): it only defines the DSL and then provides manual solutions to the problems.

The README is lacking as usual, an overview of the files is:
- [dsl.py](https://github.com/michaelhodel/arc-dsl/blob/635de4902a5fb4e376f27333feaa396d3f5dfdcb/dsl.py): defines the transformations as Python functions
- [solvers.py](https://github.com/michaelhodel/arc-dsl/blob/635de4902a5fb4e376f27333feaa396d3f5dfdcb/solvers.py): defines solvers for the 400 [ARC-AGI-1 training problems](arc-agi-1-problem/train.md)

Intended usage to run the solvers seems to be:
```
git clone https://github.com/fchollet/ARC-AGI
cd ARC-AGI
git checkout 399030444e0ab0cc8b4e199870fb20b863846f34
git clone https://github.com/michaelhodel/arc-dsl
cd arc-dsl
git checkout 635de4902a5fb4e376f27333feaa396d3f5dfdcb
python main.py
```
Unfortunately this blows up on [Ubuntu 25.04](ubuntu-25-04.md) on `test_mpapply` apparently due to a [Python 3.12](python-3-12.md) issue and the pull request [https://github.com/michaelhodel/arc-dsl/pull/7](https://github.com/michaelhodel/arc-dsl/pull/7) has been ignored for more than one year, so the project is largely dead.

## ↑ Ancestors (12)

1. [ARC-AGI implementation](arc-agi-implementation.md)
2. [ARC-AGI](arc-agi.md)
3. [AGI test](agi-test.md)
4. [Artificial general intelligence](artificial-general-intelligence.md)
5. [AI by capability](ai-by-capability.md)
6. [Artificial intelligence](artificial-intelligence-split.md)
7. [Machine learning](machine-learning-split.md)
8. [Computer](computer-split.md)
9. [Information technology](information-technology.md)
10. [Area of technology](area-of-technology.md)
11. [Technology](technology-split.md)
12. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (4)

- [Primitive](arc-agi-2-problem/primitive.md)
- [ARC-DSL-2](arc-dsl-2.md)
- [Re-arc](re-arc.md)
- [ARC-AGI-2](updates/arc-agi-2.md)
