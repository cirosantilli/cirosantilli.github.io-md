# Genesis block message

↑ **Parent:** [Genesis block](genesis-block.md)  
🏷️ **Tags:** [Coinbase message](coinbase-message.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Genesis_block_message)

[Inscription](inscription-blockchain.md) added by [Satoshi Nakamoto](satoshi-nakamoto.md) on the [Genesis block](genesis-block.md) containing:

> The Times 03/Jan/2009 Chancellor on brink of second bailout for banks 

which is a reference to: [https://www.thetimes.co.uk/article/chancellor-alistair-darling-on-brink-of-second-bailout-for-banks-n9l382mn62h](https://www.thetimes.co.uk/article/chancellor-alistair-darling-on-brink-of-second-bailout-for-banks-n9l382mn62h) wihch is fully titled:

> Chancellor Alistair Darling on brink of second bailout for banks

The "Alistair" was slikely removed due to limited payload concerns.

Through the newspaper reference, the message proves a minimal starting date for the first mine.

And it hints that one of [Bitcoin](bitcoin.md)'s motivation was the [financial crisis of 2007-2008](financial-crisis-of-2007-2008.md), where banks were given bailouts by the government to not go under, which many people opposed as the crisis was their own fault in the first place. A notable related stab is taken at [Len Sassaman tribute](cool-data-embedded-in-the-bitcoin-blockchain/len-sassaman-tribute.md).

We can extract the image from the blockchain ourselves by starting from: [https://blockchain.info/block-height/0?format=json](https://blockchain.info/block-height/0?format=json).

From that page we manually extract the hash `000000000019d6689c085ae165831e934ff763ae46a2a6c172b3f1b60a8ce26f` and then:
```
wget -O 0.hex https://blockchain.info/block/000000000019d6689c085ae165831e934ff763ae46a2a6c172b3f1b60a8ce26f?format=hex
xxd -p -r 0.hex
```
and that does contain the famous genesis block string:
```
EThe Times 03/Jan/2009 Chancellor on brink of second bailout for banks
```
The JSON clarifies that the data is encoded in the `script` field of the transaction `input`:
```
{
      {
         "script":"04ffff001d0104455468652054696d65732030332f4a616e2f32303039204368616e63656c6c6f72206f6e206272696e6b206f66207365636f6e64206261696c6f757420666f722062616e6b73"
```

The extra `E` (0x45 in [ASCII](ascii.md)) in `EThe Times` is just extra noise required by the script, we can break things up as:
```
04ffff001d0104 45 5468652054696d65732030332f4a616e2f32303039204368616e63656c6c6f72206f6e206272696e6b206f66207365636f6e64206261696c6f757420666f722062616e6b73
```
where:
- `54` is `T`
- the `04ffff001d0104` part just doesn't show up on the terminal because it is not made of any printable characters.

The initial `04` is `OP_RETURN`.

TODO what is actual the meaning of the `ffff001d010445` part? `@defango` [https://twitter.com/defango/status/1642750851134652417](https://twitter.com/defango/status/1642750851134652417) comments:

> 04ffff001d0104 is a hexadecimal string. It is commonly used in the Bitcoin network as a part of the mining process. Specifically, it is used as the target value for a block to be considered valid by the Bitcoin network.
> 
> This value represents the level of difficulty required for a miner to generate a block that meets the network's criteria. The first four bytes, 04ffff, represent the maximum possible target value. The next three bytes, 001d01, represent the current difficulty level
> 
> while the final byte, 04, is a padding byte. In summary, this value sets the difficulty level for mining a new block in the Bitcoin network.

TODO the `output` of the transaction has a jumbled script, likely just a regular output to get things going, can't be arbitrary like input.

## ↑ Ancestors (13)

1. [Genesis block](genesis-block.md)
2. [List of bitcoin blocks](list-of-bitcoin-blocks.md)
3. [Bitcoin block](bitcoin-block.md)
4. [Bitcoin protocol](bitcoin-protocol.md)
5. [Bitcoin](bitcoin.md)
6. [List of cryptocurrencies](list-of-cryptocurrencies.md)
7. [Cryptocurrency](cryptocurrency-split.md)
8. [Blockchain](blockchain.md)
9. [Money](money.md)
10. [Social technology](social-technology-split.md)
11. [Area of technology](area-of-technology.md)
12. [Technology](technology-split.md)
13. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (6)

- [Coinbase message](coinbase-message.md)
- [Custom encoded images of unknown source](cool-data-embedded-in-the-bitcoin-blockchain/custom-encoded-images-of-unknown-source.md)
- [Halving messages](cool-data-embedded-in-the-bitcoin-blockchain/halving-messages.md)
- [Len Sassaman tribute](cool-data-embedded-in-the-bitcoin-blockchain/len-sassaman-tribute.md)
- [Text](cool-data-embedded-in-the-bitcoin-blockchain/text.md)
- [How to store data in the Bitcoin blockchain](how-to-store-data-in-the-bitcoin-blockchain.md)
