# Custom encoded images of unknown source

↑ **Parent:** [Images](images.md)

<a id="image-bitcoin-jpg"></a>
<img src="https://web.archive.org/web/20220116140433im_/http://static.righto.com/images/bitcoin/bitcoin.jpg" alt="" height="300">

**[Figure 18](#image-bitcoin-jpg). `bitcoin.jpg`**. [Source](http://www.righto.com/2014/02/ascii-bernanke-wikileaks-photographs.html). <a id="_234"></a>
A bitcoin logo on [block 123573](https://www.blockchain.com/explorer/blocks/btc/123573) (2011-05-13).

<a id="_235"></a>
This is the very first ASCII string to show up at [https://github.com/cirosantilli/bitcoin-inscription-indexer](https://github.com/cirosantilli/bitcoin-inscription-indexer) after only the [Genesis block message](../genesis-block-message.md).

<a id="_236"></a>
This version of the image was just ripped from [Hidden surprises in the Bitcoin blockchain by Ken Shirriff (2014)](hidden-surprises-in-the-bitcoin-blockchain-by-ken-shirriff-2014.md).

<a id="_237"></a>
Reconstructing it should likely be a simple matter of copy pasting the ASCII [yEnc](../yenc.md) encoding present in the two transactions from [tx ceb1a7fb57ef8b75ac59b56dd859d5cb3ab5c31168aa55eb3819cd5ddbd3d806](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0123.txt#L11) into a text file and decoding the [yEnc](../yenc.md), but after searching for 20 minutes Ciro couldn't find a working yEnc decoder on [Ubuntu 21.10](../ubuntu-21-10.md). How can a format be so dead, even after considerable extensive use in the [Usenet](../usenet.md)??? It makes you think about life.

<a id="_238"></a>
As mentioned by Ken, the logo is split across two transactions: [ceb1a7fb57ef8b75ac59b56dd859d5cb3ab5c31168aa55eb3819cd5ddbd3d806](https://www.blockchain.com/explorer/transactions/btc/ceb1a7fb57ef8b75ac59b56dd859d5cb3ab5c31168aa55eb3819cd5ddbd3d806) and 9173744691ac25f3cd94f35d4fc0e0a2b9d1ab17b4fe562acc07660552f95518.

<a id="_239"></a>
There appears to be nothing strictly linking the two transactions, besides that they are very close by and the only ASCII strings around back in those pre-infinite-spam days, as can be seen at: [https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0123.txt#L11](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0123.txt#L11), so you could just see both of them by eye.

<a id="_240"></a>
Also the first one starts with:<a id="_241"></a>

```
=ybegin line=128 size=8776 name=bitcoin.jpg
```
and the second one ends in:<a id="_242"></a>

```
=yend size=8776 crc32=a7ac8449
```
so this is likely clearly part of the yEnc format for someone who knows it, and the filename `bitcoin.jpg` gives the file format.

<a id="_243"></a>
They are not even in the same block:<a id="_244"></a>

<a id="_245"></a>
- [https://www.blockchain.com/btc/tx/ceb1a7fb57ef8b75ac59b56dd859d5cb3ab5c31168aa55eb3819cd5ddbd3d806](https://www.blockchain.com/btc/tx/ceb1a7fb57ef8b75ac59b56dd859d5cb3ab5c31168aa55eb3819cd5ddbd3d806) is in block 123573
<a id="_246"></a>
- [https://www.blockchain.com/btc/tx/9173744691ac25f3cd94f35d4fc0e0a2b9d1ab17b4fe562acc07660552f95518](https://www.blockchain.com/btc/tx/9173744691ac25f3cd94f35d4fc0e0a2b9d1ab17b4fe562acc07660552f95518) is in block 123571
both from 2011-05-13. Also note that they ended up being committed reverse order, since you don't have a strict order control over the final blockchain.

---

<a id="image-v27ssra-jpg"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/v27sSra.jpg" alt="" height="500">

**[Figure 19](#image-v27ssra-jpg). v27sSra.jpg**. <a id="_247"></a>
An image of a dozen people siting at a dinner table, with each person identified by a [Twitter](../twitter.md) handle that was edited in.

<a id="_248"></a>
This image is present [tx 4be3a833ee83b4ca7d157d60fbf7411f7528314ce90df8a844f855118bc6ca11 from block 357239](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/in/0357.txt#L384) (2015-05-20), an input transaction.

<a id="_249"></a>
It contains a base 64 encoded image:<a id="_250"></a>

```
v27sSra.jpg

/9j/4AAQSkZJRgABAQEASABIAAD/2wBDACgcHiMeGSgjISMtKygwPGRBPDc3PHtYXUlkkYCZlo+A
...
TAkBaMxbbhuYXGDMyXw/MIV84IqrE//Z
...
```

<a id="_251"></a>
By manually copy pasting that into a file `v27sSra.base64` we can obtain the image with:<a id="_252"></a>

```
base64 -d <v27sSra.base64 >v27sSra.jpg
```
The exact same content appears to be present on the next input transaction 56d23a230042c094bc54bb72fc4c10a3f26750030b9927994e741d3689f5c09e on the same block.

<a id="_253"></a>
[Google reverse image search](../google-reverse-image-search.md) leads to [https://freedom-to-tinker.com/2015/05/21/the-story-behind-the-picture-of-nick-szabo-with-other-bitcoin-researchers-and-developers/](https://freedom-to-tinker.com/2015/05/21/the-story-behind-the-picture-of-nick-szabo-with-other-bitcoin-researchers-and-developers/) The story behind the picture of [Nick Szabo](../nick-szabo.md) with other Bitcoin researchers and developers by Arvind Narayanan (2015), in which Arvind ([@random\_walker](https://twitter.com/random_walker)) who attended the meeting clearly lists all names and handles, and talks about the background of gathering of Bitcoin devs that happened in March 2014. The article also contains a higher resolution version of the image uploaded to the blockchain.

<a id="_254"></a>
It also links to a popular [Reddit](../reddit.md) thread that contains the image from May 2015: [https://www.reddit.com/r/Bitcoin/comments/36hfu4/pic_coredevs_having_dinner_with_nick_szabo/](https://www.reddit.com/r/Bitcoin/comments/36hfu4/pic_coredevs_having_dinner_with_nick_szabo/)

<a id="_255"></a>
[Googling](../google-split.md) `v27sSra.jpg` leads to [https://bitcointalk.org/index.php?topic=1061926.220;wap](https://bitcointalk.org/index.php?topic=1061926.220;wap) "New York Times identifies Nick Szabo as Satoshi Nakamoto" which links to [https://i.imgur.com/v27sSra.jpg](https://i.imgur.com/v27sSra.jpg) so this is a  [Satoshi Nakamoto](../satoshi-nakamoto.md)-real-identity thing.

---

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
