# Program the Micro Bit in C

↑ **Parent:** [Program the Micro Bit with X](program-the-micro-bit-with-x.md)  
🏷️ **Tags:** [C (language)](c-programming-language.md)

[https://stackoverflow.com/questions/73877965/how-to-compile-c-c-code-into-a-hex-file-for-the-bbc-microbit](https://stackoverflow.com/questions/73877965/how-to-compile-c-c-code-into-a-hex-file-for-the-bbc-microbit)

Official support is abysmal, very focused on [MicroPython](micropython.md) and their graphical UI.

The setup impossible to achieve as it requires setting up the [Yotta](yotta-build-system.md), just like the impossible to setup [Compile MicroPython code for Micro Bit locally on Ubuntu 22.04 with your own firmware](compile-micropython-code-for-micro-bit-locally-on-ubuntu-22-04-with-your-own-firmware.md) setup.

So we just use [https://github.com/lancaster-university/microbit-samples](https://github.com/lancaster-university/microbit-samples) + [https://github.com/carlosperate/docker-microbit-toolchain](https://github.com/carlosperate/docker-microbit-toolchain):
```
docker pull ghcr.io/carlosperate/microbit-toolchain:latest
git clone https://github.com/lancaster-university/microbit-samples
cd microbit-samples
git checkout 285f9acfb54fce2381339164b6fe5c1a7ebd39d5

# Select a sample, builds one at a time. The default one is the hello world.
cp source/examples/hello-world/* source

# Build and flash.
docker run -v $(pwd):/home --rm ghcr.io/carlosperate/microbit-toolchain:latest yotta build
cp build/bbc-microbit-classic-gcc/source/microbit-samples-combined.hex "/media/$USER/MICROBIT/"
```
.hex file size for the hello world was 447 kB, much better than the [MicroPython](micropython.md) hello world downloaded from the website which was about 1.8 MB!

If you try it again for a second time from a clean tree, it fails with:
```
warning: github rate limit for anonymous requests exceeded: you must log in
```
presumably because after Yotta died it started using GitHub as a registry... sad. When will people learn. Apparently we were at 5000 API calls per hour. But if you don't clean the tree, you will be just fine.

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
