# git rebase moves commits one by one

↑ **Parent:** [Merge conflicts](merge-conflicts.md)

<a id="_93"></a>
In order to solve conflicts, you just have to understand what commit you are trying to move where.

<a id="_94"></a>
E.g. if from:<a id="_95"></a>

```
5 master
|
4 7 my-feature HEAD
| |
3 6
|/
2
|
1
```
we do:<a id="_96"></a>

```
git rebase master
```
what happens step by step is first 6 is moved on top of 5:<a id="_97"></a>

```
6on5 HEAD
|
5 master
|
4                 7 my-feature
|                 |
3                 6
|                 |
2-----------------+
|
1
```
and then 7 is moved on top of the new 6:<a id="_98"></a>

```
7on5 HEAD
|
6on5
|
5 master
|
4                 7 my-feature
|                 |
3                 6
|                 |
2-----------------+
|
1
```

<a id="_99"></a>
All good? so OK, let's move the `my-feature` to the new 7:

<a id="_100"></a>
```
7on5 my-feature HEAD
|
6on5
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
