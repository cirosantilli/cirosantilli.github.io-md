# Historical WHOIS database

↑ **Parent:** [DNS database](dns-database.md)

Bibliography:
- [https://www.reddit.com/r/Domains/comments/1g07b7b/whois_history_on_url/](https://www.reddit.com/r/Domains/comments/1g07b7b/whois_history_on_url/)

A "[DNS database](dns-database.md)" is a database that stores DNS records, notably A-records, which IP a domains is hosted at.

For currently live domains, domain to IP can of course be easily determined on the fly by just resolving the domain like the browser does, e.g. 
```
cirosantilli.com
```

What is hard however is:
- the other way around is harder however: given an IP, list all domains that it hosts. This is known as "reverse IP" searching.
- historic data, i.e. what was the IP for a given domain at a given date and vice versa

As of 2023, working with DNS data is just going through a mish-mash of closed datasets/expensive APIs.

We really need some open data in that area.
- [https://opendata.stackexchange.com/questions/1951/dataset-of-domain-names](https://opendata.stackexchange.com/questions/1951/dataset-of-domain-names)
- [https://opendata.stackexchange.com/questions/2110/domain-name-system-record-a-database](https://opendata.stackexchange.com/questions/2110/domain-name-system-record-a-database)
- [https://webmasters.stackexchange.com/questions/33395/find-the-ip-address-of-expired-domains/142751#142751](https://webmasters.stackexchange.com/questions/33395/find-the-ip-address-of-expired-domains/142751#142751)
- [https://superuser.com/questions/686195/how-to-find-the-last-ip-used-for-an-expired-domain-name/1793224#1793224](https://superuser.com/questions/686195/how-to-find-the-last-ip-used-for-an-expired-domain-name/1793224#1793224)

Some links of interest:
- [https://bushart.org/topic/ip](https://bushart.org/topic/ip)
- [https://archive.org/details/internet-mapping](https://archive.org/details/internet-mapping)
- [https://stackoverflow.com/questions/307553/possible-to-download-entire-whois-database-list-of-registered-domains](https://stackoverflow.com/questions/307553/possible-to-download-entire-whois-database-list-of-registered-domains) (deleted question, see archives)
- [https://www.reversedns.ch/en/](https://www.reversedns.ch/en/) has some OK reverse IPs, but you have to do them one by one with CAPTCHA, and we were already past that point when that source was found, so nothing new was found on it yet
- [https://iphistory.net/](https://iphistory.net/) announced at [https://www.reddit.com/r/OSINT/comments/1bip8j7/iphistorynet_find_historic_ip_addresses_from/](https://www.reddit.com/r/OSINT/comments/1bip8j7/iphistorynet_find_historic_ip_addresses_from/)

Bibliography:
- [https://www.reddit.com/r/OSINT/comments/1j8uasm/does_domaintools_offer_historical_reverse_ip_ie/](https://www.reddit.com/r/OSINT/comments/1j8uasm/does_domaintools_offer_historical_reverse_ip_ie/) by [Ciro Santilli](ciro-santilli-split.md)
- [https://www.reddit.com/r/OSINT/comments/ne27qi/really_historical_whois/](https://www.reddit.com/r/OSINT/comments/ne27qi/really_historical_whois/)
- [https://www.reddit.com/r/dns/comments/1f4y0mg/any_onestopshop_type_sites_that_are_better_for/](https://www.reddit.com/r/dns/comments/1f4y0mg/any_onestopshop_type_sites_that_are_better_for/)
- [https://www.arin.net/reference/research/whowas/](https://www.arin.net/reference/research/whowas/) you need to request access and they need to approve your usage. Bastards.

## ↑ Ancestors (10)

1. [DNS database](dns-database.md)
2. [Domain Name System](domain-name-system.md)
3. [Internet protocol suite](internet-protocol-suite.md)
4. [Internet](internet.md)
5. [Computer network](computer-network.md)
6. [Computer](computer-split.md)
7. [Information technology](information-technology.md)
8. [Area of technology](area-of-technology.md)
9. [Technology](technology-split.md)
10. [Ciro Santilli's Homepage](split.md)
