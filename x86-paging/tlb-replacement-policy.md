# TLB replacement policy

↑ **Parent:** [TLB](tlb.md)

<a id="_298"></a>
When TLB is filled up, older addresses are overwritten. Just like CPU cache, the replacement policy is a potentially complex operation, but a simple and reasonable heuristic is to remove the least recently used entry (LRU).

<a id="_299"></a>
With LRU, starting from state:<a id="_300"></a>

```
  valid  linear  physical
  -----  ------  --------
> 1      00003   00005
  1      00007   00009
  1      00009   00001
  1      0000B   00003
```
adding `0000D -> 0000A` would give:<a id="_301"></a>

```
  valid  linear  physical
  -----  ------  --------
  1      0000D   0000A
> 1      00007   00009
  1      00009   00001
  1      0000B   00003
```

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
