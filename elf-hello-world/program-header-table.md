# Program header table

↑ **Parent:** [ELF Hello World Tutorial](../elf-hello-world-split.md)

<a id="_365"></a>
Only appears in the executable.

<a id="_366"></a>
Contains information of how the executable should be put into the process virtual memory.

<a id="_367"></a>
The executable is generated from object files by the linker. The main jobs that the linker does are:

<a id="_368"></a>
<a id="_369"></a>
- <a id="_370"></a>
  determine which sections of the object files will go into which segments of the executable.

  <a id="_371"></a>
  In Binutils, this comes down to parsing a linker script, and dealing with a bunch of defaults.

  <a id="_372"></a>
  You can get the linker script used with `ld --verbose`, and set a custom one with `ld -T`.
<a id="_373"></a>
- do relocation according to the `.rela.text` section. This depends on how the multiple sections are put into memory.

<a id="_374"></a>
`readelf -l hello_world.out` gives:<a id="_375"></a>

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

<a id="_376"></a>
On the ELF header, `e_phoff`, `e_phnum` and `e_phentsize` told us that there are 2 program headers, which start at `0x40` and are `0x38` bytes long each, so they are:<a id="_377"></a>

```
00000040  01 00 00 00 05 00 00 00  00 00 00 00 00 00 00 00  |................|
00000050  00 00 40 00 00 00 00 00  00 00 40 00 00 00 00 00  |..@.......@.....|
00000060  d7 00 00 00 00 00 00 00  d7 00 00 00 00 00 00 00  |................|
00000070  00 00 20 00 00 00 00 00                           |.. .....        |
```
and:<a id="_378"></a>

```
00000070                           01 00 00 00 06 00 00 00  |        ........|
00000080  d8 00 00 00 00 00 00 00  d8 00 60 00 00 00 00 00  |..........`.....|
00000090  d8 00 60 00 00 00 00 00  0d 00 00 00 00 00 00 00  |..`.............|
000000a0  0d 00 00 00 00 00 00 00  00 00 20 00 00 00 00 00  |.......... .....|
```

<a id="_379"></a>
Structure represented [http://www.sco.com/developers/gabi/2003-12-17/ch5.pheader.html](http://www.sco.com/developers/gabi/2003-12-17/ch5.pheader.html):<a id="_380"></a>

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

<a id="_381"></a>
Breakdown of the first one:<a id="_382"></a>

<a id="_383"></a>
- 40 0: `p_type` = `01 00 00 00` = `PT_LOAD`: this is a regular segment that will get loaded in memory.
<a id="_384"></a>
- 40 4: `p_flags` = `05 00 00 00` = execute and read permissions. No write: we cannot modify the text segment. A classic way to do this in C is with string literals: [https://stackoverflow.com/a/30662565/895245](https://stackoverflow.com/a/30662565/895245) This allows kernels to do certain optimizations, like sharing the segment amongst processes.
<a id="_385"></a>
- <a id="_386"></a>
  40 8: `p_offset` = 8x `00` TODO: what is this? Standard says:

  <a id="_387"></a>
  > This member gives the offset from the beginning of the file at which the first byte of the segment resides.

  <a id="_388"></a>
  But it looks like offsets from the beginning of segments, not file?
<a id="_389"></a>
- 50 0: `p_vaddr` = `00 00 40 00 00 00 00 00`: initial virtual memory address to load this segment to
<a id="_390"></a>
- 50 8: `p_paddr` = `00 00 40 00 00 00 00 00`: unspecified effect. Intended for systems in which physical addressing matters. TODO example?
<a id="_391"></a>
- <a id="_392"></a>
  60 0: `p_filesz` = `d7 00 00 00 00 00 00 00`: size that the segment occupies in memory. If smaller than `p_memsz`, the OS fills it with zeroes to fit when loading the program. This is how BSS data is implemented to save space on executable files. i368 ABI says on `PT_LOAD`:

  <a id="_393"></a>
  > The bytes from the file are mapped to the beginning of the memory segment. If the segment’s memory size (p\_memsz) is larger than the file size (p\_filesz), the ‘‘extra’’ bytes are defined to hold the value 0 and to follow the segment’s initialized area. The file size may not be larger than the memory size.

<a id="_394"></a>
<a id="_395"></a>
- 60 8: `p_memsz` = `d7 00 00 00 00 00 00 00`: size that the segment occupies in memory
<a id="_396"></a>
- <a id="_397"></a>
  70 0: `p_align` = `00 00 20 00 00 00 00 00`: 0 or 1 mean no alignment required. TODO why is this required? Why not just use `p_addr` directly, and get that right? Docs also say:

  <a id="_398"></a>
  > p\_vaddr should equal p\_offset, modulo p\_align

<a id="_399"></a>
The second segment (`.data`) is analogous. TODO: why use offset `0x0000d8` and address `0x00000000006000d8`? Why not just use `0` and `0x00000000006000d8`?

<a id="_400"></a>
Then the:<a id="_401"></a>

```
 Section to Segment mapping:
```
section of the `readelf` tells us that:<a id="_402"></a>

<a id="_403"></a>
- 0 is the `.text` segment. Aha, so this is why it is executable, and not writable
<a id="_404"></a>
- 1 is the `.data` segment.

<a id="_405"></a>
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
