# Nobel Prize winner without a PhD

↑ **Parent:** [Rebel without a PhD](rebel-without-a-phd.md)

Notably in [STEM](science-technology-engineering-and-mathematics.md), not so interested in literature of course:
- [https://www.reddit.com/r/NoStupidQuestions/comments/mv85av/has_anybody_without_a_phd_ever_won_the_nobel/](https://www.reddit.com/r/NoStupidQuestions/comments/mv85av/has_anybody_without_a_phd_ever_won_the_nobel/)
- [https://www.quora.com/Has-anyone-ever-won-a-Nobel-Prize-without-a-PhD](https://www.quora.com/Has-anyone-ever-won-a-Nobel-Prize-without-a-PhD)
- [https://groups.google.com/g/diybio/c/SiBRwxVkZmc?pli=1](https://groups.google.com/g/diybio/c/SiBRwxVkZmc?pli=1)

Here's a [SPARQL](sparql.md) sketch for [Wikidata](wikidata.md) that can be run at [https://query.wikidata.org/](https://query.wikidata.org/). It gathers all the relevant data, but TODO we don't know how to do the proper query yet:
```
# List of living Nobel Laureates sorted by date of birth 
SELECT DISTINCT ?recipient ?recipientLabel $birthDate ?awardLabel ?nobelDate ?educatedAtLabel ?academicDegree ?academicDegreeLabel ?doctorateDate
WHERE { 
  ?recipient wdt:P31 wd:Q5 ; # recepient is human (Peace prize can go to organizations) 
             wdt:P569 ?birthDate ; 
             p:P166 ?awardStat . # recepient was awarded something 
  ?awardStat ps:P166 ?award .
  ?award wdt:P279* wd:Q7191 . # received any subclass of nobel prize (physics, chemistry, etc.) 
  ?awardStat pq:P585 ?nobelDate .
  ?recipient p:P69 ?recipientEducatedAt .
  ?recipientEducatedAt ps:P69 ?educatedAt .
  ?recipientEducatedAt pq:P512 ?academicDegree .
  ?academicDegree wdt:P279* wd:Q849697 .
  OPTIONAL{ ?recipientEducatedAt pq:P582 ?doctorateDate . }
  SERVICE wikibase:label { bd:serviceParam wikibase:language "en" . } 
} 
ORDER BY ASC(?birthDate) ASC(?nobelDate) ASC(?awardLabel)
```

## ↑ Ancestors (8)

1. [Rebel without a PhD](rebel-without-a-phd.md)
2. [Doctor of Philosophy](doctor-of-philosophy.md)
3. [Academia](academia.md)
4. [Education](education-split.md)
5. [Social technology](social-technology-split.md)
6. [Area of technology](area-of-technology.md)
7. [Technology](technology-split.md)
8. [Ciro Santilli's Homepage](split.md)
