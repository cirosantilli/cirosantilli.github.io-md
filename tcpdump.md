# tcpdump

↑ **Parent:** [Computer network software](computer-network-software.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/tcpdump)

To test it, let's get two computers on the same [local area network](local-area-network.md), e.g. connected to [Wi-Fi](wi-fi.md) on the same home [modem router](modem-router.md).

On computer B:
- [find computer IP with the `ip` CLI tool](find-computer-ip-with-the-ip-cli-tool.md). Suppose it is 192.168.1.102
- then run [Ciro's `nc` HTTP test server](ciro-s-nc-http-test-server.md)

On computer A, run on terminal 1:
```
sudo tcpdump ip src 192.168.1.102 or dst 192.168.1.102
```

Then on terminal 2 make a test request:
```
curl 192.168.1.102:8000
```

Output on terminal 1:
```
17:14:22.017001 IP ciro-p14s.55798 > 192.168.1.102.8000: Flags [S], seq 2563867413, win 64240, options [mss 1460,sackOK,TS val 303966323 ecr 0,nop,wscale 7], length 0
17:14:22.073957 IP 192.168.1.102.8000 > ciro-p14s.55798: Flags [S.], seq 1371418143, ack 2563867414, win 65160, options [mss 1460,sackOK,TS val 171832817 ecr 303966323,nop,wscale 7], length 0
17:14:22.074002 IP ciro-p14s.55798 > 192.168.1.102.8000: Flags [.], ack 1, win 502, options [nop,nop,TS val 303966380 ecr 171832817], length 0
17:14:22.074195 IP ciro-p14s.55798 > 192.168.1.102.8000: Flags [P.], seq 1:82, ack 1, win 502, options [nop,nop,TS val 303966380 ecr 171832817], length 81
17:14:22.076710 IP 192.168.1.102.8000 > ciro-p14s.55798: Flags [P.], seq 1:80, ack 1, win 510, options [nop,nop,TS val 171832821 ecr 303966380], length 79
17:14:22.076710 IP 192.168.1.102.8000 > ciro-p14s.55798: Flags [.], ack 82, win 510, options [nop,nop,TS val 171832821 ecr 303966380], length 0
17:14:22.076727 IP ciro-p14s.55798 > 192.168.1.102.8000: Flags [.], ack 80, win 502, options [nop,nop,TS val 303966383 ecr 171832821], length 0
17:14:22.077006 IP ciro-p14s.55798 > 192.168.1.102.8000: Flags [F.], seq 82, ack 80, win 502, options [nop,nop,TS val 303966383 ecr 171832821], length 0
17:14:22.077564 IP 192.168.1.102.8000 > ciro-p14s.55798: Flags [F.], seq 80, ack 82, win 510, options [nop,nop,TS val 171832821 ecr 303966380], length 0
17:14:22.077578 IP ciro-p14s.55798 > 192.168.1.102.8000: Flags [.], ack 81, win 502, options [nop,nop,TS val 303966384 ecr 171832821], length 0
17:14:22.079429 IP 192.168.1.102.8000 > ciro-p14s.55798: Flags [.], ack 83, win 510, options [nop,nop,TS val 171832824 ecr 303966383], length 0
```
TODO understand them all! Possibly correlate with [Wireshark](wireshark.md), or use `-A` option to dump content.

## ↑ Ancestors (7)

1. [Computer network software](computer-network-software.md)
2. [Computer network](computer-network.md)
3. [Computer](computer-split.md)
4. [Information technology](information-technology.md)
5. [Area of technology](area-of-technology.md)
6. [Technology](technology-split.md)
7. [Ciro Santilli's Homepage](split.md)
