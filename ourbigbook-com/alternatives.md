# Alternatives

↑ **Parent:** [OurBigBook.com](../ourbigbook-com-split.md)

These are websites that offer somewhat overlapping services, many of which served inspirations, and why we think something different is needed to achieve our goals.

Notably, OurBigBook is the result of [Ciro Santilli](../ciro-santilli-split.md)'s experiences with:
- [Wikipedia](wikipedia.md)
- [GitHub](github.md)
- [Stack Exchange](stack-exchange.md) (or as non techies might point out, [Urban Dictionary](../urban-dictionary.md), or [Quora](../quora.md) before it was such an incomprehensible shitshow)
OurBigBook could be seen as a cross between those three websites.

Quick mentions:
- [https://handwiki.org/wiki/HandWiki:About](https://handwiki.org/wiki/HandWiki:About): technically the same as [Wikipedia](wikipedia.md), but with more aligned moderation policies
- [https://ecotext.co/](https://ecotext.co/) similar goals. Their website seems quite broken now though as of 2021, can't see text properly. Crunchbase entry: [https://www.crunchbase.com/organization/ecotext](https://www.crunchbase.com/organization/ecotext) says they are from Durham, New Hampshire, United States. Cannot see how to publish, curated material only? Twitter: [https://twitter.com/ecotextinc?lang=en](https://twitter.com/ecotextinc?lang=en) One of the founders: [https://twitter.com/BigNel_21](https://twitter.com/BigNel_21) | [https://www.linkedin.com/in/ecotextnelsonthomas/](https://www.linkedin.com/in/ecotextnelsonthomas/). Their LinkedIn: [https://www.linkedin.com/company/ecotext/people/](https://www.linkedin.com/company/ecotext/people/)
- [https://fiveable.me/](https://fiveable.me/) bad: separates students and teachers, as a student I don't see where to create my content. Good: focus on teaching university level stuff to people outside of university via [Advanced Placement](../advanced-placement.md). Bad: Lots of video content. Bad: Can't see the issue tracker attached to each page.
- [LessWrong](../lesswrong.md): their website system does have some similar feature sets to what we want. Reputation, Q&A sections, links between articles most likely, sort by upvote everywhere.
- [https://crowdpub.org](https://crowdpub.org) collaborative writing website, somehow goes to paragraph level, TODO how they reconcile different authors? Closed beta as of writing, so hard to be sure. From quick presentation on beta website, appears to attempt to share revenue to authors proportionally to the size of their contribution. Some [blockchain](../blockchain.md)-based reputation. Meh.
- TODO migrate all from: [https://github.com/booktree/booktree/blob/master/alternatives.md](https://github.com/booktree/booktree/blob/master/alternatives.md)
- [https://studynotes.ie/](https://studynotes.ie/). Admin approval on everything. No ToC. Fixed tag list for [university entry exams](../university-entry-exam.md) topics.
- [https://mindstone.com](https://mindstone.com): there appears to be no sharing focus? File upload basesd? Not sure.
- [EverybodyWiki](../everybodywiki.md)
- looking for [open source](../open-source-software.md) [Confluence](../confluence-software.md)-alternatives is an interesting way to go:
  - lists:
    - [https://opensource.com/article/20/9/open-source-alternatives-confluence](https://opensource.com/article/20/9/open-source-alternatives-confluence)
    - [https://www.nuclino.com/alternatives/confluence-alternative#ynaw](https://www.nuclino.com/alternatives/confluence-alternative#ynaw)
  - [BookStack](../bookstack.md):
    - fixed 3-level page hierarchy
    - writen in [PHP](../php.md)
    - [Markdown](../markdown.md) support: [https://www.bookstackapp.com/docs/user/markdown-editor/](https://www.bookstackapp.com/docs/user/markdown-editor/)
    - no source-level import-export apparently: [https://www.bookstackapp.com/docs/admin/backup-restore/](https://www.bookstackapp.com/docs/admin/backup-restore/), [https://youtu.be/WUvtzJfCAKE?t=904](https://youtu.be/WUvtzJfCAKE?t=904)
    - [WYSIWYG](../wysiwyg.md): [https://www.bookstackapp.com/docs/user/wysiwyg-editor/](https://www.bookstackapp.com/docs/user/wysiwyg-editor/) via [TinyMCE](../tinymce.md)
    - page content repeating: [https://www.bookstackapp.com/docs/user/reusing-page-content/](https://www.bookstackapp.com/docs/user/reusing-page-content/) (will be useful for course modelling)
- [https://github.com/shuding/nextra](https://github.com/shuding/nextra) converts [Markdown](../markdown.md) links to Next.js links. We should look into how it works.
- [https://zettelkasten.de/the-archive/](https://zettelkasten.de/the-archive/) "The Archive" from zettelkasten.de/. Closed source. By German software engineer Christian Tietze [https://twitter.com/ctietze?lang=en](https://twitter.com/ctietze?lang=en)
- [LLM generated wiki](../llm-generated-wiki.md) e.g.:
  - [Kinnu](../kinnu.md)
- [https://docs.tigyog.app/cli](https://docs.tigyog.app/cli) beautiful website, but doesn't achieve much. Has a Markdown upload mechanism. Ah, those newbs who think the average user will care about markup upload to DB... Oh, wait...
- [https://www.stuvia.com/en-gb/school/uk/oxford-university/physics](https://www.stuvia.com/en-gb/school/uk/oxford-university/physics). PDF uploads. In theory you have to own copyright: [https://www.stuvia.com/en-gb/copyright/guidelines](https://www.stuvia.com/en-gb/copyright/guidelines) but it feels unlikely that most material was uploaded by the copyright owners. If those people are up, then why can't we? Maybe... Registred in the UK. People: some Dutch dudes:
  - [https://www.linkedin.com/in/jaapvannes](https://www.linkedin.com/in/jaapvannes)
  - [https://www.linkedin.com/in/hugo-kuijzer-bb81a625](https://www.linkedin.com/in/hugo-kuijzer-bb81a625)
- [Project Xanadu](../project-xanadu.md): crazy overlaps, though that project is [vaporware](../vaporware.md) apparently?> Administrators of Project Xanadu have declared it superior to the World Wide Web, with the mission statement: "Today's popular software simulates paper. The World Wide Web (another imitation of paper) trivialises our original hypertext model with one-way ever-breaking links and no management of version or contents.

[Static website](../static-website.md)-only alternatives:
- [https://quarto.org/](https://quarto.org/)
  - Links have forced file scope:[https://quarto.org/docs/websites/#linking](https://quarto.org/docs/websites/#linking)
    ```
    [about](about.qmd)
    [about](about.qmd#section)
    ```
  - [WYSIWYG](../wysiwyg.md) via [RStudio](https://ourbigbook.com/-/topic/rstudio)
- [https://vitepress.dev](https://vitepress.dev). [https://vitepress.dev/guide/markdown](https://vitepress.dev/guide/markdown) unmanaged internal links. Sample website: [https://wiki.nikiv.dev/](https://wiki.nikiv.dev/).

Conceptual:
- [The Final Encyclopedia](../the-final-encyclopedia-paul-allen.md): [science fiction](../science-fiction.md) concept, but the name was reused by [Paul Allen](../paul-allen.md) in a research project
- [second brain](../second-brain.md)
- [collective intelligence](../collective-intelligence.md)

TODO:
- [https://pressbooks.directory/](https://pressbooks.directory/)

**Table of contents**

- [Wikipedia](wikipedia.md)
- [Stack Exchange](stack-exchange.md)
- [Blogs](blogs.md)
- [University lecture notes](university-lecture-notes.md)
  - [How to convince teachers to use CC BY-SA](how-to-convince-teachers-to-use-cc-by-sa.md)
- [Existing data sources](existing-data-sources.md)
- [Personal knowledge base software](personal-knowledge-base-software.md)
- [Knowledge graph editors](knowledge-graph-editors.md)
- [Learning management systems](learning-management-systems.md)
- [GitHub](github.md)
- [Other projects](other-projects.md)

## ↑ Ancestors (6)

1. [OurBigBook.com](../ourbigbook-com-split.md)
2. [OurBigBook Web](../ourbigbook-web.md)
3. [OurBigBook](../ourbigbook.md)
4. [Ciro Santilli's projects](../ciro-santilli-s-projects-split.md)
5. [Ciro Santilli](../ciro-santilli-split.md)
6. [Ciro Santilli's Homepage](../split.md)

## ← Incoming links (1)

- [OurBigBook.com vs X](../aratu-week-2024-talk-by-ciro-santilli/ourbigbook-com-vs-x.md)
