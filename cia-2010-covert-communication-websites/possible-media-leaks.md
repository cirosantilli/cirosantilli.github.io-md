# Possible media leaks

↑ **Parent:** [Possible HTML information leaks](possible-html-information-leaks.md)

[GPT-6](../gpt-6.md) noticed the following not so mind-blowing facts about some media present in some of the websites

33 images on [stickshiftnews.com](https://web.archive.org/web/20110207232048/http://stickshiftnews.com/) record Photoshop saves on 2010-08-24, 14:16:41–14:17:50 at UTC-4 ([Langley](../langley.md)): a 69-second batch. This supports batch asset preparation possibly from ImageReady, and also gives us the exact Photoshop version used and operating system: Adobe Photoshop CS4 (released 2008). They used [Windows](../microsoft-windows.md). That's the real reason the network went down!
```
exiftool -r -q -if '$HistoryWhen' -p '$HistoryWhen | $HistoryAction | $HistorySoftwareAgent | $Directory/$FileName' stickshiftnews.com | sort
```
gives:
```
2010:08:24 14:16:41-04:00 | created | Adobe Photoshop CS4 Windows | stickshiftnews.com/20110207233507/images/199.jpg
2010:08:24 14:16:44-04:00 | saved | Adobe Photoshop CS4 Windows | stickshiftnews.com/20110207232515/images/2.jpg
...
2010:08:24 14:17:50-04:00 | created | Adobe Photoshop CS4 Windows | stickshiftnews.com/20110207232233/images/9.jpg
```

Four graphics across ballbatstumpsandbails.com and myhealthlibrary.net share `uuid:B48CC374F6E2DC1193D6E593F704EF94`:
```
exiftool -r -q -if '$OriginalDocumentID eq "uuid:B48CC374F6E2DC1193D6E593F704EF94"' -p '$Directory/$FileName | $OriginalDocumentID' ballbatstumpsandbails.com www.myhealthlibrary.net
```
gives:
```
ballbatstumpsandbails.com/20110202033048/images/bbsb-logo.jpg | uuid:B48CC374F6E2DC1193D6E593F704EF94
ballbatstumpsandbails.com/20110202033025/images/cornerimg.jpg | uuid:B48CC374F6E2DC1193D6E593F704EF94
www.myhealthlibrary.net/20111015023625/images/back.gif | uuid:B48CC374F6E2DC1193D6E593F704EF94
www.myhealthlibrary.net/20111015023519/images/top.jpg | uuid:B48CC374F6E2DC1193D6E593F704EF94
```
However that same UUID also appears on a few unrealted Google hits e.g.:
- [https://commons.wikimedia.org/wiki/File:Fortune_Brands_Home_%26_Security_Logo.png](https://commons.wikimedia.org/wiki/File:Fortune_Brands_Home_%26_Security_Logo.png)
so it cannot reliably establish a connection between their operators. TODO how did that come about. LLMs say that this UUID comes from PhotoShop and depends on the exact version, but they are not fully clear on the details of how they come about.

## ↑ Ancestors (14)

1. [Possible HTML information leaks](possible-html-information-leaks.md)
2. [Results](results.md)
3. [CIA 2010 covert communication websites](../cia-2010-covert-communication-websites-split.md)
4. [Central Intelligence Agency](../central-intelligence-agency.md)
5. [American intelligence agency](../american-intelligence-agency.md)
6. [United States Intelligence Community](../united-states-intelligence-community.md)
7. [Intelligence community](../intelligence-community.md)
8. [Secret service](../secret-service.md)
9. [Espionage](../espionage.md)
10. [War](../war.md)
11. [Social science](../social-science.md)
12. [Scientific method](../scientific-method.md)
13. [Science](../science-split.md)
14. [Ciro Santilli's Homepage](../split.md)
