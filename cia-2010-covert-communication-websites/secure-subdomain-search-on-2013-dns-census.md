# secure subdomain search on 2013 DNS Census

↑ **Parent:** [Non Reuters ranges](non-reuters-ranges.md)

<a id="_6627"></a>
Grepping the [2013 DNS Census](dns-census-2013.md) first by overused [CGI comms](cgi-comms.md) subdomains `secure.` and `ssl.` leaves 200k lines. Grepping for the overused "news" led to hits:<a id="_6628"></a>

<a id="_6629"></a>
- secure.worldnewsandent.com,2012-02-13T21:28:15,208.254.40.117
<a id="_6630"></a>
- ssl.beyondnetworknews.com,2012-02-13T20:10:13,66.104.175.40

<a id="_6631"></a>
Also tried but failed:<a id="_6632"></a>

<a id="_6633"></a>
- `sports`:<a id="_6634"></a>

  <a id="_6635"></a>
  - secure.motorsportdealers.com,2012-04-10T20:19:09,64.73.117.38 [https://web.archive.org/web/20110501000000*/motorsportdealers.com](https://web.archive.org/web/20110501000000*/motorsportdealers.com)

<a id="_6636"></a>
OK, after the initial successes in `secure.`, we went a bit more data intensive:<a id="_6637"></a>

<a id="_6638"></a>
- took all `secure.*` `ssl.*` URLs in the [2013 DNS Census](dns-census-2013.md), 70k entries
<a id="_6639"></a>
- cleaned up a bit, e.g. only `.com` or `.net`. this left only, 30k entries only
<a id="_6640"></a>
- lopped over all of them in archive CDX: [Wayback Machine CDX scanning](wayback-machine-cdx-scanning.md), searching for those that also end in `.cgi` [https://web.archive.org/cdx/search/cdx?url=$domain&matchType=domain&filter=urlkey:.*.cgi&to=20140101000000](https://web.archive.org/cdx/search/cdx?url=$domain&matchType=domain&filter=urlkey:.*.cgi&to=20140101000000). Took an afternoon, but no rate limit block.
<a id="_6641"></a>
- this leaves about 1000, so we loop over all of them manually on web archive with a script, and opened any that had the pattern of very vew hits between 2010 and 2013 only, and on those check for visual/thematic style match. Careful not to make more than 15 requests per minute or else 5 min blacklist!
New results: only one...<a id="_6642"></a>

<a id="_6643"></a>
- 208.254.42.205 secure.driversinternationalgolf.com,2012-02-13T10:42:20,

<a id="_6644"></a>
After [2013 DNS Census virtual host cleanup heuristic keyword searches](2013-dns-census-virtual-host-cleanup-heuristic-keyword-searches.md) we later understood why there were so few hits here: the [2013 DNS Census](dns-census-2013.md) didn't capture the `secure.` subdomains of many domains it had for some reason. Shame, because if it had, this method would have yielded many more results.

## ↑ Ancestors (15)

1. [Non Reuters ranges](non-reuters-ranges.md)
2. [Breakthroughs](breakthroughs.md)
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

## ← Incoming links (3)

- [Breakthroughs](breakthroughs.md)
- [CGI comms](cgi-comms.md)
- [DNS Census 2013](dns-census-2013.md)
