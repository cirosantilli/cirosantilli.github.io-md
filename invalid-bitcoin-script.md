# Invalid Bitcoin script

↑ **Parent:** [Bitcoin script type](bitcoin-script-type.md)

They appear to be included, with rationale that you can already include syntactically valid crap in an unprovable way: [https://github.com/bitcoin/bitcoin/issues/320](https://github.com/bitcoin/bitcoin/issues/320) Better then have syntactically invalid crap that is provable.

The outputs of this transaction seem to be the first syntactically incorrect scripts of the blockchain: [https://blockchain.info/tx/ebc9fa1196a59e192352d76c0f6e73167046b9d37b8302b6bb6968dfd279b767?format=json](https://blockchain.info/tx/ebc9fa1196a59e192352d76c0f6e73167046b9d37b8302b6bb6968dfd279b767?format=json), found by parsing everything locally. The transaction was made in 2013 for 0.1 [BTC](bitcoin.md), which then became unspendable.

The first invalid script is just e.g. "script":"01", which says will push one byte into the stack, but then ends prematurely.

## ↑ Ancestors (12)

1. [Bitcoin script type](bitcoin-script-type.md)
2. [Bitcoin script](bitcoin-script.md)
3. [How Bitcoin works](how-bitcoin-works.md)
4. [Bitcoin](bitcoin.md)
5. [List of cryptocurrencies](list-of-cryptocurrencies.md)
6. [Cryptocurrency](cryptocurrency-split.md)
7. [Blockchain](blockchain.md)
8. [Money](money.md)
9. [Social technology](social-technology-split.md)
10. [Area of technology](area-of-technology.md)
11. [Technology](technology-split.md)
12. [Ciro Santilli's Homepage](split.md)
