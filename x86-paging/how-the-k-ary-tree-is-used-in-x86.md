# How the K-ary tree is used in x86

↑ **Parent:** [Example: multi-level paging scheme](example-multi-level-paging-scheme.md)

x86's multi-level paging scheme uses a 2 level K-ary tree with 2^10 bits on each level.

Addresses are now split as:
```
| directory (10 bits) | table (10 bits) | offset (12 bits) |
```

Then:
- the top 10 bits are used to walk the top level of the K-ary tree (`level0`)

  The top table is called a "directory of page tables".

  `cr3` now points to the location on RAM of the page directory of the current process instead of page tables.

  Page directory entries are very similar to page table entries except that they point to the physical addresses of page tables instead of physical addresses of pages.

  Each directory entry also takes up 4 bytes, just like page entries, so that makes 4 KiB per process minimum.

  Page directory entries also contain a valid flag: if invalid, the OS does not allocate a page table for that entry, and saves memory.

  Each process has one and only one page directory associated to it (and pointed to by `cr3`), so it will contain at least `2^10 = 1K` page directory entries, much better than the minimum 1M entries required on a single-level scheme.
- the next 10 bits are used to walk the second level of the K-ary tree (`level1`)

  Second level entries are also called page tables like the single level scheme.

  Page tables are only allocated only as needed by the OS.

  Each page table has only `2^10 = 1K` page table entries instead of `2^20` for the single paging scheme.

  Each process can now have up to `2^10` page tables instead of `2^20` for the single paging scheme.
- the offset is again not used for translation, it only gives the offset within a page

One reason for using 10 bits on the first two levels (and not, say, `12 | 8 | 12` ) is that each Page Table entry is 4 bytes long. Then the 2^10 entries of Page directories and Page Tables will fit nicely into 4Kb pages. This means that it faster and simpler to allocate and deallocate pages for that purpose.

## ↑ Ancestors (13)

1. [Example: multi-level paging scheme](example-multi-level-paging-scheme.md)
2. [x86 Paging Tutorial](../x86-paging-split.md)
3. [x86](../x86.md)
4. [List of instruction set architectures](../list-of-instruction-set-architectures.md)
5. [Instruction set architecture](../instruction-set-architecture.md)
6. [Processor (computing)](../processor-computing.md)
7. [Computer hardware component type](../computer-hardware-component-type.md)
8. [Computer hardware](../computer-hardware-split.md)
9. [Computer](../computer-split.md)
10. [Information technology](../information-technology.md)
11. [Area of technology](../area-of-technology.md)
12. [Technology](../technology-split.md)
13. [Ciro Santilli's Homepage](../split.md)
