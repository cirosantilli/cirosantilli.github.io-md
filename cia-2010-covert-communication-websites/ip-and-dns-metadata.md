# IP and DNS metadata

↑ **Parent:** [Work log](work-log.md)

Some dumps from us looking for patterns, but could not find any.

Sources of whois history include:
- [https://whois-history.whoisxmlapi.com/](https://whois-history.whoisxmlapi.com/) from [whoisXMLAPI](../whoisxmlapi.md). Notably they also have historical reverse WHOIS... [https://tools.whoisxmlapi.com/reverse-whois-search](https://tools.whoisxmlapi.com/reverse-whois-search) but it needs credits. TODO we need to squeeze this a but further at some point.

When that data comes in JSON format as from [whoisXMLAPI](../whoisxmlapi.md), we are going to just dump it in [https://github.com/cirosantilli/media/blob/master/cia-2010-covert-communication-websites/whois.json](https://github.com/cirosantilli/media/blob/master/cia-2010-covert-communication-websites/whois.json)

The vast majority of domains seem to be registered either via [domainsbyproxy.com](../domains-by-proxy.md) which likely intgrates with Godaddy and is widely used, and seems to give zero infromation at all about the registrar.

A much smaller number however uses other methods, some of which sometimes leak a little bit of data:
- [Network Solutions, LLC](../network-solutions.md). These sometimes give a tiny bit of information: one name. Other times they are hidden behind Perfect Privacy, LLC. Examples\>
  - alljohnny.net: L. Glaze. [https://tools.whoisxmlapi.com/reverse-whois-search](https://tools.whoisxmlapi.com/reverse-whois-search) "Glaze, L." has
    - webstorageforme.com. [https://web.archive.org/web/20130917230604/http://webstorageforme.com/](https://web.archive.org/web/20130917230604/http://webstorageforme.com/) broken, [http://cqcounter.com/whois/www/webstorageforme.com.html](http://cqcounter.com/whois/www/webstorageforme.com.html) blank
    - welcometonyc.net. Hit!
    - international-smallbusiness.com. Same IP as alljohnny.net and quite possibly hit..
    - alljohnny.com. Hit!
    - locateontheweb.com. [http://cqcounter.com/whois/www/locateontheweb.com.html](http://cqcounter.com/whois/www/locateontheweb.com.html) broken/test page
    - rolling-in-rapids.com. [https://web.archive.org/web/20111101080224/rolling-in-rapids.com](https://web.archive.org/web/20111101080224/rolling-in-rapids.com) no archives but [http://cqcounter.com/whois/www/rolling-in-rapids.com.html](http://cqcounter.com/whois/www/rolling-in-rapids.com.html) hit style! [https://viewdns.info/iphistory/?domain=rolling-in-rapids.com](https://viewdns.info/iphistory/?domain=rolling-in-rapids.com) puts it at:
      - 208.91.197.132	British Virgin Islands	CONFLUENCE-NETWORK-INC	2014-01-31
      - 65.218.91.9	United States	UUNET	2013-12-20 so matchwith welcometonyc.com but not listed at [https://viewdns.info/reverseip/?t=1&host=65.218.91.9](https://viewdns.info/reverseip/?t=1&host=65.218.91.9) because of the [viewdns.info reverse IP bug](../viewdns-info-reverse-ip-bug.md)!
  - differentviewtoday.com: [https://tools.whoisxmlapi.com/whois-history-search](https://tools.whoisxmlapi.com/whois-history-search) kind of empty no name

  Pulley, Tammy
  - golf-on-holiday.com: Pulley, Tammy. No [https://tools.whoisxmlapi.com/whois-history-search](https://tools.whoisxmlapi.com/whois-history-search) reverse hits.
  - intoworldnews.com: Benjamin McGrew. Only that hit for reverse name at [https://tools.whoisxmlapi.com/reverse-whois-search](https://tools.whoisxmlapi.com/reverse-whois-search)
  - magneticfieldnews.com: Sarah Lowell [https://tools.whoisxmlapi.com/reverse-whois-search](https://tools.whoisxmlapi.com/reverse-whois-search) has 9 domains
    - sarahlowell.com: [https://web.archive.org/web/20110208130657/http://sarahlowell.com/](https://web.archive.org/web/20110208130657/http://sarahlowell.com/) Yoga instructor.
    - puppychallengesacademy.com
    - sarahlowelldogtraining.com
    - puppychallenges.com. [https://web.archive.org/web/20130517151924/http://puppychallenges.com/](https://web.archive.org/web/20130517151924/http://puppychallenges.com/) wordpress.
    - puppychallenges.net
    - realwomensduathlon.com. No archives of era: [https://web.archive.org/web/20180808101430/http://realwomensduathlon.com/](https://web.archive.org/web/20180808101430/http://realwomensduathlon.com/)
    - magneticfieldnews.com. Hit.
    - highflyingagility.com. Legit? Service offer.
    - ropies.com. [https://web.archive.org/web/20111101080224/http://ropies.com/](https://web.archive.org/web/20111101080224/http://ropies.com/)
  - medicatechinfo.com: Jason Noll. Has the following hits at [https://tools.whoisxmlapi.com/reverse-whois-search](https://tools.whoisxmlapi.com/reverse-whois-search)
    - dreamschemedesigns.com. Legit
    - dreamschemedesigns.net
    - aviationturbinesinternational.com. No relevant archives.
    - garysluhan.com. Seems legit.
    - cjlogic.com: registrar Godaddy (not Network Services!) and contact:
      ```
      Noll, Jason  noll.jason@gmail.com
      104 Southridge Ct.
      Marthasville, Missouri 63357
      United States
      (660) 441-0780      Fax --
      ```

      This image is his Gmail's current profile image as of 2025: [https://openclipart.org/detail/19437/high-wing-airplane](https://openclipart.org/detail/19437/high-wing-airplane)
    - medicatechinfo.com. Hit.
    - health-men-today.com. Hit. Holy fuck it has two hits out of 7!!!
  - mydailynewsreport.com: Rebecca Melancon on [https://tools.whoisxmlapi.com/reverse-whois-search](https://tools.whoisxmlapi.com/reverse-whois-search):
    - rebecca-melancon.com. [https://web.archive.org/web/20180808172531/http://rebecca-melancon.com/](https://web.archive.org/web/20180808172531/http://rebecca-melancon.com/) pilates teacher
    - swlabuyahome.net
    - swlalistmyhome.net
    - rebeccaworking4yousite.com
    - mylakecharlescityguide.com
    - swlalistmyhome.com
    - rebeccaworking4you.com
    - swlabuyahome.com
    - calcasieuhouses.com [https://web.archive.org/web/20111013212502/http://calcasieuhouses.com/.](https://web.archive.org/web/20111013212502/http://calcasieuhouses.com/.) Wordpress. Copyright Rebecca Melancon, Equal Housing Opportunity.> Message from Rebecca

      > 

      > Welcome to Calcasieu Houses! Here you will find not only information about Real Estate in Calcasieu Parish & the Lake Charles area, but also information about the area itself. I am constantly adding content so please check back often. I can help you with relocation, buying, selling, as well as looking for a great restaurant or a new activity to do! There will be information on Lake Charles, Sulphur, Westlake, & Moss Bluff. If you have something you would like to see added to the website, please feel free to contact me!
    - mydailynewsreport.com. Hit.
  - plugged-into-news.net: Godfrey Hubbard. Searching [https://tools.whoisxmlapi.com/reverse-whois-search](https://tools.whoisxmlapi.com/reverse-whois-search) for two terms "Godfrey" "Hubbard" gives a small list of 20 domains including plugged-into-news.net. They all appear to have both words in them. Searching just "Hubbard, Godfrey" has only 3 hits:
    - hubbardgodfrey.online
    - plugged-into-news.net
    - hubbardgodfrey.com

    so it seems to match the strings exactly!

  but presumably these are the names of employees of the company? We are yet to see two identical names however, which also suggests fake names. Network Solutions appears to offer both hosting and domain registration, and the CIA seems to have used this service combo a lot.
- godaddy without [domainsbyproxy.com](../domains-by-proxy.md): a few of the websites are registered in Godaddy without domainsbyproxy. These might be the ones that gives out the most information:
  - baocontact.com
Big question: [https://webmasters.stackexchange.com/questions/13237/how-do-you-view-domain-whois-history](https://webmasters.stackexchange.com/questions/13237/how-do-you-view-domain-whois-history) [DomainTools](domaintools.md) also has it.

How on Earth did did Citizen Labs find what seems to be a DNS fingerprint??? Are there simply some very rare badly registered domains? What did they see!

**Table of contents**

- [iraniangoals.com](iraniangoals-com.md)
- [iraniangoalkicks.com](iraniangoalkicks-com.md)
- [activegameinfo.com](activegameinfo-com.md)
- [feedsdemexicoyelmundo.com](feedsdemexicoyelmundo-com.md)
- [noticiasmusica.net](noticiasmusica-net.md)
- [atomworldnews.com](atomworldnews-com.md)
- [iranfootballsource.com](iranfootballsource-com.md)

## ↑ Ancestors (14)

1. [Work log](work-log.md)
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

- [CIA 2010 covert communication websites](../cia-2010-covert-communication-websites-split.md)
- [List of websites](list-of-websites.md)
- [Possible HTML information leaks](possible-html-information-leaks.md)
- [Timeline of public disclosures](timeline-of-public-disclosures.md)
