# Test driven development

↑ **Parent:** [Software testing](software-testing.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Test_driven_development)

This is a good approach. The downside is that while you are developing the implementation and testing interactively you might notice that the requirements are wrong, and then the tests have to change.

One intermediate approach [Ciro Santilli](ciro-santilli-split.md) likes is to do the implementation and be happy with interactive usage, then create the test, make it pass, then remove the code that would make it pass, and see it fail. This does have a risk that you will forget to test something, but Ciro finds it is a worth it generally. Unless it really is one of those features that you are unable to develop without an automated test, generally more "logical/mathematical" stuff. This is a sort of [laziness Driven Development](laziness-driven-development.md).

**Table of contents**

- [Laziness Driven Development](laziness-driven-development.md)

## ↑ Ancestors (8)

1. [Software testing](software-testing.md)
2. [Software quality assurance](software-quality-assurance.md)
3. [Software](software-split.md)
4. [Computer](computer-split.md)
5. [Information technology](information-technology.md)
6. [Area of technology](area-of-technology.md)
7. [Technology](technology-split.md)
8. [Ciro Santilli's Homepage](split.md)
