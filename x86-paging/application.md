# Application

↑ **Parent:** [x86 Paging Tutorial](../x86-paging-split.md)

<a id="_14"></a>
Paging makes it easier to compile and run two programs or threads at the same time on a single computer.

<a id="_15"></a>
For example, when you compile two programs, the compiler does not know if they are going to be running at the same time or not.

<a id="_16"></a>
So nothing prevents it from using the same [RAM](../random-access-memory.md) address, say, `0x1234`, to store a global variable.

<a id="_17"></a>
And thread [stacks](https://stackoverflow.com/questions/4584089/what-is-the-function-of-the-push-pop-instructions-used-on-registers-in-x86-ass/33583134#33583134), that must be contiguous and keep growing down until they overwrite each other, are an even bigger issue!

<a id="_18"></a>
But if two programs use the same address and run at the same time, this is obviously going to break them!

<a id="_19"></a>
Paging solves this problem beautifully by adding one degree of indirection:

<a id="_20"></a>
```
(logical) ------------> (physical)
             paging
```

<a id="_21"></a>
Where:<a id="_22"></a>

<a id="_23"></a>
- <a id="_24"></a>
  logical addresses are what userland programs see, e.g. the contents of `rsi` in `mov eax, [rsi]`.

  <a id="_25"></a>
  They are often called "virtual" addresses as well.
<a id="_26"></a>
- <a id="_27"></a>
  physical addresses can be though of the values that go to physical RAM index wires.

  <a id="_28"></a>
  But keep in mind that this is not 100% true because of further indirections such as:

  <a id="_29"></a>

  <a id="_30"></a>
  - [memory-mapped I/O regions](https://en.wikipedia.org/wiki/Memory-mapped_I/O)
  <a id="_31"></a>
  - [multi channel memory](https://en.wikipedia.org/wiki/Multi-channel_memory_architecture)

<a id="_32"></a>
[Compilers](../compiler.md) don't need to worry about other programs: they just use simple logical addresses.

<a id="_33"></a>
As far as programs are concerned, they think they can use any address between 0 and 4 GiB (2^32, `FFFFFFFF`) on 32-bit systems.

<a id="_34"></a>
The OS then sets up paging so that identical logical addresses will go into different physical addresses and not overwrite each other.

<a id="_35"></a>
This makes it much simpler to compile programs and run them at the same time.

<a id="_36"></a>
Paging achieves that goal, and in addition:<a id="_37"></a>

<a id="_38"></a>
- the switch between programs is very fast, because it is implemented by hardware
<a id="_39"></a>
- the memory of both programs can grow and shrink as needed without too much fragmentation
<a id="_40"></a>
- <a id="_41"></a>
  one program can never access the memory of another program, even if it wanted to.

  <a id="_42"></a>
  This is good both for security, and to prevent bugs in one program from crashing other programs.

<a id="_43"></a>
Or if you like non-funny jokes:

<a id="image-comparison-between-the-linux-kernel-userland-memory-virtualization-and-the-matrix"></a>
![](https://upload.wikimedia.org/wikipedia/commons/5/59/Funny_comparison_between_the_Linux_Kernel_and_The_Matrix_due_to_userland_memory_virtualization.png)

**[Figure 1](#image-comparison-between-the-linux-kernel-userland-memory-virtualization-and-the-matrix). Comparison between the Linux kernel userland memory virtualization and The Matrix**. [Source](https://commons.wikimedia.org/wiki/File:Funny_comparison_between_the_Linux_Kernel_and_The_Matrix_due_to_userland_memory_virtualization.png). Is this RAM real?

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
