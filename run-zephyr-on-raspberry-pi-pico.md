# Run Zephyr on Raspberry Pi Pico

↑ **Parent:** [Raspberry Pi Pico](raspberry-pi-pico.md)  
🏷️ **Tags:** [Run Zephyr on X](run-zephyr-on-x.md)

[Zephyr](zephyr-operating-system.md) docs: [https://docs.zephyrproject.org/latest/boards/raspberrypi/rpi_pico/doc/index.html](https://docs.zephyrproject.org/latest/boards/raspberrypi/rpi_pico/doc/index.html)

Note that the [LED blinker](led-blinker.md) example does not work on the [Raspberry Pi Pico W](raspberry-pi-pico-w.md), see also: [Run Zephyr on Raspberry Pi Pico W](run-zephyr-on-raspberry-pi-pico-w.md).

You can speed up the debug loop a little bit by plugging the Pi with BOOTSEL selected, and then running:
```
west flash --runner uf2
```
This flashes the image, and immediately turns off BOOTSEL mode and runs the program.

However to run again you need to unplug the USB and re-plug with BOOTSEL again so it is still painful.

<a id="video-let-s-run-zephyr-rtos-on-raspberry-pi-pico-ep-1-by-mr-green-s-workshop"></a>
**[Video 24](#video-let-s-run-zephyr-rtos-on-raspberry-pi-pico-ep-1-by-mr-green-s-workshop). Let's run Zephyr RTOS on Raspberry Pi Pico. Ep.1 by Mr. Green's Workshop.** [Source](https://www.youtube.com/watch?v=OyMyY4IwsJE).

**Table of contents**

- [Run Zephyr on Raspberry Pi Pico W](run-zephyr-on-raspberry-pi-pico-w.md)

## ↑ Ancestors (11)

1. [Raspberry Pi Pico](raspberry-pi-pico.md)
2. [Raspberry Pi](raspberry-pi.md)
3. [Raspberry Pi Foundation project](raspberry-pi-foundation-project.md)
4. [Raspberry Pi Foundation](raspberry-pi-foundation.md)
5. [Computer manufacturer](computer-manufacturer.md)
6. [Computer hardware](computer-hardware-split.md)
7. [Computer](computer-split.md)
8. [Information technology](information-technology.md)
9. [Area of technology](area-of-technology.md)
10. [Technology](technology-split.md)
11. [Ciro Santilli's Homepage](split.md)
