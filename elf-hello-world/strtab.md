# `.strtab`

↑ **Parent:** [Sections](sections.md)

<a id="_315"></a>
Holds strings for the symbol table.

<a id="_316"></a>
This section has `sh_type == SHT_STRTAB`.

<a id="_317"></a>
It is pointed to by `sh_link == 5` of the `.symtab` section.<a id="_318"></a>

```
readelf -x .strtab hello_world.o
```
outputs:<a id="_319"></a>

```
Hex dump of section '.strtab':
  0x00000000 0068656c 6c6f5f77 6f726c64 2e61736d .hello_world.asm
  0x00000010 0068656c 6c6f5f77 6f726c64 0068656c .hello_world.hel
  0x00000020 6c6f5f77 6f726c64 5f6c656e 005f7374 lo_world_len._st
  0x00000030 61727400                            art.
```

<a id="_320"></a>
This implies that it is an ELF level limitation that global variables cannot contain NUL characters.

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
