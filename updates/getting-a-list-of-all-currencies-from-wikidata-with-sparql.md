# Getting a list of all currencies from Wikidata with SPARQL

↑ **Parent:** [Updates](../updates-split.md)

[https://opendata.stackexchange.com/questions/1560/how-can-i-get-a-list-of-currencies-from-wikidata/21839#21839](https://opendata.stackexchange.com/questions/1560/how-can-i-get-a-list-of-currencies-from-wikidata/21839#21839)

I've had a bit more fun with [SPARQL](../sparql.md) and [Wikidata](../wikidata.md).

This one was way harder than my previous fun with "find the oldest people who won a given prize" ([Nobel Prize](../nobel-prize-split.md)/[Oscar](https://ourbigbook.com/-/topic/oscar)) [https://mastodon.social/@cirosantilli/112689376315990248](https://mastodon.social/@cirosantilli/112689376315990248) because unlike those prizes where all the decisions are centralized, countries are much more complicated beasts, with changing currencies and international recognition.

This was a good experience to see a few ways in which Wikidata is inconsistent, with the same concept being expressed in multiple different ways, e.g. "end time" property of the current vs the superior "end time" qualifier.

Particularly bad is the notion of a "[deprecated rank](https://www.wikidata.org/wiki/Help:Ranking#Deprecated_rank)", that should really not exist.

This is exactly the type of semi interactive data munching that I like to do, a bit in the same vein as [CIA 2010 covert communication websites](../cia-2010-covert-communication-websites-split.md) and [Cool data embedded in the Bitcoin blockchain](../cool-data-embedded-in-the-bitcoin-blockchain-split.md).

As you might imagine, the [secret services](../secret-service.md) use exactly this type of knowledge modelling to do their dirty business, e.g. [Gaffer](https://github.com/gchq/Gaffer) by the [GCHQ](../gchq.md).

If only I weren't such a rebel, I'd be a perfect fit for the [intelligence agencies](../intelligence-agency.md).

This is the best monstrosity I had the patience to come up with:
```
SELECT
  ?currency
  (GROUP_CONCAT(DISTINCT ?currencyIsoCode; SEPARATOR=", ") AS ?currencyIsoCodes)
  ?currencyLabel
  (GROUP_CONCAT(DISTINCT ?countryLabel; SEPARATOR=", ") AS ?countries)
WHERE {
  ?country wdt:P31/wdt:P279* wd:Q6256. # is country
  ?country p:P38 ?countryHasCurrency.
  ?countryHasCurrency ps:P38 ?currency.
  ?countryHasCurrency wikibase:rank ?countryHasCurrencyRank.
  OPTIONAL {
    ?currency p:P498 ?currencyHasIsoCode.
    ?currencyHasIsoCode ps:P498 ?currencyIsoCode.
  }
  FILTER NOT EXISTS {?country wdt:P576 ?countryAbolished}
  FILTER NOT EXISTS {?currency wdt:P576 ?currencyAbolished}
  FILTER NOT EXISTS {?currency wdt:P582 ?currencyEndTime}
  FILTER NOT EXISTS {?countryHasCurrency pq:P582 ?countryHasCurrencyEndtime}
  FILTER (?countryHasCurrencyRank != wikibase:DeprecatedRank)
  FILTER (!bound(?currencyHasIsoCode) || ?currencyHasIsoCode != wikibase:DeprecatedRank)
  # TODO makes query take timeout? Why? Needed to exclude PLZ.
  FILTER NOT EXISTS {?currencyHasIsoCode pq:P582 ?currencyHasIsoCodeEndtime}
  SERVICE wikibase:label {
    bd:serviceParam wikibase:language "[AUTO_LANGUAGE],en".
    ?currency rdfs:label ?currencyLabel .
    ?country rdfs:label ?countryLabel .
  }
}
GROUP BY ?currency ?currencyLabel
ORDER BY ?currencyIsoCodes ?currencyLabel
```
It got quite close to the ISO 4217 list.

I was drawn into this waste of time after I noticed that someone had managed to create the Wikipedia of [PsiQuantum](../psiquantum.md) which I had tried earlier but got deleted: [https://mastodon.social/@cirosantilli/113488891292906243](https://mastodon.social/@cirosantilli/113488891292906243), and then I made the mistake of having a look at the [Wikidata](../wikidata.md) page of [PsiQuantum](../psiquantum.md).

<a id="image-500-000-transnistrian-ruble-banknote-1997-series"></a>
![](https://files.mastodon.social/media_attachments/files/113/509/536/025/260/785/original/428906b92ab725f5.jpg)

**[Figure 25](#image-500-000-transnistrian-ruble-banknote-1997-series). 500,000 Transnistrian ruble banknote 1997 series**. This is one of the most widely used currencies which does not have an ISO 4217 code.

Announcements:
- [https://mastodon.social/@cirosantilli/113509491731720236](https://mastodon.social/@cirosantilli/113509491731720236)
- [https://x.com/cirosantilli/status/1858846619359219848](https://x.com/cirosantilli/status/1858846619359219848)

I also had one more fun with: [https://opendata.stackexchange.com/questions/15750/structured-data-for-nobel-prizes/21847#21847](https://opendata.stackexchange.com/questions/15750/structured-data-for-nobel-prizes/21847#21847) getting some basic info about [Nobel Prize](../nobel-prize-split.md) winners, and noticed one, [John Sulston](../john-sulston.md), [2002 Nobel Prize in Physiology and Medicine](../2002-nobel-prize-in-physiology-and-medicine.md) laureate, who likely has the wrong place of birth on his Nobel Prize profile: [https://www.nobelprize.org/prizes/medicine/2002/sulston/facts/](https://www.nobelprize.org/prizes/medicine/2002/sulston/facts/) which is funny. I suggested the change now. Edit they fixed it after I pointed it out:
- bad: [https://web.archive.org/web/20241008022931/https://www.nobelprize.org/prizes/medicine/2002/sulston/facts/](https://web.archive.org/web/20241008022931/https://www.nobelprize.org/prizes/medicine/2002/sulston/facts/)
- good: [https://web.archive.org/web/20241127133204/https://www.nobelprize.org/prizes/medicine/2002/sulston/facts/](https://web.archive.org/web/20241127133204/https://www.nobelprize.org/prizes/medicine/2002/sulston/facts/)

Another highlight was [1913 Nobel Prize in Chemistry](https://ourbigbook.com/-/topic/1913-nobel-prize-in-chemistry) laureate [Alfred Werner](https://ourbigbook.com/-/topic/alfred-werner) who born either in Mulhouse in Alsace, France, or in "Yo no sé qué me pasó" ("I don't know what happened to me" in [Spanish](../spanish-language.md)), a [1986 song by Mexican singer Juan Gabriel](https://www.youtube.com/watch?v=83PeS6bKla0).

Announcements:
- [https://mastodon.social/@cirosantilli/113528952716463018](https://mastodon.social/@cirosantilli/113528952716463018)
- [https://x.com/cirosantilli/status/1860088866335785187](https://x.com/cirosantilli/status/1860088866335785187)

![](https://upload.wikimedia.org/wikipedia/commons/f/fe/John_Sulston_%282008%29.jpg)

**[Figure 26](#-/556)** [Source](https://commons.wikimedia.org/wiki/File:John_Sulston_%282008%29.jpg).

Also at [https://opendata.stackexchange.com/questions/21849/how-to-get-a-list-of-all-nobel-prize-winners-who-never-had-a-doctorate-from-wiki/21850#21850](https://opendata.stackexchange.com/questions/21849/how-to-get-a-list-of-all-nobel-prize-winners-who-never-had-a-doctorate-from-wiki/21850#21850) I tried to get the list of [Nobel Prize laureates who don't have a PhD](../rebel-without-a-phd.md). I think the query was correct, but [Wikidata](../wikidata.md) data is just too incomplete. Related:
- [https://www.reddit.com/r/NoStupidQuestions/comments/mv85av/has_anybody_without_a_phd_ever_won_the_nobel/](https://www.reddit.com/r/NoStupidQuestions/comments/mv85av/has_anybody_without_a_phd_ever_won_the_nobel/)
- [https://www.quora.com/Has-anyone-ever-won-a-Nobel-Prize-without-a-PhD](https://www.quora.com/Has-anyone-ever-won-a-Nobel-Prize-without-a-PhD)

## ↑ Ancestors (3)

1. [Updates](../updates-split.md)
2. [Ciro Santilli](../ciro-santilli-split.md)
3. [Ciro Santilli's Homepage](../split.md)

## ← Incoming links (1)

- [John Sulston](../john-sulston.md)
