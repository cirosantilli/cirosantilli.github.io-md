# LLM inference batching

↑ **Parent:** [LLM inference optimization](llm-inference-optimization.md)

[LLM inference batching](llm-inference-batching.md) means running multiple independent queries in parallel on a given model.

This can be used to overcome the fact that most single prompt inference will be heavily [memory bound](memory-bound.md), see also: [Section "Theoretical peak performance of GPT inference"](theoretical-peak-performance-of-gpt-inference.md). Batching helps increase the GPU compute utilization and balance it out with the memory.

Bibliography:
- [https://medium.com/@yohoso/llm-inference-optimisation-continuous-batching-2d66844c19e9](https://medium.com/@yohoso/llm-inference-optimisation-continuous-batching-2d66844c19e9)
- [https://www.hyperstack.cloud/technical-resources/tutorials/static-vs.-continuous-batching-for-large-language-model-inference](https://www.hyperstack.cloud/technical-resources/tutorials/static-vs.-continuous-batching-for-large-language-model-inference)

## 🏷️ Tagged (1)

- [llama-cli inference batching](llama-cli-inference-batching.md)

## ↑ Ancestors (14)

1. [LLM inference optimization](llm-inference-optimization.md)
2. [Large language model](large-language-model.md)
3. [Text-to-text model](text-to-text-model.md)
4. [AI text generation](ai-text-generation.md)
5. [Generative AI by modality](generative-ai-by-modality.md)
6. [Generative AI](generative-ai.md)
7. [AI by capability](ai-by-capability.md)
8. [Artificial intelligence](artificial-intelligence-split.md)
9. [Machine learning](machine-learning-split.md)
10. [Computer](computer-split.md)
11. [Information technology](information-technology.md)
12. [Area of technology](area-of-technology.md)
13. [Technology](technology-split.md)
14. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (1)

- [LLM inference batching](llm-inference-batching.md)
