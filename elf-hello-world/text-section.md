# `.text` section

↑ **Parent:** [Sections](sections.md)

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
