# The problem with single-level paging

↑ **Parent:** [Example: multi-level paging scheme](example-multi-level-paging-scheme.md)

<a id="_172"></a>
The problem with a single-level paging scheme is that it would take up too much RAM: 4G / 4K = 1M entries per process.

<a id="_173"></a>
If each entry is 4 bytes long, that would make 4M per process, which is too much even for a desktop computer: `ps -A | wc -l` says that I am running 244 processes right now, so that would take around 1GB of my RAM!

<a id="_174"></a>
For this reason, x86 developers decided to use a multi-level scheme that reduces RAM usage.

<a id="_175"></a>
The downside of this system is that is has a slightly higher access time, as we need to access RAM more times for each translation.

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
