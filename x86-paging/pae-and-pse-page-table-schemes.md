# PAE and PSE page table schemes

↑ **Parent:** [x86 Paging Tutorial](../x86-paging-split.md)

If either PAE and PSE are active, different paging level schemes are used:
- no PAE and no PSE: `10 | 10 | 12`
- no PAE and PSE: `10 | 22`.

  22 is the offset within the 4Mb page, since 22 bits address 4Mb.
- PAE and no PSE: `2 | 9 | 9 | 12`

  The design reason why 9 is used twice instead of 10 is that now entries cannot fit anymore into 32 bits, which were all filled up by 20 address bits and 12 meaningful or reserved flag bits.

  The reason is that 20 bits are not enough anymore to represent the address of page tables: 24 bits are now needed because of the 4 extra wires added to the processor.

  Therefore, the designers decided to increase entry size to 64 bits, and to make them fit into a single page table it is necessary reduce the number of entries to 2^9 instead of 2^10.

  The starting 2 is a new Page level called Page Directory Pointer Table (PDPT), since it points to page directories and fill in the 32 bit linear address. PDPTs are also 64 bits wide.

  `cr3` now points to PDPTs which must be on the fist four 4GB of memory and aligned on 32 bit multiples for addressing efficiency. This means that now `cr3` has 27 significative bits instead of 20: 2^5 for the 32 multiples \* 2^27 to complete the 2^32 of the first 4GB.
- PAE and PSE: `2 | 9 | 21`

  Designers decided to keep a 9 bit wide field to make it fit into a single page.

  This leaves 23 bits. Leaving 2 for the PDPT to keep things uniform with the PAE case without PSE leaves 21 for offset, meaning that pages are 2M wide instead of 4M.

## ↑ Ancestors (12)

1. [x86 Paging Tutorial](../x86-paging-split.md)
2. [x86](../x86.md)
3. [List of instruction set architectures](../list-of-instruction-set-architectures.md)
4. [Instruction set architecture](../instruction-set-architecture.md)
5. [Processor (computing)](../processor-computing.md)
6. [Computer hardware component type](../computer-hardware-component-type.md)
7. [Computer hardware](../computer-hardware-split.md)
8. [Computer](../computer-split.md)
9. [Information technology](../information-technology.md)
10. [Area of technology](../area-of-technology.md)
11. [Technology](../technology-split.md)
12. [Ciro Santilli's Homepage](../split.md)
