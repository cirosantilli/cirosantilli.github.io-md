# K-ary trees to the rescue

↑ **Parent:** [Example: multi-level paging scheme](example-multi-level-paging-scheme.md)

<a id="_176"></a>
The algorithmically minded will have noticed that paging requires [associative array](../associative-array.md) (like Java `Map` of Python `dict()`) abstract data structure where:<a id="_177"></a>

<a id="_178"></a>
- the keys are linear pages addresses, thus of integer type
<a id="_179"></a>
- the values are physical page addresses, also of integer type

<a id="_180"></a>
The single level paging scheme uses a simple array implementation of the associative array:<a id="_181"></a>

<a id="_182"></a>
- the keys are the array index
<a id="_183"></a>
- this implementation is very fast in time
<a id="_184"></a>
- but it is too inefficient in memory
and in C pseudo-code it looks like this:<a id="_185"></a>

```
linear_address[0]      = physical_address_0
linear_address[1]      = physical_address_1
linear_address[2]      = physical_address_2
...
linear_address[2^20-1] = physical_address_N
```

<a id="_186"></a>
But there another simple associative array implementation that overcomes the memory problem: an (unbalanced) [k-ary tree](../k-ary-tree.md).

<a id="_187"></a>
A K-ary tree, is just like a [binary tree](../binary-tree.md), but with K children instead of 2.

<a id="_188"></a>
Using a K-ary tree instead of an array implementation has the following trade-offs:<a id="_189"></a>

<a id="_190"></a>
- it uses way less memory
<a id="_191"></a>
- it is slower since we have to de-reference extra pointers

<a id="_192"></a>
In C-pseudo code, a 2-level K-ary tree with `K = 2^10` looks like this:<a id="_193"></a>

```
level0[0] = &level1_0[0]
    level1_0[0]      = physical_address_0_0
    level1_0[1]      = physical_address_0_1
    ...
    level1_0[2^10-1] = physical_address_0_N
level0[1] = &level1_1[0]
    level1_1[0]      = physical_address_1_0
    level1_1[1]      = physical_address_1_1
    ...
    level1_1[2^10-1] = physical_address_1_N
...
level0[N] = &level1_N[0]
    level1_N[0]      = physical_address_N_0
    level1_N[1]      = physical_address_N_1
    ...
    level1_N[2^10-1] = physical_address_N_N
```
and we have the following arrays:<a id="_194"></a>

<a id="_195"></a>
- one `directory`, which has `2^10` elements. Each element contains a pointer to a page table array.
<a id="_196"></a>
- up to 2^10 `pagetable` arrays. Each one has `2^10` 4 byte page entries.
and it still contains `2^10 * 2^10 = 2^20` possible keys.

<a id="_197"></a>
K-ary trees can save up a lot of space, because if we only have one key, then we only need the following arrays:<a id="_198"></a>

<a id="_199"></a>
- one `directory` with 2^10 entries
<a id="_200"></a>
- one `pagetable` at `directory[0]` with 2^10 entries
<a id="_201"></a>
- all other `directory[i]` are marked as invalid, don't point to anything, and we don't allocate `pagetable` for them at all

## ↑ Ancestors (13)

1. [Example: multi-level paging scheme](example-multi-level-paging-scheme.md)
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
