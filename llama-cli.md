# llama-cli

↑ **Parent:** [llama.cpp](llama-cpp.md)

A [CLI](command-line-interface.md) front-end for [llama.cpp](llama-cpp.md).

A decent test command as of [llama.cpp](llama-cpp.md) 79e0b68c178656bb0632cb8602d2940b755077f8 tested on [Ubuntu 25.04](ubuntu-25-04.md):
```
git clone https://github.com/ggerganov/llama.cpp
cd llama.cpp
mkdir build
cd build
cmake ..
make -j
cd bin
time ./llama-cli \
  --no-display-prompt \
  --single-turn \
  --temp 0 \
  -c 16384 \
  -cnv \
  -m ~/Downloads/Llama-3.1-Tulu-3-8B-Q8_0.gguf \
  -n 1000 \
  -ngl 100 \
  -p 'What is quantum field theory?' \
  -t 10 |
tee output.txt
```
and that was deterministic due to `--temp 0`.

Also, this command ran 2x faster at 18 tokens/s for 1000 tokens  on [P14s](ciro-santilli-s-hardware/lenovo-thinkpad-p14s-gen4-amd.md) on GPU via Vulkan than on CPU which is achievable by removing the `-ngl 100`.

**Table of contents**

- [llama-cli inference batching](llama-cli-inference-batching.md)

## ↑ Ancestors (16)

1. [llama.cpp](llama-cpp.md)
2. [Ollama](ollama.md)
3. [Open source LLM](open-source-llm.md)
4. [Large language model](large-language-model.md)
5. [Text-to-text model](text-to-text-model.md)
6. [AI text generation](ai-text-generation.md)
7. [Generative AI by modality](generative-ai-by-modality.md)
8. [Generative AI](generative-ai.md)
9. [AI by capability](ai-by-capability.md)
10. [Artificial intelligence](artificial-intelligence-split.md)
11. [Machine learning](machine-learning-split.md)
12. [Computer](computer-split.md)
13. [Information technology](information-technology.md)
14. [Area of technology](area-of-technology.md)
15. [Technology](technology-split.md)
16. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (3)

- [llama-cli inference batching](llama-cli-inference-batching.md)
- [llama.cpp](llama-cpp.md)
- [Ollama deterministic output](ollama-deterministic-output.md)
