<h1 id="_file/riscv/timer.S">riscv/timer.S</h1>

↑ **Parent:** [RISC-V timer](../../risc-v-timer.md)

TODO: the interrupt is firing only once:
- [https://www.reddit.com/r/RISCV/comments/ov4vhh/timer_interrupt/](https://www.reddit.com/r/RISCV/comments/ov4vhh/timer_interrupt/)

Adapted from: [https://danielmangum.com/posts/risc-v-bytes-timer-interrupts/](https://danielmangum.com/posts/risc-v-bytes-timer-interrupts/)

Tested on [Ubuntu 23.10](../../ubuntu-23-10.md):
```
sudo apt install binutils-riscv64-unknown-elf qemu-system-misc gdb-multiarch
cd riscv
make
```
Then on shell 1:
```
qemu-system-riscv64 -machine virt -cpu rv64 -smp 1 -s -S -nographic -bios none -kernel timer.elf
```
and on shell 2:
```
gdb-multiarch timer.elf -nh -ex "target remote :1234" -ex 'display /i $pc' -ex 'break *mtrap' -ex 'display *0x2004000' -ex 'display *0x200BFF8'
```
[GDB](../../gnu-debugger.md) should break infinitel many times on `mtrap` as interrupts happen.

## ↑ Ancestors (12)

1. [RISC-V timer](../../risc-v-timer.md)
2. [RISC-V](../../risc-v.md)
3. [List of instruction set architectures](../../list-of-instruction-set-architectures.md)
4. [Instruction set architecture](../../instruction-set-architecture.md)
5. [Processor (computing)](../../processor-computing.md)
6. [Computer hardware component type](../../computer-hardware-component-type.md)
7. [Computer hardware](../../computer-hardware-split.md)
8. [Computer](../../computer-split.md)
9. [Information technology](../../information-technology.md)
10. [Area of technology](../../area-of-technology.md)
11. [Technology](../../technology-split.md)
12. [Ciro Santilli's Homepage](../../split.md)
