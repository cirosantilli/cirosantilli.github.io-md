# Implementations

↑ **Parent:** [Introduction](introduction.md)

<a id="_56"></a>
<a id="_57"></a>
- <a id="_58"></a>
  Compiler toolchains generate and read ELF files.

  <a id="_59"></a>
  Sane compilers should use a separate standalone library to do the dirty work. E.g., Binutils uses BFD (in-tree and canonical source).

<a id="_60"></a>
<a id="_61"></a>
- <a id="_62"></a>
  Operating systems read and run ELF files.

  <a id="_63"></a>
  Kernels cannot link to a library nor use the C stlib, so they are more likely to implement it themselves.

  <a id="_64"></a>
  This is the case of the Linux kernel 4.2 which implements it in th file `fs/binfmt_elf.c`.

<a id="_65"></a>
<a id="_66"></a>
- Specialized libraries. Examples:<a id="_67"></a>

  <a id="_68"></a>
  - [https://github.com/eliben/pyelftools.](https://github.com/eliben/pyelftools.) By a hardcore Googler: [https://plus.google.com/+EliBenderskyGplus/posts](https://plus.google.com/+EliBenderskyGplus/posts)
  <a id="_69"></a>
  - [https://sourceforge.net/projects/elftoolchain](https://sourceforge.net/projects/elftoolchain)

## ↑ Ancestors (11)

1. [Introduction](introduction.md)
2. [ELF Hello World Tutorial](../elf-hello-world-split.md)
3. [Executable and Linkable Format](../executable-and-linkable-format.md)
4. [Executable file format](../executable-file-format.md)
5. [Systems programming](../systems-programming-split.md)
6. [Software](../software-split.md)
7. [Computer](../computer-split.md)
8. [Information technology](../information-technology.md)
9. [Area of technology](../area-of-technology.md)
10. [Technology](../technology-split.md)
11. [Ciro Santilli's Homepage](../split.md)
