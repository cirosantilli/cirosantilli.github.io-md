# `.data` section

↑ **Parent:** [Sections](sections.md)

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
