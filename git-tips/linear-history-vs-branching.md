# Linear history vs branching

↑ **Parent:** [Git tips](../git-tips-split.md)

There are two ways to organize a project:
- linear history
- branched history: history with merge commits

Some people like merges, but they are ugly and stupid. Rebase instead and keep linear history.

Linear history:
```
5 master
|
4
|
3
|
2
|
1 first commit
```

Branched history:
```
7   master
|\
| \
6  \
|\  \
| |  |
3 4  5
| |  |
| /  /
|/  /
2  /
| /
1/  first commit
```

Here commits 6 and 7 are the so called "merge commits":
- they have multiple parents:
  - 6 has parents 3 and 4
  - 7 has parents 5 and 6
- they are useless and don't contain any real information

Which type of tree do you think will be easier to understand and maintain?

????

????????????

You may disconnect now if you still like branched history.

## ↑ Ancestors (10)

1. [Git tips](../git-tips-split.md)
2. [Git](../git.md)
3. [List of version control systems](../list-of-version-control-systems.md)
4. [Version control](../version-control.md)
5. [Software](../software-split.md)
6. [Computer](../computer-split.md)
7. [Information technology](../information-technology.md)
8. [Area of technology](../area-of-technology.md)
9. [Technology](../technology-split.md)
10. [Ciro Santilli's Homepage](../split.md)
