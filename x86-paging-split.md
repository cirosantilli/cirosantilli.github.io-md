# x86 Paging Tutorial

↑ **Parent:** [x86](x86.md)  
🏷️ **Tags:** [The best articles by Ciro Santilli](articles-split.md)

<a id="_2"></a>
This tutorial explains the very basics of how paging works, with focus on [x86](x86.md), although most high level concepts will also apply to other [instruction set architectures](instruction-set-architecture.md), e.g. [ARM](arm-architecture-family.md).

<a id="_3"></a>
The goals are to:<a id="_4"></a>

<a id="_5"></a>
- demonstrate minimal concrete simplified paging examples that will be useful to those learning paging for the first time
<a id="_6"></a>
- explain the motivation behind paging

<a id="_7"></a>
This tutorial was extracted and expanded from [this Stack Overflow answer](https://stackoverflow.com/a/18431262/895245).

**Table of contents**

- [Sample code](x86-paging/sample-code.md)
- [Intel manual](x86-paging/intel-manual.md)
- [Application](x86-paging/application.md)
- [Hardware implementation](x86-paging/hardware-implementation.md)
- [Segmentation](x86-paging/segmentation.md)
- [Example: simplified single-level paging scheme](x86-paging/example-simplified-single-level-paging-scheme.md)
  - [Single level paging scheme visualization](x86-paging/single-level-paging-scheme-visualization.md)
  - [Single level paging scheme numerical translation example](x86-paging/single-level-paging-scheme-numerical-translation-example.md)
  - [Multiple addresses translate to a single physical address](x86-paging/multiple-addresses-translate-to-a-single-physical-address.md)
  - [Identity mapping](x86-paging/identity-mapping.md)
  - [Page faults](x86-paging/page-faults.md)
  - [Page table entries](x86-paging/page-table-entries.md)
  - [Page size choice](x86-paging/page-size-choice.md)
- [Example: multi-level paging scheme](x86-paging/example-multi-level-paging-scheme.md)
  - [The problem with single-level paging](x86-paging/the-problem-with-single-level-paging.md)
  - [K-ary trees to the rescue](x86-paging/k-ary-trees-to-the-rescue.md)
  - [Why not a balanced tree](x86-paging/why-not-a-balanced-tree.md)
  - [How the K-ary tree is used in x86](x86-paging/how-the-k-ary-tree-is-used-in-x86.md)
  - [Multi-level paging scheme numerical translation example](x86-paging/multi-level-paging-scheme-numerical-translation-example.md)
- [64-bit architectures](x86-paging/64-bit-architectures.md)
- [PAE](x86-paging/pae.md)
- [PSE](x86-paging/pse.md)
- [PAE and PSE page table schemes](x86-paging/pae-and-pse-page-table-schemes.md)
- [TLB](x86-paging/tlb.md)
  - [Basic TLB operation](x86-paging/basic-tlb-operation.md)
  - [TLB replacement policy](x86-paging/tlb-replacement-policy.md)
  - [CAM](x86-paging/cam.md)
  - [Invalidating TLB entries](x86-paging/invalidating-tlb-entries.md)
- [Linux kernel usage](x86-paging/linux-kernel-usage.md)
  - [Play with physical addresses in Linux](x86-paging/play-with-physical-addresses-in-linux.md)
  - [Kernel vs process memory layout](x86-paging/kernel-vs-process-memory-layout.md)
  - [Process memory layout](x86-paging/process-memory-layout.md)
  - [Copy-on-write](x86-paging/copy-on-write.md)
  - [Linux source tree](x86-paging/linux-source-tree.md)
- [Memory management unit](x86-paging/memory-management-unit.md)
- [Second Level Address Translation](x86-paging/second-level-address-translation.md)
- [Other architectures](x86-paging/other-architectures.md)
  - [ARM](x86-paging/arm.md)
- [Bibliography](x86-paging/bibliography.md)

## ↑ Ancestors (11)

1. [x86](x86.md)
2. [List of instruction set architectures](list-of-instruction-set-architectures.md)
3. [Instruction set architecture](instruction-set-architecture.md)
4. [Processor (computing)](processor-computing.md)
5. [Computer hardware component type](computer-hardware-component-type.md)
6. [Computer hardware](computer-hardware-split.md)
7. [Computer](computer-split.md)
8. [Information technology](information-technology.md)
9. [Area of technology](area-of-technology.md)
10. [Technology](technology-split.md)
11. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (2)

- [The best articles by Ciro Santilli](articles-split.md)
- [Programming languages](skills/programming-languages.md)
