# Aratu Week 2024 Talk by Ciro Santilli: My Best Random Projects

↑ **Parent:** [Talk by Ciro Santilli](ciro-santilli.md#talk-by-ciro-santilli)  
🏷️ **Tags:** [Aratu Week](computer.md#aratu-week)

<a id="_2"></a>
This talk was presented on 24 September 2024 as part of the 2024 [Aratu Week](computer.md#aratu-week), a small online conference by [Brazilian](brazil.md) hacker interest group [Boitatech](computer.md#boitatech).

<a id="_3"></a>
How to contact me: [Section "How to contact Ciro Santilli"](ciro-santilli.md#contact)

<a id="_4"></a>
Links to this talk:<a id="_5"></a>

<a id="_6"></a>
- [https://cirosantilli.com/aratu-week-2024-talk-by-ciro-santilli](https://cirosantilli.com/aratu-week-2024-talk-by-ciro-santilli)
<a id="_7"></a>
- [https://ourbigbook.com/cirosantilli/aratu-week-2024-talk-by-ciro-santilli](https://ourbigbook.com/cirosantilli/aratu-week-2024-talk-by-ciro-santilli)

<a id="_8"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/CIA_Star_Wars_website_promo.jpg" alt="" height="850">

**[Figure 1](#_8)** [Source](https://web.archive.org/web/20101230033220/http://starwarsweb.net/).

<a id="video-self-recorded-presentation-vod"></a>
**[Video 1](#video-self-recorded-presentation-vod). Self-recorded presentation VOD.** [Source](https://www.youtube.com/watch?v=6YpO2UfU6to).

<a id="video-presentation-upload-by-the-organizers"></a>
**[Video 2](#video-presentation-upload-by-the-organizers). Presentation upload by the organizers.** [Source](https://youtu.be/Z7ZAzPKjzYc?t=1505).

**Table of contents**

- [Introduction](#introduction)
  - [Creative Commons CC By-SA](#creative-commons-cc-by-sa)
  - [I'm not a professional hacker, I did some very occasional OSINT just for fun](#i-m-not-a-professional-hacker-i-did-some-very-occasional-osint-just-for-fun)
- [CIA 2010 covert communication websites](#cia-2010-covert-communication-websites)
  - [Prelude: initial reports without specific websites (2018-)](#prelude-initial-reports-without-specific-websites-2018)
  - [Starting point: 2022 Reuters article](#starting-point-2022-reuters-article)
  - [Coolest findings](#coolest-findings)
    - [The Star Wars website](#the-star-wars-website)
    - [Examples of USA spying on its "allies"](#examples-of-usa-spying-on-its-allies)
      - [Brazil](#brazil)
      - [Germany](#germany)
      - [France](#france)
      - [Italy](#italy)
  - [Methodology](#methodology)
    - [The easy: IP range searches](#the-easy-ip-range-searches)
    - [The hard: finding new IP ranges!](#the-hard-finding-new-ip-ranges)
      - [2013 DNS census data](#2013-dns-census-data)
      - [Wayback Machine searches for the communication method paths: Tor army parallelization!](#wayback-machine-searches-for-the-communication-method-paths-tor-army-parallelization)
      - [Cheeky fuzzy fingerprint: the domain name contains `news`](#cheeky-fuzzy-fingerprint-the-domain-name-contains-news)
      - [Chinese expired domain trackers: another valuable domain data dump](#chinese-expired-domain-trackers-another-valuable-domain-data-dump)
        - [I scraped them and uploaded to GitHub repos, 2011 - 2022, 20-30 M entries / year](#i-scraped-them-and-uploaded-to-github-repos-2011-2022-20-30-m-entries-year)
  - [Help wanted! Some sites were almost certainly missed. Contributions will be acknowledged.](#help-wanted-some-sites-were-almost-certainly-missed-contributions-will-be-acknowledged)
- [Linux Kernel Module Cheat](#linux-kernel-module-cheat)
  - [Get a Linux terminal on QEMU](#get-a-linux-terminal-on-qemu)
  - [**Everything** is built from source and easily modifiable, powered by Buildroot](#everything-is-built-from-source-and-easily-modifiable-powered-by-buildroot)
  - [Kernel GDB step debugging just works](#kernel-gdb-step-debugging-just-works)
  - [Multiple architectures supported](#multiple-architectures-supported)
  - [Lots of in-tree examples](#lots-of-in-tree-examples)
    - [Kernel modules](#kernel-modules)
    - [Assembly](#assembly)
    - [Bare metal!](#bare-metal)
- [OurBigBook.com](#ourbigbook-com)
  - [An anonymous donor gave me 1000 Monero (~126,000 USD) on March 2024 to work on this for one year](#an-anonymous-donor-gave-me-1000-monero-126-000-usd-on-march-2024-to-work-on-this-for-one-year)
  - [Motivation: university sucks real bad right now](#motivation-university-sucks-real-bad-right-now)
  - [What you get](#what-you-get)
    - [One mega article tree for each user](#one-mega-article-tree-for-each-user)
    - [Infinitely deep table of contents](#infinitely-deep-table-of-contents)
  - [Topics: the best version of an article by other users (the killer feature)](#topics-the-best-version-of-an-article-by-other-users-the-killer-feature)
  - [Edit and publish](#edit-and-publish)
    - [Internal cross file references done right](#internal-cross-file-references-done-right)
    - [Web editor with side by side preview](#web-editor-with-side-by-side-preview)
    - [Publish from local markup files](#publish-from-local-markup-files)
  - [OurBigBook.com vs X](#ourbigbook-com-vs-x)
- [Ciro's Bitcoin Inscription Museum](#ciro-s-bitcoin-inscription-museum)
  - [How illegal does something in the Bitcoin blockchain have to be to make it illegal?](#how-illegal-does-something-in-the-bitcoin-blockchain-have-to-be-to-make-it-illegal)
    - [Pedobear memes?](#pedobear-memes)
    - [Nuclear weapon designs?](#nuclear-weapon-designs)
    - [Political memes?](#political-memes)
  - [Ordinal ruleset inscription (2022): the end of the line: Eternal September arrives](#ordinal-ruleset-inscription-2022-the-end-of-the-line-eternal-september-arrives)
  - [My obsession: find **every** image before ordinals](#my-obsession-find-every-image-before-ordinals)
    - [Fan tributes](#fan-tributes)
    - [Social media](#social-media)
    - [Art](#art)
    - [Memes](#memes)
    - [Love declaration](#love-declaration)
    - [Promotional material](#promotional-material)
- [China Dictatorship](#china-dictatorship)
  - [Xi Jinping, ruler of China](#xi-jinping-ruler-of-china)
  - [Xi Jinping, sadomasochist in leather suit](#xi-jinping-sadomasochist-in-leather-suit)
  - [Collateral freedom: **HTTPS**: the censor doesn't know which path you access](#collateral-freedom-https-the-censor-doesn-t-know-which-path-you-access)
  - [The GitHub issue tracker is quite cute, because Chinese people actually use GitHub search in addition to search engines](#the-github-issue-tracker-is-quite-cute-because-chinese-people-actually-use-github-search-in-addition-to-search-engines)
  - [Stack Overflow attacks](#stack-overflow-attacks)
  - [Package managers](#package-managers)
    - [PyPi: the cowards took it down](#pypi-the-cowards-took-it-down)
- [All GitHub commit emails](#all-github-commit-emails)
- [Other projects](#other-projects)

## Introduction

↑ **Parent:** [Aratu Week 2024 Talk by Ciro Santilli: My Best Random Projects](aratu-week-2024-talk-by-ciro-santilli.md)

### Creative Commons CC By-SA

↑ **Parent:** [Introduction](#introduction)

<a id="_9"></a>
![](https://upload.wikimedia.org/wikipedia/commons/thumb/5/57/CC-BY-SA_icon_white.svg/960px-CC-BY-SA_icon_white.svg.png)

**[Figure 2](#_9)** [Source](https://commons.wikimedia.org/wiki/File:CC-BY-SA_icon_white.svg.png).

<h3 id="i-m-not-a-professional-hacker-i-did-some-very-occasional-osint-just-for-fun">I'm not a professional hacker, I did some very occasional OSINT just for fun</h3>

↑ **Parent:** [Introduction](#introduction)

<a id="_10"></a>
[Section "How to contact Ciro Santilli"](ciro-santilli.md#contact)

<a id="_11"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/ID_photo_of_Ciro_Santilli_2024_intro_to_ourbigbook.jpg" alt="" height="600">

<a id="_12"></a>
<img src="https://stackoverflow.com/users/flair/895245.png?theme=dark" alt="" height="300">

## CIA 2010 covert communication websites

↑ **Parent:** [Aratu Week 2024 Talk by Ciro Santilli: My Best Random Projects](aratu-week-2024-talk-by-ciro-santilli.md)

<a id="video-how-i-found-a-star-wars-website-made-by-the-cia"></a>
**[Video 3](#video-how-i-found-a-star-wars-website-made-by-the-cia). How I found a Star Wars website made by the CIA.** [Source](https://www.youtube.com/watch?v=TFfuzZC5Qpc).

<a id="_14"></a>
Article: [Section "CIA 2010 covert communication websites"](#cia-2010-covert-communication-websites)

<a id="_15"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/CIA_Star_Wars_website_promo.jpg" alt="" height="850">

**[Figure 3](#_15)** [Source](https://web.archive.org/web/20101230033220/http://starwarsweb.net/).

<a id="image-boitatech-logo"></a>
<img src="https://web.archive.org/web/20240909135836im_/http://boitatech.com/assets/img/logo.svg" alt="" height="600">

**[Figure 4](#image-boitatech-logo). Boitatech logo**. [Source](https://boitatech.com).

<a id="_16"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/CIA_websites_hacker_news.png" alt="" height="600">

**[Figure 5](#_16)** [Source](https://news.ycombinator.com/item?id=36279375).

<h3 id="prelude-initial-reports-without-specific-websites-2018">Prelude: initial reports without specific websites (2018-)</h3>

↑ **Parent:** [CIA 2010 covert communication websites](#cia-2010-covert-communication-websites)

<a id="_17"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/Yahoo_CIA_website_article.png" alt="" height="900">

<a id="image-seriously-a-dumb-question-quora-answer-by-chris-from-the-us-navy"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/CIA_2010_site_Quora_question_and_Chris_answer.png" alt="" height="600">

**[Figure 6](#image-seriously-a-dumb-question-quora-answer-by-chris-from-the-us-navy). "Seriously a dumb question" Quora answer by Chris from the US Navy**.

### Starting point: 2022 Reuters article

↑ **Parent:** [CIA 2010 covert communication websites](#cia-2010-covert-communication-websites)

<a id="video-compromised-comms-by-darknet-diaries-2023"></a>
**[Video 4](#video-compromised-comms-by-darknet-diaries-2023). Compromised Comms by Darknet Diaries (2023)** [Source](https://www.youtube.com/watch?v=uh_q02eefFM).

<a id="image-banner-of-the-reuters-article"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/Reuters_CIA_website_article_banner.jpg" alt="" height="800">

**[Figure 7](#image-banner-of-the-reuters-article). Banner of the Reuters article**. [Source](https://www.reuters.com/investigates/special-report/usa-spies-iran/).

<a id="image-reuters-reconstruction-of-what-the-applet-would-have-looked-like"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/www.reuters.com_investigates_special-report_usa-spies-iran_applet_reconstruction.jpg" alt="" height="850">

**[Figure 8](#image-reuters-reconstruction-of-what-the-applet-would-have-looked-like). Reuters reconstruction of what the applet would have looked like**. [Source](https://www.reuters.com/investigates/special-report/usa-spies-iran/).

<a id="image-inspecting-the-reuters-article-html-source-code"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/Reuters_CIA_website_article_image_urls_arrow.jpg" alt="" height="800">

**[Figure 9](#image-inspecting-the-reuters-article-html-source-code). Inspecting the Reuters article HTML source code**.

### Coolest findings

↑ **Parent:** [CIA 2010 covert communication websites](#cia-2010-covert-communication-websites)

#### The Star Wars website

↑ **Parent:** [Coolest findings](#coolest-findings)

<a id="image-2010-wayback-machine-archive-of-starwarsweb-net"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/cia-2010-covert-communication-websites/screenshots/starwarsweb.net.jpg" alt="" height="1400">

**[Figure 10](#image-2010-wayback-machine-archive-of-starwarsweb-net). 2010 Wayback Machine archive of starwarsweb.net**. The [Star Wars](film.md#star-wars) one.

#### Examples of USA spying on its "allies"

↑ **Parent:** [Coolest findings](#coolest-findings)

##### Brazil

↑ **Parent:** [Examples of USA spying on its "allies"](#examples-of-usa-spying-on-its-allies)

<a id="image-2010-wayback-machine-archive-of-noticiasmusica-net"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/cia-2010-covert-communication-websites/screenshots/noticiasmusica.net.jpg" alt="" height="1400">

**[Figure 11](#image-2010-wayback-machine-archive-of-noticiasmusica-net). 2010 Wayback Machine archive of noticiasmusica.net**. The [Brazilian](brazil.md) one.

##### Germany

↑ **Parent:** [Examples of USA spying on its "allies"](#examples-of-usa-spying-on-its-allies)

<a id="image-2010-wayback-machine-archive-of-dedrickonline-com"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/cia-2010-covert-communication-websites/screenshots/www.dedrickonline.com.jpg" alt="" height="1600">

**[Figure 12](#image-2010-wayback-machine-archive-of-dedrickonline-com). 2010 Wayback Machine archive of dedrickonline.com**. The [German](continent.md#germany) one.

##### France

↑ **Parent:** [Examples of USA spying on its "allies"](#examples-of-usa-spying-on-its-allies)

<a id="image-2010-wayback-machine-archive-of-lesummumdelafinance-com"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/cia-2010-covert-communication-websites/screenshots/lesummumdelafinance.com.jpg" alt="" height="1400">

**[Figure 13](#image-2010-wayback-machine-archive-of-lesummumdelafinance-com). 2010 Wayback Machine archive of lesummumdelafinance.com**. A [French](continent.md#france) one.

##### Italy

↑ **Parent:** [Examples of USA spying on its "allies"](#examples-of-usa-spying-on-its-allies)

<a id="image-2011-wayback-machine-archive-of-attivitaestremi-com"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/cia-2010-covert-communication-websites/screenshots/attivitaestremi.com.jpg" alt="" height="1400">

**[Figure 14](#image-2011-wayback-machine-archive-of-attivitaestremi-com). 2011 Wayback Machine archive of attivitaestremi.com**. An [Italian](continent.md#italy) one about extreme sports.

### Methodology

↑ **Parent:** [CIA 2010 covert communication websites](#cia-2010-covert-communication-websites)

#### The easy: IP range searches

↑ **Parent:** [Methodology](#methodology)

<a id="image-viewdns-info-activegameinfo-com-domain-to-ip"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/viewdns.info_activegameinfo.com_domain_to_IP_arrow.png" alt="" height="550">

**[Figure 15](#image-viewdns-info-activegameinfo-com-domain-to-ip). viewdns.info `activegameinfo.com` domain to IP**. [Source](https://viewdns.info/iphistory/?domain=activegaminginfo.com).

<a id="image-viewdns-info-aroundthemiddleeast-com-ip-to-domain"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/viewdns.info_aroundthemiddleeast.com_IP_to_domain_arrow.png" alt="" height="550">

**[Figure 16](#image-viewdns-info-aroundthemiddleeast-com-ip-to-domain). viewdns.info `aroundthemiddleeast.com` IP to domain**. [Source](https://viewdns.info/reverseip/?host=66.175.106.140&t=1).

#### The hard: finding new IP ranges!

↑ **Parent:** [Methodology](#methodology)

##### 2013 DNS census data

↑ **Parent:** [The hard: finding new IP ranges!](#the-hard-finding-new-ip-ranges)

<a id="_19"></a>
[https://dnscensus2013.neocities.org/](https://dnscensus2013.neocities.org/)

<a id="image-dns-census-2013-website"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/dnscensus2013.neocities.org.png" alt="" height="574">

**[Figure 17](#image-dns-census-2013-website). DNS Census 2013 website**. [Source](https://dnscensus2013.neocities.org/). This source provided valuable historical domain to IP data.

<a id="_20"></a>
```
amazon.com,2012-02-01T21:33:36,72.21.194.1
amazon.com,2012-02-01T21:33:36,72.21.211.176
amazon.com,2013-10-02T19:03:39,72.21.194.212
amazon.com,2013-10-02T19:03:39,72.21.215.232
amazon.com.au,2012-02-10T08:03:38,207.171.166.22
amazon.com.au,2012-02-10T08:03:38,72.21.206.80
google.com,2012-01-28T05:33:40,74.125.159.103
google.com,2012-01-28T05:33:40,74.125.159.104
google.com,2013-10-02T19:02:35,74.125.239.41
google.com,2013-10-02T19:02:35,74.125.239.46
```

<a id="_21"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/ciro-love-sqlite.png" alt="" height="309">

##### Wayback Machine searches for the communication method paths: Tor army parallelization!

↑ **Parent:** [The hard: finding new IP ranges!](#the-hard-finding-new-ip-ranges)

<a id="_22"></a>
[https://web.archive.org/cdx/search/cdx?url=capture-nature.com&matchType=domain](https://web.archive.org/cdx/search/cdx?url=capture-nature.com&matchType=domain)

<a id="_23"></a>
```
com,capture-nature)/robots.txt 20211229130524 https://www.capture-nature.com/robots.txt warc/revisit - XWX2XVEZVSVIUKYXF3AJUYIRDOLOXLTO 1213
com,capture-nature)/robots.txt 20211230151913 http://capture-nature.com/robots.txt warc/revisit - XWX2XVEZVSVIUKYXF3AJUYIRDOLOXLTO 1186
com,capture-nature)/robots.txt 20220419233721 https://www.capture-nature.com/robots.txt warc/revisit - XWX2XVEZVSVIUKYXF3AJUYIRDOLOXLTO 1075
com,capture-nature)/scenes.jar 20110201104851 http://capture-nature.com/Scenes.jar application/java-archive 200 U3GPB3SPISZKLFGUJFD34C5GXWAAC2GJ 287887
com,capture-nature)/scenes.jar 20110224193204 http://capture-nature.com/Scenes.jar application/java-archive 200 U3GPB3SPISZKLFGUJFD34C5GXWAAC2GJ 287890
com,capture-nature)/scenes.jar 20130903003254 http://capture-nature.com/Scenes.jar application/x-java-archive 200 U3GPB3SPISZKLFGUJFD34C5GXWAAC2GJ 287898
com,capture-nature)/trees-and-details 20200928184446 https://www.capture-nature.com/trees-and-details text/html 200 NO6J7567VFWZLRSKBJ5HVXGT27MX2A4K 30902
com,capture-nature)/trees-and-details 20210127132910 https://www.capture-nature.com/trees-and-details text/html 200 SI73WNJUBGTOXSTRK4IRU4D4AJ637F6A 31041
com,capture-nature)/trees-and-details 20210419062751 https://www.capture-nature.com/trees-and-details text/html 200 K4Q444QJ243HW3ECXNNOBNUFMXWAPVFD 31464
```

<a id="_24"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/cia-website-comms-methods.png" alt="" height="800">

<a id="_25"></a>
Tor automation at: [https://github.com/cirosantilli/cirosantilli.github.io/blob/f45d859d4f9350e4a3deffdbb8acd86584d60f2c/cia-2010-covert-communication-websites/cdx-tor.sh](https://github.com/cirosantilli/cirosantilli.github.io/blob/f45d859d4f9350e4a3deffdbb8acd86584d60f2c/cia-2010-covert-communication-websites/cdx-tor.sh)

##### Cheeky fuzzy fingerprint: the domain name contains `news`

↑ **Parent:** [The hard: finding new IP ranges!](#the-hard-finding-new-ip-ranges)

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

##### Chinese expired domain trackers: another valuable domain data dump

↑ **Parent:** [The hard: finding new IP ranges!](#the-hard-finding-new-ip-ranges)

<a id="_30"></a>
[http://static.hupo.com/expdomain_myadmin/2012-03-06（国际域名）.txt](http://static.hupo.com/expdomain_myadmin/2012-03-06（国际域名）.txt)

<a id="_31"></a>
```
0000o.com
001cssf.com
001techan.com
0061hs-0351xc-g305h.net
006979.com
006h4g-054hs-6504ga.net
```

<h6 id="i-scraped-them-and-uploaded-to-github-repos-2011-2022-20-30-m-entries-year">I scraped them and uploaded to GitHub repos, 2011 - 2022, 20-30 M entries / year</h6>

↑ **Parent:** [Chinese expired domain trackers: another valuable domain data dump](#chinese-expired-domain-trackers-another-valuable-domain-data-dump)

<a id="_32"></a>
[https://github.com/cirosantilli/expired-domain-names-by-day-2011](https://github.com/cirosantilli/expired-domain-names-by-day-2011)

<a id="_33"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/github.com_cirosantilli_expired-domain-names-by-day-2011.png" alt="" height="850">

**[Figure 18](#_33)** [Source](https://github.com/cirosantilli/expired-domain-names-by-day-2011).

### Help wanted! Some sites were almost certainly missed. Contributions will be acknowledged.

↑ **Parent:** [CIA 2010 covert communication websites](#cia-2010-covert-communication-websites)

<a id="_34"></a>
<img src="https://web.archive.org/web/20240703222455im_/https://upload.wikimedia.org/wikipedia/commons/thumb/0/01/30a_Sammlung_Eybl_Gro%C3%9Fbritannien._Alfred_Leete_(1882%E2%80%931933)_Britons_(Kitchener)_wants_you_(Briten_Kitchener_braucht_Euch)._1914_(Nachdruck)%2C_74_x_50_cm._(Slg.Nr._552).jpg/401px-thumbnail.jpg" alt="" height="800">

## Linux Kernel Module Cheat

↑ **Parent:** [Aratu Week 2024 Talk by Ciro Santilli: My Best Random Projects](aratu-week-2024-talk-by-ciro-santilli.md)

<a id="_36"></a>
[https://github.com/cirosantilli/linux-kernel-module-cheat](https://github.com/cirosantilli/linux-kernel-module-cheat)

<a id="_37"></a>
<img src="https://upload.wikimedia.org/wikipedia/commons/3/35/Tux.svg" alt="" height="600">

**[Figure 19](#_37)** [Source](https://commons.wikimedia.org/wiki/File:Tux.svg).

### Get a Linux terminal on QEMU

↑ **Parent:** [Linux Kernel Module Cheat](#linux-kernel-module-cheat)

<a id="_38"></a>
![](https://upload.wikimedia.org/wikipedia/commons/4/45/Qemu_logo.svg)

**[Figure 20](#_38)** [Source](https://commons.wikimedia.org/wiki/File:Qemu_logo.svg).

<a id="_39"></a>
One time setup:<a id="_40"></a>

```
git clone https://github.com/cirosantilli/linux-kernel-module-cheat
cd linux-kernel-module-cheat
sudo apt install docker
python3 -m venv .venv
. .venv/bin/activate
./setup
./run-docker create
./run-docker sh
```

<a id="_41"></a>
You are now in Docker.

<a id="_42"></a>
Build everything from source inside docker:<a id="_43"></a>

```
./build --download-dependencies qemu-buildroot
```

<a id="_44"></a>
Boot Linux and get a userland shell:<a id="_45"></a>

```
./run
```

<a id="_46"></a>
Outcome:<a id="_47"></a>

```
<6>[    1.383114] NET: Registered protocol family 17
<6>[    1.383682] 9pnet: Installing 9P2000 support
<6>[    1.385473] IPI shorthand broadcast: enabled
<6>[    1.385701] sched_clock: Marking stable (1355697980, 27047205)->(1385555667, -2810482)
<6>[    1.387744] ALSA device list:
<6>[    1.387843]   No soundcards found.
<6>[    1.535981] ata2.00: ATAPI: QEMU DVD-ROM, 2.5+, max UDMA/100
<5>[    1.543470] scsi 1:0:0:0: CD-ROM            QEMU     QEMU DVD-ROM     2.5+ PQ: 0 ANSI: 5
<6>[    1.548952] EXT4-fs (vda): mounting ext2 file system using the ext4 subsystem
<6>[    1.555909] EXT4-fs (vda): mounted filesystem without journal. Opts: (null)
<6>[    1.556145] VFS: Mounted root (ext2 filesystem) on device 254:0.
<6>[    1.557451] devtmpfs: mounted
<6>[    1.605639] Freeing unused kernel image (initmem) memory: 1248K
<6>[    1.605875] Write protecting the kernel read-only data: 16384k
<6>[    1.607977] Freeing unused kernel image (text/rodata gap) memory: 2044K
<6>[    1.610190] Freeing unused kernel image (rodata/data gap) memory: 1012K
<6>[    1.610495] Run /sbin/init as init process
<6>[    1.683311] tsc: Refined TSC clocksource calibration: 3293.671 MHz
<6>[    1.683618] clocksource: tsc: mask: 0xffffffffffffffff max_cycles: 0x2f79f177aae, max_idle_ns: 440795226653 ns
<6>[    1.683849] clocksource: Switched to clocksource tsc
<3>[    1.694241] 9pnet_virtio: no channels available for device host_data
mount: mounting host_data on /mnt/9p/data failed: No such file or directory
qemu-system-x86_64: warning: 9p: degraded performance: a reasonable high msize should be chosen on client/guest side (chosen msize is <= 8192). See https://wiki.qemu.org/Documentation/9pset.
<3>[    1.712287] overlayfs: overlapping upperdir path
mount: mounting overlay on /mnt/overlay failed: Too many levels of symbolic links
hello S98
hello .profile
/lkmc
root@buildroot# pwd
/lkmc
/lkmc
root@buildroot#
```

### **Everything** is built from source and easily modifiable, powered by Buildroot

↑ **Parent:** [Linux Kernel Module Cheat](#linux-kernel-module-cheat)

<a id="_48"></a>
![](https://web.archive.org/web/20240424065053im_/https://bootlin.com/wp-content/uploads/2015/05/logo-buildroot.png)

<a id="_49"></a>
The following are [stored in submodules](https://github.com/cirosantilli/linux-kernel-module-cheat/blob/master/submodules):<a id="_50"></a>

```
submodules/binutils-gdb/
submodules/buildroot/
submodules/gcc/
submodules/glibc/
submodules/linux/
submodules/qemu/
```

<a id="_51"></a>
So you can modify source, rebuild and that's it, its in the VM.

<a id="_52"></a>
E.g., let's hack the linux kernel:

<a id="_53"></a>
```
asmlinkage __visible void __init __no_sanitize_address start_kernel(void)
{
  pr_info("I'VE HACKED THE LINUX KERNEL!!!");
```

<a id="_54"></a>
Rebuild Linux:

<a id="_55"></a>
```
./build-linux
```

<a id="_56"></a>
Rerun:

<a id="_57"></a>
```
./run
```

<a id="_58"></a>
And after boot we see:

<a id="_59"></a>
```
<6>[    0.000000] I'VE HACKED THE LINUX KERNEL!!!
```

### Kernel GDB step debugging just works

↑ **Parent:** [Linux Kernel Module Cheat](#linux-kernel-module-cheat)

<a id="_60"></a>
Start QEMU and wait for GDB:<a id="_61"></a>

```
./run --gdb-wait
```

<a id="_62"></a>
On another shell, connect GDB to QEMU and run up to a symbol that shows up at boot:<a id="_63"></a>

```
./run-gdb start_kernel
```

<a id="_64"></a>
Outcome: we are GDB step debugging the Linux Kernel:<a id="_65"></a>

```
Breakpoint 1, start_kernel () at /root/lkmc/submodules/linux/init/main.c:837
837     {
loading vmlinux
(gdb) n
841             set_task_stack_end_magic(&init_task);
(gdb) l
836     asmlinkage __visible void __init __no_sanitize_address start_kernel(void)
837     {
838             char *command_line;
839             char *after_dashes;
840
841             set_task_stack_end_magic(&init_task);
842             smp_setup_processor_id();
843             debug_objects_early_init();
844
845             cgroup_init_early();
(gdb) p &init_task
$1 = (struct task_struct *) 0xffffffff82012840 <init_task>
(gdb) bt
#0  start_kernel () at /root/lkmc/submodules/linux/init/main.c:841
#1  0xffffffff8215145c in x86_64_start_reservations (real_mode_data=<optimized out>) at /root/lkmc/submodules/linux/arch/x86/kernel/head64.c:490
#2  0xffffffff821514e3 in x86_64_start_kernel (real_mode_data=0x138d0 <bts_ctx+2256> <error: Cannot access memory at address 0x138d0>) at /root/lkmc/submodules/linux/arch/x86/kernel/head64.c:471
#3  0xffffffff810000e6 in secondary_startup_64 () at /root/lkmc/submodules/linux/arch/x86/kernel/head_64.S:243
#4  0x0000000000000000 in ?? ()
(gdb) up
#1  0xffffffff8215145c in x86_64_start_reservations (real_mode_data=<optimized out>) at /root/lkmc/submodules/linux/arch/x86/kernel/head64.c:490
490             start_kernel();
(gdb) l
485                     break;
486             default:
487                     break;
488             }
489
490             start_kernel();
491     }
```

### Multiple architectures supported

↑ **Parent:** [Linux Kernel Module Cheat](#linux-kernel-module-cheat)

<a id="_66"></a>
E.g., if you want aarch64 instead of the default x86\_64:

<a id="_67"></a>
```
./build -aA
./run -aA
```

<a id="_68"></a>
That's it.

### Lots of in-tree examples

↑ **Parent:** [Linux Kernel Module Cheat](#linux-kernel-module-cheat)

#### Kernel modules

↑ **Parent:** [Lots of in-tree examples](#lots-of-in-tree-examples)

<a id="_69"></a>
[kernel\_modules/hello.c](https://github.com/cirosantilli/linux-kernel-module-cheat/blob/master/kernel_modules/hello.c)

<a id="_70"></a>
```
#include <linux/module.h>
#include <linux/kernel.h>

static int myinit(void)
{
	pr_info("hello init\n");
	/* 0 for success, any negative value means failure,
	 * E* consts if you want to specify failure cause.
	 * https://www.linux.com/learn/kernel-newbie-corner-loadable-kernel-modules-coming-and-going */
	return 0;
}

static void myexit(void)
{
	pr_info("hello exit\n");
}

module_init(myinit)
module_exit(myexit)
MODULE_LICENSE("GPL");
```

#### Assembly

↑ **Parent:** [Lots of in-tree examples](#lots-of-in-tree-examples)

<a id="_71"></a>
Assertions! The best way to learn assembly.

<a id="_72"></a>
[userland/arch/x86\_64/add.S](https://github.com/cirosantilli/linux-kernel-module-cheat/blob/master/userland/arch/x86_64/add.S)

<a id="_73"></a>
```
#include <lkmc.h>

LKMC_PROLOGUE
    /* Register immediate. */
    mov $1, %rax
    add $2, %rax
    LKMC_ASSERT_EQ(%rax, $3)
LKMC_EPILOGUE
```

#### Bare metal!

↑ **Parent:** [Lots of in-tree examples](#lots-of-in-tree-examples)

<a id="_74"></a>
Powered by crosstool-NG:

<a id="_75"></a>
[baremetal/arch/aarch64/semihost\_exit.S](https://github.com/cirosantilli/linux-kernel-module-cheat/blob/master/baremetal/arch/aarch64/semihost_exit.S)

<a id="_76"></a>
```
.global main
main:
    /* 0x20026 == ADP_Stopped_ApplicationExit */
    mov x1, 0x26
    movk x1, 2, lsl 16
    str x1, [sp, 0]

    /* Exit status code. Host QEMU process exits with that status. */
    mov x0, 0
    str x0, [sp, 8]

    /* x1 contains the address of parameter block.
     * Any memory address could be used.
     */
    mov x1, sp

    /* SYS_EXIT */
    mov w0, 0x18

    /* Do the semihosting call on A64. */
    hlt 0xf000
```

<h2 id="ourbigbook-com">OurBigBook.com</h2>

↑ **Parent:** [Aratu Week 2024 Talk by Ciro Santilli: My Best Random Projects](aratu-week-2024-talk-by-ciro-santilli.md)

<a id="_77"></a>
What I'm doing for 1 year now!<a id="_78"></a>

<a id="_79"></a>
- [https://docs.ourbigbook.com](https://docs.ourbigbook.com)
<a id="_80"></a>
- [https://ourbigbook.com](https://ourbigbook.com)
<a id="_81"></a>
- [https://github.com/ourbigbook/ourbigbook](https://github.com/ourbigbook/ourbigbook)

<a id="image-logo-of-the-ourbigbook-project"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook/master/logo.svg" alt="" height="600">

**[Figure 21](#image-logo-of-the-ourbigbook-project). Logo of the OurBigBook Project**.

<a id="image-everything-is-open-source"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/github_com_ourbigbook_ourbigbook.png" alt="" height="1000">

**[Figure 22](#image-everything-is-open-source). Everything is open source**. [Source](https://github.com/ourbigbook/ourbigbook).

<a id="video-intro-to-the-ourbigbook-project"></a>
**[Video 5](#video-intro-to-the-ourbigbook-project). Intro to the OurBigBook Project.** [Source](https://www.youtube.com/watch?v=7JOJYx0mmhg).

<h3 id="an-anonymous-donor-gave-me-1000-monero-126-000-usd-on-march-2024-to-work-on-this-for-one-year">An anonymous donor gave me 1000 Monero (~126,000 USD) on March 2024 to work on this for one year</h3>

↑ **Parent:** [OurBigBook.com](#ourbigbook-com)

<a id="_82"></a>
[Section "1000 Monero donation"](sponsor.md#1000-monero-donation)

<a id="_83"></a>
<img src="https://web.archive.org/web/20240306094726if_/https://www.getmonero.org/press-kit/symbols/monero-symbol-on-white-1280.png" alt="" height="600">

<a id="image-screenshot-of-ciro-santilli-s-monero-wallet-with-1000-monero-in-it-just-after-the-donation"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/Ciro_Santilli_s_Monero_wallet_after_1000_Monero_donation_on_2024-03-19.png" alt="" height="800">

**[Figure 23](#image-screenshot-of-ciro-santilli-s-monero-wallet-with-1000-monero-in-it-just-after-the-donation). Screenshot of Ciro Santilli's Monero wallet with 1000 Monero in it just after the donation**.

<a id="image-still-of-the-reaction-video-after-finding-out-about-the-big-donation-around-about-midnight"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/Ciro_Santilli_s_Monero_reaction_video_still_on_2024-03-19.jpg" alt="" height="700">

**[Figure 24](#image-still-of-the-reaction-video-after-finding-out-about-the-big-donation-around-about-midnight). Still of the reaction video after finding out about the big donation around about midnight**. [Source](https://youtu.be/2jZpXOFz1pw).

<a id="image-it-s-a-role-given-to-me-by-the-internet-people"></a>
<img src="https://web.archive.org/web/20240118181009im_/https://i.kym-cdn.com/photos/images/newsfeed/001/770/306/493" alt="" height="600">

**[Figure 25](#image-it-s-a-role-given-to-me-by-the-internet-people). It's a role given to me by the Internet people**.

### Motivation: university sucks real bad right now

↑ **Parent:** [OurBigBook.com](#ourbigbook-com)

<a id="_84"></a>
The ultimate goal: create an university:<a id="_85"></a>

<a id="_86"></a>
- without entry exams
<a id="_87"></a>
- without course requirements
<a id="_88"></a>
- where **all** material is [free and available online](university.md#force-public-university-teachers-to-publish-their-teaching-material-with-an-open-license): lecture notes, problem sheets, past exam papers
<a id="_89"></a>
- where you only pay to take certification exams for the courses that you care about

<a id="_90"></a>
The technical goal:<a id="_91"></a>


> Get [university](university.md) students to write what they learn. All university material should be amazing and free!

<a id="_92"></a>
The how:<a id="_93"></a>


> Create the ultimate [personal knowledge base software](brain.md#personal-knowledge-base-software) with multi-user mind-melding features.

### What you get

↑ **Parent:** [OurBigBook.com](#ourbigbook-com)

#### One mega article tree for each user

↑ **Parent:** [What you get](#what-you-get)

<a id="image-user-home-page-on-ourbigbook-com"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/ourbigbook.com/cirosantilli.png" alt="" height="3000">

**[Figure 26](#image-user-home-page-on-ourbigbook-com). User home page on OurBigBook.com**. Live URL: [https://ourbigbook.com/cirosantilli](https://ourbigbook.com/cirosantilli)

#### Infinitely deep table of contents

↑ **Parent:** [What you get](#what-you-get)

<a id="image-dynamic-article-tree-with-infinitely-deep-table-of-contents"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/dynamic-article-tree/demo.png" alt="" height="2700">

**[Figure 27](#image-dynamic-article-tree-with-infinitely-deep-table-of-contents). Dynamic article tree with infinitely deep table of contents**. <a id="_94"></a>
Live URL: [https://ourbigbook.com/cirosantilli/chordate](https://ourbigbook.com/cirosantilli/chordate)

<a id="_95"></a>
Descendant pages can also show up as toplevel e.g.: [https://ourbigbook.com/cirosantilli/chordate-subclade](https://ourbigbook.com/cirosantilli/chordate-subclade)

---

### Topics: the best version of an article by other users (the killer feature)

↑ **Parent:** [OurBigBook.com](#ourbigbook-com)

<a id="image-the-topics-feature-allows-you-to-find-the-best-version-of-a-subject-written-by-other-users-user"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/topics/derivative.png" alt="" height="1000">

**[Figure 28](#image-the-topics-feature-allows-you-to-find-the-best-version-of-a-subject-written-by-other-users-user). The topics feature allows you to find the best version of a subject written by other users user**. Live demo: [derivative](https://ourbigbook.com/go/topic/derivative).

### Edit and publish

↑ **Parent:** [OurBigBook.com](#ourbigbook-com)

#### Internal cross file references done right

↑ **Parent:** [Edit and publish](#edit-and-publish)

<a id="_96"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/x/hilbert-space-arrow.png" alt="" height="571">

#### Web editor with side by side preview

↑ **Parent:** [Edit and publish](#edit-and-publish)

<a id="image-web-editor"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/web-editor/cirosantilli-derivative.png" alt="" height="800">

**[Figure 29](#image-web-editor). Web editor**. You can also edit articles on the [Web editor](https://docs.ourbigbook.com/#web-editor) without installing anything locally.

#### Publish from local markup files

↑ **Parent:** [Edit and publish](#edit-and-publish)

<a id="image-you-can-publish-local-lightweight-markup-files-to-either-ourbigbook-web-or-as-a-static-website"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/local-editing/bigb-publish-to-web-or-static-editor-logos.svg" alt="" height="600">

**[Figure 30](#image-you-can-publish-local-lightweight-markup-files-to-either-ourbigbook-web-or-as-a-static-website). You can publish local lightweight markup files to either OurBigBook Web or as a static website**. For example, both of the following pages:<a id="_97"></a>

<a id="_98"></a>
- [https://cirosantilli.com](https://cirosantilli.com) (static)
<a id="_99"></a>
- [https://ourbigbook.com/cirosantilli](https://ourbigbook.com/cirosantilli) (dynamic)

are generated from the exact same source code at: [https://github.com/cirosantilli/cirosantilli.github.io](https://github.com/cirosantilli/cirosantilli.github.io).

---

<a id="image-visual-studio-code-extension-installation"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/vscode/install.png" alt="" height="750">

**[Figure 31](#image-visual-studio-code-extension-installation). Visual Studio Code extension installation**.

<a id="image-visual-studio-code-extension-tree-navigation"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/vscode/tree.png" alt="" height="1100">

**[Figure 32](#image-visual-studio-code-extension-tree-navigation). Visual Studio Code extension tree navigation**.

<h3 id="ourbigbook-com-vs-x">OurBigBook.com vs X</h3>

↑ **Parent:** [OurBigBook.com](#ourbigbook-com)

<a id="_100"></a>
[Section "Alternatives"](ourbigbook-com.md#alternatives)

<a id="_101"></a>
<img src="https://upload.wikimedia.org/wikipedia/en/8/80/Wikipedia-logo-v2.svg" alt="" height="400">

<a id="_102"></a>
[Wikipedia](website.md#wikipedia):<a id="_103"></a>

<a id="_104"></a>
- notability guidelines too stringent
<a id="_105"></a>
- Encyclopedic content requirements too stringent, we need tutorials
<a id="_106"></a>
- contributors get no clear indication of their contribution
<a id="_107"></a>
- your changes can be reverted at any time losing you hours of work

<a id="_108"></a>
<img src="https://upload.wikimedia.org/wikipedia/commons/0/02/Stack_Overflow_logo.svg" alt="" height="200">

**[Figure 33](#_108)** [Source](https://commons.wikimedia.org/wiki/File:Stack_Overflow_logo.svg).

<a id="_109"></a>
[Stack Exchange](stack-overflow.md#stack-exchange): can't write a book/have table of contents, only Q&A

<a id="_110"></a>
<img src="https://upload.wikimedia.org/wikipedia/commons/1/10/2023_Obsidian_logo.svg" alt="" height="400">

**[Figure 34](#_110)** [Source](https://commons.wikimedia.org/wiki/File:2023_Obsidian_logo.svg).

<a id="_111"></a>
Other personal knowledge bases (Obsidian, static site generators, etc.), blogs, PDFs:<a id="_112"></a>

<a id="_113"></a>
- no way to merge brains of multiple users
<a id="_114"></a>
- some of them are not focused on publishing, only personal/internal company usage

<h2 id="ciro-s-bitcoin-inscription-museum">Ciro's Bitcoin Inscription Museum</h2>

↑ **Parent:** [Aratu Week 2024 Talk by Ciro Santilli: My Best Random Projects](aratu-week-2024-talk-by-ciro-santilli.md)

<a id="_116"></a>
Article: [Section "Ciro's Bitcoin Inscription Museum"](#ciro-s-bitcoin-inscription-museum)

### How illegal does something in the Bitcoin blockchain have to be to make it illegal?

↑ **Parent:** [Ciro's Bitcoin Inscription Museum](#ciro-s-bitcoin-inscription-museum)

#### Pedobear memes?

↑ **Parent:** [How illegal does something in the Bitcoin blockchain have to be to make it illegal?](#how-illegal-does-something-in-the-bitcoin-blockchain-have-to-be-to-make-it-illegal)

<a id="image-pedobear-memes"></a>
<img src="https://web.archive.org/web/20240827163843if_/https://i.gr-assets.com/images/S/compressed.photo.goodreads.com/hostedimages/1396092852i/9088465._SX540_.jpg" alt="" height="600">

**[Figure 35](#image-pedobear-memes). Pedobear memes?** [Source](https://www.goodreads.com/topic/show/1740816-epic-fail).

#### Nuclear weapon designs?

↑ **Parent:** [How illegal does something in the Bitcoin blockchain have to be to make it illegal?](#how-illegal-does-something-in-the-bitcoin-blockchain-have-to-be-to-make-it-illegal)

<a id="image-physics-package-of-a-nuclear-weapon-design-documents"></a>
<img src="https://archive.ph/ooG6G/e9f0d891e47d6941cd956ae116b4fa7d311bb3d1.webp" alt="" height="600">

**[Figure 36](#image-physics-package-of-a-nuclear-weapon-design-documents). Physics package of a nuclear weapon design documents?** [Source](https://old.reddit.com/r/nuclearweapons/comments/196er9b/some\_speculation\_on\_the\_b61\_thermonuclear\_gravity/).

#### Political memes?

↑ **Parent:** [How illegal does something in the Bitcoin blockchain have to be to make it illegal?](#how-illegal-does-something-in-the-bitcoin-blockchain-have-to-be-to-make-it-illegal)

<a id="image-tank-man"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/china-dictatorship-media/master/Tank_Man.jpg" alt="" height="600">

**[Figure 37](#image-tank-man). Tank Man?** [Source](https://www.scmp.com/culture/article/2096173/other-photographers-who-snapped-tiananmens-tank-man-and-their-memories-june).

### Ordinal ruleset inscription (2022): the end of the line: Eternal September arrives

↑ **Parent:** [Ciro's Bitcoin Inscription Museum](#ciro-s-bitcoin-inscription-museum)

<a id="image-ordinal-0"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/6fb976ab49dcec017f1e201e84395983204ae1a7c2abf7ced0a85d692e442799-0.png" alt="" height="600">

**[Figure 38](#image-ordinal-0). Ordinal \#0**.

<a id="image-bitcoin-ordinal-ruleset-inscription-frequency-with-time"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/Bitcoin_ordinal_ruleset_inscriptions_per_time_2024_08_31.png" alt="" height="510">

**[Figure 39](#image-bitcoin-ordinal-ruleset-inscription-frequency-with-time). Bitcoin ordinal ruleset inscription frequency with time**. [Source](https://dune.com/dgtl\_assets/bitcoin-ordinals-analysis).

### My obsession: find **every** image before ordinals

↑ **Parent:** [Ciro's Bitcoin Inscription Museum](#ciro-s-bitcoin-inscription-museum)

#### Fan tributes

↑ **Parent:** [My obsession: find **every** image before ordinals](#my-obsession-find-every-image-before-ordinals)

<a id="code-ascii-art-of-a-force-of-will-magic-the-gathering-card-inscribed-blockchain-in-the-bitcoin-blockchain"></a>
```
 -------------------------------------
|  Force of Will               3 U U  |
|  ---------------------------------  |
| |                  ////////////   | |
| |                ////() ()\////\  | |
| |               ///_\ (--) \///\  | |
| |        )      ////  \_____///\\ | |
| |       ) \      /   /   /    /   | |
| |    ) /   \     |   |  /   _/    | |
| |   ) \  (  (   /   / /   / \     | |
| |  / ) ( )  / (    )/(    )  \    | |
| |  \(_)/(_)/  /UUUU \  \\\/   |   | |
| .---------------------------------. |
| Interrupt                           |
| ,---------------------------------, |
| | You may pay 1 life and remove a | |
| | blue card in your hand from the | |
| | game instead of paying Force of | |
| | Will's casting cost.  Effects   | |
| | that prevent or redirect damage | |
| | cannot be used to counter this  | |
| | loss of life.                   | |
| | Counter target spell.           | |
| `---------------------------------` |
|                                     l
| Illus.  Terese Nelsen               |
 -------------------------------------
```

#### Social media

↑ **Parent:** [My obsession: find **every** image before ordinals](#my-obsession-find-every-image-before-ordinals)

<a id="image-wearestarstuff-jpg"></a>
<img src="https://web.archive.org/web/20230604115203im_/http://bitfossil.org/8d1b3c094b782198deb7381efb57b1208244375e7a1029ec159306d6a8fd25d8/WeAreStarStuff.jpg" alt="" height="600">

**[Figure 40](#image-wearestarstuff-jpg). `WeAreStarStuff.jpg`**. AtomSea and EMBII (December 2013)

#### Art

↑ **Parent:** [My obsession: find **every** image before ordinals](#my-obsession-find-every-image-before-ordinals)

<a id="image-yellowrobot-jpg"></a>
<img src="https://web.archive.org/web/20220102092623im_/http://bitfossil.org/4cbb32cd27b5b5edc12d3559bdffc1355ac2a210463d5cfaadc7ce9b06675b2b/YellowRobot.jpg" alt="" height="600">

**[Figure 41](#image-yellowrobot-jpg). `YellowRobot.jpg`**. 2017

#### Memes

↑ **Parent:** [My obsession: find **every** image before ordinals](#my-obsession-find-every-image-before-ordinals)

<a id="image-water-deer"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/357e8ae080e5a1b554eaec2953e3e6e2e7955f3af4559dd0f1bc6381d56aa183.jpg" alt="" height="600">

**[Figure 42](#image-water-deer). Water Deer**. 2016 from [https://badtaxidermy.com](https://badtaxidermy.com) Visible at: [https://web.archive.org/web/20200527070011/http://www.badtaxidermy.com/?page=3](https://web.archive.org/web/20200527070011/http://www.badtaxidermy.com/?page=3). Uploaded with: cryptograffiti.info.

#### Love declaration

↑ **Parent:** [My obsession: find **every** image before ordinals](#my-obsession-find-every-image-before-ordinals)

<a id="image-chinese-wedding-2016"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/609d5e0f968c0ab7abc2be21468cfd552483d38b08e6df23d27766eb61b9be3c.jpg" alt="" height="700">

**[Figure 43](#image-chinese-wedding-2016). Chinese wedding (2016)**

#### Promotional material

↑ **Parent:** [My obsession: find **every** image before ordinals](#my-obsession-find-every-image-before-ordinals)

<a id="_117"></a>
Free [GrrCon](https://grrcon.com/) ticket (2018):

<a id="_118"></a>
```
@@@@@@@@@@@@@@@@@@@@@@@@YOUR@FREE@GRRCON@TICKET@CODE@@@@@@@@@@@@@@@@@@@@@@@@@@@
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@,          *@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
@@@@@@@@@@@@@@@@@@@@@@@@@@%                          @@@@@@@@@@@@@@@@@@@@@@@@@@
@@@@@@@@@@@@@@@@@@@@@@                                   .@@@@@@@@@@@@@@@@@@@@@
@@@@@@@@@@@@@@@@@@@          *@@@@@@@@@@@@@@@@@@@,           @@@@@@@@@@@@@@@@@@
@@@@@@@@@@@@@@@@         @@@@(                   %@@@@          @@@@@@@@@@@@@@@
@@@@@@@@@@@@@@       @@@@                             @@@&        @@@@@@@@@@@@@
@@@@@@@@@@@@       @@@        @@@@@@@@@@@@@,@.           @@@        @@@@@@@@@@@
@@@@@@@@@@      %@@       .&@@@@@@&%@@@@@&&&@@@@@#          @@/      /@@@@@@@@@
@@@@@@@@@      @@       @@@&@@O@@@@@@@@@@@@@@@@(@@@@&         @@       @@@@@@@@
@@@@@@@@     @@.      .@@@,%&@@P@@@@@(,*&*@@@@@@@@#(#.@        (@@      @@@@@@@
@@@@@@*     @@       @@(@%@@@@@&R@@@@&@@@@@@@&@@@@@@/ @@@        @@      @@@@@@
@@@@@#     @@       @@@@@@@@,,@%@E@%@@@@@@@@@@@%@@@@@.@@@@        @@      @@@@@
@@@@@     @@        @.@@@@@,@@@(@,T@@@@@@@@@@@@@@@@@@@@@@@@        @@      @@@@
@@@@     @@        @&@@@@@@/@#@(@&@U@@@@@@@@(@@@@@@., #@@@@@        @@      @@@
@@@*    @@         @@@@&@@&@    #@@@R@.@@@@@.@@@@@@@%@@(@@@@@        @@     @@@
@@@     @@         /@@*@@        @@@/N/@,@@@@@@@@@    @@@@@@,        @@      @@
@@@    @@          @@@@@          @@.@I@@,@@@@@@@@    @@@@&@@         @@     @@
@@/    @@           @@@,           (#@/S@@@@@@.,@     **@@&,@         @@     @@
@@     @@           %((           @#@@@@M@@@@@&@    #./%&@@*          @@     %@
@@     @@           #&&@          @@@@&@@Y@@@@@     &@,@@@.(          @@     %@
@@,    @@           @@@@@@        *(@@%@@@F&@.      @@&%@@            @@     @@
@@@    @@           @#@%@/@         @@@*@@@R(      @@@&@              @@     @@
@@@     @@         @@@@@@@@@%@@@%%@@@@@@@%%/I@  @@@@, @              @@      @@
@@@.    @@         @@@@@@@*@&@@@@# @(@@@@@@@@E@@@@@@@&               @@     @@@
@@@@     @@         @@@@&@@(@@@@@@.@# @@@ @@@@N@@@@,@(              @@      @@@
@@@@@     @@            @@@*@@&@@*(@  @@@&@@&@@D@@@@&              @@      @@@@
@@@@@.     @@                  @/@,@@@@@@@@@@@@@@%                @@      @@@@@
@@@@@@      @@                 @@@@@@@@@@@@@,@@@@                @@      %@@@@@
@@@@@@@,     @@/             @&@@(@@@@ @@@@@@@@@               &@@      @@@@@@@
@@@@@@@@@      @@          #%@(,&,@@@@ @(&  @/,@              @@       @@@@@@@@
@@@@@@@@@@      /@@        @@&@@@@@,*  @@&  @@@@@@         .@@.       @@@@@@@@@
@@@@@@@@@@@@       @@@        @(@@@@@@ @@@  .@(@@,       @@@        @@@@@@@@@@@
@@@@@@@@@@@@@@       &@@@                             @@@#        @@@@@@@@@@@@@
@@@@@@@@@@@@@@@@         @@@@@                   @@@@@          @@@@@@@@@@@@@@@
@@@@@@@@@@@@@@@@@@#          .@@@@@@@@@@@@@@@@@@@            @@@@@@@@@@@@@@@@@@
@@@@@@@@@@@@@@@@@@@@@@         @  ,        .  @           @@@@@@@@@@@@@@@@@@@@@
@@@@@@@@@@@@@@@@@@@@@@@@@@     @ @   @#   @  *, @     @@@@@@@@@@@@@@@@@@@@@@@@@
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@&              @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
```

<a id="_119"></a>
Removing the `@` signs:

<a id="_120"></a>
```
                        YOUR FREE GRRCON TICKET CODE
                                  ,          *
                          %
                                                          .
                              *                   ,
                              (                   %
                                                          &
                                            , .
                %         .&      &%     &&&     #            /      /
                            &  O                (    &
                .      .   ,%&  P     (,*&*        #(#.         (
      *                ( %     &R    &       &      /
      #                      ,, % E %           %     .
                      .     ,   ( ,T
                    &      / # ( & U        (      ., #
    *                   &  &     #   R .     .       %  (
                    /  *             /N/ ,                   ,
                                    . I  ,                &
  /                    ,           (# /S      .,      **  &,
                    %((            #    M     &     #./%&  *                 %
                    #&&               &  Y          & ,   .(                 %
  ,                               *(  %   F& .        &%
                      # % /             *   R(         &
                            %   %%       %%/I       ,
    .                      * &    #  (        E       &
                        &  (      . #         N    , (
                            *  &  *(      &  &  D    &
      .                          / ,              %
                                            ,                            %
        ,       /              &  (                             &
                            #% (,&,      (&   /,
                /            &     ,*    &                 .  .
                                (            . (  ,
                      &                                   #

                  #          .
                                  ,        .
                                      #      *,
                                &
```

## China Dictatorship

↑ **Parent:** [Aratu Week 2024 Talk by Ciro Santilli: My Best Random Projects](aratu-week-2024-talk-by-ciro-santilli.md)

<a id="_122"></a>
<a id="_123"></a>
- [https://cirosantilli.com/china-dictatorship](https://cirosantilli.com/china-dictatorship)
<a id="_124"></a>
- [https://github.com/cirosantilli/china-dictatorship](https://github.com/cirosantilli/china-dictatorship)

<a id="_125"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/github.com_cirosantilli_china-dictatorship.png" alt="" height="1000">

**[Figure 44](#_125)** [Source](https://github.com/cirosantilli/china-dictatorship).

### Xi Jinping, ruler of China

↑ **Parent:** [China Dictatorship](#china-dictatorship)

<a id="image-xi-jinping-ruler-of-china"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/china-dictatorship-media/master/Xi_Jinping_The_Governance_of_China_photo.jpg" alt="" height="800">

**[Figure 45](#image-xi-jinping-ruler-of-china). Xi Jinping, ruler of China**.

### Xi Jinping, sadomasochist in leather suit

↑ **Parent:** [China Dictatorship](#china-dictatorship)

<a id="image-xi-jinping-ruler-of-china-wearing-leather-sadomasochist-outfit"></a>
<img src="https://web.archive.org/web/20230609155744im_/https://preview.redd.it/15l6tpf1dqd31.jpg?width=836&amp;auto=webp&amp;v=enabled&amp;s=2b2f3b9f0ae40826858e0f3908f621ff86d62520" alt="" height="800">

**[Figure 46](#image-xi-jinping-ruler-of-china-wearing-leather-sadomasochist-outfit). Xi Jinping, ruler of China, wearing leather sadomasochist outfit**.

<h3 id="collateral-freedom-https-the-censor-doesn-t-know-which-path-you-access">Collateral freedom: <b>HTTPS</b>: the censor doesn't know which path you access</h3>

↑ **Parent:** [China Dictatorship](#china-dictatorship)

<a id="_126"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/china-dictatorship-media/master/GitHub_collateral_freedom.jpg" alt="" height="800">

### The GitHub issue tracker is quite cute, because Chinese people actually use GitHub search in addition to search engines

↑ **Parent:** [China Dictatorship](#china-dictatorship)

<a id="_127"></a>
[https://github.com/cirosantilli/china-dictatorship/issues](https://github.com/cirosantilli/china-dictatorship/issues)

<a id="_128"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/china-dictatorship-media/master/github.com_cirosantilli_china-dictatorship_issues.png" alt="" height="2000">

**[Figure 47](#_128)** [Source](https://github.com/cirosantilli/china-dictatorship/issues).

### Stack Overflow attacks

↑ **Parent:** [China Dictatorship](#china-dictatorship)

<a id="_129"></a>
<img src="https://upload.wikimedia.org/wikipedia/commons/0/02/Stack_Overflow_logo.svg" alt="" height="200">

**[Figure 48](#_129)** [Source](https://commons.wikimedia.org/wiki/File:Stack_Overflow_logo.svg).

<a id="_130"></a>
[https://web.archive.org/web/20210917212322/https://stackoverflow.com/questions/6121094/how-do-i-run-a-program-with-commandline-arguments-using-gdb-within-a-bash-script/6121299](https://web.archive.org/web/20210917212322/https://stackoverflow.com/questions/6121094/how-do-i-run-a-program-with-commandline-arguments-using-gdb-within-a-bash-script/6121299)

<a id="_131"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/china-dictatorship-media/master/Stack_Overflow_keyword_attack_by_Ciro_Santilli.png" alt="" height="1660">

### Package managers

↑ **Parent:** [China Dictatorship](#china-dictatorship)

#### PyPi: the cowards took it down

↑ **Parent:** [Package managers](#package-managers)

<a id="_132"></a>
Up March 2023 [https://web.archive.org/web/20230306090740/https://pypi.org/project/china-dictatorship/](https://web.archive.org/web/20230306090740/https://pypi.org/project/china-dictatorship/)

<a id="_133"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/china-dictatorship-media/master/pypi.org_project_china-dictatorship.png" alt="" height="1900">

<a id="_134"></a>
Down November 2023 [http://web.archive.org/web/20231110041847/https://pypi.org/project/china-dictatorship/](http://web.archive.org/web/20231110041847/https://pypi.org/project/china-dictatorship/)

<a id="_135"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/china-dictatorship-media/master/pypi.org_project_china-dictatorship_down.png" alt="" height="916">

## All GitHub commit emails

↑ **Parent:** [Aratu Week 2024 Talk by Ciro Santilli: My Best Random Projects](aratu-week-2024-talk-by-ciro-santilli.md)  
🏷️ **Tags:** [All GitHub commit emails](#all-github-commit-emails)

<a id="_139"></a>
[https://github.com/cirosantilli/all-github-commit-emails](https://github.com/cirosantilli/all-github-commit-emails)

<a id="_140"></a>
More info: [Section "All GitHub Commit Emails"](ciro-santilli-s-projects.md#all-github-commit-emails)

<a id="_141"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/GitHub_Archive_Google_bigquery_PushEvent_email_highlight.png" alt="" height="810">

<a id="_142"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/All_GitHub_commit_emails_repo_screenshot_before_takedown_archive_is.png" alt="" height="768">

## Other projects

↑ **Parent:** [Aratu Week 2024 Talk by Ciro Santilli: My Best Random Projects](aratu-week-2024-talk-by-ciro-santilli.md)

<a id="_143"></a>
See also [Ciro Santilli's naughty projects](ciro-santilli-s-projects.md#ciro-santilli-s-naughty-projects):<a id="_144"></a>

<a id="_145"></a>
- [https://github.com/cirosantilli/stack-overflow-vote-fraud-script](https://github.com/cirosantilli/stack-overflow-vote-fraud-script)
<a id="_146"></a>
- [https://ourbigbook.com/cirosantilli/facebook-profile-face-dump](https://ourbigbook.com/cirosantilli/facebook-profile-face-dump)

## ↑ Ancestors (3)

1. [Talk by Ciro Santilli](ciro-santilli.md#talk-by-ciro-santilli)
2. [Ciro Santilli](ciro-santilli.md)
3. [Ciro Santilli's Homepage](README.md)

## ← Incoming links (8)

- [Ciro Santilli's Homepage](README.md)
- [Aratu Week IV](computer.md#aratu-week-iv)
- [CIA 2010 covert communication websites](cia-2010-covert-communication-websites.md)
- [Backlinks](cia-2010-covert-communication-websites.md#backlinks)
- [Cool data embedded in the Bitcoin blockchain](cool-data-embedded-in-the-bitcoin-blockchain.md)
- [CIA 2010 websites video](updates.md#cia-2010-websites-video)
- [Introductory video for Bitcoin inscription museum](updates.md#introductory-video-for-bitcoin-inscription-museum)
- [Two Linux Kernel Module Cheat videos](updates.md#two-linux-kernel-module-cheat-videos)
