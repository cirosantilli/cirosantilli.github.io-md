# Bitcoin varint

↑ **Parent:** [Bitcoin protocol data type](bitcoin-protocol-data-type.md)

[https://en.bitcoin.it/wiki/Protocol_documentation#Variable_length_integer](https://en.bitcoin.it/wiki/Protocol_documentation#Variable_length_integer)

Implementations:
- [Python](python-programming-language.md): [https://github.com/alecalve/python-bitcoin-blockchain-parser/blob/c06f420995b345c9a193c8be6e0916eb70335863/blockchain_parser/utils.py#L41](https://github.com/alecalve/python-bitcoin-blockchain-parser/blob/c06f420995b345c9a193c8be6e0916eb70335863/blockchain_parser/utils.py#L41). Sample usage to extract 3 values from a `bytes` object:
  ```
  file, off = decode_varint(value)
  blk_off, off = decode_varint(value[off:])
  tx_off, off = decode_varint(value[off:])
  ```

## ↑ Ancestors (11)

1. [Bitcoin protocol data type](bitcoin-protocol-data-type.md)
2. [Bitcoin protocol](bitcoin-protocol.md)
3. [Bitcoin](bitcoin.md)
4. [List of cryptocurrencies](list-of-cryptocurrencies.md)
5. [Cryptocurrency](cryptocurrency-split.md)
6. [Blockchain](blockchain.md)
7. [Money](money.md)
8. [Social technology](social-technology-split.md)
9. [Area of technology](area-of-technology.md)
10. [Technology](technology-split.md)
11. [Ciro Santilli's Homepage](split.md)
