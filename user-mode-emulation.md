# User mode emulation

↑ **Parent:** [QEMU](qemu.md)

[User mode emulation](user-mode-emulation.md) refers to the ability of certain [emulators](emulator.md) to emulate userland code running on top of a specific [operating system](operating-system.md), usually [Linux](linux.md).

For example, [QEMU](qemu.md) allows you to run a variety of userland [ELF](executable-and-linkable-format.md) programs directly on it, without an underlying [Linux kernel](linux-kernel.md) running.

User mode emulation is achieved by implementing [system calls](system-call.md) and special filesystems such as `/dev` manually on the emulator one by one.

The general tradeoff is that simulation is less acurate as it may lack certain highly advanced kernel functionality you haven't implemented yet. But it is much easier to run executables with it, and you don't have to wait for boot to finish before running, you just run executables directly from the command line.

## ↑ Ancestors (11)

1. [QEMU](qemu.md)
2. [List of emulators](list-of-emulators.md)
3. [Emulator](emulator.md)
4. [Virtualization](virtualization.md)
5. [Systems programming](systems-programming-split.md)
6. [Software](software-split.md)
7. [Computer](computer-split.md)
8. [Information technology](information-technology.md)
9. [Area of technology](area-of-technology.md)
10. [Technology](technology-split.md)
11. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (2)

- [QEMU JavaScript port](qemu-javascript-port.md)
- [User mode emulation](user-mode-emulation.md)
