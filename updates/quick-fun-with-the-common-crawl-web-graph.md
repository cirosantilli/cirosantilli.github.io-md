# Quick fun with the Common Crawl web graph

↑ **Parent:** [Updates](../updates-split.md)

[https://github.com/cirosantilli/cirosantilli.github.io/issues/198](https://github.com/cirosantilli/cirosantilli.github.io/issues/198). Previously at: [https://stackoverflow.com/questions/31321009/best-more-standard-graph-representation-file-format-graphson-gexf-graphml/79467334#79467334](https://stackoverflow.com/questions/31321009/best-more-standard-graph-representation-file-format-graphson-gexf-graphml/79467334#79467334) but [Stack Overflow fucking deleted the question](../stack-overflow-content-deletion.md).

I wanted to do a quick exploration of [open PageRank implementation and data](../open-pagerank-implementation-and-data.md).

My general motivation for this is that a [PageRank](../pagerank.md)-like algorithm could be useful for more accurate user and article ranking on [OurBigBook](../ourbigbook.md), see: [Section "PageRank-like ranking"](../ourbigbook-com/pagerank-like-ranking.md)

But it could also be just generally cool to apply it to other [graph](../graph-discrete-mathematics.md) datasets, e.g. for computing an [Wikipedia internal PageRank](../wikipedia-internal-pagerank.md).

A quick [Google](../google-split.md) reveals only [Open PageRank](../open-pagerank.md), but their methods are apparently closed source.

Then I had a look at the [Common Crawl web graph](../common-crawl-web-graph.md) data to see if I could easily calculate it myself, and... they already have it! See: [Section "Common Crawl web graph official PageRank"](../common-crawl-web-graph-official-pagerank.md)

Their graph dumps are in [BVGraph](../bvgraph.md) [graph file format](../graph-file-format.md), which is the native format of the [WebGraph](../webgraph-software.md) framework, which implements the format and algorithms such as [PageRank](../pagerank.md).

The only thing I miss is a command line interface to calculate the PageRank. That would be so awesome.

The more I look at it the more I love [Common Crawl](../common-crawl.md).

Announcements:
- [https://mastodon.social/@cirosantilli/114070985511493835](https://mastodon.social/@cirosantilli/114070985511493835)
- [https://x.com/cirosantilli/status/1894777704517406852](https://x.com/cirosantilli/status/1894777704517406852)

In cc-main-2024-25-dec-jan-feb-domain-ranks.txt:
- `cirosantilli.com` was ranked ~453k
- `ourbigbook.com` was at ~606k

## ↑ Ancestors (3)

1. [Updates](../updates-split.md)
2. [Ciro Santilli](../ciro-santilli-split.md)
3. [Ciro Santilli's Homepage](../split.md)
