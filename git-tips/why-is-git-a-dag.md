# Why is Git a DAG?

↑ **Parent:** [Git tips](../git-tips-split.md)

<a id="_24"></a>
Because a Git commit can have more than 1 parent due to merge commits when you do:<a id="_25"></a>

```
git merge
```

<a id="_26"></a>
It can even have more than 2, there's no limit. Although that is not so common (with good reason, 2 is already one too many): [https://softwareengineering.stackexchange.com/questions/314215/can-a-git-commit-have-more-than-2-parents/377903#377903](https://softwareengineering.stackexchange.com/questions/314215/can-a-git-commit-have-more-than-2-parents/377903#377903)

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
