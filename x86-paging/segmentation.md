# Segmentation

↑ **Parent:** [x86 Paging Tutorial](../x86-paging-split.md)

<a id="_66"></a>
In x86 systems, there may actually be 2 address translation steps:<a id="_67"></a>

<a id="_68"></a>
- first segmentation
<a id="_69"></a>
- then paging
like this:<a id="_70"></a>

```
(logical) ------------------> (linear) ------------> (physical)
             segmentation                 paging
```

<a id="_71"></a>
The major difference between paging and segmentation is that:<a id="_72"></a>

<a id="_73"></a>
- paging splits RAM into equal sized chunks called pages
<a id="_74"></a>
- segmentation splits memory into chunks of arbitrary sizes

<a id="_75"></a>
This is the main advantage of paging, since equal sized chunks make things more manageable by reducing memory fragmentation problems. See also:<a id="_76"></a>

<a id="_77"></a>
- [https://stackoverflow.com/questions/16643180/differences-or-similarities-between-segmented-paging-and-paged-segmentation](https://stackoverflow.com/questions/16643180/differences-or-similarities-between-segmented-paging-and-paged-segmentation)
<a id="_78"></a>
- [https://softwareengineering.stackexchange.com/questions/100047/why-not-segmentation](https://softwareengineering.stackexchange.com/questions/100047/why-not-segmentation)
<a id="_79"></a>
- [https://www.quora.com/What-is-the-difference-between-paging-and-segment-in-memory-management](https://www.quora.com/What-is-the-difference-between-paging-and-segment-in-memory-management)

<a id="_80"></a>
Paging came after segmentation historically, and largely replaced it for the implementation of virtual memory in modern OSs.

<a id="_81"></a>
Paging has become so much more popular that support for segmentation was dropped in x86-64 in 64-bit mode, the main mode of operation for new software, where it only exists in compatibility mode, which emulates IA-32.

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
