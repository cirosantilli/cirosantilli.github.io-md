# Transmon

↑ **Parent:** [Superconducting qubit type](superconducting-qubit-type.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Transmon)

Used e.g. in the [Sycamore processor](sycamore-processor.md).

The most basic type of transmon is in [Ciro's ASCII art circuit diagram notation](ciro-s-ascii-art-circuit-diagram-notation.md), an [LC circuit](lc-circuit.md) e.g. as mentioned at [https://youtu.be/cb_f9KpYipk?t=180](https://youtu.be/cb_f9KpYipk?t=180) from [Video 16. "The transmon qubit by Leo Di Carlo (2018)"](the-hardware-of-a-quantum-computer-by-tu-delft.md#video-the-transmon-qubit-by-leo-di-carlo-2018):
```
+----------+
| Island 1 |
+----------+
   |   |
   X   C
   |   |
+----------+
| Island 2 |
+----------+
```

[https://youtu.be/eZJjQGu85Ps?t=2443](https://youtu.be/eZJjQGu85Ps?t=2443) from [Video 10. "Superconducting Qubits I Part 1 by Zlatko Minev (2020)"](superconducting-quantum-computing.md#video-superconducting-qubits-i-part-1-by-zlatko-minev-2020) describes a (possibly simplified) physical model of it, as two superconducting metal islands linked up by a [Josephson junction](josephson-junction.md) marked as `X` in the diagram as per-[Ciro's ASCII art circuit diagram notation](ciro-s-ascii-art-circuit-diagram-notation.md):
```
+-------+       +-------+
|       |       |       |
| Q_1() |---X---| Q_2() |
|       |       |       |
+-------+       +-------+
```
The circuit is then analogous to a [LC circuit](lc-circuit.md), with the islands being the [capacitor](capacitor.md). The [Josephson junction](josephson-junction.md) functions as a non-linear [inductor](inductor.md).

Others define it with a [SQUID device](squid-device.md) instead: [https://youtu.be/cb_f9KpYipk?t=328](https://youtu.be/cb_f9KpYipk?t=328) from [Video 16. "The transmon qubit by Leo Di Carlo (2018)"](the-hardware-of-a-quantum-computer-by-tu-delft.md#video-the-transmon-qubit-by-leo-di-carlo-2018). He mentions that this allows tuning the inductive element without creating a new device.

<a id="video-the-superconducting-transmon-qubit-as-a-microwave-resonator-by-daniel-sank-2021"></a>
**[Video 14](#video-the-superconducting-transmon-qubit-as-a-microwave-resonator-by-daniel-sank-2021). The superconducting transmon qubit as a microwave resonator by Daniel Sank (2021)** [Source](https://www.youtube.com/watch?v=dKTNBN99xLw).

<a id="video-calibration-of-transmon-superconducting-qubits-by-stefan-titus-2021"></a>
**[Video 15](#video-calibration-of-transmon-superconducting-qubits-by-stefan-titus-2021). Calibration of Transmon Superconducting Qubits by Stefan Titus (2021)** [Source](https://www.youtube.com/watch?v=5ggYJJjlw8o). Possibly this [Keysight](keysight.md) which would make sense.

**Table of contents**

- [An Introduction to the Transmon Qubit for Electromagnetic Engineers](an-introduction-to-the-transmon-qubit-for-electromagnetic-engineers.md)
- [Rabi cycle](rabi-cycle.md)
- [The Hardware of a Quantum Computer by TU Delft](the-hardware-of-a-quantum-computer-by-tu-delft.md)

## ↑ Ancestors (12)

1. [Superconducting qubit type](superconducting-qubit-type.md)
2. [Superconducting qubit](superconducting-qubit.md)
3. [Superconducting quantum computing](superconducting-quantum-computing.md)
4. [Quantum computer physical implementation](quantum-computer-physical-implementation.md)
5. [Quantum computing hardware](quantum-computing-hardware.md)
6. [Quantum computing](quantum-computing-split.md)
7. [Quantum information](quantum-information.md)
8. [Information](information.md)
9. [Information technology](information-technology.md)
10. [Area of technology](area-of-technology.md)
11. [Technology](technology-split.md)
12. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (4)

- [Google Quantum AI](google-quantum-ai.md)
- [Superconducting quantum computing](superconducting-quantum-computing.md)
- [The Hardware of a Quantum Computer by TU Delft](the-hardware-of-a-quantum-computer-by-tu-delft.md)
- [Transmon](transmon.md)
