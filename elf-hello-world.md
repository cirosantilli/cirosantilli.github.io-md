# ELF Hello World Tutorial

↑ **Parent:** [Executable and Linkable Format](systems-programming.md#executable-and-linkable-format)  
🏷️ **Tags:** [The best articles by Ciro Santilli](articles.md)

<a id="_2"></a>
Introductory analysis of a simple example of the [executable and Linkable Format](systems-programming.md#executable-and-linkable-format).

<a id="_3"></a>
Extracted from [this Stack Overflow answer](https://stackoverflow.com/a/30648229/895245).

**Table of contents**

- [Introduction](#introduction)
  - [Standards](#standards)
  - [How to learn](#how-to-learn)
  - [Specified file formats](#specified-file-formats)
  - [Implementations](#implementations)
- [Minimal ELF file](#minimal-elf-file)
- [Generate the example](#generate-the-example)
- [Object hd](#object-hd)
- [Executable hd](#executable-hd)
- [Global file structure](#global-file-structure)
- [Section vs segment](#section-vs-segment)
- [ELF header](#elf-header)
- [Section header table](#section-header-table)
- [Sections](#sections)
  - [Index 0 section](#index-0-section)
    - [`SHT_NULL`](#sht-null)
  - [`.data` section](#data-section)
  - [`.text` section](#text-section)
  - [`SHT_STRTAB`](#sht-strtab)
  - [`.shstrtab`](#shstrtab)
  - [`.symtab`](#symtab)
    - [`STT_FILE`](#stt-file)
    - [`STT_SECTION`](#stt-section)
    - [`STT_NOTYPE`](#stt-notype)
      - [`SHN_ABS`](#shn-abs)
    - [`SHT_SYMTAB` on the executable](#sht-symtab-on-the-executable)
  - [`.strtab`](#strtab)
  - [`.rela.text`](#rela-text)
    - [`.rel.text`](#rel-text)
  - [Dynamic linking sections](#dynamic-linking-sections)
    - [`PT_INTERP`](#pt-interp)
    - [Dynamic section](#dynamic-section)
      - [`DT_FLAGS_1`](#dt-flags-1)
        - [`DF_1_PIE`](#df-1-pie)
- [Program header table](#program-header-table)
- [Backlinks](#backlinks)

## Introduction

↑ **Parent:** [ELF Hello World Tutorial](elf-hello-world.md)

<a id="_4"></a>
ELF is the dominating file format for Linux. It competes with Mach-O for OS X and PE for Windows.

<a id="_5"></a>
ELF supersedes `.coff`, which supersedes `a.out`.

### Standards

↑ **Parent:** [Introduction](#introduction)

<a id="_6"></a>
ELF is specified by the [LSB](https://en.wikipedia.org/wiki/Linux_Standard_Base):<a id="_7"></a>

<a id="_8"></a>
- core generic: [https://refspecs.linuxfoundation.org/LSB_4.1.0/LSB-Core-generic/LSB-Core-generic/elf-generic.html](https://refspecs.linuxfoundation.org/LSB_4.1.0/LSB-Core-generic/LSB-Core-generic/elf-generic.html)
<a id="_9"></a>
- core AMD64: [https://refspecs.linuxfoundation.org/LSB_4.1.0/LSB-Core-AMD64/LSB-Core-AMD64/book1.html](https://refspecs.linuxfoundation.org/LSB_4.1.0/LSB-Core-AMD64/LSB-Core-AMD64/book1.html)

<a id="_10"></a>
The LSB basically links to other standards with minor extensions, in particular:

<a id="_11"></a>
<a id="_12"></a>
- Generic (both by [SCO](https://en.wikipedia.org/wiki/Santa_Cruz_Operation)):<a id="_13"></a>

  <a id="_14"></a>
  - System V ABI 4.1 (1997) [http://www.sco.com/developers/devspecs/gabi41.pdf,](http://www.sco.com/developers/devspecs/gabi41.pdf,) no 64 bit, although a magic number is reserved for it. Same for core files. _This_ is the first document you should look at when searching for information.
  <a id="_15"></a>
  - System V ABI Update DRAFT 17 (2003) [http://www.sco.com/developers/gabi/2003-12-17/contents.html,](http://www.sco.com/developers/gabi/2003-12-17/contents.html,) adds 64 bit. Only updates chapters 4 and 5 of the previous document: the others remain valid and are still referenced.
<a id="_16"></a>
- Architecture specific (by the processor vendor):<a id="_17"></a>

  <a id="_18"></a>
  - IA-32: [https://refspecs.linuxfoundation.org/LSB_4.1.0/LSB-Core-IA32/LSB-Core-IA32/elf-ia32.html,](https://refspecs.linuxfoundation.org/LSB_4.1.0/LSB-Core-IA32/LSB-Core-IA32/elf-ia32.html,) points mostly to [http://www.sco.com/developers/devspecs/abi386-4.pdf](http://www.sco.com/developers/devspecs/abi386-4.pdf)
  <a id="_19"></a>
  - AMD64: [https://refspecs.linuxfoundation.org/LSB_4.1.0/LSB-Core-AMD64/LSB-Core-AMD64/elf-amd64.html,](https://refspecs.linuxfoundation.org/LSB_4.1.0/LSB-Core-AMD64/LSB-Core-AMD64/elf-amd64.html,) points mostly to [http://www.x86-64.org/documentation/abi.pdf](http://www.x86-64.org/documentation/abi.pdf)

<a id="_20"></a>
A handy summary can be found at:<a id="_21"></a>

```
man elf
```

### How to learn

↑ **Parent:** [Introduction](#introduction)

<a id="_22"></a>
Spin like mad between:<a id="_23"></a>

<a id="_24"></a>
- standards
<a id="_25"></a>
- high level generators. We use the [assembler](computer-hardware.md#assembler-computing) `as` and [linker](software.md#linker-computing) `ld`.
<a id="_26"></a>
- hexdumps
<a id="_27"></a>
- file decompilers. We use `readelf`. It makes it faster to read the ELF file by turning it into human readable output. But you must have seen one byte-by-byte example first, and think how `readelf` output maps to the standard.
<a id="_28"></a>
- low-level generators: stand-alone libraries that let you control every field of the ELF files you generated. [https://github.com/BR903/ELFkickers,](https://github.com/BR903/ELFkickers,) [https://github.com/sqall01/ZwoELF](https://github.com/sqall01/ZwoELF) and many more on GitHub.
<a id="_29"></a>
- consumer: the `exec` system call of the Linux kernel can parse ELF files to starts processes: [https://github.com/torvalds/linux/blob/v4.11/fs/binfmt_elf.c,](https://github.com/torvalds/linux/blob/v4.11/fs/binfmt_elf.c,) [https://stackoverflow.com/questions/8352535/how-does-kernel-get-an-executable-binary-file-running-under-linux/31394861#31394861](https://stackoverflow.com/questions/8352535/how-does-kernel-get-an-executable-binary-file-running-under-linux/31394861#31394861)

### Specified file formats

↑ **Parent:** [Introduction](#introduction)

<a id="_30"></a>
The ELF standard specifies multiple file formats:<a id="_31"></a>

<a id="_32"></a>
- <a id="_33"></a>
  Object files (`.o`).

  <a id="_34"></a>
  Intermediate step to generating executables and other formats:<a id="_35"></a>

  ```
  Source code

      |
      | Compilation
      |
      v

  Object file

      |
      | Linking
      |
      v

  Executable
  ```

  <a id="_36"></a>
  Object files exist to make compilation faster: with `make`, we only have to recompile the modified source files based on timestamps.

  <a id="_37"></a>
  We have to do the linking step every time, but it is much less expensive.

<a id="_38"></a>
<a id="_39"></a>
- <a id="_40"></a>
  Executable files (no standard Linux extension).

  <a id="_41"></a>
  This is what the Linux kernel can actually run.

<a id="_42"></a>
<a id="_43"></a>
- <a id="_44"></a>
  Archive files (`.a`).

  <a id="_45"></a>
  Libraries meant to be embedded into executables during the Linking step.

<a id="_46"></a>
<a id="_47"></a>
- <a id="_48"></a>
  Shared object files (`.so`).

  <a id="_49"></a>
  Libraries meant to be loaded when the executable starts running.

<a id="_50"></a>
<a id="_51"></a>
- <a id="_52"></a>
  Core dumps.

  <a id="_53"></a>
  Such files may be generated by the Linux kernel when the program does naughty things, e.g. segfault.

  <a id="_54"></a>
  They exist to help debugging the program.

<a id="_55"></a>
In this tutorial, we consider only object and executable files.

### Implementations

↑ **Parent:** [Introduction](#introduction)

<a id="_56"></a>
<a id="_57"></a>
- <a id="_58"></a>
  Compiler toolchains generate and read ELF files.

  <a id="_59"></a>
  Sane compilers should use a separate standalone library to do the dirty work. E.g., Binutils uses BFD (in-tree and canonical source).

<a id="_60"></a>
<a id="_61"></a>
- <a id="_62"></a>
  Operating systems read and run ELF files.

  <a id="_63"></a>
  Kernels cannot link to a library nor use the C stlib, so they are more likely to implement it themselves.

  <a id="_64"></a>
  This is the case of the Linux kernel 4.2 which implements it in th file `fs/binfmt_elf.c`.

<a id="_65"></a>
<a id="_66"></a>
- Specialized libraries. Examples:<a id="_67"></a>

  <a id="_68"></a>
  - [https://github.com/eliben/pyelftools.](https://github.com/eliben/pyelftools.) By a hardcore Googler: [https://plus.google.com/+EliBenderskyGplus/posts](https://plus.google.com/+EliBenderskyGplus/posts)
  <a id="_69"></a>
  - [https://sourceforge.net/projects/elftoolchain](https://sourceforge.net/projects/elftoolchain)

## Minimal ELF file

↑ **Parent:** [ELF Hello World Tutorial](elf-hello-world.md)

<a id="_70"></a>
It is non-trivial to determine what is the smallest legal ELF file, or the smaller one that will do something trivial in Linux.

<a id="_71"></a>
Some impressive attempts:<a id="_72"></a>

<a id="_73"></a>
- [https://codegolf.stackexchange.com/questions/5696/shortest-elf-for-hello-world-n](https://codegolf.stackexchange.com/questions/5696/shortest-elf-for-hello-world-n)
<a id="_74"></a>
- [https://www.muppetlabs.com/~breadbox/software/tiny/](https://www.muppetlabs.com/~breadbox/software/tiny/)
<a id="_75"></a>
- [http://timelessname.com/elfbin/](http://timelessname.com/elfbin/)

<a id="_76"></a>
In this example we will consider a saner `hello world` example that will better capture real life cases.

## Generate the example

↑ **Parent:** [ELF Hello World Tutorial](elf-hello-world.md)

<a id="_77"></a>
Let's break down a minimal runnable Linux x86-64 example:

<a id="_78"></a>
hello\_world.asm

<a id="_79"></a>
```
section .data
    hello_world db "Hello world!", 10
    hello_world_len  equ $ - hello_world
section .text
    global _start
    _start:
        mov rax, 1
        mov rdi, 1
        mov rsi, hello_world
        mov rdx, hello_world_len
        syscall
        mov rax, 60
        mov rdi, 0
        syscall
```

<a id="_80"></a>
Compiled with:<a id="_81"></a>

```
nasm -w+all -f elf64 -o 'hello_world.o' 'hello_world.asm'
ld -o 'hello_world.out' 'hello_world.o'
```

<a id="_82"></a>
TODO: use a minimal linker script with `-T` to be more precise and minimal.

<a id="_83"></a>
Versions:<a id="_84"></a>

<a id="_85"></a>
- NASM 2.10.09
<a id="_86"></a>
- Binutils version 2.24 (contains `ld`)
<a id="_87"></a>
- Ubuntu 14.04

<a id="_88"></a>
We don't use a C program as that would complicate the analysis, that will be level 2 :-)

## Object hd

↑ **Parent:** [ELF Hello World Tutorial](elf-hello-world.md)

<a id="_89"></a>
Running:<a id="_90"></a>

```
hd hello_world.o
```
gives:<a id="_91"></a>

```
00000000  7f 45 4c 46 02 01 01 00  00 00 00 00 00 00 00 00  |.ELF............|
00000010  01 00 3e 00 01 00 00 00  00 00 00 00 00 00 00 00  |..>.............|
00000020  00 00 00 00 00 00 00 00  40 00 00 00 00 00 00 00  |........@.......|
00000030  00 00 00 00 40 00 00 00  00 00 40 00 07 00 03 00  |....@.....@.....|
00000040  00 00 00 00 00 00 00 00  00 00 00 00 00 00 00 00  |................|
*
00000080  01 00 00 00 01 00 00 00  03 00 00 00 00 00 00 00  |................|
00000090  00 00 00 00 00 00 00 00  00 02 00 00 00 00 00 00  |................|
000000a0  0d 00 00 00 00 00 00 00  00 00 00 00 00 00 00 00  |................|
000000b0  04 00 00 00 00 00 00 00  00 00 00 00 00 00 00 00  |................|
000000c0  07 00 00 00 01 00 00 00  06 00 00 00 00 00 00 00  |................|
000000d0  00 00 00 00 00 00 00 00  10 02 00 00 00 00 00 00  |................|
000000e0  27 00 00 00 00 00 00 00  00 00 00 00 00 00 00 00  |'...............|
000000f0  10 00 00 00 00 00 00 00  00 00 00 00 00 00 00 00  |................|
00000100  0d 00 00 00 03 00 00 00  00 00 00 00 00 00 00 00  |................|
00000110  00 00 00 00 00 00 00 00  40 02 00 00 00 00 00 00  |........@.......|
00000120  32 00 00 00 00 00 00 00  00 00 00 00 00 00 00 00  |2...............|
00000130  01 00 00 00 00 00 00 00  00 00 00 00 00 00 00 00  |................|
00000140  17 00 00 00 02 00 00 00  00 00 00 00 00 00 00 00  |................|
00000150  00 00 00 00 00 00 00 00  80 02 00 00 00 00 00 00  |................|
00000160  a8 00 00 00 00 00 00 00  05 00 00 00 06 00 00 00  |................|
00000170  04 00 00 00 00 00 00 00  18 00 00 00 00 00 00 00  |................|
00000180  1f 00 00 00 03 00 00 00  00 00 00 00 00 00 00 00  |................|
00000190  00 00 00 00 00 00 00 00  30 03 00 00 00 00 00 00  |........0.......|
000001a0  34 00 00 00 00 00 00 00  00 00 00 00 00 00 00 00  |4...............|
000001b0  01 00 00 00 00 00 00 00  00 00 00 00 00 00 00 00  |................|
000001c0  27 00 00 00 04 00 00 00  00 00 00 00 00 00 00 00  |'...............|
000001d0  00 00 00 00 00 00 00 00  70 03 00 00 00 00 00 00  |........p.......|
000001e0  18 00 00 00 00 00 00 00  04 00 00 00 02 00 00 00  |................|
000001f0  04 00 00 00 00 00 00 00  18 00 00 00 00 00 00 00  |................|
00000200  48 65 6c 6c 6f 20 77 6f  72 6c 64 21 0a 00 00 00  |Hello world!....|
00000210  b8 01 00 00 00 bf 01 00  00 00 48 be 00 00 00 00  |..........H.....|
00000220  00 00 00 00 ba 0d 00 00  00 0f 05 b8 3c 00 00 00  |............<...|
00000230  bf 00 00 00 00 0f 05 00  00 00 00 00 00 00 00 00  |................|
00000240  00 2e 64 61 74 61 00 2e  74 65 78 74 00 2e 73 68  |..data..text..sh|
00000250  73 74 72 74 61 62 00 2e  73 79 6d 74 61 62 00 2e  |strtab..symtab..|
00000260  73 74 72 74 61 62 00 2e  72 65 6c 61 2e 74 65 78  |strtab..rela.tex|
00000270  74 00 00 00 00 00 00 00  00 00 00 00 00 00 00 00  |t...............|
00000280  00 00 00 00 00 00 00 00  00 00 00 00 00 00 00 00  |................|
00000290  00 00 00 00 00 00 00 00  01 00 00 00 04 00 f1 ff  |................|
000002a0  00 00 00 00 00 00 00 00  00 00 00 00 00 00 00 00  |................|
000002b0  00 00 00 00 03 00 01 00  00 00 00 00 00 00 00 00  |................|
000002c0  00 00 00 00 00 00 00 00  00 00 00 00 03 00 02 00  |................|
000002d0  00 00 00 00 00 00 00 00  00 00 00 00 00 00 00 00  |................|
000002e0  11 00 00 00 00 00 01 00  00 00 00 00 00 00 00 00  |................|
000002f0  00 00 00 00 00 00 00 00  1d 00 00 00 00 00 f1 ff  |................|
00000300  0d 00 00 00 00 00 00 00  00 00 00 00 00 00 00 00  |................|
00000310  2d 00 00 00 10 00 02 00  00 00 00 00 00 00 00 00  |-...............|
00000320  00 00 00 00 00 00 00 00  00 00 00 00 00 00 00 00  |................|
00000330  00 68 65 6c 6c 6f 5f 77  6f 72 6c 64 2e 61 73 6d  |.hello_world.asm|
00000340  00 68 65 6c 6c 6f 5f 77  6f 72 6c 64 00 68 65 6c  |.hello_world.hel|
00000350  6c 6f 5f 77 6f 72 6c 64  5f 6c 65 6e 00 5f 73 74  |lo_world_len._st|
00000360  61 72 74 00 00 00 00 00  00 00 00 00 00 00 00 00  |art.............|
00000370  0c 00 00 00 00 00 00 00  01 00 00 00 02 00 00 00  |................|
00000380  00 00 00 00 00 00 00 00  00 00 00 00 00 00 00 00  |................|
00000390
```

## Executable hd

↑ **Parent:** [ELF Hello World Tutorial](elf-hello-world.md)

<a id="_92"></a>
Running:<a id="_93"></a>

```
hd hello_world.out
```
gives:<a id="_94"></a>

```
00000000  7f 45 4c 46 02 01 01 00  00 00 00 00 00 00 00 00  |.ELF............|
00000010  02 00 3e 00 01 00 00 00  b0 00 40 00 00 00 00 00  |..>.......@.....|
00000020  40 00 00 00 00 00 00 00  10 01 00 00 00 00 00 00  |@...............|
00000030  00 00 00 00 40 00 38 00  02 00 40 00 06 00 03 00  |....@.8...@.....|
00000040  01 00 00 00 05 00 00 00  00 00 00 00 00 00 00 00  |................|
00000050  00 00 40 00 00 00 00 00  00 00 40 00 00 00 00 00  |..@.......@.....|
00000060  d7 00 00 00 00 00 00 00  d7 00 00 00 00 00 00 00  |................|
00000070  00 00 20 00 00 00 00 00  01 00 00 00 06 00 00 00  |.. .............|
00000080  d8 00 00 00 00 00 00 00  d8 00 60 00 00 00 00 00  |..........`.....|
00000090  d8 00 60 00 00 00 00 00  0d 00 00 00 00 00 00 00  |..`.............|
000000a0  0d 00 00 00 00 00 00 00  00 00 20 00 00 00 00 00  |.......... .....|
000000b0  b8 01 00 00 00 bf 01 00  00 00 48 be d8 00 60 00  |..........H...`.|
000000c0  00 00 00 00 ba 0d 00 00  00 0f 05 b8 3c 00 00 00  |............<...|
000000d0  bf 00 00 00 00 0f 05 00  48 65 6c 6c 6f 20 77 6f  |........Hello wo|
000000e0  72 6c 64 21 0a 00 2e 73  79 6d 74 61 62 00 2e 73  |rld!...symtab..s|
000000f0  74 72 74 61 62 00 2e 73  68 73 74 72 74 61 62 00  |trtab..shstrtab.|
00000100  2e 74 65 78 74 00 2e 64  61 74 61 00 00 00 00 00  |.text..data.....|
00000110  00 00 00 00 00 00 00 00  00 00 00 00 00 00 00 00  |................|
*
00000150  1b 00 00 00 01 00 00 00  06 00 00 00 00 00 00 00  |................|
00000160  b0 00 40 00 00 00 00 00  b0 00 00 00 00 00 00 00  |..@.............|
00000170  27 00 00 00 00 00 00 00  00 00 00 00 00 00 00 00  |'...............|
00000180  10 00 00 00 00 00 00 00  00 00 00 00 00 00 00 00  |................|
00000190  21 00 00 00 01 00 00 00  03 00 00 00 00 00 00 00  |!...............|
000001a0  d8 00 60 00 00 00 00 00  d8 00 00 00 00 00 00 00  |..`.............|
000001b0  0d 00 00 00 00 00 00 00  00 00 00 00 00 00 00 00  |................|
000001c0  04 00 00 00 00 00 00 00  00 00 00 00 00 00 00 00  |................|
000001d0  11 00 00 00 03 00 00 00  00 00 00 00 00 00 00 00  |................|
000001e0  00 00 00 00 00 00 00 00  e5 00 00 00 00 00 00 00  |................|
000001f0  27 00 00 00 00 00 00 00  00 00 00 00 00 00 00 00  |'...............|
00000200  01 00 00 00 00 00 00 00  00 00 00 00 00 00 00 00  |................|
00000210  01 00 00 00 02 00 00 00  00 00 00 00 00 00 00 00  |................|
00000220  00 00 00 00 00 00 00 00  90 02 00 00 00 00 00 00  |................|
00000230  08 01 00 00 00 00 00 00  05 00 00 00 07 00 00 00  |................|
00000240  08 00 00 00 00 00 00 00  18 00 00 00 00 00 00 00  |................|
00000250  09 00 00 00 03 00 00 00  00 00 00 00 00 00 00 00  |................|
00000260  00 00 00 00 00 00 00 00  98 03 00 00 00 00 00 00  |................|
00000270  4c 00 00 00 00 00 00 00  00 00 00 00 00 00 00 00  |L...............|
00000280  01 00 00 00 00 00 00 00  00 00 00 00 00 00 00 00  |................|
00000290  00 00 00 00 00 00 00 00  00 00 00 00 00 00 00 00  |................|
000002a0  00 00 00 00 00 00 00 00  00 00 00 00 03 00 01 00  |................|
000002b0  b0 00 40 00 00 00 00 00  00 00 00 00 00 00 00 00  |..@.............|
000002c0  00 00 00 00 03 00 02 00  d8 00 60 00 00 00 00 00  |..........`.....|
000002d0  00 00 00 00 00 00 00 00  01 00 00 00 04 00 f1 ff  |................|
000002e0  00 00 00 00 00 00 00 00  00 00 00 00 00 00 00 00  |................|
000002f0  11 00 00 00 00 00 02 00  d8 00 60 00 00 00 00 00  |..........`.....|
00000300  00 00 00 00 00 00 00 00  1d 00 00 00 00 00 f1 ff  |................|
00000310  0d 00 00 00 00 00 00 00  00 00 00 00 00 00 00 00  |................|
00000320  00 00 00 00 04 00 f1 ff  00 00 00 00 00 00 00 00  |................|
00000330  00 00 00 00 00 00 00 00  2d 00 00 00 10 00 01 00  |........-.......|
00000340  b0 00 40 00 00 00 00 00  00 00 00 00 00 00 00 00  |..@.............|
00000350  34 00 00 00 10 00 02 00  e5 00 60 00 00 00 00 00  |4.........`.....|
00000360  00 00 00 00 00 00 00 00  40 00 00 00 10 00 02 00  |........@.......|
00000370  e5 00 60 00 00 00 00 00  00 00 00 00 00 00 00 00  |..`.............|
00000380  47 00 00 00 10 00 02 00  e8 00 60 00 00 00 00 00  |G.........`.....|
00000390  00 00 00 00 00 00 00 00  00 68 65 6c 6c 6f 5f 77  |.........hello_w|
000003a0  6f 72 6c 64 2e 61 73 6d  00 68 65 6c 6c 6f 5f 77  |orld.asm.hello_w|
000003b0  6f 72 6c 64 00 68 65 6c  6c 6f 5f 77 6f 72 6c 64  |orld.hello_world|
000003c0  5f 6c 65 6e 00 5f 73 74  61 72 74 00 5f 5f 62 73  |_len._start.__bs|
000003d0  73 5f 73 74 61 72 74 00  5f 65 64 61 74 61 00 5f  |s_start._edata._|
000003e0  65 6e 64 00                                       |end.|
000003e4
```

## Global file structure

↑ **Parent:** [ELF Hello World Tutorial](elf-hello-world.md)

<a id="_95"></a>
An ELF file contains the following parts:<a id="_96"></a>

<a id="_97"></a>
- ELF header. Points to the position of the section header table and the program header table.
<a id="_98"></a>
- Section header table (optional on executable). Each has `e_shnum` section headers, each pointing to the position of a section.
<a id="_99"></a>
- N sections, with `N <= e_shnum` (optional on executable)
<a id="_100"></a>
- Program header table (only on executable). Each has `e_phnum` program headers, each pointing to the position of a segment.
<a id="_101"></a>
- N segments, with `N <= e_phnum` (only on executable)

<a id="_102"></a>
The order of those parts is _not_ fixed: the only fixed thing is the ELF header that must be the first thing on the file: Generic docs say:<a id="_103"></a>


> Although the figure shows the program header table immediately after the ELF header, and the section header table following the sections, actual files may differ. Moreover, sections and segments have no specified order. Only the ELF header has a fixed position in the file.

<a id="_104"></a>
In pictures: sample object file with three sections:<a id="_105"></a>

```
            +-------------------+
            | ELF header        |---+
+---------> +-------------------+   | e_shoff
|           |                   |<--+
| Section   | Section header 0  |
|           |                   |---+ sh_offset
| Header    +-------------------+   |
|           | Section header 1  |---|--+ sh_offset
| Table     +-------------------+   |  |
|           | Section header 2  |---|--|--+
+---------> +-------------------+   |  |  |
            | Section 0         |<--+  |  |
            +-------------------+      |  | sh_offset
            | Section 1         |<-----+  |
            +-------------------+         |
            | Section 2         |<--------+
            +-------------------+
```

<a id="_106"></a>
But nothing (except sanity) prevents the following topology:<a id="_107"></a>

```
            +-------------------+
            | ELF header        |---+ e_shoff
            +-------------------+   |
            | Section 1         |<--|--+
+---------> +-------------------+   |  |
|           |                   |<--+  | sh_offset
| Section   | Section header 0  |      |
|           |                   |------|---------+
| Header    +-------------------+      |         |
|           | Section header 1  |------+         |
| Table     +-------------------+                |
|           | Section header 2  |---+            | sh_offset
+---------> +-------------------+   | sh_offset  |
            | Section 2         |<--+            |
            +-------------------+                |
            | Section 0         |<---------------+
            +-------------------+
```

<a id="_108"></a>
But some newbies may prefer PNGs :-)

<a id="image-elf-executable-and-linkable-format-diagram-by-ange-albertini"></a>
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/e/e4/ELF_Executable_and_Linkable_Format_diagram_by_Ange_Albertini.png/1280px-ELF_Executable_and_Linkable_Format_diagram_by_Ange_Albertini.png" alt="" height="900">

**[Figure 1](#image-elf-executable-and-linkable-format-diagram-by-ange-albertini). ELF Executable and Linkable Format diagram by Ange Albertini**. [Source](https://github.com/corkami/pics/blob/28cb0226093ed57b348723bc473cea0162dad366/binary/elf101/elf101.pdf).

## Section vs segment

↑ **Parent:** [ELF Hello World Tutorial](elf-hello-world.md)

<a id="_109"></a>
We will get into more detail later, but it is good to have it in mind now:

<a id="_110"></a>
<a id="_111"></a>
- <a id="_112"></a>
  section: exists before linking, in object files.

  <a id="_113"></a>
  One ore more sections will be put inside a single segment by the linker.

  <a id="_114"></a>
  Major information sections contain for the linker: is this section:<a id="_115"></a>

  <a id="_116"></a>
  - raw data to be loaded into memory, e.g. `.data`, `.text`, etc.
  <a id="_117"></a>
  - or metadata about other sections, that will be used by the linker, but disappear at runtime e.g. `.symtab`, `.srttab`, `.rela.text`
<a id="_118"></a>
- <a id="_119"></a>
  segment: exists after linking, in the executable file.

  <a id="_120"></a>
  Contains information about how each segment should be loaded into memory by the OS, notably location and permissions.

<a id="_121"></a>
See also:<a id="_122"></a>

<a id="_123"></a>
- [https://stackoverflow.com/questions/14361248/whats-the-difference-of-section-and-segment-in-elf-file-format](https://stackoverflow.com/questions/14361248/whats-the-difference-of-section-and-segment-in-elf-file-format)
<a id="_124"></a>
- [https://stackoverflow.com/questions/23379880/difference-between-program-header-and-section-header-in-elf](https://stackoverflow.com/questions/23379880/difference-between-program-header-and-section-header-in-elf)

## ELF header

↑ **Parent:** [ELF Hello World Tutorial](elf-hello-world.md)

<a id="_125"></a>
Running:<a id="_126"></a>

```
readelf -h hello_world.o
```
outputs:<a id="_127"></a>

```
Magic:   7f 45 4c 46 02 01 01 00 00 00 00 00 00 00 00 00
Class:                             ELF64
Data:                              2's complement, little endian
Version:                           1 (current)
OS/ABI:                            UNIX - System V
ABI Version:                       0
Type:                              REL (Relocatable file)
Machine:                           Advanced Micro Devices X86-64
Version:                           0x1
Entry point address:               0x0
Start of program headers:          0 (bytes into file)
Start of section headers:          64 (bytes into file)
Flags:                             0x0
Size of this header:               64 (bytes)
Size of program headers:           0 (bytes)
Number of program headers:         0
Size of section headers:           64 (bytes)
Number of section headers:         7
Section header string table index: 3
```

<a id="_128"></a>
Running:<a id="_129"></a>

```
readelf -h hello_world.out
```
outputs:<a id="_130"></a>

```
Magic:   7f 45 4c 46 02 01 01 00 00 00 00 00 00 00 00 00
Class:                             ELF64
Data:                              2's complement, little endian
Version:                           1 (current)
OS/ABI:                            UNIX - System V
ABI Version:                       0
Type:                              EXEC (Executable file)
Machine:                           Advanced Micro Devices X86-64
Version:                           0x1
Entry point address:               0x4000b0
Start of program headers:          64 (bytes into file)
Start of section headers:          272 (bytes into file)
Flags:                             0x0
Size of this header:               64 (bytes)
Size of program headers:           56 (bytes)
Number of program headers:         2
Size of section headers:           64 (bytes)
Number of section headers:         6
Section header string table index: 3
```

<a id="_131"></a>
Bytes in the object file:<a id="_132"></a>

```
00000000  7f 45 4c 46 02 01 01 00  00 00 00 00 00 00 00 00  |.ELF............|
00000010  01 00 3e 00 01 00 00 00  00 00 00 00 00 00 00 00  |..>.............|
00000020  00 00 00 00 00 00 00 00  40 00 00 00 00 00 00 00  |........@.......|
00000030  00 00 00 00 40 00 00 00  00 00 40 00 07 00 03 00  |....@.....@.....|
```

<a id="_133"></a>
Executable:<a id="_134"></a>

```
00000000  7f 45 4c 46 02 01 01 00  00 00 00 00 00 00 00 00  |.ELF............|
00000010  02 00 3e 00 01 00 00 00  b0 00 40 00 00 00 00 00  |..>.......@.....|
00000020  40 00 00 00 00 00 00 00  10 01 00 00 00 00 00 00  |@...............|
00000030  00 00 00 00 40 00 38 00  02 00 40 00 06 00 03 00  |....@.8...@.....|
```

<a id="_135"></a>
Structure represented:<a id="_136"></a>

```
# define EI_NIDENT 16

typedef struct {
    unsigned char   e_ident[EI_NIDENT];
    Elf64_Half      e_type;
    Elf64_Half      e_machine;
    Elf64_Word      e_version;
    Elf64_Addr      e_entry;
    Elf64_Off       e_phoff;
    Elf64_Off       e_shoff;
    Elf64_Word      e_flags;
    Elf64_Half      e_ehsize;
    Elf64_Half      e_phentsize;
    Elf64_Half      e_phnum;
    Elf64_Half      e_shentsize;
    Elf64_Half      e_shnum;
    Elf64_Half      e_shstrndx;
} Elf64_Ehdr;
```

<a id="_137"></a>
Manual breakdown:

<a id="_138"></a>
<a id="_139"></a>
- 0 0: `EI_MAG` = `7f 45 4c 46` = `0x7f 'E', 'L', 'F'`: ELF magic number
<a id="_140"></a>
- 0 4: `EI_CLASS` = `02` = `ELFCLASS64`: 64 bit elf
<a id="_141"></a>
- 0 5: `EI_DATA` = `01` = `ELFDATA2LSB`: little endian data
<a id="_142"></a>
- 0 6: `EI_VERSION` = `01`: format version
<a id="_143"></a>
- 0 7: `EI_OSABI` (only in 2003 Update) = `00` = `ELFOSABI_NONE`: no extensions.
<a id="_144"></a>
- 0 8: `EI_PAD` = 8x `00`: reserved bytes. Must be set to 0.
<a id="_145"></a>
- <a id="_146"></a>
  1 0: `e_type` = `01 00` = 1 (big endian) = `ET_REl`: relocatable format

  <a id="_147"></a>
  On the executable it is `02 00` for `ET_EXEC`.

  <a id="_148"></a>
  Another important possibility for the executable is `ET_DYN` for PIE executables and shared libraries.

  <a id="_149"></a>
  `ET_DYN` tells the Linux kernel that the code is position independent, and can loaded at a random memory location with ASLR.

  <a id="_150"></a>
  This is explained further at:<a id="_151"></a>

  <a id="_152"></a>
  - [https://stackoverflow.com/questions/2463150/what-is-the-fpie-option-for-position-independent-executables-in-gcc-and-ld/51308031#51308031](https://stackoverflow.com/questions/2463150/what-is-the-fpie-option-for-position-independent-executables-in-gcc-and-ld/51308031#51308031)
  <a id="_153"></a>
  - [https://stackoverflow.com/questions/34519521/why-does-gcc-create-a-shared-object-instead-of-an-executable-binary-according-to/55704865#55704865](https://stackoverflow.com/questions/34519521/why-does-gcc-create-a-shared-object-instead-of-an-executable-binary-according-to/55704865#55704865)
<a id="_154"></a>
- 1 2: `e_machine` = `3e 00` = `62` = `EM_X86_64`: AMD64 architecture
<a id="_155"></a>
- 1 4: `e_version` = `01 00 00 00`: must be 1
<a id="_156"></a>
- <a id="_157"></a>
  1 8: `e_entry` = 8x `00`: execution address entry point, or 0 if not applicable like for the object file since there is no entry point.

  <a id="_158"></a>
  On the executable, it is `b0 00 40 00 00 00 00 00`. The kernel puts the RIP directly on that value when executing. It can be configured by the linker script or `-e`. But it will segfault if you set it too low: [https://stackoverflow.com/questions/2187484/why-is-the-elf-execution-entry-point-virtual-address-of-the-form-0x80xxxxx-and-n](https://stackoverflow.com/questions/2187484/why-is-the-elf-execution-entry-point-virtual-address-of-the-form-0x80xxxxx-and-n)
<a id="_159"></a>
- <a id="_160"></a>
  2 0: `e_phoff` = 8x `00`: program header table offset, 0 if not present.

  <a id="_161"></a>
  `40 00 00 00` on the executable, i.e. it starts immediately after the ELF header.
<a id="_162"></a>
- 2 8: `e_shoff` = `40` 7x `00` = `0x40`: section header table file offset, 0 if not present.
<a id="_163"></a>
- <a id="_164"></a>
  3 0: `e_flags` = `00 00 00 00` Arch specific. `i386` docs say:

  <a id="_165"></a>
  > The Intel386 architecture defines no flags; so this member contains zero.
<a id="_166"></a>
- 3 4: `e_ehsize` = `40 00`: size of this elf header. TODO why this field needed? Isn't the size fixed?
<a id="_167"></a>
- <a id="_168"></a>
  3 6: `e_phentsize` = `00 00`: size of each program header, 0 if not present.

  <a id="_169"></a>
  `38 00` on executable: it is 56 bytes long
<a id="_170"></a>
- <a id="_171"></a>
  3 8: `e_phnum` = `00 00`: number of program header entries, 0 if not present.

  <a id="_172"></a>
  `02 00` on executable: there are 2 entries.
<a id="_173"></a>
- 3 A: `e_shentsize` and `e_shnum` = `40 00 07 00`: section header size and number of entries
<a id="_174"></a>
- 3 E: `e_shstrndx` (`Section Header STRing iNDeX`) = `03 00`: index of the `.shstrtab` section.

## Section header table

↑ **Parent:** [ELF Hello World Tutorial](elf-hello-world.md)

<a id="_175"></a>
Array of `Elf64_Shdr` structs.

<a id="_176"></a>
Each entry contains metadata about a given section.

<a id="_177"></a>
`e_shoff` of the ELF header gives the starting position, 0x40 here.

<a id="_178"></a>
`e_shentsize` and `e_shnum` from the ELF header say that we have 7 entries, each `0x40` bytes long.

<a id="_179"></a>
So the table takes bytes from 0x40 to `0x40 + 7 + 0x40 - 1` = 0x1FF.

<a id="_180"></a>
Some section names are reserved for certain section types: [http://www.sco.com/developers/gabi/2003-12-17/ch4.sheader.html#special_sections](http://www.sco.com/developers/gabi/2003-12-17/ch4.sheader.html#special_sections) e.g. `.text` requires a `SHT_PROGBITS` type and `SHF_ALLOC` + `SHF_EXECINSTR`

<a id="_181"></a>
Running:<a id="_182"></a>

```
readelf -S hello_world.o
```
outputs:<a id="_183"></a>

```
There are 7 section headers, starting at offset 0x40:

Section Headers:
  [Nr] Name              Type             Address           Offset
       Size              EntSize          Flags  Link  Info  Align
  [ 0]                   NULL             0000000000000000  00000000
       0000000000000000  0000000000000000           0     0     0
  [ 1] .data             PROGBITS         0000000000000000  00000200
       000000000000000d  0000000000000000  WA       0     0     4
  [ 2] .text             PROGBITS         0000000000000000  00000210
       0000000000000027  0000000000000000  AX       0     0     16
  [ 3] .shstrtab         STRTAB           0000000000000000  00000240
       0000000000000032  0000000000000000           0     0     1
  [ 4] .symtab           SYMTAB           0000000000000000  00000280
       00000000000000a8  0000000000000018           5     6     4
  [ 5] .strtab           STRTAB           0000000000000000  00000330
       0000000000000034  0000000000000000           0     0     1
  [ 6] .rela.text        RELA             0000000000000000  00000370
       0000000000000018  0000000000000018           4     2     4
Key to Flags:
  W (write), A (alloc), X (execute), M (merge), S (strings), l (large)
  I (info), L (link order), G (group), T (TLS), E (exclude), x (unknown)
  O (extra OS processing required) o (OS specific), p (processor specific)
```

<a id="_184"></a>
The `struct` represented by each entry is:<a id="_185"></a>

```
typedef struct {
    Elf64_Word  sh_name;
    Elf64_Word  sh_type;
    Elf64_Xword sh_flags;
    Elf64_Addr  sh_addr;
    Elf64_Off   sh_offset;
    Elf64_Xword sh_size;
    Elf64_Word  sh_link;
    Elf64_Word  sh_info;
    Elf64_Xword sh_addralign;
    Elf64_Xword sh_entsize;
} Elf64_Shdr;
```

## Sections

↑ **Parent:** [ELF Hello World Tutorial](elf-hello-world.md)

### Index 0 section

↑ **Parent:** [Sections](#sections)

<a id="_186"></a>
Contained in bytes 0x40 to 0x7F.

<a id="_187"></a>
The first section is always magic: [http://www.sco.com/developers/gabi/2003-12-17/ch4.sheader.html](http://www.sco.com/developers/gabi/2003-12-17/ch4.sheader.html) says:

<a id="_188"></a>
> If the number of sections is greater than or equal to SHN\_LORESERVE (0xff00), e\_shnum has the value SHN\_UNDEF (0) and the actual number of section header table entries is contained in the sh\_size field of the section header at index 0 (otherwise, the sh\_size member of the initial entry contains 0).

<a id="_189"></a>
There are also other magic sections detailed in `Figure 4-7: Special Section Indexes`.

<h4 id="sht-null"><code>SHT_NULL</code></h4>

↑ **Parent:** [Index 0 section](#index-0-section)

<a id="_190"></a>
In index 0, `SHT_NULL` is mandatory. Are there any other uses for it: [https://stackoverflow.com/questions/26812142/what-is-the-use-of-the-sht-null-section-in-elf](https://stackoverflow.com/questions/26812142/what-is-the-use-of-the-sht-null-section-in-elf) ?

### `.data` section

↑ **Parent:** [Sections](#sections)

<a id="_191"></a>
`.data` is section 1:<a id="_192"></a>

```
00000080  01 00 00 00 01 00 00 00  03 00 00 00 00 00 00 00  |................|
00000090  00 00 00 00 00 00 00 00  00 02 00 00 00 00 00 00  |................|
000000a0  0d 00 00 00 00 00 00 00  00 00 00 00 00 00 00 00  |................|
000000b0  04 00 00 00 00 00 00 00  00 00 00 00 00 00 00 00  |................|
```

<a id="_193"></a>
<a id="_194"></a>
- <a id="_195"></a>
  80 0: `sh_name` = `01 00 00 00`: index 1 in the `.shstrtab` string table

  <a id="_196"></a>
  Here, `1` says the name of this section starts at the first character of that section, and ends at the first NUL character, making up the string `.data`.

  <a id="_197"></a>
  `.data` is one of the section names which has a predefined meaning according to [http://www.sco.com/developers/gabi/2003-12-17/ch4.strtab.html](http://www.sco.com/developers/gabi/2003-12-17/ch4.strtab.html):<a id="_198"></a>


  > These sections hold initialized data that contribute to the program's memory image.

<a id="_199"></a>
<a id="_200"></a>
- 80 4: `sh_type` = `01 00 00 00`: `SHT_PROGBITS`: the section content is not specified by ELF, only by how the program interprets it. Normal since a `.data` section.
<a id="_201"></a>
- 80 8: `sh_flags` = `03` 7x `00`: `SHF_WRITE` and `SHF_ALLOC`: [http://www.sco.com/developers/gabi/2003-12-17/ch4.sheader.html#sh_flags,](http://www.sco.com/developers/gabi/2003-12-17/ch4.sheader.html#sh_flags,) as required from a `.data` section
<a id="_202"></a>
- 90 0: `sh_addr` = 8x `00`: TODO: standard says:<a id="_203"></a>
  > If the section will appear in the memory image of a process, this member gives the address at which the section's first byte should reside. Otherwise, the member contains 0.

  but I don't understand it very well yet.
<a id="_204"></a>
- 90 8: `sh_offset` = `00 02 00 00 00 00 00 00` = `0x200`: number of bytes from the start of the program to the first byte in this section
<a id="_205"></a>
- <a id="_206"></a>
  a0 0: `sh_size` = `0d 00 00 00 00 00 00 00`

  <a id="_207"></a>
  If we take 0xD bytes starting at `sh_offset` 200, we see:

  <a id="_208"></a>
  ```
  00000200  48 65 6c 6c 6f 20 77 6f  72 6c 64 21 0a 00        |Hello world!..  |
  ```

  <a id="_209"></a>
  AHA! So our `"Hello world!"` string is in the data section like we told it to be on the NASM.

  <a id="_210"></a>
  Once we graduate from `hd`, we will look this up like:

  <a id="_211"></a>
  ```
  readelf -x .data hello_world.o
  ```

  <a id="_212"></a>
  which outputs:

  <a id="_213"></a>
  ```
  Hex dump of section '.data':
    0x00000000 48656c6c 6f20776f 726c6421 0a       Hello world!.
  ```

  <a id="_214"></a>
  NASM sets decent properties for that section because it treats `.data` magically: [https://www.nasm.us/doc/nasmdoc7.html#section-7.9.2](https://www.nasm.us/doc/nasmdoc7.html#section-7.9.2)

  <a id="_215"></a>
  Also note that this was a bad section choice: a good C compiler would put the string in `.rodata` instead, because it is read-only and it would allow for further OS optimizations.<a id="_216"></a>

  <a id="_217"></a>
  - a0 8: `sh_link` and `sh_info` = 8x 0: do not apply to this section type. [http://www.sco.com/developers/gabi/2003-12-17/ch4.sheader.html#special_sections](http://www.sco.com/developers/gabi/2003-12-17/ch4.sheader.html#special_sections)
  <a id="_218"></a>
  - b0 0: `sh_addralign` = `04` = TODO: why is this alignment necessary? Is it only for `sh_addr`, or also for symbols inside `sh_addr`?
  <a id="_219"></a>
  - b0 8: `sh_entsize` = `00` = the section does not contain a table. If != 0, it means that the section contains a table of fixed size entries. In this file, we see from the `readelf` output that this is the case for the `.symtab` and `.rela.text` sections.

### `.text` section

↑ **Parent:** [Sections](#sections)

<a id="_220"></a>
Now that we've done one section manually, let's graduate and use the `readelf -S` of the other sections:<a id="_221"></a>

```
  [Nr] Name              Type             Address           Offset
       Size              EntSize          Flags  Link  Info  Align
  [ 2] .text             PROGBITS         0000000000000000  00000210
       0000000000000027  0000000000000000  AX       0     0     16
```

<a id="_222"></a>
`.text` is executable but not writable: if we try to write to it Linux segfaults. Let's see if we really have some code there:<a id="_223"></a>

```
objdump -d hello_world.o
```
gives:<a id="_224"></a>

```
hello_world.o:     file format elf64-x86-64


Disassembly of section .text:

0000000000000000 <_start>:
   0:       b8 01 00 00 00          mov    $0x1,%eax
   5:       bf 01 00 00 00          mov    $0x1,%edi
   a:       48 be 00 00 00 00 00    movabs $0x0,%rsi
  11:       00 00 00
  14:       ba 0d 00 00 00          mov    $0xd,%edx
  19:       0f 05                   syscall
  1b:       b8 3c 00 00 00          mov    $0x3c,%eax
  20:       bf 00 00 00 00          mov    $0x0,%edi
  25:       0f 05                   syscall
```

<a id="_225"></a>
If we grep `b8 01 00 00` on the `hd`, we see that this only occurs at `00000210`, which is what the section says. And the Size is 27, which matches as well. So we must be talking about the right section.

<a id="_226"></a>
This looks like the right code: a `write` followed by an `exit`.

<a id="_227"></a>
The most interesting part is line `a` which does:<a id="_228"></a>

```
movabs $0x0,%rsi
```
to pass the address of the string to the system call. Currently, the `0x0` is just a placeholder. After linking happens, it will be modified to contain:<a id="_229"></a>

```
4000ba: 48 be d8 00 60 00 00    movabs $0x6000d8,%rsi
```
This modification is possible because of the data of the `.rela.text` section.

<h3 id="sht-strtab"><code>SHT_STRTAB</code></h3>

↑ **Parent:** [Sections](#sections)

<a id="_230"></a>
Sections with `sh_type == SHT_STRTAB` are called string tables.

<a id="_231"></a>
They hold a null separated array of strings.

<a id="_232"></a>
Such sections are used by other sections when string names are to be used. The using section says:<a id="_233"></a>

<a id="_234"></a>
- which string table they are using
<a id="_235"></a>
- what is the index on the target string table where the string starts

<a id="_236"></a>
So for example, we could have a string table containing:<a id="_237"></a>

```
Data: \0 a b c \0 d e f \0
Index: 0 1 2 3  4 5 6 7  8
```

<a id="_238"></a>
The first byte must be a 0. TODO rationale?

<a id="_239"></a>
And if another section wants to use the string `d e f`, they have to point to index `5` of this section (letter `d`).

<a id="_240"></a>
Notable string table sections:<a id="_241"></a>

<a id="_242"></a>
- `.shstrtab`
<a id="_243"></a>
- `.strtab`

### `.shstrtab`

↑ **Parent:** [Sections](#sections)

<a id="_244"></a>
Section type: `sh_type == SHT_STRTAB`.

<a id="_245"></a>
Common name: "section header string table".

<a id="_246"></a>
The section name `.shstrtab` is reserved. The standard says:<a id="_247"></a>


> This section holds section names.

<a id="_248"></a>
This section gets pointed to by the `e_shstrnd` field of the ELF header itself.

<a id="_249"></a>
String indexes of this section are are pointed to by the `sh_name` field of section headers, which denote strings.

<a id="_250"></a>
This section does not have `SHF_ALLOC` marked, so it will not appear on the executing program.<a id="_251"></a>

```
readelf -x .shstrtab hello_world.o
```
outputs:<a id="_252"></a>

```
Hex dump of section '.shstrtab':
  0x00000000 002e6461 7461002e 74657874 002e7368 ..data..text..sh
  0x00000010 73747274 6162002e 73796d74 6162002e strtab..symtab..
  0x00000020 73747274 6162002e 72656c61 2e746578 strtab..rela.tex
  0x00000030 7400                                t.
```

<a id="_253"></a>
The data in this section has a fixed format: [http://www.sco.com/developers/gabi/2003-12-17/ch4.strtab.html](http://www.sco.com/developers/gabi/2003-12-17/ch4.strtab.html)

<a id="_254"></a>
If we look at the names of other sections, we see that they all contain numbers, e.g. the `.text` section is number `7`.

<a id="_255"></a>
Then each string ends when the first NUL character is found, e.g. character `12` is `\0` just after `.text\0`.

### `.symtab`

↑ **Parent:** [Sections](#sections)

<a id="_256"></a>
Section type: `sh_type == SHT_SYMTAB`.

<a id="_257"></a>
Common name: "symbol table".

<a id="_258"></a>
First the we note that:<a id="_259"></a>

<a id="_260"></a>
- `sh_link` = `5`
<a id="_261"></a>
- `sh_info` = `6`

<a id="_262"></a>
For `SHT_SYMTAB` sections, those numbers mean that:<a id="_263"></a>

<a id="_264"></a>
- strings that give symbol names are in section 5, `.strtab`
<a id="_265"></a>
- the relocation data is in section 6, `.rela.text`

<a id="_266"></a>
A good high level tool to disassemble that section is:<a id="_267"></a>

```
nm hello_world.o
```
which gives:<a id="_268"></a>

```
0000000000000000 T _start
0000000000000000 d hello_world
000000000000000d a hello_world_len
```

<a id="_269"></a>
This is however a high level view that omits some types of symbols and in which the symbol types . A more detailed disassembly can be obtained with:<a id="_270"></a>

```
readelf -s hello_world.o
```
which gives:<a id="_271"></a>

```
Symbol table '.symtab' contains 7 entries:
   Num:    Value          Size Type    Bind   Vis      Ndx Name
     0: 0000000000000000     0 NOTYPE  LOCAL  DEFAULT  UND
     1: 0000000000000000     0 FILE    LOCAL  DEFAULT  ABS hello_world.asm
     2: 0000000000000000     0 SECTION LOCAL  DEFAULT    1
     3: 0000000000000000     0 SECTION LOCAL  DEFAULT    2
     4: 0000000000000000     0 NOTYPE  LOCAL  DEFAULT    1 hello_world
     5: 000000000000000d     0 NOTYPE  LOCAL  DEFAULT  ABS hello_world_len
     6: 0000000000000000     0 NOTYPE  GLOBAL DEFAULT    2 _start
```

<a id="_272"></a>
The binary format of the table is documented at [http://www.sco.com/developers/gabi/2003-12-17/ch4.symtab.html](http://www.sco.com/developers/gabi/2003-12-17/ch4.symtab.html)

<a id="_273"></a>
The data is:<a id="_274"></a>

```
readelf -x .symtab hello_world.o
```
which gives:<a id="_275"></a>

```
Hex dump of section '.symtab':
  0x00000000 00000000 00000000 00000000 00000000 ................
  0x00000010 00000000 00000000 01000000 0400f1ff ................
  0x00000020 00000000 00000000 00000000 00000000 ................
  0x00000030 00000000 03000100 00000000 00000000 ................
  0x00000040 00000000 00000000 00000000 03000200 ................
  0x00000050 00000000 00000000 00000000 00000000 ................
  0x00000060 11000000 00000100 00000000 00000000 ................
  0x00000070 00000000 00000000 1d000000 0000f1ff ................
  0x00000080 0d000000 00000000 00000000 00000000 ................
  0x00000090 2d000000 10000200 00000000 00000000 -...............
  0x000000a0 00000000 00000000                   ........
```

<a id="_276"></a>
The entries are of type:<a id="_277"></a>

```
typedef struct {
    Elf64_Word  st_name;
    unsigned char   st_info;
    unsigned char   st_other;
    Elf64_Half  st_shndx;
    Elf64_Addr  st_value;
    Elf64_Xword st_size;
} Elf64_Sym;
```

<a id="_278"></a>
Like in the section table, the first entry is magical and set to a fixed meaningless values.

<h4 id="stt-file"><code>STT_FILE</code></h4>

↑ **Parent:** [`.symtab`](#symtab)

<a id="_279"></a>
Entry 1 has `ELF64_R_TYPE == STT_FILE`. `ELF64_R_TYPE` is continued inside of `st_info`.

<a id="_280"></a>
Byte analysis:

<a id="_281"></a>
<a id="_282"></a>
- <a id="_283"></a>
  10 8: `st_name` = `01000000` = character 1 in the `.strtab`, which until the following `\0` makes `hello_world.asm`

  <a id="_284"></a>
  This piece of information file may be used by the linker to decide on which segment sections go: e.g. in `ld` linker script we write:

  <a id="_285"></a>
  ```
  segment_name :
  {
      file(section)
  }
  ```

  <a id="_286"></a>
  to pick a section from a given file.

  <a id="_287"></a>
  Most of the time however, we will just dump all sections with a given name together with:

  <a id="_288"></a>
  ```
  segment_name :
  {
      *(section)
  }
  ```
<a id="_289"></a>
- <a id="_290"></a>
  10 12: `st_info` = `04`

  <a id="_291"></a>
  Bits 0-3 = `ELF64_R_TYPE` = Type = `4` = `STT_FILE`: the main purpose of this entry is to use `st_name` to indicate the name of the file which generated this object file.

  <a id="_292"></a>
  Bits 4-7 = `ELF64_ST_BIND` = Binding = `0` = `STB_LOCAL`. Required value for `STT_FILE`.
<a id="_293"></a>
- 10 13: `st_shndx` = Symbol Table Section header Index = `f1ff` = `SHN_ABS`. Required for `STT_FILE`.
<a id="_294"></a>
- 20 0: `st_value` = 8x `00`: required for value for `STT_FILE`
<a id="_295"></a>
- 20 8: `st_size` = 8x `00`: no allocated size

<a id="_296"></a>
Now from the `readelf`, we interpret the others quickly.

<h4 id="stt-section"><code>STT_SECTION</code></h4>

↑ **Parent:** [`.symtab`](#symtab)

<a id="_297"></a>
There are two such entries, one pointing to `.data` and the other to `.text` (section indexes `1` and `2`).<a id="_298"></a>

```
Num:    Value          Size Type    Bind   Vis      Ndx Name
  2: 0000000000000000     0 SECTION LOCAL  DEFAULT    1
  3: 0000000000000000     0 SECTION LOCAL  DEFAULT    2
```

<a id="_299"></a>
TODO what is their purpose?

<h4 id="stt-notype"><code>STT_NOTYPE</code></h4>

↑ **Parent:** [`.symtab`](#symtab)

<a id="_300"></a>
Then come the most important symbols:<a id="_301"></a>

```
Num:    Value          Size Type    Bind   Vis      Ndx Name
  4: 0000000000000000     0 NOTYPE  LOCAL  DEFAULT    1 hello_world
  5: 000000000000000d     0 NOTYPE  LOCAL  DEFAULT  ABS hello_world_len
  6: 0000000000000000     0 NOTYPE  GLOBAL DEFAULT    2 _start
```

<a id="_302"></a>
`hello_world` string is in the `.data` section (index 1). It's value is 0: it points to the first byte of that section.

<a id="_303"></a>
`_start` is marked with `GLOBAL` visibility since we wrote:<a id="_304"></a>

```
global _start
```

<a id="_305"></a>
in NASM. This is necessary since it must be seen as the entry point. Unlike in C, by default NASM labels are local.

<h5 id="shn-abs"><code>SHN_ABS</code></h5>

↑ **Parent:** [`STT_NOTYPE`](#stt-notype)

<a id="_306"></a>
`hello_world_len` points to the special `st_shndx == SHN_ABS == 0xF1FF`.

<a id="_307"></a>
`0xF1FF` is chosen so as to not conflict with other sections.

<a id="_308"></a>
`st_value == 0xD == 13` which is the value we have stored there on the assembly: the length of the string `Hello World!`.

<a id="_309"></a>
This means that relocation will not affect this value: it is a constant.

<a id="_310"></a>
This is small optimization that our assembler does for us and which has ELF support.

<a id="_311"></a>
If we had used the address of `hello_world_len` anywhere, the assembler would not have been able to mark it as `SHN_ABS`, and the linker would have extra relocation work on it later.

<h4 id="sht-symtab-on-the-executable"><code>SHT_SYMTAB</code> on the executable</h4>

↑ **Parent:** [`.symtab`](#symtab)

<a id="_312"></a>
By default, NASM places a `.symtab` on the executable as well.

<a id="_313"></a>
This is only used for debugging. Without the symbols, we are completely blind, and must reverse engineer everything.

<a id="_314"></a>
You can strip it with `objcopy`, and the executable will still run. Such executables are called "stripped executables".

### `.strtab`

↑ **Parent:** [Sections](#sections)

<a id="_315"></a>
Holds strings for the symbol table.

<a id="_316"></a>
This section has `sh_type == SHT_STRTAB`.

<a id="_317"></a>
It is pointed to by `sh_link == 5` of the `.symtab` section.<a id="_318"></a>

```
readelf -x .strtab hello_world.o
```
outputs:<a id="_319"></a>

```
Hex dump of section '.strtab':
  0x00000000 0068656c 6c6f5f77 6f726c64 2e61736d .hello_world.asm
  0x00000010 0068656c 6c6f5f77 6f726c64 0068656c .hello_world.hel
  0x00000020 6c6f5f77 6f726c64 5f6c656e 005f7374 lo_world_len._st
  0x00000030 61727400                            art.
```

<a id="_320"></a>
This implies that it is an ELF level limitation that global variables cannot contain NUL characters.

<h3 id="rela-text"><code>.rela.text</code></h3>

↑ **Parent:** [Sections](#sections)

<a id="_321"></a>
Section type: `sh_type == SHT_RELA`.

<a id="_322"></a>
Common name: "relocation section".

<a id="_323"></a>
`.rela.text` holds relocation data which says how the address should be modified when the final executable is linked. This points to bytes of the text area that must be modified when linking happens to point to the correct memory locations.

<a id="_324"></a>
Basically, it translates the object text containing the placeholder 0x0 address:<a id="_325"></a>

```
   a:       48 be 00 00 00 00 00    movabs $0x0,%rsi
  11:       00 00 00
```
to the actual executable code containing the final 0x6000d8:<a id="_326"></a>

```
4000ba: 48 be d8 00 60 00 00    movabs $0x6000d8,%rsi
4000c1: 00 00 00
```

<a id="_327"></a>
It was pointed to by `sh_info` = `6` of the `.symtab` section.

<a id="_328"></a>
`readelf -r hello_world.o` outputs:<a id="_329"></a>

```
Relocation section '.rela.text' at offset 0x3b0 contains 1 entries:
  Offset          Info           Type           Sym. Value    Sym. Name + Addend
00000000000c  000200000001 R_X86_64_64       0000000000000000 .data + 0
```

<a id="_330"></a>
The section does not exist in the executable.

<a id="_331"></a>
The actual bytes are:<a id="_332"></a>

```
00000370  0c 00 00 00 00 00 00 00  01 00 00 00 02 00 00 00  |................|
00000380  00 00 00 00 00 00 00 00  00 00 00 00 00 00 00 00  |................|
```

<a id="_333"></a>
The `struct` represented is:<a id="_334"></a>

```
typedef struct {
    Elf64_Addr  r_offset;
    Elf64_Xword r_info;
    Elf64_Sxword    r_addend;
} Elf64_Rela;
```

<a id="_335"></a>
So:<a id="_336"></a>

<a id="_337"></a>
- 370 0: `r_offset` = 0xC: address into the `.text` whose address this relocation will modify
<a id="_338"></a>
- <a id="_339"></a>
  370 8: `r_info` = 0x200000001. Contains 2 fields:<a id="_340"></a>

  <a id="_341"></a>
  - `ELF64_R_TYPE` = 0x1: meaning depends on the exact architecture.
  <a id="_342"></a>
  - `ELF64_R_SYM` = 0x2: index of the section to which the address points, so `.data` which is at index 2.

  <a id="_343"></a>
  The AMD64 ABI says that type `1` is called `R_X86_64_64` and that it represents the operation `S + A` where:<a id="_344"></a>

  <a id="_345"></a>
  - `S`: the value of the symbol on the object file, here `0` because we point to the `00 00 00 00 00 00 00 00` of `movabs $0x0,%rsi`
  <a id="_346"></a>
  - `A`: the addend, present in field `r_added`

  <a id="_347"></a>
  This address is added to the section on which the relocation operates.

  <a id="_348"></a>
  This relocation operation acts on a total 8 bytes.
<a id="_349"></a>
- 380 0: `r_addend` = 0

<a id="_350"></a>
So in our example we conclude that the new address will be: `S + A` = `.data + 0`, and thus the first thing in the data section.

<h4 id="rel-text"><code>.rel.text</code></h4>

↑ **Parent:** [`.rela.text`](#rela-text)

<a id="_351"></a>
Besides `sh_type == SHT_RELA`, there also exists `SHT_REL`, which would have section name `.text.rel` (not present in this object file).

<a id="_352"></a>
Those represent the same `struct`, but without the addend, e.g.:<a id="_353"></a>

```
typedef struct {
    Elf64_Addr  r_offset;
    Elf64_Xword r_info;
} Elf64_Rela;
```

<a id="_354"></a>
The ELF standard says that in many cases the both can be used, and it is just a matter of convenience.

### Dynamic linking sections

↑ **Parent:** [Sections](#sections)

<a id="_355"></a>
This program did not have certain dynamic linking related sections because we linked it minimally with `ld`.

<a id="_356"></a>
However, if you compile a C hello world with GCC 8.2:<a id="_357"></a>

```
gcc -o main.out main.c
```

<a id="_358"></a>
some other interesting sections would appear.

<h4 id="pt-interp"><code>PT_INTERP</code></h4>

↑ **Parent:** [Dynamic linking sections](#dynamic-linking-sections)

<a id="_359"></a>
Contains the path to the dynamic loader, i.e. `/lib64/ld-linux-x86-64.so.2` in Ubuntu 18.10. Explained at: [https://stackoverflow.com/questions/8040631/checking-if-a-binary-compiled-with-static/55664341#55664341](https://stackoverflow.com/questions/8040631/checking-if-a-binary-compiled-with-static/55664341#55664341)

#### Dynamic section

↑ **Parent:** [Dynamic linking sections](#dynamic-linking-sections)

<a id="_360"></a>
Contains a lot of different flag masks.

<h5 id="dt-flags-1"><code>DT_FLAGS_1</code></h5>

↑ **Parent:** [Dynamic section](#dynamic-section)

<a id="_361"></a>
Seems to be a GNU Binutils extension

<h6 id="df-1-pie"><code>DF_1_PIE</code></h6>

↑ **Parent:** [`DT_FLAGS_1`](#dt-flags-1)

<a id="_362"></a>
Determines if an executable is a position independent executable (PIE).

<a id="_363"></a>
Seems to be informational only, since not used by Linux kernel 5.0 or glibc 2.29.

<a id="_364"></a>
`file` 5.36 however does use it to display file type as explained at: [https://stackoverflow.com/questions/34519521/why-does-gcc-create-a-shared-object-instead-of-an-executable-binary-according-to/55704865#55704865](https://stackoverflow.com/questions/34519521/why-does-gcc-create-a-shared-object-instead-of-an-executable-binary-according-to/55704865#55704865)

## Program header table

↑ **Parent:** [ELF Hello World Tutorial](elf-hello-world.md)

<a id="_365"></a>
Only appears in the executable.

<a id="_366"></a>
Contains information of how the executable should be put into the process virtual memory.

<a id="_367"></a>
The executable is generated from object files by the linker. The main jobs that the linker does are:

<a id="_368"></a>
<a id="_369"></a>
- <a id="_370"></a>
  determine which sections of the object files will go into which segments of the executable.

  <a id="_371"></a>
  In Binutils, this comes down to parsing a linker script, and dealing with a bunch of defaults.

  <a id="_372"></a>
  You can get the linker script used with `ld --verbose`, and set a custom one with `ld -T`.
<a id="_373"></a>
- do relocation according to the `.rela.text` section. This depends on how the multiple sections are put into memory.

<a id="_374"></a>
`readelf -l hello_world.out` gives:<a id="_375"></a>

```
Elf file type is EXEC (Executable file)
Entry point 0x4000b0
There are 2 program headers, starting at offset 64

Program Headers:
  Type           Offset             VirtAddr           PhysAddr
                 FileSiz            MemSiz              Flags  Align
  LOAD           0x0000000000000000 0x0000000000400000 0x0000000000400000
                 0x00000000000000d7 0x00000000000000d7  R E    200000
  LOAD           0x00000000000000d8 0x00000000006000d8 0x00000000006000d8
                 0x000000000000000d 0x000000000000000d  RW     200000

 Section to Segment mapping:
  Segment Sections...
   00     .text
   01     .data
```

<a id="_376"></a>
On the ELF header, `e_phoff`, `e_phnum` and `e_phentsize` told us that there are 2 program headers, which start at `0x40` and are `0x38` bytes long each, so they are:<a id="_377"></a>

```
00000040  01 00 00 00 05 00 00 00  00 00 00 00 00 00 00 00  |................|
00000050  00 00 40 00 00 00 00 00  00 00 40 00 00 00 00 00  |..@.......@.....|
00000060  d7 00 00 00 00 00 00 00  d7 00 00 00 00 00 00 00  |................|
00000070  00 00 20 00 00 00 00 00                           |.. .....        |
```
and:<a id="_378"></a>

```
00000070                           01 00 00 00 06 00 00 00  |        ........|
00000080  d8 00 00 00 00 00 00 00  d8 00 60 00 00 00 00 00  |..........`.....|
00000090  d8 00 60 00 00 00 00 00  0d 00 00 00 00 00 00 00  |..`.............|
000000a0  0d 00 00 00 00 00 00 00  00 00 20 00 00 00 00 00  |.......... .....|
```

<a id="_379"></a>
Structure represented [http://www.sco.com/developers/gabi/2003-12-17/ch5.pheader.html](http://www.sco.com/developers/gabi/2003-12-17/ch5.pheader.html):<a id="_380"></a>

```
typedef struct {
    Elf64_Word  p_type;
    Elf64_Word  p_flags;
    Elf64_Off   p_offset;
    Elf64_Addr  p_vaddr;
    Elf64_Addr  p_paddr;
    Elf64_Xword p_filesz;
    Elf64_Xword p_memsz;
    Elf64_Xword p_align;
} Elf64_Phdr;
```

<a id="_381"></a>
Breakdown of the first one:<a id="_382"></a>

<a id="_383"></a>
- 40 0: `p_type` = `01 00 00 00` = `PT_LOAD`: this is a regular segment that will get loaded in memory.
<a id="_384"></a>
- 40 4: `p_flags` = `05 00 00 00` = execute and read permissions. No write: we cannot modify the text segment. A classic way to do this in C is with string literals: [https://stackoverflow.com/a/30662565/895245](https://stackoverflow.com/a/30662565/895245) This allows kernels to do certain optimizations, like sharing the segment amongst processes.
<a id="_385"></a>
- <a id="_386"></a>
  40 8: `p_offset` = 8x `00` TODO: what is this? Standard says:

  <a id="_387"></a>
  > This member gives the offset from the beginning of the file at which the first byte of the segment resides.

  <a id="_388"></a>
  But it looks like offsets from the beginning of segments, not file?
<a id="_389"></a>
- 50 0: `p_vaddr` = `00 00 40 00 00 00 00 00`: initial virtual memory address to load this segment to
<a id="_390"></a>
- 50 8: `p_paddr` = `00 00 40 00 00 00 00 00`: unspecified effect. Intended for systems in which physical addressing matters. TODO example?
<a id="_391"></a>
- <a id="_392"></a>
  60 0: `p_filesz` = `d7 00 00 00 00 00 00 00`: size that the segment occupies in memory. If smaller than `p_memsz`, the OS fills it with zeroes to fit when loading the program. This is how BSS data is implemented to save space on executable files. i368 ABI says on `PT_LOAD`:

  <a id="_393"></a>
  > The bytes from the file are mapped to the beginning of the memory segment. If the segment’s memory size (p\_memsz) is larger than the file size (p\_filesz), the ‘‘extra’’ bytes are defined to hold the value 0 and to follow the segment’s initialized area. The file size may not be larger than the memory size.

<a id="_394"></a>
<a id="_395"></a>
- 60 8: `p_memsz` = `d7 00 00 00 00 00 00 00`: size that the segment occupies in memory
<a id="_396"></a>
- <a id="_397"></a>
  70 0: `p_align` = `00 00 20 00 00 00 00 00`: 0 or 1 mean no alignment required. TODO why is this required? Why not just use `p_addr` directly, and get that right? Docs also say:

  <a id="_398"></a>
  > p\_vaddr should equal p\_offset, modulo p\_align

<a id="_399"></a>
The second segment (`.data`) is analogous. TODO: why use offset `0x0000d8` and address `0x00000000006000d8`? Why not just use `0` and `0x00000000006000d8`?

<a id="_400"></a>
Then the:<a id="_401"></a>

```
 Section to Segment mapping:
```
section of the `readelf` tells us that:<a id="_402"></a>

<a id="_403"></a>
- 0 is the `.text` segment. Aha, so this is why it is executable, and not writable
<a id="_404"></a>
- 1 is the `.data` segment.

<a id="_405"></a>
TODO where does this information come from? [https://stackoverflow.com/questions/23018496/section-to-segment-mapping-in-elf-files](https://stackoverflow.com/questions/23018496/section-to-segment-mapping-in-elf-files)

## Backlinks

↑ **Parent:** [ELF Hello World Tutorial](elf-hello-world.md)

<a id="_406"></a>
News aggregators:<a id="_407"></a>

<a id="_408"></a>
- 2017-05: [https://news.ycombinator.com/item?id=14359159](https://news.ycombinator.com/item?id=14359159) [https://web.archive.org/web/20170517174951/https://news.ycombinator.com/news](https://web.archive.org/web/20170517174951/https://news.ycombinator.com/news)

<a id="_409"></a>
Personal websites:<a id="_410"></a>

<a id="_411"></a>
- [https://www.etherington.xyz/elfguide](https://www.etherington.xyz/elfguide)

## ↑ Ancestors (9)

1. [Executable and Linkable Format](systems-programming.md#executable-and-linkable-format)
2. [Executable file format](systems-programming.md#executable-file-format)
3. [Systems programming](systems-programming.md)
4. [Software](software.md)
5. [Computer](computer.md)
6. [Information technology](technology.md#information-technology)
7. [Area of technology](technology.md#area-of-technology)
8. [Technology](technology.md)
9. [Ciro Santilli's Homepage](README.md)

## ← Incoming links (2)

- [The best articles by Ciro Santilli](articles.md)
- [Executable and Linkable Format](systems-programming.md#executable-and-linkable-format)
