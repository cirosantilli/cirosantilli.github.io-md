# Wakatime redirects

↑ **Parent:** [Work log](work-log.md)

Summary: this is just a red herring. Wakatime owner likely registered the domains just after this article was published as a [publicity stunt](../publicity-stunt.md). Fair play though.

As raised at: [https://news.ycombinator.com/item?id=36280666](https://news.ycombinator.com/item?id=36280666), many, but not all, of the domains currently redirect to [https://wakatime.com/](https://wakatime.com/) as of 2023, and apparently they were taken up in 2013 (TODO how to confirm that). TODO what is the explanation for that? Some examples that do:
- [http://dedrickonline.com](http://dedrickonline.com)
- [http://tee-shot.net](http://tee-shot.net)
But some failed resolution examples:
- [http://pangawana.com/](http://pangawana.com/)
- [http://kessingerssportsnews.com/](http://kessingerssportsnews.com/)
Even more suspiciously, according to his LinkedIn: [https://www.linkedin.com/in/alanhamlett/](https://www.linkedin.com/in/alanhamlett/), the owner of Wakatime, Alan Hamlett, worked at WhiteHat Security, Inc from Aug 2011 - Sep 2013. The company was then acquired by Synopsys in 2022. Holy crap!!! As shown at: [https://web.archive.org/web/20131013193406/https://www.whitehatsec.com/](https://web.archive.org/web/20131013193406/https://www.whitehatsec.com/) that company made website security tools. Did that dude use the tools to find the vulnerabilty and then just gobble up all the domains??? What a fucking legend if he did!!!

Let's try:
- [https://host.io/redirects/wakatime.com](https://host.io/redirects/wakatime.com): failure
- [https://www.whatsmydns.net/redirect-checker?q=wakatime.com](https://www.whatsmydns.net/redirect-checker?q=wakatime.com): failure
- [https://app.neilpatel.com/en/seo_analyzer/backlinks?domain=wakatime.com&mode=domain](https://app.neilpatel.com/en/seo_analyzer/backlinks?domain=wakatime.com&mode=domain): failure

Running e.g.
```
curl -vvv dedrickonline.com
```
gives:
```
*   Trying 162.255.119.197:80...
* Connected to dedrickonline.com (162.255.119.197) port 80 (#0)
> GET / HTTP/1.1
> Host: dedrickonline.com
> User-Agent: curl/7.88.1
> Accept: */*
>
< HTTP/1.1 301 Moved Permanently
< Date: Mon, 12 Jun 2023 20:30:19 GMT
< Content-Type: text/html; charset=utf-8
< Content-Length: 55
< Connection: keep-alive
< Location: https://wakatime.com
< X-Served-By: Namecheap URL Forward
< Server: namecheap-nginx
<
<a href='https://wakatime.com'>Moved Permanently</a>.

* Connection #0 to host dedrickonline.com left intact
```
so we see that he must have setup redirection with Namecheap as mentioned at: [https://www.namecheap.com/support/knowledgebase/article.aspx/385/2237/how-to-redirect-a-url-for-a-domain/](https://www.namecheap.com/support/knowledgebase/article.aspx/385/2237/how-to-redirect-a-url-for-a-domain/)

Let's also try [DNS](../domain-name-system.md) history
- [https://whoisrequest.com/history/](https://whoisrequest.com/history/):
  - dedrickonline.com: registered: 1 Nov, 2010, dropped: 24 Nov, 2013
  - activegaminginfo.com : registered: 1 Feb, 2010, dropped: 1 Apr, 2012
- [https://tools.whoisxmlapi.com/whois-history-search](https://tools.whoisxmlapi.com/whois-history-search)
  - dedrickonline.com:
    - CIA (registrar: Godaddy, registrant name: [domainsbyproxy.com](../domains-by-proxy.md))
      - Created Date: October 27, 2010 00:00:00 UTC
      - Updated Date: October 28, 2013 00:00:00 UTC
      - Expires Date: October 27, 2014 00:00:00 UTC
    - Alan (namecheap):
      - Created Date: June 11, 2023 09:59:25 UTC
      - Expires Date: June 11, 2024 09:59:25 UTC
  - activegaminginfo.com:
    - CIA (Network Solutions, registrant name: LLC. Corral, Elizabeth|ATTN ACTIVEGAMINGINFO.COM|care of Network Solutions)
      - Created Date: January 26, 2010 00:00:00 UTC
      - Updated Date: November 27, 2010 00:00:00 UTC
      - Expires Date: January 26, 2012 00:00:00 UTC
    - Alan:
      - Created Date: June 11, 2023 09:59:40 UTC
      - Expires Date: June 11, 2024 09:59:40 UTC
  - iraniangoalkicks.com:
    - CIA (registrar: Godaddy, registrant name: [domainsbyproxy.com](../domains-by-proxy.md))
      - Created Date: April 9, 2007 00:00:00 UTC
      - Updated Date: March 2, 2011 00:00:00 UTC
      - Expires Date: April 9, 2011 00:00:00 UTC
    - Alan:
      - Created Date: June 11, 2023 09:59:20 UTC
      - Expires Date: June 11, 2024 09:59:20 UTC
  - iraniangoals.com:
    - CIA (registrar: Godaddy, registrant name: [domainsbyproxy.com](../domains-by-proxy.md)):
      - Created Date: March 6, 2008 00:00:00 UTC
      - Updated Date: March 7, 2011 00:00:00 UTC
      - Expires Date: March 6, 2014 00:00:00 UTC
    - Reuters:
      - Created Date: September 29, 2022 11:16:09 UTC
      - Updated Date: September 29, 2022 11:16:09 UTC
      - Expires Date: September 29, 2023 11:16:09 UTC

So these suggest Alan might have just come along in 2023 way after the 2022 Reuters article and did the same basic IP range search that Ciro is doing now, so possibly no new tech. Let's ask... [https://twitter.com/cirosantilli/status/1668369786865164289](https://twitter.com/cirosantilli/status/1668369786865164289)

The domain name history presented is however of interest, and could lead to patterns being found.

Searching [https://tools.whoisxmlapi.com/reverse-whois-search](https://tools.whoisxmlapi.com/reverse-whois-search) with term "Corral, Elizabeth" gave no results unfortunately.

Basic search under [https://tools.whoisxmlapi.com/reverse-whois-search](https://tools.whoisxmlapi.com/reverse-whois-search) for "Corral" also empty. They can't see their own data? Ah, need advanced. Marked "Historic" and selected "Corral, Elizabeth", ony one hit, activegaminginfo.com.

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
