# Section vs segment

↑ **Parent:** [ELF Hello World Tutorial](../elf-hello-world-split.md)

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
