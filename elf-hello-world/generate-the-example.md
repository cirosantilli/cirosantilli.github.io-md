# Generate the example

↑ **Parent:** [ELF Hello World Tutorial](../elf-hello-world-split.md)

Let's break down a minimal runnable Linux x86-64 example:

hello\_world.asm

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

Compiled with:
```
nasm -w+all -f elf64 -o 'hello_world.o' 'hello_world.asm'
ld -o 'hello_world.out' 'hello_world.o'
```

TODO: use a minimal linker script with `-T` to be more precise and minimal.

Versions:
- NASM 2.10.09
- Binutils version 2.24 (contains `ld`)
- Ubuntu 14.04

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
