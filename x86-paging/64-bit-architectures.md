# 64-bit architectures

↑ **Parent:** [x86 Paging Tutorial](../x86-paging-split.md)

<a id="_250"></a>
64 bits is still too much address for current RAM sizes, so most architectures will use less bits.

<a id="_251"></a>
x86\_64 uses 48 bits (256 TiB), and legacy mode's PAE already allows 52-bit addresses (4 PiB). 56-bits is a likely future candidate.

<a id="_252"></a>
12 of those 48 bits are already reserved for the offset, which leaves 36 bits.

<a id="_253"></a>
If a 2 level approach is taken, the best split would be two 18 bit levels.

<a id="_254"></a>
But that would mean that the page directory would have `2^18 = 256K` entries, which would take too much RAM: close to a single-level paging for 32 bit architectures!

<a id="_255"></a>
Therefore, 64 bit architectures create even further page levels, commonly 3 or 4.

<a id="_256"></a>
x86\_64 uses 4 levels in a `9 | 9 | 9 | 9` scheme, so that the upper level only takes up only `2^9` higher level entries.

<a id="_257"></a>
The 48 bits are split equally into two disjoint parts:<a id="_258"></a>

```
----------------- FFFFFFFF FFFFFFFF
Top half
----------------- FFFF8000 00000000


Not addressable


----------------- 00007FFF FFFFFFFF
Bottom half
----------------- 00000000 00000000
```

<a id="_259"></a>
A 5-level scheme is emerging in 2016: [https://software.intel.com/sites/default/files/managed/2b/80/5-level_paging_white_paper.pdf](https://software.intel.com/sites/default/files/managed/2b/80/5-level_paging_white_paper.pdf) which allows 52-bit addresses with 4k pagetables.

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
