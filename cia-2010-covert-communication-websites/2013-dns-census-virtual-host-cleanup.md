# 2013 DNS Census virtual host cleanup

↑ **Parent:** [DNS Census 2013](dns-census-2013.md)

<a id="_6033"></a>
We've noticed that often when there is a hit range:<a id="_6034"></a>

<a id="_6035"></a>
- there is only one IP for each domain
<a id="_6036"></a>
- there is a range of about 20-30 of those
and that this does not seem to be that common. Let's see if that is a reasonable fingerprint or not.

<a id="_6037"></a>
Note that although this is the most common case, we have found multiple hits that [viewdns.info](viewdns-info.md) maps to the same IP.

<a id="_6038"></a>
First we create a table `u` (`unique`) that only have domains which are the only domain for an IP, let's see by how much that lowers the 191 M total unique domains:<a id="_6039"></a>

```
time sqlite3 u.sqlite 'create table t (d text, i text)'
time sqlite3 av.sqlite -cmd "attach 'u.sqlite' as u" "insert into u.t select min(d) as d, min(i) as i from t where d not like '%.%.%' group by i having count(distinct d) = 1"
```
The `not like '%.%.%'` removes subdomains from the counts so that [CGI comms](cgi-comms.md) are still included, and `distinct` in `count(distinct` is because we have multiple entries at different timestamps for some of the hits.

<a id="_6040"></a>
Let's start with the 208 subset to see how it goes:<a id="_6041"></a>

```
time sqlite3 av.sqlite -cmd "attach 'u.sqlite' as u" "insert into u.t select min(d) as d, min(i) as i from t where i glob '208.*' and d not like '%.%.%' and (d like '%.com' or d like '%.net') group by i having count(distinct d) = 1"
```
OK, after we fixed bugs with the above we are down to 4 million lines with unique domain/IP pairs and which contains all of the original hits! Almost certainly more are to be found!

<a id="_6042"></a>
This data is so valuable that we've decided to upload it to: [https://archive.org/details/2013-dns-census-a-novirt.csv](https://archive.org/details/2013-dns-census-a-novirt.csv) Format:<a id="_6043"></a>

```
8,chrisjmcgregor.com
11,80end.com
28,fine5.net
38,bestarabictv.com
49,xy005.com
50,cmsasoccer.com
80,museemontpellier.net
100,newtiger.com
108,lps-promptservice.com
111,bridesmaiddressesshow.com
```
The numbers of the first column are the IPs as a 32-bit integer representation, which is more useful to search for ranges in.

<a id="_6044"></a>
To make a [histogram](../histogram.md) with the distribution of the single hostname IPs:<a id="_6045"></a>

```
#!/usr/bin/env bash
bin=$((2**24))
sqlite3 2013-dns-census-a-novirt.sqlite -cmd '.mode csv' >2013-dns-census-a-novirt-hist.csv <<EOF
select i, sum(cnt) from (
  select floor(i/${bin}) as i,
         count(*) as cnt
    from t
    group by 1
  union
  select *, 0 as cnt from generate_series(0, 255)
)
group by i
EOF
gnuplot \
  -e 'set terminal svg size 1200, 800' \
  -e 'set output "2013-dns-census-a-novirt-hist.svg"' \
  -e 'set datafile separator ","' \
  -e 'set tics scale 0' \
  -e 'unset key' \
  -e 'set xrange[0:255]' \
  -e 'set title "Counts of IPs with a single hostname"' \
  -e 'set xlabel "IPv4 first byte"' \
  -e 'set ylabel "count"' \
  -e 'plot "2013-dns-census-a-novirt-hist.csv" using 1:2:1 with labels' \
;
```
Which gives the following useless noise, there is basically no pattern:<a id="_6046"></a>


![](https://raw.githubusercontent.com/cirosantilli/media/master/cia-2010-covert-communication-websites/2013-dns-census-a-novirt-hist.svg)

**Table of contents**

- [2013 DNS Census virtual host cleanup heuristic keyword searches](2013-dns-census-virtual-host-cleanup-heuristic-keyword-searches.md)

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

## ← Incoming links (4)

- [2013 DNS census MX records](2013-dns-census-mx-records.md)
- [2013 DNS census secureserver.net MX records intersection 2013 DNS Census virtual host cleanup](2013-dns-census-secureserver-net-mx-records-intersection-2013-dns-census-virtual-host-cleanup.md)
- [Hits with nearby IP hits](hits-with-nearby-ip-hits.md)
- [Wayback Machine CDX scanning with Tor parallelization](wayback-machine-cdx-scanning-with-tor-parallelization.md)
