<h1 id="ourbigbook-project-update-march-2025/how-the-tech-improved">How the tech improved</h1>

↑ **Parent:** [OurBigBook Project Update March 2025](../ourbigbook-project-update-march-2025.md)

<a id="ourbigbook-project-update-march-2025/_402"></a>
In any case, the outcome of that is that the tech has improved. And I have done a relatively good job of clearly publishing any "more user visible" improvements to [https://docs.ourbigbook.com/news](https://docs.ourbigbook.com/news) and social media such as <a id="ourbigbook-project-update-march-2025/_403"></a>

<a id="ourbigbook-project-update-march-2025/_404"></a>
- [https://mastodon.social/@OurBigBook](https://mastodon.social/@OurBigBook)
<a id="ourbigbook-project-update-march-2025/_405"></a>
- [https://x.com/OurBigBook](https://x.com/OurBigBook)
though it is important to note that there have been more than one "fix a hard bug" weeks that were not published because they would just bore readers.

<a id="ourbigbook-project-update-march-2025/_406"></a>
During this period the main focus has been on improving [OurBigBook Web](../../ourbigbook-web.md), i.e. the dynamic website that powers [OurBigBook.com](../../ourbigbook-com-split.md). There are two reasons for that:<a id="ourbigbook-project-update-march-2025/_407"></a>

<a id="ourbigbook-project-update-march-2025/_408"></a>
- <a id="ourbigbook-project-update-march-2025/_409"></a>
  Web is what has the [OurBigBook topics feature](../../ourbigbook-topic-feature.md) for mind-melding, which is the killer feature of OurBigBook compared to other [note taking apps](../../personal-knowledge-base-software.md) and therefore deserves the highest levels of priority

  <a id="ourbigbook-project-update-march-2025/_410"></a>
  Static website generation is an indispensable escape valve that ensures that your content can be published forever even if [OurBigBook.com](../../ourbigbook-com-split.md) goes down one day, which it won't as long as I live. But the innovation is Web.
<a id="ourbigbook-project-update-march-2025/_411"></a>
- <a id="ourbigbook-project-update-march-2025/_412"></a>
  static website generation was closer to good enough, but web was much further and is fundamentally harder.

  <a id="ourbigbook-project-update-march-2025/_413"></a>
  I'm extremely satisfied with [OurBigBook](../../ourbigbook.md) static website generation and haven't touched it as much. It wasn't easy to reach this state, but I'm there.

  <a id="ourbigbook-project-update-march-2025/_414"></a>
  But Web is a different and much more complex beast.

  <a id="ourbigbook-project-update-march-2025/_415"></a>
  Making CLI software that will run on a person's local computer under full trust and building a bunch of HTML from [lightweight markup](../../lightweight-markup-language.md) in bulk is one thing.

  <a id="ourbigbook-project-update-march-2025/_416"></a>
  But making a public dynamic website that has to continuously maintain a coherent database state on granular updates, while giving users some trust but not enough for them to blow everything up is on a totally different level. See e.g. [the recent SPAM attack we've had to fend off](https://docs.ourbigbook.com/news/signup-ip-blacklist-vpn-detection-and-account-locking).

  <a id="ourbigbook-project-update-march-2025/image-screenshot-showing-voting-manipulated-spam-as-the-most-highly-upvoted-article-on-ourbigbook-com"></a>
  <img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/spam/crypto.png" alt="" height="971">

  **[Figure 20](#ourbigbook-project-update-march-2025/image-screenshot-showing-voting-manipulated-spam-as-the-most-highly-upvoted-article-on-ourbigbook-com). Screenshot showing voting manipulated SPAM as the most highly upvoted article on OurBigBook.com**. [Source](https://web.archive.org/web/20250228110911/https://ourbigbook.com/go/articles?sort=score).

  <a id="ourbigbook-project-update-march-2025/_417"></a>
  And then there's also the issue of front-end being mega-hard to get right.
As a result, Web is now way less buggy and much more usable.

<a id="ourbigbook-project-update-march-2025/_418"></a>
If you look through the list of Web updates, there is nothing specifically mind blowing. The core ideas have largely crystallized, and we are just trying to making them click. I have a few more punches up my sleeve, but the core is decided.

<a id="ourbigbook-project-update-march-2025/image-ourbigbook-web-search"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/search/full-text-calculus-fun-arrow.png" alt="" height="738">

**[Figure 21](#ourbigbook-project-update-march-2025/image-ourbigbook-web-search). OurBigBook Web search**. [Source](https://ourbigbook.com/go/articles?body=false&search=calculus%20fun). This is one of the many basic quality of life improvements that have been done on OurBigBook Web.

<a id="ourbigbook-project-update-march-2025/image-ourbigbook-web-article-announcement"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/announce/modal.png" alt="" height="349">

**[Figure 22](#ourbigbook-project-update-march-2025/image-ourbigbook-web-article-announcement). OurBigBook Web article announcement**. [Source](https://ourbigbook.com/cirosantilli/chain-rule). Another cute new feature, you can send an email to your followers about a new amazing article you created.

<a id="ourbigbook-project-update-march-2025/_419"></a>
Web process has been somewhat slower than what I'd like. Of course, it is the case of any project that things are easily said than done. But there are two other main structural factors that have played into it:<a id="ourbigbook-project-update-march-2025/_420"></a>

<a id="ourbigbook-project-update-march-2025/_421"></a>
- <a id="ourbigbook-project-update-march-2025/_422"></a>
  I have my first baby now, and we're learning how to deal with that on the fly.

  <a id="ourbigbook-project-update-march-2025/_423"></a>
  For example, we could have put him on childcare a bit earlier, but due to inexperience we've kept him a bit longer than we maybe should have.

  <a id="ourbigbook-project-update-march-2025/_424"></a>
  Things are well sorted out now, but not matter how good your support system is, at the end of the day, and more often night, it is you the parents that have to deal with a lot of inevitable baby issues. Unless you want them to turn into psychopaths and drug addicts that is, which I don't. I've reached the point of semi failure middle age that the baby feels like my best moonshot.

  <a id="ourbigbook-project-update-march-2025/_425"></a>
  All of this sets a fundamental limit on how many hours you can work per week.

  <a id="ourbigbook-project-update-march-2025/_426"></a>
  But at least with the donations I was able to work on OurBigBook at all. Because if it weren't for that, I would have to focus entirely on the generic job instead and OurBigBook would have been put on hold.
<a id="ourbigbook-project-update-march-2025/_427"></a>
- <a id="ourbigbook-project-update-march-2025/_428"></a>
  the choice of Web stack. I was allured by [Next.js](../../next-js.md). I can see the beauty and usefulness of a [Node.js](../../node-js-split.md) render front-end that also runs on backend and hydration. That is awesome.

  <a id="ourbigbook-project-update-march-2025/_429"></a>
  But:<a id="ourbigbook-project-update-march-2025/_430"></a>

  <a id="ourbigbook-project-update-march-2025/_431"></a>
  - [React](../../react-split.md) is insanely hard to learn and understand. Furthermore, it is also hard to understand the performance problem that it solves, and actually have a benchmark where this problem is solved faster than just delivering some HTML files with ad-hoc Js on top.
  <a id="ourbigbook-project-update-march-2025/_432"></a>
  - the lack (or perhaps excess of shitty) actual web framework like [Ruby on Rails](../../ruby-on-rails.md) and [Django](../../django-web-framework.md) means that I have to rediscover the wheel many times over for all the essential support activities like testing, login and so one

  <a id="ourbigbook-project-update-march-2025/_433"></a>
  At this point a rewrite is out of the question. I've managed to master things well enough to get a decent result, [and given up on the few things that I couldn't for the life of me achieve](https://github.com/ourbigbook/ourbigbook/issues/361), after documenting them very well for posterity of course.

<a id="ourbigbook-project-update-march-2025/_434"></a>
Aside from Web, there was only one thing that received a significant improvement, and that was the [OurBigBook VS Code extension](https://docs.ourbigbook.com/visual-studio-code). The extension is not perfect, and it is not the "final UI", which has to be some [WYSIWYG](../../wysiwyg.md) implementation, and there are some fundamental limitations that cannot be overcome without patching VS Code itself. However, the extension is already extremely usable, and I'm writing this on it right now. Basics like syntax highlighting, jump to definition and autocomplete are very useful and usable.

<a id="ourbigbook-project-update-march-2025/image-tree-navigation-in-the-ourbigbook-visual-studio-code-extension"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/vscode/tree.png" alt="" height="1100">

**[Figure 23](#ourbigbook-project-update-march-2025/image-tree-navigation-in-the-ourbigbook-visual-studio-code-extension). Tree navigation in the OurBigBook Visual Studio Code extension**.

## ↑ Ancestors (4)

1. [OurBigBook Project Update March 2025](../ourbigbook-project-update-march-2025.md)
2. [Updates](../../updates-split.md)
3. [Ciro Santilli](../../ciro-santilli-split.md)
4. [Ciro Santilli's Homepage](../../split.md)
