# Ordinal ruleset inscription

↑ **Parent:** [Images](images.md)

<a id="_670"></a>
Ordinals are inscriptions created with the protocol described at: [https://docs.ordinals.com/inscriptions.html](https://docs.ordinals.com/inscriptions.html) The protocol was designed by developer Casey Rodarmor, and shares a few similarities with the [AtomSea & EMBII](atomsea-and-embii.md) protocol.

<a id="_671"></a>
The protocol also includes a way to have ownership over inscriptions, effectively creating an [NFT](../non-fungible-token.md) system on top of the bitcoin blockchain. [AtomSea & EMBII](atomsea-and-embii.md) also already had such a system however. In either case, [Ciro Santilli](../ciro-santilli-split.md) couldn't give less of a fuck about who owns some random publicly viewable digital asset.

<a id="_672"></a>
For whatever reason, orinals became extremelly popular compared to the [AtomSea & EMBII](atomsea-and-embii.md) format, leading to millions os inscriptions, and 10k+ images as of block 830k. They also started to take up a substatial portion of the available block space.

<a id="_673"></a>
This in turn led to a lot of [child porn](../child-pornography.md) rediscussion, and people linking back to this page to view earlier inscriptions: [incoming links](incoming-links.md).<a id="_674"></a>

<a id="_675"></a>
- [https://www.reddit.com/r/Buttcoin/comments/10rbkas/ordinals_nft_was_used_to_store_terrible_porn/](https://www.reddit.com/r/Buttcoin/comments/10rbkas/ordinals_nft_was_used_to_store_terrible_porn/)

<a id="_676"></a>
Unfortunately, unlike [AtomSea & EMBII](atomsea-and-embii.md) and even [cryptograffiti.info](cryptograffiti-info.md) uploads, most ordinals are designed to be just [souless bulk collectibles](ordinal-ruleset-inscription-collection.md), as with as much artistic merit as any random collectible card set or postage stamps you may find at a newpaper stall. To make things worse many of them are likely algorithmically generated. [Eternal September](../eternal-september.md) had truly arrived to the [Bitcoin blockchain](../bitcoin.md). As a result, [machine learning](../machine-learning-split.md) would be almost essential in order to find interesting uploads amidst such bulk.

<a id="_677"></a>
The source code for the reference uploader and indexer is at: [https://github.com/ordinals/ord](https://github.com/ordinals/ord)

<a id="_678"></a>
The reference viewer server for the runs at: [ordinals.com](ordinals-com.md).

<a id="image-ordinal-0"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/6fb976ab49dcec017f1e201e84395983204ae1a7c2abf7ced0a85d692e442799-0.png)

**[Figure 83](#image-ordinal-0). Ordinal \#0**. This is the first [ordinal ruleset inscription](ordinal-ruleset-inscription.md): [https://ordinals.com/inscription/6fb976ab49dcec017f1e201e84395983204ae1a7c2abf7ced0a85d692e442799i0](https://ordinals.com/inscription/6fb976ab49dcec017f1e201e84395983204ae1a7c2abf7ced0a85d692e442799i0). It was made on block 767430 ([2022-12-14](https://www.blockchain.com/explorer/blocks/btc/767430)).

<a id="_679"></a>
The `i0` at the end of the URL above means "inscription 0". This is because a single transaction can have multiple inscriptions.

<a id="_680"></a>
Some of them have sold for high prices. [Magic Eden](../magic-eden.md) is a popular interface for trading them:<a id="_681"></a>

<a id="_682"></a>
- <a id="_683"></a>
  2023-12-08: \#8 was sold dor 10.4 BTC[https://cryptopotato.com/this-bitcoin-ordinals-inscription-was-sold-for-the-highest-price-ever/](https://cryptopotato.com/this-bitcoin-ordinals-inscription-was-sold-for-the-highest-price-ever/) (~$450,000 at the time)

  <a id="image-ordinal-8"></a>
  ![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/d95c0fb86bc0f0dce6a732c5ab77d47e33ed24099bdb01133f768cef75a47724-0.png)

  **[Figure 84](#image-ordinal-8). Ordinal \#8**. On [ordinals.com](ordinals-com.md): [https://ordinals.com/inscription/d95c0fb86bc0f0dce6a732c5ab77d47e33ed24099bdb01133f768cef75a47724i0](https://ordinals.com/inscription/d95c0fb86bc0f0dce6a732c5ab77d47e33ed24099bdb01133f768cef75a47724i0)

<a id="_684"></a>
The ordinals also started taking up large portions of the Bitcoin blockchain:<a id="_685"></a>

<a id="_686"></a>
- [https://dune.com/dataalways/ordinals](https://dune.com/dataalways/ordinals)
<a id="_687"></a>
- [https://research.aimultiple.com/bitcoins-block-space/](https://research.aimultiple.com/bitcoins-block-space/)

<a id="_688"></a>
Apparently the "Taproot" Bitcoin update made it easier to upload image-sized data once again, which had become prohibitively expensive 2023 and much earlier:<a id="_689"></a>

<a id="_690"></a>
- [https://protos.com/did-taproot-ruin-bitcoin-with-nft-inscriptions-of-monkey-jpegs/](https://protos.com/did-taproot-ruin-bitcoin-with-nft-inscriptions-of-monkey-jpegs/)
<a id="_691"></a>
- [https://ordinals.com/](https://ordinals.com/) appears to index some types of ordinals

<a id="_692"></a>
Bibliography:<a id="_693"></a>

<a id="_694"></a>
- [https://blocktelegraph.io/parent-child-bitcoin-inscriptions/](https://blocktelegraph.io/parent-child-bitcoin-inscriptions/) parent-child relationshipsi are possible between two ordinals
<a id="_695"></a>
- [https://ordinals.com/](https://ordinals.com/)
<a id="_696"></a>
- [https://bitcoin.stackexchange.com/questions/117018/understanding-how-ordinals-work-with-the-bitcoin-blockchain-what-is-exactly-sto](https://bitcoin.stackexchange.com/questions/117018/understanding-how-ordinals-work-with-the-bitcoin-blockchain-what-is-exactly-sto)
<a id="_697"></a>
- [https://bitcoin.stackexchange.com/questions/118405/read-ordinal-transaction-data](https://bitcoin.stackexchange.com/questions/118405/read-ordinal-transaction-data)
<a id="_698"></a>
- [https://bitcoin.stackexchange.com/questions/118247/can-someone-explain-the-byte-composition-of-an-inscription-reveal-transaction](https://bitcoin.stackexchange.com/questions/118247/can-someone-explain-the-byte-composition-of-an-inscription-reveal-transaction)
<a id="_699"></a>
- [https://nftnow.com/guides/bitcoin-nfts-most-notable-ordinals-inscriptions/](https://nftnow.com/guides/bitcoin-nfts-most-notable-ordinals-inscriptions/)

**Table of contents**

- [ordinals.com](ordinals-com.md)
- [Ordinal ruleset inscription porn](ordinal-ruleset-inscription-porn.md)
- [Technically interesting ordinal](technically-interesting-ordinal.md)
  - [Largest ordinal inscription](largest-ordinal-inscription.md)
    - [Largest text ordinal inscription](largest-text-ordinal-inscription.md)
      - [Ordinal ASCII art inscription](ordinal-ascii-art-inscription.md)
        - [We are 256, We are 1](we-are-256-we-are-1.md)
  - [Cursed ordinal](cursed-ordinal.md)
- [Ordinal ruleset inscription collection](ordinal-ruleset-inscription-collection.md)
  - [OnChainMonkey](onchainmonkey.md)
  - [Taproot Wizards](taproot-wizards.md)

## ↑ Ancestors (13)

1. [Images](images.md)
2. [Media type](media-type.md)
3. [Cool data embedded in the Bitcoin blockchain](../cool-data-embedded-in-the-bitcoin-blockchain-split.md)
4. [Bitcoin inscription](../bitcoin-inscription.md)
5. [Bitcoin](../bitcoin.md)
6. [List of cryptocurrencies](../list-of-cryptocurrencies.md)
7. [Cryptocurrency](../cryptocurrency-split.md)
8. [Blockchain](../blockchain.md)
9. [Money](../money.md)
10. [Social technology](../social-technology-split.md)
11. [Area of technology](../area-of-technology.md)
12. [Technology](../technology-split.md)
13. [Ciro Santilli's Homepage](../split.md)

## ← Incoming links (9)

- [Cool data embedded in the Bitcoin blockchain](../cool-data-embedded-in-the-bitcoin-blockchain-split.md)
- [ASCII art](ascii-art.md)
- [AtomSea & EMBII](atomsea-and-embii.md)
- [Encrypted data](encrypted-data.md)
- [Incoming links](incoming-links.md)
- [Ordinal ruleset inscription](ordinal-ruleset-inscription.md)
- [Ordinal ruleset inscription collection](ordinal-ruleset-inscription-collection.md)
- [Ordinals.com](ordinals-com.md)
- [Themes](themes.md)
