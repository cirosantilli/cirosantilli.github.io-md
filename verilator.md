# Verilator

↑ **Parent:** [Verilog](verilog.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Verilator)

[Verilog](verilog.md) simulator that [transpiles](source-to-source-compiler.md) to [C++](c-plus-plus.md).

One very good thing about this is that it makes it easy to create test cases directly in C++. You just supply inputs and clock the simulation directly in a C++ loop, then read outputs and assert them with `assert()`. And you can inspect variables by printing them or with GDB. This is infinitely more convenient than doing these IO-type tasks in [Verilog](verilog.md) itself.

Some simulation examples under [verilog](verilog).

First install [Verilator](verilator.md). On [Ubuntu](ubuntu.md):
```
sudo apt install verilator
```
Tested on Verilator 4.038, [Ubuntu 22.04](ubuntu-22-04.md).

Run all examples, which have assertions in them:
```
cd verilator
make run
```

File structure is for example:
- [verilog/counter.v](verilog/counter.v): [Verilog](verilog.md) file
- [verilog/counter.cpp](verilog/counter.cpp): [C++](c-plus-plus.md) loop which clocks the design and runs tests with assertions on the outputs
- [verilog/counter.params](verilog/counter.params): [gcc](gnu-compiler-collection.md) compilation flags for this example
- [verilog/counter_tb.v](verilog/counter_tb.v): [Verilog](verilog.md) version of the [C++](c-plus-plus.md) test. Not used by Verilator. Verilator can't actually run out `_tb` files, because they do in Verilog IO things that we do better from [C++](c-plus-plus.md) in Verilator, so Verilator didn't bother implementing them. This is a good thing.

Example list:
- [verilog/negator.v](verilog/negator.v), [verilog/negator.cpp](verilog/negator.cpp): the simplest non-identity combinatorial circuit!
- [verilog/counter.v](verilog/counter.v), [verilog/counter.cpp](verilog/counter.cpp): sequential hello world. Synchronous active high reset with active high enable signal. Adapted from: [http://www.asic-world.com/verilog/first1.html](http://www.asic-world.com/verilog/first1.html)
- [verilog/subleq.v](verilog/subleq.v), [verilog/subleq.cpp](verilog/subleq.cpp): subleq [one instruction set computer](one-instruction-set-computer.md) with separated instruction and data RAMs

**Table of contents**

- [Verilator interactive example](verilator-interactive-example.md)

## ↑ Ancestors (8)

1. [Verilog](verilog.md)
2. [Register transfer level](register-transfer-level.md)
3. [Computer hardware](computer-hardware-split.md)
4. [Computer](computer-split.md)
5. [Information technology](information-technology.md)
6. [Area of technology](area-of-technology.md)
7. [Technology](technology-split.md)
8. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (5)

- [The best articles by Ciro Santilli](articles-split.md)
- [How computers work?](how-computers-work.md)
- [Verilator](verilator.md)
- [Verilator interactive example](verilator-interactive-example.md)
- [Verilog](verilog.md)
