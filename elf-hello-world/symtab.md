# `.symtab`

↑ **Parent:** [Sections](sections.md)

<a id="_256"></a>
Section type: `sh_type == SHT_SYMTAB`.

<a id="_257"></a>
Common name: "symbol table".

<a id="_258"></a>
First the we note that:<a id="_259"></a>

<a id="_260"></a>
- `sh_link` = `5`
<a id="_261"></a>
- `sh_info` = `6`

<a id="_262"></a>
For `SHT_SYMTAB` sections, those numbers mean that:<a id="_263"></a>

<a id="_264"></a>
- strings that give symbol names are in section 5, `.strtab`
<a id="_265"></a>
- the relocation data is in section 6, `.rela.text`

<a id="_266"></a>
A good high level tool to disassemble that section is:<a id="_267"></a>

```
nm hello_world.o
```
which gives:<a id="_268"></a>

```
0000000000000000 T _start
0000000000000000 d hello_world
000000000000000d a hello_world_len
```

<a id="_269"></a>
This is however a high level view that omits some types of symbols and in which the symbol types . A more detailed disassembly can be obtained with:<a id="_270"></a>

```
readelf -s hello_world.o
```
which gives:<a id="_271"></a>

```
Symbol table '.symtab' contains 7 entries:
   Num:    Value          Size Type    Bind   Vis      Ndx Name
     0: 0000000000000000     0 NOTYPE  LOCAL  DEFAULT  UND
     1: 0000000000000000     0 FILE    LOCAL  DEFAULT  ABS hello_world.asm
     2: 0000000000000000     0 SECTION LOCAL  DEFAULT    1
     3: 0000000000000000     0 SECTION LOCAL  DEFAULT    2
     4: 0000000000000000     0 NOTYPE  LOCAL  DEFAULT    1 hello_world
     5: 000000000000000d     0 NOTYPE  LOCAL  DEFAULT  ABS hello_world_len
     6: 0000000000000000     0 NOTYPE  GLOBAL DEFAULT    2 _start
```

<a id="_272"></a>
The binary format of the table is documented at [http://www.sco.com/developers/gabi/2003-12-17/ch4.symtab.html](http://www.sco.com/developers/gabi/2003-12-17/ch4.symtab.html)

<a id="_273"></a>
The data is:<a id="_274"></a>

```
readelf -x .symtab hello_world.o
```
which gives:<a id="_275"></a>

```
Hex dump of section '.symtab':
  0x00000000 00000000 00000000 00000000 00000000 ................
  0x00000010 00000000 00000000 01000000 0400f1ff ................
  0x00000020 00000000 00000000 00000000 00000000 ................
  0x00000030 00000000 03000100 00000000 00000000 ................
  0x00000040 00000000 00000000 00000000 03000200 ................
  0x00000050 00000000 00000000 00000000 00000000 ................
  0x00000060 11000000 00000100 00000000 00000000 ................
  0x00000070 00000000 00000000 1d000000 0000f1ff ................
  0x00000080 0d000000 00000000 00000000 00000000 ................
  0x00000090 2d000000 10000200 00000000 00000000 -...............
  0x000000a0 00000000 00000000                   ........
```

<a id="_276"></a>
The entries are of type:<a id="_277"></a>

```
typedef struct {
    Elf64_Word  st_name;
    unsigned char   st_info;
    unsigned char   st_other;
    Elf64_Half  st_shndx;
    Elf64_Addr  st_value;
    Elf64_Xword st_size;
} Elf64_Sym;
```

<a id="_278"></a>
Like in the section table, the first entry is magical and set to a fixed meaningless values.

**Table of contents**

- [`STT_FILE`](stt-file.md)
- [`STT_SECTION`](stt-section.md)
- [`STT_NOTYPE`](stt-notype.md)
  - [`SHN_ABS`](shn-abs.md)
- [`SHT_SYMTAB` on the executable](sht-symtab-on-the-executable.md)

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
