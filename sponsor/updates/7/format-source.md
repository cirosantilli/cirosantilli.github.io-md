<h1 id="format-source"><code>--format-source</code></h1>

↑ **Parent:** [Advances](advances.md)

<a id="_17"></a>
Added `ourbigbook --format-source` automatic code formatting. I implemented it for the following reasons:<a id="_18"></a>

<a id="_19"></a>
- I want to do certain automatic modifications to source code on web, e.g.:<a id="_20"></a>

  <a id="_21"></a>
  - allow users to select the parent article of a new article on the web UI, but that is currently doable only with `\Include` macros
  <a id="_22"></a>
  - allow users to edit the source only for a specific header
<a id="_23"></a>
- later on, much later, this will allow [WYSIWYG](../../../wysiwyg.md) export to plaintext

<a id="_24"></a>
This also ended up having one unexpected benefit: whenever a new feature is added that deprecates an old feature, by converting the large corpus from [https://github.com/cirosantilli/cirosantilli.github.io](https://github.com/cirosantilli/cirosantilli.github.io) to the new feature I can test the new preferred feature very well.

<a id="_25"></a>
For example, converting `\x[blue cat]` en masse to the new insane syntax `<blue cat>` found several bugs with the new insane syntax.

<a id="_26"></a>
This seemed somewhat easy at first, so I started it as a way of procrastinating more urgent Web features (web scares me, you know), but it ended being insanely hard to implement, because there are many edge cases. Also, most bugs are not acceptable, as they would corrupt your precious source code and potentially output.

<a id="_27"></a>
But well, it is done!

## ↑ Ancestors (7)

1. [Advances](advances.md)
2. [Ourbigbook.com](ourbigbook-com.md)
3. [Ciro's Edict \#7](../7-split.md)
4. [Sponsor updates](../../../sponsor-updates.md)
5. [Update from Ciro Santilli](../../../update-from-ciro-santilli.md)
6. [Ciro Santilli](../../../ciro-santilli-split.md)
7. [Ciro Santilli's Homepage](../../../split.md)
