# Invalidating TLB entries

↑ **Parent:** [TLB](tlb.md)

When the process changes, `cr3` change to point to the page table of the new current process.

This creates a problem: the TLB is now filled with a bunch of cached entries for the old process.

A simple and naive solution would be to completely invalidate the TLB whenever the `cr3` changes.

However, this is would not be very efficient, because it often happens that we switch back to process 1 before process 2 has completely used up the entire TLB cache entries.

The solution for this is to use so called "Address Space Identifiers" (ASID) as mentioned in sources such as:
- [https://stackoverflow.com/questions/52813239/how-many-bits-there-are-in-a-tlb-asid-tag-for-intel-processors-and-how-to-handl](https://stackoverflow.com/questions/52813239/how-many-bits-there-are-in-a-tlb-asid-tag-for-intel-processors-and-how-to-handl)
- [https://stackoverflow.com/questions/52713940/purpose-of-address-spaced-identifiersasids](https://stackoverflow.com/questions/52713940/purpose-of-address-spaced-identifiersasids)
- [https://www.inf.ed.ac.uk/teaching/courses/os/slides/10-paging16.pdf](https://www.inf.ed.ac.uk/teaching/courses/os/slides/10-paging16.pdf)

Basically, the OS assigns a different ASID for each process, and then TLB entries are automatically also tagged with that ASID. This way when the process makes an access, the TLB can determine if a hit is actually for the current process, or if it is an old address coincidence with another process.

The x86 also offers the `invlpg` instruction which explicitly invalidates a single TLB entry. Other architectures offer even more instructions to invalidated TLB entries, such as invalidating all entries on a given range.

## ↑ Ancestors (13)

1. [TLB](tlb.md)
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
