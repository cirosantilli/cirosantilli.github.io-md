# Lenovo ThinkPad P14s gen4 amd

↑ **Parent:** [Laptop](laptop.md)

<a id="_283"></a>
Bought: November 2023 during Black Friday sale for £1,323.00 to be [Ciro Santilli](../ciro-santilli-split.md)'s main personal laptop.

<a id="_284"></a>
Six years after, and we are 2x on every key spec (except processor Hz ;-) at about 1/2 the price and 1/2 the weight (though smaller 14" screen for greater portability), so not bad! Customized to max out each hardware spec:

<a id="_285"></a>
Specs:<a id="_286"></a>

<a id="_287"></a>
- Processor: [AMD Ryzen 7 PRO 7840U](../amd-7840u.md) Processor (3.30 GHz up to 5.10 GHz)<a id="_288"></a>

  <a id="_289"></a>
  - <a id="_290"></a>
    Graphic Card: Integrated Graphics

    <a id="_291"></a>
    The [Ubuntu 23.10](../ubuntu-23-10.md) "About system GUI describes its graphics as: Radeon 780M Graphics × 16, which e.g. [https://www.techpowerup.com/gpu-specs/radeon-780m.c4020](https://www.techpowerup.com/gpu-specs/radeon-780m.c4020) documents as running the [RDNA 3](../rdna-3.md) [microarchitecture](../microarchitecture.md).
<a id="_292"></a>
- Operating System: No Operating System selected upgrade
<a id="_293"></a>
- Operating System Language: No Operating System Language selected upgrade
<a id="_294"></a>
- Microsoft Productivity Software: None
<a id="_295"></a>
- Memory: 64 GB LPDDR5X-6400MHz (Soldered)selected upgrade. Specs at: [https://www.lenovo.com/gb/en/p/accessories-and-software/memory-and-storage/memory-and-storage-hard-drives/4xb1d04758](https://www.lenovo.com/gb/en/p/accessories-and-software/memory-and-storage/memory-and-storage-hard-drives/4xb1d04758) quotes "64 Gbps", i.e. 8 GB/s. `dd count=1M if=/dev/zero of=tmp` gives only 255 MB/s however.
<a id="_296"></a>
- Solid State Drive: 2 TB SSD M.2 2280 PCIe Gen4 Performance TLC Opalselected upgrade
<a id="_297"></a>
- Display: 14" WUXGA (1920 x 1200), IPS, Anti-Glare, Touch, 45%NTSC, 300 nits, 60Hz
<a id="_298"></a>
- Camera: 1080P FHD RGB/IR Hybrid with Microphone
<a id="_299"></a>
- Color: Thunder Black
<a id="_300"></a>
- Factory Color Calibration: No Factory Color Calibration
<a id="_301"></a>
- Wireless: Qualcomm Wi-Fi 6E NFA725A 2x2 AX & Bluetooth® 5.1 or above
<a id="_302"></a>
- Integrated Mobile Broadband: No Wireless WAN
<a id="_303"></a>
- Ethernet: Wired Ethernet
<a id="_304"></a>
- Near Field Communication: No NFC
<a id="_305"></a>
- Fingerprint Reader: Fingerprint Reader
<a id="_306"></a>
- Keyboard: Black - English (EU)selected upgrade
<a id="_307"></a>
- Battery: 4 Cell Li-Polymer 52.5Whselected upgrade
<a id="_308"></a>
- Power Cord: 65W USB-C Slim 90% PCC 3pin AC Adapter - UKselected upgrade
<a id="_309"></a>
- Electronic Privacy Filter: No ePrivacy Filter
<a id="_310"></a>
- Adobe Elements: None
<a id="_311"></a>
- Adobe Acrobat: None
<a id="_312"></a>
- Adobe Creative Cloud: None
<a id="_313"></a>
- Security Software: None
<a id="_314"></a>
- Cloud Security Software: No Cloud Security Software
<a id="_315"></a>
- Warranty: 3 Year Courier or Carry-in

<a id="_316"></a>
Identifiers:<a id="_317"></a>

<a id="_318"></a>
- [Ethernet](../ethernet.md) [MAC address](../mac-address.md): fc:5c:ee:24:fb:b4
<a id="_319"></a>
- [Wi-Fi](../wi-fi.md) [MAC address](../mac-address.md): 04:7b:cb:cc:1b:10

<a id="_320"></a>
Upon arrival:<a id="_321"></a>

<a id="_322"></a>
- Weight: 1490 g
<a id="_323"></a>
- Charger weight: 323 g
<a id="_324"></a>
- Firmware according to `sudo dmidecode -t bios`:<a id="_325"></a>

  ```
  Vendor: LENOVO
  Version: R2FET33W (1.13 )
  Release Date: 09/08/2023
  ```

<a id="_326"></a>
Buy research:<a id="_327"></a>

<a id="_328"></a>
- [https://www.phoronix.com/review/thinkpad-p14s-gen4](https://www.phoronix.com/review/thinkpad-p14s-gen4) says Ubuntu running fine
<a id="_329"></a>
- Intel vs amd: the Intel ones could come with a discrete rtx A500 GPU. GPU likely makes laptop heavier and less power efficient. And both have basically the same benchmark which is crazy:<a id="_330"></a>

  <a id="_331"></a>
  - [https://www.videocardbenchmark.net/gpu.php?gpu=RTX+A500+Laptop+GPU&id=4649](https://www.videocardbenchmark.net/gpu.php?gpu=RTX+A500+Laptop+GPU&id=4649)
  <a id="_332"></a>
  - [https://www.videocardbenchmark.net/gpu.php?gpu=Radeon+780M&id=4818](https://www.videocardbenchmark.net/gpu.php?gpu=Radeon+780M&id=4818)

  So the only downside is not being able to run CUDA.
<a id="_333"></a>
- thought about Yoga or other Ultrabook options, but 2x price at same specs, so nah...

<a id="_334"></a>
Log:

<a id="_335"></a>
2024-01-17: firmware update:<a id="_336"></a>

```
Vendor: LENOVO
Version: R2FET36W (1.16 )
Release Date: 10/24/2023
```
Actually fixed performance mode: [https://askubuntu.com/questions/604720/setting-to-high-performance/1343879#1343879](https://askubuntu.com/questions/604720/setting-to-high-performance/1343879#1343879)

**Table of contents**

- [P14s cannot dual monitor on Wayland](p14s-cannot-dual-monitor-on-wayland.md)
- [P14s benchmark](p14s-benchmark.md)

## ↑ Ancestors (5)

1. [Laptop](laptop.md)
2. [Computers](computers.md)
3. [Ciro Santilli's hardware](../ciro-santilli-s-hardware-split.md)
4. [Ciro Santilli](../ciro-santilli-split.md)
5. [Ciro Santilli's Homepage](../split.md)

## ← Incoming links (2)

- [Backpacks](backpacks.md)
- [Internet speed](internet-speed.md)
