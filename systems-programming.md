# Systems programming

↑ **Parent:** [Software](software.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Systems_programming)

[Ciro Santilli](ciro-santilli.md)'s definition: [https://softwareengineering.stackexchange.com/questions/151610/what-exactly-is-system-programming/399625#399625](https://softwareengineering.stackexchange.com/questions/151610/what-exactly-is-system-programming/399625#399625)

Ciro's tutorial: [Linux Kernel Module Cheat](the-most-important-projects-done-by-ciro-santilli.md#linux-kernel-module-cheat).

**Table of contents**

- [Being proud of low level programming is stupid](#being-proud-of-low-level-programming-is-stupid)
- [Bootloader](#bootloader)
- [Operating system](#operating-system)
  - [Operating system concept](#operating-system-concept)
    - [User and kernel space](#user-and-kernel-space)
      - [User space](#user-space)
      - [Kernel space](#kernel-space)
  - [Bare metal](#bare-metal)
  - [Driver (software)](#driver-software)
  - [Embedded operating system](#embedded-operating-system)
    - [MicroPython](#micropython)
      - [Run MicroPython on X](#run-micropython-on-x)
      - [MicroPython example](#micropython-example)
        - [micropython/blink\_gpio.py](#_file/micropython/blink_gpio.py)
    - [Zephyr (operating system)](#zephyr-operating-system)
      - [Zephyr example](#zephyr-example)
        - [Zephyr non-official example](#zephyr-non-official-example)
        - [zephyr/blink\_gpio.c](#_file/zephyr/blink_gpio.c)
        - [Zephyr official example](#zephyr-official-example)
          - [Zephyr blinky example](#zephyr-blinky-example)
          - [Zephyr hello world example](#zephyr-hello-world-example)
      - [Run Zephyr on X](#run-zephyr-on-x)
        - [Run Zephyr on QEMU](#run-zephyr-on-qemu)
  - [Firmware](#firmware)
    - [BIOS](#bios)
  - [System call](#system-call)
  - [The three operating systems](#the-three-operating-systems)
  - [List of operating systems](#list-of-operating-systems)
    - [Linux](#linux)
      - [Tux (mascot)](#tux-mascot)
      - [Linux kernel](#linux-kernel)
        - [Linux kernel system](#linux-kernel-system)
        - [Linux kernel security system](#linux-kernel-security-system)
          - [Landlock (Linux kernel)](#landlock-linux-kernel)
        - [Linux Foundation](#linux-foundation)
        - [Linux kernel build output](#linux-kernel-build-output)
          - [vmlinux](#vmlinux)
        - [Step debug the Linux kernel](#step-debug-the-linux-kernel)
          - [JTAG](#jtag)
            - [Serial wire debug](#serial-wire-debug)
        - [Linux kernel bibliography](#linux-kernel-bibliography)
          - [Linux insides](#linux-insides)
          - [Linux Device Drivers book](#linux-device-drivers-book)
            - [Linux Device Drivers book edition](#linux-device-drivers-book-edition)
              - [Linux Device Drivers book 3rd edition](#linux-device-drivers-book-3rd-edition)
                - [martinezjavier/ldd3](#martinezjavier-ldd3)
      - [Linux distribution](#linux-distribution)
        - [Linux distribution buildable from source](#linux-distribution-buildable-from-source)
        - [Package manager](#package-manager)
        - [Cross distro package manager](#cross-distro-package-manager)
          - [AppImage](#appimage)
          - [Flatpak](#flatpak)
          - [Snap (package manager)](#snap-package-manager)
      - [List of Linux distributions](#list-of-linux-distributions)
        - [Android (operating system)](#android-operating-system)
          - [Android Open Source Project](#android-open-source-project)
          - [Transfer Android 11 camera videos to Ubuntu 20.10](#transfer-android-11-camera-videos-to-ubuntu-20-10)
          - [F-Droid](#f-droid)
        - [Arch Linux](#arch-linux)
        - [Buildroot](#buildroot)
          - [BusyBox](#busybox)
        - [NixOS](#nixos)
        - [Ubuntu](#ubuntu)
          - [Canonical (company)](#canonical-company)
          - [apport (software)](#apport-software)
            - [apport-cli](#apport-cli)
          - [Ubuntu HOWTO](#ubuntu-howto)
            - [Make a bug report for a crash on Ubuntu](#make-a-bug-report-for-a-crash-on-ubuntu)
            - [Find GPU information in Ubuntu](#find-gpu-information-in-ubuntu)
            - [How to report Ubuntu crashes](#how-to-report-ubuntu-crashes)
            - [Compile Linux kernel for Ubuntu](#compile-linux-kernel-for-ubuntu)
            - [Emulate Windows on Ubuntu](#emulate-windows-on-ubuntu)
          - [Ubuntu release](#ubuntu-release)
            - [Ubuntu 26.04](#ubuntu-26-04)
            - [Ubuntu 25.10](#ubuntu-25-10)
              - [Ubuntu 25.10 bug](#ubuntu-25-10-bug)
            - [Ubuntu 25.04](#ubuntu-25-04)
            - [Ubuntu 24.10](#ubuntu-24-10)
            - [Ubuntu 24.04](#ubuntu-24-04)
              - [Ubuntu 24.04 installer "Erase disk and install Ubuntu" doesn't work when BitLocker enabled](#ubuntu-24-04-installer-erase-disk-and-install-ubuntu-doesn-t-work-when-bitlocker-enabled)
              - [Ubuntu 24.04 "The application files has closed unexpectedly"](#ubuntu-24-04-the-application-files-has-closed-unexpectedly)
            - [Ubuntu 23.10](#ubuntu-23-10)
              - [gfx\_v11\_0\_priv\_reg\_irq: register access in command stream](#gfx-v11-0-priv-reg-irq-register-access-in-command-stream)
              - [Unable to lock screen on Ubuntu](#unable-to-lock-screen-on-ubuntu)
            - [Ubuntu 23.04](#ubuntu-23-04)
              - [Ubuntu 23.04 boot broken on kernel 6.2](#ubuntu-23-04-boot-broken-on-kernel-6-2)
            - [Ubuntu 22.10](#ubuntu-22-10)
            - [Ubuntu 22.04](#ubuntu-22-04)
              - [snap "Pending Update of" notifications](#snap-pending-update-of-notifications)
            - [Ubuntu 21.10](#ubuntu-21-10)
              - [Ubuntu 21.10 does not wake up from suspend](#ubuntu-21-10-does-not-wake-up-from-suspend)
            - [Ubuntu 21.04](#ubuntu-21-04)
            - [Ubuntu 20.04](#ubuntu-20-04)
            - [Ubuntu 18.04](#ubuntu-18-04)
            - [Ubuntu 16.04](#ubuntu-16-04)
          - [Ubuntu feature request](#ubuntu-feature-request)
            - [couldn't save system state: Minimum free space to take a snapshot and preserve ZFS performance is](#couldn-t-save-system-state-minimum-free-space-to-take-a-snapshot-and-preserve-zfs-performance-is)
            - [Hide top bar on Ubuntu](#hide-top-bar-on-ubuntu)
          - [Launchpad (website)](#launchpad-website)
    - [Berkeley Software Distribution](#berkeley-software-distribution)
      - [FreeBSD](#freebsd)
    - [TempleOS](#templeos)
      - [Terry A. Davis](#terry-a-davis)
  - [UNIX](#unix)
    - [POSIX](#posix)
      - [Environment variable](#environment-variable)
        - [POSIX environment variable](#posix-environment-variable)
          - [`PATH` environment variable](#path-environment-variable)
      - [GNU Core Utils](#gnu-core-utils)
        - [GNU Core Utils command line utility](#gnu-core-utils-command-line-utility)
          - [sha1sum](#sha1sum)
          - [shred (UNIX)](#shred-unix)
      - [Non-POSIX command line utility](#non-posix-command-line-utility)
      - [POSIX command line utility](#posix-command-line-utility)
      - [`diff`](#diff)
      - [`grep`](#grep)
        - [grep large binary files](#grep-large-binary-files)
        - [`bgrep`](#bgrep)
      - [`sed`](#sed)
      - [`wc` (unix)](#wc-unix)
      - [Standard streams](#standard-streams)
        - [Standard input](#standard-input)
        - [Standard output](#standard-output)
- [Executable file format](#executable-file-format)
  - [Executable and Linkable Format](#executable-and-linkable-format)
    - [ELF Hello World Tutorial](elf-hello-world.md)
      - [Introduction](elf-hello-world.md#introduction)
        - [Standards](elf-hello-world.md#standards)
        - [How to learn](elf-hello-world.md#how-to-learn)
        - [Specified file formats](elf-hello-world.md#specified-file-formats)
        - [Implementations](elf-hello-world.md#implementations)
      - [Minimal ELF file](elf-hello-world.md#minimal-elf-file)
      - [Generate the example](elf-hello-world.md#generate-the-example)
      - [Object hd](elf-hello-world.md#object-hd)
      - [Executable hd](elf-hello-world.md#executable-hd)
      - [Global file structure](elf-hello-world.md#global-file-structure)
      - [Section vs segment](elf-hello-world.md#section-vs-segment)
      - [ELF header](elf-hello-world.md#elf-header)
      - [Section header table](elf-hello-world.md#section-header-table)
      - [Sections](elf-hello-world.md#sections)
        - [Index 0 section](elf-hello-world.md#index-0-section)
          - [`SHT_NULL`](elf-hello-world.md#sht-null)
        - [`.data` section](elf-hello-world.md#data-section)
        - [`.text` section](elf-hello-world.md#text-section)
        - [`SHT_STRTAB`](elf-hello-world.md#sht-strtab)
        - [`.shstrtab`](elf-hello-world.md#shstrtab)
        - [`.symtab`](elf-hello-world.md#symtab)
          - [`STT_FILE`](elf-hello-world.md#stt-file)
          - [`STT_SECTION`](elf-hello-world.md#stt-section)
          - [`STT_NOTYPE`](elf-hello-world.md#stt-notype)
            - [`SHN_ABS`](elf-hello-world.md#shn-abs)
          - [`SHT_SYMTAB` on the executable](elf-hello-world.md#sht-symtab-on-the-executable)
        - [`.strtab`](elf-hello-world.md#strtab)
        - [`.rela.text`](elf-hello-world.md#rela-text)
          - [`.rel.text`](elf-hello-world.md#rel-text)
        - [Dynamic linking sections](elf-hello-world.md#dynamic-linking-sections)
          - [`PT_INTERP`](elf-hello-world.md#pt-interp)
          - [Dynamic section](elf-hello-world.md#dynamic-section)
            - [`DT_FLAGS_1`](elf-hello-world.md#dt-flags-1)
              - [`DF_1_PIE`](elf-hello-world.md#df-1-pie)
      - [Program header table](elf-hello-world.md#program-header-table)
      - [Backlinks](elf-hello-world.md#backlinks)
- [Molecular biology feels like systems programming](#molecular-biology-feels-like-systems-programming)
- [Virtualization](#virtualization)
  - [Docker (software)](#docker-software)
  - [Emulator](#emulator)
    - [List of emulators](#list-of-emulators)
      - [gem5](#gem5)
      - [QEMU](#qemu)
        - [User mode emulation](#user-mode-emulation)
        - [QEMU JavaScript port](#qemu-javascript-port)
          - [QEMU.js](#qemu-js)
        - [Binary translation](#binary-translation)
    - [Emulator manager](#emulator-manager)
      - [virt-manager](#virt-manager)
      - [quickemu](#quickemu)
        - [quickemu HOWTO](#quickemu-howto)
          - [quickemu directory sharing](#quickemu-directory-sharing)
          - [quickemu serial without GUI](#quickemu-serial-without-gui)
- [Systems programmer](#systems-programmer)
  - [The most awesome systems programmers](#the-most-awesome-systems-programmers)
  - [List of systems programmers](#list-of-systems-programmers)
    - [Bert Hubert](#bert-hubert)
    - [D. Richard Hipp](#d-richard-hipp)
    - [Eli Benderski](#eli-benderski)
    - [Fabrice Bellard](#fabrice-bellard)
    - [Linus Torvalds](#linus-torvalds)
    - [Robert O'Callahan](#robert-o-callahan)

## Being proud of low level programming is stupid

↑ **Parent:** [Systems programming](systems-programming.md)  
🏷️ **Tags:** [Essays by Ciro Santilli](ciro-santilli.md#essays-by-ciro-santilli)

Ciro's word of caution for 2019 aspiring system programmers: [Should you waste your life with systems programming?](https://cirosantilli.com/linux-kernel-module-cheat/#should-you-waste-your-life-with-systems-programming)

This is basically a direct consequence of [backward design](cirism.md#backward-design).

The higher the level you can operate at, the better.

[C](programming-language.md#c-programming-language) is better than [assembly](computer-hardware.md#assembly-language), [userland](#user-space) better than [kernelland](#kernel-space).

The ideal level to operate at, and one of humankind's greatest ambitions is "[AGI](artificial-intelligence.md#artificial-general-intelligence), make me money", the highest possible level.

Only go down a level when it seems necessary.

## Bootloader

↑ **Parent:** [Systems programming](systems-programming.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Bootloader)

## Operating system

↑ **Parent:** [Systems programming](systems-programming.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Operating_system)

Magic software that allows you to write a single program that runs on a wide range of hardware.

### Operating system concept

↑ **Parent:** [Operating system](#operating-system)

#### User and kernel space

↑ **Parent:** [Operating system concept](#operating-system-concept)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/User_and_kernel_space)

Bibliography:
- [https://unix.stackexchange.com/questions/137820/whats-the-difference-of-the-userland-vs-the-kernel](https://unix.stackexchange.com/questions/137820/whats-the-difference-of-the-userland-vs-the-kernel)
- [https://unix.stackexchange.com/questions/87625/what-is-difference-between-user-space-and-kernel-space](https://unix.stackexchange.com/questions/87625/what-is-difference-between-user-space-and-kernel-space)
- [https://stackoverflow.com/questions/18717016/what-are-ring-0-and-ring-3-in-the-context-of-operating-systems](https://stackoverflow.com/questions/18717016/what-are-ring-0-and-ring-3-in-the-context-of-operating-systems)

##### User space

↑ **Parent:** [User and kernel space](#user-and-kernel-space)

##### Kernel space

↑ **Parent:** [User and kernel space](#user-and-kernel-space)

### Bare metal

↑ **Parent:** [Operating system](#operating-system)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Bare_machine)

Bare metal programming is to run a program without an [operating system](#operating-system) below it.

Or in other words, it is basically implementing an [operating system](#operating-system)/[firmware](#firmware) yourself ad hoc, together with your actual program.

### Driver (software)

↑ **Parent:** [Operating system](#operating-system)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Driver_(software))

### Embedded operating system

↑ **Parent:** [Operating system](#operating-system)  
🏷️ **Tags:** [Microcontroller](computer-hardware.md#microcontroller)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Embedded_operating_system)

#### MicroPython

↑ **Parent:** [Embedded operating system](#embedded-operating-system)  
🏷️ **Tags:** [Python (programming language)](programming-language.md#python-programming-language)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/MicroPython)

It is interpreted. It actually implements a Python (-like ?) interpreter that can run on a microcontroller. See e.g.: [Compile MicroPython code for Micro Bit locally](electronics.md#compile-micropython-code-for-micro-bit-locally).

As a result, it is both very convenient, as it does not require a C toolchain to build for, but also very slow and produces larger images.

##### Run MicroPython on X

↑ **Parent:** [MicroPython](#micropython)

##### MicroPython example

↑ **Parent:** [MicroPython](#micropython)

Under: [micropython](micropython)

<h6 id="_file/micropython/blink_gpio.py">micropython/blink_gpio.py</h6>

↑ **Parent:** [MicroPython example](#micropython-example)

Toggle pin 0 twice per second. This could be used for example to blink LED on pin 0 once per second with this test circuit:

```
BOARD__1gp0____3gnd
       |       |
       R_2k    |
       |       |
       +-aLEDc-+
```

Tested on:

- [RPI Pico W](computer-hardware.md#raspberry-pi-pico-w)

#### Zephyr (operating system)

↑ **Parent:** [Embedded operating system](#embedded-operating-system)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Zephyr_(operating_system))

Zephyr is cool. Its installation setup is annoying. But the project is cool.

##### Zephyr example

↑ **Parent:** [Zephyr (operating system)](#zephyr-operating-system)

###### Zephyr non-official example

↑ **Parent:** [Zephyr example](#zephyr-example)

<h6 id="_file/zephyr/blink_gpio.c">zephyr/blink_gpio.c</h6>

↑ **Parent:** [Zephyr example](#zephyr-example)

Same behavior as [micropython/blink_gpio.py](#_file/micropython/blink_gpio.py).

###### Zephyr official example

↑ **Parent:** [Zephyr example](#zephyr-example)

###### Zephyr blinky example

↑ **Parent:** [Zephyr official example](#zephyr-official-example)

Blinks the on-board LED if the board has one.

Does not work on:
- [Micro Bit](electronics.md#micro-bit): build fails
- [Raspberry Pi Pico W](computer-hardware.md#raspberry-pi-pico-w): build works but does nothing because the LED is connected differently

###### Zephyr hello world example

↑ **Parent:** [Zephyr official example](#zephyr-official-example)

Uses `printf` to print some bytes somewhere, usually the first [UART](computer.md#universal-asynchronous-receiver-transmitter) of the board.

##### Run Zephyr on X

↑ **Parent:** [Zephyr (operating system)](#zephyr-operating-system)

###### Run Zephyr on [QEMU](#qemu)

↑ **Parent:** [Run Zephyr on X](#run-zephyr-on-x)  
🏷️ **Tags:** [QEMU](#qemu)

Real hardware is for newbs. Real hardware is for newbs.

Tested on [Ubuntu 23.10](#ubuntu-23-10) we approximately follow instructions from: [https://docs.zephyrproject.org/3.4.0/develop/getting_started/index.html](https://docs.zephyrproject.org/3.4.0/develop/getting_started/index.html) stopping before the "Flash the sample" section, as we don't flash [QEMU](#qemu). We just run it.

```
sudo apt install --no-install-recommends git cmake ninja-build gperf \
  ccache dfu-util device-tree-compiler wget \
  python3-dev python3-pip python3-setuptools python3-tk python3-wheel xz-utils file \
  make gcc gcc-multilib g++-multilib libsdl2-dev libmagic1 python3-pyelftools
python3 -m venv ~/zephyrproject/.venv
source ~/zephyrproject/.venv/bin/activate
pip install west
west init ~/zephyrproject
cd ~/zephyrproject
west update
west zephyr-export
cd ~
wget https://github.com/zephyrproject-rtos/sdk-ng/releases/download/v0.16.1/zephyr-sdk-0.16.1_linux-x86_64.tar.xz
tar xvf zephyr-sdk-0.16.1_linux-x86_64.tar.xz
cd zephyr-sdk-0.16.1
./setup.sh
```

The installation procedure install all [compiler toolchains](software.md#compiler-toolchain) for us, so we can then basically compile for any target. It also fetches the latest Git source code of Zephyr under:
```
~/zephyrproject/zephyr
```

The "most default" blinky hello world example which blinks an LED is a bit useless for us because QEMU doesn't have LEDs, so instead we are going to use one of the [UART](computer.md#universal-asynchronous-receiver-transmitter) examples which will print characters we can see on QEMU stdout.

Let's start with the [hello world](software.md#hello-world-program) example on an x86 target:
```
cd ~/zephyrproject/zephyr
west build -b qemu_x86 samples/hello_world -t run
```
and it outputs:
```
Hello World! qemu_x86
```
The `qemu_x64` on the output comes from the `CONFIG_BOARD` macro [https://github.com/zephyrproject-rtos/zephyr/blob/c15ff103001899ba0321b2c38013d1008584edc0/samples/hello_world/src/main.c#L11](https://github.com/zephyrproject-rtos/zephyr/blob/c15ff103001899ba0321b2c38013d1008584edc0/samples/hello_world/src/main.c#L11)
```
#include <zephyr/kernel.h>

int main(void)
{
	printk("Hello World! %s\n", CONFIG_BOARD);
	return 0;
}
```

The `qemu_x86` board is documented at: [https://docs.zephyrproject.org/3.4.0/boards/x86/qemu_x86/doc/index.html](https://docs.zephyrproject.org/3.4.0/boards/x86/qemu_x86/doc/index.html)

You can also first `cd` into the directory that you want to build in to avoid typing `samples/hello_world` all the time:
```
cd ~/zephyrproject/zephyr/samples/hello_world
zephyr west build -b qemu_x86 -t run
```

You can also build and run separately with:
```
west build -b qemu_x86
west build -t run
```

Another important option is:
```
west build -t menuconfig
```
But note that it does not modify your `prj.conf` automatically for you.

Let's try on another target:
```
rm -rf build
zephyr west build -b qemu_cortex_a53 -t run
```
and same output, but on a completely different board! The `qemu_cortex_a53` board is documented at: [https://docs.zephyrproject.org/3.4.0/boards/arm64/qemu_cortex_a53/doc/index.html](https://docs.zephyrproject.org/3.4.0/boards/arm64/qemu_cortex_a53/doc/index.html)

The list of all examples can be seen under:
```
ls ~/zephyrproject/zephyr/samples
```
which for example contains:
```
zephyrproject/zephyr/samples/hello_world
```

So run another sample simply select it, e.g. to run `zephyrproject/zephyr/samples/synchronization`:
```
west build -b qemu_cortex_a53 samples/synchronization -t run
```

### Firmware

↑ **Parent:** [Operating system](#operating-system)  
🏷️ **Tags:** [Software](software.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Firmware)

#### BIOS

↑ **Parent:** [Firmware](#firmware)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/BIOS)

### System call

↑ **Parent:** [Operating system](#operating-system)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/System_call)

### The three operating systems

↑ **Parent:** [Operating system](#operating-system)

As of 2025 and much earlier, there were only 3 operating systems that mattered on desktop:
- [Windows](microsoft.md#microsoft-windows)
- [MacOS](apple-inc.md#macos)
- [Linux](#linux)
We refer to them as "the three operating systems".

### List of operating systems

↑ **Parent:** [Operating system](#operating-system)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/List_of_operating_systems)

#### Linux

↑ **Parent:** [List of operating systems](#list-of-operating-systems)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Linux)

It ain't perfect, but it's decent enough.

From a technical point of view, it can do anything that [Microsoft Windows](microsoft.md#microsoft-windows) can. Except being forcefully installed on every non-[MacOS](apple-inc.md#macos) 2019 computer you can buy.

[Ciro Santilli](ciro-santilli.md)'s conversion to Linux happened around 2012, and was a central part of [Ciro Santilli's Open Source Enlightenment](ciro-santilli.md#ciro-santilli-s-open-source-enlightenment), since it fundamentally enables the discovery and contribution to [open source software](software.md#open-source-software). Because what awesome open source person would waste time porting their amazing projects to closed source OSes?

Ciro's modest nature can be seen as he likes to compare this event [Buddha's Great Renunciation](https://en.wikipedia.org/wiki/Great_Renunciation).

Linux should track glibc and [POSIX command line utilities](#posix-command-line-utility) in-tree like [BSD Operating System](#berkeley-software-distribution), otherwise people have [no way to get the thing running in the first place without blobs or large out-of-tree scripts](the-most-important-projects-done-by-ciro-santilli.md#linux-kernel-module-cheat)! [Another enlightened soul](https://blog.farhan.codes/2018/06/25/linux-maintains-bugs-the-real-reason-ifconfig-on-linux-is-deprecated/) who agrees.

Particularly interesting in the history of Linux is how it won out over the open competitors that were coming up in the time: [MINIX](https://en.wikipedia.org/wiki/MINIX) (see [the chat](https://ponderwall.com/index.php/2019/04/02/linux-tanenbaum-newsgroup-linus-torvalds/)) and [BSD Operating System](#berkeley-software-distribution) that got [legally bogged down](https://en.wikipedia.org/wiki/UNIX_System_Laboratories,_Inc._v._Berkeley_Software_Design,_Inc.) at the critical growth moment.

You must watch this: [truth Happens advertisement by Red Hat](software.md#truth-happens-advertisement-by-red-hat).

<a id="image-xkcd-619-supported-features"></a>
![](https://web.archive.org/web/20210129024945if_/https://imgs.xkcd.com/comics/supported_features.png)

**[Figure 1](#image-xkcd-619-supported-features). xkcd 619: Supported Features**. [Source](https://xkcd.com/619/). This perfectly illustrates Linux development. First features that matter. Then useless features.

<a id="video-bill-gates-vs-steve-jobs-by-epic-rap-battles-of-history-2012"></a>
**[Video 1](#video-bill-gates-vs-steve-jobs-by-epic-rap-battles-of-history-2012). Bill Gates vs Steve Jobs by Epic Rap Battles of History (2012)** [Source](http://youtube.com/watch?v=njos57IJf-0). Just stop whatever you are doing, and watch this right now. "I'm on [Linux](#linux), bitch, I thought you GNU". [Fandom explanations](https://epicrapbattlesofhistory.fandom.com/wiki/Steve_Jobs_vs_Bill_Gates/Rap_Meanings). It is just a shame that the Bill Gates actor looks absolutely nothing like the real gates. Actually, the entire Gates/Jobs parts are good, but not genial. But the Linux one is.

##### Tux (mascot)

↑ **Parent:** [Linux](#linux)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Tux_(mascot))

##### Linux kernel

↑ **Parent:** [Linux](#linux)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Linux_kernel)

[Ciro Santilli](ciro-santilli.md) has a tutorial at [Linux Kernel Module Cheat](the-most-important-projects-done-by-ciro-santilli.md#linux-kernel-module-cheat).

###### Linux kernel system

↑ **Parent:** [Linux kernel](#linux-kernel)

###### Linux kernel security system

↑ **Parent:** [Linux kernel](#linux-kernel)

###### Landlock (Linux kernel)

↑ **Parent:** [Linux kernel security system](#linux-kernel-security-system)

[https://docs.kernel.org/userspace-api/landlock.html](https://docs.kernel.org/userspace-api/landlock.html)

- generic jail:
  - [https://unix.stackexchange.com/questions/6433/how-to-jail-a-process-without-being-root/805147#805147](https://unix.stackexchange.com/questions/6433/how-to-jail-a-process-without-being-root/805147#805147)
  - [https://stackoverflow.com/questions/4249063/run-an-untrusted-c-program-in-a-sandbox-in-linux-that-prevents-it-from-opening-f/79915566#79915566](https://stackoverflow.com/questions/4249063/run-an-untrusted-c-program-in-a-sandbox-in-linux-that-prevents-it-from-opening-f/79915566#79915566)
- prevent disk write:
  - [https://superuser.com/questions/594322/how-to-prevent-application-from-writing-to-disk/1936162#1936162](https://superuser.com/questions/594322/how-to-prevent-application-from-writing-to-disk/1936162#1936162)
  - [https://unix.stackexchange.com/questions/64642/how-to-prevent-a-process-from-writing-files/805142#805142](https://unix.stackexchange.com/questions/64642/how-to-prevent-a-process-from-writing-files/805142#805142)
  - prevent single directory write:
    - [https://unix.stackexchange.com/questions/223006/restrict-a-process-to-accessing-only-a-specific-directory/805145#805145](https://unix.stackexchange.com/questions/223006/restrict-a-process-to-accessing-only-a-specific-directory/805145#805145)
    - [https://askubuntu.com/questions/618160/server-run-a-program-allowing-it-to-write-only-on-a-specific-directory/1565143#1565143](https://askubuntu.com/questions/618160/server-run-a-program-allowing-it-to-write-only-on-a-specific-directory/1565143#1565143)

###### Linux Foundation

↑ **Parent:** [Linux kernel](#linux-kernel)

The fact that this foundation has a bunch of paid, closed, certification courses makes [Ciro Santilli](ciro-santilli.md) not respect them at all. They should be making [open access](education.md#open-access) content instead!

###### Linux kernel build output

↑ **Parent:** [Linux kernel](#linux-kernel)

###### vmlinux

↑ **Parent:** [Linux kernel build output](#linux-kernel-build-output)

###### Step debug the Linux kernel

↑ **Parent:** [Linux kernel](#linux-kernel)

- [https://stackoverflow.com/questions/11408041/how-to-debug-the-linux-kernel-with-gdb-and-qemu/33203642#33203642](https://stackoverflow.com/questions/11408041/how-to-debug-the-linux-kernel-with-gdb-and-qemu/33203642#33203642) How to debug the Linux kernel with GDB and QEMU?
- [https://cirosantilli.com/linux-kernel-module-cheat/gdb](https://cirosantilli.com/linux-kernel-module-cheat/gdb)

###### JTAG

↑ **Parent:** [Step debug the Linux kernel](#step-debug-the-linux-kernel)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/JTAG)

###### Serial wire debug

↑ **Parent:** [JTAG](#jtag)

###### Linux kernel bibliography

↑ **Parent:** [Linux kernel](#linux-kernel)

###### Linux insides

↑ **Parent:** [Linux kernel bibliography](#linux-kernel-bibliography)

[https://github.com/0xAX/linux-insides](https://github.com/0xAX/linux-insides)

Documents the [Linux kernel](#linux-kernel). Somewhat of a competitor to [Linux Kernel Module Cheat](the-most-important-projects-done-by-ciro-santilli.md#linux-kernel-module-cheat), but more wordy and less automated.

###### Linux Device Drivers book

↑ **Parent:** [Linux kernel bibliography](#linux-kernel-bibliography)

This is perhaps by far the most famous kernel driver book.

As of 2025 the latest version was quite old however, [Linux Device Drivers book 3rd edition](#linux-device-drivers-book-3rd-edition) from 2005.

###### Linux Device Drivers book edition

↑ **Parent:** [Linux Device Drivers book](#linux-device-drivers-book)

###### Linux Device Drivers book 3rd edition

↑ **Parent:** [Linux Device Drivers book edition](#linux-device-drivers-book-edition)

[https://lwn.net/Kernel/LDD3/](https://lwn.net/Kernel/LDD3/) contains the PDF of each chapter.

[https://www.amazon.co.uk/dp/B0026OR2XQ](https://www.amazon.co.uk/dp/B0026OR2XQ)

The book covers the Linux kernel version 2.6.10.

<h6 id="martinezjavier-ldd3">martinezjavier/ldd3</h6>

↑ **Parent:** [Linux Device Drivers book 3rd edition](#linux-device-drivers-book-3rd-edition)

[https://github.com/martinezjavier/ldd3](https://github.com/martinezjavier/ldd3)

This repo has ported the kernels up to 5.10 as of writing. [https://github.com/martinezjavier/ldd3/pull/86](https://github.com/martinezjavier/ldd3/pull/86) attempts to go further into 6.x but has been ignored for two years unfortunately.

##### Linux distribution

↑ **Parent:** [Linux](#linux)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Linux_distribution)

###### Linux distribution buildable from source

↑ **Parent:** [Linux distribution](#linux-distribution)

As of 2020, no one knows how to build the major desktop distros fully from source into the ISO, and especially so in a reproducible build way. Everything is done in build servers somewhere with complicated layers of prebuilds. It's crap.

See also: [https://cirosantilli.com/linux-kernel-module-cheat/#linux-distro-choice](https://cirosantilli.com/linux-kernel-module-cheat/#linux-distro-choice)

Yes:
- [Buildroot](#buildroot)
- [NixOS](#nixos)

No:
- [Ubuntu](#ubuntu): [https://askubuntu.com/questions/82302/how-to-compile-ubuntu-from-source-code](https://askubuntu.com/questions/82302/how-to-compile-ubuntu-from-source-code) source: [sausage factory](https://quoteinvestigator.com/2010/07/08/laws-sausages/)

###### Package manager

↑ **Parent:** [Linux distribution](#linux-distribution)

###### Cross distro package manager

↑ **Parent:** [Linux distribution](#linux-distribution)

###### AppImage

↑ **Parent:** [Cross distro package manager](#cross-distro-package-manager)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/AppImage)

###### Flatpak

↑ **Parent:** [Cross distro package manager](#cross-distro-package-manager)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Flatpak)

###### Snap (package manager)

↑ **Parent:** [Cross distro package manager](#cross-distro-package-manager)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Snap_(package_manager))

[https://merlijn.sebrechts.be/blog/2020-08-02-why-one-snap-store/](https://merlijn.sebrechts.be/blog/2020-08-02-why-one-snap-store/) has some very good comments on how `snap` is more closed than [Flatpak](#flatpak).

Snap's permission system is extremely annoying, notably restricting access to home files. They need a popup that says "permission required by app, accept?" urgently!!!
- [https://askubuntu.com/questions/1238211/how-to-make-snaps-access-hidden-files-and-folders-in-home](https://askubuntu.com/questions/1238211/how-to-make-snaps-access-hidden-files-and-folders-in-home)

##### List of Linux distributions

↑ **Parent:** [Linux](#linux)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/List_of_Linux_distributions)

###### Android (operating system)

↑ **Parent:** [List of Linux distributions](#list-of-linux-distributions)

- the best full featured free OS we have today, since POSIX gave up short of any UI specification, and Chrome OS is not there yet
- usable and likely efficient [Java](programming-language.md#java-programming-language) [API](software.md#application-programming-interface) for apps if [Oracle doesn't manage to destroy it with its lawsuit](https://en.wikipedia.org/wiki/Google_v._Oracle_America)

However, many, many, many terrible horrors come with it:
- it hasn't made the move to desktop for too many years. It could destroy [Microsoft Windows](microsoft.md#microsoft-windows) and replace it with open source, but they just won't budge towards an unified mobile/desktop setup.
- vendors litter it with uninstallable bloatware that should be [illegal](law.md). [European Union](continent.md#european-union) to the rescue!!! [https://www.cnbc.com/2020/12/15/digital-markets-act-eus-new-rules-on-big-tech.html](https://www.cnbc.com/2020/12/15/digital-markets-act-eus-new-rules-on-big-tech.html)
- vendors lock down devices so it is very hard to get sudo, let alone to modify their images!
- there isn't enough hardware standardization for open source distros to thrive like on desktop
- code drops mean that "master" is useless and trying to contribute from outside vendors' closed walls is a waste of time: [https://stackoverflow.com/questions/1809774/how-to-compile-the-android-aosp-kernel-and-test-it-with-the-android-emulator/48310014#48310014](https://stackoverflow.com/questions/1809774/how-to-compile-the-android-aosp-kernel-and-test-it-with-the-android-emulator/48310014#48310014)
- if you ever go below the Java API, e.g. to [C++](programming-language.md#c-plus-plus) or AOSP build, everything is horrendous and [undocumented](https://unix.stackexchange.com/questions/122787/how-to-compile-extra-files-into-the-root-directory-of-an-android-rom)
- [Google](google.md) doesn't care about the CLI, even the [hello world](software.md#hello-world-program) requires creating infinite out-of-control boilerplate from a [GUI](software.md#graphical-user-interface): [https://stackoverflow.com/questions/20801042/how-to-create-android-project-with-gradle-from-command-line/46994747#46994747](https://stackoverflow.com/questions/20801042/how-to-create-android-project-with-gradle-from-command-line/46994747#46994747)
- the boot is uber bloated and takes forever in cycle simulators

###### Android Open Source Project

↑ **Parent:** [Android (operating system)](#android-operating-system)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Android_Open_Source_Project)

<h6 id="transfer-android-11-camera-videos-to-ubuntu-20-10">Transfer Android 11 camera videos to Ubuntu 20.10</h6>

↑ **Parent:** [Android (operating system)](#android-operating-system)

[https://android.stackexchange.com/questions/66385/how-to-transfer-files-from-an-android-phone-to-a-ubuntu-pc-by-using-a-usb-cable/194107#194107](https://android.stackexchange.com/questions/66385/how-to-transfer-files-from-an-android-phone-to-a-ubuntu-pc-by-using-a-usb-cable/194107#194107)

The video folder is `DCIM/Camera`.

###### F-Droid

↑ **Parent:** [Android (operating system)](#android-operating-system)  
🏷️ **Tags:** [Good](cirism.md#good)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/F-Droid)

###### Arch Linux

↑ **Parent:** [List of Linux distributions](#list-of-linux-distributions)  
🏷️ **Tags:** [Linux distribution buildable from source](#linux-distribution-buildable-from-source)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Arch_Linux)

Respect. Big respect. Those people are hardcore from scratch hackers, and their wiki is amazing: [https://wiki.archlinux.org/](https://wiki.archlinux.org/)

It's just that [Buildroot](#buildroot) is more hardcore ;-)

But can you build the ISO full from source: [Linux distribution buildable from source](#linux-distribution-buildable-from-source)

###### Buildroot

↑ **Parent:** [List of Linux distributions](#list-of-linux-distributions)  
🏷️ **Tags:** [Good](cirism.md#good), [Linux distribution buildable from source](#linux-distribution-buildable-from-source)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Buildroot)

The basis for [Linux Kernel Module Cheat](the-most-important-projects-done-by-ciro-santilli.md#linux-kernel-module-cheat).

Buildroot is [good](cirism.md#good).

###### BusyBox

↑ **Parent:** [Buildroot](#buildroot)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/BusyBox)

###### NixOS

↑ **Parent:** [List of Linux distributions](#list-of-linux-distributions)  
🏷️ **Tags:** [Linux distribution buildable from source](#linux-distribution-buildable-from-source)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/NixOS)

This thing is sexy.

###### Ubuntu

↑ **Parent:** [List of Linux distributions](#list-of-linux-distributions)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Ubuntu)

[Ciro Santilli](ciro-santilli.md)'s Linux distro of choice as of 2019.

It ain't perfect, but it's decent enough.

The greatest advantage of it being that it has the likely largest desktop user base, and therefore the highest likelihood that your problems are solved on [Ask Ubuntu](https://askubuntu.com/users/52975), and goes together with Ciro's philosophy that ["people should do everything in the same way to factor stuff out"](cirism.md#having-more-than-one-natural-language-is-bad-for-the-world), especially the [open source losers](software.md#open-source-software).

Ciro considers that the killer flaw of Ubuntu, and most desktop distros of 2020, is that no one under the Sun knows how to build them fully from source: [Linux distribution buildable from source](#linux-distribution-buildable-from-source). This is why Ciro based the [Linux Kernel Module Cheat](the-most-important-projects-done-by-ciro-santilli.md#linux-kernel-module-cheat) on [Buildroot](#buildroot), see also: [Linux distribution buildable from source](#linux-distribution-buildable-from-source).

###### Canonical (company)

↑ **Parent:** [Ubuntu](#ubuntu)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Canonical_(company))

###### apport (software)

↑ **Parent:** [Ubuntu](#ubuntu)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/apport_(software))

[Source code](software.md#source-code): [https://github.com/canonical/apport](https://github.com/canonical/apport)

###### apport-cli

↑ **Parent:** [apport (software)](#apport-software)

###### Ubuntu HOWTO

↑ **Parent:** [Ubuntu](#ubuntu)

###### Make a bug report for a crash on Ubuntu

↑ **Parent:** [Ubuntu HOWTO](#ubuntu-howto)

On [Ubuntu 23.10](#ubuntu-23-10), a crash led to the creation of:
```
/var/crash/_usr_bin_gnome-shell.1000.crash
```
After that simply running [apport-cli](#apport-cli) as:
```
apport-cli gnome-shell
```
 led to the creation of: [https://bugs.launchpad.net/ubuntu/+source/gnome-shell/+bug/2049368](https://bugs.launchpad.net/ubuntu/+source/gnome-shell/+bug/2049368) a bug on the `gnome-shell` package.

###### Find GPU information in Ubuntu

↑ **Parent:** [Ubuntu HOWTO](#ubuntu-howto)

- [https://askubuntu.com/questions/5417/how-to-get-the-gpu-info/692858#692858](https://askubuntu.com/questions/5417/how-to-get-the-gpu-info/692858#692858)
- [https://askubuntu.com/questions/68028/how-do-i-check-if-ubuntu-is-using-my-nvidia-graphics-card/692412#692412](https://askubuntu.com/questions/68028/how-do-i-check-if-ubuntu-is-using-my-nvidia-graphics-card/692412#692412)
- [https://askubuntu.com/questions/524242/how-to-find-out-which-nvidia-gpu-i-have/1469351#1469351](https://askubuntu.com/questions/524242/how-to-find-out-which-nvidia-gpu-i-have/1469351#1469351)

###### How to report Ubuntu crashes

↑ **Parent:** [Ubuntu HOWTO](#ubuntu-howto)

Their crash system does not have an amazing user interface.

Tested on [Ubuntu 21.10](#ubuntu-21-10).

After something crashes, look under `/var/crash` for a crash file, which helps to determine which package to report under on [Launchpad](#launchpad-website).

E.g. a file `/var/crash/_usr_sbin_gdm3.0.crash` makes you want to file the bug under gdm at: [https://bugs.launchpad.net/ubuntu/+source/gdm/+filebug](https://bugs.launchpad.net/ubuntu/+source/gdm/+filebug)

Then, while reporting the bug, you want to give the developpers access to that `.crash` file. But you can't publicly upload it because it contains memory dumps and could contain secret information. The way to do it is to look at the ID under:
```
sudo cat /var/crash/_usr_sbin_gdm3.0.uploaded
```
Ubuntu's crash report system has already uploaded the `.crash` for you, so you just have to confirm it and give the ID on the ticket.

You can view a list of all your uploaded errors at:
```
xdg-open https://errors.ubuntu.com/user/$(sudo cat /var/lib/whoopsie/whoopsie-id)
```
and each of those contain a link to:
```
https://errors.ubuntu.com/oops/<.uloaded error id>
```
which you yourself cannot see.

[https://askubuntu.com/questions/434431/how-can-i-read-a-crash-file-from-var-crash](https://askubuntu.com/questions/434431/how-can-i-read-a-crash-file-from-var-crash) asks how to read the `.crash` files.

Running:
```
sudo apport-unpack /var/crash/_usr_sbin_gdm3.0.crash /tmp/app
```
splits it up into a few files, but does not make any major improvements.

`apport-retrace`
```
sudo apt install apport-retrace
sudo chmod 666 /var/crash/_usr_sbin_gdm3.0.crash
apport-retrace -g /var/crash/_usr_sbin_gdm3.0.crash
```
opens GDB with the core dump. Debug symbols are supplied as separate packages, which is a really cool idea: so you should be able to download them after the crash to see symbols. [https://askubuntu.com/questions/487222/how-to-install-debug-symbols-for-installed-packages](https://askubuntu.com/questions/487222/how-to-install-debug-symbols-for-installed-packages) mentions how to install them. Official docs at: [https://wiki.ubuntu.com/DebuggingProgramCrash#Debug_Symbol_Packages](https://wiki.ubuntu.com/DebuggingProgramCrash#Debug_Symbol_Packages)

Tried:
```
echo "deb http://ddebs.ubuntu.com $(lsb_release -cs) main restricted universe multiverse" | sudo tee -a /etc/apt/sources.list.d/ddebs.list
echo -e "deb http://ddebs.ubuntu.com $(lsb_release -cs)-updates main restricted universe multiverse\ndeb http://ddebs.ubuntu.com $(lsb_release -cs)-proposed main restricted universe multiverse" | sudo tee -a /etc/apt/sources.list.d/ddebs.list
sudo apt install ubuntu-dbgsym-keyring
```
but then `sudo apt update` fails with:
```
E: The repository 'http://ddebs.ubuntu.com impish-security Release' does not have a Release file.
```

###### Compile Linux kernel for Ubuntu

↑ **Parent:** [Ubuntu HOWTO](#ubuntu-howto)

This section describes our attempts at compiling the [Linux kernel](#linux-kernel) for [Ubuntu](#ubuntu) so as to use the exact patches and build configuration as used for a given [Ubuntu release](#ubuntu-release). The same toolchain would also be ideal, but perhaps this would require a [Linux distribution buildable from source](#linux-distribution-buildable-from-source).

[https://canonical-kteam-docs.readthedocs-hosted.com/en/public/how-to/build-kernel.html](https://canonical-kteam-docs.readthedocs-hosted.com/en/public/how-to/build-kernel.html) seems promising it says that for [Ubuntu 24.04](#ubuntu-24-04) and above you should do the following which was tested on [Ubuntu 24.10](#ubuntu-24-10):

```
sudo cp /etc/apt/sources.list /etc/apt/sources.list~
sudo sed -Ei 's/^# deb-src /deb-src /' /etc/apt/sources.list
sudo apt-get update
sudo apt build-dep -y linux linux-image-unsigned-$(uname -r)
sudo apt install -y fakeroot llvm libncurses-dev dwarves
apt source linux-image-unsigned-$(uname -r)
~/tmp/ubuntu/linux-6.11.0
cd linux-6.11.0
chmod a+x debian/rules
chmod a+x debian/scripts/*
chmod a+x debian/scripts/misc/*
fakeroot debian/rules clean
fakeroot debian/rules binary
```

The build is extremely slow compared to a build of a more embedded and specifically targeted minimal kernel, and took about 2 hours on [P14s](ciro-santilli-s-hardware.md#lenovo-thinkpad-p14s-gen4-amd). Their philosophy is likely to enable as many drivers as possible so that a single download will work for everyone. Which makes sense, fair enough. It would be cute though if there was a smarter way. Oh well.

After it finally finishes the build including our [vmlinux](#vmlinux) is present at:

```
linux-6.11.0/debian/build/build-generic
```

###### Emulate [Windows](microsoft.md#microsoft-windows) on Ubuntu

↑ **Parent:** [Ubuntu HOWTO](#ubuntu-howto)

- [https://superuser.com/questions/1707074/create-a-stable-virtualized-windows-os-on-ubuntu](https://superuser.com/questions/1707074/create-a-stable-virtualized-windows-os-on-ubuntu)
- [https://www.reddit.com/r/linux/comments/11ruj9u/creating_a_qemu_windows_10_vm_on_linux/](https://www.reddit.com/r/linux/comments/11ruj9u/creating_a_qemu_windows_10_vm_on_linux/)

More specialized versions:
- [https://askubuntu.com/questions/1523535/installing-windows-11-in-a-vm-on-ubuntu-24-04](https://askubuntu.com/questions/1523535/installing-windows-11-in-a-vm-on-ubuntu-24-04) wants to keep real Windows data as well
- [https://askubuntu.com/questions/1528367/what-is-the-best-way-to-set-up-a-windows-10-vm-with-hypervisor-and-virtual-machi](https://askubuntu.com/questions/1528367/what-is-the-best-way-to-set-up-a-windows-10-vm-with-hypervisor-and-virtual-machi) asks for some hypervisor stuff

###### Ubuntu release

↑ **Parent:** [Ubuntu](#ubuntu)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Ubuntu_release)

<h6 id="ubuntu-26-04">Ubuntu 26.04</h6>

↑ **Parent:** [Ubuntu release](#ubuntu-release)

<h6 id="ubuntu-25-10">Ubuntu 25.10</h6>

↑ **Parent:** [Ubuntu release](#ubuntu-release)

<h6 id="ubuntu-25-10-bug">Ubuntu 25.10 bug</h6>

↑ **Parent:** [Ubuntu 25.10](#ubuntu-25-10)

- [https://askubuntu.com/questions/1560258/how-to-prevent-ubuntu-25-10-from-waking-up-from-suspend-when-i-close-the-laptop?noredirect=1&lq=1](https://askubuntu.com/questions/1560258/how-to-prevent-ubuntu-25-10-from-waking-up-from-suspend-when-i-close-the-laptop?noredirect=1&lq=1)

<h6 id="ubuntu-25-04">Ubuntu 25.04</h6>

↑ **Parent:** [Ubuntu release](#ubuntu-release)

<h6 id="ubuntu-24-10">Ubuntu 24.10</h6>

↑ **Parent:** [Ubuntu release](#ubuntu-release)

<h6 id="ubuntu-24-04">Ubuntu 24.04</h6>

↑ **Parent:** [Ubuntu release](#ubuntu-release)

<h6 id="ubuntu-24-04-installer-erase-disk-and-install-ubuntu-doesn-t-work-when-bitlocker-enabled">Ubuntu 24.04 installer "Erase disk and install Ubuntu" doesn't work when BitLocker enabled</h6>

↑ **Parent:** [Ubuntu 24.04](#ubuntu-24-04)

[https://bugs.launchpad.net/subiquity/+bug/2045480](https://bugs.launchpad.net/subiquity/+bug/2045480)

[Ciro Santilli](ciro-santilli.md) reproduced on [Dell Inspiron 15 3520](ciro-santilli-s-hardware.md#dell-inspiron-15-3520) with factory defaults. This bug prevents "wipe windows" installation without workarounds, one of which is to disable encryption in Windows.

<h6 id="ubuntu-24-04-the-application-files-has-closed-unexpectedly">Ubuntu 24.04 "The application files has closed unexpectedly"</h6>

↑ **Parent:** [Ubuntu 24.04](#ubuntu-24-04)

Happens at startup without doing anything, and then keeps happening randomly infinitely many times... on a almost clean 24.04 ISO install on [Dell Inspiron 15 3520](ciro-santilli-s-hardware.md#dell-inspiron-15-3520)... God how can it be so bad.

Viewing the [apport](#apport-software) issue a bit further shows title:
```
nautilus crashed with sigabrt in g_assertion_message_expr
```

Possibly related:
- [https://www.reddit.com/r/Ubuntu/comments/1ce1027/2404_is_a_terrible_release/](https://www.reddit.com/r/Ubuntu/comments/1ce1027/2404_is_a_terrible_release/)
- [https://bugs.launchpad.net/ubuntu/+source/nautilus/+bug/1795210](https://bugs.launchpad.net/ubuntu/+source/nautilus/+bug/1795210)
- [https://bugs.launchpad.net/ubuntu/+source/nautilus/+bug/1823529](https://bugs.launchpad.net/ubuntu/+source/nautilus/+bug/1823529)
- [https://askubuntu.com/questions/1406294/nautilus-keeps-crashing-in-22-04](https://askubuntu.com/questions/1406294/nautilus-keeps-crashing-in-22-04)
- [https://superuser.com/questions/42068/application-are-closed-down-unexpectedly-under-ubuntu](https://superuser.com/questions/42068/application-are-closed-down-unexpectedly-under-ubuntu)
- [https://ubuntuforums.org/showthread.php?t=2466502](https://ubuntuforums.org/showthread.php?t=2466502)
- [https://x.com/cirosantilli/status/1792792620323967227](https://x.com/cirosantilli/status/1792792620323967227)

![](https://web.archive.org/web/20240521054355if_/https://files.mastodon.social/media_attachments/files/112/477/476/049/270/962/original/d6346176be376ff5.jpg)

<h6 id="ubuntu-23-10">Ubuntu 23.10</h6>

↑ **Parent:** [Ubuntu release](#ubuntu-release)

<h6 id="gfx-v11-0-priv-reg-irq-register-access-in-command-stream">gfx_v11_0_priv_reg_irq: register access in command stream</h6>

↑ **Parent:** [Ubuntu 23.10](#ubuntu-23-10)

Had this happen on [P14s](ciro-santilli-s-hardware.md#lenovo-thinkpad-p14s-gen4-amd) on [Ubuntu 23.10](#ubuntu-23-10) while causally using [Chromium](web-technology.md#chromium-web-browser). The screen went blank for a few seconds, but it apparently managed to reboot itself, and things started working again, except that and most windows were killed:
```
[drm:gfx_v11_0_priv_reg_irq [amdgpu]] *ERROR* Illegal register access in command stream
[drm:amdgpu_job_timedout [amdgpu]] *ERROR* ring gfx_0.0.0 timeout, signaled seq=5774109, emitted seq=5774111
[drm:amdgpu_job_timedout [amdgpu]] *ERROR* Process information: process chrome pid 14023 thread chrome:cs0 pid 14087
amdgpu 0000:64:00.0: amdgpu: GPU reset begin!
[drm:mes_v11_0_submit_pkt_and_poll_completion.constprop.0 [amdgpu]] *ERROR* MES failed to response msg=3
[drm:amdgpu_mes_unmap_legacy_queue [amdgpu]] *ERROR* failed to unmap legacy queue
[drm:mes_v11_0_submit_pkt_and_poll_completion.constprop.0 [amdgpu]] *ERROR* MES failed to response msg=3
[drm:amdgpu_mes_unmap_legacy_queue [amdgpu]] *ERROR* failed to unmap legacy queue
[drm:mes_v11_0_submit_pkt_and_poll_completion.constprop.0 [amdgpu]] *ERROR* MES failed to response msg=3
[drm:amdgpu_mes_unmap_legacy_queue [amdgpu]] *ERROR* failed to unmap legacy queue
[drm:mes_v11_0_submit_pkt_and_poll_completion.constprop.0 [amdgpu]] *ERROR* MES failed to response msg=3
[drm:amdgpu_mes_unmap_legacy_queue [amdgpu]] *ERROR* failed to unmap legacy queue
[drm:mes_v11_0_submit_pkt_and_poll_completion.constprop.0 [amdgpu]] *ERROR* MES failed to response msg=3
[drm:amdgpu_mes_unmap_legacy_queue [amdgpu]] *ERROR* failed to unmap legacy queue
[drm:mes_v11_0_submit_pkt_and_poll_completion.constprop.0 [amdgpu]] *ERROR* MES failed to response msg=3
[drm:amdgpu_mes_unmap_legacy_queue [amdgpu]] *ERROR* failed to unmap legacy queue
[drm:mes_v11_0_submit_pkt_and_poll_completion.constprop.0 [amdgpu]] *ERROR* MES failed to response msg=3
[drm:amdgpu_mes_unmap_legacy_queue [amdgpu]] *ERROR* failed to unmap legacy queue
[drm:mes_v11_0_submit_pkt_and_poll_completion.constprop.0 [amdgpu]] *ERROR* MES failed to response msg=3
[drm:amdgpu_mes_unmap_legacy_queue [amdgpu]] *ERROR* failed to unmap legacy queue
[drm:mes_v11_0_submit_pkt_and_poll_completion.constprop.0 [amdgpu]] *ERROR* MES failed to response msg=3
[drm:amdgpu_mes_unmap_legacy_queue [amdgpu]] *ERROR* failed to unmap legacy queue
[drm:gfx_v11_0_cp_gfx_enable.isra.0 [amdgpu]] *ERROR* failed to halt cp gfx
Dec 27 15:03:38 ciro-p14s kernel: amdgpu 0000:64:00.0: amdgpu: MODE2 reset
Dec 27 15:03:38 ciro-p14s kernel: amdgpu 0000:64:00.0: amdgpu: GPU reset succeeded, trying to resume
Dec 27 15:03:38 ciro-p14s kernel: [drm] PCIE GART of 512M enabled (table at 0x0000008000900
```
It appears to be a bug in the [AMDGPU](computer-hardware.md#amdgpu) open source driver.

Related reports:
- [https://gitlab.freedesktop.org/drm/amd/-/issues/2451](https://gitlab.freedesktop.org/drm/amd/-/issues/2451)
- [https://gitlab.freedesktop.org/drm/amd/-/issues/475](https://gitlab.freedesktop.org/drm/amd/-/issues/475)
- [https://github.com/ValveSoftware/csgo-osx-linux/issues/3386](https://github.com/ValveSoftware/csgo-osx-linux/issues/3386)

I think this was on [Wayland](technology.md#wayland). Possibly relatd but on [X Window System](technology.md#x-window-system), crashed the UI, showed message "oh no! Something has gone wrong."
```
2024-01-13_21-55-07@ciro@ciro-p14s$ cat /var/log/apport.log
ERROR: apport (pid 975172) 2024-01-13 21:41:02,087: host pid 3528 crashed in a separate mount namespace, ignoring
INFO: apport (pid 975227) 2024-01-13 21:41:02,398: called for pid 2728, signal 5, core limit 0, dump mode 1
INFO: apport (pid 975227) 2024-01-13 21:41:02,401: executable: /usr/bin/gnome-shell (command line "/usr/bin/gnome-shell")
INFO: apport (pid 975227) 2024-01-13 21:41:12,667: wrote report /var/crash/_usr_bin_gnome-shell.1000.crash
```

###### Unable to lock screen on Ubuntu

↑ **Parent:** [Ubuntu 23.10](#ubuntu-23-10)

Happened on [P14s](ciro-santilli-s-hardware.md#lenovo-thinkpad-p14s-gen4-amd) on [Ubuntu 23.10](#ubuntu-23-10), which started with fresh Ubuntu 23.10 install.

However it did not happen on [Lenovo ThinkPad P51 (2017)](ciro-santilli-s-hardware.md#lenovo-thinkpad-p51-2017) also on [Ubuntu 23.10](#ubuntu-23-10) which had been upgraded several times from God knows what starting point... At first one had X11 (forced by [Nvidia](computer-hardware.md#nvidia) drivers) and the other Wayland, but moving to p14s X11 changed nothing.

Both were running [GNOME Display Manager](software.md#gnome-display-manager).

Same happens with Super + L, but also CLI commands: [https://askubuntu.com/questions/7776/how-do-i-lock-the-desktop-screen-via-command-line](https://askubuntu.com/questions/7776/how-do-i-lock-the-desktop-screen-via-command-line)

Bibliography:
- [https://askubuntu.com/questions/1242110/after-upgrading-to-ubuntu-20-04-lockscreen-not-working](https://askubuntu.com/questions/1242110/after-upgrading-to-ubuntu-20-04-lockscreen-not-working) canon
- [https://askubuntu.com/questions/1246622/ubuntu-20-04-unable-to-lock-screen](https://askubuntu.com/questions/1246622/ubuntu-20-04-unable-to-lock-screen)
- [https://askubuntu.com/questions/1245071/cant-lock-screen-with-shortcut-on-ubuntu-20-04-gnome](https://askubuntu.com/questions/1245071/cant-lock-screen-with-shortcut-on-ubuntu-20-04-gnome)
- [https://askubuntu.com/questions/1248756/super-l-not-working-on-ubuntu-20-04](https://askubuntu.com/questions/1248756/super-l-not-working-on-ubuntu-20-04)

<h6 id="ubuntu-23-04">Ubuntu 23.04</h6>

↑ **Parent:** [Ubuntu release](#ubuntu-release)

<h6 id="ubuntu-23-04-boot-broken-on-kernel-6-2">Ubuntu 23.04 boot broken on kernel 6.2</h6>

↑ **Parent:** [Ubuntu 23.04](#ubuntu-23-04)

On [Lenovo ThinkPad P51 (2017)](ciro-santilli-s-hardware.md#lenovo-thinkpad-p51-2017).

Switching to the other installed kernel, 5.9 made boot work.

The solution on kernel 6.2 was:
```
sudo apt instal nvidia-driver-515
```
as per comments under: [https://bugs.launchpad.net/ubuntu/+source/linux/+bug/2012559](https://bugs.launchpad.net/ubuntu/+source/linux/+bug/2012559). This also made the nvidia driver work: [Find GPU information in Ubuntu](#find-gpu-information-in-ubuntu).

Previously I had:
```
nvidia-driver-510
```
and it blew up before reaching disk decryption.

I also tried:
```
nvidia-driver-525
```
but that broke in a different way:
```
Finished apport-autoreport.service - Process error reports when automatic reporting is enabled.
nvidia-modeset: ERROR: GPU:0: Idling display engine timed out: 0x0000947d:0:0:407
(1 of 2) Job systemd-backlight@backlight: nvidia_e.service/start running (32s no limit)
```

Some threads:
- [https://askubuntu.com/questions/1465606/kubuntu-23-04-not-booting-with-the-6-2-kernel](https://askubuntu.com/questions/1465606/kubuntu-23-04-not-booting-with-the-6-2-kernel)
- [https://bugs.launchpad.net/ubuntu/+source/linux/+bug/2012559](https://bugs.launchpad.net/ubuntu/+source/linux/+bug/2012559)

<h6 id="ubuntu-22-10">Ubuntu 22.10</h6>

↑ **Parent:** [Ubuntu release](#ubuntu-release)

<h6 id="ubuntu-22-04">Ubuntu 22.04</h6>

↑ **Parent:** [Ubuntu release](#ubuntu-release)

###### snap "Pending Update of" notifications

↑ **Parent:** [Ubuntu 22.04](#ubuntu-22-04)

Happening multiple times a day on Ubuntu 22.04 for Chromium, even though I turn computer on and off daily, unbearable:
- [https://askubuntu.com/questions/1412575/pending-update-of-snap-store](https://askubuntu.com/questions/1412575/pending-update-of-snap-store)
- [https://askubuntu.com/questions/1412140/pending-update-of-firefox-snap-close-the-app-to-avoid-disruptions](https://askubuntu.com/questions/1412140/pending-update-of-firefox-snap-close-the-app-to-avoid-disruptions)
- [https://forum.snapcraft.io/t/how-to-disable-snapd-update-notifications-permanently/31117](https://forum.snapcraft.io/t/how-to-disable-snapd-update-notifications-permanently/31117) Settings \> Notifications \> Snapd User Session Agent
- [https://www.reddit.com/r/Ubuntu/comments/v1s919/disable_pending_update_of_snap_message_kiosk/](https://www.reddit.com/r/Ubuntu/comments/v1s919/disable_pending_update_of_snap_message_kiosk/)
- [https://forum.snapcraft.io/t/refresh-app-awareness-call-for-testing/29123](https://forum.snapcraft.io/t/refresh-app-awareness-call-for-testing/29123)

<h6 id="ubuntu-21-10">Ubuntu 21.10</h6>

↑ **Parent:** [Ubuntu release](#ubuntu-release)

GDM crashes sometimes when switching windows right after opening a new window: [https://bugs.launchpad.net/ubuntu/+source/gdm/+bug/1956299](https://bugs.launchpad.net/ubuntu/+source/gdm/+bug/1956299)

<h6 id="ubuntu-21-10-does-not-wake-up-from-suspend">Ubuntu 21.10 does not wake up from suspend</h6>

↑ **Parent:** [Ubuntu 21.10](#ubuntu-21-10)

Please refer to [Video "Linus Torvalds saying "Nvidia Fuck You" (2012)"](computer-hardware.md#video-linus-torvalds-saying-nvidia-fuck-you-2012).

[https://askubuntu.com/questions/1032633/18-04-screen-remains-blank-after-wake-up-from-suspend/1391917#1391917](https://askubuntu.com/questions/1032633/18-04-screen-remains-blank-after-wake-up-from-suspend/1391917#1391917)

Reported at: [https://bugs.launchpad.net/ubuntu/+source/nvidia-graphics-drivers-470/+bug/1953674](https://bugs.launchpad.net/ubuntu/+source/nvidia-graphics-drivers-470/+bug/1953674)

On [Lenovo ThinkPad P51 (2017)](ciro-santilli-s-hardware.md#lenovo-thinkpad-p51-2017).

Does not happen every time, only some times. Can't figure out why. Usually happens when has suspended for a longer time.

[https://bugs.launchpad.net/ubuntu/+source/nvidia-graphics-drivers-470/+bug/1946303](https://bugs.launchpad.net/ubuntu/+source/nvidia-graphics-drivers-470/+bug/1946303) sounds like a likely report, [Nvidia](computer-hardware.md#nvidia) driver version 470, but can't find those error messages anywhere. The last line of:
```
journalctl -o short-precise -k -b -1
```
once was:
```
PM: suspend entry (deep)
```
which is when sleep starts.

This suggests that it is not a video bug then, seems that it is not waking up at all? Gotta try to SSH into it. OK. I did SSH into it, and that was fine, so it is just the video that won't start.

```
PM: suspend exit
```

[https://bugs.launchpad.net/ubuntu/+source/linux/+bug/1949977](https://bugs.launchpad.net/ubuntu/+source/linux/+bug/1949977) is another possible bug, based on kernel version. I'm running 5.13, which is one of the failing versions on the report. Can't find any interesting dmesg though.

In another crash:
```
journalctl -o short-precise -k -b -1
```
had the following interesting lines:
```
nvidia-modeset: WARNING: GPU:0: Lost display notification (0:0x00000000); continuing.
[24307.640014] NVRM: GPU at PCI:0000:01:00: GPU-18af74bb-7c72-ff70-e447-87d48378ea20
[24307.640018] NVRM: Xid (PCI:0000:01:00): 79, pid=8828, GPU has fallen off the bus.
[24307.640021] NVRM: GPU 0000:01:00.0: GPU has fallen off the bus.
[24328.054022] nvidia-modeset: ERROR: GPU:0: The requested configuration of display devices (LGD (DP-4)) is not supported on this GPU.
[repeats several more times]
[24328.056767] nvidia-modeset: ERROR: GPU:0: The requested configuration of display devices (LGD (DP-4)) is not supported on this GPU.
[24328.056951] nvidia-modeset: ERROR: GPU:0: Failed to query display engine channel state: 0x0000927c:0:0:0x0000000f
[24328.056955] nvidia-modeset: ERROR: GPU:0: Failed to query display engine channel state: 0x0000927c:1:0:0x0000000f
[24328.056959] nvidia-modeset: ERROR: GPU:0: Failed to query display engine channel state: 0x0000927c:2:0:0x0000000f
[24328.056962] nvidia-modeset: ERROR: GPU:0: Failed to query display engine channel state: 0x0000927c:3:0:0x0000000f
[24328.056983] nvidia-modeset: ERROR: GPU:0: DP-4: Failed to disable DisplayPort audio stream-0
[24328.056992] nvidia-modeset: ERROR: GPU:0: Failed to query display engine channel state: 0x0000947d:0:0:0x0000000f
```
and there was a corresponding `/var/crash/_usr_sbin_gdm3.0.crash`.

Related "GPU has fallen off the bus": [https://askubuntu.com/questions/868321/gpu-has-fallen-off-the-bus-nvidia](https://askubuntu.com/questions/868321/gpu-has-fallen-off-the-bus-nvidia)

<h6 id="ubuntu-21-04">Ubuntu 21.04</h6>

↑ **Parent:** [Ubuntu release](#ubuntu-release)

<h6 id="ubuntu-20-04">Ubuntu 20.04</h6>

↑ **Parent:** [Ubuntu release](#ubuntu-release)

<h6 id="ubuntu-18-04">Ubuntu 18.04</h6>

↑ **Parent:** [Ubuntu release](#ubuntu-release)

<h6 id="ubuntu-16-04">Ubuntu 16.04</h6>

↑ **Parent:** [Ubuntu release](#ubuntu-release)

###### Ubuntu feature request

↑ **Parent:** [Ubuntu](#ubuntu)

Sometimes it just feels like Ubuntu devs don't actually use Ubuntu as a desktop.

Some extremely annoying problems are introduced and just never get fixed, even though they feel so obvious!

Would never happen on [Mac](apple-inc.md#macintosh)...

<h6 id="couldn-t-save-system-state-minimum-free-space-to-take-a-snapshot-and-preserve-zfs-performance-is">couldn't save system state: Minimum free space to take a snapshot and preserve ZFS performance is</h6>

↑ **Parent:** [Ubuntu feature request](#ubuntu-feature-request)

This BS started after the move to ZFS. The temporary solution appears to be: [https://askubuntu.com/questions/1293685/out-of-space-on-boot-zpool-and-cant-run-updates-anymore/1374204#1374204](https://askubuntu.com/questions/1293685/out-of-space-on-boot-zpool-and-cant-run-updates-anymore/1374204#1374204)

And then this to disable automatic snapshots in the future: [https://askubuntu.com/questions/1233049/disable-automatic-zsys-snapshots-zfs-on-root/1279593#1279593](https://askubuntu.com/questions/1233049/disable-automatic-zsys-snapshots-zfs-on-root/1279593#1279593)
```
sudo mv /etc/apt/apt.conf.d/90_zsys_system_autosnapshot /etc/apt/apt.conf.d/90_zsys_system_autosnapshot.disabled
```

God, this is so annoying:
- [https://askubuntu.com/questions/1382986/zfs-bpool-is-almost-full-how-can-i-free-up-space-so-i-can-keep-updating-my-syst](https://askubuntu.com/questions/1382986/zfs-bpool-is-almost-full-how-can-i-free-up-space-so-i-can-keep-updating-my-syst)
- [https://askubuntu.com/questions/1233049/disable-automatic-zsys-snapshots-zfs-on-root](https://askubuntu.com/questions/1233049/disable-automatic-zsys-snapshots-zfs-on-root)
- [https://askubuntu.com/questions/1246232/ubuntu-20-04-thinks-its-out-of-free-space-but-it-isnt](https://askubuntu.com/questions/1246232/ubuntu-20-04-thinks-its-out-of-free-space-but-it-isnt)

###### Hide top bar on Ubuntu

↑ **Parent:** [Ubuntu feature request](#ubuntu-feature-request)

This has annoyed [Ciro Santilli](ciro-santilli.md) for many years, it is just too wasteful of screen space on [laptops](computer-hardware.md#laptop)!

Or likely more generally, on [GNOME desktop](software.md#gnome-desktop), which is the default [desktop environment](software.md#desktop-environment) as of [Ubuntu 22.10](#ubuntu-22-10).

Issues:
- [https://askubuntu.com/questions/1029881/how-to-hide-top-bar-in-ubuntu-18-04](https://askubuntu.com/questions/1029881/how-to-hide-top-bar-in-ubuntu-18-04)
- [https://stackoverflow.com/questions/71204126/how-to-remove-the-title-bar-of-gnome-applications](https://stackoverflow.com/questions/71204126/how-to-remove-the-title-bar-of-gnome-applications)
- [https://superuser.com/questions/1764903/am-i-able-to-hide-the-gnome-title-bar-for-applications](https://superuser.com/questions/1764903/am-i-able-to-hide-the-gnome-title-bar-for-applications)

###### Launchpad (website)

↑ **Parent:** [Ubuntu](#ubuntu)  
🏷️ **Tags:** [Software with bad user interface](technology.md#software-with-bad-user-interface)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Launchpad_(website))

#### Berkeley Software Distribution

↑ **Parent:** [List of operating systems](#list-of-operating-systems)

[https://en.wikipedia.org/wiki/List_of_BSD_operating_systems](https://en.wikipedia.org/wiki/List_of_BSD_operating_systems)

[Legal](law.md) issues stalled them at the turning point of the [Internet](computer.md#internet), and [Linux](#linux) won. Can't change [history](science.md#history).

Did [Apple](apple-inc.md) just fork it and made Mac OS X without giving anything back?

##### FreeBSD

↑ **Parent:** [Berkeley Software Distribution](#berkeley-software-distribution)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/FreeBSD)

#### TempleOS

↑ **Parent:** [List of operating systems](#list-of-operating-systems)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/TempleOS)

The OS that the [Gods](religion.md#god) ordered be made.

One is reminded of [Ulillillia](https://ulillillia.fandom.com/wiki/Ulillillia), see also: [https://www.youtube.com/watch?v=9-79yOZ13qg](https://www.youtube.com/watch?v=9-79yOZ13qg) The Story of Ulillillia by Atrocity Guide (2019)

We are [all somewhere in the spectrum](brain.md#autism).

<a id="video-i-like-elephants-and-god-likes-elephants"></a>
**[Video 2](#video-i-like-elephants-and-god-likes-elephants). I like elephants and God likes elephants.** [Source](https://www.youtube.com/watch?v=FoTYV22qZTg).

##### Terry A. Davis

↑ **Parent:** [TempleOS](#templeos)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Terry_A._Davis)

<a id="video-terry-a-davis-writes-a-message-to-the-cia"></a>
**[Video 3](#video-terry-a-davis-writes-a-message-to-the-cia). Terry A. Davis writes a message to the CIA.** [Source](https://www.youtube.com/watch?v=ozhHrzOXZkI).

### UNIX

↑ **Parent:** [Operating system](#operating-system)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/UNIX)

#### POSIX

↑ **Parent:** [UNIX](#unix)  
🏷️ **Tags:** [Good](cirism.md#good)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/POSIX)

The real explanation: [https://stackoverflow.com/questions/1780599/what-is-the-meaning-of-posix/31865755#31865755](https://stackoverflow.com/questions/1780599/what-is-the-meaning-of-posix/31865755#31865755)

##### Environment variable

↑ **Parent:** [POSIX](#posix)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Environment_variable)

Overview by [Ciro Santilli](ciro-santilli.md) at: [https://superuser.com/questions/284342/what-are-path-and-other-environment-variables-and-how-can-i-set-or-use-them/1864687#1864687](https://superuser.com/questions/284342/what-are-path-and-other-environment-variables-and-how-can-i-set-or-use-them/1864687#1864687)

###### POSIX environment variable

↑ **Parent:** [Environment variable](#environment-variable)

This section is about [POSIX](#posix) environment variable that have special effects.

They are documented by [POSIX](#posix) at: [https://pubs.opengroup.org/onlinepubs/9699919799/basedefs/V1_chap08.html#tag_08](https://pubs.opengroup.org/onlinepubs/9699919799/basedefs/V1_chap08.html#tag_08)

###### `PATH` environment variable

↑ **Parent:** [POSIX environment variable](#posix-environment-variable)

Some mentions by [Ciro Santilli](ciro-santilli.md) at: [https://superuser.com/questions/284342/what-are-path-and-other-environment-variables-and-how-can-i-set-or-use-them/1864687#1864687](https://superuser.com/questions/284342/what-are-path-and-other-environment-variables-and-how-can-i-set-or-use-them/1864687#1864687)

##### GNU Core Utils

↑ **Parent:** [POSIX](#posix)  
🏷️ **Tags:** [GNU package](software.md#gnu-package)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/GNU_Core_Utils)

[https://pubs.opengroup.org/onlinepubs/9699919799/utilities/contents.html](https://pubs.opengroup.org/onlinepubs/9699919799/utilities/contents.html)

###### GNU Core Utils command line utility

↑ **Parent:** [GNU Core Utils](#gnu-core-utils)

Non-[POSIX](#posix) only here.

###### sha1sum

↑ **Parent:** [GNU Core Utils command line utility](#gnu-core-utils-command-line-utility)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/sha1sum)

###### shred (UNIX)

↑ **Parent:** [GNU Core Utils command line utility](#gnu-core-utils-command-line-utility)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/shred_(UNIX))

##### Non-POSIX command line utility

↑ **Parent:** [POSIX](#posix)

##### POSIX command line utility

↑ **Parent:** [POSIX](#posix)  
🏷️ **Tags:** [Command line utility](software.md#command-line-utility)

Listed at: [https://pubs.opengroup.org/onlinepubs/9699919799/utilities/contents.htm](https://pubs.opengroup.org/onlinepubs/9699919799/utilities/contents.htm)

##### `diff`

↑ **Parent:** [POSIX](#posix)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/diff)

##### `grep`

↑ **Parent:** [POSIX](#posix)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/grep)

If you are a programmer, `grep` becomes a verb: "to grep" means "to search text files", much like "to [Google](google.md)" means "to search random stuff online".

###### grep large binary files

↑ **Parent:** [`grep`](#grep)

This is a weak point of grep, it can't handle large lines that don't fit fully into memory:
- [https://superuser.com/questions/1703029/is-there-a-limit-for-a-line-length-for-grep-command-to-process-correctly](https://superuser.com/questions/1703029/is-there-a-limit-for-a-line-length-for-grep-command-to-process-correctly) what is the grep line limit?
- [https://unix.stackexchange.com/questions/223078/best-way-to-grep-big-binary-file/758528#758528](https://unix.stackexchange.com/questions/223078/best-way-to-grep-big-binary-file/758528#758528) Ciro's `bgrep` canon
- large not required but mentioning bgrep anyways:
  - [https://superuser.com/questions/1368263/use-grep-for-a-long-line-to-get-the-part-of-the-line/1811969#1811969](https://superuser.com/questions/1368263/use-grep-for-a-long-line-to-get-the-part-of-the-line/1811969#1811969)
  - [https://unix.stackexchange.com/questions/217936/equivalent-command-to-grep-binary-files/758544#758544](https://unix.stackexchange.com/questions/217936/equivalent-command-to-grep-binary-files/758544#758544)
  - [https://stackoverflow.com/questions/2034799/how-to-truncate-long-matching-lines-returned-by-grep-or-ack/77263826#77263826](https://stackoverflow.com/questions/2034799/how-to-truncate-long-matching-lines-returned-by-grep-or-ack/77263826#77263826)
  - [https://stackoverflow.com/questions/9988379/how-to-grep-a-text-file-which-contains-some-binary-data](https://stackoverflow.com/questions/9988379/how-to-grep-a-text-file-which-contains-some-binary-data) leaving this one alone for now
- [https://stackoverflow.com/questions/65674717/how-to-check-if-a-binary-file-is-contained-inside-another-binary-from-the-linux](https://stackoverflow.com/questions/65674717/how-to-check-if-a-binary-file-is-contained-inside-another-binary-from-the-linux) search pattern from file

###### `bgrep`

↑ **Parent:** [`grep`](#grep)

[https://github.com/tmbinc/bgrep](https://github.com/tmbinc/bgrep)

Getting started tutorial: [https://unix.stackexchange.com/questions/223078/best-way-to-grep-a-big-binary-file/758528#758528](https://unix.stackexchange.com/questions/223078/best-way-to-grep-a-big-binary-file/758528#758528)

##### `sed`

↑ **Parent:** [POSIX](#posix)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/sed)

##### `wc` (unix)

↑ **Parent:** [POSIX](#posix)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/wc_(unix))

##### Standard streams

↑ **Parent:** [POSIX](#posix)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Standard_streams)

###### Standard input

↑ **Parent:** [Standard streams](#standard-streams)

###### Standard output

↑ **Parent:** [Standard streams](#standard-streams)

## Executable file format

↑ **Parent:** [Systems programming](systems-programming.md)

- [https://en.wikipedia.org/wiki/Executable](https://en.wikipedia.org/wiki/Executable)
- [https://en.wikipedia.org/wiki/Comparison_of_executable_file_formats](https://en.wikipedia.org/wiki/Comparison_of_executable_file_formats)
- [https://en.wikipedia.org/wiki/Object_file](https://en.wikipedia.org/wiki/Object_file)

### Executable and Linkable Format

↑ **Parent:** [Executable file format](#executable-file-format)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Executable_and_Linkable_Format)

For a quick and dirty introduction to the format, see: [ELF Hello World Tutorial](elf-hello-world.md).

<h4 id="elf-hello-world">ELF Hello World Tutorial</h4>

↑ **Parent:** [Executable and Linkable Format](#executable-and-linkable-format)

[This section is present in another page, follow this link to view it.](elf-hello-world.md)

## Molecular biology feels like systems programming

↑ **Parent:** [Systems programming](systems-programming.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Molecular_biology_feels_like_systems_programming)

Whenever [Ciro Santilli](ciro-santilli.md) learns about molecular biology, he can't help but to feel that it feels like programming, and notably systems programming and computer hardware design.

In some sense, the comparison is obvious: [DNA](dna.md) is clearly a programmable medium like any [assembly language](computer-hardware.md#assembly-language), but still, systems programming did give Ciro some further feelings.

- The most important analogy perhaps is observability, or more precisely the lack of it. For the computer, this is described at: [The lower level you go into a computer, the harder it is to observe things](computer.md#the-lower-level-you-go-into-a-computer-the-harder-it-is-to-observe-things).

  And then, when Ciro started learning a bit about biology techniques, he started to feel the exact same thing.

  For example when he played with [E. Coli Whole Cell Model by Covert Lab](e-coli-whole-cell-model-by-covert-lab.md), the main thing Ciro felt was: it is going to be hard to verify any of this data, because it is hard/impossible to know the concentration of each element in a cell as a function of time.

  More generally of course, this is exactly why making any biology discovery is so hard: we can't easily see what's going on inside the cell, and have to resort to indirect ways of doing so..

  This exact idea was highlighted by [I should have loved biology by James Somers](software.md#i-should-have-loved-biology-by-james-somers):

  > For a computer scientist, a biologist's methods can seem insane; the trouble comes from the fact that cells are too small, too numerous, too complex to analyze the way a programmer would, say in a [step-by-step debugger](software.md#debugger).

  And then just like in software, some of the methods biologists use to overcome the lack of visibility have direct software analogues:
  - add [instrumentation](computer.md#instrumentation-computer-programming) to cells, e.g. [GFP tagging](molecular-biology.md#gfp-tagging) comes to mind
  - [emulation](#emulator), e.g. [E. Coli Whole Cell Model by Covert Lab](e-coli-whole-cell-model-by-covert-lab.md)
- The boot process is another one. E.g. in [x86](computer-hardware.md#x86) the way that you start in 16-bit mode, largely compatible into the 70's, then move to 32-bit and finally 64, does feel a lot the way a earlier stages of embryo development looks more and more like more ancient animals.

Ciro likes to think that maybe that is why a hardcore [systems programmer](#systems-programmer) like [Bert Hubert](#bert-hubert) got into molecular biology.

Some other people who mention similar things:
- [I should have loved biology by James Somers](software.md#i-should-have-loved-biology-by-james-somers) highlights the [computer abstraction layer](computer.md#how-computers-work) analogy between the two:> Everywhere you look - the [compiler](software.md#compiler), the shell, the [CPU](computer-hardware.md#central-processing-unit), the DOM - is an abstraction hiding lifetimes of work.

## Virtualization

↑ **Parent:** [Systems programming](systems-programming.md)  
🏷️ **Tags:** [Good](cirism.md#good)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Virtualization)

### Docker (software)

↑ **Parent:** [Virtualization](#virtualization)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Docker_(software))

Docker is good.

As a lightweight virtualization however, it does break more often than full proper virtualization like [QEMU](#qemu) after some updates.

The images also appear to randomly update slightly and break things, even though you've specified e.g.:
```
FROM ubuntu:20.04
```

Also, we need more [Linux distributions buildable from source](#linux-distribution-buildable-from-source), especially with [Reproducible builds](software.md#reproducible-builds).

### Emulator

↑ **Parent:** [Virtualization](#virtualization)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Emulator)

One of the things [Ciro Santilli](ciro-santilli.md) really likes, see: [Linux Kernel Module Cheat](the-most-important-projects-done-by-ciro-santilli.md#linux-kernel-module-cheat).

If [computational physics](physics.md#computational-physics) simulates physics, emulators simulates [computers](computer.md).

#### List of emulators

↑ **Parent:** [Emulator](#emulator)

##### gem5

↑ **Parent:** [List of emulators](#list-of-emulators)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/gem5)

[https://cirosantilli.com/linux-kernel-module-cheat/gem5](https://cirosantilli.com/linux-kernel-module-cheat/gem5)

##### QEMU

↑ **Parent:** [List of emulators](#list-of-emulators)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/QEMU)

[https://cirosantilli.com/linux-kernel-module-cheat/introduction-to-qemu](https://cirosantilli.com/linux-kernel-module-cheat/introduction-to-qemu)

The leading open source cross architecture and KVM emulator of the 2010's.

Great way to understand how operating systems work, which [Ciro Santilli](ciro-santilli.md) used extensively in his [Linux Kernel Module Cheat](the-most-important-projects-done-by-ciro-santilli.md#linux-kernel-module-cheat).

[Ciro Santilli](ciro-santilli.md) has some good related articles listed under: [Section "The best articles by Ciro Santilli"](articles.md).

###### User mode emulation

↑ **Parent:** [QEMU](#qemu)

[User mode emulation](#user-mode-emulation) refers to the ability of certain [emulators](#emulator) to emulate userland code running on top of a specific [operating system](#operating-system), usually [Linux](#linux).

For example, [QEMU](#qemu) allows you to run a variety of userland [ELF](#executable-and-linkable-format) programs directly on it, without an underlying [Linux kernel](#linux-kernel) running.

User mode emulation is achieved by implementing [system calls](#system-call) and special filesystems such as `/dev` manually on the emulator one by one.

The general tradeoff is that simulation is less acurate as it may lack certain highly advanced kernel functionality you haven't implemented yet. But it is much easier to run executables with it, and you don't have to wait for boot to finish before running, you just run executables directly from the command line.

###### QEMU JavaScript port

↑ **Parent:** [QEMU](#qemu)  
🏷️ **Tags:** [JavaScript library](programming-language.md#javascript-library)

This is especially interesting for [user mode emulation](#user-mode-emulation).

<h6 id="qemu-js">QEMU.js</h6>

↑ **Parent:** [QEMU JavaScript port](#qemu-javascript-port)

Stopped 2019 apparently. Shame. We need something to be upstreamed!

- source code: [https://github.com/atrosinenko/qemujs](https://github.com/atrosinenko/qemujs)
- demo: [https://atrosinenko.github.io/qemujs-demo/](https://atrosinenko.github.io/qemujs-demo/)
- demo source code: [https://github.com/atrosinenko/qemujs-demo](https://github.com/atrosinenko/qemujs-demo)

###### Binary translation

↑ **Parent:** [QEMU](#qemu)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Binary_translation)

#### Emulator manager

↑ **Parent:** [Emulator](#emulator)

##### virt-manager

↑ **Parent:** [Emulator manager](#emulator-manager)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/virt-manager)

[https://virt-manager.org/](https://virt-manager.org/)

##### quickemu

↑ **Parent:** [Emulator manager](#emulator-manager)

This is a cool project that attempts to make it easy to emulate any of [the three operating systems](#the-three-operating-systems) on [QEMU](#qemu).

Homepage: [https://github.com/quickemu-project/quickemu](https://github.com/quickemu-project/quickemu)

Introductor tutorial by [Ciro Santilli](ciro-santilli.md): [https://askubuntu.com/questions/884534/how-to-run-ubuntu-desktop-on-qemu/1545712#1545712](https://askubuntu.com/questions/884534/how-to-run-ubuntu-desktop-on-qemu/1545712#1545712) intro

Unofrtunately as of 2025 the project was falling a bit back on support, and the latest versions of the two closed source systems were buggy, tested as of quickemu 4.9.7 on [Ubuntu 25.04](#ubuntu-25-04):
- [Windows 11](microsoft.md#windows-11): [https://github.com/quickemu-project/quickemu/issues/1475](https://github.com/quickemu-project/quickemu/issues/1475)
- [MacOS 14](apple-inc.md#macos-14) (Sonoma) installs [MacOS 15](apple-inc.md#macos-15), which is not listed on the list of installable systems: [https://github.com/quickemu-project/quickemu/issues/1561](https://github.com/quickemu-project/quickemu/issues/1561). The issue was closed, but it still happens.

###### quickemu HOWTO

↑ **Parent:** [quickemu](#quickemu)

###### quickemu directory sharing

↑ **Parent:** [quickemu HOWTO](#quickemu-howto)

Tutorial by [Ciro Santilli](ciro-santilli.md): [https://www.reddit.com/r/commandline/comments/v85fmx/comment/mpsvd25/](https://www.reddit.com/r/commandline/comments/v85fmx/comment/mpsvd25/)

###### quickemu serial without GUI

↑ **Parent:** [quickemu HOWTO](#quickemu-howto)

This would serve as a good workaround for the lack of clipboard and the default annoyiance of mouse capture!

I don't see how to get it working out of box immediately, but after you do on guest:
```
sudo apt install openssh-server
```
then the host terminal tells you the ssh command e.g.:
```
ssh user@localhost -p 22220
```
and that worked. You can also [quickemu](#quickemu) with:
```
quickemu --display none
```
to not get any annoying GUI.

## Systems programmer

↑ **Parent:** [Systems programming](systems-programming.md)  
🏷️ **Tags:** [Software engineer](software.md#software-engineer)

### The most awesome systems programmers

↑ **Parent:** [Systems programmer](#systems-programmer)

Notable mentions:
- Tom Tromey from [Red Hat](software.md#red-hat): [https://www.youtube.com/watch?v=RwDA3oIOtWw](https://www.youtube.com/watch?v=RwDA3oIOtWw) Dude's a [GDB](software.md#gnu-debugger) God! He might be gay from that talk.

Other notable people that are likely also awesome but Ciro has less familiarity with their contributions:
- [Dwayne Richard Hipp](#d-richard-hipp) from [SQLite](sql.md#sqlite)
- [Daniel Stenberg](https://en.wikipedia.org/wiki/Daniel_Stenberg) from cURL
- Michael Niedermayer also from [FFmpeg](software.md#ffmpeg). [http://ikaruga.co.uk/~snacky/mn.html](http://ikaruga.co.uk/~snacky/mn.html) highlights his brutal directness and efficiency, and sometimes sense of humour

### List of systems programmers

↑ **Parent:** [Systems programmer](#systems-programmer)

#### Bert Hubert

↑ **Parent:** [List of systems programmers](#list-of-systems-programmers)  
🏷️ **Tags:** [Ciro Santilli's e-soulmates](ciro-santilli-s-psychology-and-physiology.md#ciro-santilli-s-e-soulmates)

Co-founder of PowerDNS, an [open source](software.md#open-source-software) [dNS](computer.md#domain-name-system) implementation.

Homepage: [https://berthub.eu/](https://berthub.eu/) says:

> I sometimes contribute to science, I care a lot about [Europe](continent.md#europe), innovation, [biology](biology.md) & health

.  
All stuff Ciro cares about too! Cool dude! In particular Ciro loved [his quote of I should have loved biology](science.md#quote-i-should-have-loved-biology-by-james-somers-intro).

He's writing a fun-sounding book about [molecular biology](molecular-biology.md) as of 2022: [https://berthub.eu/dna-book](https://berthub.eu/dna-book). Appears to be closed source though. Ciro wonders if he really needs to sell the book for money after all those years though, rather than just publishing it online for free.

Looking at Bert just brings the [Dutch Golden Age](continent.md#dutch-golden-age), and more in particular [Antonie van Leeuwenhoek](biology.md#antonie-van-leeuwenhoek) to mind. Epic.

<a id="video-how-life-is-digital-by-bert-hubert-2021"></a>
**[Video 4](#video-how-life-is-digital-by-bert-hubert-2021). How life is Digital by Bert Hubert (2021)** [Source](https://www.youtube.com/watch?v=8aVBAcwDY7g). Just a "boring" overview of the [central dogma of molecular biology](molecular-biology.md#central-dogma-of-molecular-biology) ;-)

#### D. Richard Hipp

↑ **Parent:** [List of systems programmers](#list-of-systems-programmers)  
🏷️ **Tags:** [SQLite](sql.md#sqlite), [The most awesome systems programmers](#the-most-awesome-systems-programmers)

![](https://upload.wikimedia.org/wikipedia/en/e/e7/Richard_hipp.jpeg)

His standard C header seems to be as per example: [https://www.sqlite.org/src/file/ext/misc/rot13.c](https://www.sqlite.org/src/file/ext/misc/rot13.c)

```
** The author disclaims copyright to this source code.  In place of
** a legal notice, here is a blessing:
**
**    May you do good and not evil.
**    May you find forgiveness for yourself and forgive others.
**    May you share freely, never taking more than you give.
```

#### Eli Benderski

↑ **Parent:** [List of systems programmers](#list-of-systems-programmers)  
🏷️ **Tags:** [The most awesome systems programmers](#the-most-awesome-systems-programmers)

Homepage: [https://eli.thegreenplace.net/](https://eli.thegreenplace.net/)

Amazing [systems programming](systems-programming.md) tutorials. Whenever you [Google](google.md) a hard topic, his blog comes up.

Also has many great contributions on [Stack Overflow](stack-overflow.md): [https://stackoverflow.com/users/8206/eli-bendersky](https://stackoverflow.com/users/8206/eli-bendersky)

As of 2016, Eli worked at [Google](google.md) ([reference](https://dl.acm.org/citation.cfm?doid=2854038.2854041)). TODO before that, I had found his earlier info previously but lost it.

Eli focuses mostly on [compiler toolchains](software.md#compiler-toolchain).

He also has some [mathematics](mathematics.md) stuff, so cute: [https://eli.thegreenplace.net/2015/change-of-basis-in-linear-algebra/](https://eli.thegreenplace.net/2015/change-of-basis-in-linear-algebra/)

#### Fabrice Bellard

↑ **Parent:** [List of systems programmers](#list-of-systems-programmers)  
🏷️ **Tags:** [The most awesome systems programmers](#the-most-awesome-systems-programmers)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Fabrice_Bellard)

Creator of [QEMU](#qemu) and [FFmpeg](software.md#ffmpeg), both of which [Ciro Santilli](ciro-santilli.md) deeply respects. And a bunch other random stuff.

What is shocking about Fabrice this is that both are insanely important software that [Ciro Santilli](ciro-santilli.md) really likes, and both seem to be completely unrelated subjects!

[Google](google.md) made billions on top of this dude:
- [FFmpeg is the backend of YouTube](software.md#ffmpeg-is-the-backend-of-youtube)
- [QEMU](#qemu) is the default emulator for [Android Studio](https://en.wikipedia.org/wiki/Android_Studio) as of 2019, which [Android](#android-operating-system) developers use by default under the hood to develop Android Apps on their desktop without the need for a real device.

At last but not least, Fabrice also studied in the same school that [Ciro Santilli](ciro-santilli.md) studied in France, [École Polytechnique](ecole-polytechnique.md).

It is a shame that he keeps such a low profile, there are no videos of him on the web, and he [declines interviews](https://smartbear.com/blog/test-and-monitor/fabrice-bellard-portrait-of-a-super-productive-pro/).

Another surprising fact is that Fabrice has not worked for the "Big Tech Companies" as far as can be publicly seen, but rather mostly on smaller companies that he co-founded: [https://www.quora.com/Computer-Programmers/Computer-Programmers-Where-is-Fabrice-Bellard-employed](https://www.quora.com/Computer-Programmers/Computer-Programmers-Where-is-Fabrice-Bellard-employed)

And he's also into some completely random projcts unsurprisingly:
- [https://www.computerhistory.org/tdih/january/6/](https://www.computerhistory.org/tdih/january/6/) Computer Scientist Fabrice Bellard Announces Computing Pi to Record Number of Digits

Bibliography:
- [https://smartbear.com/de/blog/2011/fabrice-bellard-portrait-of-a-super-productive-pro/](https://smartbear.com/de/blog/2011/fabrice-bellard-portrait-of-a-super-productive-pro/) contains a list of his projects as of 2011

<a id="image-fabrice-bellard-in-2007"></a>
<img src="https://web.archive.org/web/20151227191405if_/https://dufoli.files.wordpress.com/2007/06/picture060.jpg" alt="" height="600">

**[Figure 2](#image-fabrice-bellard-in-2007). Fabrice Bellard in 2007**. [Source](https://dufoli.wordpress.com/2007/06/23/ammmmaaaazing-night/). At a restaurant with the author apparently. Plus Miguel De Icaza who was in Paris for some conference, which they all presumably attended.

<a id="image-fabrice-bellard-with-light"></a>
![](https://web.archive.org/web/20221216161034im_/https://images.computerhistory.org/tdih/06january-2.jpg?w=600)

**[Figure 3](#image-fabrice-bellard-with-light). Fabrice Bellard with light**. There are no in-focus images of Fabrice on the [Internet](computer.md#internet).

#### Linus Torvalds

↑ **Parent:** [List of systems programmers](#list-of-systems-programmers)  
🏷️ **Tags:** [The most awesome systems programmers](#the-most-awesome-systems-programmers)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Linus_Torvalds)

<h4 id="robert-o-callahan">Robert O'Callahan</h4>

↑ **Parent:** [List of systems programmers](#list-of-systems-programmers)

Creator of [Mozilla rr](software.md#mozilla-rr), of which [Ciro Santilli](ciro-santilli.md) is a huge fan of!

He quit Mozilla in 2016 to try and commercialize an `rr` extension called [Pernosco](software.md#pernosco).

But as of 2022, he advertised himself as part of "[Google](google.md) Research", so maybe that went under, sample source: [https://archive.ph/o9622](https://archive.ph/o9622). TODO when did he start? There's apparently an unrelated homonym: [https://www.linkedin.com/in/rob-ocallahan/](https://www.linkedin.com/in/rob-ocallahan/)

He's apparently very religious, and very New Zelandish, [https://twitter.com/rocallahan](https://twitter.com/rocallahan) auto-describes:

> Christian. Repatriate Kiwi.

[Terry A. Davis](#terry-a-davis) and [D. Richard Hipp](#d-richard-hipp) come to mind. One is tempted to speculate a correlation even, the proportion amongst systems programmers feels so much higher than in other areas of programming! Maybe it is because you have to be a God to do it in the first place.

<a id="video-robert-o-callahan-interview-by-toby-ho-2022"></a>
**[Video 5](#video-robert-o-callahan-interview-by-toby-ho-2022). Robert O'Callahan interview by Toby Ho (2022)** [Source](https://www.youtube.com/watch?v=dMroSfg9kio).

## ↑ Ancestors (6)

1. [Software](software.md)
2. [Computer](computer.md)
3. [Information technology](technology.md#information-technology)
4. [Area of technology](technology.md#area-of-technology)
5. [Technology](technology.md)
6. [Ciro Santilli's Homepage](README.md)

## ← Incoming links (6)

- [The best articles by Ciro Santilli](articles.md)
- [Ciro Santilli's Stack Overflow contributions](the-most-important-projects-done-by-ciro-santilli.md#ciro-santilli-s-stack-overflow-contributions)
- [Computer security](software.md#computer-security)
- [Eli Benderski](#eli-benderski)
- [Epic Stack Overflow users](stack-overflow.md#epic-stack-overflow-users)
- [Post OurBigBook job search round 2025](updates.md#post-ourbigbook-job-search-round-2025)
