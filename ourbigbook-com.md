# OurBigBook.com

↑ **Parent:** [OurBigBook Web](ciro-santilli-s-projects.md#ourbigbook-web)  
🏷️ **Tags:** [Personal knowledge base software](#personal-knowledge-base-software), [Personal knowledge base software](brain.md#personal-knowledge-base-software), [The most important projects Ciro Santilli wants to do](todo.md)

[https://ourbigbook.com](https://ourbigbook.com) is a [website](website.md) created by [Ciro Santilli](ciro-santilli.md).

The website is the reference instance of [OurBigBook Web](ciro-santilli-s-projects.md#ourbigbook-web), which is part of the [OurBigBook Project](ciro-santilli-s-projects.md#ourbigbook), the other main part of the project are software that users can run locally to publish their content such as the [OurBigBook CLI](ciro-santilli-s-projects.md#ourbigbook-cli).

The source code for ourbigbook.com is present at: [https://github.com/ourbigbook/ourbigbook/tree/master/web](https://github.com/ourbigbook/ourbigbook/tree/master/web)

The project documentation is present at: [https://docs.ourbigbook.com#ourbigbook-web-user-manual](https://docs.ourbigbook.com#ourbigbook-web-user-manual)

This page contains further information about the project's rationale, motivation and planning.

<a id="video-intro-to-the-ourbigbook-project"></a>
**[Video 1](#video-intro-to-the-ourbigbook-project). Intro to the OurBigBook Project.** [Source](https://www.youtube.com/watch?v=7JOJYx0mmhg).

<a id="image-the-topics-feature-allows-you-to-find-the-best-version-of-a-subject-written-by-other-users-user"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/topics/derivative.png" alt="" height="1000">

**[Figure 1](#image-the-topics-feature-allows-you-to-find-the-best-version-of-a-subject-written-by-other-users-user). The topics feature allows you to find the best version of a subject written by other users user**. Live demo: [derivative](https://ourbigbook.com/-/topic/derivative).

<a id="image-take-a-look-at-my-github-there-are-great-projects"></a>
<img src="https://web.archive.org/web/20240307065717im_/https://devhumor.com/content/uploads/images/February2024/my_great_projects_github_meme.jpg" alt="" height="500">

**[Figure 2](#image-take-a-look-at-my-github-there-are-great-projects). Take a look at my GitHub, there are great projects!** [OurBigBook](ciro-santilli-s-projects.md#ourbigbook)'s weird specialization towards the weird overly niche interests of its creator [Ciro Santilli](ciro-santilli.md), notably "I want to create the perfect documentation for every atom in the universe, is undoubtedly partly to blame for the project's failure to gain even a single user outside of its own creator.

However, Ciro does also believe that innovation requires to some degree specializing weirdly in some niche direction. Success comes perhaps from both going into a novel and valuable direction, while still being anatomic enough for enough people.

---

**Table of contents**

- [How the website works](#how-the-website-works)
- [Alternatives](#alternatives)
  - [Wikipedia](#wikipedia)
  - [Stack Exchange](#stack-exchange)
  - [Blogs](#blogs)
  - [University lecture notes](#university-lecture-notes)
    - [How to convince teachers to use CC BY-SA](#how-to-convince-teachers-to-use-cc-by-sa)
  - [Existing data sources](#existing-data-sources)
  - [Personal knowledge base software](#personal-knowledge-base-software)
  - [Knowledge graph editors](#knowledge-graph-editors)
  - [Learning management systems](#learning-management-systems)
  - [GitHub](#github)
  - [Other projects](#other-projects)
- [Action plan](#action-plan)
- [Philosophy](#philosophy)
  - [Desired social impact](#desired-social-impact)
  - [Motivation](#motivation)
  - [Manifesto](#manifesto)
- [Feature ideas](#feature-ideas)
  - [PageRank-like ranking](#pagerank-like-ranking)
- [User acquisition](#user-acquisition)
- [Funding](#funding)
  - [Why it is hard to make money from this website](#why-it-is-hard-to-make-money-from-this-website)
  - [Crowdfunding](#crowdfunding)
  - [Charitable grant opportunities](#charitable-grant-opportunities)
  - [Consulting](#consulting)
  - [Knowledge market](#knowledge-market)
  - [Advertisement](#advertisement)
  - [Association with innovative schools](#association-with-innovative-schools)
  - [Venture capital](#venture-capital)

## How the website works

↑ **Parent:** [OurBigBook.com](ourbigbook-com.md)

See: [https://docs.ourbigbook.com/#ourbigbook-web-user-manual](https://docs.ourbigbook.com/#ourbigbook-web-user-manual)

## Alternatives

↑ **Parent:** [OurBigBook.com](ourbigbook-com.md)

These are websites that offer somewhat overlapping services, many of which served inspirations, and why we think something different is needed to achieve our goals.

Notably, OurBigBook is the result of [Ciro Santilli](ciro-santilli.md)'s experiences with:
- [Wikipedia](#wikipedia)
- [GitHub](#github)
- [Stack Exchange](#stack-exchange) (or as non techies might point out, [Urban Dictionary](linguistics.md#urban-dictionary), or [Quora](website.md#quora) before it was such an incomprehensible shitshow)
OurBigBook could be seen as a cross between those three websites.

Quick mentions:
- [https://handwiki.org/wiki/HandWiki:About](https://handwiki.org/wiki/HandWiki:About): technically the same as [Wikipedia](#wikipedia), but with more aligned moderation policies
- [https://ecotext.co/](https://ecotext.co/) similar goals. Their website seems quite broken now though as of 2021, can't see text properly. Crunchbase entry: [https://www.crunchbase.com/organization/ecotext](https://www.crunchbase.com/organization/ecotext) says they are from Durham, New Hampshire, United States. Cannot see how to publish, curated material only? Twitter: [https://twitter.com/ecotextinc?lang=en](https://twitter.com/ecotextinc?lang=en) One of the founders: [https://twitter.com/BigNel_21](https://twitter.com/BigNel_21) | [https://www.linkedin.com/in/ecotextnelsonthomas/](https://www.linkedin.com/in/ecotextnelsonthomas/). Their LinkedIn: [https://www.linkedin.com/company/ecotext/people/](https://www.linkedin.com/company/ecotext/people/)
- [https://fiveable.me/](https://fiveable.me/) bad: separates students and teachers, as a student I don't see where to create my content. Good: focus on teaching university level stuff to people outside of university via [Advanced Placement](cirism.md#advanced-placement). Bad: Lots of video content. Bad: Can't see the issue tracker attached to each page.
- [LessWrong](website.md#lesswrong): their website system does have some similar feature sets to what we want. Reputation, Q&A sections, links between articles most likely, sort by upvote everywhere.
- [https://crowdpub.org](https://crowdpub.org) collaborative writing website, somehow goes to paragraph level, TODO how they reconcile different authors? Closed beta as of writing, so hard to be sure. From quick presentation on beta website, appears to attempt to share revenue to authors proportionally to the size of their contribution. Some [blockchain](social-technology.md#blockchain)-based reputation. Meh.
- TODO migrate all from: [https://github.com/booktree/booktree/blob/master/alternatives.md](https://github.com/booktree/booktree/blob/master/alternatives.md)
- [https://studynotes.ie/](https://studynotes.ie/). Admin approval on everything. No ToC. Fixed tag list for [university entry exams](university.md#university-entry-exam) topics.
- [https://mindstone.com](https://mindstone.com): there appears to be no sharing focus? File upload basesd? Not sure.
- [EverybodyWiki](website.md#everybodywiki)
- looking for [open source](software.md#open-source-software) [Confluence](website.md#confluence-software)-alternatives is an interesting way to go:
  - lists:
    - [https://opensource.com/article/20/9/open-source-alternatives-confluence](https://opensource.com/article/20/9/open-source-alternatives-confluence)
    - [https://www.nuclino.com/alternatives/confluence-alternative#ynaw](https://www.nuclino.com/alternatives/confluence-alternative#ynaw)
  - [BookStack](website.md#bookstack):
    - fixed 3-level page hierarchy
    - writen in [PHP](programming-language.md#php)
    - [Markdown](computer.md#markdown) support: [https://www.bookstackapp.com/docs/user/markdown-editor/](https://www.bookstackapp.com/docs/user/markdown-editor/)
    - no source-level import-export apparently: [https://www.bookstackapp.com/docs/admin/backup-restore/](https://www.bookstackapp.com/docs/admin/backup-restore/), [https://youtu.be/WUvtzJfCAKE?t=904](https://youtu.be/WUvtzJfCAKE?t=904)
    - [WYSIWYG](software.md#wysiwyg): [https://www.bookstackapp.com/docs/user/wysiwyg-editor/](https://www.bookstackapp.com/docs/user/wysiwyg-editor/) via [TinyMCE](software.md#tinymce)
    - page content repeating: [https://www.bookstackapp.com/docs/user/reusing-page-content/](https://www.bookstackapp.com/docs/user/reusing-page-content/) (will be useful for course modelling)
- [https://github.com/shuding/nextra](https://github.com/shuding/nextra) converts [Markdown](computer.md#markdown) links to Next.js links. We should look into how it works.
- [https://zettelkasten.de/the-archive/](https://zettelkasten.de/the-archive/) "The Archive" from zettelkasten.de/. Closed source. By German software engineer Christian Tietze [https://twitter.com/ctietze?lang=en](https://twitter.com/ctietze?lang=en)
- [LLM generated wiki](website.md#llm-generated-wiki) e.g.:
  - [Kinnu](website.md#kinnu)
- [https://docs.tigyog.app/cli](https://docs.tigyog.app/cli) beautiful website, but doesn't achieve much. Has a Markdown upload mechanism. Ah, those newbs who think the average user will care about markup upload to DB... Oh, wait...
- [https://www.stuvia.com/en-gb/school/uk/oxford-university/physics](https://www.stuvia.com/en-gb/school/uk/oxford-university/physics). PDF uploads. In theory you have to own copyright: [https://www.stuvia.com/en-gb/copyright/guidelines](https://www.stuvia.com/en-gb/copyright/guidelines) but it feels unlikely that most material was uploaded by the copyright owners. If those people are up, then why can't we? Maybe... Registred in the UK. People: some Dutch dudes:
  - [https://www.linkedin.com/in/jaapvannes](https://www.linkedin.com/in/jaapvannes)
  - [https://www.linkedin.com/in/hugo-kuijzer-bb81a625](https://www.linkedin.com/in/hugo-kuijzer-bb81a625)
- [Project Xanadu](brain.md#project-xanadu): crazy overlaps, though that project is [vaporware](computer.md#vaporware) apparently?> Administrators of Project Xanadu have declared it superior to the World Wide Web, with the mission statement: "Today's popular software simulates paper. The World Wide Web (another imitation of paper) trivialises our original hypertext model with one-way ever-breaking links and no management of version or contents.

[Static website](website.md#static-website)-only alternatives:
- [https://quarto.org/](https://quarto.org/)
  - Links have forced file scope:[https://quarto.org/docs/websites/#linking](https://quarto.org/docs/websites/#linking)
    ```
    [about](about.qmd)
    [about](about.qmd#section)
    ```
  - [WYSIWYG](software.md#wysiwyg) via [RStudio](https://ourbigbook.com/-/topic/rstudio)
- [https://vitepress.dev](https://vitepress.dev). [https://vitepress.dev/guide/markdown](https://vitepress.dev/guide/markdown) unmanaged internal links. Sample website: [https://wiki.nikiv.dev/](https://wiki.nikiv.dev/).

Conceptual:
- [The Final Encyclopedia](literature.md#the-final-encyclopedia-paul-allen): [science fiction](literature.md#science-fiction) concept, but the name was reused by [Paul Allen](microsoft.md#paul-allen) in a research project
- [second brain](brain.md#second-brain)
- [collective intelligence](brain.md#collective-intelligence)

TODO:
- [https://pressbooks.directory/](https://pressbooks.directory/)

### Wikipedia

↑ **Parent:** [Alternatives](#alternatives)

- you don't get any/sufficient recognition for your contributions. The closest they have to upvotes and reputation is the incredibly obscure "thank" feature which is only visible to the receiver itself: [https://en.wikipedia.org/wiki/Help:Notifications/Thanks](https://en.wikipedia.org/wiki/Help:Notifications/Thanks)
- [deletionism](website.md#deletionism) is a tremendous problem on Wikipedia, for two main causes:
  - tutorial-like subjectivity
  - notability
  The stuff you wrote can be deleted anytime by some random admin/opposing editor, examples at: [Section "Deletionism on Wikipedia"](website.md#deletionism-on-wikipedia).

  This also possibly leads to [edit wars](website.md#edit-war) in the case of sub-page content (full page deletion is more clearly arbitrated).
- Scope too limited, and politics defined. Everything has to sound encyclopedic and be notable enough. This basically excludes completely good tutorials.
- Insane impossible to use [markup language](computer.md#markup-language)-base talk pages instead of issue trackers?! Ridiculous!!! That change alone could make Wikipedia so much more amazing. Wikipedia could become a Stack Exchange killer by doing that alone + some basic reputation system. Some work on that is being done at: [https://www.mediawiki.org/wiki/Extension:DiscussionTools](https://www.mediawiki.org/wiki/Extension:DiscussionTools), already in Beta as of 2022.
- [Edit wars](website.md#edit-war)

### Stack Exchange

↑ **Parent:** [Alternatives](#alternatives)

[Stack Exchange](#stack-exchange) solves to a good extent the use  cases:
- I have a very specific question, type it on [Google](google.md), find top answers
- I have an answer, and I put it here because it has a much greater chance of being found due to the larger [PageRank](google.md#pagerank) than my [personal web page](website.md#personal-web-page) will ever have
points of view. It is a big open question if we can actually substantially improve it.

Major shortcoming are mentioned at [idiotic Stack Overflow policies](stack-overflow.md#bad-stack-overflow-policies):
- Scope restrictions can lead to a lot of content deletion: [closing questions as off-topic](stack-overflow.md#closing-questions-as-off-topic)
  - [closing questions as off-topic](stack-overflow.md#closing-questions-as-off-topic)
  - [Stack Overflow content deletion](stack-overflow.md#stack-overflow-content-deletion)
  - [Stack Overflow link-only answer policy](stack-overflow.md#stack-overflow-link-only-answer-policy)
  - [Stack Overflow no duplicate answers policy](stack-overflow.md#stack-overflow-no-duplicate-answers-policy)
  This greatly discourages new users, who might still have added value to the project.

  On our website, anyone can post anything that is legal in a given country. No one can ever delete your content if it is legal, no matter their reputation.
- Although you can answer your own question, there's no way to write an organized multi-page book with Stack Exchange due to shortcomings such as no table of contents, 30k max chars on answer, huge risk of deletion due to "too broad"
- Absolutely no algorithmic attempt to overcome the fastest gun in the West problem (early answers have huge advantage over newer ones): [https://meta.stackoverflow.com/questions/404535/closing-an-old-upvoted-question-as-duplicate-of-new-unvoted-questions/404567#404567](https://meta.stackoverflow.com/questions/404535/closing-an-old-upvoted-question-as-duplicate-of-new-unvoted-questions/404567#404567)
- Native reputation system:
  - if the living ultimate [God](religion.md#god) of `C++` upvotes you, you get `10` reputation
  - if the first-day newb of `Java` upvotes you, you also get `10` reputation
- Randomly split between sites like Stack Overflow vs Super User, with separate user reputations, but huge overlaps, and many questions that appears as dupes on both and never get merged.
- Possible edit wars, just like [Wikipedia](#wikipedia), but these are much less common since content ownership is much clearer than in Wikipedia however

Bibliography:
- [https://dev.to/codemouse92/has-stackoverflow-become-an-antipattern-3icb](https://dev.to/codemouse92/has-stackoverflow-become-an-antipattern-3icb) ([archive](http://web.archive.org/web/20191021090247/https://dev.to/codemouse92/has-stackoverflow-become-an-antipattern-3icb))

### Blogs

↑ **Parent:** [Alternatives](#alternatives)

Where [blog](website.md#blog) is taken in a wide sense, including e.g. [Medium](website.md#medium-website), [WordPress](website.md#wordpress), [Facebook](social-technology.md#facebook), [Twitter](social-technology.md#twitter), etc., etc.

The main shortcoming of blogs is the lack of topic convergence across blogs. Each blog is a moderated castle. So who is the best user for a given topic, or the best content for a given tag, across the entire website?

The only reasonable free material we have for advanced subjects nowadays are [university lecture notes](#university-lecture-notes).

While some of those are awesome, when writing a large content, no one can keep quality high across all sections, there will always be knowledge that you don't have which is enlightening. And [Googlers](google.md) are more often than not interested only in specific sections of your content.

Our website aims to make smaller subjects vertically curated across horizontal single author tutorials.

```
MIT calculus course             UCLA calculus course

* Calculus                <---> * Calculus
  * Limit                 <--->   * Limit
    * Limit of a function
    * Limit of a series   <--->     * Limit of a series
  * Derivative            <--->   * Derivative
                                    * L'Hôpital's rule
  * Integral              <--->   * Integral
```

Some more links:
- [https://prose.sh/](https://prose.sh/) multiblog, the only feature is easy of publishing from CLI

### University lecture notes

↑ **Parent:** [Alternatives](#alternatives)

Basically everything that applies to the [blogs](#blogs) section also applies here, but university lecture notes are so important to us that they deserve a bit more talk.

It is arguable that this is currently the best way to learn any university subject, and that it can already be used to learn any subject.

We basically just want to make the process more efficient and enjoyable, by making it easier:
- to find what you want based on an initial subject hit across the best version of any author
- and to publish your own stuff with one click, and get feedback if people like it or not, and improvement suggestions like you do you GitHub

One major problem with lecture notes is that, as the name suggests, they are merely a complement to the lecture, and don't contain enough detail for you to really learn solely from them without watching the lecture.

The only texts that generally teach in enough depth are actual books, which are almost always commercial.

So in a sense, this project can be seen as a path to upgrade free lecture notes into full blown free books, from which you can learn from scratch without any external material.

And a major way in which we believe this can be done is through the reuse of sections of lecture notes by from other universities, which greatly reduces the useless effort of writing things from scratch.

The intended mental picture is clear: the topics feature [https://docs.ourbigbook.com/#ourbigbook-web-topics](https://docs.ourbigbook.com/#ourbigbook-web-topics) will is intended to act as the missing horizontal topic integration across lecture notes of specific universities, e.g:

```
MIT calculus course             UCLA calculus course

* Calculus                <---> * Calculus
  * Limit                 <--->   * Limit
    * Limit of a function
    * Limit of a series   <--->     * Limit of a series
  * Derivative            <--->   * Derivative
                                    * L'Hôpital's rule
  * Integral              <--->   * Integral
```

<a id="image-example-topics-page-of-ourbigbook-com"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/Fundamental_theorem_of_calculus_topic_page.png" alt="" height="700">

**[Figure 3](#image-example-topics-page-of-ourbigbook-com). Example topics page of OurBigBook.com**.

One important advantage of lecture notes is that since they are written by the teacher, they should match exactly what "students are supposed to learn to get good grades", which [unfortunately is a major motivation for student's learning](cirism.md#students-must-have-a-flexible-choice-of-what-to-learn) weather we want it or not.

One big open question for this project is to what extent notes written for lectures at one university will be relevant to the lectures at another university?

Is it possible to write notes in a way that they are naturally reusable?

It is our gut feeling that this is possible. But it almost certainly requires an small intentional effort on the part of authors.

The question then becomes whether the "become famous by getting your content viewed in other universities" factor is strong enough to attract users.

And we believe that it might, it just might be.

#### How to convince teachers to use CC BY-SA

↑ **Parent:** [University lecture notes](#university-lecture-notes)

A major difficulty of getting such this to work is that may university teachers want to retain closed copyright of their work because they:
- want to publish a book later and get paid. Yes, the root problem is that teachers get paid way too little and have way too little job security for the incredibly important and difficult extremely difficult job they are doing, and we have to [vote](social-technology.md#voting) to change that
- are afraid that if amazing material is made freely available, then they would not be needed and lose their jobs.  Once again, job security issue.
- believe that if anyone were allowed to touch their precious content, those people would just "screw it up" and make it worse
- don't even want to publish their notes online because "someone will copy it and take their credit". What a mentality! In order to prevent a theft, you are basically guaranteeing that your work will be completely forgotten!
- don't want students to read the notes and skip class, because spoken word has magic properties and imparts knowledge that cannot otherwise conveyed by a book
- are afraid that mistakes will be found in their material. Reputation is of course everything in academia, since there is no money.

  So it's less risky to have closed, more buggy notes, than open, more correct ones.

  This can be seen clearly for example on [Physics Stack Exchange](stack-overflow.md#physics-stack-exchange), and most notably in [particle physics](particle-physics.md) (well, which is basically the only subject that really gets asked, since anything more experimental is going to be blocked off by patents/interlab competition), where a large proportion incredibly amazing users have anonymous profiles.

  They prefer to get no reputation gains from their amazing contributions, due to the fear that a single mistake will ruin their career.

  This is in stark contrast for example to [Stack Overflow](stack-overflow.md), where almost all top users are not anonymous:

  List of top users: [https://physics.stackexchange.com/users?tab=Reputation&filter=all](https://physics.stackexchange.com/users?tab=Reputation&filter=all) and some notable anonymous ones:
  - [https://physics.stackexchange.com/users/2451/qmechanic](https://physics.stackexchange.com/users/2451/qmechanic)
  - [https://physics.stackexchange.com/users/50583/acuriousmind](https://physics.stackexchange.com/users/50583/acuriousmind)
  - [https://physics.stackexchange.com/users/43351/profrob](https://physics.stackexchange.com/users/43351/profrob)
  - [https://physics.stackexchange.com/users/84967/accidentalfouriertransform](https://physics.stackexchange.com/users/84967/accidentalfouriertransform)
  - [https://physics.stackexchange.com/users/56997/curiousone](https://physics.stackexchange.com/users/56997/curiousone)
  - [https://physics.stackexchange.com/users/139781/probably-someone](https://physics.stackexchange.com/users/139781/probably-someone)
  - [https://physics.stackexchange.com/users/206691/chiral-anomaly](https://physics.stackexchange.com/users/206691/chiral-anomaly)

Therefore the only way is to find teachers who are:
- enlightened to use such licenses
- forced by their organizations to use such licenses
The forced option therefore seems like a more bulk efficient starting point for searches.

No matter how much effort a single person puts into writing perfect tutorials, they will never beat 1000x people + an algorithm.

It is not simply a matter of how much time you have. The fundamental reason is that each person has a different background and different skills. Notably the [young students have radically different understanding than that of the experienced teacher](cirism.md#there-is-value-in-tutorials-written-by-beginners).

Therefore, those that refuse to contribute to such platforms, or at least license their content with open licenses, will inevitably have their work forgotten in favor of those that have contributed to the more open platform, which will eventually dominate everything.

Perhaps [OurBigBook.com](ourbigbook-com.md) is not he killer platform that will make this happen. Perhaps the world is not yet ready for it. But Ciro believes that this will happen, sooner or later, inevitable, and he wants to give it a shot.

Also worth checking:
- [https://jornal.usp.br/universidade/usp-de-sao-carlos-oferece-aulas-de-graduacao-em-matematica-e-estatistica-abertas-ao-publico/](https://jornal.usp.br/universidade/usp-de-sao-carlos-oferece-aulas-de-graduacao-em-matematica-e-estatistica-abertas-ao-publico/) "Open Classroom" program from the [University of São Paulo](university.md#university-of-sao-paulo). We should Google for "Open Classroom" a bit more actually.
- [https://open.ed.ac.uk/about/](https://open.ed.ac.uk/about/): talk only

<a id="image-the-grad-student-brain-by-phd-comics-2010"></a>
<img src="https://web.archive.org/web/20220120132903if_/https://phdcomics.com/comics/archive/phd100610s.gif" alt="" height="500">

**[Figure 4](#image-the-grad-student-brain-by-phd-comics-2010). The Grad Student Brain by PhD Comics (2010)** [Source](https://phdcomics.com/comics/archive.php?comicid=1379). Convincing academics that their tutorial are not always perfect is one of blocking points to the acceptance of solutions such as [OurBigBook.com](ourbigbook-com.md). To thrive in the competition of academia, those people are amazing at publishing novel results. Explaining to beginners however, not necessarily so.

### Existing data sources

↑ **Parent:** [Alternatives](#alternatives)

Some possible/not possible sources that could be used to manually bootstrap content:
- [LibreTexts](social-technology.md#libretexts). Good project. "Teacher-only-content" unfortunately as usual. But besides that fundamental flaw, they do exactly what we want to do in a sense.
- [OpenStax](website.md#openstax): [CC BY](law.md#cc-by). This could be a great entry point, as they already have some university integration going on, and might be interested in this project.
- [https://physics.stackexchange.com/questions/6157/list-of-freely-available-physics-books](https://physics.stackexchange.com/questions/6157/list-of-freely-available-physics-books) "List of freely available physics books" explicitly asks for:> a list of physics books with open-source licenses, like Creative Commons, GPL

  but the thread [was locked](stack-overflow.md#closing-questions-as-off-topic), and basically none of the sources in the answers have free licenses, nor do they note it. It just seems that the [physicists](physicist.md) don't know what a [free license](law.md#free-license) is.
- [MIT OpenCourseWare](university.md#mit-opencourseware): [CC BY-NC-SA](law.md#cc-by-nc-sa), so not really usable
- [https://github.com/certik/theoretical-physics](https://github.com/certik/theoretical-physics): [MIT License](law.md#mit-license). [Workable](https://opensource.stackexchange.com/questions/324/are-permissive-licenses-mit-bsd-zlib-compatible-with-cc-by) but wonky.
- [https://subwiki.org/](https://subwiki.org/): [wiki](website.md#wiki) with some upper graduate [math](mathematics.md) subjects presumably by this [Indian](continent.md#india) dude: [https://www.linkedin.com/in/vipul-naik-0ab1898/](https://www.linkedin.com/in/vipul-naik-0ab1898/). Description on his homepage: [https://vipulnaik.com/subwiki/](https://vipulnaik.com/subwiki/). He's also got other interesting but not so relevant projects:
  - pro freer immigration laws: [https://vipulnaik.com/openborders/](https://vipulnaik.com/openborders/)
  - [https://vipulnaik.com/cognito-mentoring/](https://vipulnaik.com/cognito-mentoring/) free mentoring project for interested students

  He's also into [Stack Overflow](stack-overflow.md), [Quora](website.md#quora) and [Wikipedia](#wikipedia) editing. That's a cool dude. He's into in [LessWrong](website.md#lesswrong) it seems.
- massive [mathematics](mathematics.md) books
  - [Infinite Napkin](mathematics.md#infinite-napkin).[CC BY-SA](law.md#cc-by-sa) [mathematics](mathematics.md) infinite book: [https://github.com/vEnhance/napkin/issues/77](https://github.com/vEnhance/napkin/issues/77). Very similar type of content to what we want in this project!
  - [Stacks Project](mathematics.md#stacks-project)

Existing lecture notes by students:
- [https://github.com/mb2g17/NotesNetworkArchive](https://github.com/mb2g17/NotesNetworkArchive) [Google Docs](google.md#google-docs)-based: [https://docs.google.com/document/d/1OIcQ8dJ_FAhdkirU94M29-ZbNZ4oQs1LbWF3Nz-mq_U/edit#heading=h.vehxib58w1iw](https://docs.google.com/document/d/1OIcQ8dJ_FAhdkirU94M29-ZbNZ4oQs1LbWF3Nz-mq_U/edit#heading=h.vehxib58w1iw). An actual student uploading tons of lecture notes in one coherent system. [CC BY-NC-SA](law.md#cc-by-nc-sa) unfortunately.
- [https://academia.stackexchange.com/questions/148261/do-you-keep-your-study-notes-publicly-available](https://academia.stackexchange.com/questions/148261/do-you-keep-your-study-notes-publicly-available) mentions:
  - Cambridge Mathematics Lecture Notes by Dexter Chua (2014-2018)
    - [http://dec41.user.srcf.net/notes/](http://dec41.user.srcf.net/notes/)
    - [https://github.com/dalcde/cam-notes](https://github.com/dalcde/cam-notes)

    Comments:
    - on [Reddit](website.md#reddit): [https://www.reddit.com/r/math/comments/98wsoa/undergraduate_maths_lecture_notes_uni_of_cambridge/](https://www.reddit.com/r/math/comments/98wsoa/undergraduate_maths_lecture_notes_uni_of_cambridge/)  

  Related: [https://academia.stackexchange.com/questions/40381/how-common-is-it-that-professors-have-their-students-write-textbooks](https://academia.stackexchange.com/questions/40381/how-common-is-it-that-professors-have-their-students-write-textbooks)

Lecture note upload website:
- [https://nexusnotes.com](https://nexusnotes.com) likely illegal reuploads of PDFs from teachers
- [https://www.studocu.com/en-gb](https://www.studocu.com/en-gb) Paywall. PDF uploads. Unclear if simple teacher reuploads or actual novel notes.
- [https://www.studydrive.net/](https://www.studydrive.net/)
- Chinese GitHub repos. Some of these are very advanced in terms of content quantity and organizational quality! The Chinese are miles ahead in this area:
  - [https://github.com/PKUanonym/REKCARC-TSC-UHT](https://github.com/PKUanonym/REKCARC-TSC-UHT) Guidance for courses in Department of Computer Science and Technology, Tsinghua University. Chinese. Appears to try and store all past exams.
  - [https://github.com/lib-pku/libpku](https://github.com/lib-pku/libpku)
  - [https://github.com/openwhu/OpenWHU](https://github.com/openwhu/OpenWHU): Wuhan University
  - [https://github.com/USTC-Resource/USTC-Course](https://github.com/USTC-Resource/USTC-Course): USTC
  - [https://github.com/Zeal-L/UNSW](https://github.com/Zeal-L/UNSW): [UNSW](university.md#university-of-new-south-wales) from [Australia](continent.md#australia), but by a Chinese dude
  - [https://github.com/apachecn/mit-18.06-linalg-notes](https://github.com/apachecn/mit-18.06-linalg-notes): translation of [MIT](university.md#massachusetts-institute-of-technology) course to Chinese
  - [https://github.com/chenyang1999/MyComputerCollegeCourses](https://github.com/chenyang1999/MyComputerCollegeCourses): TODO which univeresity
  - [https://github.com/elder-frog/OpenCourseCatalog](https://github.com/elder-frog/OpenCourseCatalog): nothing to do with this project, but since I'm making a list, this dude is copying [YouTube](website.md#youtube) videos to [Bilibili](china.md#bilibili). And he's edgy anti-CCP on Twitter, what a legend.
  - [https://github.com/TheBloodthirster/BUAA_Course_Sharing](https://github.com/TheBloodthirster/BUAA_Course_Sharing): [https://en.wikipedia.org/wiki/Beihang_University](https://en.wikipedia.org/wiki/Beihang_University)
  - [https://github.com/1051727403/SHU-CS-Source-Share](https://github.com/1051727403/SHU-CS-Source-Share): ShangHai University CS course source code
  - [https://github.com/Willie169/tw-gifted-k12-notes](https://github.com/Willie169/tw-gifted-k12-notes): [Taiwanese](continent.md#taiwan) high school notes

Exams uploads:
- [https://questions.tripos.org/part-ib/all/](https://questions.tripos.org/part-ib/all/) [University of Cambridge](university-of-cambridge.md) Mathematics past examinations

### Personal knowledge base software

↑ **Parent:** [Alternatives](#alternatives)

### Knowledge graph editors

↑ **Parent:** [Alternatives](#alternatives)

A list of reviews of such systems is maintained at:
- [Section 2.6. "Personal knowledge base software"](#personal-knowledge-base-software)
- [Section "Markdown editor"](computer.md#markdown-editor)

This is the class of existing software the perhaps comes the closest to [OurBigBook](ciro-santilli-s-projects.md#ourbigbook), in particular systems such as:
- [Roam Research](brain.md#roam-research) and its [open source](software.md#open-source-software) clone [Foam](brain.md#foam-personal-knowledge-base)
- [Forester](brain.md#forester)

While we believe that [OurBigBook](ciro-santilli-s-projects.md#ourbigbook) can hold its own against most of them as a [personal knowledge base](brain.md#personal-knowledge-base), there is one feature which we believe truly distinguishes OurBigBook from all others in a big way: trustless mind meld with the [OurBigBook topic feature](ciro-santilli-s-projects.md#ourbigbook-topic-feature), which no other system seems to have.

Many such systems are also no publishing focused enough, and are more focused only in maintaining people's private knowledge bases. Some of them don't even have publishing at all, or its complicated. While publishing is optional in OurBigBook, it is a crucial feature and extremely well supported.

### Learning management systems

↑ **Parent:** [Alternatives](#alternatives)

This website basically aims to be a [learning management system](website.md#learning-management-system), allowing in particular a teacher to focus his help on students that he is legally obliged to help due to their job. But it will have the following unusual characteristics in current LMS solutions:
- public first, to allow reuse across universities, rather than paywalled as is the case for most top universities
- students can create material just like teachers, both are on equal footing. Students/teachers will see an indicator "this is your teacher"/"this is your student for this/past semester", but that is the only difference between their interfaces.

### GitHub

↑ **Parent:** [Alternatives](#alternatives)  
🏷️ **Tags:** [GitHub](#github)

If [Ciro Santilli](ciro-santilli.md) were to write a book about [quantum mechanics](quantum-mechanics.md) as of 2020 (before [OurBigBook.com](ourbigbook-com.md) went live), he would upload an [OurBigBook Markup](ciro-santilli-s-projects.md#ourbigbook-markup) website to [GitHub Pages](software.md#github-pages).

But there is one major problem with that: the entry barrier for new contributors is very large.

If they submit a pull request, Ciro has to review it, otherwise, no one will ever see it.

Our amazing website would allow the reader to add his own example of, say, The [uncertainty principle](quantum-mechanics.md#uncertainty-principle), whenever they wants, under the appropriate section.

Then, people who want to learn more about it, would click on the "defined tag" by the article, and our amazing analytics would point them to the best such articles.

### Other projects

↑ **Parent:** [Alternatives](#alternatives)

- [HyperCard](website.md#hypercard): we are kind of a "multiuser" version of HyperCard, trying to tie up cards made by different users. It is worth noting that [HyperCard](website.md#hypercard) was one of the inspirations for [WikiWikiWeb](website.md#wikiwikiweb), which then inspired [Wikipedia](#wikipedia)
- [Semantic Web](https://en.wikipedia.org/wiki/Semantic_Web)
- [NLab](website.md#nlab)
- [https://physicstravelguide.com/](https://physicstravelguide.com/) Nice manifesto: [https://physicstravelguide.com/about](https://physicstravelguide.com/about) by [Jakob Schwichtenberg](physicist.md#jakob-schwichtenberg).
- [OpenStax](website.md#openstax)
- [https://www.ft.com/content/5515ec3e-0040-4d90-85a9-df19d6e3ebd2](https://www.ft.com/content/5515ec3e-0040-4d90-85a9-df19d6e3ebd2) ([archive](https://archive.ph/nlr1h)) Twilio’s Jeff Lawson: an evangelist for software developers

  > As a student at the University of Michigan, he started a company that made lecture notes available free online, drawing a large audience of Midwestern college students and, soon enough, advertisers. At the height of the dotcom bubble, he dropped out of college, raised $10m from the venture firm Venrock and moved the company to Silicon Valley.
  > 
  > His start-up drew interest from an acquirer that was planning to go public early in 2000. They closed the acquisition but missed their IPO window as the market plunged, and by August the company had filed for bankruptcy. Stock that Lawson and investors in his start-up received from the sale became worthless.

  You can never be first. But you can have the correct business model. That company's website must have gone into [IP](law.md#intellectual-property) [Purgatory](religion.md#purgatory), and could never be released as an open source website.

  This project won't make a lot of [money](social-technology.md#money). [Open source](software.md#open-source-software) and [not-for-profit](social-technology.md#nonprofit-organization) seems like the way to go.

  The website was called [https://stubhub.com/](https://stubhub.com/), as of 2021 the domain had been sold to an unrelated website.

  He might actually be interested in donating to [OurBigBook.com](ourbigbook-com.md) if it move forward now that he's a billionaire.
- [Knol](google.md#knol): basically the exact same thing by [Google](google.md) but 14 years earlier and declared a failure. Quite ominous:> Any contributor could create and own new Knol articles, and there could be multiple articles on the same topic with each written by a different author.
- [leanpub](telecommunication.md#leanpub): similar goals, [markdown](computer.md#markdown)-based, but the usual "you own your book copyright and you are trying to sell your book" approach
- [nature Scitable](website.md#nature-scitable)

OK, just going random now:
- [https://twitter.com/jwmares/status/1136273581455958017](https://twitter.com/jwmares/status/1136273581455958017)

## Action plan

↑ **Parent:** [OurBigBook.com](ourbigbook-com.md)

The steps are sorted in roughly chronological order. The project might fail at any point, and some steps may be carried in parallel:
- make [OurBigBook Markup](ciro-santilli-s-projects.md#ourbigbook-markup) good enough, to the point that it allows to create a static version of the website, which is used to prototype certain ideas, and for Ciro to start writing test content.

  Status March 2022: reached a point that it is already highly usable. The following website may continue.
- create a basic implementation of the website, without advanced features like PageRank sorting and WYSIWYG. This is not much more than a blog with some extra metadata, so it is definitely achievable with constrained resources.
- find a university teacher would would like to try it out.

  Ciro would like to volunteer to work for free for this teacher and students to help the students learn.

  He would like act like a "super student" who has a lot of free time and motivation.

  Ciro would start by mapping the headers of the lecture notes onto the website, and then slowly adding content as he feels the need to improve certain explanations.

  Finding teachers willing to allow this will be a major roadblock: [how to convince teachers to use CC BY-SA](#how-to-convince-teachers-to-use-cc-by-sa).

  If such enlightened teacher is found, it will allow for the initial validation of the website, to decide what kind of tweaking the idea might need, and start uploading quality technical content to the site.
- once some level of validation as been done, Ciro will start looking for charitable [charitable grant opportunities](#charitable-grant-opportunities) more aggressively
- if things seem to be working, start adding more advance features: [PageRank-like ranking](#pagerank-like-ranking) sorting and WYSIWYG editing

  The recommendation algorithms notably is left for a second stage because it needs real world data to be tested. And at the beginning, before [Eternal September](website.md#eternal-september) kicks in, there would be few posts written by well educated university students, so a simple sort by upvote would likely be good enough.

Ciro decided to start with a decent [markup language](computer.md#markup-language) with a decent implementation: [OurBigBook Markup](ciro-santilli-s-projects.md#ourbigbook-markup). Once that gets reasonable, he will move on to another attempt at the website itself.

The project description was originally at: [https://github.com/cirosantilli/write-free-science-books-to-get-famous-website](https://github.com/cirosantilli/write-free-science-books-to-get-famous-website) but being migrated here. The original working project name was "Write free books to get famous website", until Ciro decided to settle for `OurBigBook.com` and fixed the domain name.

## Philosophy

↑ **Parent:** [OurBigBook.com](ourbigbook-com.md)

### Desired social impact

↑ **Parent:** [Philosophy](#philosophy)

Crush the current grossly inefficient educational system, replace today's students + teachers + researchers with unified "online content creators/consumers".

Gamify them, and pay the best creators so they can work it full time, until some company hires for more them since they are so provenly good.

Destroy useless [exams](education.md#exam), the only metrics of society are either:
- how much money you make
- how high is your educational content creator reputation score

Reduce the entry barrier to education, like Uber has done for taxis.

Help create much greater [equal opportunity](economy.md#equal-opportunity) to talented poor students as described at [free gifted education](cirism.md#free-gifted-education).

Give the students [a flexible choice of what to learn](cirism.md#students-must-have-a-flexible-choice-of-what-to-learn), which basically implies that a much large proportion of students get a de-facto [gifted education](education.md#gifted-education).

In some ways, Ciro wants the website to feel like a [video game](video-game.md), where you fluidly interact with headers, comments and their metadata. If game developers can achieve impressively complicated game engines, why can't we achieve a decent amazing elearning website? :-)

Related:
- [https://www.edsurge.com/news/2021-08-17-it-s-time-to-blur-the-boundaries-between-high-school-college-and-work](https://www.edsurge.com/news/2021-08-17-it-s-time-to-blur-the-boundaries-between-high-school-college-and-work)

### Motivation

↑ **Parent:** [Philosophy](#philosophy)

Many subjects have changed very little in the last hundred years, and so it is mind-blowing that people have to pay for books that teach them!

If [computers are bicycles for the mind](computer.md#video-a-computer-is-the-equivalent-of-a-bicycle-for-our-minds-by-steve-jobs-1980), Ciro wants this website to be the Ferrari of the mind.

Since [Ciro Santilli](ciro-santilli.md) was young, he has been bewildered by the natural sciences and mathematics [due to his bad memory](ciro-santilli-s-psychology-and-physiology.md#ciro-santilli-s-bad-old-event-memory).

The beauty of those subjects has always felt like intense sunlight in a fresh morning to Ciro. Sometimes it gets covered by clouds and obscured by less important things, but it always comes back again and again, weaker or stronger with its warmth, guiding Ciro's life path.

As a result, he has always suffered a lot at school: his grades were good, but he wasn't really learning those beautiful things that he wanted to learn!

School, instead of helping him, was just wasting his time with superficial knowledge.

First, before [university](university.md), school organization had only one goal: put you into the best universities, to make a poster out of you and get publicity, so that more parents will be willing to pay them [money](social-technology.md#money) to put their kids into good university.

Ciro once asked a [chemistry](chemistry.md) teacher some "deeper question" after course was over, related to the superficial vision of the topic they were learning to get grades in university entry [exams](education.md#exam). The teacher replied something like:

> You remind me of a friend of mine. He always wanted to understand the deeper reason for things. He now works at NASA.

Ciro feels that this was one of the greatest compliments he has ever received in his life. This teacher, understood him. Funny how some things stick, [while all the rest fades](ciro-santilli-s-psychology-and-physiology.md#ciro-santilli-s-bad-old-event-memory).

Another interesting anecdote is how [Ciro Santilli's mother](ciro-santilli.md#ciro-santilli-s-mother) recalls that she always found out about exams in the same way: when the phone started ringing as Ciro's friends started asking for help with the subjects just before the exam. Sometimes it was already too hopelessly late, but Ciro almost always tried. Nothing shows how much better you are than someone than teaching them.

Then, after entering university, although things got way better because were are able to learn things that are borderline useful.

Ciro still felt a strong emotion of nostalgia when after university his mother asked if she could throw away his high school books, and Ciro started tearing them all down for recycling. Such is life.

University teachers were still to a large extent researchers who didn't want to, know how to and above all have enough time and institutional freedom to teach things properly and make you see their beauty, some good relate articles:
- [The Purpose of Harvard is Not to Educate People by Sean Carroll (2008)](physicist.md#the-purpose-of-harvard-is-not-to-educate-people-by-sean-carroll-2008)
- [How To Get Tenure at a Major Research University by Sean Carroll (2011)](physicist.md#how-to-get-tenure-at-a-major-research-university-by-sean-carroll-2011)

The very fact that you had very little choice of what to learn so that a large group can get a "Diploma", makes it impossible for people to deeply learn what the really want.

This is especially true because Ciro was in [Brazil](brazil.md), a third world country, where the opportunities are comparatively extremely limited to the [first world](what-poor-countries-have-to-do-to-get-richer.md).

Also extremely frustrating is how you might have to wait for years to get to the subject you really want. For example, on a [physics](physics.md) course, [quantum mechanics](quantum-mechanics.md) is normally only taught on the third year! While there is value to knowing the pre-requisites, holding people back for years is just too sad, and Ciro much prefers [backward design](cirism.md#backward-design). And just like the university entry exams, this creates an entry barrier situation where you might in the end find that "hey, that's not what I wanted to learn after all", see also: [students must have a flexible choice of what to learn](cirism.md#students-must-have-a-flexible-choice-of-what-to-learn).

We've created a system where people just wait, and wait, and wait, never really doing what they really want. They wait through school to get into university. They wait through university to get to masters. They wait through masters to get to [PhD](education.md#doctor-of-philosophy). They wait through [PhD](education.md#doctor-of-philosophy) to become a PI. And for the minuscule fraction of those that make it, they become fund proposal writers. And if you make any wrong choice along the, it's all over, you can't continue anymore, the cost would be too great. So you just become software engineer or a consultant. Is this the society that we really want?

And all of this is considering that he was very lucky to not be in a poor family, and was already in some of the best educational institutions locally available already, and had comparatively awesome teachers, without which he wouldn't be where he is today if he hadn't had such advantages in the first place.

But no matter how awesome one teacher is, no single person can overcome a system so large and broken. Without technological innovation that is.

The key problem all along the way is the Society's/Government's belief that everyone has to learn the same things, and that grades in exams mean anything.

Ciro believes however, that [exams](education.md#exam) are useless, and that there are only two meaningful metrics:
- how much [money](social-technology.md#money) you make
- fame for doing for doing useful work for society without earning money, which notably includes creating new or better free knowledge such as in [academic papers](education.md#academic-paper), either novel or [review](education.md#review-article)

Even if you wanted to really learn natural sciences and had the time available, it is just too hard to find good resources to properly learn it. Even attending university courses are hit and miss between amazing and mediocre teachers.

If you go into a large book shop, the science section is tiny, and useless popular science books dominate it without [precise experiment descriptions](todo.md#videos-of-all-key-physics-experiments). And then, the only few "serious" books are a huge list of formulas without any experimental motivation.

And if you are lucky to have access to an university library that has open doors, most books are likely to be old and boring as well. [Googling](google.md) for [PDFs](computer.md#pdf) from university courses is the best bet.

Around 2012 however, he finally saw the light, and started his path to [Ciro Santilli's Open Source Enlightenment](ciro-santilli.md#ciro-santilli-s-open-source-enlightenment). University was not needed anymore. He could learn whatever he wanted. A vision was born.

To make things worse, for a long time he was tired of [seeing poor people begging on the streets every day and not doing anything about it](economy.md#social-inequality). He thought:

> He who teaches one thousand, saves one million.

which like everything else is likely derived subconsciously from something else, here [Schindler's list possibly adapted quote from the Talmud](https://en.wikiquote.org/wiki/Talmud):

> He who saves the life of one man saves the entire world.

So, by the time he left University, instead of pursuing a PhD in theoretical Mathematics or Physics just for the beauty of it as he had once considered, he had new plans.

We needed a new educational system. One that would allow people to fulfill their potential and desires, and truly [improve society as a result](cirism.md#universal-basic-income), both in rich and poor countries.

And he found out that programming and applied mathematics could also be fun, so he might as well have some fun while doing this! ;-)

So he started [Booktree](https://github.com/booktree/booktree) in 2014, a [GitLab](software.md#gitlab) fork, worked on it for an year, noticed the [approach was dumb](https://github.com/booktree/booktree/blob/master/blog/2015-01-why-ciro-stopped-working-on-booktree.md), and a few years later started building this new version. The repo [https://github.com/booktree/booktree](https://github.com/booktree/booktree) is a small snapshot of Ciro's 2014 brain on the area, there were quite a few similar projects at the time, and most have died.

Ciro is basically a librarian at heart, and wants to be the next:
- [Jimmy Wales](https://en.wikipedia.org/wiki/Jimmy_Wales)
- [Brewster Kahle](https://en.wikipedia.org/wiki/Brewster_Kahle)
- [Tim Berners Lee](https://en.wikipedia.org/wiki/Tim_Berners-Lee)
- [Tim O'Reilly](software.md#tim-o-reilly), who once brilliantly described [O'Reilly Media](telecommunication.md#o-reilly-media) as "a lifestyle business that got out of control" [https://www.inc.com/magazine/20100501/the-oracle-of-silicon-valley.html](https://www.inc.com/magazine/20100501/the-oracle-of-silicon-valley.html)
- [Aaron Swartz](software.md#aaron-swartz). Minus [suicide](brain.md#suicide) hopefully.

<a id="video-jimmy-wales-how-a-ragtag-band-created-wikipedia-2005-ted-conference-talk"></a>
**[Video 2](#video-jimmy-wales-how-a-ragtag-band-created-wikipedia-2005-ted-conference-talk). "Jimmy Wales: How a ragtag band created Wikipedia" 2005 TED talk.** [Source](https://youtube.com/watch?v=WQR0gx0QBZ4). Original source: [https://www.ted.com/talks/jimmy_wales_the_birth_of_wikipedia](https://www.ted.com/talks/jimmy_wales_the_birth_of_wikipedia).

<a id="video-brewster-kahle-a-digital-library-free-to-the-world-2007-ted-conference-talk"></a>
**[Video 3](#video-brewster-kahle-a-digital-library-free-to-the-world-2007-ted-conference-talk). "Brewster Kahle: A digital library, free to the world." 2007 TED Talk.** [Source](https://youtube.com/watch?v=pXoHC2D15hM). Talks about the [Internet Archive](website.md#internet-archive) which he created.

<a id="video-sal-khan-from-khan-academy-2016-ted-conference-talk"></a>
**[Video 4](#video-sal-khan-from-khan-academy-2016-ted-conference-talk). Sal Khan from Khan Academy 2016 TED talk.** [Source](https://www.youtube.com/watch?v=-MTRxRO5SRA). Ciro is not a big fan of the "basis on top of basis focus" because of his obsession with [backward design](cirism.md#backward-design), but "learn to mastery at your own pace" and "everyone can be a world class innovator" are obviously good.

### Manifesto

↑ **Parent:** [Philosophy](#philosophy)

Education has become an expensive bureaucratic exercise, completely dissociated from reality and usefulness.

It completely rejects what the individual wants to achieve, and instead attempts to mass homogenize and test people through endless hours of boredom.

And the only goals it achieves are testing student's resilience to stress, and facilitating the finding of sexual partners. True learning is completely absent.

Teachers only teach because they have to do it to get paid, not for passion. Their only true incentive is co-authoring papers.

We reject this bullshit.

Education is meant to help us, the students, achieve our goals through passionate learning.

And, we, the students, are individuals, with different goals and capabilities.

The way we protest is to publish the knowledge from University for free, on the Internet, so that anyone can access it.

And we do this is a law-abiding way, without copyright infringement, so that no one can legally take it down.

We come to our courses just for the useless roll calls. But we already know all the subject better than the "teacher" on the very first day.

And we are already more famous than the "teacher" online, and through the Internet have already taught more way way more people than they ever will.

The effect of this is to demoralize the entire school system at all levels, until only one conclusion is possible: implosion.

And from the ashes of the old system, we will build a new one, which does only what matters with absolute efficiency: help the individual students achieve their goals.

A system in which the only reason why university exist will be to [allow the most knowledgeable students to access million dollar laboratory equipment](university.md#the-only-reason-for-universities-to-exist-should-be-the-laboratories), and to pay the most prolific content creators so they can continue content creating.

No more useless courses. No more useless tests. Only passion, usefulness and focus.

## Feature ideas

↑ **Parent:** [OurBigBook.com](ourbigbook-com.md)

In this section we will gather some more advanced ideas besides the basic features described at [how the website works](#how-the-website-works).

### PageRank-like ranking

↑ **Parent:** [Feature ideas](#feature-ideas)

It would be really cool to have a [PageRank](google.md#pagerank)-link algorithm that answers the key questions:
- what is the best content for subject X.

  For example, if you are reading `cirosantilli/riemann-integral` and it is crap, you would be able to click the button

  > Versions by other authors

  which leads you to the URL: [http://ourbigbook.com/subject/mathematics](http://ourbigbook.com/subject/mathematics). This URL then contains a list of all pages people have written about the subject `mathematics`, sorted by some algorithm, containing for example:
  - [http://ourbigbook.com/johnsmith/riemann-integral](http://ourbigbook.com/johnsmith/riemann-integral)
  - [http://ourbigbook.com/cirosantilli/riemann-integral](http://ourbigbook.com/cirosantilli/riemann-integral)

  This URL would also contain a list of issues/comments that are related to the subject.
- who knows the most about subject X. This can be found by visiting: [http://ourbigbook.com/users/mathematics](http://ourbigbook.com/users/mathematics) "Top Mathematics users", which would contain the list of users sorted by the algorithm:
  - [http://ourbigbook.com/johnsmith](http://ourbigbook.com/johnsmith)
  - [http://ourbigbook.com/cirosantilli](http://ourbigbook.com/cirosantilli)
However, Ciro has decided to leave this for phase two [action plan](#action-plan), because it is impossible to tune such an algorithm if you have no users or test data.

Perhaps it is also worth looking into [ExpertRank](google.md#expertrank), they appear to do some kind of "expert in this area", but with [clustering](artificial-intelligence.md#cluster-analysis) (unlike us, where the clustering would be more explicit).

Other dump of things worth looking into:
- [https://en.wikipedia.org/wiki/Hilltop_algorithm](https://en.wikipedia.org/wiki/Hilltop_algorithm)

## User acquisition

↑ **Parent:** [OurBigBook.com](ourbigbook-com.md)

The general and ideal user acquisition is of course organic Googling:
- user does not understand his teacher's explanation of a subject
- user [Googles](google.md) into rare specific subject
- looks around, then login/create account with [OAuth](software.md#oauth) to leaves a comment or upvote
- notice that you can fork anything
- [mind = KABOOM](brain.md#mind-blown)

However, before that point, it is very likely that Ciro will have to physically do some very hard and specific user acquisition work at some University. Maybe there is a more virtual way of achieving this.

This work will involve going through some open set of [university lecture notes](#university-lecture-notes), and creating a superior version of them on OurBigBook.com, and somehow getting students to notice it and use it as a superior alternative to their crappy lecture notes.

Another very promising route is publishing the answers to old examination questions on the website. It is likely that we will be able to overcome any copyright issues by uploading only the answers to numbered questions. There is a minor risk that these would be considered [derivative works](law.md#derivative-work) of the copyrighted questions. But universities would have to be very anal to enforce a DMCA for that!!!
- [https://www.reddit.com/r/learnmath/comments/lj12pg/problem_sets_and_solutions_equivalent_to/](https://www.reddit.com/r/learnmath/comments/lj12pg/problem_sets_and_solutions_equivalent_to/)

Getting in contact with students is an epic challenge, as an incredibly deep chasm separates us:
- it is basically impossible to try and approach teachers: [how to convince teachers to use CC BY-SA](#how-to-convince-teachers-to-use-cc-by-sa)
- and on the other hand, how will you get university students to trust you are not a pedophile and that you actually want to help them?

  The missing aspect is how to join their main "class communication group", e.g. a [WhatsApp](messaging-software.md#whatsapp) or [Discord](messaging-software.md#discord-software) chat they have. That would be the perfect entry point to communicate with the end users. But that entry point is also generally closed exclusively for students, and sometimes lecturers, and will not accept anyone external.

  Perhaps Ciro would be able to do something with one of the two Universities he attended in the past: [École Polytechnique](ecole-polytechnique.md) or [University of São Paulo](university.md#university-of-sao-paulo). But there was no clear channel in those institutions for that. There is either an "infinitely noisy Facebook with everyone that bothered" or silence, deathly silence and isolation of no contact. The key hard part is getting a per-course granularity chat. [Discord](messaging-software.md#discord-software) Student Hubs are a fantastic initiative in that area. Shame that Discord is an unusable mess with zero ways to select which notifications you care about: [Section "Discord email notifications"](messaging-software.md#discord-email-notifications)!

  One approach method that shows some promise is to follow the [Student societies](education.md#student-society), which often host open events of interest outside of work hours.

Walking with advertisement t-shirts mentioning specific course names in some university location is something Ciro seriously considers, that's how desperate things are. Watch out: [https://docs.ourbigbook.com/#public-relations](https://docs.ourbigbook.com/#public-relations) for T-shirt news!

## Funding

↑ **Parent:** [OurBigBook.com](ourbigbook-com.md)

Ciro is looking for:
- university teachers who might be interested in trying it out as described at [Section 3. "Action plan"](#action-plan), especially [those who already use open licenses for their lecture notes](#how-to-convince-teachers-to-use-cc-by-sa)
- [funding possibilities](#funding) for this project, including donations as mentioned at [Section "Sponsor Ciro Santilli's work on OurBigBook.com"](sponsor.md) and contracts

The initial incentive for the creators is to make them famous and allow them to get more fulfilling jobs more easily, although Ciro also wants to add [money transfer](#knowledge-market) mechanisms to it later on.

We [can't rely on teachers writing materials, because they simply don't have enough incentive](#how-to-convince-teachers-to-use-cc-by-sa): publication count is all that matters to their careers. The students however, are desperate to prove themselves to the world, and becoming famous for amazing educational content is something that some of them might want to spend their times on, besides grinding for useless [grade](education.md#grade-exam).

### Why it is hard to make money from this website

↑ **Parent:** [Funding](#funding)

There is basically only one scalable business model in education as of the 2020's: helping teenagers pass [university entry exams](university.md#university-entry-exam). And nothing else. Everything else is a "waste" of time.

Perhaps there is a little bit of publicity incentive to helping them win [knowledge olympiads](social-technology.md#knowledge-olympiad) as well, but it is tiny in comparison, and almost certainly not a scalable investment. This may also depend on whether universities consider anything but exams, which varies by country.

That marked is completely saturated, and [Ciro Santilli](ciro-santilli.md) refuses to participate in it for [moral reasons](#motivation).

Beyond that, there is no scalable investment. Other non-scalable investments that could allow one to make a [lifestyle business](company.md#lifestyle-business) are:
- extra-curricular initiatives to get younger children interested in science. These may have some money stream coming from the parents of the children. This happens because for young children, the parents are more in control, and the parents, unlike the students, have some money to spend. An example: [https://www.littlehouseofscience.com/](https://www.littlehouseofscience.com/)

  The space is also further crowded by several not-for profits.

  This business model is possible because experiments for young children may be cheap to realize, unlike any experiment that would matter to a teenager or adult.
- creating a private university, for profit or not. Of course, at this point, you would be either:
  - competing against the reputation and funding of century old universities
  - or be offering more boring, lower tech or techless courses, to (God forbid the phrasing) "worse students", i.e. at a "worse university"

Teenagers and young adults:
- don't have money to give you if you want to "help them learn for real"
- are somewhat forced to obtain their "reputable university" reputation to kickstart their careers

It is this perfect storm that places this specific section of education in such a bad shape that it is today.

This project is likely to fail. It could become the [TempleOS](systems-programming.md#templeos) of [wikis](website.md#wiki). The project' [autism](brain.md#autism) score is quite high. It might be an impossible attempt at a [lifestyle business](company.md#lifestyle-business). But Ciro is beyond caring now. It must be done. Other things that come to mind:
- [https://www.youtube.com/playlist?list=PLibNZv5Zd0dzvoxXrjA9xNHLpdgLhTkZz](https://www.youtube.com/playlist?list=PLibNZv5Zd0dzvoxXrjA9xNHLpdgLhTkZz) "Obsessed" playlist by Wired. Helps Ciro feel better about himself.
- [Don Quixote](https://en.wikipedia.org/wiki/Don_Quixote)
- [pipe dream](https://en.wiktionary.org/wiki/pipe_dream)
- [Video "Don't Try - The Philosophy of Charles Bukowski by Pursuit of Wonder (2019)"](ciro-santilli-s-psychology-and-physiology.md#video-don-t-try-the-philosophy-of-charles-bukowski-by-pursuit-of-wonder-2019)

Dangerous combination:

> One man with a laptop and a dream.

and for any crazy person who might wish to join: [Men Wanted for Hazardous Journey](art.md#men-wanted-for-hazardous-journey).

<a id="video-one-man-s-dream-ken-fritz-documentary-2021"></a>
**[Video 5](#video-one-man-s-dream-ken-fritz-documentary-2021). One Man's Dream - Ken Fritz Documentary (2021)** [Source](https://www.youtube.com/watch?v=4b2IOOhJmxw). In some ways, Ciro was reminded of [OurBigBook.com](ourbigbook-com.md) by this documentary. Ken built his ultimate audio system without regard to money and time, to enjoy until he dies. Ciro is doing something similar. There is one fundamental difference however: everyone can enjoy a website all over the world.

A bit ominous though that the whole thing was eventually sold off for a fraction of the building cost: [https://www.washingtonpost.com/style/interactive/2024/ken-fritz-greatest-stereo-auction-cost/](https://www.washingtonpost.com/style/interactive/2024/ken-fritz-greatest-stereo-auction-cost/).

---

### Crowdfunding

↑ **Parent:** [Funding](#funding)

See: [Section "Sponsor Ciro Santilli's work on OurBigBook.com"](sponsor.md).

### Charitable grant opportunities

↑ **Parent:** [Funding](#funding)

Once the ball starts rolling, these are people who should be contacted.

Basically anything under [educational charitable organization](social-technology.md#educational-charitable-organization) counts.

It is also worth having a look under the [Wikipedia](#wikipedia) page for [open educational resources](software.md#open-educational-resources): [https://en.wikipedia.org/wiki/Open_educational_resources](https://en.wikipedia.org/wiki/Open_educational_resources)

### Consulting

↑ **Parent:** [Funding](#funding)

Start with consulting for universities to get some cash flowing.

Help teachers create perfect courses.

At the same time, develop the website, and use the generated content to bootstrap it.

Choose a domain of knowledge, generate perfect courses for it, and find all teachers of the domain in the world who are teaching that and help them out.

Then expand out to other domains.

TODO: which domain of knowledge should we go for? The more precise the better.
- maths is perfect because it "never" changes. But does not make money.
- computer science might be good, e.g. machine learning.

### Knowledge market

↑ **Parent:** [Funding](#funding)

If enough people use it, we could let people sell knowledge content through us.

Teachers have the incentive of making open source to get more students.

Students pay when they want help to learn something.

We take a cut of the transactions.

However this goes a bit against our "open content" ideal.

Forced [sponsorware](law.md#sponsorware) would be a possibility.

Would be a bit like [Fiverr](website.md#fiverr). Hmmm, maybe this is not a good thing ;-)

### Advertisement

↑ **Parent:** [Funding](#funding)

Don't like this very much, but if it's the only way...

Maybe focus on job ads like [Stack Overflow](stack-overflow.md).

Then:
- like [YouTube](website.md#youtube), pay creators proportionally to views/metrics
- paid subscription to remove ads from site

### Association with innovative schools

↑ **Parent:** [Funding](#funding)

Maybe we should talk to [innovative schools](education.md#innovative-school), as they might be more open to such use of technology.

### Venture capital

↑ **Parent:** [Funding](#funding)

Not a fun of giving up control for such a low-maintenance cost venture... but keeping a list just in case...
- [https://twitter.com/Borthwick/status/1533511605081845761](https://twitter.com/Borthwick/status/1533511605081845761) Betaworks

## ↑ Ancestors (5)

1. [OurBigBook Web](ciro-santilli-s-projects.md#ourbigbook-web)
2. [OurBigBook](ciro-santilli-s-projects.md#ourbigbook)
3. [Ciro Santilli's projects](ciro-santilli-s-projects.md)
4. [Ciro Santilli](ciro-santilli.md)
5. [Ciro Santilli's Homepage](README.md)

## ← Incoming links (97)

- [Ciro Santilli's Homepage](README.md)
- [108 Stars of Destiny](china.md#108-stars-of-destiny)
- [Aaron Swartz](software.md#aaron-swartz)
- [Ainan Celeste Cawley](brain.md#ainan-celeste-cawley)
- [Amit Singhal](university.md#amit-singhal)
- [Autodidacticism](education.md#autodidacticism)
- [CIA 2010 covert communication websites](cia-2010-covert-communication-websites.md)
- [Backlinks](cia-2010-covert-communication-websites.md#backlinks)
- [Overview of Ciro Santilli's investigation](cia-2010-covert-communication-websites.md#overview-of-ciro-santilli-s-investigation)
- [Ciro Santilli](ciro-santilli.md)
- [Ciro Santilli's bad old event memory](ciro-santilli-s-psychology-and-physiology.md#ciro-santilli-s-bad-old-event-memory)
- [Ciro Santilli's formal education](ciro-santilli.md#ciro-santilli-s-formal-education)
- [Ciro Santilli's knowledge hoarding](ciro-santilli-s-psychology-and-physiology.md#ciro-santilli-s-knowledge-hoarding)
- [Ciro Santilli's minor projects](the-most-important-projects-done-by-ciro-santilli.md#ciro-santilli-s-minor-projects)
- [Ciro Santilli's Open Source Enlightenment](ciro-santilli.md#ciro-santilli-s-open-source-enlightenment)
- [Ciro Santilli's psychology and physiology](ciro-santilli-s-psychology-and-physiology.md)
- [Ciro Santilli's self perceived compassionate personality](ciro-santilli-s-psychology-and-physiology.md#ciro-santilli-s-self-perceived-compassionate-personality)
- [Ciro Santilli's Stack Overflow contributions](the-most-important-projects-done-by-ciro-santilli.md#ciro-santilli-s-stack-overflow-contributions)
- [cirosantilli.com](cirosantilli-com.md)
- [Closed access academic journals are evil](education.md#closed-access-academic-journals-are-evil)
- [Collaborative writing platform](website.md#collaborative-writing-platform)
- [Common Crawl WWW Ranking](google.md#common-crawl-www-ranking)
- [Dan Abramson](education.md#dan-abramson)
- [Daniel Sank](quantum-computing.md#daniel-sank)
- [Dietterich Labs](particle-physics.md#dietterich-labs)
- [Don't be a pussy](don-t-be-a-pussy.md)
- [E-learning websites must allow students to create learning content](website.md#e-learning-websites-must-allow-students-to-create-learning-content)
- [E-learning websites must keep content free, only charge for certification](website.md#e-learning-websites-must-keep-content-free-only-charge-for-certification)
- [Education](education.md)
- [Encyclopedia Britannica](literature.md#encyclopedia-britannica)
- [Evil](cirism.md#evil)
- [Force public university teachers to publish their teaching material with an open license](university.md#force-public-university-teachers-to-publish-their-teaching-material-with-an-open-license)
- [Free gifted education](cirism.md#free-gifted-education)
- [GitBook](website.md#gitbook)
- [Google Analytics](google.md#google-analytics)
- [Google X](google.md#google-x)
- [Gülen movement](religion.md#gulen-movement)
- [How Ciro Santilli manages to write so much](ciro-santilli-s-psychology-and-physiology.md#how-ciro-santilli-manages-to-write-so-much)
- [How to teach](how-to-teach.md)
- [How to teach and learn physics](physics.md#how-to-teach-and-learn-physics)
- [It is not possible to teach natural sciences on Wikipedia](website.md#it-is-not-possible-to-teach-natural-sciences-on-wikipedia)
- [Khan Academy](website.md#khan-academy)
- [Knol](google.md#knol)
- [Leanpub](telecommunication.md#leanpub)
- [Learning management system](website.md#learning-management-system)
- [LibreTexts](social-technology.md#libretexts)
- [Massive open online course](website.md#massive-open-online-course)
- [MathDoctorBob](mathematics.md#mathdoctorbob)
- [MathWorld](website.md#mathworld)
- [Medium (website)](website.md#medium-website)
- [Michael J. Saylor](social-technology.md#michael-j-saylor)
- [Nature Scitable](website.md#nature-scitable)
- [Open knowledge](software.md#open-knowledge)
- [Open PageRank](google.md#open-pagerank)
- [OpenStax](website.md#openstax)
- [OurBigBook.com is number one](todo.md#ourbigbook-com-is-number-one)
- [OurBigBook.com](the-most-important-projects-done-by-ciro-santilli.md#ourbigbook-com-top-project)
- [GitHub](#github)
- [How to convince teachers to use CC BY-SA](#how-to-convince-teachers-to-use-cc-by-sa)
- [Other projects](#other-projects)
- [Why it is hard to make money from this website](#why-it-is-hard-to-make-money-from-this-website)
- [OurBigBook Markup](ciro-santilli-s-projects.md#ourbigbook-markup)
- [OurBigBook Web](ciro-santilli-s-projects.md#ourbigbook-web)
- [Paul Dirac](physicist.md#paul-dirac)
- [Physics](physics.md)
- [PlanetMath](website.md#planetmath)
- [Popular science](science.md#popular-science)
- [Quantum Field Theory lecture notes by David Tong (2007)](quantum-field-theory.md#quantum-field-theory-lecture-notes-by-david-tong-2007)
- [Quora](website.md#quora)
- [Saylor Academy](social-technology.md#saylor-academy)
- [School must offer free accommodation for students](cirism.md#school-must-offer-free-accommodation-for-students)
- [Second brain](brain.md#second-brain)
- [Social inequality](economy.md#social-inequality)
- [Sponsor Ciro Santilli's work on OurBigBook.com](sponsor.md)
- [Ourbigbook.com](sponsor/updates/4.md#ourbigbook-com)
- [Why you should give money to Ciro Santilli](sponsor.md#why-you-should-give-money-to-ciro-santilli)
- [Stack Overflow content deletion](stack-overflow.md#stack-overflow-content-deletion)
- [Stack Overflow is doomed](stack-overflow.md#stack-overflow-is-doomed)
- [Steve Jobs' 2005 Stanford Commencement Address](don-t-be-a-pussy.md#steve-jobs-2005-stanford-commencement-address)
- [Students must have a flexible choice of what to learn](cirism.md#students-must-have-a-flexible-choice-of-what-to-learn)
- [The missing link between basic and advanced](ciro-santilli.md#the-missing-link-between-basic-and-advanced)
- [The only reason for universities to exist should be the laboratories](university.md#the-only-reason-for-universities-to-exist-should-be-the-laboratories)
- [The Playlist](film.md#the-playlist)
- [The most important projects Ciro Santilli wants to do](todo.md)
- [Trillium Notes](website.md#trillium-notes)
- [Universal basic income](cirism.md#universal-basic-income)
- [University](university.md)
- [How the tech improved](updates.md#ourbigbook-project-update-march-2025/how-the-tech-improved)
- [I ended up doing tech rather than content as usual](updates.md#ourbigbook-project-update-march-2025/i-ended-up-doing-tech-rather-than-content-as-usual)
- [Videos of all key physics experiments](todo.md#videos-of-all-key-physics-experiments)
- [vistomail.com](cryptocurrency.md#vistomail-com)
- [Website front-end for a mathematical formal proof system](todo.md#website-front-end-for-a-mathematical-formal-proof-system)
- [Make your education system more efficient](what-poor-countries-have-to-do-to-get-richer.md#make-your-education-system-more-efficient)
- [When in doubt, choose the course that has the most experimental work](university.md#when-in-doubt-choose-the-course-that-has-the-most-experimental-work)
- [Why Ciro Santilli refers to himself in the third person](cirosantilli-com.md#why-ciro-santilli-refers-to-himself-in-the-third-person)
- [Wikipedia subpages](website.md#wikipedia-subpages)
- [WikiWikiWeb](website.md#wikiwikiweb)
