# How to learn

↑ **Parent:** [Introduction](introduction.md)

<a id="_22"></a>
Spin like mad between:<a id="_23"></a>

<a id="_24"></a>
- standards
<a id="_25"></a>
- high level generators. We use the [assembler](../assembler-computing.md) `as` and [linker](../linker-computing.md) `ld`.
<a id="_26"></a>
- hexdumps
<a id="_27"></a>
- file decompilers. We use `readelf`. It makes it faster to read the ELF file by turning it into human readable output. But you must have seen one byte-by-byte example first, and think how `readelf` output maps to the standard.
<a id="_28"></a>
- low-level generators: stand-alone libraries that let you control every field of the ELF files you generated. [https://github.com/BR903/ELFkickers,](https://github.com/BR903/ELFkickers,) [https://github.com/sqall01/ZwoELF](https://github.com/sqall01/ZwoELF) and many more on GitHub.
<a id="_29"></a>
- consumer: the `exec` system call of the Linux kernel can parse ELF files to starts processes: [https://github.com/torvalds/linux/blob/v4.11/fs/binfmt_elf.c,](https://github.com/torvalds/linux/blob/v4.11/fs/binfmt_elf.c,) [https://stackoverflow.com/questions/8352535/how-does-kernel-get-an-executable-binary-file-running-under-linux/31394861#31394861](https://stackoverflow.com/questions/8352535/how-does-kernel-get-an-executable-binary-file-running-under-linux/31394861#31394861)

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
