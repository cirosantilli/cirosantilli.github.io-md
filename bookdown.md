# Bookdown

↑ **Parent:** [List of static site generators](list-of-static-site-generators.md)  
🏷️ **Tags:** [R (programming language)](r-programming-language.md)

[https://github.com/rstudio/bookdown](https://github.com/rstudio/bookdown)

Written in [R](r-programming-language.md), but also relies on [pandoc](pandoc.md), so quite bad dependency wise.

Cross files references to IDs: yes. But no check by default for duplicates when doing automatic ID from title. Just automatically disambiguates with `-1`, `-2` suffixes, and links take the last one available.

Source page splitting: splits at h2 by default. If configurable, likely always af fixed level?

Has some nice image generation from inline code from standard R plotting functions.

[Hello world](hello-world-program.md) documented at: [https://bookdown.org/yihui/bookdown/get-started.html](https://bookdown.org/yihui/bookdown/get-started.html)

[Hello world](hello-world-program.md) on [Ubuntu 23.04](ubuntu-23-04.md) after installing [R](r-programming-language.md):
```
sudo R -e 'install.packages("bookdown")'
git clone https://github.com/rstudio/bookdown-demo
cd bookdown-demo
Rscript -e 'bookdown::render_book("index.Rmd")'
xdg-open _book/index.html
```
The build CLI comes from: [https://stackoverflow.com/questions/50888871/how-to-use-rscript-command-line-tool-to-build-a-book-in-bookdown](https://stackoverflow.com/questions/50888871/how-to-use-rscript-command-line-tool-to-build-a-book-in-bookdown)

The installatoin `Rscript -e 'bookdown::render_book("index.Rmd")'` takes several minutes, it compiles a bunch of stuff from source apparently. but it did work.

## ↑ Ancestors (6)

1. [List of static site generators](list-of-static-site-generators.md)
2. [Static site generator](static-site-generator.md)
3. [Static website](static-website.md)
4. [Website](website-split.md)
5. [Art](art-split.md)
6. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (2)

- [C7.4 Oxford physics course](c7-4-oxford-physics-course.md)
- [R (programming language)](r-programming-language.md)
