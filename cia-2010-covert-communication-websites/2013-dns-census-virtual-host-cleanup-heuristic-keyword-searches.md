# 2013 DNS Census virtual host cleanup heuristic keyword searches

↑ **Parent:** [2013 DNS Census virtual host cleanup](2013-dns-census-virtual-host-cleanup.md)

<a id="_6047"></a>
There are two keywords that are killers: "news" and "world" and their translations or closely related words. Everything else is hard. So a good start is:

<a id="_6048"></a>
```
grep -e news -e noticias -e nouvelles -e world -e global
```

<a id="_6049"></a>
iran + football:<a id="_6050"></a>

<a id="_6051"></a>
- iranfootballsource.com: the third hit for this area after the two given by Reuters! Epic.

<a id="_6052"></a>
3 easy hits with "noticias" (news in Portuguese or Spanish"), uncovering two brand new ip ranges:<a id="_6053"></a>

<a id="_6054"></a>
- 66.45.179.205 noticiasporjanua.com
<a id="_6055"></a>
- 66.237.236.247 comunidaddenoticias.com
<a id="_6056"></a>
- 204.176.38.143 noticiassofisticadas.com

<a id="_6057"></a>
Let's see some French "nouvelles/actualites" for those tumultuous Maghrebis:<a id="_6058"></a>

<a id="_6059"></a>
- 216.97.231.56 nouvelles-d-aujourdhuis.com

<a id="_6060"></a>
news + world:<a id="_6061"></a>

<a id="_6062"></a>
- 210.80.75.55 philippinenewsonline.net

<a id="_6063"></a>
news + global:<a id="_6064"></a>

<a id="_6065"></a>
- 204.176.39.115 globalprovincesnews.com
<a id="_6066"></a>
- 212.209.74.105 globalbaseballnews.com
<a id="_6067"></a>
- 212.209.79.40: hydradraco.com

<a id="_6068"></a>
OK, I've decided to do a complete [Wayback Machine CDX scanning](wayback-machine-cdx-scanning.md) of `news`... Searching for `.JAR` or `https.*cgi-bin.*\.cgi` are killers, particularly the .jar hits, here's what came out:<a id="_6069"></a>

<a id="_6070"></a>
- 62.22.60.49 telecom-headlines.com
<a id="_6071"></a>
- 62.22.61.206 worldnewsnetworking.com
<a id="_6072"></a>
- 64.16.204.55 holein1news.com
<a id="_6073"></a>
- 66.104.169.184 bcenews.com
<a id="_6074"></a>
- 69.84.156.90 stickshiftnews.com
<a id="_6075"></a>
- 74.116.72.236 techtopnews.com
<a id="_6076"></a>
- 74.254.12.168 non-stop-news.net
<a id="_6077"></a>
- 193.203.49.212 inews-today.com
<a id="_6078"></a>
- 199.85.212.118 just-kidding-news.com
<a id="_6079"></a>
- 207.210.250.132 aeronet-news.com
<a id="_6080"></a>
- 212.4.18.129 sightseeingnews.com
<a id="_6081"></a>
- 212.209.90.84 thenewseditor.com
<a id="_6082"></a>
- 216.105.98.152 modernarabicnews.com

<a id="_6083"></a>
[Wayback Machine CDX scanning](wayback-machine-cdx-scanning.md) of "world":<a id="_6084"></a>

<a id="_6085"></a>
- 66.104.173.186 myworldlymusic.com

<a id="_6086"></a>
"headline": only 140 matches in 2013-dns-census-a-novirt.csv and 3 hits out of 269 hits. Full inspection without CDX led to no new hits.

<a id="_6087"></a>
"today": only 3.5k matches in 2013-dns-census-a-novirt.csv and 12 hits out of 269 hits, TODO how many on those on 2013-dns-census-a-novirt? No new hits.

<a id="_6088"></a>
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
