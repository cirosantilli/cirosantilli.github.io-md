# 2013 DNS Census virtual host cleanup heuristic keyword searches

↑ **Parent:** [2013 DNS Census virtual host cleanup](2013-dns-census-virtual-host-cleanup.md)

There are two keywords that are killers: "news" and "world" and their translations or closely related words. Everything else is hard. So a good start is:

```
grep -e news -e noticias -e nouvelles -e world -e global
```

iran + football:
- iranfootballsource.com: the third hit for this area after the two given by Reuters! Epic.

3 easy hits with "noticias" (news in Portuguese or Spanish"), uncovering two brand new ip ranges:
- 66.45.179.205 noticiasporjanua.com
- 66.237.236.247 comunidaddenoticias.com
- 204.176.38.143 noticiassofisticadas.com

Let's see some French "nouvelles/actualites" for those tumultuous Maghrebis:
- 216.97.231.56 nouvelles-d-aujourdhuis.com

news + world:
- 210.80.75.55 philippinenewsonline.net

news + global:
- 204.176.39.115 globalprovincesnews.com
- 212.209.74.105 globalbaseballnews.com
- 212.209.79.40: hydradraco.com

OK, I've decided to do a complete [Wayback Machine CDX scanning](wayback-machine-cdx-scanning.md) of `news`... Searching for `.JAR` or `https.*cgi-bin.*\.cgi` are killers, particularly the .jar hits, here's what came out:
- 62.22.60.49 telecom-headlines.com
- 62.22.61.206 worldnewsnetworking.com
- 64.16.204.55 holein1news.com
- 66.104.169.184 bcenews.com
- 69.84.156.90 stickshiftnews.com
- 74.116.72.236 techtopnews.com
- 74.254.12.168 non-stop-news.net
- 193.203.49.212 inews-today.com
- 199.85.212.118 just-kidding-news.com
- 207.210.250.132 aeronet-news.com
- 212.4.18.129 sightseeingnews.com
- 212.209.90.84 thenewseditor.com
- 216.105.98.152 modernarabicnews.com

[Wayback Machine CDX scanning](wayback-machine-cdx-scanning.md) of "world":
- 66.104.173.186 myworldlymusic.com

"headline": only 140 matches in 2013-dns-census-a-novirt.csv and 3 hits out of 269 hits. Full inspection without CDX led to no new hits.

"today": only 3.5k matches in 2013-dns-census-a-novirt.csv and 12 hits out of 269 hits, TODO how many on those on 2013-dns-census-a-novirt? No new hits.

"world", "global", "international", and spanish/portuguese/French versions like "mondo", "mundo", "mondi": 15k matches in 2013-dns-census-a-novirt.csv. No new hits.

## ↑ Ancestors (16)

1. [2013 DNS Census virtual host cleanup](2013-dns-census-virtual-host-cleanup.md)
2. [DNS Census 2013](dns-census-2013.md)
3. [Data sources](data-sources.md)
4. [Methodology](methodology.md)
5. [CIA 2010 covert communication websites](../cia-2010-covert-communication-websites-split.md)
6. [Central Intelligence Agency](../central-intelligence-agency.md)
7. [American intelligence agency](../american-intelligence-agency.md)
8. [United States Intelligence Community](../united-states-intelligence-community.md)
9. [Intelligence community](../intelligence-community.md)
10. [Secret service](../secret-service.md)
11. [Espionage](../espionage.md)
12. [War](../war.md)
13. [Social science](../social-science.md)
14. [Scientific method](../scientific-method.md)
15. [Science](../science-split.md)
16. [Ciro Santilli's Homepage](../split.md)

## ← Incoming links (6)

- [2013 DNS census secureserver.net MX records intersection 2013 DNS Census virtual host cleanup](2013-dns-census-secureserver-net-mx-records-intersection-2013-dns-census-virtual-host-cleanup.md)
- [Breakthroughs](breakthroughs.md)
- [Hits with nearby IP hits](hits-with-nearby-ip-hits.md)
- [Hits without nearby IP hits](hits-without-nearby-ip-hits.md)
- [List of websites](list-of-websites.md)
- [Secure subdomain search on 2013 DNS Census](secure-subdomain-search-on-2013-dns-census.md)
