# Satoshi uploader

↑ **Parent:** [How to extract data from the Bitcoin blockchain](how-to-extract-data-from-the-bitcoin-blockchain.md)  
🏷️ **Tags:** [P2FMS](pay-to-fake-multisig.md)

See also: [https://bitcoin.stackexchange.com/questions/35959/how-is-the-whitepaper-decoded-from-the-blockchain-tx-with-1000x-m-of-n-multisi/105574#105574](https://bitcoin.stackexchange.com/questions/35959/how-is-the-whitepaper-decoded-from-the-blockchain-tx-with-1000x-m-of-n-multisi/105574#105574)

By "Satoshi uploader" we mean the data upload script present in tx [4b72a223007eab8a951d43edc171befeabc7b5dca4213770c88e09ba5b936e17](https://www.blockchain.com/btc/tx/4b72a223007eab8a951d43edc171befeabc7b5dca4213770c88e09ba5b936e17) of the [Bitcoin blockchain](bitcoin.md).

The uploader, and its accompanying downloader, are [Python](python-programming-language.md) programs stored in the blockchain itself. They are made to upload and download arbitrary data into the blockchain via RPC.

These scripts were notably used for: [illegal content of block 229k](cool-data-embedded-in-the-bitcoin-blockchain/illegal-content-of-block-229k.md). The script did not maintain its popularity much after this initial surge up loads, likely all done by the same user: there are very very few uploads done after block 229k with the Satoshi uploader.

Our choice of name as "Satoshi uploader" is copied from [A Quantitative Analysis of the Impact of Arbitrary Blockchain Content on Bitcoin by Matzutt et al. (2018)](cool-data-embedded-in-the-bitcoin-blockchain/a-quantitative-analysis-of-the-impact-of-arbitrary-blockchain-content-on-bitcoin-by-matzutt-et-al-2018.md) because the scripts are Copyrighted Satoshi Nakamoto on the header comment, although as mentioned at [Hidden surprises in the Bitcoin blockchain by Ken Shirriff (2014)](cool-data-embedded-in-the-bitcoin-blockchain/hidden-surprises-in-the-bitcoin-blockchain-by-ken-shirriff-2014.md) this feels very unlikely to be true.

A more convenient version of those scripts that can download directly from [blockchain.info](blockchain-info.md) without the need for a full local node can be found at: [https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/download_tx_consts.py](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/download_tx_consts.py) by using the `--satoshi` option. E.g. with it you can download the uploader script with:
```
./download_tx_consts.py --satoshi 4b72a223007eab8a951d43edc171befeabc7b5dca4213770c88e09ba5b936e17
mv 4b72a223007eab8a951d43edc171befeabc7b5dca4213770c88e09ba5b936e17.bin uploader.py
```

The scripts can be found in the blockchain at:
- uploader: tx 4b72a223007eab8a951d43edc171befeabc7b5dca4213770c88e09ba5b936e17 block 229991 reproduced at: [https://gist.github.com/cirosantilli/ade4dde7c2f2f5020d792872681763e8](https://gist.github.com/cirosantilli/ade4dde7c2f2f5020d792872681763e8)

  The uploader [creates a standard Pay-to-PubkeyHash transaction](https://gist.github.com/cirosantilli/ade4dde7c2f2f5020d792872681763e8#file-bitcoin-insertion-tool-py-L161) with a single output and data as a fake pubkey hash, and sends change to an address specified on the command line:
  ```
  ./bitcoinInsertionTool.py <data> <change-addr>
  ```
- downloader: tx 6c53cd987119ef797d5adccd76241247988a0a5ef783572a9972e7371c5fb0cc block 229991 reproduced at [https://gist.github.com/cirosantilli/e90bd2e6c3fab25a20898e61e3ab3e90](https://gist.github.com/cirosantilli/e90bd2e6c3fab25a20898e61e3ab3e90)

  The downloader just [strips all operands](https://gist.github.com/shirriff/64f48fa09a61b56ffcf9#file-bitcoin-file-downloader-py-L32), and keeps all data, notably where public key hashes would be normally put.

The uploader script uses its own cumbersome data encoding format, which we call the "Satoshi uploader format". The is as follows:
- ignore all script operands and constants less than 20 bytes (40 hex characters). And there are a lot of small operands, e.g. the uploader itself uses format [https://www.blockchain.com/btc/tx/4b72a223007eab8a951d43edc171befeabc7b5dca4213770c88e09ba5b936e17](https://www.blockchain.com/btc/tx/4b72a223007eab8a951d43edc171befeabc7b5dca4213770c88e09ba5b936e17) has a `OP_1`, data, `OP_3`, `OP_CHECKMULTISIG` pattern on every output script, so the `OP_1` and `OP_3` are ignored. I.e., it is [P2FMS](pay-to-fake-multisig.md).
- ignore the last output, which contains a real change transaction instead of arbitrary data. TODO why not just do what with the length instead?
- the first 4 bytes are the payload length, the next 4 bytes a [CRC-32](crc-32.md) signature. The payload length is in particular useful because of possible granularity of transactions. But it is hard to understand why a CRC-32 is needed in the middle of the largest [hash tree](merkle-tree.md) ever created by human kind!!! It does however have the adavantage that it allows us to more uniquely identify which transactions use the format or not.
This means that if we want to index certain file types encoded in this format, a good heuristic is to skip the first 9 bytes (4 size, 4 CRC, 1 `OP_1`) and look for file signatures.

Let's try out the downloader to download itself. First you have to be running a [Bitcoin Core](bitcoin-core.md) server locally. Then, supposing `.bitcon/bitoin.conf` containing:
```
rpcuser=asdf
rpcpassword=qwer
server=1
txindex=1
```
we run:
```
git clone git://github.com/jgarzik/python-bitcoinrpc.git
git -C python-bitcoinrpc checkout cdf43b41f982b4f811cd4ebfbc787ab2abf5c94a
wget https://gist.githubusercontent.com/shirriff/64f48fa09a61b56ffcf9/raw/ad1d2e041edc0fb7ef23402e64eeb92c045b5ef7/bitcoin-file-downloader.py
pip install python-bitcoinrpc==1.0
BTCRPCURL=http://asdf:qwer@127.0.0.1:8332 \
  PYTHONPATH="$(pwd)/python-bitcoinrpc:$PYTHONPATH" \
  python3 bitcoin-file-downloader.py \
  6c53cd987119ef797d5adccd76241247988a0a5ef783572a9972e7371c5fb0cc
```
worked! The source of the downloader script is visible! Note that we had to wait for the sync of the entire blockchain to be fully finished for some reason for that to work.

Other known uploads in Satoshi format except from the first few:
- tx 89248ecadd51ada613cf8bdf46c174c57842e51de4f99f4bbd8b8b34d3cb7792 block 344068 see [ASCII art](ascii-art.md)
- tx 1ff17021495e4afb27f2f55cc1ef487c48e33bd5a472a4a68c56a84fc38871ec contains the ASCII text `e5a6f30ff7d43f96f61af05efaf96f869aa072b5a071f32a24b03702d1dcd2a6`. This number however is not a known transaction ID in the blockchain, and has no Google hits.

**Table of contents**

- [Peter Todd's data upload scripts](peter-todd-s-data-upload-scripts.md)

## ↑ Ancestors (10)

1. [How to extract data from the Bitcoin blockchain](how-to-extract-data-from-the-bitcoin-blockchain.md)
2. [Bitcoin](bitcoin.md)
3. [List of cryptocurrencies](list-of-cryptocurrencies.md)
4. [Cryptocurrency](cryptocurrency-split.md)
5. [Blockchain](blockchain.md)
6. [Money](money.md)
7. [Social technology](social-technology-split.md)
8. [Area of technology](area-of-technology.md)
9. [Technology](technology-split.md)
10. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (4)

- [Bitcoin whitepaper](bitcoin-whitepaper.md)
- [A Quantitative Analysis of the Impact of Arbitrary Blockchain Content on Bitcoin by Matzutt et al. (2018)](cool-data-embedded-in-the-bitcoin-blockchain/a-quantitative-analysis-of-the-impact-of-arbitrary-blockchain-content-on-bitcoin-by-matzutt-et-al-2018.md)
- [AtomSea & EMBII](cool-data-embedded-in-the-bitcoin-blockchain/atomsea-and-embii.md)
- [Illegal content of block 229k](cool-data-embedded-in-the-bitcoin-blockchain/illegal-content-of-block-229k.md)
