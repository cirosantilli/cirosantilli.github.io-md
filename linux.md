# Linux

↑ **Parent:** [List of operating systems](list-of-operating-systems.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Linux)

It ain't perfect, but it's decent enough.

From a technical point of view, it can do anything that [Microsoft Windows](microsoft-windows.md) can. Except being forcefully installed on every non-[MacOS](macos.md) 2019 computer you can buy.

[Ciro Santilli](ciro-santilli-split.md)'s conversion to Linux happened around 2012, and was a central part of [Ciro Santilli's Open Source Enlightenment](ciro-santilli-s-open-source-enlightenment.md), since it fundamentally enables the discovery and contribution to [open source software](open-source-software.md). Because what awesome open source person would waste time porting their amazing projects to closed source OSes?

Ciro's modest nature can be seen as he likes to compare this event [Buddha's Great Renunciation](https://en.wikipedia.org/wiki/Great_Renunciation).

Linux should track glibc and [POSIX command line utilities](posix-command-line-utility.md) in-tree like [BSD Operating System](berkeley-software-distribution.md), otherwise people have [no way to get the thing running in the first place without blobs or large out-of-tree scripts](linux-kernel-module-cheat-split.md)! [Another enlightened soul](https://blog.farhan.codes/2018/06/25/linux-maintains-bugs-the-real-reason-ifconfig-on-linux-is-deprecated/) who agrees.

Particularly interesting in the history of Linux is how it won out over the open competitors that were coming up in the time: [MINIX](https://en.wikipedia.org/wiki/MINIX) (see [the chat](https://ponderwall.com/index.php/2019/04/02/linux-tanenbaum-newsgroup-linus-torvalds/)) and [BSD Operating System](berkeley-software-distribution.md) that got [legally bogged down](https://en.wikipedia.org/wiki/UNIX_System_Laboratories,_Inc._v._Berkeley_Software_Design,_Inc.) at the critical growth moment.

You must watch this: [truth Happens advertisement by Red Hat](truth-happens-advertisement-by-red-hat.md).

<a id="image-xkcd-619-supported-features"></a>
![](https://web.archive.org/web/20210129024945if_/https://imgs.xkcd.com/comics/supported_features.png)

**[Figure 1](#image-xkcd-619-supported-features). xkcd 619: Supported Features**. [Source](https://xkcd.com/619/). This perfectly illustrates Linux development. First features that matter. Then useless features.

<a id="video-bill-gates-vs-steve-jobs-by-epic-rap-battles-of-history-2012"></a>
**[Video 1](#video-bill-gates-vs-steve-jobs-by-epic-rap-battles-of-history-2012). Bill Gates vs Steve Jobs by Epic Rap Battles of History (2012)** [Source](http://youtube.com/watch?v=njos57IJf-0). Just stop whatever you are doing, and watch this right now. "I'm on [Linux](linux.md), bitch, I thought you GNU". [Fandom explanations](https://epicrapbattlesofhistory.fandom.com/wiki/Steve_Jobs_vs_Bill_Gates/Rap_Meanings). It is just a shame that the Bill Gates actor looks absolutely nothing like the real gates. Actually, the entire Gates/Jobs parts are good, but not genial. But the Linux one is.

**Table of contents**

- [Tux (mascot)](tux-mascot.md)
- [Linux kernel](linux-kernel.md)
  - [Linux kernel system](linux-kernel-system.md)
  - [Linux kernel security system](linux-kernel-security-system.md)
    - [Landlock (Linux kernel)](landlock-linux-kernel.md)
  - [Linux Foundation](linux-foundation.md)
  - [Linux kernel build output](linux-kernel-build-output.md)
    - [vmlinux](vmlinux.md)
  - [Step debug the Linux kernel](step-debug-the-linux-kernel.md)
    - [JTAG](jtag.md)
      - [Serial wire debug](serial-wire-debug.md)
  - [Linux kernel bibliography](linux-kernel-bibliography.md)
    - [Linux insides](linux-insides.md)
    - [Linux Device Drivers book](linux-device-drivers-book.md)
      - [Linux Device Drivers book edition](linux-device-drivers-book-edition.md)
        - [Linux Device Drivers book 3rd edition](linux-device-drivers-book-3rd-edition.md)
          - [martinezjavier/ldd3](martinezjavier-ldd3.md)
- [Linux distribution](linux-distribution.md)
  - [Linux distribution buildable from source](linux-distribution-buildable-from-source.md)
  - [Package manager](package-manager.md)
  - [Cross distro package manager](cross-distro-package-manager.md)
    - [AppImage](appimage.md)
    - [Flatpak](flatpak.md)
    - [Snap (package manager)](snap-package-manager.md)
- [List of Linux distributions](list-of-linux-distributions.md)
  - [Android (operating system)](android-operating-system.md)
    - [Android Open Source Project](android-open-source-project.md)
    - [Transfer Android 11 camera videos to Ubuntu 20.10](transfer-android-11-camera-videos-to-ubuntu-20-10.md)
    - [F-Droid](f-droid.md)
  - [Arch Linux](arch-linux.md)
  - [Buildroot](buildroot.md)
    - [BusyBox](busybox.md)
  - [NixOS](nixos.md)
  - [Ubuntu](ubuntu.md)
    - [Canonical (company)](canonical-company.md)
    - [apport (software)](apport-software.md)
      - [apport-cli](apport-cli.md)
    - [Ubuntu HOWTO](ubuntu-howto.md)
      - [Make a bug report for a crash on Ubuntu](make-a-bug-report-for-a-crash-on-ubuntu.md)
      - [Find GPU information in Ubuntu](find-gpu-information-in-ubuntu.md)
      - [How to report Ubuntu crashes](how-to-report-ubuntu-crashes.md)
      - [Compile Linux kernel for Ubuntu](compile-linux-kernel-for-ubuntu.md)
      - [Emulate Windows on Ubuntu](emulate-windows-on-ubuntu.md)
    - [Ubuntu release](ubuntu-release.md)
      - [Ubuntu 26.04](ubuntu-26-04.md)
      - [Ubuntu 25.10](ubuntu-25-10.md)
        - [Ubuntu 25.10 bug](ubuntu-25-10-bug.md)
      - [Ubuntu 25.04](ubuntu-25-04.md)
      - [Ubuntu 24.10](ubuntu-24-10.md)
      - [Ubuntu 24.04](ubuntu-24-04.md)
        - [Ubuntu 24.04 installer "Erase disk and install Ubuntu" doesn't work when BitLocker enabled](ubuntu-24-04-installer-erase-disk-and-install-ubuntu-doesn-t-work-when-bitlocker-enabled.md)
        - [Ubuntu 24.04 "The application files has closed unexpectedly"](ubuntu-24-04-the-application-files-has-closed-unexpectedly.md)
      - [Ubuntu 23.10](ubuntu-23-10.md)
        - [gfx\_v11\_0\_priv\_reg\_irq: register access in command stream](gfx-v11-0-priv-reg-irq-register-access-in-command-stream.md)
        - [Unable to lock screen on Ubuntu](unable-to-lock-screen-on-ubuntu.md)
      - [Ubuntu 23.04](ubuntu-23-04.md)
        - [Ubuntu 23.04 boot broken on kernel 6.2](ubuntu-23-04-boot-broken-on-kernel-6-2.md)
      - [Ubuntu 22.10](ubuntu-22-10.md)
      - [Ubuntu 22.04](ubuntu-22-04.md)
        - [snap "Pending Update of" notifications](snap-pending-update-of-notifications.md)
      - [Ubuntu 21.10](ubuntu-21-10.md)
        - [Ubuntu 21.10 does not wake up from suspend](ubuntu-21-10-does-not-wake-up-from-suspend.md)
      - [Ubuntu 21.04](ubuntu-21-04.md)
      - [Ubuntu 20.04](ubuntu-20-04.md)
      - [Ubuntu 18.04](ubuntu-18-04.md)
      - [Ubuntu 16.04](ubuntu-16-04.md)
    - [Ubuntu feature request](ubuntu-feature-request.md)
      - [couldn't save system state: Minimum free space to take a snapshot and preserve ZFS performance is](couldn-t-save-system-state-minimum-free-space-to-take-a-snapshot-and-preserve-zfs-performance-is.md)
      - [Hide top bar on Ubuntu](hide-top-bar-on-ubuntu.md)
    - [Launchpad (website)](launchpad-website.md)

## 🏷️ Tagged (1)

- [Linux networking HOWTO](linux-networking-howto.md)

## ↑ Ancestors (9)

1. [List of operating systems](list-of-operating-systems.md)
2. [Operating system](operating-system.md)
3. [Systems programming](systems-programming-split.md)
4. [Software](software-split.md)
5. [Computer](computer-split.md)
6. [Information technology](information-technology.md)
7. [Area of technology](area-of-technology.md)
8. [Technology](technology-split.md)
9. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (14)

- [Berkeley Software Distribution](berkeley-software-distribution.md)
- [Ciro Santilli's Open Source Enlightenment](ciro-santilli-s-open-source-enlightenment.md)
- [Excessive encapsulation is the root of much evil](excessive-encapsulation-is-the-root-of-much-evil.md)
- [Info-ZIP](info-zip.md)
- [Linux](linux.md)
- [MacOS](macos.md)
- [Microsoft Windows](microsoft-windows.md)
- [Open source software](open-source-software.md)
- [Peer authentication](peer-authentication.md)
- [PostgreSQL](postgresql.md)
- [The Bibites](the-bibites.md)
- [The three operating systems](the-three-operating-systems.md)
- [Truth Happens advertisement by Red Hat](truth-happens-advertisement-by-red-hat.md)
- [User mode emulation](user-mode-emulation.md)
