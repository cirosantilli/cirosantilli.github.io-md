<h1 id="ubuntu-23-04-boot-broken-on-kernel-6-2">Ubuntu 23.04 boot broken on kernel 6.2</h1>

↑ **Parent:** [Ubuntu 23.04](ubuntu-23-04.md)

On [Lenovo ThinkPad P51 (2017)](ciro-santilli-s-hardware/lenovo-thinkpad-p51-2017.md).

Switching to the other installed kernel, 5.9 made boot work.

The solution on kernel 6.2 was:
```
sudo apt instal nvidia-driver-515
```
as per comments under: [https://bugs.launchpad.net/ubuntu/+source/linux/+bug/2012559](https://bugs.launchpad.net/ubuntu/+source/linux/+bug/2012559). This also made the nvidia driver work: [Find GPU information in Ubuntu](find-gpu-information-in-ubuntu.md).

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

## ↑ Ancestors (14)

1. [Ubuntu 23.04](ubuntu-23-04.md)
2. [Ubuntu release](ubuntu-release.md)
3. [Ubuntu](ubuntu.md)
4. [List of Linux distributions](list-of-linux-distributions.md)
5. [Linux](linux.md)
6. [List of operating systems](list-of-operating-systems.md)
7. [Operating system](operating-system.md)
8. [Systems programming](systems-programming-split.md)
9. [Software](software-split.md)
10. [Computer](computer-split.md)
11. [Information technology](information-technology.md)
12. [Area of technology](area-of-technology.md)
13. [Technology](technology-split.md)
14. [Ciro Santilli's Homepage](split.md)
