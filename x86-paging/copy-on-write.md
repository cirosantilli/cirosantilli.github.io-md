# Copy-on-write

↑ **Parent:** [Linux kernel usage](linux-kernel-usage.md)

<a id="_379"></a>
[https://en.wikipedia.org/wiki/Copy-on-write](https://en.wikipedia.org/wiki/Copy-on-write)

<a id="_380"></a>
Besides a missing page, a very common source of page faults is copy-on-write (COW).

<a id="_381"></a>
Page tables have extra flags that allow the OS to mark a page a read-only.

<a id="_382"></a>
Those page faults only happen when a process tries to write to the page, and not read from it.

<a id="_383"></a>
When Linux forks a process:<a id="_384"></a>

<a id="_385"></a>
- instead of copying all the pages, which is unnecessarily costly, it makes the page tables of the two process point to the same physical address.
<a id="_386"></a>
- it marks those linear addresses as read-only
<a id="_387"></a>
- whenever one of the processes tries to write to a page, the makes a copy of the physical memory, and updates the pages of the two process to point to the two different physical addresses

## ↑ Ancestors (13)

1. [Linux kernel usage](linux-kernel-usage.md)
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
