# How to use a single source multiple times in a Wikipedia article?

↑ **Parent:** [Wikipedia HOWTO](wikipedia-howto.md)

[https://www.quora.com/On-Wikipedia-how-can-you-cite-the-same-source-more-than-once-without-them-becoming-separate-references](https://www.quora.com/On-Wikipedia-how-can-you-cite-the-same-source-more-than-once-without-them-becoming-separate-references)

[https://en.wikipedia.org/wiki/Help:Footnotes#Footnotes:_using_a_source_more_than_once](https://en.wikipedia.org/wiki/Help:Footnotes#Footnotes:_using_a_source_more_than_once) gives the following method:

Definition, anywhere on article, likely ideally as the first usage:
```
<ref name="myname">{{cite web ...}}</ref>
```

And then you can use it later on as:
```
<ref name="myname" />
```
which automatically expands the exact same thing, or using the shortcut:
```
{{r|myname}}
```

To cite multiple pages of a book: [https://en.wikipedia.org/wiki/Wikipedia:Citing_sources#Citing_multiple_pages_of_the_same_source](https://en.wikipedia.org/wiki/Wikipedia:Citing_sources#Citing_multiple_pages_of_the_same_source), the best method is to define and use the reference without adding the `p` or `location` in `cite` as:
```
<ref name="googleStory">{{cite book |title=The Google Story}}</ref>{{rp|p=123}}
```
Do not set the page in `cite`, otherwise it shows up on the references. Instead we use the [`{{rp}}` template](https://en.wikipedia.org/wiki/Template:Rp). And then use the reference with the [`{{r}}`](https://en.wikipedia.org/wiki/Template:R) template as:
```
{{r|googleStory|p=456}}
```
or for multiple pages:
```
{{r|googleStory|pp=123, 156-158}}
```

## ↑ Ancestors (9)

1. [Wikipedia HOWTO](wikipedia-howto.md)
2. [Wikipedia](wikipedia.md)
3. [List of Wikis](list-of-wikis.md)
4. [Wiki](wiki.md)
5. [Collaborative writing platform](collaborative-writing-platform.md)
6. [Website genre](website-genre.md)
7. [Website](website-split.md)
8. [Art](art-split.md)
9. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (2)

- [How to cite a book on Wikipedia](how-to-cite-a-book-on-wikipedia.md)
- [Wikipedia](wikipedia.md)
