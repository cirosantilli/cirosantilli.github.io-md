# Daisy chain Bitcoin inscription

↑ **Parent:** [Bitcoin inscription method](bitcoin-inscription-method.md)

This is a term invented by [Ciro Santilli](ciro-santilli-split.md), and refers to a loose set of uncommon [Bitcoin inscription methods](bitcoin-inscription-method.md) that involve inscribing one or a small number of payloads per [Bitcoin transaction](bitcoin-transaction.md).

These methods are both inefficient and hard to detect and decode, partly because [Bitcoin Core](bitcoin-core.md) does not index spending transactions: [https://bitcoin.stackexchange.com/questions/61794/bitcoin-rpc-how-to-find-the-transaction-that-spends-a-txo](https://bitcoin.stackexchange.com/questions/61794/bitcoin-rpc-how-to-find-the-transaction-that-spends-a-txo). This makes finding them all that more rewarding however.

On the other hand, they do have the advantage of not depending on any block size limits, as their individual transactions are very small.

Inscribing anything large would however take a very long time, as you'd have to wait until the previous payload chunk is confirmed before going to the next one. This alone makes the format impractical perhaps.

Known examples:
- [Figure "Iranian lady with polar bear hat."](cool-data-embedded-in-the-bitcoin-blockchain/raw-images.md#image-iranian-lady-with-polar-bear-hat)
- [Figure "The Economist logo"](cool-data-embedded-in-the-bitcoin-blockchain/raw-images.md#image-the-economist-logo)

## ↑ Ancestors (11)

1. [Bitcoin inscription method](bitcoin-inscription-method.md)
2. [Bitcoin inscription](bitcoin-inscription.md)
3. [Bitcoin](bitcoin.md)
4. [List of cryptocurrencies](list-of-cryptocurrencies.md)
5. [Cryptocurrency](cryptocurrency-split.md)
6. [Blockchain](blockchain.md)
7. [Money](money.md)
8. [Social technology](social-technology-split.md)
9. [Area of technology](area-of-technology.md)
10. [Technology](technology-split.md)
11. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (1)

- [Raw images](cool-data-embedded-in-the-bitcoin-blockchain/raw-images.md)
