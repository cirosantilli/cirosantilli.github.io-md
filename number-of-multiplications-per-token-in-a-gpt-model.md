# Number of multiplications per token in a [GPT](generative-pre-trained-transformer.md) model

↑ **Parent:** [Theoretical peak performance of GPT inference](theoretical-peak-performance-of-gpt-inference.md)

The following is for a "classic" [GPT-2](gpt-2.md)-style model, the following estimates the number attention multiplications.

For each layer (L):
- for each attention head (h):
  - K = d\_model \* d\_head (takes embedding of one token and converts to vector of length d\_head)
  - Q = d\_model \* d\_head (same)
  - K Q dot product for attention pattern: n\_ctx \* d\_head (n\_ctx times dot products of vectors of size d\_head, once new K vs every Q. Q vs every K zeroed out by causality.)
  - new value vector for new token: d\_model \* d\_model
  - new updates: n\_ctx \* d\_model (multiply each value vector by the new attention column scalar)
- fully connected: d\_model \* d\_ff + d\_ff \* d\_model (converts the embedding to the hidden layer size and then back)
So the total sum is:
```
L * (
  h * (
    2 * d_model * d_head +
    n_ctx * d_head +
    d_model * d_model +
    n_ctx * d_model
  ) +
  2 * d_model * d_ff
)
```

This is coded at: [llm_count_mults.py](llm_count_mults.py).

Bibliography:
- [https://www.reddit.com/r/theydidthemath/comments/1fzrs1k/request_how_many_individual/](https://www.reddit.com/r/theydidthemath/comments/1fzrs1k/request_how_many_individual/)
- [https://www.gaohongnan.com/playbook/training/how_to_calculate_flops_in_transformer_based_models.html#sanity-check-with-palm-paper-s-flops-calculation](https://www.gaohongnan.com/playbook/training/how_to_calculate_flops_in_transformer_based_models.html#sanity-check-with-palm-paper-s-flops-calculation)

## ↑ Ancestors (16)

1. [Theoretical peak performance of GPT inference](theoretical-peak-performance-of-gpt-inference.md)
2. [GPT model](gpt-model.md)
3. [Generative pre-trained transformer](generative-pre-trained-transformer.md)
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
