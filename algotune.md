# AlgoTune

↑ **Parent:** [AI code generation benchmark](ai-code-generation-benchmark.md)

[https://algotune.io/](https://algotune.io/)

This one focuses on improving speed of important numerical algorithms as compared to popular implementations.

The general pattern can be seen by observing the optimization of: [https://algotune.io/aes_gcm_encryption_anthropic_claude-opus-4-1-20250805.html](https://algotune.io/aes_gcm_encryption_anthropic_claude-opus-4-1-20250805.html) This shows the chat that the system had.

They define an OS interface to edit files and run right on the prompt, and tell at each stage how many credits are left for a given API and what the speedup was. Amazing. Each task has a $1 budget per provider. Then their software parses commands out of the LLM output and sends formatted responses back. Quite amazing that it works at all.

All pieces of code seem to be in [Python](python-programming-language.md), and the speedups come mainly from using more advanced external computing libraries, like compiling with [Cython](cython.md) or using faster external libraries that are pre-compiled, or more parallel. So it is not that impressive from a purely algorithmic point of view, but it is not bad either.

Correctness is checked automatically by comparing the optimized solution to the original non-optimized one likely for certain inputs.

## ↑ Ancestors (9)

1. [AI code generation benchmark](ai-code-generation-benchmark.md)
2. [Automatic programming](automatic-programming.md)
3. [Compiler](compiler.md)
4. [Software](software-split.md)
5. [Computer](computer-split.md)
6. [Information technology](information-technology.md)
7. [Area of technology](area-of-technology.md)
8. [Technology](technology-split.md)
9. [Ciro Santilli's Homepage](split.md)
