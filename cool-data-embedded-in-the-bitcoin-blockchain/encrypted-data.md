# Encrypted data

↑ **Parent:** [Media type](media-type.md)  
🏷️ **Tags:** [Encryption](../encryption.md)

<a id="_1224"></a>
Transactions such as [tx fe37c7eee73be5fda91068dbe0eb74a68495a3fc7185712b8417032db7fc9c5e](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/7e95546479508e9fe5158dad6bc8601e2b4e02ee/data/out/0339.txt#L74) ([2015-01-15](https://www.blockchain.com/explorer/transactions/btc/fe37c7eee73be5fda91068dbe0eb74a68495a3fc7185712b8417032db7fc9c5e)) starting with<a id="_1225"></a>

```
U2FsdGVkX1/4iSjLxQ5epo8eRSCOQLGgAsn1CucGii27k8ZyC7Jz6wxhYcevVmxi
6Q4ZFN04WDN0UhKqYardgQf26oeBMURupduDd0ZozxlgMrBkFOCaARqU7RABVWDO
/ruPUcOY0VC8p4lrMNqSdqvN7y6OWwOSH3c0duumZfFNZs9+BbtKCxtaqR5+RkUI
```
are [Base64](../base64.md) encoded. Running them through `base64 -d` leads to starting output bytes `Salted__` which as mentioned at [https://security.stackexchange.com/questions/124312/decrypting-binary-code-from-a-base64-string](https://security.stackexchange.com/questions/124312/decrypting-binary-code-from-a-base64-string) is [OpenSSL](https://ourbigbook.com/go/topic/openssl) encrypted data. So hwerever we see the start:<a id="_1226"></a>

```
U2FsdGVkX1/
```
we might as well give up. That string appears 26 times in our data currently, between [6c091e6152b83ec0df8d0d87c7c5f3da72a3328ed3a5d91768ba0ab899c16b9d](https://www.blockchain.com/explorer/transactions/btc/6c091e6152b83ec0df8d0d87c7c5f3da72a3328ed3a5d91768ba0ab899c16b9d) (2014-09-28) and [84189c82995db355e92e37f8cfe8a9274e9a5d157f1f1658067672e707469a09](https://www.blockchain.com/explorer/transactions/btc/84189c82995db355e92e37f8cfe8a9274e9a5d157f1f1658067672e707469a09) (2019-07-06)

<a id="_1227"></a>
The following via [cryptograffiti.info](cryptograffiti-info.md) get marked by `file` as "openssl enc'd data with salted password, [Base64](../base64.md) encoded":<a id="_1228"></a>

<a id="_1229"></a>
- ad3d8a0a5d57114b1780341cb5104284f029bb01b1b3558f7c7b9ce51eb67e18
<a id="_1230"></a>
- 1cd0c631f444d664601468f644b70e0166019a54d8678de51310139b6c8b2bd7
<a id="_1231"></a>
- ccc3fb2c9cb1c640b76645a8658693066fd63433ab17c318691ad5bd62601c0e
<a id="_1232"></a>
- e6eb0cb8268a9b3d012d2957b32d4b28ccc3317593f54f4bfe4b387326588bd2
<a id="_1233"></a>
- c40e322b198b715accc4a67fad244ed131b8cef0785070e06d10d56c4ab389f2
<a id="_1234"></a>
- 37a261ac6dbf59e3c9673a22028bcdbdd08926a9d32134ab8fba0897f6dcd196
<a id="_1235"></a>
- f1aa516fe00ec2156f16fcb9da422f6cbcd141e8e58c895d8bc37b4ad2fd714e
<a id="_1236"></a>
- 7faf29c7dd7d9cc6d099c262f7ec7edd7fc768276482ad66ceefdd814f1d38ab
<a id="_1237"></a>
- 69cac244051661cc0b8b08905af5ab312a1282b68c932e5d1e3c46ad47ff0f7a
<a id="_1238"></a>
- 1773c39f844951b7169dc34aa0c72aa7b43cae6a103ed1223527ef0f4deec2a9
<a id="_1239"></a>
- b1d4bf3fc46e63c995ad4299f3576340077bc810dfa5c502d1c068460d54bc98
<a id="_1240"></a>
- a52625837741902e1dd24de3dbd3b948d6e0907ad3fc957c13cdf53fa2c3b9ac
<a id="_1241"></a>
- 4ca742813eaccef009e24e92150dda06540c2ac81782f1569b1ebb3179a413d2
<a id="_1242"></a>
- 6c3bab5fc6e6352c62a16ab0f47394845aa41a2c0b25e1a1073a4aeac150e03d
<a id="_1243"></a>
- 20b8feef3d293a0dd79e3c169fceb1217465502a523acbab903a7eb0cd183709
<a id="_1244"></a>
- b7863215b99567bc9e71155b13f3c5f26d15eac52493ee2e834129460ffd2aec
<a id="_1245"></a>
- 2c8961a64bb11d5855790085f51007273467f7ef862137215c9f1d958dcb6c57
<a id="_1246"></a>
- bed542957bdd8f644a4fcd671a8c66a5cc5d6168f9fa60d37177703e77558eee
<a id="_1247"></a>
- 3e45af9d828754d5a38c86636a070610f6e828482718c4a597d272d41a3e31fa
<a id="_1248"></a>
- a13af4817e85cacce3cfb445001e2fb2f56cdc30f78348fd2580bf8f4c84dc55
<a id="_1249"></a>
- 87a10f6bc65a08067b2544e46be00d4af62c0cfed3ae0b165d5eedaff09d81da
<a id="_1250"></a>
- ef55826befabbe9dcd44d87fc385d600dd4c4cba3346cde53d8c591960e9b4dc
<a id="_1251"></a>
- 5d30f63131dcf2b4d001b4ab530e18cc6ff8ffd16cade055ff4587a59b84e420
<a id="_1252"></a>
- 8a75514829b6e30b9fea434eef77b1589ff3f4bdfc0056bd087efbfb8314eb59
<a id="_1253"></a>
- e2be1062c9d43cc6ed43de6f7a40c728d2d92ed0325abde24ff3300cf3ae136a
<a id="_1254"></a>
- 8fe5c2679237e36c74fda04bb083f732c4afdd06af81121b1d7b4d5bd677135f
<a id="_1255"></a>
- 7f099f094d8d51105d8655253d45ebddf1c88b9e138c302a65d2878a237e620c
<a id="_1256"></a>
- 0fc4b3a305e2a7faa2e7d9c2f23d23d626e9e75f1f2a37133f283334b314645b
<a id="_1257"></a>
- 933b321e7b7144ed5e4e1750f944be9ed10293633d9b288bf05febdeb9dc40a3
<a id="_1258"></a>
- 6215486bc024dea7991b142e50e111c4063e1db4a867514612b8e794b8ef5635
<a id="_1259"></a>
- fc0613e11269962d97373b10e310f451fb76c7bb477ba1afb45773c44851e9ed
<a id="_1260"></a>
- ab51d2c037b4625394c68706da83c26bad751018d2a3e377a51988bd8ee18647
<a id="_1261"></a>
- 7ca9b337172f4feff67a0ecbfbd76798265e08c6ebe989a319883c695d756247
<a id="_1262"></a>
- 0f0b477e456dcf286d7262497bcd5b3b6a3ce89f81761c2f59ff702539ab6183
<a id="_1263"></a>
- a320152fd59426c8853dd781db9d682f89755953b39a653f9e9c9628a5fce7fb
<a id="_1264"></a>
- e96221da774fb52d24dda1b83b14c99085eb4befac64691722c56eb750562d68
<a id="_1265"></a>
- a7a5ca68dd340dd42bd5c91e0febe68e5fd2fb993da2992661183eaafe8ad89e
<a id="_1266"></a>
- 64e9d95e2333cfd155506199c8d926649e63a98dbc83c1221b8dd1580937b942

<a id="_1267"></a>
[https://blockchain.news/news/mysterious-bitcoin-inscriptions-a-puzzle-in-raw-binary-data](https://blockchain.news/news/mysterious-bitcoin-inscriptions-a-puzzle-in-raw-binary-data) mentions a huge 9 MB [Ordinal ruleset inscription](ordinal-ruleset-inscription.md) that no-one managed to decode, and so people suspect is encrypted data. Seems to be split across transactions, starting at fed7de7fb75a3fe3c1acbbd8e19a4c540fb368474c8834e4ddb1d5bab764a767

## ↑ Ancestors (12)

1. [Media type](media-type.md)
2. [Cool data embedded in the Bitcoin blockchain](../cool-data-embedded-in-the-bitcoin-blockchain-split.md)
3. [Bitcoin inscription](../bitcoin-inscription.md)
4. [Bitcoin](../bitcoin.md)
5. [List of cryptocurrencies](../list-of-cryptocurrencies.md)
6. [Cryptocurrency](../cryptocurrency-split.md)
7. [Blockchain](../blockchain.md)
8. [Money](../money.md)
9. [Social technology](../social-technology-split.md)
10. [Area of technology](../area-of-technology.md)
11. [Technology](../technology-split.md)
12. [Ciro Santilli's Homepage](../split.md)
