# Kernel vs process memory layout

↑ **Parent:** [Linux kernel usage](linux-kernel-usage.md)

The Linux Kernel reserves two zones of virtual memory:
- one for kernel memory
- one for programs

The exact split is configured by `CONFIG_VMSPLIT_...`. By default:
- on 32-bit:
  - the bottom 3/4 is program space: `00000000` to `BFFFFFFF`
  - the top 1/4 is kernel memory: `C0000000` to `FFFFFFFF`, like this:
    ```
    ------------------ FFFFFFFF
    Kernel
    ------------------ C0000000
    ------------------ BFFFFFFF


    Process


    ------------------ 00000000
    ```
- on 64-bit: currently only 48-bits are actually used, split into two equally sized disjoint spaces. The Linux kernel just assigns:
  - the bottom part to processes `00000000 00000000` to `008FFFFF FFFFFFFF`
  - the top part to the kernel: `FFFF8000 00000000` to `FFFFFFFF FFFFFFFF`, like this:

    ```
    ------------------ FFFFFFFF
    Kernel
    ------------------ C0000000


    (not addressable)


    ------------------ BFFFFFFF
    Process
    ------------------ 00000000
    ```

Kernel memory [is also paged](https://stackoverflow.com/questions/18953598/is-it-true-that-whole-system-space-address-space-in-linux-does-not-use-demand-pa).

In previous versions, [the paging was continuous, but with HIGHMEM this changed](https://stackoverflow.com/questions/1658757/linux-3-1-virtual-address-split).

There is no clear physical memory split: [https://stackoverflow.com/questions/30471742/physical-memory-userspace-kernel-split-on-linux-x86-64](https://stackoverflow.com/questions/30471742/physical-memory-userspace-kernel-split-on-linux-x86-64)

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
