# Work log

↑ **Parent:** [Methodology](methodology.md)

Scrapped justdropped data, patched:
```
+++ b/cia-2010-covert-communication-websites/cdx-post.sh
@@ -1,7 +1,7 @@
 #!/usr/bin/env bash
 # Post process the output of cdx.sh to enrich IDs even further, and reconstruct easier to Web Archive inspect domain names.
-grep -P -e '([^,)]+)\)\/\1\.swf|\)/[^/]+.jar|([^,)]+),([^,)]+),([^,)]+)\)/cgi-bin/[^/]+\.cgi' "$1" |
-  sed -r 's/\).*//' | awk -F, '{ printf("%s.%s\n", $2, $1) }' | uniq -c | awk '$1 == 1{ print $2 }' | tee $1.post
+grep -P -e '([^,)]+)\)\/\1\.swf|\)/[^/]+.jar|([^,)]+),([^,)]+),([^,)]+)\)/cgi-bin/[^/]+\.cgi' "$1"|
+  sed -r 's/\).*//' | awk -F, '{ printf("%s.%s\n", $2, $1) }' | uniq -c | awk '{ print $2 }' | tee $1.post
```
and then:
```
./hupo-cdx-tor.sh out 'news|headline|internationali|mondo|mundo|mondi|iran|today' 2006 2022
```

