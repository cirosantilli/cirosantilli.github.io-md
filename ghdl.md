# GHDL

↑ **Parent:** [VHDL](vhdl.md)

[https://github.com/ghdl/ghdl](https://github.com/ghdl/ghdl)

Examples under [vhdl](vhdl).

First install [GHDL](ghdl.md). On [Ubuntu](ubuntu.md):
```
sudo apt install verilator
```
Tested on Verilator 1.0.0, [Ubuntu 22.04](ubuntu-22-04.md).

Run all examples, which have assertions in them:
```
cd vhdl
./run
```

Files:
- Examples
  - Basic
    - [vhdl/hello_world_tb.vhdl](vhdl/hello_world_tb.vhdl): hello world
    - [vhdl/min_tb.vhdl](vhdl/min_tb.vhdl): min
    - [vhdl/assert_tb.vhdl](vhdl/assert_tb.vhdl): assert
  - Lexer
    - [vhdl/comments_tb.vhdl](vhdl/comments_tb.vhdl): comments
    - [vhdl/case_insensitive_tb.vhdl](vhdl/case_insensitive_tb.vhdl): case insensitive
    - [vhdl/whitespace_tb.vhdl](vhdl/whitespace_tb.vhdl): whitespace
    - [vhdl/literals_tb.vhdl](vhdl/literals_tb.vhdl): literals
  - Flow control
    - [vhdl/procedure_tb.vhdl](vhdl/procedure_tb.vhdl): procedure
    - [vhdl/function_tb.vhdl](vhdl/function_tb.vhdl): function
  - [vhdl/operators_tb.vhdl](vhdl/operators_tb.vhdl): operators
  - Types
    - [vhdl/integer_types_tb.vhdl](vhdl/integer_types_tb.vhdl): integer types
    - [vhdl/array_tb.vhdl](vhdl/array_tb.vhdl): array
    - [vhdl/record_tb.vhdl.bak](vhdl/record_tb.vhdl.bak): record. TODO fails with "GHDL Bug occurred" on GHDL 1.0.0
    - [vhdl/generic_tb.vhdl](vhdl/generic_tb.vhdl): generic
  - [vhdl/package_test_tb.vhdl](vhdl/package_test_tb.vhdl): Packages
    - [vhdl/standard_package_tb.vhdl](vhdl/standard_package_tb.vhdl): standard package
    - textio  
        \* [vhdl/write_tb.vhdl](vhdl/write_tb.vhdl): write  
        \* [vhdl/read_tb.vhdl](vhdl/read_tb.vhdl): read
    - [vhdl/std_logic_tb.vhdl](vhdl/std_logic_tb.vhdl): std\_logic
  - [vhdl/stop_delta_tb.vhdl](vhdl/stop_delta_tb.vhdl): `--stop-delta`
- Applications
  - Combinatoric
    - [vhdl/adder.vhdl](vhdl/adder.vhdl): adder
    - [vhdl/sqrt8_tb.vhdl](vhdl/sqrt8_tb.vhdl): sqrt8
  - Sequential
    - [vhdl/clock_tb.vhdl](vhdl/clock_tb.vhdl): clock
    - [vhdl/counter.vhdl](vhdl/counter.vhdl): counter
- Helpers  
    \* [vhdl/template_tb.vhdl](vhdl/template_tb.vhdl): template

## ↑ Ancestors (8)

1. [VHDL](vhdl.md)
2. [Register transfer level](register-transfer-level.md)
3. [Computer hardware](computer-hardware-split.md)
4. [Computer](computer-split.md)
5. [Information technology](information-technology.md)
6. [Area of technology](area-of-technology.md)
7. [Technology](technology-split.md)
8. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (3)

- [Merged by others](ciro-santilli-s-open-source-contributions/merged-by-others.md)
- [GHDL](ghdl.md)
- [VHDL](vhdl.md)
