# Power, performance and area

↑ **Parent:** [Semiconductor device fabrication](semiconductor-device-fabrication.md)

[https://en.wikichip.org/wiki/power-performance-area](https://en.wikichip.org/wiki/power-performance-area)

This is the mantra of the [semiconductor industry](semiconductor-industry.md):
- power and area are the main limiting factors of chips, i.e., your budget:
  - chip area is ultra expensive because there are sporadic errors in the fabrication process, and each error in any part of the chip can potentially break the entire chip. Although there are 

    The percentage of working chips is called the yield.

    In some cases however, e.g. if the error only affects single CPU of a multi-core CPU, then they actually deactivate the broken CPU after testing, and sell the worse CPU cheaper with a clear branding of that: this is called binning [https://www.tomshardware.com/uk/reviews/glossary-binning-definition,5892.html](https://www.tomshardware.com/uk/reviews/glossary-binning-definition,5892.html)
  - power is a major semiconductor limit as of 2010's and onwards. If everything turns on at once, the chip would burn. Designs have to account for that.
- performance is the goal.

  Conceptually, this is basically a set of algorithms that you want your hardware to solve, each one with a respective weight of importance.

  Serial performance is fundamentally limited by the [longest path](critical-path.md) that electrons have to travel in a given clock cycle.

  The way to work around it is to create pipelines, splitting up single operations into multiple smaller operations, and storing intermediate results in memories.

## ↑ Ancestors (7)

1. [Semiconductor device fabrication](semiconductor-device-fabrication.md)
2. [Computer hardware](computer-hardware-split.md)
3. [Computer](computer-split.md)
4. [Information technology](information-technology.md)
5. [Area of technology](area-of-technology.md)
6. [Technology](technology-split.md)
7. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (2)

- [How computers work?](how-computers-work.md)
- [Standard cell library](standard-cell-library.md)
