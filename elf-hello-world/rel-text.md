<h1 id="rel-text"><code>.rel.text</code></h1>

↑ **Parent:** [`.rela.text`](rela-text.md)

<a id="_351"></a>
Besides `sh_type == SHT_RELA`, there also exists `SHT_REL`, which would have section name `.text.rel` (not present in this object file).

<a id="_352"></a>
Those represent the same `struct`, but without the addend, e.g.:<a id="_353"></a>

```
typedef struct {
    Elf64_Addr  r_offset;
    Elf64_Xword r_info;
} Elf64_Rela;
```

<a id="_354"></a>
The ELF standard says that in many cases the both can be used, and it is just a matter of convenience.

## ↑ Ancestors (12)

1. [`.rela.text`](rela-text.md)
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
