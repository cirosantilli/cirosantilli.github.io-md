# Single level paging scheme numerical translation example

↑ **Parent:** [Example: simplified single-level paging scheme](example-simplified-single-level-paging-scheme.md)

<a id="_93"></a>
Suppose that the OS has setup the following page tables for process 1:<a id="_94"></a>

```
entry index   entry address       page address   present
-----------   ------------------  ------------   -------
0             CR3_1 + 0      * 4  0x00001        1
1             CR3_1 + 1      * 4  0x00000        1
2             CR3_1 + 2      * 4  0x00003        1
3             CR3_1 + 3      * 4                 0
...
2^20-1        CR3_1 + 2^20-1 * 4  0x00005        1
```
and for process 2:<a id="_95"></a>

```
entry index   entry address       page address   present
-----------   -----------------   ------------   -------
0             CR3_2 + 0      * 4  0x0000A        1
1             CR3_2 + 1      * 4  0x12345        1
2             CR3_2 + 2      * 4                 0
3             CR3_2 + 3      * 4  0x00003        1
...
2^20-1        CR3_2 + 2^20-1 * 4  0xFFFFF        1
```

<a id="_96"></a>
Before process 1 starts running, the OS sets its `cr3` to point to the page table 1 at `CR3_1`.

<a id="_97"></a>
When process 1 tries to access a linear address, this is the physical addresses that will be actually accessed:<a id="_98"></a>

```
linear     physical
---------  ---------
00000 001  00001 001
00000 002  00001 002
00000 003  00001 003
00000 FFF  00001 FFF
00001 000  00000 000
00001 001  00000 001
00001 FFF  00000 FFF
00002 000  00003 000
FFFFF 000  00005 000
```

<a id="_99"></a>
To switch to process 2, the OS simply sets `cr3` to `CR3_2`, and now the following translations would happen:<a id="_100"></a>

```
linear     physical
---------  ---------
00000 002  0000A 002
00000 003  0000A 003
00000 FFF  0000A FFF
00001 000  12345 000
00001 001  12345 001
00001 FFF  12345 FFF
00004 000  00003 000
FFFFF 000  FFFFF 000
```

<a id="_101"></a>
Step-by-step translation for process 1 of logical address `0x00000001` to physical address `0x00001001`:<a id="_102"></a>

<a id="_103"></a>
- <a id="_104"></a>
  split the linear address into two parts:

  <a id="_105"></a>
  ```
  | page (20 bits) | offset (12 bits) |
  ```

  <a id="_106"></a>
  So in this case we would have:  
  \*page = 0x00000. This part must be translated to a physical location.  
  \*offset = 0x001. This part is added directly to the page address, and is not translated: it contains the position within the page.
<a id="_107"></a>
- look into Page table 1 because `cr3` points to it.
<a id="_108"></a>
- The hardware knows that this entry is located at RAM address `CR3 + 0x00000 * 4 = CR3`:  
  \*`0x00000` because the page part of the logical address is `0x00000`  
  \*`4` because that is the fixed size in bytes of every page table entry
<a id="_109"></a>
- since it is present, the access is valid
<a id="_110"></a>
- by the page table, the location of page number `0x00000` is at `0x00001 * 4K = 0x00001000`.
<a id="_111"></a>
- <a id="_112"></a>
  to find the final physical address we just need to add the offset:

  <a id="_113"></a>
  ```
    00001 000
  + 00000 001
    ---------
    00001 001
  ```

  <a id="_114"></a>
  because `00001` is the physical address of the page looked up on the table and `001` is the offset.

  <a id="_115"></a>
  We shift `00001` by 12 bits because the pages are always aligned to 4 KiB.

  <a id="_116"></a>
  The offset is always simply added the physical address of the page.
<a id="_117"></a>
- the hardware then gets the memory at that physical location and puts it in a register.

<a id="_118"></a>
Another example: for logical address `0x00001001`:<a id="_119"></a>

<a id="_120"></a>
- the page part is `00001`, and the offset part is `001`
<a id="_121"></a>
- the hardware knows that its page table entry is located at RAM address: `CR3 + 1 * 4` (`1` because of the page part), and that is where it will look for it
<a id="_122"></a>
- it finds the page address `0x00000` there
<a id="_123"></a>
- so the final address is `0x00000 * 4k + 0x001 = 0x00000001`

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
