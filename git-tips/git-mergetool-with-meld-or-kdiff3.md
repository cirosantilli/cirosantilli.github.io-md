# `git mergetool` with `meld` or `kdiff3`

↑ **Parent:** [Conflict resolution tool](conflict-resolution-tool.md)

<a id="_130"></a>
These are good free newbie GUI options:<a id="_131"></a>

```
sudo apt install meld
git mergetool --tool meld

sudo apt install kdiff3
git mergetool --tool kdiff3
```

<a id="_132"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/meld.png" alt="" height="500">

<a id="_133"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/kdiff3.png" alt="" height="500">

<a id="_134"></a>
Let's make a more interesting conflict:

<a id="_135"></a>
git-tips-2.sh<a id="_136"></a>

```
#!/usr/bin/env bash

set -eux

add() (
  rm -f f
  for i in `seq 10`; do
    printf "before $i\n\n" >> f
  done
  printf "conflict 1 $1\n\n" >> f
  for i in `seq 10`; do
    printf "middle $i\n\n" >> f
  done
  printf "conflict 2 $2\n\n" >> f
  for i in `seq 10`; do
    printf "after $i\n\n" >> f
  done
  git add f
)

rm -rf git-tips-2
mkdir git-tips-2
cd git-tips-2
git init

for i in 1 2 3; do
  add $i $i
  git commit -m $i
done

add 3 4
git commit -m 4

add 5 4
git commit -m 5

git checkout HEAD~2
git checkout -b my-feature

add 3 6
git commit -m 6

add 7 6
git commit -m 7
```

## ↑ Ancestors (12)

1. [Conflict resolution tool](conflict-resolution-tool.md)
2. [Merge conflicts](merge-conflicts.md)
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
