<h1 id="_file/rpi-pico-w/upython/uart.py">rpi-pico-w/upython/uart.py</h1>

↑ **Parent:** [Raspberry Pi Pico W MicroPython example](../../../raspberry-pi-pico-w-micropython-example.md)  
🏷️ **Tags:** [LED blinker](../../../led-blinker.md)

Any `print()` command ends up on the USB, and is shown on the computer via programs such as [ampy](../../../ampy.md) get back.

However, you can also send data over actual UART.

We managed to get it working based on: [https://timhanewich.medium.com/using-uart-between-a-raspberry-pi-pico-and-raspberry-pi-3b-raspbian-71095d1b259f](https://timhanewich.medium.com/using-uart-between-a-raspberry-pi-pico-and-raspberry-pi-3b-raspbian-71095d1b259f) with the help of a [DSD TECH USB to TTL Serial Converter CP2102](../../../ciro-santilli-s-hardware/dsd-tech-usb-to-ttl-serial-converter-cp2102.md) just as shown at: [https://stackoverflow.com/questions/16040128/hook-up-raspberry-pi-via-ethernet-to-laptop-without-router/39086537#39086537](https://stackoverflow.com/questions/16040128/hook-up-raspberry-pi-via-ethernet-to-laptop-without-router/39086537#39086537) for the RPI.

We connect Pin 0 (TX), Pin 1 (RX) and Pin 2 (GND) to the DSD TECH, and the USB to the [Ubuntu 25.04](../../../ubuntu-25-04.md) host laptop.

Then on the host laptop I run:
```
screen /dev/ttyUSB0 9600
```
and a counter shows up there just fine!

## ↑ Ancestors (16)

1. [Raspberry Pi Pico W MicroPython example](../../../raspberry-pi-pico-w-micropython-example.md)
2. [Program Raspberry Pi Pico W with MicroPython](../../../program-raspberry-pi-pico-w-with-micropython.md)
3. [Program Raspberry Pi Pico W with X](../../../program-raspberry-pi-pico-w-with-x.md)
4. [Raspberry Pi Pico W](../../../raspberry-pi-pico-w.md)
5. [Raspberry Pi Pico variant](../../../raspberry-pi-pico-variant.md)
6. [Raspberry Pi Pico](../../../raspberry-pi-pico.md)
7. [Raspberry Pi](../../../raspberry-pi.md)
8. [Raspberry Pi Foundation project](../../../raspberry-pi-foundation-project.md)
9. [Raspberry Pi Foundation](../../../raspberry-pi-foundation.md)
10. [Computer manufacturer](../../../computer-manufacturer.md)
11. [Computer hardware](../../../computer-hardware-split.md)
12. [Computer](../../../computer-split.md)
13. [Information technology](../../../information-technology.md)
14. [Area of technology](../../../area-of-technology.md)
15. [Technology](../../../technology-split.md)
16. [Ciro Santilli's Homepage](../../../split.md)
