<h1 id="gfx-v11-0-priv-reg-irq-register-access-in-command-stream">gfx_v11_0_priv_reg_irq: register access in command stream</h1>

↑ **Parent:** [Ubuntu 23.10](ubuntu-23-10.md)

Had this happen on [P14s](ciro-santilli-s-hardware/lenovo-thinkpad-p14s-gen4-amd.md) on [Ubuntu 23.10](ubuntu-23-10.md) while causally using [Chromium](chromium-web-browser.md). The screen went blank for a few seconds, but it apparently managed to reboot itself, and things started working again, except that and most windows were killed:
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
It appears to be a bug in the [AMDGPU](amdgpu.md) open source driver.

Related reports:
- [https://gitlab.freedesktop.org/drm/amd/-/issues/2451](https://gitlab.freedesktop.org/drm/amd/-/issues/2451)
- [https://gitlab.freedesktop.org/drm/amd/-/issues/475](https://gitlab.freedesktop.org/drm/amd/-/issues/475)
- [https://github.com/ValveSoftware/csgo-osx-linux/issues/3386](https://github.com/ValveSoftware/csgo-osx-linux/issues/3386)

I think this was on [Wayland](wayland.md). Possibly relatd but on [X Window System](x-window-system.md), crashed the UI, showed message "oh no! Something has gone wrong."
```
2024-01-13_21-55-07@ciro@ciro-p14s$ cat /var/log/apport.log
ERROR: apport (pid 975172) 2024-01-13 21:41:02,087: host pid 3528 crashed in a separate mount namespace, ignoring
INFO: apport (pid 975227) 2024-01-13 21:41:02,398: called for pid 2728, signal 5, core limit 0, dump mode 1
INFO: apport (pid 975227) 2024-01-13 21:41:02,401: executable: /usr/bin/gnome-shell (command line "/usr/bin/gnome-shell")
INFO: apport (pid 975227) 2024-01-13 21:41:12,667: wrote report /var/crash/_usr_bin_gnome-shell.1000.crash
```

## ↑ Ancestors (14)

1. [Ubuntu 23.10](ubuntu-23-10.md)
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
