# Merge two or more commits into one

↑ **Parent:** [Git rebase 101](git-rebase-101.md)

Before
```
7 my-feature HEAD
|
6
|
5 master
|
4
|
3
|
2
|
1
```

Oh, commit 6 was just a temporary step, should be put together with commit 7:
```
git rebase -i HEAD~2
```

Mark `6` to be squashed.

After:
```
67 my-feature HEAD
|
5 master
|
4
|
3
|
2
|
1
```
Better now, ready to push.

## ↑ Ancestors (12)

1. [Git rebase 101](git-rebase-101.md)
2. [How to modify the commit tree](how-to-modify-the-commit-tree.md)
3. [Git tips](../git-tips-split.md)
4. [Git](../git.md)
5. [List of version control systems](../list-of-version-control-systems.md)
6. [Version control](../version-control.md)
7. [Software](../software-split.md)
8. [Computer](../computer-split.md)
9. [Information technology](../information-technology.md)
10. [Area of technology](../area-of-technology.md)
11. [Technology](../technology-split.md)
12. [Ciro Santilli's Homepage](../split.md)
