<h1 id="format-source"><code>--format-source</code></h1>

↑ **Parent:** [Advances](advances.md)

Added `ourbigbook --format-source` automatic code formatting. I implemented it for the following reasons:
- I want to do certain automatic modifications to source code on web, e.g.:
  - allow users to select the parent article of a new article on the web UI, but that is currently doable only with `\Include` macros
  - allow users to edit the source only for a specific header
- later on, much later, this will allow [WYSIWYG](../../../wysiwyg.md) export to plaintext

This also ended up having one unexpected benefit: whenever a new feature is added that deprecates an old feature, by converting the large corpus from [https://github.com/cirosantilli/cirosantilli.github.io](https://github.com/cirosantilli/cirosantilli.github.io) to the new feature I can test the new preferred feature very well.

For example, converting `\x[blue cat]` en masse to the new insane syntax `<blue cat>` found several bugs with the new insane syntax.

This seemed somewhat easy at first, so I started it as a way of procrastinating more urgent Web features (web scares me, you know), but it ended being insanely hard to implement, because there are many edge cases. Also, most bugs are not acceptable, as they would corrupt your precious source code and potentially output.

But well, it is done!

## ↑ Ancestors (7)

1. [Advances](advances.md)
2. [Ourbigbook.com](ourbigbook-com.md)
3. [Ciro's Edict \#7](../7-split.md)
4. [Sponsor updates](../../../sponsor-updates.md)
5. [Update from Ciro Santilli](../../../update-from-ciro-santilli.md)
6. [Ciro Santilli](../../../ciro-santilli-split.md)
7. [Ciro Santilli's Homepage](../../../split.md)
