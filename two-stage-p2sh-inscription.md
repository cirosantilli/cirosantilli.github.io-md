# Two-stage P2SH inscription

↑ **Parent:** [Bitcoin inscription method](bitcoin-inscription-method.md)

To decode these, we throw away the last tx and the last constant of each input, e.g.:
```
btc getrawtransaction 033d185d1a04c4bd6de9bb23985f8c15aa46234206ad29101c31f4b33f1a0e49 true | jq -r '.vin[].scriptSig.asm' | head -n -1 | sed -r 's/ [^ ]+$//' | tr -d '\n'  | xxd -r -p > tmp.jpg
```

Terminology mentioned e.g. at: [Data Insertion in Bitcoin's Blockchain by Andrew Sward, Vecna OP\_0 and Forrest Stonedahl](data-insertion-in-bitcoin-s-blockchain-by-andrew-sward-vecna-op-0-and-forrest-stonedahl.md).

## ↑ Ancestors (11)

1. [Bitcoin inscription method](bitcoin-inscription-method.md)
2. [Bitcoin inscription](bitcoin-inscription.md)
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

- [Raw images](cool-data-embedded-in-the-bitcoin-blockchain/raw-images.md)
