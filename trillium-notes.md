# Trillium Notes

↑ **Parent:** [List of Wikis](list-of-wikis.md)  
🏷️ **Tags:** [Personal knowledge base software](personal-knowledge-base-software.md), [Software that uses Electron](software-that-uses-electron.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Trillium_Notes)

Originally at [https://github.com/zadam/trilium](https://github.com/zadam/trilium), then after development stopped the community took it up at: [https://github.com/TriliumNext/Notes](https://github.com/TriliumNext/Notes).

Tree based organization at last. Infinitely deep.

Amazing [WYSIWYG](wysiwyg.md), including maths and tables, plus insane plugins like canvas mode, and specific file formats like code/mermaid diagrams/drawing mode.

Intentionally or not, they've basically made an [open source](open-source-software.md) [Notion](notion-productivity-software.md), with the possible exception that Notion historically started on web and moved to the desktop, while Trillium went the other way round.

Version history with automatic snapshots at intervals. TODO how is it implemented? Do they just [ZIP](zip-file-format.md) multiple versions?

No multiuser features. Except for that, could have been a good starting point of an online multiuser thing such as [OurBigBook.com](ourbigbook-com-split.md)!

With [Book Notes](https://github.com/zadam/trilium/wiki/Book-note) it is possible possible to see more than one page at a time on the output, which his a major feature of [OurBigBook](ourbigbook.md). But does it show on HTML export as well?

You can static HTML export any subtree by right clicking on it in the navigation tree.

Is there a CLI to export to HTML? [https://github.com/zadam/trilium/issues/3012](https://github.com/zadam/trilium/issues/3012)

HTML export keeps all data as HTML is their native format. This may be inherited from CKEditor. The files are mostly visible, but there is some CSS missing, it is not 100% like editor, notably math is broken. There is also a hosted way of exposing: [https://github.com/zadam/trilium/wiki/Sharing](https://github.com/zadam/trilium/wiki/Sharing).

[https://trilium.rocks](https://trilium.rocks) however has a very good export, it is just a question of how much they had to hacked things, source at: [https://github.com/zerebos/trilium.rocks](https://github.com/zerebos/trilium.rocks)

The default tHTML export uses frame navigation, with a toc fixed on the left frame. Efficient, but not of this century.

There is no concept of user created unique text IDs: you can have the same headers in the same folders in the UI. It's not even a matter of scopes. On exports they are differentiated as `1_name`, `2_name`, etc.
```
./Trilium Demo/Books/To read/1_HR.md
./Trilium Demo/Books/To read/2_HR.md
./Trilium Demo/Books/To read/HR.md
```

Markdown export warns:

> this preserves most of the formatting

Architecture: runs on local SQLite database via better-sqlite3. Data apparently stored in SQLite database at `~/.local/share/trilium-data`, no raw files.

Markup is stored as HTML as seen from: `sqlite3 document.db 'SELECT * from note_contents'`. HTML is their native storage format, quite interesting. But this means it is not source centric, so any source editing would have to go via import/export. It can be done apparently: [https://github.com/zadam/trilium/wiki/Markdown](https://github.com/zadam/trilium/wiki/Markdown) but involves shoving a ZIP around.

WYSIWYG based on [https://ckeditor.com/](https://ckeditor.com/) which is a dependency. It is kind of cool that the view in which you view the output is exactly the same as the one you edit in, and there is no intermediate format, just the HTML.

Math is [KaTeX](katex.md) based.

It also runs on the browser via a server: [https://github.com/zadam/trilium/wiki/Server-installation](https://github.com/zadam/trilium/wiki/Server-installation). And they have a paid service for it at: [https://trilium.cc/](https://trilium.cc/). Quite impressive.

They have server to from desktop sync: [https://github.com/zadam/trilium/wiki/synchronization](https://github.com/zadam/trilium/wiki/synchronization). There is no conflict resolution, one of them wins randomly. But they have revision history, and anything lost will be in the revision history. They have so many features it is mind blowing.

Maintainer announced he would be slowing down development since January 2024: [https://github.com/zadam/trilium/issues/4620?ref=selfh.st](https://github.com/zadam/trilium/issues/4620?ref=selfh.st)

## ↑ Ancestors (7)

1. [List of Wikis](list-of-wikis.md)
2. [Wiki](wiki.md)
3. [Collaborative writing platform](collaborative-writing-platform.md)
4. [Website genre](website-genre.md)
5. [Website](website-split.md)
6. [Art](art-split.md)
7. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (4)

- [List of personal knowledge base software](list-of-personal-knowledge-base-software.md)
- [Next steps](sponsor/updates/8/next-steps.md)
- [Metrics and rationales](updates/ourbigbook-project-update-march-2025/metrics-and-rationales.md)
- [What might be next](updates/ourbigbook-project-update-march-2025/what-might-be-next.md)
