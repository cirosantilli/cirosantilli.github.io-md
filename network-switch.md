# Network switch

↑ **Parent:** [Networking hardware](networking-hardware.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Network_switch)

A switch is a box with a bunch of [Ethernet](ethernet.md) wires coming into it:
```
+--------------------+
| +-+  +-+  +-+  +-+ |
| |1|  |2|  |3|  |4| |
| +-+  +-+  +-+  +-+ |
+--------------------+
```
Except that it doesn't have to be [Ethernet](ethernet.md), e.g. it would also be a [Wi-Fi](wi-fi.md).

What the switch does is:
- an [Ethernet](ethernet.md) request came in from wire 1
- decide which wire to send it out on, e.g. wire 2, 3, 4, 5, etc. You likely don't want to send it back through 1 where it came from.
After the destination is found, a confirmation is somehow sent back to the switch, which then learns which wire to send each [MAC address](mac-address.md) to.

A switch is a bit like a [router](router-computing.md) but it is a bit dumber/operates at a lower level: it basically operates only on [MAC addresses](mac-address.md), not on [IP addresses](ip-address.md).

The [Internet service provider](internet-service-provider.md) boxes most people have at home combines a switch for the local network and a [router](router-computing.md) for the ISP communication.

## ↑ Ancestors (7)

1. [Networking hardware](networking-hardware.md)
2. [Computer network](computer-network.md)
3. [Computer](computer-split.md)
4. [Information technology](information-technology.md)
5. [Area of technology](area-of-technology.md)
6. [Technology](technology-split.md)
7. [Ciro Santilli's Homepage](split.md)
