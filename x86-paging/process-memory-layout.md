# Process memory layout

↑ **Parent:** [Linux kernel usage](linux-kernel-usage.md)

For each process, the virtual address space looks like this:
```
------------------ 2^32 - 1
Stack (grows down)
v v v v v v v v v
------------------

(unmapped)

------------------ Maximum stack size.


(unmapped)


-------------------
mmap
-------------------


(unmapped)


-------------------
^^^^^^^^^^^^^^^^^^^
brk (grows up)
-------------------
BSS
-------------------
Data
-------------------
Text
-------------------

------------------- 0
```

The kernel maintains a list of pages that belong to each process, and synchronizes that with the paging.

If the program accesses memory that does not belong to it, the kernel handles a page-fault, and decides what to do:
- if it is above the maximum stack size, allocate those pages to the process
- otherwise, send a SIGSEGV to the process, which usually kills it

When an ELF file is loaded by the kernel to start a program with the `exec` system call, the kernel automatically registers text, data, BSS and stack for the program.

The `brk` and `mmap` areas can be modified by request of the program through the [`brk`](https://stackoverflow.com/questions/6988487/what-does-brk-system-call-do/31082353#31082353) and `mmap` system calls. But the kernel can also deny the program those areas if there is not enough memory.

`brk` and `mmap` can be used to implement `malloc`, or the so called "heap".

`mmap` is also used to load dynamically loaded libraries into the program's memory so that it can access and run it.

Stack allocation: [https://stackoverflow.com/questions/17671423/stack-allocation-for-process](https://stackoverflow.com/questions/17671423/stack-allocation-for-process)

Calculating exact addresses Things are complicated by:
- [Address Space Layout Randomization](https://en.wikipedia.org/wiki/Address_space_layout_randomization).
- the fact that environment variables, CLI arguments, and some ELF header data take up initial stack space: [https://unix.stackexchange.com/questions/145557/how-does-stack-allocation-work-in-linux/239323#239323](https://unix.stackexchange.com/questions/145557/how-does-stack-allocation-work-in-linux/239323#239323)

Why the text does not start at 0: [https://stackoverflow.com/questions/14795164/why-do-linux-program-text-sections-start-at-0x0804800-and-stack-tops-start-at-0](https://stackoverflow.com/questions/14795164/why-do-linux-program-text-sections-start-at-0x0804800-and-stack-tops-start-at-0)

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
