# Raspberry Pi Pico

↑ **Parent:** [Raspberry Pi](raspberry-pi.md)  
🏷️ **Tags:** [Microcontroller devboard](microcontroller-devboard.md)

Some key specs:
- [SoC](system-on-a-chip.md):
  - name: RP2040. Custom designed by [Raspberry Pi Foundation](raspberry-pi-foundation.md), likely the first they make themselves rather than using a [Broadcom](broadcom.md) chip. But the design still is closed source, likely wouldn't be easy to open source due to the usage of closed proprietary IP like the [ARM](arm-architecture-family.md)
  - dual core [ARM Cortex-M0+](arm-cortex-m0-plus.md)
  - frequency: 2 kHz to 133 MHz, 125 MHz by default
  - memory: 264KB on-chip [SRAM](static-random-access-memory.md)
- GPIO voltage: 3.3V

Datasheet: [https://datasheets.raspberrypi.com/pico/pico-datasheet.pdf](https://datasheets.raspberrypi.com/pico/pico-datasheet.pdf)

![](https://web.archive.org/web/20220808214856im_/https://twilio-cms-prod.s3.amazonaws.com/images/6ofE97USO9rBn4LidgxTgfrAqK0UiI3v524IPNHc7ac3SA.width-800.png)

**[Figure 9](#_667)** [Source](https://datasheets.raspberrypi.com/pico/Pico-R3-A4-Pinout.pdf).

**Table of contents**

- [Raspberry Pi Pico getting started](raspberry-pi-pico-getting-started.md)
  - [Flash the Raspberry Pi Pico](flash-the-raspberry-pi-pico.md)
    - [picotool](picotool.md)
- [Run Zephyr on Raspberry Pi Pico](run-zephyr-on-raspberry-pi-pico.md)
  - [Run Zephyr on Raspberry Pi Pico W](run-zephyr-on-raspberry-pi-pico-w.md)
- [Raspberry Pi Pico variant](raspberry-pi-pico-variant.md)
  - [Raspberry Pi Pico 1](raspberry-pi-pico-1.md)
  - [Raspberry Pi Pico H](raspberry-pi-pico-h.md)
  - [Raspberry Pi Pico W](raspberry-pi-pico-w.md)
    - [Raspberry Pi Pico W UART](raspberry-pi-pico-w-uart.md)
    - [Program Raspberry Pi Pico W with X](program-raspberry-pi-pico-w-with-x.md)
      - [Program Raspberry Pi Pico W with MicroPython](program-raspberry-pi-pico-w-with-micropython.md)
        - [How to run a MicroPython script from a file on the Raspberry Pi Pico W from the command line?](how-to-run-a-micropython-script-from-a-file-on-the-raspberry-pi-pico-w-from-the-command-line.md)
        - [MicroPython connection tool](micropython-connection-tool.md)
          - [ampy](ampy.md)
          - [rshell](rshell.md)
            - [How to exit from repl in rshell?](how-to-exit-from-repl-in-rshell.md)
        - [Raspberry Pi Pico W freezes a few seconds after after screen disconnects from UART](raspberry-pi-pico-w-freezes-a-few-seconds-after-after-screen-disconnects-from-uart.md)
        - [Program Raspberry Pi Pico W with MicroPython code from the command line](program-raspberry-pi-pico-w-with-micropython-code-from-the-command-line.md)
        - [Program the Raspberry Pi Pico W with MicroPython from Thonny](program-the-raspberry-pi-pico-w-with-micropython-from-thonny.md)
        - [Raspberry Pi Pico W MicroPython example](raspberry-pi-pico-w-micropython-example.md)
          - [rpi-pico-w/upython/blink.py](_file/rpi-pico-w/upython/blink.py.md)
          - [rpi-pico-w/upython/blink\_gpio.py](_file/rpi-pico-w/upython/blink_gpio.py.md)
          - [rpi-pico-w/upython/uart.py](_file/rpi-pico-w/upython/uart.py.md)
          - [rpi-pico-w/upython/adc.py](_file/rpi-pico-w/upython/adc.py.md)
          - [rpi-pico-w/upython/thermistor\_fan\_control.py](_file/rpi-pico-w/upython/thermistor_fan_control.py.md)
      - [Program Raspberry Pi Pico W with C](program-raspberry-pi-pico-w-with-c.md)

## ↑ Ancestors (10)

1. [Raspberry Pi](raspberry-pi.md)
2. [Raspberry Pi Foundation project](raspberry-pi-foundation-project.md)
3. [Raspberry Pi Foundation](raspberry-pi-foundation.md)
4. [Computer manufacturer](computer-manufacturer.md)
5. [Computer hardware](computer-hardware-split.md)
6. [Computer](computer-split.md)
7. [Information technology](information-technology.md)
8. [Area of technology](area-of-technology.md)
9. [Technology](technology-split.md)
10. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (5)

- [Analog-to-digital converter](analog-to-digital-converter.md)
- [Micro Bit v1](ciro-santilli-s-hardware/micro-bit-v1.md)
- [Raspberry Pi Pico 1](raspberry-pi-pico-1.md)
- [Raspberry Pi Pico getting started](raspberry-pi-pico-getting-started.md)
- [UF2](uf2.md)
