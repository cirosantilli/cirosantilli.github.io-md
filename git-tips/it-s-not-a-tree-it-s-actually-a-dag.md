<h1 id="it-s-not-a-tree-it-s-actually-a-dag">It's not a tree, it's actually a DAG</h1>

↑ **Parent:** [Git tips](../git-tips-split.md)

<a id="_8"></a>
Every [tree](../tree-data-structure.md) is a [directed acyclic graph](../directed-acyclic-graph.md).

<a id="_9"></a>
But not every [directed acyclic graph](../directed-acyclic-graph.md) is a tree.

<a id="_10"></a>
Example of a tree (and therefore also a DAG):<a id="_11"></a>

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
Convention in this presentation: arrows implicitly point up, just like in a `git log`, i.e.:<a id="_12"></a>

<a id="_13"></a>
- 1 is parent of 2
<a id="_14"></a>
- 2 is parent of 3 and 6
<a id="_15"></a>
- 3 is parent of 4
and so on.

<a id="_16"></a>
Example of a DAG that is not a tree:<a id="_17"></a>

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
This is not a tree because there are two ways to reach 7:<a id="_18"></a>

<a id="_19"></a>
- 2, 3, 4, 7
<a id="_20"></a>
- 2, 5, 6, 7

<a id="_21"></a>
But we often say "tree" intead of "DAG" in the context of Git because DAG sounds ugly.

<a id="_22"></a>
Example of a graph that is not a DAG:<a id="_23"></a>

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
