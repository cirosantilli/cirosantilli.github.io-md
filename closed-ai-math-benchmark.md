# Closed AI math benchmark

↑ **Parent:** [Math AI benchmark](math-ai-benchmark.md)  
🏷️ **Tags:** [Closed source benchmark](closed-source-benchmark.md)

Even more than in other areas of benchmarking, in maths where you only have a right or wrong answer, and it is costly to come up with good sample problems, some benchmarks have adopted private test data sets.

The situation is kind of sad, in that ideally we should have open data sets and only test them on models that were trained on data exclusively published before the problem publish date.

However this is not practical for the following reasons:
- some of the best models are closed source and don't have a reproducible training with specified cutoff
- having a private test set allows you to automatically check answers from untrusted sources. If they get answers right, they are onto something, you don't even need to check their methodology

Perhaps the ideal scenario therefore is what [ARC-AGI](arc-agi.md) has done: give a sizeable public dataset, which you feel is highly representative of the difficulty level of the private test data, while at the same time holding out some private test data. Half half seems reasonable.

This way, reproducible models can actually self test themselves reliably on the open data, while the closed data can then be used for the cases where the open data can't be used.

## ↑ Ancestors (10)

1. [Math AI benchmark](math-ai-benchmark.md)
2. [Automated theorem proving](automated-theorem-proving.md)
3. [AI by capability](ai-by-capability.md)
4. [Artificial intelligence](artificial-intelligence-split.md)
5. [Machine learning](machine-learning-split.md)
6. [Computer](computer-split.md)
7. [Information technology](information-technology.md)
8. [Area of technology](area-of-technology.md)
9. [Technology](technology-split.md)
10. [Ciro Santilli's Homepage](split.md)
