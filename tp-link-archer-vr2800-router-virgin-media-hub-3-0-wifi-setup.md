<h1 id="tp-link-archer-vr2800-router-virgin-media-hub-3-0-wifi-setup">TP-Link Archer VR2800 router Virgin Media Hub 3.0 Wifi setup</h1>

↑ **Parent:** [TP-Link](tp-link.md)

Put Hub 3.0 in modem mode on 192.168.0.1. Turn it off. You MUST TURN IT OFF NOW.

TP Link Archer VR2800 192.168.1.1 and set:

- "Operation mode" \> "Wireless router mode" (was "DSL Modem/Router mode" by default).
- "Network" \> "Internet" \> "Add" \> "Internet Connection Type" \> "Dynamic IP" \> "Save"

Custom configs we had, not sure if mandatory:
- Dynamic DHPC mode
- Unicast DHCP

Wait for TP link to fully reboot.

Connect port 4 of tp link (marked WAN/LAn) to port 1 of VM Hub (unmarked, but it is magic, has to be port 1).

Finally, AFTER everything else is setup, turn on the Hub and wait for a few minutes. It ONY WORKS if you turn it on after everything is setup.

Outcome:
- hub light turns purple: [https://www.reddit.com/r/VirginMedia/comments/c703t6/purple_light_on_the_box/](https://www.reddit.com/r/VirginMedia/comments/c703t6/purple_light_on_the_box/)
- Archer WAN light turns on white. Not red. Red means error
- you have Wifi. Notably, the 5G Wifi is way way faster and reaches the WAN limit of 256 Mbps.
- Ethernet does not work anymore on either Hub nor Archer, Wifi only. But it doesn't matter because the 5G Wifi already reaches the speed limit.

<a id="video-how-to-use-a-tp-link-archer-vr2800-modem-router-with-virgin-media-hub-3-0-for-wifi"></a>
**[Video 16](#video-how-to-use-a-tp-link-archer-vr2800-modem-router-with-virgin-media-hub-3-0-for-wifi). How to use a TP-Link ARCHER VR2800 modem/router with Virgin Media Hub 3.0 for Wifi.** [Source](https://www.youtube.com/watch?v=7vqVVlEFnV4).

Bibliography:
- [https://community.virginmedia.com/t5/Forum-Archive/Connecting-Tp-link-archer-vr2800-to-Hub-3/td-p/4765927](https://community.virginmedia.com/t5/Forum-Archive/Connecting-Tp-link-archer-vr2800-to-Hub-3/td-p/4765927) This was The thread, the only one that clearly explained the fundamental importance of turn on off ordering by "jbrennand".
- [https://community.tp-link.com/en/home/forum/topic/269540](https://community.tp-link.com/en/home/forum/topic/269540)
- [https://community.tp-link.com/en/home/forum/topic/170344](https://community.tp-link.com/en/home/forum/topic/170344)
- [https://community.virginmedia.com/t5/Gaming-Support/Connecting-Archer-VR2800-to-Hub-4/td-p/5246513](https://community.virginmedia.com/t5/Gaming-Support/Connecting-Archer-VR2800-to-Hub-4/td-p/5246513)

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

## ← Incoming links (1)

- [TP-Link Archer VR2800 router allow external access to the network](tp-link-archer-vr2800-router-allow-external-access-to-the-network.md)
