# Multi-level paging scheme numerical translation example

↑ **Parent:** [Example: multi-level paging scheme](example-multi-level-paging-scheme.md)

<a id="_229"></a>
Page directory given to process by the OS:<a id="_230"></a>

```
entry index   entry address      page table address  present
-----------   ----------------   ------------------  --------
0             CR3 + 0      * 4   0x10000             1
1             CR3 + 1      * 4                       0
2             CR3 + 2      * 4   0x80000             1
3             CR3 + 3      * 4                       0
...
2^10-1        CR3 + 2^10-1 * 4                       0
```

<a id="_231"></a>
Page tables given to process by the OS at `PT1 = 0x10000000` (`0x10000` \* 4K):<a id="_232"></a>

```
entry index   entry address      page address  present
-----------   ----------------   ------------  -------
0             PT1 + 0      * 4   0x00001       1
1             PT1 + 1      * 4                 0
2             PT1 + 2      * 4   0x0000D       1
...                                  ...
2^10-1        PT1 + 2^10-1 * 4   0x00005       1
```

<a id="_233"></a>
Page tables given to process by the OS at `PT2  = 0x80000000` (`0x80000` \* 4K):<a id="_234"></a>

```
entry index   entry address     page address  present
-----------   ---------------   ------------  ------------
0             PT2 + 0     * 4   0x0000A       1
1             PT2 + 1     * 4   0x0000C       1
2             PT2 + 2     * 4                 0
...
2^10-1        PT2 + 0x3FF * 4   0x00003       1
```
where `PT1` and `PT2`: initial position of page table 1 and page table 2 for process 1 on RAM.

<a id="_235"></a>
With that setup, the following translations would happen:<a id="_236"></a>

```
linear    10 10 12 split  physical
--------  --------------  ----------
00000001  000 000 001     00001001
00001001  000 001 001     page fault
003FF001  000 3FF 001     00005001
00400000  001 000 000     page fault
00800001  002 000 001     0000A001
00801004  002 001 004     0000C004
00802004  002 002 004     page fault
00B00001  003 000 000     page fault
```

<a id="_237"></a>
Let's translate the linear address `0x00801004` step by step:<a id="_238"></a>

<a id="_239"></a>
- In binary the linear address is:<a id="_240"></a>

  ```
  0    0    8    0    1    0    0    4
  0000 0000 1000 0000 0001 0000 0000 0100
  ```
<a id="_241"></a>
- Grouping as `10 | 10 | 12` gives:<a id="_242"></a>

  ```
  0000000010 0000000001 000000000100
  0x2        0x1        0x4
  ```

  which gives:<a id="_243"></a>

  ```
  page directory entry = 0x2
  page table     entry = 0x1
  offset               = 0x4
  ```

  So the hardware looks for entry 2 of the page directory.
<a id="_244"></a>
- <a id="_245"></a>
  The page directory table says that the page table is located at `0x80000 * 4K = 0x80000000`. This is the first RAM access of the process.

  <a id="_246"></a>
  Since the page table entry is `0x1`, the hardware looks at entry 1 of the page table at `0x80000000`, which tells it that the physical page is located at address `0x0000C * 4K = 0x0000C000`. This is the second RAM access of the process.
<a id="_247"></a>
- Finally, the paging hardware adds the offset, and the final address is `0x0000C004`.

<a id="_248"></a>
Page faults occur if either a page directory entry or a page table entry is not present.

<a id="_249"></a>
The Intel manual gives a picture of this translation process in the image "Linear-Address Translation to a 4-KByte Page using 32-Bit Paging": [Figure 3. "x86 page translation process"](#image-x86-page-translation-process)

<a id="image-x86-page-translation-process"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/x86_page_translation_process.png" alt="" height="300">

**[Figure 3](#image-x86-page-translation-process). x86 page translation process**.

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
