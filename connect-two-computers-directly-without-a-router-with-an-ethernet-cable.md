# Connect two computers directly without a router with an Ethernet cable

↑ **Parent:** [Linux networking HOWTO](linux-networking-howto.md)

For [IP](internet-protocol.md)-level communication, [https://askubuntu.com/questions/22835/how-to-network-two-ubuntu-computers-using-ethernet-without-a-router/116680#116680](https://askubuntu.com/questions/22835/how-to-network-two-ubuntu-computers-using-ethernet-without-a-router/116680#116680) just worked between [P51](ciro-santilli-s-hardware/lenovo-thinkpad-p51-2017.md) and [P14s](ciro-santilli-s-hardware/lenovo-thinkpad-p14s-gen4-amd.md) both on [Ubuntu 23.10](ubuntu-23-10.md) connected with a regular [Cat 5e](cat-5e.md) cable.

On both machines, first we found the [Ethernet cable](ethernet-cable.md) interface name with the [`ip` CLI tool](ip-cli-tool.md):
```
ip a
```
which outputs on the P41s:
```
1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN group default qlen 1000
    link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
    inet 127.0.0.1/8 scope host lo
       valid_lft forever preferred_lft forever
    inet6 ::1/128 scope host
       valid_lft forever preferred_lft forever
2: enp1s0f0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc pfifo_fast state UP group default qlen 1000
    link/ether fc:5c:ee:24:fb:b4 brd ff:ff:ff:ff:ff:ff
3: wlp2s0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc noqueue state UP group default qlen 1000
    link/ether 04:7b:cb:cc:1b:10 brd ff:ff:ff:ff:ff:ff
    inet 192.168.1.123/24 brd 192.168.1.255 scope global dynamic noprefixroute wlp2s0
       valid_lft 61284sec preferred_lft 61284sec
    inet6 fe80::3597:15d8:74ff:e112/64 scope link noprefixroute
       valid_lft forever preferred_lft forever
```
so the interface was `enp1s0f0`, because `wlp` is wireless and `lo` is localhost.

So on the P14s we assign an IP of 10.0.0.10 to the P51:
```
sudo ip address add 10.0.0.10/24 dev enp1s0f0
```

Then on the P51 analogously, giving IP of 10.0.0.20 to the P14s:
```
sudo ip address add 10.0.0.20/24 dev enp0s31f6
```

And after that, P14s can:
```
ping 10.0.0.10
```
and P51 can:
```
ping 10.0.0.20
```

TODO after a few seconds, the settings appear to be forgotten, and `ping` stops working unless you do `sudo ip address add` on the local machine again. This seems to happen after a popup appears saying "Activation of network connection failed" as it fails to obtain Internet from the cable.

TODO list and delete such manual assignments we've made.

**Table of contents**

- [Find MAC address of a device on the other end of an Ethernet cable](find-mac-address-of-a-device-on-the-other-end-of-an-ethernet-cable.md)
  - [Find MAC address of a device on the other end of an Ethernet cable without IP](find-mac-address-of-a-device-on-the-other-end-of-an-ethernet-cable-without-ip.md)

## ↑ Ancestors (7)

1. [Linux networking HOWTO](linux-networking-howto.md)
2. [Computer network](computer-network.md)
3. [Computer](computer-split.md)
4. [Information technology](information-technology.md)
5. [Area of technology](area-of-technology.md)
6. [Technology](technology-split.md)
7. [Ciro Santilli's Homepage](split.md)
