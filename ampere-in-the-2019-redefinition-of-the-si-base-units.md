# Ampere in the 2019 redefinition of the SI base units

↑ **Parent:** [Ampere](ampere.md)  
🏷️ **Tags:** [2019 redefinition of the SI base units](2019-redefinition-of-the-si-base-units.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Ampere_in_the_2019_redefinition_of_the_SI_base_units)

Starting in the [2019 redefinition of the SI base units](2019-redefinition-of-the-si-base-units.md), the [elementary charge](elementary-charge.md) is assigned a fixed number, and the Ampere is based on it and on the [second](second.md), which is beautiful.

This choice is not because we attempt to count individual [electrons](electron.md) going through a wire, as it would be far too many to count!

Rather, it is because because there are two crazy [quantum mechanical](quantum-mechanics-split.md) effects that give us macroscopic measures that are directly related to the electron charge. [https://www.nist.gov/si-redefinition/ampere/ampere-quantum-metrology-triangle](https://www.nist.gov/si-redefinition/ampere/ampere-quantum-metrology-triangle) by the [NIST](national-institute-of-standards-and-technology.md) explains that the two effects are:
- [quantum Hall effect](quantum-hall-effect.md), which has [discrete](discrete.md) [resistances](electrical-resistance.md) of type:$$
  R_{xy} = \frac{V_\text{Hall}}{I_\text{channel}} = \frac{h}{e^2\nu}
  $$

  for integer values of $\nu$.
- [Josephson effect](josephson-effect.md), used in the [Josephson voltage standard](josephson-voltage-standard.md). With the [Inverse AC Josephson effect](inverse-ac-josephson-effect.md) we are able to produce:

  $$
  K_{J} = \frac{2e}{h} V \cdot s
  $$

  per [Josephson junction](josephson-junction.md). This is about 2 microvolt / GHz, where GHz is a practical input frequency. [Video "The evolution of voltage metrology to the latest generation of JVSs by Alain Rüfenacht"](josephson-voltage-standard.md#video-the-evolution-of-voltage-metrology-to-the-latest-generation-of-jvss-by-alain-rufenacht) mentions that a typical operating frequency is 20 GHz.

  Therefore to attain a good 10 V, we need something in the order of a million [Josephson junctions](josephson-junction.md).

  But this is possible to implement in a single chip with existing micro fabrication techniques, and is exactly what the [Josephson voltage standard](josephson-voltage-standard.md) does!

Those effect work because they also involve dividing by the [Planck constant](planck-constant.md), the fundamental constant of [quantum mechanics](quantum-mechanics-split.md), which is also tiny, and thus brings values into a much more measurable order of size.

## ↑ Ancestors (9)

1. [Ampere](ampere.md)
2. [Unit of the International System of Units](unit-of-the-international-system-of-units.md)
3. [International System of Units](international-system-of-units.md)
4. [List of systems of units](list-of-systems-of-units.md)
5. [System of units](system-of-units-split.md)
6. [Physics](physics-split.md)
7. [Natural science](natural-science.md)
8. [Science](science-split.md)
9. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (4)

- [Ampere](ampere.md)
- [Applications of Josephson Junctions](applications-of-josephson-junctions.md)
- [Josephson voltage standard](josephson-voltage-standard.md)
- [Quantum Hall effect](quantum-hall-effect.md)
