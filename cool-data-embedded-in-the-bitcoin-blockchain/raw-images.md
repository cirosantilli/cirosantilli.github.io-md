# Raw images

↑ **Parent:** [Images](images.md)

<a id="_495"></a>
In this section contains a list of images we could find that wre uploaded as raw data to the blockchain, without any special encoding, e.g. as done by the [AtomSea & EMBII](atomsea-and-embii.md) system.

<a id="_496"></a>
It is possible that some/most of those were uploaded via the [cryptograffiti.info](cryptograffiti-info.md) system, but since that indexer stopped working, and since the format is so non-specific, it is not possible be sure as far as we can tell.

<a id="_497"></a>
These images were indexed by looking for standard transaction output script hashes that contain [JPEG](../jpeg.md) or [PNG](../portable-network-graphics.md) images immediately on the first payload byte based on file signature bytes and indexed/easily downloaded at [https://github.com/cirosantilli/bitcoin-inscription-indexer#image-indexing-and-download](https://github.com/cirosantilli/bitcoin-inscription-indexer#image-indexing-and-download).

<a id="image-western-union-bitcoin-spoof-jpg-gz"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/200f3f6f8a91ae438d1924e5cedca98cea7f0197b9eba11343948b5621ca19ed.jpg)

**[Figure 40](#image-western-union-bitcoin-spoof-jpg-gz). western-union-bitcoin-spoof.jpg.gz**. <a id="_498"></a>
[200f3f6f8a91ae438d1924e5cedca98cea7f0197b9eba11343948b5621ca19ed](https://www.blockchain.com/explorer/transactions/btc/200f3f6f8a91ae438d1924e5cedca98cea7f0197b9eba11343948b5621ca19ed) block 331804 (2014-11-27) [JPEG](../jpeg.md) in [Gzip](https://ourbigbook.com/go/topic/gzip) as a single [input script](../bitcoin-input-script.md) constant.

<a id="_499"></a>
This ad highlights one of the claimed potential advantages of Bitcoin: cheaper/faster cross border transactions.

<a id="_500"></a>
This inscription is highlighted at [Data Insertion in Bitcoin's Blockchain by Andrew Sward, Vecna OP\_0 and Forrest Stonedahl](../data-insertion-in-bitcoin-s-blockchain-by-andrew-sward-vecna-op-0-and-forrest-stonedahl.md). Finding Gzips with [binwalk](../binwalk.md) is hard because the file signature is only 2 bytes long (1F 8B), so there are lots of false positives.

<a id="_501"></a>
Gzip binary uploaded at: [https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/200f3f6f8a91ae438d1924e5cedca98cea7f0197b9eba11343948b5621ca19ed.jpg.gz](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/200f3f6f8a91ae438d1924e5cedca98cea7f0197b9eba11343948b5621ca19ed.jpg.gz) gunzip 1.12 complains:<a id="_502"></a>

```
western-union-bitcoin-spoof.jpg.gz: decompression OK, trailing garbage ignored
```
but we were not able to fix that: removing bytes at the end goes straight from "trailing garbage" to "incomplete file" after a certain byte.

---

<a id="image-super-mario-coin-sprite"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/bf7ef3216ae09f8252c76e7d0031bc4aa131a23a6900f8371c44ffde7957c8da.png)

**[Figure 41](#image-super-mario-coin-sprite). Super Mario coin sprite**. [tx bf7ef3216ae09f8252c76e7d0031bc4aa131a23a6900f8371c44ffde7957c8da](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0345.txt#L182) ([2015-03-01](https://www.blockchain.com/explorer/transactions/btc/bf7ef3216ae09f8252c76e7d0031bc4aa131a23a6900f8371c44ffde7957c8da)). Possibly from [Super Mario World](../super-mario-world.md) for the [SNES](../super-nintendo-entertainment-system.md) (1990). No doubt a self-reference to [Bitcoin](../bitcoin.md) itself. Encoded as a [data URL](../data-uri-scheme.md) for a [PNG](../portable-network-graphics.md) image:<a id="_503"></a>

```
<img src="data:image/png;base64,
```

Visible e.g. at [https://www.pinterest.fr/pin/137993176075040653/](https://www.pinterest.fr/pin/137993176075040653/).

---

<a id="image-jpg-thumbnail"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/515a95381e511141229966d722db19db7da66a0d629b1f883d296287632e72b3.jpg)

**[Figure 42](#image-jpg-thumbnail). JPG thumbnail**. Presumably a [JPEG](../jpeg.md) upload test. [tx 515a95381e511141229966d722db19db7da66a0d629b1f883d296287632e72b3](https://www.blockchain.com/explorer/transactions/btc/515a95381e511141229966d722db19db7da66a0d629b1f883d296287632e72b3), [block 349362](https://www.blockchain.com/explorer/blocks/btc/349362) (2015-03-26) via [cryptograffiti.info](cryptograffiti-info.md).

<a id="image-we-love-bitcoin"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/9bdb59a0f5858af670d9b412041b8918114d7c56cc637f57f1d8469f101a5d0b.jpg" alt="" height="200">

**[Figure 43](#image-we-love-bitcoin). we love bitcoin**. <a id="_504"></a>
A heart next to a bitcoin logo and written "we love bitcoin". Reproduced at: [https://kryptomoney.com/grayscale-report-institutional-investors-retirement-funds-love-bitcoin/](https://kryptomoney.com/grayscale-report-institutional-investors-retirement-funds-love-bitcoin/)

<a id="_505"></a>
Embedded in the image itself, there's a message in the header comments:<a id="_506"></a>


> Bitcoin uses peer-to-peer technology to operate with no central authority or banks

which is the opening paragraph of: [https://bitcoin.org/en/](https://bitcoin.org/en/)

<a id="_507"></a>
[tx 9bdb59a0f5858af670d9b412041b8918114d7c56cc637f57f1d8469f101a5d0b](https://www.blockchain.com/explorer/transactions/btc/9bdb59a0f5858af670d9b412041b8918114d7c56cc637f57f1d8469f101a5d0b), [block 351375](https://www.blockchain.com/explorer/blocks/btc/351375) (2015-04-09) via [cryptograffiti.info](cryptograffiti-info.md).

---

<a id="image-the-economist-logo"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/b70bfe6a9b314611655554576feb11f15d47b9e80c5993e91829bb87895ef23c.png" alt="" height="300">

**[Figure 44](#image-the-economist-logo). The Economist logo**. <a id="_508"></a>
[tx b70bfe6a9b314611655554576feb11f15d47b9e80c5993e91829bb87895ef23c](https://www.blockchain.com/explorer/transactions/btc/b70bfe6a9b314611655554576feb11f15d47b9e80c5993e91829bb87895ef23c) block 355899 (2015-05-11). [PNG](../portable-network-graphics.md) inscribed as a [Daisy chain Bitcoin inscription](../daisy-chain-bitcoin-inscription.md) using [OP\_RETURN](../op-return.md).

<a id="_509"></a>
The daisy then follows up to the [Figure 45. "City of London School logo"](#image-city-of-london-school-logo), which therefore must be by the same uploader.

<a id="image-city-of-london-school-logo"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/6ab2f3dbff0ebd856f6cf0360fc7db987f8789508dfdefdcc1f9e2aacf9ac0de.jpg)

**[Figure 45](#image-city-of-london-school-logo). City of London School logo**. <a id="_510"></a>
[tx 6ab2f3dbff0ebd856f6cf0360fc7db987f8789508dfdefdcc1f9e2aacf9ac0de](https://www.blockchain.com/explorer/transactions/btc/6ab2f3dbff0ebd856f6cf0360fc7db987f8789508dfdefdcc1f9e2aacf9ac0de) block 355901 (2015-05-11). [PNG](../portable-network-graphics.md) inscribed as a [Daisy chain Bitcoin inscription](../daisy-chain-bitcoin-inscription.md) using [OP\_RETURN](../op-return.md).

<a id="_511"></a>
This image is encoded on the very same daisy chain as [Figure 44. "The Economist logo"](#image-the-economist-logo), immediately afterwards.

<a id="_512"></a>
Furthermore, we understand that they used the following convention to "split them up":<a id="_513"></a>

<a id="_514"></a>
- paylout in vout 0: continue image
<a id="_515"></a>
- payload in vout 1: end of image

---

<a id="_516"></a>
The transactions leading up to b70bfe6a9b314611655554576feb11f15d47b9e80c5993e91829bb87895ef23c contain multiple text daisy inscriptions that show up on our text dumps at: [https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/e716e317b703e1bad63edf5064f90f5e80c5aaf5/data/out/0355.txt#L635](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/e716e317b703e1bad63edf5064f90f5e80c5aaf5/data/out/0355.txt#L635)<a id="_517"></a>

<a id="_518"></a>
- 5256d3059520c9ecda22bcf17776adcc962a5ae90333efbb00cf45818e9bf0bb:<a id="_519"></a>
  > You're poo you're papa, says WeeWaWeeWa

  then a quote from [https://bitcoin.org/en/faq](https://bitcoin.org/en/faq) ([archive](https://web.archive.org/web/20240321230812/https://bitcoin.org/en/faq)):<a id="_520"></a>
  > Bitcoin is the first implementation of a concept called "cryptocurrency", which was first described in 1998 by [Wei Dai](../wei-dai.md) on the cypherpunks mailing list, suggesting the idea of a new form of money that uses cryptography to control its creation and transactions, rather than a central authority. The first Bitcoin specification and proof of concept was published in 2009 in a cryptography mailing list by [Satoshi Nakamoto](../satoshi-nakamoto.md). Satoshi left the project in late 2010 without revealing much about himself. The community has since grown exponentially with many developers working on Bitcoin.

  then:<a id="_521"></a>
  > And now, via JSON-RPC!
<a id="_522"></a>
- d6b006f3cd9b545d5015263e954dae7c52c71bb5f4a0573918ff0e1ce8785de4 contains another quote from [https://bitcoin.org/en/faq](https://bitcoin.org/en/faq) ([archive](https://web.archive.org/web/20240321230812/https://bitcoin.org/en/faq)):<a id="_523"></a>
  > Much of the trust in Bitcoin comes from the fact that it requires no trust at all. Bitcoin is fully open-source and decentralized. This means that anyone has access to the entire source code at any time. Any developer in the world can therefore verify exactly how Bitcoin works. All transactions and bitcoins issued into existence can be transparently consulted in real-time by anyone. All payments can be made without reliance on a third party and the whole system is protected by heavily peer-reviewed cryptographic algorithms like those used for online banking. No organization or individual can control Bitcoin, and the network remains secure even if not all of its users can be trusted.

  followed by:<a id="_524"></a>
  > One day this will be for general storage
<a id="_525"></a>
- d9450fbd228d7a19d08f700d43200184b0d46561ffd7eb9ddbb378435ec66789 says:<a id="_526"></a>
  > Let's agree on 5MB blocks and move on?

  These inscriptions were made right in the midst of the [protests against larger block sizes](protests-against-larger-block-sizes.md).
<a id="_527"></a>
- a689707f77882eb5a3b1954747f159b1c22b688a57ec17b4d636b7f94e451e3d<a id="_528"></a>
  > a single piece of data

  then the intro from [https://bitcoin.org/en/](https://bitcoin.org/en/) ([archive](https://web.archive.org/web/20240327000314/https://bitcoin.org/en/)):<a id="_529"></a>
  > Bitcoin uses peer-to-peer technology to operate with no central authority or banks; managing transactions and the issuing of bitcoins is carried out collectively by the network.

  then:<a id="_530"></a>
  > It's my cake day. I pressed the button. I have no regrets. Just stick it on the blockchain

  Parents daisy more text visible on our text dumps: [https://www.blockchain.com/explorer/transactions/btc/b70bfe6a9b314611655554576feb11f15d47b9e80c5993e91829bb87895ef23c](https://www.blockchain.com/explorer/transactions/btc/b70bfe6a9b314611655554576feb11f15d47b9e80c5993e91829bb87895ef23c)

---

<a id="image-iranian-lady-with-polar-bear-hat"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/b673c7d0c62cce8315ad6cc63a2c8ca8169bf73432435760b808735e1a7fe0e2-fix.jpg)

**[Figure 46](#image-iranian-lady-with-polar-bear-hat). Iranian lady with polar bear hat.** <a id="_531"></a>
[tx b673c7d0c62cce8315ad6cc63a2c8ca8169bf73432435760b808735e1a7fe0e2](https://www.blockchain.com/explorer/transactions/btc/b673c7d0c62cce8315ad6cc63a2c8ca8169bf73432435760b808735e1a7fe0e2) block 401255 (2016-03-05). [JPEG](../jpeg.md) encoded with [daisy chain Bitcoin inscription](../daisy-chain-bitcoin-inscription.md) using [OP\_RETURN](../op-return.md).

<a id="_532"></a>
We don't know if she's actually [Iranian](../iran.md), it's just an uneducated guess.

<a id="_533"></a>
The image data is cut in half. This makes the image an invalid [JPEG](../jpeg.md), but [ImageMagick](../imagemagick.md) is able to recover and convert to a valid image which is what we show here to make it portable to more browsers. The raw invalid image is present at: [https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/b673c7d0c62cce8315ad6cc63a2c8ca8169bf73432435760b808735e1a7fe0e2.jpg](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/b673c7d0c62cce8315ad6cc63a2c8ca8169bf73432435760b808735e1a7fe0e2.jpg), but it can also be generally viewed by most viewers.

<a id="_534"></a>
This embedding uses a novel more specialiezd protocol on top of a raw [daisy chain Bitcoin inscription](../daisy-chain-bitcoin-inscription.md).

<a id="_535"></a>
The daisy actually starts at f49e79889b34d355fa8a02f13b9db4ed69c067f975e25339737ef10e4b993d7a and data is encoded as follows:

<a id="_536"></a>
```
OP_RETURN 62 00000000 48656c6c6f20776f726c64212052657475726e20626c6f622070726f746f636f6c2076
OP_RETURN 62 00000001 313a204d41474943203d20307836322c205041434b414745203d2075696e7431362c20
OP_RETURN 62 00000002 53455155454e4345203d2075696e7431362c205041594c4f4144203d20757020746f20

OP_RETURN 62 00000000 48656c6c6f20776f726c64212052657475726e20626c6f622070726f746f636f6c2076
OP_RETURN 62 00000001 313a204d41474943203d20307836322c205041434b414745203d2075696e7431362c20
OP_RETURN 62 00000002 53455155454e4345203d2075696e7431362c205041594c4f4144203d20757020746f20

OP_RETURN 62 00000003 33352062797465732e0a

OP_RETURN 62 00010000 ffd8ffe1001845786966000049492a00080000000000000000000000ffec0011447563
OP_RETURN 62 00010001 6b79000100040000003c0000ffe1039a687474703a2f2f6e732e61646f62652e636f6d
OP_RETURN 62 00010002 2f7861702f312e302f003c3f787061636b657420626567696e3d22efbbbf222069643d
OP_RETURN 62 00010003 2257354d304d7043656869487a7265537a4e54637a6b633964223f3e203c783a786d70

...

OP_RETURN 62 00010085 51290358a41fe5408b4435254208d4810a5fe9113044c1ae3aa544656d729756395b87
OP_RETURN 62 00010086 c4e261f55c5d19e1c792c3f78adff1368db58e5a0bb85b2c6753c42de6d973edae0642
OP_RETURN 62 00010087 1b2c8370f203aaa0a6eb7ea0871d8e9ae6534b785b57347171e4df6a5463d7ce77b93b
OP_RETURN 62 00010088 9b8bf96edd1b982e2474a41ad28e3c01e74586d1d1ad7a874c5a1b7c742d2285c371f6
```

<a id="_537"></a>
The first block is:<a id="_538"></a>


> Hello world! Return blob protocol v1: MAGIC = 0x62, PACKAGE = uint16, SEQUENCE = uint16, PAYLOAD = up to

which then gets repeated, probably an error, but now with the sentence completed:<a id="_539"></a>


> Hello world! Return blob protocol v1: MAGIC = 0x62, PACKAGE = uint16, SEQUENCE = uint16, PAYLOAD = up to 35 bytes

This therefore gives us the name of the protocol as "return blob protocol". We also understand that the 0x62 was aconfiguration parameter.

<a id="_540"></a>
`ffd8ffe1` marks the start of the [JPEG](../jpeg.md).

<a id="_541"></a>
If the rest of the image were inscribed somewhere random in the blockchain, we'd expect to find the string `6200010089` containing the netxt data chunck on a nearby block, but [`bgrep`](../bgrep.md) did not find it, so perhaps the data just isn't there.

<a id="_542"></a>
The last tx of the daisy is 43b182065ab2c7d1908ec3cee756d9f626c1e4bd1efa17a7c3993433b653d499 which is followed by 9e6838a3545bd59a708d0c177d6840c7d82b8ac6220138ca3d8133a1376405aa which does not contain any data.

---

<a id="image-erich-erstu"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/c206e8fff656f07b27dac831ef9b956792bae4e76a2cb43f14f49f0298bf2c2f.jpg)

**[Figure 47](#image-erich-erstu). Erich Erstu**. Alias: 1Hyena. A well built man wearing a gas mask. Google image search leads to: [https://github.com/1Hyena](https://github.com/1Hyena) ([archive](https://web.archive.org/web/20201103193934/https://github.com/1Hyena)), who is the creator of [cryptograffiti.info](cryptograffiti-info.md). It was around after this time that the number of raw images surged dramatically in the blockchain, so it is possible that this is when the service started operating. This further suggests that most raw image uploads we found were made with [cryptograffiti.info](cryptograffiti-info.md). [tx c206e8fff656f07b27dac831ef9b956792bae4e76a2cb43f14f49f0298bf2c2f](https://www.blockchain.com/explorer/transactions/btc/c206e8fff656f07b27dac831ef9b956792bae4e76a2cb43f14f49f0298bf2c2f), [block 416527](https://www.blockchain.com/explorer/blocks/btc/416527) (2016-06-16). Embedded text:<a id="_543"></a>
> Hyena was here on the 16th of June 2016.

and:<a id="_544"></a>
> Hi mom! I love you.

---

<a id="image-water-deer"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/357e8ae080e5a1b554eaec2953e3e6e2e7955f3af4559dd0f1bc6381d56aa183.jpg)

**[Figure 48](#image-water-deer). Water Deer**. [https://badtaxidermy.com](https://badtaxidermy.com) "Water Deer" image, visible at: [https://web.archive.org/web/20200527070011/http://www.badtaxidermy.com/?page=3](https://web.archive.org/web/20200527070011/http://www.badtaxidermy.com/?page=3). [tx 357e8ae080e5a1b554eaec2953e3e6e2e7955f3af4559dd0f1bc6381d56aa183](https://www.blockchain.com/explorer/transactions/btc/357e8ae080e5a1b554eaec2953e3e6e2e7955f3af4559dd0f1bc6381d56aa183), [block 416735](https://www.blockchain.com/explorer/blocks/btc/416527) (2016-06-16) via [cryptograffiti.info](cryptograffiti-info.md). The file contains the strings:<a id="_545"></a>
> www.badtaxidermy.com

and:<a id="_546"></a>
> [Cryptograffiti.info](cryptograffiti-info.md) now allows you to attach JPEG images to your messages.

---

<a id="image-hotmine-io"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/8ec01c5e8f3b57adb13079af3b7e40e7acd3986a5ed14325388405771bd43f9b.png)

**[Figure 49](#image-hotmine-io). hotmine.io**. A mining supplier: [https://hotmine.io/en](https://hotmine.io/en). [https://twitter.com/uahotmine](https://twitter.com/uahotmine). [tx 8ec01c5e8f3b57adb13079af3b7e40e7acd3986a5ed14325388405771bd43f9b](https://www.blockchain.com/explorer/transactions/btc/8ec01c5e8f3b57adb13079af3b7e40e7acd3986a5ed14325388405771bd43f9b), [block 416835](https://www.blockchain.com/explorer/blocks/btc/416835) (2016-06-18) via [cryptograffiti.info](cryptograffiti-info.md). The file contains the following string embedded into it:<a id="_547"></a>
> Smart Heating, Bitcoin Mining For You - [http://en.hotmine.io](http://en.hotmine.io)

---

<a id="image-nada-from-they-live-1988"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/83df1e5ecc1c7ac455d2855e15cff8fa5771afe2ad1796c8b6b1a8e910e829c4.jpg)

**[Figure 50](#image-nada-from-they-live-1988). Nada from They Live (1988)** <a id="_548"></a>
[tx 83df1e5ecc1c7ac455d2855e15cff8fa5771afe2ad1796c8b6b1a8e910e829c4](https://www.blockchain.com/explorer/transactions/btc/83df1e5ecc1c7ac455d2855e15cff8fa5771afe2ad1796c8b6b1a8e910e829c4), [block 416896](https://www.blockchain.com/explorer/blocks/btc/416896) (2016-06-18) via [cryptograffiti.info](cryptograffiti-info.md). The file has the following string embedded into it:<a id="_549"></a>


> <a id="_550"></a>
> I have come here to chew bubble gum and dance on [Ethereum](../ethereum.md)'s grave.
> 
> <a id="_551"></a>
> And I'm all out of bubble gum.

which is a reference to Nada's original dialogue:<a id="_552"></a>


> I have come here to chew bubblegum and kick ass... and I'm all out of bubblegum.

<a id="video-i-m-here-to-chew-bubblegum"></a>
**[Video 5](#video-i-m-here-to-chew-bubblegum). I'm here to chew bubblegum.** [Source](https://www.youtube.com/watch?v=Wp_K8prLfso). Off-chain film scene for context.

---

<a id="image-cryptocurrency-minning-ad"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/eda07af9584391bb6f5ebb07ba57a51b610751fdf06ae49d9166225c36d97d0b.jpg)

**[Figure 51](#image-cryptocurrency-minning-ad). Cryptocurrency Minning ad**. Twitter "@dobcrypto": [https://twitter.com/dobcrypto](https://twitter.com/dobcrypto) Reuploaded at: [https://imgur.com/gallery/00oOuhm](https://imgur.com/gallery/00oOuhm). [tx eda07af9584391bb6f5ebb07ba57a51b610751fdf06ae49d9166225c36d97d0b](https://www.blockchain.com/explorer/transactions/btc/eda07af9584391bb6f5ebb07ba57a51b610751fdf06ae49d9166225c36d97d0b), [block 417111](https://www.blockchain.com/explorer/blocks/btc/417111) (2016-06-20) via [cryptograffiti.info](cryptograffiti-info.md). The file contains the following string:<a id="_553"></a>
> Subscribe, I will be glad to see you! [http://www.youtube.com/c/dobcryptocurrency](http://www.youtube.com/c/dobcryptocurrency)

---

<a id="image-chinese-wedding"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/609d5e0f968c0ab7abc2be21468cfd552483d38b08e6df23d27766eb61b9be3c.jpg" alt="" height="700">

**[Figure 52](#image-chinese-wedding). Chinese wedding**. <a id="_554"></a>
[tx 609d5e0f968c0ab7abc2be21468cfd552483d38b08e6df23d27766eb61b9be3c](https://www.blockchain.com/explorer/transactions/btc/609d5e0f968c0ab7abc2be21468cfd552483d38b08e6df23d27766eb61b9be3c), [block 417131](https://www.blockchain.com/explorer/blocks/btc/417131) (2016-06-20) via [cryptograffiti.info](cryptograffiti-info.md).

<a id="_555"></a>
A white man and a [Chinese](../china-split.md) [woman](../female.md) wearing Chinese traditional dressess holding hands, presumably a token from their wedding. A Chinese poem is visible next to them, with four vertical setences made up of 7 characters each, to be read from right to left. This is a classic [Classical Chinese poetry form](../classical-chinese-poetry-form.md) known as [qijue](../qijue.md).

<a id="_556"></a>
A photo of a snowy mountain is shown in the background, fitting the theme of the poem. It looks like an European mountain, possibly Mont Blanc? TODO identify. Perhaps a reference to the nationality of the husband.

<a id="_557"></a>
TODO transcribe the [Chinese](../chinese-language.md) text, [cursive grass script](../cursive-script-east-asia.md) + traditional characters + ultra-low res put this beyond [Ciro Santilli](../ciro-santilli-split.md)'s capabilities/patience ratio. [Ciro Santilli's wife](../ciro-santilli-s-wife.md)'s transcribed gave the first column as:<a id="_558"></a>


> 丹珍默然藏山中  
> A scarlet gemstone hides quietly in the midst of the mountains.

and no [Google](../google-split.md) hits, so maybe an original poem? What a hero. TODO transcribe the rest.

<a id="_559"></a>
The image file contains the [English](../english-language.md) transalation of the Chinese poem embeded into it:<a id="_560"></a>


> A scarlet gemstone hides quietly in the midst of the mountains.  
> Its beauty softly enters the wanderer's dreams.  
> Fame and fortune become like drifting clouds  
> But the gem endures like the constellations above.

---

<a id="image-superbuffo"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/6240f61bbaeac66cd623e921a153addaf5f379a996f2de0f0c6506d628fe3812.jpg)

**[Figure 53](#image-superbuffo). Superbuffo**. [Googling](../google-split.md) gives a Toni Caradonna: [https://twitter.com/superbuffo](https://twitter.com/superbuffo). At [https://twitter.com/Superbuffo/status/1620900765014556672](https://twitter.com/Superbuffo/status/1620900765014556672) that twitter account claimed the art or its depiction. [https://www.imdb.com/name/nm9516368/](https://www.imdb.com/name/nm9516368/) has some obscure references to him. [tx 6240f61bbaeac66cd623e921a153addaf5f379a996f2de0f0c6506d628fe3812](https://www.blockchain.com/explorer/transactions/btc/6240f61bbaeac66cd623e921a153addaf5f379a996f2de0f0c6506d628fe3812), [block 417354](https://www.blockchain.com/explorer/blocks/btc/417354) (2016-06-21) via [cryptograffiti.info](cryptograffiti-info.md). The file contains the following string embedded into it, in addition to a lot of [Adobe](../adobe.md) boilerplate:<a id="_561"></a>
> Superbuffo the first comedian on the blockchain

---

<a id="image-rene-angelil-and-celine-dion"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/e2e5b9cf04d93ae5fc1b54e9208b92b668823e014b251f57510e4702661fa1a6.jpg)

**[Figure 54](#image-rene-angelil-and-celine-dion). Rene Angelil and Celine Dion**. Reproduced at: [https://web.archive.org/web/20191130174338/https://people.com/celebrity/inside-celine-dion-and-rene-angelils-21-year-marriage/](https://web.archive.org/web/20191130174338/https://people.com/celebrity/inside-celine-dion-and-rene-angelils-21-year-marriage/) but cropped to faces. [tx e2e5b9cf04d93ae5fc1b54e9208b92b668823e014b251f57510e4702661fa1a6](https://www.blockchain.com/explorer/transactions/btc/e2e5b9cf04d93ae5fc1b54e9208b92b668823e014b251f57510e4702661fa1a6), [block 417272](https://www.blockchain.com/explorer/blocks/btc/417272) (2016-06-21) via [cryptograffiti.info](cryptograffiti-info.md). Embedded text:<a id="_562"></a>
> You will be here forever

---

<a id="image-new-age-dance"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/0602dd1b375bc71818db0a40d7a14f438499af3eda9056125eb5a1b74bed790b.jpg)

**[Figure 55](#image-new-age-dance). New Age dance**. [Woman](../female.md) dancing a [New Age](../new-age.md)-like dance with [New Age](../new-age.md)-like [Indian](../india.md) looking clothes, holding a lamp, and with a rose on her hair. TODO identify. [tx 0602dd1b375bc71818db0a40d7a14f438499af3eda9056125eb5a1b74bed790b](https://www.blockchain.com/explorer/transactions/btc/0602dd1b375bc71818db0a40d7a14f438499af3eda9056125eb5a1b74bed790b), [block 419676](https://www.blockchain.com/explorer/blocks/btc/419676) (2016-07-07) via [cryptograffiti.info](cryptograffiti-info.md). The image contains the following text embedded into it (TODO unknown mechanism, does not show up on [exifTool](../exiftool.md):<a id="_563"></a>
> No alcohol and smoking since 07.07.2016. Love girls!

---

<a id="image-snake-penetration-sculputure"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/83f412eb7ff40fe542901186a6d37cba0eb4f8458c574bc02a6f7236c599fe07.jpg)

**[Figure 56](#image-snake-penetration-sculputure). Snake penetration sculputure**. Sculpture of what seems to be a snake penetrating a [vagina](../vagina.md). [tx 83f412eb7ff40fe542901186a6d37cba0eb4f8458c574bc02a6f7236c599fe07](https://www.blockchain.com/explorer/transactions/btc/83f412eb7ff40fe542901186a6d37cba0eb4f8458c574bc02a6f7236c599fe07), [block 420122](https://www.blockchain.com/explorer/blocks/btc/420122) (2016-07-10) via [cryptograffiti.info](cryptograffiti-info.md).

<a id="image-wedding-invitation"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/01c3af71c12d49260231dcb3cc86d6ff21b3cd90878e9556482ef3b0908abffe.jpg)

**[Figure 57](#image-wedding-invitation). Wedding invitation**. TODO: make out names, quite low res, no patience. Looks like [Cyrillic script](../cyrillic-script.md). [tx 01c3af71c12d49260231dcb3cc86d6ff21b3cd90878e9556482ef3b0908abffe](https://www.blockchain.com/explorer/transactions/btc/01c3af71c12d49260231dcb3cc86d6ff21b3cd90878e9556482ef3b0908abffe), [block 420960](https://www.blockchain.com/explorer/blocks/btc/420960) (2016-07-16) via [cryptograffiti.info](cryptograffiti-info.md).

<a id="image-bitcoin-love-certificate"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/075d1c78883ccb237b374c7ed7f9ff0f90df3308c48f9e7a29348b815326b769.jpg" alt="" height="700">

**[Figure 58](#image-bitcoin-love-certificate). Bitcoin love certificate**. Hard to make out due to ultra-low-res, and in [Cyrillic script](../cyrillic-script.md). Contains three dates: 8.02.1982, 16.07.1992 and 17.07.2016. [tx 075d1c78883ccb237b374c7ed7f9ff0f90df3308c48f9e7a29348b815326b769](https://www.blockchain.com/explorer/transactions/btc/075d1c78883ccb237b374c7ed7f9ff0f90df3308c48f9e7a29348b815326b769), [block 421151](https://www.blockchain.com/explorer/blocks/btc/421151) (2016-07-17) via [cryptograffiti.info](cryptograffiti-info.md). The file contains the following text embedded into it:<a id="_564"></a>
> Wedding Wallled 15Nz214yv76BmkKLCi8kAVssa5C7nQHLjx

---

<a id="image-oles-slobodenyuk"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/10cc5d45396ba271659a4b00d2f70c433533227e5f7ea30bb5bd3c8563d7468a.jpg" alt="" height="500">

**[Figure 59](#image-oles-slobodenyuk). Oles Slobodenyuk**. <a id="_565"></a>
[tx 10cc5d45396ba271659a4b00d2f70c433533227e5f7ea30bb5bd3c8563d7468a](https://www.blockchain.com/explorer/transactions/btc/10cc5d45396ba271659a4b00d2f70c433533227e5f7ea30bb5bd3c8563d7468a), [Block 421280](https://www.blockchain.com/explorer/blocks/btc/421280) (2016-07-18) via [cryptograffiti.info](cryptograffiti-info.md)

<a id="_566"></a>
Wedding picture with people holding "Blockchain" and "Ipa" signs.

<a id="_567"></a>
Reproduced at: [https://web.archive.org/web/20200926150213/https://freebitcoins.com.ua/zapushhen-ukrainskij-bitkoin-pul-bitcoinukraine/](https://web.archive.org/web/20200926150213/https://freebitcoins.com.ua/zapushhen-ukrainskij-bitkoin-pul-bitcoinukraine/) Google translate:<a id="_568"></a>


> One of the initiators of the launch of this pool was Oles Slobodenyuk, who earlier created a grocery store in Kiev accepting bitcoins, arranged a TakeMyBitcoin flash mob, and also registered his own marriage in the bitcoin blockchain on the weddingbook.io website.

<a id="_569"></a>
Oles is for example featured at: [https://uk.sports.yahoo.com/news/bitcoin-miners-heating-homes-free-133053106.html](https://uk.sports.yahoo.com/news/bitcoin-miners-heating-homes-free-133053106.html) Bitcoin Miners Are Heating Homes Free of Charge in Frigid Siberia by Anna Baydakova (2019)

<a id="_570"></a>
The image file contains the following text embedded into it:<a id="_571"></a>


> \<Wedding date: Jul 17, 2016 ****  
> proof link [https://goo.gl/photos/2GToBx1WqRyiQtxQ6](https://goo.gl/photos/2GToBx1WqRyiQtxQ6)

The link is dead of course.

---

<a id="image-nematode"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/554846025e808df7adec3b1d099e3d4d54b7367cddaa959939cb5ca0fc6abf7b.png)

**[Figure 60](#image-nematode). Nematode**. A... [nematode](../nematode.md)-like shaped hand drawn extremely simple image? A test upload presumably? The squiggle outside of the worm might be a test direction marker. [tx 554846025e808df7adec3b1d099e3d4d54b7367cddaa959939cb5ca0fc6abf7b](https://www.blockchain.com/explorer/transactions/btc/554846025e808df7adec3b1d099e3d4d54b7367cddaa959939cb5ca0fc6abf7b), [block 424414](https://www.blockchain.com/explorer/blocks/btc/424414) (2016-08-09) via [cryptograffiti.info](cryptograffiti-info.md). The image file contains the following string embedded into it:<a id="_572"></a>
> 2016, painting, 135.7 x 130.7 cm (18 DPI)

---

<a id="image-hand-written-contract"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/cc9c0b95ac772515235147d8354ec8b8b0763bf842ad16b8b23f855c3dc6a57e.jpg" alt="" height="600">

**[Figure 61](#image-hand-written-contract). Hand written contract**. <a id="_573"></a>
Wedding contract written in Czech. Transcription and translation [by Petr Kadlec](https://github.com/cirosantilli/cirosantilli.github.io/issues/81):<a id="_574"></a>


> Svým podpisem pod tímto textem potvrzuji, že Daniela Dudysová a Pavel Urbaczka v mé přítomnosti dne 20.8.2016 v Ropici projevili vůli uzavřít spolu manželství, přičemž ani jeden z těchto projevů se mi nejevil jako nesvobodný, nikoliv vážný, nesrozumitelný, omylný nebo uzavřený v tísni.

Translation:<a id="_575"></a>


> With my signature under this text, I confirm Daniela Dudysová and Pavel Urbaczka have, in my presence on 2016-08-20 in Ropice, expressed the will to enter marriage, whereas neither of their expressions seemed to me to be non-free, not serious, in error, or under distress.

Signatures:<a id="_576"></a>


> Tereza (unreadable) Hana (unreadable) Jakub (unreadable) Radim Kozub (unreadable) (unreadable) Lenka (unreadable)

<a id="_577"></a>
Petr also conjectures that Jakub may refer to [Jakub Olšina from Blockchain Legal](https://www.blockchainlegal.cz/cs/tym). [Figure 62. "Wedding on grass"](#image-wedding-on-grass) on the same block contains a image of a wedding, presumably the same of the contract. The photo of the man might be the same person as [https://www.linkedin.com/in/olsinajakub/](https://www.linkedin.com/in/olsinajakub/), but a bit younger.

<a id="_578"></a>
[tx cc9c0b95ac772515235147d8354ec8b8b0763bf842ad16b8b23f855c3dc6a57e](https://www.blockchain.com/explorer/transactions/btc/cc9c0b95ac772515235147d8354ec8b8b0763bf842ad16b8b23f855c3dc6a57e), [block 426072](https://www.blockchain.com/explorer/blocks/btc/426072) (2016-08-20) via [cryptograffiti.info](cryptograffiti-info.md).

---

<a id="image-wedding-on-grass"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/693848d56098a0ad16736bea7f24336c9b47a7f0a6f776659e8d01f00b46af76.jpg)

**[Figure 62](#image-wedding-on-grass). Wedding on grass**. <a id="_579"></a>
[tx 693848d56098a0ad16736bea7f24336c9b47a7f0a6f776659e8d01f00b46af76](https://www.blockchain.com/explorer/transactions/btc/693848d56098a0ad16736bea7f24336c9b47a7f0a6f776659e8d01f00b46af76), [block 426072](https://www.blockchain.com/explorer/blocks/btc/426072) (2016-08-20) via [cryptograffiti.info](cryptograffiti-info.md).

<a id="_580"></a>
The file contains the following text embedded into it:<a id="_581"></a>


> Danila a Pavel se právě vzali!

which is Czech for:<a id="_582"></a>


> Danila and Pavel just got married!

So it is a followup to [Figure 61. "Hand written contract"](#image-hand-written-contract).

---

<a id="image-onshape-ad"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/c0bb963cb3ceffc49059f09db94e3fd73caa3b7a8e005160d49e99020ff6b51a.png" alt="" height="300">

**[Figure 63](#image-onshape-ad). Onshape ad**. Ad for [https://www.onshape.com/en/](https://www.onshape.com/en/), an online [CAD](../computer-aided-design.md) company:<a id="_583"></a>
> \#CAD users all over the world are designing in the cloud! Join them by creating a \#free Onshape account: [http://hubs.ly/HO3vJ6tO](http://hubs.ly/HO3vJ6tO). [tx c0bb963cb3ceffc49059f09db94e3fd73caa3b7a8e005160d49e99020ff6b51a](https://www.blockchain.com/explorer/transactions/btc/c0bb963cb3ceffc49059f09db94e3fd73caa3b7a8e005160d49e99020ff6b51a), [block 426832](https://www.blockchain.com/explorer/blocks/btc/426832) (2016-08-25) via [cryptograffiti.info](cryptograffiti-info.md). Embedded text:<a id="_584"></a>
> > @Onshape - The Future of Professional CAD

---

<a id="image-pepe-the-frog"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/ca933de16b6466e40b37c7ee0ec0dcd9a56bc365a567a5fff81ba4927dd61e23.gif)

**[Figure 64](#image-pepe-the-frog). Pepe the Frog**. [ca933de16b6466e40b37c7ee0ec0dcd9a56bc365a567a5fff81ba4927dd61e23](https://www.blockchain.com/explorer/transactions/btc/ca933de16b6466e40b37c7ee0ec0dcd9a56bc365a567a5fff81ba4927dd61e23) (2016-10-17) via [cryptograffiti.info](cryptograffiti-info.md). Embedded text:<a id="_585"></a>
> In Pepe We Trust  
> \#BITCOINPEPE

---

<a id="image-hello-yes-this-is-dog"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/4b0cd7e191ef0a14a9b6ab1c5900be534118c20a332ff26407648168d2722a2e.jpg)

**[Figure 65](#image-hello-yes-this-is-dog). Hello. Yes, this is dog**. [https://knowyourmeme.com/memes/yes-this-is-dog](https://knowyourmeme.com/memes/yes-this-is-dog). [tx 4b0cd7e191ef0a14a9b6ab1c5900be534118c20a332ff26407648168d2722a2e](https://www.blockchain.com/explorer/transactions/btc/4b0cd7e191ef0a14a9b6ab1c5900be534118c20a332ff26407648168d2722a2e), [block 440418](https://www.blockchain.com/explorer/blocks/btc/440418) (2016-11-24) via [cryptograffiti.info](cryptograffiti-info.md).

<a id="image-ross-ulbricht"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/b25ba2080d15c1277569bd2fee707a216c4e2ee0a1f479349c2309651c261511.jpg)

**[Figure 66](#image-ross-ulbricht). Ross Ulbricht**. Exact image also reproduced at: [https://ethereumworldnews.com/ross-ulbricht-attorney-dismiss-2018/](https://ethereumworldnews.com/ross-ulbricht-attorney-dismiss-2018/). [tx b25ba2080d15c1277569bd2fee707a216c4e2ee0a1f479349c2309651c261511](https://www.blockchain.com/explorer/transactions/btc/b25ba2080d15c1277569bd2fee707a216c4e2ee0a1f479349c2309651c261511), [block 442225](https://www.blockchain.com/explorer/blocks/btc/442225) (2016-12-06) via [cryptograffiti.info](cryptograffiti-info.md). Embedded text:<a id="_586"></a>
> <a id="_587"></a>
> [Silk Road](../silk-road-marketplace.md) saved lives that would  
> have otherwise been lost on the  
> streets.
> 
> <a id="_588"></a>
> [https://freeross.org/](https://freeross.org/)

---

<a id="image-tuxedo-and-rose"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/c67dca17d3e5544d8d2c70d143196e1c1438a09c7371b80086d0a71ec5aec3c8.jpg)

**[Figure 67](#image-tuxedo-and-rose). Tuxedo and rose**. Black and white and intentionally blurred photo of couple, the [woman](../female.md) wears a tuxedo, and the man holds a red rose/light-like thing in the middle. [tx c67dca17d3e5544d8d2c70d143196e1c1438a09c7371b80086d0a71ec5aec3c8](https://www.blockchain.com/explorer/transactions/btc/c67dca17d3e5544d8d2c70d143196e1c1438a09c7371b80086d0a71ec5aec3c8), [block 453083](https://www.blockchain.com/explorer/blocks/btc/453083) (2017-02-14) via [cryptograffiti.info](cryptograffiti-info.md).

<a id="image-couple-on-mountains"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/00a64f2ff9aae7a34c21d07b8fc9bad79989f25295ccbddc6fbe73b3685b65a9.jpg)

**[Figure 68](#image-couple-on-mountains). Couple on mountains**. Middle aged couple selfie in front of some mountains. [tx 00a64f2ff9aae7a34c21d07b8fc9bad79989f25295ccbddc6fbe73b3685b65a9](https://www.blockchain.com/explorer/transactions/btc/00a64f2ff9aae7a34c21d07b8fc9bad79989f25295ccbddc6fbe73b3685b65a9), [block 456370](https://www.blockchain.com/explorer/blocks/btc/456370) (2017-03-09) via [cryptograffiti.info](cryptograffiti-info.md). The file contains the following [Spanish](../spanish-language.md) poem, whch confirms that their [Spanish](../spain.md) looking faces are actually [Spanish](../spain.md), perhaps they are at the Pyrenees:<a id="_589"></a>
> <a id="_590"></a>
> Entre tus brazos y los míos  
> no hay espacio, tan juntitos  
> estamos que los pensamientos  
> son uno.
> 
> <a id="_591"></a>
> A veces somos casi dos desconocidos,  
> raros tan raros cómo distintos,  
> pero nos engañamos, tú lo sabes yo lo sé,  
> en realidad somos muy dentro  
> la misma verdad.
> 
> <a id="_592"></a>
> Escondidos en tus ojitos  
> duermen mis sueños más hermosos,  
> cuándo los abres frente a mi  
> se despiertan alegres y rumbosos.

Which translates as:<a id="_593"></a>
> <a id="_594"></a>
> Between your arms and mine  
> there is no space, so close together  
> we are the thoughts  
> They are one.
> 
> <a id="_595"></a>
> Sometimes we are almost two strangers,  
> strange as strange as they are different,  
> but we deceive ourselves, you know it, I know it,  
> actually we are very inside  
> the same truth.
> 
> <a id="_596"></a>
> Hidden in your eyes  
> my most beautiful dreams sleep,  
> when do you open them in front of me  
> They wake up happy and cheerful.

Not easy [Google](../google-split.md) hits so possibly novel.

---

<a id="image-tank-man"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/ca4f11131eca6b4d61daf707a470cfccd1ef3d80a6f8b70f1f07616b451ca64e.jpg)

**[Figure 69](#image-tank-man). Tank Man**. <a id="_597"></a>
[tx ca4f11131eca6b4d61daf707a470cfccd1ef3d80a6f8b70f1f07616b451ca64e](https://www.blockchain.com/explorer/transactions/btc/ca4f11131eca6b4d61daf707a470cfccd1ef3d80a6f8b70f1f07616b451ca64e), [block 458238](https://www.blockchain.com/explorer/blocks/btc/458238) (2017-03-21) via [cryptograffiti.info](cryptograffiti-info.md).

<a id="_598"></a>
See also: [Section "China"](china.md).

<a id="_599"></a>
Searching for the image hash ca4f11131eca6b4d61daf707a470cfccd1ef3d80a6f8b70f1f07616b451ca64e leads to [https://archive.4plebs.org/pol/thread/191157608/#q191162145](https://archive.4plebs.org/pol/thread/191157608/#q191162145) which links to the now dead as of 2021: [https://cryptograffiti.info/#ca4f11131eca6b4d61daf707a470cfccd1ef3d80a6f8b70f1f07616b451ca64e.jpg](https://cryptograffiti.info/#ca4f11131eca6b4d61daf707a470cfccd1ef3d80a6f8b70f1f07616b451ca64e.jpg).

---

<a id="image-mr-burns-you-re-here-forever"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/94e319d09fc236fb9d7a24e60af8f47ed41ca3cc01e9950c925d806153ed8aa3.jpg)

**[Figure 70](#image-mr-burns-you-re-here-forever). Mr. Burns You're here forever**. <a id="_600"></a>
[tx 94e319d09fc236fb9d7a24e60af8f47ed41ca3cc01e9950c925d806153ed8aa3](https://www.blockchain.com/explorer/transactions/btc/94e319d09fc236fb9d7a24e60af8f47ed41ca3cc01e9950c925d806153ed8aa3) block 460435 (2017-04-05)

<a id="_601"></a>
Mr. Burns from [The Simpsons](../the-simpsons.md) showing a sign:<a id="_602"></a>


> Don't forget, you're here forever

Still from S06E13 of [The Simpsons](../the-simpsons.md). A reference to the immutability of the [blockchain](../blockchain.md).

<a id="video-mr-burns-you-re-here-horever"></a>
**[Video 6](#video-mr-burns-you-re-here-horever). Mr. Burns "You're Here Horever".** [Source](https://www.youtube.com/watch?v=GhSW9vDTRyY). Off-chain source clip for the still.

<a id="_603"></a>
This transaction is given at [Data Insertion in Bitcoin's Blockchain by Andrew Sward, Vecna OP\_0 and Forrest Stonedahl](../data-insertion-in-bitcoin-s-blockchain-by-andrew-sward-vecna-op-0-and-forrest-stonedahl.md). We've decoded it with:<a id="_604"></a>

```
btc getrawtransaction 94e319d09fc236fb9d7a24e60af8f47ed41ca3cc01e9950c925d806153ed8aa3 true | jq -r '.vin[].scriptSig.asm' | sed -r 's/^[^ ]+ //' | sed -r 's/ [^ ]+$//' | tr -d '\n'  | xxd -r -p > tmp.jpg
```
TODO understand the encoding better. Our indexing scripts [Bitcoin Inscription Indexer](../bitcoin-inscription-indexer.md) missed it because the image is encoded on starting on the second constant of the input script and not the first.

<a id="_605"></a>
This was missed by [binwalk](../binwalk.md) because it does not index the valid [JPEG](../jpeg.md) signature "ffd8ffdb"... we should patch it... [https://github.com/ReFirmLabs/binwalk/blob/cddfede795971045d99422bd7a9676c8803ec5ee/src/binwalk/magic/images#L107](https://github.com/ReFirmLabs/binwalk/blob/cddfede795971045d99422bd7a9676c8803ec5ee/src/binwalk/magic/images#L107)

---

<a id="image-augustana-college-old-main-jpg"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/033d185d1a04c4bd6de9bb23985f8c15aa46234206ad29101c31f4b33f1a0e49.jpg" alt="" height="500">

**[Figure 71](#image-augustana-college-old-main-jpg). Augustana College Old-Main.jpg**. <a id="_606"></a>
[tx 033d185d1a04c4bd6de9bb23985f8c15aa46234206ad29101c31f4b33f1a0e49](https://www.blockchain.com/explorer/transactions/btc/033d185d1a04c4bd6de9bb23985f8c15aa46234206ad29101c31f4b33f1a0e49) block 474586 (2017-07-07)

<a id="_607"></a>
First tx 1e347cf7521a1318ef31af4f5758efbc45f1bb2a7db9bc1cc469bfe93599eaf7 sets up 48 [P2SH](../p2sh.md) outputs and gives ASCII message<a id="_608"></a>


> Augustana College Old-Main.jpg Reconstruct with data preceding redeemscripts

<a id="_609"></a>
Then tx 033d185d1a04c4bd6de9bb23985f8c15aa46234206ad29101c31f4b33f1a0e49 redeems those with 48 input scripts that encode the image with ASCII message:<a id="_610"></a>


> Augustana College Old-Main.jpg Reconstruct with data preceding redeemscripts

<a id="_611"></a>
Encoded with [Two-stage P2SH inscription](../two-stage-p2sh-inscription.md). Mentioned at: [Data Insertion in Bitcoin's Blockchain by Andrew Sward, Vecna OP\_0 and Forrest Stonedahl](../data-insertion-in-bitcoin-s-blockchain-by-andrew-sward-vecna-op-0-and-forrest-stonedahl.md). See also this [ASCII art](ascii-art.md) by the same authors: [Code 4. "Study Math and Computer Science at Augustana College"](ascii-art.md#code-study-math-and-computer-science-at-augustana-college). Previously mentioned at: [https://twitter.com/ottosch_/status/1735297943563837726](https://twitter.com/ottosch_/status/1735297943563837726)

---

<a id="image-pdf-demo"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/b4f537bc536c392d425af0693e3282bbf697df01debeeaf7f9918b93af6bdd14.png" alt="" height="600">

**[Figure 72](#image-pdf-demo). PDF demo**. [tx b4f537bc536c392d425af0693e3282bbf697df01debeeaf7f9918b93af6bdd14](https://www.blockchain.com/explorer/transactions/btc/b4f537bc536c392d425af0693e3282bbf697df01debeeaf7f9918b93af6bdd14) block 474646 (2017-07-07) via [cryptograffiti.info](cryptograffiti-info.md) contains a single page 7.9 KB [PDF](../pdf.md) sample file also present e.g. at: [https://www.studocu.com/en-gb/document/harrow-college-uxbridge-college/assessing-risk-in-sport-unit/pdf-sample-its-nothing-dw/61244699](https://www.studocu.com/en-gb/document/harrow-college-uxbridge-college/assessing-risk-in-sport-unit/pdf-sample-its-nothing-dw/61244699). This image is a screenshot of the PDF made manually to make it easier to view here, the actual inscribed file has been uploaded to: [https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/b4f537bc536c392d425af0693e3282bbf697df01debeeaf7f9918b93af6bdd14.pdf](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/b4f537bc536c392d425af0693e3282bbf697df01debeeaf7f9918b93af6bdd14.pdf). The first lines of the document read:<a id="_612"></a>
> <a id="_613"></a>
> Adobe Acrobat PDF Files
> 
> <a id="_614"></a>
> Adobe® Portable Document Format (PDF) is a universal file format that preserves all of the fonts, formatting, colours and graphics of any source document, regardless of the application and platform used to create it.

---

<a id="image-cat-manga"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/4986e9cd20b75bb534df92e60b232945e18274f4c46d25b8853af9bdda5166b8.png)

**[Figure 73](#image-cat-manga). Cat manga**. TODO identify, transcribe japanese. [tx 4986e9cd20b75bb534df92e60b232945e18274f4c46d25b8853af9bdda5166b8](https://www.blockchain.com/explorer/transactions/btc/4986e9cd20b75bb534df92e60b232945e18274f4c46d25b8853af9bdda5166b8), [block 581526](https://www.blockchain.com/explorer/blocks/btc/581526) (2019-06-20).

<a id="image-arms-crossed"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/a55e5e7492848445a9f9ecf55ce566242c9d95e6c46a171fd94a345e8b74c355.jpg" alt="" height="500">

**[Figure 74](#image-arms-crossed). Arms crossed**. Nerdy caucasian [woman](../female.md) in her late teens/early 20's wearing glasses and a jeans jacked with her arms crossed. TODO identify. [tx a55e5e7492848445a9f9ecf55ce566242c9d95e6c46a171fd94a345e8b74c355](https://www.blockchain.com/explorer/transactions/btc/a55e5e7492848445a9f9ecf55ce566242c9d95e6c46a171fd94a345e8b74c355), [block 597374](https://www.blockchain.com/explorer/blocks/btc/597374) (2019-10-01) with [P2FKH](../fake-p2pkh-address.md)

<a id="image-black-cat"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/8cf28eb9ac221d8cd15298b9ae63eca910b536a5234c133c7e364b29a4e39d21.jpg)

**[Figure 75](#image-black-cat). Black cat**. No, [Google reverse image search](../google-reverse-image-search.md) is never going to find the exact one amongst billions of pics. [tx 8cf28eb9ac221d8cd15298b9ae63eca910b536a5234c133c7e364b29a4e39d21](https://www.blockchain.com/explorer/transactions/btc/8cf28eb9ac221d8cd15298b9ae63eca910b536a5234c133c7e364b29a4e39d21), [block 625045](https://www.blockchain.com/explorer/blocks/btc/625045) (2020-04-09) with [P2FKH](../fake-p2pkh-address.md).

<a id="image-teddy-bear"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/546124c6ad55acc6e0cd00a66fbd29e9b7df5fe8505e2ebf8470bb44aa35bc16.jpg)

**[Figure 76](#image-teddy-bear). Teddy bear**. [tx 546124c6ad55acc6e0cd00a66fbd29e9b7df5fe8505e2ebf8470bb44aa35bc16](https://www.blockchain.com/explorer/transactions/btc/546124c6ad55acc6e0cd00a66fbd29e9b7df5fe8505e2ebf8470bb44aa35bc16), [block 654100](https://www.blockchain.com/explorer/blocks/btc/654100) (2020-10-24) with [P2FKH](../fake-p2pkh-address.md). Cost: ~0.002 BTC ~ $25.77 at the time. Transaction made up of 339 \* 550 SAT outputs.

<a id="image-the-starry-night-by-van-gogh"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/225ed8bc432d37cf434f80717286fd5671f676f12b573294db72a2a8f9b1e7ba.jpg)

**[Figure 77](#image-the-starry-night-by-van-gogh). The Starry Night by van Gogh**. <a id="_615"></a>
[tx 225ed8bc432d37cf434f80717286fd5671f676f12b573294db72a2a8f9b1e7ba](https://www.blockchain.com/explorer/transactions/btc/225ed8bc432d37cf434f80717286fd5671f676f12b573294db72a2a8f9b1e7ba), [block 685647](https://www.blockchain.com/explorer/blocks/btc/654100) (2021-05-31) Stored on SegWit. Googling leads to this hit: [https://github.com/aureleoules/bitcandle](https://github.com/aureleoules/bitcandle) by French programmer Aurèle Oulès which is an obscure uploader not known to us before this transaction was found.

<a id="_616"></a>
[tx 8dc2785335c59df6c00257f9b20e5df9b932a717f97066b279e292faba71a67a](https://www.blockchain.com/explorer/transactions/btc/8dc2785335c59df6c00257f9b20e5df9b932a717f97066b279e292faba71a67a) block 685737 contains another one, but with a slightly different encoding, presumably Aureole was trying out different things.

---

<a id="image-kitchen-mirror-selfie-in-swimming-glasses"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/3110f49fb6047d62e6fa198a0a4b180d9abf7075d6f29472747990ae286295cb.jpg" alt="" height="600">

**[Figure 78](#image-kitchen-mirror-selfie-in-swimming-glasses). Kitchen mirror selfie in swimming glasses**. <a id="_617"></a>
[tx 3110f49fb6047d62e6fa198a0a4b180d9abf7075d6f29472747990ae286295cb](https://www.blockchain.com/explorer/transactions/btc/3110f49fb6047d62e6fa198a0a4b180d9abf7075d6f29472747990ae286295cb) block 690497 (2021-07-10). [JPEG](../jpeg.md) using [P2FMS](../pay-to-fake-multisig.md)

<a id="_618"></a>
This [P2FMS](../pay-to-fake-multisig.md) has the peculiarity that each payload constant is preceded by a `04` byte which must be thrown away, we've decoded it manually with:<a id="_619"></a>

```
bitcoin-core.cli getrawtransaction 3110f49fb6047d62e6fa198a0a4b180d9abf7075d6f29472747990ae286295cb true | jq -r '.vout[].scriptPubKey.asm' | head -n-2 | sed -r 's/^....//;s/ 3 .*//' | tr -d ' \n' | xxd -r -p  > tmp.jpg
```

<a id="_620"></a>
This transactions is also mentioned at: [https://github.com/bitcoin/bitcoin/pull/28400](https://github.com/bitcoin/bitcoin/pull/28400) "Make provably unsignable standard P2PK and P2MS outpoints unspendable"

---

<a id="image-gulagu-net-logo"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/9c1a5d5a9e65e9a35050d67574681695a5c46a3df3feb27834848daa49c2fb92.jpg)

**[Figure 79](#image-gulagu-net-logo). Gulagu.net logo**. [tx 9c1a5d5a9e65e9a35050d67574681695a5c46a3df3feb27834848daa49c2fb92](https://www.blockchain.com/explorer/transactions/btc/9c1a5d5a9e65e9a35050d67574681695a5c46a3df3feb27834848daa49c2fb92) block 710352 (2021-11-19) Logo of [https://gulagu.net/](https://gulagu.net/), a "[Russian](../russia.md) anti-corruption, anti-torture human rights organization and website"[https://en.wikipedia.org/wiki/Gulagu.net](https://en.wikipedia.org/wiki/Gulagu.net) [Two-stage P2SH inscription](../two-stage-p2sh-inscription.md).

<a id="image-gulagu-net-people"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/36e7f004ff22aa1146a00705d166fbca64d174c472a5296ed1f38d4749a74e10.jpg)

**[Figure 80](#image-gulagu-net-people). Gulagu.net people**. [tx 36e7f004ff22aa1146a00705d166fbca64d174c472a5296ed1f38d4749a74e10](https://www.blockchain.com/explorer/transactions/btc/36e7f004ff22aa1146a00705d166fbca64d174c472a5296ed1f38d4749a74e10) block 710354 (2021-11-19). Rightmost [Vladimir Osechkin](https://twitter.com/vlad_osechkin). [Two-stage P2SH inscription](../two-stage-p2sh-inscription.md).

<a id="image-low-resolution-gif-screenshot-of-the-bitcoin-whitepaper-intro"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/cad2c46b0f7feb56191f2ab7d8ed59184615cbf0ca46af8c8b5a21a2045a42d2.gif)

**[Figure 81](#image-low-resolution-gif-screenshot-of-the-bitcoin-whitepaper-intro). Low resolution GIF screenshot of the Bitcoin whitepaper intro**. <a id="_621"></a>
[tx cad2c46b0f7feb56191f2ab7d8ed59184615cbf0ca46af8c8b5a21a2045a42d2](https://www.blockchain.com/explorer/transactions/btc/cad2c46b0f7feb56191f2ab7d8ed59184615cbf0ca46af8c8b5a21a2045a42d2) block 724270 (2022-02-21). Inscribed with [P2FKH](../fake-p2pkh-address.md).

<a id="_622"></a>
The payload starts with: `7b260000` before the acutal [GIF](../gif.md), which is why we hadn't found it before using [binwalk](../binwalk.md). TODO what do those bytes mean?

<a id="_623"></a>
The last payload uses [OP\_RETURN](../op-return.md) and encodes the ascii filename:<a id="_624"></a>


> BTGC:satoshi.gif

TODO what is BTGC?

---

<a id="image-a-man-and-his-cactus"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/4719e7252f4bdefd9f7bdf5058f17af28729b79c303b067eb01c107e57235754.jpg)

**[Figure 82](#image-a-man-and-his-cactus). A man and his cactus**. [tx 4719e7252f4bdefd9f7bdf5058f17af28729b79c303b067eb01c107e57235754](https://www.blockchain.com/explorer/transactions/btc/4719e7252f4bdefd9f7bdf5058f17af28729b79c303b067eb01c107e57235754) (2024-01-27). The man depicted is Cryptocurrency developer [Sahil Chaturvedi](https://x.com/SahilC0/status/1980386338450075867). Encoded as a [data URL](../data-uri-scheme.md) for a [JPEG](../jpeg.md) image in an [OP\_RETURN](../op-return.md):<a id="_625"></a>

```
data:image/jpeg;base64
```

Perhaps a meme given the phalic shape of the plant.

---

<a id="_626"></a>
[tx 976e0766ebe0528d44595170f83f46ab1304c0a3b809f16454ee9be0e816e3a3](https://mempool.space/tx/976e0766ebe0528d44595170f83f46ab1304c0a3b809f16454ee9be0e816e3a3), block 921133 (2025-10-28) contains an [OP\_RETURN](../op-return.md) encoded [MP4](../mp4.md) AI generated video of Bitcoin Core developer Gloria Zhao standing up and showing her buttocks. This transaction takes up most of the block with an [Ethereum](../ethereum.md) tatoo on her lower back. Presumably it is from someone criticizing Gloria's design choices regarding [inscriptions on the blockchain](../inscription-blockchain.md). Also mentioned at:<a id="_627"></a>

<a id="_628"></a>
- [https://www.reddit.com/r/btc/comments/1oohqa1/bitcoin_core_v30s_100kb_op_return_where_does/](https://www.reddit.com/r/btc/comments/1oohqa1/bitcoin_core_v30s_100kb_op_return_where_does/)
<a id="_629"></a>
- [https://x.com/zawy3/status/1986499864096837900](https://x.com/zawy3/status/1986499864096837900)

<a id="_630"></a>
TODO decode:<a id="_631"></a>

<a id="_632"></a>
- get all from [Data Insertion in Bitcoin's Blockchain by Andrew Sward, Vecna OP\_0 and Forrest Stonedahl](../data-insertion-in-bitcoin-s-blockchain-by-andrew-sward-vecna-op-0-and-forrest-stonedahl.md), some are missing. TODO list then explicitly here
<a id="_633"></a>
- 6fa03193609f6506c2fa76540fa9930adf68d50b21c942434a90486a694ccacd contains a JPEG in its input script but a bit broken. The script contains a single constant. We could not decode it by looking at nearby transactions either

**Table of contents**

- [cryptograffiti.info](cryptograffiti-info.md)

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

## ← Incoming links (2)

- [Cool data embedded in the Bitcoin blockchain](../cool-data-embedded-in-the-bitcoin-blockchain-split.md)
- [ASCII art](ascii-art.md)
