<h1 id="how-to-develop-ciro-santilli-s-website-before-the-ourbigbook-migration">How to develop Ciro Santilli's website before the OurBigBook migration</h1>

↑ **Parent:** [cirosantilli.com](cirosantilli-com-split.md)

The website moved from [AsciiDoctor](asciidoctor.md) to [OurBigBook Markup](ourbigbook-markup.md) in 2020, making this section mostly useless. But hey, history!

Ciro's website is powered by [GitHub Pages](github-pages.md) and [Jekyll Asciidoc](https://github.com/asciidoctor/jekyll-asciidoc).

The source code is located at: [https://github.com/cirosantilli/cirosantilli.github.io](https://github.com/cirosantilli/cirosantilli.github.io)

Build locally, watch for changes and rebuild automatically, and start a local server with:
```
git clone --recursive https://github.com/cirosantilli/cirosantilli.github.io
cd cirosantilli.github.io
bundle install
npm install
./run
```

Source: `./run`.

The website will be visible at: [http://localhost:4000](http://localhost:4000).

Tested on the latest Ubuntu.

Publish changes to [GitHub Pages](github-pages.md):
```
git add -u
git commit -m 'make yourself look sillier'
./publish
```

Source: `./publish`.

GitHub forces us to use the master branch for the build output... so the actual source is in the branch `dev`.

Update the gems with:
```
bundle update
git add Gemfile.lock
git commit -m 'update gems'
```

His website was originally written in [markdown](markdown.md), however those were deprecated in favour of [AsciiDoctor](asciidoctor.md) when Ciro saw the light, rationale shown at: [markdown-style-guide[use-asciidoc](https://ourbigbook.com/go/topic/use-asciidoc)](markdown-style-guide[use-asciidoc](https://ourbigbook.com/go/topic/use-asciidoc))

GitHub pages is chosen instead of a single page GitHub README.adoc for the following reasons:
- Ciro will want some unsupported extensions, notably mathematics, likely with [KaTeX server side](mathematics-typesetting-setup-of-ciro-santilli-s-website.md):
  - [https://github.com/asciidoctor/asciidoctor/pull/3338](https://github.com/asciidoctor/asciidoctor/pull/3338)
  - [https://stackoverflow.com/questions/11256433/how-to-show-math-equations-in-general-githubs-markdownnot-githubs-blog](https://stackoverflow.com/questions/11256433/how-to-show-math-equations-in-general-githubs-markdownnot-githubs-blog)
  - [https://g14n.info/2014/09/math-on-github-pages/](https://g14n.info/2014/09/math-on-github-pages/)
  - [https://stackoverflow.com/questions/11256433/how-to-show-math-equations-in-general-githubs-markdownnot-githubs-blog](https://stackoverflow.com/questions/11256433/how-to-show-math-equations-in-general-githubs-markdownnot-githubs-blog)
  - [https://www.quora.com/How-can-I-combine-latex-and-markdown-in-GitHub](https://www.quora.com/How-can-I-combine-latex-and-markdown-in-GitHub)
- when GitHub dies, Ciro's website URL still lives and retains the [PageRank](pagerank.md)!

## ↑ Ancestors (3)

1. [cirosantilli.com](cirosantilli-com-split.md)
2. [Ciro Santilli](ciro-santilli-split.md)
3. [Ciro Santilli's Homepage](split.md)
