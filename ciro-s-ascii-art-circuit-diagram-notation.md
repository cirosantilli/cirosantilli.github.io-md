<h1 id="ciro-s-ascii-art-circuit-diagram-notation">Ciro's ASCII art circuit diagram notation</h1>

↑ **Parent:** [ASCII art circuit diagram](ascii-art-circuit-diagram.md)

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
- `AC`: [AC source](alternating-current-source.md). Parameters:
  - `Hz`: frequency
  - `V`: peak voltage

  e.g.:
  ```
  AC_1Hz_2V
  ```

  If only one side is given, the other is assumed to be at a ground `G`.
- `C`: [capacitor](capacitor.md)
- `G`: ground. Often used together with `DC`, e.g.:
  ```
  DC_10---R_10---G
  ```

  means applying a voltage of 10 V across a 10 Ohm [resistor](resistor.md), which would lead to a current of 1 A
- `L`: [inductor](inductor.md)
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
- `R`: [resistor](resistor.md)
- `SQUID`: [SQUID device](squid-device.md)
- `X`: [Josephson junction](josephson-junction.md)

Asymmetric components have multiple letters indicating different ports. The capital letter indicates the device, and lower case letters the ports. The wires then go into the ports:
- `D`: [diode](diode.md)
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
- `DC` [DC source](direct-current-source.md). Ports:
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
- `I`: [electric current](electric-current.md) source. Ports:
  - `s`: electron source
  - `d`: electron destination
- `P`: [potentiometer](potentiometer.md) source. Ports:
  - `1`: one of the sides
  - `2`: the middle
  - `3`: the other side
- `T`: [transistor](transistor.md). The ports are `sgTd`:
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
- `V`: [Voltmeter](voltmeter.md). Ports:
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

  represents a circuit linking port 1 of a [Raspberry Pi Pico W](raspberry-pi-pico-w.md), which is GPIO pin 0, through a [resistor](resistor.md) and an [LED](light-emitting-diode.md), back to pin 3 of the board, which is ground.

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
means applying a voltage of 10 V across a 10 Ohm [resistor](resistor.md), which would lead to a current of 1 A

If a component has more than two parameters, units are used to distinguish them when possible, e.g.:
```
AC_1kV_2MHz
```
means an [AC source](alternating-current-source.md) with:
- 1 kV [voltage](voltage.md)
- 1 MHz frequency

## ↑ Ancestors (6)

1. [ASCII art circuit diagram](ascii-art-circuit-diagram.md)
2. [Circuit diagram](circuit-diagram.md)
3. [Electronics](electronics-split.md)
4. [Area of technology](area-of-technology.md)
5. [Technology](technology-split.md)
6. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (8)

- [Rpi-pico-w/upython/adc.py](_file/rpi-pico-w/upython/adc.py.md)
- [Rpi-pico-w/upython/thermistor\_fan\_control.py](_file/rpi-pico-w/upython/thermistor_fan_control.py.md)
- [DC SQUID](dc-squid.md)
- [Flux qubit](flux-qubit.md)
- [Microphone](microphone.md)
- [Probable observation of the Josephson superconducting tunneling effect](probable-observation-of-the-josephson-superconducting-tunneling-effect.md)
- [Superconducting quantum computing](superconducting-quantum-computing.md)
- [Transmon](transmon.md)
