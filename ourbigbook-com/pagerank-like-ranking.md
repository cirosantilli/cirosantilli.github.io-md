# PageRank-like ranking

↑ **Parent:** [Feature ideas](feature-ideas.md)

It would be really cool to have a [PageRank](../pagerank.md)-link algorithm that answers the key questions:
- what is the best content for subject X.

  For example, if you are reading `cirosantilli/riemann-integral` and it is crap, you would be able to click the button

  > Versions by other authors

  which leads you to the URL: [http://ourbigbook.com/subject/mathematics](http://ourbigbook.com/subject/mathematics). This URL then contains a list of all pages people have written about the subject `mathematics`, sorted by some algorithm, containing for example:
  - [http://ourbigbook.com/johnsmith/riemann-integral](http://ourbigbook.com/johnsmith/riemann-integral)
  - [http://ourbigbook.com/cirosantilli/riemann-integral](http://ourbigbook.com/cirosantilli/riemann-integral)

  This URL would also contain a list of issues/comments that are related to the subject.
- who knows the most about subject X. This can be found by visiting: [http://ourbigbook.com/users/mathematics](http://ourbigbook.com/users/mathematics) "Top Mathematics users", which would contain the list of users sorted by the algorithm:
  - [http://ourbigbook.com/johnsmith](http://ourbigbook.com/johnsmith)
  - [http://ourbigbook.com/cirosantilli](http://ourbigbook.com/cirosantilli)
However, Ciro has decided to leave this for phase two [action plan](action-plan.md), because it is impossible to tune such an algorithm if you have no users or test data.

Perhaps it is also worth looking into [ExpertRank](../expertrank.md), they appear to do some kind of "expert in this area", but with [clustering](../cluster-analysis.md) (unlike us, where the clustering would be more explicit).

Other dump of things worth looking into:
- [https://en.wikipedia.org/wiki/Hilltop_algorithm](https://en.wikipedia.org/wiki/Hilltop_algorithm)

## ↑ Ancestors (7)

1. [Feature ideas](feature-ideas.md)
2. [OurBigBook.com](../ourbigbook-com-split.md)
3. [OurBigBook Web](../ourbigbook-web.md)
4. [OurBigBook](../ourbigbook.md)
5. [Ciro Santilli's projects](../ciro-santilli-s-projects-split.md)
6. [Ciro Santilli](../ciro-santilli-split.md)
7. [Ciro Santilli's Homepage](../split.md)

## ← Incoming links (2)

- [Action plan](action-plan.md)
- [Quick fun with the Common Crawl web graph](../updates/quick-fun-with-the-common-crawl-web-graph.md)
