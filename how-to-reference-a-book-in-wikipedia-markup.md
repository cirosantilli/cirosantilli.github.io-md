# How to reference a book in Wikipedia markup?

↑ **Parent:** [MediaWiki markup](mediawiki-markup.md)

Their reference markup is incredibly overengineered, convoluted, and underdocumented, it is unbelivable!

Use the reference:
```
This is a fact.{{sfn|Schweber|1994|p=487}}
```

Define the reference:
```
===Sources===
{{refbegin|2|indent=yes}}
*{{Cite book|author-link=Silvan S. Schweber |title=QED and the Men Who Made It: Dyson, Feynman, Schwinger, and Tomonaga|last=Schweber|first=Silvan S.|location=Princeton|publisher=University Press|year=1994 |isbn=978-0-691-03327-3 |url=https://archive.org/details/qedmenwhomadeitd0000schw/page/492 |url-access=registration}}
{{refend}}
```

`sfn` is magic and matches the the author last name and date from the `Cite`, it is documented at: [https://en.wikipedia.org/wiki/Template:Sfn](https://en.wikipedia.org/wiki/Template:Sfn)

Unforutunately, if there are multiple duplicate `Cite`s inline in the article, it will complain that there are multiple definitions, and you have to first factor out the article by replacing all those existing `Cite` with `sfn`, and keeping just one `Cite` at the bottom. What a pain...

You can also link to a specific page of the book, e.g. if it is a book is on [Internet Archive Open Library](internet-archive-open-library.md) with:
```
{{sfn|Murray|1997|p=[https://archive.org/details/supermenstory00murr/page/86 86]}}
```

For multiple pages should use `pp=` instead of `p=`. Does not seem to make much difference on the rendered output besides showing `p.` vs `pp.`, but so be it:
```
{{sfn|Murray|1997|pp=[https://archive.org/details/supermenstory00murr/page/86 86-87]}}
```

## ↑ Ancestors (10)

1. [MediaWiki markup](mediawiki-markup.md)
2. [MediaWiki](mediawiki.md)
3. [Wikipedia](wikipedia.md)
4. [List of Wikis](list-of-wikis.md)
5. [Wiki](wiki.md)
6. [Collaborative writing platform](collaborative-writing-platform.md)
7. [Website genre](website-genre.md)
8. [Website](website-split.md)
9. [Art](art-split.md)
10. [Ciro Santilli's Homepage](split.md)
