<h1 id="nelson-mandela-jpg-analysis">Nelson-Mandela.jpg analysis</h1>

↑ **Parent:** [Nelson-Mandela.jpg](nelson-mandela-jpg.md)

<a id="_396"></a>
The toplevel transaction is 78f0e6de0ce007f4dd4a09085e649d7e354f70bc7da06d697b167f353f115b8e

<a id="_397"></a>
Like all [AtomSea & EMBII](atomsea-and-embii.md) uploads, the data it is encoded as [P2FKH](../fake-p2pkh-address.md).

<a id="_398"></a>
The full concatenated payload contains the following [ASCII](../ascii.md) characters:

<a id="_399"></a>
```
8881a937a437ff6ce83be3a89d77ea88ee12315f37f7ef0dd3742c30eef92dba|396*8881a937a437ff6ce83be3a89d77ea88ee12315f37f7ef0dd3742c30eef92dba
575061146335bd57f2dc132112152d0eeea44cf187ea6a52ac02435a7e5bea44
674c7cc34ea44bb276c6caf76f2b28fa1597380ab6e6a6906076d8f7229ca5b3
8e2642416ad20924b43f51a633fa1c0a5ba8e4a7b631877db1c64540a42081c9
a3084018096b92af04df57b6116e01ff4b7c7e8bd228235ed49e23f4a2817029
39348722b841afa0c5b67e5af10839afe965ed1b24874e89336bea9fa4ef3091
tomSea & EMBII
```

<a id="_400"></a>
Output 2 is a [change](../change-bitcoin.md), so it contains no data and has been excluded. Change appear to be randomly placed in the list of output of the uploads, but they can be easily removed because they are the only output with a different value.

<a id="_401"></a>
The newlines shown above are explicitly encoded as CR LF newlines with characters 0d 0a.

<a id="_402"></a>
`396` is the number of payload bytes between `396*8881a937a437ff6ce83be3a89d77ea88ee12315f37f7ef0dd3742c30eef92dba` and the last txid `39348722b841afa0c5b67e5af10839afe965ed1b24874e89336bea9fa4ef3091`, including newlines but exclusding the last line.

<a id="_403"></a>
The last line appears to contain arbitrary data to fill out the 20 byte payload granularity:<a id="_404"></a>

<a id="_405"></a>
- `A` is missing from `AtomSea`
<a id="_406"></a>
- there is a NUL character just after EMBII, possibly part of the protocol?

<a id="_407"></a>
Now let's inspect the transactions linked to from toplevel.

<a id="_408"></a>
tx 8881a937a437ff6ce83be3a89d77ea88ee12315f37f7ef0dd3742c30eef92dba contains only payloads without any change. It starts with the following [UTF-8](../utf-8.md) string with CR LF spaces;<a id="_409"></a>

```
"396\“There is nothing like returning to a place
 that remains unchanged to find the ways in
 which you yourself have altered.”
 -Nelson Mandela


Nelson Rolihlahla Mandela was a South African anti-apartheid revolutionary, politician and philanthropist who served as President of South Afrd۽^2c'︨`ica from 1994 to 1999. -Wikipedia

Born: July 18, 1918, Mvezo, South Africa
Died: December 5, 2013
```

<a id="_410"></a>
`396` is once again the number of payload bytes present in that string.

<a id="_411"></a>
This is immediately followed without any separator by a filename, and another size marker:<a id="_412"></a>

```
Nelson-Mandela.jpg?14400/
```
then followed by all the `14400 - len(Nelson-Mandela.jpg?) + len(/)` JPEG bytes bytes, starting with the two [JPEG file signature](../jpeg-file-signature.md) byte "FF D8".

<a id="_413"></a>
Further toplevel transaction payloads are then simply concatenated with the previous ones, until the last bytes of the image "FF D9" appears at the end of the payload.<a id="_414"></a>

```
00000430  d2 81 de 80 0c 52 f1 40  ea 29 68 03 ff d9 6f 6d  |.....R.@.)h...om|
00000440  53 65 61 20 26 20 45 4d  42 49 49 00              |Sea & EMBII.|
```
padded once again by an `AtomSea & EMBII` string fragment terminated by a NUL character.

## ↑ Ancestors (16)

1. [Nelson-Mandela.jpg](nelson-mandela-jpg.md)
2. [Early AtomSea & EMBII uploads](early-atomsea-and-embii-uploads.md)
3. [AtomSea & EMBII](atomsea-and-embii.md)
4. [Images](images.md)
5. [Media type](media-type.md)
6. [Cool data embedded in the Bitcoin blockchain](../cool-data-embedded-in-the-bitcoin-blockchain-split.md)
7. [Bitcoin inscription](../bitcoin-inscription.md)
8. [Bitcoin](../bitcoin.md)
9. [List of cryptocurrencies](../list-of-cryptocurrencies.md)
10. [Cryptocurrency](../cryptocurrency-split.md)
11. [Blockchain](../blockchain.md)
12. [Money](../money.md)
13. [Social technology](../social-technology-split.md)
14. [Area of technology](../area-of-technology.md)
15. [Technology](../technology-split.md)
16. [Ciro Santilli's Homepage](../split.md)
