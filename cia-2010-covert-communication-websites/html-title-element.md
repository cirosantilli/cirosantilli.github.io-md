# HTML title element

↑ **Parent:** [HTML analysis](html-analysis.md)

The discoverty of a [possible HTML information leaks](possible-html-information-leaks.md) on HTML `<title>` of [webofcheer.com](https://web.archive.org/web/20110207150839/http://webofcheer.com/) which is cryptically set as:
```
pg1c
```
motivated us to download all HTML and have a grep.

We started grepping with:
```
grep -ai '<title>' */index.html
```
and to just get the titles alone for visual inspection:
```
grep -ahi '<title>' */index.html | sed -r 's/^\s*<title>//;s/<\/title>.*//'
```

Some mildly interesting facts include:
- opensourcenewstoday.com is titled just as "Title"
  ```
  opensourcenewstoday.com/index.html:<title>Title</title>
  ```
- a few sites are titled "Untitled Document" e.g.:
  ```
  media-coverage-now.com/index.html:<title>Untitled Document</title>
  newsandsportscentral.com/index.html:  <title>Untitled Document</title>
  newsincirculation.com/index.html:<title>Untitled Document</title>
  newsworldsite.com/index.html:<title>Untitled Document</title>
  primetimemovies.net/index.html:<title>Untitled Document</title>
  unganadormundial.com/index.html:<title>Untitled Document</title>
  ```

  This may have been the default title in Adobe Dreamweaver.
- some others have empty title:
  ```
  aeronet-news.com/index.html:<title></title>
  al-rashidrealestate.com/index.html:             <title></title>
  arabicnewsunfiltered.com/index.html:<title></title>
  dailynewsandsports.com/index.html:<title></title>
  electronictechreviews.com/index.html:<title></title>
  indirectfreekick.com/index.html:<title></title>
  iran-newslink-today.com/index.html:<title></title>
  iraniangoals.com/index.html:<title></title>
  kickitnews.com/index.html:<title></title>
  mediocampodefutbol.com/index.html:<title></title>
  middle-east-newstoday.com/index.html:      <title></title>
  mygadgettech.com/index.html:<title></title>
  sayaara-auto.com/index.html:<title></title>
  techwatchtoday.com/index.html:<title></title>
  the-open-book-online.com/index.html:<title></title>
  thenewsofpakistan.com/index.html:<title></title>
  theworld-news.net/index.html:<title></title>
  todaysengineering.com/index.html:<title></title>
  todaysnewsreports.net/index.html:<title></title>
  worldnewsandent.com/index.html:<title></title>
  ```
- some others are titled just "index" or a variant of it:
  ```
  all-sport-headlines.com/index.html:<title>index</title>
  europeannewsflash.com/index.html:<title>Index</title>
  fgnl.net/index.html:<title>Index Page</title>
  iraniangoalkicks.com/index.html:<title>index</title>
  just-the-news.com/index.html:<title>index</title>
  mide-news.com/index.html:<title>index</title>
  mytravelopian.com/index.html:<title>Index</title>
  noticiasdelmundolatino.com/index.html:<title>index</title>
  pakcricketgrd.com/index.html:  <title>index</title>
  pangawana.com/index.html:<title>index</title>
  sportsnewsfinder.com/index.html:<title>index</title>
  thenewseditor.com/index.html:<title>index</title>
  turkishnewslinks.com/index.html:<title>index2</title>
  wahidfutbol.com/index.html:<title>index</title>
  webscooper.com/index.html:<title>index</title>
  webworldsports.com/index.html:<title>index</title>
  ```
- a few don't have `<title>` at all:
  ```
  b2bworldglobal.com/index.html
  bailandstump.com/index.html
  businessexchangetoday.com/index.html
  commercialspacedesign.com/index.html
  court-masters.com/index.html
  flyingtimeline.com/index.html
  marketflows.net/index.html
  nouvellesetdesrapports.com/index.html
  senderosdemontana.com/index.html
  sixty2media.com/index.htm
  ```
It is impossible to tell if these were oversights, or intentional to simulate common web development quircks. But they are cute in any case.

## ↑ Ancestors (15)

1. [HTML analysis](html-analysis.md)
2. [Fingerprints](fingerprints.md)
3. [Methodology](methodology.md)
4. [CIA 2010 covert communication websites](../cia-2010-covert-communication-websites-split.md)
5. [Central Intelligence Agency](../central-intelligence-agency.md)
6. [American intelligence agency](../american-intelligence-agency.md)
7. [United States Intelligence Community](../united-states-intelligence-community.md)
8. [Intelligence community](../intelligence-community.md)
9. [Secret service](../secret-service.md)
10. [Espionage](../espionage.md)
11. [War](../war.md)
12. [Social science](../social-science.md)
13. [Scientific method](../scientific-method.md)
14. [Science](../science-split.md)
15. [Ciro Santilli's Homepage](../split.md)

## ← Incoming links (1)

- [Possible HTML information leaks](possible-html-information-leaks.md)
