# ELEGOO Upgraded Electronics Fun Kit

↑ **Parent:** [Electronic components](electronic-components.md)

2022-10 ELEGOO Upgraded Electronics Fun Kit [https://www.elegoo.com/products/elegoo-electronics-fun-kits-4-versions](https://www.elegoo.com/products/elegoo-electronics-fun-kits-4-versions) Manuals:

- [https://www.elegoo.com/blogs/arduino-projects/elegoo-electronic-fun-kit-upgraded-electronic-fun-kit-tutorial](https://www.elegoo.com/blogs/arduino-projects/elegoo-electronic-fun-kit-upgraded-electronic-fun-kit-tutorial)
- [http://69.195.111.207/tutorial/ELEGOO/05%20Accessory%20Kit%20Tutorial/09%20Electronic%20Starter%20Kit/E2&E3/Elegoo%20Electronics%20Fun%20Kit(No%20UNO%20Board%20Included)%20V1.0.19.09.10.zip](http://69.195.111.207/tutorial/ELEGOO/05%20Accessory%20Kit%20Tutorial/09%20Electronic%20Starter%20Kit/E2&E3/Elegoo%20Electronics%20Fun%20Kit(No%20UNO%20Board%20Included)%20V1.0.19.09.10.zip)

- Elegoo [Breadboard](../breadboard.md) power supply module MB‐V2:


  - Input voltage: 6.5-9v (DC) via 5.5mm x 2.1mm plug
  - Output voltage: 3.3V/5v
  - Maximum output current: 700 mA

  TODO center positive or center negative?

  Does not come with [AC adapter](../ac-adapter.md), getting this one: [https://www.amazon.co.uk/dp/B08ZN476FW](https://www.amazon.co.uk/dp/B08ZN476FW) output: DC 9V 1A Power Supply Adapter, Plug 5.5mm x 2.1mm, Center Positive,B rand: Security-01, input: AC 100-240V 50/60 Hz, Cable length: 1.8m

  Parts list from the ZIP:
- resistors:
  - 10x each:
    - 10
    - 100
    - 330
    - 2k
    - 5.1k
    - 10k
    - 100k
    - 1M
  - 30x 220
- 1n4007 General Purpose Rectifier
- 22pf 104 Ceramic Capacitor
- 4N35 optocoupler
- 74HC595 8-bit serial-in, serial or parallel-out shift register with output latches; 3-state
- Active buzzer
- Buttons
- CDS-55 Photoresistor
- Electrolytic Capacitor
- Focusens MF52D 103f 3950 thermistor. Beta value 25/50 Celcius: 3950. R\_25: I measured 9.61 k Ohms. The number 103 they document as:
  - digit 1: code of dimension
  - digit 2: rated resistance
  - digit 3: fills with its precision symbol

  These descriptions are weird, but ChatGPT has the theory that the first two digits are actual values, and the last is multiplier, so $10 \times 10^3$ which makes 10k.  
  but I have no idea how that maps to 10 k Ohms.
- PN2222 General Purpose Transistor
- Passive buzzer
- 3386p Bourns Precision Potentiometer - 1 103T: from 0 to 10k Ohms, measured with multimeter. According to the manual the "103" mean 10 k oms, which is consistent with our measurement. "P 103" is etched into the part.
- [LEDs](../light-emitting-diode.md):
  - White LED 10x
  - Kingbright RGB LEDs 10x red, green, yellow, blue:
    - maximum Continuous Forward Current: 30 mA for read and blue, 25 mA for green
    - 303025
    - under 20 mA
      - Forward Voltage: 2.0 V typical, 2.5 V max

    20 mA appears to be the typical operation. So with the 2.0 V drop on 5 V power we want a resistor such that:

    $$
    (5 - 2)/r = 20 \times 10^{-3} \implies r = 150 \Omega
    $$

    for the max 50 mA we would instead have 60 [Ohms](../ohm.md)

## ↑ Ancestors (5)

1. [Electronic components](electronic-components.md)
2. [Mechanical and electrical tools](mechanical-and-electrical-tools.md)
3. [Ciro Santilli's hardware](../ciro-santilli-s-hardware-split.md)
4. [Ciro Santilli](../ciro-santilli-split.md)
5. [Ciro Santilli's Homepage](../split.md)
