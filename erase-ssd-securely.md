# Erase SSD securely

↑ **Parent:** [Solid-state storage](solid-state-storage.md)

You can't just [shred](shred-unix.md) individual [sSD](solid-state-storage.md) files because SSD writes only at large granularities, so hardware/drivers have to copy stuff around all the time to compact it. This means that leftover copies are left around everywhere.

What you can do however is to erase the entire thing with vendor support, which most hardware has support for. On hardware encrypted disks, you can even just erase the keys:
- ATA: [https://www.thomas-krenn.com/en/wiki/Perform_a_SSD_Secure_Erase](https://www.thomas-krenn.com/en/wiki/Perform_a_SSD_Secure_Erase) for ATA.
- NVMe: [http://forum.notebookreview.com/threads/secure-erase-hdds-ssds-sata-nvme-using-hdparm-nvme-cli-on-linux.827525/](http://forum.notebookreview.com/threads/secure-erase-hdds-ssds-sata-nvme-using-hdparm-nvme-cli-on-linux.827525/)

TODO does shredding the

## ↑ Ancestors (12)

1. [Solid-state storage](solid-state-storage.md)
2. [Non-volatile memory](non-volatile-memory.md)
3. [Computer data storage hardware](computer-data-storage-hardware.md)
4. [Computer data storage](computer-data-storage.md)
5. [I/O device](i-o-device.md)
6. [Computer hardware component type](computer-hardware-component-type.md)
7. [Computer hardware](computer-hardware-split.md)
8. [Computer](computer-split.md)
9. [Information technology](information-technology.md)
10. [Area of technology](area-of-technology.md)
11. [Technology](technology-split.md)
12. [Ciro Santilli's Homepage](split.md)
