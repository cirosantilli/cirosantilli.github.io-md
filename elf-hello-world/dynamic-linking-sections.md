# Dynamic linking sections

↑ **Parent:** [Sections](sections.md)

This program did not have certain dynamic linking related sections because we linked it minimally with `ld`.

However, if you compile a C hello world with GCC 8.2:
```
gcc -o main.out main.c
```

some other interesting sections would appear.

**Table of contents**

- [`PT_INTERP`](pt-interp.md)
- [Dynamic section](dynamic-section.md)
  - [`DT_FLAGS_1`](dt-flags-1.md)
    - [`DF_1_PIE`](df-1-pie.md)

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
