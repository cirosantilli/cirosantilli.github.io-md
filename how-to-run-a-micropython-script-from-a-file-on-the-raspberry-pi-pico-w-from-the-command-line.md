# How to run a MicroPython script from a file on the Raspberry Pi Pico W from the command line?

↑ **Parent:** [Program Raspberry Pi Pico W with MicroPython](program-raspberry-pi-pico-w-with-micropython.md)

The first/only way Ciro could find was with [ampy](ampy.md): [https://stackoverflow.com/questions/74150782/how-to-run-a-micropython-host-script-file-on-the-raspbery-pi-pico-from-the-host/74150783#74150783](https://stackoverflow.com/questions/74150782/how-to-run-a-micropython-host-script-file-on-the-raspbery-pi-pico-from-the-host/74150783#74150783) That just worked and it worked perfectly!
```
pipx install adafruit-ampy
ampy --port /dev/ttyACM0 run blink.py
```

TODO: possible with [rshell](rshell.md)?

## ↑ Ancestors (15)

1. [Program Raspberry Pi Pico W with MicroPython](program-raspberry-pi-pico-w-with-micropython.md)
2. [Program Raspberry Pi Pico W with X](program-raspberry-pi-pico-w-with-x.md)
3. [Raspberry Pi Pico W](raspberry-pi-pico-w.md)
4. [Raspberry Pi Pico variant](raspberry-pi-pico-variant.md)
5. [Raspberry Pi Pico](raspberry-pi-pico.md)
6. [Raspberry Pi](raspberry-pi.md)
7. [Raspberry Pi Foundation project](raspberry-pi-foundation-project.md)
8. [Raspberry Pi Foundation](raspberry-pi-foundation.md)
9. [Computer manufacturer](computer-manufacturer.md)
10. [Computer hardware](computer-hardware-split.md)
11. [Computer](computer-split.md)
12. [Information technology](information-technology.md)
13. [Area of technology](area-of-technology.md)
14. [Technology](technology-split.md)
15. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (2)

- [Program Raspberry Pi Pico W with MicroPython](program-raspberry-pi-pico-w-with-micropython.md)
- [Raspberry Pi Pico W UART](raspberry-pi-pico-w-uart.md)
