# Run [Zephyr](zephyr-operating-system.md) on Micro Bit

↑ **Parent:** [Program the Micro Bit with X](program-the-micro-bit-with-x.md)  
🏷️ **Tags:** [Run Zephyr on X](run-zephyr-on-x.md)

Docs: [https://docs.zephyrproject.org/2.7.0/boards/arm/bbc_microbit/doc/index.html](https://docs.zephyrproject.org/2.7.0/boards/arm/bbc_microbit/doc/index.html)

Build worked:
```
west build -d build/microbit/hello_world -b bbc_microbit samples/hello_world
```
but flash failed:
```
west flash -d build/microbit/hello_world
```
Related: [https://mattoppenheim.com/2018/06/24/using-udev-to-remove-the-need-for-sudo-with-the-bbc-microbit](https://mattoppenheim.com/2018/06/24/using-udev-to-remove-the-need-for-sudo-with-the-bbc-microbit)

The build also generates a .hex file by default, and we've tried to flash it manually with:
```
cp build/microbit/hello_world/zephyr/zephyr.hex /media/ciro/MICROBIT/
```
but we failed to see it do anything with [zephyr/blink\_gpio.c](_file/zephyr/blink_gpio.c.md), so not sure if the flashing was broken or if the code was broken, or if we didn't find the IO pins correctly.

## ↑ Ancestors (11)

1. [Program the Micro Bit with X](program-the-micro-bit-with-x.md)
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
