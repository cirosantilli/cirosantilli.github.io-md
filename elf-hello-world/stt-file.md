<h1 id="stt-file"><code>STT_FILE</code></h1>

↑ **Parent:** [`.symtab`](symtab.md)

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

## ↑ Ancestors (12)

1. [`.symtab`](symtab.md)
2. [Sections](sections.md)
3. [ELF Hello World Tutorial](../elf-hello-world-split.md)
4. [Executable and Linkable Format](../executable-and-linkable-format.md)
5. [Executable file format](../executable-file-format.md)
6. [Systems programming](../systems-programming-split.md)
7. [Software](../software-split.md)
8. [Computer](../computer-split.md)
9. [Information technology](../information-technology.md)
10. [Area of technology](../area-of-technology.md)
11. [Technology](../technology-split.md)
12. [Ciro Santilli's Homepage](../split.md)
