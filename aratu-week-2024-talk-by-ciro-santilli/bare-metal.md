# Bare metal!

↑ **Parent:** [Lots of in-tree examples](lots-of-in-tree-examples.md)

<a id="_74"></a>
Powered by crosstool-NG:

<a id="_75"></a>
[baremetal/arch/aarch64/semihost\_exit.S](https://github.com/cirosantilli/linux-kernel-module-cheat/blob/master/baremetal/arch/aarch64/semihost_exit.S)

<a id="_76"></a>
```
.global main
main:
    /* 0x20026 == ADP_Stopped_ApplicationExit */
    mov x1, 0x26
    movk x1, 2, lsl 16
    str x1, [sp, 0]

    /* Exit status code. Host QEMU process exits with that status. */
    mov x0, 0
    str x0, [sp, 8]

    /* x1 contains the address of parameter block.
     * Any memory address could be used.
     */
    mov x1, sp

    /* SYS_EXIT */
    mov w0, 0x18

    /* Do the semihosting call on A64. */
    hlt 0xf000
```

## ↑ Ancestors (6)

1. [Lots of in-tree examples](lots-of-in-tree-examples.md)
2. [Linux Kernel Module Cheat](linux-kernel-module-cheat.md)
3. [Aratu Week 2024 Talk by Ciro Santilli: My Best Random Projects](../aratu-week-2024-talk-by-ciro-santilli-split.md)
4. [Talk by Ciro Santilli](../talk-by-ciro-santilli.md)
5. [Ciro Santilli](../ciro-santilli-split.md)
6. [Ciro Santilli's Homepage](../split.md)
