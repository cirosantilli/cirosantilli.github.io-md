# Communication mechanism

↑ **Parent:** [Reverse engineering](reverse-engineering.md)

<a id="_6429"></a>
There are four main types of communication mechanisms found:<a id="_6430"></a>

<a id="_6431"></a>
- <a id="_6432"></a>
  [Java](../java-programming-language.md) [JAR](../jar-file-format.md)

  <a id="_6433"></a>
  There is also one known instance where a .zip extension was used! [https://web.archive.org/web/20131101104829*/http://plugged-into-news.net/weatherbug.zip](https://web.archive.org/web/20131101104829*/http://plugged-into-news.net/weatherbug.zip) as:<a id="_6434"></a>

  ```
  <applet codebase="/web/20101229222144oe_/http://plugged-into-news.net/" archive="/web/20101229222144oe_/http://plugged-into-news.net/weatherbug.zip"
  ```

  <a id="_6435"></a>
  JAR is the most common comms, and one of the most distinctive, making it a great [fingerprint](fingerprints.md).

  <a id="_6436"></a>
  Several of the JAR files are named something like either:<a id="_6437"></a>

  <a id="_6438"></a>
  - meter.jar
  <a id="_6439"></a>
  - bandwidth.jar
  <a id="_6440"></a>
  - speed.jar
  as if to pose as Internet speed testing tools? The wonderful subtleties of the late 2000s Internet are a bit over our heads.

  <a id="_6441"></a>
  All JARs are directly under root, not in subdirectories, and the basename usually consist of one word, though sometimes two camel cased.
<a id="_6442"></a>
- [JavaScript](../javascript.md) file. There are two subtypes:<a id="_6443"></a>

  <a id="_6444"></a>
  - [JavaScript with SHAs](javascript-with-shas.md). Rare. Likely older. Way more fingerprintable.
  <a id="_6445"></a>
  - JavaScript without SHAs. They have all been obfuscated slightly different and compressed. But the file sizes are all very similar from 8kB to 10kB, and they all look similar, so visually it is very easy to detect a match with good likelyhood.
<a id="_6446"></a>
- <a id="_6447"></a>
  [Adobe Flash](../adobe-flash.md) swf file. In all instances found so far, the name of the SWF matches the name of the second level domain exactly, e.g.:<a id="_6448"></a>

  ```
  http://tee-shot.net/tee-shot.swf
  ```
  While this is somewhat of a fingerprint, it is worth noting that is was a relatively commonly used pattern. But it is also the rarest of the mechanisms. This is a at a dissonance with the rest of the web, which circa 2010 already had way more SWF than JAR apparently.

  <a id="_6449"></a>
  Some of the SWF websites have archives for empty `/servlet` pages:<a id="_6450"></a>

  ```
  ./bailsnboots.com/20110201234509/servlet/teammate/index.html
  ./currentcommunique.com/20110130162713/servlet/summer/index.html
  ./mynepalnews.com/20110204095758/servlet/SnoopServlet/index.html
  ./mynepalnews.com/20110204095403/servlet/release/index.html
  ./www.hassannews.net/20101230175421/servlet/jordan/index.html
  ./zerosandonesnews.com/20110209084339/servlet/technews/index.html
  ```
  which makes us think that it is a part of the SWF system.
<a id="_6451"></a>
- [CGI comms](cgi-comms.md)
These have short single word names with some meaning linked to their website.

<a id="_6452"></a>
Because the communication mechanisms are so crucial, they tend to be less varied, and serve as very good fingerprints. It is not ludicrous, e.g. identical files, but one look at a few and you will know the others.

**Table of contents**

- [CGI comms](cgi-comms.md)
  - [CGI comms variant](cgi-comms-variant.md)
  - [SSL certificate](ssl-certificate.md)
- [JAR reverse engineering](jar-reverse-engineering.md)
- [JS comms](js-comms.md)
  - [JavaScript reverse engineering](javascript-reverse-engineering.md)
    - [JavaScript with SHAs](javascript-with-shas.md)
      - [iraniangoals.com JavaScript reverse engineering](iraniangoals-com-javascript-reverse-engineering.md)
    - [feedsdemexicoyelmundo.com JavaScript reverse engineering](feedsdemexicoyelmundo-com-javascript-reverse-engineering.md)

## ↑ Ancestors (14)

1. [Reverse engineering](reverse-engineering.md)
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

## ← Incoming links (5)

- [Fingerprints](fingerprints.md)
- [List of websites](list-of-websites.md)
- [Overview of Ciro Santilli's investigation](overview-of-ciro-santilli-s-investigation.md)
- [Timeline of public disclosures](timeline-of-public-disclosures.md)
- [44 new CIA websites](../updates/44-new-cia-websites.md)
