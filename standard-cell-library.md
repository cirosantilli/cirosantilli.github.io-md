# Standard cell library

↑ **Parent:** [Semiconductor device fabrication](semiconductor-device-fabrication.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Standard_cell_library)

Basically what [register transfer level](register-transfer-level.md) compiles to in order to achieve a real chip implementation.

After this is done, the final step is [place and route](place-and-route.md).

They can be designed by third parties besides the [semiconductor fabrication plants](semiconductor-fabrication-plant.md). E.g. [Arm Ltd.](arm-company.md) markets its [Artisan](arm-artisan.md) Standard Cell Libraries as mentioned e.g. at: [https://web.archive.org/web/20211007050341/https://developer.arm.com/ip-products/physical-ip/logic](https://web.archive.org/web/20211007050341/https://developer.arm.com/ip-products/physical-ip/logic) This came from a 2004 acquisition: [https://www.eetimes.com/arm-to-acquire-artisan-components-for-913-million/](https://www.eetimes.com/arm-to-acquire-artisan-components-for-913-million/), [obviously](if-a-product-of-a-big-company-has-a-catchy-name-it-came-from-an-acquisition.md).

The standard cell library is typically composed of a bunch of versions of somewhat simple gates, e.g.:
- AND with 2 inputs
- AND with 3 inputs
- AND with 4 inputs
- OR with 2 inputs
- OR with 3 inputs
and so on.

Each of those gates has to be designed by hand as a [3D](real-coordinate-space-of-dimension-three.md) structure that can be produced in a given [fab](semiconductor-fabrication-plant.md).

Simulations are then carried out, and the electric properties of those structures are characterized in a standard way as a bunch of tables of numbers that specify things like:
- how long it takes for electrons to pass through
- how much heat it produces
Those are then used in [power, performance and area](power-performance-and-area.md) estimates.

**Table of contents**

- [Open source standard cell library](open-source-standard-cell-library.md)

## ↑ Ancestors (7)

1. [Semiconductor device fabrication](semiconductor-device-fabrication.md)
2. [Computer hardware](computer-hardware-split.md)
3. [Computer](computer-split.md)
4. [Information technology](information-technology.md)
5. [Area of technology](area-of-technology.md)
6. [Technology](technology-split.md)
7. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (6)

- [CIDARLAB/cello](cidarlab-cello.md)
- [Electronic design automation](electronic-design-automation.md)
- [How computers work?](how-computers-work.md)
- [Logic synthesis](logic-synthesis.md)
- [Place and route](place-and-route.md)
- [Register transfer level](register-transfer-level.md)
