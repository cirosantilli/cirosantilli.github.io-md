# CAM

↑ **Parent:** [TLB](tlb.md)

<a id="_302"></a>
Using the TLB makes translation faster, because the initial translation takes one access per TLB level, which means 2 on a simple 32 bit scheme, but 3 or 4 on 64 bit architectures.

<a id="_303"></a>
The TLB is usually implemented as an expensive type of RAM called content-addressable memory (CAM). CAM implements an associative map on hardware, that is, a structure that given a key (linear address), retrieves a value.

<a id="_304"></a>
Mappings could also be implemented on RAM addresses, but CAM mappings may required much less entries than a RAM mapping.

<a id="_305"></a>
For example, a map in which:<a id="_306"></a>

<a id="_307"></a>
- both keys and values have 20 bits (the case of a simple paging schemes)
<a id="_308"></a>
- at most 4 values need to be stored at each time
could be stored in a TLB with 4 entries:

<a id="_309"></a>
```
linear  physical
------  --------
00000   00001
00001   00010
00010   00011
FFFFF   00000
```

<a id="_310"></a>
However, to implement this with RAM, it would be necessary to have 2^20 addresses:<a id="_311"></a>

```
linear  physical
------  --------
00000   00001
00001   00010
00010   00011
... (from 00011 to FFFFE)
FFFFF   00000
```
which would be even more expensive than using a TLB.

## ↑ Ancestors (13)

1. [TLB](tlb.md)
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
