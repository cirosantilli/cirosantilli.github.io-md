# Get Bitcoin transaction id from position in dat file

↑ **Parent:** [Bitcoin HOWTO](bitcoin-howto.md)

Suppose we specify:
- a .dat file
- the offset in bytes within that file
The question then is, which transaction is encoded at that position of the file?

This would allow us to index inscriptions in the .dat files directly with fast C tools, and then retrive the transaction ID to get cleaner data and metadata.

It should be possible if we managed to take the information from [https://bitcoindev.network/understanding-the-data/](https://bitcoindev.network/understanding-the-data/) and dump into an indexed [SQLite](sqlite.md) database.

I tried to start things off with [LevelDBDumper](leveldbdumper.md):
```
LevelDBDumper -d ~/snap/bitcoin-core/common/.bitcoin/indexes/txindex -f btc.csv -q -o . -t csv
```
but that consumed all 64 GB of RAM on [P51](ciro-santilli-s-hardware/lenovo-thinkpad-p51-2017.md)... [https://github.com/mdawsonuk/LevelDBDumper/issues/15](https://github.com/mdawsonuk/LevelDBDumper/issues/15)

But OK, nevermind that repo, it can be done easily with the [LevelDB](leveldb.md) API of any language: [https://bitcoin.stackexchange.com/questions/121888/what-is-the-data-format-layout-for-txindex-leveldb-values](https://bitcoin.stackexchange.com/questions/121888/what-is-the-data-format-layout-for-txindex-leveldb-values). Just the data seems wrong and we don't know why.

## ↑ Ancestors (10)

1. [Bitcoin HOWTO](bitcoin-howto.md)
2. [Bitcoin](bitcoin.md)
3. [List of cryptocurrencies](list-of-cryptocurrencies.md)
4. [Cryptocurrency](cryptocurrency-split.md)
5. [Blockchain](blockchain.md)
6. [Money](money.md)
7. [Social technology](social-technology-split.md)
8. [Area of technology](area-of-technology.md)
9. [Technology](technology-split.md)
10. [Ciro Santilli's Homepage](split.md)
