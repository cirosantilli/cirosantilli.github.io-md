# Expired domain trackers

↑ **Parent:** [Data sources](data-sources.md)  
🏷️ **Tags:** [Expired domain tracker](../expired-domain-tracker.md)

<a id="_6212"></a>
When you [Google](../google-split.md) most of the hit domains, many of them show up on "expired domain trackers", and above all Chinese expired domain trackers for some reason, notably e.g.:<a id="_6213"></a>

<a id="_6214"></a>
- <a id="_6215"></a>
  [https://hupo.com](https://hupo.com): e.g. [http://static.hupo.com/expdomain_myadmin/2012-03-06（国际域名）.txt](http://static.hupo.com/expdomain_myadmin/2012-03-06（国际域名）.txt). Heavily IP throttled. Tor hindered more than helped.

  <a id="_6216"></a>
  First known working day: `2011-07-29`.

  <a id="_6217"></a>
  Scraping script: [cia-2010-covert-communication-websites/hupo.sh](cia-2010-covert-communication-websites/hupo.sh). Scraping does about 1 day every 5 minutes relatively reliably, so about 36 hours / year. Not bad.

  <a id="_6218"></a>
  Results are stored under `tmp/humo/<day>`.

  <a id="_6219"></a>
  Check for hit overlap:<a id="_6220"></a>

  ```
  grep -Fx -f <( jq -r '.[].host' ../media/cia-2010-covert-communication-websites/hits.json ) cia-2010-covert-communication-websites/tmp/hupo/*
  ```
  The hits are very well distributed amongst days and months, at least they did a good job hiding these potential timing fingerprints. This feels very deliberately designed.

  <a id="_6221"></a>
  There are lots of hits. The data set is very inclusive. Also we understand that it must have been obtains through means other than [Web crawling](../web-crawling.md), since it contains so many of the hits.

  <a id="_6222"></a>
  Nice output format for scraping as the HTML is very minimal

  <a id="_6223"></a>
  They randomly changed their URL format to remove the space before the .com after 2012-02-03:<a id="_6224"></a>

  <a id="_6225"></a>
  - [http://static.hupo.com/expdomain_myadmin/2012-01-01（国际域名）%20.txt](http://static.hupo.com/expdomain_myadmin/2012-01-01（国际域名）%20.txt)
  <a id="_6226"></a>
  - [http://static.hupo.com/expdomain_myadmin/2013-01-01（国际域名）.txt](http://static.hupo.com/expdomain_myadmin/2013-01-01（国际域名）.txt)

  <a id="_6227"></a>
  Some of their files are simply missing however unfortunately, e.g. neither of the following exist:<a id="_6228"></a>

  <a id="_6229"></a>
  - [http://static.hupo.com/expdomain_myadmin/2012-07-01（国际域名）%20.txt](http://static.hupo.com/expdomain_myadmin/2012-07-01（国际域名）%20.txt)
  <a id="_6230"></a>
  - [http://static.hupo.com/expdomain_myadmin/2012-07-01（国际域名）.txt](http://static.hupo.com/expdomain_myadmin/2012-07-01（国际域名）.txt)
  webmasterhome.cn did contain that one however: [http://domain.webmasterhome.cn/com/2012-07-01.asp](http://domain.webmasterhome.cn/com/2012-07-01.asp). Hmm. we might have better luck over there then?

  <a id="_6231"></a>
  2018-11-19 is corrupt in a new and wonderful way, with a bunch of trailing zeros:<a id="_6232"></a>

  ```
  wget -O hupo-2018-11-19 'http://static.hupo.com/expdomain_myadmin/2018-11-19%EF%BC%88%E5%9B%BD%E9%99%85%E5%9F%9F%E5%90%8D%EF%BC%89.txt
  hd hupo-2018-11-19
  ```
  ends in:<a id="_6233"></a>

  ```
  000ffff0  74 75 64 69 65 73 2e 63  6f 6d 0d 0a 70 31 63 6f  |tudies.com..p1co|
  00100000  00 00 00 00 00 00 00 00  00 00 00 00 00 00 00 00  |................|
  *
  0018a5e0  00 00 00 00 00 00 00 00  00                       |.........|
  ```

  <a id="_6234"></a>
  More generally, several files contain invalid domain names with non-ASCII characters, e.g. 2013-01-02 contains `365<D3>л<FA><C2><CC>.com`. Domain names can only contain ASCII charters: [https://stackoverflow.com/questions/1133424/what-are-the-valid-characters-that-can-show-up-in-a-url-host](https://stackoverflow.com/questions/1133424/what-are-the-valid-characters-that-can-show-up-in-a-url-host) Maybe we should get rid of any such lines as noise.

  <a id="_6235"></a>
  Some files around 2011-09-06 start with an empty line. 2014-01-15 starts with about twenty empty lines. Oh and that last one also has some trash bytes the end  `<B7><B5><BB><D8>`. Beauty.
<a id="_6236"></a>
- <a id="_6237"></a>
  [https://webmasterhome.cn](https://webmasterhome.cn): e.g. [http://domain.webmasterhome.cn/com/2012-03-06.asp](http://domain.webmasterhome.cn/com/2012-03-06.asp). Appears to contain the exact same data as "static.hupo.com"

  <a id="_6238"></a>
  First known working day: `2011-08-18`.

  <a id="_6239"></a>
  Also heavily IP throttled, and a bit more than hupo apparently.

  <a id="_6240"></a>
  Scraper [cia-2010-covert-communication-websites/webmastercn.sh](cia-2010-covert-communication-websites/webmastercn.sh).

  <a id="_6241"></a>
  Also has some randomly missing dates like hupo.com, though different missing ones from hupo, so they complement each other nicely.

  <a id="_6242"></a>
  Some of the URLs are broken and don't inform that with HTTP status code, they just replace the results with some Chinese text 无法找到该页 (The requested page could not be found):<a id="_6243"></a>

  <a id="_6244"></a>
  - [https://domain.webmasterhome.cn/com/2012-02-06.asp](https://domain.webmasterhome.cn/com/2012-02-06.asp)
  <a id="_6245"></a>
  - [https://domain.webmasterhome.cn/com/2012-02-14.asp](https://domain.webmasterhome.cn/com/2012-02-14.asp)
  <a id="_6246"></a>
  - [https://domain.webmasterhome.cn/com/2013-04-30.asp](https://domain.webmasterhome.cn/com/2013-04-30.asp)

  <a id="_6247"></a>
  Several URLs just return length 0 content, e.g.:<a id="_6248"></a>

  ```
  curl -vvv http://domain.webmasterhome.cn/com/2015-10-31.asp
  *   Trying 125.90.93.11:80...
  * Connected to domain.webmasterhome.cn (125.90.93.11) port 80 (#0)
  > GET /com/2015-10-31.asp HTTP/1.1
  > Host: domain.webmasterhome.cn
  > User-Agent: curl/7.88.1
  > Accept: */*
  >
  < HTTP/1.1 200 OK
  < Date: Sat, 21 Oct 2023 15:12:23 GMT
  < Server: Microsoft-IIS/6.0
  < X-Powered-By: ASP.NET
  < Content-Length: 0
  < Content-Type: text/html
  < Set-Cookie: ASPSESSIONIDCSTTTBAD=BGGPAONBOFKMMFIPMOGGHLMJ; path=/
  < Cache-control: private
  <
  * Connection #0 to host domain.webmasterhome.cn left intact
  ```
  It is not fully clear if this is a throttling mechanism, or if the data is just missing entirely.

  <a id="_6249"></a>
  Starting around 2018, the IP limiting became very intense, 30 mins / 1 hour per URL, so we just gave up. Therefore, data from 2018 onwards does not contain webmasterhome.cn data.

  <a id="_6250"></a>
  Starting from `2013-05-10` the format changes randomly. This also shows us that they just have all the HTML pages as static files on their server. E.g. with:<a id="_6251"></a>

  ```
  grep -a '<pre' * | s
  ```
  we see:<a id="_6252"></a>

  ```
  2013-05-09:<pre style='font-family:Verdana, Arial, Helvetica, sans-serif; '><strong>2013<C4><EA>05<D4><C2>09<C8>յ<BD><C6>ڹ<FA><BC><CA><D3><F2><C3><FB></strong><br>0-3y.com
  2013-05-10:<pre><strong>2013<C4><EA>05<D4><C2>10<C8>յ<BD><C6>ڹ<FA><BC><CA><D3><F2><C3><FB></strong>
  ```
<a id="_6253"></a>
- [justdropped.com](../justdropped-com.md): e.g. [https://www.justdropped.com/drops/010112com.html](https://www.justdropped.com/drops/010112com.html). First known working day: `2006-01-01`. Unthrottled.
<a id="_6254"></a>
- [http://yoid.com](http://yoid.com): e.g.: [http://yoid.com/bydate.php?d=2016-06-03&a=a](http://yoid.com/bydate.php?d=2016-06-03&a=a). First known workding day: `2016-06-01`.
This suggests that scraping these lists might be a good starting point to obtaining "all expired domains ever".

<a id="_6255"></a>
Data comparison:<a id="_6256"></a>

<a id="_6257"></a>
- <a id="_6258"></a>
  2012-01-01<a id="_6259"></a>

  <a id="_6260"></a>
  - [http://static.hupo.com/expdomain_myadmin/2012-01-01%EF%BC%88%E5%9B%BD%E9%99%85%E5%9F%9F%E5%90%8D%EF%BC%89%20.txt](http://static.hupo.com/expdomain_myadmin/2012-01-01%EF%BC%88%E5%9B%BD%E9%99%85%E5%9F%9F%E5%90%8D%EF%BC%89%20.txt)
  <a id="_6261"></a>
  - [http://domain.webmasterhome.cn/com/2012-01-01.asp](http://domain.webmasterhome.cn/com/2012-01-01.asp)
  <a id="_6262"></a>
  - [https://www.justdropped.com/drops/010112com.html](https://www.justdropped.com/drops/010112com.html)
  Looking only at the `.com`:<a id="_6263"></a>

  <a id="_6264"></a>
  - webmastercn has just about ten extra ones than justdropped, the rest is exactly the same
  <a id="_6265"></a>
  - justdropped has some extra and some missing from hupo
  The lists are quite similar however.

  <a id="_6266"></a>
  Considering toplevels:<a id="_6267"></a>

  <a id="_6268"></a>
  - hupo has several toplevels that webmastercn does not have, e.g. .org and many others
  <a id="_6269"></a>
  - justdropped only covers exactly 6 tlds: `.us`, `.org`, `.net`, `.info`, `.com` and `.biz`. The `.com` lists are very similar to hupo + webmastercn. But it has a lot more non-`.com` domains apparently.

<a id="_6270"></a>
We've made the following pipelines for hupo.com + webmasterhome.cn merging:<a id="_6271"></a>

```
./hupo.sh &
./webmastercn.sh &
./justdropped.sh &
wait
./justdropped-post.sh
./hupo-merge.sh
# Export as small Google indexable files in a Git repository.
./hupo-repo.sh
# Export as per year zips for Internet Archive.
./hupo-zip.sh
# Obtain count statistics:
./hupo-wc.sh
```

<a id="_6272"></a>
Count unique domains in the repos:<a id="_6273"></a>

```
( echo */*/*/* | xargs cat ) | sort -u | wc
```

<a id="_6274"></a>
The extracted data is present at:<a id="_6275"></a>

<a id="_6276"></a>
- [https://archive.org/details/expired-domain-names-by-day](https://archive.org/details/expired-domain-names-by-day)
<a id="_6277"></a>
- [https://github.com/cirosantilli/expired-domain-names-by-day-*](https://github.com/cirosantilli/expired-domain-names-by-day-*) repos:<a id="_6278"></a>

  <a id="_6279"></a>
  - [https://github.com/cirosantilli/expired-domain-names-by-day-2006](https://github.com/cirosantilli/expired-domain-names-by-day-2006)
  <a id="_6280"></a>
  - [https://github.com/cirosantilli/expired-domain-names-by-day-2007](https://github.com/cirosantilli/expired-domain-names-by-day-2007)
  <a id="_6281"></a>
  - [https://github.com/cirosantilli/expired-domain-names-by-day-2008](https://github.com/cirosantilli/expired-domain-names-by-day-2008)
  <a id="_6282"></a>
  - [https://github.com/cirosantilli/expired-domain-names-by-day-2009](https://github.com/cirosantilli/expired-domain-names-by-day-2009)
  <a id="_6283"></a>
  - [https://github.com/cirosantilli/expired-domain-names-by-day-2010](https://github.com/cirosantilli/expired-domain-names-by-day-2010)
  <a id="_6284"></a>
  - [https://github.com/cirosantilli/expired-domain-names-by-day-2011](https://github.com/cirosantilli/expired-domain-names-by-day-2011) (~11M)
  <a id="_6285"></a>
  - [https://github.com/cirosantilli/expired-domain-names-by-day-2012](https://github.com/cirosantilli/expired-domain-names-by-day-2012) (~18M)
  <a id="_6286"></a>
  - [https://github.com/cirosantilli/expired-domain-names-by-day-2013](https://github.com/cirosantilli/expired-domain-names-by-day-2013) (~28M)
  <a id="_6287"></a>
  - [https://github.com/cirosantilli/expired-domain-names-by-day-2014](https://github.com/cirosantilli/expired-domain-names-by-day-2014) (~29M)
  <a id="_6288"></a>
  - [https://github.com/cirosantilli/expired-domain-names-by-day-2015](https://github.com/cirosantilli/expired-domain-names-by-day-2015) (~28M)
  <a id="_6289"></a>
  - [https://github.com/cirosantilli/expired-domain-names-by-day-2016](https://github.com/cirosantilli/expired-domain-names-by-day-2016)
  <a id="_6290"></a>
  - [https://github.com/cirosantilli/expired-domain-names-by-day-2017](https://github.com/cirosantilli/expired-domain-names-by-day-2017)
  <a id="_6291"></a>
  - [https://github.com/cirosantilli/expired-domain-names-by-day-2018](https://github.com/cirosantilli/expired-domain-names-by-day-2018)
  <a id="_6292"></a>
  - [https://github.com/cirosantilli/expired-domain-names-by-day-2019](https://github.com/cirosantilli/expired-domain-names-by-day-2019)
  <a id="_6293"></a>
  - [https://github.com/cirosantilli/expired-domain-names-by-day-2020](https://github.com/cirosantilli/expired-domain-names-by-day-2020)
  <a id="_6294"></a>
  - [https://github.com/cirosantilli/expired-domain-names-by-day-2021](https://github.com/cirosantilli/expired-domain-names-by-day-2021)
  <a id="_6295"></a>
  - [https://github.com/cirosantilli/expired-domain-names-by-day-2022](https://github.com/cirosantilli/expired-domain-names-by-day-2022)
  <a id="_6296"></a>
  - [https://github.com/cirosantilli/expired-domain-names-by-day-2023](https://github.com/cirosantilli/expired-domain-names-by-day-2023)
  <a id="_6297"></a>
  - [https://github.com/cirosantilli/expired-domain-names-by-day-2024](https://github.com/cirosantilli/expired-domain-names-by-day-2024)
Soon after uploading, these repos started getting some interesting traffic, presumably started by security trackers going "bling bling" on certain malicious domain names in their databases:<a id="_6298"></a>

<a id="_6299"></a>
- GitHub trackers:<a id="_6300"></a>

  <a id="_6301"></a>
  - admin-monitor.shiyue.com
  <a id="_6302"></a>
  - anquan.didichuxing.com
  <a id="_6303"></a>
  - app.cloudsek.com
  <a id="_6304"></a>
  - app.flare.io
  <a id="_6305"></a>
  - app.rainforest.tech
  <a id="_6306"></a>
  - app.shadowmap.com
  <a id="_6307"></a>
  - bo.serenety.xmco.fr 8 1
  <a id="_6308"></a>
  - bts.linecorp.com
  <a id="_6309"></a>
  - burn2give.vercel.app
  <a id="_6310"></a>
  - cbs.ctm360.com 17 2
  <a id="_6311"></a>
  - code6.d1m.cn
  <a id="_6312"></a>
  - code6-ops.juzifenqi.com
  <a id="_6313"></a>
  - codefend.devops.cndatacom.com
  <a id="_6314"></a>
  - dlp-code.airudder.com
  <a id="_6315"></a>
  - easm.atrust.sangfor.com
  <a id="_6316"></a>
  - ec2-34-248-93-242.eu-west-1.compute.amazonaws.com
  <a id="_6317"></a>
  - ecall.beygoo.me 2 1
  <a id="_6318"></a>
  - eos.vip.vip.com 1 1
  <a id="_6319"></a>
  - foradar.baimaohui.net 2 1
  <a id="_6320"></a>
  - fty.beygoo.me
  <a id="_6321"></a>
  - hive.telefonica.com.br 2 1
  <a id="_6322"></a>
  - hulrud.tistory.com
  <a id="_6323"></a>
  - kartos.enthec.com
  <a id="_6324"></a>
  - soc.futuoa.com
  <a id="_6325"></a>
  - lullar-com-3.appspot.com
  <a id="_6326"></a>
  - penetration.houtai.io 2 1
  <a id="_6327"></a>
  - platform.sec.corp.qihoo.net
  <a id="_6328"></a>
  - plus.k8s.onemt.co	4 1
  <a id="_6329"></a>
  - pmp.beygoo.me 2 1
  <a id="_6330"></a>
  - portal.protectorg.com
  <a id="_6331"></a>
  - qa-boss.amh-group.com
  <a id="_6332"></a>
  - saicmotor.saas.cubesec.cn
  <a id="_6333"></a>
  - scan.huoban.com
  <a id="_6334"></a>
  - sec.welab-inc.com
  <a id="_6335"></a>
  - security.ctrip.com 10 3
  <a id="_6336"></a>
  - siem-gs.int.black-unique.com 2 1
  <a id="_6337"></a>
  - soc-github.daojia-inc.com
  <a id="_6338"></a>
  - spigotmc.org 2 1
  <a id="_6339"></a>
  - tcallzgroup.blueliv.com
  <a id="_6340"></a>
  - tcthreatcompass05.blueliv.com 4 1
  <a id="_6341"></a>
  - tix.testsite.woa.com 2 1
  <a id="_6342"></a>
  - toucan.belcy.com 1 1
  <a id="_6343"></a>
  - turbo.gwmdevops.com 18 2
  <a id="_6344"></a>
  - urlscan.watcherlab.com
  <a id="_6345"></a>
  - zelenka.guru. Looks like a Russian hacker forum.
<a id="_6346"></a>
- LinkedIn profile views:<a id="_6347"></a>

  <a id="_6348"></a>
  - "Information Security Specialist at Forcepoint"

<a id="_6349"></a>
Check for overlap of the merge:<a id="_6350"></a>

```
grep -Fx -f <( jq -r '.[].host' ../media/cia-2010-covert-communication-websites/hits.json ) cia-2010-covert-communication-websites/tmp/merge/*
```

<a id="_6351"></a>
Next, we can start searching by keyword with [Wayback Machine CDX scanning with Tor parallelization](wayback-machine-cdx-scanning-with-tor-parallelization.md) with out helper [cia-2010-covert-communication-websites/hupo-cdx-tor.sh](cia-2010-covert-communication-websites/hupo-cdx-tor.sh), e.g. to check domains that contain the term "news":<a id="_6352"></a>

```
./hupo-cdx-tor.sh mydir 'news|global' 2011 2019
```
produces per-year results for the regex term `news|global` between the years under:<a id="_6353"></a>

```
tmp/hupo-cdx-tor/mydir/2011
tmp/hupo-cdx-tor/mydir/2012
```
OK lets:<a id="_6354"></a>

```
./hupo-cdx-tor.sh out 'news|headline|internationali|mondo|mundo|mondi|iran|today'
```

<a id="_6355"></a>
Other searches that are not dense enough for our patience:<a id="_6356"></a>

```
world|global|[^.]info
```

<a id="_6357"></a>
OMG `news` search might be producing some golden, golden new hits!!! Going full into this. Hits:<a id="_6358"></a>

<a id="_6359"></a>
- thepyramidnews.com
<a id="_6360"></a>
- echessnews.com
<a id="_6361"></a>
- tickettonews.com
<a id="_6362"></a>
- airuafricanews.com
<a id="_6363"></a>
- vuvuzelanews.com
<a id="_6364"></a>
- dayenews.com
<a id="_6365"></a>
- newsupdatesite.com
<a id="_6366"></a>
- arabicnewsonline.com
<a id="_6367"></a>
- arabicnewsunfiltered.com
<a id="_6368"></a>
- newsandsportscentral.com
<a id="_6369"></a>
- networkofnews.com
<a id="_6370"></a>
- trekkingtoday.com
<a id="_6371"></a>
- financial-crisis-news.com
and a few more. It's amazing.

<a id="_6372"></a>
Related:<a id="_6373"></a>

<a id="_6374"></a>
- [https://webmasters.stackexchange.com/questions/33806/expired-domains-database/143542#143542](https://webmasters.stackexchange.com/questions/33806/expired-domains-database/143542#143542)
<a id="_6375"></a>
- [https://stackoverflow.com/questions/928549/how-to-create-a-list-of-recently-expired-domains/77336749#77336749](https://stackoverflow.com/questions/928549/how-to-create-a-list-of-recently-expired-domains/77336749#77336749)
<a id="_6376"></a>
- [https://github.com/spaze/domains](https://github.com/spaze/domains)

**Table of contents**

- [club.domain.cn](club-domain-cn.md)

## ↑ Ancestors (14)

1. [Data sources](data-sources.md)
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

- [Are there .org hits?](are-there-org-hits.md)
- [Overview of Ciro Santilli's investigation](overview-of-ciro-santilli-s-investigation.md)
- [Searching for Carson](searching-for-carson.md)
- [44 new CIA websites](../updates/44-new-cia-websites.md)
