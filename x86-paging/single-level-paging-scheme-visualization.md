# Single level paging scheme visualization

↑ **Parent:** [Example: simplified single-level paging scheme](example-simplified-single-level-paging-scheme.md)

<a id="_83"></a>
This is how the memory could look like in a single level paging scheme:<a id="_84"></a>

```
Links   Data                    Physical address

      +-----------------------+ 2^32 - 1
      |                       |
      .                       .
      |                       |
      +-----------------------+ page0 + 4k
      | data of page 0        |
+---->+-----------------------+ page0
|     |                       |
|     .                       .
|     |                       |
|     +-----------------------+ pageN + 4k
|     | data of page N        |
|  +->+-----------------------+ pageN
|  |  |                       |
|  |  .                       .
|  |  |                       |
|  |  +-----------------------+ CR3 + 2^20 * 4
|  +--| entry[2^20-1] = pageN |
|     +-----------------------+ CR3 + 2^20 - 1 * 4
|     |                       |
|     .    many entires       .
|     |                       |
|     +-----------------------+ CR3 + 2 * 4
|  +--| entry[1] = page1      |
|  |  +-----------------------+ CR3 + 1 * 4
+-----| entry[0] = page0      |
   |  +-----------------------+ <--- CR3
   |  |                       |
   |  .                       .
   |  |                       |
   |  +-----------------------+ page1 + 4k
   |  | data of page 1        |
   +->+-----------------------+ page1
      |                       |
      .                       .
      |                       |
      +-----------------------+  0
```

<a id="_85"></a>
Notice that:<a id="_86"></a>

<a id="_87"></a>
- the CR3 register points to the first entry of the page table
<a id="_88"></a>
- the page table is just a large array with 2^20 page table entries
<a id="_89"></a>
- each entry is 4 bytes big, so the array takes up 4 MiB
<a id="_90"></a>
- each page table contains the physical address a page
<a id="_91"></a>
- each page is a 4 KiB aligned 4 KiB chunk of memory that user processes may use
<a id="_92"></a>
- we have 2^20 table entries. Since each page is 4 KiB == 2^12, this covers the whole 4 GiB (2^32) of 32-bit memory

## ↑ Ancestors (13)

1. [Example: simplified single-level paging scheme](example-simplified-single-level-paging-scheme.md)
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
