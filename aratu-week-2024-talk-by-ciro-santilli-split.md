# Aratu Week 2024 Talk by Ciro Santilli: My Best Random Projects

↑ **Parent:** [Talk by Ciro Santilli](talk-by-ciro-santilli.md)  
🏷️ **Tags:** [Aratu Week](aratu-week.md)

<a id="_2"></a>
This talk was presented on 24 September 2024 as part of the 2024 [Aratu Week](aratu-week.md), a small online conference by [Brazilian](brazil-split.md) hacker interest group [Boitatech](boitatech.md).

<a id="_3"></a>
How to contact me: [Section "How to contact Ciro Santilli"](contact.md)

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

- [Introduction](aratu-week-2024-talk-by-ciro-santilli/introduction.md)
  - [Creative Commons CC By-SA](aratu-week-2024-talk-by-ciro-santilli/creative-commons-cc-by-sa.md)
  - [I'm not a professional hacker, I did some very occasional OSINT just for fun](aratu-week-2024-talk-by-ciro-santilli/i-m-not-a-professional-hacker-i-did-some-very-occasional-osint-just-for-fun.md)
- [CIA 2010 covert communication websites](aratu-week-2024-talk-by-ciro-santilli/cia-2010-covert-communication-websites.md)
  - [Prelude: initial reports without specific websites (2018-)](aratu-week-2024-talk-by-ciro-santilli/prelude-initial-reports-without-specific-websites-2018.md)
  - [Starting point: 2022 Reuters article](aratu-week-2024-talk-by-ciro-santilli/starting-point-2022-reuters-article.md)
  - [Coolest findings](aratu-week-2024-talk-by-ciro-santilli/coolest-findings.md)
    - [The Star Wars website](aratu-week-2024-talk-by-ciro-santilli/the-star-wars-website.md)
    - [Examples of USA spying on its "allies"](aratu-week-2024-talk-by-ciro-santilli/examples-of-usa-spying-on-its-allies.md)
      - [Brazil](aratu-week-2024-talk-by-ciro-santilli/brazil.md)
      - [Germany](aratu-week-2024-talk-by-ciro-santilli/germany.md)
      - [France](aratu-week-2024-talk-by-ciro-santilli/france.md)
      - [Italy](aratu-week-2024-talk-by-ciro-santilli/italy.md)
  - [Methodology](aratu-week-2024-talk-by-ciro-santilli/methodology.md)
    - [The easy: IP range searches](aratu-week-2024-talk-by-ciro-santilli/the-easy-ip-range-searches.md)
    - [The hard: finding new IP ranges!](aratu-week-2024-talk-by-ciro-santilli/the-hard-finding-new-ip-ranges.md)
      - [2013 DNS census data](aratu-week-2024-talk-by-ciro-santilli/2013-dns-census-data.md)
      - [Wayback Machine searches for the communication method paths: Tor army parallelization!](aratu-week-2024-talk-by-ciro-santilli/wayback-machine-searches-for-the-communication-method-paths-tor-army-parallelization.md)
      - [Cheeky fuzzy fingerprint: the domain name contains `news`](aratu-week-2024-talk-by-ciro-santilli/cheeky-fuzzy-fingerprint-the-domain-name-contains-news.md)
      - [Chinese expired domain trackers: another valuable domain data dump](aratu-week-2024-talk-by-ciro-santilli/chinese-expired-domain-trackers-another-valuable-domain-data-dump.md)
        - [I scraped them and uploaded to GitHub repos, 2011 - 2022, 20-30 M entries / year](aratu-week-2024-talk-by-ciro-santilli/i-scraped-them-and-uploaded-to-github-repos-2011-2022-20-30-m-entries-year.md)
  - [Help wanted! Some sites were almost certainly missed. Contributions will be acknowledged.](aratu-week-2024-talk-by-ciro-santilli/help-wanted-some-sites-were-almost-certainly-missed-contributions-will-be-acknowledged.md)
- [Linux Kernel Module Cheat](aratu-week-2024-talk-by-ciro-santilli/linux-kernel-module-cheat.md)
  - [Get a Linux terminal on QEMU](aratu-week-2024-talk-by-ciro-santilli/get-a-linux-terminal-on-qemu.md)
  - [**Everything** is built from source and easily modifiable, powered by Buildroot](aratu-week-2024-talk-by-ciro-santilli/everything-is-built-from-source-and-easily-modifiable-powered-by-buildroot.md)
  - [Kernel GDB step debugging just works](aratu-week-2024-talk-by-ciro-santilli/kernel-gdb-step-debugging-just-works.md)
  - [Multiple architectures supported](aratu-week-2024-talk-by-ciro-santilli/multiple-architectures-supported.md)
  - [Lots of in-tree examples](aratu-week-2024-talk-by-ciro-santilli/lots-of-in-tree-examples.md)
    - [Kernel modules](aratu-week-2024-talk-by-ciro-santilli/kernel-modules.md)
    - [Assembly](aratu-week-2024-talk-by-ciro-santilli/assembly.md)
    - [Bare metal!](aratu-week-2024-talk-by-ciro-santilli/bare-metal.md)
- [OurBigBook.com](aratu-week-2024-talk-by-ciro-santilli/ourbigbook-com.md)
  - [An anonymous donor gave me 1000 Monero (~126,000 USD) on March 2024 to work on this for one year](aratu-week-2024-talk-by-ciro-santilli/an-anonymous-donor-gave-me-1000-monero-126-000-usd-on-march-2024-to-work-on-this-for-one-year.md)
  - [Motivation: university sucks real bad right now](aratu-week-2024-talk-by-ciro-santilli/motivation-university-sucks-real-bad-right-now.md)
  - [What you get](aratu-week-2024-talk-by-ciro-santilli/what-you-get.md)
    - [One mega article tree for each user](aratu-week-2024-talk-by-ciro-santilli/one-mega-article-tree-for-each-user.md)
    - [Infinitely deep table of contents](aratu-week-2024-talk-by-ciro-santilli/infinitely-deep-table-of-contents.md)
  - [Topics: the best version of an article by other users (the killer feature)](aratu-week-2024-talk-by-ciro-santilli/topics-the-best-version-of-an-article-by-other-users-the-killer-feature.md)
  - [Edit and publish](aratu-week-2024-talk-by-ciro-santilli/edit-and-publish.md)
    - [Internal cross file references done right](aratu-week-2024-talk-by-ciro-santilli/internal-cross-file-references-done-right.md)
    - [Web editor with side by side preview](aratu-week-2024-talk-by-ciro-santilli/web-editor-with-side-by-side-preview.md)
    - [Publish from local markup files](aratu-week-2024-talk-by-ciro-santilli/publish-from-local-markup-files.md)
  - [OurBigBook.com vs X](aratu-week-2024-talk-by-ciro-santilli/ourbigbook-com-vs-x.md)
- [Ciro's Bitcoin Inscription Museum](aratu-week-2024-talk-by-ciro-santilli/ciro-s-bitcoin-inscription-museum.md)
  - [How illegal does something in the Bitcoin blockchain have to be to make it illegal?](aratu-week-2024-talk-by-ciro-santilli/how-illegal-does-something-in-the-bitcoin-blockchain-have-to-be-to-make-it-illegal.md)
    - [Pedobear memes?](aratu-week-2024-talk-by-ciro-santilli/pedobear-memes.md)
    - [Nuclear weapon designs?](aratu-week-2024-talk-by-ciro-santilli/nuclear-weapon-designs.md)
    - [Political memes?](aratu-week-2024-talk-by-ciro-santilli/political-memes.md)
  - [Ordinal ruleset inscription (2022): the end of the line: Eternal September arrives](aratu-week-2024-talk-by-ciro-santilli/ordinal-ruleset-inscription-2022-the-end-of-the-line-eternal-september-arrives.md)
  - [My obsession: find **every** image before ordinals](aratu-week-2024-talk-by-ciro-santilli/my-obsession-find-every-image-before-ordinals.md)
    - [Fan tributes](aratu-week-2024-talk-by-ciro-santilli/fan-tributes.md)
    - [Social media](aratu-week-2024-talk-by-ciro-santilli/social-media.md)
    - [Art](aratu-week-2024-talk-by-ciro-santilli/art.md)
    - [Memes](aratu-week-2024-talk-by-ciro-santilli/memes.md)
    - [Love declaration](aratu-week-2024-talk-by-ciro-santilli/love-declaration.md)
    - [Promotional material](aratu-week-2024-talk-by-ciro-santilli/promotional-material.md)
- [China Dictatorship](aratu-week-2024-talk-by-ciro-santilli/china-dictatorship.md)
  - [Xi Jinping, ruler of China](aratu-week-2024-talk-by-ciro-santilli/xi-jinping-ruler-of-china.md)
  - [Xi Jinping, sadomasochist in leather suit](aratu-week-2024-talk-by-ciro-santilli/xi-jinping-sadomasochist-in-leather-suit.md)
  - [Collateral freedom: **HTTPS**: the censor doesn't know which path you access](aratu-week-2024-talk-by-ciro-santilli/collateral-freedom-https-the-censor-doesn-t-know-which-path-you-access.md)
  - [The GitHub issue tracker is quite cute, because Chinese people actually use GitHub search in addition to search engines](aratu-week-2024-talk-by-ciro-santilli/the-github-issue-tracker-is-quite-cute-because-chinese-people-actually-use-github-search-in-addition-to-search-engines.md)
  - [Stack Overflow attacks](aratu-week-2024-talk-by-ciro-santilli/stack-overflow-attacks.md)
  - [Package managers](aratu-week-2024-talk-by-ciro-santilli/package-managers.md)
    - [PyPi: the cowards took it down](aratu-week-2024-talk-by-ciro-santilli/pypi-the-cowards-took-it-down.md)
- [All GitHub commit emails](aratu-week-2024-talk-by-ciro-santilli/all-github-commit-emails.md)
- [Other projects](aratu-week-2024-talk-by-ciro-santilli/other-projects.md)

## ↑ Ancestors (3)

1. [Talk by Ciro Santilli](talk-by-ciro-santilli.md)
2. [Ciro Santilli](ciro-santilli-split.md)
3. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (8)

- [Ciro Santilli's Homepage](split.md)
- [Aratu Week IV](aratu-week-iv.md)
- [CIA 2010 covert communication websites](cia-2010-covert-communication-websites-split.md)
- [Backlinks](cia-2010-covert-communication-websites/backlinks.md)
- [Cool data embedded in the Bitcoin blockchain](cool-data-embedded-in-the-bitcoin-blockchain-split.md)
- [CIA 2010 websites video](updates/cia-2010-websites-video.md)
- [Introductory video for Bitcoin inscription museum](updates/introductory-video-for-bitcoin-inscription-museum.md)
- [Two Linux Kernel Module Cheat videos](updates/two-linux-kernel-module-cheat-videos.md)
