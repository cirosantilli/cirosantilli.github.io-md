# How computers work?

↑ **Parent:** [Computer](computer-split.md)  
🏷️ **Tags:** [Essays by Ciro Santilli](essays-by-ciro-santilli.md)

A computer is a highly layered system, and so you have to decide which layers you are the most interested in studying.

Although the layer are somewhat independent, they also sometimes interact, and when that happens it usually hurts your brain. E.g., if [compilers](compiler.md) were perfect, no one optimizing software would have to know anything about [microarchitecture](microarchitecture.md). But if you want to go hardcore enough, you might have to learn some lower layer.

It must also be said that like in any industry, certain layers are hidden in commercial secrecy mysteries making it harder to actually learn them. In computing, the lower level you go, the more [closed source](closed-source-software.md) things tend to become.

But as you climb down into the abyss of low level hardcoreness, don't forget that [making usefulness is more important than being hardcore](backward-design.md): [Figure 1. "xkcd 378: Real Programmers"](#image-xkcd-378-real-programmers).

First, the most important thing you should know about this subject: [https://cirosantilli.com/linux-kernel-module-cheat/should-you-waste-your-life-with-systems-programming](https://cirosantilli.com/linux-kernel-module-cheat/should-you-waste-your-life-with-systems-programming)

Here's a summary from low-level to high-level:
- [semiconductor physical implementation](semiconductor-device-fabrication.md) this level is of course the most closed, but it is fun to try and peek into it from any openings given by commercials and academia:
  - [photolithography](photolithography.md), and notably [photomask](photomask.md) design
- [register transfer level](register-transfer-level.md)
  - interactive [Verilator](verilator.md) fun: [Is it possible to do interactive user input and output simulation in VHDL or Verilog?](https://stackoverflow.com/questions/38108243/is-it-possible-to-do-interactive-user-input-and-output-simulation-in-vhdl-or-ver/38174654#38174654)
  - more importantly, and much harder/maybe impossible with [open source](open-source-software.md), would be to try and set up a open source [standard cell library](standard-cell-library.md) and supporting software to obtain [power, performance and area](power-performance-and-area.md) estimates
    - [Are there good open source standard cell libraries to learn IC synthesis with EDA tools?](https://www.quora.com/Are-there-good-open-source-standard-cell-libraries-to-learn-IC-synthesis-with-EDA-tools/answer/Ciro-Santilli) on [Quora](quora.md)
    - the most open source ones are some initiatives targeting FPGAs, e.g. [https://symbiflow.github.io/](https://symbiflow.github.io/), [http://www.clifford.at/icestorm/](http://www.clifford.at/icestorm/)
    - [qflow](qflow.md) is an initiative targeting actual [integrated circuits](integrated-circuit.md)
- [microarchitecture](microarchitecture.md): a good way to play with this is to try and run some minimal userland examples on [gem5](gem5.md) userland simulation with logging, e.g. see on the [Linux Kernel Module Cheat](linux-kernel-module-cheat-split.md):
  - [https://cirosantilli.com/linux-kernel-module-cheat/gem5-event-queue-derivo3cpu-syscall-emulation-freestanding-example-analysis](https://cirosantilli.com/linux-kernel-module-cheat/gem5-event-queue-derivo3cpu-syscall-emulation-freestanding-example-analysis)
  This should be done at the same time as books/website/courses that explain the microarchitecture basics.

  This is the level of abstraction that [Ciro Santilli](ciro-santilli-split.md) finds the most interesting of the hardware stack. Learning it for actual [CPUs](central-processing-unit.md) (which as of 2020 is only partially documented by vendors) could actually be useful in hardcore software optimization use cases.
- [instruction set architecture](instruction-set-architecture.md): a good approach to learn this is to manually write some userland assembly with assertions as done in the [Linux Kernel Module Cheat](linux-kernel-module-cheat-split.md) e.g. at:
  - [https://github.com/cirosantilli/linux-kernel-module-cheat/blob/9b6552ab6c66cb14d531eff903c4e78f3561e9ca/userland/arch/x86_64/add.S](https://github.com/cirosantilli/linux-kernel-module-cheat/blob/9b6552ab6c66cb14d531eff903c4e78f3561e9ca/userland/arch/x86_64/add.S)
  - [https://cirosantilli.com/linux-kernel-module-cheat/x86-userland-assembly](https://cirosantilli.com/linux-kernel-module-cheat/x86-userland-assembly)
  - learn a bit about calling conventions, e.g. by calling C standard library functions from assembly:
    - [https://github.com/cirosantilli/linux-kernel-module-cheat/blob/9b6552ab6c66cb14d531eff903c4e78f3561e9ca/userland/arch/aarch64/inline_asm/linux/asm_from_c.c](https://github.com/cirosantilli/linux-kernel-module-cheat/blob/9b6552ab6c66cb14d531eff903c4e78f3561e9ca/userland/arch/aarch64/inline_asm/linux/asm_from_c.c)
    - [Calling C functions from x86 assembly language](https://stackoverflow.com/questions/16255608/calling-c-functions-from-x86-assembly-language/56328708#56328708)
  - you can also try and understand what some simple [C](c-programming-language.md) programs [compile](compiler.md) to. Things can get a bit hard though when `-O3` is used. Some cute examples:
    - [What is tail call optimization?](https://stackoverflow.com/questions/310974/what-is-tail-call-optimization/55230417#55230417)
    - [What is the "Stack smashing detected" error in GCC and how to solve it?](https://stackoverflow.com/questions/1345670/stack-smashing-detected/51897264#51897264)
    - [Realistic usage of the C99 'restrict' keyword?](https://stackoverflow.com/questions/745870/realistic-usage-of-the-c99-restrict-keyword/30827311#30827311)
- [executable file format](executable-file-format.md), notably [executable and Linkable Format](executable-and-linkable-format.md). Particularly important is to understand the basics of:
  - address relocation:  [How do linkers and address relocation work?](https://stackoverflow.com/questions/3322911/what-do-linkers-do/33690144#33690144)
  - position independent code: [What is the -fPIE option for position-independent executables in GCC and ld?](https://stackoverflow.com/questions/2463150/what-is-the-fpie-option-for-position-independent-executables-in-gcc-and-ld/51308031#51308031)
  - how to observe which symbols are present in object files, e.g.:
    - how C++ uses name mangling [What is the effect of extern "C" in C++?](https://stackoverflow.com/questions/1041866/what-is-the-effect-of-extern-c-in-c/30526795#30526795)
    - how C++ template instantiation can help reduce link time and size: [Explicit template instantiation - when is it used?](https://stackoverflow.com/questions/2351148/explicit-template-instantiation-when-is-it-used/59614755#59614755)
- [operating system](operating-system.md). There are two ways to approach this:
  - learn about the Linux kernel [Linux kernel](linux-kernel.md). A good starting point is to learn about its main interfaces. This is well shown at [Linux Kernel Module Cheat](linux-kernel-module-cheat-split.md):
    - system calls
      - write some system calls in
        - pure assembly:
          - [https://github.com/cirosantilli/linux-kernel-module-cheat/blob/9b6552ab6c66cb14d531eff903c4e78f3561e9ca/userland/arch/x86_64/freestanding/linux/hello.S](https://github.com/cirosantilli/linux-kernel-module-cheat/blob/9b6552ab6c66cb14d531eff903c4e78f3561e9ca/userland/arch/x86_64/freestanding/linux/hello.S)
          - [How should strace be used?](https://stackoverflow.com/questions/174942/how-should-strace-be-used/55397255#55397255)
        - C GCC inline assembly:
          - [https://stackoverflow.com/questions/9506353/how-to-invoke-a-system-call-via-syscall-or-sysenter-in-inline-assembly/54956854#54956854](https://stackoverflow.com/questions/9506353/how-to-invoke-a-system-call-via-syscall-or-sysenter-in-inline-assembly/54956854#54956854)
          - [https://github.com/cirosantilli/linux-kernel-module-cheat/blob/9b6552ab6c66cb14d531eff903c4e78f3561e9ca/userland/arch/x86_64/inline_asm/freestanding/linux/hello.c](https://github.com/cirosantilli/linux-kernel-module-cheat/blob/9b6552ab6c66cb14d531eff903c4e78f3561e9ca/userland/arch/x86_64/inline_asm/freestanding/linux/hello.c)
    - learn about kernel modules and their interfaces. Notably, learn about to demystify special files such `/dev/random` and so on:
      - [https://stackoverflow.com/questions/22632713/how-to-write-a-simple-linux-device-driver/44640466#44640466](https://stackoverflow.com/questions/22632713/how-to-write-a-simple-linux-device-driver/44640466#44640466)
      - [https://github.com/cirosantilli/linux-kernel-module-cheat/tree/9b6552ab6c66cb14d531eff903c4e78f3561e9ca/kernel_modules](https://github.com/cirosantilli/linux-kernel-module-cheat/tree/9b6552ab6c66cb14d531eff903c4e78f3561e9ca/kernel_modules)
    - learn how to do a minimal Linux kernel disk image/boot to userland hello world: [What is the smallest possible Linux implementation?](https://unix.stackexchange.com/questions/2692/what-is-the-smallest-possible-linux-implementation/203902#203902)
    - learn how to GDB [Step debug the Linux kernel](step-debug-the-linux-kernel.md) itself. Once you know this, you will feel that "given enough patience, I could understand anything that I wanted about the kernel", and you can then proceed to not learn almost anything about it and carry on with your life
  - write your own (mini-) OS, or study a minimal educational OS, e.g. as in:
    - [x86 bare metal examples](x86-bare-metal-examples-split.md)
    - [https://stackoverflow.com/questions/22054578/how-to-run-a-program-without-an-operating-system/32483545#32483545](https://stackoverflow.com/questions/22054578/how-to-run-a-program-without-an-operating-system/32483545#32483545)
- [programming language](programming-language-split.md)

<a id="image-xkcd-378-real-programmers"></a>
<img src="https://web.archive.org/web/20191222121520if_/http://imgs.xkcd.com/comics/real_programmers.png" alt="" height="600">

**[Figure 1](#image-xkcd-378-real-programmers). xkcd 378: Real Programmers**. [Source](https://xkcd.com/378/).

<a id="video-how-low-can-you-go-video-by-ciro-santilli-2017"></a>
**[Video 3](#video-how-low-can-you-go-video-by-ciro-santilli-2017). How low can you go video by Ciro Santilli (2017)** [Source](https://youtube.com/watch?v=_6D05gCWh_I). In this infamous video Ciro has summarized the computer hierarchy.

**Table of contents**

- [The lower level you go into a computer, the harder it is to observe things](the-lower-level-you-go-into-a-computer-the-harder-it-is-to-observe-things.md)
  - [Instrumentation (computer programming)](instrumentation-computer-programming.md)
- [Computer architecture](computer-architecture.md)

## ↑ Ancestors (5)

1. [Computer](computer-split.md)
2. [Information technology](information-technology.md)
3. [Area of technology](area-of-technology.md)
4. [Technology](technology-split.md)
5. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (1)

- [Molecular biology feels like systems programming](molecular-biology-feels-like-systems-programming.md)
