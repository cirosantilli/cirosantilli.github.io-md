# Horrors of open source

↑ **Parent:** [Open source software](open-source-software.md)

Not everything is perfect.

One big problem of many big open source projects is that they are contributed to by separate selfish organizations, that have private information. Then what happens is that:
- people implement the same thing twice, or one change makes the other completely unmergeable
- you get bugs but can't share your closed source test cases, and then you can't automate tests for them, or clearly demonstrate the problem
- other contributors don't see your full semi secret important motivation, and may either nitpick too much or take too long to review your stuff

Another common difficulty is that open source maintainers may simply not care enough about their own project (maybe they did in the past but lost interest) to review external patches by people they don't know.

This is understandable: a new patch, is a new risk of things breaking.

Therefore, if you ever submit patches and they get ignore, don't be too sad. It just comes down to a question of maintenance cost, and means that you will waste some extra time on the next rebase. You just have to decide your goals and be cold about it:
- are you doing the right thing and going for a specific goal [backward design](backward-design.md)? Then just fork, run as fast as possible towards a minimum viable product, and if you start to feel that rebase is costing you a lot, or feel you could get some open source fame for cheap, open reviews and see what upstream says. If they ignore you, politely tell yourself in your mind silently "[fuck](sexual-intercourse.md) them", and carry on with the MVP
- otherwise, e.g. you just want to randomly help out, you have to ask them before doing anything big "how can I be of help". If I propose a patch for this issue, do you promise to review it?

Writing documentation in an open source project in which you don't have immediate push rights is another major pain due to code reviews. Code code reviews tend to be much less subjective, because if you do something wrong, stuff crashes, runs slower, or you need more lines of code to reach the same goal. There are tradeoffs, but in a limited number. Documentation code reviews on the other hand, are an open invitation to [infinite bike-shedding](https://en.wikipedia.org/wiki/Law_of_triviality), since you can't "run" documentation through a standardized [brain model](brain-split.md). Much better is for one good documenter person to just make one cohesive [Stack Overflow](stack-overflow-split.md) post, and ping others with more knowledge to review details or add any missing pieces :-)

## ↑ Ancestors (7)

1. [Open source software](open-source-software.md)
2. [Software](software-split.md)
3. [Computer](computer-split.md)
4. [Information technology](information-technology.md)
5. [Area of technology](area-of-technology.md)
6. [Technology](technology-split.md)
7. [Ciro Santilli's Homepage](split.md)
