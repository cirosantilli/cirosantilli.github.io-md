# HTML analysis

↑ **Parent:** [Fingerprints](fingerprints.md)

<a id="_4586"></a>
The HTML from the index page of Wayback Machine were:<a id="_4587"></a>

<a id="_4588"></a>
- dumped at: [https://github.com/cirosantilli/media/tree/master/cia-2010-covert-communication-websites/html](https://github.com/cirosantilli/media/tree/master/cia-2010-covert-communication-websites/html)
<a id="_4589"></a>
- downloaded with: [https://github.com/cirosantilli/media/tree/master/cia-2010-covert-communication-websites/download-html.sh](https://github.com/cirosantilli/media/tree/master/cia-2010-covert-communication-websites/download-html.sh). Note that there were many supurious errors notably:<a id="_4590"></a>
  > OpenSSL SSL\_connect: SSL\_ERROR\_SYSCALL in connection to web.archive.org:443

  we just ran it multiple times until all errors were gone.

<a id="_4591"></a>
The best way to analyse the HTML is to grap our dumps from: [https://github.com/cirosantilli/cia-2010-websites-dump](https://github.com/cirosantilli/cia-2010-websites-dump).

<a id="_4592"></a>
Some possibly interesting searches include:<a id="_4593"></a>

<a id="_4594"></a>
- list all HTML comments, maybe something spicy was left over:<a id="_4595"></a>

  ```
  git grep '<!--'
  ```
<a id="_4596"></a>
- search for weird file extensions:<a id="_4597"></a>

  ```
  git ls-files | grep -Ev '\.(jpg|gif|html|txt|png|css|php|js|jar|cgi|htm|swf|ico|JPG|class|zip|sf)'
  ```
<a id="_4598"></a>
- have a look at the largest folers:<a id="_4599"></a>

  ```
  ncdu
  ```

<a id="_4600"></a>
Some of the HTML files contain [conditional comments](https://ourbigbook.com/go/topic/conditional-comments) e.g. [https://web.archive.org/web/20091023041107/http://aquaswimming.com/](https://web.archive.org/web/20091023041107/http://aquaswimming.com/) contains:<a id="_4601"></a>

```
<!--[if IE 6]> <link href="swimstyleie6.css" rel="stylesheet" type="text/css"> <![endif]-->
```

<a id="_4602"></a>
Varios of the non-English websites seem to have comments translating the content e.g.:<a id="_4603"></a>

```
./noticiasmusica.net/20101230165001/index.html:<h2>Alguns dos Melhores Sites Nacionais</h2><!--some of the best national sites (in music)-->
```
This feels like it could be the translation helping the technical webdev team know what is what.

<a id="_4604"></a>
Many of the RSS frame pages use:<a id="_4605"></a>

```
<base target="_blank" />
```
which is a weird HTML tag that would lead all links to open on new tabs, e.g. [https://web.archive.org/web/20110202124411/http://thecricketfan.com/home.html](https://web.archive.org/web/20110202124411/http://thecricketfan.com/home.html).

<a id="_4606"></a>
Various websites have pages with .php extension. It feels likely that all websites were written in [PHP](../php.md).

<a id="_4607"></a>
Some sites use a `feeds.php` for the feeds, e.g. [http://www.absolutebearing.net//absolutebearing\_feeds/feeds.php?src=http%3A%2F%2Ffeeds2.feedburner.com%2FOceanyachtsinfo&desc=1](https://web.archive.org/web/20101231174008/http://www.absolutebearing.net//absolutebearing_feeds/feeds.php?src=http%3A%2F%2Ffeeds2.feedburner.com%2FOceanyachtsinfo&desc=1)

<a id="_4608"></a>
Some URLs existed both in HTML and .php extension, or were converted at some point:<a id="_4609"></a>

```
allworldstatistics.com/20110207151941/comprehensivesources.html
allworldstatistics.com/20130818155225/comprehensivesources.php
```

<a id="_4610"></a>
A few of the PHP urls have weird IDs in them like `omktf`, `juqwt` and `qlaqft`:<a id="_4611"></a>

```
./middle-east-newstoday.com/20100829004127/omktf/uirl.php?ok=461128
./newsandsportscentral.com/20100327130237/juqwt/eubcek.php?pe=747155
./pondernews.net/20100826031745/lldwg/qlaqft.php?fc=281298
```
we wonder what they mean.

<a id="_4612"></a>
A few separate websites have an archive with the same `pid` parameter:<a id="_4613"></a>

```
fightwithoutrules.com/20131220205811/?pid=2POQ7BC1G/index.html
half-court.net/20131223165013/?pid=2POQ7BC1G/index.html
health-men-today.com/20131223002237/?pid=2POQ7BC1G/index.html
intlnewsdaily.com/20131221121441/?pid=2POQ7BC1G/index.html
intoworldnews.com/20131217193621/?pid=2POQ7BC1G/index.html
```
It is unclear what it means. All of them contain something like:<a id="_4614"></a>

```
<html>
<head>
<meta name="robots" content="noarchive" />
<meta name="googlebot" content="nosnippet" />
</head>
<body>
<div align=center>
<h3>Error. Page cannot be displayed. Please contact your service provider for more details.  (11)</h3>
</div>
</body>
</html>
```
so looks like an archival artifact only.

<a id="_4615"></a>
The following two websites have a `feeds.php` system for their RSS:<a id="_4616"></a>

```
./mydailynewsreport.com/20110211111053/myrss/feeds.php?src=http:/www.refahemelli.com/pashto/news/rss.php&chan=y&desc=1&targ=y&utf=y
./magneticfieldnews.com/20110208063545/magneticfeeds/feeds.php?src=http:/www.bbc.co.uk/pashto/index.xml&chan=y&desc=1&targ=y&utf=y
```

<a id="_4617"></a>
Some of the HTML uses attributes without quotes, which is legal, but very unusual nowadays:<a id="_4618"></a>

```
soldiersofsouthasia.com/20110207203705/home.htm: <a href=http://www.rss-to-javascript.com
```

<a id="_4619"></a>
We can try to search for any link leaks by listing all domains linked to with:<a id="_4620"></a>

```
git grep --no-color -I -h --no-line -o 'https?://[^/">?]+[/">?]' | sed -r 's/.$//' | sort | uniq -c | sort -nk1
```
The first thing that shows up is that there are some IPs linked to directly! But they seem to be the direct IPs of legitimate websites, we are not sure why IPs were used rather than domain names:<a id="_4621"></a>

<a id="_4622"></a>
- [http://69.167.160.171](http://69.167.160.171) at [https://web.archive.org/web/20110208053653/http://sa-michigan.com/](https://web.archive.org/web/20110208053653/http://sa-michigan.com/) to [https://web.archive.org/web/20100304122019/http://69.167.160.171/](https://web.archive.org/web/20100304122019/http://69.167.160.171/) marked with image "fantasyplayers.com", a legit website called Fantasy Players Network
<a id="_4623"></a>
- [http://69.94.11.53](http://69.94.11.53) at [https://web.archive.org/web/20101229193800/http://newsresolution.net/](https://web.archive.org/web/20101229193800/http://newsresolution.net/) titled "International Tribunal for Rwanda" to [https://web.archive.org/web/20101229193800/http://69.94.11.53/default.htm](https://web.archive.org/web/20101229193800/http://69.94.11.53/default.htm)
<a id="_4624"></a>
- [http://74.125.77.132](http://74.125.77.132) mynepalnews.com Webalizer
<a id="_4625"></a>
- [http://194.165.154.66/index.php](http://194.165.154.66/index.php) [https://web.archive.org/web/20110129161937/http://icwb-news.com/](https://web.archive.org/web/20110129161937/http://icwb-news.com/) MiddleEast links to 194.165.154.66/index.php but that is an actual page: [https://web.archive.org/web/20110529142501/http://194.165.154.66/index.php](https://web.archive.org/web/20110529142501/http://194.165.154.66/index.php)
<a id="_4626"></a>
- [http://200.55.6.87](http://200.55.6.87) at [https://web.archive.org/web/20110128170204/http://noticiasdelmundolatino.com/](https://web.archive.org/web/20110128170204/http://noticiasdelmundolatino.com/) after clicking "Maps" tab entitled "Mapas en la red" to [https://web.archive.org/web/20100329150648/http://200.55.6.87/es/index.htm](https://web.archive.org/web/20100329150648/http://200.55.6.87/es/index.htm)
<a id="_4627"></a>
- [http://213.97.154.118](http://213.97.154.118) at [https://web.archive.org/web/20120429042725/http://montanismoaventura.com/](https://web.archive.org/web/20120429042725/http://montanismoaventura.com/) entitled "Mallorca Verde" to [https://web.archive.org/web/20120430191214/http://213.97.154.118/mallorcaverde/](https://web.archive.org/web/20120430191214/http://213.97.154.118/mallorcaverde/) The target is a bit weird and almost empty.
<a id="_4628"></a>
- [http://216.218.196.146](http://216.218.196.146) at entitled "AskTheDr.com" to [https://web.archive.org/web/20070303080403/http://216.218.196.146/askthedr/index.htm](https://web.archive.org/web/20070303080403/http://216.218.196.146/askthedr/index.htm)

<a id="_4629"></a>
We can also get the full line for each with sorted by least common domains with the slow:<a id="_4630"></a>

```
git grep --no-color -I -h --no-line -o 'https?://[^/">?]+[/">?]' | sed -r 's/.$//' | sort | uniq -c | sort -nk1 | awk '{if ($1 < 10) print $2}' | xargs -I{} git --no-pager grep -h --no-line -o '{}.*<' | tee tmp.log
```

<a id="_4631"></a>
We can search for all IP-like strings with:<a id="_4632"></a>

```
git grep '[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\b'
```

**Table of contents**

- [Binary files](binary-files.md)
- [HTML title element](html-title-element.md)
- [Adobe Dreamwaver JS functions](adobe-dreamwaver-js-functions.md)

## ↑ Ancestors (14)

1. [Fingerprints](fingerprints.md)
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

- [Hits without nearby IP hits](hits-without-nearby-ip-hits.md)
- [Possible HTML information leaks](possible-html-information-leaks.md)
