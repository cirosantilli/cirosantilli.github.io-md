# Kernel GDB step debugging just works

↑ **Parent:** [Linux Kernel Module Cheat](linux-kernel-module-cheat.md)

<a id="_60"></a>
Start QEMU and wait for GDB:<a id="_61"></a>

```
./run --gdb-wait
```

<a id="_62"></a>
On another shell, connect GDB to QEMU and run up to a symbol that shows up at boot:<a id="_63"></a>

```
./run-gdb start_kernel
```

<a id="_64"></a>
Outcome: we are GDB step debugging the Linux Kernel:<a id="_65"></a>

```
Breakpoint 1, start_kernel () at /root/lkmc/submodules/linux/init/main.c:837
837     {
loading vmlinux
(gdb) n
841             set_task_stack_end_magic(&init_task);
(gdb) l
836     asmlinkage __visible void __init __no_sanitize_address start_kernel(void)
837     {
838             char *command_line;
839             char *after_dashes;
840
841             set_task_stack_end_magic(&init_task);
842             smp_setup_processor_id();
843             debug_objects_early_init();
844
845             cgroup_init_early();
(gdb) p &init_task
$1 = (struct task_struct *) 0xffffffff82012840 <init_task>
(gdb) bt
#0  start_kernel () at /root/lkmc/submodules/linux/init/main.c:841
#1  0xffffffff8215145c in x86_64_start_reservations (real_mode_data=<optimized out>) at /root/lkmc/submodules/linux/arch/x86/kernel/head64.c:490
#2  0xffffffff821514e3 in x86_64_start_kernel (real_mode_data=0x138d0 <bts_ctx+2256> <error: Cannot access memory at address 0x138d0>) at /root/lkmc/submodules/linux/arch/x86/kernel/head64.c:471
#3  0xffffffff810000e6 in secondary_startup_64 () at /root/lkmc/submodules/linux/arch/x86/kernel/head_64.S:243
#4  0x0000000000000000 in ?? ()
(gdb) up
#1  0xffffffff8215145c in x86_64_start_reservations (real_mode_data=<optimized out>) at /root/lkmc/submodules/linux/arch/x86/kernel/head64.c:490
490             start_kernel();
(gdb) l
485                     break;
486             default:
487                     break;
488             }
489
490             start_kernel();
491     }
```

## ↑ Ancestors (5)

1. [Linux Kernel Module Cheat](linux-kernel-module-cheat.md)
2. [Aratu Week 2024 Talk by Ciro Santilli: My Best Random Projects](../aratu-week-2024-talk-by-ciro-santilli-split.md)
3. [Talk by Ciro Santilli](../talk-by-ciro-santilli.md)
4. [Ciro Santilli](../ciro-santilli-split.md)
5. [Ciro Santilli's Homepage](../split.md)
