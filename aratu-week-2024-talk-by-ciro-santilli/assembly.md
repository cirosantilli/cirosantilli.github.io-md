# Assembly

↑ **Parent:** [Lots of in-tree examples](lots-of-in-tree-examples.md)

<a id="_71"></a>
Assertions! The best way to learn assembly.

<a id="_72"></a>
[userland/arch/x86\_64/add.S](https://github.com/cirosantilli/linux-kernel-module-cheat/blob/master/userland/arch/x86_64/add.S)

<a id="_73"></a>
```
#include <lkmc.h>

LKMC_PROLOGUE
    /* Register immediate. */
    mov $1, %rax
    add $2, %rax
    LKMC_ASSERT_EQ(%rax, $3)
LKMC_EPILOGUE
```

## ↑ Ancestors (6)

1. [Lots of in-tree examples](lots-of-in-tree-examples.md)
2. [Linux Kernel Module Cheat](linux-kernel-module-cheat.md)
3. [Aratu Week 2024 Talk by Ciro Santilli: My Best Random Projects](../aratu-week-2024-talk-by-ciro-santilli-split.md)
4. [Talk by Ciro Santilli](../talk-by-ciro-santilli.md)
5. [Ciro Santilli](../ciro-santilli-split.md)
6. [Ciro Santilli's Homepage](../split.md)
