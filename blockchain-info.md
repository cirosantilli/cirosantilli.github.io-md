<h1 id="blockchain-info">Blockchain.info</h1>

↑ **Parent:** [Blockchain explorer website](blockchain-explorer-website.md)

TODO who owns it? Are they reliable?

- transaction hex data: [https://blockchain.info/tx/930a2114cdaa86e1fac46d15c74e81c09eee1d4150ff9d48e76cb0697d8e1d72?format=hex](https://blockchain.info/tx/930a2114cdaa86e1fac46d15c74e81c09eee1d4150ff9d48e76cb0697d8e1d72?format=hex)
- disassembled transaction as JSON: [https://blockchain.info/tx/930a2114cdaa86e1fac46d15c74e81c09eee1d4150ff9d48e76cb0697d8e1d72?format=json](https://blockchain.info/tx/930a2114cdaa86e1fac46d15c74e81c09eee1d4150ff9d48e76cb0697d8e1d72?format=json)
- block by height:
  - [https://blockchain.info/block/0?format=json](https://blockchain.info/block/0?format=json)
  - [https://blockchain.info/block/0?format=hex](https://blockchain.info/block/0?format=hex)

This helper dumps a transaction JSON to a binary:
```
bitcoin-tx-out-scripts() (
    # Dump data contained in out scripts. Remove first 3 last 2 bytes of
    # standard transaction boilerplate.
    h="$1"
    echo curl "https://blockchain.info/tx/${h}?format=json" |
    jq '.out[].script' tmp.json |
    sed 's/"76a914//;s/88ac"//' |
    xxd -r -p > "${h}.bin"
)
```

Their API limit witout key is 1 query per 10 seconds!!!

## ↑ Ancestors (12)

1. [Blockchain explorer website](blockchain-explorer-website.md)
2. [Blockchain explorer](blockchain-explorer.md)
3. [How to extract data from the Bitcoin blockchain](how-to-extract-data-from-the-bitcoin-blockchain.md)
4. [Bitcoin](bitcoin.md)
5. [List of cryptocurrencies](list-of-cryptocurrencies.md)
6. [Cryptocurrency](cryptocurrency-split.md)
7. [Blockchain](blockchain.md)
8. [Money](money.md)
9. [Social technology](social-technology-split.md)
10. [Area of technology](area-of-technology.md)
11. [Technology](technology-split.md)
12. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (1)

- [Satoshi uploader](satoshi-uploader.md)
