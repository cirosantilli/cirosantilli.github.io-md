# Micro Bit getting started

↑ **Parent:** [Micro Bit](micro-bit.md)

When plugged into [Ubuntu 22.04](ubuntu-22-04.md) via the [USB Micro-B](usb-micro-b.md) the [Micro Bit](micro-bit.md) mounts as:
```
/media/$USER/MICROBIT/
```
e.g.:
```
/media/ciro/MICROBIT/
```
for username `ciro`.

Loading the program is done by simply copying a `.hex` binary into the image e.g. with:
```
cp ~/Downloads/microbit_program.hex /media/$USER/MICROBIT/
```
The file name does not matter, only the `.hex` extension.

The back power light flashes while upload is happening.

Flashing takes about 10-15 seconds for the 1.8 MB scroll display hello world from [https://microbit-micropython.readthedocs.io/en/v1.0.1/tutorials/hello.html](https://microbit-micropython.readthedocs.io/en/v1.0.1/tutorials/hello.html):
```
from microbit import *
display.scroll("Hello, World!")
```
and the program starts executing immediately after flash ends.

You can restart the program by clicking the reset button near the USB. When you push down the program dies, and it restarts as soon as you release the button.

## ↑ Ancestors (10)

1. [Micro Bit](micro-bit.md)
2. [Microcontroller devboard](microcontroller-devboard.md)
3. [Microprocessor development board](microprocessor-development-board.md)
4. [Printed circuit board](printed-circuit-board.md)
5. [Circuit board](circuit-board.md)
6. [Electronic circuit](electronic-circuit.md)
7. [Electronics](electronics-split.md)
8. [Area of technology](area-of-technology.md)
9. [Technology](technology-split.md)
10. [Ciro Santilli's Homepage](split.md)
