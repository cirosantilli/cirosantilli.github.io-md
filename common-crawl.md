# Common Crawl

↑ **Parent:** [Open web crawling](open-web-crawling.md)  
🏷️ **Tags:** [Good](good.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Common_Crawl)

[https://commoncrawl.org/](https://commoncrawl.org/)

Amazing project, that basically makes a more searchable [Wayback Machine](wayback-machine.md).

A bit hard to use their data though, partly due to size, but also lack of free to use querrying mechanisms, and how obtuse [Amazon S3](amazon-s3.md) is to use.

Notably, [aws-cli](aws-cli.md) with an account is the only reliable way, everything else is way too broken, e.g. trying the to check the an index [https://index.commoncrawl.org/CC-MAIN-2023-06/](https://index.commoncrawl.org/CC-MAIN-2023-06/) very often 500s.

But still, their projct is amazing.

The only out-of-the-box search they seem to have is: [http://urlsearch.commoncrawl.org/](http://urlsearch.commoncrawl.org/) for domains/URLs. It is good, but there could be so much more... notably [IPs](ip-address.md).

Also could should document the data shape a bit better.

Sample sizes can be found at: [https://commoncrawl.org/2023/04/mar-apr-2023-crawl-archive-now-available/](https://commoncrawl.org/2023/04/mar-apr-2023-crawl-archive-now-available/)

To explore the data, after login:
```
aws s3 ls s3://commoncrawl/crawl-data/CC-MAIN-2013-20/
```

Copy the toplevel directory only:
```
aws s3 cp s3://commoncrawl/crawl-data/CC-MAIN-2013-20/ . --recursive --exclude "*/*"
```

Copy some wet/wat files:
```
aws s3 cp s3://commoncrawl/crawl-data/CC-MAIN-2013-20/segments/1368696381249/wat/CC-MAIN-20130516092621-00000-ip-10-60-113-184.ec2.internal.warc.wat.gz .
aws s3 sync s3://commoncrawl/crawl-data/CC-MAIN-2013-20/segments/1368696381249/wet/CC-MAIN-20130516092621-00000-ip-10-60-113-184.ec2.internal.warc.wet.gz .
```

Directory structrure:
- cc-index.paths.gz (1K)
- cc-index-table.paths.gz (1K)
- segment.paths.gz (1.7K) Sample lines:
  ```
  crawl-data/CC-MAIN-2013-20/segments/1368696381249/
  crawl-data/CC-MAIN-2013-20/segments/1368696381630/
  ```
- index.html (2.3K)
- wat.paths.gz (98K) Sample lines:
  ```
  crawl-data/CC-MAIN-2013-20/segments/1368696381249/wat/CC-MAIN-20130516092621-00000-ip-10-60-113-184.ec2.internal.warc.wat.gz
  crawl-data/CC-MAIN-2013-20/segments/1368696381249/wat/CC-MAIN-20130516092621-00001-ip-10-60-113-184.ec2.internal.warc.wat.gz
  ```
- wet.paths.gz (98K) Sample lines:
  ```
  crawl-data/CC-MAIN-2013-20/segments/1368696381249/wet/CC-MAIN-20130516092621-00000-ip-10-60-113-184.ec2.internal.warc.wet.gz
  crawl-data/CC-MAIN-2013-20/segments/1368696381249/wet/CC-MAIN-20130516092621-00001-ip-10-60-113-184.ec2.internal.warc.wet.gz
  ```
- warc.paths.gz (99K)
  ```
  crawl-data/CC-MAIN-2013-20/segments/1368696381249/warc/CC-MAIN-20130516092621-00000-ip-10-60-113-184.ec2.internal.warc.gz
  crawl-data/CC-MAIN-2013-20/segments/1368696381249/warc/CC-MAIN-20130516092621-00001-ip-10-60-113-184.ec2.internal.warc.gz
  ```
- segments: directgory with actual data
  - 1368696381249: one of many segments, any meaning of name?
    - CC-MAIN-20130516092621-00000-ip-10-60-113-184.ec2.internal.warc.wet.gz (142M, 334M unzipped)

      A tiny bit of metadata, and then plaintext content from the website, e.g. the second one:
      ```
      WARC/1.0
      WARC-Type: conversion
      WARC-Target-URI: http://004eeb5.netsolhost.com/stephensilver.htm
      WARC-Date: 2013-05-18T08:11:02Z
      WARC-Record-ID: <urn:uuid:773b31ba-ddc6-47a5-ae24-d08141b9944d>
      WARC-Refers-To: <urn:uuid:4b1bdbff-4926-4ced-86f6-072f5bb3837a>
      WARC-Block-Digest: sha1:LQFSCR2LIJQYMPTXRHWU7HAPQTVSYS3A
      Content-Type: text/plain
      Content-Length: 12046

      Stephen Silver is a journalist and editor who specializes in the areas of politics, pop culture, film and sports. He works as an editor with the North American Publishing Co. and as a film critic with The Trend, a local newspaper in the Philadelphia area.
      ```
      No [IP](ip-address.md) unfortunately.
    - CC-MAIN-20130516092621-00000-ip-10-60-113-184.ec2.internal.warc.wat.gz (329M, 1.4G unzipped)

      A lot of JSON metadata and no contents as desired. Contains IP! Some entries however are humongous with a ton of useless data, that's what bloats these so much:
      ```
      WARC/1.0
      WARC-Type: metadata
      WARC-Target-URI: CC-MAIN-20130516092621-00000-ip-10-60-113-184.ec2.internal.warc.gz
      WARC-Date: 2013-11-22T14:51:12Z
      WARC-Record-ID: <urn:uuid:ec54e493-8965-41be-b344-07596cc30b3a>
      WARC-Refers-To: <urn:uuid:cfeff436-7c4c-4119-aaa4-ec2ce27ad3e1>
      Content-Type: application/json
      Content-Length: 1180

      {"Envelope":{"Format":"WARC","WARC-Header-Length":"274","Block-Digest":"sha1:JCZOI4V3UOTXGIRLFMPLW4J2WPLAKGVR","Actual-Content-Length":"372","WARC-Header-Metadata":{"WARC-Type":"warcinfo","WARC-Filename":"CC-MAIN-20130516092621-00000-ip-10-60-113-184.ec2.internal.warc.gz","WARC-Date":"2013-11-22T14:51:12Z","Content-Length":"372","WARC-Record-ID":"<urn:uuid:cfeff436-7c4c-4119-aaa4-ec2ce27ad3e1>","Content-Type":"application/warc-fields"},"Payload-Metadata":{"Trailing-Slop-Length":"0","Actual-Content-Type":"application/warc-fields","Actual-Content-Length":"372","Headers-Corrupt":true,"WARC-Info-Metadata":{"robots":"classic","software":"Nutch 1.6 (CC)/CC WarcExport 1.0","description":"Wide crawl of the web with URLs provided by Blekko for Spring 2013","hostname":"ip-10-60-113-184.ec2.internal","format":"WARC File Format 1.0","isPartOf":"CC-MAIN-2013-20","operator":"CommonCrawl Admin","publisher":"CommonCrawl"}}},"Container":{"Compressed":true,"Gzip-Metadata":{"Footer-Length":"8","Deflate-Length":"453","Header-Length":"10","Inflated-CRC":"866052549","Inflated-Length":"650"},"Offset":"0","Filename":"CC-MAIN-20130516092621-00000-ip-10-60-113-184.ec2.internal.warc.gz"}}

      WARC/1.0
      WARC-Type: metadata
      WARC-Target-URI: http://%20jwashington@ap.org/Content/Press-Release/2012/How-AP-reported-in-all-formats-from-tornado-stricken-regions
      WARC-Date: 2013-05-18T05:48:54Z
      WARC-Record-ID: <urn:uuid:d519658f-7a63-46c1-849b-4cd92332ddb8>
      WARC-Refers-To: <urn:uuid:cefd363b-1fec-4590-8305-4c6fab2e095f>
      Content-Type: application/json
      Content-Length: 1501

      {"Envelope":{"Format":"WARC","WARC-Header-Length":"433","Block-Digest":"sha1:B2B6JDSGWCUQIIUGV54SXEE25RX4SANS","Actual-Content-Length":"302","WARC-Header-Metadata":{"WARC-Type":"request","WARC-Date":"2013-05-18T05:48:54Z","WARC-Warcinfo-ID":"<urn:uuid:cfeff436-7c4c-4119-aaa4-ec2ce27ad3e1>","Content-Length":"302","WARC-Record-ID":"<urn:uuid:cefd363b-1fec-4590-8305-4c6fab2e095f>","WARC-Target-URI":"http://%20jwashington@ap.org/Content/Press-Release/2012/How-AP-reported-in-all-formats-from-tornado-stricken-regions","WARC-IP-Address":"165.1.125.44","Content-Type":"application/http; msgtype=request"},"Payload-Metadata":{"Trailing-Slop-Length":"4","HTTP-Request-Metadata":{"Headers":{"Accept-Language":"en-us,en-gb,en;q=0.7,*;q=0.3","Host":"ap.org","Accept-Encoding":"x-gzip, gzip, deflate","User-Agent":"CCBot/2.0","Accept":"text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8"},"Headers-Length":"300","Entity-Length":"0","Entity-Trailing-Slop-Bytes":"0","Request-Message":{"Method":"GET","Version":"HTTP/1.0","Path":"/Content/Press-Release/2012/How-AP-reported-in-all-formats-from-tornado-stricken-regions"},"Entity-Digest":"sha1:3I42H3S6NNFQ2MSVX7XZKYAYSCX5QBYJ"},"Actual-Content-Type":"application/http; msgtype=request"}},"Container":{"Compressed":true,"Gzip-Metadata":{"Footer-Length":"8","Deflate-Length":"455","Header-Length":"10","Inflated-CRC":"453539965","Inflated-Length":"739"},"Offset":"453","Filename":"CC-MAIN-20130516092621-00000-ip-10-60-113-184.ec2.internal.warc.gz"}}
      ```
      Let's beautify one of them to see it better:
      ```

      {
        "Envelope": {
          "Format": "WARC",
          "WARC-Header-Length": "274",
          "Block-Digest": "sha1:JCZOI4V3UOTXGIRLFMPLW4J2WPLAKGVR",
          "Actual-Content-Length": "372",
          "WARC-Header-Metadata": {
            "WARC-Type": "warcinfo",
            "WARC-Filename": "CC-MAIN-20130516092621-00000-ip-10-60-113-184.ec2.internal.warc.gz",
            "WARC-Date": "2013-11-22T14:51:12Z",
            "Content-Length": "372",
            "WARC-Record-ID": "<urn:uuid:cfeff436-7c4c-4119-aaa4-ec2ce27ad3e1>",
            "Content-Type": "application/warc-fields"
          },
          "Payload-Metadata": {
            "Trailing-Slop-Length": "0",
            "Actual-Content-Type": "application/warc-fields",
            "Actual-Content-Length": "372",
            "Headers-Corrupt": true,
            "WARC-Info-Metadata": {
              "robots": "classic",
              "software": "Nutch 1.6 (CC)/CC WarcExport 1.0",
              "description": "Wide crawl of the web with URLs provided by Blekko for Spring 2013",
              "hostname": "ip-10-60-113-184.ec2.internal",
              "format": "WARC File Format 1.0",
              "isPartOf": "CC-MAIN-2013-20",
              "operator": "CommonCrawl Admin",
              "publisher": "CommonCrawl"
            }
          }
        },
        "Container": {
          "Compressed": true,
          "Gzip-Metadata": {
            "Footer-Length": "8",
            "Deflate-Length": "453",
            "Header-Length": "10",
            "Inflated-CRC": "866052549",
            "Inflated-Length": "650"
          },
          "Offset": "0",
          "Filename": "CC-MAIN-20130516092621-00000-ip-10-60-113-184.ec2.internal.warc.gz"
        }
      }
      ```
      Fuck no IP addresses either. But other entries do have it, why not this one?

      The reason these can be huge is the `HTML-Metadata` section which contain all outlinks! [https://gist.github.com/Smerity/e750f0ef0ab9aa366558#file-bbc-pretty-wat-L34](https://gist.github.com/Smerity/e750f0ef0ab9aa366558#file-bbc-pretty-wat-L34)
    - `CC-MAIN-20130516092621-00000-ip-10-60-113-184.ec2.internal.warc.gz` ()

      Obtain:
      ```
      aws s3 cp s3://commoncrawl/crawl-data/CC-MAIN-2013-20/segments/1368696381249/warc/CC-MAIN-20130516092621-00000-ip-10-60-113-184.ec2.internal.warc.gz .
      ```

**Table of contents**

- [Common Crawl Athena](common-crawl-athena.md)
- [Common Crawl web graph](common-crawl-web-graph.md)

## ↑ Ancestors (9)

1. [Open web crawling](open-web-crawling.md)
2. [Web crawling](web-crawling.md)
3. [Search engine](search-engine.md)
4. [Software](software-split.md)
5. [Computer](computer-split.md)
6. [Information technology](information-technology.md)
7. [Area of technology](area-of-technology.md)
8. [Technology](technology-split.md)
9. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (3)

- [Job application by Ciro Santilli](job-application-by-ciro-santilli.md)
- [Open PageRank implementation and data](open-pagerank-implementation-and-data.md)
- [Quick fun with the Common Crawl web graph](updates/quick-fun-with-the-common-crawl-web-graph.md)
