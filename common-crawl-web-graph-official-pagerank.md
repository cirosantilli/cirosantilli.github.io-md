# Common Crawl web graph official PageRank

↑ **Parent:** [Open PageRank implementation and data](open-pagerank-implementation-and-data.md)  
🏷️ **Tags:** [Common Crawl web graph](common-crawl-web-graph.md)

As of 2025 [Common Crawl web graph](common-crawl-web-graph.md) also dumps its own [PageRank](pagerank.md) for each release. See e.g. the file `cc-main-2024-25-dec-jan-feb-host-ranks.txt.gz` from at: [https://data.commoncrawl.org/projects/hyperlinkgraph/cc-main-2024-25-dec-jan-feb/index.html](https://data.commoncrawl.org/projects/hyperlinkgraph/cc-main-2024-25-dec-jan-feb/index.html) The first 20 rows are:
```
#harmonicc_pos  #harmonicc_val  #pr_pos #pr_val #host_rev
1       3.4626736E7     3       0.005384977821460953    com.facebook
2       3.42356E7       2       0.007010813553170503    com.googleapis.fonts
3       3.007577E7      1       0.008634952900502719    com.google
4       3.0036014E7     4       0.004411782034463272    com.googletagmanager
5       2.9900088E7     5       0.0036940035989790525   com.youtube
6       2.9537252E7     6       0.0032959808223701      com.instagram
7       2.9092556E7     9       0.0027616338842143423   com.twitter
8       2.7346152E7     7       0.0032101332824200743   com.gstatic.fonts
9       2.6818654E7     11      0.0017699438634060259   com.linkedin
10      2.5383126E7     8       0.0027849243241515574   org.gmpg
11      2.3747762E7     12      0.0016577826631867043   com.google.maps
12      2.3514198E7     15      0.0013399414238881337   com.googleapis.ajax
13      2.3504832E7     16      0.0012791339750445332   com.google.play
14      2.337092E7      47      3.794876113587071E-4    be.youtu
15      2.2925148E7     14      0.0013857916784687163   com.cloudflare.cdnjs
16      2.2851038E7     18      0.0012066313543285154   com.google.plus
17      2.2833728E7     13      0.0015745738381307273   org.wordpress
18      2.2830926E7     36      6.02400471665468E-4     com.pinterest
19      2.27056E7       45      4.001342924757244E-4    com.google.support
20      2.2687704E7     24      9.381217848819624E-4    net.jsdelivr.cdn
```
so quite plausible, except for `org.gmpg`. What the fuck is that and why is it ranked so high? Is it a quirk with the hosts inside subdomains?

Perhaps a more relevant dump might be the domain-only one `cc-main-2024-25-dec-jan-feb-domain-ranks.txt.gz`:
```
#harmonicc_pos  #harmonicc_val  #pr_pos #pr_val #host_rev       #n_hosts
1       3.1238044E7     3       0.01110707704411023     com.facebook    3632
2       3.0950192E7     2       0.016650558868491434    com.googleapis  3470
3       3.000803E7      1       0.01749148008448444     com.google      14053
4       2.7319046E7     5       0.00670112168785935     com.instagram   789
5       2.7020862E7     7       0.005464885844102939    com.youtube     1628
6       2.6954494E7     4       0.007740808154448889    com.googletagmanager    42
7       2.6344278E7     8       0.0052073382920908295   com.twitter     712
8       2.5414934E7     6       0.0058790483755603844   com.gstatic     171
9       2.4803688E7     11      0.0038589161241338816   com.linkedin    690
10      2.4683842E7     10      0.004929923081722034    org.gmpg        2
11      2.3575146E7     9       0.005111453489231459    com.cloudflare  951
12      2.2735678E7     14      0.002131882799792225    com.gravatar    98
13      2.2356142E7     12      0.002513741654851857    org.wordpress   1250
14      2.2132868E7     15      0.0019991529719988496   com.apple       3261
15      2.2095914E7     31      0.0010706467268355303   org.wikipedia   2099
16      2.2057972E7     21      0.0015644264715267535   com.pinterest   360
17      2.1941062E7     40      8.52391305373285E-4     be.youtu        15
18      2.1826452E7     16      0.0018442726685905964   net.jsdelivr    40
19      2.1764224E7     34      9.747994384099485E-4    gl.goo  951
20      2.1690982E7     35      9.740295347556525E-4    com.vimeo 
```
But nope, `org.gmpg` is still there!

[https://vigna.di.unimi.it/ftp/papers/GraphStructure.pdf](https://vigna.di.unimi.it/ftp/papers/GraphStructure.pdf) comments on it: 

> for instance, gmpg.org is the reference for a vocabulary that describes relationships

so it appears to be a computer-readable [ontology](ontology.md) mechanism in the lines of [Resource Description Framework](resource-description-framework.md) which interlinks many websites. The article also mentions another interesting noise in `miibeian.gov.cn` which every Chinese website is required to link to for their [ICP license](https://ourbigbook.com/go/topic/icp-license).

The source code for it seem to be at: [https://github.com/commoncrawl/cc-webgraph](https://github.com/commoncrawl/cc-webgraph) and seems to use the [Java](java-programming-language.md) version of the [WebGraph](webgraph-software.md) quite directly on their [BVGraph](bvgraph.md) dump. There is apparently no [CLI](command-line-interface.md) for [PageRank](pagerank.md) however unfortunately, they have to use a bit of [Java](java-programming-language.md) code. That would be so awesome!

**Table of contents**

- [Common Crawl WWW Ranking](common-crawl-www-ranking.md)

## ↑ Ancestors (11)

1. [Open PageRank implementation and data](open-pagerank-implementation-and-data.md)
2. [PageRank](pagerank.md)
3. [Google](google-split.md)
4. [Internet company](internet-company.md)
5. [Internet](internet.md)
6. [Computer network](computer-network.md)
7. [Computer](computer-split.md)
8. [Information technology](information-technology.md)
9. [Area of technology](area-of-technology.md)
10. [Technology](technology-split.md)
11. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (4)

- [Common Crawl web graph](common-crawl-web-graph.md)
- [Common Crawl WWW Ranking](common-crawl-www-ranking.md)
- [Open PageRank implementation and data](open-pagerank-implementation-and-data.md)
- [Quick fun with the Common Crawl web graph](updates/quick-fun-with-the-common-crawl-web-graph.md)
