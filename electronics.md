# Electronics

↑ **Parent:** [Area of technology](technology.md#area-of-technology)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Electronics)

**Table of contents**

- [Alternating and direct current](#alternating-and-direct-current)
  - [Alternating current](#alternating-current)
    - [Alternating current source](#alternating-current-source)
      - [Signal generator](#signal-generator)
      - [Hippolyte Pixii](#hippolyte-pixii)
        - [Hippolyte Pixiis alternator](#hippolyte-pixiis-alternator)
      - [Inverter](#inverter)
  - [Direct current](#direct-current)
    - [Direct current source](#direct-current-source)
      - [5v vs 3.3V](#5v-vs-3-3v)
      - [AC adapter](#ac-adapter)
        - [Coaxial power connector](#coaxial-power-connector)
        - [Polarity symbols](#polarity-symbols)
        - [Rectifier](#rectifier)
          - [Diode bridge](#diode-bridge)
- [Biasing](#biasing)
- [Circuit diagram](#circuit-diagram)
  - [ASCII art circuit diagram](#ascii-art-circuit-diagram)
    - [Ciro's ASCII art circuit diagram notation](#ciro-s-ascii-art-circuit-diagram-notation)
  - [Electronic symbol](#electronic-symbol)
- [Electronic component](#electronic-component)
  - [Electrical cable](#electrical-cable)
    - [Twisted pair](#twisted-pair)
  - [Current source](#current-source)
  - [Current-voltage characteristic](#current-voltage-characteristic)
  - [Amplifier](#amplifier)
  - [Capacitor](#capacitor)
    - [Leyden jar](#leyden-jar)
      - [Pieter van Musschenbroek](#pieter-van-musschenbroek)
    - [RC circuit](#rc-circuit)
      - [Series RC circuit](#series-rc-circuit)
        - [Step response of the series RC circuit](#step-response-of-the-series-rc-circuit)
    - [Capacitance](#capacitance)
  - [Diode](#diode)
    - [Semiconductor diode](#semiconductor-diode)
      - [Crystal detector](#crystal-detector)
        - [Crystal radio](#crystal-radio)
  - [Electrical connector](#electrical-connector)
    - [Breakout board](#breakout-board)
    - [General-purpose input/output](#general-purpose-input-output)
      - [Pulse width modulation](#pulse-width-modulation)
    - [Jump wire](#jump-wire)
    - [Pin header](#pin-header)
      - [Jumper (computing)](#jumper-computing)
  - [Electronic oscillator](#electronic-oscillator)
    - [Relaxation oscillator](#relaxation-oscillator)
      - [RC oscillator](#rc-oscillator)
        - [555 timer IC](#555-timer-ic)
      - [LC oscillator](#lc-oscillator)
    - [Crystal oscillator](#crystal-oscillator)
  - [Light-emitting diode](#light-emitting-diode)
    - [LED HOWTO](#led-howto)
      - [Calculate resistor needed for an LED](#calculate-resistor-needed-for-an-led)
    - [LED electronic package](#led-electronic-package)
    - [LED spectrum](#led-spectrum)
      - [Are LEDs monochromatic?](#are-leds-monochromatic)
        - [Why aren't LEDs monochromatic](#why-aren-t-leds-monochromatic)
    - [LED vs](#led-vs)
      - [LED vs diode](#led-vs-diode)
      - [LED vs photodetector](#led-vs-photodetector)
  - [Inductor](#inductor)
  - [Multiplexer](#multiplexer)
  - [Resistor](#resistor)
    - [Thermistor](#thermistor)
    - [Potentiometer](#potentiometer)
    - [Electrical resistance and conductance](#electrical-resistance-and-conductance)
      - [Electrical conductance](#electrical-conductance)
      - [Electrical resistance](#electrical-resistance)
        - [Drude model](#drude-model)
          - [Free electron model](#free-electron-model)
        - [Ohm](#ohm)
  - [Transformer](#transformer)
    - [Magnetic core](#magnetic-core)
  - [Electronic switch](#electronic-switch)
    - [Vacuum tube](#vacuum-tube)
    - [Transistor](#transistor)
      - [Point-contact transistor](#point-contact-transistor)
      - [Bipolar junction transistor](#bipolar-junction-transistor)
      - [Field-effect transistor](#field-effect-transistor)
        - [MOSFET](#mosfet)
          - [CMOS](#cmos)
  - [Voltage transformer](#voltage-transformer)
- [Electronic lab equipment](#electronic-lab-equipment)
  - [Arbitrary waveform generator](#arbitrary-waveform-generator)
  - [Electron multiplier](#electron-multiplier)
  - [Power supply](#power-supply)
  - [Electronic test equipment](#electronic-test-equipment)
    - [Oscilloscope](#oscilloscope)
      - [Oscilloscope mode](#oscilloscope-mode)
        - [Oscilloscope XY mode](#oscilloscope-xy-mode)
      - [Digital storage oscilloscope](#digital-storage-oscilloscope)
      - [PC-based oscilloscope](#pc-based-oscilloscope)
      - [Cheap oscilloscope](#cheap-oscilloscope)
      - [Open source oscilloscope](#open-source-oscilloscope)
        - [Haascope](#haascope)
        - [ScopeFun](#scopefun)
        - [ThunderScope](#thunderscope)
- [Electronics vendor](#electronics-vendor)
  - [Hewlett-Packard](#hewlett-packard)
    - [HP spinoff](#hp-spinoff)
      - [Agilent Technologies](#agilent-technologies)
        - [Keysight](#keysight)
        - [Agilent Technologies oscilloscope](#agilent-technologies-oscilloscope)
      - [Hewlett Packard Enterprise](#hewlett-packard-enterprise)
  - [Philips](#philips)
  - [Rohde & Schwarz](#rohde-and-schwarz)
  - [STAR Cryoelectronics](#star-cryoelectronics)
    - [Mr. SQUID](#mr-squid)
- [Electronic circuit](#electronic-circuit)
  - [Circuit board](#circuit-board)
    - [Breadboard](#breadboard)
    - [Printed circuit board](#printed-circuit-board)
      - [Microprocessor development board](#microprocessor-development-board)
        - [Microcontroller devboard](#microcontroller-devboard)
          - [Arduino](#arduino)
          - [Micro Bit](#micro-bit)
            - [Micro Bit simulator](#micro-bit-simulator)
              - [Micro Bit Python editor](#micro-bit-python-editor)
              - [MakeCode Miro Bit](#makecode-miro-bit)
            - [Micro Bit getting started](#micro-bit-getting-started)
            - [Program the Micro Bit with X](#program-the-micro-bit-with-x)
              - [Run Zephyr on Micro Bit](#run-zephyr-on-micro-bit)
              - [Run MicroPython on Micro Bit](#run-micropython-on-micro-bit)
                - [Compile MicroPython code for Micro Bit locally](#compile-micropython-code-for-micro-bit-locally)
                  - [Compile MicroPython code for Micro Bit locally on Ubuntu 22.04 with your own firmware](#compile-micropython-code-for-micro-bit-locally-on-ubuntu-22-04-with-your-own-firmware)
              - [Program the Micro Bit in C](#program-the-micro-bit-in-c)
            - [Yotta (build system)](#yotta-build-system)
            - [Micro Bit version](#micro-bit-version)
              - [Micro Bit v1](#micro-bit-v1)
            - [nRF51 series](#nrf51-series)
            - [Micro Bit example](#micro-bit-example)
            - [Micro Bit GPIO](#micro-bit-gpio)
        - [It is hard to do something useful with a devboard](#it-is-hard-to-do-something-useful-with-a-devboard)
        - [Devboard battery power](#devboard-battery-power)
    - [Point-to-point construction](#point-to-point-construction)
    - [Solder](#solder)
  - [Digital and analog electronics](#digital-and-analog-electronics)
    - [Analog-to-digital converter](#analog-to-digital-converter)
      - [Open source analog-to-digital converter](#open-source-analog-to-digital-converter)
    - [Digital-to-analog converter](#digital-to-analog-converter)
    - [Digital electronics](#digital-electronics)
      - [Digital electronic circuit](#digital-electronic-circuit)
        - [Frequency divider](#frequency-divider)
    - [Analog electronics](#analog-electronics)
  - [LC circuit](#lc-circuit)
    - [An LC circuit is analogous to a spring-mass system](#an-lc-circuit-is-analogous-to-a-spring-mass-system)
    - [Series LC circuit](#series-lc-circuit)
    - [Parallel LC circuit](#parallel-lc-circuit)
    - [Audio feedback](#audio-feedback)
    - [RLC circuit](#rlc-circuit)
- [Heartbeat (computing)](#heartbeat-computing)
- [Semiconductor package](#semiconductor-package)
  - [Dual in-line package](#dual-in-line-package)
- [Electrical engineer](#electrical-engineer)
  - [Oliver Heaviside](#oliver-heaviside)
- [Electronics bibliography](#electronics-bibliography)
  - [Electronics YouTube channel](#electronics-youtube-channel)
    - [CuriousMarc](#curiousmarc)
      - [Marc Verdiell](#marc-verdiell)
        - [LightLogic](#lightlogic)
    - [Marco Reps](#marco-reps)

## Alternating and direct current

↑ **Parent:** [Electronics](electronics.md)

### Alternating current

↑ **Parent:** [Alternating and direct current](#alternating-and-direct-current)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Alternating_current)

#### Alternating current source

↑ **Parent:** [Alternating current](#alternating-current)  
🏷️ **Tags:** [Electronic component](#electronic-component)

##### Signal generator

↑ **Parent:** [Alternating current source](#alternating-current-source)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Signal_generator)

##### Hippolyte Pixii

↑ **Parent:** [Alternating current source](#alternating-current-source)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Hippolyte_Pixii)

###### Hippolyte Pixiis alternator

↑ **Parent:** [Hippolyte Pixii](#hippolyte-pixii)

Operated by a hand crank.

![](https://upload.wikimedia.org/wikipedia/commons/5/56/Wechselstromerzeuger.jpg)

**[Figure 1](#_6)** [Source](https://commons.wikimedia.org/wiki/File:Wechselstromerzeuger.jpg).

##### Inverter

↑ **Parent:** [Alternating current source](#alternating-current-source)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Inverter)

### Direct current

↑ **Parent:** [Alternating and direct current](#alternating-and-direct-current)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Direct_current)

#### Direct current source

↑ **Parent:** [Direct current](#direct-current)  
🏷️ **Tags:** [Electronic component](#electronic-component)

<h5 id="5v-vs-3-3v">5v vs 3.3V</h5>

↑ **Parent:** [Direct current source](#direct-current-source)

- [https://electronics.stackexchange.com/questions/186353/which-is-better-5v-or-3-3v-as-the-supply-voltage#:~:text=3.3V%20has%20a%20lower,ICs%20still%20target%205V%20systems.](https://electronics.stackexchange.com/questions/186353/which-is-better-5v-or-3-3v-as-the-supply-voltage#:~:text=3.3V%20has%20a%20lower,ICs%20still%20target%205V%20systems.)
- [https://forum.arduino.cc/t/5v-vs-3-3v-really-whats-the-difference/648063](https://forum.arduino.cc/t/5v-vs-3-3v-really-whats-the-difference/648063)

##### AC adapter

↑ **Parent:** [Direct current source](#direct-current-source)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/AC_adapter)

![](https://upload.wikimedia.org/wikipedia/commons/thumb/7/7f/Wall-Wart-AC-Adapter.jpg/960px-Wall-Wart-AC-Adapter.jpg)

**[Figure 2](#_15)** [Source](https://commons.wikimedia.org/wiki/File:Wall-Wart-AC-Adapter.jpg).

![](https://upload.wikimedia.org/wikipedia/commons/thumb/2/2d/Notebook-Computer-AC-Adapter.jpg/960px-Notebook-Computer-AC-Adapter.jpg)

**[Figure 3](#_16)** [Source](https://commons.wikimedia.org/wiki/File:Notebook-Computer-AC-Adapter.jpg).

###### Coaxial power connector

↑ **Parent:** [AC adapter](#ac-adapter)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Coaxial_power_connector)

###### Polarity symbols

↑ **Parent:** [AC adapter](#ac-adapter)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Polarity_symbols)

Positive center is way more popular: [https://gearspace.com/board/electronic-music-instruments-and-electronic-music-production/1222518-center-negative-vs-center-positive-power-supply.html](https://gearspace.com/board/electronic-music-instruments-and-electronic-music-production/1222518-center-negative-vs-center-positive-power-supply.html)

![](https://upload.wikimedia.org/wikipedia/commons/thumb/2/2e/Polarity_marking_center_positive.svg/500px-Polarity_marking_center_positive.svg.png)

**[Figure 4](#_18)** [Source](https://commons.wikimedia.org/wiki/File:Polarity_marking_center_positive.svg.png).

![](https://upload.wikimedia.org/wikipedia/commons/thumb/d/d4/Polarity_marking_center_negative.svg/500px-Polarity_marking_center_negative.svg.png)

**[Figure 5](#_19)** [Source](https://commons.wikimedia.org/wiki/File:Polarity_marking_center_negative.svg.png).

###### Rectifier

↑ **Parent:** [AC adapter](#ac-adapter)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Rectifier)

###### Diode bridge

↑ **Parent:** [Rectifier](#rectifier)

## Biasing

↑ **Parent:** [Electronics](electronics.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Biasing)

## Circuit diagram

↑ **Parent:** [Electronics](electronics.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Circuit_diagram)

### ASCII art circuit diagram

↑ **Parent:** [Circuit diagram](#circuit-diagram)  
🏷️ **Tags:** [ASCII art](art.md#ascii-art)

- [https://github.com/Blokkendoos/AACircuit](https://github.com/Blokkendoos/AACircuit)
- [https://hackaday.com/2021/04/29/ascii-schematic-diagrams/](https://hackaday.com/2021/04/29/ascii-schematic-diagrams/)
- [https://www.qsl.net/yo5ofh/hobby%20circuits/ascii.htm](https://www.qsl.net/yo5ofh/hobby%20circuits/ascii.htm)

<h4 id="ciro-s-ascii-art-circuit-diagram-notation">Ciro's ASCII art circuit diagram notation</h4>

↑ **Parent:** [ASCII art circuit diagram](#ascii-art-circuit-diagram)

This notation is designed to be relatively easy to write. This is achieved by not drawing ultra complex ASCII art boxes of every component. It would be slightly more readable if we did that, but prioritizing the writer here.

Two wires are only joined if `+` is given. E.g. the following two wires are not joined:
```
  |
--|--
  |
```
but the following are:
```
  |
--+--
  |
```

Simple symmetric components:
- `-`, `+` and `|`: wire
- `AC`: [AC source](#alternating-current-source). Parameters:
  - `Hz`: frequency
  - `V`: peak voltage

  e.g.:
  ```
  AC_1Hz_2V
  ```

  If only one side is given, the other is assumed to be at a ground `G`.
- `C`: [capacitor](#capacitor)
- `G`: ground. Often used together with `DC`, e.g.:
  ```
  DC_10---R_10---G
  ```

  means applying a voltage of 10 V across a 10 Ohm [resistor](#resistor), which would lead to a current of 1 A
- `L`: [inductor](#inductor)
- `MICROPHONE`. As a multi-letter symmetric component, you can connect the two wires anywhere, e.g.
  ```
  ---MICROPHONE---
  ```

  or:
  ```
  |
  MICROPHONE
      |
  ```
- `SPEAKER`
- `R`: [resistor](#resistor)
- `SQUID`: [SQUID device](condensed-matter-physics.md#squid-device)
- `X`: [Josephson junction](condensed-matter-physics.md#josephson-junction)

Asymmetric components have multiple letters indicating different ports. The capital letter indicates the device, and lower case letters the ports. The wires then go into the ports:
- `D`: [diode](#diode)
  - `a`: anode (where electrons can come in from)
  - `c`: cathode

  Sample usage in a circuit:
  ```
  --aDc--
  ```

  Can also be used vertically like aany other circuit:
  ```
  |
  a
  D
  c
  |
  ```

  We can also change the port order, the device is still the same due to capital `D`:
  ```
  --cDa--

   |
  Dac--

   |
  Dca--

     |
  --caD
  ```
- `DC` [DC source](#direct-current-source). Ports:
  - `p`: positive
  - `n`: negative

  E.g. a 10 V source with a 10 Ohm resistor would be:
  ```
  +---pDC_10_n---+
  |              |
  +----R_10------+
  ```

  If only one side is given, the other is assumed to be at a the ground `G`. We can also omit `p` and `m` in that case and assume that `p` is the one used, e.g. the above would be equivalent to:
  ```
  DC_10---R_10---G
  ```

  If the voltage is not given, it is assumed to be a variable voltage power supply.
- `LED`: same as diode
- `I`: [electric current](electromagnetism.md#electric-current) source. Ports:
  - `s`: electron source
  - `d`: electron destination
- `P`: [potentiometer](#potentiometer) source. Ports:
  - `1`: one of the sides
  - `2`: the middle
  - `3`: the other side
- `T`: [transistor](#transistor). The ports are `sgTd`:
  - `s`: source
  - `g`: gate
  - `d`: gate

  Sample usage in a circuit:
  ```
  ---+
     |
  --sgTd--
  ```

  All the following are also equivalent:
  ```
     |
     g
  --sTd--

      |
  --Tsgd--
     |
  ```
- `V`: [Voltmeter](electromagnetism.md#voltmeter). Ports:
  - `p`: positive
  - `n`: negative
  If we don't need to specify explicit positive and negative sides, we can just use:
  ```
  ---V---
  ```
  without any ports. This is notably often the case for AC circuits.

  Optionally, we can also add the sides as in:
- ports can also be separated by double underscores from the component names to increase readability. Single underscores can also be used to increase readability of longer multi-word component names e.g.:
  ```
  RPI_PICO_W__1gp0__3gnd
              |       |
              R_2k    |
              |       |
              +-aLEDc-+
  ```

  which is the same as:
  ```
  RPI_PICO_W
  1gp0  3gnd
  |       |
  R_2k    |
  |       |
  +-aLEDc-+
  ```

  represents a circuit linking port 1 of a [Raspberry Pi Pico W](computer-hardware.md#raspberry-pi-pico-w), which is GPIO pin 0, through a [resistor](#resistor) and an [LED](#light-emitting-diode), back to pin 3 of the board, which is ground.

Numbers characterizing components are put just next to each component with an underscore. When there is only one parameter, standard units are assumed, e.g.:
```
+-----+
|     |
C_1p  R_2k
|     |
+-----+
```
means:
- a capacitor with 1 pico Faraday
- a resistor with 2 k Ohms
Micro is denoted as `u`.

Wires can just freely come in and out of specs of a component, they are then just connected to the component, e.g.:
```
DC_10---R_10---G
```
means applying a voltage of 10 V across a 10 Ohm [resistor](#resistor), which would lead to a current of 1 A

If a component has more than two parameters, units are used to distinguish them when possible, e.g.:
```
AC_1kV_2MHz
```
means an [AC source](#alternating-current-source) with:
- 1 kV [voltage](electromagnetism.md#voltage)
- 1 MHz frequency

### Electronic symbol

↑ **Parent:** [Circuit diagram](#circuit-diagram)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Electronic_symbol)

## Electronic component

↑ **Parent:** [Electronics](electronics.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Electronic_component)

<a id="video-open-circuits-book-interview-by-curiousmarc-2022"></a>
**[Video 1](#video-open-circuits-book-interview-by-curiousmarc-2022). Open Circuits book interview by CuriousMarc (2022)** [Source](https://www.youtube.com/watch?v=byKyJ0b04Lo).

### Electrical cable

↑ **Parent:** [Electronic component](#electronic-component)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Electrical_cable)

One more more electrical wires surrounded by an insulator.

#### Twisted pair

↑ **Parent:** [Electrical cable](#electrical-cable)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Twisted_pair)

**[Video 2](#_103)** [Source](https://commons.wikimedia.org/wiki/File:CAT5e_Cable.jpg). [Cat 5e cable](computer.md#cat-5e) stripped

### Current source

↑ **Parent:** [Electronic component](#electronic-component)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Current_source)

### Current-voltage characteristic

↑ **Parent:** [Electronic component](#electronic-component)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Current-voltage_characteristic)

### Amplifier

↑ **Parent:** [Electronic component](#electronic-component)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Amplifier)

Main implementations: the same as [electronic switches](#electronic-switch): [vacuum tubes](#vacuum-tube) in the past, and [transistors](#transistor) in the second half of the 20th century.

<a id="video-how-to-make-an-lm386-audio-amplifier-circuit-by-afrotechmods-2017"></a>
**[Video 3](#video-how-to-make-an-lm386-audio-amplifier-circuit-by-afrotechmods-2017). How to make an LM386 audio amplifier circuit by Afrotechmods (2017)** [Source](https://www.youtube.com/watch?v=4ObzEft2R_g). Builds the circuit on a [breadboard](#breadboard) from minimal components, including one discrete [transistor](#transistor). Then plays music from phone through headset cables into a [speaker](telecommunication.md#loudspeaker).

### Capacitor

↑ **Parent:** [Electronic component](#electronic-component)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Capacitor)

The fundamental intuition about capacitors is that they never let [electrons](standard-model.md#electron) through.

They can only absorb [electrons](standard-model.md#electron) up to a certain point, but then the pushback becomes too strong, and current stops.

Therefore, they cannot conduct [direct current](#direct-current) long term.

For [alternating current](#alternating-current) however, things are different, because in alternating current, [electrons](standard-model.md#electron) are just jiggling back and forward a little bit around a center point. So you can send alternating current power across a capacitor.

The key equation that relates [Voltage](electromagnetism.md#voltage) to [electric current](electromagnetism.md#electric-current) in the [capacitor](#capacitor) is:

$$
I(t) = C \dv{V(t)}{t}
$$

So if a voltage [Heavyside step function](formalization-of-mathematics.md#heavyside-step-function) is applied what happens is:
- the capacitor fills up instantly with an infinite current
- the current then stops instantly
More realistically, one may consider the behavior or the [series RC circuit](#series-rc-circuit) to see what happens without infinities when a capacitor is involved as in the [step response of the series RC circuit](#step-response-of-the-series-rc-circuit).

<a id="image-electronic-symbol-of-a-capacitor"></a>
![](https://upload.wikimedia.org/wikipedia/commons/7/73/IEEE_315_Fundamental_Items_Symbols_%2832%29.svg)

**[Figure 6](#image-electronic-symbol-of-a-capacitor). Electronic symbol of a capacitor**. [Source](https://commons.wikimedia.org/wiki/File:IEEE_315_Fundamental_Items_Symbols_%2832%29.svg).

<a id="video-finding-capacitance-with-an-oscilloscope-by-jacob-watts-2020"></a>
**[Video 4](#video-finding-capacitance-with-an-oscilloscope-by-jacob-watts-2020). Finding capacitance with an oscilloscope by Jacob Watts (2020)** [Source](https://www.youtube.com/watch?v=4PkcOeZCE0g). Good experiment.

<a id="video-capacitors-explained-by-the-engineering-mindset"></a>
**[Video 5](#video-capacitors-explained-by-the-engineering-mindset). Capacitors Explained by The Engineering Mindset.** [Source](https://www.youtube.com/watch?v=X4EUwTwZ110). 2019.

#### Leyden jar

↑ **Parent:** [Capacitor](#capacitor)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Leyden_jar)

[Pieter van Musschenbroek](#pieter-van-musschenbroek) is the perfect example that if your surname is too complicated, things you invent will not be named after you!

![](https://upload.wikimedia.org/wikipedia/commons/1/15/Andreas_Cunaeus_discovering_the_Leyden_jar.png)

**[Figure 7](#_116)** [Source](https://commons.wikimedia.org/wiki/File:Andreas_Cunaeus_discovering_the_Leyden_jar.png).

##### Pieter van Musschenbroek

↑ **Parent:** [Leyden jar](#leyden-jar)  
🏷️ **Tags:** [Physicist](physicist.md)

#### RC circuit

↑ **Parent:** [Capacitor](#capacitor)  
🏷️ **Tags:** [Electronic circuit](#electronic-circuit)

##### Series RC circuit

↑ **Parent:** [RC circuit](#rc-circuit)

![](https://upload.wikimedia.org/wikipedia/commons/thumb/e/e0/RC_Series_Filter_%28with_V%26I_Labels%29.svg/250px-RC_Series_Filter_%28with_V%26I_Labels%29.svg.png)

**[Figure 8](#_119)** [Source](https://commons.wikimedia.org/wiki/File:RC_Series_Filter_%28with_V%26I_Labels%29.svg.png).

###### Step response of the series RC circuit

↑ **Parent:** [Series RC circuit](#series-rc-circuit)

This is what happens when you apply a step [voltage](electromagnetism.md#voltage) to a [series RC circuit](#series-rc-circuit): TODO $I(t)$ graph.

#### Capacitance

↑ **Parent:** [Capacitor](#capacitor)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Capacitance)

### Diode

↑ **Parent:** [Electronic component](#electronic-component)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Diode)

Ideally can be thought of as a one-way ticket gate that only lets electrons go in one direction with zero resistance! Real devices do have imperfections however, so there is some resistance.

First they were made out of [vacuum tubes](#vacuum-tube), but later [semiconductor diodes](#semiconductor-diode) were invented and became much more widespread.

#### Semiconductor diode

↑ **Parent:** [Diode](#diode)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Diode#Semiconductor_diodes)

<a id="image-i-v-curve-of-a-diode"></a>
![](https://upload.wikimedia.org/wikipedia/commons/2/2a/Diode_current_wiki.png)

**[Figure 9](#image-i-v-curve-of-a-diode). I-V curve of a diode**. [Source](https://commons.wikimedia.org/wiki/File:Diode_current_wiki.png). This image shows well how the diode is only an approximation of the ideal one way device. Notably, there is this $V_d$ non-ideal voltage drop across the device, which can be modelled as constant. It is however an exponential in fact.

<a id="video-diodes-explained-by-the-engineering-mindset-2020"></a>
**[Video 6](#video-diodes-explained-by-the-engineering-mindset-2020). Diodes Explained by The Engineering Mindset (2020)** [Source](https://www.youtube.com/watch?v=Fwj_d3uO5g8). Good video:
- [https://youtu.be/Fwj_d3uO5g8?t=153](https://youtu.be/Fwj_d3uO5g8?t=153) how it works
- [https://youtu.be/Fwj_d3uO5g8?t=514](https://youtu.be/Fwj_d3uO5g8?t=514) applications:
  - protection against accidental battery inversion
  - [rectifiers](#rectifier), notably mentions a [diode bridge](#diode-bridge)

---

##### Crystal detector

↑ **Parent:** [Semiconductor diode](#semiconductor-diode)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Crystal_detector)

The first [diodes](#diode). These were apparently incredibly unreliable, especially for portable radios, as you had to randomly search for the best contact point you could find in a random polycrystalline material!!

And also quality was highly dependant on where the material was sourced from as that affected the impurities present in the material. Later this was understood to be an issue of [doping](condensed-matter-physics.md#doping-semiconductor).

It was so unreliable that [vacuum tube](#vacuum-tube) diodes overtook them in many applications, even though [crystal detectors](#crystal-detector) are actually [semiconductor diodes](#semiconductor-diode), which eventually won over!

For a long time, before artificial [semiconductors](condensed-matter-physics.md#semiconductor) kicked in, people just didn't know the underlying physical working principle of these detectors. [What I cannot create, I do not understand](what-i-cannot-create-i-do-not-understand.md) basically.

###### Crystal radio

↑ **Parent:** [Crystal detector](#crystal-detector)  
🏷️ **Tags:** [Radio receiver](telecommunication.md#radio-receiver)

This was the first generation of commercially successful radios.

It uses a [crystal detector](#crystal-detector) as its [diode](#diode), which is a crucial element of the radio, thus its name.

They were superseded by [transistor radios](https://ourbigbook.com/go/topic/transistor-radios), which were much more reliable, portable and could amplify the signal received.

![](https://upload.wikimedia.org/wikipedia/commons/3/3b/Kristallradio.JPG)

**[Figure 10](#_137)** [Source](https://commons.wikimedia.org/wiki/File:Kristallradio.JPG).

<a id="video-how-a-crystal-radio-works-by-rimstarorg"></a>
**[Video 7](#video-how-a-crystal-radio-works-by-rimstarorg). How a Crystal radio Works by RimstarOrg.** [Source](https://www.youtube.com/watch?v=0-PParSmwtE).

### Electrical connector

↑ **Parent:** [Electronic component](#electronic-component)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Electrical_connector)

#### Breakout board

↑ **Parent:** [Electrical connector](#electrical-connector)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Breakout_board)

<h4 id="general-purpose-input-output">General-purpose input/output</h4>

↑ **Parent:** [Electrical connector](#electrical-connector)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/General-purpose_input/output)

##### Pulse width modulation

↑ **Parent:** [General-purpose input/output](#general-purpose-input-output)

GPIO generally only supports discrete outputs.

But for some types of hardware, like LEDs and some motors, the system has some inertia, and if you switch on and off fast enough, you get a result similar to having an intermediate voltage.

So with pulse width modulation we can fake [analog](#analog-electronics) output from digital output in a good enough manner.

#### Jump wire

↑ **Parent:** [Electrical connector](#electrical-connector)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Jump_wire)

Notably used to connect:
- [pin headers](#pin-header)
- [breadboard](#breadboard) holes

You can buy large sets of them in combitation of male/male, male/female, female/female. Male/male is perhaps the most important

<a id="video-making-jumper-wires-by-pcburn-2018"></a>
**[Video 8](#video-making-jumper-wires-by-pcburn-2018). Making Jumper Wires by PCBurn! (2018)** [Source](https://www.youtube.com/watch?v=o53uveSmJR0).

#### Pin header

↑ **Parent:** [Electrical connector](#electrical-connector)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Pin_header)

These often come pre-soldered on [devboards](#microprocessor-development-board), e.g. and allow for easy access to [GPIO](#general-purpose-input-output) pins. E.g. they're present on the [Raspberry Pi 2](computer-hardware.md#raspberry-pi-2).

Why would someone ever sell a devboard without them pre-soldered!

<a id="image-6x1-pin-header"></a>
![](https://upload.wikimedia.org/wikipedia/commons/b/bf/6_Pin_Header.jpg)

**[Figure 11](#image-6x1-pin-header). 6x1 pin header**. [Source](https://commons.wikimedia.org/wiki/File:6_Pin_Header.jpg).

<a id="image-underside-of-a-raspberry-pi-2"></a>
![](https://upload.wikimedia.org/wikipedia/commons/thumb/2/2e/Raspberry_Pi_2_Model_B_v1.1_underside_new_%28bg_cut_out%29.jpg/500px-Raspberry_Pi_2_Model_B_v1.1_underside_new_%28bg_cut_out%29.jpg)

**[Figure 12](#image-underside-of-a-raspberry-pi-2). Underside of a Raspberry Pi 2**. [Source](https://commons.wikimedia.org/wiki/File:Raspberry_Pi_2_Model_B_v1.1_underside_new_%28bg_cut_out%29.jpg). At the top of this image we can clearly see how the usually pre-soldered [pin header](#pin-header) connectors go through the [PCB](#printed-circuit-board) and are soldered on both sides.

##### Jumper (computing)

↑ **Parent:** [Pin header](#pin-header)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Jumper_(computing))

Allows you to connect two adjacent pins of a [pin header](#pin-header). Sometimes used as a hardware configuration interface!

![](https://upload.wikimedia.org/wikipedia/commons/b/b0/Jumper_on_motherboard.jpg)

**[Figure 13](#_150)** [Source](https://commons.wikimedia.org/wiki/File:Jumper_on_motherboard.jpg).

### Electronic oscillator

↑ **Parent:** [Electronic component](#electronic-component)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Electronic_oscillator)

Something where [DC voltage](#direct-current) comes in, and a periodic voltage comes out.

<a id="video-oscillators-rc-lc-crystal-by-greatscott-2015"></a>
**[Video 9](#video-oscillators-rc-lc-crystal-by-greatscott-2015). Oscillators: RC, LC, Crystal by GreatScott! (2015)** [Source](https://www.youtube.com/watch?v=eYVOdlK15Og). Good video. Contains actual [breadboard](#breadboard) experiments on [oscilloscope](#oscilloscope) and circuit diagrams
- [https://youtu.be/eYVOdlK15Og?t=66](https://youtu.be/eYVOdlK15Og?t=66) [RC oscillator](#rc-oscillator) on [breadboard](#breadboard). Produces [rectangular wave](formalization-of-mathematics.md#rectangular-wave). Mentions popular [integrated circuit](computer-hardware.md#integrated-circuit) that does it: [555 timer IC](#555-timer-ic).
- [https://youtu.be/eYVOdlK15Og?t=175](https://youtu.be/eYVOdlK15Og?t=175) [LC oscillators](#lc-oscillator) allows for higher frequencies. Produces [sinusoidal](calculus.md#sinusoidal) output on [MHz](system-of-units.md#megahertz) range. Uses an amplifier to feed back into input and maintain same voltage. Hard to make reliably on breadboard.
- [https://youtu.be/eYVOdlK15Og?t=315](https://youtu.be/eYVOdlK15Og?t=315) [crystal oscillator](#crystal-oscillator). Mentions it acts like an [LC oscillators](#lc-oscillator). Shows and equivalent model. Wish he had talked more about them. You need support components around it: similarly to the LC case, the amplifier is generally not packaged in.

---

#### Relaxation oscillator

↑ **Parent:** [Electronic oscillator](#electronic-oscillator)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Relaxation_oscillator)

##### RC oscillator

↑ **Parent:** [Relaxation oscillator](#relaxation-oscillator)

First watch: [Video 9. "Oscillators: RC, LC, Crystal by GreatScott! (2015)"](#video-oscillators-rc-lc-crystal-by-greatscott-2015)

###### 555 timer IC

↑ **Parent:** [RC oscillator](#rc-oscillator)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/555_timer_IC)

##### LC oscillator

↑ **Parent:** [Relaxation oscillator](#relaxation-oscillator)

Oscillator made of an [LC circuit](#lc-circuit).

First watch: [Video 9. "Oscillators: RC, LC, Crystal by GreatScott! (2015)"](#video-oscillators-rc-lc-crystal-by-greatscott-2015)

#### Crystal oscillator

↑ **Parent:** [Electronic oscillator](#electronic-oscillator)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Crystal_oscillator)

First watch: [Video 9. "Oscillators: RC, LC, Crystal by GreatScott! (2015)"](#video-oscillators-rc-lc-crystal-by-greatscott-2015)

<a id="video-from-raw-crystal-to-crystal-oscillator"></a>
**[Video 10](#video-from-raw-crystal-to-crystal-oscillator). From Raw Crystal to Crystal oscillator.** [Source](https://www.youtube.com/watch?v=duZlWWwxIPQ). by United States Army Signal Corps (1943)

### Light-emitting diode

↑ **Parent:** [Electronic component](#electronic-component)  
🏷️ **Tags:** [Light source](photon.md#light-source)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Light-emitting_diode)

<a id="video-how-leds-work-by-virtualbrain"></a>
**[Video 11](#video-how-leds-work-by-virtualbrain). How LEDs work by VirtualBrain.** [Source](https://www.youtube.com/watch?v=9BDTtcRMxpA). 2021. Good 3d schematics clearly explaining part of the [LED electronic package](#led-electronic-package).

#### LED HOWTO

↑ **Parent:** [Light-emitting diode](#light-emitting-diode)

##### Calculate resistor needed for an LED

↑ **Parent:** [LED HOWTO](#led-howto)

[https://electronics.stackexchange.com/questions/492867/calculating-the-resistor-needed-for-a-simple-led-and-battery-circuit](https://electronics.stackexchange.com/questions/492867/calculating-the-resistor-needed-for-a-simple-led-and-battery-circuit)

#### LED electronic package

↑ **Parent:** [Light-emitting diode](#light-emitting-diode)

[https://electronics.stackexchange.com/questions/93858/reason-for-anvil-and-post-in-leds](https://electronics.stackexchange.com/questions/93858/reason-for-anvil-and-post-in-leds)

<a id="video-how-are-led-chips-and-led-encapsulation-is-made-by-future-linear"></a>
**[Video 12](#video-how-are-led-chips-and-led-encapsulation-is-made-by-future-linear). How are LED Chips and LED Encapsulation is made by Future Linear.** [Source](https://www.youtube.com/watch?v=EvAFRB4E68Q). Starts from some level of cut square chips. Still in round wafer form.

#### LED spectrum

↑ **Parent:** [Light-emitting diode](#light-emitting-diode)

[https://electronics.stackexchange.com/questions/477264/spectrum-of-leds](https://electronics.stackexchange.com/questions/477264/spectrum-of-leds)

##### Are LEDs monochromatic?

↑ **Parent:** [LED spectrum](#led-spectrum)

[https://electronics.stackexchange.com/questions/477264/spectrum-of-leds](https://electronics.stackexchange.com/questions/477264/spectrum-of-leds)

<h6 id="why-aren-t-leds-monochromatic">Why aren't LEDs monochromatic</h6>

↑ **Parent:** [Are LEDs monochromatic?](#are-leds-monochromatic)

[https://www.reddit.com/r/Optics/comments/18f6bdt/comment/kcsiook/](https://www.reddit.com/r/Optics/comments/18f6bdt/comment/kcsiook/) mentions:

> LEDs are broadband by nature, since the spontaneous emission broadly speaking reflects the overlap of the Fermi distribution and the density of states

#### LED vs

↑ **Parent:** [Light-emitting diode](#light-emitting-diode)

##### LED vs diode

↑ **Parent:** [LED vs](#led-vs)

[Direct and indirect band gaps](condensed-matter-physics.md#direct-and-indirect-band-gaps) is an important part of why [diodes](#diode) don't emit light apparently.

Bibliography:
- [https://www.quora.com/What-is-the-difference-between-an-LED-and-a-diode](https://www.quora.com/What-is-the-difference-between-an-LED-and-a-diode)
- [https://youtu.be/9BDTtcRMxpA?t=388](https://youtu.be/9BDTtcRMxpA?t=388) from [Video 11. "How LEDs work by VirtualBrain"](#video-how-leds-work-by-virtualbrain) explains the geometry aspect well

##### LED vs photodetector

↑ **Parent:** [LED vs](#led-vs)  
🏷️ **Tags:** [Photodetector](photon.md#photodetector)

[https://electronics.stackexchange.com/questions/548353/can-led-strips-be-used-as-photodetectors](https://electronics.stackexchange.com/questions/548353/can-led-strips-be-used-as-photodetectors)

Apparently fundamentally LEDs in principle work as [photodetectors](https://ourbigbook.com/go/topic/photodetectors), but 

### Inductor

↑ **Parent:** [Electronic component](#electronic-component)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Inductor)

It resists to change in [electric current](electromagnetism.md#electric-current). Well seen at: [Video 27. "LC circuit by Eugene Khutoryansky (2016)"](#video-lc-circuit-by-eugene-khutoryansky-2016).

### Multiplexer

↑ **Parent:** [Electronic component](#electronic-component)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Multiplexer)

### Resistor

↑ **Parent:** [Electronic component](#electronic-component)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Resistor)

#### Thermistor

↑ **Parent:** [Resistor](#resistor)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Thermistor)

![](https://upload.wikimedia.org/wikipedia/commons/3/3b/NTC_bead.jpg)

**[Figure 14](#_177)** [Source](https://commons.wikimedia.org/wiki/File:NTC_bead.jpg).

#### Potentiometer

↑ **Parent:** [Resistor](#resistor)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Potentiometer)

Variable [resistance](#electrical-resistance) element.

![](https://upload.wikimedia.org/wikipedia/commons/0/0a/Electronic-Component-Potentiometer.jpg)

**[Figure 15](#_179)** [Source](https://commons.wikimedia.org/wiki/File:Electronic-Component-Potentiometer.jpg).

![](https://upload.wikimedia.org/wikipedia/commons/1/19/Potentiometer_symbol.svg)

**[Figure 16](#_180)** [Source](https://commons.wikimedia.org/wiki/File:Potentiometer_symbol.svg).

#### Electrical resistance and conductance

↑ **Parent:** [Resistor](#resistor)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Electrical_resistance_and_conductance)

##### Electrical conductance

↑ **Parent:** [Electrical resistance and conductance](#electrical-resistance-and-conductance)

##### Electrical resistance

↑ **Parent:** [Electrical resistance and conductance](#electrical-resistance-and-conductance)

###### Drude model

↑ **Parent:** [Electrical resistance](#electrical-resistance)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Drude_model)

###### Free electron model

↑ **Parent:** [Drude model](#drude-model)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Free_electron_model)

###### Ohm

↑ **Parent:** [Electrical resistance](#electrical-resistance)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Ohm)

### Transformer

↑ **Parent:** [Electronic component](#electronic-component)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Transformer)

#### Magnetic core

↑ **Parent:** [Transformer](#transformer)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Magnetic_core)

<a id="image-hand-drawn-schematic-of-the-magnetic-field-induced-in-a-magnetic-core-by-an-electromagnetic-coil"></a>
![](https://upload.wikimedia.org/wikipedia/commons/thumb/d/d0/Electromagnet_with_gap.svg/500px-Electromagnet_with_gap.svg.png)

**[Figure 17](#image-hand-drawn-schematic-of-the-magnetic-field-induced-in-a-magnetic-core-by-an-electromagnetic-coil). Hand drawn schematic of the magnetic field induced in a magnetic core by an electromagnetic coil**. [Source](https://commons.wikimedia.org/wiki/File:Electromagnet_with_gap.svg.png).

### Electronic switch

↑ **Parent:** [Electronic component](#electronic-component)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Electronic_switch)

#### Vacuum tube

↑ **Parent:** [Electronic switch](#electronic-switch)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Vacuum_tube)

#### Transistor

↑ **Parent:** [Electronic switch](#electronic-switch)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Transistor)

A [solid-state](condensed-matter-physics.md#solid-state-physics) [electronic switch](#electronic-switch) and [amplifier](#amplifier).

Although transistors were revolutionary, it is fun to note that they were just "way cheaper and more reliable and smaller" versions of exactly the main functions that a [vacuum tube](#vacuum-tube) could achieve
- [amplifier](#amplifier)
- [electronic switch](#electronic-switch)

##### Point-contact transistor

↑ **Parent:** [Transistor](#transistor)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Point-contact_transistor)

The first working one in 1947 by [John Bardeen](physicist.md#john-bardeen) and [walter Brattain](physicist.md#walter-houser-brattain) in [Bell Labs Murray Hill](research-institute.md#bell-labs-murray-hill).

People had already [patented](law.md#patent) a lot of stuff before without being able to make them work. Nonsense.

As the name suggests, this is not very sturdy, and was quickly replaced by [bipolar junction transistor](#bipolar-junction-transistor).

##### Bipolar junction transistor

↑ **Parent:** [Transistor](#transistor)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Bipolar_junction_transistor)

By [William Shockley](physicist.md#william-shockley) in 1948 also at [Bell Labs Murray Hill](research-institute.md#bell-labs-murray-hill).

As of 2020, not used anymore in [logic gates](computer-hardware.md#logic-gate), but still used in [amplifiers](#amplifier).

![](https://upload.wikimedia.org/wikipedia/commons/6/6b/NPN_BJT_%28Planar%29_Cross-section.svg)

**[Figure 18](#_195)** [Source](https://commons.wikimedia.org/wiki/File:NPN_BJT_%28Planar%29_Cross-section.svg).

##### Field-effect transistor

↑ **Parent:** [Transistor](#transistor)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Field-effect_transistor)

![](https://upload.wikimedia.org/wikipedia/commons/4/44/FET_cross_section.svg)

**[Figure 19](#_197)** [Source](https://commons.wikimedia.org/wiki/File:FET_cross_section.svg).

###### MOSFET

↑ **Parent:** [Field-effect transistor](#field-effect-transistor)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/MOSFET)

![](https://upload.wikimedia.org/wikipedia/commons/4/44/FET_cross_section.svg)

**[Figure 20](#_199)** [Source](https://commons.wikimedia.org/wiki/File:FET_cross_section.svg).

###### CMOS

↑ **Parent:** [MOSFET](#mosfet)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/CMOS)

### Voltage transformer

↑ **Parent:** [Electronic component](#electronic-component)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Voltage_transformer)

## Electronic lab equipment

↑ **Parent:** [Electronics](electronics.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Electronic_lab_equipment)

<a id="video-a-perfect-electronics-bench-by-keysight-2021"></a>
**[Video 13](#video-a-perfect-electronics-bench-by-keysight-2021). A Perfect Electronics Bench? by Keysight (2021)** [Source](https://www.youtube.com/watch?v=l7OOnv8_m0c).

### Arbitrary waveform generator

↑ **Parent:** [Electronic lab equipment](#electronic-lab-equipment)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Arbitrary_waveform_generator)

### Electron multiplier

↑ **Parent:** [Electronic lab equipment](#electronic-lab-equipment)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Electron_multiplier)

### Power supply

↑ **Parent:** [Electronic lab equipment](#electronic-lab-equipment)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Power_supply)

### Electronic test equipment

↑ **Parent:** [Electronic lab equipment](#electronic-lab-equipment)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Electronic_test_equipment)

#### Oscilloscope

↑ **Parent:** [Electronic test equipment](#electronic-test-equipment)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Oscilloscope)

<a id="video-fnirsi-1014d-review-by-kerry-wong-2022"></a>
**[Video 14](#video-fnirsi-1014d-review-by-kerry-wong-2022). FNIRSI 1014D review by Kerry Wong (2022)** [Source](https://www.youtube.com/watch?v=yQKuHJELEOs). One of the cheapest oscilloscopes available at the time.

##### Oscilloscope mode

↑ **Parent:** [Oscilloscope](#oscilloscope)

###### Oscilloscope XY mode

↑ **Parent:** [Oscilloscope mode](#oscilloscope-mode)

##### Digital storage oscilloscope

↑ **Parent:** [Oscilloscope](#oscilloscope)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Digital_storage_oscilloscope)

##### PC-based oscilloscope

↑ **Parent:** [Oscilloscope](#oscilloscope)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/PC-based_oscilloscope)

##### Cheap oscilloscope

↑ **Parent:** [Oscilloscope](#oscilloscope)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Cheap_oscilloscope)

- [https://www.reddit.com/r/ECE/comments/jqfv4f/what_is_the_cheapest_oscilloscope_available_and/](https://www.reddit.com/r/ECE/comments/jqfv4f/what_is_the_cheapest_oscilloscope_available_and/)

<a id="video-diy-oscilloscope-kit-20-vs-regular-ds-oscilloscope-400-by-great-scott-2016"></a>
**[Video 15](#video-diy-oscilloscope-kit-20-vs-regular-ds-oscilloscope-400-by-great-scott-2016). DIY Oscilloscope Kit (20$) VS Regular DS Oscilloscope (400$) by Great Scott (2016)** [Source](https://www.youtube.com/watch?v=x19kwG-wJRI).

<a id="video-hantek-6022be-review-by-adrian-s-digital-basement-2022"></a>
**[Video 16](#video-hantek-6022be-review-by-adrian-s-digital-basement-2022). Hantek 6022BE Review by Adrian's Digital Basement (2022)** [Source](https://www.youtube.com/watch?v=8ts5J09Y7Gc).

##### Open source oscilloscope

↑ **Parent:** [Oscilloscope](#oscilloscope)  
🏷️ **Tags:** [Open source hardware](software.md#open-source-hardware)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Open_source_oscilloscope)

###### Haascope

↑ **Parent:** [Open source oscilloscope](#open-source-oscilloscope)

[https://www.crowdsupply.com/andy-haas/haasoscope](https://www.crowdsupply.com/andy-haas/haasoscope)

By Andy Haas, an experimental [particle physics](particle-physics.md) professor: [https://as.nyu.edu/content/nyu-as/as/faculty/andy-haas.html](https://as.nyu.edu/content/nyu-as/as/faculty/andy-haas.html) What an awesome dude!

<a id="video-haasoscope-prototype-2-4-channel-boards"></a>
**[Video 17](#video-haasoscope-prototype-2-4-channel-boards). Haasoscope prototype, 2 4-channel boards.** [Source](https://www.youtube.com/watch?v=tDUg0Q3wInE).

###### ScopeFun

↑ **Parent:** [Open source oscilloscope](#open-source-oscilloscope)

- [https://www.scopefun.com/](https://www.scopefun.com/)

899 USD as of 2022, takes a year to ship as they gather up a lot of orders before producing.

Sounds so cool, especially the multi functionality. Shame so expensive.

###### ThunderScope

↑ **Parent:** [Open source oscilloscope](#open-source-oscilloscope)

- [https://github.com/EEVengers/ThunderScope](https://github.com/EEVengers/ThunderScope)
- [https://www.crowdsupply.com/eevengers/thunderscope](https://www.crowdsupply.com/eevengers/thunderscope)

<a id="video-thunderscope-presentation-for-hackaday-prize-2021"></a>
**[Video 18](#video-thunderscope-presentation-for-hackaday-prize-2021). ThunderScope presentation for Hackaday Prize (2021)** [Source](https://www.youtube.com/watch?v=TIc-xa1BUYk).

## Electronics vendor

↑ **Parent:** [Electronics](electronics.md)  
🏷️ **Tags:** [Company](company.md)

### Hewlett-Packard

↑ **Parent:** [Electronics vendor](#electronics-vendor)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Hewlett-Packard)

They do seem to have been very innovative, and have had a very good work culture. They also had a huge impact on the [Silicon Valley](united-states.md#silicon-valley) startup scene.

Some products they are known for:
- oscilloscopes
- [Atomic clocks](system-of-units.md#atomic-clock), notably highly portable ones, see e.g. [Video "Inside the HP 5061A Cesium Clock by CuriousMarc (2020)"](system-of-units.md#video-inside-the-hp-5061a-cesium-clock-by-curiousmarc-2020)
- pocket calculator

<a id="video-the-decline-of-hp-by-company-man-2022"></a>
**[Video 19](#video-the-decline-of-hp-by-company-man-2022). The decline of HP by Company Man (2022)** [Source](https://www.youtube.com/watch?v=ppqC0tNghSk).

<a id="video-hp-origins-promotional-documentary-by-hp-2006"></a>
**[Video 20](#video-hp-origins-promotional-documentary-by-hp-2006). HP Origins promotional documentary by HP (2006)** [Source](https://www.youtube.com/watch?v=Iqv6DhtLay4). A bit too star eyed, but gives some good ideas.

#### HP spinoff

↑ **Parent:** [Hewlett-Packard](#hewlett-packard)

##### Agilent Technologies

↑ **Parent:** [HP spinoff](#hp-spinoff)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Agilent_Technologies)

In a way, Agilent represents the most grassroots electronics parts of [HP](#hewlett-packard) from before they became overly invested in laptops and fell.

They spun out the electronics part as [Keysight](#keysight) in 2014, becoming life science only.

###### Keysight

↑ **Parent:** [Agilent Technologies](#agilent-technologies)  
🏷️ **Tags:** [Electronics vendor](#electronics-vendor)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Keysight)

###### Agilent Technologies oscilloscope

↑ **Parent:** [Agilent Technologies](#agilent-technologies)

##### Hewlett Packard Enterprise

↑ **Parent:** [HP spinoff](#hp-spinoff)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Hewlett_Packard_Enterprise)

### Philips

↑ **Parent:** [Electronics vendor](#electronics-vendor)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Philips)

<h3 id="rohde-and-schwarz">Rohde &amp; Schwarz</h3>

↑ **Parent:** [Electronics vendor](#electronics-vendor)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Rohde_&_Schwarz)

### STAR Cryoelectronics

↑ **Parent:** [Electronics vendor](#electronics-vendor)

[https://starcryo.com/](https://starcryo.com/)

#### Mr. SQUID

↑ **Parent:** [STAR Cryoelectronics](#star-cryoelectronics)  
🏷️ **Tags:** [SQUID device](condensed-matter-physics.md#squid-device)

[https://starcryo.com/mr-squid/](https://starcryo.com/mr-squid/)

This is the cutest product name ever.

> Since 1992, Mr. SQUID has been the standard educational demonstration system for undergraduate physics lab courses.

Used e.g. at [Video "Superconducting Quantum Interference Devices by UNSW Physics (2020)"](condensed-matter-physics.md#video-superconducting-quantum-interference-devices-by-unsw-physics-2020)

Their manual: [https://www.phys.ksu.edu/personal/cocke/classes/phys506/squidman.pdf](https://www.phys.ksu.edu/personal/cocke/classes/phys506/squidman.pdf)

[YBCO](condensed-matter-physics.md#yttrium-barium-copper-oxide) device, runs on [liquid nitrogen](chemistry.md#liquid-nitrogen).

## Electronic circuit

↑ **Parent:** [Electronics](electronics.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Electronic_circuit)

### Circuit board

↑ **Parent:** [Electronic circuit](#electronic-circuit)

#### Breadboard

↑ **Parent:** [Circuit board](#circuit-board)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Breadboard)

This is how [electronic circuits](#electronic-circuit) are normally prototyped!

Once you validate them like this, the next step is usually to move on to [printed circuit boards](#printed-circuit-board) for more reliable production setups.

Breadboards are a thing of beauty and wonder.

<a id="image-point-to-point-constructions-on-woden-boards"></a>
![](https://upload.wikimedia.org/wikipedia/commons/thumb/5/56/Wooden_Breadboard_Circuits.jpg/960px-Wooden_Breadboard_Circuits.jpg)

**[Figure 21](#image-point-to-point-constructions-on-woden-boards). Point-to-point constructions on woden boards**. [Source](https://commons.wikimedia.org/wiki/File:Wooden_Breadboard_Circuits.jpg). Predecessors to [breadboards](#breadboard) from where the name came. A thing of beauty, so vintage. You could actually write stuff on those with a pencil!

<a id="video-breadboards-trash-or-treasure-by-keysight-2020"></a>
**[Video 21](#video-breadboards-trash-or-treasure-by-keysight-2020). Breadboards - Trash or Treasure? by Keysight (2020)** [Source](https://www.youtube.com/watch?v=SI8DGyl0K8E).

#### Printed circuit board

↑ **Parent:** [Circuit board](#circuit-board)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Printed_circuit_board)

##### Microprocessor development board

↑ **Parent:** [Printed circuit board](#printed-circuit-board)  
🏷️ **Tags:** [Computer form factor](computer-hardware.md#computer-form-factor)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Microprocessor_development_board)

###### [Microcontroller](computer-hardware.md#microcontroller) devboard

↑ **Parent:** [Microprocessor development board](#microprocessor-development-board)

###### Arduino

↑ **Parent:** [Microcontroller devboard](#microcontroller-devboard)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Arduino)

###### Micro Bit

↑ **Parent:** [Microcontroller devboard](#microcontroller-devboard)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Micro_Bit)

[Bluetooth](computer.md#bluetooth) support: not enough [RAM](computer-hardware.md#random-access-memory) for it, though in principle its chip/[transceiver](telecommunication.md#radio-transceiver) could support it! [https://microbit-micropython.readthedocs.io/en/v1.0.1/ble.html](https://microbit-micropython.readthedocs.io/en/v1.0.1/ble.html)

Supported editors: [https://microbit.org/code/](https://microbit.org/code/)

MicroPython web editor and compiler: [https://python.microbit.org/v/2](https://python.microbit.org/v/2)

Everything in this section is tested on the [Micro Bit v1](#micro-bit-v1) from [Micro Bit v1](ciro-santilli-s-hardware.md#micro-bit-v1) unless otherwise noted.

Bibliography:
- [https://github.com/carlosperate/awesome-microbit](https://github.com/carlosperate/awesome-microbit)

![](https://upload.wikimedia.org/wikipedia/commons/thumb/a/a3/Micro-bit_v1_%26_v2.JPG/960px-Micro-bit_v1_%26_v2.JPG)

**[Figure 22](#_254)** [Source](https://commons.wikimedia.org/wiki/File:Micro-bit_v1_%26_v2.JPG).

###### Micro Bit simulator

↑ **Parent:** [Micro Bit](#micro-bit)

###### Micro Bit Python editor

↑ **Parent:** [Micro Bit simulator](#micro-bit-simulator)

[https://python.microbit.org/v/3/reference](https://python.microbit.org/v/3/reference)

###### MakeCode Miro Bit

↑ **Parent:** [Micro Bit simulator](#micro-bit-simulator)

[https://makecode.microbit.org](https://makecode.microbit.org)

Microbit simulator using some [Microsoft](microsoft.md) framework.

TODO the Python code from there does not seem to run on the microbit via `uflash`, because it is not [MicroPython](systems-programming.md#micropython).

[https://support.microbit.org/support/solutions/articles/19000111744-makecode-python-and-micropython](https://support.microbit.org/support/solutions/articles/19000111744-makecode-python-and-micropython) explains.

[https://forum.makecode.com/t/help-understanding-local-build-options/6130](https://forum.makecode.com/t/help-understanding-local-build-options/6130) asks how to compile locally and suggests it is possible. Seems to require [Yotta](#yotta-build-system), so presumably compiles?

Presumably this is because Microsoft ported their MakeCode thing to the MicroBit, and the Micro Bit foundation accepted them.

E.g. there toggling a LED:
```
led.toggle(0, 0)
```
but the code that works locally is a completely differently named API `set_pixel`:
```
microbit.display.set_pixel(0, 0, )
```
Microsoft going all in on adopt extend extinguish from an early age!

###### Micro Bit getting started

↑ **Parent:** [Micro Bit](#micro-bit)

When plugged into [Ubuntu 22.04](systems-programming.md#ubuntu-22-04) via the [USB Micro-B](computer-hardware.md#usb-micro-b) the [Micro Bit](#micro-bit) mounts as:
```
/media/$USER/MICROBIT/
```
e.g.:
```
/media/ciro/MICROBIT/
```
for username `ciro`.

Loading the program is done by simply copying a `.hex` binary into the image e.g. with:
```
cp ~/Downloads/microbit_program.hex /media/$USER/MICROBIT/
```
The file name does not matter, only the `.hex` extension.

The back power light flashes while upload is happening.

Flashing takes about 10-15 seconds for the 1.8 MB scroll display hello world from [https://microbit-micropython.readthedocs.io/en/v1.0.1/tutorials/hello.html](https://microbit-micropython.readthedocs.io/en/v1.0.1/tutorials/hello.html):
```
from microbit import *
display.scroll("Hello, World!")
```
and the program starts executing immediately after flash ends.

You can restart the program by clicking the reset button near the USB. When you push down the program dies, and it restarts as soon as you release the button.

###### Program the Micro Bit with X

↑ **Parent:** [Micro Bit](#micro-bit)

###### Run [Zephyr](systems-programming.md#zephyr-operating-system) on Micro Bit

↑ **Parent:** [Program the Micro Bit with X](#program-the-micro-bit-with-x)  
🏷️ **Tags:** [Run Zephyr on X](systems-programming.md#run-zephyr-on-x)

Docs: [https://docs.zephyrproject.org/2.7.0/boards/arm/bbc_microbit/doc/index.html](https://docs.zephyrproject.org/2.7.0/boards/arm/bbc_microbit/doc/index.html)

Build worked:
```
west build -d build/microbit/hello_world -b bbc_microbit samples/hello_world
```
but flash failed:
```
west flash -d build/microbit/hello_world
```
Related: [https://mattoppenheim.com/2018/06/24/using-udev-to-remove-the-need-for-sudo-with-the-bbc-microbit](https://mattoppenheim.com/2018/06/24/using-udev-to-remove-the-need-for-sudo-with-the-bbc-microbit)

The build also generates a .hex file by default, and we've tried to flash it manually with:
```
cp build/microbit/hello_world/zephyr/zephyr.hex /media/ciro/MICROBIT/
```
but we failed to see it do anything with [zephyr/blink\_gpio.c](systems-programming.md#_file/zephyr/blink_gpio.c), so not sure if the flashing was broken or if the code was broken, or if we didn't find the IO pins correctly.

###### Run MicroPython on Micro Bit

↑ **Parent:** [Program the Micro Bit with X](#program-the-micro-bit-with-x)  
🏷️ **Tags:** [Run MicroPython on X](systems-programming.md#run-micropython-on-x)

Bibliography:
- [https://tech.microbit.org/software/micropython/](https://tech.microbit.org/software/micropython/)

###### Compile MicroPython code for Micro Bit locally

↑ **Parent:** [Run MicroPython on Micro Bit](#run-micropython-on-micro-bit)

- [https://stackoverflow.com/questions/73425359/is-it-possible-to-compile-microbit-python-code-locally](https://stackoverflow.com/questions/73425359/is-it-possible-to-compile-microbit-python-code-locally)
- [https://stackoverflow.com/questions/52691853/generating-micropython-python-code-hex-file-from-commandline](https://stackoverflow.com/questions/52691853/generating-micropython-python-code-hex-file-from-commandline)

To use a prebuilt firmware, you can just use `uflash`, tested on [Ubuntu 22.04](systems-programming.md#ubuntu-22-04):
```
git clone https://github.com/bbcmicrobit/micropython
cd micropython
git checkout 7fc33d13b31a915cbe90dc5d515c6337b5fa1660
uflash examples/led_dance.py
```
What that does is:
- convert the [MicroPython](systems-programming.md#micropython) code to bytecode
- join it up with a prebuilt firmware that ships with uflash which contains the MicroPython interpreter
- flashes that

To build your own firmware see: [Compile MicroPython code for Micro Bit locally on Ubuntu 22.04 with your own firmware](#compile-micropython-code-for-micro-bit-locally-on-ubuntu-22-04-with-your-own-firmware)

<h6 id="compile-micropython-code-for-micro-bit-locally-on-ubuntu-22-04-with-your-own-firmware">Compile MicroPython code for Micro Bit locally on <a href="systems-programming.html#ubuntu-22-04">Ubuntu 22.04</a> with your own firmware</h6>

↑ **Parent:** [Compile MicroPython code for Micro Bit locally](#compile-micropython-code-for-micro-bit-locally)

TODO didn't manage from source [Ubuntu 22.04](systems-programming.md#ubuntu-22-04), their setup bitrotted way too fast... it's shameful even. Until I gave up and went for the magic [Docker](systems-programming.md#docker-software) of + [https://github.com/bbcmicrobit/micropython](https://github.com/bbcmicrobit/micropython), and it bloody worked:
```
git clone https://github.com/bbcmicrobit/micropython
cd micropython
git checkout 7fc33d13b31a915cbe90dc5d515c6337b5fa1660
docker pull ghcr.io/carlosperate/microbit-toolchain:latest
docker run -v $(pwd):/home --rm ghcr.io/carlosperate/microbit-toolchain:latest yt target bbc-microbit-classic-gcc-nosd@https://github.com/lancaster-university/yotta-target-bbc-microbit-classic-gcc-nosd
docker run -v $(pwd):/home --rm ghcr.io/carlosperate/microbit-toolchain:latest make all

# Build one.
tools/makecombinedhex.py build/firmware.hex examples/counter.py -o build/counter.hex
cp build/counter.hex "/media/$USER/MICROBIT/"

# Build all.
for f in examples/*; do b="$(basename "$f")"; echo $b; tools/makecombinedhex.py build/firmware.hex "$f" -o "build/${b%.py}.hex"; done
```

The pre-Docker attempts:
```
sudo add-apt-repository -y ppa:team-gcc-arm-embedded
sudo apt update
sudo apt install gcc-arm-embedded
sudo apt install cmake ninja-build srecord libssl-dev

# Rust required for some Yotta component, OMG.
sudo snap install rustup
rustup default 1.64.0

python3 -m pip install yotta
```

The line:
```
sudo add-apt-repository -y ppa:team-gcc-arm-embedded
```
warns:
```
E: The repository 'https://ppa.launchpadcontent.net/team-gcc-arm-embedded/ppa/ubuntu jammy Release' does not have a Release file.
N: Updating from such a repository can't be done securely, and is therefore disabled by default.
N: See apt-secure(8) manpage for repository creation and user configuration details.
```
and then the update/`sudo apt-get install gcc-arm-embedded` fails, bibliography:
- [https://askubuntu.com/questions/732985/force-update-from-unsigned-repository](https://askubuntu.com/questions/732985/force-update-from-unsigned-repository)
- [https://askubuntu.com/questions/1243252/how-to-install-arm-none-eabi-gdb-on-ubuntu-20-04-lts-focal-fossa](https://askubuntu.com/questions/1243252/how-to-install-arm-none-eabi-gdb-on-ubuntu-20-04-lts-focal-fossa)

Attempting to install [Yotta](#yotta-build-system):
```
sudo -H pip3 install yotta
```
or:
```
python3 -m pip install --user yotta
```
was failing with:
```
Exception: Version mismatch: this is the 'cffi' package version 1.15.1, located in '/tmp/pip-build-env-dinhie_9/overlay/local/lib/python3.10/dist-packages/cffi/api.py'.  When we import the top-level '_cffi_backend' extension module, we get version 1.15.0, located in '/usr/lib/python3/dist-packages/_cffi_backend.cpython-310-x86_64-linux-gnu.so'.  The two versions should be equal; check your installation.
```
Running:
```
python3 -m pip install --user cffi==1.15.1
```
did not help. Bibliography:
- [https://stackoverflow.com/questions/58552666/exception-version-mismatch-this-is-the-cffi-package-version-1-13-1](https://stackoverflow.com/questions/58552666/exception-version-mismatch-this-is-the-cffi-package-version-1-13-1)
- [https://github.com/ARMmbed/yotta/issues/289](https://github.com/ARMmbed/yotta/issues/289)
- [https://github.com/pyocd/pyOCD/issues/163](https://github.com/pyocd/pyOCD/issues/163)
- [http://docs.yottabuild.org/#installing-on-linux](http://docs.yottabuild.org/#installing-on-linux)

From a clean [virtualenv](programming-language.md#virtualenv), it appears to move further, and then fails at:
```
Building wheel for cmsis-pack-manager (pyproject.toml) ... error
error: [Errno 2] No such file or directory: 'cargo'
```
So we install [Rust](programming-language.md#rust-programming-language) and try again, OMG:
```
sudo snap install rustup
rustup default stable
```
which at the time of writing was `rustc 1.64.0`, and then OMG, it worked!! We have the `yt` command.

However, it is still broken, e.g.:
```
git clone https://github.com/lancaster-university/microbit-samples
cd microbit-samples
git checkout 285f9acfb54fce2381339164b6fe5c1a7ebd39d5
cp source/examples/invaders/* source
yt clean
yt build
```
blows up:
```
annot import name 'soft_unicode' from 'markupsafe'
```
bibliography:
- [https://github.com/aws/aws-sam-cli/issues/3661](https://github.com/aws/aws-sam-cli/issues/3661)
- [https://stackoverflow.com/questions/72191560/importerror-cannot-import-name-soft-unicode-from-markupsafe](https://stackoverflow.com/questions/72191560/importerror-cannot-import-name-soft-unicode-from-markupsafe)

###### Program the Micro Bit in C

↑ **Parent:** [Program the Micro Bit with X](#program-the-micro-bit-with-x)  
🏷️ **Tags:** [C (language)](programming-language.md#c-programming-language)

[https://stackoverflow.com/questions/73877965/how-to-compile-c-c-code-into-a-hex-file-for-the-bbc-microbit](https://stackoverflow.com/questions/73877965/how-to-compile-c-c-code-into-a-hex-file-for-the-bbc-microbit)

Official support is abysmal, very focused on [MicroPython](systems-programming.md#micropython) and their graphical UI.

The setup impossible to achieve as it requires setting up the [Yotta](#yotta-build-system), just like the impossible to setup [Compile MicroPython code for Micro Bit locally on Ubuntu 22.04 with your own firmware](#compile-micropython-code-for-micro-bit-locally-on-ubuntu-22-04-with-your-own-firmware) setup.

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
.hex file size for the hello world was 447 kB, much better than the [MicroPython](systems-programming.md#micropython) hello world downloaded from the website which was about 1.8 MB!

If you try it again for a second time from a clean tree, it fails with:
```
warning: github rate limit for anonymous requests exceeded: you must log in
```
presumably because after Yotta died it started using GitHub as a registry... sad. When will people learn. Apparently we were at 5000 API calls per hour. But if you don't clean the tree, you will be just fine.

###### Yotta (build system)

↑ **Parent:** [Micro Bit](#micro-bit)

Dead:
- [https://yottabuild.org/](https://yottabuild.org/)
- [https://github.com/ARMmbed/yotta](https://github.com/ARMmbed/yotta)

###### Micro Bit version

↑ **Parent:** [Micro Bit](#micro-bit)

Identification: [https://kitronik.co.uk/blogs/resources/explore-micro-bit-v1-microbit-v2-differences](https://kitronik.co.uk/blogs/resources/explore-micro-bit-v1-microbit-v2-differences) The easiest thing is perhaps the GPIO notches.

###### Micro Bit v1

↑ **Parent:** [Micro Bit version](#micro-bit-version)

###### nRF51 series

↑ **Parent:** [Micro Bit](#micro-bit)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/nRF51_series)

###### Micro Bit example

↑ **Parent:** [Micro Bit](#micro-bit)

- [microbit/micropython/uart.py](microbit/micropython/uart.py): the Micro BIt comes with a [UART](computer.md#universal-asynchronous-receiver-transmitter) simulator via the USB connection, it is very convenient: [https://support.microbit.org/support/solutions/articles/19000022103-outputing-serial-data-from-the-micro-bit-to-a-computer](https://support.microbit.org/support/solutions/articles/19000022103-outputing-serial-data-from-the-micro-bit-to-a-computer) To output data to the computer simply use Python `print`. To receive you can e.g. use [GNU screen](software.md#gnu-screen):
  ```
  screen /dev/ttyACM0 115200
  ```

  It appears to be very unreliable however, some times it shows up, sometimes it doesn't.

###### Micro Bit GPIO

↑ **Parent:** [Micro Bit](#micro-bit)

Pinout overview: [https://makecode.microbit.org/device/pins](https://makecode.microbit.org/device/pins) Basically 0, 1, and 2 are the truly generic ones. They can also serve as [ADCs](#analog-to-digital-converter).

Micropython documentation: [https://microbit-micropython.readthedocs.io/en/latest/pin.html](https://microbit-micropython.readthedocs.io/en/latest/pin.html)

###### It is hard to do something useful with a devboard

↑ **Parent:** [Microprocessor development board](#microprocessor-development-board)  
🏷️ **Tags:** [Essays by Ciro Santilli](ciro-santilli.md#essays-by-ciro-santilli)

In the 2010's/2020's, many people got excited about getting children in to [electronics](electronics.md) with cheap [devboards](#microprocessor-development-board), notably with [Raspberry Pi](computer-hardware.md#raspberry-pi) and [Arduino](#arduino).

While there is some potential in that, [Ciro Santilli](ciro-santilli.md) always felt that this is very difficult to do, while also keeping his sacred principle of [backward design](cirism.md#backward-design) in mind.

The reason for this is that "everyone" already has much more powerful computers at hand: their laptops/desktops and even [mobile phones](computer-hardware.md#mobile-phone) as of the 2020s. Except perhaps if you are thing specifically about poor countries.

Therefore, the advantage using such devboards for doing something that could useful must come from either:
- their low cost. This would be an important consideration if you were to mass produce your product, but that is not going to be the case for learners, at least initially.
- their portability, and closely linked their ability to act as sensors
- their ability to act as [actuators](robotics.md#actuator), which is often missing from regular computers
- them having [hardware accelerators](computer-hardware.md#application-specific-integrated-circuit) that are not normally present in regular computers, e.g. [FPGAs](computer-hardware.md#field-programmable-gate-array) or [AI accelerators](computer-hardware.md#ai-accelerator). And then the demo project must demonstrate that the project is able to do something significantly faster/cheaper on the devboard than on a desktop computer.

###### Devboard battery power

↑ **Parent:** [Microprocessor development board](#microprocessor-development-board)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Devboard_battery_power)

Many devborads require a 5V power supply.

This is common on wall transformers and [USB](computer-hardware.md#usb), but not in [batteries](chemistry.md#electric-battery).

For battery power you need a [transformer](#transformer).

<a id="video-raspberry-pi-battery-power-by-explainingcomputers-2021"></a>
**[Video 22](#video-raspberry-pi-battery-power-by-explainingcomputers-2021). Raspberry Pi Battery Power by ExplainingComputers (2021)** [Source](https://www.youtube.com/watch?v=lPyDtuzYE5s).

#### Point-to-point construction

↑ **Parent:** [Circuit board](#circuit-board)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Point-to-point_construction)

#### Solder

↑ **Parent:** [Circuit board](#circuit-board)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Solder)

### Digital and analog electronics

↑ **Parent:** [Electronic circuit](#electronic-circuit)

#### Analog-to-digital converter

↑ **Parent:** [Digital and analog electronics](#digital-and-analog-electronics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Analog-to-digital_converter)

Many/most [microcontroller](computer-hardware.md#microcontroller) boards have [analog-to-digital converters](#analog-to-digital-converter) built into them, it is very convenient. E.g. it is the case for the [Raspberry Pi Pico](computer-hardware.md#raspberry-pi-pico).

##### Open source analog-to-digital converter

↑ **Parent:** [Analog-to-digital converter](#analog-to-digital-converter)  
🏷️ **Tags:** [Open source hardware](software.md#open-source-hardware)

<a id="video-open-source-8-5-digit-voltmeter-from-cern-by-marco-reps-2021"></a>
**[Video 23](#video-open-source-8-5-digit-voltmeter-from-cern-by-marco-reps-2021). Open Source 8.5 Digit Voltmeter from CERN by Marco Reps (2021)** [Source](https://www.youtube.com/watch?v=D28uSzCs7-k).

#### Digital-to-analog converter

↑ **Parent:** [Digital and analog electronics](#digital-and-analog-electronics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Digital-to-analog_converter)

#### Digital electronics

↑ **Parent:** [Digital and analog electronics](#digital-and-analog-electronics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Digital_electronics)

##### Digital electronic circuit

↑ **Parent:** [Digital electronics](#digital-electronics)

###### Frequency divider

↑ **Parent:** [Digital electronic circuit](#digital-electronic-circuit)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Frequency_divider)

#### Analog electronics

↑ **Parent:** [Digital and analog electronics](#digital-and-analog-electronics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Analog_electronics)

### LC circuit

↑ **Parent:** [Electronic circuit](#electronic-circuit)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/LC_circuit)

When [Ciro Santilli](ciro-santilli.md) was studying electronics at the [University of São Paulo](university.md#university-of-sao-paulo), the courses, which were heavily inspired from the [USA](united-states.md) 50's were obsessed by this one! Thinking about it, it is kind of a cool thing though.

That [Wikipedia page](https://en.wikipedia.org/w/index.php?title=LC_circuit&oldid=1085148789) is the epitome of [Wikipedia failure to explain things in a way that is of any interest to any learner](website.md#it-is-not-possible-to-teach-natural-sciences-on-wikipedia). [Video 24. "Tutorial on LC resonant circuits by w2aew (2012)"](#video-tutorial-on-lc-resonant-circuits-by-w2aew-2012) is the opposite.

<a id="video-tutorial-on-lc-resonant-circuits-by-w2aew-2012"></a>
**[Video 24](#video-tutorial-on-lc-resonant-circuits-by-w2aew-2012). Tutorial on LC resonant circuits by w2aew (2012)** [Source](https://www.youtube.com/watch?v=hqhV50852jA). - [https://youtu.be/hqhV50852jA?t=239](https://youtu.be/hqhV50852jA?t=239) [series LC circuit](#series-lc-circuit) on a [breadboard](#breadboard) driven by an [AC source](#alternating-current-source). Shows behaviour on [oscilloscope](#oscilloscope) as source frequency is modified. We clearly see voltage going to zero at resonance. This is why thie circuit can be seen as a [filter](technology.md#filter-signal-processing).
- [https://youtu.be/hqhV50852jA?t=489](https://youtu.be/hqhV50852jA?t=489) shows the [parallel LC circuit](#parallel-lc-circuit). We clearly see current reaching a maximum on resonance.

---

<a id="video-lc-circuit-dampened-oscillations-on-an-oscilloscope-by-queuerious-guy-2014"></a>
**[Video 25](#video-lc-circuit-dampened-oscillations-on-an-oscilloscope-by-queuerious-guy-2014). LC circuit dampened oscillations on an oscilloscope by Queuerious Guy (2014)** [Source](https://www.youtube.com/watch?v=XSUiCeCHAvw). Finally a video that shows the oscillations without a driving [AC source](#alternating-current-source). The dude just move wires around on his [breadboard](#breadboard) manually, first charging the [capacitor](#capacitor) and then closing the LC circuit, and is able to see damped oscillations on the [oscilloscope](#oscilloscope).

<a id="video-introduction-to-lc-oscillators-by-usaf-1974"></a>
**[Video 26](#video-introduction-to-lc-oscillators-by-usaf-1974). Introduction to LC Oscillators by USAF (1974)** [Source](https://www.youtube.com/watch?v=W31CCN_ZF34). - [https://youtu.be/W31CCN_ZF34?t=740](https://youtu.be/W31CCN_ZF34?t=740) mentions that [LC circuit](#lc-circuit) formation is the root cause for [Audio feedback](#audio-feedback) with a quick demo. Not very scientific, but cool.

---

<a id="video-lc-circuit-by-eugene-khutoryansky-2016"></a>
**[Video 27](#video-lc-circuit-by-eugene-khutoryansky-2016). LC circuit by Eugene Khutoryansky (2016)** [Source](https://www.youtube.com/watch?v=Mq-PF1vo9QA). Exactly what you would expect from an [Eugene Khutoryansky](particle-physics.md#eugene-khutoryansky) video. The key insight is that the [inductor](#inductor) resists to changes in current. So when current is zero, it slows down the current. And when current is high, it tries to keep it going, which recharges the other side of the [capacitor](#capacitor).

#### An LC circuit is analogous to a spring-mass system

↑ **Parent:** [LC circuit](#lc-circuit)  
🏷️ **Tags:** [Spring-mass system](mechanics.md#spring-mass-system)

Both are [harmonic oscillators](mechanics.md#harmonic-oscillator).

In the [LC circuit](#lc-circuit):
- the current current may be seen as the velocity and containing the [kinetic energy](physics.md#kinetic-energy)
- the charge stored in the capacitor as the [potential energy](physics.md#potential-energy)

You can kickstart motion in either of those systems in two ways:
- charge the capacitor, i.e. pull the string, and then let it go, i.e. close the circuit. This is the simpler one to realise. Shown concretely at: [Video 25. "LC circuit dampened oscillations on an oscilloscope by Queuerious Guy (2014)"](#video-lc-circuit-dampened-oscillations-on-an-oscilloscope-by-queuerious-guy-2014)
- give speed to the mass, i.e. make a current pass through the inductor

#### Series LC circuit

↑ **Parent:** [LC circuit](#lc-circuit)

#### Parallel LC circuit

↑ **Parent:** [LC circuit](#lc-circuit)

#### Audio feedback

↑ **Parent:** [LC circuit](#lc-circuit)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Audio_feedback)

#### RLC circuit

↑ **Parent:** [LC circuit](#lc-circuit)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/RLC_circuit)

## Heartbeat (computing)

↑ **Parent:** [Electronics](electronics.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Heartbeat_(computing))

## Semiconductor package

↑ **Parent:** [Electronics](electronics.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Semiconductor_package)

### Dual in-line package

↑ **Parent:** [Semiconductor package](#semiconductor-package)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Dual_in-line_package)

## Electrical engineer

↑ **Parent:** [Electronics](electronics.md)

### Oliver Heaviside

↑ **Parent:** [Electrical engineer](#electrical-engineer)  
🏷️ **Tags:** [Autodidact](education.md#autodidacticism), [Idealist](science.md#idealist)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Oliver_Heaviside)

He participated in the development of the [electrical telegraph](telecommunication.md#electrical-telegraph), and he did some good modeling work that improved the foundations of the field, notably creating the [telegrapher's equations](telecommunication.md#telegrapher-s-equations).

He was one of those [idealists](science.md#idealist) who just want to do some cool work even if they have to starve for it, people had to get a state pension for him for his contributions. Nice guy. [https://en.wikipedia.org/w/index.php?title=Oliver_Heaviside&oldid=1230097796#Later_years_and_views](https://en.wikipedia.org/w/index.php?title=Oliver_Heaviside&oldid=1230097796#Later_years_and_views):

> In 1896, FitzGerald and John Perry obtained a civil list pension of £120 per year for Heaviside, who was now living in Devon, and persuaded him to accept it, after he had rejected other charitable offers from the [Royal Society](education.md#royal-society).

He also never married: [https://www.nndb.com/people/627/000204015/](https://www.nndb.com/people/627/000204015/)

<a id="image-oliver-heaviside-c- 1900"></a>
![](https://upload.wikimedia.org/wikipedia/commons/thumb/9/95/Oheaviside.jpg/330px-Oheaviside.jpg)

**[Figure 23](#image-oliver-heaviside-c- 1900). Oliver Heaviside c. 1900**. [Source](https://commons.wikimedia.org/wiki/File:Oheaviside.jpg).

## Electronics bibliography

↑ **Parent:** [Electronics](electronics.md)

### Electronics YouTube channel

↑ **Parent:** [Electronics bibliography](#electronics-bibliography)

#### CuriousMarc

↑ **Parent:** [Electronics YouTube channel](#electronics-youtube-channel)

[https://www.youtube.com/channel/UC3bosUr3WlKYm4sBaLs-Adw](https://www.youtube.com/channel/UC3bosUr3WlKYm4sBaLs-Adw)

Mostly on vintage electronics. Lots of focus on [microwave](photon.md#microwave), which he has worked a lot with.

Has been going wild with restoration and reverse engineering of the Apollo moon mission.

<a id="video-inside-the-wild-lab-of-curiousmarc-by-keysight-labs-2022"></a>
**[Video 28](#video-inside-the-wild-lab-of-curiousmarc-by-keysight-labs-2022). Inside the WILD Lab of CuriousMarc by Keysight Labs (2022)** [Source](https://www.youtube.com/watch?v=qwocVH3_1Eo). - [https://youtu.be/qwocVH3_1Eo?t=841](https://youtu.be/qwocVH3_1Eo?t=841) the [IBM System/360](computer.md#ibm-system-360) is insane!

---

##### Marc Verdiell

↑ **Parent:** [CuriousMarc](#curiousmarc)  
🏷️ **Tags:** [École Polytechnique alumnus of 1983](ecole-polytechnique.md#ecole-polytechnique-alumnus-of-1983), [Human](human.md), [Intel fellow](computer-hardware.md#intel-fellow)

[Marc Verdiell](#marc-verdiell) is a [French](continent.md#france) [electrical engineer](#electrical-engineer) born in 1963 or 1964[https://www.intel.com/pressroom/archive/releases/2001/20011129corp.htm](https://www.intel.com/pressroom/archive/releases/2001/20011129corp.htm) and best known for being the creator and host of the [CuriousMarc](#curiousmarc) YouTube channel where he does [mind blowing](brain.md#mind-blown) repairs and [reverse engineering](technology.md#reverse-engineering) of vintage [computers](computer.md) and other [electronic](electronics.md) equipment.

Marc sold his company [LightLogic](#lightlogic), an [optoelectronics](photon.md#optoelectronics) company he founded, to [Intel](computer-hardware.md#intel) in April 2001. This was just after the [dot-com crash](economy.md#dot-com-bubble), but [Intel](computer-hardware.md#intel) apparently still correctly believed that the networking and the [Internet](computer.md#internet) would continue to grow and was investing in the area. His associate [Frank Shum](https://ourbigbook.com/go/topic/frank-shum) sued claiming he should be credited for some of the inventions sold but lost and Marc got it all.[https://www.courthousenews.com/inventor-barred-from-proceeds-of-intel-buyout/](https://www.courthousenews.com/inventor-barred-from-proceeds-of-intel-buyout/)[https://mergr.com/intel-acquires-lightlogic](https://mergr.com/intel-acquires-lightlogic)[https://www.lightreading.com/business-management/lightlogic-bulks-up-under-intel](https://www.lightreading.com/business-management/lightlogic-bulks-up-under-intel). Marc was then almost immediately appointed an [Intel fellow](computer-hardware.md#intel-fellow) at the extremelly early age of 37, and then stayed for a few years at [Intel](computer-hardware.md#intel) until 2006 according to his LinkedIn.[https://www.intel.com/pressroom/archive/releases/2001/20011129corp.htm](https://www.intel.com/pressroom/archive/releases/2001/20011129corp.htm)[https://web.archive.org/web/20030213010020/http://www.intel.com/pressroom/kits/bios/verdiell.htm](https://web.archive.org/web/20030213010020/http://www.intel.com/pressroom/kits/bios/verdiell.htm)

Marc's [LinkedIn](social-technology.md#linkedin) profile: [https://www.linkedin.com/in/marc-verdiell-9742795/](https://www.linkedin.com/in/marc-verdiell-9742795/)

<a id="image-marc-verdiell-at-the-computer-history-museum"></a>
<img src="https://web.archive.org/web/20230423183349if_/https://lh3.googleusercontent.com/3D9u7fe3v94I-Y8jbrCCTdVHJIOIwum1xFWoxeFcJvA1KfX9YwvHzaXINyrNKJGQ_I5tBMsFnpw2kKX6kAPqd_r2yYB7a85QriBq5-hkf1mN2SYh%3Dw1280" alt="" height="600">

**[Figure 24](#image-marc-verdiell-at-the-computer-history-museum). Marc Verdiell at the Computer History Museum**. [Source](https://www.curiousmarc.com/about). Location inferred from Marc's videos, but likely, he often frequents the place, and it looks a bit like that.

Marc's full name is actualy [Jean-Marc Verdiell](#marc-verdiell), but [Ciro Santilli](ciro-santilli.md) remembers there was one [YouTube](website.md#youtube) video where he mentions he gave up on "Jean" partly because [anglophones](linguistics.md#english-language) would murder its pronounciation all the time.

Marc's [PhD thesis](education.md#phd-thesis) is listed at: [https://theses.fr/1990PA112048](https://theses.fr/1990PA112048) and it is entitled:

> Mise en phase de reseaux de lasers a semi-conducteur

which is translated into English as:

> Phase locking of [semiconductor laser](condensed-matter-physics.md#laser-diode) arrays

but the full text is not available online.

<a id="video-profile-of-marc-verdiell-by-gizmodo-2018"></a>
**[Video 29](#video-profile-of-marc-verdiell-by-gizmodo-2018). Profile of Marc Verdiell by Gizmodo (2018)** [Source](https://www.youtube.com/watch?v=tJ2-kkhghD4). [https://youtu.be/tJ2-kkhghD4?t=74](https://youtu.be/tJ2-kkhghD4?t=74) gives his house's location [Atherton, California](united-states.md#atherton-california), part of [Silicon Valley](united-states.md#silicon-valley).

[https://youtu.be/ZgAreiFXhJk?t=253](https://youtu.be/ZgAreiFXhJk?t=253) lists some famous people who live there. It's like a micro heaven.

And a person who makes [open educational content](software.md#open-educational-resources) like Marc, truly deserves it.

Atherton managed to keep the entire place green and every house has a pool. Wikipedia comments [https://web.archive.org/web/20220906010554/https://www.forbes.com/home-improvement/features/most-expensive-zip-codes-us/](https://web.archive.org/web/20220906010554/https://www.forbes.com/home-improvement/features/most-expensive-zip-codes-us/):

> Atherton is known for its wealth; in 1990 and 2019, Atherton was ranked as having the highest per capita income among U.S. towns with a population between 2,500 and 9,999, and it is regularly ranked as the most expensive ZIP Code in the United States \[(94027)\]. The town has very restricting zoning, only permitting one single-family home per acre and no sidewalks. The inhabitants have strongly opposed proposals to permit more housing construction and [Forbes](social-technology.md#forbes) confirms it for 2022: [https://web.archive.org/web/20220906010554/https://www.forbes.com/home-improvement/features/most-expensive-zip-codes-us/](https://web.archive.org/web/20220906010554/https://www.forbes.com/home-improvement/features/most-expensive-zip-codes-us/), by far on top.

---

Marc has reached out to us and requested that some personal information be removed from this article, to which we complied.

###### LightLogic

↑ **Parent:** [Marc Verdiell](#marc-verdiell)

Company founded by [Marc Verdiell](#marc-verdiell) in his garage, and later acquired by [Intel](computer-hardware.md#intel) which was going on a [optoelectronics](photon.md#optoelectronics) buying spree. The division was later sold off in 2023 of course during more difficult times: [https://www.theregister.com/2023/10/31/intel_silicon_photonics_jabil/](https://www.theregister.com/2023/10/31/intel_silicon_photonics_jabil/)

On [Crunchbase](website.md#crunchbase): [https://www.crunchbase.com/organization/lightlogic](https://www.crunchbase.com/organization/lightlogic)

It's hard to understand exactly what the company did by [Googling](google.md) it nowadays. Sad and usual fate. Presumably something related to [transceiver](telecommunication.md#radio-transceiver) for [fiber-optic communication](photon.md#fiber-optic-communication). Only the [patents](law.md#patent) remain: [https://patents.google.com/?assignee=lightlogic&oq=lightlogic](https://patents.google.com/?assignee=lightlogic&oq=lightlogic) to tell its story to the brave.

#### Marco Reps

↑ **Parent:** [Electronics YouTube channel](#electronics-youtube-channel)

[https://www.youtube.com/c/MarcoReps](https://www.youtube.com/c/MarcoReps)

This mostly faceless German dude is awesome!

## ↑ Ancestors (3)

1. [Area of technology](technology.md#area-of-technology)
2. [Technology](technology.md)
3. [Ciro Santilli's Homepage](README.md)

## ← Incoming links (4)

- [The best articles by Ciro Santilli](articles.md)
- [It is hard to do something useful with a devboard](#it-is-hard-to-do-something-useful-with-a-devboard)
- [Optical table](photon.md#optical-table)
- [Sinusoidal](calculus.md#sinusoidal)
