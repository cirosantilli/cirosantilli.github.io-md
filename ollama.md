# Ollama

↑ **Parent:** [Open source LLM](open-source-llm.md)  
🏷️ **Tags:** [Good](good.md)

[https://github.com/jmorganca/ollama](https://github.com/jmorganca/ollama)

[Ollama](ollama.md) is a highly automated open source wrapper that makes it very easy to run multiple [Open weight LLM models](open-weight-llm-model.md) either on [CPU](central-processing-unit.md) or [GPU](graphics-processing-unit.md).

Its README alone is of great value, serving as a fantastic list of the most popular [Open weight LLM models](open-weight-llm-model.md) in existence.

Install with:
```
curl https://ollama.ai/install.sh | sh
```

The below was tested on Ollama 0.1.14 from December 2013.

Download [llama2 7B](llama-2-7b.md) and open a prompt:
```
ollama run llama2
```

On [P14s](ciro-santilli-s-hardware/lenovo-thinkpad-p14s-gen4-amd.md) it runs on [CPU](central-processing-unit.md) and generates a few tokens per second, which is quite usable for a quick interactive play.

As mentioned at [https://github.com/jmorganca/ollama/blob/0174665d0e7dcdd8c60390ab2dd07155ef84eb3f/docs/faq.md](https://github.com/jmorganca/ollama/blob/0174665d0e7dcdd8c60390ab2dd07155ef84eb3f/docs/faq.md) the downloads to under `/usr/share/ollama/.ollama/models/` and [ncdu](ncdu.md) tells me:
```
--- /usr/share/ollama ----------------------------------
    3.6 GiB [###########################] /.ollama
    4.0 KiB [                           ]  .bashrc
    4.0 KiB [                           ]  .profile
    4.0 KiB [                           ]  .bash_logout
```
The file:
```
/usr/share/ollama/.ollama/models/manifests/hf.co/mlabonne/Meta-Llama-3.1-8B-Instruct-abliterated-GGUF/Q2_K
```
gives a the exact model name and parameters.

We can also do it non-interactively with:
```
/bin/time ollama run llama2 'What is quantum field theory?'
```
which gave me:
```
0.13user 0.17system 2:06.32elapsed 0%CPU (0avgtext+0avgdata 17280maxresident)k
0inputs+0outputs (0major+2203minor)pagefaults 0swaps
```
but note that there is a random seed that affects each run by default. [ollama-expect](_file/ollama-expect.md) is an attempt to make the output deterministic.

Some other quick benchmarks from [Amazon EC2 GPU](amazon-ec2-gpu.md) on a [g4nd.xlarge](g4nd-xlarge.md) instance which had an [Nvidia Tesla T4](nvidia-t4.md):
```
0.07user 0.05system 0:16.91elapsed 0%CPU (0avgtext+0avgdata 16896maxresident)k
0inputs+0outputs (0major+1960minor)pagefaults 0swaps
```
and on [Nvidia A10G](nvidia-a10g.md) in an [g5.xlarge](g5-xlarge.md) instance:
```
0.03user 0.05system 0:09.59elapsed 0%CPU (0avgtext+0avgdata 17312maxresident)k
8inputs+0outputs (1major+1934minor)pagefaults 0swaps
```

So it's not too bad, a small article in 10s.

It tends to babble quite a lot by default, but eventually decides to stop.

**Table of contents**

- [llama.cpp](llama-cpp.md)
  - [llama-cli](llama-cli.md)
    - [llama-cli inference batching](llama-cli-inference-batching.md)
- [Ollama HOWTO](ollama-howto.md)
  - [Ollama output size](ollama-output-size.md)
  - [Ollama deterministic output](ollama-deterministic-output.md)
- [Ollama parameter](ollama-parameter.md)
  - [Ollama set parameter on CLI](ollama-set-parameter-on-cli.md)
    - [ollama-expect](_file/ollama-expect.md)

## ↑ Ancestors (14)

1. [Open source LLM](open-source-llm.md)
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

## ← Incoming links (4)

- [Amazon EC2 GPU](amazon-ec2-gpu.md)
- [llama.cpp](llama-cpp.md)
- [Mlabonne/Meta-Llama-3.1-8B-Instruct-abliterated-GGUF ](mlabonne-meta-llama-3-1-8b-instruct-abliterated-gguf.md)
- [Ollama](ollama.md)
