# PAE and PSE page table schemes

↑ **Parent:** [x86 Paging Tutorial](../x86-paging-split.md)

<a id="_270"></a>
If either PAE and PSE are active, different paging level schemes are used:<a id="_271"></a>

<a id="_272"></a>
- no PAE and no PSE: `10 | 10 | 12`
<a id="_273"></a>
- <a id="_274"></a>
  no PAE and PSE: `10 | 22`.

  <a id="_275"></a>
  22 is the offset within the 4Mb page, since 22 bits address 4Mb.
<a id="_276"></a>
- <a id="_277"></a>
  PAE and no PSE: `2 | 9 | 9 | 12`

  <a id="_278"></a>
  The design reason why 9 is used twice instead of 10 is that now entries cannot fit anymore into 32 bits, which were all filled up by 20 address bits and 12 meaningful or reserved flag bits.

  <a id="_279"></a>
  The reason is that 20 bits are not enough anymore to represent the address of page tables: 24 bits are now needed because of the 4 extra wires added to the processor.

  <a id="_280"></a>
  Therefore, the designers decided to increase entry size to 64 bits, and to make them fit into a single page table it is necessary reduce the number of entries to 2^9 instead of 2^10.

  <a id="_281"></a>
  The starting 2 is a new Page level called Page Directory Pointer Table (PDPT), since it points to page directories and fill in the 32 bit linear address. PDPTs are also 64 bits wide.

  <a id="_282"></a>
  `cr3` now points to PDPTs which must be on the fist four 4GB of memory and aligned on 32 bit multiples for addressing efficiency. This means that now `cr3` has 27 significative bits instead of 20: 2^5 for the 32 multiples \* 2^27 to complete the 2^32 of the first 4GB.
<a id="_283"></a>
- <a id="_284"></a>
  PAE and PSE: `2 | 9 | 21`

  <a id="_285"></a>
  Designers decided to keep a 9 bit wide field to make it fit into a single page.

  <a id="_286"></a>
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
