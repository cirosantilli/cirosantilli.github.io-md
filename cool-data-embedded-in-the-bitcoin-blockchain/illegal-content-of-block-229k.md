# Illegal content of block 229k

↑ **Parent:** [Themes](themes.md)

<a id="_1406"></a>
These can be viewed at [https://bitcoinstrings.com/blk00052.txt](https://bitcoinstrings.com/blk00052.txt) and are mostly commented on the "Wikileaks cablegate data" section of [Hidden surprises in the Bitcoin blockchain by Ken Shirriff (2014)](hidden-surprises-in-the-bitcoin-blockchain-by-ken-shirriff-2014.md).

<a id="_1407"></a>
Soon after block 229991 uploaded the [Satoshi uploader](../satoshi-uploader.md), several interesting files were added to the blockchain using the uploader, and notably some containing content that might be [illegal](../law-split.md) in certain [countries](../country.md), as a test to see if this type of content would make the Bitcoin blockchain illegal or not:<a id="_1408"></a>

<a id="_1409"></a>
- [tx 08654f9dc9d673b3527b48ad06ab1b199ad47b61fd54033af30c2ee975c588bd](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0229.txt#L241) block 229999 contains a leaked private key and a link to: [http://threatpost.com/en_us/blogs/ami-firmware-source-codAe-private-key-leaked-040513](http://threatpost.com/en_us/blogs/ami-firmware-source-codAe-private-key-leaked-040513)
<a id="_1410"></a>
- <a id="_1411"></a>
  [tx b96af3b69b48a82c5eae3e44ebb6ef93f30d7764b1d5b40243e11b0d374ac1b7](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0230.txt#L1) block 230001 contains the link:<a id="_1412"></a>


  > [http://en.wikipedia.org/wiki/Illegal_prime](http://en.wikipedia.org/wiki/Illegal_prime)

  followed presumably by one such prime starting with:<a id="_1413"></a>


  > 4 85650 78965 73978 29309 84189 46942 86137 70744 20873 51357 92401 96520 73668

  The number is quoted e.g. at: [https://www.computerforum.com/threads/illegal-prime-number.67782/](https://www.computerforum.com/threads/illegal-prime-number.67782/)<a id="_1414"></a>

  <a id="_1415"></a>
  - [tx 237783998a6799264983150187a73ab6d116f2ba78d3e1f88529e95229f59d67](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0233.txt#L2) [block 233620](https://www.blockchain.com/explorer/transactions/btc/237783998a6799264983150187a73ab6d116f2ba78d3e1f88529e95229f59d67) contains another illegal prime starting with:

  <a id="_1416"></a>
  <a id="_1417"></a>


  > 49310 83597 02850 19002 75777 67239 07649 57284

  This one is quoted in a few places online in blockchain illegality discussions:<a id="_1418"></a>

  <a id="_1419"></a>
  - [https://www.reddit.com/r/Bitcoin/comments/1akyy4/comment/c8yel60](https://www.reddit.com/r/Bitcoin/comments/1akyy4/comment/c8yel60) "What happens if someone inserts illegal content into the block chain?" (2013-03-19)
  <a id="_1420"></a>
  - [https://news.ycombinator.com/item?id=8055243](https://news.ycombinator.com/item?id=8055243) "Filecoin – Data storage network and crypto-currency based on Bitcoin" (2014-07-18)
<a id="_1421"></a>
- [tx 54e48e5f5c656b26c3bca14a8c95aa583d07ebe84dde3b7dd4a78f4e4186e713](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0230.txt#L7) block 230009 contains the Bitcoin white paper: [https://bitcoin.org/bitcoin.pdf](https://bitcoin.org/bitcoin.pdf) More context: [https://bitcoin.stackexchange.com/questions/35959/how-is-the-whitepaper-decoded-from-the-blockchain-tx-with-1000x-m-of-n-multisi](https://bitcoin.stackexchange.com/questions/35959/how-is-the-whitepaper-decoded-from-the-blockchain-tx-with-1000x-m-of-n-multisi)
<a id="_1422"></a>
- [tx 691dd277dc0e90a462a3d652a1171686de49cf19067cd33c7df0392833fb986a](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0230.txt#L557) block 230203 [Cablegate](../united-states-diplomatic-cables-leak.md) index. The announced filename is `cablegate-201012041811.7z`. As mentioned in [Hidden surprises in the Bitcoin blockchain by Ken Shirriff (2014)](hidden-surprises-in-the-bitcoin-blockchain-by-ken-shirriff-2014.md), it has an ASCII list of several other transactions, which presumably when downloaded with the [Satoshi uploader](../satoshi-uploader.md) can concatenated lead to the full 7z file. Also as mentioned by Ken, it is infinitely easier for the average user to just access the cables directly on [WikiLeaks](../wikileaks.md) :-) The data is preceded by the message:<a id="_1423"></a>

  ```
  sSEXWikileaks Cablegate Backup

  cablegate-201012041811.7z

  Download the following transactions with Satoshi Nakamoto's download tool which
  can be found in transaction 6c53cd987119ef797d5adccd76241247988a0a5ef783572a9972e7371c5fb0cc

  Free speech and free enterprise! Thank you Satoshi!
  ```
<a id="_1424"></a>
- tx dde7cd8e8f073a525c16c5ee4e4a254f847b7ad6babef257231813166fbef551 block 230229 and tx 4a0088a249e9099d205fb4760c28275d4b8965ac9fd56f5ddf6771cdb0d94f38 block 230231 contain indexes of pages from [The Hidden Wiki](../the-hidden-wiki.md). These can be viewed at: [https://bitcoinstrings.com/blk00052.txt](https://bitcoinstrings.com/blk00052.txt). Not reproduced here because we are cowards.

<a id="_1425"></a>
So basically, this was the first obviously illegal block attempt.

<a id="_1426"></a>
None of this content is particularly eye-popping for [Ciro Santilli](../ciro-santilli-split.md)'s slightly crazy [freedom of speech](../freedom-of-speech.md) standards, and as of 2021, the Bitcoin blockchain likely hasn't become illegal anywhere yet due to freedom of speech concerns.

<a id="_1427"></a>
Furthermore, it is likely much easier to find much worse illegal content by browsing any [uncensored Onion service search engine](../uncensored-onion-service-search-engine.md) for 2 minutes.

<a id="_1428"></a>
[Ciro Santilli](../ciro-santilli-split.md) estimates that perhaps the uploader didn't upload [child pornography](../child-pornography.md), which is basically the apex of illegality of this era, because they were afraid that their identities would one day be found.

<a id="_1429"></a>
Bibliography:<a id="_1430"></a>

<a id="_1431"></a>
- [https://bitcointalk.org/index.php?topic=191039.0](https://bitcointalk.org/index.php?topic=191039.0) "WTF - Kiddy Porn in the Blockchain for life?" (2013-04-29) on the [Bitcoin Forum](../bitcoin-forum.md)

## ↑ Ancestors (12)

1. [Themes](themes.md)
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

## ← Incoming links (1)

- [Satoshi uploader](../satoshi-uploader.md)
