# Prayer wars

↑ **Parent:** [Themes](themes.md)  
🏷️ **Tags:** [Cute Coinbase messages](cute-coinbase-messages.md)

Starting at [tx cbbaa0a64924fe1d6ace3352f23242aa0028d4e0ff6ae8ed615244d66079cfb1](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/in/0139.txt#L1) ([2011-08-05](https://www.blockchain.com/explorer/transactions/btc/cbbaa0a64924fe1d6ace3352f23242aa0028d4e0ff6ae8ed615244d66079cfb1)), [Catholic](../catholic-church.md) [Bitcoin developer](../bitcoin-developer.md) [Luke Dashjr](../luke-dashjr.md) started to [inscribe](../inscription-blockchain.md) prayers in the [miner messages](../miner-message.md) of his [mining pool](../mining-pool.md) "[Eligius pool](../eligius-pool.md)", usually one verse per message.

<a id="image-saint-eligius-by-petrus-christus"></a>
![](https://upload.wikimedia.org/wikipedia/commons/1/11/Petrus_Christus_003.jpg)

**[Figure 98](#image-saint-eligius-by-petrus-christus). Saint Eligius by Petrus Christus**. [Source](https://commons.wikimedia.org/wiki/File:Petrus_Christus_003.jpg). Off-chain image for illustration. [Eligius pool](../eligius-pool.md) is named after [Saint Eligius](../saint-eligius.md), patron of goldsmiths and miners[https://twitter.com/LukeDashjr/status/1749183638313246875](https://twitter.com/LukeDashjr/status/1749183638313246875)

These are some of the earliest inscriptions in the blockchain, and therefore extremelly visible.

Although the prayer verses appear contiguous in ASCII dumps, Eligius was not actually mining every block: it is just that in those early days, miners still hadn't started adding advertisement messages to every block, so only Eligius shows up and appears contiguous.

At some point, opponents noticed these messages, and started adding atheist mockery graffiti replies, which appear interspersed in ASCII dumps with the prayer.

The first prayer is  the [Latin](../latin.md) version of the [Divine Praises](../divine-praises.md), a [Catholic](../catholic-church.md) prayer composed in 1797 in [Italian](../italy.md) by Luigi Felici for the purpose of making reparation after saying or hearing sacrilege or blasphemy. Luke claims he was referring to anything in particular that came prior in the blockchain: [https://twitter.com/LukeDashjr/status/1749182637569122434](https://twitter.com/LukeDashjr/status/1749182637569122434). There arent many earlier inscriptions at all to refer to in any case! The prayer and correspondong interrupts (in transaction outputs, not by other miners) ordered by block are:

- [139690](https://www.blockchain.com/explorer/blocks/btc/139690) (2011-08-05) prayer: "Eligius/Benedictus Deus. Benedictum Nomen Sanctum eius."
- [139717](https://www.blockchain.com/explorer/blocks/btc/139717) prayer: "Eligius/Benedictus Deus. Benedictum Nomen Sanctum eius.'
- [139758](https://www.blockchain.com/explorer/blocks/btc/139758) interruption: `***************************************************`. This is not a [Coinbase message](../coinbase-message.md): [https://www.blockchain.com/explorer/transactions/btc/23befff6eea3dded0e34574af65c266c9398e7d7d9d07022bf1cd526c5cdbc94](https://www.blockchain.com/explorer/transactions/btc/23befff6eea3dded0e34574af65c266c9398e7d7d9d07022bf1cd526c5cdbc94). This [Bitcoin input script](../bitcoin-input-script.md) appears to spend a standard [P2PKH](../p2pkh.md) output, but it first adds an extra value to the stack which contains the `***`.
- [139792](https://www.blockchain.com/explorer/blocks/btc/139792) prayer: "Benedictus Iesus Christus, verus Deus et verus homo.'
- [139831](https://www.blockchain.com/explorer/blocks/btc/139831) prayer: "Benedictum Nomen Iesu.'
- [139838](https://www.blockchain.com/explorer/blocks/btc/139838) (2011-08-06) interruption: "I LIKE TURTLES" (tx 78eb16507b3d3df615e3b474e853db4667f4b11954ec6d918b1ded0fca7ad25a)
- [138898](https://www.blockchain.com/explorer/blocks/btc/138898) prayer: "Benedictum Cor eius sacratissimum."
- [139904](https://www.blockchain.com/explorer/blocks/btc/139904) prayer: "Benedictus Sanguis eius pretiosissimus."
- [139921](https://www.blockchain.com/explorer/blocks/btc/139921) prayer: "Benedictus Iesus in sanctissimo altaris Sacramento."
- [139942](https://www.blockchain.com/explorer/blocks/btc/139942) prayer: "Benedictus Sanctus Spiritus, Paraclitus."
- [139954](https://www.blockchain.com/explorer/blocks/btc/139954) interrupion: "aC-C-C-COMBO BREAKER" (tx 138c024a76df99ecafd2236d5429cf574b7778a3c6508bd83f116c832f3c6980)
- [139960](https://www.blockchain.com/explorer/blocks/btc/139960) prayer: "Benedictus Sanctus Spiritus, Paraclitus."
- [139977](https://www.blockchain.com/explorer/blocks/btc/139977) prayer: "Benedicta excelsa Mater Dei, Maria sanctissima."
- [139990](https://www.blockchain.com/explorer/blocks/btc/139990) (2011-08-06) prayer: "Benedicta sancta eius et immaculata Conceptio."

Then comes:
- [140181](https://www.blockchain.com/explorer/blocks/btc/140181) [Latin](../latin.md) [Trinitarian formula](https://ourbigbook.com/-/topic/trinitarian-formula)> In nomine Patris et Filii et Spiritus Sancti. Amen.
- [Act of Contrition](https://ourbigbook.com/-/topic/act-of-contrition)
- [Act of Hope](https://ourbigbook.com/-/topic/act-of-hope)
and various others + output message interruptions.

Then at last come the first [miner message](../miner-message.md) interruptions. Luke explained on Twitter[https://twitter.com/LukeDashjr/status/1749183094081335413](https://twitter.com/LukeDashjr/status/1749183094081335413) that they were also made by Eligius pool, as there was a system in which contributors besides Luke could submit their own strings:
- [142547](https://www.blockchain.com/explorer/blocks/btc/142547): (2011-08-25) tx 8e1e44a48b5e79636675d1476f8e4add075bbeb7f49e00ec743eed56f17feaaa A yandere game is starting in 60 seconds! Please type "\]yandere" to join. [Yandere Simulator](https://ourbigbook.com/-/topic/yandere-simulator) comes to mind, but it can't be because that was pitched 2014.
- [142550](https://www.blockchain.com/explorer/blocks/btc/142550): "A yandere game is starting in 60 seconds! Please type "\]yandere" to join."
- [142573](https://www.blockchain.com/explorer/blocks/btc/142573): (2011-08-25) "Militant atheists, [http://bit.ly/naNhG2](http://bit.ly/naNhG2) -- happy now?". A [Rickrolling](rickrolling.md) link. Perhaps one of the fist.
- [142596](https://www.blockchain.com/explorer/blocks/btc/142596): (2011-08-25) "\<cjdelisle\> ran out of prayers?! That explains the price drop.". Possibly quoting this dude on som [https://twitter.com/cjdelisle](https://twitter.com/cjdelisle) [Bitcoin IRC channel](../bitcoin-irc-channel.md) givesn the `<USERNAME>` format?
- [142640](https://www.blockchain.com/explorer/blocks/btc/142640): "an de ti go su by ra me ni ko hu vy la po fy ton": [Tonal system](https://ourbigbook.com/-/topic/tonal-system) numerals. Interesting.
followed by more prayers and interruptions such as [tx ec92d245822fa1ff862f3314b9102f36fe1eb8bc055865674c75323540aedef6](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0142.txt#L10):

> FFS [Luke-Jr](../luke-dashjr.md) leave the blockchain alone!  
> Oh, and [God](../god.md) isn't real

The last Luke prayer appears to be on [block 143822](https://www.blockchain.com/explorer/blocks/btc/143822) (2011-09-03)

> ... the Lord of the harvest, that he send forth labourers into his harvest.

Then there is a bit of [radio silence](https://ourbigbook.com/-/topic/radio-silence), until finally [Slush Pool](../slush-pool.md) started self advertising for the first time on [block 163970](https://www.blockchain.com/explorer/blocks/btc/163970) (2012-01-26):
```
/P2SH/BIP16/slush/R,
```
They had been mining for a long time by then (December 2010 according to [https://en.bitcoin.it/wiki/Slush_Pool](https://en.bitcoin.it/wiki/Slush_Pool)), but this is when they decided to add a human readable [ASCII](../ascii.md) message as well.

From then on, [miner messages](../miner-message.md) would be forever polluted with ads, and Luke's multi-[miner message](../miner-message.md) feat would never again be reproduced.

The non-obvious interruptions are all well known [memes](../meme.md)/anime references:
- "I like turtles": [https://knowyourmeme.com/memes/i-like-turtles](https://knowyourmeme.com/memes/i-like-turtles)
- Combo breaker: [https://knowyourmeme.com/memes/combo-breaker](https://knowyourmeme.com/memes/combo-breaker)
- "Yukkuri Shiteitte ne": [https://knowyourmeme.com/memes/yukkuri-shiteitte-ne](https://knowyourmeme.com/memes/yukkuri-shiteitte-ne)
- "kLhLUKE-JR IS A [Pedophile](../pedophilia.md)! Oh, and [God](../god.md) isn't real, sucka. Stop polluting the blockchain with your nonsense.", [tx 9740e7d646f5278603c04706a366716e5e87212c57395e0d24761c0ae784b2c6](https://www.blockchain.com/explorer/transactions/btc/9740e7d646f5278603c04706a366716e5e87212c57395e0d24761c0ae784b2c6), [block 141460](https://www.blockchain.com/explorer/blocks/btc/141460)
- "Help me, ERINNNNNN!!": [https://touhou.fandom.com/wiki/Lyrics:_Help_me,_ERINNNNNN!!](https://touhou.fandom.com/wiki/Lyrics:_Help_me,_ERINNNNNN!!)
- "EASY MODO? How lame!F?": [https://knowyourmeme.com/memes/kimoi-girls](https://knowyourmeme.com/memes/kimoi-girls)

Bibliography:
- 2011-08-19 [https://bitcointalk.org/index.php?topic=38007.0](https://bitcointalk.org/index.php?topic=38007.0) "Eligius miners aware of prayers in block headers?" from on [bitcointalk.org](../bitcoin-forum.md) by user "Graet" who quotes prior discussion from a [Bitcoin IRC channel](../bitcoin-irc-channel.md):> \<luke-jr\> cosurgi: by design, it contains "random" data-- I've just been setting some of that "random" data to prayers
  > 
  > \<Graet\> mm interesting luke-jr i understand you are strong in your faith but you dont think putting prayers in might alienate some ppl - after all btc is multidenominational
  > 
  > \<luke-jr\> Graet: Catholics do not believe in freedom of religion.
  > 
  > \<Graet\> and you make your non catholic miners aware of this?
- 2011-11-02 [https://bitcointalk.org/index.php?topic=52979.0](https://bitcointalk.org/index.php?topic=52979.0) "Mysterious transaction spotted in blockchain!"

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

## ← Incoming links (7)

- [Coinbase message](../coinbase-message.md)
- [Cool data embedded in the Bitcoin blockchain](../cool-data-embedded-in-the-bitcoin-blockchain-split.md)
- [Force of Will](force-of-will.md)
- [Incoming links](incoming-links.md)
- [Rickrolling](rickrolling.md)
- [Divine Praises](../divine-praises.md)
- [Luke Dashjr](../luke-dashjr.md)
