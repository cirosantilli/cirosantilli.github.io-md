# Cheeky fuzzy fingerprint: the domain name contains `news`

↑ **Parent:** [The hard: finding new IP ranges!](the-hard-finding-new-ip-ranges.md)

<a id="_26"></a>
They really screwed up there:<a id="_27"></a>

```
$ jq <hits.json '.[].host' | wc
    361     361    7777
$ jq <hits.json '.[].host' | grep news | wc
    129     129    2809
```

<a id="_28"></a>
More than 1/3 of my hits found contain the word "news" in the title!!! E.g.:<a id="_29"></a>

```
global-view-news.com
firstnewssource.com
theworldnewsfeeds.com
pars-technews.com
newdaynewsonline.com
sportsnewsfinder.com
newsworldsite.com
todaysnewsreports.net
hassannews.net
weblognewsinfo.com
newsincirculation.com
```

## ↑ Ancestors (7)

1. [The hard: finding new IP ranges!](the-hard-finding-new-ip-ranges.md)
2. [Methodology](methodology.md)
3. [CIA 2010 covert communication websites](cia-2010-covert-communication-websites.md)
4. [Aratu Week 2024 Talk by Ciro Santilli: My Best Random Projects](../aratu-week-2024-talk-by-ciro-santilli-split.md)
5. [Talk by Ciro Santilli](../talk-by-ciro-santilli.md)
6. [Ciro Santilli](../ciro-santilli-split.md)
7. [Ciro Santilli's Homepage](../split.md)
