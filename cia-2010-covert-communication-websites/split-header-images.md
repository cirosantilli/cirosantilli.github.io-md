# Split header images

↑ **Parent:** [Fingerprints](fingerprints.md)

Many of the website banners are composed of several images cut up.

Often stock images were first assembled into the banner, and then the resulting image was cut.

Possibly this was done to make reverse image search to their stock image provider harder.

But it somewhat backfired and serves as a good marker that confirms authorship.

Maybe it is some kind of outdated web design thing, which they took much further in time than the average website, like the JAR.

Their websites do appear to follow common style guidelines form earlier eras, around the early 2000s notably, some legit sites that look a lot like hits:

An example:
- [http://classicalmusicboxonline.com/images/banner_01.jpg](http://classicalmusicboxonline.com/images/banner_01.jpg)
- [http://classicalmusicboxonline.com/images/banner_02.jpg](http://classicalmusicboxonline.com/images/banner_02.jpg)
- ...
- [http://classicalmusicboxonline.com/images/banner_19.jpg](http://classicalmusicboxonline.com/images/banner_19.jpg)
- [http://classicalmusicboxonline.com/images/banner_20.jpg](http://classicalmusicboxonline.com/images/banner_20.jpg)

- [https://web.archive.org/web/20031002010827/http://www.ausiranstudy.com/](https://web.archive.org/web/20031002010827/http://www.ausiranstudy.com/)

Looking at the source code of: [https://web.archive.org/web/20130828122833/http://euronewsonline.net/euro_bus.php](https://web.archive.org/web/20130828122833/http://euronewsonline.net/euro_bus.php) we noticed an interesting comment:
```
<!-- ImageReady Slices (enewsweather.psd) -->
```
which presumably refers to Adobe ImageReady:

> Adobe ImageReady was a bitmap graphics editor that was shipped with Adobe Photoshop for six years. It was available for Windows, Classic Mac OS and Mac OS X from 1998 to 2007. ImageReady was designed for web development and closely interacted with Photoshop

A sample tutorial: [https://people.goshen.edu/~paulmr/physix/326/imageready/slicendice.php](https://people.goshen.edu/~paulmr/physix/326/imageready/slicendice.php)

Some of the websites use CSS background images to populate the images, e.g. [ingenuitytrendz.com](https://web.archive.org/web/20110201170354/http://ingenuitytrendz.com/) has HTML:
```
ingenuitytrendz.com/20110201170354/index.html:                  <li><a id="banner1">&nbsp;</a></li>
ingenuitytrendz.com/20110201170354/index.html:                  <li><a id="banner2">&nbsp;</a></li>
ingenuitytrendz.com/20110201170354/index.html:                  <li><a id="banner3">&nbsp;</a></li>
```
and then the CSS [engineering.css](https://web.archive.org/web/20110201170405cs_/http://ingenuitytrendz.com/engineering.css) does:
```
#banner1 { background: url(/web/20110201170405im_/http://ingenuitytrendz.com/images/banner_01.jpg) no-repeat center; }
#banner2 { background: url(/web/20110201170405im_/http://ingenuitytrendz.com/images/banner_02.jpg) no-repeat center; }
#banner3 { background: url(/web/20110201170405im_/http://ingenuitytrendz.com/images/banner_03.jpg) no-repeat center; }
```

## ↑ Ancestors (14)

1. [Fingerprints](fingerprints.md)
2. [Methodology](methodology.md)
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

## ← Incoming links (3)

- [Fingerprints](fingerprints.md)
- [List of websites](list-of-websites.md)
- [Backing up CIA website archives for research and posterity](../updates/backing-up-cia-website-archives-for-research-and-posterity.md)
