# Quick fun with the Common Crawl web graph

↑ **Parent:** [Updates](../updates-split.md)

<a id="_476"></a>
[https://github.com/cirosantilli/cirosantilli.github.io/issues/198](https://github.com/cirosantilli/cirosantilli.github.io/issues/198). Previously at: [https://stackoverflow.com/questions/31321009/best-more-standard-graph-representation-file-format-graphson-gexf-graphml/79467334#79467334](https://stackoverflow.com/questions/31321009/best-more-standard-graph-representation-file-format-graphson-gexf-graphml/79467334#79467334) but [Stack Overflow fucking deleted the question](../stack-overflow-content-deletion.md).

<a id="_477"></a>
I wanted to do a quick exploration of [open PageRank implementation and data](../open-pagerank-implementation-and-data.md).

<a id="_478"></a>
My general motivation for this is that a [PageRank](../pagerank.md)-like algorithm could be useful for more accurate user and article ranking on [OurBigBook](../ourbigbook.md), see: [Section "PageRank-like ranking"](../ourbigbook-com/pagerank-like-ranking.md)

<a id="_479"></a>
But it could also be just generally cool to apply it to other [graph](../graph-discrete-mathematics.md) datasets, e.g. for computing an [Wikipedia internal PageRank](../wikipedia-internal-pagerank.md).

<a id="_480"></a>
A quick [Google](../google-split.md) reveals only [Open PageRank](../open-pagerank.md), but their methods are apparently closed source.

<a id="_481"></a>
Then I had a look at the [Common Crawl web graph](../common-crawl-web-graph.md) data to see if I could easily calculate it myself, and... they already have it! See: [Section "Common Crawl web graph official PageRank"](../common-crawl-web-graph-official-pagerank.md)

<a id="_482"></a>
Their graph dumps are in [BVGraph](../bvgraph.md) [graph file format](../graph-file-format.md), which is the native format of the [WebGraph](../webgraph-software.md) framework, which implements the format and algorithms such as [PageRank](../pagerank.md).

<a id="_483"></a>
The only thing I miss is a command line interface to calculate the PageRank. That would be so awesome.

<a id="_484"></a>
The more I look at it the more I love [Common Crawl](../common-crawl.md).

<a id="_485"></a>
Announcements:<a id="_486"></a>

<a id="_487"></a>
- [https://mastodon.social/@cirosantilli/114070985511493835](https://mastodon.social/@cirosantilli/114070985511493835)
<a id="_488"></a>
- [https://x.com/cirosantilli/status/1894777704517406852](https://x.com/cirosantilli/status/1894777704517406852)

<a id="_489"></a>
In cc-main-2024-25-dec-jan-feb-domain-ranks.txt:<a id="_490"></a>

<a id="_491"></a>
- `cirosantilli.com` was ranked ~453k
<a id="_492"></a>
- `ourbigbook.com` was at ~606k

## ↑ Ancestors (3)

1. [Updates](../updates-split.md)
2. [Ciro Santilli](../ciro-santilli-split.md)
3. [Ciro Santilli's Homepage](../split.md)
