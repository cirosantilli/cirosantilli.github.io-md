# IonQ

↑ **Parent:** [Organization developing trapped ion quantum computer](organization-developing-trapped-ion-quantum-computer.md)  
🏷️ **Tags:** [Company](company-split.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/IonQ)

<a id="video-quantum-simulation-and-computation-with-trapped-ions-by-christopher-monroe-2021"></a>
**[Video 37](#video-quantum-simulation-and-computation-with-trapped-ions-by-christopher-monroe-2021). Quantum Simulation and Computation with Trapped Ions by Christopher Monroe (2021)** [Source](https://www.youtube.com/watch?v=LEqPlDrMXjs).

<a id="video-quantum-computing-with-trapped-ions-by-christopher-monroe-2018"></a>
**[Video 38](#video-quantum-computing-with-trapped-ions-by-christopher-monroe-2018). Quantum Computing with Trapped Ions by Christopher Monroe (2018)** [Source](https://www.youtube.com/watch?v=9aOLwjUZLm0). Co-founder of [IonQ](ionq.md). Cool dude. Starts with basic background we already know now. Mentions that there is some relationship between [atomic clocks](atomic-clock.md) and [trapped ion quantum computers](trapped-ion-quantum-computer.md), which is interesting. Then he goes into turbo mode, and you get lost unless you're an expert! [Video 37. "Quantum Simulation and Computation with Trapped Ions by Christopher Monroe (2021)"](#video-quantum-simulation-and-computation-with-trapped-ions-by-christopher-monroe-2021) is perhaps a better watch.
- [https://youtu.be/9aOLwjUZLm0?t=1216](https://youtu.be/9aOLwjUZLm0?t=1216) [superconducting qubits are bad because it is harder to ensure that they are all the same](superconducting-qubits-are-bad-because-it-is-harder-to-ensure-that-they-are-all-the-same.md)
- [https://youtu.be/9aOLwjUZLm0?t=1270](https://youtu.be/9aOLwjUZLm0?t=1270) our wires are provided by [lasers](laser.md). Gives example of [ytterbium](ytterbium.md)$^{+1}$, which has nice frequencies for practical [laser](laser.md) choice. Ytterbium ends in 6s2 5d1, so they must remove the 5d1 electron? But then you are left with 2 electrons in 6s2, can you just change their spins at will without problem?
- [https://youtu.be/9aOLwjUZLm0?t=1391](https://youtu.be/9aOLwjUZLm0?t=1391) a single atom actually reflects 1% of the input laser, not bad!
- [https://youtu.be/9aOLwjUZLm0?t=1475](https://youtu.be/9aOLwjUZLm0?t=1475) a transition that they want to drive in Ytterbium has 355 nm, which is easy to generate TODO why.
- [https://youtu.be/9aOLwjUZLm0?t=1520](https://youtu.be/9aOLwjUZLm0?t=1520) mentions that 351 would be much harder, e.g. as used in inertially confied fusion, takes up a room
- [https://youtu.be/9aOLwjUZLm0?t=1539](https://youtu.be/9aOLwjUZLm0?t=1539) what they use: a [pulsed laser](pulsed-laser.md). It is made primarily for [photolithography](photolithography.md), [Coherent, Inc.](coherent-inc.md) makes 200 of them a year, so it is reliable stuff and easy to operate. At [https://www.coherent.com/lasers/nanosecond/avia-nx](https://www.coherent.com/lasers/nanosecond/avia-nx) we can see some of their 355 offers. [https://archive.ph/wip/JKuHI](https://archive.ph/wip/JKuHI) shows a used system going for 4500 USD.
- [https://youtu.be/9aOLwjUZLm0?t=1584](https://youtu.be/9aOLwjUZLm0?t=1584) Cirac and Zoller proposed the idea of using entangled ions soon after they heard about [Shor's algorithm](shor-s-algorithm.md) in 1995
- [https://youtu.be/9aOLwjUZLm0?t=1641](https://youtu.be/9aOLwjUZLm0?t=1641) you use [optical tweezers](optical-tweezers.md) to move the pairs of ions you want to entangle. This means shining a [laser](laser.md) on two ions at the same time. Their movement depends on their [spin](spin-physics.md), which is already in a superposition. If both move up, their distance stats the same, so the [Coulomb interaction](coulomb-s-law.md) is unchanged. But if they are different, then one goes up and the other down, distance increases due to the diagonal, and energy is lower.
- [https://youtu.be/9aOLwjUZLm0?t=1939](https://youtu.be/9aOLwjUZLm0?t=1939) S. Debnah 2016 Nature experiment with a pentagon. Well, it is not a pentagon, they are just in a linear chain, the pentagon is just to convey the full connectivity. Maybe also [Satanism](satanism.md). Anyways. This point also mentions usage of an [acousto-optic modulator](acousto-optic-modulator.md) to select which atoms we want to act on. On the other side, a simpler wide laser is used that hits all atoms ([optical tweezers](optical-tweezers.md) are literally like tweezers in the sense that you use two lasers). Later on mentions that the modulator is from Harris, later merged with L3, so: [https://www.l3harris.com/all-capabilities/acousto-optic-solutions](https://www.l3harris.com/all-capabilities/acousto-optic-solutions)
- [https://youtu.be/9aOLwjUZLm0?t=2119](https://youtu.be/9aOLwjUZLm0?t=2119) [Bernstein-Vazirani algorithm](bernstein-vazirani-algorithm.md). This to illustrate better connectivity of their ion approach compared to an [IBM quantum computer](ibm-quantum-computer.md), which is a [superconducting quantum computer](superconducting-quantum-computing.md)
- [https://youtu.be/9aOLwjUZLm0?t=2354](https://youtu.be/9aOLwjUZLm0?t=2354) [hidden shift algorithm](hidden-shift-algorithm.md)
- [https://youtu.be/9aOLwjUZLm0?t=2740](https://youtu.be/9aOLwjUZLm0?t=2740) Zhang et al. Nature 2017 paper about a 53 ion system that calculates something that cannot be classically calculated. Not fully controllable though, so more of a [continuous-variable quantum information](continuous-variable-quantum-information.md) operation.
- [https://youtu.be/9aOLwjUZLm0?t=2923](https://youtu.be/9aOLwjUZLm0?t=2923) usage of cooling to 4 K to get lower pressures on top of vacuum. Before this point all experiments were room temperature. Shows image of refrigerator labelled Janis cooler, presumably something like: [https://qd-uki.co.uk/cryogenics/janis-recirculating-gas-coolers/](https://qd-uki.co.uk/cryogenics/janis-recirculating-gas-coolers/)
- [https://youtu.be/9aOLwjUZLm0?t=2962](https://youtu.be/9aOLwjUZLm0?t=2962) qubit vs gates plot by H. Neven
- [https://youtu.be/9aOLwjUZLm0?t=3108](https://youtu.be/9aOLwjUZLm0?t=3108) [modular trapped ion quantum computer](modular-trapped-ion-quantum-computer.md) ideas. Mentions experiment with 2 separate systems with optical link. Miniaturization and their black box. Mentions again that their chip is from [Sandia](sandia-national-laboratories.md). Amazing how you pronounce that.

---

## ↑ Ancestors (11)

1. [Organization developing trapped ion quantum computer](organization-developing-trapped-ion-quantum-computer.md)
2. [Trapped ion quantum computer](trapped-ion-quantum-computer.md)
3. [Quantum computer physical implementation](quantum-computer-physical-implementation.md)
4. [Quantum computing hardware](quantum-computing-hardware.md)
5. [Quantum computing](quantum-computing-split.md)
6. [Quantum information](quantum-information.md)
7. [Information](information.md)
8. [Information technology](information-technology.md)
9. [Area of technology](area-of-technology.md)
10. [Technology](technology-split.md)
11. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (2)

- [Algorithmic qubits](algorithmic-qubits.md)
- [IonQ](ionq.md)
