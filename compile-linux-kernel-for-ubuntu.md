# Compile Linux kernel for Ubuntu

↑ **Parent:** [Ubuntu HOWTO](ubuntu-howto.md)

This section describes our attempts at compiling the [Linux kernel](linux-kernel.md) for [Ubuntu](ubuntu.md) so as to use the exact patches and build configuration as used for a given [Ubuntu release](ubuntu-release.md). The same toolchain would also be ideal, but perhaps this would require a [Linux distribution buildable from source](linux-distribution-buildable-from-source.md).

[https://canonical-kteam-docs.readthedocs-hosted.com/en/public/how-to/build-kernel.html](https://canonical-kteam-docs.readthedocs-hosted.com/en/public/how-to/build-kernel.html) seems promising it says that for [Ubuntu 24.04](ubuntu-24-04.md) and above you should do the following which was tested on [Ubuntu 24.10](ubuntu-24-10.md):

```
sudo cp /etc/apt/sources.list /etc/apt/sources.list~
sudo sed -Ei 's/^# deb-src /deb-src /' /etc/apt/sources.list
sudo apt-get update
sudo apt build-dep -y linux linux-image-unsigned-$(uname -r)
sudo apt install -y fakeroot llvm libncurses-dev dwarves
apt source linux-image-unsigned-$(uname -r)
~/tmp/ubuntu/linux-6.11.0
cd linux-6.11.0
chmod a+x debian/rules
chmod a+x debian/scripts/*
chmod a+x debian/scripts/misc/*
fakeroot debian/rules clean
fakeroot debian/rules binary
```

The build is extremely slow compared to a build of a more embedded and specifically targeted minimal kernel, and took about 2 hours on [P14s](ciro-santilli-s-hardware/lenovo-thinkpad-p14s-gen4-amd.md). Their philosophy is likely to enable as many drivers as possible so that a single download will work for everyone. Which makes sense, fair enough. It would be cute though if there was a smarter way. Oh well.

After it finally finishes the build including our [vmlinux](vmlinux.md) is present at:

```
linux-6.11.0/debian/build/build-generic
```

## ↑ Ancestors (13)

1. [Ubuntu HOWTO](ubuntu-howto.md)
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
