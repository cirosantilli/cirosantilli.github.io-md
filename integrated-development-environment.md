# Integrated development environment

↑ **Parent:** [Software](software-split.md)  
🏷️ **Tags:** [Good](good.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Integrated_development_environment)

IDEs are absolutely essential for developing complex software.

The funny thing is that you don't notice this until someone shows it to you. But once you see it, there is not turning back, just like [Steve Jobs customers don't know what they want quote](steve-jobs-customers-don-t-know-what-they-want-quote.md).

Unfortunately, after the [Fall of Eclipse](https://movingfulcrum.com/the-fall-of-eclipse/) ([archive](https://web.archive.org/web/20190824081229/https://movingfulcrum.com/the-fall-of-eclipse/)), the IDE landscape in 2019 is horrible and split between:
- highly buggy but still feature rich Eclipse
- many may many other feature lacking options using possibly more trendy and forward lasting implementations like [Electron](https://en.wikipedia.org/wiki/Electron_(software_framework))
- awesome cross-platform proprietary [JetBrains](https://en.wikipedia.org/wiki/JetBrains) IDEs
- the God-like Windows-only proprietary language-lacking Visual Studio

Programmers of the world: unite! Focus on one IDE, and make it work for all languages and all build systems. Give it all the features that Eclipse has, but none of the bugginess. Work with top project to make sure the IDE works for all top projects.

Projects of the world: support one IDE, with in-tree configuration. Complex integration is often required between the IDE and the build system, and successful projects must to that once for all developers. Either do this, or watch you complex project wither away.

Build tool maintainers: make it possible for IDEs to support your tool! E.g., implement [JSON Compilation Database](https://clang.llvm.org/docs/JSONCompilationDatabase.html) output so that IDEs can read the exact compiler commands from that, in order to automatically determine how files should be parsed! Or better, just use libllvm in your IDE itself as the main parser.

Ciro is evaluating some IDEs at: [https://github.com/cirosantilli/ide-test-projects](https://github.com/cirosantilli/ide-test-projects)

**Table of contents**

- [Text editor](text-editor.md)
  - [JavaScript text editor](javascript-text-editor.md)
    - [Monaco (editor)](monaco-editor.md)
  - [WYSIWYG text editor](wysiwyg-text-editor.md)
    - [JavaScript WYSIWYG text editor](javascript-wysiwyg-text-editor.md)
      - [CKEditor](ckeditor.md)
      - [TinyMCE](tinymce.md)
- [Vim](vim.md)
  - [Gvim](gvim.md)
  - [vader.vim](vader-vim.md)
    - [plasticboy/vim-markdown](plasticboy-vim-markdown.md)
    - [honza/vim-snippets](honza-vim-snippets.md)
    - [Vimium](vimium.md)
- [Eclipse (IDE)](eclipse-ide.md)
- [JetBrains](jetbrains.md)
- [Visual Studio Code](visual-studio-code.md)
  - [vscode freezes or crashes when opening a large folder](vscode-freezes-or-crashes-when-opening-a-large-folder.md)
  - [vscode bug](vscode-bug.md)
  - [vscode Vim](vscode-vim.md)
  - [vscode HOWTO](vscode-howto.md)
    - [vscode jump to definition broken](vscode-jump-to-definition-broken.md)
    - [vscode restore windows after restart](vscode-restore-windows-after-restart.md)

## ↑ Ancestors (6)

1. [Software](software-split.md)
2. [Computer](computer-split.md)
3. [Information technology](information-technology.md)
4. [Area of technology](area-of-technology.md)
5. [Technology](technology-split.md)
6. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (8)

- [Ciro Santilli](ciro-santilli-split.md)
- [Evil](evil.md)
- [Git UI](git-ui.md)
- [Good](good.md)
- [Keep debug notes](keep-debug-notes.md)
- [Numerical computing language](numerical-computing-language.md)
- [Open source video game](open-source-video-game.md)
- [Vim](vim.md)
