# Hits without nearby IP hits

↑ **Parent:** [IP range search](ip-range-search.md)  
🏷️ **Tags:** [TODO](todo.md)

<a id="_4711"></a>
Here we list of suspected domains for which the correct IP was apparently not found since there are no neighbouring hits.

<a id="_4712"></a>
These are suspicious, and suggest either that we didn't obtain the correct reverse IP, or a change in CIA methodology from an older time at which they were not yet using the obscene IP ranges.

<a id="_4713"></a>
For example, in the case of inews-today.com, [2013 DNS Census](dns-census-2013.md) gave one IP 193.203.49.212, but then [viewdns.info](viewdns-info.md) gave another one 66.175.106.146 which fit into an existing IP range, and which assumed to be the correct IP of interest.

<a id="_4714"></a>
A similar case happened when we found IP 212.209.74.126 for headlines2day.com with [dnshistory.org](dnshistory-org.md): [https://dnshistory.org/historical-dns-records/a/headlines2day.com.](https://dnshistory.org/historical-dns-records/a/headlines2day.com.)

<a id="_4715"></a>
It is also possible that some of them are simply false positives so they should be taken with a grain of salt. Further reverse engineering e.g. of [comms](communication-mechanism.md) or [HTML analysis](html-analysis.md) might be able to exclude some of them.

<a id="_4716"></a>
It is interesting to note that Reuters seems to have featured disproportionately many hits from that range, one wonders why that happened. It is possible that they chose these because they actually didn't have any nearby hits to give away less obvious information, though they did pick some from the ranges as wel.

<a id="_4717"></a>
In what follows we list the domains with possible reverse IPs and what was explored so far for each. We consider IPs not in a range to be uncertain, and that instead their domains might have been previously in a range which we

<a id="_4718"></a>
dailynewsandsports.com. Found with: [2013 DNS Census virtual host cleanup heuristic keyword searches](2013-dns-census-virtual-host-cleanup-heuristic-keyword-searches.md)<a id="_4719"></a>

<a id="_4720"></a>
- 216.119.129.94. rdns source: [viewdns.info](viewdns-info.md) "location": "United States", "owner": "A2 Hosting, Inc.", "lastseen": "2012-04-13". Tested viewdns.info range: 216.119.129.85 - 216.119.129.86, 216.119.129.89 - 216.119.129.99, ran out of queries for 87 and 88<a id="_4721"></a>

  <a id="_4722"></a>
  - 216.119.129.90: eastdairies.com 2011-04-04. Promising name and date, but no archives alas.
  <a id="_4723"></a>
  - 216.119.129.97: miideaco.com 2016-02-01
<a id="_4724"></a>
- 216.119.129.114 Found with: [2013 DNS Census virtual host cleanup heuristic keyword searches](2013-dns-census-virtual-host-cleanup-heuristic-keyword-searches.md), also present on viewdns.info but at a later date from previous "location": "United States", "owner": "A2 Hosting, Inc.", "lastseen": "2013-11-29". Tested viewdns.info range: 216.119.129.109 - 216.119.129.119<a id="_4725"></a>

  <a id="_4726"></a>
  - 216.119.129.110: dommoejmechty.com.ua. Legit.
  <a id="_4727"></a>
  - 216.119.129.111: dailybeatz.com: Legit
  <a id="_4728"></a>
  - 216.119.129.113:<a id="_4729"></a>

    <a id="_4730"></a>
    - audreygeneve.com
    <a id="_4731"></a>
    - reyzheng.com
    <a id="_4732"></a>
    - jacintorey.com
  <a id="_4733"></a>
  - 216.119.129.114: dailynewsandsports.com. hit.
  <a id="_4734"></a>
  - 216.119.129.115: afxchange.com legit/broken
  <a id="_4735"></a>
  - 216.119.129.116: danafunkfinancial.com: legit
<a id="_4736"></a>
- 208.73.33.194 on [securitytrails.com](securitytrails-com.md)<a id="_4737"></a>

  <a id="_4738"></a>
  - 69.64.155.77 Amazon.com, Inc. 2008-12-10 (16 years)	2008-12-19 (16 years)	9 days
  <a id="_4739"></a>
  - 68.178.232.100 GoDaddy.com, LLC 2008-10-04 (16 years)	2008-11-02 (16 years)	29 days
  <a id="_4740"></a>
  - 208.73.33.194 Jumpline Inc 2008-09-01 (17 years)	2008-10-03 (16 years)	1 month

<a id="_4741"></a>
iranfootballsource.com:<a id="_4742"></a>

<a id="_4743"></a>
- 34.98.99.30	Kansas City - United States	Google LLC	2021-05-24
<a id="_4744"></a>
- 184.168.221.94	United States	GoDaddy.com	2020-07-21
<a id="_4745"></a>
- 50.63.202.66	United States	GoDaddy.com	2020-07-07
<a id="_4746"></a>
- 50.63.202.86	United States	GoDaddy.com	2020-05-28
<a id="_4747"></a>
- 184.168.221.94	United States	GoDaddy.com	2020-05-13
<a id="_4748"></a>
- 50.63.202.74	United States	GoDaddy.com	2020-04-29
<a id="_4749"></a>
- 50.18.223.191	San Jose - United States	Amazon.com	2015-03-23. Sources: [2013 DNS Census](dns-census-2013.md) and [viewdns.info](viewdns-info.md)<a id="_4750"></a>

  <a id="_4751"></a>
  - no viewdns.info hits +- 10
<a id="_4752"></a>
- 85.13.200.108	United Kingdom	Coreix Dedicated Customer Allocation	2013-06-30. Source: [viewdns.info](viewdns-info.md)<a id="_4753"></a>

  <a id="_4754"></a>
  - 85.13.200.108: 1000 hits, so unlikely to be the one

<a id="_4755"></a>
iraniangoalkicks.com:<a id="_4756"></a>

<a id="_4757"></a>
- 68.178.232.100: treverse IP source: [viewdns.info](viewdns-info.md). see rastadirect.net.
<a id="_4758"></a>
- 208.71.138.130 2010-02-22 -\> 2010-08-06, QWK.net Hosting, L.L.C.. source: [https://dnshistory.org/historical-dns-records/a/iraniangoalkicks.com.](https://dnshistory.org/historical-dns-records/a/iraniangoalkicks.com.) Large shared hosting domain, no good nearby hits, several legit sites.
<a id="_4759"></a>
- [https://securitytrails.com/domain/iraniangoalkicks.com/history/a](https://securitytrails.com/domain/iraniangoalkicks.com/history/a) says:<a id="_4760"></a>

  <a id="_4761"></a>
  - 2011-03-31 68.178.232.100
  <a id="_4762"></a>
  - 2008-09-01 208.71.138.130

<a id="_4763"></a>
iraniangoals.com:<a id="_4764"></a>

<a id="_4765"></a>
- 68.178.232.100: see rastadirect.net
<a id="_4766"></a>
- 69.65.33.21 - Flushing - United States - GigeNET - 2011-09-08. Also at: [https://dnshistory.org/historical-dns-records/a/iraniangoals.com](https://dnshistory.org/historical-dns-records/a/iraniangoals.com) 2009-08-03 -\> 2011-01-12 69.65.33.21 [https://viewdns.info/reverseip/?t=1&host=69.65.33.21](https://viewdns.info/reverseip/?t=1&host=69.65.33.21) 80 virtual nothing pops to eye on quick read:<a id="_4767"></a>

  <a id="_4768"></a>
  - 69.65.33.2: onemincustomerservice.com. [https://web.archive.org/web/20091015044922/http://www.onemincustomerservice.com/](https://web.archive.org/web/20091015044922/http://www.onemincustomerservice.com/). Doesn't feel like a hit. [http://cqcounter.com/whois/www/onemincustomerservice.com.html](http://cqcounter.com/whois/www/onemincustomerservice.com.html) error
  <a id="_4769"></a>
  - 69.65.33.5: 400+ domains
  <a id="_4770"></a>
  - 69.65.33.6: 4 domains but recent resolutions only
  <a id="_4771"></a>
  - similar status for everything else withing +-20. A couple of domains, no easy hits
<a id="_4772"></a>
- [https://securitytrails.com/domain/iraniangoals.com/history/a](https://securitytrails.com/domain/iraniangoals.com/history/a) same from 2008-09-17

<a id="_4773"></a>
football-enthusiast.com:<a id="_4774"></a>

<a id="_4775"></a>
- 212.4.18.14: Tested viewdns.info range: 212.4.18.1 - 212.4.18.29. This is a curious case, rather close to 212.4.18.129 sightseeingnews.com, but not quite in the same range apparently. Viewdns.info also agrees on its history with only "212.4.18.14", "location" : "Milan - Italy", "owner" : "MCI Worldcom Italy Spa", "lastseen" : "2013-06-30" of interest.

<a id="_4776"></a>
cyhiraeth-intlnews.com:<a id="_4777"></a>

<a id="_4778"></a>
- [https://dnshistory.org/historical-dns-records/a/cyhiraeth-intlnews.com](https://dnshistory.org/historical-dns-records/a/cyhiraeth-intlnews.com) 2009-07-31 -\> 2011-01-05 0.0.0.0 WTF?
<a id="_4779"></a>
- [https://viewdns.info/iphistory/?domain=cyhiraeth-intlnews.com](https://viewdns.info/iphistory/?domain=cyhiraeth-intlnews.com)<a id="_4780"></a>

  <a id="_4781"></a>
  - 68.178.232.100	United States	AS-26496-GO-DADDY-COM-LLC	2011-07-27 virtual
  <a id="_4782"></a>
  - 0.0.0.0	Unknown	Unknown	2011-07-02. Hmm also the 0.0.0.0. Weird!

<a id="_4783"></a>
news-latina.com: [domainsbyproxy.com](../domains-by-proxy.md) 2007-12-17<a id="_4784"></a>

<a id="_4785"></a>
- [https://dnshistory.org/historical-dns-records/a/news-latina.com](https://dnshistory.org/historical-dns-records/a/news-latina.com) 2010-03-11 -\> 2010-08-16 64.92.111.3. this has several hits for the same IP on [DNS Census 2013](dns-census-2013.md) which is unusual. Tested viewdns.info range: 64.92.111.1 - 64.92.111.13<a id="_4786"></a>

  <a id="_4787"></a>
  - 64.92.111.2 virtual
  <a id="_4788"></a>
  - 64.92.111.3 virtual
<a id="_4789"></a>
- [https://viewdns.info/iphistory/?domain=news-latina.com](https://viewdns.info/iphistory/?domain=news-latina.com)<a id="_4790"></a>

  <a id="_4791"></a>
  - 68.178.232.100	United States	AS-26496-GO-DADDY-COM-LLC	2011-08-11 virtual
  <a id="_4792"></a>
  - 64.92.111.3	United States	MASSIVE-NETWORKS	2011-07-27 mdeium virtual [https://viewdns.info/reverseip/?t=1&host=64.92.111.3](https://viewdns.info/reverseip/?t=1&host=64.92.111.3)<a id="_4793"></a>

    <a id="_4794"></a>
    - [https://web.archive.org/web/20110211133905/http://tipsypotpole.com/](https://web.archive.org/web/20110211133905/http://tipsypotpole.com/) off
    <a id="_4795"></a>
    - [https://web.archive.org/web/20250000000000*/quantumhealing.com](https://web.archive.org/web/20250000000000*/quantumhealing.com) popular
    <a id="_4796"></a>
    - [https://web.archive.org/web/20110202114353/http://outdoortradition.com/](https://web.archive.org/web/20110202114353/http://outdoortradition.com/) redirecting. [https://dawhois.com/www/outdoortradition.com.html](https://dawhois.com/www/outdoortradition.com.html) not found.
    <a id="_4797"></a>
    - [https://web.archive.org/web/20250000000000*/gtinvestigations.com](https://web.archive.org/web/20250000000000*/gtinvestigations.com) popular
    <a id="_4798"></a>
    - [https://web.archive.org/web/20250000000000*/dig-itmag.com](https://web.archive.org/web/20250000000000*/dig-itmag.com) big

<a id="_4799"></a>
europeannewsflash.com:<a id="_4800"></a>

<a id="_4801"></a>
- [https://viewdns.info/iphistory/?domain=europeannewsflash.com](https://viewdns.info/iphistory/?domain=europeannewsflash.com)<a id="_4802"></a>

  <a id="_4803"></a>
  - 68.178.232.100	United States	AS-26496-GO-DADDY-COM-LLC	2011-10-09 virtual
  <a id="_4804"></a>
  - 216.131.66.209	San Francisco - United States	STRTEC	2011-09-08. Tested viewdns.info range: 216.131.66.201 216.131.66.219
<a id="_4805"></a>
- [https://dnshistory.org/historical-dns-records/a/europeannewsflash.com](https://dnshistory.org/historical-dns-records/a/europeannewsflash.com) 2010-02-06 -\> 2010-08-02 216.131.66.209. Tested.

<a id="_4806"></a>
outlooknewscast.com:<a id="_4807"></a>

<a id="_4808"></a>
- [https://dnshistory.org/historical-dns-records/a/outlooknewscast.com](https://dnshistory.org/historical-dns-records/a/outlooknewscast.com)<a id="_4809"></a>

  <a id="_4810"></a>
  - 2009-08-08 -\> 2011-02-11 74.53.159.130. Tested viewdns.info range: 74.53.159.120 - 74.53.159.140<a id="_4811"></a>

    <a id="_4812"></a>
    - 74.53.159.130: aeromedhistory.org 2014-11-29
    <a id="_4813"></a>
    - 74.53.159.130: mariposahorticultural.com 2022-11-28
    <a id="_4814"></a>
    - 74.53.159.130: thewritestuffresume.com 2011-04-04. Legit.
<a id="_4815"></a>
- [https://viewdns.info/iphistory/?domain=outlooknewscast.com](https://viewdns.info/iphistory/?domain=outlooknewscast.com)<a id="_4816"></a>

  <a id="_4817"></a>
  - 204.93.178.121	Chicago - United States	SERVERCENTRAL	2011-09-08. Tested viewdns.info range: 204.93.178.111 - 204.93.178.131. Skimmed through, nothing of great interest.
  <a id="_4818"></a>
  - 74.53.159.130	United States	SOFTLAYER	2011-04-04. Tested.

<a id="_4819"></a>
24hoursprimenews.com:<a id="_4820"></a>

<a id="_4821"></a>
- [https://dnshistory.org/historical-dns-records/a/24hoursprimenews.com](https://dnshistory.org/historical-dns-records/a/24hoursprimenews.com) 2009-12-14 -\> 2011-10-04 216.9.68.24. Mid virtual: [https://viewdns.info/reverseip/?t=1&host=216.9.68.24](https://viewdns.info/reverseip/?t=1&host=216.9.68.24) had a quick look but no hits:<a id="_4822"></a>

  <a id="_4823"></a>
  - [https://web.archive.org/web/20110208211446/http://mynews-togo.com/](https://web.archive.org/web/20110208211446/http://mynews-togo.com/) invalid page. [https://dawhois.com/www/mynews-togo.com.html](https://dawhois.com/www/mynews-togo.com.html) same.
  <a id="_4824"></a>
  - [https://web.archive.org/web/20110207202025/http://nefiexpo.com/](https://web.archive.org/web/20110207202025/http://nefiexpo.com/)
<a id="_4825"></a>
- [https://viewdns.info/iphistory/?domain=24hoursprimenews.com](https://viewdns.info/iphistory/?domain=24hoursprimenews.com) 216.9.68.24	United States	VONAGE-BUSINESS	2012-01-11. Tested.
<a id="_4826"></a>
- [https://securitytrails.com/domain/24hoursprimenews.com/history/a](https://securitytrails.com/domain/24hoursprimenews.com/history/a) same

<a id="_4827"></a>
farsi-newsandweather.com:<a id="_4828"></a>

<a id="_4829"></a>
- [https://dnshistory.org/historical-dns-records/a/farsi-newsandweather.com](https://dnshistory.org/historical-dns-records/a/farsi-newsandweather.com) 2010-02-07 -\> 2010-08-03 69.49.101.19. Tested viewdns.info range: 69.49.101.9 - 69.49.101.19
<a id="_4830"></a>
- [https://viewdns.info/iphistory/?domain=farsi-newsandweather.com](https://viewdns.info/iphistory/?domain=farsi-newsandweather.com)<a id="_4831"></a>

  <a id="_4832"></a>
  - 68.178.232.100	United States	AS-26496-GO-DADDY-COM-LLC	2012-01-11 virtual
  <a id="_4833"></a>
  - 69.49.101.19	Canada	INFB-AS	2011-11-13. Tested.

<a id="_4834"></a>
global-view-news.com:<a id="_4835"></a>

<a id="_4836"></a>
- [https://dnshistory.org/historical-dns-records/a/global-view-news.com](https://dnshistory.org/historical-dns-records/a/global-view-news.com) 2010-02-13 -\> 2010-08-04 67.220.228.130. Tested viewdns.info range: 67.220.228.120 - 67.220.228.160:<a id="_4837"></a>

  <a id="_4838"></a>
  - 67.220.228.150: investfromhome.co.uk 2011-09-05. No archives.
<a id="_4839"></a>
- [https://viewdns.info/iphistory/?domain=global-view-news.com](https://viewdns.info/iphistory/?domain=global-view-news.com)<a id="_4840"></a>

  <a id="_4841"></a>
  - 68.178.232.100	United States	AS-26496-GO-DADDY-COM-LLC	2012-01-11 virtual
  <a id="_4842"></a>
  - 69.90.161.195	Canada	COGECO-PEER1	2011-09-08. Unknown. Tested viewdns.info range: 69.90.161.185 69.90.161.205. Some virtual misses. [https://viewdns.info/reverseip/?t=1&host=69.90.161.195](https://viewdns.info/reverseip/?t=1&host=69.90.161.195) medium virtual, canada.

<a id="_4843"></a>
health-men-today.com:<a id="_4844"></a>

<a id="_4845"></a>
- [https://dnshistory.org/historical-dns-records/a/health-men-today.com](https://dnshistory.org/historical-dns-records/a/health-men-today.com)<a id="_4846"></a>

  <a id="_4847"></a>
  - 2011-01-07 -\> 2011-01-07 69.90.162.165. Tested viewdns.info range: 69.90.162.155 - 69.90.162.175. Virtuals.
  <a id="_4848"></a>
  - 2009-11-30 -\> 2010-05-27 67.220.228.224. New range with global-view-news.com? Tested viewdns.info range: 67.220.228.214 67.220.228.234<a id="_4849"></a>

    <a id="_4850"></a>
    - 67.220.228.223: stagedwithdistinction.com 2011-10-09. One archive of godaddy only.
  <a id="_4851"></a>
  - 2009-08-01 -\> 2009-09-19 69.42.58.50. Tested viewdns.info range: 69.42.58.40 - 69.42.58.60. Virtuals, canada.
<a id="_4852"></a>
- [https://viewdns.info/iphistory/?domain=health-men-today.com](https://viewdns.info/iphistory/?domain=health-men-today.com)<a id="_4853"></a>

  <a id="_4854"></a>
  - 204.11.56.19	British Virgin Islands	CONFLUENCE-NETWORK-INC	2014-04-19. Virtuals.
  <a id="_4855"></a>
  - 208.91.197.19	British Virgin Islands	CONFLUENCE-NETWORK-INC	2013-05-20. Unknown range.
  <a id="_4856"></a>
  - 69.90.162.165	Canada	COGECO-PEER1	2012-06-29. Tested.
<a id="_4857"></a>
- [https://securitytrails.com/domain/health-men-today.com/history/a](https://securitytrails.com/domain/health-men-today.com/history/a)<a id="_4858"></a>

  <a id="_4859"></a>
  - 69.42.58.50 Aptum Technologies 2008-09-01 (17 years)	2008-09-04 (17 years)	3 days

<a id="_4860"></a>
firstnewssource.com:<a id="_4861"></a>

<a id="_4862"></a>
- [https://dnshistory.org/historical-dns-records/a/firstnewssource.com](https://dnshistory.org/historical-dns-records/a/firstnewssource.com)<a id="_4863"></a>

  <a id="_4864"></a>
  - 2010-02-09 -\> 2010-02-09 67.220.228.150 TODO new range with global-view-news.com? Tested.
  <a id="_4865"></a>
  - 2010-08-03 -\> 2010-08-03 69.90.162.70  TODO new range with global-view-news.com?

<a id="_4866"></a>
pars-technews.com:<a id="_4867"></a>

<a id="_4868"></a>
- [https://dnshistory.org/historical-dns-records/a/pars-technews.com](https://dnshistory.org/historical-dns-records/a/pars-technews.com) 2009-08-08 -\> 2011-02-13 74.220.219.104 Tested viewdns.info range: 74.220.219.94 74.220.219.114. [https://viewdns.info/reverseip/?t=1&host=74.220.219.104](https://viewdns.info/reverseip/?t=1&host=74.220.219.104) medium virtual haven't bothered much.
<a id="_4869"></a>
- [https://viewdns.info/iphistory/?domain=pars-technews.com](https://viewdns.info/iphistory/?domain=pars-technews.com) 74.220.219.104	United States	UNIFIEDLAYER-AS-1	2012-11-12. Tested.

<a id="_4870"></a>
newdaynewsonline.com:<a id="_4871"></a>

<a id="_4872"></a>
- [https://dnshistory.org/historical-dns-records/a/newdaynewsonline.com](https://dnshistory.org/historical-dns-records/a/newdaynewsonline.com) 2010-03-10 -\> 2010-08-15 76.163.54.16. Tested viewdns.info range: 76.163.54.6 76.163.54.26. [https://viewdns.info/reverseip/?t=1&host=76.163.54.16](https://viewdns.info/reverseip/?t=1&host=76.163.54.16) empty.<a id="_4873"></a>

  <a id="_4874"></a>
  - 76.163.54.23: leewoodwork.com 2014-07-05
<a id="_4875"></a>
- [https://viewdns.info/iphistory/?domain=newdaynewsonline.com](https://viewdns.info/iphistory/?domain=newdaynewsonline.com)<a id="_4876"></a>

  <a id="_4877"></a>
  - 74.91.154.56	United States	INTERNAP-BLOCK-4	2012-11-12 unknown range. Tested viewdns.info range: 74.91.154.46 74.91.154.66<a id="_4878"></a>

    <a id="_4879"></a>
    - 74.91.154.61: benefitsla.com 2013-04-21. Legit.
  <a id="_4880"></a>
  - 76.163.54.16	United States	WINDSTREAM	2011-09-08 unknown range. Tested.

<a id="_4881"></a>
sportsnewsfinder.com:<a id="_4882"></a>

<a id="_4883"></a>
- [https://dnshistory.org/historical-dns-records/a/sportsnewsfinder.com](https://dnshistory.org/historical-dns-records/a/sportsnewsfinder.com) 2009-08-11 -\> 2011-02-24 66.113.196.128. Tested viewdns.info range: 66.113.196.118 66.113.196.138. [https://viewdns.info/reverseip/?t=1&host=66.113.196.128](https://viewdns.info/reverseip/?t=1&host=66.113.196.128) empty.
<a id="_4884"></a>
- [https://viewdns.info/iphistory/?domain=sportsnewsfinder.com](https://viewdns.info/iphistory/?domain=sportsnewsfinder.com)<a id="_4885"></a>

  <a id="_4886"></a>
  - 50.63.202.58	United States	AS-26496-GO-DADDY-COM-LLC	2013-03-23 some similar hits on other sites, possibly all flukes
  <a id="_4887"></a>
  - 207.150.219.159	United States	AFFINITY-INTER	2013-03-02
  <a id="_4888"></a>
  - 66.113.196.128	United States	NETNATION	2012-01-11. Tested.

<a id="_4889"></a>
newsworldsite.com:<a id="_4890"></a>

<a id="_4891"></a>
- [https://viewdns.info/iphistory/?domain=newsworldsite.com](https://viewdns.info/iphistory/?domain=newsworldsite.com)<a id="_4892"></a>

  <a id="_4893"></a>
  - 68.178.232.100	United States	AS-26496-GO-DADDY-COM-LLC	2013-05-20 big virtual
  <a id="_4894"></a>
  - 204.93.159.80	Chicago - United States	SERVERCENTRAL	2013-04-21. Tested viewdns.info range: 204.93.159.70 204.93.159.90. [https://viewdns.info/reverseip/?t=1&host=204.93.159.80](https://viewdns.info/reverseip/?t=1&host=204.93.159.80) medium virtual.<a id="_4895"></a>

    <a id="_4896"></a>
    - 204.93.159.84: team-merk.com 2011-08-11. No archives.

<a id="_4897"></a>
todaysnewsreports.net:<a id="_4898"></a>

<a id="_4899"></a>
- [https://viewdns.info/iphistory/?domain=todaysnewsreports.net](https://viewdns.info/iphistory/?domain=todaysnewsreports.net)<a id="_4900"></a>

  <a id="_4901"></a>
  - 208.91.197.132	British Virgin Islands	CONFLUENCE-NETWORK-INC	2013-07-01
  <a id="_4902"></a>
  - 205.178.189.129	United States	NETWORK-SOLUTIONS-HOSTING	2013-05-20 likely virtual
  <a id="_4903"></a>
  - 173.255.131.72	Reno - United States	UK-2 Limited	2012-08-27. Tested viewdns.info range: 173.255.131.62 173.255.131.82. Virtual and modern hits only.
  <a id="_4904"></a>
  - 67.213.211.232	United States	UK-2 Limited	2011-09-07 unknown. Tested viewdns.info range: 67.213.211.222 67.213.211.242. [https://viewdns.info/reverseip/?t=1&host=67.213.211.232](https://viewdns.info/reverseip/?t=1&host=67.213.211.232) empty.<a id="_4905"></a>

    <a id="_4906"></a>
    - 67.213.211.236: icf-finan.com 2015-01-20
    <a id="_4907"></a>
    - 67.213.211.237: playinside.me 2016-02-04. Nice domain hack, but no.
    <a id="_4908"></a>
    - 67.213.211.239: reality-sexxx.com 2011-09-08

<a id="_4909"></a>
hassannews.net:<a id="_4910"></a>

<a id="_4911"></a>
- [https://viewdns.info/iphistory/?domain=hassannews.net](https://viewdns.info/iphistory/?domain=hassannews.net)<a id="_4912"></a>

  <a id="_4913"></a>
  - 208.91.197.132	British Virgin Islands	CONFLUENCE-NETWORK-INC	2013-07-08
  <a id="_4914"></a>
  - 205.178.189.131	United States	NETWORK-SOLUTIONS-HOSTING	2013-07-01. Likely virtual.

<a id="_4915"></a>
todayoutdoors.com:<a id="_4916"></a>

<a id="_4917"></a>
- [https://dnshistory.org/historical-dns-records/a/todayoutdoors.com](https://dnshistory.org/historical-dns-records/a/todayoutdoors.com)<a id="_4918"></a>

  <a id="_4919"></a>
  - 2009-08-11 -\> 2010-07-07 174.133.44.90. Tested viewdns.info range: 174.133.44.80 174.133.44.100. Virtual and modern. [https://viewdns.info/reverseip/?t=1&host=174.133.44.90](https://viewdns.info/reverseip/?t=1&host=174.133.44.90) two modern domains.
  <a id="_4920"></a>
  - 2011-03-01 -\> 2011-03-01 174.123.172.82 unknown. Tested viewdns.info range: 174.123.172.72 174.123.172.92. Virtuals.
<a id="_4921"></a>
- [https://viewdns.info/iphistory/?domain=todayoutdoors.com](https://viewdns.info/iphistory/?domain=todayoutdoors.com)<a id="_4922"></a>

  <a id="_4923"></a>
  - 68.178.232.100	United States	AS-26496-GO-DADDY-COM-LLC	2011-07-02 virtual
  <a id="_4924"></a>
  - 174.123.172.82	United States	SOFTLAYER	2011-04-04. Tested.

<a id="_4925"></a>
globaltourist.net:<a id="_4926"></a>

<a id="_4927"></a>
- [https://dnshistory.org/historical-dns-records/a/](https://dnshistory.org/historical-dns-records/a/) 2009-07-30 -\> 2011-01-01 69.59.20.215 unknown. Tested viewdns.info range: 69.59.20.205 69.59.20.225. Virtuals.
<a id="_4928"></a>
- [https://viewdns.info/iphistory/?domain=globaltourist.net](https://viewdns.info/iphistory/?domain=globaltourist.net)<a id="_4929"></a>

  <a id="_4930"></a>
  - 216.172.170.14	United States	NETWORK-SOLUTIONS-HOSTING	2013-07-08
  <a id="_4931"></a>
  - 216.21.239.197	United States	NETWORK-SOLUTIONS-HOSTING	2012-06-25
  <a id="_4932"></a>
  - 68.178.232.100	United States	AS-26496-GO-DADDY-COM-LLC	2012-04-09 big virtual
  <a id="_4933"></a>
  - 174.136.34.154	United States	IHNET	2012-03-12 unknown. Tested viewdns.info range: 174.136.34.144 174.136.34.164
  <a id="_4934"></a>
  - 74.119.145.101	Frankfurt am Main - Germany	PERFORMIVE	2011-09-07. Tested viewdns.info range: 74.119.145.91 74.119.145.111. One virtual.
  <a id="_4935"></a>
  - 69.59.20.215	United States	ATLRETAIL	2011-06-22. Tested [https://viewdns.info/reverseip/?t=1&host=69.59.20.215](https://viewdns.info/reverseip/?t=1&host=69.59.20.215)<a id="_4936"></a>

    <a id="_4937"></a>
    - [https://web.archive.org/web/20080521063605/http://piasawine.com/](https://web.archive.org/web/20080521063605/http://piasawine.com/) index of

<a id="_4938"></a>
terrain-news.com:<a id="_4939"></a>

<a id="_4940"></a>
- [JAR](https://web.archive.org/web/20110202060511/http://terrain-news.com/internetspeed.jar)
<a id="_4941"></a>
- [https://viewdns.info/iphistory/?domain=terrain-news.com](https://viewdns.info/iphistory/?domain=terrain-news.com) None in simple ranges.<a id="_4942"></a>

  <a id="_4943"></a>
  - 204.11.56.25	British Virgin Islands	CONFLUENCE-NETWORK-INC	2013-11-08. Virtuals.
  <a id="_4944"></a>
  - 208.91.197.19	British Virgin Islands	CONFLUENCE-NETWORK-INC	2013-05-20. Virtual 167. [https://viewdns.info/reverseip/?host=208.91.197.19&t=1](https://viewdns.info/reverseip/?host=208.91.197.19&t=1) not very promising.<a id="_4945"></a>

    <a id="_4946"></a>
    - eurotravelnyc.com legit [https://web.archive.org/web/20110201195411/http://eurotravelnyc.com/](https://web.archive.org/web/20110201195411/http://eurotravelnyc.com/)
  <a id="_4947"></a>
  - 208.187.167.20	United States	DATANOC	2012-01-11. Tested viewdns.info range: 208.187.167.10 208.187.167.30. Newer domains. [https://viewdns.info/reverseip/?t=1&host=208.187.167.20](https://viewdns.info/reverseip/?t=1&host=208.187.167.20) only has one conck.ooo. WTF.
<a id="_4948"></a>
- [https://securitytrails.com/domain/terrain-news.com/history/a](https://securitytrails.com/domain/terrain-news.com/history/a) same:<a id="_4949"></a>

  <a id="_4950"></a>
  - 208.91.197.19 Confluence Networks Inc 2012-05-12 (13 years)	2012-05-31 (13 years)	19 days
  <a id="_4951"></a>
  - 208.187.167.20 Lanset America Corporation 2008-11-12 (16 years)	2009-12-09 (15 years)	1 year

<a id="_4952"></a>
intlnewsdaily.com<a id="_4953"></a>

<a id="_4954"></a>
- [https://dnshistory.org/historical-dns-records/a/intlnewsdaily.com](https://dnshistory.org/historical-dns-records/a/intlnewsdaily.com) 2010-02-21 -\> 2010-08-06 75.126.136.179. unknown range. [https://viewdns.info/reverseip/?t=1&host=75.126.136.179](https://viewdns.info/reverseip/?t=1&host=75.126.136.179) empty checked 75.126.136.171 - 75.126.136.179
<a id="_4955"></a>
- [https://viewdns.info/iphistory/?domain=intlnewsdaily.com](https://viewdns.info/iphistory/?domain=intlnewsdaily.com)<a id="_4956"></a>

  <a id="_4957"></a>
  - 208.91.197.19	British Virgin Islands	CONFLUENCE-NETWORK-INC	2013-05-20. Virtual. Tested.
  <a id="_4958"></a>
  - 63.247.95.50	Austell - United States	NTHL	2012-06-29 unknown. Tested viewdns.info range: 63.247.95.40 63.247.95.60<a id="_4959"></a>

    <a id="_4960"></a>
    - 63.247.95.50: 2b-sports.com 2013-04-21
    <a id="_4961"></a>
    - 63.247.95.50: caldentalinsurance.com 2014-07-05
    <a id="_4962"></a>
    - 63.247.95.50: cameronbal-photography.com 2012-06-29
    <a id="_4963"></a>
    - 63.247.95.50: congbetham.com 2014-07-05
    <a id="_4964"></a>
    - 63.247.95.50: essentialintelligenceagency.com 2023-03-07
    <a id="_4965"></a>
    - 63.247.95.50: isabellavalentina.com 2014-07-05
    <a id="_4966"></a>
    - 63.247.95.50: jhraccounting.com.au 2021-05-03
    <a id="_4967"></a>
    - 63.247.95.50: missouribreaks294.com 2012-06-29
    <a id="_4968"></a>
    - 63.247.95.50: startorganize.com 2011-08-11
    <a id="_4969"></a>
    - 63.247.95.50: tifocus.net 2011-08-11
    <a id="_4970"></a>
    - 63.247.95.50: tifocus.org 2011-08-10
    <a id="_4971"></a>
    - 63.247.95.50: whitepartyorlando.com 2012-01-11
  <a id="_4972"></a>
  - 204.11.56.25 ([ipinf.ru](ipinf-ru.md)) [https://viewdns.info/reverseip/?t=1&host=204.11.56.25](https://viewdns.info/reverseip/?t=1&host=204.11.56.25) Virtual 2,999
<a id="_4973"></a>
- [https://securitytrails.com/domain/intlnewsdaily.com/history/a](https://securitytrails.com/domain/intlnewsdaily.com/history/a) empty on dates

<a id="_4974"></a>
opensourcenewstoday.com:<a id="_4975"></a>

<a id="_4976"></a>
- [https://viewdns.info/iphistory/?domain=opensourcenewstoday.com](https://viewdns.info/iphistory/?domain=opensourcenewstoday.com)<a id="_4977"></a>

  <a id="_4978"></a>
  - 68.178.232.100	United States	AS-26496-GO-DADDY-COM-LLC	2011-11-13 virtual
  <a id="_4979"></a>
  - 64.16.193.48	Riyadh - Saudi Arabia	Saudi Telecom Company JSC	2011-09-08. Tested viewdns.info range: 64.16.193.38 64.16.193.55. Ran out. [https://viewdns.info/reverseip/?t=1&host=64.16.193.48](https://viewdns.info/reverseip/?t=1&host=64.16.193.48) virtual 55, lots of porn
<a id="_4980"></a>
- [https://securitytrails.com/domain/opensourcenewstoday.com/history/a](https://securitytrails.com/domain/opensourcenewstoday.com/history/a)<a id="_4981"></a>

  <a id="_4982"></a>
  - 64.16.193.48 Saudi Telecom Company JSC 2010-05-04 (15 years)	2010-05-20 (15 years)	16 days

<a id="_4983"></a>
techwatchtoday.com:<a id="_4984"></a>

<a id="_4985"></a>
- [https://viewdns.info/iphistory/?domain=techwatchtoday.com](https://viewdns.info/iphistory/?domain=techwatchtoday.com)<a id="_4986"></a>

  <a id="_4987"></a>
  - 208.91.197.132	British Virgin Islands	CONFLUENCE-NETWORK-INC	2013-11-29 virtual
  <a id="_4988"></a>
  - 66.11.225.226	United States	TNWEB-LEW-001	2012-01-11 unknown. Checked 66.11.225.220 - 66.11.225.233<a id="_4989"></a>

    <a id="_4990"></a>
    - [https://viewdns.info/reverseip/?t=1&host=66.11.225.223](https://viewdns.info/reverseip/?t=1&host=66.11.225.223)<a id="_4991"></a>

      <a id="_4992"></a>
      - [https://web.archive.org/web/20110201142759/http://usdconnection.com/](https://web.archive.org/web/20110201142759/http://usdconnection.com/) broken
    <a id="_4993"></a>
    - [https://viewdns.info/reverseip/?t=1&host=66.11.225.226](https://viewdns.info/reverseip/?t=1&host=66.11.225.226) has [https://web.archive.org/web/20100201000000*/tsgardens.com](https://web.archive.org/web/20100201000000*/tsgardens.com) No archives. [http://cqcounter.com/whois/www/tsgardens.com.html](http://cqcounter.com/whois/www/tsgardens.com.html) empty.
    <a id="_4994"></a>
    - [https://viewdns.info/reverseip/?t=1&host=66.11.225.227](https://viewdns.info/reverseip/?t=1&host=66.11.225.227)<a id="_4995"></a>

      <a id="_4996"></a>
      - [https://web.archive.org/web/20110108222333/http://inhospitality.net/](https://web.archive.org/web/20110108222333/http://inhospitality.net/) off
<a id="_4997"></a>
- [https://dnshistory.org/historical-dns-records/a/techwatchtoday.com](https://dnshistory.org/historical-dns-records/a/techwatchtoday.com) 2009-08-11 -\> 2011-02-26 66.11.225.226 big shared host
<a id="_4998"></a>
- [https://securitytrails.com/domain/techwatchtoday.com/history/a](https://securitytrails.com/domain/techwatchtoday.com/history/a) same<a id="_4999"></a>

  <a id="_5000"></a>
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
