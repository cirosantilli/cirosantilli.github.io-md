# PAE

↑ **Parent:** [x86 Paging Tutorial](../x86-paging-split.md)

<a id="_260"></a>
Physical address extension.

<a id="_261"></a>
With 32 bits, only 4GB RAM can be addressed.

<a id="_262"></a>
This started becoming a limitation for large servers, so Intel introduced the PAE mechanism to Pentium Pro.

<a id="_263"></a>
To relieve the problem, Intel added 4 new address lines, so that 64GB could be addressed.

<a id="_264"></a>
Page table structure is also altered if PAE is on. The exact way in which it is altered depends on weather PSE is on or off.

<a id="_265"></a>
PAE is turned on and off via the `PAE` bit of `cr4`.

<a id="_266"></a>
Even if the total addressable memory is 64GB, individual process are still only able to use up to 4GB. The OS can however put different processes on different 4GB chunks.

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
