# **Everything** is built from source and easily modifiable, powered by Buildroot

↑ **Parent:** [Linux Kernel Module Cheat](linux-kernel-module-cheat.md)

<a id="_48"></a>
![](https://web.archive.org/web/20240424065053im_/https://bootlin.com/wp-content/uploads/2015/05/logo-buildroot.png)

<a id="_49"></a>
The following are [stored in submodules](https://github.com/cirosantilli/linux-kernel-module-cheat/blob/master/submodules):<a id="_50"></a>

```
submodules/binutils-gdb/
submodules/buildroot/
submodules/gcc/
submodules/glibc/
submodules/linux/
submodules/qemu/
```

<a id="_51"></a>
So you can modify source, rebuild and that's it, its in the VM.

<a id="_52"></a>
E.g., let's hack the linux kernel:

<a id="_53"></a>
```
asmlinkage __visible void __init __no_sanitize_address start_kernel(void)
{
  pr_info("I'VE HACKED THE LINUX KERNEL!!!");
```

<a id="_54"></a>
Rebuild Linux:

<a id="_55"></a>
```
./build-linux
```

<a id="_56"></a>
Rerun:

<a id="_57"></a>
```
./run
```

<a id="_58"></a>
And after boot we see:

<a id="_59"></a>
```
<6>[    0.000000] I'VE HACKED THE LINUX KERNEL!!!
```

## ↑ Ancestors (5)

1. [Linux Kernel Module Cheat](linux-kernel-module-cheat.md)
2. [Aratu Week 2024 Talk by Ciro Santilli: My Best Random Projects](../aratu-week-2024-talk-by-ciro-santilli-split.md)
3. [Talk by Ciro Santilli](../talk-by-ciro-santilli.md)
4. [Ciro Santilli](../ciro-santilli-split.md)
5. [Ciro Santilli's Homepage](../split.md)
