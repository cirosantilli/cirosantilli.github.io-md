<h1 id="_file/rpi-pico-w/upython/adc.py">rpi-pico-w/upython/adc.py</h1>

↑ **Parent:** [Raspberry Pi Pico W MicroPython example](../../../raspberry-pi-pico-w-micropython-example.md)  
🏷️ **Tags:** [LED blinker](../../../led-blinker.md)

[rpi-pico-w/upython/adc.py](rpi-pico-w/upython/adc.py): [analog-to-digital converter](../../../analog-to-digital-converter.md).

The program continuously prints to the USB the value of the ADC on GPIO 26 once every 0.2 seconds.

The onboard LED is blinked as a [heartbeat](../../../heartbeat-computing.md).

The hello world is with a [potentiometer](../../../potentiometer.md): extremes on GND and VCC pins of the Pi, and middle output on pin GIO26, then as you turn the knob, the uart value goes from about 0 to about 64k.

The 0 side is quite noisy and varies between 0 and 300 for some reason.

In [Ciro's ASCII art circuit diagram notation](../../../ciro-s-ascii-art-circuit-diagram-notation.md):
```
RPI_PICO_W__gnd__gpio26Adc__3.3V@36
            |    |          |
            |    |          |
            |  +-+          |
            |  |            |
            |  |  +---------+ 
            |  |  |
         P__1__2__3
```

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
