# Hits without nearby IP hits

↑ **Parent:** [IP range search](ip-range-search.md)  
🏷️ **Tags:** [TODO](todo.md)

Here we list of suspected domains for which the correct IP was apparently not found since there are no neighbouring hits.

These are suspicious, and suggest either that we didn't obtain the correct reverse IP, or a change in CIA methodology from an older time at which they were not yet using the obscene IP ranges.

For example, in the case of inews-today.com, [2013 DNS Census](dns-census-2013.md) gave one IP 193.203.49.212, but then [viewdns.info](viewdns-info.md) gave another one 66.175.106.146 which fit into an existing IP range, and which assumed to be the correct IP of interest.

A similar case happened when we found IP 212.209.74.126 for headlines2day.com with [dnshistory.org](dnshistory-org.md): [https://dnshistory.org/historical-dns-records/a/headlines2day.com.](https://dnshistory.org/historical-dns-records/a/headlines2day.com.)

It is also possible that some of them are simply false positives so they should be taken with a grain of salt. Further reverse engineering e.g. of [comms](communication-mechanism.md) or [HTML analysis](html-analysis.md) might be able to exclude some of them.

It is interesting to note that Reuters seems to have featured disproportionately many hits from that range, one wonders why that happened. It is possible that they chose these because they actually didn't have any nearby hits to give away less obvious information, though they did pick some from the ranges as wel.

In what follows we list the domains with possible reverse IPs and what was explored so far for each. We consider IPs not in a range to be uncertain, and that instead their domains might have been previously in a range which we

dailynewsandsports.com. Found with: [2013 DNS Census virtual host cleanup heuristic keyword searches](2013-dns-census-virtual-host-cleanup-heuristic-keyword-searches.md)
- 216.119.129.94. rdns source: [viewdns.info](viewdns-info.md) "location": "United States", "owner": "A2 Hosting, Inc.", "lastseen": "2012-04-13". Tested viewdns.info range: 216.119.129.85 - 216.119.129.86, 216.119.129.89 - 216.119.129.99, ran out of queries for 87 and 88
  - 216.119.129.90: eastdairies.com 2011-04-04. Promising name and date, but no archives alas.
  - 216.119.129.97: miideaco.com 2016-02-01
- 216.119.129.114 Found with: [2013 DNS Census virtual host cleanup heuristic keyword searches](2013-dns-census-virtual-host-cleanup-heuristic-keyword-searches.md), also present on viewdns.info but at a later date from previous "location": "United States", "owner": "A2 Hosting, Inc.", "lastseen": "2013-11-29". Tested viewdns.info range: 216.119.129.109 - 216.119.129.119
  - 216.119.129.110: dommoejmechty.com.ua. Legit.
  - 216.119.129.111: dailybeatz.com: Legit
  - 216.119.129.113:
    - audreygeneve.com
    - reyzheng.com
    - jacintorey.com
  - 216.119.129.114: dailynewsandsports.com. hit.
  - 216.119.129.115: afxchange.com legit/broken
  - 216.119.129.116: danafunkfinancial.com: legit
- 208.73.33.194 on [securitytrails.com](securitytrails-com.md)
  - 69.64.155.77 Amazon.com, Inc. 2008-12-10 (16 years)	2008-12-19 (16 years)	9 days
  - 68.178.232.100 GoDaddy.com, LLC 2008-10-04 (16 years)	2008-11-02 (16 years)	29 days
  - 208.73.33.194 Jumpline Inc 2008-09-01 (17 years)	2008-10-03 (16 years)	1 month

iranfootballsource.com:
- 34.98.99.30	Kansas City - United States	Google LLC	2021-05-24
- 184.168.221.94	United States	GoDaddy.com	2020-07-21
- 50.63.202.66	United States	GoDaddy.com	2020-07-07
- 50.63.202.86	United States	GoDaddy.com	2020-05-28
- 184.168.221.94	United States	GoDaddy.com	2020-05-13
- 50.63.202.74	United States	GoDaddy.com	2020-04-29
- 50.18.223.191	San Jose - United States	Amazon.com	2015-03-23. Sources: [2013 DNS Census](dns-census-2013.md) and [viewdns.info](viewdns-info.md)
  - no viewdns.info hits +- 10
- 85.13.200.108	United Kingdom	Coreix Dedicated Customer Allocation	2013-06-30. Source: [viewdns.info](viewdns-info.md)
  - 85.13.200.108: 1000 hits, so unlikely to be the one

iraniangoalkicks.com:
- 68.178.232.100: treverse IP source: [viewdns.info](viewdns-info.md). see rastadirect.net.
- 208.71.138.130 2010-02-22 -\> 2010-08-06, QWK.net Hosting, L.L.C.. source: [https://dnshistory.org/historical-dns-records/a/iraniangoalkicks.com.](https://dnshistory.org/historical-dns-records/a/iraniangoalkicks.com.) Large shared hosting domain, no good nearby hits, several legit sites.
- [https://securitytrails.com/domain/iraniangoalkicks.com/history/a](https://securitytrails.com/domain/iraniangoalkicks.com/history/a) says:
  - 2011-03-31 68.178.232.100
  - 2008-09-01 208.71.138.130

iraniangoals.com:
- 68.178.232.100: see rastadirect.net
- 69.65.33.21 - Flushing - United States - GigeNET - 2011-09-08. Also at: [https://dnshistory.org/historical-dns-records/a/iraniangoals.com](https://dnshistory.org/historical-dns-records/a/iraniangoals.com) 2009-08-03 -\> 2011-01-12 69.65.33.21 [https://viewdns.info/reverseip/?t=1&host=69.65.33.21](https://viewdns.info/reverseip/?t=1&host=69.65.33.21) 80 virtual nothing pops to eye on quick read:
  - 69.65.33.2: onemincustomerservice.com. [https://web.archive.org/web/20091015044922/http://www.onemincustomerservice.com/](https://web.archive.org/web/20091015044922/http://www.onemincustomerservice.com/). Doesn't feel like a hit. [http://cqcounter.com/whois/www/onemincustomerservice.com.html](http://cqcounter.com/whois/www/onemincustomerservice.com.html) error
  - 69.65.33.5: 400+ domains
  - 69.65.33.6: 4 domains but recent resolutions only
  - similar status for everything else withing +-20. A couple of domains, no easy hits
- [https://securitytrails.com/domain/iraniangoals.com/history/a](https://securitytrails.com/domain/iraniangoals.com/history/a) same from 2008-09-17

football-enthusiast.com:
- 212.4.18.14: Tested viewdns.info range: 212.4.18.1 - 212.4.18.29. This is a curious case, rather close to 212.4.18.129 sightseeingnews.com, but not quite in the same range apparently. Viewdns.info also agrees on its history with only "212.4.18.14", "location" : "Milan - Italy", "owner" : "MCI Worldcom Italy Spa", "lastseen" : "2013-06-30" of interest.

cyhiraeth-intlnews.com:
- [https://dnshistory.org/historical-dns-records/a/cyhiraeth-intlnews.com](https://dnshistory.org/historical-dns-records/a/cyhiraeth-intlnews.com) 2009-07-31 -\> 2011-01-05 0.0.0.0 WTF?
- [https://viewdns.info/iphistory/?domain=cyhiraeth-intlnews.com](https://viewdns.info/iphistory/?domain=cyhiraeth-intlnews.com)
  - 68.178.232.100	United States	AS-26496-GO-DADDY-COM-LLC	2011-07-27 virtual
  - 0.0.0.0	Unknown	Unknown	2011-07-02. Hmm also the 0.0.0.0. Weird!

news-latina.com: [domainsbyproxy.com](../domains-by-proxy.md) 2007-12-17
- [https://dnshistory.org/historical-dns-records/a/news-latina.com](https://dnshistory.org/historical-dns-records/a/news-latina.com) 2010-03-11 -\> 2010-08-16 64.92.111.3. this has several hits for the same IP on [DNS Census 2013](dns-census-2013.md) which is unusual. Tested viewdns.info range: 64.92.111.1 - 64.92.111.13
  - 64.92.111.2 virtual
  - 64.92.111.3 virtual
- [https://viewdns.info/iphistory/?domain=news-latina.com](https://viewdns.info/iphistory/?domain=news-latina.com)
  - 68.178.232.100	United States	AS-26496-GO-DADDY-COM-LLC	2011-08-11 virtual
  - 64.92.111.3	United States	MASSIVE-NETWORKS	2011-07-27 mdeium virtual [https://viewdns.info/reverseip/?t=1&host=64.92.111.3](https://viewdns.info/reverseip/?t=1&host=64.92.111.3)
    - [https://web.archive.org/web/20110211133905/http://tipsypotpole.com/](https://web.archive.org/web/20110211133905/http://tipsypotpole.com/) off
    - [https://web.archive.org/web/20250000000000*/quantumhealing.com](https://web.archive.org/web/20250000000000*/quantumhealing.com) popular
    - [https://web.archive.org/web/20110202114353/http://outdoortradition.com/](https://web.archive.org/web/20110202114353/http://outdoortradition.com/) redirecting. [https://dawhois.com/www/outdoortradition.com.html](https://dawhois.com/www/outdoortradition.com.html) not found.
    - [https://web.archive.org/web/20250000000000*/gtinvestigations.com](https://web.archive.org/web/20250000000000*/gtinvestigations.com) popular
    - [https://web.archive.org/web/20250000000000*/dig-itmag.com](https://web.archive.org/web/20250000000000*/dig-itmag.com) big

europeannewsflash.com:
- [https://viewdns.info/iphistory/?domain=europeannewsflash.com](https://viewdns.info/iphistory/?domain=europeannewsflash.com)
  - 68.178.232.100	United States	AS-26496-GO-DADDY-COM-LLC	2011-10-09 virtual
  - 216.131.66.209	San Francisco - United States	STRTEC	2011-09-08. Tested viewdns.info range: 216.131.66.201 216.131.66.219
- [https://dnshistory.org/historical-dns-records/a/europeannewsflash.com](https://dnshistory.org/historical-dns-records/a/europeannewsflash.com) 2010-02-06 -\> 2010-08-02 216.131.66.209. Tested.

outlooknewscast.com:
- [https://dnshistory.org/historical-dns-records/a/outlooknewscast.com](https://dnshistory.org/historical-dns-records/a/outlooknewscast.com)
  - 2009-08-08 -\> 2011-02-11 74.53.159.130. Tested viewdns.info range: 74.53.159.120 - 74.53.159.140
    - 74.53.159.130: aeromedhistory.org 2014-11-29
    - 74.53.159.130: mariposahorticultural.com 2022-11-28
    - 74.53.159.130: thewritestuffresume.com 2011-04-04. Legit.
- [https://viewdns.info/iphistory/?domain=outlooknewscast.com](https://viewdns.info/iphistory/?domain=outlooknewscast.com)
  - 204.93.178.121	Chicago - United States	SERVERCENTRAL	2011-09-08. Tested viewdns.info range: 204.93.178.111 - 204.93.178.131. Skimmed through, nothing of great interest.
  - 74.53.159.130	United States	SOFTLAYER	2011-04-04. Tested.

24hoursprimenews.com:
- [https://dnshistory.org/historical-dns-records/a/24hoursprimenews.com](https://dnshistory.org/historical-dns-records/a/24hoursprimenews.com) 2009-12-14 -\> 2011-10-04 216.9.68.24. Mid virtual: [https://viewdns.info/reverseip/?t=1&host=216.9.68.24](https://viewdns.info/reverseip/?t=1&host=216.9.68.24) had a quick look but no hits:
  - [https://web.archive.org/web/20110208211446/http://mynews-togo.com/](https://web.archive.org/web/20110208211446/http://mynews-togo.com/) invalid page. [https://dawhois.com/www/mynews-togo.com.html](https://dawhois.com/www/mynews-togo.com.html) same.
  - [https://web.archive.org/web/20110207202025/http://nefiexpo.com/](https://web.archive.org/web/20110207202025/http://nefiexpo.com/)
- [https://viewdns.info/iphistory/?domain=24hoursprimenews.com](https://viewdns.info/iphistory/?domain=24hoursprimenews.com) 216.9.68.24	United States	VONAGE-BUSINESS	2012-01-11. Tested.
- [https://securitytrails.com/domain/24hoursprimenews.com/history/a](https://securitytrails.com/domain/24hoursprimenews.com/history/a) same

farsi-newsandweather.com:
- [https://dnshistory.org/historical-dns-records/a/farsi-newsandweather.com](https://dnshistory.org/historical-dns-records/a/farsi-newsandweather.com) 2010-02-07 -\> 2010-08-03 69.49.101.19. Tested viewdns.info range: 69.49.101.9 - 69.49.101.19
- [https://viewdns.info/iphistory/?domain=farsi-newsandweather.com](https://viewdns.info/iphistory/?domain=farsi-newsandweather.com)
  - 68.178.232.100	United States	AS-26496-GO-DADDY-COM-LLC	2012-01-11 virtual
  - 69.49.101.19	Canada	INFB-AS	2011-11-13. Tested.

global-view-news.com:
- [https://dnshistory.org/historical-dns-records/a/global-view-news.com](https://dnshistory.org/historical-dns-records/a/global-view-news.com) 2010-02-13 -\> 2010-08-04 67.220.228.130. Tested viewdns.info range: 67.220.228.120 - 67.220.228.160:
  - 67.220.228.150: investfromhome.co.uk 2011-09-05. No archives.
- [https://viewdns.info/iphistory/?domain=global-view-news.com](https://viewdns.info/iphistory/?domain=global-view-news.com)
  - 68.178.232.100	United States	AS-26496-GO-DADDY-COM-LLC	2012-01-11 virtual
  - 69.90.161.195	Canada	COGECO-PEER1	2011-09-08. Unknown. Tested viewdns.info range: 69.90.161.185 69.90.161.205. Some virtual misses. [https://viewdns.info/reverseip/?t=1&host=69.90.161.195](https://viewdns.info/reverseip/?t=1&host=69.90.161.195) medium virtual, canada.

health-men-today.com:
- [https://dnshistory.org/historical-dns-records/a/health-men-today.com](https://dnshistory.org/historical-dns-records/a/health-men-today.com)
  - 2011-01-07 -\> 2011-01-07 69.90.162.165. Tested viewdns.info range: 69.90.162.155 - 69.90.162.175. Virtuals.
  - 2009-11-30 -\> 2010-05-27 67.220.228.224. New range with global-view-news.com? Tested viewdns.info range: 67.220.228.214 67.220.228.234
    - 67.220.228.223: stagedwithdistinction.com 2011-10-09. One archive of godaddy only.
  - 2009-08-01 -\> 2009-09-19 69.42.58.50. Tested viewdns.info range: 69.42.58.40 - 69.42.58.60. Virtuals, canada.
- [https://viewdns.info/iphistory/?domain=health-men-today.com](https://viewdns.info/iphistory/?domain=health-men-today.com)
  - 204.11.56.19	British Virgin Islands	CONFLUENCE-NETWORK-INC	2014-04-19. Virtuals.
  - 208.91.197.19	British Virgin Islands	CONFLUENCE-NETWORK-INC	2013-05-20. Unknown range.
  - 69.90.162.165	Canada	COGECO-PEER1	2012-06-29. Tested.
- [https://securitytrails.com/domain/health-men-today.com/history/a](https://securitytrails.com/domain/health-men-today.com/history/a)
  - 69.42.58.50 Aptum Technologies 2008-09-01 (17 years)	2008-09-04 (17 years)	3 days

firstnewssource.com:
- [https://dnshistory.org/historical-dns-records/a/firstnewssource.com](https://dnshistory.org/historical-dns-records/a/firstnewssource.com)
  - 2010-02-09 -\> 2010-02-09 67.220.228.150 TODO new range with global-view-news.com? Tested.
  - 2010-08-03 -\> 2010-08-03 69.90.162.70  TODO new range with global-view-news.com?

pars-technews.com:
- [https://dnshistory.org/historical-dns-records/a/pars-technews.com](https://dnshistory.org/historical-dns-records/a/pars-technews.com) 2009-08-08 -\> 2011-02-13 74.220.219.104 Tested viewdns.info range: 74.220.219.94 74.220.219.114. [https://viewdns.info/reverseip/?t=1&host=74.220.219.104](https://viewdns.info/reverseip/?t=1&host=74.220.219.104) medium virtual haven't bothered much.
- [https://viewdns.info/iphistory/?domain=pars-technews.com](https://viewdns.info/iphistory/?domain=pars-technews.com) 74.220.219.104	United States	UNIFIEDLAYER-AS-1	2012-11-12. Tested.

newdaynewsonline.com:
- [https://dnshistory.org/historical-dns-records/a/newdaynewsonline.com](https://dnshistory.org/historical-dns-records/a/newdaynewsonline.com) 2010-03-10 -\> 2010-08-15 76.163.54.16. Tested viewdns.info range: 76.163.54.6 76.163.54.26. [https://viewdns.info/reverseip/?t=1&host=76.163.54.16](https://viewdns.info/reverseip/?t=1&host=76.163.54.16) empty.
  - 76.163.54.23: leewoodwork.com 2014-07-05
- [https://viewdns.info/iphistory/?domain=newdaynewsonline.com](https://viewdns.info/iphistory/?domain=newdaynewsonline.com)
  - 74.91.154.56	United States	INTERNAP-BLOCK-4	2012-11-12 unknown range. Tested viewdns.info range: 74.91.154.46 74.91.154.66
    - 74.91.154.61: benefitsla.com 2013-04-21. Legit.
  - 76.163.54.16	United States	WINDSTREAM	2011-09-08 unknown range. Tested.

sportsnewsfinder.com:
- [https://dnshistory.org/historical-dns-records/a/sportsnewsfinder.com](https://dnshistory.org/historical-dns-records/a/sportsnewsfinder.com) 2009-08-11 -\> 2011-02-24 66.113.196.128. Tested viewdns.info range: 66.113.196.118 66.113.196.138. [https://viewdns.info/reverseip/?t=1&host=66.113.196.128](https://viewdns.info/reverseip/?t=1&host=66.113.196.128) empty.
- [https://viewdns.info/iphistory/?domain=sportsnewsfinder.com](https://viewdns.info/iphistory/?domain=sportsnewsfinder.com)
  - 50.63.202.58	United States	AS-26496-GO-DADDY-COM-LLC	2013-03-23 some similar hits on other sites, possibly all flukes
  - 207.150.219.159	United States	AFFINITY-INTER	2013-03-02
  - 66.113.196.128	United States	NETNATION	2012-01-11. Tested.

newsworldsite.com:
- [https://viewdns.info/iphistory/?domain=newsworldsite.com](https://viewdns.info/iphistory/?domain=newsworldsite.com)
  - 68.178.232.100	United States	AS-26496-GO-DADDY-COM-LLC	2013-05-20 big virtual
  - 204.93.159.80	Chicago - United States	SERVERCENTRAL	2013-04-21. Tested viewdns.info range: 204.93.159.70 204.93.159.90. [https://viewdns.info/reverseip/?t=1&host=204.93.159.80](https://viewdns.info/reverseip/?t=1&host=204.93.159.80) medium virtual.
    - 204.93.159.84: team-merk.com 2011-08-11. No archives.

todaysnewsreports.net:
- [https://viewdns.info/iphistory/?domain=todaysnewsreports.net](https://viewdns.info/iphistory/?domain=todaysnewsreports.net)
  - 208.91.197.132	British Virgin Islands	CONFLUENCE-NETWORK-INC	2013-07-01
  - 205.178.189.129	United States	NETWORK-SOLUTIONS-HOSTING	2013-05-20 likely virtual
  - 173.255.131.72	Reno - United States	UK-2 Limited	2012-08-27. Tested viewdns.info range: 173.255.131.62 173.255.131.82. Virtual and modern hits only.
  - 67.213.211.232	United States	UK-2 Limited	2011-09-07 unknown. Tested viewdns.info range: 67.213.211.222 67.213.211.242. [https://viewdns.info/reverseip/?t=1&host=67.213.211.232](https://viewdns.info/reverseip/?t=1&host=67.213.211.232) empty.
    - 67.213.211.236: icf-finan.com 2015-01-20
    - 67.213.211.237: playinside.me 2016-02-04. Nice domain hack, but no.
    - 67.213.211.239: reality-sexxx.com 2011-09-08

hassannews.net:
- [https://viewdns.info/iphistory/?domain=hassannews.net](https://viewdns.info/iphistory/?domain=hassannews.net)
  - 208.91.197.132	British Virgin Islands	CONFLUENCE-NETWORK-INC	2013-07-08
  - 205.178.189.131	United States	NETWORK-SOLUTIONS-HOSTING	2013-07-01. Likely virtual.

todayoutdoors.com:
- [https://dnshistory.org/historical-dns-records/a/todayoutdoors.com](https://dnshistory.org/historical-dns-records/a/todayoutdoors.com)
  - 2009-08-11 -\> 2010-07-07 174.133.44.90. Tested viewdns.info range: 174.133.44.80 174.133.44.100. Virtual and modern. [https://viewdns.info/reverseip/?t=1&host=174.133.44.90](https://viewdns.info/reverseip/?t=1&host=174.133.44.90) two modern domains.
  - 2011-03-01 -\> 2011-03-01 174.123.172.82 unknown. Tested viewdns.info range: 174.123.172.72 174.123.172.92. Virtuals.
- [https://viewdns.info/iphistory/?domain=todayoutdoors.com](https://viewdns.info/iphistory/?domain=todayoutdoors.com)
  - 68.178.232.100	United States	AS-26496-GO-DADDY-COM-LLC	2011-07-02 virtual
  - 174.123.172.82	United States	SOFTLAYER	2011-04-04. Tested.

globaltourist.net:
- [https://dnshistory.org/historical-dns-records/a/](https://dnshistory.org/historical-dns-records/a/) 2009-07-30 -\> 2011-01-01 69.59.20.215 unknown. Tested viewdns.info range: 69.59.20.205 69.59.20.225. Virtuals.
- [https://viewdns.info/iphistory/?domain=globaltourist.net](https://viewdns.info/iphistory/?domain=globaltourist.net)
  - 216.172.170.14	United States	NETWORK-SOLUTIONS-HOSTING	2013-07-08
  - 216.21.239.197	United States	NETWORK-SOLUTIONS-HOSTING	2012-06-25
  - 68.178.232.100	United States	AS-26496-GO-DADDY-COM-LLC	2012-04-09 big virtual
  - 174.136.34.154	United States	IHNET	2012-03-12 unknown. Tested viewdns.info range: 174.136.34.144 174.136.34.164
  - 74.119.145.101	Frankfurt am Main - Germany	PERFORMIVE	2011-09-07. Tested viewdns.info range: 74.119.145.91 74.119.145.111. One virtual.
  - 69.59.20.215	United States	ATLRETAIL	2011-06-22. Tested [https://viewdns.info/reverseip/?t=1&host=69.59.20.215](https://viewdns.info/reverseip/?t=1&host=69.59.20.215)
    - [https://web.archive.org/web/20080521063605/http://piasawine.com/](https://web.archive.org/web/20080521063605/http://piasawine.com/) index of

terrain-news.com:
- [JAR](https://web.archive.org/web/20110202060511/http://terrain-news.com/internetspeed.jar)
- [https://viewdns.info/iphistory/?domain=terrain-news.com](https://viewdns.info/iphistory/?domain=terrain-news.com) None in simple ranges.
  - 204.11.56.25	British Virgin Islands	CONFLUENCE-NETWORK-INC	2013-11-08. Virtuals.
  - 208.91.197.19	British Virgin Islands	CONFLUENCE-NETWORK-INC	2013-05-20. Virtual 167. [https://viewdns.info/reverseip/?host=208.91.197.19&t=1](https://viewdns.info/reverseip/?host=208.91.197.19&t=1) not very promising.
    - eurotravelnyc.com legit [https://web.archive.org/web/20110201195411/http://eurotravelnyc.com/](https://web.archive.org/web/20110201195411/http://eurotravelnyc.com/)
  - 208.187.167.20	United States	DATANOC	2012-01-11. Tested viewdns.info range: 208.187.167.10 208.187.167.30. Newer domains. [https://viewdns.info/reverseip/?t=1&host=208.187.167.20](https://viewdns.info/reverseip/?t=1&host=208.187.167.20) only has one conck.ooo. WTF.
- [https://securitytrails.com/domain/terrain-news.com/history/a](https://securitytrails.com/domain/terrain-news.com/history/a) same:
  - 208.91.197.19 Confluence Networks Inc 2012-05-12 (13 years)	2012-05-31 (13 years)	19 days
  - 208.187.167.20 Lanset America Corporation 2008-11-12 (16 years)	2009-12-09 (15 years)	1 year

intlnewsdaily.com
- [https://dnshistory.org/historical-dns-records/a/intlnewsdaily.com](https://dnshistory.org/historical-dns-records/a/intlnewsdaily.com) 2010-02-21 -\> 2010-08-06 75.126.136.179. unknown range. [https://viewdns.info/reverseip/?t=1&host=75.126.136.179](https://viewdns.info/reverseip/?t=1&host=75.126.136.179) empty checked 75.126.136.171 - 75.126.136.179
- [https://viewdns.info/iphistory/?domain=intlnewsdaily.com](https://viewdns.info/iphistory/?domain=intlnewsdaily.com)
  - 208.91.197.19	British Virgin Islands	CONFLUENCE-NETWORK-INC	2013-05-20. Virtual. Tested.
  - 63.247.95.50	Austell - United States	NTHL	2012-06-29 unknown. Tested viewdns.info range: 63.247.95.40 63.247.95.60
    - 63.247.95.50: 2b-sports.com 2013-04-21
    - 63.247.95.50: caldentalinsurance.com 2014-07-05
    - 63.247.95.50: cameronbal-photography.com 2012-06-29
    - 63.247.95.50: congbetham.com 2014-07-05
    - 63.247.95.50: essentialintelligenceagency.com 2023-03-07
    - 63.247.95.50: isabellavalentina.com 2014-07-05
    - 63.247.95.50: jhraccounting.com.au 2021-05-03
    - 63.247.95.50: missouribreaks294.com 2012-06-29
    - 63.247.95.50: startorganize.com 2011-08-11
    - 63.247.95.50: tifocus.net 2011-08-11
    - 63.247.95.50: tifocus.org 2011-08-10
    - 63.247.95.50: whitepartyorlando.com 2012-01-11
  - 204.11.56.25 ([ipinf.ru](ipinf-ru.md)) [https://viewdns.info/reverseip/?t=1&host=204.11.56.25](https://viewdns.info/reverseip/?t=1&host=204.11.56.25) Virtual 2,999
- [https://securitytrails.com/domain/intlnewsdaily.com/history/a](https://securitytrails.com/domain/intlnewsdaily.com/history/a) empty on dates

opensourcenewstoday.com:
- [https://viewdns.info/iphistory/?domain=opensourcenewstoday.com](https://viewdns.info/iphistory/?domain=opensourcenewstoday.com)
  - 68.178.232.100	United States	AS-26496-GO-DADDY-COM-LLC	2011-11-13 virtual
  - 64.16.193.48	Riyadh - Saudi Arabia	Saudi Telecom Company JSC	2011-09-08. Tested viewdns.info range: 64.16.193.38 64.16.193.55. Ran out. [https://viewdns.info/reverseip/?t=1&host=64.16.193.48](https://viewdns.info/reverseip/?t=1&host=64.16.193.48) virtual 55, lots of porn
- [https://securitytrails.com/domain/opensourcenewstoday.com/history/a](https://securitytrails.com/domain/opensourcenewstoday.com/history/a)
  - 64.16.193.48 Saudi Telecom Company JSC 2010-05-04 (15 years)	2010-05-20 (15 years)	16 days

techwatchtoday.com:
- [https://viewdns.info/iphistory/?domain=techwatchtoday.com](https://viewdns.info/iphistory/?domain=techwatchtoday.com)
  - 208.91.197.132	British Virgin Islands	CONFLUENCE-NETWORK-INC	2013-11-29 virtual
  - 66.11.225.226	United States	TNWEB-LEW-001	2012-01-11 unknown. Checked 66.11.225.220 - 66.11.225.233
    - [https://viewdns.info/reverseip/?t=1&host=66.11.225.223](https://viewdns.info/reverseip/?t=1&host=66.11.225.223)
      - [https://web.archive.org/web/20110201142759/http://usdconnection.com/](https://web.archive.org/web/20110201142759/http://usdconnection.com/) broken
    - [https://viewdns.info/reverseip/?t=1&host=66.11.225.226](https://viewdns.info/reverseip/?t=1&host=66.11.225.226) has [https://web.archive.org/web/20100201000000*/tsgardens.com](https://web.archive.org/web/20100201000000*/tsgardens.com) No archives. [http://cqcounter.com/whois/www/tsgardens.com.html](http://cqcounter.com/whois/www/tsgardens.com.html) empty.
    - [https://viewdns.info/reverseip/?t=1&host=66.11.225.227](https://viewdns.info/reverseip/?t=1&host=66.11.225.227)
      - [https://web.archive.org/web/20110108222333/http://inhospitality.net/](https://web.archive.org/web/20110108222333/http://inhospitality.net/) off
- [https://dnshistory.org/historical-dns-records/a/techwatchtoday.com](https://dnshistory.org/historical-dns-records/a/techwatchtoday.com) 2009-08-11 -\> 2011-02-26 66.11.225.226 big shared host
- [https://securitytrails.com/domain/techwatchtoday.com/history/a](https://securitytrails.com/domain/techwatchtoday.com/history/a) same
  - 66.11.225.226 TNWEB LLC 2008-11-04 (16 years)	2009-04-10 (16 years)	5 months

**Table of contents**

- [Possible hits](possible-hits.md)

## ↑ Ancestors (14)

1. [IP range search](ip-range-search.md)
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

## ← Incoming links (2)

- [List of websites](list-of-websites.md)
- [Possible hits](possible-hits.md)
