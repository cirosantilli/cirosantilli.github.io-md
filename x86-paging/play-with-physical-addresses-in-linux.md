# Play with physical addresses in Linux

↑ **Parent:** [Linux kernel usage](linux-kernel-usage.md)

<a id="_325"></a>
Convert virtual addresses to physical from user space with `/proc/<pid>/pagemap` and from kernel space with `virt_to_phys`:<a id="_326"></a>

<a id="_327"></a>
- [https://stackoverflow.com/questions/5748492/is-there-any-api-for-determining-the-physical-address-from-virtual-address-in-li/45128487#45128487](https://stackoverflow.com/questions/5748492/is-there-any-api-for-determining-the-physical-address-from-virtual-address-in-li/45128487#45128487)
<a id="_328"></a>
- [https://github.com/cirosantilli/linux-kernel-module-cheat/blob/1f4f7faebacca75267cc1d63bfeffc30080d017d/kernel_module/user/virt_to_phys_user.c](https://github.com/cirosantilli/linux-kernel-module-cheat/blob/1f4f7faebacca75267cc1d63bfeffc30080d017d/kernel_module/user/virt_to_phys_user.c)
<a id="_329"></a>
- `virt_to_phys`:<a id="_330"></a>

  <a id="_331"></a>
  - [https://github.com/cirosantilli/linux-kernel-module-cheat/blob/0677dbd4b582d1a913462d75caad0abf21e87f32/kernel_module/virt_to_phys.c](https://github.com/cirosantilli/linux-kernel-module-cheat/blob/0677dbd4b582d1a913462d75caad0abf21e87f32/kernel_module/virt_to_phys.c)
  <a id="_332"></a>
  - [https://github.com/cirosantilli/linux-kernel-module-cheat/blob/1f4f7faebacca75267cc1d63bfeffc30080d017d/kernel_module/user/virt_to_phys_user.c](https://github.com/cirosantilli/linux-kernel-module-cheat/blob/1f4f7faebacca75267cc1d63bfeffc30080d017d/kernel_module/user/virt_to_phys_user.c)

<a id="_333"></a>
Dump all page tables from userspace with `/proc/<pid>/maps` and `/proc/<pid>/pagemap`:<a id="_334"></a>

<a id="_335"></a>
- [https://github.com/cirosantilli/linux-kernel-module-cheat/blob/1f4f7faebacca75267cc1d63bfeffc30080d017d/kernel_module/user/virt_to_phys_user.c](https://github.com/cirosantilli/linux-kernel-module-cheat/blob/1f4f7faebacca75267cc1d63bfeffc30080d017d/kernel_module/user/virt_to_phys_user.c)
<a id="_336"></a>
- [https://stackoverflow.com/questions/6284810/proc-pid-pagemaps-and-proc-pid-maps-linux/45500208#45500208](https://stackoverflow.com/questions/6284810/proc-pid-pagemaps-and-proc-pid-maps-linux/45500208#45500208)

<a id="_337"></a>
Read and write physical addresses from userspace with `/dev/mem`:<a id="_338"></a>

<a id="_339"></a>
- [https://stackoverflow.com/questions/12040303/accessing-physical-address-from-user-space/45127890#45127890](https://stackoverflow.com/questions/12040303/accessing-physical-address-from-user-space/45127890#45127890)
<a id="_340"></a>
- [https://free-electrons.com/pub/mirror/devmem2.c](https://free-electrons.com/pub/mirror/devmem2.c)

## ↑ Ancestors (13)

1. [Linux kernel usage](linux-kernel-usage.md)
2. [x86 Paging Tutorial](../x86-paging-split.md)
3. [x86](../x86.md)
4. [List of instruction set architectures](../list-of-instruction-set-architectures.md)
5. [Instruction set architecture](../instruction-set-architecture.md)
6. [Processor (computing)](../processor-computing.md)
7. [Computer hardware component type](../computer-hardware-component-type.md)
8. [Computer hardware](../computer-hardware-split.md)
9. [Computer](../computer-split.md)
10. [Information technology](../information-technology.md)
11. [Area of technology](../area-of-technology.md)
12. [Technology](../technology-split.md)
13. [Ciro Santilli's Homepage](../split.md)
