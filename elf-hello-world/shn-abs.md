<h1 id="shn-abs"><code>SHN_ABS</code></h1>

↑ **Parent:** [`STT_NOTYPE`](stt-notype.md)

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

## ↑ Ancestors (13)

1. [`STT_NOTYPE`](stt-notype.md)
2. [`.symtab`](symtab.md)
3. [Sections](sections.md)
4. [ELF Hello World Tutorial](../elf-hello-world-split.md)
5. [Executable and Linkable Format](../executable-and-linkable-format.md)
6. [Executable file format](../executable-file-format.md)
7. [Systems programming](../systems-programming-split.md)
8. [Software](../software-split.md)
9. [Computer](../computer-split.md)
10. [Information technology](../information-technology.md)
11. [Area of technology](../area-of-technology.md)
12. [Technology](../technology-split.md)
13. [Ciro Santilli's Homepage](../split.md)
