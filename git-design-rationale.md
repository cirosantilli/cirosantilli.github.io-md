# Git design rationale

↑ **Parent:** [Git](git.md)

The fundamental insight of Git design is: a [SHA](secure-hash-algorithms.md) represents not only current state, but also the full history due to the [Merkle tree](merkle-tree.md) implementation, see notably:

This makes it so that you will always notice if you are overwriting history on the remote, even if you are developing from two separate local computers (or more commonly, two people in two different local computers) and therefore will never lose any work accidentally.

It is very hard to achieve that without the [Merkle tree](merkle-tree.md).

Consider for example the most naive approach possible of marking versions with consecutive numbers:
- Local 1:
  - 0: root commit
  - 1: commit 1
  - 2: commit 2 by local 1
- Local 2:
  - 0: root commit
  - 1: commit 1
  - 2: commit 2 by local 2
  - 3: commit 3 by local 2
- Remote
  - 0: root commit
  - 1: commit 1

If Local 1 were to push to Remote first, how could Local 2 notice that when it tries to push itself? The navie method of just checking: "does Remote have commit "2"" does not work, because Local 2 has a different version of commit 2 than local 1.

## ↑ Ancestors (9)

1. [Git](git.md)
2. [List of version control systems](list-of-version-control-systems.md)
3. [Version control](version-control.md)
4. [Software](software-split.md)
5. [Computer](computer-split.md)
6. [Information technology](information-technology.md)
7. [Area of technology](area-of-technology.md)
8. [Technology](technology-split.md)
9. [Ciro Santilli's Homepage](split.md)
