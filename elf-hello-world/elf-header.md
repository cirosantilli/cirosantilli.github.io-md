# ELF header

↑ **Parent:** [ELF Hello World Tutorial](../elf-hello-world-split.md)

Running:
```
readelf -h hello_world.o
```
outputs:
```
Magic:   7f 45 4c 46 02 01 01 00 00 00 00 00 00 00 00 00
Class:                             ELF64
Data:                              2's complement, little endian
Version:                           1 (current)
OS/ABI:                            UNIX - System V
ABI Version:                       0
Type:                              REL (Relocatable file)
Machine:                           Advanced Micro Devices X86-64
Version:                           0x1
Entry point address:               0x0
Start of program headers:          0 (bytes into file)
Start of section headers:          64 (bytes into file)
Flags:                             0x0
Size of this header:               64 (bytes)
Size of program headers:           0 (bytes)
Number of program headers:         0
Size of section headers:           64 (bytes)
Number of section headers:         7
Section header string table index: 3
```

Running:
```
readelf -h hello_world.out
```
outputs:
```
Magic:   7f 45 4c 46 02 01 01 00 00 00 00 00 00 00 00 00
Class:                             ELF64
Data:                              2's complement, little endian
Version:                           1 (current)
OS/ABI:                            UNIX - System V
ABI Version:                       0
Type:                              EXEC (Executable file)
Machine:                           Advanced Micro Devices X86-64
Version:                           0x1
Entry point address:               0x4000b0
Start of program headers:          64 (bytes into file)
Start of section headers:          272 (bytes into file)
Flags:                             0x0
Size of this header:               64 (bytes)
Size of program headers:           56 (bytes)
Number of program headers:         2
Size of section headers:           64 (bytes)
Number of section headers:         6
Section header string table index: 3
```

Bytes in the object file:
```
00000000  7f 45 4c 46 02 01 01 00  00 00 00 00 00 00 00 00  |.ELF............|
00000010  01 00 3e 00 01 00 00 00  00 00 00 00 00 00 00 00  |..>.............|
00000020  00 00 00 00 00 00 00 00  40 00 00 00 00 00 00 00  |........@.......|
00000030  00 00 00 00 40 00 00 00  00 00 40 00 07 00 03 00  |....@.....@.....|
```

Executable:
```
00000000  7f 45 4c 46 02 01 01 00  00 00 00 00 00 00 00 00  |.ELF............|
00000010  02 00 3e 00 01 00 00 00  b0 00 40 00 00 00 00 00  |..>.......@.....|
00000020  40 00 00 00 00 00 00 00  10 01 00 00 00 00 00 00  |@...............|
00000030  00 00 00 00 40 00 38 00  02 00 40 00 06 00 03 00  |....@.8...@.....|
```

Structure represented:
```
# define EI_NIDENT 16

typedef struct {
    unsigned char   e_ident[EI_NIDENT];
    Elf64_Half      e_type;
    Elf64_Half      e_machine;
    Elf64_Word      e_version;
    Elf64_Addr      e_entry;
    Elf64_Off       e_phoff;
    Elf64_Off       e_shoff;
    Elf64_Word      e_flags;
    Elf64_Half      e_ehsize;
    Elf64_Half      e_phentsize;
    Elf64_Half      e_phnum;
    Elf64_Half      e_shentsize;
    Elf64_Half      e_shnum;
    Elf64_Half      e_shstrndx;
} Elf64_Ehdr;
```

Manual breakdown:

- 0 0: `EI_MAG` = `7f 45 4c 46` = `0x7f 'E', 'L', 'F'`: ELF magic number
- 0 4: `EI_CLASS` = `02` = `ELFCLASS64`: 64 bit elf
- 0 5: `EI_DATA` = `01` = `ELFDATA2LSB`: little endian data
- 0 6: `EI_VERSION` = `01`: format version
- 0 7: `EI_OSABI` (only in 2003 Update) = `00` = `ELFOSABI_NONE`: no extensions.
- 0 8: `EI_PAD` = 8x `00`: reserved bytes. Must be set to 0.
- 1 0: `e_type` = `01 00` = 1 (big endian) = `ET_REl`: relocatable format

  On the executable it is `02 00` for `ET_EXEC`.

  Another important possibility for the executable is `ET_DYN` for PIE executables and shared libraries.

  `ET_DYN` tells the Linux kernel that the code is position independent, and can loaded at a random memory location with ASLR.

  This is explained further at:
  - [https://stackoverflow.com/questions/2463150/what-is-the-fpie-option-for-position-independent-executables-in-gcc-and-ld/51308031#51308031](https://stackoverflow.com/questions/2463150/what-is-the-fpie-option-for-position-independent-executables-in-gcc-and-ld/51308031#51308031)
  - [https://stackoverflow.com/questions/34519521/why-does-gcc-create-a-shared-object-instead-of-an-executable-binary-according-to/55704865#55704865](https://stackoverflow.com/questions/34519521/why-does-gcc-create-a-shared-object-instead-of-an-executable-binary-according-to/55704865#55704865)
- 1 2: `e_machine` = `3e 00` = `62` = `EM_X86_64`: AMD64 architecture
- 1 4: `e_version` = `01 00 00 00`: must be 1
- 1 8: `e_entry` = 8x `00`: execution address entry point, or 0 if not applicable like for the object file since there is no entry point.

  On the executable, it is `b0 00 40 00 00 00 00 00`. The kernel puts the RIP directly on that value when executing. It can be configured by the linker script or `-e`. But it will segfault if you set it too low: [https://stackoverflow.com/questions/2187484/why-is-the-elf-execution-entry-point-virtual-address-of-the-form-0x80xxxxx-and-n](https://stackoverflow.com/questions/2187484/why-is-the-elf-execution-entry-point-virtual-address-of-the-form-0x80xxxxx-and-n)
- 2 0: `e_phoff` = 8x `00`: program header table offset, 0 if not present.

  `40 00 00 00` on the executable, i.e. it starts immediately after the ELF header.
- 2 8: `e_shoff` = `40` 7x `00` = `0x40`: section header table file offset, 0 if not present.
- 3 0: `e_flags` = `00 00 00 00` Arch specific. `i386` docs say:

  > The Intel386 architecture defines no flags; so this member contains zero.
- 3 4: `e_ehsize` = `40 00`: size of this elf header. TODO why this field needed? Isn't the size fixed?
- 3 6: `e_phentsize` = `00 00`: size of each program header, 0 if not present.

  `38 00` on executable: it is 56 bytes long
- 3 8: `e_phnum` = `00 00`: number of program header entries, 0 if not present.

  `02 00` on executable: there are 2 entries.
- 3 A: `e_shentsize` and `e_shnum` = `40 00 07 00`: section header size and number of entries
- 3 E: `e_shstrndx` (`Section Header STRing iNDeX`) = `03 00`: index of the `.shstrtab` section.

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
