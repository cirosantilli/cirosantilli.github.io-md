# Wayback Machine rate limit

↑ **Parent:** [Wayback Machine](wayback-machine.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Wayback_Machine_rate_limit)

[https://archive.org/details/toomanyrequests_20191110](https://archive.org/details/toomanyrequests_20191110) says 15 archives / minute, but apparently aslo 15 retrievals per minutes on Wikipedia, after which 5 min blacklist. After that, you start getting some 429s, and after that, server refuses to connect at al.

CDX: no limits apparently, they might just throttle you? Made 10k requets on bash loop and was going fine. But not that if you get blacklisted by create/fetch requests blacklist, server fails to connect here as well.

## ↑ Ancestors (6)

1. [Wayback Machine](wayback-machine.md)
2. [Internet Archive](internet-archive.md)
3. [Web archiving](web-archiving.md)
4. [Website](website-split.md)
5. [Art](art-split.md)
6. [Ciro Santilli's Homepage](split.md)
