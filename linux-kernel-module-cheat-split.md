# Linux Kernel Module Cheat

↑ **Parent:** [The most important projects done by Ciro Santilli](the-most-important-projects-done-by-ciro-santilli-split.md)

[https://github.com/cirosantilli/linux-kernel-module-cheat](https://github.com/cirosantilli/linux-kernel-module-cheat)

[Dan Kaminsky approves Linux Kernel Module Cheat](dan-kaminsky-approves-linux-kernel-module-cheat.md).

This is the most important technical tutorial project that [Ciro Santilli](ciro-santilli-split.md) has done in his life so far as of 2019.

The scope is insane and unprecedented, and goes beyond [Linux kernel](linux-kernel.md)-land alone, which is where it started.

It ended up [eating](eating.md) every system programming content Ciro had previously written! Including:
- [C](c-programming-language.md), [C++](c-plus-plus.md), [POSIX](posix.md)
- [x86](x86.md) and arm userland assembly
- arm baremetal assembly. x86 baremetal is at: [https://github.com/cirosantilli/x86-bare-metal-examples](https://github.com/cirosantilli/x86-bare-metal-examples) and would in theory be migrated, but he's lazy
- [QEMU](qemu.md) and [gem5](gem5.md) emulation
so that that repo would better be called "System Programming Cheat". But "Linux Kernel Module Cheat" sounds more hardcore ;-)

Other major things that could be added there as well in the future are:
- [https://github.com/cirosantilli/algorithm-cheat](https://github.com/cirosantilli/algorithm-cheat)
- [computer architecture](computer-architecture.md) tutorials with [gem5](gem5.md)

Due to this project, some have [considered Ciro to be](https://github.com/cirosantilli/linux-kernel-module-cheat/issues/105#issuecomment-553220982) ([archive](https://web.archive.org/web/20191113151131/https://github.com/cirosantilli/linux-kernel-module-cheat/issues/105#issuecomment-553220982)):

> some kind of Linux kernel god.

which made Ciro smile, although "Linux kernel documenter [God](god.md)" would have been more precise.

<a id="code-terminal-dump-of-a-lkmc-session-with-two-tmux-panes-with-qemu-on-left-and-gdb-on-right-showing-a-backtrace-of-the-linux-kernel-code-currently-being-under-qemu"></a>
```
[    1.451857] input: AT Translated Set 2 keyboard as /devices/platform/i8042/s1│loading @0xffffffffc0000000: ../kernel_modules-1.0//timer.ko
[    1.454310] ledtrig-cpu: registered to indicate activity on CPUs             │(gdb) b lkmc_timer_callback
[    1.455621] usbcore: registered new interface driver usbhid                  │Breakpoint 1 at 0xffffffffc0000000: file /home/ciro/bak/git/linux-kernel-module
[    1.455811] usbhid: USB HID core driver                                      │-cheat/out/x86_64/buildroot/build/kernel_modules-1.0/./timer.c, line 28.
[    1.462044] NET: Registered protocol family 10                               │(gdb) c
[    1.467911] Segment Routing with IPv6                                        │Continuing.
[    1.468407] sit: IPv6, IPv4 and MPLS over IPv4 tunneling driver              │
[    1.470859] NET: Registered protocol family 17                               │Breakpoint 1, lkmc_timer_callback (data=0xffffffffc0002000 <mytimer>)
[    1.472017] 9pnet: Installing 9P2000 support                                 │    at /linux-kernel-module-cheat//out/x86_64/buildroot/build/
[    1.475461] sched_clock: Marking stable (1473574872, 0)->(1554017593, -80442)│kernel_modules-1.0/./timer.c:28
[    1.479419] ALSA device list:                                                │28      {
[    1.479567]   No soundcards found.                                           │(gdb) c
[    1.619187] ata2.00: ATAPI: QEMU DVD-ROM, 2.5+, max UDMA/100                 │Continuing.
[    1.622954] ata2.00: configured for MWDMA2                                   │
[    1.644048] scsi 1:0:0:0: CD-ROM            QEMU     QEMU DVD-ROM     2.5+ P5│Breakpoint 1, lkmc_timer_callback (data=0xffffffffc0002000 <mytimer>)
[    1.741966] tsc: Refined TSC clocksource calibration: 2904.010 MHz           │    at /linux-kernel-module-cheat//out/x86_64/buildroot/build/
[    1.742796] clocksource: tsc: mask: 0xffffffffffffffff max_cycles: 0x29dc0f4s│kernel_modules-1.0/./timer.c:28
[    1.743648] clocksource: Switched to clocksource tsc                         │28      {
[    2.072945] input: ImExPS/2 Generic Explorer Mouse as /devices/platform/i8043│(gdb) bt
[    2.078641] EXT4-fs (vda): couldn't mount as ext3 due to feature incompatibis│#0  lkmc_timer_callback (data=0xffffffffc0002000 <mytimer>)
[    2.080350] EXT4-fs (vda): mounting ext2 file system using the ext4 subsystem│    at /linux-kernel-module-cheat//out/x86_64/buildroot/build/
[    2.088978] EXT4-fs (vda): mounted filesystem without journal. Opts: (null)  │kernel_modules-1.0/./timer.c:28
[    2.089872] VFS: Mounted root (ext2 filesystem) readonly on device 254:0.    │#1  0xffffffff810ab494 in call_timer_fn (timer=0xffffffffc0002000 <mytimer>,
[    2.097168] devtmpfs: mounted                                                │    fn=0xffffffffc0000000 <lkmc_timer_callback>) at kernel/time/timer.c:1326
[    2.126472] Freeing unused kernel memory: 1264K                              │#2  0xffffffff810ab71f in expire_timers (head=<optimized out>,
[    2.126706] Write protecting the kernel read-only data: 16384k               │    base=<optimized out>) at kernel/time/timer.c:1363
[    2.129388] Freeing unused kernel memory: 2024K                              │#3  __run_timers (base=<optimized out>) at kernel/time/timer.c:1666
[    2.139370] Freeing unused kernel memory: 1284K                              │#4  run_timer_softirq (h=<optimized out>) at kernel/time/timer.c:1692
[    2.246231] EXT4-fs (vda): warning: mounting unchecked fs, running e2fsck isd│#5  0xffffffff81a000cc in __do_softirq () at kernel/softirq.c:285
[    2.259574] EXT4-fs (vda): re-mounted. Opts: block_validity,barrier,user_xatr│#6  0xffffffff810577cc in invoke_softirq () at kernel/softirq.c:365
hello S98                                                                       │#7  irq_exit () at kernel/softirq.c:405
                                                                                │#8  0xffffffff818021ba in exiting_irq () at ./arch/x86/include/asm/apic.h:541
Apr 15 23:59:23 login[49]: root login on 'console'                              │#9  smp_apic_timer_interrupt (regs=<optimized out>)
hello /root/.profile                                                            │    at arch/x86/kernel/apic/apic.c:1052
# insmod /timer.ko                                                              │#10 0xffffffff8180190f in apic_timer_interrupt ()
[    6.791945] timer: loading out-of-tree module taints kernel.                 │    at arch/x86/entry/entry_64.S:857
# [    7.821621] 4294894248                                                     │#11 0xffffffff82003df8 in init_thread_union ()
[    8.851385] 4294894504                                                       │#12 0x0000000000000000 in ?? ()
                                                                                │(gdb)
```

## ↑ Ancestors (3)

1. [The most important projects done by Ciro Santilli](the-most-important-projects-done-by-ciro-santilli-split.md)
2. [Ciro Santilli](ciro-santilli-split.md)
3. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (23)

- [Ciro Santilli's Homepage](split.md)
- [Test\_executables.js](_file/test_executables.js.md)
- [Assembly language](assembly-language.md)
- [Buildroot](buildroot.md)
- [Ciro Santilli's documentation superpowers](ciro-santilli-s-documentation-superpowers.md)
- [Computers](ciro-santilli-s-hardware/computers.md)
- [Computer security](computer-security.md)
- [Emulator](emulator.md)
- [High flying bird vs gophers](high-flying-bird-vs-gophers.md)
- [How computers work?](how-computers-work.md)
- [Linux](linux.md)
- [Linux insides](linux-insides.md)
- [Linux kernel](linux-kernel.md)
- [Molecular biology technologies](molecular-biology-technologies.md)
- [One page to rule them all](one-page-to-rule-them-all.md)
- [QEMU](qemu.md)
- [Systems programming](systems-programming-split.md)
- [Ubuntu](ubuntu.md)
- [I ended up doing tech rather than content as usual](updates/ourbigbook-project-update-march-2025/i-ended-up-doing-tech-rather-than-content-as-usual.md)
- [Post OurBigBook job search round 2025](updates/post-ourbigbook-job-search-round-2025.md)
- [Two Linux Kernel Module Cheat videos](updates/two-linux-kernel-module-cheat-videos.md)
- [Website front-end for a mathematical formal proof system](website-front-end-for-a-mathematical-formal-proof-system.md)
- [x86 bare metal examples](x86-bare-metal-examples-split.md)
