# Page table entries

↑ **Parent:** [Example: simplified single-level paging scheme](example-simplified-single-level-paging-scheme.md)

<a id="_147"></a>
The exact format of table entries is fixed by the hardware.

<a id="_148"></a>
Each page entry can be seen as a `struct` with many fields.

<a id="_149"></a>
The page table is then an array of `struct`.

<a id="_150"></a>
On this simplified example, the page table entries contain only two fields:<a id="_151"></a>

```
bits   function
-----  -----------------------------------------
20     physical address of the start of the page
1      present flag
```
so in this example the hardware designers could have chosen the size of the page table to b `21` instead of `32` as we've used so far.

<a id="_152"></a>
All real page table entries have other fields, notably fields to set pages to read-only for Copy-on-write. This will be explained elsewhere.

<a id="_153"></a>
It would be impractical to align things at 21 bits since memory is addressable by bytes and not bits. Therefore, even in only 21 bits are needed in this case, hardware designers would probably choose 32 to make access faster, and just reserve bits the remaining bits for later usage. The actual value on x86 is 32 bits.

<a id="_154"></a>
Here is a screenshot from the Intel manual image "Formats of CR3 and Paging-Structure Entries with 32-Bit Paging" showing the structure of a page table in all its glory: [Figure 2. "x86 page entry format"](#image-x86-page-entry-format).

<a id="image-x86-page-entry-format"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/x86_page_entry_format.png" alt="" height="300">

**[Figure 2](#image-x86-page-entry-format). x86 page entry format**.

<a id="_155"></a>
The fields are explained in the manual just after.

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
