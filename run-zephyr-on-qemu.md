# Run Zephyr on [QEMU](qemu.md)

↑ **Parent:** [Run Zephyr on X](run-zephyr-on-x.md)  
🏷️ **Tags:** [QEMU](qemu.md)

Real hardware is for newbs. Real hardware is for newbs.

Tested on [Ubuntu 23.10](ubuntu-23-10.md) we approximately follow instructions from: [https://docs.zephyrproject.org/3.4.0/develop/getting_started/index.html](https://docs.zephyrproject.org/3.4.0/develop/getting_started/index.html) stopping before the "Flash the sample" section, as we don't flash [QEMU](qemu.md). We just run it.

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

The installation procedure install all [compiler toolchains](compiler-toolchain.md) for us, so we can then basically compile for any target. It also fetches the latest Git source code of Zephyr under:
```
~/zephyrproject/zephyr
```

The "most default" blinky hello world example which blinks an LED is a bit useless for us because QEMU doesn't have LEDs, so instead we are going to use one of the [UART](universal-asynchronous-receiver-transmitter.md) examples which will print characters we can see on QEMU stdout.

Let's start with the [hello world](hello-world-program.md) example on an x86 target:
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

## ↑ Ancestors (11)

1. [Run Zephyr on X](run-zephyr-on-x.md)
2. [Zephyr (operating system)](zephyr-operating-system.md)
3. [Embedded operating system](embedded-operating-system.md)
4. [Operating system](operating-system.md)
5. [Systems programming](systems-programming-split.md)
6. [Software](software-split.md)
7. [Computer](computer-split.md)
8. [Information technology](information-technology.md)
9. [Area of technology](area-of-technology.md)
10. [Technology](technology-split.md)
11. [Ciro Santilli's Homepage](split.md)
