# `.shstrtab`

↑ **Parent:** [Sections](sections.md)

Section type: `sh_type == SHT_STRTAB`.

Common name: "section header string table".

The section name `.shstrtab` is reserved. The standard says:

> This section holds section names.

This section gets pointed to by the `e_shstrnd` field of the ELF header itself.

String indexes of this section are are pointed to by the `sh_name` field of section headers, which denote strings.

This section does not have `SHF_ALLOC` marked, so it will not appear on the executing program.
```
readelf -x .shstrtab hello_world.o
```
outputs:
```
Hex dump of section '.shstrtab':
  0x00000000 002e6461 7461002e 74657874 002e7368 ..data..text..sh
  0x00000010 73747274 6162002e 73796d74 6162002e strtab..symtab..
  0x00000020 73747274 6162002e 72656c61 2e746578 strtab..rela.tex
  0x00000030 7400                                t.
```

The data in this section has a fixed format: [http://www.sco.com/developers/gabi/2003-12-17/ch4.strtab.html](http://www.sco.com/developers/gabi/2003-12-17/ch4.strtab.html)

If we look at the names of other sections, we see that they all contain numbers, e.g. the `.text` section is number `7`.

Then each string ends when the first NUL character is found, e.g. character `12` is `\0` just after `.text\0`.

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
