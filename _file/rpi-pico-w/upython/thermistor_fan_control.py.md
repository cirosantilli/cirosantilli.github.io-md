<h1 id="_file/rpi-pico-w/upython/thermistor_fan_control.py">rpi-pico-w/upython/thermistor_fan_control.py</h1>

↑ **Parent:** [Raspberry Pi Pico W MicroPython example](../../../raspberry-pi-pico-w-micropython-example.md)  
🏷️ **Tags:** [LED blinker](../../../led-blinker.md)

This example attempts to keep temperature to a fixed point by turning on a fan when a [thermistor](../../../thermistor.md) gets too hot.

You can test it easily if you are not in a place that is too hot by holding the [thermistor](../../../thermistor.md) with your finger to turn on the fan.

You can use a simple [LED](../../../light-emitting-diode.md) to represent the fan if you don't have one handy.

In [Ciro's ASCII art circuit diagram notation](../../../ciro-s-ascii-art-circuit-diagram-notation.md):
```
            +----------FAN-----------+
            |                        |
            |                        |
RPI_PICO_W__gnd__gpio26Adc__3.3V@36__gpio2
            |    |          |
            |    |          |
            |    |          |
            |    +-THERMISTOR
            |    |
            |    |
            R_10-+
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
