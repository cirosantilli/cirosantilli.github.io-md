# Linear history vs branching

↑ **Parent:** [Git tips](../git-tips-split.md)

<a id="_27"></a>
There are two ways to organize a project:<a id="_28"></a>

<a id="_29"></a>
- linear history
<a id="_30"></a>
- branched history: history with merge commits

<a id="_31"></a>
Some people like merges, but they are ugly and stupid. Rebase instead and keep linear history.

<a id="_32"></a>
Linear history:<a id="_33"></a>

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

<a id="_34"></a>
Branched history:<a id="_35"></a>

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

<a id="_36"></a>
Here commits 6 and 7 are the so called "merge commits":<a id="_37"></a>

<a id="_38"></a>
- they have multiple parents:<a id="_39"></a>

  <a id="_40"></a>
  - 6 has parents 3 and 4
  <a id="_41"></a>
  - 7 has parents 5 and 6
<a id="_42"></a>
- they are useless and don't contain any real information

<a id="_43"></a>
Which type of tree do you think will be easier to understand and maintain?

<a id="_44"></a>
????

<a id="_45"></a>
????????????

<a id="_46"></a>
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
