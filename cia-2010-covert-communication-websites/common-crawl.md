# Common Crawl

↑ **Parent:** [Data sources](data-sources.md)

So far, no new domains have been found with [Common Crawl](common-crawl.md), nor have any existing known domains been found to be present in Common Crawl. Our working theory is that Common Crawl never reached the domains [How did Alexa find the domains?](how-did-alexa-find-the-domains.md)

Let's try and do something with [Common Crawl](common-crawl.md).

Unfortunately there's no [IP](../ip-address.md) data apparently: [https://github.com/commoncrawl/cc-index-table/issues/30](https://github.com/commoncrawl/cc-index-table/issues/30), so let's focus on the URLs.

Using their [Common Crawl Athena](../common-crawl-athena.md) method: [https://commoncrawl.org/2018/03/index-to-warc-files-and-urls-in-columnar-format/](https://commoncrawl.org/2018/03/index-to-warc-files-and-urls-in-columnar-format/)

Hello world:
```
select * from "ccindex"."ccindex" limit 100;
```
Data scanned: 11.75 MB

Sample first output line:
```
#                            2
url_surtkey                  org,whwheelers)/robots.txt
url                          https://whwheelers.org/robots.txt
url_host_name                whwheelers.org
url_host_tld                 org
url_host_2nd_last_part       whwheelers
url_host_3rd_last_part
url_host_4th_last_part
url_host_5th_last_part
url_host_registry_suffix     org
url_host_registered_domain   whwheelers.org
url_host_private_suffix      org
url_host_private_domain      whwheelers.org
url_host_name_reversed
url_protocol                 https
url_port
url_path                     /robots.txt
url_query
fetch_time                   2021-06-22 16:36:50.000
fetch_status                 301
fetch_redirect               https://www.whwheelers.org/robots.txt
content_digest               3I42H3S6NNFQ2MSVX7XZKYAYSCX5QBYJ
content_mime_type            text/html
content_mime_detected        text/html
content_charset
content_languages
content_truncated
warc_filename                crawl-data/CC-MAIN-2021-25/segments/1623488519183.85/robotstxt/CC-MAIN-20210622155328-20210622185328-00312.warc.gz
warc_record_offset           1854030
warc_record_length           639
warc_segment                 1623488519183.85
crawl                        CC-MAIN-2021-25
subset                       robotstxt
```
So `url_host_3rd_last_part` might be a winner for [CGI comms](cgi-comms.md) fingerprinting!

Naive one for one index:
```
select * from "ccindex"."ccindex" where url_host_registered_domain = 'conquermstoday.com' limit 100;
```
have no results... data scanned: 5.73 GB

Let's see if they have any of the domain hits. Let's also restrict by date to try and reduce the data scanned:
```
select * from "ccindex"."ccindex" where
  fetch_time < TIMESTAMP '2014-01-01 00:00:00' AND
  url_host_registered_domain IN (
   'activegaminginfo.com',
   'altworldnews.com',
   ...
   'topbillingsite.com',
   'worldwildlifeadventure.com'
 )
```
Humm, data scanned: 60.59 GB and no hits... weird.

Sanity check:
```
select * from "ccindex"."ccindex" WHERE
  crawl = 'CC-MAIN-2013-20' AND
  subset = 'warc' AND
  url_host_registered_domain IN (
   'google.com',
   'amazon.com'
 )
```
has a bunch of hits of course. Data scanned: 212.88 MB, `WHERE` `crawl` and `subset` are a must! Should have read the article first.

Let's widen a bit more:
```
select * from "ccindex"."ccindex" WHERE
  crawl IN (
    'CC-MAIN-2013-20',
    'CC-MAIN-2013-48',
    'CC-MAIN-2014-10'
  ) AND
  subset = 'warc' AND
  url_host_registered_domain IN (
    'activegaminginfo.com',
    'altworldnews.com',
    ...
    'worldnewsandent.com',
    'worldwildlifeadventure.com'
 )
```
Still nothing found... they don't seem to have any of the URLs of interest?

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

## ← Incoming links (3)

- [Common Crawl](common-crawl.md)
- [How did Alexa find the domains?](how-did-alexa-find-the-domains.md)
- [Wayback Machine](wayback-machine.md)
