<h1 id="ubuntu-21-10-does-not-wake-up-from-suspend">Ubuntu 21.10 does not wake up from suspend</h1>

↑ **Parent:** [Ubuntu 21.10](ubuntu-21-10.md)

Please refer to [Video "Linus Torvalds saying "Nvidia Fuck You" (2012)"](nvidia.md#video-linus-torvalds-saying-nvidia-fuck-you-2012).

[https://askubuntu.com/questions/1032633/18-04-screen-remains-blank-after-wake-up-from-suspend/1391917#1391917](https://askubuntu.com/questions/1032633/18-04-screen-remains-blank-after-wake-up-from-suspend/1391917#1391917)

Reported at: [https://bugs.launchpad.net/ubuntu/+source/nvidia-graphics-drivers-470/+bug/1953674](https://bugs.launchpad.net/ubuntu/+source/nvidia-graphics-drivers-470/+bug/1953674)

On [Lenovo ThinkPad P51 (2017)](ciro-santilli-s-hardware/lenovo-thinkpad-p51-2017.md).

Does not happen every time, only some times. Can't figure out why. Usually happens when has suspended for a longer time.

[https://bugs.launchpad.net/ubuntu/+source/nvidia-graphics-drivers-470/+bug/1946303](https://bugs.launchpad.net/ubuntu/+source/nvidia-graphics-drivers-470/+bug/1946303) sounds like a likely report, [Nvidia](nvidia.md) driver version 470, but can't find those error messages anywhere. The last line of:
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

## ↑ Ancestors (14)

1. [Ubuntu 21.10](ubuntu-21-10.md)
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

## ← Incoming links (2)

- [Lenovo ThinkPad P51 (2017) log](ciro-santilli-s-hardware/lenovo-thinkpad-p51-2017-log.md)
- [Nvidia](nvidia.md)
