# Kernel modules

↑ **Parent:** [Lots of in-tree examples](lots-of-in-tree-examples.md)

<a id="_69"></a>
[kernel\_modules/hello.c](https://github.com/cirosantilli/linux-kernel-module-cheat/blob/master/kernel_modules/hello.c)

<a id="_70"></a>
```
#include <linux/module.h>
#include <linux/kernel.h>

static int myinit(void)
{
	pr_info("hello init\n");
	/* 0 for success, any negative value means failure,
	 * E* consts if you want to specify failure cause.
	 * https://www.linux.com/learn/kernel-newbie-corner-loadable-kernel-modules-coming-and-going */
	return 0;
}

static void myexit(void)
{
	pr_info("hello exit\n");
}

module_init(myinit)
module_exit(myexit)
MODULE_LICENSE("GPL");
```

## ↑ Ancestors (6)

1. [Lots of in-tree examples](lots-of-in-tree-examples.md)
2. [Linux Kernel Module Cheat](linux-kernel-module-cheat.md)
3. [Aratu Week 2024 Talk by Ciro Santilli: My Best Random Projects](../aratu-week-2024-talk-by-ciro-santilli-split.md)
4. [Talk by Ciro Santilli](../talk-by-ciro-santilli.md)
5. [Ciro Santilli](../ciro-santilli-split.md)
6. [Ciro Santilli's Homepage](../split.md)
