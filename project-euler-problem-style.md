# Project Euler problem style

↑ **Parent:** [Project Euler](project-euler-split.md)

[Project Euler](project-euler-split.md) problems typically involve finding or proving and then using a [lemma](lemma-mathematics.md) that makes computation of the solution feasible without brute force. There is often an obvious brute force approach, but the pick problem sizes large enough such that it is just not fast enough, but the non-brute-force is.

As such, they live in the intersection of [mathematics](mathematics-split.md) and [computer science](computer-science-split.md).

[https://news.ycombinator.com/item?id=7057408](https://news.ycombinator.com/item?id=7057408) which is mega high on [Google](google-split.md) says:

> I love project euler, but I've come to the realization that its purpose is to beat programmers soundly about the head and neck with a big math stick. At work last week, we were working on project euler at lunch, and had the one CS PhD in our midst not jumped up and explained the chinese remainder theorem to us, we wouldn't have had a chance.

In many cases, the efficient solution involves [dynamic programming](dynamic-programming.md).

There are also a set of problems which are very [numerical analysis](numerical-analysis.md) in nature and require the approximation of some [real number](real-number.md) to a given precision. These are often very fiddly as I doubt most people can prove that their chosen [hyperparameters](hyperparameter.md) guarantee the required precision.

Many problems ask for solution modulo some number. In general, this is only so that C/C++ users won't have to resort to using an [arbitrary-precision arithmetic](arbitrary-precision-arithmetic.md) library and be able to fit everything into `uint64` instead. Maybe it also helps the judge system slightly having smaller strings to compare. The final modulos usually don't add any insight to the problems.

Bibliography:
- [https://www.reddit.com/r/cscareerquestions/comments/620u4x/what_are_peoples_thoughts_on_project_euler/](https://www.reddit.com/r/cscareerquestions/comments/620u4x/what_are_peoples_thoughts_on_project_euler/) What are peoples thoughts on Project Euler?

## ↑ Ancestors (12)

1. [Project Euler](project-euler-split.md)
2. [Exercism](exercism.md)
3. [Competitive programming website](competitive-programming-website.md)
4. [Competitive programming](competitive-programming.md)
5. [Knowledge olympiad by domain of knowledge](knowledge-olympiad-by-domain-of-knowledge.md)
6. [Knowledge olympiad](knowledge-olympiad.md)
7. [STEM prize](stem-prize.md)
8. [Prize](prize.md)
9. [Social technology](social-technology-split.md)
10. [Area of technology](area-of-technology.md)
11. [Technology](technology-split.md)
12. [Ciro Santilli's Homepage](split.md)
