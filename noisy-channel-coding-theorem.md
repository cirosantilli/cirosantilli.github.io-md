# Noisy-channel coding theorem

↑ **Parent:** [Information theory](information-theory.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Noisy-channel_coding_theorem)

Setting: you are sending bits through a communication channel, each bit has a random probability of getting flipped, and so you use some error correction code to achieve some minimal error, at the expense of longer messages.

This theorem sets an upper bound on how efficient you can be in your encoding, for any encoding.

The next big question, which the theorem does not cover is how to construct codes that reach or approach the limit. Important such codes include:
- [turbo code](turbo-code.md)
- [low-density parity-check code](low-density-parity-check-code.md)

But besides this, there is also the practical consideration of if you can encode/decode fast enough to keep up with the coded bandwidth given your hardware capabilities.

[https://news.mit.edu/2010/gallager-codes-0121](https://news.mit.edu/2010/gallager-codes-0121) explains how turbo codes were first reached without a very good mathematical proof behind them, but were still revolutionary in experimental performance, e.g. turbo codes were used in 3G/4G.

But this motivated researchers to find other such algorithms that they would be able to prove things about, and so they rediscovered the much earlier [low-density parity-check code](low-density-parity-check-code.md), which had been published in the 60's but was forgotten, partially because it was computationally expensive.

**Table of contents**

- [Turbo code](turbo-code.md)
- [Low-density parity-check code](low-density-parity-check-code.md)

## ↑ Ancestors (6)

1. [Information theory](information-theory.md)
2. [Information](information.md)
3. [Information technology](information-technology.md)
4. [Area of technology](area-of-technology.md)
5. [Technology](technology-split.md)
6. [Ciro Santilli's Homepage](split.md)
