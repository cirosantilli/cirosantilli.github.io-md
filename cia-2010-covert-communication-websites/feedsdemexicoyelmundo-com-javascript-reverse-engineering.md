<h1 id="feedsdemexicoyelmundo-com-javascript-reverse-engineering">feedsdemexicoyelmundo.com JavaScript reverse engineering</h1>

↑ **Parent:** [JavaScript reverse engineering](javascript-reverse-engineering.md)

<a id="_6606"></a>
The [JavaScript](../javascript.md) of each website appears to be quite small and similarly sized. They are all minimized, but have reordered things around a bit.

<a id="_6607"></a>
For example consider: [https://web.archive.org/web/20110202190932/http://feedsdemexicoyelmundo.com/mundo.js](https://web.archive.org/web/20110202190932/http://feedsdemexicoyelmundo.com/mundo.js)

<a id="_6608"></a>
First we have to know that the [Wayback Machine](wayback-machine.md) adds some stuff before and after the original code. The actual code there starts at:<a id="_6609"></a>

```
ap={fg:['MSXML2.XMLHTTP
```
and ends in:<a id="_6610"></a>

```
ck++;};return fu;};
```

<a id="_6611"></a>
We can use a [JavaScript](../javascript.md) beautifier such as [https://beautifier.io/](https://beautifier.io/) to be abe to better read the code.

<a id="_6612"></a>
It is worth noting that there's a lot of `<script>` tags inline as well, which seem to matter.

<a id="_6613"></a>
Further analysis would be needed.

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