[https://web.archive.org/web/20110203041325/http://financecentraltoday.com/](https://web.archive.org/web/20110203041325/http://financecentraltoday.com/)
- [https://viewdns.info/iphistory/?domain=financecentraltoday.com](https://viewdns.info/iphistory/?domain=financecentraltoday.com)
  - 208.91.197.27	British Virgin Islands	CONFLUENCE-NETWORK-INC	2013-11-08
  - 69.90.163.85	Canada	COGECO-PEER1	2013-09-26
  - 69.90.160.75	Canada	COGECO-PEER1	2011-06-22 [https://viewdns.info/reverseip/?t=1&host=69.90.160.75](https://viewdns.info/reverseip/?t=1&host=69.90.160.75) says small virtual. Checked all but no hits.
- [https://securitytrails.com/domain/financecentraltoday.com/history/a](https://securitytrails.com/domain/financecentraltoday.com/history/a)
  - 69.90.160.75 Aptum Technologies 2010-04-04 (15 years)	2010-04-27 (15 years)	23 days
  - 69.42.58.70 Aptum Technologies 2009-01-07 (16 years)	2009-01-28 (16 years)	21 days. Near health-men-today.com.

[https://web.archive.org/web/20110202221328/http://thenewsofpakistan.com/](https://web.archive.org/web/20110202221328/http://thenewsofpakistan.com/)
- [https://viewdns.info/iphistory/?domain=thenewsofpakistan.com](https://viewdns.info/iphistory/?domain=thenewsofpakistan.com)
  - 50.22.27.227	Dallas - United States	SOFTLAYER	2013-06-30
  - 174.133.70.18	United States	SOFTLAYER	2012-11-12. In range.
- [https://securitytrails.com/domain/thenewsofpakistan.com/history/a](https://securitytrails.com/domain/thenewsofpakistan.com/history/a)
  - 50.22.27.227 SoftLayer Technologies Inc. 2013-02-20 (12 years)	2013-04-26 (12 years)	2 months
  - 174.133.70.18 SoftLayer Technologies Inc. 2009-09-17 (15 years)	2009-12-19 (15 years)	3 months
  - 68.178.232.100 GoDaddy.com, LLC 2009-09-12 (16 years)	2009-09-17 (15 years)	5 days

[https://web.archive.org/web/20110201184753/http://shadesofnews.com/](https://web.archive.org/web/20110201184753/http://shadesofnews.com/)
- [https://viewdns.info/iphistory/?domain=shadesofnews.com](https://viewdns.info/iphistory/?domain=shadesofnews.com)
  - 64.6.225.2	United States	WEBINT	2013-11-29 [https://viewdns.info/reverseip/?t=1&host=64.6.225.2](https://viewdns.info/reverseip/?t=1&host=64.6.225.2) mid virtual.
- [https://securitytrails.com/domain/shadesofnews.com/history/a](https://securitytrails.com/domain/shadesofnews.com/history/a)
  - 64.6.225.2 Jumpline Inc 2009-09-17 (15 years)	2009-12-13 (15 years)	3 months

[https://web.archive.org/web/20050424123432/http://www.pokernewsweb.com/](https://web.archive.org/web/20050424123432/http://www.pokernewsweb.com/) likely legit in the intended emulated style

[https://web.archive.org/web/20101226225311/http://world-news-online.net/](https://web.archive.org/web/20101226225311/http://world-news-online.net/) [domainsbyproxy.com](../domains-by-proxy.md) registered 2006-06-14T21
- [https://viewdns.info/iphistory/?domain=world-news-online.net](https://viewdns.info/iphistory/?domain=world-news-online.net)
  - 199.187.208.12	Miami - United States	PERFORMIVE	2013-12-02 [https://viewdns.info/reverseip/?t=1&host=199.187.208.12](https://viewdns.info/reverseip/?t=1&host=199.187.208.12) is small virtual, checked all in there and 199.187.208.5 - 199.187.208.15
    - [https://web.archive.org/web/20110207150839/http://webofcheer.com/](https://web.archive.org/web/20110207150839/http://webofcheer.com/) hit! [domainsbyproxy.com](../domains-by-proxy.md)
  - 63.247.81.241	United States	NTHL	2011-09-07 [https://viewdns.info/reverseip/?t=1&host=63.247.81.241](https://viewdns.info/reverseip/?t=1&host=63.247.81.241) searching 63.247.81.249
    - 63.247.81.241 [https://web.archive.org/web/20110202210855/http://motornstyle.com/](https://web.archive.org/web/20110202210855/http://motornstyle.com/) off
    - 63.247.81.244 [https://web.archive.org/web/20110106222053/http://puzzlesgalore.net/](https://web.archive.org/web/20110106222053/http://puzzlesgalore.net/) under construction
    - 63.247.81.245 [https://web.archive.org/web/20110202102921/http://chairyogavideo.com/](https://web.archive.org/web/20110202102921/http://chairyogavideo.com/) under construction
    - 63.247.81.247 [https://web.archive.org/web/20110207131727/http://pccubeservice.com/indexPage.jsp](https://web.archive.org/web/20110207131727/http://pccubeservice.com/indexPage.jsp)
- [https://securitytrails.com/domain/world-news-online.net/history/a](https://securitytrails.com/domain/world-news-online.net/history/a)
  - 199.187.208.12 Performive LLC 2011-09-10 (14 years)	2012-04-08 (13 years)	7 months
  - 63.247.81.241 NETWORK TRANSIT HOLDINGS LLC 2008-09-01 (17 years)	2009-04-23 (16 years)	8 months

[https://web.archive.org/web/20100923090646/http://mideasttoday.net/](https://web.archive.org/web/20100923090646/http://mideasttoday.net/)
- [https://viewdns.info/iphistory/?domain=mideasttoday.net](https://viewdns.info/iphistory/?domain=mideasttoday.net) says:
  - 208.91.197.27	British Virgin Islands	CONFLUENCE-NETWORK-INC	2013-12-09
  - 65.98.118.97	United States	FORTRESSITX	2013-12-02
  - 65.98.118.101	United States	FORTRESSITX	2013-05-20. [https://viewdns.info/reverseip/?t=1&host=65.98.118.101](https://viewdns.info/reverseip/?t=1&host=65.98.118.101) empty
- [https://securitytrails.com/domain/mideasttoday.net/history/a](https://securitytrails.com/domain/mideasttoday.net/history/a) says:
  - 208.91.197.27 Confluence Networks Inc 2013-12-06 (11 years)	2013-12-15 (11 years)	9 days
  - 65.98.118.97 FortressITX 2013-05-23 (12 years)	2013-06-20 (12 years)	28 days
  - 65.98.118.101 FortressITX 2008-11-11 (16 years)	2010-07-08 (15 years)	2 years

[https://web.archive.org/web/20110209045123/http://dryterrainnews.com/](https://web.archive.org/web/20110209045123/http://dryterrainnews.com/)
- [https://viewdns.info/iphistory/?domain=dryterrainnews.com](https://viewdns.info/iphistory/?domain=dryterrainnews.com) says:
  - 50.22.27.227	Dallas - United States	SOFTLAYER	2013-11-29
  - 174.133.70.18	United States	SOFTLAYER	2012-11-12
    - [https://viewdns.info/reverseip/?t=1&host=174.133.70.18](https://viewdns.info/reverseip/?t=1&host=174.133.70.18) says small virtual also contains hits:
      - [https://web.archive.org/web/20110202151142/http://thefootball-life.com/](https://web.archive.org/web/20110202151142/http://thefootball-life.com/)
      - [https://web.archive.org/web/20110207201846/http://totallynewsnow.com/](https://web.archive.org/web/20110207201846/http://totallynewsnow.com/)
- [https://securitytrails.com/domain/dryterrainnews.com/history/a](https://securitytrails.com/domain/dryterrainnews.com/history/a)
  - 74.133.70.18 SoftLayer Technologies Inc. 2010-06-18 (15 years)	2010-07-11 (15 years)	23 days
  - 68.178.232.100 GoDaddy.com, LLC 2010-06-16 (15 years)	2010-06-18 (15 years)	2 days

[https://web.archive.org/web/20100206221718/http://euronewsonline.net/](https://web.archive.org/web/20100206221718/http://euronewsonline.net/)
- [https://viewdns.info/iphistory/?domain=euronewsonline.net](https://viewdns.info/iphistory/?domain=euronewsonline.net) says:
  - 74.220.207.94	United States	UNIFIEDLAYER-AS-1	2013-12-09
  - 184.168.221.55	United States	AS-26496-GO-DADDY-COM-LLC	2013-11-25
  - 74.220.207.94	United States	UNIFIEDLAYER-AS-1	2013-09-23. [https://viewdns.info/reverseip/?t=1&host=74.220.207.94](https://viewdns.info/reverseip/?t=1&host=74.220.207.94) says medium virtual.
- [https://securitytrails.com/domain/euronewsonline.net/history/a](https://securitytrails.com/domain/euronewsonline.net/history/a) also says
  - 74.220.207.94 Unified Layer 2008-09-01 (17 years)	2008-12-26 (16 years)	4 months

[https://web.archive.org/web/20110208063146/http://news-and-sports.com/](https://web.archive.org/web/20110208063146/http://news-and-sports.com/) Hit.
- [https://viewdns.info/iphistory/?domain=news-and-sports.com](https://viewdns.info/iphistory/?domain=news-and-sports.com) says:
  - 204.11.56.25	British Virgin Islands	CONFLUENCE-NETWORK-INC	2014-07-05
  - 208.91.197.19	British Virgin Islands	CONFLUENCE-NETWORK-INC	2013-05-20
  - 66.104.175.42	United States	XO-AS15	2012-06-29 In range.

[https://web.archive.org/web/20110202054628/http://intoworldnews.com/](https://web.archive.org/web/20110202054628/http://intoworldnews.com/) hit.
- [https://viewdns.info/iphistory/?domain=intoworldnews.com](https://viewdns.info/iphistory/?domain=intoworldnews.com) says:
  - 208.91.197.19	British Virgin Islands	CONFLUENCE-NETWORK-INC	2013-05-20
  - 208.91.197.132	British Virgin Islands	CONFLUENCE-NETWORK-INC	2013-04-21
  - 219.90.61.118	Taiwan	UUNET	2013-03-02
    - [https://viewdns.info/reverseip/?t=1&host=219.90.61.118](https://viewdns.info/reverseip/?t=1&host=219.90.61.118) empty

    19.90.61.118
- securitytrails:
  - 219.90.61.118 Verizon Business 2010-12-11 (14 years)	2011-07-13 (14 years)	7 months
  - 205.178.189.129 Network Solutions, LLC 2010-03-10 (15 years)	2010-03-29 (15 years)	19 days

[https://web.archive.org/web/20110207171340/http://mydailynewsreport.com/](https://web.archive.org/web/20110207171340/http://mydailynewsreport.com/) hit
- [https://viewdns.info/iphistory/?domain=mydailynewsreport.com](https://viewdns.info/iphistory/?domain=mydailynewsreport.com) says
  - 208.91.197.132	British Virgin Islands	CONFLUENCE-NETWORK-INC	2014-03-15
  - 74.52.51.139	United States	SOFTLAYER	2012-06-29 [https://viewdns.info/reverseip/?t=1&host=74.52.51.139](https://viewdns.info/reverseip/?t=1&host=74.52.51.139) says small virtual  
    On that same IP...


    - [https://web.archive.org/web/20110208004005/http://networkconnectionsite.com/](https://web.archive.org/web/20110208004005/http://networkconnectionsite.com/) Hit. [https://viewdns.info/iphistory/?domain=networkconnectionsite.com](https://viewdns.info/iphistory/?domain=networkconnectionsite.com) says only at that IP.
    - [https://web.archive.org/web/20110207103008/http://soccerguidesite.com/](https://web.archive.org/web/20110207103008/http://soccerguidesite.com/) Korean site, would be unusual given a splash page. Has a JAR at: [https://web.archive.org/web/20110207103045/http://soccerguidesite.com/tools.jar](https://web.archive.org/web/20110207103045/http://soccerguidesite.com/tools.jar) but everything else unarchived. JAR is atypical.

    Around checked 74.52.51.133 - 74.52.51.149
    - [https://viewdns.info/reverseip/?t=1&host=74.52.51.136](https://viewdns.info/reverseip/?t=1&host=74.52.51.136) large virtual
- [https://securitytrails.com/domain/mydailynewsreport.com/history/a](https://securitytrails.com/domain/mydailynewsreport.com/history/a) says
  - 74.52.51.139 SoftLayer Technologies Inc. 2011-03-06 (14 years)	2011-03-21 (14 years)	15 days
  - 174.123.39.202 SoftLayer Technologies Inc. 2010-12-08 (14 years)	2011-03-05 (14 years)	3 months
  - 75.125.247.170 SoftLayer Technologies Inc. 2010-02-20 (15 years)	2010-05-22 (15 years)	3 months
  - 205.178.189.129 Network Solutions, LLC 2010-02-10 (15 years)	2010-02-20 (15 years)	10 days. [https://viewdns.info/reverseip/?t=1&host=205.178.189.129](https://viewdns.info/reverseip/?t=1&host=205.178.189.129) is large virtual.

[https://web.archive.org/web/20050508220858/http://www.asianewsupdate.com/](https://web.archive.org/web/20050508220858/http://www.asianewsupdate.com/) this looks like the exact format of legitimate site the CIA was emulating. Copyright 2005, a CGI link to as: [http://www.asianewsupdate.com:80/cgi-sys/FormMail.cgi](http://www.asianewsupdate.com:80/cgi-sys/FormMail.cgi) There's a phone there 01 647-0910 so seems less likely?

[2010](https://web.archive.org/web/20101226034643/http://newsdelivered.net/). [JAR unarchived](https://web.archive.org/web/20101226034643oe_/http://newsdelivered.net/tours.jar). rss, split image
- [https://viewdns.info/iphistory/?domain=newsdelivered.net](https://viewdns.info/iphistory/?domain=newsdelivered.net) says:
  - 192.96.218.41	United States	123NET	2013-06-10
  - 196.40.84.210	Costa Rica	RADIOGRAFICA COSTARRICENSE	2013-05-20
  - 50.63.202.40	United States	AS-26496-GO-DADDY-COM-LLC	2013-04-08
  - 74.220.207.158	United States	UNIFIEDLAYER-AS-1	2013-03-11. [https://viewdns.info/reverseip/?host=74.220.207.158&t=1](https://viewdns.info/reverseip/?host=74.220.207.158&t=1) says large virtual.
- securitytrails:
  - 192.96.218.41 123.Net, Inc. 2013-05-29 (12 years)	2013-06-02 (12 years)	4 days
  - 196.40.84.210 RADIOGRAFICA COSTARRICENSE 2013-05-21 (12 years)	2013-05-27 (12 years)	6 days
  - 74.220.207.158 Unified Layer 2008-09-01 (17 years)	2009-02-26 (16 years)	6 months

[2010](https://web.archive.org/web/20100513190714/http://latinamericanewsbeat.com/). [JAR](https://web.archive.org/web/20110201000000*/http://latinamericanewsbeat.com/today.jar). Split header.
- [https://viewdns.info/iphistory/?domain=latinamericanewsbeat.com](https://viewdns.info/iphistory/?domain=latinamericanewsbeat.com) says:
  - 184.168.221.34	United States	AS-26496-GO-DADDY-COM-LLC	2013-03-23
  - 74.91.172.195	United States	INTERNAP-BLOCK-4	2012-11-12
  - 76.162.90.179	United States	WINDSTREAM	2011-09-08. [https://viewdns.info/reverseip/?host=76.162.90.179&t=1](https://viewdns.info/reverseip/?host=76.162.90.179&t=1) says small virtual? Explored 76.162.90.174 - 76.162.90.183.
- [https://securitytrails.com/domain/latinamericanewsbeat.com/history/a](https://securitytrails.com/domain/latinamericanewsbeat.com/history/a)
  - 74.91.172.195 Unified Layer 2011-09-11 (14 years)	2011-11-02 (13 years)	2 months
  - 76.162.90.179 Amazon.com, Inc. 2008-09-01 (17 years)	2008-11-18 (16 years)	3 months

[2011](https://web.archive.org/web/20110201180802/http://inkfreenews.com/). [JAR unarchived](https://web.archive.org/web/20110201180802oe_/http://inkfreenews.com/break.jar). Split header.
- [https://viewdns.info/iphistory/?domain=inkfreenews.com](https://viewdns.info/iphistory/?domain=inkfreenews.com) says:
  - 68.178.232.100	United States	AS-26496-GO-DADDY-COM-LLC	2012-09-21
  - 128.121.9.46	United States	NTT-LTD-2914	2012-06-29. Reverse empty. Checked: 128.121.9.43 - 128.121.9.53
- [https://securitytrails.com/domain/inkfreenews.com/history/a](https://securitytrails.com/domain/inkfreenews.com/history/a)
  - 128.121.9.46 NTT America, Inc. 2008-09-01 (17 years)	2010-06-23 (15 years)	2 years

[2011](https://web.archive.org/web/20110128181622/http://profile-news.com/). [JAR](https://web.archive.org/web/20110128181907/http://profile-news.com/speedtest.jar). a.newslink, a.newslinkalt.
- [https://viewdns.info/iphistory/?domain=profile-news.com](https://viewdns.info/iphistory/?domain=profile-news.com) says:
  - 68.178.232.100	United States	AS-26496-GO-DADDY-COM-LLC	2012-06-29
  - 199.204.248.105	United States	WEBINT	2012-01-11. [https://viewdns.info/reverseip/?host=199.204.248.105&t=1](https://viewdns.info/reverseip/?host=199.204.248.105&t=1) says large virtual.
  - 205.214.86.38	United States	DATABANK-LATISYS	2011-08-11. [https://viewdns.info/reverseip/?host=205.214.86.38&t=1](https://viewdns.info/reverseip/?host=205.214.86.38&t=1) says small virtual.
- [https://securitytrails.com/domain/profile-news.com/history/a](https://securitytrails.com/domain/profile-news.com/history/a)
  - 205.214.86.38 Latisys-Denver, LLC 2010-06-19 (15 years)	2010-06-29 (15 years)	10 days
  - 209.151.94.18 Latisys-Denver, LLC 2008-09-01 (17 years)	2009-08-18 (16 years)	12 months. [https://viewdns.info/reverseip/?t=1&host=209.151.94.18](https://viewdns.info/reverseip/?t=1&host=209.151.94.18) empty.

[2011](https://web.archive.org/web/20110207210023/http://nejadnews.com/). Arabic. RSS.
- [https://viewdns.info/iphistory/?domain=nejadnews.com](https://viewdns.info/iphistory/?domain=nejadnews.com) says: 208.254.38.56	United States	COLO-PREM-VZB	2012-06-29.
  - [https://viewdns.info/reverseip/?host=208.254.38.56&t=1](https://viewdns.info/reverseip/?host=208.254.38.56&t=1) says single domain and we see that todaysengineering.com was not too far confirming a new range

[https://web.archive.org/web/20110129115400/http://kmirano.com/](https://web.archive.org/web/20110129115400/http://kmirano.com/) shallow but off style? Has a kmirano.sfw... [https://viewdns.info/iphistory/?domain=kmirano.com](https://viewdns.info/iphistory/?domain=kmirano.com) says 211.1.224.71	Japan	NTT SmartConnect Corporation	2012-01-11

[2011](https://web.archive.org/web/20110208191615/http://wiredworldnews.com/). [JAR](https://web.archive.org/web/20110208191739/http://wiredworldnews.com/development.jar). Copyright 2008. Split header and other images. They are obsessed about CDMA (2G).
- [https://viewdns.info/iphistory/?domain=wiredworldnews.com](https://viewdns.info/iphistory/?domain=wiredworldnews.com) says:
  - 69.89.237.152	United States	RINGSQUARED	2012-01-11. Empty.
  - 67.213.209.10	Atlanta - United States	UK-2 Limited	2011-04-04. Virtual.
- [https://securitytrails.com/domain/wiredworldnews.com/history/a](https://securitytrails.com/domain/wiredworldnews.com/history/a)
  - 69.89.237.152 RingSquared 2011-06-25 (14 years)	2011-07-30 (14 years)	1 month
  - 69.89.237.152 RingSquared 2011-06-14 (14 years)	2011-06-24 (14 years)	10 days
  - 67.213.209.10 UK-2 Limited 2008-12-03 (16 years)	2009-02-10 (16 years)	2 months
  - 69.4.225.2 SoftLayer Technologies Inc. 2008-09-01 (17 years)	2008-09-09 (17 years)	8 days. [https://viewdns.info/reverseip/?t=1&host=69.4.225.2](https://viewdns.info/reverseip/?t=1&host=69.4.225.2) empty.

[2011](https://web.archive.org/web/20110202221408/http://the-news-scene.com/). [JAR](https://web.archive.org/web/20110202221510/http://the-news-scene.com/world.jar). split header, RSS.
- [https://viewdns.info/iphistory/?domain=the-news-scene.com](https://viewdns.info/iphistory/?domain=the-news-scene.com) says 74.81.69.194	United States	NTHL	2012-01-11. [https://viewdns.info/reverseip/?host=74.81.69.194&t=1](https://viewdns.info/reverseip/?host=74.81.69.194&t=1) says virtual.
- [https://securitytrails.com/domain/the-news-scene.com/history/a](https://securitytrails.com/domain/the-news-scene.com/history/a) says
  - 74.81.69.194 NETWORK TRANSIT HOLDINGS LLC 2009-12-24 (15 years)	2010-03-23 (15 years)	3 months
  - 209.51.136.178 QuickMeg Inc 2008-09-01 (17 years)	2009-12-24 (15 years)	1 year. [https://viewdns.info/reverseip/?t=1&host=209.51.136.178](https://viewdns.info/reverseip/?t=1&host=209.51.136.178) says small virtual and in there we obtain:
    - [https://web.archive.org/web/20110202110916/http://cellar-notes.com/](https://web.archive.org/web/20110202110916/http://cellar-notes.com/) hit

    Explored viewdns.info 209.51.136.170 - 209.51.136.185 empty.

[2010](https://web.archive.org/web/20100528104248/http://eqranews.com/). Suspicious. But no clear fingrenprint. Also not as shallow as others. Also Joomla based which would be novel.
- [https://viewdns.info/iphistory/?domain=eqranews.com](https://viewdns.info/iphistory/?domain=eqranews.com) says:
  - 69.64.147.243	United States	RIGHTSIDE	2012-03-03
  - 67.228.81.180	Seattle - United States	SOFTLAYER	2011-04-04. [https://viewdns.info/reverseip/?t=1&host=67.228.81.180](https://viewdns.info/reverseip/?t=1&host=67.228.81.180) says virtual.
- [https://securitytrails.com/domain/eqranews.com/history/a](https://securitytrails.com/domain/eqranews.com/history/a) says
  - 69.64.147.243 Amazon.com, Inc. 2011-04-28 (14 years)	2012-01-19 (13 years)	9 months
  - 67.228.81.180 SoftLayer Technologies Inc. 2011-04-18 (14 years)	2011-04-28 (14 years)	10 days
  - 174.37.172.68 SoftLayer Technologies Inc. 2011-04-13 (14 years)	2011-04-18 (14 years)	5 days
  - 67.228.81.180 SoftLayer Technologies Inc. 2011-03-19 (14 years)	2011-04-13 (14 years)	25 days
  - 74.220.215.62 Unified Layer 2010-03-18 (15 years)	2011-03-19 (14 years)	1 year

[2010](https://web.archive.org/web/20100515102926/http://magneticfieldnews.com/). [JAR](https://web.archive.org/web/20100515103300/http://magneticfieldnews.com/science.jar).
- [https://viewdns.info/iphistory/?domain=magneticfieldnews.com](https://viewdns.info/iphistory/?domain=magneticfieldnews.com) says 173.205.124.151	United States	IMH-IAD	2012-01-11. [https://viewdns.info/reverseip/?host=173.205.124.151&t=1](https://viewdns.info/reverseip/?host=173.205.124.151&t=1) says large-ish virtual.
- [https://dnshistory.org/dns-records/magneticfieldnews.com](https://dnshistory.org/dns-records/magneticfieldnews.com) empty
- [https://securitytrails.com/domain/magneticfieldnews.com/history/a](https://securitytrails.com/domain/magneticfieldnews.com/history/a)
  - 208.91.197.132 Confluence Networks Inc 2012-02-11 (13 years)	2012-03-14 (13 years)	1 month
  - 173.205.124.151 InMotion Hosting, Inc. 2010-02-12 (15 years)	2012-02-11 (13 years)	2 years
  - 205.178.189.129 Network Solutions, LLC 2010-02-05 (15 years)	2010-02-12 (15 years)	7 days

[2011](https://web.archive.org/web/20110131054130/http://segomonews.com/). [JAR](https://web.archive.org/web/20110131054332/http://segomonews.com/myjar.jar). RSS, Split header images.
- [https://viewdns.info/iphistory/?domain=segomonews.com](https://viewdns.info/iphistory/?domain=segomonews.com) 204.13.11.6	United States	KATTARE	2012-01-11. [https://viewdns.info/reverseip/?host=204.13.11.6&t=1](https://viewdns.info/reverseip/?host=204.13.11.6&t=1) says virtual.
- [https://dnshistory.org/historical-dns-records/a/segomonews.com](https://dnshistory.org/historical-dns-records/a/segomonews.com) same
- [https://securitytrails.com/domain/segomonews.com/history/a](https://securitytrails.com/domain/segomonews.com/history/a) same

[http://newspapergateway.com/](http://newspapergateway.com/) [https://web.archive.org/web/20110208070309/http://newspapergateway.com/](https://web.archive.org/web/20110208070309/http://newspapergateway.com/) hard to tell but generally off. Has both JAR and SWF.
- [https://viewdns.info/iphistory/?domain=newspapergateway.com](https://viewdns.info/iphistory/?domain=newspapergateway.com) says:
  - 63.251.171.80	United States	INTERNAP-BLOCK-4	2011-11-13
  - 66.115.138.101	United States	PERFORMIVE	2011-09-08

[2011](https://web.archive.org/web/20110106212939/http://pondernews.net/) Farsi. [JAR](https://web.archive.org/web/20111021233539*/http://pondernews.net/reports.jar). RSS.
- [https://dnshistory.org/dns-records/pondernews.net](https://dnshistory.org/dns-records/pondernews.net) nothing
- [https://viewdns.info/iphistory/?domain=pondernews.net](https://viewdns.info/iphistory/?domain=pondernews.net). privatesystems.net.
  - 68.178.232.100	United States	AS-26496-GO-DADDY-COM-LLC	2011-11-28
  - 67.222.6.108	Atlanta - United States	PRIVATESYSTEMS	2011-10-31. Virtual. Also here on very quick look at promising names:


    - [https://web.archive.org/web/20100517070603/http://middle-east-newstoday.com/](https://web.archive.org/web/20100517070603/http://middle-east-newstoday.com/) Only at that IP. [JS](https://web.archive.org/web/20100517070625/http://middle-east-newstoday.com/kurds.js).
- [https://securitytrails.com/domain/pondernews.net/history/a](https://securitytrails.com/domain/pondernews.net/history/a)
  - 67.222.6.108 PrivateSystems Networks 2008-09-01 (17 years)	2008-09-23 (16 years)	22 days

[2010](https://web.archive.org/web/20100514160029/http://localtoglobalnews.com/) [JAR](https://web.archive.org/web/20110203005520*/http://localtoglobalnews.com/news.jar). Split header, rss.
- [https://viewdns.info/iphistory/?domain=localtoglobalnews.com](https://viewdns.info/iphistory/?domain=localtoglobalnews.com) says 212.4.17.160	Fidenza - Italy	UUNET	2011-06-22. TODO we need to check out all of 2012.4.17.\*.
  - 2012.4.17.125: worldaroundyunnan.com. [2011](https://web.archive.org/web/20110210004831/http://worldaroundyunnan.com/). Unarchived JAR: /web/20110210004831oe\_/[http://worldaroundyunnan.com/kunming.jar.](http://worldaroundyunnan.com/kunming.jar.) Chinese. rss, split header.

[2011](https://web.archive.org/web/20110202031020/http://internationalnewsworthiness.com/). English. Split header, RSS.
- [https://viewdns.info/iphistory/?domain=internationalnewsworthiness.com](https://viewdns.info/iphistory/?domain=internationalnewsworthiness.com) says 216.86.153.116	United States	STEADFAST	2011-04-04. Checking 216.86.153.106 - 216.86.153.125
  - [https://viewdns.info/reverseip/?host=216.86.153.114&t=1](https://viewdns.info/reverseip/?host=216.86.153.114&t=1) big virtual
  - [https://viewdns.info/reverseip/?host=216.86.153.116&t=1](https://viewdns.info/reverseip/?host=216.86.153.116&t=1) says it became a medium virtual
- [https://dnshistory.org/dns-records/internationalnewsworthiness.com](https://dnshistory.org/dns-records/internationalnewsworthiness.com) empty
- [https://securitytrails.com/domain/internationalnewsworthiness.com/history/a](https://securitytrails.com/domain/internationalnewsworthiness.com/history/a)
  - 68.178.232.100 GoDaddy.com, LLC 2011-04-13 (14 years)	2011-05-12 (14 years)	29 days
  - 216.86.153.116 Steadfast 2010-03-18 (15 years)	2010-09-12 (15 years)	6 months

[https://web.archive.org/web/20110202091919/http://irankhodro3026.com/](https://web.archive.org/web/20110202091919/http://irankhodro3026.com/) don't think it's a hit, too many SWFs

sandstormnews.com [2011](https://web.archive.org/web/20110208085035/http://sandstormnews.com/), [SWF](https://web.archive.org/web/20110208085820/http://sandstormnews.com/sandstormnews.swf) Arabic. `ul.rss-items > li.rss-item`, split header
- [https://viewdns.info/iphistory/?domain=sandstormnews.com](https://viewdns.info/iphistory/?domain=sandstormnews.com)
  - 68.178.232.99	United States	AS-26496-GO-DADDY-COM-LLC	2011-04-04. [https://viewdns.info/reverseip/?t=1&host=68.178.232.99](https://viewdns.info/reverseip/?t=1&host=68.178.232.99) says big virtual.
- [https://securitytrails.com/domain/sandstormnews.com/history/a](https://securitytrails.com/domain/sandstormnews.com/history/a)
  - 68.178.232.99 GoDaddy.com, LLC 2011-03-11 (14 years)	2011-04-04 (14 years)	24 days
  - 62.22.61.213 Verizon Business 2009-03-11 (16 years)	2010-03-05 (15 years)	12 months which is in range

zerosandonesnews.com [2011](https://web.archive.org/web/20110209083732/http://zerosandonesnews.com/). [SWF](https://web.archive.org/web/20110209084342/http://zerosandonesnews.com/zerosandonesnews.swf) Split header, `ul.rss-items > li.rss-item`
- [https://viewdns.info/iphistory/?domain=zerosandonesnews.com](https://viewdns.info/iphistory/?domain=zerosandonesnews.com) empty
- [https://dnshistory.org/dns-records/zerosandonesnews.com](https://dnshistory.org/dns-records/zerosandonesnews.com) empty
- [https://securitytrails.com/domain/zerosandonesnews.com/history/a](https://securitytrails.com/domain/zerosandonesnews.com/history/a) says 62.22.61.200 which is in range

differentviewtoday.com: [https://web.archive.org/web/20110202185635/http://differentviewtoday.com/](https://web.archive.org/web/20110202185635/http://differentviewtoday.com/) split header images JAR archived at: [https://web.archive.org/web/20110202185659/http://differentviewtoday.com/bwm.jar](https://web.archive.org/web/20110202185659/http://differentviewtoday.com/bwm.jar)
- [https://viewdns.info/iphistory/?domain=differentviewtoday.com](https://viewdns.info/iphistory/?domain=differentviewtoday.com) empty
- [https://dnshistory.org/dns-records/differentviewtoday.com](https://dnshistory.org/dns-records/differentviewtoday.com) empty
- [https://securitytrails.com/domain/differentviewtoday.com/history/a](https://securitytrails.com/domain/differentviewtoday.com/history/a) says
  - 66.45.179.198 TierPoint, LLC 2010-02-05 (15 years)	2011-03-17 (14 years)	1 year
  - 205.178.189.129 Network Solutions, LLC 2010-01-27 (15 years)	2010-02-05 (15 years)	9 days

lasthournews.com [https://web.archive.org/web/20100513182623/http://lasthournews.com/](https://web.archive.org/web/20100513182623/http://lasthournews.com/). Urdu. JAR at: [https://web.archive.org/web/20100513182724/http://lasthournews.com/recent.jar](https://web.archive.org/web/20100513182724/http://lasthournews.com/recent.jar). Split header images.
- [https://viewdns.info/iphistory/?domain=lasthournews.com](https://viewdns.info/iphistory/?domain=lasthournews.com) no relevant IPs
- [https://dnshistory.org/historical-dns-records/a/lasthournews.com](https://dnshistory.org/historical-dns-records/a/lasthournews.com) mentions 2010-02-27 -\> 2010-08-07 216.93.248.194
- [https://securitytrails.com/domain/lasthournews.com/history/a](https://securitytrails.com/domain/lasthournews.com/history/a) says
  - 68.178.232.100 GoDaddy.com, LLC 2010-12-21 (14 years)	2012-10-11 (12 years)	2 years
  - 216.93.248.194 TowardEX Technologies International, Inc. 2009-09-16 (15 years)	2010-01-19 (15 years)	4 months

mynepalnews.com, split header images, `ul.rss-items > li.rss-item`, Unarchived jar:
- [https://viewdns.info/iphistory/?domain=mynepalnews.com](https://viewdns.info/iphistory/?domain=mynepalnews.com)
  - 5.9.240.230	Falkenstein - Germany	Hetzner Online GmbH	2014-01-31
  - 142.4.222.67	Canada	OVH SAS	2013-12-20
  - 72.9.137.7	Nepal	WorldLink Communications Pvt Ltd	2013-06-30. Big virtual.
  - 64.71.179.79	United States	HURRICANE	2012-11-12. Nothing else on 64.71.179.71 - 64.71.179.89.

    This IP address also shows up on [https://web.archive.org/web/20110204095753/http://mynepalnews.com/cgi-bin/check.cgi/](https://web.archive.org/web/20110204095753/http://mynepalnews.com/cgi-bin/check.cgi/)

    ```
    SERVER_ADDR = 64.71.179.79
    ```

    There we also see:
    ```
    REMOTE_ADDR = 204.236.235.245
    ```
    which appears to be the crawler's IP: [https://github.com/duy13/vDDoS-Protection/issues/29](https://github.com/duy13/vDDoS-Protection/issues/29)
- [https://securitytrails.com/domain/mynepalnews.com/history/a](https://securitytrails.com/domain/mynepalnews.com/history/a)
  - 5.9.219.166 Hetzner Online GmbH 2013-12-31 (11 years)	2014-01-08 (11 years)	8 days
  - 142.4.222.67 OVH SAS 2013-12-02 (11 years)	2013-12-31 (11 years)	29 days
  - 72.9.137.7 WorldLink Communications Pvt Ltd 2013-01-24 (12 years)	2013-04-02 (12 years)	2 months
  - 64.71.179.79 Hurricane Electric LLC 2008-09-01 (17 years)	2008-10-21 (16 years)	2 months

- [https://web.archive.org/web/20111008211517/http://elgintoday.com/](https://web.archive.org/web/20111008211517/http://elgintoday.com/) wordpress so unlikely
  - 50.63.202.88	United States	AS-26496-GO-DADDY-COM-LLC	2014-02-21
  - 97.74.249.128 	United States	AS-26496-GO-DADDY-COM-LLC	2014-01-11 big virtual

**Table of contents**

- [Wakatime redirects](wakatime-redirects.md)
- [IP and DNS metadata](ip-and-dns-metadata.md)
  - [iraniangoals.com](iraniangoals-com.md)
  - [iraniangoalkicks.com](iraniangoalkicks-com.md)
  - [activegameinfo.com](activegameinfo-com.md)
  - [feedsdemexicoyelmundo.com](feedsdemexicoyelmundo-com.md)
  - [noticiasmusica.net](noticiasmusica-net.md)
  - [atomworldnews.com](atomworldnews-com.md)
  - [iranfootballsource.com](iranfootballsource-com.md)

## ↑ Ancestors (13)

1. [Methodology](methodology.md)
2. [CIA 2010 covert communication websites](../cia-2010-covert-communication-websites-split.md)
3. [Central Intelligence Agency](../central-intelligence-agency.md)
4. [American intelligence agency](../american-intelligence-agency.md)
5. [United States Intelligence Community](../united-states-intelligence-community.md)
6. [Intelligence community](../intelligence-community.md)
7. [Secret service](../secret-service.md)
8. [Espionage](../espionage.md)
9. [War](../war.md)
10. [Social science](../social-science.md)
11. [Scientific method](../scientific-method.md)
12. [Science](../science-split.md)
13. [Ciro Santilli's Homepage](../split.md)
