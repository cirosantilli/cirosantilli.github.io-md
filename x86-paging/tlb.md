# TLB

↑ **Parent:** [x86 Paging Tutorial](../x86-paging-split.md)

<a id="_287"></a>
The Translation Lookahead Buffer (TLB) is a cache for paging addresses.

<a id="_288"></a>
Since it is a cache, it shares many of the design issues of the CPU cache, such as associativity level.

<a id="_289"></a>
This section shall describe a simplified fully associative TLB with 4 single address entries. Note that like other caches, real TLBs are not usually fully associative.

**Table of contents**

- [Basic TLB operation](basic-tlb-operation.md)
- [TLB replacement policy](tlb-replacement-policy.md)
- [CAM](cam.md)
- [Invalidating TLB entries](invalidating-tlb-entries.md)

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
