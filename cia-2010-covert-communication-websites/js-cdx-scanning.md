# JS CDX scanning

↑ **Parent:** [Wayback Machine CDX scanning](wayback-machine-cdx-scanning.md)

<a id="_6007"></a>
JAR, SWF and CGI-bin scanning by path only is fine, since there are relatively few of those. But .js scanning by path only is too broad.

<a id="_6008"></a>
One option would be to filter out by size, an information that is contained on the CDX. Let's check typical ones:<a id="_6009"></a>

```
grep -f <(jq -r '.[]|select(select(.comms)|.comms|test("\\.js"))|.host' ../media/cia-2010-covert-communication-websites/hits.json) out | out.jshits.cdx
sort -n -k7 out.jshits.cdx
```
Ignoring some obvious unrelated non-comms files visually we get a range of about 2732 to 3632:<a id="_6010"></a>

```
net,hollywoodscreen)/current.js 20110106082232 http://hollywoodscreen.net/current.js text/javascript 200 XY5NHVW7UMFS3WSKPXLOQ5DJA34POXMV 2732
com,amishkanews)/amishkanewss.js 20110208032713 http://amishkanews.com/amishkanewss.js text/javascript 200 S5ZWJ53JFSLUSJVXBBA3NBJXNYLNCI4E 3632
```
This ignores the obviously atypical [JavaScript with SHAs](javascript-with-shas.md) from iranfootballsource, and the particularly small old menu.js from cutabovenews.com, which we embed into [cia-2010-covert-communication-websites/cdx-post-js.sh](cia-2010-covert-communication-websites/cdx-post-js.sh).

<a id="_6011"></a>
The size helps a bit, but it's not insanely good unfortunately, only about 3x, these are some common JS sizes right there!

## ↑ Ancestors (16)

1. [Wayback Machine CDX scanning](wayback-machine-cdx-scanning.md)
2. [Wayback Machine](wayback-machine.md)
3. [Data sources](data-sources.md)
4. [Methodology](methodology.md)
5. [CIA 2010 covert communication websites](../cia-2010-covert-communication-websites-split.md)
6. [Central Intelligence Agency](../central-intelligence-agency.md)
7. [American intelligence agency](../american-intelligence-agency.md)
8. [United States Intelligence Community](../united-states-intelligence-community.md)
9. [Intelligence community](../intelligence-community.md)
10. [Secret service](../secret-service.md)
11. [Espionage](../espionage.md)
12. [War](../war.md)
13. [Social science](../social-science.md)
14. [Scientific method](../scientific-method.md)
15. [Science](../science-split.md)
16. [Ciro Santilli's Homepage](../split.md)
