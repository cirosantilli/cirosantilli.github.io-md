<h1 id="rela-text"><code>.rela.text</code></h1>

↑ **Parent:** [Sections](sections.md)

Section type: `sh_type == SHT_RELA`.

Common name: "relocation section".

`.rela.text` holds relocation data which says how the address should be modified when the final executable is linked. This points to bytes of the text area that must be modified when linking happens to point to the correct memory locations.

Basically, it translates the object text containing the placeholder 0x0 address:
```
   a:       48 be 00 00 00 00 00    movabs $0x0,%rsi
  11:       00 00 00
```
to the actual executable code containing the final 0x6000d8:
```
4000ba: 48 be d8 00 60 00 00    movabs $0x6000d8,%rsi
4000c1: 00 00 00
```

It was pointed to by `sh_info` = `6` of the `.symtab` section.

`readelf -r hello_world.o` outputs:
```
Relocation section '.rela.text' at offset 0x3b0 contains 1 entries:
  Offset          Info           Type           Sym. Value    Sym. Name + Addend
00000000000c  000200000001 R_X86_64_64       0000000000000000 .data + 0
```

The section does not exist in the executable.

The actual bytes are:
```
00000370  0c 00 00 00 00 00 00 00  01 00 00 00 02 00 00 00  |................|
00000380  00 00 00 00 00 00 00 00  00 00 00 00 00 00 00 00  |................|
```

The `struct` represented is:
```
typedef struct {
    Elf64_Addr  r_offset;
    Elf64_Xword r_info;
    Elf64_Sxword    r_addend;
} Elf64_Rela;
```

So:
- 370 0: `r_offset` = 0xC: address into the `.text` whose address this relocation will modify
- 370 8: `r_info` = 0x200000001. Contains 2 fields:
  - `ELF64_R_TYPE` = 0x1: meaning depends on the exact architecture.
  - `ELF64_R_SYM` = 0x2: index of the section to which the address points, so `.data` which is at index 2.

  The AMD64 ABI says that type `1` is called `R_X86_64_64` and that it represents the operation `S + A` where:
  - `S`: the value of the symbol on the object file, here `0` because we point to the `00 00 00 00 00 00 00 00` of `movabs $0x0,%rsi`
  - `A`: the addend, present in field `r_added`

  This address is added to the section on which the relocation operates.

  This relocation operation acts on a total 8 bytes.
- 380 0: `r_addend` = 0

So in our example we conclude that the new address will be: `S + A` = `.data + 0`, and thus the first thing in the data section.

**Table of contents**

- [`.rel.text`](rel-text.md)

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
