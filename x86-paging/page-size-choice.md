# Page size choice

↑ **Parent:** [Example: simplified single-level paging scheme](example-simplified-single-level-paging-scheme.md)

<a id="_156"></a>
Why are pages 4 KiB anyways?

<a id="_157"></a>
There is a trade-off between memory wasted in:<a id="_158"></a>

<a id="_159"></a>
- page tables
<a id="_160"></a>
- extra padding memory within pages

<a id="_161"></a>
This can be seen with the extreme cases:<a id="_162"></a>

<a id="_163"></a>
- if the page size were 1 byte:<a id="_164"></a>

  <a id="_165"></a>
  - granularity would be great, and the OS would never have to allocate unneeded padding memory
  <a id="_166"></a>
  - but the page table would have 2^32 entries, and take up the entire memory!
<a id="_167"></a>
- if the page size were 4 GiB:<a id="_168"></a>

  <a id="_169"></a>
  - we would need to swap 4 GiB to disk every time a new process becomes active
  <a id="_170"></a>
  - the page size would be a single entry, so it would take almost no memory at all

<a id="_171"></a>
x86 designers have found that 4 KiB pages are a good middle ground.

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
