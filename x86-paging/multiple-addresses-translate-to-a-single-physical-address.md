# Multiple addresses translate to a single physical address

↑ **Parent:** [Example: simplified single-level paging scheme](example-simplified-single-level-paging-scheme.md)

<a id="_124"></a>
The same linear address can translate to different physical addresses for different processes, depending only on the value inside `cr3`.

<a id="_125"></a>
Both linear addresses `00002 000` from process 1 and `00004 000` from process 2 point to the same physical address `00003 000`. This is completely allowed by the hardware, and it is up to the operating system to handle such cases.

<a id="_126"></a>
This often in normal operation because of Copy-on-write (COW), which be explained elsewhere.

<a id="_127"></a>
Such mappings are sometime called "aliases".

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
