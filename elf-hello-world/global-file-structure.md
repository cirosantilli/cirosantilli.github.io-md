# Global file structure

↑ **Parent:** [ELF Hello World Tutorial](../elf-hello-world-split.md)

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

## ↑ Ancestors (10)

1. [ELF Hello World Tutorial](../elf-hello-world-split.md)
2. [Executable and Linkable Format](../executable-and-linkable-format.md)
3. [Executable file format](../executable-file-format.md)
4. [Systems programming](../systems-programming-split.md)
5. [Software](../software-split.md)
6. [Computer](../computer-split.md)
7. [Information technology](../information-technology.md)
8. [Area of technology](../area-of-technology.md)
9. [Technology](../technology-split.md)
10. [Ciro Santilli's Homepage](../split.md)
