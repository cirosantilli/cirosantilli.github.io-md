# Section header table

↑ **Parent:** [ELF Hello World Tutorial](../elf-hello-world-split.md)

<a id="_175"></a>
Array of `Elf64_Shdr` structs.

<a id="_176"></a>
Each entry contains metadata about a given section.

<a id="_177"></a>
`e_shoff` of the ELF header gives the starting position, 0x40 here.

<a id="_178"></a>
`e_shentsize` and `e_shnum` from the ELF header say that we have 7 entries, each `0x40` bytes long.

<a id="_179"></a>
So the table takes bytes from 0x40 to `0x40 + 7 + 0x40 - 1` = 0x1FF.

<a id="_180"></a>
Some section names are reserved for certain section types: [http://www.sco.com/developers/gabi/2003-12-17/ch4.sheader.html#special_sections](http://www.sco.com/developers/gabi/2003-12-17/ch4.sheader.html#special_sections) e.g. `.text` requires a `SHT_PROGBITS` type and `SHF_ALLOC` + `SHF_EXECINSTR`

<a id="_181"></a>
Running:<a id="_182"></a>

```
readelf -S hello_world.o
```
outputs:<a id="_183"></a>

```
There are 7 section headers, starting at offset 0x40:

Section Headers:
  [Nr] Name              Type             Address           Offset
       Size              EntSize          Flags  Link  Info  Align
  [ 0]                   NULL             0000000000000000  00000000
       0000000000000000  0000000000000000           0     0     0
  [ 1] .data             PROGBITS         0000000000000000  00000200
       000000000000000d  0000000000000000  WA       0     0     4
  [ 2] .text             PROGBITS         0000000000000000  00000210
       0000000000000027  0000000000000000  AX       0     0     16
  [ 3] .shstrtab         STRTAB           0000000000000000  00000240
       0000000000000032  0000000000000000           0     0     1
  [ 4] .symtab           SYMTAB           0000000000000000  00000280
       00000000000000a8  0000000000000018           5     6     4
  [ 5] .strtab           STRTAB           0000000000000000  00000330
       0000000000000034  0000000000000000           0     0     1
  [ 6] .rela.text        RELA             0000000000000000  00000370
       0000000000000018  0000000000000018           4     2     4
Key to Flags:
  W (write), A (alloc), X (execute), M (merge), S (strings), l (large)
  I (info), L (link order), G (group), T (TLS), E (exclude), x (unknown)
  O (extra OS processing required) o (OS specific), p (processor specific)
```

<a id="_184"></a>
The `struct` represented by each entry is:<a id="_185"></a>

```
typedef struct {
    Elf64_Word  sh_name;
    Elf64_Word  sh_type;
    Elf64_Xword sh_flags;
    Elf64_Addr  sh_addr;
    Elf64_Off   sh_offset;
    Elf64_Xword sh_size;
    Elf64_Word  sh_link;
    Elf64_Word  sh_info;
    Elf64_Xword sh_addralign;
    Elf64_Xword sh_entsize;
} Elf64_Shdr;
```

## ↑ Ancestors (10)

1. [ELF Hello World Tutorial](../elf-hello-world-split.md)
2. [Executable and Linkable Format](../executable-and-linkable-format.md)
3. [Executable file format](../executable-file-format.md)
4. [Systems programming](../systems-programming-split.md)
5. [Software](../software-split.md)
6. [Computer](../computer-split.md)
7. [Information technology](../information-technology.md)
8. [Area of technology](../area-of-technology.md)
9. [Technology](../technology-split.md)
10. [Ciro Santilli's Homepage](../split.md)
