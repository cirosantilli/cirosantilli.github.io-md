# LLVM IR hello world

↑ **Parent:** [LLVM Intermediate Representation](llvm-intermediate-representation.md)

Example: [llvm/hello.ll](llvm/hello.ll) adapted from: [https://llvm.org/docs/LangRef.html#module-structure](https://llvm.org/docs/LangRef.html#module-structure) but without double newline.

To execute it as mentioned at [https://github.com/dfellis/llvm-hello-world](https://github.com/dfellis/llvm-hello-world) we can either use their crazy assembly interpreter, tested on [Ubuntu 22.10](ubuntu-22-10.md):
```
sudo apt install llvm-runtime
lli hello.ll
```
This seems to use `puts` from the [C standard library](c-standard-library.md).

Or we can [Lower](lower-compilation.md) it to [assembly](assembly-language.md) of the local machine:
```
sudo apt install llvm
llc hello.ll
```
which produces:
```
hello.s
```
and then we can assemble link and run with [gcc](gnu-compiler-collection.md):
```
gcc -o hello.out hello.s -no-pie
./hello.out
```
or with [clang](clang.md):
```
clang -o hello.out hello.s -no-pie
./hello.out
```
`hello.s` uses the [GNU GAS](gnu-assembler.md) format, which [clang](clang.md) is highly compatible with, so both should work in general.

## ↑ Ancestors (10)

1. [LLVM Intermediate Representation](llvm-intermediate-representation.md)
2. [LLVM](llvm.md)
3. [List of compilers](list-of-compilers.md)
4. [Compiler](compiler.md)
5. [Software](software-split.md)
6. [Computer](computer-split.md)
7. [Information technology](information-technology.md)
8. [Area of technology](area-of-technology.md)
9. [Technology](technology-split.md)
10. [Ciro Santilli's Homepage](split.md)
