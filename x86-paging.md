# x86 Paging Tutorial

↑ **Parent:** [x86](computer-hardware.md#x86)  
🏷️ **Tags:** [The best articles by Ciro Santilli](articles.md)

<a id="_2"></a>
This tutorial explains the very basics of how paging works, with focus on [x86](computer-hardware.md#x86), although most high level concepts will also apply to other [instruction set architectures](computer-hardware.md#instruction-set-architecture), e.g. [ARM](computer-hardware.md#arm-architecture-family).

<a id="_3"></a>
The goals are to:<a id="_4"></a>

<a id="_5"></a>
- demonstrate minimal concrete simplified paging examples that will be useful to those learning paging for the first time
<a id="_6"></a>
- explain the motivation behind paging

<a id="_7"></a>
This tutorial was extracted and expanded from [this Stack Overflow answer](https://stackoverflow.com/a/18431262/895245).

**Table of contents**

- [Sample code](#sample-code)
- [Intel manual](#intel-manual)
- [Application](#application)
- [Hardware implementation](#hardware-implementation)
- [Segmentation](#segmentation)
- [Example: simplified single-level paging scheme](#example-simplified-single-level-paging-scheme)
  - [Single level paging scheme visualization](#single-level-paging-scheme-visualization)
  - [Single level paging scheme numerical translation example](#single-level-paging-scheme-numerical-translation-example)
  - [Multiple addresses translate to a single physical address](#multiple-addresses-translate-to-a-single-physical-address)
  - [Identity mapping](#identity-mapping)
  - [Page faults](#page-faults)
  - [Page table entries](#page-table-entries)
  - [Page size choice](#page-size-choice)
- [Example: multi-level paging scheme](#example-multi-level-paging-scheme)
  - [The problem with single-level paging](#the-problem-with-single-level-paging)
  - [K-ary trees to the rescue](#k-ary-trees-to-the-rescue)
  - [Why not a balanced tree](#why-not-a-balanced-tree)
  - [How the K-ary tree is used in x86](#how-the-k-ary-tree-is-used-in-x86)
  - [Multi-level paging scheme numerical translation example](#multi-level-paging-scheme-numerical-translation-example)
- [64-bit architectures](#64-bit-architectures)
- [PAE](#pae)
- [PSE](#pse)
- [PAE and PSE page table schemes](#pae-and-pse-page-table-schemes)
- [TLB](#tlb)
  - [Basic TLB operation](#basic-tlb-operation)
  - [TLB replacement policy](#tlb-replacement-policy)
  - [CAM](#cam)
  - [Invalidating TLB entries](#invalidating-tlb-entries)
- [Linux kernel usage](#linux-kernel-usage)
  - [Play with physical addresses in Linux](#play-with-physical-addresses-in-linux)
  - [Kernel vs process memory layout](#kernel-vs-process-memory-layout)
  - [Process memory layout](#process-memory-layout)
  - [Copy-on-write](#copy-on-write)
  - [Linux source tree](#linux-source-tree)
- [Memory management unit](#memory-management-unit)
- [Second Level Address Translation](#second-level-address-translation)
- [Other architectures](#other-architectures)
  - [ARM](#arm)
- [Bibliography](#bibliography)

## Sample code

↑ **Parent:** [x86 Paging Tutorial](x86-paging.md)

<a id="_8"></a>
Minimal example: [https://github.com/cirosantilli/x86-bare-metal-examples/blob/5c672f73884a487414b3e21bd9e579c67cd77621/paging.S](https://github.com/cirosantilli/x86-bare-metal-examples/blob/5c672f73884a487414b3e21bd9e579c67cd77621/paging.S)

<a id="_9"></a>
Like everything else in programming, the only way to really understand this is to play with minimal examples.

<a id="_10"></a>
What makes this a "hard" subject is that the minimal example is large because you need to make your own small [OS](systems-programming.md#operating-system).

## Intel manual

↑ **Parent:** [x86 Paging Tutorial](x86-paging.md)

<a id="_11"></a>
Although it is impossible to understand without examples in mind, try to get familiar with the manuals as soon as possible.

<a id="_12"></a>
Intel describes paging in the [Intel Manual Volume 3 System Programming Guide - 325384-056US September 2015](https://web.archive.org/web/20151025081259/http://www.intel.com/content/dam/www/public/us/en/documents/manuals/64-ia-32-architectures-software-developer-system-programming-manual-325384.pdf) Chapter 4 "Paging".

<a id="_13"></a>
Specially interesting is Figure 4-4 "Formats of CR3 and Paging-Structure Entries with 32-Bit Paging", which gives the key data structures.

## Application

↑ **Parent:** [x86 Paging Tutorial](x86-paging.md)

<a id="_14"></a>
Paging makes it easier to compile and run two programs or threads at the same time on a single computer.

<a id="_15"></a>
For example, when you compile two programs, the compiler does not know if they are going to be running at the same time or not.

<a id="_16"></a>
So nothing prevents it from using the same [RAM](computer-hardware.md#random-access-memory) address, say, `0x1234`, to store a global variable.

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
[Compilers](software.md#compiler) don't need to worry about other programs: they just use simple logical addresses.

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

## Hardware implementation

↑ **Parent:** [x86 Paging Tutorial](x86-paging.md)

<a id="_44"></a>
Paging is implemented by the [CPU](computer-hardware.md#central-processing-unit) hardware itself.

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

## Segmentation

↑ **Parent:** [x86 Paging Tutorial](x86-paging.md)

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

## Example: simplified single-level paging scheme

↑ **Parent:** [x86 Paging Tutorial](x86-paging.md)

<a id="_82"></a>
This is an example of how paging operates on a simplified version of a x86 architecture to implement a virtual memory space with a `20 | 12` address split (4 KiB page size).

### Single level paging scheme visualization

↑ **Parent:** [Example: simplified single-level paging scheme](#example-simplified-single-level-paging-scheme)

<a id="_83"></a>
This is how the memory could look like in a single level paging scheme:<a id="_84"></a>

```
Links   Data                    Physical address

      +-----------------------+ 2^32 - 1
      |                       |
      .                       .
      |                       |
      +-----------------------+ page0 + 4k
      | data of page 0        |
+---->+-----------------------+ page0
|     |                       |
|     .                       .
|     |                       |
|     +-----------------------+ pageN + 4k
|     | data of page N        |
|  +->+-----------------------+ pageN
|  |  |                       |
|  |  .                       .
|  |  |                       |
|  |  +-----------------------+ CR3 + 2^20 * 4
|  +--| entry[2^20-1] = pageN |
|     +-----------------------+ CR3 + 2^20 - 1 * 4
|     |                       |
|     .    many entires       .
|     |                       |
|     +-----------------------+ CR3 + 2 * 4
|  +--| entry[1] = page1      |
|  |  +-----------------------+ CR3 + 1 * 4
+-----| entry[0] = page0      |
   |  +-----------------------+ <--- CR3
   |  |                       |
   |  .                       .
   |  |                       |
   |  +-----------------------+ page1 + 4k
   |  | data of page 1        |
   +->+-----------------------+ page1
      |                       |
      .                       .
      |                       |
      +-----------------------+  0
```

<a id="_85"></a>
Notice that:<a id="_86"></a>

<a id="_87"></a>
- the CR3 register points to the first entry of the page table
<a id="_88"></a>
- the page table is just a large array with 2^20 page table entries
<a id="_89"></a>
- each entry is 4 bytes big, so the array takes up 4 MiB
<a id="_90"></a>
- each page table contains the physical address a page
<a id="_91"></a>
- each page is a 4 KiB aligned 4 KiB chunk of memory that user processes may use
<a id="_92"></a>
- we have 2^20 table entries. Since each page is 4 KiB == 2^12, this covers the whole 4 GiB (2^32) of 32-bit memory

### Single level paging scheme numerical translation example

↑ **Parent:** [Example: simplified single-level paging scheme](#example-simplified-single-level-paging-scheme)

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

### Multiple addresses translate to a single physical address

↑ **Parent:** [Example: simplified single-level paging scheme](#example-simplified-single-level-paging-scheme)

<a id="_124"></a>
The same linear address can translate to different physical addresses for different processes, depending only on the value inside `cr3`.

<a id="_125"></a>
Both linear addresses `00002 000` from process 1 and `00004 000` from process 2 point to the same physical address `00003 000`. This is completely allowed by the hardware, and it is up to the operating system to handle such cases.

<a id="_126"></a>
This often in normal operation because of Copy-on-write (COW), which be explained elsewhere.

<a id="_127"></a>
Such mappings are sometime called "aliases".

### Identity mapping

↑ **Parent:** [Example: simplified single-level paging scheme](#example-simplified-single-level-paging-scheme)

<a id="_128"></a>
`FFFFF 000` points to its own physical address `FFFFF 000`. This kind of translation is called an "identity mapping", and can be very convenient for OS-level debugging.

### Page faults

↑ **Parent:** [Example: simplified single-level paging scheme](#example-simplified-single-level-paging-scheme)

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

### Page table entries

↑ **Parent:** [Example: simplified single-level paging scheme](#example-simplified-single-level-paging-scheme)

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

### Page size choice

↑ **Parent:** [Example: simplified single-level paging scheme](#example-simplified-single-level-paging-scheme)

<a id="_156"></a>
Why are pages 4 KiB anyways?

<a id="_157"></a>
There is a trade-off between memory wasted in:<a id="_158"></a>

<a id="_159"></a>
- page tables
<a id="_160"></a>
- extra padding memory within pages

<a id="_161"></a>
This can be seen with the extreme cases:<a id="_162"></a>

<a id="_163"></a>
- if the page size were 1 byte:<a id="_164"></a>

  <a id="_165"></a>
  - granularity would be great, and the OS would never have to allocate unneeded padding memory
  <a id="_166"></a>
  - but the page table would have 2^32 entries, and take up the entire memory!
<a id="_167"></a>
- if the page size were 4 GiB:<a id="_168"></a>

  <a id="_169"></a>
  - we would need to swap 4 GiB to disk every time a new process becomes active
  <a id="_170"></a>
  - the page size would be a single entry, so it would take almost no memory at all

<a id="_171"></a>
x86 designers have found that 4 KiB pages are a good middle ground.

## Example: multi-level paging scheme

↑ **Parent:** [x86 Paging Tutorial](x86-paging.md)

### The problem with single-level paging

↑ **Parent:** [Example: multi-level paging scheme](#example-multi-level-paging-scheme)

<a id="_172"></a>
The problem with a single-level paging scheme is that it would take up too much RAM: 4G / 4K = 1M entries per process.

<a id="_173"></a>
If each entry is 4 bytes long, that would make 4M per process, which is too much even for a desktop computer: `ps -A | wc -l` says that I am running 244 processes right now, so that would take around 1GB of my RAM!

<a id="_174"></a>
For this reason, x86 developers decided to use a multi-level scheme that reduces RAM usage.

<a id="_175"></a>
The downside of this system is that is has a slightly higher access time, as we need to access RAM more times for each translation.

### K-ary trees to the rescue

↑ **Parent:** [Example: multi-level paging scheme](#example-multi-level-paging-scheme)

<a id="_176"></a>
The algorithmically minded will have noticed that paging requires [associative array](computer-science.md#associative-array) (like Java `Map` of Python `dict()`) abstract data structure where:<a id="_177"></a>

<a id="_178"></a>
- the keys are linear pages addresses, thus of integer type
<a id="_179"></a>
- the values are physical page addresses, also of integer type

<a id="_180"></a>
The single level paging scheme uses a simple array implementation of the associative array:<a id="_181"></a>

<a id="_182"></a>
- the keys are the array index
<a id="_183"></a>
- this implementation is very fast in time
<a id="_184"></a>
- but it is too inefficient in memory
and in C pseudo-code it looks like this:<a id="_185"></a>

```
linear_address[0]      = physical_address_0
linear_address[1]      = physical_address_1
linear_address[2]      = physical_address_2
...
linear_address[2^20-1] = physical_address_N
```

<a id="_186"></a>
But there another simple associative array implementation that overcomes the memory problem: an (unbalanced) [k-ary tree](mathematics.md#k-ary-tree).

<a id="_187"></a>
A K-ary tree, is just like a [binary tree](mathematics.md#binary-tree), but with K children instead of 2.

<a id="_188"></a>
Using a K-ary tree instead of an array implementation has the following trade-offs:<a id="_189"></a>

<a id="_190"></a>
- it uses way less memory
<a id="_191"></a>
- it is slower since we have to de-reference extra pointers

<a id="_192"></a>
In C-pseudo code, a 2-level K-ary tree with `K = 2^10` looks like this:<a id="_193"></a>

```
level0[0] = &level1_0[0]
    level1_0[0]      = physical_address_0_0
    level1_0[1]      = physical_address_0_1
    ...
    level1_0[2^10-1] = physical_address_0_N
level0[1] = &level1_1[0]
    level1_1[0]      = physical_address_1_0
    level1_1[1]      = physical_address_1_1
    ...
    level1_1[2^10-1] = physical_address_1_N
...
level0[N] = &level1_N[0]
    level1_N[0]      = physical_address_N_0
    level1_N[1]      = physical_address_N_1
    ...
    level1_N[2^10-1] = physical_address_N_N
```
and we have the following arrays:<a id="_194"></a>

<a id="_195"></a>
- one `directory`, which has `2^10` elements. Each element contains a pointer to a page table array.
<a id="_196"></a>
- up to 2^10 `pagetable` arrays. Each one has `2^10` 4 byte page entries.
and it still contains `2^10 * 2^10 = 2^20` possible keys.

<a id="_197"></a>
K-ary trees can save up a lot of space, because if we only have one key, then we only need the following arrays:<a id="_198"></a>

<a id="_199"></a>
- one `directory` with 2^10 entries
<a id="_200"></a>
- one `pagetable` at `directory[0]` with 2^10 entries
<a id="_201"></a>
- all other `directory[i]` are marked as invalid, don't point to anything, and we don't allocate `pagetable` for them at all

### Why not a balanced tree

↑ **Parent:** [Example: multi-level paging scheme](#example-multi-level-paging-scheme)

<a id="_202"></a>
Learned readers will ask themselves: so why use an unbalanced tree instead of balanced one, which offers better asymptotic times [https://en.wikipedia.org/wiki/Self-balancing_binary_search_tree?](https://en.wikipedia.org/wiki/Self-balancing_binary_search_tree?)

<a id="_203"></a>
Likely:<a id="_204"></a>

<a id="_205"></a>
- the maximum number of entries is small enough due to memory size limitations, that we won't waste too much memory with the root directory entry
<a id="_206"></a>
- different entries would have different levels, and thus different access times
<a id="_207"></a>
- tree rotations would likely make caching more complicated

### How the K-ary tree is used in x86

↑ **Parent:** [Example: multi-level paging scheme](#example-multi-level-paging-scheme)

<a id="_208"></a>
x86's multi-level paging scheme uses a 2 level K-ary tree with 2^10 bits on each level.

<a id="_209"></a>
Addresses are now split as:<a id="_210"></a>

```
| directory (10 bits) | table (10 bits) | offset (12 bits) |
```

<a id="_211"></a>
Then:<a id="_212"></a>

<a id="_213"></a>
- <a id="_214"></a>
  the top 10 bits are used to walk the top level of the K-ary tree (`level0`)

  <a id="_215"></a>
  The top table is called a "directory of page tables".

  <a id="_216"></a>
  `cr3` now points to the location on RAM of the page directory of the current process instead of page tables.

  <a id="_217"></a>
  Page directory entries are very similar to page table entries except that they point to the physical addresses of page tables instead of physical addresses of pages.

  <a id="_218"></a>
  Each directory entry also takes up 4 bytes, just like page entries, so that makes 4 KiB per process minimum.

  <a id="_219"></a>
  Page directory entries also contain a valid flag: if invalid, the OS does not allocate a page table for that entry, and saves memory.

  <a id="_220"></a>
  Each process has one and only one page directory associated to it (and pointed to by `cr3`), so it will contain at least `2^10 = 1K` page directory entries, much better than the minimum 1M entries required on a single-level scheme.
<a id="_221"></a>
- <a id="_222"></a>
  the next 10 bits are used to walk the second level of the K-ary tree (`level1`)

  <a id="_223"></a>
  Second level entries are also called page tables like the single level scheme.

  <a id="_224"></a>
  Page tables are only allocated only as needed by the OS.

  <a id="_225"></a>
  Each page table has only `2^10 = 1K` page table entries instead of `2^20` for the single paging scheme.

  <a id="_226"></a>
  Each process can now have up to `2^10` page tables instead of `2^20` for the single paging scheme.
<a id="_227"></a>
- the offset is again not used for translation, it only gives the offset within a page

<a id="_228"></a>
One reason for using 10 bits on the first two levels (and not, say, `12 | 8 | 12` ) is that each Page Table entry is 4 bytes long. Then the 2^10 entries of Page directories and Page Tables will fit nicely into 4Kb pages. This means that it faster and simpler to allocate and deallocate pages for that purpose.

### Multi-level paging scheme numerical translation example

↑ **Parent:** [Example: multi-level paging scheme](#example-multi-level-paging-scheme)

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

## 64-bit architectures

↑ **Parent:** [x86 Paging Tutorial](x86-paging.md)

<a id="_250"></a>
64 bits is still too much address for current RAM sizes, so most architectures will use less bits.

<a id="_251"></a>
x86\_64 uses 48 bits (256 TiB), and legacy mode's PAE already allows 52-bit addresses (4 PiB). 56-bits is a likely future candidate.

<a id="_252"></a>
12 of those 48 bits are already reserved for the offset, which leaves 36 bits.

<a id="_253"></a>
If a 2 level approach is taken, the best split would be two 18 bit levels.

<a id="_254"></a>
But that would mean that the page directory would have `2^18 = 256K` entries, which would take too much RAM: close to a single-level paging for 32 bit architectures!

<a id="_255"></a>
Therefore, 64 bit architectures create even further page levels, commonly 3 or 4.

<a id="_256"></a>
x86\_64 uses 4 levels in a `9 | 9 | 9 | 9` scheme, so that the upper level only takes up only `2^9` higher level entries.

<a id="_257"></a>
The 48 bits are split equally into two disjoint parts:<a id="_258"></a>

```
----------------- FFFFFFFF FFFFFFFF
Top half
----------------- FFFF8000 00000000


Not addressable


----------------- 00007FFF FFFFFFFF
Bottom half
----------------- 00000000 00000000
```

<a id="_259"></a>
A 5-level scheme is emerging in 2016: [https://software.intel.com/sites/default/files/managed/2b/80/5-level_paging_white_paper.pdf](https://software.intel.com/sites/default/files/managed/2b/80/5-level_paging_white_paper.pdf) which allows 52-bit addresses with 4k pagetables.

## PAE

↑ **Parent:** [x86 Paging Tutorial](x86-paging.md)

<a id="_260"></a>
Physical address extension.

<a id="_261"></a>
With 32 bits, only 4GB RAM can be addressed.

<a id="_262"></a>
This started becoming a limitation for large servers, so Intel introduced the PAE mechanism to Pentium Pro.

<a id="_263"></a>
To relieve the problem, Intel added 4 new address lines, so that 64GB could be addressed.

<a id="_264"></a>
Page table structure is also altered if PAE is on. The exact way in which it is altered depends on weather PSE is on or off.

<a id="_265"></a>
PAE is turned on and off via the `PAE` bit of `cr4`.

<a id="_266"></a>
Even if the total addressable memory is 64GB, individual process are still only able to use up to 4GB. The OS can however put different processes on different 4GB chunks.

## PSE

↑ **Parent:** [x86 Paging Tutorial](x86-paging.md)

<a id="_267"></a>
Page size extension.

<a id="_268"></a>
Allows for pages to be 4M (or 2M if PAE is on) in length instead of 4K.

<a id="_269"></a>
PSE is turned on and off via the `PSE` bit of `cr4`.

## PAE and PSE page table schemes

↑ **Parent:** [x86 Paging Tutorial](x86-paging.md)

<a id="_270"></a>
If either PAE and PSE are active, different paging level schemes are used:<a id="_271"></a>

<a id="_272"></a>
- no PAE and no PSE: `10 | 10 | 12`
<a id="_273"></a>
- <a id="_274"></a>
  no PAE and PSE: `10 | 22`.

  <a id="_275"></a>
  22 is the offset within the 4Mb page, since 22 bits address 4Mb.
<a id="_276"></a>
- <a id="_277"></a>
  PAE and no PSE: `2 | 9 | 9 | 12`

  <a id="_278"></a>
  The design reason why 9 is used twice instead of 10 is that now entries cannot fit anymore into 32 bits, which were all filled up by 20 address bits and 12 meaningful or reserved flag bits.

  <a id="_279"></a>
  The reason is that 20 bits are not enough anymore to represent the address of page tables: 24 bits are now needed because of the 4 extra wires added to the processor.

  <a id="_280"></a>
  Therefore, the designers decided to increase entry size to 64 bits, and to make them fit into a single page table it is necessary reduce the number of entries to 2^9 instead of 2^10.

  <a id="_281"></a>
  The starting 2 is a new Page level called Page Directory Pointer Table (PDPT), since it points to page directories and fill in the 32 bit linear address. PDPTs are also 64 bits wide.

  <a id="_282"></a>
  `cr3` now points to PDPTs which must be on the fist four 4GB of memory and aligned on 32 bit multiples for addressing efficiency. This means that now `cr3` has 27 significative bits instead of 20: 2^5 for the 32 multiples \* 2^27 to complete the 2^32 of the first 4GB.
<a id="_283"></a>
- <a id="_284"></a>
  PAE and PSE: `2 | 9 | 21`

  <a id="_285"></a>
  Designers decided to keep a 9 bit wide field to make it fit into a single page.

  <a id="_286"></a>
  This leaves 23 bits. Leaving 2 for the PDPT to keep things uniform with the PAE case without PSE leaves 21 for offset, meaning that pages are 2M wide instead of 4M.

## TLB

↑ **Parent:** [x86 Paging Tutorial](x86-paging.md)

<a id="_287"></a>
The Translation Lookahead Buffer (TLB) is a cache for paging addresses.

<a id="_288"></a>
Since it is a cache, it shares many of the design issues of the CPU cache, such as associativity level.

<a id="_289"></a>
This section shall describe a simplified fully associative TLB with 4 single address entries. Note that like other caches, real TLBs are not usually fully associative.

### Basic TLB operation

↑ **Parent:** [TLB](#tlb)

<a id="_290"></a>
After a translation between linear and physical address happens, it is stored on the TLB. For example, a 4 entry TLB starts in the following state:<a id="_291"></a>

```
  valid  linear  physical
  -----  ------  --------
> 0      00000   00000
  0      00000   00000
  0      00000   00000
  0      00000   00000
```

<a id="_292"></a>
The `>` indicates the current entry to be replaced.

<a id="_293"></a>
And after a page linear address `00003` is translated to a physical address `00005`, the TLB becomes:<a id="_294"></a>

```
  valid  linear  physical
  -----  ------  --------
  1      00003   00005
> 0      00000   00000
  0      00000   00000
  0      00000   00000
```
and after a second translation of `00007` to `00009` it becomes:<a id="_295"></a>

```
  valid  linear  physical
  -----  ------  --------
  1      00003   00005
  1      00007   00009
> 0      00000   00000
  0      00000   00000
```

<a id="_296"></a>
Now if `00003` needs to be translated again, hardware first looks up the TLB and finds out its address with a single RAM access `00003 --> 00005`.

<a id="_297"></a>
Of course, `00000` is not on the TLB since no valid entry contains `00000` as a key.

### TLB replacement policy

↑ **Parent:** [TLB](#tlb)

<a id="_298"></a>
When TLB is filled up, older addresses are overwritten. Just like CPU cache, the replacement policy is a potentially complex operation, but a simple and reasonable heuristic is to remove the least recently used entry (LRU).

<a id="_299"></a>
With LRU, starting from state:<a id="_300"></a>

```
  valid  linear  physical
  -----  ------  --------
> 1      00003   00005
  1      00007   00009
  1      00009   00001
  1      0000B   00003
```
adding `0000D -> 0000A` would give:<a id="_301"></a>

```
  valid  linear  physical
  -----  ------  --------
  1      0000D   0000A
> 1      00007   00009
  1      00009   00001
  1      0000B   00003
```

### CAM

↑ **Parent:** [TLB](#tlb)

<a id="_302"></a>
Using the TLB makes translation faster, because the initial translation takes one access per TLB level, which means 2 on a simple 32 bit scheme, but 3 or 4 on 64 bit architectures.

<a id="_303"></a>
The TLB is usually implemented as an expensive type of RAM called content-addressable memory (CAM). CAM implements an associative map on hardware, that is, a structure that given a key (linear address), retrieves a value.

<a id="_304"></a>
Mappings could also be implemented on RAM addresses, but CAM mappings may required much less entries than a RAM mapping.

<a id="_305"></a>
For example, a map in which:<a id="_306"></a>

<a id="_307"></a>
- both keys and values have 20 bits (the case of a simple paging schemes)
<a id="_308"></a>
- at most 4 values need to be stored at each time
could be stored in a TLB with 4 entries:

<a id="_309"></a>
```
linear  physical
------  --------
00000   00001
00001   00010
00010   00011
FFFFF   00000
```

<a id="_310"></a>
However, to implement this with RAM, it would be necessary to have 2^20 addresses:<a id="_311"></a>

```
linear  physical
------  --------
00000   00001
00001   00010
00010   00011
... (from 00011 to FFFFE)
FFFFF   00000
```
which would be even more expensive than using a TLB.

### Invalidating TLB entries

↑ **Parent:** [TLB](#tlb)

<a id="_312"></a>
When the process changes, `cr3` change to point to the page table of the new current process.

<a id="_313"></a>
This creates a problem: the TLB is now filled with a bunch of cached entries for the old process.

<a id="_314"></a>
A simple and naive solution would be to completely invalidate the TLB whenever the `cr3` changes.

<a id="_315"></a>
However, this is would not be very efficient, because it often happens that we switch back to process 1 before process 2 has completely used up the entire TLB cache entries.

<a id="_316"></a>
The solution for this is to use so called "Address Space Identifiers" (ASID) as mentioned in sources such as:<a id="_317"></a>

<a id="_318"></a>
- [https://stackoverflow.com/questions/52813239/how-many-bits-there-are-in-a-tlb-asid-tag-for-intel-processors-and-how-to-handl](https://stackoverflow.com/questions/52813239/how-many-bits-there-are-in-a-tlb-asid-tag-for-intel-processors-and-how-to-handl)
<a id="_319"></a>
- [https://stackoverflow.com/questions/52713940/purpose-of-address-spaced-identifiersasids](https://stackoverflow.com/questions/52713940/purpose-of-address-spaced-identifiersasids)
<a id="_320"></a>
- [https://www.inf.ed.ac.uk/teaching/courses/os/slides/10-paging16.pdf](https://www.inf.ed.ac.uk/teaching/courses/os/slides/10-paging16.pdf)

<a id="_321"></a>
Basically, the OS assigns a different ASID for each process, and then TLB entries are automatically also tagged with that ASID. This way when the process makes an access, the TLB can determine if a hit is actually for the current process, or if it is an old address coincidence with another process.

<a id="_322"></a>
The x86 also offers the `invlpg` instruction which explicitly invalidates a single TLB entry. Other architectures offer even more instructions to invalidated TLB entries, such as invalidating all entries on a given range.

## Linux kernel usage

↑ **Parent:** [x86 Paging Tutorial](x86-paging.md)

<a id="_323"></a>
The Linux kernel makes extensive usage of the paging features of x86 to allow fast process switches with small data fragmentation.

<a id="_324"></a>
There are also however some features that the Linux kernel might not use, either because they are only for backwards compatibility, or because the Linux devs didn't feel it was worth it yet.

### Play with physical addresses in Linux

↑ **Parent:** [Linux kernel usage](#linux-kernel-usage)

<a id="_325"></a>
Convert virtual addresses to physical from user space with `/proc/<pid>/pagemap` and from kernel space with `virt_to_phys`:<a id="_326"></a>

<a id="_327"></a>
- [https://stackoverflow.com/questions/5748492/is-there-any-api-for-determining-the-physical-address-from-virtual-address-in-li/45128487#45128487](https://stackoverflow.com/questions/5748492/is-there-any-api-for-determining-the-physical-address-from-virtual-address-in-li/45128487#45128487)
<a id="_328"></a>
- [https://github.com/cirosantilli/linux-kernel-module-cheat/blob/1f4f7faebacca75267cc1d63bfeffc30080d017d/kernel_module/user/virt_to_phys_user.c](https://github.com/cirosantilli/linux-kernel-module-cheat/blob/1f4f7faebacca75267cc1d63bfeffc30080d017d/kernel_module/user/virt_to_phys_user.c)
<a id="_329"></a>
- `virt_to_phys`:<a id="_330"></a>

  <a id="_331"></a>
  - [https://github.com/cirosantilli/linux-kernel-module-cheat/blob/0677dbd4b582d1a913462d75caad0abf21e87f32/kernel_module/virt_to_phys.c](https://github.com/cirosantilli/linux-kernel-module-cheat/blob/0677dbd4b582d1a913462d75caad0abf21e87f32/kernel_module/virt_to_phys.c)
  <a id="_332"></a>
  - [https://github.com/cirosantilli/linux-kernel-module-cheat/blob/1f4f7faebacca75267cc1d63bfeffc30080d017d/kernel_module/user/virt_to_phys_user.c](https://github.com/cirosantilli/linux-kernel-module-cheat/blob/1f4f7faebacca75267cc1d63bfeffc30080d017d/kernel_module/user/virt_to_phys_user.c)

<a id="_333"></a>
Dump all page tables from userspace with `/proc/<pid>/maps` and `/proc/<pid>/pagemap`:<a id="_334"></a>

<a id="_335"></a>
- [https://github.com/cirosantilli/linux-kernel-module-cheat/blob/1f4f7faebacca75267cc1d63bfeffc30080d017d/kernel_module/user/virt_to_phys_user.c](https://github.com/cirosantilli/linux-kernel-module-cheat/blob/1f4f7faebacca75267cc1d63bfeffc30080d017d/kernel_module/user/virt_to_phys_user.c)
<a id="_336"></a>
- [https://stackoverflow.com/questions/6284810/proc-pid-pagemaps-and-proc-pid-maps-linux/45500208#45500208](https://stackoverflow.com/questions/6284810/proc-pid-pagemaps-and-proc-pid-maps-linux/45500208#45500208)

<a id="_337"></a>
Read and write physical addresses from userspace with `/dev/mem`:<a id="_338"></a>

<a id="_339"></a>
- [https://stackoverflow.com/questions/12040303/accessing-physical-address-from-user-space/45127890#45127890](https://stackoverflow.com/questions/12040303/accessing-physical-address-from-user-space/45127890#45127890)
<a id="_340"></a>
- [https://free-electrons.com/pub/mirror/devmem2.c](https://free-electrons.com/pub/mirror/devmem2.c)

### Kernel vs process memory layout

↑ **Parent:** [Linux kernel usage](#linux-kernel-usage)

<a id="_341"></a>
The Linux Kernel reserves two zones of virtual memory:<a id="_342"></a>

<a id="_343"></a>
- one for kernel memory
<a id="_344"></a>
- one for programs

<a id="_345"></a>
The exact split is configured by `CONFIG_VMSPLIT_...`. By default:<a id="_346"></a>

<a id="_347"></a>
- on 32-bit:<a id="_348"></a>

  <a id="_349"></a>
  - the bottom 3/4 is program space: `00000000` to `BFFFFFFF`
  <a id="_350"></a>
  - the top 1/4 is kernel memory: `C0000000` to `FFFFFFFF`, like this:<a id="_351"></a>

    ```
    ------------------ FFFFFFFF
    Kernel
    ------------------ C0000000
    ------------------ BFFFFFFF


    Process


    ------------------ 00000000
    ```
<a id="_352"></a>
- on 64-bit: currently only 48-bits are actually used, split into two equally sized disjoint spaces. The Linux kernel just assigns:<a id="_353"></a>

  <a id="_354"></a>
  - the bottom part to processes `00000000 00000000` to `008FFFFF FFFFFFFF`
  <a id="_355"></a>
  - <a id="_356"></a>
    the top part to the kernel: `FFFF8000 00000000` to `FFFFFFFF FFFFFFFF`, like this:

    <a id="_357"></a>
    ```
    ------------------ FFFFFFFF
    Kernel
    ------------------ C0000000


    (not addressable)


    ------------------ BFFFFFFF
    Process
    ------------------ 00000000
    ```

<a id="_358"></a>
Kernel memory [is also paged](https://stackoverflow.com/questions/18953598/is-it-true-that-whole-system-space-address-space-in-linux-does-not-use-demand-pa).

<a id="_359"></a>
In previous versions, [the paging was continuous, but with HIGHMEM this changed](https://stackoverflow.com/questions/1658757/linux-3-1-virtual-address-split).

<a id="_360"></a>
There is no clear physical memory split: [https://stackoverflow.com/questions/30471742/physical-memory-userspace-kernel-split-on-linux-x86-64](https://stackoverflow.com/questions/30471742/physical-memory-userspace-kernel-split-on-linux-x86-64)

### Process memory layout

↑ **Parent:** [Linux kernel usage](#linux-kernel-usage)

<a id="_361"></a>
For each process, the virtual address space looks like this:<a id="_362"></a>

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

<a id="_363"></a>
The kernel maintains a list of pages that belong to each process, and synchronizes that with the paging.

<a id="_364"></a>
If the program accesses memory that does not belong to it, the kernel handles a page-fault, and decides what to do:<a id="_365"></a>

<a id="_366"></a>
- if it is above the maximum stack size, allocate those pages to the process
<a id="_367"></a>
- otherwise, send a SIGSEGV to the process, which usually kills it

<a id="_368"></a>
When an ELF file is loaded by the kernel to start a program with the `exec` system call, the kernel automatically registers text, data, BSS and stack for the program.

<a id="_369"></a>
The `brk` and `mmap` areas can be modified by request of the program through the [`brk`](https://stackoverflow.com/questions/6988487/what-does-brk-system-call-do/31082353#31082353) and `mmap` system calls. But the kernel can also deny the program those areas if there is not enough memory.

<a id="_370"></a>
`brk` and `mmap` can be used to implement `malloc`, or the so called "heap".

<a id="_371"></a>
`mmap` is also used to load dynamically loaded libraries into the program's memory so that it can access and run it.

<a id="_372"></a>
Stack allocation: [https://stackoverflow.com/questions/17671423/stack-allocation-for-process](https://stackoverflow.com/questions/17671423/stack-allocation-for-process)

<a id="_373"></a>
Calculating exact addresses Things are complicated by:<a id="_374"></a>

<a id="_375"></a>
- [Address Space Layout Randomization](https://en.wikipedia.org/wiki/Address_space_layout_randomization).
<a id="_376"></a>
- the fact that environment variables, CLI arguments, and some ELF header data take up initial stack space: [https://unix.stackexchange.com/questions/145557/how-does-stack-allocation-work-in-linux/239323#239323](https://unix.stackexchange.com/questions/145557/how-does-stack-allocation-work-in-linux/239323#239323)

<a id="_377"></a>
Why the text does not start at 0: [https://stackoverflow.com/questions/14795164/why-do-linux-program-text-sections-start-at-0x0804800-and-stack-tops-start-at-0](https://stackoverflow.com/questions/14795164/why-do-linux-program-text-sections-start-at-0x0804800-and-stack-tops-start-at-0)

### Copy-on-write

↑ **Parent:** [Linux kernel usage](#linux-kernel-usage)

<a id="_379"></a>
[https://en.wikipedia.org/wiki/Copy-on-write](https://en.wikipedia.org/wiki/Copy-on-write)

<a id="_380"></a>
Besides a missing page, a very common source of page faults is copy-on-write (COW).

<a id="_381"></a>
Page tables have extra flags that allow the OS to mark a page a read-only.

<a id="_382"></a>
Those page faults only happen when a process tries to write to the page, and not read from it.

<a id="_383"></a>
When Linux forks a process:<a id="_384"></a>

<a id="_385"></a>
- instead of copying all the pages, which is unnecessarily costly, it makes the page tables of the two process point to the same physical address.
<a id="_386"></a>
- it marks those linear addresses as read-only
<a id="_387"></a>
- whenever one of the processes tries to write to a page, the makes a copy of the physical memory, and updates the pages of the two process to point to the two different physical addresses

### Linux source tree

↑ **Parent:** [Linux kernel usage](#linux-kernel-usage)

<a id="_388"></a>
In `v4.2`, look under `arch/x86/`:<a id="_389"></a>

<a id="_390"></a>
- `include/asm/pgtable*`
<a id="_391"></a>
- `include/asm/page*`
<a id="_392"></a>
- `mm/pgtable*`
<a id="_393"></a>
- `mm/page*`

<a id="_394"></a>
There seems to be no structs defined to represent the pages, only macros: `include/asm/page_types.h` is specially interesting. Excerpt:<a id="_395"></a>

```
#define _PAGE_BIT_PRESENT   0   /* is present */
#define _PAGE_BIT_RW        1   /* writeable */
#define _PAGE_BIT_USER      2   /* userspace addressable */
#define _PAGE_BIT_PWT       3   /* page write through */
```

<a id="_396"></a>
`arch/x86/include/uapi/asm/processor-flags.h` defines `CR0`, and in particular the `PG` bit position:<a id="_397"></a>

```
#define X86_CR0_PG_BIT      31 /* Paging */
```

## Memory management unit

↑ **Parent:** [x86 Paging Tutorial](x86-paging.md)

<a id="_398"></a>
Paging is done by the [Memory Management Unit](https://en.wikipedia.org/wiki/Memory_management_unit) (MMU) part of the CPU.

<a id="_399"></a>
Like many others (e.g. [x87 co-processor](https://en.wikipedia.org/wiki/X87), [APIC](https://en.wikipedia.org/wiki/Advanced_Programmable_Interrupt_Controller)), this used to be by separate chip on early days.

<a id="_400"></a>
It was later integrated into the CPU, but the term MMU still used.

## Second Level Address Translation

↑ **Parent:** [x86 Paging Tutorial](x86-paging.md)

<a id="_401"></a>
[https://en.wikipedia.org/wiki/Second_Level_Address_Translation](https://en.wikipedia.org/wiki/Second_Level_Address_Translation)

<a id="_402"></a>
Two level address translation to make OS emulation more efficient.

## Other architectures

↑ **Parent:** [x86 Paging Tutorial](x86-paging.md)

<a id="_403"></a>
[Peter Cordes mentions](https://stackoverflow.com/a/32258855/895245) that some architectures like MIPS leave paging almost completely in the hands of software: a TLB miss runs an OS-supplied function to walk the page tables, and insert the new mapping into the TLB. In such architectures, the OS can use whatever data structure it wants.

### ARM

↑ **Parent:** [Other architectures](#other-architectures)

<a id="_404"></a>
Information about ARM paging can be found at: [https://cirosantilli.com/linux-kernel-module-cheat#arm-paging](https://cirosantilli.com/linux-kernel-module-cheat#arm-paging)

## Bibliography

↑ **Parent:** [x86 Paging Tutorial](x86-paging.md)

<a id="_405"></a>
Free:<a id="_406"></a>

<a id="_407"></a>
- <a id="_408"></a>
  [rutgers-pxk-416](https://www.cs.rutgers.edu/~pxk/416/notes/) chapter "Memory management: lecture notes"

  <a id="_409"></a>
  Good historical review of memory organization techniques used by older OS.

<a id="_410"></a>
Non-free:<a id="_411"></a>

<a id="_412"></a>
- <a id="_413"></a>
  [bovet05](https://www.amazon.com/books/dp/0596005652) chapter "Memory addressing"

  <a id="_414"></a>
  Reasonable intro to x86 memory addressing. Missing some good and simple examples.

## ↑ Ancestors (11)

1. [x86](computer-hardware.md#x86)
2. [List of instruction set architectures](computer-hardware.md#list-of-instruction-set-architectures)
3. [Instruction set architecture](computer-hardware.md#instruction-set-architecture)
4. [Processor (computing)](computer-hardware.md#processor-computing)
5. [Computer hardware component type](computer-hardware.md#computer-hardware-component-type)
6. [Computer hardware](computer-hardware.md)
7. [Computer](computer.md)
8. [Information technology](technology.md#information-technology)
9. [Area of technology](technology.md#area-of-technology)
10. [Technology](technology.md)
11. [Ciro Santilli's Homepage](README.md)

## ← Incoming links (2)

- [The best articles by Ciro Santilli](articles.md)
- [Programming languages](skills.md#programming-languages)
