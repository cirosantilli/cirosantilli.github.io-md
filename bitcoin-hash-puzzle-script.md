# Bitcoin hash puzzle script

↑ **Parent:** [Puzzle script](puzzle-script.md)

We've found three unspent puzzle scripts that require finding [SHA-256](sha-256.md) hashes:
```
c4b46c5d88327d7af6254820562327c5f11b6ee5449da04b7cfd3710b48b6f55 0 OP_SHA256 None OP_EQUAL
702c36851ed202495c2bec1dd0cefb448b50fafd3a5cdd5058c18ca53fc2c3d1 0 OP_SHA256 None OP_EQUAL
fb01987b540ec286973aac248fab643de82813af452d958056fee8de9f4535ab 0 OP_SHA256 None OP_EQUAL
```

All three are also mentioned at: [https://bitcoincashresearch.org/t/p2sh32-a-long-term-solution-for-80-bit-p2sh-collision-attacks/750/23](https://bitcoincashresearch.org/t/p2sh32-a-long-term-solution-for-80-bit-p2sh-collision-attacks/750/23) in addition to some `OP_HASH256` ones. The thread manages to identify one of the `OP_HASH256` ones as a fake [Genesis block](genesis-block.md) hash.

They can be viewed disassembled at:
- [https://mempool.space/tx/c4b46c5d88327d7af6254820562327c5f11b6ee5449da04b7cfd3710b48b6f55](https://mempool.space/tx/c4b46c5d88327d7af6254820562327c5f11b6ee5449da04b7cfd3710b48b6f55) hash required: 5efe500c58a4847dab87162f88a79f08249b988265d5061696b5d0c94fd8080d. Mentions:
  - [https://github.com/manly/BlockChainParser/blob/0c65312abfaa659d38bfa465c1413d72284cf30d/Documentation/patterns.txt#L99](https://github.com/manly/BlockChainParser/blob/0c65312abfaa659d38bfa465c1413d72284cf30d/Documentation/patterns.txt#L99)
- [https://mempool.space/tx/702c36851ed202495c2bec1dd0cefb448b50fafd3a5cdd5058c18ca53fc2c3d1](https://mempool.space/tx/702c36851ed202495c2bec1dd0cefb448b50fafd3a5cdd5058c18ca53fc2c3d1) hash required: 3f6d4081222a35483cdf4cefd128167f133c33e1e0f0b1d638be131a14dc2c5e
- [https://mempool.space/tx/fb01987b540ec286973aac248fab643de82813af452d958056fee8de9f4535ab](https://mempool.space/tx/fb01987b540ec286973aac248fab643de82813af452d958056fee8de9f4535ab) hash required: 6380315536fa75ccf0d8180755c9f8106466ee3561405081cab736f49e25baab Mentions:
  - [https://github.com/RKlompUU/SCRIPTAnalyser/blob/398410419e199a3ecb219ebe5fed570a2aabd7bb/scripts/ns10#L1](https://github.com/RKlompUU/SCRIPTAnalyser/blob/398410419e199a3ecb219ebe5fed570a2aabd7bb/scripts/ns10#L1)

They were mined on 01 Apr 2014, 02 Apr 2014 and 03 Apr 2014, suggesting a possible April fool's reference?

Each is worth 0.0002 BTC, which is only 20$ as of 2024, so it's not worth much effort beyond the fun aspect of it. But it is fun!

## ↑ Ancestors (12)

1. [Puzzle script](puzzle-script.md)
2. [Bitcoin script](bitcoin-script.md)
3. [How Bitcoin works](how-bitcoin-works.md)
4. [Bitcoin](bitcoin.md)
5. [List of cryptocurrencies](list-of-cryptocurrencies.md)
6. [Cryptocurrency](cryptocurrency-split.md)
7. [Blockchain](blockchain.md)
8. [Money](money.md)
9. [Social technology](social-technology-split.md)
10. [Area of technology](area-of-technology.md)
11. [Technology](technology-split.md)
12. [Ciro Santilli's Homepage](split.md)
