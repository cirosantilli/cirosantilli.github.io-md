# picotool

↑ **Parent:** [Flash the Raspberry Pi Pico](flash-the-raspberry-pi-pico.md)

[https://github.com/raspberrypi/picotool](https://github.com/raspberrypi/picotool)

Tested on [Ubuntu 25.04](ubuntu-25-04.md), 


```
sudo apt install libusb-1.0-0-dev
git clone https://github.com/raspberrypi/pico-sdk
git clone https://github.com/raspberrypi/picotool
cd picotool
git checkout de8ae5ac334e1126993f72a5c67949712fd1e1a4
export PICO_SDK_PATH="$(pwd)/../pico-sdk"
mkdir build
cd build
cmake ..
cmake --build . -- -j"$(npro)" VERBOSE=1
```
and the executable is there under `build/picotool` so copy it somewhere in your `PATH` like:
```
cp picotool ~/bin
```
and then trying to use a [Zephyr](zephyr-operating-system.md) example:
```
sudo ~/bin/picotool load -f build/zephyr/zephyr.uf2
```
fails with:
```
No accessible RP2040 devices in BOOTSEL mode were found
```
TODO: how to avoid that? [https://youtu.be/tRXLxrtfU_s?t=207](https://youtu.be/tRXLxrtfU_s?t=207) gives a workaround if you are using the Pico SDK by adding to CMakeLists.txt:
```
pico_enable_stdio_usb(blink 1)
```
but how to do it in [Zephyr](zephyr-operating-system.md)? Video description says:

> make sure that your program initializes the USB code via a call to "stdio\_init\_all()".

but again how to do that from [Zephyr](zephyr-operating-system.md)? It appears that this only works if the code currently running has support for the feature:
- [https://forums.raspberrypi.com/viewtopic.php?t=361359](https://forums.raspberrypi.com/viewtopic.php?t=361359)

<a id="video-never-unplug-your-raspberry-pi-pico-again-by-deltocode"></a>
**[Video 23](#video-never-unplug-your-raspberry-pi-pico-again-by-deltocode). Never unplug your Raspberry Pi Pico again by deltocode.** [Source](https://www.youtube.com/watch?v=tRXLxrtfU_s).

## ↑ Ancestors (13)

1. [Flash the Raspberry Pi Pico](flash-the-raspberry-pi-pico.md)
2. [Raspberry Pi Pico getting started](raspberry-pi-pico-getting-started.md)
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
