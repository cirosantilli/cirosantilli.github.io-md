# Compile MicroPython code for Micro Bit locally

↑ **Parent:** [Run MicroPython on Micro Bit](run-micropython-on-micro-bit.md)

- [https://stackoverflow.com/questions/73425359/is-it-possible-to-compile-microbit-python-code-locally](https://stackoverflow.com/questions/73425359/is-it-possible-to-compile-microbit-python-code-locally)
- [https://stackoverflow.com/questions/52691853/generating-micropython-python-code-hex-file-from-commandline](https://stackoverflow.com/questions/52691853/generating-micropython-python-code-hex-file-from-commandline)

To use a prebuilt firmware, you can just use `uflash`, tested on [Ubuntu 22.04](ubuntu-22-04.md):
```
git clone https://github.com/bbcmicrobit/micropython
cd micropython
git checkout 7fc33d13b31a915cbe90dc5d515c6337b5fa1660
uflash examples/led_dance.py
```
What that does is:
- convert the [MicroPython](micropython.md) code to bytecode
- join it up with a prebuilt firmware that ships with uflash which contains the MicroPython interpreter
- flashes that

To build your own firmware see: [Compile MicroPython code for Micro Bit locally on Ubuntu 22.04 with your own firmware](compile-micropython-code-for-micro-bit-locally-on-ubuntu-22-04-with-your-own-firmware.md)

**Table of contents**

- [Compile MicroPython code for Micro Bit locally on Ubuntu 22.04 with your own firmware](compile-micropython-code-for-micro-bit-locally-on-ubuntu-22-04-with-your-own-firmware.md)

## ↑ Ancestors (12)

1. [Run MicroPython on Micro Bit](run-micropython-on-micro-bit.md)
2. [Program the Micro Bit with X](program-the-micro-bit-with-x.md)
3. [Micro Bit](micro-bit.md)
4. [Microcontroller devboard](microcontroller-devboard.md)
5. [Microprocessor development board](microprocessor-development-board.md)
6. [Printed circuit board](printed-circuit-board.md)
7. [Circuit board](circuit-board.md)
8. [Electronic circuit](electronic-circuit.md)
9. [Electronics](electronics-split.md)
10. [Area of technology](area-of-technology.md)
11. [Technology](technology-split.md)
12. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (1)

- [MicroPython](micropython.md)
