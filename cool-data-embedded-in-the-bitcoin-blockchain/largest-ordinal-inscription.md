# Largest ordinal inscription

↑ **Parent:** [Technically interesting ordinal](technically-interesting-ordinal.md)

<a id="_774"></a>
We can get a list of the ordinals at: [https://archive.org/details/bitcoin-ordinal-inscriptions.csv](https://archive.org/details/bitcoin-ordinal-inscriptions.csv) and then sort them by payload size with:<a id="_775"></a>

```
sort -k6 -n -t, ordinals.csv -o ordinals-sort-size.csv
```

<a id="_776"></a>
This shows to us that as of block ~831k, there are 4 ordinals which are far far larger than any other between 3 MiB and 4 MiB, at about 10x larger than then 5th one d115a6e689086fd587e5032f24ba2a8c01f2f87cba758c9d5eb8cf7f6e9a816a

<a id="_777"></a>
In those cases, a single inscription takes almost the entire block, and the inscribers must have had direct dealings with their mining pool:<a id="_778"></a>

<a id="_779"></a>
- [https://ordinals.com/inscription/4af9047d8b4b6ffffaa5c74ee36d0506a6741ba6fc6b39fe20e4e08df799cf99i0](https://ordinals.com/inscription/4af9047d8b4b6ffffaa5c74ee36d0506a6741ba6fc6b39fe20e4e08df799cf99i0): 3,946,469 bytes (image/jpeg). [Bitcoin Magazine](https://ourbigbook.com/go/topic/bitcoin-magazine) cover showing the face of [Julian Assange](https://ourbigbook.com/go/topic/julian-assange). [tx 4af9047d8b4b6ffffaa5c74ee36d0506a6741ba6fc6b39fe20e4e08df799cf99](https://www.blockchain.com/explorer/transactions/btc/4af9047d8b4b6ffffaa5c74ee36d0506a6741ba6fc6b39fe20e4e08df799cf99) block 786501 (2023-04-22). Mined by [Terra Pool](https://ourbigbook.com/go/topic/terra-pool).
<a id="_780"></a>
- [https://ordinals.com/inscription/0301e0480b374b32851a9462db29dc19fe830a7f7d7a88b81612b9d42099c0aei0](https://ordinals.com/inscription/0301e0480b374b32851a9462db29dc19fe830a7f7d7a88b81612b9d42099c0aei0): 3,915,537 bytes (image/jpeg). [Taproot Wizards](taproot-wizards.md) ad. This was apparently the largest block ever mined at the time: [https://www.reddit.com/r/Bitcoin/comments/10r6t1l/the_first_4_mb_block_in_bitcoin_history_mined_by/](https://www.reddit.com/r/Bitcoin/comments/10r6t1l/the_first_4_mb_block_in_bitcoin_history_mined_by/) and received some notice. [tx 0301e0480b374b32851a9462db29dc19fe830a7f7d7a88b81612b9d42099c0ae](https://www.blockchain.com/explorer/transactions/btc/0301e0480b374b32851a9462db29dc19fe830a7f7d7a88b81612b9d42099c0ae) block 774628 (2023-02-01). Mined by Luxor pool.<a id="image-ordinal-652"></a>
  ![](https://web.archive.org/web/20230511232827im_/https://ordinals.com/content/0301e0480b374b32851a9462db29dc19fe830a7f7d7a88b81612b9d42099c0aei0)

  **[Figure 85](#image-ordinal-652). Ordinal \#652**. [Source](https://ordinals.com/inscription/0301e0480b374b32851a9462db29dc19fe830a7f7d7a88b81612b9d42099c0aei0).
<a id="_781"></a>
- [https://ordinals.com/inscription/79b91e594c03c8f06d70c44a288a88a413c540abca007829ca119686a7f979dai0](https://ordinals.com/inscription/79b91e594c03c8f06d70c44a288a88a413c540abca007829ca119686a7f979dai0): 3,878,842 bytes (image/webp). "Bitcoin War Bonds". A spoof of something. No time to understand now. [tx 79b91e594c03c8f06d70c44a288a88a413c540abca007829ca119686a7f979da](https://www.blockchain.com/explorer/transactions/btc/79b91e594c03c8f06d70c44a288a88a413c540abca007829ca119686a7f979da) block 777945 (2023-02-23). Mined by [Terra Pool](https://ourbigbook.com/go/topic/terra-pool).
<a id="_782"></a>
- [https://ordinals.com/inscription/b5a7e05f28d00e4a791759ad7b6bd6799d856693293ceeaad9b0bb93c8851f7fi0](https://ordinals.com/inscription/b5a7e05f28d00e4a791759ad7b6bd6799d856693293ceeaad9b0bb93c8851f7fi0): 3,379,682 bytes (video/mp4). Short looping video of a "purple frog drinking from a glass with a straw". Yes you heard that right. TODO context? [tx b5a7e05f28d00e4a791759ad7b6bd6799d856693293ceeaad9b0bb93c8851f7f](https://www.blockchain.com/explorer/transactions/btc/b5a7e05f28d00e4a791759ad7b6bd6799d856693293ceeaad9b0bb93c8851f7f) block 776884 (2023-02-16 ) Despite being huge, this received very little attention, the only [Google](../google-split.md) mention is at [An overview of recent non-standard Bitcoin transactions by 0xB10C](../an-overview-of-recent-non-standard-bitcoin-transactions-by-0xb10c.md). Mined by [Terra Pool](https://ourbigbook.com/go/topic/terra-pool).

<a id="_783"></a>
As of 2024, all of the big ones were made in early 2023, so it seems that the trend has died down a bit.

**Table of contents**

- [Largest text ordinal inscription](largest-text-ordinal-inscription.md)
  - [Ordinal ASCII art inscription](ordinal-ascii-art-inscription.md)
    - [We are 256, We are 1](we-are-256-we-are-1.md)

## ↑ Ancestors (15)

1. [Technically interesting ordinal](technically-interesting-ordinal.md)
2. [Ordinal ruleset inscription](ordinal-ruleset-inscription.md)
3. [Images](images.md)
4. [Media type](media-type.md)
5. [Cool data embedded in the Bitcoin blockchain](../cool-data-embedded-in-the-bitcoin-blockchain-split.md)
6. [Bitcoin inscription](../bitcoin-inscription.md)
7. [Bitcoin](../bitcoin.md)
8. [List of cryptocurrencies](../list-of-cryptocurrencies.md)
9. [Cryptocurrency](../cryptocurrency-split.md)
10. [Blockchain](../blockchain.md)
11. [Money](../money.md)
12. [Social technology](../social-technology-split.md)
13. [Area of technology](../area-of-technology.md)
14. [Technology](../technology-split.md)
15. [Ciro Santilli's Homepage](../split.md)
