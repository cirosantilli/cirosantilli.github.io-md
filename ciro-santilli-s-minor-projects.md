<h1 id="ciro-santilli-s-minor-projects">Ciro Santilli's minor projects</h1>

↑ **Parent:** [The most important projects done by Ciro Santilli](the-most-important-projects-done-by-ciro-santilli-split.md)

Major projects can be seen at: [Section "The most important projects done by Ciro Santilli"](the-most-important-projects-done-by-ciro-santilli-split.md).

These are some smaller projects that [Ciro Santilli](ciro-santilli-split.md) carried out. They are all either for fun, or misguided use of his time done by an younger self:
- small naughty stuff is listed at: [Section "Ciro Santilli's naughty projects"](ciro-santilli-s-naughty-projects.md)
- Because Ciro [cares about education](ourbigbook-com-split.md), around 2014 he looked into markup languages and version control for books, before he noticed that this approach was useless and that ranking algorithms are all that matter:
  - [GitLab](gitlab.md): very important to Ciro because he wanted to base [Booktree](https://github.com/booktree/booktree) on it.

    He was [the number 2 contributor from 2013 to 2015](https://github.com/gitlabhq/gitlabhq/graphs/contributors?from=2013-01-01&to=2015-01-01&type=a).

    He implemented some large features and several smaller improvements.

    For this reason, Ciro was made a moderator of [/r/gitlab](https://www.reddit.com/r/gitlab) in [2016-05](https://web.archive.org/web/20160524164714/https://www.reddit.com/r/gitlab/about/moderators).

    GitLab sent Ciro a free swag bottle later after they got funding on to thank him for his contributions: [Figure 8. "Ciro Santilli in a dune lake in Jericoacoara, Brazil, with his GitLab bottle"](#image-ciro-santilli-in-a-dune-lake-in-jericoacoara-brazil-with-his-gitlab-bottle). He had to pay for the beach trip though.

    <a id="image-ciro-santilli-in-a-dune-lake-in-jericoacoara-brazil-with-his-gitlab-bottle"></a>
    <img src="https://raw.githubusercontent.com/cirosantilli/media/master/Ciro_Santilli_in_a_dune_lake_in_Jericoacoara,_Brazil_with_his_GitLab_bottle.jpg" alt="" height="300">

    **[Figure 8](#image-ciro-santilli-in-a-dune-lake-in-jericoacoara-brazil-with-his-gitlab-bottle). Ciro Santilli in a dune lake in Jericoacoara, Brazil, with his GitLab bottle**.
  - [Markdown Style Guide](markdown-style-guide)
  - [karlcow/markdown-testsuite](karlcow-markdown-testsuite.md) improvements: Ciro has implemented the test runner a few months before CommonMark left stealth mode and killed it instantaneously.

    At least MacFarlane was able to [reuse](https://github.com/jgm/CommonMark/blob/2528c87c0cf08e02eb3e201c149cb3acf521e0c8/test/normalize.py#L8) part of the [HTML](html.md) normalizer [he wrote](https://github.com/karlcow/markdown-testsuite/blame/639cd234d71ca81956b61ff7876f37c3cdc5c043/run-tests.py), and he extracted the multi-engine comparison to: [CommonMark Implementation Compare](https://github.com/cirosantilli/commonmark-implementation-compare).

    Playing with this project has led Ciro to find and report many Markdown bugs/bad behavior on other software, e.g. [GitHub](https://github.com/isaacs/github/issues/297) and [MultiMarkdown-4](https://github.com/fletcher/MultiMarkdown-4/issues/68).
  - [isaacs/github public unofficial GitHub issue tracker](https://github.com/isaacs/github): he has commented there so often that he [was made a collaborator](https://github.com/isaacs/github/issues/430#issuecomment-123851480)
  - [Node Express Sequelize Next.js realworld example app](node-express-sequelize-next-js-realworld-example-app.md)
- [VCDVCD](https://github.com/cirosantilli/vcdvcd): [value change dump](value-change-dump.md) [command-line](command-line-interface.md) pretty printer!!! The type of thing that a billion dollar [EDA tool](electronic-design-automation.md) vendor will never implement ;-)
  ```
  0 time
  1 counter_tb.clock
  2 counter_tb.enable
  3 counter_tb.out[1:0]
  4 counter_tb.reset
  5 counter_tb.top.out[1:0]

  0 1 2 3 4 5
  ===========
  0 1 0 x 0 x
  1 0 0 x 1 x
  2 1 0 0 1 0
  3 0 0 0 0 0
  4 1 0 0 0 0
  5 0 1 0 0 0
  ```
- [Vim](vim.md): sometimes Ciro want crazy and wasted his time with Vimscript:
  - [Vim Markdown](https://github.com/plasticboy/vim-markdown): the owner `plasticboy` was really nice and made Ciro a collaborator for his contributions, notably a live ToC outline and the header mappings
  - [Vundle Plugin Tester](https://github.com/cirosantilli/vundle-plugin-tester), which he used to start the testing system of Vim Markdown
- [Breakthrough Message](https://github.com/cirosantilli/breakthrough-message): [aliens](extraterrestrial-life.md)!!! Creative/media project, powered by some [Python](python-programming-language.md) scripts.
- making [Google Maps](google-maps.md) reviews of places he's visited to help other people. Ciro's photos reached 1 million views in 2019: [https://www.google.com/maps/contrib/106598607405640635523/photos](https://www.google.com/maps/contrib/106598607405640635523/photos) ([archive](http://web.archive.org/web/20190905081800/https://www.google.com/maps/contrib/106598607405640635523/photos))

## 🏷️ Tagged (2)

- [Cirosantilli/parsec-benchmark](cirosantilli-parsec-benchmark.md)
- [Wikipedia CatTree](wikipedia-cattree-split.md)

## ↑ Ancestors (3)

1. [The most important projects done by Ciro Santilli](the-most-important-projects-done-by-ciro-santilli-split.md)
2. [Ciro Santilli](ciro-santilli-split.md)
3. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (6)

- [Ciro Santilli's projects](ciro-santilli-s-projects-split.md)
- [CommonMark](commonmark.md)
- [GitLab](gitlab.md)
- [Karlcow/markdown-testsuite](karlcow-markdown-testsuite.md)
- [Plasticboy/vim-markdown](plasticboy-vim-markdown.md)
- [The most important projects done by Ciro Santilli](the-most-important-projects-done-by-ciro-santilli-split.md)
