# Dell Inspiron 15 3520

↑ **Parent:** [Laptop](laptop.md)

Bought May 2024 to be my clean crypto-only computer. Searched for cheapest 1 TB disk 16 GB RAM not too old on Amazon with Ubuntu certification, and that was it at £479.00.
- [https://www.dell.com/en-uk/shop/laptops-2-in-1-pcs/inspiron-15-laptop/spd/inspiron-15-3520-laptop/cn32043sc](https://www.dell.com/en-uk/shop/laptops-2-in-1-pcs/inspiron-15-laptop/spd/inspiron-15-3520-laptop/cn32043sc)
- Core™ i5-1235U [https://www.intel.com/content/www/us/en/products/sku/226266/intel-core-i51235u-processor-12m-cache-up-to-4-40-ghz-with-ipu/specifications.html](https://www.intel.com/content/www/us/en/products/sku/226266/intel-core-i51235u-processor-12m-cache-up-to-4-40-ghz-with-ipu/specifications.html) Q1'22

Some reviews:
- the keyboard is kind of crap. Notably the key "a" is very hard to press!!
- the lack of a sleep state indication LED and "I'm powering on LED" compared to Lenovo is really sad
- it gets way too hot doing work (Monero bootstrap) with lid closed, likely brought system down

[OPSEC](../operations-security.md): will run only cryptocurrency wallets and nothing else. Will connect to Internet, but never ever to a non clean USB flash drive.

The [OPSEC](../operations-security.md) for this machine supposes:
- no supply of chain attack on USB hardware, Laptop hardware, pre-installed Windows and Ubuntu ISO
- connecting with browser to a few well known websites to download stuff (Ubuntu ISO, Monero software) is safe

Bootstrap [OPSEC](../operations-security.md):
- turn on from factory, start Windows 11 Home 23H2 build 22631.2715, connect to home Wifi during setup process. Considered skipping WiFi, but I'll want to download the Ubuntu ISO later on anyways [https://answers.microsoft.com/en-us/windows/forum/all/bypass-lets-connect-you-to-a-network/2ce188f6-1b28-45a0-97d2-bfccfa3c9188](https://answers.microsoft.com/en-us/windows/forum/all/bypass-lets-connect-you-to-a-network/2ce188f6-1b28-45a0-97d2-bfccfa3c9188). Don't sign in to online Windows account, and turn off all spyware requests.
- on preinstalled Edge browser, download [Ubuntu 24.04](../ubuntu-24-04.md) ISO from [https://ubuntu.com](https://ubuntu.com), check sha256 with `Get-FileHash` on powershell even though that is pointless [https://security.stackexchange.com/questions/1687/does-hashing-a-file-from-an-unsigned-website-give-a-false-sense-of-security](https://security.stackexchange.com/questions/1687/does-hashing-a-file-from-an-unsigned-website-give-a-false-sense-of-security), download balenaEtcher portable from [https://etcher.balena.io/](https://etcher.balena.io/) (currently recommended burner at [https://ubuntu.com/download/desktop#how-to-install](https://ubuntu.com/download/desktop#how-to-install)) from etc, and burn Ubuntu into a [SanDisk Ultra Flair 64 GB](sandisk-ultra-flair-64-gb.md)
- install Ubuntu from USB flash. No internet connection initially, default everything.
- notice that Ubuntu 24.04 is too broken, install [Ubuntu 22.04](../ubuntu-22-04.md).4 on the previously used USB from Ubuntu, and then install 22.04 instead... minimal installation, encrypted ZFS
  - [Ubuntu 24.04 "The application files has closed unexpectedly"](../ubuntu-24-04-the-application-files-has-closed-unexpectedly.md). This likely terminated uncompression of the bz2 halfway, and led to a corrupted monerod...
  - [https://askubuntu.com/questions/15520/how-can-i-tell-ubuntu-to-do-nothing-when-i-close-my-laptop-lid](https://askubuntu.com/questions/15520/how-can-i-tell-ubuntu-to-do-nothing-when-i-close-my-laptop-lid) fix the eternal laptop lid issue without GUI solution...
- copy view only wallet private key by takinga picture of the QR code with Android cell phone. This gives it to the [CIA](../central-intelligence-agency.md) immediately, but that's fine as we're going to publish it publicly.
It must have taken about one week running full time to sync the Monero blockchain which at the time was at about 3.1M blocks! I checked on system explorer, and CPU and internet usage was never maxed out, suggesting simply slow network. But the computer still overheated quite a bit and froze a few times.

## ↑ Ancestors (5)

1. [Laptop](laptop.md)
2. [Computers](computers.md)
3. [Ciro Santilli's hardware](../ciro-santilli-s-hardware-split.md)
4. [Ciro Santilli](../ciro-santilli-split.md)
5. [Ciro Santilli's Homepage](../split.md)

## ← Incoming links (4)

- [SanDisk Ultra Flair 64 GB](sandisk-ultra-flair-64-gb.md)
- [Sponsor Ciro Santilli's work on OurBigBook.com](../sponsor-split.md)
- [Ubuntu 24.04 installer "Erase disk and install Ubuntu" doesn't work when BitLocker enabled](../ubuntu-24-04-installer-erase-disk-and-install-ubuntu-doesn-t-work-when-bitlocker-enabled.md)
- [Ubuntu 24.04 "The application files has closed unexpectedly"](../ubuntu-24-04-the-application-files-has-closed-unexpectedly.md)
