<h1 id="sht-symtab-on-the-executable"><code>SHT_SYMTAB</code> on the executable</h1>

↑ **Parent:** [`.symtab`](symtab.md)

<a id="_312"></a>
By default, NASM places a `.symtab` on the executable as well.

<a id="_313"></a>
This is only used for debugging. Without the symbols, we are completely blind, and must reverse engineer everything.

<a id="_314"></a>
You can strip it with `objcopy`, and the executable will still run. Such executables are called "stripped executables".

## ↑ Ancestors (12)

1. [`.symtab`](symtab.md)
2. [Sections](sections.md)
3. [ELF Hello World Tutorial](../elf-hello-world-split.md)
4. [Executable and Linkable Format](../executable-and-linkable-format.md)
5. [Executable file format](../executable-file-format.md)
6. [Systems programming](../systems-programming-split.md)
7. [Software](../software-split.md)
8. [Computer](../computer-split.md)
9. [Information technology](../information-technology.md)
10. [Area of technology](../area-of-technology.md)
11. [Technology](../technology-split.md)
12. [Ciro Santilli's Homepage](../split.md)
