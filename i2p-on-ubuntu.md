# I2P on [Ubuntu](ubuntu.md)

↑ **Parent:** [I2P](i2p.md)

On [Ubuntu 26.04](ubuntu-26-04.md), visiting [https://i2p.net/en/downloads/](https://i2p.net/en/downloads/) recommended me to download [https://files.i2p.net/2.12.0/i2pinstall_2.12.0.jar](https://files.i2p.net/2.12.0/i2pinstall_2.12.0.jar) so I did:
```
cd ~
wget https://files.i2p.net/2.12.0/i2pinstall_2.12.0.jar
sudo apt install openjdk-17-jre
JAVA_HOME=/usr/lib/jvm/java-17-openjdk-amd64 PATH="$JAVA_HOME/bin:$PATH" java -jar ./i2pinstall_2.12.0.jar -console
```
Then after some clicking faff
```
cd ~/i2p
JAVA_HOME=/usr/lib/jvm/java-17-openjdk-amd64 PATH="$JAVA_HOME/bin:$PATH" ./i2prouter start
```
and it told me:
```
Starting I2P Service...
Waiting for I2P Service....
running: PID:423806
```
and it automatically opened up a Chrome tab at: [http://127.0.0.1:7657/welcome](http://127.0.0.1:7657/welcome)

The default Java 8 installed on my machine is too old, needed 17 or above. Very annoying.

To make things more bearable I added this to my `.bashrc`:

```
i2p() (
  cd ~/i2p
  JAVA_HOME=/usr/lib/jvm/java-17-openjdk-amd64 PATH="$JAVA_HOME/bin:$PATH" ./i2prouter "$@"
)
```

so I can just:

```
i2p start
i2p stop
```

**Table of contents**

- [I2P on Ubuntu browser setup](i2p-on-ubuntu-browser-setup.md)
- [I2P Ubuntu via PPA](i2p-ubuntu-via-ppa.md)

## ↑ Ancestors (10)

1. [I2P](i2p.md)
2. [Internet privacy technology](internet-privacy-technology.md)
3. [Internet privacy](internet-privacy.md)
4. [Cryptography](cryptography-split.md)
5. [Computer science](computer-science-split.md)
6. [Computer](computer-split.md)
7. [Information technology](information-technology.md)
8. [Area of technology](area-of-technology.md)
9. [Technology](technology-split.md)
10. [Ciro Santilli's Homepage](split.md)
