# Excessive encapsulation is the root of much evil

↑ **Parent:** [Ciro Santilli's software engineering wisdom](ciro-santilli-s-software-engineering-wisdom.md)  
🏷️ **Tags:** [You aren't gonna need it](you-aren-t-gonna-need-it.md)

Some anecdotes.

[Ciro Santilli](ciro-santilli-split.md) never splits up functions unless there is more than one calling point. If you split early, the chances that the interface will be wrong are huge, and a much larger refactoring follows.

If you just want to separate variables, just use a scope e.g.:

```
int cross_block_var;

// First step.
{
    int myvar;
}

// Second step.
{
    int myvar;
}
```

Ciro has seen and had to deal with in his lifetime with two projects that had like 3 to 10 git separate Git repositories, all created and maintained by the same small group of developers of the same organization, even though one could not build without the other. Keeping everything in sync was Hell! Why not just have three directories inside a single repository with a single source of truth?

Another important case: [Linux](linux.md) should have at least a C standard library, init system, and shell in-tree, like [BSD Operating Systems](berkeley-software-distribution.md), as mentioned at: [Section "Linux"](linux.md).

## ↑ Ancestors (8)

1. [Ciro Santilli's software engineering wisdom](ciro-santilli-s-software-engineering-wisdom.md)
2. [Software engineering](software-engineering.md)
3. [Software](software-split.md)
4. [Computer](computer-split.md)
5. [Information technology](information-technology.md)
6. [Area of technology](area-of-technology.md)
7. [Technology](technology-split.md)
8. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (1)

- [Evil](evil.md)
