# Wayback Machine CDX scanning with Tor parallelization

↑ **Parent:** [Wayback Machine CDX scanning](wayback-machine-cdx-scanning.md)

<a id="_5989"></a>
Dire times require dire methods: [cia-2010-covert-communication-websites/cdx-tor.sh](cia-2010-covert-communication-websites/cdx-tor.sh).

<a id="_5990"></a>
First we must start the tor servers with the `tor-army` command from: [https://stackoverflow.com/questions/14321214/how-to-run-multiple-tor-processes-at-once-with-different-exit-ips/76749983#76749983](https://stackoverflow.com/questions/14321214/how-to-run-multiple-tor-processes-at-once-with-different-exit-ips/76749983#76749983)<a id="_5991"></a>

```
tor-army 100
```
and then use it on a newline separated domain name list to check;<a id="_5992"></a>

```
./cdx-tor.sh infile.txt
```
This creates a directory `infile.txt.cdx/` containing:<a id="_5993"></a>

<a id="_5994"></a>
- `infile.txt.cdx/out00`, `out01`, etc.: the suspected CDX lines from domains from each tor instance based on the simple criteria that the CDX can handle directly. We split the input domains into 100 piles, and give one selected pile per tor instance.
<a id="_5995"></a>
- `infile.txt.cdx/out`: the final combined CDX output of `out00`, `out01`, ...
<a id="_5996"></a>
- `infile.txt.cdx/out.post`: the final output containing only domain names that match further CLI criteria that cannot be easily encoded on the CDX query. This is the cleanest domain name list you should look into at the end basically.

<a id="_5997"></a>
Since archive is so abysmal in its data access, e.g. a [Google BigQuery](../google-bigquery.md) would solve our issues in seconds, we have to come up with creative ways of getting around their IP throttling.

<a id="_5998"></a>
The [CIA](../central-intelligence-agency.md) doesn't play fair. They're actually the exact opposite of fair. So neither shall we.

<a id="_5999"></a>
Distilled into an answer at: [https://stackoverflow.com/questions/14321214/how-to-run-multiple-tor-processes-at-once-with-different-exit-ips/76749983#76749983](https://stackoverflow.com/questions/14321214/how-to-run-multiple-tor-processes-at-once-with-different-exit-ips/76749983#76749983)

<a id="_6000"></a>
This should allow a full sweep of the 4.5M records in [2013 DNS Census virtual host cleanup](2013-dns-census-virtual-host-cleanup.md) in a reasonable amount of time. After JAR/SWF/CGI filtering we obtained 5.8k domains, so a reduction factor of about 1 million with likely very few losses. Not bad.

<a id="_6001"></a>
5.8k is still a bit annoying to fully go over however, so we can also try to count CDX hits to the domains and remove anything with too many hits, since the CIA websites basically have very few archives:<a id="_6002"></a>

```
cd 2013-dns-census-a-novirt-domains.txt.cdx
./cdx-tor.sh -d out.post domain-list.txt
cd out.post.cdx
cut -d' ' -f1 out | uniq -c | sort -k1 -n | awk 'match($2, /([^,]+),([^)]+)/, a) {printf("%s.%s %d\n", a[2], a[1], $1)}' > out.count
```
This gives us something like:<a id="_6003"></a>

```
12654montana.com 1
aeronet-news.com 1
atohms.com 1
av3net.com 1
beechstreetas400.com 1
```
sorted by increasing hit counts, so we can go down as far as patience allows for!

<a id="_6004"></a>
New results from a full CDX scan of 2013-dns-census-a-novirt.csv:<a id="_6005"></a>

<a id="_6006"></a>
- 219.90.61.123 journeystravelled.com

## ↑ Ancestors (16)

1. [Wayback Machine CDX scanning](wayback-machine-cdx-scanning.md)
2. [Wayback Machine](wayback-machine.md)
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

## ← Incoming links (2)

- [Expired domain trackers](expired-domain-trackers.md)
- [Overview of Ciro Santilli's investigation](overview-of-ciro-santilli-s-investigation.md)
