# **Everything** is built from source and easily modifiable, powered by Buildroot

↑ **Parent:** [Linux Kernel Module Cheat](linux-kernel-module-cheat.md)

![](https://web.archive.org/web/20240424065053im_/https://bootlin.com/wp-content/uploads/2015/05/logo-buildroot.png)

The following are [stored in submodules](https://github.com/cirosantilli/linux-kernel-module-cheat/blob/master/submodules):
```
submodules/binutils-gdb/
submodules/buildroot/
submodules/gcc/
submodules/glibc/
submodules/linux/
submodules/qemu/
```

So you can modify source, rebuild and that's it, its in the VM.

E.g., let's hack the linux kernel:

```
asmlinkage __visible void __init __no_sanitize_address start_kernel(void)
{
  pr_info("I'VE HACKED THE LINUX KERNEL!!!");
```

Rebuild Linux:

```
./build-linux
```

Rerun:

```
./run
```

And after boot we see:

```
<6>[    0.000000] I'VE HACKED THE LINUX KERNEL!!!
```

## ↑ Ancestors (5)

1. [Linux Kernel Module Cheat](linux-kernel-module-cheat.md)
2. [Aratu Week 2024 Talk by Ciro Santilli: My Best Random Projects](../aratu-week-2024-talk-by-ciro-santilli-split.md)
3. [Talk by Ciro Santilli](../talk-by-ciro-santilli.md)
4. [Ciro Santilli](../ciro-santilli-split.md)
5. [Ciro Santilli's Homepage](../split.md)
