# JavaScript with SHAs

↑ **Parent:** [JavaScript reverse engineering](javascript-reverse-engineering.md)

<a id="_6593"></a>
There are two types of JavaScript found so far. The ones with SHA and the ones without. There are only 2 examples of JS with SHA:<a id="_6594"></a>

<a id="_6595"></a>
- iraniangoals.com: [https://web.archive.org/web/20110202091909/http://iraniangoals.com/journal.js](https://web.archive.org/web/20110202091909/http://iraniangoals.com/journal.js) Commented at: [iraniangoals.com JavaScript reverse engineering](iraniangoals-com-javascript-reverse-engineering.md)
<a id="_6596"></a>
- iranfootballsource.com: [https://web.archive.org/web/20110202091901/http://iranfootballsource.com/futbol.js](https://web.archive.org/web/20110202091901/http://iranfootballsource.com/futbol.js)
<a id="_6597"></a>
- kukrinews.com: [https://web.archive.org/web/20100513094909/http://kukrinews.com/news.js](https://web.archive.org/web/20100513094909/http://kukrinews.com/news.js)
<a id="_6598"></a>
- todaysnewsandweather-ru.com: [https://web.archive.org/web/20110207094735/http://todaysnewsandweather-ru.com/blacksea.js](https://web.archive.org/web/20110207094735/http://todaysnewsandweather-ru.com/blacksea.js)
Both files start with precisely the same string:<a id="_6599"></a>

```
var ms="\u062F\u0631\u064A\u0627\u0641\u062A\u06CC",lc="\u062A\u0647\u064A\u0647 \u0645\u062A\u0646",mn="\u0628\u0631\u062F\u0627\u0632\u0634 \u062F\u0631 \u062C\u0631\u064A\u0627\u0646 \u0627\u0633\u062A...\u0644\u0637\u0641\u0627 \u0635\u0628\u0631 \u0643\u0646\u064A\u062F",lt="\u062A\u0647\u064A\u0647 \u0645\u062A\u0646",ne="\u067E\u0627\u0633\u062E",kf="\u062E\u0631\u0648\u062C",mb="\u062D\u0630\u0641",mv="\u062F\u0631\u064A\u0627\u0641\u062A\u06CC",nt="\u0627\u0631\u0633\u0627\u0644",ig="\u062B\u0628\u062A \u063A\u0644\u0637. \u062C\u0647\u062A \u062A\u062C\u062F\u064A\u062F \u062B\u0628\u062A \u0635\u0641\u062D\u0647 \u0631\u0627 \u0628\u0627\u0632\u0622\u0648\u0631\u06CC \u06A9\u0646\u064A\u062F",hs="\u063A\u064A\u0631 \u0642\u0627\u0628\u0644 \u0627\u062C\u0631\u0627. \u062E\u0637\u0627 \u062F\u0631 \u0627\u062A\u0651\u0635\u0627\u0644",ji="\u063A\u064A\u0631 \u0642\u0627\u0628\u0644 \u0627\u062C\u0631\u0627. \u062E\u0637\u0627 \u062F\u0631 \u0627\u062A\u0651\u0635\u0627\u0644",ie="\u063A\u064A\u0631 \u0642\u0627\u0628\u0644 \u0627\u062C\u0631\u0627. \u062E\u0637\u0627 \u062F\u0631 \u0627\u062A\u0651\u0635\u0627\u0644",gc="\u0633\u0648\u0627\u0631 \u06A9\u0631\u062F\u0646 \u062A\u06A9\u0645\u064A\u0644 \u0634\u062F",gz="\u0645\u0637\u0645\u0626\u0646\u064A\u062F \u06A9\u0647 \u0645\u064A\u062E\u0648\u0627\u0647\u064A\u062F \u067E\u064A\u0627\u0645 \u0631\u0627 \u062D\u0630\u0641 \u06A9\u0646\u064A\u062F\u061F"
```

<a id="_6600"></a>
Good fingerprint present in all of them:<a id="_6601"></a>

```
throw new Error("B64 D.1");};if(at[1]==-1){throw new Error("B64 D.2");};if(at[2]==-1){if(f<ay.length){throw new Error("B64 D.3");};dg=2;}else if(at[3]==-1){if(f<ay.length){throw new Error("B64 D.4")
```

**Table of contents**

- [iraniangoals.com JavaScript reverse engineering](iraniangoals-com-javascript-reverse-engineering.md)

## ↑ Ancestors (17)

1. [JavaScript reverse engineering](javascript-reverse-engineering.md)
2. [JS comms](js-comms.md)
3. [Communication mechanism](communication-mechanism.md)
4. [Reverse engineering](reverse-engineering.md)
5. [Methodology](methodology.md)
6. [CIA 2010 covert communication websites](../cia-2010-covert-communication-websites-split.md)
7. [Central Intelligence Agency](../central-intelligence-agency.md)
8. [American intelligence agency](../american-intelligence-agency.md)
9. [United States Intelligence Community](../united-states-intelligence-community.md)
10. [Intelligence community](../intelligence-community.md)
11. [Secret service](../secret-service.md)
12. [Espionage](../espionage.md)
13. [War](../war.md)
14. [Social science](../social-science.md)
15. [Scientific method](../scientific-method.md)
16. [Science](../science-split.md)
17. [Ciro Santilli's Homepage](../split.md)

## ← Incoming links (3)

- [Communication mechanism](communication-mechanism.md)
- [JS CDX scanning](js-cdx-scanning.md)
- [List of websites](list-of-websites.md)
