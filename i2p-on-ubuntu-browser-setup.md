# I2P on [Ubuntu](ubuntu.md) browser setup

↑ **Parent:** [I2P on Ubuntu](i2p-on-ubuntu.md)

It does not come with a default browser... A popular option seems to be to install a praivate browser such as LibreWolf (Firefox based) to be your I2P thing [https://www.youtube.com/watch?v=qFE1J9YhhWg](https://www.youtube.com/watch?v=qFE1J9YhhWg) Setting it up as such makes it not work as a regular clearnet browser. Instructions at: [https://librewolf.net/installation/debian/](https://librewolf.net/installation/debian/)

```
sudo apt update && sudo apt install extrepo -y
sudo extrepo enable librewolf && sudo extrepo update librewolf
sudo apt update && sudo apt install librewolf -y
```

Then go to Proxy settings and set Manual proxy configuration:

- HTTP Proxy: 127.0.0.1:4444
- SOCKS Host: 127.0.0.1:4447

Another setting you really want in LibreWolf is:

> Don't enable HTTPS-Only Mode

otherwise it keeps complaining every time that pages are not https, because they are all http, because the security is happening at a lower layer of the protocol already. 

Then I can visit the sample website [http://tracker2.postman.i2p.](http://tracker2.postman.i2p.) It complains that it's not https, but I say, OK, I think I'm already mega encrypted figers crossed. It is a simple oldschool forum like phpBB where people announce their I2P compatible Torrents. From the posts I can copy a Magnet link and add it to [http://127.0.0.1:7657/i2psnark/,](http://127.0.0.1:7657/i2psnark/,) the built-in Torrent thing, the only convenient thing they have pre-setup for you :-)

Shame setting up this project is so difficult, it can never reach mainstream like this. Tor Browser and centralized VPN are so much more streamlined. But if it were mainstream, it would be boring? Early 200ss vibes come to mind.

## ↑ Ancestors (11)

1. [I2P on Ubuntu](i2p-on-ubuntu.md)
2. [I2P](i2p.md)
3. [Internet privacy technology](internet-privacy-technology.md)
4. [Internet privacy](internet-privacy.md)
5. [Cryptography](cryptography-split.md)
6. [Computer science](computer-science-split.md)
7. [Computer](computer-split.md)
8. [Information technology](information-technology.md)
9. [Area of technology](area-of-technology.md)
10. [Technology](technology-split.md)
11. [Ciro Santilli's Homepage](split.md)
