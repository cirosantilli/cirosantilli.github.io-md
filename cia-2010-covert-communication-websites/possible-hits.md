# Possible hits

↑ **Parent:** [Hits without nearby IP hits](hits-without-nearby-ip-hits.md)

Likely hits possible but whose archives is too broken to be easily certain. If:
- [nearby IP hits](hits-without-nearby-ip-hits.md)
- proper reverse engineering of their comms if any, or any other page fingerprints
were to ever be found, these would be considered hits.

- 216.97.231.56 nouvelles-d-aujourdhuis.com. [2011](https://web.archive.org/web/20110128173431/http://nouvelles-d-aujourdhuis.com/). Stylistically perfect, but no nearby IP hits. [domainsbyproxy.com](../domains-by-proxy.md). Maybe looking into HTML would help confirm:
  - `rss-items`
  But wrong IP? likely [CGI comms variant](cgi-comms-variant.md) under the signup page: [https://web.archive.org/web/20090405045548/http://nouvelles-d-aujourdhuis.com/members.html](https://web.archive.org/web/20090405045548/http://nouvelles-d-aujourdhuis.com/members.html).

  Tested [viewdns.info](viewdns-info.md) range: 216.97.231.46 - 216.97.231.66. Not a single reverse IP hit in there.

  [viewdns.info](viewdns-info.md) also assigns it 50.63.202.46, GoDaddy.com, LLC, 2013-11-08 in addition to 216.97.231.56, Canada, IPXO LLC, 2013-09-06. This is very near other iranfootballsource.com flukes, so likely useless.

  [securitytrails.com](securitytrails-com.md) also gives it one earlier IP 209.200.240.250 last seen 2008-09-20: [https://securitytrails.com/domain/nouvelles-d-aujourdhuis.com/history/a](https://securitytrails.com/domain/nouvelles-d-aujourdhuis.com/history/a) Hydra Communications Ltd before 216.97.231.56 "ASU doctor" first seen 2008-09-20 (15 years)\> Tested viewdns.info range: 209.200.240.240 - 209.200.240.260 empty at the time of interest.

  Marked copyright 2006, so mega early.

africainnews.com
- no archives of the HTML. [https://dawhois.com/www/africainnews.com.html](https://dawhois.com/www/africainnews.com.html) somewhat in-style but unclear.
- [SWF](https://web.archive.org/web/20110202135525/http://africainnews.com/africainnews.swf). A reverse engineering of the SWF should be able to confirm.
- [https://web.archive.org/web/20111007194814/http://africainnews.com/robots.txt](https://web.archive.org/web/20111007194814/http://africainnews.com/robots.txt)
- [https://dnshistory.org/historical-dns-records/a/africainnews.com](https://dnshistory.org/historical-dns-records/a/africainnews.com)
  - 2009-12-29 -\> 2010-07-28 72.167.232.43. Tested viewdns.info range: 72.167.232.33 - 72.167.232.53. Several virtual hosts there. [https://viewdns.info/reverseip/?t=1&host=72.167.232.43](https://viewdns.info/reverseip/?t=1&host=72.167.232.43) medium virtual haven't bothered to explore much
  - 2011-10-14 -\> 2011-10-14 68.178.232.100 virtual
  - 2012-08-12 -\> 2012-08-12 97.74.42.79. Tested viewdns.info range: 97.74.42.69 - 97.74.42.89
    - 97.74.42.74: landtex.net 2023-03-22
    - 97.74.42.76: solidasshonky.com 2023-03-07
    - 97.74.42.77: solidasshonky.com 2023-03-07
    - 97.74.42.78: blakebrothers.co 2018-05-05
    - 97.74.42.78: learningjbe.com 2023-02-02
    - 97.74.42.78: solidasshonky.com 2023-03-07
    - 97.74.42.78: sourceuae.com 2023-03-07
    - 97.74.42.78: superiorfoodservicesales.com 2017-09-10
    - 97.74.42.79: large virtual
    - 97.74.42.80: waiasialtd.com 2016-10-17
- [https://viewdns.info/iphistory/?domain=africainnews.com](https://viewdns.info/iphistory/?domain=africainnews.com)
  - 50.63.202.92	United States	AS-26496-GO-DADDY-COM-LLC	2013-06-30. Likely large virtual.
  - 97.74.42.79	United States	AS-26496-GO-DADDY-COM-LLC	2013-05-20. tested.
  - 68.178.232.100	United States	AS-26496-GO-DADDY-COM-LLC	2012-06-29 virtual
  - 68.178.232.99	United States	AS-26496-GO-DADDY-COM-LLC	2011-11-13
  - 68.178.232.100	United States	AS-26496-GO-DADDY-COM-LLC	2011-10-09 virtual
  - 72.167.232.43	United States	GO-DADDY-COM-LLC	2011-09-08. Tested.

globalsentinelsite.com. [https://dawhois.com/www/globalsentinelsite.com.html](https://dawhois.com/www/globalsentinelsite.com.html) empty. Copyright 2011 on top and 2008 on bottom. Unusually wide, has a few sections, but somewhat shallow. Copyright 2008. JAR [JAR](https://web.archive.org/web/20110201094846/http://globalsentinelsite.com/steps.jar). a.rss-item
- [https://dnshistory.org/historical-dns-records/a/globalsentinelsite.com](https://dnshistory.org/historical-dns-records/a/globalsentinelsite.com) 2010-02-13 -\> 2010-08-04 74.124.210.249 unknown
- [https://viewdns.info/iphistory/?domain=globalsentinelsite.com](https://viewdns.info/iphistory/?domain=globalsentinelsite.com)
  - 74.124.210.249	United States	INMOTION	2011-11-13 unknown [https://viewdns.info/reverseip/?host=74.124.210.249&t=1](https://viewdns.info/reverseip/?host=74.124.210.249&t=1) has 347 hits
- JAR file structure:
  ```
  ./META-INF/MANIFEST.MF
  ./META-INF/WORLD.DSA
  ./META-INF/WORLD.SF
  ./global
  ./global/applet
  ./global/applet/A.class
  ./global/applet/Aa.class
  ./resource/resources.bin
  ```

  with:
  ```
  Manifest-Version: 1.0
  Created-By: 1.4.2_15-b02 (Sun Microsystems Inc.)
  Ant-Version: Apache Ant 1.6.5

  Name: global/applet/Bs.class
  SHA1-Digest: R1qrWUT6kYTLKa6TSmyWbBhLQSw=

  Name: global/applet/Ay.class
  SHA1-Digest: L0xOVdhBzEcmW8czjERAVH+tNyI=
  ```

todaysolar.com. This might just be legit, but keeping it around just in case.
- [2011](https://web.archive.org/web/20110207094740/http://todaysolar.com/)
- [JAR](https://web.archive.org/web/20110207094748/http://todaysolar.com/AdBannerDeploy.jar)
- [https://dnshistory.org/historical-dns-records/a/todaysolar.com](https://dnshistory.org/historical-dns-records/a/todaysolar.com) 2009-08-11 -\> 2011-03-01 74.208.62.112 unknown
- [https://viewdns.info/iphistory/?domain=todaysolar.com](https://viewdns.info/iphistory/?domain=todaysolar.com) 74.208.62.112	United States	PROFITBRICKS-USA	2012-11-12

## ↑ Ancestors (15)

1. [Hits without nearby IP hits](hits-without-nearby-ip-hits.md)
2. [IP range search](ip-range-search.md)
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
