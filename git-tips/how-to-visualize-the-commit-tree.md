# How to visualize the commit tree

↑ **Parent:** [Git tips](../git-tips-split.md)

<a id="_47"></a>
Generate a minimal test repo. You should get in the habit of doing this to test stuff out.<a id="_48"></a>

```
#!/usr/bin/env bash

mkdir git-tips
cd git-tips
git init

for i in 1 2 3 4 5; do
  echo $i > f
  git add f
  git commit -m $i
done

git checkout HEAD~2
git checkout -b my-feature

for i in 6 7; do
  echo $i > f
  git add f
  git commit -m $i
done
```

**Table of contents**

- [gitk](gitk.md)
- [`git log --graph`](git-log-graph.md)

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
