# ELF Hello World Tutorial

↑ **Parent:** [Executable and Linkable Format](executable-and-linkable-format.md)  
🏷️ **Tags:** [The best articles by Ciro Santilli](articles-split.md)

<a id="_2"></a>
Introductory analysis of a simple example of the [executable and Linkable Format](executable-and-linkable-format.md).

<a id="_3"></a>
Extracted from [this Stack Overflow answer](https://stackoverflow.com/a/30648229/895245).

**Table of contents**

- [Introduction](elf-hello-world/introduction.md)
  - [Standards](elf-hello-world/standards.md)
  - [How to learn](elf-hello-world/how-to-learn.md)
  - [Specified file formats](elf-hello-world/specified-file-formats.md)
  - [Implementations](elf-hello-world/implementations.md)
- [Minimal ELF file](elf-hello-world/minimal-elf-file.md)
- [Generate the example](elf-hello-world/generate-the-example.md)
- [Object hd](elf-hello-world/object-hd.md)
- [Executable hd](elf-hello-world/executable-hd.md)
- [Global file structure](elf-hello-world/global-file-structure.md)
- [Section vs segment](elf-hello-world/section-vs-segment.md)
- [ELF header](elf-hello-world/elf-header.md)
- [Section header table](elf-hello-world/section-header-table.md)
- [Sections](elf-hello-world/sections.md)
  - [Index 0 section](elf-hello-world/index-0-section.md)
    - [`SHT_NULL`](elf-hello-world/sht-null.md)
  - [`.data` section](elf-hello-world/data-section.md)
  - [`.text` section](elf-hello-world/text-section.md)
  - [`SHT_STRTAB`](elf-hello-world/sht-strtab.md)
  - [`.shstrtab`](elf-hello-world/shstrtab.md)
  - [`.symtab`](elf-hello-world/symtab.md)
    - [`STT_FILE`](elf-hello-world/stt-file.md)
    - [`STT_SECTION`](elf-hello-world/stt-section.md)
    - [`STT_NOTYPE`](elf-hello-world/stt-notype.md)
      - [`SHN_ABS`](elf-hello-world/shn-abs.md)
    - [`SHT_SYMTAB` on the executable](elf-hello-world/sht-symtab-on-the-executable.md)
  - [`.strtab`](elf-hello-world/strtab.md)
  - [`.rela.text`](elf-hello-world/rela-text.md)
    - [`.rel.text`](elf-hello-world/rel-text.md)
  - [Dynamic linking sections](elf-hello-world/dynamic-linking-sections.md)
    - [`PT_INTERP`](elf-hello-world/pt-interp.md)
    - [Dynamic section](elf-hello-world/dynamic-section.md)
      - [`DT_FLAGS_1`](elf-hello-world/dt-flags-1.md)
        - [`DF_1_PIE`](elf-hello-world/df-1-pie.md)
- [Program header table](elf-hello-world/program-header-table.md)
- [Backlinks](elf-hello-world/backlinks.md)

## ↑ Ancestors (9)

1. [Executable and Linkable Format](executable-and-linkable-format.md)
2. [Executable file format](executable-file-format.md)
3. [Systems programming](systems-programming-split.md)
4. [Software](software-split.md)
5. [Computer](computer-split.md)
6. [Information technology](information-technology.md)
7. [Area of technology](area-of-technology.md)
8. [Technology](technology-split.md)
9. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (2)

- [The best articles by Ciro Santilli](articles-split.md)
- [Executable and Linkable Format](executable-and-linkable-format.md)
