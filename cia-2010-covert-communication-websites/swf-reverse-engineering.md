# SWF reverse engineering

↑ **Parent:** [Communication mechanism](communication-mechanism.md)

Codex did some SWF reverse engineering for us creating the analysis script: [jar.py](https://github.com/cirosantilli/media/blob/master/cia-2010-covert-communication-websites/jar.py) and should be pointed to a dump directory of the websites such as [CIA 2010 websites dump](cia-2010-websites-dump.md). The analysis below was done as of commit b9eb31618c36421133e4875bc1cd7d7ac7763a32.

Unfortunately, the SWF are much less interesting than the JAR files.

According to Codex' analysis, it is just a lean client, and doesn't even contain its own UI which seems to be downloaded from the server. As such, we will never know what it actually looked like.

One thing that they do do is to load a gallery or things that it loops through, presumably images, and loop through them automatically. These are loaded one by one from the server, and it keeps doing server requests after that.

Codex mentions that the SWF could also download another SWF to execute, which could in turn contain the login UI, possibly upon click. But it is all hidden.

A particularly interesting example is [worlddispatch.net/servlet/news2](https://web.archive.org/web/20130625064723id_/http://worlddispatch.net/servlet/news2). This is apparently a helper page for the SWF, but perhaps because the website became broken after it was abandoned, it was archived, and contains the following 10 bytes of a URL query string:
```
c=0&f=3424
```
Codex' reverse engineering identified what the parameters do exactly:
- `c=0`: Selects the ordinary content-cycling mode. `c=1` selects a different scrolling/animated branch.
- `f=3424`: advance to the next content item every 3.424 seconds, when content is available. The code's default is 4 seconds.

## ↑ Ancestors (15)

1. [Communication mechanism](communication-mechanism.md)
2. [Reverse engineering](reverse-engineering.md)
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
