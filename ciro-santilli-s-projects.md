# Ciro Santilli's projects

↑ **Parent:** [Ciro Santilli](ciro-santilli.md)

Major projects can be seen at: [Section "The most important projects done by Ciro Santilli"](the-most-important-projects-done-by-ciro-santilli.md).

A summary of minor projects is given at: [Ciro Santilli's minor projects](the-most-important-projects-done-by-ciro-santilli.md#ciro-santilli-s-minor-projects).

This section is a dump for anything else, to keep those sacred first sections that show on the top of the homepage clean.

**Table of contents**

- [OurBigBook](#ourbigbook)
  - [OurBigBook Markup](#ourbigbook-markup)
  - [OurBigBook CLI](#ourbigbook-cli)
  - [OurBigBook Library](#ourbigbook-library)
  - [OurBigBook Web](#ourbigbook-web)
    - [OurBigBook.com](ourbigbook-com.md)
      - [How the website works](ourbigbook-com.md#how-the-website-works)
      - [Alternatives](ourbigbook-com.md#alternatives)
        - [Wikipedia](ourbigbook-com.md#wikipedia)
        - [Stack Exchange](ourbigbook-com.md#stack-exchange)
        - [Blogs](ourbigbook-com.md#blogs)
        - [University lecture notes](ourbigbook-com.md#university-lecture-notes)
          - [How to convince teachers to use CC BY-SA](ourbigbook-com.md#how-to-convince-teachers-to-use-cc-by-sa)
        - [Existing data sources](ourbigbook-com.md#existing-data-sources)
        - [Personal knowledge base software](ourbigbook-com.md#personal-knowledge-base-software)
        - [Knowledge graph editors](ourbigbook-com.md#knowledge-graph-editors)
        - [Learning management systems](ourbigbook-com.md#learning-management-systems)
        - [GitHub](ourbigbook-com.md#github)
        - [Other projects](ourbigbook-com.md#other-projects)
      - [Action plan](ourbigbook-com.md#action-plan)
      - [Philosophy](ourbigbook-com.md#philosophy)
        - [Desired social impact](ourbigbook-com.md#desired-social-impact)
        - [Motivation](ourbigbook-com.md#motivation)
        - [Manifesto](ourbigbook-com.md#manifesto)
      - [Feature ideas](ourbigbook-com.md#feature-ideas)
        - [PageRank-like ranking](ourbigbook-com.md#pagerank-like-ranking)
      - [User acquisition](ourbigbook-com.md#user-acquisition)
      - [Funding](ourbigbook-com.md#funding)
        - [Why it is hard to make money from this website](ourbigbook-com.md#why-it-is-hard-to-make-money-from-this-website)
        - [Crowdfunding](ourbigbook-com.md#crowdfunding)
        - [Charitable grant opportunities](ourbigbook-com.md#charitable-grant-opportunities)
        - [Consulting](ourbigbook-com.md#consulting)
        - [Knowledge market](ourbigbook-com.md#knowledge-market)
        - [Advertisement](ourbigbook-com.md#advertisement)
        - [Association with innovative schools](ourbigbook-com.md#association-with-innovative-schools)
        - [Venture capital](ourbigbook-com.md#venture-capital)
  - [OurBigBook feature](#ourbigbook-feature)
    - [OurBigBook topic feature](#ourbigbook-topic-feature)
    - [OurBigBook dynamic tree](#ourbigbook-dynamic-tree)
- [x86 bare metal examples](#x86-bare-metal-examples)
- [Ciro Santilli's naughty projects](#ciro-santilli-s-naughty-projects)
  - [All GitHub Commit Emails](#all-github-commit-emails)
  - [Facebook profile face dump](#facebook-profile-face-dump)
- [Ciro Santilli's data projects](#ciro-santilli-s-data-projects)
  - [Wikipedia CatTree](#wikipedia-cattree)
- [Ciro Santilli's open source contributions](ciro-santilli-s-open-source-contributions.md)
  - [Size scale](ciro-santilli-s-open-source-contributions.md#size-scale)
  - [Patches](ciro-santilli-s-open-source-contributions.md#patches)
    - [Merged by others](ciro-santilli-s-open-source-contributions.md#merged-by-others)
    - [Merged by Ciro](ciro-santilli-s-open-source-contributions.md#merged-by-ciro)
  - [Bug reports and feature requests](ciro-santilli-s-open-source-contributions.md#bug-reports-and-feature-requests)
    - [Closed source](ciro-santilli-s-open-source-contributions.md#closed-source)
    - [Open source](ciro-santilli-s-open-source-contributions.md#open-source)
    - [Not verified](ciro-santilli-s-open-source-contributions.md#not-verified)
  - [Security](ciro-santilli-s-open-source-contributions.md#security)

## OurBigBook

↑ **Parent:** [Ciro Santilli's projects](ciro-santilli-s-projects.md)

[https://docs.ourbigbook.com/](https://docs.ourbigbook.com/)

<a id="image-logo-of-the-ourbigbook-project"></a>
![](https://raw.githubusercontent.com/ourbigbook/ourbigbook/master/logo.svg)

**[Figure 1](#image-logo-of-the-ourbigbook-project). Logo of the OurBigBook Project**.

### OurBigBook Markup

↑ **Parent:** [OurBigBook](#ourbigbook)  
🏷️ **Tags:** [Lightweight markup language](computer.md#lightweight-markup-language), [Personal knowledge base](brain.md#personal-knowledge-base)

The [markup language](computer.md#markup-language) of [OurBigBook.com](ourbigbook-com.md).

Also used on [Ciro Santilli's website](cirosantilli-com.md) as a [static website](website.md#static-website) via the [OurBigBook CLI](#ourbigbook-cli).

The one [markup language](computer.md#markup-language) to rule them all?

Documentation at: [https://docs.ourbigbook.com](https://docs.ourbigbook.com).

### OurBigBook CLI

↑ **Parent:** [OurBigBook](#ourbigbook)  
🏷️ **Tags:** [Static site generator](website.md#static-site-generator)

Official [Command-line interface](software.md#command-line-interface) to convert a directory of [OurBigBook Markup](#ourbigbook-markup) files into a [static website](website.md#static-website). See also: [https://cirosantilli.com/ourbigbook/ourbigbook-cli](https://cirosantilli.com/ourbigbook/ourbigbook-cli)

### OurBigBook Library

↑ **Parent:** [OurBigBook](#ourbigbook)

Base [JavaScript](programming-language.md#javascript) library that implements the [OurBigBook Markup](#ourbigbook-markup). Use by both:
- [OurBigBook CLI](#ourbigbook-cli)
- [OurBigBook Web](#ourbigbook-web)

### OurBigBook Web

↑ **Parent:** [OurBigBook](#ourbigbook)

The website system that runs [OurBigBook.com](ourbigbook-com.md). For further information see:
- [OurBigBook.com](ourbigbook-com.md): rationale
- [https://cirosantilli.com/ourbigbook/ourbigbook-web](https://cirosantilli.com/ourbigbook/ourbigbook-web): project documentation
Relies on the [OurBigBook Library](#ourbigbook-library) to compile [OurBigBook Markup](#ourbigbook-markup).

<h4 id="ourbigbook-com">OurBigBook.com</h4>

↑ **Parent:** [OurBigBook Web](#ourbigbook-web)

[This section is present in another page, follow this link to view it.](ourbigbook-com.md)

### OurBigBook feature

↑ **Parent:** [OurBigBook](#ourbigbook)

#### OurBigBook topic feature

↑ **Parent:** [OurBigBook feature](#ourbigbook-feature)

More info at: [https://docs.ourbigbook.com#ourbigbook-web-topics](https://docs.ourbigbook.com#ourbigbook-web-topics)

#### OurBigBook dynamic tree

↑ **Parent:** [OurBigBook feature](#ourbigbook-feature)

More info at: [https://docs.ourbigbook.com/ourbigbook-web-dynamic-article-tree](https://docs.ourbigbook.com/ourbigbook-web-dynamic-article-tree)

## x86 bare metal examples

↑ **Parent:** [Ciro Santilli's projects](ciro-santilli-s-projects.md)

[https://github.com/cirosantilli/x86-bare-metal-examples](https://github.com/cirosantilli/x86-bare-metal-examples)

As mentioned at [Section "Linux Kernel Module Cheat"](the-most-important-projects-done-by-ciro-santilli.md#linux-kernel-module-cheat), this should be merged into that other project.

<h2 id="ciro-santilli-s-naughty-projects">Ciro Santilli's naughty projects</h2>

↑ **Parent:** [Ciro Santilli's projects](ciro-santilli-s-projects.md)

If [Ciro Santilli](ciro-santilli.md) weren't a [natural born activist](the-most-important-projects-done-by-ciro-santilli.md#ciro-santilli-s-campaign-for-freedom-of-speech-in-china), he chould have made an excellent [intelligence analyst](science.md#intelligence-analysis)! See also: [Section "Being naughty and creative are correlated"](don-t-be-a-pussy.md#being-naughty-and-creative-are-correlated).
- [Stack Overflow Vote Fraud Script](stack-overflow.md#stack-overflow-vote-fraud-script)
- [GitHub](software.md#github) makes Ciro feel especially naughty:
  - [All GitHub Commit Emails](#all-github-commit-emails): he extracted (almost) all Git commit emails from [GitHub](software.md#github) with [Google BigQuery](google.md#google-bigquery)

    <a id="image-all-github-commit-emails-repo-before-takedown-naughty"></a>
    <img src="https://raw.githubusercontent.com/cirosantilli/media/master/All_GitHub_commit_emails_repo_screenshot_before_takedown_archive_is.png" alt="" height="768">

    **[Figure 2](#image-all-github-commit-emails-repo-before-takedown-naughty). All GitHub Commit Emails repo before takedown**. Screenshot from [archive.is](website.md#archive-today).
  - [A repository with 1 million commits](https://github.com/cirosantilli/test-many-commits-1m/): likely the [live repo with the most commits as of 2017](https://www.quora.com/Which-GitHub-repo-has-the-most-commits/answer/Ciro-SantilliI)
  - [An 100 year GitHub streak](https://stackoverflow.com/questions/20099235/who-is-the-user-with-the-longest-streak-on-github/27742165#27742165), likely longest ever when that existed. It was consuming too much [server](computer.md#server-computing) resources however, which led to GitHub admins manually [turning off his contribution history](https://web.archive.org/web/20151021135921/https://github.com/cirosantilli/).

    <a id="image-screenshot-of-ciro-santilli-s-github-profile-with-an-100-year-streak-visible"></a>
    ![](https://web.archive.org/web/20210703060931im_/https://i.stack.imgur.com/dckHn.png)

    **[Figure 3](#image-screenshot-of-ciro-santilli-s-github-profile-with-an-100-year-streak-visible). Screenshot of Ciro Santilli's GitHub profile with an 100 year streak visible**. [Source](https://stackoverflow.com/questions/20099235/who-is-the-user-with-the-longest-streak-on-github).
  - [A repository with a 100k commit Git octopus merge](https://github.com/cirosantilli/test-octopus-100k). Now that is a true [Cthulhu merge](https://softwareengineering.stackexchange.com/questions/314215/can-a-git-commit-have-more-than-2-parents/377903#377903).

    <a id="image-screenshot-of-a-commit-with-100k-parents-on-github"></a>
    ![](https://raw.githubusercontent.com/cirosantilli/media/refs/heads/master/github.com_cirosantilli_test-octopus-100k_commit_07fdcceb20ac3626a07c08166d0c410707b1cb9b_arrow.png)

    **[Figure 4](#image-screenshot-of-a-commit-with-100k-parents-on-github). Screenshot of a commit with 100k parents on GitHub**. URL: [https://github.com/cirosantilli/test-octopus-100k/commit/07fdcceb20ac3626a07c08166d0c410707b1cb9b](https://github.com/cirosantilli/test-octopus-100k/commit/07fdcceb20ac3626a07c08166d0c410707b1cb9b)
  - [500 on adoc infinite header xref recursion](https://github.com/isaacs/github/issues/1718): that was fun while it lasted

Outside this website:
- [https://cirosantilli.com/china-dictatorship/zhihu-censorship-of-hao-haidong](https://cirosantilli.com/china-dictatorship/zhihu-censorship-of-hao-haidong)

### All GitHub Commit Emails

↑ **Parent:** [Ciro Santilli's naughty projects](#ciro-santilli-s-naughty-projects)  
🏷️ **Tags:** [Ciro Santilli's data projects](#ciro-santilli-s-data-projects), [Open-source intelligence](science.md#open-source-intelligence)

[https://github.com/cirosantilli/all-github-commit-emails](https://github.com/cirosantilli/all-github-commit-emails)

In this project [Ciro Santilli](ciro-santilli.md) extracted (almost) all Git commit emails from [GitHub](software.md#github) with [Google BigQuery](google.md#google-bigquery)! The repo was later taken down by [GitHub](software.md#github). Newbs, censoring publicly available data!

Ciro also created a beautifully named variant with one email per commit: [https://github.com/cirosantilli/imagine-all-the-people](https://github.com/cirosantilli/imagine-all-the-people). True art. It also had the effect of breaking this "what's my first commit tracker": [https://twitter.com/NachoSoto/status/1761873362706698469](https://twitter.com/NachoSoto/status/1761873362706698469)

<a id="image-github-archive-query-showing-hashed-emails"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/GitHub_Archive_Google_bigquery_PushEvent_email_highlight.png" alt="" height="810">

**[Figure 5](#image-github-archive-query-showing-hashed-emails). GitHub Archive query showing hashed emails**. It was [Ciro Santilli](ciro-santilli.md) that made them hash the emails. They weren't hashed before he published the emails publicly.

<a id="image-all-github-commit-emails-repo-before-takedown"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/All_GitHub_commit_emails_repo_screenshot_before_takedown_archive_is.png" alt="" height="768">

**[Figure 6](#image-all-github-commit-emails-repo-before-takedown). All GitHub Commit Emails repo before takedown**. Screenshot from [archive.is](website.md#archive-today).

### Facebook profile face dump

↑ **Parent:** [Ciro Santilli's naughty projects](#ciro-santilli-s-naughty-projects)  
🏷️ **Tags:** [Ciro Santilli's data projects](#ciro-santilli-s-data-projects)

In 2016 Ciro made a script downloaded [Facebook](social-technology.md#facebook) profile pictures.

This was possible at the time without any login by using a 2010 profile ID dump from originally announced at: [https://blog.skullsecurity.org/2010/return-of-the-facebook-snatchers](https://blog.skullsecurity.org/2010/return-of-the-facebook-snatchers) since profile picture access was not authenticated.

The profile ID dump was downloadable through a [BitTorrent](software.md#bittorrent) named `fbdata.torrent` of about 2.8GB, mostly compressed. Doing:
```
find . -type f | xargs sha256sum | sha256sum
```
on Ubuntu 20.04 gives:
```
2c9a739c9c5495e38ebab81fc67411b7c6562f139dcb8619901a3f01230efdd5
```
This dump widely reported e.g. on [Hacker News](website.md#hacker-news) at: [https://news.ycombinator.com/item?id=1554558](https://news.ycombinator.com/item?id=1554558).

At some point however, Facebook finally started to require tokens to view public profile pictures, thus making such further collection impossible, e.g. as of 2021: [https://developers.facebook.com/docs/graph-api/reference/v9.0/user/picture](https://developers.facebook.com/docs/graph-api/reference/v9.0/user/picture) mentions:

> Querying a User ID (UID) now requires an access token.

This is also mentioned e.g. at: [https://stackoverflow.com/questions/11442442/get-user-profile-picture-by-id](https://stackoverflow.com/questions/11442442/get-user-profile-picture-by-id). This major privacy flaw was therefore finally addressed at some point, making it impossible to reproduce this project.

Ciro downloaded 10 thousand of those pictures, and did facial extraction with: [https://stackoverflow.com/questions/13211745/detect-face-then-autocrop-pictures/37501314#37501314](https://stackoverflow.com/questions/13211745/detect-face-then-autocrop-pictures/37501314#37501314)

He then created single a video by joining 10 thousand of those cropped faces which can be uploaded e.g. to [YouTube](website.md#youtube). Ciro later decided it was better to make those videos private however, as sooner later he'd lose his account for it.

[Companies](company.md) like [YouTube](website.md#youtube) blocking this kind of content is the type of thing that makes companies take longer to fix such gaping privacy issues, and is a bit like [security through obscurity](software.md#security-through-obscurity). A video makes it clear to everyone that there is a privacy issue very effectively. But people prefer to hide and look away, and then 99% of people who know nothing about tech get their privacy busted by actual criminals/government spies and never learn about it.

But now that Facebook finally fixed it, it's fine, no need for the video anymore.

<h2 id="ciro-santilli-s-data-projects">Ciro Santilli's data projects</h2>

↑ **Parent:** [Ciro Santilli's projects](ciro-santilli-s-projects.md)

[Ciro Santilli](ciro-santilli.md) has enjoyed doing projects dealing with with lots of data! They usually have a large overlap with [Ciro Santilli's naughty projects](#ciro-santilli-s-naughty-projects), but not always!

### Wikipedia CatTree

↑ **Parent:** [Ciro Santilli's data projects](#ciro-santilli-s-data-projects)  
🏷️ **Tags:** [Ciro Santilli's minor projects](the-most-important-projects-done-by-ciro-santilli.md#ciro-santilli-s-minor-projects)

This mini-project walks the category hierarchy [Wikipedia dumps](website.md#wikipedia-dumps) and dumps them in various simple formats, [HTML](web-technology.md#html) being the most interesting!
- [HTML](web-technology.md#html) dumps: [https://cirosantilli.com/wikipedia-cattree/](https://cirosantilli.com/wikipedia-cattree/)
- methodology: [https://stackoverflow.com/questions/17432254/wikipedia-category-hierarchy-from-dumps/77313490#77313490](https://stackoverflow.com/questions/17432254/wikipedia-category-hierarchy-from-dumps/77313490#77313490)

Scripts used:
- [wikipedia/import-sqlite.sh](wikipedia/import-sqlite.sh)
- [wikipedia/sqlite_preorder.py](wikipedia/sqlite_preorder.py)
- [wikipedia/wikipedia-cattree.sh](wikipedia/wikipedia-cattree.sh)

<a id="image-mathematics-dump-of-wikipedia-cattree"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master//Wikipedia_CatTree.png" alt="" height="500">

**[Figure 7](#image-mathematics-dump-of-wikipedia-cattree). Mathematics dump of Wikipedia CatTree**. [Source](https://cirosantilli.com/wikipedia-cattree/Mathematics).

<h2 id="ciro-santilli-s-open-source-contributions">Ciro Santilli's open source contributions</h2>

↑ **Parent:** [Ciro Santilli's projects](ciro-santilli-s-projects.md)

[This section is present in another page, follow this link to view it.](ciro-santilli-s-open-source-contributions.md)

## ↑ Ancestors (2)

1. [Ciro Santilli](ciro-santilli.md)
2. [Ciro Santilli's Homepage](README.md)
