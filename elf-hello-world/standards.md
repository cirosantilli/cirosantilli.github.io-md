# Standards

↑ **Parent:** [Introduction](introduction.md)

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

## ↑ Ancestors (11)

1. [Introduction](introduction.md)
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
