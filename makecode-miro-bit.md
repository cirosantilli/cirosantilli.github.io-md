# MakeCode Miro Bit

↑ **Parent:** [Micro Bit simulator](micro-bit-simulator.md)

[https://makecode.microbit.org](https://makecode.microbit.org)

Microbit simulator using some [Microsoft](microsoft-split.md) framework.

TODO the Python code from there does not seem to run on the microbit via `uflash`, because it is not [MicroPython](micropython.md).

[https://support.microbit.org/support/solutions/articles/19000111744-makecode-python-and-micropython](https://support.microbit.org/support/solutions/articles/19000111744-makecode-python-and-micropython) explains.

[https://forum.makecode.com/t/help-understanding-local-build-options/6130](https://forum.makecode.com/t/help-understanding-local-build-options/6130) asks how to compile locally and suggests it is possible. Seems to require [Yotta](yotta-build-system.md), so presumably compiles?

Presumably this is because Microsoft ported their MakeCode thing to the MicroBit, and the Micro Bit foundation accepted them.

E.g. there toggling a LED:
```
led.toggle(0, 0)
```
but the code that works locally is a completely differently named API `set_pixel`:
```
microbit.display.set_pixel(0, 0, )
```
Microsoft going all in on adopt extend extinguish from an early age!

## ↑ Ancestors (11)

1. [Micro Bit simulator](micro-bit-simulator.md)
2. [Micro Bit](micro-bit.md)
3. [Microcontroller devboard](microcontroller-devboard.md)
4. [Microprocessor development board](microprocessor-development-board.md)
5. [Printed circuit board](printed-circuit-board.md)
6. [Circuit board](circuit-board.md)
7. [Electronic circuit](electronic-circuit.md)
8. [Electronics](electronics-split.md)
9. [Area of technology](area-of-technology.md)
10. [Technology](technology-split.md)
11. [Ciro Santilli's Homepage](split.md)
