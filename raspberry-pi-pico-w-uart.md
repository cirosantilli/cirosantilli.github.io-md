# Raspberry Pi Pico W UART

↑ **Parent:** [Raspberry Pi Pico W](raspberry-pi-pico-w.md)  
🏷️ **Tags:** [UART](universal-asynchronous-receiver-transmitter.md)

You can connect form an [Ubuntu 22.04](ubuntu-22-04.md) host as:
```
screen /dev/ttyACM0 115200
```
When in `screen`, you can Ctrl + C to kill `main.py`, and then execution stops and you are left in a Python shell. From there:
- Ctrl + D: reboots
- Ctrl + A K: kills the [GNU screen](gnu-screen.md) window. Execution continues normally
but be aware of: [Raspberry Pi Pico W freezes a few seconds after after screen disconnects from UART](raspberry-pi-pico-w-freezes-a-few-seconds-after-after-screen-disconnects-from-uart.md).

Other options:
- [ampy](ampy.md) `run` command, which solves [How to run a MicroPython script from a file on the Raspberry Pi Pico W from the command line?](how-to-run-a-micropython-script-from-a-file-on-the-raspberry-pi-pico-w-from-the-command-line.md)

## ↑ Ancestors (13)

1. [Raspberry Pi Pico W](raspberry-pi-pico-w.md)
2. [Raspberry Pi Pico variant](raspberry-pi-pico-variant.md)
3. [Raspberry Pi Pico](raspberry-pi-pico.md)
4. [Raspberry Pi](raspberry-pi.md)
5. [Raspberry Pi Foundation project](raspberry-pi-foundation-project.md)
6. [Raspberry Pi Foundation](raspberry-pi-foundation.md)
7. [Computer manufacturer](computer-manufacturer.md)
8. [Computer hardware](computer-hardware-split.md)
9. [Computer](computer-split.md)
10. [Information technology](information-technology.md)
11. [Area of technology](area-of-technology.md)
12. [Technology](technology-split.md)
13. [Ciro Santilli's Homepage](split.md)
