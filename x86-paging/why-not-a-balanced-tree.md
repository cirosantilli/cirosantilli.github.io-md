# Why not a balanced tree

↑ **Parent:** [Example: multi-level paging scheme](example-multi-level-paging-scheme.md)

Learned readers will ask themselves: so why use an unbalanced tree instead of balanced one, which offers better asymptotic times [https://en.wikipedia.org/wiki/Self-balancing_binary_search_tree?](https://en.wikipedia.org/wiki/Self-balancing_binary_search_tree?)

Likely:
- the maximum number of entries is small enough due to memory size limitations, that we won't waste too much memory with the root directory entry
- different entries would have different levels, and thus different access times
- tree rotations would likely make caching more complicated

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
