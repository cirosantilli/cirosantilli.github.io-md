# The largest transactions in the Bitcoin Blockchain

↑ **Parent:** [Interesting transactions](interesting-transactions.md)

<a id="_1573"></a>
[https://bitcoin.stackexchange.com/questions/11542/by-byte-size-and-number-of-inputs-outputs-what-are-the-largest-transactions-in/105384#105384](https://bitcoin.stackexchange.com/questions/11542/by-byte-size-and-number-of-inputs-outputs-what-are-the-largest-transactions-in/105384#105384)

<a id="_1574"></a>
<a id="_1575"></a>
- bb41a757f405890fb0f5856228e23b715702d714d59bf2b1feb70d8b2b4e3e08 999,657 bytes. Joins a bunch of tiny inputs into a single output
<a id="_1576"></a>
- 623463a2a8a949e0590ffe6b2fd3e4e1028b2b99c747e82e899da4485eb0b6be and 5143cf232576ae53e8991ca389334563f14ea7a7c507a3e081fbef2538c84f6e both have 3,075 outputs of 1 satoshi each and a single input. We were not able to identify any meaningful data in it, `file` just says `data`, and there aren't long ASCII strings. However, the outputs were unspent as of 2021, which suggests that they might actually be data.

<a id="_1577"></a>
Analysis of some of them follows.

<a id="_1578"></a>
<a id="_1579"></a>
- dd9f6bbf80ab36b722ca95d93268667a3ea6938288e0d4cf0e7d2e28a7a91ab3 has 13107 with payload 256KB in size, but some of them at least have been spent: [https://www.blockchain.com/btc/tx/dd9f6bbf80ab36b722ca95d93268667a3ea6938288e0d4cf0e7d2e28a7a91ab3](https://www.blockchain.com/btc/tx/dd9f6bbf80ab36b722ca95d93268667a3ea6938288e0d4cf0e7d2e28a7a91ab3) therefore it's not data. `file` says their payload is a DOS executable, but it must be a coincidence

## ↑ Ancestors (12)

1. [Interesting transactions](interesting-transactions.md)
2. [Cool data embedded in the Bitcoin blockchain](../cool-data-embedded-in-the-bitcoin-blockchain-split.md)
3. [Bitcoin inscription](../bitcoin-inscription.md)
4. [Bitcoin](../bitcoin.md)
5. [List of cryptocurrencies](../list-of-cryptocurrencies.md)
6. [Cryptocurrency](../cryptocurrency-split.md)
7. [Blockchain](../blockchain.md)
8. [Money](../money.md)
9. [Social technology](../social-technology-split.md)
10. [Area of technology](../area-of-technology.md)
11. [Technology](../technology-split.md)
12. [Ciro Santilli's Homepage](../split.md)
