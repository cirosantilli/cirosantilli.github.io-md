# Program header table

↑ **Parent:** [ELF Hello World Tutorial](../elf-hello-world-split.md)

Only appears in the executable.

Contains information of how the executable should be put into the process virtual memory.

The executable is generated from object files by the linker. The main jobs that the linker does are:

- determine which sections of the object files will go into which segments of the executable.

  In Binutils, this comes down to parsing a linker script, and dealing with a bunch of defaults.

  You can get the linker script used with `ld --verbose`, and set a custom one with `ld -T`.
- do relocation according to the `.rela.text` section. This depends on how the multiple sections are put into memory.

`readelf -l hello_world.out` gives:
```
Elf file type is EXEC (Executable file)
Entry point 0x4000b0
There are 2 program headers, starting at offset 64

Program Headers:
  Type           Offset             VirtAddr           PhysAddr
                 FileSiz            MemSiz              Flags  Align
  LOAD           0x0000000000000000 0x0000000000400000 0x0000000000400000
                 0x00000000000000d7 0x00000000000000d7  R E    200000
  LOAD           0x00000000000000d8 0x00000000006000d8 0x00000000006000d8
                 0x000000000000000d 0x000000000000000d  RW     200000

 Section to Segment mapping:
  Segment Sections...
   00     .text
   01     .data
```

On the ELF header, `e_phoff`, `e_phnum` and `e_phentsize` told us that there are 2 program headers, which start at `0x40` and are `0x38` bytes long each, so they are:
```
00000040  01 00 00 00 05 00 00 00  00 00 00 00 00 00 00 00  |................|
00000050  00 00 40 00 00 00 00 00  00 00 40 00 00 00 00 00  |..@.......@.....|
00000060  d7 00 00 00 00 00 00 00  d7 00 00 00 00 00 00 00  |................|
00000070  00 00 20 00 00 00 00 00                           |.. .....        |
```
and:
```
00000070                           01 00 00 00 06 00 00 00  |        ........|
00000080  d8 00 00 00 00 00 00 00  d8 00 60 00 00 00 00 00  |..........`.....|
00000090  d8 00 60 00 00 00 00 00  0d 00 00 00 00 00 00 00  |..`.............|
000000a0  0d 00 00 00 00 00 00 00  00 00 20 00 00 00 00 00  |.......... .....|
```

Structure represented [http://www.sco.com/developers/gabi/2003-12-17/ch5.pheader.html](http://www.sco.com/developers/gabi/2003-12-17/ch5.pheader.html):
```
typedef struct {
    Elf64_Word  p_type;
    Elf64_Word  p_flags;
    Elf64_Off   p_offset;
    Elf64_Addr  p_vaddr;
    Elf64_Addr  p_paddr;
    Elf64_Xword p_filesz;
    Elf64_Xword p_memsz;
    Elf64_Xword p_align;
} Elf64_Phdr;
```

Breakdown of the first one:
- 40 0: `p_type` = `01 00 00 00` = `PT_LOAD`: this is a regular segment that will get loaded in memory.
- 40 4: `p_flags` = `05 00 00 00` = execute and read permissions. No write: we cannot modify the text segment. A classic way to do this in C is with string literals: [https://stackoverflow.com/a/30662565/895245](https://stackoverflow.com/a/30662565/895245) This allows kernels to do certain optimizations, like sharing the segment amongst processes.
- 40 8: `p_offset` = 8x `00` TODO: what is this? Standard says:

  > This member gives the offset from the beginning of the file at which the first byte of the segment resides.

  But it looks like offsets from the beginning of segments, not file?
- 50 0: `p_vaddr` = `00 00 40 00 00 00 00 00`: initial virtual memory address to load this segment to
- 50 8: `p_paddr` = `00 00 40 00 00 00 00 00`: unspecified effect. Intended for systems in which physical addressing matters. TODO example?
- 60 0: `p_filesz` = `d7 00 00 00 00 00 00 00`: size that the segment occupies in memory. If smaller than `p_memsz`, the OS fills it with zeroes to fit when loading the program. This is how BSS data is implemented to save space on executable files. i368 ABI says on `PT_LOAD`:

  > The bytes from the file are mapped to the beginning of the memory segment. If the segment’s memory size (p\_memsz) is larger than the file size (p\_filesz), the ‘‘extra’’ bytes are defined to hold the value 0 and to follow the segment’s initialized area. The file size may not be larger than the memory size.

- 60 8: `p_memsz` = `d7 00 00 00 00 00 00 00`: size that the segment occupies in memory
- 70 0: `p_align` = `00 00 20 00 00 00 00 00`: 0 or 1 mean no alignment required. TODO why is this required? Why not just use `p_addr` directly, and get that right? Docs also say:

  > p\_vaddr should equal p\_offset, modulo p\_align

The second segment (`.data`) is analogous. TODO: why use offset `0x0000d8` and address `0x00000000006000d8`? Why not just use `0` and `0x00000000006000d8`?

Then the:
```
 Section to Segment mapping:
```
section of the `readelf` tells us that:
- 0 is the `.text` segment. Aha, so this is why it is executable, and not writable
- 1 is the `.data` segment.

TODO where does this information come from? [https://stackoverflow.com/questions/23018496/section-to-segment-mapping-in-elf-files](https://stackoverflow.com/questions/23018496/section-to-segment-mapping-in-elf-files)

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
