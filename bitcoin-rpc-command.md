# Bitcoin RPC command

↑ **Parent:** [Bitcoin daemon](bitcoin-daemon.md)

These are commands that e.g. the [Bitcoin CLI client](bitcoin-cli-client.md) can make to the server.

[https://bitcoincore.org/en/doc/22.0.0/rpc/rawtransactions/getrawtransaction/](https://bitcoincore.org/en/doc/22.0.0/rpc/rawtransactions/getrawtransaction/)

The commands can be listed with:
```
bitcoin-core.cli help
```
and full help with:
```
bitcoin-core.cli help getrawtransaction
```

For example. to run the [Bitcoin `getrawtransaction` command](bitcoin-getrawtransaction-command.md), first in one shell we start [bitcoind](bitcoin-daemon.md):
```
bitcoin-core.daemon
```
and then on another shell:
```
bitcoin-core.cli getrawtransaction 75b431e0a8c4617ca8adefe593ba66aa30907742b6dc8772761bfe7edabd74b4 true
```

**Table of contents**

- [Bitcoin `getrawtransaction` command](bitcoin-getrawtransaction-command.md)

## ↑ Ancestors (13)

1. [Bitcoin daemon](bitcoin-daemon.md)
2. [Bitcoin Core executable](bitcoin-core-executable.md)
3. [Bitcoin Core](bitcoin-core.md)
4. [Bitcoin implementation](bitcoin-implementation.md)
5. [Bitcoin](bitcoin.md)
6. [List of cryptocurrencies](list-of-cryptocurrencies.md)
7. [Cryptocurrency](cryptocurrency-split.md)
8. [Blockchain](blockchain.md)
9. [Money](money.md)
10. [Social technology](social-technology-split.md)
11. [Area of technology](area-of-technology.md)
12. [Technology](technology-split.md)
13. [Ciro Santilli's Homepage](split.md)
