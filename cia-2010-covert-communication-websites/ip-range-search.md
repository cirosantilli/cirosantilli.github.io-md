# IP range search

↑ **Parent:** [Methodology](methodology.md)

One promising way to find more of those would be with [IP](../ip-address.md) searches, since it was stated in the [Reuters article](reuters-article.md) that the [CIA](../central-intelligence-agency.md) made the terrible mistake of using several contiguous IP blocks for those website. What a phenomenal [OPSEC](../operations-security.md) failure!!!

The easiest way would be if [Wayback Machine](wayback-machine.md) itself had an IP search function, but we couldn't find one: [Search Wayback Machine by IP](../search-wayback-machine-by-ip.md).

[https://viewdns.info](https://viewdns.info) was the first easily accessible website that [Ciro Santilli](../ciro-santilli-split.md) could find that contained such information.

Our current results indicate that the typical IP range is about 30 IPs wide.

E.g. searching: [https://viewdns.info/iphistory](https://viewdns.info/iphistory) and considering only hits from 2011 or earlier we obtain:
- capture-nature.com
  - 65.61.127.163 - Greenacres - United States - TierPoint - 2013-10-19
- activegaminginfo.com
  - 66.175.106.148 - United States - Verizon Business - 2012-03-03
- iraniangoals.com
  - 68.178.232.100 - United States - GoDaddy.com - 2011-11-13
  - 69.65.33.21 - Flushing - United States - GigeNET - 2011-09-08
- rastadirect.net
  - 68.178.232.100 - United States - GoDaddy.com - 2011-05-02
- iraniangoalkicks.com
  - 68.178.232.100 - United States - GoDaddy.com - 2011-04-04
- headlines2day.com
  - 118.139.174.1 - Singapore - Web Hosting Service - 2013-06-30. Source: viewdns.info
  - 184.168.221.91 2013-08-12T06:17:39. Source: [2013 DNS Census](dns-census-2013.md) grep
- fightwithoutrules.com
  - 204.11.56.25 - British Virgin Islands - Confluence Networks Inc - 2013-09-26
  - 208.91.197.19 - British Virgin Islands - Confluence Networks Inc - 2013-05-20
  - 212.4.17.38 - Milan - Italy - MCI Worldcom Italy Spa - 2012-03-03
- fitness-dawg.com
  - 219.90.62.243 - Taiwan - Verizon Taiwan Co. Limited - 2012-01-11

Neither of these seem to be in the same ranges, the only common nearby hit amongst these ranges is the exact `68.178.232.100`, and doing reverse IP search at [https://viewdns.info/reverseip/?host=68.178.232.100&t=1](https://viewdns.info/reverseip/?host=68.178.232.100&t=1) states that it has 2.5 million hostnames associated to it, so it must be some kind of [Shared web hosting service](https://en.wikipedia.org/wiki/Shared_web_hosting_service), see also: [https://superuser.com/questions/577070/is-it-possible-for-many-domain-names-to-share-one-ip-address](https://superuser.com/questions/577070/is-it-possible-for-many-domain-names-to-share-one-ip-address), which makes search hard.

Ciro then tried some of the other IPs, and soon hit gold.

Initially, Ciro started by doing manual queries to viewdns.info/reversip until his IP was blocked. Then he created an account and used his 250 free queries with the following helper script: [cia-2010-covert-communication-websites/viewdns-info.sh](cia-2010-covert-communication-websites/viewdns-info.sh). The output of that script can be seen at: [https://github.com/cirosantilli/media/blob/master/cia-2010-covert-communication-websites/viewdns-info.sh](https://github.com/cirosantilli/media/blob/master/cia-2010-covert-communication-websites/viewdns-info.sh).

Ciro then found [2013 DNS Census](dns-census-2013.md) which contained data highly disjoint form the viewdns-info one!

Summaries of the IP range exploration done so far follows, combined data from all databases above.

**Table of contents**

- [Hits without nearby IP hits](hits-without-nearby-ip-hits.md)
  - [Possible hits](possible-hits.md)
- [Hits with nearby IP hits](hits-with-nearby-ip-hits.md)

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

## ← Incoming links (1)

- [List of websites](list-of-websites.md)
