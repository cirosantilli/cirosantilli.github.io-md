# Oh, but there are 2 trees: local and remote

↑ **Parent:** [Git tips](../git-tips-split.md)

Oh but there are usually 2 trees: local and remote.

So you also have to learn how to observe and modify and sync with the remote tree!

But basically:
```
git fetch
```
to update the remote tree. And then you can use it exactly like any other branch, except you prefix them with the remote (usually `origin/*`), e.g.:
- `origin/master` is the latest fetch of the remote version of `master`
- `origin/my-feature`  is the latest fetch of the remote version of `my-feature`

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
