# The development cycle time is your God

↑ **Parent:** [Ciro Santilli's software engineering wisdom](ciro-santilli-s-software-engineering-wisdom.md)

A slow development test cycle will kill your software.

New developers won't want to learn your project, because they would rather shoot themselves.

This means that build time, and the time to run tests, must be short.

5 seconds to rebuild is the maximum upper limit.

Of course, at some point software gets large enough that things won't fit anymore in 5 seconds. But then you _must_ have either some kind of build caching, or options to do partial builds/tests that will bring things down to that 5 second mark.

You also have to spend some time profiling execution and build from scratch times.

A slow build from scratch will mean that your [continuous integration](continuous-integration.md) costs a lot, money that could be invested in a new developer!

It also means that people won't bother to reproduce bugs on given commits, or [bisect stuff](bisection-software-engineering.md).

One anecdote comes to mind. [Ciro Santilli](ciro-santilli-split.md) was trying to debug something, and more experience colleague came over.

To reproduce a problem, ciro was running one command, wait 5 seconds, run a second command, wait 5 seconds, run a third command:
```
cmd1
# wait 5 seconds
cmd2
# wait 5 seconds
cmd3
```

The first thing the colleague said: join those three commands into one:
```
cmd1;cmd2;cmd3
```
And so, [Ciro was enlightened](the-correlation-between-software-engineers-and-buddhism.md).

<a id="image-xkcd-303-compiling"></a>
![](https://web.archive.org/web/20220930224719im_/https://imgs.xkcd.com/comics/compiling.png)

**[Figure 4](#image-xkcd-303-compiling). xkcd 303: Compiling**. [Source](https://xkcd.com/303/). They should be benchmarking and fixing their shitty build system instead.

## ↑ Ancestors (8)

1. [Ciro Santilli's software engineering wisdom](ciro-santilli-s-software-engineering-wisdom.md)
2. [Software engineering](software-engineering.md)
3. [Software](software-split.md)
4. [Computer](computer-split.md)
5. [Information technology](information-technology.md)
6. [Area of technology](area-of-technology.md)
7. [Technology](technology-split.md)
8. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (3)

- [Effortless effort](effortless-effort.md)
- [JCVI-syn3A](jcvi-syn3a.md)
- [The perfect video game is an infinitely hard one](the-perfect-video-game-is-an-infinitely-hard-one.md)
