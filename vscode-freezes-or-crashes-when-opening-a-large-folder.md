# vscode freezes or crashes when opening a large folder

↑ **Parent:** [Visual Studio Code](visual-studio-code.md)

[snap](snap-package-manager.md) vscode 1.100.2, [Ubuntu 25.04](ubuntu-25-04.md)

The issue appears to be that the file watcher goes out of control.

The reproduction is very simple:
```
mkdir mytest
cd mytest
seq 1000000 | xargs touch
code --disable-extensions .
```
and now the editor GUI hangs and Ubuntu shows a popup:

> The window is not responding

[htop](htop.md) reveals a bunch of processes or threads of type:
```
/snap/code/194/usr/share/code/code
```

Infinite duplicate pool:
- [https://github.com/microsoft/vscode/issues/237394](https://github.com/microsoft/vscode/issues/237394)
- [https://github.com/microsoft/vscode/issues/79336](https://github.com/microsoft/vscode/issues/79336)

## ↑ Ancestors (8)

1. [Visual Studio Code](visual-studio-code.md)
2. [Integrated development environment](integrated-development-environment.md)
3. [Software](software-split.md)
4. [Computer](computer-split.md)
5. [Information technology](information-technology.md)
6. [Area of technology](area-of-technology.md)
7. [Technology](technology-split.md)
8. [Ciro Santilli's Homepage](split.md)
