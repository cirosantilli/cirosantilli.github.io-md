# Wireshark capture filter

↑ **Parent:** [Wireshark](wireshark.md)

Capture by instead:
```
sudo wireshark -f http -k
sudo wireshark -f icmp -k
```

Filter by both protocol and host:
```
sudo wireshark -f 'host 192.168.1.102 and icmp' -k
```

For [application layer](application-layer.md) capture filtering, the best you can do is by port:
```
sudo wireshark -f 'tcp port 80'
```
There is an `http` filter but only for as a [wireshark display filter](wireshark-display-filter.md)

## ↑ Ancestors (8)

1. [Wireshark](wireshark.md)
2. [Computer network software](computer-network-software.md)
3. [Computer network](computer-network.md)
4. [Computer](computer-split.md)
5. [Information technology](information-technology.md)
6. [Area of technology](area-of-technology.md)
7. [Technology](technology-split.md)
8. [Ciro Santilli's Homepage](split.md)
