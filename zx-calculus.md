# ZX-calculus

↑ **Parent:** [Quantum computing](quantum-computing-split.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/ZX-calculus)

As [https://en.wikipedia.org/w/index.php?title=ZX-calculus&oldid=1071329204#Diagram_rewriting](https://en.wikipedia.org/w/index.php?title=ZX-calculus&oldid=1071329204#Diagram_rewriting) tries to explain [but fails to deliver as usual](ourbigbook-com/wikipedia.md) consider the [GHZ state](quantum-memory.md) represented as a quantum circuit.

How can we easily prove that that quantum circuit equals the state:

$$
\frac{|000> + |111>}{\sqrt{2}}
$$

?

The naive way would be to just do the matrix multiplication as explained at [Section "Quantum computing is just matrix multiplication"](programmer-s-model-of-quantum-computers.md).

However, ZX-calculus provides a simpler way.

And even more importantly, sometimes it is the only way, because in a real circuit, we would not be able to do the matrix multiplication 

What we do in ZX-calculus is we first transform the original quantum circuit into a ZX graph.

This is always possible, because we can describe how to do the conversion simply for any of the [Clifford plus T](clifford-plus-t.md) gates, which is a set of [universal quantum gates](universal-quantum-gates.md).

Then, after we do this transformation, we can start applying further transformations that simplify the circuit.

It has already been proven that there is no efficient algorithm for this (TODO source, someone said P-sharp complete best case)

But it has been proven in 2017 that any possible equivalence between quantum circuits can be reached by modifying ZX-calculus circuits.

There are only 7 transformation rules that we need, and all others can be derived from those, universality.

So, we can apply those rules to do [the transformation shown in Wikipedia](https://en.wikipedia.org/w/index.php?title=ZX-calculus&oldid=1071329204#Diagram_rewriting):

<a id="image-ghz-circuit-as-zx-diagram"></a>
<img src="https://upload.wikimedia.org/wikipedia/commons/0/05/GHZ_circuit_as_ZX-diagram.svg" alt="" height="500">

**[Figure 10](#image-ghz-circuit-as-zx-diagram). GHZ circuit as ZX-diagram**. [Source](https://commons.wikimedia.org/wiki/File:GHZ_circuit_as_ZX-diagram.svg).

and one of those rules finally tells us that that last graph means our desired state:

$$
\frac{|000> + |111>}{\sqrt{2}}
$$

because it is a Z spider with $m = 3$ and $n = 1$.

<a id="video-working-with-pyzx-by-aleks-kissinger-2019"></a>
**[Video 49](#video-working-with-pyzx-by-aleks-kissinger-2019). Working with PyZX by Aleks Kissinger (2019)** [Source](https://www.youtube.com/watch?v=JafI_LZts2g). This video appears to give amazing motivation on why you should care about [ZX-calculus](zx-calculus.md), it mentions
- [quantum compilation](quantum-compilation.md)
- [quantum computer simulation](quantum-computer-simulator.md)

---

Bibliography:
- [https://quantumcomputing.stackexchange.com/questions/9774/what-are-some-applications-of-the-zx-calculus](https://quantumcomputing.stackexchange.com/questions/9774/what-are-some-applications-of-the-zx-calculus)
- [https://github.com/zxcalc/book](https://github.com/zxcalc/book) Picturing Quantum Software by [Aleks Kissinger](https://ourbigbook.com/go/topic/aleks-kissinger) and [John van de Wetering](https://ourbigbook.com/go/topic/john-van-de-wetering) (2024), [CC BY-NC-SA](cc-by-nc-sa.md).

**Table of contents**

- [ZX-calculus biliography](zx-calculus-biliography.md)
  - [Picturing Quantum Processes](picturing-quantum-processes.md)
- [PyZX](pyzx.md)

## 🏷️ Tagged (2)

- [Quantum Processes and Computation course of the University of Oxford](quantum-processes-and-computation-course-of-the-university-of-oxford.md)
- [Quantum Software course of the University of Oxford](quantum-software-course-of-the-university-of-oxford.md)

## ↑ Ancestors (7)

1. [Quantum computing](quantum-computing-split.md)
2. [Quantum information](quantum-information.md)
3. [Information](information.md)
4. [Information technology](information-technology.md)
5. [Area of technology](area-of-technology.md)
6. [Technology](technology-split.md)
7. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (4)

- [Quantum logic gates are needed for physical implementation](quantum-logic-gates-are-needed-for-physical-implementation.md)
- [Quantum Processes and Computation course of the University of Oxford](quantum-processes-and-computation-course-of-the-university-of-oxford.md)
- [Quantum Software course of the University of Oxford](quantum-software-course-of-the-university-of-oxford.md)
- [ZX-calculus](zx-calculus.md)
