<h1 id="it-s-not-a-tree-it-s-actually-a-dag">It's not a tree, it's actually a DAG</h1>

↑ **Parent:** [Git tips](../git-tips-split.md)

Every [tree](../tree-data-structure.md) is a [directed acyclic graph](../directed-acyclic-graph.md).

But not every [directed acyclic graph](../directed-acyclic-graph.md) is a tree.

Example of a tree (and therefore also a DAG):
```
5
|
4 7
| |
3 6
|/
2
|
1
```
Convention in this presentation: arrows implicitly point up, just like in a `git log`, i.e.:
- 1 is parent of 2
- 2 is parent of 3 and 6
- 3 is parent of 4
and so on.

Example of a DAG that is not a tree:
```
7
|\
4 6
| |
3 5
|/
2
|
1
```
This is not a tree because there are two ways to reach 7:
- 2, 3, 4, 7
- 2, 5, 6, 7

But we often say "tree" intead of "DAG" in the context of Git because DAG sounds ugly.

Example of a graph that is not a DAG:
```
6
^
|
3->4
^  |
|  v
2<-5
^
|
1
```
This one is not acyclic because there is a cycle 2, 3, 4, 5, 2.

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
