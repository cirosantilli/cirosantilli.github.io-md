# Register transfer level

↑ **Parent:** [Computer hardware](computer-hardware-split.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Register_transfer_level)

Register transfer level is the abstraction level at which computer chips are mostly designed.

The only two truly relevant RTL languages as of 2020 are: [Verilog](verilog.md) and [VHDL](vhdl.md). Everything else compiles to those, because that's all that [EDA vendors](eda-company.md) support.

Much like a [C](c-programming-language.md) compiler abstracts away the [CPU](central-processing-unit.md) assembly to:
- increase portability across ISAs
- do optimizations that programmers can't feasibly do without going crazy

Compilers for RTL languages such as Verilog and [VHDL](vhdl.md) abstract away the details of the specific [semiconductor technology](semiconductor-device-fabrication.md) used for those exact same reasons.

The compilers essentially compile the RTL languages into a [standard cell library](standard-cell-library.md).

Examples of companies that work at this level include:
- [Intel](intel.md). Intel also has [semiconductor fabrication plants](semiconductor-fabrication-plant.md) however.
- [Arm](arm-company.md) which does not have [fabs](semiconductor-fabrication-plant.md), and is therefore called a "[fabless](fabless-manufacturing.md)" company.

**Table of contents**

- [High-level synthesis](high-level-synthesis.md)
- [Fabless manufacturing](fabless-manufacturing.md)
  - [Fabless semiconductor company](fabless-semiconductor-company.md)
- [Logic gate](logic-gate.md)
  - [Truth table](truth-table.md)
- [Verilog](verilog.md)
  - [Value change dump](value-change-dump.md)
  - [Verilator](verilator.md)
    - [Verilator interactive example](verilator-interactive-example.md)
- [VHDL](vhdl.md)
  - [GHDL](ghdl.md)

## ↑ Ancestors (6)

1. [Computer hardware](computer-hardware-split.md)
2. [Computer](computer-split.md)
3. [Information technology](information-technology.md)
4. [Area of technology](area-of-technology.md)
5. [Technology](technology-split.md)
6. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (9)

- [The best articles by Ciro Santilli](articles-split.md)
- [Electronic design automation](electronic-design-automation.md)
- [Fabless manufacturing](fabless-manufacturing.md)
- [High level quantum synthesis](high-level-quantum-synthesis.md)
- [How computers work?](how-computers-work.md)
- [Logic synthesis](logic-synthesis.md)
- [Programmer's model of quantum computers](programmer-s-model-of-quantum-computers.md)
- [Quantum circuits vs classical circuits](quantum-circuits-vs-classical-circuits.md)
- [Standard cell library](standard-cell-library.md)
