# Superconducting quantum computing

↑ **Parent:** [Quantum computer physical implementation](quantum-computer-physical-implementation.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Superconducting_quantum_computing)

Based on the [Josephson effect](josephson-effect.md). Yet another application of that phenomenal phenomena!

Philosophically, [superconducting qubits are good because superconductivity is macroscopic](superconducting-qubits-are-good-because-superconductivity-is-macroscopic.md).

It is fun to see that the representation of information in the QC basically uses an [LC circuit](lc-circuit.md), which is a very classical resonator circuit.

As mentioned at [https://en.wikipedia.org/wiki/Superconducting_quantum_computing#Qubit_archetypes](https://en.wikipedia.org/wiki/Superconducting_quantum_computing#Qubit_archetypes) there are actually a few different types of superconducting qubits:
- flux
- charge
- phase

and hybridizations of those such as:
- [transmon](transmon.md)

Input:
- [microwave](microwave.md) radiation to excite circuit, or do nothing and wait for it to fall to 0 spontaneously
- interaction: TODO
- readout: TODO

<a id="video-quantum-computing-with-superconducting-qubits-by-alexandre-blais-2012"></a>
**[Video 6](#video-quantum-computing-with-superconducting-qubits-by-alexandre-blais-2012). Quantum Computing with Superconducting Qubits by Alexandre Blais (2012)** [Source](http://youtube.com/watch?v=t5nxusm_Umk). - [https://youtu.be/t5nxusm_Umk?t=176](https://youtu.be/t5nxusm_Umk?t=176) [quantum computing is hard because we want long coherence but fast control](quantum-computing-is-hard-because-we-want-long-coherence-but-fast-control.md)
- [https://youtu.be/t5nxusm_Umk?t=784](https://youtu.be/t5nxusm_Umk?t=784) [superconducting quantum computer need non-linear components](superconducting-quantum-computer-need-non-linear-components.md)

---

<a id="video-quantum-transport-lecture-16-superconducting-qubits-by-sergey-frolov-2013"></a>
**[Video 7](#video-quantum-transport-lecture-16-superconducting-qubits-by-sergey-frolov-2013). Quantum Transport, Lecture 16: Superconducting qubits by Sergey Frolov (2013)** [Source](http://youtube.com/watch?v=Kz6mhh1A_mU). [https://youtu.be/Kz6mhh1A_mU?t=1171](https://youtu.be/Kz6mhh1A_mU?t=1171) describes several possible realizations: charge, flux, charge/flux and phase.

<a id="video-building-a-quantum-computer-with-superconducting-qubits-by-daniel-sank-2019"></a>
**[Video 8](#video-building-a-quantum-computer-with-superconducting-qubits-by-daniel-sank-2019). Building a quantum computer with superconducting qubits by Daniel Sank (2019)** [Source](https://www.youtube.com/watch?v=uPw9nkJAwDY). Daniel wears a "Google SB" t-shirt, which either means [shabi](shabi.md) in [Chinese](chinese-language.md), or [Santa Barbara](santa-barbara.md). [Google Quantum AI](google-quantum-ai.md) is based in [Santa Barbara](santa-barbara.md), with links to [UCSB](university-of-california-santa-barbara.md).
- [https://youtu.be/uPw9nkJAwDY?t=293](https://youtu.be/uPw9nkJAwDY?t=293) [superconducting qubits are good because superconductivity is macroscopic](superconducting-qubits-are-good-because-superconductivity-is-macroscopic.md). Explains how in non superconducting metal, each electron moves separatelly, and can hit atoms and leak vibration/photos, which lead to observation and quantum error
- [https://youtu.be/uPw9nkJAwDY?t=429](https://youtu.be/uPw9nkJAwDY?t=429) made of [aluminium](aluminium.md)
- [https://youtu.be/uPw9nkJAwDY?t=432](https://youtu.be/uPw9nkJAwDY?t=432) shows the [circuit diagram](circuit-diagram.md), and notes that the thing is basically a [LC circuit](lc-circuit.md)
  ```
  +-----+
  |     |
  |   +-+-+
  |   |   |
  C   X   X
  |   |   |
  |   +-+-+
  |     |
  +-----+
  ```

  using the newly created just now [Ciro's ASCII art circuit diagram notation](ciro-s-ascii-art-circuit-diagram-notation.md). Note that the block on the right is a [SQUID device](squid-device.md).
- [https://youtu.be/uPw9nkJAwDY?t=471](https://youtu.be/uPw9nkJAwDY?t=471) mentions that the frequency between states 0 and 1 is chosen to be 6 GHz:
  - higher frequencies would be harder/more expensive to generate
  - lower frequencies would mean less energy according to the [Planck relation](planck-einstein-relation.md). And less energy means that thermal energy would matter more, and introduce more noise.

    6 GHz is about $6^9 \times h = 6 \times 10^9 \times 6.62 \times 10^{-34} \approx 4\e{-24} J$

    From the definition of the [Boltzmann constant](boltzmann-constant.md), the temperature which has that average energe of particles is of the order of:

    $$
    T = E/k_b = 4\e{-24}/1.38\e{-23} \approx 0.3K
    $$

  This explains why we need to go to much lower temperatures than simply the [superconducting temperature of aluminum](superconducting-temperature-of-aluminum.md)!

---

<a id="video-a-brief-history-of-superconducting-quantum-computing-by-steven-girvin-2021"></a>
**[Video 9](#video-a-brief-history-of-superconducting-quantum-computing-by-steven-girvin-2021). A Brief History of Superconducting quantum computing by Steven Girvin (2021)** [Source](https://www.youtube.com/watch?v=xjlGL4Mvq7A). - [https://youtu.be/xjlGL4Mvq7A?t=138](https://youtu.be/xjlGL4Mvq7A?t=138) [superconducting quantum computer need non-linear components](superconducting-quantum-computer-need-non-linear-components.md) (too brief if you don't know what he means in advance)
- [https://youtu.be/xjlGL4Mvq7A?t=169](https://youtu.be/xjlGL4Mvq7A?t=169) [quantum computing is hard because we want long coherence but fast control](quantum-computing-is-hard-because-we-want-long-coherence-but-fast-control.md)

---

<a id="video-superconducting-qubits-i-part-1-by-zlatko-minev-2020"></a>
**[Video 10](#video-superconducting-qubits-i-part-1-by-zlatko-minev-2020). Superconducting Qubits I Part 1 by Zlatko Minev (2020)** [Source](https://www.youtube.com/watch?v=eZJjQGu85Ps). The Q&A in the middle of talking is a bit annoying.


- [https://youtu.be/eZJjQGu85Ps?t=2443](https://youtu.be/eZJjQGu85Ps?t=2443) the first actually useful part, shows a [transmon](transmon.md) diagram with some useful formulas on it

---

<a id="video-superconducting-qubits-i-part-2-by-zlatko-minev-2020"></a>
**[Video 11](#video-superconducting-qubits-i-part-2-by-zlatko-minev-2020). Superconducting Qubits I Part 2 by Zlatko Minev (2020)** [Source](https://www.youtube.com/watch?v=SDiiFOham6Y).

<a id="video-how-to-turn-superconductors-into-a-quantum-computer-by-lukas-s-lab-2023"></a>
**[Video 12](#video-how-to-turn-superconductors-into-a-quantum-computer-by-lukas-s-lab-2023). How to Turn Superconductors Into A Quantum Computer by Lukas's Lab (2023)** [Source](https://www.youtube.com/watch?v=xsdleM-f0i8). This video is just the introduction, too basic. But if he goes through with the followups he promisses, then something might actually come out of it.

**Table of contents**

- [Superconducting quantum computer need non-linear components](superconducting-quantum-computer-need-non-linear-components.md)
- [Superconducting qubit](superconducting-qubit.md)
  - [Pros and cons of superconducting qubits](pros-and-cons-of-superconducting-qubits.md)
    - [Con of superconducting qubits](con-of-superconducting-qubits.md)
      - [Superconducting qubits are bad because it is harder to ensure that they are all the same](superconducting-qubits-are-bad-because-it-is-harder-to-ensure-that-they-are-all-the-same.md)
    - [Pro of superconducting qubits](pro-of-superconducting-qubits.md)
      - [Superconducting qubits are good because superconductivity is macroscopic](superconducting-qubits-are-good-because-superconductivity-is-macroscopic.md)
      - [Superconducting qubits are bad because of fabrication variation](superconducting-qubits-are-bad-because-of-fabrication-variation.md)
  - [Superconducting qubit type](superconducting-qubit-type.md)
    - [Flux qubit](flux-qubit.md)
    - [Transmon](transmon.md)
      - [An Introduction to the Transmon Qubit for Electromagnetic Engineers](an-introduction-to-the-transmon-qubit-for-electromagnetic-engineers.md)
      - [Rabi cycle](rabi-cycle.md)
      - [The Hardware of a Quantum Computer by TU Delft](the-hardware-of-a-quantum-computer-by-tu-delft.md)
- [Organization developing superconducting quantum computer](organization-developing-superconducting-quantum-computer.md)
  - [Alice&Bob](alice-and-bob.md)
    - [Cat qubit](cat-qubit.md)
  - [Google Quantum AI](google-quantum-ai.md)
    - [Google Quantum Campus](google-quantum-campus.md)
    - [Google Quantum AI employee](google-quantum-ai-employee.md)
      - [Daniel Sank](daniel-sank.md)
      - [Julian Kelly](julian-kelly.md)
      - [John M. Martinis](john-m-martinis.md)
    - [Google Quantum AI hardware](google-quantum-ai-hardware.md)
      - [Sycamore processor](sycamore-processor.md)
      - [Willow (quantum computer)](willow-quantum-computer.md)
  - [IBM Quantum Computing](ibm-quantum-computing.md)
    - [IBM quantum computer](ibm-quantum-computer.md)
  - [IQM](iqm.md)
  - [OpenSuperQ](opensuperq.md)
  - [Oxford Quantum Circuits](oxford-quantum-circuits.md)
    - [Ilana Wisby](ilana-wisby.md)
  - [Rigetti Computing](rigetti-computing.md)

## ↑ Ancestors (9)

1. [Quantum computer physical implementation](quantum-computer-physical-implementation.md)
2. [Quantum computing hardware](quantum-computing-hardware.md)
3. [Quantum computing](quantum-computing-split.md)
4. [Quantum information](quantum-information.md)
5. [Information](information.md)
6. [Information technology](information-technology.md)
7. [Area of technology](area-of-technology.md)
8. [Technology](technology-split.md)
9. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (1)

- [Superconducting quantum computing](superconducting-quantum-computing.md)
