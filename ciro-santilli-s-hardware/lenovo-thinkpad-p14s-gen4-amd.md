# Lenovo ThinkPad P14s gen4 amd

↑ **Parent:** [Laptop](laptop.md)

Bought: November 2023 during Black Friday sale for £1,323.00 to be [Ciro Santilli](../ciro-santilli-split.md)'s main personal laptop.

Six years after, and we are 2x on every key spec (except processor Hz ;-) at about 1/2 the price and 1/2 the weight (though smaller 14" screen for greater portability), so not bad! Customized to max out each hardware spec:

Specs:
- Processor: [AMD Ryzen 7 PRO 7840U](../amd-7840u.md) Processor (3.30 GHz up to 5.10 GHz)
  - Graphic Card: Integrated Graphics

    The [Ubuntu 23.10](../ubuntu-23-10.md) "About system GUI describes its graphics as: Radeon 780M Graphics × 16, which e.g. [https://www.techpowerup.com/gpu-specs/radeon-780m.c4020](https://www.techpowerup.com/gpu-specs/radeon-780m.c4020) documents as running the [RDNA 3](../rdna-3.md) [microarchitecture](../microarchitecture.md).
- Operating System: No Operating System selected upgrade
- Operating System Language: No Operating System Language selected upgrade
- Microsoft Productivity Software: None
- Memory: 64 GB LPDDR5X-6400MHz (Soldered)selected upgrade. Specs at: [https://www.lenovo.com/gb/en/p/accessories-and-software/memory-and-storage/memory-and-storage-hard-drives/4xb1d04758](https://www.lenovo.com/gb/en/p/accessories-and-software/memory-and-storage/memory-and-storage-hard-drives/4xb1d04758) quotes "64 Gbps", i.e. 8 GB/s. `dd count=1M if=/dev/zero of=tmp` gives only 255 MB/s however.
- Solid State Drive: 2 TB SSD M.2 2280 PCIe Gen4 Performance TLC Opalselected upgrade
- Display: 14" WUXGA (1920 x 1200), IPS, Anti-Glare, Touch, 45%NTSC, 300 nits, 60Hz
- Camera: 1080P FHD RGB/IR Hybrid with Microphone
- Color: Thunder Black
- Factory Color Calibration: No Factory Color Calibration
- Wireless: Qualcomm Wi-Fi 6E NFA725A 2x2 AX & Bluetooth® 5.1 or above
- Integrated Mobile Broadband: No Wireless WAN
- Ethernet: Wired Ethernet
- Near Field Communication: No NFC
- Fingerprint Reader: Fingerprint Reader
- Keyboard: Black - English (EU)selected upgrade
- Battery: 4 Cell Li-Polymer 52.5Whselected upgrade
- Power Cord: 65W USB-C Slim 90% PCC 3pin AC Adapter - UKselected upgrade
- Electronic Privacy Filter: No ePrivacy Filter
- Adobe Elements: None
- Adobe Acrobat: None
- Adobe Creative Cloud: None
- Security Software: None
- Cloud Security Software: No Cloud Security Software
- Warranty: 3 Year Courier or Carry-in

Identifiers:
- [Ethernet](../ethernet.md) [MAC address](../mac-address.md): fc:5c:ee:24:fb:b4
- [Wi-Fi](../wi-fi.md) [MAC address](../mac-address.md): 04:7b:cb:cc:1b:10

Upon arrival:
- Weight: 1490 g
- Charger weight: 323 g
- Firmware according to `sudo dmidecode -t bios`:
  ```
  Vendor: LENOVO
  Version: R2FET33W (1.13 )
  Release Date: 09/08/2023
  ```

Buy research:
- [https://www.phoronix.com/review/thinkpad-p14s-gen4](https://www.phoronix.com/review/thinkpad-p14s-gen4) says Ubuntu running fine
- Intel vs amd: the Intel ones could come with a discrete rtx A500 GPU. GPU likely makes laptop heavier and less power efficient. And both have basically the same benchmark which is crazy:
  - [https://www.videocardbenchmark.net/gpu.php?gpu=RTX+A500+Laptop+GPU&id=4649](https://www.videocardbenchmark.net/gpu.php?gpu=RTX+A500+Laptop+GPU&id=4649)
  - [https://www.videocardbenchmark.net/gpu.php?gpu=Radeon+780M&id=4818](https://www.videocardbenchmark.net/gpu.php?gpu=Radeon+780M&id=4818)

  So the only downside is not being able to run CUDA.
- thought about Yoga or other Ultrabook options, but 2x price at same specs, so nah...

Log:

2024-01-17: firmware update:
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
