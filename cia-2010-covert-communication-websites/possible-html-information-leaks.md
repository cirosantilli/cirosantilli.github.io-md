# Possible HTML information leaks

↑ **Parent:** [Results](results.md)

<a id="_4481"></a>
This section is about possible "real-world" information leaks found in the HTML of the pages. Domain [DNS metadata](ip-and-dns-metadata.md) may of course expose more, and is more likely to do so, this section is only about in-page findings, notably in the HTML.

<a id="_4482"></a>
We haven't found anything too mind-blowying so far, but the ones we have are curious.

<a id="_4483"></a>
The HTML `<title>` of [webofcheer.com](https://web.archive.org/web/20110207150839/http://webofcheer.com/) is cryptically set as:<a id="_4484"></a>

```
pg1c
```
rather than a more natural title like "Web of cheer" as is the case for the other website. This feels like a forgotten placeholder for an internal page identifier, e.g. "page 1C" sounds plausible. At [Section "HTML title element"](html-title-element.md) we riefly inspected the `<title>` of every other hit with a wayback machine archive, and unfortunately none other seemed to have any such interesting title.

<a id="_4485"></a>
The [2010 archive of europeantravelcafe.com](https://web.archive.org/web/20100724024623/http://www.europeantravelcafe.com/) has a "plan your trip" link links to a different domain: [https://secure-cert.net/~etc/transport.html](https://secure-cert.net/~etc/transport.html). This appears to have been a link to the system used by CIA operators to manage the website. Furthermore, the link then was later [removed from the 2011 version](https://web.archive.org/web/20110201192245/http://europeantravelcafe.com/), so it was almost certainly a leak! "secure-cert.net" is obscure, the only other surviving online mention of it is [https://www.leewillis.co.uk/wordpress-plugins/#comment-6513](https://www.leewillis.co.uk/wordpress-plugins/#comment-6513) to  
[http://secure-cert.net/~sayitint/products-page/bags-totes/duffel-bag/](http://secure-cert.net/~sayitint/products-page/bags-totes/duffel-bag/) We've grepped all the HTML downloaded as [HTML analysis](html-analysis.md) but no other links to it were found.

<a id="image-2010-wayback-machine-archive-of-www-europeantravelcafe-com-with-plan-your-trip-highlighted-by-us"></a>
<img src="https://github.com/cirosantilli/media/blob/master/cia-2010-covert-communication-websites/screenshots/www.europeantravelcafe.com-arrow.jpg?raw=true" alt="" height="1024">

**[Figure 37](#image-2010-wayback-machine-archive-of-www-europeantravelcafe-com-with-plan-your-trip-highlighted-by-us). 2010 Wayback Machine archive of www.europeantravelcafe.com with "plan your trip" highlighted by us**. [Source](https://web.archive.org/web/20100724024623/http://www.europeantravelcafe.com/).

<a id="_4486"></a>
A similar thing happened to alljohnny.com Starting [December 2004](https://web.archive.org/web/20041215182457/http://alljohnny.com/index.html) the "Submit your favorite carlson quote" was mind blowingly switched to point to [https://washington.serversecured.net/~alljohnn/cgi-bin/memlog.cgi](https://web.archive.org/web/20050328224840/https://washington.serversecured.net/~alljohnn/cgi-bin/memlog.cgi) thus likely leaking the control site URL. Beauty. It previously pointed to the more sensible: [https://web.archive.org/web/20040901162621/https://secure.alljohnny.com/cgi-bin/memlog.cgi](https://web.archive.org/web/20040901162621/https://secure.alljohnny.com/cgi-bin/memlog.cgi)

## ↑ Ancestors (13)

1. [Results](results.md)
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

- [HTML title element](html-title-element.md)
