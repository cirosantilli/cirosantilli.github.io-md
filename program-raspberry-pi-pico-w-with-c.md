# Program Raspberry Pi Pico W with C

↑ **Parent:** [Program Raspberry Pi Pico W with X](program-raspberry-pi-pico-w-with-x.md)  
🏷️ **Tags:** [MicroPython](micropython.md)

- [https://www.raspberrypi.com/documentation/microcontrollers/c_sdk.html](https://www.raspberrypi.com/documentation/microcontrollers/c_sdk.html)
- [https://github.com/raspberrypi/pico-sdk](https://github.com/raspberrypi/pico-sdk)
- [https://github.com/raspberrypi/pico-examples](https://github.com/raspberrypi/pico-examples) The key hello world examples are:
  - [https://github.com/raspberrypi/pico-examples/tree/a7ad17156bf60842ee55c8f86cd39e9cd7427c1d/hello_world/usb](https://github.com/raspberrypi/pico-examples/tree/a7ad17156bf60842ee55c8f86cd39e9cd7427c1d/hello_world/usb)
  - [https://github.com/raspberrypi/pico-examples/tree/a7ad17156bf60842ee55c8f86cd39e9cd7427c1d/blink](https://github.com/raspberrypi/pico-examples/tree/a7ad17156bf60842ee55c8f86cd39e9cd7427c1d/blink)

[Ubuntu 22.04](ubuntu-22-04.md) build just worked, nice! Much feels much cleaner than the [Micro Bit](micro-bit.md) C setup:
```
sudo apt install cmake gcc-arm-none-eabi libnewlib-arm-none-eabi libstdc++-arm-none-eabi-newlib

git clone https://github.com/raspberrypi/pico-sdk
cd pico-sdk
git checkout 2e6142b15b8a75c1227dd3edbe839193b2bf9041
cd ..

git clone https://github.com/raspberrypi/pico-examples
cd pico-examples
git checkout a7ad17156bf60842ee55c8f86cd39e9cd7427c1d
cd ..

export PICO_SDK_PATH="$(pwd)/pico-sdk"
cd pico-exampes
mkdir build
cd build
# Board selection.
# https://www.raspberrypi.com/documentation/microcontrollers/c_sdk.html also says you can give wifi ID and password here for W.
cmake -DPICO_BOARD=pico_w ..
make -j
```

Then we install the programs just like any other [UF2](uf2.md) but plugging it in with BOOTSEL pressed and copying the UF2 over, e.g.:
```
cp pico_w/blink/picow_blink.uf2 /media/$USER/RPI-RP2/
```
Note that there is a separate example for the W and non W LED, for non-W it is:
```
cp blink/blink.uf2 /media/$USER/RPI-RP2/
```

Also tested the UART over USB example:
```
cp hello_world/usb/hello_usb.uf2 /media/$USER/RPI-RP2/
```
You can then see the UART messages with:
```
screen /dev/ttyACM0 115200
```

TODO understand the proper debug setup, and a flash setup that doesn't require us to plug out and replug the thing every two seconds. [https://www.electronicshub.org/programming-raspberry-pi-pico-with-swd/](https://www.electronicshub.org/programming-raspberry-pi-pico-with-swd/) appears to describe it, with SWD to do both debug and flash. To do it, you seem need another board with [GPIO](general-purpose-input-output.md), e.g. a [Raspberry Pi](raspberry-pi.md), the laptop alone is not enough.

## ↑ Ancestors (14)

1. [Program Raspberry Pi Pico W with X](program-raspberry-pi-pico-w-with-x.md)
2. [Raspberry Pi Pico W](raspberry-pi-pico-w.md)
3. [Raspberry Pi Pico variant](raspberry-pi-pico-variant.md)
4. [Raspberry Pi Pico](raspberry-pi-pico.md)
5. [Raspberry Pi](raspberry-pi.md)
6. [Raspberry Pi Foundation project](raspberry-pi-foundation-project.md)
7. [Raspberry Pi Foundation](raspberry-pi-foundation.md)
8. [Computer manufacturer](computer-manufacturer.md)
9. [Computer hardware](computer-hardware-split.md)
10. [Computer](computer-split.md)
11. [Information technology](information-technology.md)
12. [Area of technology](area-of-technology.md)
13. [Technology](technology-split.md)
14. [Ciro Santilli's Homepage](split.md)
