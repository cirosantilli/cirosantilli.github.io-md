# Index 0 section

↑ **Parent:** [Sections](sections.md)

<a id="_186"></a>
Contained in bytes 0x40 to 0x7F.

<a id="_187"></a>
The first section is always magic: [http://www.sco.com/developers/gabi/2003-12-17/ch4.sheader.html](http://www.sco.com/developers/gabi/2003-12-17/ch4.sheader.html) says:

<a id="_188"></a>
> If the number of sections is greater than or equal to SHN\_LORESERVE (0xff00), e\_shnum has the value SHN\_UNDEF (0) and the actual number of section header table entries is contained in the sh\_size field of the section header at index 0 (otherwise, the sh\_size member of the initial entry contains 0).

<a id="_189"></a>
There are also other magic sections detailed in `Figure 4-7: Special Section Indexes`.

**Table of contents**

- [`SHT_NULL`](sht-null.md)

## ↑ Ancestors (11)

1. [Sections](sections.md)
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
