# Micro Bit example

↑ **Parent:** [Micro Bit](micro-bit.md)

- [microbit/micropython/uart.py](microbit/micropython/uart.py): the Micro BIt comes with a [UART](universal-asynchronous-receiver-transmitter.md) simulator via the USB connection, it is very convenient: [https://support.microbit.org/support/solutions/articles/19000022103-outputing-serial-data-from-the-micro-bit-to-a-computer](https://support.microbit.org/support/solutions/articles/19000022103-outputing-serial-data-from-the-micro-bit-to-a-computer) To output data to the computer simply use Python `print`. To receive you can e.g. use [GNU screen](gnu-screen.md):
  ```
  screen /dev/ttyACM0 115200
  ```

  It appears to be very unreliable however, some times it shows up, sometimes it doesn't.

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
