# P51 hardware

↑ **Parent:** [Lenovo ThinkPad P51 (2017)](lenovo-thinkpad-p51-2017.md)

<a id="_400"></a>
<a id="_401"></a>

```
lspci
```
output:<a id="_402"></a>

```
00:00.0 Host bridge: Intel Corporation Xeon E3-1200 v6/7th Gen Core Processor Host Bridge/DRAM Registers (rev 05)
00:01.0 PCI bridge: Intel Corporation 6th-10th Gen Core Processor PCIe Controller (x16) (rev 05)
00:08.0 System peripheral: Intel Corporation Xeon E3-1200 v5/v6 / E3-1500 v5 / 6th/7th/8th Gen Core Processor Gaussian Mixture Model
00:14.0 USB controller: Intel Corporation 100 Series/C230 Series Chipset Family USB 3.0 xHCI Controller (rev 31)
00:14.2 Signal processing controller: Intel Corporation 100 Series/C230 Series Chipset Family Thermal Subsystem (rev 31)
00:15.0 Signal processing controller: Intel Corporation 100 Series/C230 Series Chipset Family Serial IO I2C Controller #0 (rev 31)
00:16.0 Communication controller: Intel Corporation 100 Series/C230 Series Chipset Family MEI Controller #1 (rev 31)
00:17.0 SATA controller: Intel Corporation Q170/Q150/B150/H170/H110/Z170/CM236 Chipset SATA Controller [AHCI Mode] (rev 31)
00:1c.0 PCI bridge: Intel Corporation 100 Series/C230 Series Chipset Family PCI Express Root Port #1 (rev f1)
00:1c.2 PCI bridge: Intel Corporation 100 Series/C230 Series Chipset Family PCI Express Root Port #3 (rev f1)
00:1c.4 PCI bridge: Intel Corporation 100 Series/C230 Series Chipset Family PCI Express Root Port #5 (rev f1)
00:1d.0 PCI bridge: Intel Corporation 100 Series/C230 Series Chipset Family PCI Express Root Port #9 (rev f1)
00:1d.4 PCI bridge: Intel Corporation 100 Series/C230 Series Chipset Family PCI Express Root Port #13 (rev f1)
00:1f.0 ISA bridge: Intel Corporation CM238 Chipset LPC/eSPI Controller (rev 31)
00:1f.2 Memory controller: Intel Corporation 100 Series/C230 Series Chipset Family Power Management Controller (rev 31)
00:1f.3 Audio device: Intel Corporation CM238 HD Audio Controller (rev 31)
00:1f.4 SMBus: Intel Corporation 100 Series/C230 Series Chipset Family SMBus (rev 31)
00:1f.6 Ethernet controller: Intel Corporation Ethernet Connection (5) I219-LM (rev 31)
01:00.0 VGA compatible controller: NVIDIA Corporation GM107GLM [Quadro M1200 Mobile] (rev a2)
01:00.1 Audio device: NVIDIA Corporation GM107 High Definition Audio Controller [GeForce 940MX] (rev a1)
04:00.0 Network controller: Intel Corporation Wireless 8265 / 8275 (rev 78)
3e:00.0 Non-Volatile memory controller: Samsung Electronics Co Ltd NVMe SSD Controller SM981/PM981/PM983
3f:00.0 Unassigned class [ff00]: Realtek Semiconductor Co., Ltd. RTS525A PCI Express Card Reader (rev 01)
```

<a id="_403"></a>
<a id="_404"></a>

```
lspci -t
```
output:<a id="_405"></a>

```
-[0000:00]-+-00.0
           +-00.2
           +-01.0
           +-02.0
           +-02.1-[01]----00.0
           +-02.2-[02]----00.0
           +-02.4-[03]----00.0
           +-03.0
           +-04.0
           +-04.1-[04-63]--
           +-08.0
           +-08.1-[64]--+-00.0
           |            +-00.1
           |            +-00.2
           |            +-00.3
           |            +-00.4
           |            +-00.5
           |            \-00.6
           +-08.2-[65]--+-00.0
           |            \-00.1
           +-08.3-[66]--+-00.0
           |            +-00.3
           |            +-00.4
           |            \-00.6
           +-14.0
           +-14.3
           +-18.0
           +-18.1
           +-18.2
           +-18.3
           +-18.4
           +-18.5
           +-18.6
           \-18.7
```

**Table of contents**

- [Samsung MZVLB512HAJQ-000L7 512GB SSD](samsung-mzvlb512hajq-000l7-512gb-ssd.md)
- [Seagate ST1000LM035-1RK1 1TB hard disk](seagate-st1000lm035-1rk1-1tb-hard-disk.md)

## ↑ Ancestors (6)

1. [Lenovo ThinkPad P51 (2017)](lenovo-thinkpad-p51-2017.md)
2. [Laptop](laptop.md)
3. [Computers](computers.md)
4. [Ciro Santilli's hardware](../ciro-santilli-s-hardware-split.md)
5. [Ciro Santilli](../ciro-santilli-split.md)
6. [Ciro Santilli's Homepage](../split.md)
