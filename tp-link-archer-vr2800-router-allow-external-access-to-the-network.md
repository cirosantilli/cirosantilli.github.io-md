# TP-Link Archer VR2800 router allow external access to the network

↑ **Parent:** [TP-Link](tp-link.md)

This section explains a tutorial on how to allow external computers to access a computer in your network.

For example, this could for example be used to allow you to access [SSH](secure-shell.md) or a web server running on a computer at your home from your laptop when you are outside of your home.

What you need to do seems to be:
- NAT Forwarding: allows you to select which external port you want to forward to which internal IP + port
- Network \> LAN Settings \> Address reservation \> and reserve the IP above to the MAC of your computer
From there on, you just need to [find your public IP](find-your-public-ip.md) and use that, e.g. you could test accessing a test server from your cell phone cellular network after turning [Wifi](wi-fi.md) off for the cell phone.

[Ciro Santilli](ciro-santilli-split.md) tested this on his [TP-Link Archer VR2800 router Virgin Media Hub 3.0 Wifi setup](tp-link-archer-vr2800-router-virgin-media-hub-3-0-wifi-setup.md) and it just worked. Virgin Media doesn't seem to pose any strict restrictions to this.

A next good step if you are going to have a workhorse computer without much personal logins of value is to setup "group isolation" so that if that computer ever gets compromised, hackers won't be able to infiltrate the rest of the network. But TODO: couldn't find the setting on the TP-Link Archer VR2800 even though the manual says it should be there. Oh well.

## ↑ Ancestors (10)

1. [TP-Link](tp-link.md)
2. [Modem router](modem-router.md)
3. [Router (computing)](router-computing.md)
4. [Networking hardware](networking-hardware.md)
5. [Computer network](computer-network.md)
6. [Computer](computer-split.md)
7. [Information technology](information-technology.md)
8. [Area of technology](area-of-technology.md)
9. [Technology](technology-split.md)
10. [Ciro Santilli's Homepage](split.md)
