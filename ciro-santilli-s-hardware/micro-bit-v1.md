# Micro Bit v1

↑ **Parent:** [Microcontroller](microcontroller.md)

<a id="_494"></a>
General information: [Micro Bit v1](../micro-bit-v1.md)

<a id="_495"></a>
The file:<a id="_496"></a>

```
/media/$USER/MICROBIT/DETAILS.TXT
```
contains:<a id="_497"></a>

```
DAPLink Firmware - see https://mbed.com/daplink
Version: 0234
Build:   Oct 12 2015 14:53:22
```

<a id="_498"></a>
2022-10-14: stopped being able to connect to Ubuntu 22.04. Was trying to do a UART video demo, connected USB, disconnected, connected, disconnected several times on different filming attempts. Was working some of the time, Ubuntu did recognize it, I even saw UART output for sure, but was a bit unstable. But then at one point it just stopped getting recognized by Ubuntu 100% of the time. The board is still being powered by USB, and the previously flashed program still runs, but nothing showed on `sudo dmesg -w` at all, and I can't reprogram it!

<a id="_499"></a>
A day later, managed to get tit to connect once more with a different cable, but just once!<a id="_500"></a>

```
[15310.385055] usb 1-5: new full-speed USB device number 38 using xhci_hcd
[15310.534996] usb 1-5: New USB device found, idVendor=0d28, idProduct=0204, bcdDevice=10.00
[15310.535000] usb 1-5: New USB device strings: Mfr=1, Product=2, SerialNumber=3
[15310.535001] usb 1-5: Product: MBED CMSIS-DAP
[15310.535002] usb 1-5: Manufacturer: MBED
[15310.535003] usb 1-5: SerialNumber: 9900023436424e45001d30150000005d00000000cb8928bd
[15310.541267] usb-storage 1-5:1.0: USB Mass Storage device detected
[15310.541643] scsi host4: usb-storage 1-5:1.0
[15310.542658] hid-generic 0003:0D28:0204.000A: hiddev1,hidraw2: USB HID v1.00 Device [MBED MBED CMSIS-DAP] on usb-0000:00:14.0-5/input3
[15310.543121] cdc_acm 1-5:1.1: ttyACM0: USB ACM device
[15311.549969] scsi 4:0:0:0: Direct-Access     MBED     DAPLINK VFS      0.1  PQ: 0 ANSI: 2
[15311.550273] scsi 4:0:0:0: Attached scsi generic sg1 type 0
[15311.550825] sd 4:0:0:0: [sdb] 16512 512-byte logical blocks: (8.45 MB/8.06 MiB)
[15311.551052] sd 4:0:0:0: [sdb] Write Protect is off
[15311.551054] sd 4:0:0:0: [sdb] Mode Sense: 03 00 00 00
[15311.551204] sd 4:0:0:0: [sdb] No Caching mode page found
[15311.551207] sd 4:0:0:0: [sdb] Assuming drive cache: write through
[15311.572160] sd 4:0:0:0: [sdb] Attached SCSI removable disk
[15316.317438] usb 1-5: reset full-speed USB device number 38 using xhci_hcd
[15316.445093] usb 1-5: device descriptor read/64, error -71
[15316.681102] usb 1-5: device descriptor read/64, error -71
[15316.917102] usb 1-5: reset full-speed USB device number 38 using xhci_hcd
[15317.045028] usb 1-5: device descriptor read/64, error -71
[15317.281149] usb 1-5: device descriptor read/64, error -71
[15317.517154] usb 1-5: reset full-speed USB device number 38 using xhci_hcd
[15317.517466] usb 1-5: Device not responding to setup address.
[15317.725358] usb 1-5: Device not responding to setup address.
[15317.933042] usb 1-5: device not accepting address 38, error -71
[15318.061027] usb 1-5: reset full-speed USB device number 38 using xhci_hcd
[15318.061347] usb 1-5: Device not responding to setup address.
[15318.269270] usb 1-5: Device not responding to setup address.
[15318.477018] usb 1-5: device not accepting address 38, error -71
[15318.477153] usb 1-5: USB disconnect, device number 38
[15318.652912] usb 1-5: new full-speed USB device number 39 using xhci_hcd
[15318.785044] usb 1-5: device descriptor read/64, error -71
[15319.021068] usb 1-5: device descriptor read/64, error -71
[15319.257030] usb 1-5: new full-speed USB device number 40 using xhci_hcd
[15319.385075] usb 1-5: device descriptor read/64, error -71
[15319.621147] usb 1-5: device descriptor read/64, error -71
[15319.729170] usb usb1-port5: attempt power cycle
[15320.384941] usb 1-5: new full-speed USB device number 41 using xhci_hcd
[15320.385176] usb 1-5: Device not responding to setup address.
[15320.593188] usb 1-5: Device not responding to setup address.
[15320.801023] usb 1-5: device not accepting address 41, error -71
[15320.928909] usb 1-5: new full-speed USB device number 42 using xhci_hcd
[15320.929073] usb 1-5: Device not responding to setup address.
[15321.137244] usb 1-5: Device not responding to setup address.
[15321.344947] usb 1-5: device not accepting address 42, error -71
[15321.345173] usb usb1-port5: unable to enumerate USB device
[15321.384929] FAT-fs (sdb): unable to read boot sector to mark fs as dirty
```

<a id="_501"></a>
Some threads:<a id="_502"></a>

<a id="_503"></a>
- [https://askubuntu.com/questions/1317548/webusb-doesnt-work-connecting-to-microbit](https://askubuntu.com/questions/1317548/webusb-doesnt-work-connecting-to-microbit) after system upgrade, Ubuntu sees it but fails
<a id="_504"></a>
- [https://askubuntu.com/questions/1288738/cannot-pair-microbit-through-usb-on-xubuntu-16](https://askubuntu.com/questions/1288738/cannot-pair-microbit-through-usb-on-xubuntu-16)

<a id="_505"></a>
Exact same USB and port could still mount the [Raspberry Pi Pico](../raspberry-pi-pico.md).

## ↑ Ancestors (5)

1. [Microcontroller](microcontroller.md)
2. [Computers](computers.md)
3. [Ciro Santilli's hardware](../ciro-santilli-s-hardware-split.md)
4. [Ciro Santilli](../ciro-santilli-split.md)
5. [Ciro Santilli's Homepage](../split.md)

## ← Incoming links (2)

- [Micro Bit v1](micro-bit-v1.md)
- [Micro Bit](../micro-bit.md)
