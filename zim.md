# Zim

↑ **Parent:** [List of personal knowledge base software](list-of-personal-knowledge-base-software.md)  
🏷️ **Tags:** [Open source software](open-source-software.md), [WYSIWYG text editor](wysiwyg-text-editor.md)

Zim [https://zim-wiki.org/](https://zim-wiki.org/)

Local only.

[WYSIWYG](wysiwyg.md):
- bold
- images
- lists. But it is either hard or impossible to have a paragraph inside a list item.

<a id="image-zim"></a>
<img src="https://web.archive.org/web/20250218231148im_/https://zim-wiki.org/screenshots/zim-normal.png" alt="" height="600">

**[Figure 2](#image-zim). Zim**.

Mathematics requires a plugin and a full [LaTeX](latex.md) install: [https://zim-wiki.org/manual/Plugins/Equation_Editor.html](https://zim-wiki.org/manual/Plugins/Equation_Editor.html) They have a bunch of plugins: [https://zim-wiki.org/manual/Plugins.html](https://zim-wiki.org/manual/Plugins.html)

Can only link to toplevel of each source, not subheaders? And subpages get forced scope. [https://github.com/zim-desktop-wiki/zim-desktop-wiki](https://github.com/zim-desktop-wiki/zim-desktop-wiki)

Publishing to static HTML can be done with:
```
zim --export Notes -o out
```
The output does not contain any table of contents? There is a plugin however: [https://zim-wiki.org/manual/Plugins/Table_Of_Contents.html](https://zim-wiki.org/manual/Plugins/Table_Of_Contents.html)

It is unclear if their markup is compatible with an existing language of if it was made up from scratch. Wikipedia says:

> In Zim, text is written and saved in a lightweight mark-up that is a hybrid of [DokuWiki](dokuwiki.md) and [Markdown](markdown.md). 

You can't determine the ordering or pages at the same level, alphabetical ordering of force. The poplevel is encoded in `notebook.zim`:
```
[Notebook]
home=Home
```
Feature request: [https://github.com/zim-desktop-wiki/zim-desktop-wiki/issues/32](https://github.com/zim-desktop-wiki/zim-desktop-wiki/issues/32). It's not usable as a publishing system!

Doesn't seem to have image captions: [https://superuser.com/questions/1285898/picture-description-in-zim-wiki-0-64](https://superuser.com/questions/1285898/picture-description-in-zim-wiki-0-64)

## ↑ Ancestors (11)

1. [List of personal knowledge base software](list-of-personal-knowledge-base-software.md)
2. [Personal knowledge base software](personal-knowledge-base-software.md)
3. [Personal knowledge base](personal-knowledge-base.md)
4. [Braindumping](braindumping.md)
5. [Brain](brain-split.md)
6. [Organ (anatomy)](organ-anatomy.md)
7. [Level of organization of bodies](level-of-organization-of-bodies.md)
8. [Biology](biology-split.md)
9. [Natural science](natural-science.md)
10. [Science](science-split.md)
11. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (1)

- [Zim](zim.md)
