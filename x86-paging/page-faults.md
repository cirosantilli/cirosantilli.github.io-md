# Page faults

↑ **Parent:** [Example: simplified single-level paging scheme](example-simplified-single-level-paging-scheme.md)

<a id="_129"></a>
What if Process 1 tries to access `0x00003000`, which is not present?

<a id="_130"></a>
The hardware notifies the software via a Page Fault Exception.

<a id="_131"></a>
When an exception happens, the CPU jumps to an address that the OS had previously registered as the fault handler. This is usually done at boot time by the OS.

<a id="_132"></a>
This could happen for example due to a programming error:<a id="_133"></a>

```
int *is = malloc(1);
is[2] = 1;
```
but there are cases where it is not a bug, for example in Linux when:<a id="_134"></a>

<a id="_135"></a>
- <a id="_136"></a>
  the program wants to increase its stack.

  <a id="_137"></a>
  It just tries to accesses a certain byte in a given possible range, and if the OS is happy it adds that page to the process address space, otherwise, it sends a signal to the process.
<a id="_138"></a>
- <a id="_139"></a>
  the page was swapped to disk.

  <a id="_140"></a>
  The OS will need to do some work behind the processes back to get the page back into RAM.

  <a id="_141"></a>
  The OS can discover that this is the case based on the contents of the rest of the page table entry, since if the present flag is clear, the other entries of the page table entry are completely left for the OS to to what it wants.

  <a id="_142"></a>
  On Linux for example, when present = 0:<a id="_143"></a>

  <a id="_144"></a>
  - if all the fields of the page table entry are 0, invalid address.
  <a id="_145"></a>
  - else, the page has been swapped to disk, and the actual values of those fields encode the position of the page on the disk.

<a id="_146"></a>
In any case, the OS needs to know which address generated the Page Fault to be able to deal with the problem. This is why the nice IA32 developers set the value of `cr2` to that address whenever a Page Fault occurs. The exception handler can then just look into `cr2` to get the address.

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
