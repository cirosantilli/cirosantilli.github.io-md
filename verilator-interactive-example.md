# Verilator interactive example

↑ **Parent:** [Verilator](verilator.md)

The example under [verilog/interactive](verilog/interactive) showcases how to create a simple interactive visual [Verilog](verilog.md) example using [Verilator](verilator.md) and [SDL](simple-directmedia-layer.md).

![](https://raw.githubusercontent.com/cirosantilli/media/master/verilog-interactive.gif)

You could e.g. expand such an example to create a simple (or complex) [video game](video-game-split.md) for example if you were insane enough. But please don't waste your time doing that, [Ciro Santilli begs you](backward-design.md).

The example is also described at: [https://stackoverflow.com/questions/38108243/is-it-possible-to-do-interactive-user-input-and-output-simulation-in-vhdl-or-ver/38174654#38174654](https://stackoverflow.com/questions/38108243/is-it-possible-to-do-interactive-user-input-and-output-simulation-in-vhdl-or-ver/38174654#38174654)

Usage: install dependencies:
```
sudo apt install libsdl2-dev verilator
```
then run as either:
```
make run RUN=and2
make run RUN=move
```
Tested on Verilator 4.038, Ubuntu 22.04.

File overview:
- and2
  - [verilog/interactive/and2.cpp](verilog/interactive/and2.cpp)
  - [verilog/interactive/and2.v](verilog/interactive/and2.v)
- move
  - [verilog/interactive/move.cpp](verilog/interactive/move.cpp)
  - [verilog/interactive/move.v](verilog/interactive/move.v)
- [verilog/interactive/display.cpp](verilog/interactive/display.cpp)

In those examples, the more interesting application specific logic is delegated to Verilog (e.g.: move game character on map), while boring timing and display matters can be handled by SDL and C++.

## ↑ Ancestors (9)

1. [Verilator](verilator.md)
2. [Verilog](verilog.md)
3. [Register transfer level](register-transfer-level.md)
4. [Computer hardware](computer-hardware-split.md)
5. [Computer](computer-split.md)
6. [Information technology](information-technology.md)
7. [Area of technology](area-of-technology.md)
8. [Technology](technology-split.md)
9. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (1)

- [The best articles by Ciro Santilli](articles-split.md)
