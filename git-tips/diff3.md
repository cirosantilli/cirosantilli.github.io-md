# `diff3`

↑ **Parent:** [Conflict resolution tool](conflict-resolution-tool.md)

`diff3` conflict is basically what you always want to see, either by setting it as the default as per [https://stackoverflow.com/questions/27417656/should-diff3-be-default-conflictstyle-on-git](https://stackoverflow.com/questions/27417656/should-diff3-be-default-conflictstyle-on-git):
```
git config --global merge.conflictstyle diff3
```
or as a one off:
```
git checkout --conflict=diff3
```

With this, conflicts now show up as:
```
++<<<<<<< HEAD
 +5
++||||||| parent of 7b0f59d (6)
++3
++=======
+ 6
++>>>>>>> 7b0f59d (6)
```
`7b0f59d` is the [SHA-2](../sha-2.md) of commit 6.

instead of the inferior default:
```
++<<<<<<< ours
 +5
++=======
+ 6
++>>>>>>> theirs
```

We can also observe the current tree state during resolution:
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

So it is much clearer what is happening:
- master changed the code from `3` to `5`
- our feature changed the code from `3` to `6`
and so now we have to decide what the new code is that will put both of these together.

Let's say we decide it is `5 + 6 = 11` and continue rebasing:
```
git add .
git rebase --continue
```

We now reach:
```
++<<<<<<< HEAD
 +11
++||||||| parent of fbfbfe8 (7)
++6
++=======
+ 7
++>>>>>>> fbfbfe8 (7)
```
and the tree looks like:
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
So we understand that:
- after the previous step we added commit 6 on top of 5
- now we are adding 7 on top of the new 6 (which we decided would contain `11`)
and after resolving that one we now reach:
```
* e1aaf20 (HEAD -> my-feature) 7
* ca7f7ff 6
* b4ec057 (master) 5
* 0b37c1b 4
* 661cfab 3
* 6d748a9 2
* c5f8a2c 1
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
