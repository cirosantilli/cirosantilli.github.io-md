# Expired domain trackers

↑ **Parent:** [Data sources](data-sources.md)  
🏷️ **Tags:** [Expired domain tracker](../expired-domain-tracker.md)

When you [Google](../google-split.md) most of the hit domains, many of them show up on "expired domain trackers", and above all Chinese expired domain trackers for some reason, notably e.g.:
- [https://hupo.com](https://hupo.com): e.g. [http://static.hupo.com/expdomain_myadmin/2012-03-06（国际域名）.txt](http://static.hupo.com/expdomain_myadmin/2012-03-06（国际域名）.txt). Heavily IP throttled. Tor hindered more than helped.

  First known working day: `2011-07-29`.

  Scraping script: [cia-2010-covert-communication-websites/hupo.sh](cia-2010-covert-communication-websites/hupo.sh). Scraping does about 1 day every 5 minutes relatively reliably, so about 36 hours / year. Not bad.

  Results are stored under `tmp/humo/<day>`.

  Check for hit overlap:
  ```
  grep -Fx -f <( jq -r '.[].host' ../media/cia-2010-covert-communication-websites/hits.json ) cia-2010-covert-communication-websites/tmp/hupo/*
  ```
  The hits are very well distributed amongst days and months, at least they did a good job hiding these potential timing fingerprints. This feels very deliberately designed.

  There are lots of hits. The data set is very inclusive. Also we understand that it must have been obtains through means other than [Web crawling](../web-crawling.md), since it contains so many of the hits.

  Nice output format for scraping as the HTML is very minimal

  They randomly changed their URL format to remove the space before the .com after 2012-02-03:
  - [http://static.hupo.com/expdomain_myadmin/2012-01-01（国际域名）%20.txt](http://static.hupo.com/expdomain_myadmin/2012-01-01（国际域名）%20.txt)
  - [http://static.hupo.com/expdomain_myadmin/2013-01-01（国际域名）.txt](http://static.hupo.com/expdomain_myadmin/2013-01-01（国际域名）.txt)

  Some of their files are simply missing however unfortunately, e.g. neither of the following exist:
  - [http://static.hupo.com/expdomain_myadmin/2012-07-01（国际域名）%20.txt](http://static.hupo.com/expdomain_myadmin/2012-07-01（国际域名）%20.txt)
  - [http://static.hupo.com/expdomain_myadmin/2012-07-01（国际域名）.txt](http://static.hupo.com/expdomain_myadmin/2012-07-01（国际域名）.txt)
  webmasterhome.cn did contain that one however: [http://domain.webmasterhome.cn/com/2012-07-01.asp](http://domain.webmasterhome.cn/com/2012-07-01.asp). Hmm. we might have better luck over there then?

  2018-11-19 is corrupt in a new and wonderful way, with a bunch of trailing zeros:
  ```
  wget -O hupo-2018-11-19 'http://static.hupo.com/expdomain_myadmin/2018-11-19%EF%BC%88%E5%9B%BD%E9%99%85%E5%9F%9F%E5%90%8D%EF%BC%89.txt
  hd hupo-2018-11-19
  ```
  ends in:
  ```
  000ffff0  74 75 64 69 65 73 2e 63  6f 6d 0d 0a 70 31 63 6f  |tudies.com..p1co|
  00100000  00 00 00 00 00 00 00 00  00 00 00 00 00 00 00 00  |................|
  *
  0018a5e0  00 00 00 00 00 00 00 00  00                       |.........|
  ```

  More generally, several files contain invalid domain names with non-ASCII characters, e.g. 2013-01-02 contains `365<D3>л<FA><C2><CC>.com`. Domain names can only contain ASCII charters: [https://stackoverflow.com/questions/1133424/what-are-the-valid-characters-that-can-show-up-in-a-url-host](https://stackoverflow.com/questions/1133424/what-are-the-valid-characters-that-can-show-up-in-a-url-host) Maybe we should get rid of any such lines as noise.

  Some files around 2011-09-06 start with an empty line. 2014-01-15 starts with about twenty empty lines. Oh and that last one also has some trash bytes the end  `<B7><B5><BB><D8>`. Beauty.
- [https://webmasterhome.cn](https://webmasterhome.cn): e.g. [http://domain.webmasterhome.cn/com/2012-03-06.asp](http://domain.webmasterhome.cn/com/2012-03-06.asp). Appears to contain the exact same data as "static.hupo.com"

  First known working day: `2011-08-18`.

  Also heavily IP throttled, and a bit more than hupo apparently.

  Scraper [cia-2010-covert-communication-websites/webmastercn.sh](cia-2010-covert-communication-websites/webmastercn.sh).

  Also has some randomly missing dates like hupo.com, though different missing ones from hupo, so they complement each other nicely.

  Some of the URLs are broken and don't inform that with HTTP status code, they just replace the results with some Chinese text 无法找到该页 (The requested page could not be found):
  - [https://domain.webmasterhome.cn/com/2012-02-06.asp](https://domain.webmasterhome.cn/com/2012-02-06.asp)
  - [https://domain.webmasterhome.cn/com/2012-02-14.asp](https://domain.webmasterhome.cn/com/2012-02-14.asp)
  - [https://domain.webmasterhome.cn/com/2013-04-30.asp](https://domain.webmasterhome.cn/com/2013-04-30.asp)

  Several URLs just return length 0 content, e.g.:
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

  Starting around 2018, the IP limiting became very intense, 30 mins / 1 hour per URL, so we just gave up. Therefore, data from 2018 onwards does not contain webmasterhome.cn data.

  Starting from `2013-05-10` the format changes randomly. This also shows us that they just have all the HTML pages as static files on their server. E.g. with:
  ```
  grep -a '<pre' * | s
  ```
  we see:
  ```
  2013-05-09:<pre style='font-family:Verdana, Arial, Helvetica, sans-serif; '><strong>2013<C4><EA>05<D4><C2>09<C8>յ<BD><C6>ڹ<FA><BC><CA><D3><F2><C3><FB></strong><br>0-3y.com
  2013-05-10:<pre><strong>2013<C4><EA>05<D4><C2>10<C8>յ<BD><C6>ڹ<FA><BC><CA><D3><F2><C3><FB></strong>
  ```
- [justdropped.com](../justdropped-com.md): e.g. [https://www.justdropped.com/drops/010112com.html](https://www.justdropped.com/drops/010112com.html). First known working day: `2006-01-01`. Unthrottled.
- [http://yoid.com](http://yoid.com): e.g.: [http://yoid.com/bydate.php?d=2016-06-03&a=a](http://yoid.com/bydate.php?d=2016-06-03&a=a). First known workding day: `2016-06-01`.
This suggests that scraping these lists might be a good starting point to obtaining "all expired domains ever".

Data comparison:
- 2012-01-01
  - [http://static.hupo.com/expdomain_myadmin/2012-01-01%EF%BC%88%E5%9B%BD%E9%99%85%E5%9F%9F%E5%90%8D%EF%BC%89%20.txt](http://static.hupo.com/expdomain_myadmin/2012-01-01%EF%BC%88%E5%9B%BD%E9%99%85%E5%9F%9F%E5%90%8D%EF%BC%89%20.txt)
  - [http://domain.webmasterhome.cn/com/2012-01-01.asp](http://domain.webmasterhome.cn/com/2012-01-01.asp)
  - [https://www.justdropped.com/drops/010112com.html](https://www.justdropped.com/drops/010112com.html)
  Looking only at the `.com`:
  - webmastercn has just about ten extra ones than justdropped, the rest is exactly the same
  - justdropped has some extra and some missing from hupo
  The lists are quite similar however.

  Considering toplevels:
  - hupo has several toplevels that webmastercn does not have, e.g. .org and many others
  - justdropped only covers exactly 6 tlds: `.us`, `.org`, `.net`, `.info`, `.com` and `.biz`. The `.com` lists are very similar to hupo + webmastercn. But it has a lot more non-`.com` domains apparently.

We've made the following pipelines for hupo.com + webmasterhome.cn merging:
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

Count unique domains in the repos:
```
( echo */*/*/* | xargs cat ) | sort -u | wc
```

The extracted data is present at:
- [https://archive.org/details/expired-domain-names-by-day](https://archive.org/details/expired-domain-names-by-day)
- [https://github.com/cirosantilli/expired-domain-names-by-day-*](https://github.com/cirosantilli/expired-domain-names-by-day-*) repos:
  - [https://github.com/cirosantilli/expired-domain-names-by-day-2006](https://github.com/cirosantilli/expired-domain-names-by-day-2006)
  - [https://github.com/cirosantilli/expired-domain-names-by-day-2007](https://github.com/cirosantilli/expired-domain-names-by-day-2007)
  - [https://github.com/cirosantilli/expired-domain-names-by-day-2008](https://github.com/cirosantilli/expired-domain-names-by-day-2008)
  - [https://github.com/cirosantilli/expired-domain-names-by-day-2009](https://github.com/cirosantilli/expired-domain-names-by-day-2009)
  - [https://github.com/cirosantilli/expired-domain-names-by-day-2010](https://github.com/cirosantilli/expired-domain-names-by-day-2010)
  - [https://github.com/cirosantilli/expired-domain-names-by-day-2011](https://github.com/cirosantilli/expired-domain-names-by-day-2011) (~11M)
  - [https://github.com/cirosantilli/expired-domain-names-by-day-2012](https://github.com/cirosantilli/expired-domain-names-by-day-2012) (~18M)
  - [https://github.com/cirosantilli/expired-domain-names-by-day-2013](https://github.com/cirosantilli/expired-domain-names-by-day-2013) (~28M)
  - [https://github.com/cirosantilli/expired-domain-names-by-day-2014](https://github.com/cirosantilli/expired-domain-names-by-day-2014) (~29M)
  - [https://github.com/cirosantilli/expired-domain-names-by-day-2015](https://github.com/cirosantilli/expired-domain-names-by-day-2015) (~28M)
  - [https://github.com/cirosantilli/expired-domain-names-by-day-2016](https://github.com/cirosantilli/expired-domain-names-by-day-2016)
  - [https://github.com/cirosantilli/expired-domain-names-by-day-2017](https://github.com/cirosantilli/expired-domain-names-by-day-2017)
  - [https://github.com/cirosantilli/expired-domain-names-by-day-2018](https://github.com/cirosantilli/expired-domain-names-by-day-2018)
  - [https://github.com/cirosantilli/expired-domain-names-by-day-2019](https://github.com/cirosantilli/expired-domain-names-by-day-2019)
  - [https://github.com/cirosantilli/expired-domain-names-by-day-2020](https://github.com/cirosantilli/expired-domain-names-by-day-2020)
  - [https://github.com/cirosantilli/expired-domain-names-by-day-2021](https://github.com/cirosantilli/expired-domain-names-by-day-2021)
  - [https://github.com/cirosantilli/expired-domain-names-by-day-2022](https://github.com/cirosantilli/expired-domain-names-by-day-2022)
  - [https://github.com/cirosantilli/expired-domain-names-by-day-2023](https://github.com/cirosantilli/expired-domain-names-by-day-2023)
  - [https://github.com/cirosantilli/expired-domain-names-by-day-2024](https://github.com/cirosantilli/expired-domain-names-by-day-2024)
Soon after uploading, these repos started getting some interesting traffic, presumably started by security trackers going "bling bling" on certain malicious domain names in their databases:
- GitHub trackers:
  - admin-monitor.shiyue.com
  - anquan.didichuxing.com
  - app.cloudsek.com
  - app.flare.io
  - app.rainforest.tech
  - app.shadowmap.com
  - bo.serenety.xmco.fr 8 1
  - bts.linecorp.com
  - burn2give.vercel.app
  - cbs.ctm360.com 17 2
  - code6.d1m.cn
  - code6-ops.juzifenqi.com
  - codefend.devops.cndatacom.com
  - dlp-code.airudder.com
  - easm.atrust.sangfor.com
  - ec2-34-248-93-242.eu-west-1.compute.amazonaws.com
  - ecall.beygoo.me 2 1
  - eos.vip.vip.com 1 1
  - foradar.baimaohui.net 2 1
  - fty.beygoo.me
  - hive.telefonica.com.br 2 1
  - hulrud.tistory.com
  - kartos.enthec.com
  - soc.futuoa.com
  - lullar-com-3.appspot.com
  - penetration.houtai.io 2 1
  - platform.sec.corp.qihoo.net
  - plus.k8s.onemt.co	4 1
  - pmp.beygoo.me 2 1
  - portal.protectorg.com
  - qa-boss.amh-group.com
  - saicmotor.saas.cubesec.cn
  - scan.huoban.com
  - sec.welab-inc.com
  - security.ctrip.com 10 3
  - siem-gs.int.black-unique.com 2 1
  - soc-github.daojia-inc.com
  - spigotmc.org 2 1
  - tcallzgroup.blueliv.com
  - tcthreatcompass05.blueliv.com 4 1
  - tix.testsite.woa.com 2 1
  - toucan.belcy.com 1 1
  - turbo.gwmdevops.com 18 2
  - urlscan.watcherlab.com
  - zelenka.guru. Looks like a Russian hacker forum.
- LinkedIn profile views:
  - "Information Security Specialist at Forcepoint"

Check for overlap of the merge:
```
grep -Fx -f <( jq -r '.[].host' ../media/cia-2010-covert-communication-websites/hits.json ) cia-2010-covert-communication-websites/tmp/merge/*
```

Next, we can start searching by keyword with [Wayback Machine CDX scanning with Tor parallelization](wayback-machine-cdx-scanning-with-tor-parallelization.md) with out helper [cia-2010-covert-communication-websites/hupo-cdx-tor.sh](cia-2010-covert-communication-websites/hupo-cdx-tor.sh), e.g. to check domains that contain the term "news":
```
./hupo-cdx-tor.sh mydir 'news|global' 2011 2019
```
produces per-year results for the regex term `news|global` between the years under:
```
tmp/hupo-cdx-tor/mydir/2011
tmp/hupo-cdx-tor/mydir/2012
```
OK lets:
```
./hupo-cdx-tor.sh out 'news|headline|internationali|mondo|mundo|mondi|iran|today'
```

Other searches that are not dense enough for our patience:
```
world|global|[^.]info
```

OMG `news` search might be producing some golden, golden new hits!!! Going full into this. Hits:
- thepyramidnews.com
- echessnews.com
- tickettonews.com
- airuafricanews.com
- vuvuzelanews.com
- dayenews.com
- newsupdatesite.com
- arabicnewsonline.com
- arabicnewsunfiltered.com
- newsandsportscentral.com
- networkofnews.com
- trekkingtoday.com
- financial-crisis-news.com
and a few more. It's amazing.

Related:
- [https://webmasters.stackexchange.com/questions/33806/expired-domains-database/143542#143542](https://webmasters.stackexchange.com/questions/33806/expired-domains-database/143542#143542)
- [https://stackoverflow.com/questions/928549/how-to-create-a-list-of-recently-expired-domains/77336749#77336749](https://stackoverflow.com/questions/928549/how-to-create-a-list-of-recently-expired-domains/77336749#77336749)
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
