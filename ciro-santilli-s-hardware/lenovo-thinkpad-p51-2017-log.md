# Lenovo ThinkPad P51 (2017) log

↑ **Parent:** [Lenovo ThinkPad P51 (2017)](lenovo-thinkpad-p51-2017.md)

<a id="_420"></a>
[https://cirosantilli.com/linux-kernel-module-cheat/#p51](https://cirosantilli.com/linux-kernel-module-cheat/#p51) ([permalink](https://raw.githubusercontent.com/cirosantilli/linux-kernel-module-cheat/a0d6fa15a207cb40cd8ce090c77aa9b55d7605a6/README.adoc))

<a id="_421"></a>
<a id="_422"></a>
- battery life:<a id="_423"></a>

  <a id="_424"></a>
  - 2023-04: on-browser streaming + light browsing on [Ubuntu 22.10](../ubuntu-22-10.md): about 2h45. Too low! Gotta try buying a new battery.
<a id="_425"></a>
- <a id="_426"></a>
  2022-01-04 updated firmward after noticing that [ubuntu 21.10 does not wake up from suspend](../ubuntu-21-10-does-not-wake-up-from-suspend.md) seemed to happen every time when not connected to external power. `dmidecode` diff excerpt:<a id="_427"></a>

  ```
   BIOS Information
          Vendor: LENOVO
  -       Version: N1UET40W (1.14 )
  -       Release Date: 09/28/2017
  +       Version: N1UET71W (1.45 )
  +       Release Date: 07/18/2018
  ```
  used the "Ubuntu Software" GUI as mentioned at: [https://support.lenovo.com/gb/en/solutions/ht510810-how-to-do-software-updates-linux](https://support.lenovo.com/gb/en/solutions/ht510810-how-to-do-software-updates-linux). Kudos for making this accessible to newbs.

  <a id="_428"></a>
  After doing that, another update became available to: 0.1.56, clicked it and was much faster than the previous one, and didn't auto reboot. After manual reboot, `dmidecode` diffed again:<a id="_429"></a>

  ```
   BIOS Information
          Vendor: LENOVO
  -       Version: N1UET71W (1.45 )
  -       Release Date: 07/18/2018
  +       Version: N1UET82W (1.56 )
  +       Release Date: 08/12/2021
  ```
  plus a bunch of other lines.
<a id="_430"></a>
- <a id="_431"></a>
  2021-06-05 upgraded to [Ubuntu](../ubuntu.md) 21.04 with a clean install from an ISO. Selected<a id="_432"></a>

  <a id="_433"></a>
  - "Minimal installation"
  <a id="_434"></a>
  - "Erase disk and install Ubuntu". Notably, this erased the [Microsoft Windows](../microsoft-windows.md) that came with the computer and was never used not even once
  <a id="_435"></a>
  - "Erase disk ans use ZFS"
  <a id="_436"></a>
  - Encrypt the new Ubuntu installation for security
  After this, the GUI felt fast, who would have thought that erasing a bunch of stuff would make the system faster!

  <a id="_437"></a>
  `lsblk` contains:<a id="_438"></a>

  ```
  zd0               230:0    0   500M  0 disk
  └─keystore-rpool  253:0    0   484M  0 crypt /run/keystore/rpool
  nvme0n1           259:0    0 476.9G  0 disk
  ├─nvme0n1p1       259:1    0   512M  0 part  /boot/efi
  ├─nvme0n1p2       259:2    0     2G  0 part
  │ └─cryptoswap    253:1    0     2G  0 crypt
  ├─nvme0n1p3       259:3    0     2G  0 part
  └─nvme0n1p4       259:4    0 472.4G  0 part
  ```
  and `lsblk -f`:<a id="_439"></a>

  ```
  zd0               crypto_LUKS 2
  └─keystore-rpool  ext4        1.0   keystore-rpool
  nvme0n1
  ├─nvme0n1p1       vfat        FAT32
  ├─nvme0n1p2       crypto_LUKS 2
  │ └─cryptoswap
  ├─nvme0n1p3       zfs_member  5000  bpool
  └─nvme0n1p4       zfs_member  5000  rpoo
  ```

  <a id="_440"></a>
  Then:<a id="_441"></a>

  ```
  grep '[rb]pool' /proc/mounts
  ```
  contains:<a id="_442"></a>

  ```
  rpool/ROOT/ubuntu_uvs1fq / zfs rw,relatime,xattr,posixacl 0 0
  rpool/USERDATA/ciro_czngbg /home/ciro zfs rw,relatime,xattr,posixacl 0 0
  rpool/USERDATA/root_czngbg /root zfs rw,relatime,xattr,posixacl 0 0
  rpool/ROOT/ubuntu_uvs1fq/srv /srv zfs rw,relatime,xattr,posixacl 0 0
  rpool/ROOT/ubuntu_uvs1fq/usr/local /usr/local zfs rw,relatime,xattr,posixacl 0 0
  rpool/ROOT/ubuntu_uvs1fq/var/games /var/games zfs rw,relatime,xattr,posixacl 0 0
  rpool/ROOT/ubuntu_uvs1fq/var/log /var/log zfs rw,relatime,xattr,posixacl 0 0
  rpool/ROOT/ubuntu_uvs1fq/var/lib /var/lib zfs rw,relatime,xattr,posixacl 0 0
  rpool/ROOT/ubuntu_uvs1fq/var/mail /var/mail zfs rw,relatime,xattr,posixacl 0 0
  rpool/ROOT/ubuntu_uvs1fq/var/snap /var/snap zfs rw,relatime,xattr,posixacl 0 0
  rpool/ROOT/ubuntu_uvs1fq/var/www /var/www zfs rw,relatime,xattr,posixacl 0 0
  rpool/ROOT/ubuntu_uvs1fq/var/spool /var/spool zfs rw,relatime,xattr,posixacl 0 0
  rpool/ROOT/ubuntu_uvs1fq/var/lib/AccountsService /var/lib/AccountsService zfs rw,relatime,xattr,posixacl 0 0
  rpool/ROOT/ubuntu_uvs1fq/var/lib/NetworkManager /var/lib/NetworkManager zfs rw,relatime,xattr,posixacl 0 0
  rpool/ROOT/ubuntu_uvs1fq/var/lib/apt /var/lib/apt zfs rw,relatime,xattr,posixacl 0 0
  rpool/ROOT/ubuntu_uvs1fq/var/lib/dpkg /var/lib/dpkg zfs rw,relatime,xattr,posixacl 0 0
  bpool/BOOT/ubuntu_uvs1fq /boot zfs rw,nodev,relatime,xattr,posixacl 0 0
  ```
  which gives an idea of how the above map to mountpoints.

  <a id="_443"></a>
  Had two GUI freezes since installation, a fixed images shows no matter what I do, possibly graphics only, but impossible to tell (next time I'll try SSH access). No [Nvidia](../nvidia.md) drivers installed yet.

<a id="_444"></a>
2020-06-06: dropped some lemon juice on the bottom left of touchpad. Bottom left button not working anymore... I'm an idiot. There are many other alternatives, but very aggravating, I'll replace it for sure. Can't find the exact replacement part or any videos showing its replacement online easliy, dang. For the T430: [https://www.youtube.com/watch?v=F3lzV9uXRjU](https://www.youtube.com/watch?v=F3lzV9uXRjU) Asked at: [https://forums.lenovo.com/t5/ThinkPad-P-and-W-Series-Mobile-Workstations/P51-left-bottom-button-below-trackpad-mouse-left-click-stopped-working-possible-to-replace/m-p/5019903](https://forums.lenovo.com/t5/ThinkPad-P-and-W-Series-Mobile-Workstations/P51-left-bottom-button-below-trackpad-mouse-left-click-stopped-working-possible-to-replace/m-p/5019903) Also I could not access it because you need to remove the HDD first: [https://www.youtube.com/watch?v=5Klawxc7T_Y](https://www.youtube.com/watch?v=5Klawxc7T_Y) and I can't pull it out even with considerable force, unlike in the video... And OMG, those button caps are impossible to re-install once removed!!! Then when I put the whole thing back together, the upper buttons were not working anymore. FUUUUUUUUCK. When first opening I pulled on it without properly removing the cap and it came off, but it didn't look broken in any way and I put it back in. Keyboard works thank God, so right black connector is fine, left white one oppears to be the one for upper keys and trackpoint, both of which stopped working. The hardware manual confirms that they are both part of the same device, so basically a mouse :-) TODO can it be bought separately from te keyboard? Doesn't look like it, photo of keyboard part includes those buttons. The manual also confirms that the bottom buttons are one device with the trackpad "trackpad with buttons", thus forming the second entire mouse.

<a id="_445"></a>
2019-04-17: popup asking about "ThinkPad P51 Management Engine Update" from from 182.29.3287 to 184.60.3561, said yes.

<a id="_446"></a>
[Ubuntu](../ubuntu.md) 17.10 setup after buying it:

<a id="_447"></a>
<a id="_448"></a>
- partition setup: [https://askubuntu.com/questions/343268/how-to-use-manual-partitioning-during-installation/976430#976430](https://askubuntu.com/questions/343268/how-to-use-manual-partitioning-during-installation/976430#976430)
<a id="_449"></a>
- BIOS:<a id="_450"></a>

  <a id="_451"></a>
  - for NVIDIA driver:
  <a id="_452"></a>
  - for KVM, required by Android Emulator: enable virtualization extensions
<a id="_453"></a>
- TODO fix the brightness keys:<a id="_454"></a>

  <a id="_455"></a>
  - failed: [https://askubuntu.com/questions/769006/brightness-key-not-working-ubuntu-16-04-lts/770100#770100](https://askubuntu.com/questions/769006/brightness-key-not-working-ubuntu-16-04-lts/770100#770100)

<a id="_456"></a>
Battery life shown by Ubuntu battery app after installation:

<a id="_457"></a>
<a id="_458"></a>
- before NVIDIA driver setup: 8h
<a id="_459"></a>
- after: 6.5h

## ↑ Ancestors (6)

1. [Lenovo ThinkPad P51 (2017)](lenovo-thinkpad-p51-2017.md)
2. [Laptop](laptop.md)
3. [Computers](computers.md)
4. [Ciro Santilli's hardware](../ciro-santilli-s-hardware-split.md)
5. [Ciro Santilli](../ciro-santilli-split.md)
6. [Ciro Santilli's Homepage](../split.md)
