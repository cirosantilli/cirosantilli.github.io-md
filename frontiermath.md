# FrontierMath

↑ **Parent:** [List of math AI benchmarks](list-of-math-ai-benchmarks.md)  
🏷️ **Tags:** [Closed source benchmark](closed-source-benchmark.md), [OpenAI project](openai-project.md)

[https://epoch.ai/frontiermath](https://epoch.ai/frontiermath)

Paper: [https://arxiv.org/abs/2411.04872](https://arxiv.org/abs/2411.04872)

[https://arstechnica.com/ai/2024/11/new-secret-math-benchmark-stumps-ai-models-and-phds-alike/](https://arstechnica.com/ai/2024/11/new-secret-math-benchmark-stumps-ai-models-and-phds-alike/) mentions what the official website is unable to clearly state out:

> The design of FrontierMath differs from many existing AI benchmarks because the problem set remains private and unpublished to prevent data contamination

The expected answer output for all problems is one single SymPy expression, which is kind of a cool approach which allows either for large integers like [Project Euler](project-euler-split.md), but also for irrational expressions to be given, e.g. "An optimization problem in BMO space" from the sample problems has answer:

$$
\frac{\sqrt{3}}{36} + \frac{\sqrt{3}}{6} e^{-20\sqrt{3} - \frac{1}{6}}
$$

Of course, when the output is not an integer, this leads to the question of simplification equivalence questions. Also, like [Project Euler](project-euler-split.md), solutions essentially expect you to write and execute code.

The most interesting aspect of this benchmark is the difficulty. [Mathematical olympiad](mathematical-olympiad.md) coach [Evan Chen](evan-chen.md) comments:[https://arstechnica.com/ai/2024/11/new-secret-math-benchmark-stumps-ai-models-and-phds-alike/](https://arstechnica.com/ai/2024/11/new-secret-math-benchmark-stumps-ai-models-and-phds-alike/)

> Problems in \[the [International Mathematical Olympiad](international-mathematical-olympiad.md)\] typically require creative insight while avoiding complex implementation and specialized knowledge \[but for [FrontierMath](frontiermath.md)\] they keep the first requirement, but outright invert the second and third requirement

**Table of contents**

- [Elliot Glazer](elliot-glazer.md)

## ↑ Ancestors (11)

1. [List of math AI benchmarks](list-of-math-ai-benchmarks.md)
2. [Math AI benchmark](math-ai-benchmark.md)
3. [Automated theorem proving](automated-theorem-proving.md)
4. [AI by capability](ai-by-capability.md)
5. [Artificial intelligence](artificial-intelligence-split.md)
6. [Machine learning](machine-learning-split.md)
7. [Computer](computer-split.md)
8. [Information technology](information-technology.md)
9. [Area of technology](area-of-technology.md)
10. [Technology](technology-split.md)
11. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (2)

- [Elliot Glazer](elliot-glazer.md)
- [FrontierMath](frontiermath.md)
