# 2013 DNS census NS records

↑ **Parent:** [DNS Census 2013](dns-census-2013.md)

<a id="_6113"></a>
ns.csv is 57 GB. This file is too massive, working with it is a pain.

<a id="_6114"></a>
We can also cut down the data a lot with [https://stackoverflow.com/questions/1915636/is-there-a-way-to-uniq-by-column/76605540#76605540](https://stackoverflow.com/questions/1915636/is-there-a-way-to-uniq-by-column/76605540#76605540) and [tld filtering](non-com-net-tlds.md):<a id="_6115"></a>

```
awk -F, 'BEGIN{OFS=","} { if ($1 != last) { print $1, $3; last = $1; } }' ns.csv | grep -E '\.(com|net|info|org|biz),' > nsu.csv
```
This brings us down to a much more manageable 3.0 GB, 83 M rows.

<a id="_6116"></a>
Let's just scan it once real quick to start with, since likely nothing will come of this venue:<a id="_6117"></a>

```
grep -f <(awk -F, 'NR>1{print $2}' ../media/cia-2010-covert-communication-websites/hits.csv) nsu.csv | tee nsu-hits.csv
cat nsu-hits.csv | csvcut -c 2 | sort | awk -F. '{OFS="."; print $(NF-1), $(NF)}' | sort | uniq -c | sort -k1 -n
```
As of 267 hits we get:<a id="_6118"></a>

```
      1 a2hosting.com
      1 amerinoc.com
      1 ayns.net
      1 dailyrazor.com
      1 domainingdepot.com
      1 easydns.com
      1 frienddns.ru
      1 hostgator.com
      1 kolmic.com
      1 name-services.com
      1 namecity.com
      1 netnames.net
      1 tonsmovies.net
      1 webmailer.de
      2 cashparking.com
     55 worldnic.com
     86 domaincontrol.com
```
so yeah, most of those are likely going to be humongous just by looking at the names.

<a id="_6119"></a>
The smallest ones by far from the total are: frienddns.ru with only 487 hits, all others quite large or fake hits due to CSV. Did a quick [Wayback Machine CDX scanning](wayback-machine-cdx-scanning.md) there but no luck alas.

<a id="_6120"></a>
Let's check the smaller ones:<a id="_6121"></a>

```
inews-today.com,2013-08-12T03:14:01,ns1.frienddns.ru
source-commodities.net,2012-12-13T20:58:28,ns1.namecity.com -> fake hit due to grep e-commodities.net
dailynewsandsports.com,2013-08-13T08:36:28,ns3.a2hosting.com
just-kidding-news.com,2012-02-04T07:40:50,jns3.dailyrazor.com
fightwithoutrules.com,2012-11-09T01:17:40,sk.s2.ns1.ns92.kolmic.com
fightwithoutrules.com,2013-07-01T22:46:23,ns1625.ztomy.com
half-court.net,2012-09-10T09:49:15,sk.s2.ns1.ns92.kolmic.com
half-court.net,2013-07-07T00:31:12,ns1621.ztomy.com
```
Doubt anything will come out of this.

<a id="_6122"></a>
Let's do a bit of counting out of the total:<a id="_6123"></a>

```
grep domaincontrol.com ns.csv | awk -F, '{print $1}' | uniq | wc
```
gives ~20M domain using `domaincontrol`. Let's see how many domains are in the first place:<a id="_6124"></a>

```
awk -F, '{print $1}' ns.csv | uniq | wc
```
so it accounts for 1/4 of the total.

## ↑ Ancestors (15)

1. [DNS Census 2013](dns-census-2013.md)
2. [Data sources](data-sources.md)
3. [Methodology](methodology.md)
4. [CIA 2010 covert communication websites](../cia-2010-covert-communication-websites-split.md)
5. [Central Intelligence Agency](../central-intelligence-agency.md)
6. [American intelligence agency](../american-intelligence-agency.md)
7. [United States Intelligence Community](../united-states-intelligence-community.md)
8. [Intelligence community](../intelligence-community.md)
9. [Secret service](../secret-service.md)
10. [Espionage](../espionage.md)
11. [War](../war.md)
12. [Social science](../social-science.md)
13. [Scientific method](../scientific-method.md)
14. [Science](../science-split.md)
15. [Ciro Santilli's Homepage](../split.md)

## ← Incoming links (1)

- [2013 DNS census SOA records](2013-dns-census-soa-records.md)
