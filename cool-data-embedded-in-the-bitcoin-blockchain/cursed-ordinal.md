# Cursed ordinal

↑ **Parent:** [Technically interesting ordinal](technically-interesting-ordinal.md)

<a id="_920"></a>
These were ordinals that were only indexed in later versions of the script. So to prevent changing the useless indices of existing ordinals, they gave them negative numbers.

<a id="_921"></a>
The word "cursed" is a meme from the 2010/20s, e.g. [https://knowyourmeme.com/memes/cursed-images--2](https://knowyourmeme.com/memes/cursed-images--2).

<a id="_922"></a>
Some examples:<a id="_923"></a>

<a id="_924"></a>
- [https://ordinals.com/inscription/4b9a822a057743813efbefa0dd21d0a01342ee793ce2ce5bd499a5f262187553i0](https://ordinals.com/inscription/4b9a822a057743813efbefa0dd21d0a01342ee793ce2ce5bd499a5f262187553i0) first inscription with no mime type.
<a id="_925"></a>
- [https://ordinals.com/inscription/2fa287270e4203ca2fc9f82ea3de7a0f7b785875791a76387ef6f4ccbb54eee2i0](https://ordinals.com/inscription/2fa287270e4203ca2fc9f82ea3de7a0f7b785875791a76387ef6f4ccbb54eee2i0) is -38:<a id="_926"></a>
  > Hello World, this is a Rust Taproot test

  is bugged because it is missing the mime type, on [Python](../python-programming-language.md):<a id="_927"></a>

  ```
  [b"'a\xf9\x19X%\xa8Q\x87SP\xe5\xf2H\xa6\xeew\x0e\x81\xa5hl\xcd\xaa\x97e\xfeqJ\x16\x12?", OP_CHECKSIG, 0, OP_IF, b'ord', 1, b'text/plain', 0, b'Hello World, this is a Rust Taproot test\xe2\x80\xa6', OP_ENDIF]
  ```

  because the `1` should instead be `b'\x01`.

<a id="_928"></a>
Bibliography:<a id="_929"></a>

<a id="_930"></a>
- [https://decrypt.co/212908/mysterious-ordinals-inscription-teases-cursed-bitcoin-art-project](https://decrypt.co/212908/mysterious-ordinals-inscription-teases-cursed-bitcoin-art-project)

## ↑ Ancestors (15)

1. [Technically interesting ordinal](technically-interesting-ordinal.md)
2. [Ordinal ruleset inscription](ordinal-ruleset-inscription.md)
3. [Images](images.md)
4. [Media type](media-type.md)
5. [Cool data embedded in the Bitcoin blockchain](../cool-data-embedded-in-the-bitcoin-blockchain-split.md)
6. [Bitcoin inscription](../bitcoin-inscription.md)
7. [Bitcoin](../bitcoin.md)
8. [List of cryptocurrencies](../list-of-cryptocurrencies.md)
9. [Cryptocurrency](../cryptocurrency-split.md)
10. [Blockchain](../blockchain.md)
11. [Money](../money.md)
12. [Social technology](../social-technology-split.md)
13. [Area of technology](../area-of-technology.md)
14. [Technology](../technology-split.md)
15. [Ciro Santilli's Homepage](../split.md)
