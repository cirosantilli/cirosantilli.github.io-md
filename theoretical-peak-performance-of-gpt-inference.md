# Theoretical peak performance of [GPT](generative-pre-trained-transformer.md) inference

↑ **Parent:** [GPT model](gpt-model.md)

For inferencing just a single prompt, things appear to be very obviously memory bound, i.e. bound by the transfer speeds of [VRAM](video-random-access-memory.md) to GPU cache for loading model parameters into GPU so they can be used, supposing that the model fits in [VRAM](video-random-access-memory.md), which is the case for many popular models.

It is however possible to make fuller utilization of the GPU's compute power by running multiple independent queries in parallel, this way you load the subset of model weights that you need, and then use those to do part of the inference for multiple input prompts. With this it should be possible to reach full utilization.

Bibliography:
- [https://www.reddit.com/r/LocalLLaMA/comments/1brcnps/is_inferencing_memory_bandwidth_limited/](https://www.reddit.com/r/LocalLLaMA/comments/1brcnps/is_inferencing_memory_bandwidth_limited/)
- [https://zeux.io/2024/03/15/llm-inference-sol/](https://zeux.io/2024/03/15/llm-inference-sol/)
8 [https://jax-ml.github.io/scaling-book/](https://jax-ml.github.io/scaling-book/)

**Table of contents**

- [Number of multiplications per token in a GPT model](number-of-multiplications-per-token-in-a-gpt-model.md)

## ↑ Ancestors (15)

1. [GPT model](gpt-model.md)
2. [Generative pre-trained transformer](generative-pre-trained-transformer.md)
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

## ← Incoming links (1)

- [LLM inference batching](llm-inference-batching.md)
