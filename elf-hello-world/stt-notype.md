<h1 id="stt-notype"><code>STT_NOTYPE</code></h1>

↑ **Parent:** [`.symtab`](symtab.md)

<a id="_300"></a>
Then come the most important symbols:<a id="_301"></a>

```
Num:    Value          Size Type    Bind   Vis      Ndx Name
  4: 0000000000000000     0 NOTYPE  LOCAL  DEFAULT    1 hello_world
  5: 000000000000000d     0 NOTYPE  LOCAL  DEFAULT  ABS hello_world_len
  6: 0000000000000000     0 NOTYPE  GLOBAL DEFAULT    2 _start
```

<a id="_302"></a>
`hello_world` string is in the `.data` section (index 1). It's value is 0: it points to the first byte of that section.

<a id="_303"></a>
`_start` is marked with `GLOBAL` visibility since we wrote:<a id="_304"></a>

```
global _start
```

<a id="_305"></a>
in NASM. This is necessary since it must be seen as the entry point. Unlike in C, by default NASM labels are local.

**Table of contents**

- [`SHN_ABS`](shn-abs.md)

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
