# Get a Linux terminal on QEMU

↑ **Parent:** [Linux Kernel Module Cheat](linux-kernel-module-cheat.md)

<a id="_38"></a>
![](https://upload.wikimedia.org/wikipedia/commons/4/45/Qemu_logo.svg)

**[Figure 20](#_38)** [Source](https://commons.wikimedia.org/wiki/File:Qemu_logo.svg).

<a id="_39"></a>
One time setup:<a id="_40"></a>

```
git clone https://github.com/cirosantilli/linux-kernel-module-cheat
cd linux-kernel-module-cheat
sudo apt install docker
python3 -m venv .venv
. .venv/bin/activate
./setup
./run-docker create
./run-docker sh
```

<a id="_41"></a>
You are now in Docker.

<a id="_42"></a>
Build everything from source inside docker:<a id="_43"></a>

```
./build --download-dependencies qemu-buildroot
```

<a id="_44"></a>
Boot Linux and get a userland shell:<a id="_45"></a>

```
./run
```

<a id="_46"></a>
Outcome:<a id="_47"></a>

```
<6>[    1.383114] NET: Registered protocol family 17
<6>[    1.383682] 9pnet: Installing 9P2000 support
<6>[    1.385473] IPI shorthand broadcast: enabled
<6>[    1.385701] sched_clock: Marking stable (1355697980, 27047205)->(1385555667, -2810482)
<6>[    1.387744] ALSA device list:
<6>[    1.387843]   No soundcards found.
<6>[    1.535981] ata2.00: ATAPI: QEMU DVD-ROM, 2.5+, max UDMA/100
<5>[    1.543470] scsi 1:0:0:0: CD-ROM            QEMU     QEMU DVD-ROM     2.5+ PQ: 0 ANSI: 5
<6>[    1.548952] EXT4-fs (vda): mounting ext2 file system using the ext4 subsystem
<6>[    1.555909] EXT4-fs (vda): mounted filesystem without journal. Opts: (null)
<6>[    1.556145] VFS: Mounted root (ext2 filesystem) on device 254:0.
<6>[    1.557451] devtmpfs: mounted
<6>[    1.605639] Freeing unused kernel image (initmem) memory: 1248K
<6>[    1.605875] Write protecting the kernel read-only data: 16384k
<6>[    1.607977] Freeing unused kernel image (text/rodata gap) memory: 2044K
<6>[    1.610190] Freeing unused kernel image (rodata/data gap) memory: 1012K
<6>[    1.610495] Run /sbin/init as init process
<6>[    1.683311] tsc: Refined TSC clocksource calibration: 3293.671 MHz
<6>[    1.683618] clocksource: tsc: mask: 0xffffffffffffffff max_cycles: 0x2f79f177aae, max_idle_ns: 440795226653 ns
<6>[    1.683849] clocksource: Switched to clocksource tsc
<3>[    1.694241] 9pnet_virtio: no channels available for device host_data
mount: mounting host_data on /mnt/9p/data failed: No such file or directory
qemu-system-x86_64: warning: 9p: degraded performance: a reasonable high msize should be chosen on client/guest side (chosen msize is <= 8192). See https://wiki.qemu.org/Documentation/9pset.
<3>[    1.712287] overlayfs: overlapping upperdir path
mount: mounting overlay on /mnt/overlay failed: Too many levels of symbolic links
hello S98
hello .profile
/lkmc
root@buildroot# pwd
/lkmc
/lkmc
root@buildroot#
```

## ↑ Ancestors (5)

1. [Linux Kernel Module Cheat](linux-kernel-module-cheat.md)
2. [Aratu Week 2024 Talk by Ciro Santilli: My Best Random Projects](../aratu-week-2024-talk-by-ciro-santilli-split.md)
3. [Talk by Ciro Santilli](../talk-by-ciro-santilli.md)
4. [Ciro Santilli](../ciro-santilli-split.md)
5. [Ciro Santilli's Homepage](../split.md)
