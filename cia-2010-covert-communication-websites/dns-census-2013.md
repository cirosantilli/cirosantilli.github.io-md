# DNS Census 2013

↑ **Parent:** [Data sources](data-sources.md)

Main article: [DNS Census 2013](../dns-census-2013.md).

This data source was very valuable, and led to many hits, and to finding the first non Reuters ranges with [Section "secure subdomain search on 2013 DNS Census"](secure-subdomain-search-on-2013-dns-census.md).

Hit overlap:
```
jq -r '.[].host' ../media/cia-2010-covert-communication-websites/hits.json ) | xargs -I{} sqlite3 aiddcu.sqlite "select * from t where d = '{}'"
```
Domain hit count when we were at 279 hits: 142 hits, so about half of the hits were present.

The timing of the database is perfect for this project, it is as if the CIA had planted it themselves!

**Table of contents**

- [2013 DNS Census virtual host cleanup](2013-dns-census-virtual-host-cleanup.md)
  - [2013 DNS Census virtual host cleanup heuristic keyword searches](2013-dns-census-virtual-host-cleanup-heuristic-keyword-searches.md)
- [2013 DNS census MX records](2013-dns-census-mx-records.md)
- [2013 DNS census secureserver.net MX records intersection 2013 DNS Census virtual host cleanup](2013-dns-census-secureserver-net-mx-records-intersection-2013-dns-census-virtual-host-cleanup.md)
- [2013 DNS census NS records](2013-dns-census-ns-records.md)
- [2013 DNS census SOA records](2013-dns-census-soa-records.md)

## ↑ Ancestors (14)

1. [Data sources](data-sources.md)
2. [Methodology](methodology.md)
3. [CIA 2010 covert communication websites](../cia-2010-covert-communication-websites-split.md)
4. [Central Intelligence Agency](../central-intelligence-agency.md)
5. [American intelligence agency](../american-intelligence-agency.md)
6. [United States Intelligence Community](../united-states-intelligence-community.md)
7. [Intelligence community](../intelligence-community.md)
8. [Secret service](../secret-service.md)
9. [Espionage](../espionage.md)
10. [War](../war.md)
11. [Social science](../social-science.md)
12. [Scientific method](../scientific-method.md)
13. [Science](../science-split.md)
14. [Ciro Santilli's Homepage](../split.md)

## ← Incoming links (4)

- [Backlinks](backlinks.md)
- [Hits with nearby IP hits](hits-with-nearby-ip-hits.md)
- [Hits without nearby IP hits](hits-without-nearby-ip-hits.md)
- [Overview of Ciro Santilli's investigation](overview-of-ciro-santilli-s-investigation.md)
