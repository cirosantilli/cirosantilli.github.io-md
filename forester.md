# Forester

↑ **Parent:** [List of personal knowledge base software](list-of-personal-knowledge-base-software.md)

[https://www.jonmsterling.com/tfmt-0001.xml](https://www.jonmsterling.com/tfmt-0001.xml)

Intro/docs: [https://www.jonmsterling.com/jms-005P.xml](https://www.jonmsterling.com/jms-005P.xml). It is very hard to find information in that system however, largely because they don't seem to have a proper recursive cross file table of contents.

This is the project with the closest philosophy to [OurBigBook](ourbigbook.md) that [Ciro Santilli](ciro-santilli-split.md) has ever found. It just tends to be even more idealistic than, [OurBigBook](ourbigbook.md) in general, which is insane!

Source code: [https://sr.ht/~jonsterling/forester](https://sr.ht/~jonsterling/forester). Not on [GitHub](github.md), too much idealism for that.

"Docs" at: [https://www.jonmsterling.com/foreign-forester-jms-005P.xml](https://www.jonmsterling.com/foreign-forester-jms-005P.xml) Sample repo at: [https://github.com/jonsterling/forest](https://github.com/jonsterling/forest) but all parts of interest are in submodules on the authors private Git server.

Example:
- sample source file: [https://git.sr.ht/~jonsterling/public-trees/tree/2356f52303c588fadc2136ffaa168e9e5fbe346c/item/jms-005P.tree](https://git.sr.ht/~jonsterling/public-trees/tree/2356f52303c588fadc2136ffaa168e9e5fbe346c/item/jms-005P.tree)
- appears rendered at: [https://www.jonmsterling.com/foreign-forester-jms-005P.xml](https://www.jonmsterling.com/foreign-forester-jms-005P.xml)

Author's main social media account seems to be: [https://mathstodon.xyz/@jonmsterling](https://mathstodon.xyz/@jonmsterling) e.g. [https://mathstodon.xyz/@jonmsterling/111359099228291730](https://mathstodon.xyz/@jonmsterling/111359099228291730) His home page:
- [https://www.jonmsterling.com/index.xml](https://www.jonmsterling.com/index.xml)
- [https://git.sr.ht/~jonsterling/public-trees/tree/2356f52303c588fadc2136ffaa168e9e5fbe346c/item/jms-0001.tree](https://git.sr.ht/~jonsterling/public-trees/tree/2356f52303c588fadc2136ffaa168e9e5fbe346c/item/jms-0001.tree)

They have `\Include` like [OurBigBook](ourbigbook.md), nice: [https://www.jonmsterling.com/jms-007L.xml](https://www.jonmsterling.com/jms-007L.xml), but OMG that name `\transclude{xxx-NNNN}`!! It seems to be possible to have human readable IDs too if you want: [https://www.jonmsterling.com/foreign-forester-armaëlguéneau.xml](https://www.jonmsterling.com/foreign-forester-armaëlguéneau.xml) is under `trees/public/roladex/armaëlguéneau.tree`.

Headers have open/close:
```
\subtree[jms-00YG]{}
```
[OurBigBook](ourbigbook.md) considered this, but went with `parent=` instead finally to avoid huge lists of close parenthesis at the end of deep nodes.

One really cool thing is that the headers render internal links as clickable, which brings it all closer to the "knowledge base as a formal [ontology](ontology.md)" approach.

Does not encourage human readable IDs, uses stuff like `jms-00YG`.

The markup has relatively few insane constructs, notably you need explicit open paragraphs everywhere `\p{}`?! OMG, too idealistic, not enough pragmatism. There are however a few insane constructs:
- `[]()`: markdown like links
- `[[bluecat]]`: wikilinks (but to raw IDs only, you can't seem to be able to do `[[blue cat]]`
- `#{}` and `##{}` for inline and block maths, though that might just be a sane construct with an insane name
The markup is documented at: [https://www.jonmsterling.com/foreign-forester-jms-007N.xml](https://www.jonmsterling.com/foreign-forester-jms-007N.xml)

Jon has some very good theory of [personal knowledge base](personal-knowledge-base.md), rationalizing several points that [Ciro Santilli](ciro-santilli-split.md) had in his mind but hadn't fully put into words, which is quite cool.

OCaml dependency is not so bad, but it relies on actually [LaTeX](latex.md) for maths, which is bad. Maybe using [JavaScript](javascript.md) for [OurBigBook](ourbigbook.md) wasn't such a bad choice after all, [KaTeX](katex.md) just works.

Viewing the generated output HTML directly requires `security.fileuri.strict_origin_policy` which is sad, but using a local server solves it. So it appears to actually pull pieces together with JavaScript? Also output files have .xml extension, the idealism! They are reconsidering that though: [https://www.jonmsterling.com/foreign-forester-jms-005P.xml#tree-8720](https://www.jonmsterling.com/foreign-forester-jms-005P.xml#tree-8720).

The Ctrl+K article dropdown search navigation is quite cool.

`\rel` and `\meta` allows for arbitrary ontologies between nodes as [semantic triples](semantic-triple.md). But they suffer from one fatal flaw: the relations are headers in themselves. We often want to explain why a relation is true, give intuition to it, and refer to it from other nodes. This is obviously how the brain works: relations are nodes just like objects.

They do appear to be putting full trees on every toplevel regardless how deep and with [JavaScript](javascript.md) turned off e.g.:
- [https://www.jonmsterling.com/foreign-forester-jms-005P.xml](https://www.jonmsterling.com/foreign-forester-jms-005P.xml)
- [https://www.jonmsterling.com/foreign-forester-jms-00WK.xml](https://www.jonmsterling.com/foreign-forester-jms-00WK.xml)
- [https://www.jonmsterling.com/foreign-forester-jms-00WS.xml](https://www.jonmsterling.com/foreign-forester-jms-00WS.xml)
which is cool but will take lots of storage. In [OurBigBook](ourbigbook.md) [Ciro Santilli](ciro-santilli-split.md) only does that on [OurBigBook Web](ourbigbook-web.md) where each page can be dynamically generated.

## ↑ Ancestors (11)

1. [List of personal knowledge base software](list-of-personal-knowledge-base-software.md)
2. [Personal knowledge base software](personal-knowledge-base-software.md)
3. [Personal knowledge base](personal-knowledge-base.md)
4. [Braindumping](braindumping.md)
5. [Brain](brain-split.md)
6. [Organ (anatomy)](organ-anatomy.md)
7. [Level of organization of bodies](level-of-organization-of-bodies.md)
8. [Biology](biology-split.md)
9. [Natural science](natural-science.md)
10. [Science](science-split.md)
11. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (1)

- [Knowledge graph editors](ourbigbook-com/knowledge-graph-editors.md)
