# Cool data embedded in the Bitcoin blockchain

↑ **Parent:** [Bitcoin inscription](bitcoin-inscription.md)  
🏷️ **Tags:** [The best articles by Ciro Santilli](articles-split.md), [Ciro Santilli's data projects](ciro-santilli-s-data-projects.md), [Ciro Santilli's naughty projects](ciro-santilli-s-naughty-projects.md), [Digital preservation](digital-preservation.md), [Inscription (blockchain)](inscription-blockchain.md)

<a id="_7"></a>
This is a collection of cool data found in the Bitcoin blockchain using techniques mentioned at: [Section "How to extract data from the Bitcoin blockchain"](how-to-extract-data-from-the-bitcoin-blockchain.md). Notably, [Ciro Santilli](ciro-santilli-split.md) developed his own set of scripts at [https://github.com/cirosantilli/bitcoin-inscription-indexer](https://github.com/cirosantilli/bitcoin-inscription-indexer) to find some of this data. This article is based on data analyzed up to around block 831k (February 2024).

<a id="_8"></a>
Drop some [Bitcoins](bitcoin.md) at **3KRk7f2JgekF6x7QBqPHdZ3pPDuMdY3eWR** if you are loaded and like this article in order to support some much needed higher educational reform: [Section "Sponsor Ciro Santilli's work on OurBigBook.com"](sponsor-split.md).

<a id="_9"></a>
When this kind of non-financial data is embedded into a blockchain some people called an "[inscription](inscription-blockchain.md)". The study or "early" inscriptions had been called a form of "archaeology"[https://docs.ordinals.com/overview.html](https://docs.ordinals.com/overview.html)[http://blockchainarchaeology.com/](http://blockchainarchaeology.com/). Since this is a collection of archeological artifacts, we call it a "[museum](museum.md)"!

<a id="video-my-bitcoin-inscription-museum-by-ciro-santilli"></a>
**[Video 1](#video-my-bitcoin-inscription-museum-by-ciro-santilli). My Bitcoin inscription museum by Ciro Santilli.** [Source](https://www.youtube.com/watch?v=6XJ6wZBqgUo). Introductory video to this article. Edited from [Aratu Week 2024 Talk by Ciro Santilli: My Best Random Projects](aratu-week-2024-talk-by-ciro-santilli-split.md).

<a id="_10"></a>
One really cool thing about inscriptions is that because blockchains are huge [Merkle trees](merkle-tree.md), it is impossible to censor any one inscription without censoring the entire blockchain. It is also really cool to see people treating the Bitcoin blockchain basically like a global social media feed!

<a id="_11"></a>
Starting on December 2022, [ordinal ruleset inscriptions](cool-data-embedded-in-the-bitcoin-blockchain/ordinal-ruleset-inscription.md) took the bitcoin blockchain by storm, and dwarfed in volume all other previous inscriptions. This museum focuses mostly on non-ordinals, though certain specific ordinal topics that especially interest he curators may be covered, e.g. [Ordinal ruleset inscription porn](cool-data-embedded-in-the-bitcoin-blockchain/ordinal-ruleset-inscription-porn.md) and [ordinal ASCII art inscription](cool-data-embedded-in-the-bitcoin-blockchain/ordinal-ascii-art-inscription.md).

<a id="_12"></a>
[Hidden surprises in the Bitcoin blockchain by Ken Shirriff (2014)](cool-data-embedded-in-the-bitcoin-blockchain/hidden-surprises-in-the-bitcoin-blockchain-by-ken-shirriff-2014.md) is a mandatory precursor to this article and contains the most interesting examples of the time. But much happened since Ken's article which we try to cover. This analysis is also a bit more data oriented through our usage of scripting.

<a id="_13"></a>
Artifacts can be organized in various ways:<a id="_14"></a>

<a id="_15"></a>
- chronologically
<a id="_16"></a>
- by [media type](cool-data-embedded-in-the-bitcoin-blockchain/media-type.md), e.g. [images](cool-data-embedded-in-the-bitcoin-blockchain/images.md) vs [text](cool-data-embedded-in-the-bitcoin-blockchain/text.md)
<a id="_17"></a>
- by [themes](cool-data-embedded-in-the-bitcoin-blockchain/themes.md) or events, e.g. the [Prayer wars](cool-data-embedded-in-the-bitcoin-blockchain/prayer-wars.md) or [Mt. Gox' shutdown](cool-data-embedded-in-the-bitcoin-blockchain/mt-gox-shutdown.md)
<a id="_18"></a>
- encoding, e.g. [AtomSea & EMBII](cool-data-embedded-in-the-bitcoin-blockchain/atomsea-and-embii.md) vs [raw images](cool-data-embedded-in-the-bitcoin-blockchain/raw-images.md)
In this article we've done a mixture of:<a id="_19"></a>

<a id="_20"></a>
- [themes](cool-data-embedded-in-the-bitcoin-blockchain/themes.md): if multiple items fall in a theme, we tend to put it there first
<a id="_21"></a>
- then by [media type](cool-data-embedded-in-the-bitcoin-blockchain/media-type.md) if they don't fit any specific theme
<a id="_22"></a>
- then by encoding
<a id="_23"></a>
- and finally chronologically within each section
Who said it was easy to be a museum curator!

**Table of contents**

- [Media type](cool-data-embedded-in-the-bitcoin-blockchain/media-type.md)
  - [Images](cool-data-embedded-in-the-bitcoin-blockchain/images.md)
    - [ASCII art](cool-data-embedded-in-the-bitcoin-blockchain/ascii-art.md)
      - [Len Sassaman tribute](cool-data-embedded-in-the-bitcoin-blockchain/len-sassaman-tribute.md)
      - [Marijuana plant](cool-data-embedded-in-the-bitcoin-blockchain/marijuana-plant.md)
      - [Force of Will](cool-data-embedded-in-the-bitcoin-blockchain/force-of-will.md)
    - [Custom encoded images of unknown source](cool-data-embedded-in-the-bitcoin-blockchain/custom-encoded-images-of-unknown-source.md)
    - [AtomSea & EMBII](cool-data-embedded-in-the-bitcoin-blockchain/atomsea-and-embii.md)
      - [Early AtomSea & EMBII uploads](cool-data-embedded-in-the-bitcoin-blockchain/early-atomsea-and-embii-uploads.md)
        - [ILoveYouMore.jpg](cool-data-embedded-in-the-bitcoin-blockchain/iloveyoumore-jpg.md)
        - [Nelson-Mandela.jpg](cool-data-embedded-in-the-bitcoin-blockchain/nelson-mandela-jpg.md)
          - [Nelson-Mandela.jpg analysis](cool-data-embedded-in-the-bitcoin-blockchain/nelson-mandela-jpg-analysis.md)
      - [Interesting AtomSea & EMBII uploads](cool-data-embedded-in-the-bitcoin-blockchain/interesting-atomsea-and-embii-uploads.md)
      - [AtomSea & EMBII data format](cool-data-embedded-in-the-bitcoin-blockchain/atomsea-and-embii-data-format.md)
      - [bitfossil.org](cool-data-embedded-in-the-bitcoin-blockchain/bitfossil-org.md)
    - [Raw images](cool-data-embedded-in-the-bitcoin-blockchain/raw-images.md)
      - [cryptograffiti.info](cool-data-embedded-in-the-bitcoin-blockchain/cryptograffiti-info.md)
    - [Ordinal ruleset inscription](cool-data-embedded-in-the-bitcoin-blockchain/ordinal-ruleset-inscription.md)
      - [ordinals.com](cool-data-embedded-in-the-bitcoin-blockchain/ordinals-com.md)
      - [Ordinal ruleset inscription porn](cool-data-embedded-in-the-bitcoin-blockchain/ordinal-ruleset-inscription-porn.md)
      - [Technically interesting ordinal](cool-data-embedded-in-the-bitcoin-blockchain/technically-interesting-ordinal.md)
        - [Largest ordinal inscription](cool-data-embedded-in-the-bitcoin-blockchain/largest-ordinal-inscription.md)
          - [Largest text ordinal inscription](cool-data-embedded-in-the-bitcoin-blockchain/largest-text-ordinal-inscription.md)
            - [Ordinal ASCII art inscription](cool-data-embedded-in-the-bitcoin-blockchain/ordinal-ascii-art-inscription.md)
              - [We are 256, We are 1](cool-data-embedded-in-the-bitcoin-blockchain/we-are-256-we-are-1.md)
        - [Cursed ordinal](cool-data-embedded-in-the-bitcoin-blockchain/cursed-ordinal.md)
      - [Ordinal ruleset inscription collection](cool-data-embedded-in-the-bitcoin-blockchain/ordinal-ruleset-inscription-collection.md)
        - [OnChainMonkey](cool-data-embedded-in-the-bitcoin-blockchain/onchainmonkey.md)
        - [Taproot Wizards](cool-data-embedded-in-the-bitcoin-blockchain/taproot-wizards.md)
  - [Text](cool-data-embedded-in-the-bitcoin-blockchain/text.md)
    - [Software](cool-data-embedded-in-the-bitcoin-blockchain/software.md)
    - [Cute Coinbase messages](cool-data-embedded-in-the-bitcoin-blockchain/cute-coinbase-messages.md)
      - [HHTT](cool-data-embedded-in-the-bitcoin-blockchain/hhtt.md)
    - [Base58 messages](cool-data-embedded-in-the-bitcoin-blockchain/base58-messages.md)
      - [etchablock.com](cool-data-embedded-in-the-bitcoin-blockchain/etchablock-com.md)
    - [Eternity Wall](cool-data-embedded-in-the-bitcoin-blockchain/eternity-wall.md)
    - [Quotes and threes](cool-data-embedded-in-the-bitcoin-blockchain/quotes-and-threes.md)
  - [Encrypted data](cool-data-embedded-in-the-bitcoin-blockchain/encrypted-data.md)
- [Themes](cool-data-embedded-in-the-bitcoin-blockchain/themes.md)
  - [Prayer wars](cool-data-embedded-in-the-bitcoin-blockchain/prayer-wars.md)
  - [Illegal content of block 229k](cool-data-embedded-in-the-bitcoin-blockchain/illegal-content-of-block-229k.md)
  - [Porn](cool-data-embedded-in-the-bitcoin-blockchain/porn.md)
    - [ASCII porn](cool-data-embedded-in-the-bitcoin-blockchain/ascii-porn.md)
  - [Mt. Gox' shutdown](cool-data-embedded-in-the-bitcoin-blockchain/mt-gox-shutdown.md)
  - [Protests against larger block sizes](cool-data-embedded-in-the-bitcoin-blockchain/protests-against-larger-block-sizes.md)
    - [IRC log dumps](cool-data-embedded-in-the-bitcoin-blockchain/irc-log-dumps.md)
  - [503: Bitcoin over capacity](cool-data-embedded-in-the-bitcoin-blockchain/503-bitcoin-over-capacity.md)
  - [Rickrolling](cool-data-embedded-in-the-bitcoin-blockchain/rickrolling.md)
  - [Halving messages](cool-data-embedded-in-the-bitcoin-blockchain/halving-messages.md)
  - [Politics](cool-data-embedded-in-the-bitcoin-blockchain/politics.md)
    - [China](cool-data-embedded-in-the-bitcoin-blockchain/china.md)
    - [Trump](cool-data-embedded-in-the-bitcoin-blockchain/trump.md)
- [Interesting transactions](cool-data-embedded-in-the-bitcoin-blockchain/interesting-transactions.md)
  - [The largest transactions in the Bitcoin Blockchain](cool-data-embedded-in-the-bitcoin-blockchain/the-largest-transactions-in-the-bitcoin-blockchain.md)
- [Bibliography](cool-data-embedded-in-the-bitcoin-blockchain/bibliography.md)
  - [Hidden surprises in the Bitcoin blockchain by Ken Shirriff (2014)](cool-data-embedded-in-the-bitcoin-blockchain/hidden-surprises-in-the-bitcoin-blockchain-by-ken-shirriff-2014.md)
  - [A Quantitative Analysis of the Impact of Arbitrary Blockchain Content on Bitcoin by Matzutt et al. (2018)](cool-data-embedded-in-the-bitcoin-blockchain/a-quantitative-analysis-of-the-impact-of-arbitrary-blockchain-content-on-bitcoin-by-matzutt-et-al-2018.md)
  - [Messages from the mines](cool-data-embedded-in-the-bitcoin-blockchain/messages-from-the-mines.md)
  - [Bitcoin Burn Addresses: Unveiling the Permanent Losses and Their Underlying Causes](cool-data-embedded-in-the-bitcoin-blockchain/bitcoin-burn-addresses-unveiling-the-permanent-losses-and-their-underlying-causes.md)
- [Other blockchains](cool-data-embedded-in-the-bitcoin-blockchain/other-blockchains.md)
- [Incoming links](cool-data-embedded-in-the-bitcoin-blockchain/incoming-links.md)

## 🏷️ Tagged (1)

- [New Bitcoin Base58 messages found due to a new paper: Bitcoin Burn Addresses: Unveiling the Permanent Losses and Their Underlying Causes](updates/new-bitcoin-base58-messages-found-due-to-a-new-paper-bitcoin-burn-addresses-unveiling-the-permanent-losses-and-their-underlying-causes.md)

## ↑ Ancestors (10)

1. [Bitcoin inscription](bitcoin-inscription.md)
2. [Bitcoin](bitcoin.md)
3. [List of cryptocurrencies](list-of-cryptocurrencies.md)
4. [Cryptocurrency](cryptocurrency-split.md)
5. [Blockchain](blockchain.md)
6. [Money](money.md)
7. [Social technology](social-technology-split.md)
8. [Area of technology](area-of-technology.md)
9. [Technology](technology-split.md)
10. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (11)

- [Ciro Santilli's Homepage](split.md)
- [The best articles by Ciro Santilli](articles-split.md)
- [Backward design](backward-design.md)
- [Bitcoin Inscription Indexer](bitcoin-inscription-indexer.md)
- [Exams and homework are useless, only projects matter](how-to-teach/exams-and-homework-are-useless-only-projects-matter.md)
- [Inscription (blockchain)](inscription-blockchain.md)
- [kenorb](kenorb.md)
- [1000 Monero donation](sponsor/1000-monero-donation.md)
- [Getting a list of all currencies from Wikidata with SPARQL](updates/getting-a-list-of-all-currencies-from-wikidata-with-sparql.md)
- [Introductory video for Bitcoin inscription museum](updates/introductory-video-for-bitcoin-inscription-museum.md)
- [New Bitcoin Base58 messages found due to a new paper: Bitcoin Burn Addresses: Unveiling the Permanent Losses and Their Underlying Causes](updates/new-bitcoin-base58-messages-found-due-to-a-new-paper-bitcoin-burn-addresses-unveiling-the-permanent-losses-and-their-underlying-causes.md)
