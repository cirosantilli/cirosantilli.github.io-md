# Hardware implementation

↑ **Parent:** [x86 Paging Tutorial](../x86-paging-split.md)

<a id="_44"></a>
Paging is implemented by the [CPU](../central-processing-unit.md) hardware itself.

<a id="_45"></a>
Paging could be implemented in software, but that would be too slow, because every single RAM memory access uses it!

<a id="_46"></a>
Operating systems must setup and control paging by communicating to the CPU hardware. This is done mostly via:<a id="_47"></a>

<a id="_48"></a>
- the CR3 register, which tells the CPU where the page table is in RAM memory
<a id="_49"></a>
- <a id="_50"></a>
  writing the correct paging data structures to the RAM pointed to the CR3 register.

  <a id="_51"></a>
  Using RAM data structures is a common technique when lots of data must be transmitted to the CPU as it would cost too much to have such a large CPU register.

  <a id="_52"></a>
  The format of the configuration data structures is fixed by the hardware, but it is up to the OS to set up and manage those data structures on RAM correctly, and to tell the hardware where to find them (via `cr3`).

  <a id="_53"></a>
  Then some heavy caching is done to ensure that the RAM access will be fast, in particular using the TLB.

  <a id="_54"></a>
  Another notable example of RAM data structure used by the CPU is the [IDT](https://en.wikipedia.org/wiki/Interrupt_descriptor_table) which sets up interrupt handlers.

  <a id="_55"></a>
  The OS makes it impossible for programs to change the paging setup directly without going through the OS:
<a id="_56"></a>
- CR3 cannot be modified in ring 3. The OS runs in ring 0. See also:<a id="_57"></a>

  <a id="_58"></a>
  - [https://stackoverflow.com/questions/5957570/what-is-the-difference-between-the-kernel-space-and-the-user-space/44285809#44285809](https://stackoverflow.com/questions/5957570/what-is-the-difference-between-the-kernel-space-and-the-user-space/44285809#44285809)
  <a id="_59"></a>
  - [https://stackoverflow.com/questions/18717016/what-are-ring-0-and-ring-3-in-os](https://stackoverflow.com/questions/18717016/what-are-ring-0-and-ring-3-in-os)
<a id="_60"></a>
- the page table structures are made invisible to the process using paging itself!

<a id="_61"></a>
Processes can however make requests to the OS that cause the page tables to be modified, notably:<a id="_62"></a>

<a id="_63"></a>
- stack size changes
<a id="_64"></a>
- `brk` and `mmap` calls, see also: [https://stackoverflow.com/questions/6988487/what-does-brk-system-call-do/31082353#31082353](https://stackoverflow.com/questions/6988487/what-does-brk-system-call-do/31082353#31082353)

<a id="_65"></a>
The kernel then decides if the request will be granted or not in a controlled manner.

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
