<h1 id="git-log-graph"><code>git log --graph</code></h1>

↑ **Parent:** [How to visualize the commit tree](how-to-visualize-the-commit-tree.md)

<a id="_54"></a>
For the strong.

<a id="_55"></a>
```
git log --abbrev-commit --decorate --graph --pretty=oneline master HEAD
```

<a id="_56"></a>
Output:<a id="_57"></a>

```
* b4ec057 (master) 5
* 0b37c1b 4
| * fbfbfe8 (HEAD -> my-feature) 7
| * 7b0f59d 6
|/
* 661cfab 3
* 6d748a9 2
* c5f8a2c 1
```

<a id="_58"></a>
If we also add the `--simplify-by-decoration`, which you very often want want on a real repository with many commits:<a id="_59"></a>

```
* b4ec057 (master) 5
| * fbfbfe8 (HEAD -> my-feature) 7
|/
* c5f8a2c 1
```
As we can see, this removes any commit that is neither:<a id="_60"></a>

<a id="_61"></a>
- under a branch or tag
<a id="_62"></a>
- at the intersection of too branches or tags

## ↑ Ancestors (11)

1. [How to visualize the commit tree](how-to-visualize-the-commit-tree.md)
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
