# Basic TLB operation

↑ **Parent:** [TLB](tlb.md)

<a id="_290"></a>
After a translation between linear and physical address happens, it is stored on the TLB. For example, a 4 entry TLB starts in the following state:<a id="_291"></a>

```
  valid  linear  physical
  -----  ------  --------
> 0      00000   00000
  0      00000   00000
  0      00000   00000
  0      00000   00000
```

<a id="_292"></a>
The `>` indicates the current entry to be replaced.

<a id="_293"></a>
And after a page linear address `00003` is translated to a physical address `00005`, the TLB becomes:<a id="_294"></a>

```
  valid  linear  physical
  -----  ------  --------
  1      00003   00005
> 0      00000   00000
  0      00000   00000
  0      00000   00000
```
and after a second translation of `00007` to `00009` it becomes:<a id="_295"></a>

```
  valid  linear  physical
  -----  ------  --------
  1      00003   00005
  1      00007   00009
> 0      00000   00000
  0      00000   00000
```

<a id="_296"></a>
Now if `00003` needs to be translated again, hardware first looks up the TLB and finds out its address with a single RAM access `00003 --> 00005`.

<a id="_297"></a>
Of course, `00000` is not on the TLB since no valid entry contains `00000` as a key.

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
