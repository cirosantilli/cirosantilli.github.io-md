# Raspberry Pi 2

↑ **Parent:** [Raspberry Pis](raspberry-pis.md)

As of 2018-12, I believe that I might have fried the UART on this board when I burnt my last UART to USB converter by connecting ground to 5V.

Linux kernel logs don't show, but do show with the exact same components on the Pi 3 (SD card with `enable_uart=1` + image Raspbian Lite 2018-11-03 and UART cables).

Serial from `cat /proc/cpuinfo`: 00000000a50c1f69

Datasheets: [Raspberry Pi 2](../raspberry-pi-2.md).

## ↑ Ancestors (5)

1. [Raspberry Pis](raspberry-pis.md)
2. [Computers](computers.md)
3. [Ciro Santilli's hardware](../ciro-santilli-s-hardware-split.md)
4. [Ciro Santilli](../ciro-santilli-split.md)
5. [Ciro Santilli's Homepage](../split.md)
