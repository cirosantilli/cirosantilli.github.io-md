# Generate the example

↑ **Parent:** [ELF Hello World Tutorial](../elf-hello-world-split.md)

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
