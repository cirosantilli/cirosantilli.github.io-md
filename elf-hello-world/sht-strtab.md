<h1 id="sht-strtab"><code>SHT_STRTAB</code></h1>

↑ **Parent:** [Sections](sections.md)

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

## ↑ Ancestors (11)

1. [Sections](sections.md)
2. [ELF Hello World Tutorial](../elf-hello-world-split.md)
3. [Executable and Linkable Format](../executable-and-linkable-format.md)
4. [Executable file format](../executable-file-format.md)
5. [Systems programming](../systems-programming-split.md)
6. [Software](../software-split.md)
7. [Computer](../computer-split.md)
8. [Information technology](../information-technology.md)
9. [Area of technology](../area-of-technology.md)
10. [Technology](../technology-split.md)
11. [Ciro Santilli's Homepage](../split.md)
