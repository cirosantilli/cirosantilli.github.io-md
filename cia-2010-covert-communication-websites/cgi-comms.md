# CGI comms

↑ **Parent:** [Communication mechanism](communication-mechanism.md)

We've come across a few shallow and stylistically similar websites on suspicious ranges with this pattern.

No JS/JAR/SWF comms, but rather a subdomain, and an HTTPS page with .cgi extension that leads to a login page. Some names seen for this subdomain:
- `secure.`: most common
- `ssl.`: also common
- various other more creative ones linked to the website theme itself, e.g.:
  - musical-fortune.net has a backstage.musical-fortune.net

The question is, is this part of some legitimate tooling that created such patterns? And if so which? Or are they actual hits with a new comms mechanism not previously seen?

The fact that:
- hits of this type are so dense in the suspicious ranges
- they are so stylistically similar between on another
- citizenlabs specifically mentioned a "CGI" comms method
suggests to Ciro that they are an actual hit.

In particular, the `secure` and `ssl` ones are overused, and together with some heuristics allowed us to find our first two non Reuters ranges! [Section "secure subdomain search on 2013 DNS Census"](secure-subdomain-search-on-2013-dns-census.md)

Some currently known URLs
- [https://backstage.musical-fortune.net/cgi-bin/backstage.cgi](https://backstage.musical-fortune.net/cgi-bin/backstage.cgi)
- [https://clients.smart-travel-consultant.com/cgi-bin/clients.cgi](https://clients.smart-travel-consultant.com/cgi-bin/clients.cgi)
- [https://members.it-proonline.com/cgi-bin/members.cgi](https://members.it-proonline.com/cgi-bin/members.cgi)
- [https://members.metanewsdaily.com/cgi-bin/ABC.cgi](https://members.metanewsdaily.com/cgi-bin/ABC.cgi)
- [https://miembros.todosperuahora.com/cgi-bin/business.cgi](https://miembros.todosperuahora.com/cgi-bin/business.cgi)
- [https://secure.altworldnews.com/cgi-bin/desk.cgi](https://secure.altworldnews.com/cgi-bin/desk.cgi)
- [https://secure.driversinternationalgolf.com/cgi-bin/drivers.cgi](https://secure.driversinternationalgolf.com/cgi-bin/drivers.cgi)
- [https://secure.freshtechonline.com/cgi-bin/tech.cgi](https://secure.freshtechonline.com/cgi-bin/tech.cgi)
- [https://secure.globalnewsbulletin.com/cgi-bin/index.cgi](https://secure.globalnewsbulletin.com/cgi-bin/index.cgi)
- [https://secure.negativeaperture.com/cgi-bin/canon.cgi](https://secure.negativeaperture.com/cgi-bin/canon.cgi)
- [https://secure.riskandrewardnews.com/cgi-bin/worldwide.cgi](https://secure.riskandrewardnews.com/cgi-bin/worldwide.cgi)
- [https://secure.theworld-news.net/cgi-bin/news.cgi](https://secure.theworld-news.net/cgi-bin/news.cgi)
- [https://secure.topbillingsite.com/cgi-bin/main.cgi](https://secure.topbillingsite.com/cgi-bin/main.cgi)
- [https://secure.worldnewsandent.com/cgi-bin/news.cgi](https://secure.worldnewsandent.com/cgi-bin/news.cgi)
- [https://ssl.beyondnetworknews.com/cgi-bin/local.cgi](https://ssl.beyondnetworknews.com/cgi-bin/local.cgi)
- [https://ssl.newtechfrontier.com/cgi-bin/tech.cgi](https://ssl.newtechfrontier.com/cgi-bin/tech.cgi)
- [https://www.businessexchangetoday.com/cgi-bin/business.cgi](https://www.businessexchangetoday.com/cgi-bin/business.cgi)
- [https://heal.conquermstoday.com](https://heal.conquermstoday.com) (path unknown)
If we could do a crawl search for `secure.*com/cgi-bin/*.cgi` that might be a good enough fingerprint, maybe even `*.*com/cgi-bin/*.cgi`. Edit: it is not perfect, but we kind of did it: [Section "secure subdomain search on 2013 DNS Census"](secure-subdomain-search-on-2013-dns-census.md).

**Table of contents**

- [CGI comms variant](cgi-comms-variant.md)
- [SSL certificate](ssl-certificate.md)

## ↑ Ancestors (15)

1. [Communication mechanism](communication-mechanism.md)
2. [Reverse engineering](reverse-engineering.md)
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

## ← Incoming links (9)

- [2013 DNS Census virtual host cleanup](2013-dns-census-virtual-host-cleanup.md)
- [Breakthroughs](breakthroughs.md)
- [Common Crawl](common-crawl.md)
- [Communication mechanism](communication-mechanism.md)
- [Hits with nearby IP hits](hits-with-nearby-ip-hits.md)
- [List of websites](list-of-websites.md)
- [Secure subdomain search on 2013 DNS Census](secure-subdomain-search-on-2013-dns-census.md)
- [SSL certificate](ssl-certificate.md)
- [The Reuters websites](the-reuters-websites.md)
