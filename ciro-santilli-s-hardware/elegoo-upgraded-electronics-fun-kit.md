# ELEGOO Upgraded Electronics Fun Kit

↑ **Parent:** [Electronic components](electronic-components.md)

<a id="_42"></a>
2022-10 ELEGOO Upgraded Electronics Fun Kit [https://www.elegoo.com/products/elegoo-electronics-fun-kits-4-versions](https://www.elegoo.com/products/elegoo-electronics-fun-kits-4-versions) Manuals:

<a id="_43"></a>
<a id="_44"></a>
- [https://www.elegoo.com/blogs/arduino-projects/elegoo-electronic-fun-kit-upgraded-electronic-fun-kit-tutorial](https://www.elegoo.com/blogs/arduino-projects/elegoo-electronic-fun-kit-upgraded-electronic-fun-kit-tutorial)
<a id="_45"></a>
- [http://69.195.111.207/tutorial/ELEGOO/05%20Accessory%20Kit%20Tutorial/09%20Electronic%20Starter%20Kit/E2&E3/Elegoo%20Electronics%20Fun%20Kit(No%20UNO%20Board%20Included)%20V1.0.19.09.10.zip](http://69.195.111.207/tutorial/ELEGOO/05%20Accessory%20Kit%20Tutorial/09%20Electronic%20Starter%20Kit/E2&E3/Elegoo%20Electronics%20Fun%20Kit(No%20UNO%20Board%20Included)%20V1.0.19.09.10.zip)

<a id="_46"></a>
<a id="_47"></a>
- <a id="_48"></a>
  Elegoo [Breadboard](../breadboard.md) power supply module MB‐V2:

  <a id="_49"></a>

  <a id="_50"></a>
  - Input voltage: 6.5-9v (DC) via 5.5mm x 2.1mm plug
  <a id="_51"></a>
  - Output voltage: 3.3V/5v
  <a id="_52"></a>
  - Maximum output current: 700 mA

  <a id="_53"></a>
  TODO center positive or center negative?

  <a id="_54"></a>
  Does not come with [AC adapter](../ac-adapter.md), getting this one: [https://www.amazon.co.uk/dp/B08ZN476FW](https://www.amazon.co.uk/dp/B08ZN476FW) output: DC 9V 1A Power Supply Adapter, Plug 5.5mm x 2.1mm, Center Positive,B rand: Security-01, input: AC 100-240V 50/60 Hz, Cable length: 1.8m

  <a id="_55"></a>
  Parts list from the ZIP:
<a id="_56"></a>
- resistors:<a id="_57"></a>

  <a id="_58"></a>
  - 10x each:<a id="_59"></a>

    <a id="_60"></a>
    - 10
    <a id="_61"></a>
    - 100
    <a id="_62"></a>
    - 330
    <a id="_63"></a>
    - 2k
    <a id="_64"></a>
    - 5.1k
    <a id="_65"></a>
    - 10k
    <a id="_66"></a>
    - 100k
    <a id="_67"></a>
    - 1M
  <a id="_68"></a>
  - 30x 220
<a id="_69"></a>
- 1n4007 General Purpose Rectifier
<a id="_70"></a>
- 22pf 104 Ceramic Capacitor
<a id="_71"></a>
- 4N35 optocoupler
<a id="_72"></a>
- 74HC595 8-bit serial-in, serial or parallel-out shift register with output latches; 3-state
<a id="_73"></a>
- Active buzzer
<a id="_74"></a>
- Buttons
<a id="_75"></a>
- CDS-55 Photoresistor
<a id="_76"></a>
- Electrolytic Capacitor
<a id="_77"></a>
- Focusens MF52D 103f 3950 thermistor. Beta value 25/50 Celcius: 3950. R\_25: I measured 9.61 k Ohms. The number 103 they document as:<a id="_78"></a>

  <a id="_79"></a>
  - digit 1: code of dimension
  <a id="_80"></a>
  - digit 2: rated resistance
  <a id="_81"></a>
  - digit 3: fills with its precision symbol

  These descriptions are weird, but ChatGPT has the theory that the first two digits are actual values, and the last is multiplier, so $10 \times 10^3$ which makes 10k.  
  but I have no idea how that maps to 10 k Ohms.
<a id="_82"></a>
- PN2222 General Purpose Transistor
<a id="_83"></a>
- Passive buzzer
<a id="_84"></a>
- 3386p Bourns Precision Potentiometer - 1 103T: from 0 to 10k Ohms, measured with multimeter. According to the manual the "103" mean 10 k oms, which is consistent with our measurement. "P 103" is etched into the part.
<a id="_85"></a>
- [LEDs](../light-emitting-diode.md):<a id="_86"></a>

  <a id="_87"></a>
  - White LED 10x
  <a id="_88"></a>
  - <a id="_89"></a>
    Kingbright RGB LEDs 10x red, green, yellow, blue:<a id="_90"></a>

    <a id="_91"></a>
    - maximum Continuous Forward Current: 30 mA for read and blue, 25 mA for green
    <a id="_92"></a>
    - 303025
    <a id="_93"></a>
    - under 20 mA<a id="_94"></a>

      <a id="_95"></a>
      - Forward Voltage: 2.0 V typical, 2.5 V max

    <a id="_96"></a>
    20 mA appears to be the typical operation. So with the 2.0 V drop on 5 V power we want a resistor such that:<a id="_97"></a>


    $$
    (5 - 2)/r = 20 \times 10^{-3} \implies r = 150 \Omega
    $$

    <a id="_98"></a>
    for the max 50 mA we would instead have 60 [Ohms](../ohm.md)

## ↑ Ancestors (5)

1. [Electronic components](electronic-components.md)
2. [Mechanical and electrical tools](mechanical-and-electrical-tools.md)
3. [Ciro Santilli's hardware](../ciro-santilli-s-hardware-split.md)
4. [Ciro Santilli](../ciro-santilli-split.md)
5. [Ciro Santilli's Homepage](../split.md)
