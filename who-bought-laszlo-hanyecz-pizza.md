# Who bought Laszlo Hanyecz pizza?

↑ **Parent:** [Laszlo's pizzas](laszlo-s-pizzas.md)

TODO who bought the Bitcoins? Is anyone else besides [Jeremy Sturdivant](jeremy-sturdivant.md)

The original forum thread [https://bitcointalk.org/index.php?topic=137.msg1195](https://bitcointalk.org/index.php?topic=137.msg1195) suggests multiple purchases were made, until he had to withdrawl the offer. Perhaps an easier question is how many pizzas he got in the first place.

[https://www.reddit.com/r/Bitcoin/comments/13on6px/comment/jl55025/?utm_source=reddit&utm_medium=web2x&context=3](https://www.reddit.com/r/Bitcoin/comments/13on6px/comment/jl55025/?utm_source=reddit&utm_medium=web2x&context=3) mentions without source:

> I know. Laszlo Hanyecz estimates that he spent 100,000 [BTC](bitcoin.md) on pizza in 2010. Laszlo is the man that invented [GPU](graphics-processing-unit.md) mining and he mined well over 100,000 [BTC](bitcoin.md).

One source is: [https://bitcoinmagazine.com/culture/the-man-behind-bitcoin-pizza-day-is-more-than-a-meme-hes-a-mining-pioneer](https://bitcoinmagazine.com/culture/the-man-behind-bitcoin-pizza-day-is-more-than-a-meme-hes-a-mining-pioneer)

Related thread from May 2023: [https://bitcointalk.org/index.php?topic=5453728.msg62286606#msg62286606](https://bitcointalk.org/index.php?topic=5453728.msg62286606#msg62286606) "Did Laszlo Hanyecz exchange 40000 [BTC](bitcoin.md) for 8 pizzas, not 10000 [BTC](bitcoin.md) for 2 pizzas?" but their Googling is so bad no one had found the 100,000 quote before Ciro.

As per [https://bitcoin.stackexchange.com/questions/113831/searching-the-blockchain-based-on-transaction-amount-and-or-date](https://bitcoin.stackexchange.com/questions/113831/searching-the-blockchain-based-on-transaction-amount-and-or-date) at [https://blockchair.com/bitcoin/outputs?s=time(asc)&q=value(1000000000000),time(2010-05-18..2010-08-05)](https://blockchair.com/bitcoin/outputs?s=time(asc)&q=value(1000000000000),time(2010-05-18..2010-08-05)) we can list all the transactions made between the offer and withdrawal dates for value exactly 10k. There are only about 20 of them, and including someone the 22nd of May, so it is extremely likely that this will contain the hits. No repeated recipients however, so it is hard to progress with more advanced analytics tools

Some of the transactions are:
- [49d2adb6e476fa46d8357babf78b1b501fd39e177ac7833124b3f67b17c40c2a](https://www.blockchain.com/explorer/transactions/btc/49d2adb6e476fa46d8357babf78b1b501fd39e177ac7833124b3f67b17c40c2a) (22 May 2010 06:17:59 GMT+1). This one has some [Google](google-split.md) mentions:
  - [https://github.com/bitcoinbook/bitcoinbook/blob/6c472dd00b649b18b6ca6bbcc8ba23775619ce08/appdx-pycoin.asciidoc](https://github.com/bitcoinbook/bitcoinbook/blob/6c472dd00b649b18b6ca6bbcc8ba23775619ce08/appdx-pycoin.asciidoc)
  - [https://github.com/richardkiss/pycoin/blob/367a58e25aacf85549a7335f7607ba8a53727c81/COMMAND-LINE-TOOLS.md](https://github.com/richardkiss/pycoin/blob/367a58e25aacf85549a7335f7607ba8a53727c81/COMMAND-LINE-TOOLS.md)
  This is a highly unusual transaction from a single address [17WFx2GQZUmh6Up2NDNCEDk3deYomdNCfk](https://www.blockchain.com/explorer/addresses/btc/17WFx2GQZUmh6Up2NDNCEDk3deYomdNCfk) to a single address [1CZDM6oTttND6WPdt3D6bydo7DYKzd9Qik](https://www.blockchain.com/explorer/addresses/btc/1CZDM6oTttND6WPdt3D6bydo7DYKzd9Qik) for the exact value with no [change](change-bitcoin.md).

  By digging a bit, we see that the input comes from exactly 20 outputs, e.g. [1E43t1VCc3Q3STKauEiUoVqLbT81XT67xj](https://www.blockchain.com/explorer/addresses/btc/1E43t1VCc3Q3STKauEiUoVqLbT81XT67xj), each of which is a block reward of 50 BTC, the [reward value at those early times](bitcoin-halving.md), thus satisfactorily explaining how the exact 10k value was obtained without [change](change-bitcoin.md). Because we know that Laszlo was a big [GPU](graphics-processing-unit.md) miner, it is extremelly likely that this transaction was made by him.
- [a1075db55d416d3ca199f55b6084e2115b9345e16c5cf302fc80e9d5fbf5d48d](https://www.blockchain.com/explorer/transactions/btc/a1075db55d416d3ca199f55b6084e2115b9345e16c5cf302fc80e9d5fbf5d48d) (22 May 2010 07:16:31 GMT+1) also has several [Google](google-split.md) mentions, e.g.:
  - [https://tokenview.medium.com/bitcoin-pizza-day-the-story-of-buying-pizza-with-10-000-btc-54cd0896f9f1](https://tokenview.medium.com/bitcoin-pizza-day-the-story-of-buying-pizza-with-10-000-btc-54cd0896f9f1)

  [https://www.blockchain.com/explorer/transactions/btc/a1075db55d416d3ca199f55b6084e2115b9345e16c5cf302fc80e9d5fbf5d48d](https://www.blockchain.com/explorer/transactions/btc/a1075db55d416d3ca199f55b6084e2115b9345e16c5cf302fc80e9d5fbf5d48d) even specially marks it "Bitcoin Pizza" and "Notable". Furthermore, the receiving address [17SkEw2md5avVNyYgj6RiXuQKNwkXaxFyQ](https://www.blockchain.com/explorer/addresses/btc/17SkEw2md5avVNyYgj6RiXuQKNwkXaxFyQ) is even marked as verified an as belonging to [Jeremy Sturdivant](jeremy-sturdivant.md).

  Furthermore this also shows us how Jeremy then transferred about half of Bitcoins 10 minutes later, but we can't know if it was to his own accounts or to cash out.

  The nature of this transaction is very different from the previous one. It uses a bunch of inputs to a single address [1XPTgDRhN8RFnzniWCddobD9iKZatrvH4](https://www.blockchain.com/explorer/addresses/btc/1XPTgDRhN8RFnzniWCddobD9iKZatrvH4). 1XPTgDRhN8RFnzniWCddobD9iKZatrvH4 contains a mixture of regular small inputs, but also a bunch of block rewards e.g. [https://www.blockchain.com/explorer/addresses/btc/1MUoh2nJudSDdKu9NkcevaCG1Qe3nZHWFZ](https://www.blockchain.com/explorer/addresses/btc/1MUoh2nJudSDdKu9NkcevaCG1Qe3nZHWFZ), thus also clearly indicating Lsazlo ownership.
8 [d1a429c05868f9be6cf312498b77f4e81c2d4db3268b007b6b80716fb56a35ad](https://www.blockchain.com/explorer/transactions/btc/d1a429c05868f9be6cf312498b77f4e81c2d4db3268b007b6b80716fb56a35ad) (29 May) is a common looking transaction with a single input from [1Bc7T7ygkKKvcburmEg14hJKBrLD7BXCkX](https://www.blockchain.com/explorer/addresses/btc/1Bc7T7ygkKKvcburmEg14hJKBrLD7BXCkX) and two outputs, one likely being the change to [1GH4dRUAagj67XVjr4TV6J9RFNmGYsLe7c](https://www.blockchain.com/explorer/addresses/btc/1GH4dRUAagj67XVjr4TV6J9RFNmGYsLe7c) and the other the actual value to [138eoqfNcEdeU9EG9CKfAxnYYz62uHRNrA](https://www.blockchain.com/explorer/addresses/btc/138eoqfNcEdeU9EG9CKfAxnYYz62uHRNrA).

  The input chain is complex, but it does contain one block reward on the third level: [17PBFeDzks3LzBTyt6bAMATNhowrvx5kBw](https://www.blockchain.com/explorer/addresses/btc/17PBFeDzks3LzBTyt6bAMATNhowrvx5kBw) + 79 rewards 4th level at [045795627ca29ec72a94c23a65ee775ea1949d60b6fba0938b75e1cfe1e6643e](https://www.blockchain.com/explorer/transactions/btc/045795627ca29ec72a94c23a65ee775ea1949d60b6fba0938b75e1cfe1e6643e).
- [d3498960e5f73031f726cb878382cc696938810fa43f918696cbf242afc9765e](https://www.blockchain.com/btc/tx/d3498960e5f73031f726cb878382cc696938810fa43f918696cbf242afc9765e) (04 June): complex chain, unclear
- [2ea2914c131b2798041a80c00c44081a3559233d69d8b367e4244e6b12096610](https://www.blockchain.com/explorer/transactions/btc/2ea2914c131b2798041a80c00c44081a3559233d69d8b367e4244e6b12096610) (10 June): single input/single output. Complex input, but has some 2nd order mines e.g. [e6393f613ef12f5708fa511875b8ff5080f6c8864709f8d92bd99435826a9d0d](https://www.blockchain.com/explorer/transactions/btc/e6393f613ef12f5708fa511875b8ff5080f6c8864709f8d92bd99435826a9d0d)
- [ea595789878b673776d0577cbc6063db611bb4e2954e226459d556995f547922](https://www.blockchain.com/explorer/transactions/btc/ea595789878b673776d0577cbc6063db611bb4e2954e226459d556995f547922) (24 June): single input/single output. Complex input, but has some 2nd order mines e.g. [b9a0c2d24a744b79fe001a67468c456746b74e94a6ce68a2e5f80bf645d678b9](https://www.blockchain.com/explorer/transactions/btc/b9a0c2d24a744b79fe001a67468c456746b74e94a6ce68a2e5f80bf645d678b9)
- [461f91a98bbe2f269d8af938039e185287761677f0418fcc8238c5f3dca72935](https://www.blockchain.com/explorer/transactions/btc/461f91a98bbe2f269d8af938039e185287761677f0418fcc8238c5f3dca72935) (02 Jul 2010 08:39:17 GMT+1): single 20k input to two 10k outputs. Did he get 2x two pizzas at once? Complex input.
- [a47f927ca1adeeb4394200e8a37a9297b07e784a251569074a9fc2c04855560f](https://www.blockchain.com/explorer/transactions/btc/a47f927ca1adeeb4394200e8a37a9297b07e784a251569074a9fc2c04855560f) (02 Jul 2010 09:07:35 GMT+1): too close in time to the previous one, unless he was having a massive pizza party with invitees!
- [77036fa2ac75212be1ce93e8e1008d5cb2bcbb51aa560a5fe29c9c1423bbd00e](https://www.blockchain.com/explorer/transactions/btc/77036fa2ac75212be1ce93e8e1008d5cb2bcbb51aa560a5fe29c9c1423bbd00e) (02 Jul 2010 09:14:33 GMT+1): the party grows even larger

## ↑ Ancestors (11)

1. [Laszlo's pizzas](laszlo-s-pizzas.md)
2. [History of Bitcoin](history-of-bitcoin.md)
3. [Bitcoin](bitcoin.md)
4. [List of cryptocurrencies](list-of-cryptocurrencies.md)
5. [Cryptocurrency](cryptocurrency-split.md)
6. [Blockchain](blockchain.md)
7. [Money](money.md)
8. [Social technology](social-technology-split.md)
9. [Area of technology](area-of-technology.md)
10. [Technology](technology-split.md)
11. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (1)

- [Laszlo's pizzas](laszlo-s-pizzas.md)
