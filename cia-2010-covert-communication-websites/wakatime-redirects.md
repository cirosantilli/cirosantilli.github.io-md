# Wakatime redirects

↑ **Parent:** [Work log](work-log.md)

<a id="_7060"></a>
Summary: this is just a red herring. Wakatime owner likely registered the domains just after this article was published as a [publicity stunt](../publicity-stunt.md). Fair play though.

<a id="_7061"></a>
As raised at: [https://news.ycombinator.com/item?id=36280666](https://news.ycombinator.com/item?id=36280666), many, but not all, of the domains currently redirect to [https://wakatime.com/](https://wakatime.com/) as of 2023, and apparently they were taken up in 2013 (TODO how to confirm that). TODO what is the explanation for that? Some examples that do:<a id="_7062"></a>

<a id="_7063"></a>
- [http://dedrickonline.com](http://dedrickonline.com)
<a id="_7064"></a>
- [http://tee-shot.net](http://tee-shot.net)
But some failed resolution examples:<a id="_7065"></a>

<a id="_7066"></a>
- [http://pangawana.com/](http://pangawana.com/)
<a id="_7067"></a>
- [http://kessingerssportsnews.com/](http://kessingerssportsnews.com/)
Even more suspiciously, according to his LinkedIn: [https://www.linkedin.com/in/alanhamlett/](https://www.linkedin.com/in/alanhamlett/), the owner of Wakatime, Alan Hamlett, worked at WhiteHat Security, Inc from Aug 2011 - Sep 2013. The company was then acquired by Synopsys in 2022. Holy crap!!! As shown at: [https://web.archive.org/web/20131013193406/https://www.whitehatsec.com/](https://web.archive.org/web/20131013193406/https://www.whitehatsec.com/) that company made website security tools. Did that dude use the tools to find the vulnerabilty and then just gobble up all the domains??? What a fucking legend if he did!!!

<a id="_7068"></a>
Let's try:<a id="_7069"></a>

<a id="_7070"></a>
- [https://host.io/redirects/wakatime.com](https://host.io/redirects/wakatime.com): failure
<a id="_7071"></a>
- [https://www.whatsmydns.net/redirect-checker?q=wakatime.com](https://www.whatsmydns.net/redirect-checker?q=wakatime.com): failure
<a id="_7072"></a>
- [https://app.neilpatel.com/en/seo_analyzer/backlinks?domain=wakatime.com&mode=domain](https://app.neilpatel.com/en/seo_analyzer/backlinks?domain=wakatime.com&mode=domain): failure

<a id="_7073"></a>
Running e.g.<a id="_7074"></a>

```
curl -vvv dedrickonline.com
```
gives:<a id="_7075"></a>

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

<a id="_7076"></a>
Let's also try [DNS](../domain-name-system.md) history<a id="_7077"></a>

<a id="_7078"></a>
- [https://whoisrequest.com/history/](https://whoisrequest.com/history/):<a id="_7079"></a>

  <a id="_7080"></a>
  - dedrickonline.com: registered: 1 Nov, 2010, dropped: 24 Nov, 2013
  <a id="_7081"></a>
  - activegaminginfo.com : registered: 1 Feb, 2010, dropped: 1 Apr, 2012
<a id="_7082"></a>
- [https://tools.whoisxmlapi.com/whois-history-search](https://tools.whoisxmlapi.com/whois-history-search)<a id="_7083"></a>

  <a id="_7084"></a>
  - dedrickonline.com:<a id="_7085"></a>

    <a id="_7086"></a>
    - CIA (registrar: Godaddy, registrant name: [domainsbyproxy.com](../domains-by-proxy.md))<a id="_7087"></a>

      <a id="_7088"></a>
      - Created Date: October 27, 2010 00:00:00 UTC
      <a id="_7089"></a>
      - Updated Date: October 28, 2013 00:00:00 UTC
      <a id="_7090"></a>
      - Expires Date: October 27, 2014 00:00:00 UTC
    <a id="_7091"></a>
    - Alan (namecheap):<a id="_7092"></a>

      <a id="_7093"></a>
      - Created Date: June 11, 2023 09:59:25 UTC
      <a id="_7094"></a>
      - Expires Date: June 11, 2024 09:59:25 UTC
  <a id="_7095"></a>
  - activegaminginfo.com:<a id="_7096"></a>

    <a id="_7097"></a>
    - CIA (Network Solutions, registrant name: LLC. Corral, Elizabeth|ATTN ACTIVEGAMINGINFO.COM|care of Network Solutions)<a id="_7098"></a>

      <a id="_7099"></a>
      - Created Date: January 26, 2010 00:00:00 UTC
      <a id="_7100"></a>
      - Updated Date: November 27, 2010 00:00:00 UTC
      <a id="_7101"></a>
      - Expires Date: January 26, 2012 00:00:00 UTC
    <a id="_7102"></a>
    - Alan:<a id="_7103"></a>

      <a id="_7104"></a>
      - Created Date: June 11, 2023 09:59:40 UTC
      <a id="_7105"></a>
      - Expires Date: June 11, 2024 09:59:40 UTC
  <a id="_7106"></a>
  - iraniangoalkicks.com:<a id="_7107"></a>

    <a id="_7108"></a>
    - CIA (registrar: Godaddy, registrant name: [domainsbyproxy.com](../domains-by-proxy.md))<a id="_7109"></a>

      <a id="_7110"></a>
      - Created Date: April 9, 2007 00:00:00 UTC
      <a id="_7111"></a>
      - Updated Date: March 2, 2011 00:00:00 UTC
      <a id="_7112"></a>
      - Expires Date: April 9, 2011 00:00:00 UTC
    <a id="_7113"></a>
    - Alan:<a id="_7114"></a>

      <a id="_7115"></a>
      - Created Date: June 11, 2023 09:59:20 UTC
      <a id="_7116"></a>
      - Expires Date: June 11, 2024 09:59:20 UTC
  <a id="_7117"></a>
  - iraniangoals.com:<a id="_7118"></a>

    <a id="_7119"></a>
    - CIA (registrar: Godaddy, registrant name: [domainsbyproxy.com](../domains-by-proxy.md)):<a id="_7120"></a>

      <a id="_7121"></a>
      - Created Date: March 6, 2008 00:00:00 UTC
      <a id="_7122"></a>
      - Updated Date: March 7, 2011 00:00:00 UTC
      <a id="_7123"></a>
      - Expires Date: March 6, 2014 00:00:00 UTC
    <a id="_7124"></a>
    - Reuters:<a id="_7125"></a>

      <a id="_7126"></a>
      - Created Date: September 29, 2022 11:16:09 UTC
      <a id="_7127"></a>
      - Updated Date: September 29, 2022 11:16:09 UTC
      <a id="_7128"></a>
      - Expires Date: September 29, 2023 11:16:09 UTC

<a id="_7129"></a>
So these suggest Alan might have just come along in 2023 way after the 2022 Reuters article and did the same basic IP range search that Ciro is doing now, so possibly no new tech. Let's ask... [https://twitter.com/cirosantilli/status/1668369786865164289](https://twitter.com/cirosantilli/status/1668369786865164289)

<a id="_7130"></a>
The domain name history presented is however of interest, and could lead to patterns being found.

<a id="_7131"></a>
Searching [https://tools.whoisxmlapi.com/reverse-whois-search](https://tools.whoisxmlapi.com/reverse-whois-search) with term "Corral, Elizabeth" gave no results unfortunately.

<a id="_7132"></a>
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
