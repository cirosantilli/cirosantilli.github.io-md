<h1 id="couldn-t-save-system-state-minimum-free-space-to-take-a-snapshot-and-preserve-zfs-performance-is">couldn't save system state: Minimum free space to take a snapshot and preserve ZFS performance is</h1>

↑ **Parent:** [Ubuntu feature request](ubuntu-feature-request.md)

This BS started after the move to ZFS. The temporary solution appears to be: [https://askubuntu.com/questions/1293685/out-of-space-on-boot-zpool-and-cant-run-updates-anymore/1374204#1374204](https://askubuntu.com/questions/1293685/out-of-space-on-boot-zpool-and-cant-run-updates-anymore/1374204#1374204)

And then this to disable automatic snapshots in the future: [https://askubuntu.com/questions/1233049/disable-automatic-zsys-snapshots-zfs-on-root/1279593#1279593](https://askubuntu.com/questions/1233049/disable-automatic-zsys-snapshots-zfs-on-root/1279593#1279593)
```
sudo mv /etc/apt/apt.conf.d/90_zsys_system_autosnapshot /etc/apt/apt.conf.d/90_zsys_system_autosnapshot.disabled
```

God, this is so annoying:
- [https://askubuntu.com/questions/1382986/zfs-bpool-is-almost-full-how-can-i-free-up-space-so-i-can-keep-updating-my-syst](https://askubuntu.com/questions/1382986/zfs-bpool-is-almost-full-how-can-i-free-up-space-so-i-can-keep-updating-my-syst)
- [https://askubuntu.com/questions/1233049/disable-automatic-zsys-snapshots-zfs-on-root](https://askubuntu.com/questions/1233049/disable-automatic-zsys-snapshots-zfs-on-root)
- [https://askubuntu.com/questions/1246232/ubuntu-20-04-thinks-its-out-of-free-space-but-it-isnt](https://askubuntu.com/questions/1246232/ubuntu-20-04-thinks-its-out-of-free-space-but-it-isnt)

## ↑ Ancestors (13)

1. [Ubuntu feature request](ubuntu-feature-request.md)
2. [Ubuntu](ubuntu.md)
3. [List of Linux distributions](list-of-linux-distributions.md)
4. [Linux](linux.md)
5. [List of operating systems](list-of-operating-systems.md)
6. [Operating system](operating-system.md)
7. [Systems programming](systems-programming-split.md)
8. [Software](software-split.md)
9. [Computer](computer-split.md)
10. [Information technology](information-technology.md)
11. [Area of technology](area-of-technology.md)
12. [Technology](technology-split.md)
13. [Ciro Santilli's Homepage](split.md)
