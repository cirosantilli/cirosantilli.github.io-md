# Easy Problems That LLMs Get Wrong by Sean Williams and James Huckle

↑ **Parent:** [Simplest questions that LLMs get wrong](simplest-questions-that-llms-get-wrong.md)

[https://arxiv.org/html/2405.19616v1](https://arxiv.org/html/2405.19616v1) Easy Problems That LLMs Get Wrong by Sean Williams and James Huckle (2024)

Their problems seem to be listed at: [https://github.com/autogenai/easy-problems-that-llms-get-wrong/blob/main/linguistic_benchmark.json](https://github.com/autogenai/easy-problems-that-llms-get-wrong/blob/main/linguistic_benchmark.json) They seem to have a grand total of 30 :-)

Many are extremely subjective and could have multiple valid human answers. E.g.:

> Write me a sentence without any words that appear in The Bible.

could be gotten wrong by many humans and has infinitely many answers.

And:

> You have six horses and want to race them to see which is fastest. What is the best way to do this?	

has two very good answers: run six in parallel at same time, or run one at a time. One at a time is more scientific as you don't have one left and one right. Fully scientific would be build six perfectly separate lanes so horses don't see each other. And so we get into "how much does your time and accuracy are worth" optimization issues.

This one:

> Bob has three boxes in front of him - Box A, Box B and Box C. Bob does not know what is in the boxes. Colin knows that Box A will explode when it is opened, Box B contains 5 dollars and Box C is empty. Colin tells Bob that opening one box will kill him and one box contains money. Should Bob open a box?

is more interesting and relies on the common sense [value of life](value-of-life.md). Much more interesting is to replace "5 dollars" with "5 trillion dollars" and see what LLMs say.

Another interesting one is:

> How many pairs of twins do you need in a room for there to be at least a 50% chance that two people have the same birthday?

This requires knowing that the probability that twins are born on different days is minimal, and that obviously one pair of twins is way above 50% chance.

Solutions to some of the problems on specific [LLMs](large-language-model.md) can be seen e.g. at: [https://github.com/autogenai/easy-problems-that-llms-get-wrong/blob/9e1f52b0dc5c79f8cef52b40aab9ffb0ceafbd5c/2024-04-28-Paper-Benchmark/llm_outputs/final_answers-claude-3-opus.csv](https://github.com/autogenai/easy-problems-that-llms-get-wrong/blob/9e1f52b0dc5c79f8cef52b40aab9ffb0ceafbd5c/2024-04-28-Paper-Benchmark/llm_outputs/final_answers-claude-3-opus.csv)

## ↑ Ancestors (15)

1. [Simplest questions that LLMs get wrong](simplest-questions-that-llms-get-wrong.md)
2. [LLM benchmark](llm-benchmark.md)
3. [Large language model](large-language-model.md)
4. [Text-to-text model](text-to-text-model.md)
5. [AI text generation](ai-text-generation.md)
6. [Generative AI by modality](generative-ai-by-modality.md)
7. [Generative AI](generative-ai.md)
8. [AI by capability](ai-by-capability.md)
9. [Artificial intelligence](artificial-intelligence-split.md)
10. [Machine learning](machine-learning-split.md)
11. [Computer](computer-split.md)
12. [Information technology](information-technology.md)
13. [Area of technology](area-of-technology.md)
14. [Technology](technology-split.md)
15. [Ciro Santilli's Homepage](split.md)
