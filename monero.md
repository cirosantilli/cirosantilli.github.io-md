# Monero

↑ **Parent:** [List of cryptocurrencies](list-of-cryptocurrencies.md)  
🏷️ **Tags:** [Privacy coin](privacy-coin.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Monero)

Cryptocurrency with focus on [anonymity](anonymity.md). Was almost certainly the leading [privacy coin](privacy-coin.md) since its inception until as of writing in the 2020s.

[Ciro Santilli](ciro-santilli-split.md) has received and held considerable quantities of [Monero](monero.md), notably [1000 Monero donation](sponsor/1000-monero-donation.md). so bias alert.

As mentioned at [Section "Are cryptocurrencies useful?"](are-cryptocurrencies-useful.md), [Ciro Santilli](ciro-santilli-split.md) believes that anonymity is the most valuable feature that really matters on crypto coins, and therefore if he were to invest in crypto, he would invest in Monero or some other [privacy coin](privacy-coin.md).

[https://localmonero.co/knowledge/monero-stealth-addresses?language=en](https://localmonero.co/knowledge/monero-stealth-addresses?language=en) gives an overview of the privacy mechanisms:
- [ring signatures](ring-signature.md), which hide the true output (sender)

  [https://localmonero.co/knowledge/ring-signatures](https://localmonero.co/knowledge/ring-signatures) Gives an overview. Mentions that it is prone to heuristic attacks.

  Uses a system of decoys, that adds 10 fake possible previous outputs as inputs, in addition to the actual input.

  So the network only knows/verifies that one of those 11 previous outputs was used, but it does not know which one.

  It's a bit like having a built-in [cryptocurrency tumbler](cryptocurrency-tumbler.md) in every transaction.

  TODO so how do you know which previous outputs were spent or not?
- RingCT which hides the amounts.
- stealth addresses, which hides who you send to

  This forces receivers to scan try and unlock every single transaction in the chain to see if it is theirs or not.

  The sender therefore can know when the money is spent, but once again, not to whom it is being sent.

Based on [https://en.wikipedia.org/wiki/CryptoNote](https://en.wikipedia.org/wiki/CryptoNote) and like [Satoshi Nakamoto](satoshi-nakamoto.md) created by under the pseudonym "Nicolas van Saberhagen" [https://www.reddit.com/r/Monero/comments/7v2obe/offering_a_bounty_for_a_video_of_the_speech_by/](https://www.reddit.com/r/Monero/comments/7v2obe/offering_a_bounty_for_a_video_of_the_speech_by/)

[Coinbase](coinbase.md) has actually stayed away from trading it even as of 2019 when Monero was the third largest market capitalization crypto because of fear of regulatory slashback: [https://decrypt.co/36731/heres-why-coinbase-still-hasnt-listed-monero](https://decrypt.co/36731/heres-why-coinbase-still-hasnt-listed-monero). Although it must be said, the value of privacy crypto is greatly reduced when everyone is trading it on exchanges, which require a passport upload to work.

**Table of contents**

- [Monero Chan](monero-chan.md)
- [How to mine Monero](how-to-mine-monero.md)
- [Monero mining](monero-mining.md)
  - [Monero ASIC resistance](monero-asic-resistance.md)
    - [Monero GPU mining](monero-gpu-mining.md)
  - [RandomX](randomx.md)
- [Monero community](monero-community.md)
  - [Monero Core Team](monero-core-team.md)
    - [Riccardo Spagni](riccardo-spagni.md)
  - [DontTraceMeBruh](donttracemebruh.md)

## ↑ Ancestors (8)

1. [List of cryptocurrencies](list-of-cryptocurrencies.md)
2. [Cryptocurrency](cryptocurrency-split.md)
3. [Blockchain](blockchain.md)
4. [Money](money.md)
5. [Social technology](social-technology-split.md)
6. [Area of technology](area-of-technology.md)
7. [Technology](technology-split.md)
8. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (16)

- [Are cryptocurrencies useful?](are-cryptocurrencies-useful.md)
- [CIA 2010 covert communication websites](cia-2010-covert-communication-websites-split.md)
- [P51 benchmark](ciro-santilli-s-hardware/p51-benchmark.md)
- [Other blockchains](cool-data-embedded-in-the-bitcoin-blockchain/other-blockchains.md)
- [Cryptocurrency swapper](cryptocurrency-swapper.md)
- [Electronic voting](electronic-voting.md)
- [Freedom of speech](freedom-of-speech.md)
- [Monero](monero.md)
- [Privacy coin](privacy-coin.md)
- [Ring signature](ring-signature.md)
- [Serai DEX](serai-dex.md)
- [Sponsor Ciro Santilli's work on OurBigBook.com](sponsor-split.md)
- [1000 Monero donation](sponsor/1000-monero-donation.md)
- [Anonymity of the donation](sponsor/1000-monero-donation/anonymity-of-the-donation.md)
- [Barclays regulation](sponsor/1000-monero-donation/barclays-regulation.md)
- [THORSwap](thorswap.md)
