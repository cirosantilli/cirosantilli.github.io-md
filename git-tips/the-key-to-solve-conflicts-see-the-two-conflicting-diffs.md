# The key to solve conflicts: see the two conflicting diffs

↑ **Parent:** [Merge conflicts](merge-conflicts.md)

The key to solve conflicts is:

> You have to understand what are the two commits that touched a given line (one from master, one from features), and then combine them somehow.

Or in other words, at every rebase conflict we have something like:
```
master-commit    feature-commit
|                |
|                |
base-commit------+
|
|
```
Therefore there are 2 diffs that you have to understand and reconcile:
- `base-commit` to `master-commit`
- `base-commit` to `feature-commit`

## ↑ Ancestors (11)

1. [Merge conflicts](merge-conflicts.md)
2. [Git tips](../git-tips-split.md)
3. [Git](../git.md)
4. [List of version control systems](../list-of-version-control-systems.md)
5. [Version control](../version-control.md)
6. [Software](../software-split.md)
7. [Computer](../computer-split.md)
8. [Information technology](../information-technology.md)
9. [Area of technology](../area-of-technology.md)
10. [Technology](../technology-split.md)
11. [Ciro Santilli's Homepage](../split.md)
