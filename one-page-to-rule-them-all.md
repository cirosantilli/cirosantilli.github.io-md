# One page to rule them all

↑ **Parent:** [Media rationale of Ciro Santilli's website](media-rationale-of-ciro-santilli-s-website.md)  
🏷️ **Tags:** [Monolithic system](monolithic-system.md)

It is true that one image is worth a thousand words, but unfortunately it is also true that one image takes up at least as much bytes as a thousand words!

Having one single page to rule them all is of course the [ideal](idealism.md) setup for a website, as you can Ctrl + F one ToC and quickly find what you want.

And, with [Linux Kernel Module Cheat](linux-kernel-module-cheat-split.md) Ciro noticed that it is very hard to write so much intelligent prose that becomes larger than reasonable to load on a single webpage.

He then started using this technique for everything he writes, including this page and [Chinese government](ciro-santilli-s-campaign-for-freedom-of-speech-in-china.md).

However, if there are too many images on the page, the loading of the last images would take forever in case users want to view the last sections.

There are two solutions to that:
- be traditional and create separate web pages
- be bold and load images as they appear on the viewport: [https://stackoverflow.com/questions/2321907/how-do-you-make-images-load-only-when-they-are-in-the-viewport/57389607#57389607](https://stackoverflow.com/questions/2321907/how-do-you-make-images-load-only-when-they-are-in-the-viewport/57389607#57389607)

  Edit: OK, it was standardized with `loading=lazy`, without need [JavaScript](javascript.md)!

  Now the last awesome thing would be a method that loads first images in viewport, then those below, and then those above, that would be the ultimate solution.

  This question comes close: [https://stackoverflow.com/questions/7906348/change-loading-order-of-images-already-on-page](https://stackoverflow.com/questions/7906348/change-loading-order-of-images-already-on-page)

Ciro is still deciding between those two. The traditional approach works for sure but loses the one page to rule them all benefits.

The innovative approach will work for interactive viewing, but archive.org will fail to load the images for example, and there may be other unforseen consequences.

Wikimedia Commons is awesome and automatically converts and serves smaller versions of images, so always choose the smallest images size needed by the output document. Readers can then find the higher resolution versions by following the page source.

This also comes to mind: [https://motherfuckingwebsite.com](https://motherfuckingwebsite.com)

[https://zettelkasten.de/posts/overview/](https://zettelkasten.de/posts/overview/) from [zettelkasten](zettelkasten.md):

> How many Zettelkästen should I have? The answer is, most likely, only one for the duration of your life. But there are exceptions to this rule.

## ↑ Ancestors (4)

1. [Media rationale of Ciro Santilli's website](media-rationale-of-ciro-santilli-s-website.md)
2. [cirosantilli.com](cirosantilli-com-split.md)
3. [Ciro Santilli](ciro-santilli-split.md)
4. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (4)

- [Publications](e-coli-whole-cell-model-by-covert-lab/publications.md)
- [README](readme.md)
- [The CSS of Ciro Santilli's website looks broken](the-css-of-ciro-santilli-s-website-looks-broken.md)
- [Zettelkasten](zettelkasten.md)
