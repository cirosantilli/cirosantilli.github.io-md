# Eternity Wall

↑ **Parent:** [Text](text.md)  
🏷️ **Tags:** [Inscription service](../inscription-service.md)

<a id="_1207"></a>
[https://eternitywall.it](https://eternitywall.it)

<a id="_1208"></a>
This website used to allow embedding text messages with [OP\_RETURN](../op-return.md), here's an archive from 2015: [https://web.archive.org/web/20150718052659/http://eternitywall.it/](https://web.archive.org/web/20150718052659/http://eternitywall.it/)

<a id="_1209"></a>
As of January 2024, it seems to read-only mode, where it simply indexes matching transactions that were made via other means: [https://web.archive.org/web/20230929075331/https://eternitywall.it/](https://web.archive.org/web/20230929075331/https://eternitywall.it/)

<a id="_1210"></a>
A [Reddit](../reddit.md) announcement from July 2015: [https://www.reddit.com/r/Bitcoin/comments/3dxy9f/eternity_wall_messages_lasting_forever/](https://www.reddit.com/r/Bitcoin/comments/3dxy9f/eternity_wall_messages_lasting_forever/)

<a id="_1211"></a>
There were 3191 hits for the search term:<a id="_1212"></a>

```
git grep '\bEW '
```
in our data starting with [tx a3b3af21514bd79a4cbcac9916a8514636a72d813539192214542fd85247082e](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0362.txt#L966) ([2015-06-24](https://www.blockchain.com/explorer/transactions/btc/a3b3af21514bd79a4cbcac9916a8514636a72d813539192214542fd85247082e)):<a id="_1213"></a>


> EW Eternity wall is live

up to the last entry on [tx 28820bc14cf2cfda58ecbc9ac6df3f41a1cb90f4246543f01ba42a5e9dac3cf8](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0794.txt#L4692) ([2023-06-15](https://www.blockchain.com/explorer/transactions/btc/28820bc14cf2cfda58ecbc9ac6df3f41a1cb90f4246543f01ba42a5e9dac3cf8))<a id="_1214"></a>


> EW May our friendship endure, signed by hg, kty, wjj, and xyz.

no doubt initials of 4 [Chinese](../china-split.md)people. A [blood brother](../blood-brother.md) oath comes to mind, akin to the [Oath of the Peach Garden](../oath-of-the-peach-garden.md). Will these four be the ones to take down the evil dictator [Xi Jinping](../xi-jinping.md)?

<a id="_1215"></a>
The very first message gives away the name of what we assume is a web-based upload system, "EW" being its [advertisement](../advertisement.md) signature added to every message.

<a id="_1216"></a>
Running [`bitcoin-cli`](../bitcoin-cli-client.md):<a id="_1217"></a>

```
bitcoin-core.cli getrawtransaction a3b3af21514bd79a4cbcac9916a8514636a72d813539192214542fd85247082e true
```
shows that the messages are encoded with [OP\_RETURN](../op-return.md):<a id="_1218"></a>

```
  "vout": [
    {
      "value": 0.00000000,
      "n": 0,
      "scriptPubKey": {
        "asm": "OP_RETURN 455720457465726e6974792077616c6c206973206c697665
```

## ↑ Ancestors (13)

1. [Text](text.md)
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

## ← Incoming links (1)

- [Themes](themes.md)
