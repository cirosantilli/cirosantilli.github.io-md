<h1 id="cryptograffiti-info">cryptograffiti.info</h1>

↑ **Parent:** [Raw images](raw-images.md)  
🏷️ **Tags:** [Inscription service](../inscription-service.md)

<a id="_636"></a>
[https://cryptograffiti.info](https://cryptograffiti.info)

<a id="_637"></a>
[https://github.com/1Hyena/cryptograffiti](https://github.com/1Hyena/cryptograffiti)

<a id="_638"></a>
[https://twitter.com/cryptograffiti](https://twitter.com/cryptograffiti) (marked as joined March 2014)

<a id="_639"></a>
Bitcoin blockchain image indexer and uploader. Uses [fake P2PKH address](../fake-p2pkh-address.md).

<a id="_640"></a>
At some point it stopped using Bitcoin mainline and moved to Bitcoin Cash instead: [https://www.newsbtc.com/news/bitcoin/cryptograffiti-rejects-bitcoin-core-bch-now-available-payment-method/](https://www.newsbtc.com/news/bitcoin/cryptograffiti-rejects-bitcoin-core-bch-now-available-payment-method/) and therefore became useless. Existing indexes seem to have been broken as well.

<a id="_641"></a>
Also, based on the timing of [Figure 47. "Erich Erstu"](raw-images.md#image-erich-erstu), this service may be responsible for a large part of the raw JPEG images present in the blockchain from [block 416527](https://www.blockchain.com/btc/block/416527) (2016) onwards. This is also suggested by the comments at [Figure 69. "Tank Man"](raw-images.md#image-tank-man).

<a id="_642"></a>
[A Quantitative Analysis of the Impact of Arbitrary Blockchain Content on Bitcoin](../a-quantitative-analysis-of-the-impact-of-arbitrary-blockchain-content-on-bitcoin.md) gives the interesting insight that all its transactions seem to return change/fees to one or two given addresses, thus making it very easy to list all their uploads if they were consistent! So all we need are some starting points, which we have mostly due to ASCII mentions of the site on known inscriptions, all of which have a few common spent addresses at the very end:<a id="_643"></a>

<a id="_644"></a>
- 4c903a377addab7c1e35a685d3dabc664199e406374b1e5ce2fc59e78fb5b754: [1MVpQJA7FtcDrwKC6zATkZvZcxqma4JixS](../1mvpqja7ftcdrwkc6zatkzvzcxqma4jixs.md)
<a id="_645"></a>
- 87aad85c6cd75a516789f364637d243c668e3424d031ae510e43c6edfe6ed206: [1MVpQJA7FtcDrwKC6zATkZvZcxqma4JixS](../1mvpqja7ftcdrwkc6zatkzvzcxqma4jixs.md)
<a id="_646"></a>
- c206e8fff656f07b27dac831ef9b956792bae4e76a2cb43f14f49f0298bf2c2f: [1MVpQJA7FtcDrwKC6zATkZvZcxqma4JixS](../1mvpqja7ftcdrwkc6zatkzvzcxqma4jixs.md)
<a id="_647"></a>
- ca4f11131eca6b4d61daf707a470cfccd1ef3d80a6f8b70f1f07616b451ca64e: [1MVpQJA7FtcDrwKC6zATkZvZcxqma4JixS](../1mvpqja7ftcdrwkc6zatkzvzcxqma4jixs.md)
so we just have to solve [get all Bitcoin transactions from and to a given address](../get-all-bitcoin-transactions-from-and-to-a-given-address.md) and we are done. [Blockchair](../blockchair.md) shows about 800 entries as of February 2024, between 4f94f97eb156b8563a213bb292314a0bd9c95b39afc521fc5965d050daab2a78 (2014-03-02) and ac5f4ea03597b43a72fb8ab42bd5384629f87f4f4abc534f38b8c15148ccaf9f (2017-10-12): [https://blockchair.com/bitcoin/outputs?s=time(desc)&q=recipient(1MVpQJA7FtcDrwKC6zATkZvZcxqma4JixS)](https://blockchair.com/bitcoin/outputs?s=time(desc)&q=recipient(1MVpQJA7FtcDrwKC6zATkZvZcxqma4JixS))

<a id="_648"></a>
Other related transactions:<a id="_649"></a>

<a id="_650"></a>
- [tx 87aad85c6cd75a516789f364637d243c668e3424d031ae510e43c6edfe6ed206](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0474.txt#L3990) block 474652 (2017-07-07) via [cryptograffiti.info](cryptograffiti-info.md) the default [pandoc](../pandoc.md) [markdown](../markdown.md) [https://pandoc.org/try](https://pandoc.org/try) markdown tutorial string! First, unseen in our ASCII dumps due to [UTF-8](../utf-8.md) encoding::<a id="_651"></a>

  ```
  Unicode test: `Ä Ö Õ Ü ä ö õ ü`.
  ```

  followed by:<a id="_652"></a>

  ```
  An h1 header
  ============

  Paragraphs are separated by a blank line.
  ```

  And if ends with:<a id="_653"></a>

  ```
  Uploaded from http://cryptograffiti.info to demonstrate Markdown rendering.
  ```

<a id="_654"></a>
TODO understand what these are:<a id="_655"></a>

<a id="_656"></a>
- ae92dc4c31943955ad6e3e45a4eb0067f488fdd9aecca65c946460dd2a85488d
<a id="_657"></a>
- 3020dbd7c850bf8c19ebacf670a2830fe50999a8b2560a202af21d536760eea4
<a id="_658"></a>
- d65384a21cb1c327cc42416a0b1e2a78ad0296cb7a15312bdcd67ef169ecb309
<a id="_659"></a>
- a3e3100d2b9a86e310430945c001df97a70626220a9e151208aecbb613f1f152
<a id="_660"></a>
- a9c82ebc47fabd1eed7eeea7760d0a3c99288af3c3a17e396ec790fc280698a2
<a id="_661"></a>
- 92bfd5c0fb0f24efa6ca568c4475f44e94dfc8d0d4d5da04dfafc6261bf17f45
<a id="_662"></a>
- 73c22adb21b93f9220d00d2614a50350824be95b8ea966349e6f35fe5ac5537b
<a id="_663"></a>
- 099c0fd06d18953c886121ff143ea0a20d0baf29999f424fa1ac707a81cf4987
<a id="_664"></a>
- 3ad6677303fb6f700a4f2f977fe86e5324e0ddb0d3b33a649e513d7e88904e85
<a id="_665"></a>
- 31a2ddaf4b146e021246e1f82e28121f5c9c8729620978309004515c7e559910
<a id="_666"></a>
- adaae897fd286aefb64a69e88a53e9af17ee98611ea595c3c92d038f3274d723
<a id="_667"></a>
- d8bf48e9ad3de62c695ff34a96e340912bd62e0a0282b94da6386b837c31a30d

## ↑ Ancestors (14)

1. [Raw images](raw-images.md)
2. [Images](images.md)
3. [Media type](media-type.md)
4. [Cool data embedded in the Bitcoin blockchain](../cool-data-embedded-in-the-bitcoin-blockchain-split.md)
5. [Bitcoin inscription](../bitcoin-inscription.md)
6. [Bitcoin](../bitcoin.md)
7. [List of cryptocurrencies](../list-of-cryptocurrencies.md)
8. [Cryptocurrency](../cryptocurrency-split.md)
9. [Blockchain](../blockchain.md)
10. [Money](../money.md)
11. [Social technology](../social-technology-split.md)
12. [Area of technology](../area-of-technology.md)
13. [Technology](../technology-split.md)
14. [Ciro Santilli's Homepage](../split.md)

## ← Incoming links (14)

- [1MVpQJA7FtcDrwKC6zATkZvZcxqma4JixS](../1mvpqja7ftcdrwkc6zatkzvzcxqma4jixs.md)
- [ASCII art](ascii-art.md)
- [ASCII porn](ascii-porn.md)
- [Cryptograffiti.info](cryptograffiti-info.md)
- [Encrypted data](encrypted-data.md)
- [Force of Will](force-of-will.md)
- [Marijuana plant](marijuana-plant.md)
- [Ordinal ruleset inscription](ordinal-ruleset-inscription.md)
- [Porn](porn.md)
- [Raw images](raw-images.md)
- [Software](software.md)
- [Text](text.md)
- [Themes](themes.md)
- [Inscription service](../inscription-service.md)
