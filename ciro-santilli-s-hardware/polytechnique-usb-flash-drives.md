# Polytechnique USB flash drives

↑ **Parent:** [USB flash drives](usb-flash-drives.md)

<a id="_566"></a>
~8GB, `lsblk` reports 7796176 \* 1KB = 7983284224 bytes.

<a id="_567"></a>
We got a handful of those from [École Polytechnique](../ecole-polytechnique-split.md) at the end of studies I think.

<a id="_568"></a>
They are shaped like [bicornes](https://en.wikipedia.org/wiki/Bicorne), which is super cool, but also super impractical!

<a id="_569"></a>
Markings: "AX ÉCOLE POLYTECHNIQUE PROMOTION X2009"

<a id="_570"></a>
20.04 `gnome-disks` program reports it as: "SMI USB DISK".

<a id="_571"></a>
From [Ubuntu](../ubuntu.md) 20.04 on an ext4 formatted one:<a id="_572"></a>

```
/dev/sdb:
 Timing cached reads:   28656 MB in  1.99 seconds = 14421.31 MB/sec
SG_IO: bad/missing sense data, sb[]:  70 00 05 00 00 00 00 0a 00 00 00 00 20 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
 Timing buffered disk reads:  42 MB in  3.03 seconds =  13.88 MB/sec
```
With [Linux Unified Key Setup](../linux-unified-key-setup.md) + ext4 the results are similar, maybe hdparam bypasses it?<a id="_573"></a>

```
/dev/sdb:
 Timing cached reads:   28326 MB in  1.99 seconds = 14251.55 MB/sec
SG_IO: bad/missing sense data, sb[]:  70 00 05 00 00 00 00 0a 00 00 00 00 20 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
 Timing buffered disk reads:  38 MB in  3.11 seconds =  12.23 MB/sec
```
`gnome-disks` LUKS + ext4 benchmark with default params also gives about 14 MB/s.

## ↑ Ancestors (7)

1. [USB flash drives](usb-flash-drives.md)
2. [External storage](external-storage.md)
3. [Computer accessories](computer-accessories.md)
4. [Computers](computers.md)
5. [Ciro Santilli's hardware](../ciro-santilli-s-hardware-split.md)
6. [Ciro Santilli](../ciro-santilli-split.md)
7. [Ciro Santilli's Homepage](../split.md)
