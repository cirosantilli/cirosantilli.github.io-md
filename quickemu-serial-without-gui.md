# quickemu serial without GUI

↑ **Parent:** [quickemu HOWTO](quickemu-howto.md)

This would serve as a good workaround for the lack of clipboard and the default annoyiance of mouse capture!

I don't see how to get it working out of box immediately, but after you do on guest:
```
sudo apt install openssh-server
```
then the host terminal tells you the ssh command e.g.:
```
ssh user@localhost -p 22220
```
and that worked. You can also [quickemu](quickemu.md) with:
```
quickemu --display none
```
to not get any annoying GUI.

## ↑ Ancestors (12)

1. [quickemu HOWTO](quickemu-howto.md)
2. [quickemu](quickemu.md)
3. [Emulator manager](emulator-manager.md)
4. [Emulator](emulator.md)
5. [Virtualization](virtualization.md)
6. [Systems programming](systems-programming-split.md)
7. [Software](software-split.md)
8. [Computer](computer-split.md)
9. [Information technology](information-technology.md)
10. [Area of technology](area-of-technology.md)
11. [Technology](technology-split.md)
12. [Ciro Santilli's Homepage](split.md)
