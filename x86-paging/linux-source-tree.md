# Linux source tree

↑ **Parent:** [Linux kernel usage](linux-kernel-usage.md)

In `v4.2`, look under `arch/x86/`:
- `include/asm/pgtable*`
- `include/asm/page*`
- `mm/pgtable*`
- `mm/page*`

There seems to be no structs defined to represent the pages, only macros: `include/asm/page_types.h` is specially interesting. Excerpt:
```
#define _PAGE_BIT_PRESENT   0   /* is present */
#define _PAGE_BIT_RW        1   /* writeable */
#define _PAGE_BIT_USER      2   /* userspace addressable */
#define _PAGE_BIT_PWT       3   /* page write through */
```

`arch/x86/include/uapi/asm/processor-flags.h` defines `CR0`, and in particular the `PG` bit position:
```
#define X86_CR0_PG_BIT      31 /* Paging */
```

## ↑ Ancestors (13)

1. [Linux kernel usage](linux-kernel-usage.md)
2. [x86 Paging Tutorial](../x86-paging-split.md)
3. [x86](../x86.md)
4. [List of instruction set architectures](../list-of-instruction-set-architectures.md)
5. [Instruction set architecture](../instruction-set-architecture.md)
6. [Processor (computing)](../processor-computing.md)
7. [Computer hardware component type](../computer-hardware-component-type.md)
8. [Computer hardware](../computer-hardware-split.md)
9. [Computer](../computer-split.md)
10. [Information technology](../information-technology.md)
11. [Area of technology](../area-of-technology.md)
12. [Technology](../technology-split.md)
13. [Ciro Santilli's Homepage](../split.md)
