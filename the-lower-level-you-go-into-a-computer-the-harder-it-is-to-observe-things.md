# The lower level you go into a computer, the harder it is to observe things

↑ **Parent:** [How computers work?](how-computers-work.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/The_lower_level_you_go_into_a_computer,_the_harder_it_is_to_observe_things)

This is a general principle of software/hardware design that Ciro feels holds wide applicability.

The most extreme case of this is of course the [integrated circuit](integrated-circuit.md) itself, in which it is essentially impossible (?) to observe the specific value of some indidual wire at some point.

Somewhat on the other extreme, we have high level programming languages running on top of an [operating system](operating-system.md): at this point, you can just [GDB step debug](gnu-debugger.md) your program, print the value of any variable/memory location, and fully understand anything that you want. Provided that you manage to easily reach that point of interest.

And for anything in between we have various intermediate levels of complication. The most notable perhaps being developing the operating system itself. At this level, you can't so easily step debug (although [techniques do exist](step-debug-the-linux-kernel.md)). For early boot or [bootloaders](bootloader.md) for example, you might want to use [JTAG](jtag.md) for example on real hardware.

In parallel to this, there is also another very important pair of closely linked tradeoffs:
- the lower level at which something is implemented, the faster it runs
- [emulation](emulator.md) gives you observability back, at the cost of slower runtime

Emulation also has another potential downside: unless you are very careful at implementing things correctly, your model might not be representative of the real thing. Also, there may be important tradeoffs between how much the model looks like the real thing, and how fast it runs. For example, [QEMU](qemu.md)'s use of [binary translation](binary-translation.md) allows it to run orders of magnitude faster than [gem5](gem5.md). However, you are unable to make any predictions about system performance with QEMU, since you are not modelling key elements like the cache or CPU pipeline.

[Instrumentation](instrumentation-computer-programming.md) is another technique that has can be considered to achieve greater observability.

**Table of contents**

- [Instrumentation (computer programming)](instrumentation-computer-programming.md)

## ↑ Ancestors (6)

1. [How computers work?](how-computers-work.md)
2. [Computer](computer-split.md)
3. [Information technology](information-technology.md)
4. [Area of technology](area-of-technology.md)
5. [Technology](technology-split.md)
6. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (1)

- [Molecular biology feels like systems programming](molecular-biology-feels-like-systems-programming.md)
