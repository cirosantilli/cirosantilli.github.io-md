# Git tips

↑ **Parent:** [Git](software.md#git)

<a id="_1"></a>
This is a quick presentation that goes over some of the most common difficulties people find with [Git](software.md#git).

**Table of contents**

- [Understand the commit tree](#understand-the-commit-tree)
- [It's not a tree, it's actually a DAG](#it-s-not-a-tree-it-s-actually-a-dag)
- [Why is Git a DAG?](#why-is-git-a-dag)
- [Linear history vs branching](#linear-history-vs-branching)
- [How to visualize the commit tree](#how-to-visualize-the-commit-tree)
  - [gitk](#gitk)
  - [`git log --graph`](#git-log-graph)
- [How to modify the commit tree](#how-to-modify-the-commit-tree)
  - [git rebase 101](#git-rebase-101)
    - [Move your branch on top of newest master](#move-your-branch-on-top-of-newest-master)
    - [Modify contents of an old commit in your branch](#modify-contents-of-an-old-commit-in-your-branch)
    - [Merge two or more commits into one](#merge-two-or-more-commits-into-one)
- [Oh, but there are 2 trees: local and remote](#oh-but-there-are-2-trees-local-and-remote)
- [Merge conflicts](#merge-conflicts)
  - [git rebase moves commits one by one](#git-rebase-moves-commits-one-by-one)
  - [The key to solve conflicts: see the two conflicting diffs](#the-key-to-solve-conflicts-see-the-two-conflicting-diffs)
  - [Conflict resolution tool](#conflict-resolution-tool)
    - [`diff3`](#diff3)
    - [`git mergetool` with `meld` or `kdiff3`](#git-mergetool-with-meld-or-kdiff3)
    - [But which commit from master did we conflict with exactly?](#but-which-commit-from-master-did-we-conflict-with-exactly)

## Understand the commit tree

↑ **Parent:** [Git tips](git-tips.md)

<a id="_2"></a>
This is the most important thing to understand Git!

<a id="_3"></a>
You must:<a id="_4"></a>

<a id="_5"></a>
- be able to visualize the commit tree
<a id="_6"></a>
- understand how each git command modifies the commit DAG

<h2 id="it-s-not-a-tree-it-s-actually-a-dag">It's not a tree, it's actually a DAG</h2>

↑ **Parent:** [Git tips](git-tips.md)

<a id="_8"></a>
Every [tree](mathematics.md#tree-data-structure) is a [directed acyclic graph](mathematics.md#directed-acyclic-graph).

<a id="_9"></a>
But not every [directed acyclic graph](mathematics.md#directed-acyclic-graph) is a tree.

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

## Why is Git a DAG?

↑ **Parent:** [Git tips](git-tips.md)

<a id="_24"></a>
Because a Git commit can have more than 1 parent due to merge commits when you do:<a id="_25"></a>

```
git merge
```

<a id="_26"></a>
It can even have more than 2, there's no limit. Although that is not so common (with good reason, 2 is already one too many): [https://softwareengineering.stackexchange.com/questions/314215/can-a-git-commit-have-more-than-2-parents/377903#377903](https://softwareengineering.stackexchange.com/questions/314215/can-a-git-commit-have-more-than-2-parents/377903#377903)

## Linear history vs branching

↑ **Parent:** [Git tips](git-tips.md)

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

## How to visualize the commit tree

↑ **Parent:** [Git tips](git-tips.md)

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

### gitk

↑ **Parent:** [How to visualize the commit tree](#how-to-visualize-the-commit-tree)

<a id="_49"></a>
For the newbs.

<a id="_50"></a>
Slick? No. But [gitk](#gitk) does the job, like any one of the other 100 billion free [Git UI](software.md#git-ui) viewers out there

<a id="_51"></a>
```
gitk master HEAD
```

<a id="_52"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/gitk.png" alt="" height="500">

<a id="_53"></a>
Many [IDEs](software.md#integrated-development-environment) are also implementing this now (e.g. [VS Code](software.md#visual-studio-code), [Eclipse](software.md#eclipse-ide). Most free IDE GIt implementations are still crap, but that is the future, because you want to edit, view history, edit, view history, commit, edit.

<h3 id="git-log-graph"><code>git log --graph</code></h3>

↑ **Parent:** [How to visualize the commit tree](#how-to-visualize-the-commit-tree)

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

## How to modify the commit tree

↑ **Parent:** [Git tips](git-tips.md)

<a id="_63"></a>
Option 1) `git commit`. Doh!!!

<a id="_64"></a>
Option 2) `git rebase`. Basically allows you to do arbitrary modifications to the tree. The most important ones are:

### git rebase 101

↑ **Parent:** [How to modify the commit tree](#how-to-modify-the-commit-tree)

#### Move your branch on top of newest master

↑ **Parent:** [Git rebase 101](#git-rebase-101)

<a id="_65"></a>
Before:<a id="_66"></a>

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

<a id="_67"></a>
Action:<a id="_68"></a>

```
git rebase
```

<a id="_69"></a>
After:<a id="_70"></a>

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
Ready to push with linear history!

#### Modify contents of an old commit in your branch

↑ **Parent:** [Git rebase 101](#git-rebase-101)

<a id="_71"></a>
Before:<a id="_72"></a>

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

<a id="_73"></a>
Oh, commit 6 was crap:<a id="_74"></a>

```
git rebase -i HEAD~2
```

<a id="_75"></a>
Mark `6` to be modified.

<a id="_76"></a>
After:<a id="_77"></a>

```
7 my-feature HEAD
|
6v2
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

<a id="_78"></a>
Note: history changes change all commits SHAs. All parents are considereEven time is considered. So is commit message/author. And obviously file contents. So now commit "7" will actually have a different SHA.

#### Merge two or more commits into one

↑ **Parent:** [Git rebase 101](#git-rebase-101)

<a id="_79"></a>
Before<a id="_80"></a>

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

<a id="_81"></a>
Oh, commit 6 was just a temporary step, should be put together with commit 7:<a id="_82"></a>

```
git rebase -i HEAD~2
```

<a id="_83"></a>
Mark `6` to be squashed.

<a id="_84"></a>
After:<a id="_85"></a>

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

## Oh, but there are 2 trees: local and remote

↑ **Parent:** [Git tips](git-tips.md)

<a id="_86"></a>
Oh but there are usually 2 trees: local and remote.

<a id="_87"></a>
So you also have to learn how to observe and modify and sync with the remote tree!

<a id="_88"></a>
But basically:<a id="_89"></a>

```
git fetch
```
to update the remote tree. And then you can use it exactly like any other branch, except you prefix them with the remote (usually `origin/*`), e.g.:<a id="_90"></a>

<a id="_91"></a>
- `origin/master` is the latest fetch of the remote version of `master`
<a id="_92"></a>
- `origin/my-feature`  is the latest fetch of the remote version of `my-feature`

## Merge conflicts

↑ **Parent:** [Git tips](git-tips.md)

### git rebase moves commits one by one

↑ **Parent:** [Merge conflicts](#merge-conflicts)

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

### The key to solve conflicts: see the two conflicting diffs

↑ **Parent:** [Merge conflicts](#merge-conflicts)

<a id="_101"></a>
The key to solve conflicts is:<a id="_102"></a>


> You have to understand what are the two commits that touched a given line (one from master, one from features), and then combine them somehow.

<a id="_103"></a>
Or in other words, at every rebase conflict we have something like:<a id="_104"></a>

```
master-commit    feature-commit
|                |
|                |
base-commit------+
|
|
```
Therefore there are 2 diffs that you have to understand and reconcile:<a id="_105"></a>

<a id="_106"></a>
- `base-commit` to `master-commit`
<a id="_107"></a>
- `base-commit` to `feature-commit`

### Conflict resolution tool

↑ **Parent:** [Merge conflicts](#merge-conflicts)

#### `diff3`

↑ **Parent:** [Conflict resolution tool](#conflict-resolution-tool)

<a id="_108"></a>
`diff3` conflict is basically what you always want to see, either by setting it as the default as per [https://stackoverflow.com/questions/27417656/should-diff3-be-default-conflictstyle-on-git](https://stackoverflow.com/questions/27417656/should-diff3-be-default-conflictstyle-on-git):<a id="_109"></a>

```
git config --global merge.conflictstyle diff3
```
or as a one off:<a id="_110"></a>

```
git checkout --conflict=diff3
```

<a id="_111"></a>
With this, conflicts now show up as:<a id="_112"></a>

```
++<<<<<<< HEAD
 +5
++||||||| parent of 7b0f59d (6)
++3
++=======
+ 6
++>>>>>>> 7b0f59d (6)
```
`7b0f59d` is the [SHA-2](computer-science.md#sha-2) of commit 6.

<a id="_113"></a>
instead of the inferior default:<a id="_114"></a>

```
++<<<<<<< ours
 +5
++=======
+ 6
++>>>>>>> theirs
```

<a id="_115"></a>
We can also observe the current tree state during resolution:<a id="_116"></a>

```
* b4ec057 (HEAD, master) 5
* 0b37c1b 4
| * fbfbfe8 (my-feature) 7
| * 7b0f59d 6
|/
* 661cfab 3
* 6d748a9 2
* c5f8a2c 1
```
so we understand that we are now at 5 and that we are trying to apply our commit `6`

<a id="_117"></a>
So it is much clearer what is happening:<a id="_118"></a>

<a id="_119"></a>
- master changed the code from `3` to `5`
<a id="_120"></a>
- our feature changed the code from `3` to `6`
and so now we have to decide what the new code is that will put both of these together.

<a id="_121"></a>
Let's say we decide it is `5 + 6 = 11` and continue rebasing:<a id="_122"></a>

```
git add .
git rebase --continue
```

<a id="_123"></a>
We now reach:<a id="_124"></a>

```
++<<<<<<< HEAD
 +11
++||||||| parent of fbfbfe8 (7)
++6
++=======
+ 7
++>>>>>>> fbfbfe8 (7)
```
and the tree looks like:<a id="_125"></a>

```
* ca7f7ff (HEAD) 6
* b4ec057 (master) 5
* 0b37c1b 4
| * fbfbfe8 (my-feature) 7
| * 7b0f59d 6
|/
* 661cfab 3
* 6d748a9 2
* c5f8a2c 1
```
So we understand that:<a id="_126"></a>

<a id="_127"></a>
- after the previous step we added commit 6 on top of 5
<a id="_128"></a>
- now we are adding 7 on top of the new 6 (which we decided would contain `11`)
and after resolving that one we now reach:<a id="_129"></a>

```
* e1aaf20 (HEAD -> my-feature) 7
* ca7f7ff 6
* b4ec057 (master) 5
* 0b37c1b 4
* 661cfab 3
* 6d748a9 2
* c5f8a2c 1
```

#### `git mergetool` with `meld` or `kdiff3`

↑ **Parent:** [Conflict resolution tool](#conflict-resolution-tool)

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

#### But which commit from master did we conflict with exactly?

↑ **Parent:** [Conflict resolution tool](#conflict-resolution-tool)

<a id="_137"></a>
`git rebase` does not tell you that, and that sucks.

<a id="_138"></a>
We only know which commit from the feature branch caused the problem.

<a id="_139"></a>
Generally we can guess or it is not needed, but `imerge` does look promising: [https://stackoverflow.com/questions/18162930/how-can-i-find-out-which-git-commits-cause-conflicts](https://stackoverflow.com/questions/18162930/how-can-i-find-out-which-git-commits-cause-conflicts)

## ↑ Ancestors (9)

1. [Git](software.md#git)
2. [List of version control systems](software.md#list-of-version-control-systems)
3. [Version control](software.md#version-control)
4. [Software](software.md)
5. [Computer](computer.md)
6. [Information technology](technology.md#information-technology)
7. [Area of technology](technology.md#area-of-technology)
8. [Technology](technology.md)
9. [Ciro Santilli's Homepage](README.md)
