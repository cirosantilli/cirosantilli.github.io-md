# Universal asynchronous receiver-transmitter

↑ **Parent:** [Physical layer](physical-layer.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Universal_asynchronous_receiver-transmitter)

A good project to see UARTs at work in all their beauty is to connect two [Raspberry Pis](raspberry-pi.md) via UART, and then:
- type in one and see characters appear in the other: [https://scribles.net/setting-up-uart-serial-communication-between-raspberry-pis/](https://scribles.net/setting-up-uart-serial-communication-between-raspberry-pis/)
- send data via a script: [https://raspberrypi.stackexchange.com/questions/29027/how-should-i-properly-communicate-2-raspberry-pi-via-uart](https://raspberrypi.stackexchange.com/questions/29027/how-should-i-properly-communicate-2-raspberry-pi-via-uart)

Part of the beauty of this is that you can just connect both boards directly manually with a few wire-to-wire connections with simple [jump wire](jump-wire.md). Its simplicity is just quite refreshing. Sure, you could do something like that for any physical layer link presumably...

Remember that you can only have one [GNU screen](gnu-screen.md) connected at a time or else they will mess each other up: [https://unix.stackexchange.com/questions/93892/why-is-screen-is-terminating-without-root/367549#367549](https://unix.stackexchange.com/questions/93892/why-is-screen-is-terminating-without-root/367549#367549)

On [Ubuntu 22.04](ubuntu-22-04.md) you can screen without [sudo](sudo.md) by adding yourself to the `dialout` group with:
```
sudo usermod -a -G dialout $USER
```

## ↑ Ancestors (8)

1. [Physical layer](physical-layer.md)
2. [OSI model](osi-model.md)
3. [Computer network](computer-network.md)
4. [Computer](computer-split.md)
5. [Information technology](information-technology.md)
6. [Area of technology](area-of-technology.md)
7. [Technology](technology-split.md)
8. [Ciro Santilli's Homepage](split.md)
