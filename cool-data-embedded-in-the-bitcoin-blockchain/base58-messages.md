# Base58 messages

↑ **Parent:** [Text](text.md)

<a id="_1045"></a>
Bitcoin addresses are by convention expressed in [Base58](../base58.md), which is a human readable [binary-to-text encoding](../binary-to-text-encoding.md) invented by Bitcoin.

<a id="_1046"></a>
It is a bit like [Base64](../base64.md), but obsessed with eliminating characters that look like one another in popular but stupid fonts like capital "I" and lower case ell "l". As such, any embedded text is rather obfuscated due to this limitations, and people often resort to [leet](https://ourbigbook.com/go/topic/leet)-like replacements such as '1' to represent 'I'.

<a id="_1047"></a>
This seems to be one of the earliest strategies used to encode messages into the [Bitcoin blockchain](../bitcoin.md). The first known example appears in 2011. Then starting November 2011, a large number of messages were inscribed n short successsion, presumably by a single person or small group.

<a id="_1048"></a>
The interest in Base58 encoding might have initially arisen with people's desire to have "[vanity addresses](../vanity-address.md)", that is [Bitcoin addresses](../bitcoin-address.md) that have real words in them, much like [vanity plates](../vanity-plate.md) or [vanity numbers](../vanity-number.md). Such addresses with long words in them are hard to find while keeping the address spendable, because they have to correspond to a [private key](../public-key-cryptography.md). An extreme notable example is:<a id="_1049"></a>


> [1EMBARraSSABLezwXrdWu1dDAVMMdJ7Ci2](https://www.blockchain.com/explorer/addresses/btc/1EMBARraSSABLezwXrdWu1dDAVMMdJ7Ci2)

which contains the awkward 13 letter word:<a id="_1050"></a>


> embarrassable

in it. TODO: proof that it is pendable?

<a id="_1051"></a>
Perhaps inspired by this, some people also decided to use Base58 addresses as a way to create more general unspendable [inscriptions](../inscription-blockchain.md), even even though the method is much more clumsy and complicated than [P2FKHS](../fake-p2pkh-address.md). There is however a certain art to working under limitations.

<a id="image-total-burn-addresses-as-a-function-of-time-found-by-bitcoin-burn-addresses-unveiling-the-permanent-losses-and-their-underlying-causes"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/Total_burn_address_vs_time_by_Khatib_Legout.png" alt="" height="600">

**[Figure 91](#image-total-burn-addresses-as-a-function-of-time-found-by-bitcoin-burn-addresses-unveiling-the-permanent-losses-and-their-underlying-causes). Total burn addresses as a function of time found by Bitcoin Burn Addresses: Unveiling the Permanent Losses and Their Underlying Causes**. Although it is not solely focused on inscriptions and may also contain functional burn addresses, it is likely that the methods of Khatib/Legout capture the overall trend of base58 inscription counts.

<a id="_1052"></a>
These messages were originally found with: [https://github.com/cirosantilli/bitcoin-inscription-indexer#payload-size-out-utxo-2vals](https://github.com/cirosantilli/bitcoin-inscription-indexer#payload-size-out-utxo-2vals) which tracks the largest transactions with unspent outputs.  
[Bitcoin Burn Addresses: Unveiling the Permanent Losses and Their Underlying Causes](bitcoin-burn-addresses-unveiling-the-permanent-losses-and-their-underlying-causes.md) later revealed many new ones.

<a id="_1053"></a>
Finding Base58 messages is intrinsically hard for a few reasons<a id="_1054"></a>

<a id="_1055"></a>
- the words may be garbled by Base58 leet
<a id="_1056"></a>
- only very small ammounts of data can be encoded at a time, and all of it contains ASCII, so you can't just "find all long ASCII strings" as we started doing for other ASCII inscriptions a la [`strings -n20`](../strings-binutils.md); you have to use some dictionary as a basis
<a id="_1057"></a>
- the Base58 does not show up raw on the blockchain, as it is just a human representation for the actual binary data that does, so you can't just [strings](../strings-binutils.md) the blockchain, you have to parse it

<a id="_1058"></a>
The interesting following transactions contain base58 encoded messages on addresses, sorted chronologically, and heighlighted either due to their earliness or historical or artistic quality:

<a id="_1059"></a>
<a id="_1060"></a>
- on two transactions of block 124726 (2011-05-18) someone created two addresses whose base58 differs only by one character, `W` in one is replaced by `x` in he other:<a id="_1061"></a>

  <a id="_1062"></a>
  - [1ByteCoinAddressesMatch1kpCWNXmHKW](https://www.blockchain.com/explorer/addresses/btc/1ByteCoinAddressesMatch1kpCWNXmHKW) in [tx c8348659071d4c56cccc5f33379586d71dd97e3468316558fe3c51b808acc8fd](https://www.blockchain.com/explorer/transactions/btc/c8348659071d4c56cccc5f33379586d71dd97e3468316558fe3c51b808acc8fd)
  <a id="_1063"></a>
  - [1ByteCoinAddressesMatch1kpCxNXmHKW](https://www.blockchain.com/explorer/addresses/btc/1ByteCoinAddressesMatch1kpCxNXmHKW) in [5fa33898655cb949e26712316840b941158c334634d3b80b82e29ce08dd7ebca](https://www.blockchain.com/explorer/transactions/btc/5fa33898655cb949e26712316840b941158c334634d3b80b82e29ce08dd7ebca)

  [https://bitcointalk.org/index.php?topic=20955.msg264038#msg264038](https://bitcointalk.org/index.php?topic=20955.msg264038#msg264038) How is this address possible? (2011-06-22) user [ByteCoin](https://bitcointalk.org/index.php?action=profile;u=490) suggests that this was done to highlight the fact that the checksum at the end of base58 addresses against 1 character changes. They also highlight another pair where addresses are equal except for two adjacent swapped characters: `18` -\> `81`<a id="_1064"></a>

  ```
  1ByteCoinAddressesMatchcNN781jjwLY
  1ByteCoinAddressesMatchcNN718jjwLY
  ```

  but these are not present in the blockchain itself.
<a id="_1065"></a>
- Around July 2011 there seems to have been a surge of interest in [vanity addresses](../vanity-address.md), and it appears that someone was "squatting" long lists of interesting addresses that they managed to generate for later sale. These addresses are present in the hundreds in a few transactions chains, and they do not seem to contain any coherent messages across the outputs. Most encode [given names](../given-name.md), which would be the easiest type of address to sell. This theory is proposed e.g. at: [https://bitcointalk.org/index.php?topic=84569.msg992950#msg992950](https://bitcointalk.org/index.php?topic=84569.msg992950#msg992950) and it seems as the most plausible one to us. An example of this is [tx acdd81bab63ee42e28296dd5c21e8a29392e409026fc206acf5931b12a31141d](https://www.blockchain.com/explorer/transactions/btc/acdd81bab63ee42e28296dd5c21e8a29392e409026fc206acf5931b12a31141d) block 136273 (2011-07-14) which starts off with:<a id="_1066"></a>

  ```
  1MeNDez2hmZoehh5JAtS2ZJQfAFZFfSQSi
  1ALonzoPwyf8CNVQnVNXNBjacPXaUdZGgm
  1MattieiicNRfse5jTVU2X8pX6Cyr7BZVR
  1TraciFRboW661p1LfRaULwwefeo8KtQa
  ```

  For the purposes of this museum, this is a noteworty event, but it has little artistic value for large ammounts of bulk, and therefore also serves as noise that must be removed if we want to find other more personal and varied inscriptions. We will keep a list of such transactions at: [Section "Bitcoin 2011 vanity address pool"](../bitcoin-2011-vanity-address-pool.md).
<a id="_1067"></a>
- [`1MartinHaferkorncii112o11HdkMrtttD`](https://www.blockchain.com/explorer/addresses/btc/1MartinHaferkorncii112o11HdkMrtttD) on [tx dab55eefd5cef495719a43bbd190c57c8ca60ecc45d630edf3442b2096965a97](https://www.blockchain.com/explorer/transactions/btc/dab55eefd5cef495719a43bbd190c57c8ca60ecc45d630edf3442b2096965a97) block 152851 (2011-11-11) encodes the name:<a id="_1068"></a>
  > Martin Haferkorn

  Likely:<a id="_1069"></a>

  <a id="_1070"></a>
  - [https://www.efinance.wiwi.uni-frankfurt.de/en/team/alumni/dr-martin-haferkorn.html](https://www.efinance.wiwi.uni-frankfurt.de/en/team/alumni/dr-martin-haferkorn.html)
  <a id="_1071"></a>
  - [https://scholar.google.com/citations?hl=de&user=BNLeMMAAAAAJ&view_op=list_works&sortby=pubdate](https://scholar.google.com/citations?hl=de&user=BNLeMMAAAAAJ&view_op=list_works&sortby=pubdate)
<a id="_1072"></a>
- <a id="_1073"></a>
  [`1EricLombrozoXXXXXXXXXXXXXXXWACBVB`](https://www.blockchain.com/explorer/addresses/btc/1EricLombrozoXXXXXXXXXXXXXXXWACBVB) appears on 3 separate transactions on 2011-11-24:<a id="_1074"></a>

  <a id="_1075"></a>
  - block 154630:<a id="_1076"></a>

    <a id="_1077"></a>
    - [tx 65a3a76d26b9ba82d1419368311727d46452341bd62c3de543eb79a7b918642b](https://www.blockchain.com/explorer/transactions/btc/65a3a76d26b9ba82d1419368311727d46452341bd62c3de543eb79a7b918642b)
    <a id="_1078"></a>
    - [tx 87b34e465fb96d7c73345e1a3b14e4326905e850fa5ab569bf2b3f4ec650214c](https://www.blockchain.com/explorer/transactions/btc/87b34e465fb96d7c73345e1a3b14e4326905e850fa5ab569bf2b3f4ec650214c) burns 0.005 BTC
  <a id="_1079"></a>
  - block 154637: [tx dea183908e40e0cebfee6a0d8362b299e07cf193fbc02ffd3308b43781eca208](https://www.blockchain.com/explorer/transactions/btc/dea183908e40e0cebfee6a0d8362b299e07cf193fbc02ffd3308b43781eca208). This one is more interesting and also contains a second output, both at 0.005 BTC<a id="_1080"></a>
    > 1969SandraSandicXXXXXXXXXXXXXvdEiU

    so possibly a wedding token of Eric with Sandra Sandic after two previous test transactions. This also possibly gives Sandra's birth year of 1969. Pinged him at: [https://x.com/cirosantilli/status/1904212575211901129](https://x.com/cirosantilli/status/1904212575211901129).
  Alsmost certainly this guy:<a id="_1081"></a>

  <a id="_1082"></a>
  - [https://www.linkedin.com/in/ericlombrozo/](https://www.linkedin.com/in/ericlombrozo/)
  <a id="_1083"></a>
  - [https://x.com/eric_lombrozo](https://x.com/eric_lombrozo)
  [https://www.officialusa.com/names/Sandra-Sandic/](https://www.officialusa.com/names/Sandra-Sandic/) suggests a link between Eric and Sandra sharing phone number (858) 461-1843 and residing at 12631 El Camino Real, San Diego, CA. Eric's LinkedIn marks him as living in San Diego, and Sandra's birthday is marked 1969-01-05, so matching the inscription year. The address shows as a regular appartment block on [Google Maps](../google-maps.md), so maybe they are not crazy rich, or they have restraint. [https://besthistorysites.net/name/eric-lombrozo](https://besthistorysites.net/name/eric-lombrozo) reconfirms the address.

  <a id="_1084"></a>
  In 2023 [this Sandra Sandic on Facebook](https://www.facebook.com/sandra.sandic.3) liked [this post related](https://www.facebook.com/story.php/?story_fbid=563741739148161&id=100065370197668&_rdr) to a show in San Diego, giving a possible profile. At [this post](https://www.facebook.com/sandra.sandic.3/posts/pfbid0s92xQqhSRGWyRNU4PKfWZQQ8LVmxofvet7sGHnQ8REfxLJPvSFKKSuKwSnwt1fQsl) she links to [this story](https://www.cnbc.com/2017/06/20/bitcoin-millionaire-erik-finman-says-going-to-college-isnt-worth-it.html) about [Erik Finman](../erik-finman.md), young [Bitcoin](../bitcoin.md) millionaire, thus establishing an interest link between that profile and Bitcoin. She also has various posts in Bosnian, so she speaks the language and is likely a [first generation immigrant](../first-generation-immigrant.md).

  <a id="image-eric-lombrozo"></a>
  ![](https://web.archive.org/web/20250323225851im_/https://cryptotutor.in/images/crypto-celebrity/eric.jpg)

  **[Figure 92](#image-eric-lombrozo). Eric Lombrozo**. [Source](https://cryptotutor.in/crypto-celebrity/eric-lombrozo). Off-chain image. He's just a cool nerd like us.
<a id="_1085"></a>
- <a id="_1086"></a>
  [`1BitTaLkTVChristmasSpeciaLXXRix9Ea`](https://www.blockchain.com/explorer/addresses/btc/1BitTaLkTVChristmasSpeciaLXXRix9Ea) is repeated a dozen times on transactions between [tx 8e2bacf9971ce1a29d69d1a0484bfaa198257cc116530c7415ab6c38ae54ebc3](https://www.blockchain.com/explorer/transactions/btc/8e2bacf9971ce1a29d69d1a0484bfaa198257cc116530c7415ab6c38ae54ebc3) block 154721 (2011-11-25) and 2011-11-27.

  <a id="_1087"></a>
  It is a quick ad for the [BitTalk.tv Christmas Special](https://web.archive.org/web/20120219155246/http://bittalk.tv/?p=114) by Matthew N. Wright. [https://bitcointalk.org/index.php?topic=3025298.0](https://bitcointalk.org/index.php?topic=3025298.0) mentions he is the founder bittalk.tv and co-founder of [Bitcoin Magazine](https://ourbigbook.com/go/topic/bitcoin-magazine). TODO is the video still watchable somewhere? Also announced at: [https://bitcointalk.org/index.php?topic=52712](https://bitcointalk.org/index.php?topic=52712). As of 2025, the domain had been reappropriated as a [SolarMovie](https://ourbigbook.com/go/topic/solarmovie) mirror. It is quite likely that all the large set of message that follow were inscribed by him. Related:<a id="_1088"></a>

  <a id="_1089"></a>
  - [https://www.reddit.com/r/Bitcoin/comments/ruo73/matthew_n_wright_scammer_of_bitcoinmagazine_and/](https://www.reddit.com/r/Bitcoin/comments/ruo73/matthew_n_wright_scammer_of_bitcoinmagazine_and/) Matthew N. Wright, scammer of BitcoinMagazine and BBBB (2012)
  <a id="_1090"></a>
  - [https://www.reddit.com/r/Bitcoin/comments/znhsj/matthew_n_wright_apologizes/](https://www.reddit.com/r/Bitcoin/comments/znhsj/matthew_n_wright_apologizes/) Matthew N. Wright "apologizes" (2012)

  <a id="_1091"></a>
  Later on there is also another variant addresses [`11Bitta1ktvchristmasspecia1WNDvAa`](https://www.blockchain.com/explorer/addresses/BTC/11Bitta1ktvchristmasspecia1WNDvAa) on repeated almost 300 times on [tx ace9524519577138ca98ec01651758fd1e5ec33ce0110c6681eccba0e716cc7a](https://www.blockchain.com/btc/tx/ace9524519577138ca98ec01651758fd1e5ec33ce0110c6681eccba0e716cc7a) block 155545 (2011-12-01)

  <a id="_1092"></a>
  Other likely mentions of Matthew N Wright:<a id="_1093"></a>

  <a id="_1094"></a>
  - [`11MatthewLovesmandaXXXXXXXXabCJPY`](https://www.blockchain.com/explorer/addresses/btc/11MatthewLovesmandaXXXXXXXXabCJPY) on [tx d7c57205d69420dc7f4593b4de0806c9ec96f4755b64315cd034bd4b0b90dc2a](https://www.blockchain.com/explorer/transactions/btc/d7c57205d69420dc7f4593b4de0806c9ec96f4755b64315cd034bd4b0b90dc2a) block 155698 (2011-12-01) has a quick love declaration:<a id="_1095"></a>
    > Matthew loves Amanda
  <a id="_1096"></a>
  - [`1MatthewNWrightisaScammer124DNsfX`](https://www.blockchain.com/explorer/addresses/btc/1MatthewNWrightisaScammer124DNsfX) is etched twice
<a id="_1097"></a>
- [tx 28ccf29cfcc9f82d42793db770e7c7894d61ccf3d18299f34bda2e54415da287](https://www.blockchain.com/explorer/transactions/btc/28ccf29cfcc9f82d42793db770e7c7894d61ccf3d18299f34bda2e54415da287) block 154769 (2011-11-25) contains a short excerpt from [Alice in Wonderland](https://ourbigbook.com/go/topic/alice-in-wonderland)<a id="_1098"></a>

  ```
  1But1DontWantToGoAmongMadxxxzDmyW6
  1Peop1eA1iceRemarkedxxxxxxxxxuLyKu
  12ohYouCantHe1pThatxxxxxxxxxzCjyMs
  19SaidTheCatWereA11MadHerexxyTvEir
  191mMadYoureMadxxxxxxxxxxxxxvwA4Up
  1HowDoYouKnow1mMadSaidA1icexxZA4Nr
  12YouMustBeSaidTheCatxxxxxxxz2tFa2
  12orYouWou1dntHaveComeHerexxvtHbqq
  ```

  Original text referred to:<a id="_1099"></a>
  > But I don't want to go among mad people," Alice remarked. "Oh, you can't help that," said the Cat: "we're all mad here. I'm mad. You're mad." "How do you know I'm mad?" said Alice. "You must be," said the Cat, "or you wouldn’t have come here."
<a id="_1100"></a>
- [tx 3bbd94d22346a3bfb44257293e10c3b5c9ee39230c1cd358bdce2bf03c61ba0b](https://www.blockchain.com/explorer/transactions/btc/3bbd94d22346a3bfb44257293e10c3b5c9ee39230c1cd358bdce2bf03c61ba0b) (block 154965 , 2011-11-27) contains 49 base58 messages on a single transaction transcribing [this version](https://fiefgoldenlake.proboards.com/thread/30870/passages?page=3) of the [Emerald Tablet](https://ourbigbook.com/go/topic/emerald-tablet), a type of mystical medieval text:<a id="_1101"></a>

  ```
  12TisTrueWithoutALie22222221wT3qjn
  1CertainAndMostTrue2222222225YPnJF
  12ThatWhich1sBe1ow1sAs222221y3G7mv
  12ThatWhich1sAboveAnd2222221vxkcEq
  ...
  1AboutTheWorkingsofTheSun1zzyWJtfm
  ```

  Some of the messages weirdly have "xoxo" inserted into them, not sure why, e.g.<a id="_1102"></a>

  ```
  12TheFatherofTheWho1eWor1d2249xs5g
  191sHereXoXoXoXoXoXoXoXoXoXo72uqJv
  191tsPower1sWho1e1f1tHasXoXoWhYr3M
  1BeenTurned1ntoEarth222222221soWAL
  ```

  The full decoded text is:<a id="_1103"></a>
  > It is true, without error, certain and most true,  
  > That which is below is as that which is above, and that which is above is as that which is below, to perform the miracles of the one thing.  
  > And as all things were from the one, by means of the meditation of the one, thus all things were born from the one, by means of adaptation.  
  > Its father is the Sun, its mother is the Moon, the Wind carried it in its belly, its nurse is the earth.  
  > The father of the whole world is here.  
  > Its power is whole if it has been turned into earth.  
  > You will separate the earth from the fire, the subtle from the dense, sweetly, with great skill.  
  > It ascends from earth into heaven and again it descends to the earth, and receives the power of higher and of lower things.  
  > Thus you will have the Glory of the whole world.  
  > Therefore will all obscurity flee from you.  
  > Of all strength this is true strength, because it will conquer all that is subtle, and penetrate all that is solid.  
  > Thus was the world created.  
  > From this were wonderful adaptations, of which this is the means. Therefore am I named Thrice-Great Hermes, having the three parts of the philosophy of the whole world.  
  > It is finished, what I have said about the working of the Sun.
<a id="_1104"></a>
- <a id="_1105"></a>
  [`11111111LeonhardEu1er111126nxjP`](https://www.blockchain.com/explorer/addresses/btc/11111111LeonhardEu1er111126nxjP) on [tx 80ddf2e7e04922e2cbf6e744dbf47aec02d781505d8b2c4ee5f725b8882ddb2d](https://www.blockchain.com/explorer/transactions/btc/80ddf2e7e04922e2cbf6e744dbf47aec02d781505d8b2c4ee5f725b8882ddb2d) block 155051 (2011-11-28) is a tribute to Swiss mathematician [Leonhard Euler](https://ourbigbook.com/go/topic/leonhard-euler)

  <a id="image-swiss-mathematician-leonard-euler"></a>
  ![](https://upload.wikimedia.org/wikipedia/commons/thumb/f/f9/Leonhard_Euler_-_Jakob_Emanuel_Handmann_%28Kunstmuseum_Basel%29.jpg/500px-Leonhard_Euler_-_Jakob_Emanuel_Handmann_%28Kunstmuseum_Basel%29.jpg)

  **[Figure 93](#image-swiss-mathematician-leonard-euler). Swiss mathematician Leonard Euler**. [Source](https://commons.wikimedia.org/wiki/File:Leonhard_Euler_-_Jakob_Emanuel_Handmann_%28Kunstmuseum_Basel%29.jpg). Off-chain image.
<a id="_1106"></a>
- [024b093afb54f69426c5624f09a5f2d3791ce20513225cbb42d333ad72f8576e](https://www.blockchain.com/explorer/transactions/btc/024b093afb54f69426c5624f09a5f2d3791ce20513225cbb42d333ad72f8576e) block 155256 (2011-11-29) has two self-explanatory outputs:<a id="_1107"></a>
  > Just A Two Line  
  > Test

  <a id="_1108"></a>
  ```
  112JustATwoLine222222222221vcJxpZ
  11111Test111112222222222222LiApa
  ```
<a id="_1109"></a>
- [tx 8f64d2b7a762767e3870c4aee95f8c7b5439cf02cf7d7e5d99b6e39967ecada8](https://www.blockchain.com/explorer/transactions/btc/8f64d2b7a762767e3870c4aee95f8c7b5439cf02cf7d7e5d99b6e39967ecada8) block 155256 (2011-11-29) encodes the poem "Shall I compare thee to a summer's day?" by [Shakespeare](https://ourbigbook.com/go/topic/shakespeare) 22 addresses starting with:<a id="_1110"></a>

  ```
  11Sha111CompareTheeToAXXXXXVnRohE
  11SummersDayThouArtMoreXXXXUcpgnX
  11Love1yAndMoreTemperateXXXUu485j
  ...
  ```

  Full original text:<a id="_1111"></a>
  > Shall I compare thee to a summer's day?  
  > Thou art more lovely and more temperate.  
  > Rough winds do shake the darling buds of May,  
  > And summer's lease hath all too short a date.  
  > Sometime too hot the eye of heaven shines,  
  > And often is his gold complexion dimmed;  
  > And every fair from fair sometime declines,  
  > By chance, or nature's changing course, untrimmed;  
  > But thy eternal summer shall not fade,  
  > Nor lose possession of that fair thou ow'st,  
  > Nor shall death brag thou wand'rest in his shade,  
  > When in eternal lines to Time thou grow'st.  
  > So long as men can breathe, or eyes can see,  
  > So long lives this, and this gives life to thee.

  More Shakespeare follows at [tx 0ae2eaaa9cddafba89b4c92d074f4e5254cbf7691cbe7f64660bf549c7071147](https://www.blockchain.com/explorer/transactions/btc/0ae2eaaa9cddafba89b4c92d074f4e5254cbf7691cbe7f64660bf549c7071147) block 155383 (2011-11-20) has a passage from [Romeo and Juliet](https://ourbigbook.com/go/topic/romeo-and-juliet) starting with:<a id="_1112"></a>

  ```
  11TisButThyNameThat1sMyXXXXWabTZh
  11EnemyThouArtThyse1fThoughXNRG4J
  11NotAMontagueWhatsMontagueYEJDfM
  111t1sNorHandNorFootNorArmXVNeFEV
  ```

  Full original text:<a id="_1113"></a>
  > 'Tis but thy name that is my enemy;  
  > Thou art thyself, though not a Montague.  
  > What's Montague? It is nor hand, nor foot,  
  > Nor arm, nor face, nor any other part  
  > Belonging to a man. O, be some other name!  
  > What's in a name? That which we call a rose,  
  > By any other word would smell as sweet.  
  > So Romeo would - were he not Romeo called -  
  > Retain that dear perfection which he owes  
  > Without that title. Romeo, doff thy name,  
  > And for that name, which is no part of thee,  
  > Take all myself.
<a id="_1114"></a>
- Various other notable texts follow on 2011-12-01:<a id="_1115"></a>

  <a id="_1116"></a>
  - [tx 1f9606f267cc398356663b14d1a7a3591e3da06572893394c14975a6fc11798f](https://www.blockchain.com/explorer/transactions/btc/1f9606f267cc398356663b14d1a7a3591e3da06572893394c14975a6fc11798f) block 155467 (2011-12-01) contains an excerpt from Newton's [Principia](../philosophiae-naturalis-principia-mathematica.md) starting with:<a id="_1117"></a>

    ```
    11Ru1e1WeAreToAdmitNoMoreXXazQ96z
    11CausesofNatura1ThingsThanZAQ9ig
    11SuchAsAreBothTrueAndXXXXXZyzfQp
    11SufficientToExp1ainTheirXVSC2gY
    ```

    Full original text[https://history.hanover.edu/courses/excerpts/212newt.html](https://history.hanover.edu/courses/excerpts/212newt.html):<a id="_1118"></a>
    > <a id="_1119"></a>
    > RULE 1 We are to admit no more causes of natural things, than such as are both true and sufficient to explain their appearances.
    > 
    > <a id="_1120"></a>
    > RULE II Therefore to the same natural effects we must, as far as possible, assign the same causes.
    > 
    > <a id="_1121"></a>
    > RULE III The qualities of bodies, which admit neither intension nor remission of degrees, and which are found to belong to all bodies within reach of our experiments, are to be esteemed the universal qualities of all bodies whatsoever.
    > 
    > <a id="_1122"></a>
    > RULE IV In experimental philosophy we are to look upon propositions collected by general induction from phenomena as accurately or very nearly true, notwithstanding any contrary hypotheses that may be imagined, till such time as other phenomena occur, by which they may either be made more accurate, or liable to exceptions.
  <a id="_1123"></a>
  - [tx 89010c791c9d7ed24affa1d638b12179d2ca7ec91704fe906834386f43a8101d](https://www.blockchain.com/explorer/transactions/btc/89010c791c9d7ed24affa1d638b12179d2ca7ec91704fe906834386f43a8101d) starting at `11When1nTheCourseofHumanXXXXdfMdQ`: [Declaration of Independence](https://ourbigbook.com/go/topic/declaration-of-independence)
  <a id="_1124"></a>
  - [tx f7ca83a8a2e1c78efdfde0791d99a567ddaa60805c3b5b857bc7ec14ec2c8204](https://www.blockchain.com/explorer/transactions/btc/f7ca83a8a2e1c78efdfde0791d99a567ddaa60805c3b5b857bc7ec14ec2c8204) starting at `11AVa1id1dentifier1sAXXXXXXcrnyki`: likely contains an excerpt of the C or C++ standard. Possible source: [https://en.wikipedia.org/wiki/C_data_types](https://en.wikipedia.org/wiki/C_data_types).
  <a id="_1125"></a>
  - [tx 028b8514a4f6cc96ac3c1c83dbb117ab9dc5eb09deab7b49bf038fd460173127](https://www.blockchain.com/explorer/transactions/btc/028b8514a4f6cc96ac3c1c83dbb117ab9dc5eb09deab7b49bf038fd460173127) starting at `11TheSetupTheJokeA1waysXXXXTF9Wzp`: [The aristocrats by HP Lovecraft](https://www.reddit.com/r/Lovecraft/comments/zxtkd/hp_lovecrafts_the_aristocrats/), which talks about the [The Aristocrats](https://ourbigbook.com/go/topic/the-aristocrats) joke pattern
  <a id="_1126"></a>
  - [tx bd513d9ee605ead1a299c9dfb77de1127bf651c54d99820e9be8b40cef8c8dfe](https://www.blockchain.com/explorer/transactions/btc/bd513d9ee605ead1a299c9dfb77de1127bf651c54d99820e9be8b40cef8c8dfe) starting at `11Si1ex1sAnAcronymForXXXXXXcujTa5` talks briefly about SILEX ([separation of isotopes by laser excitation](https://ourbigbook.com/go/topic/separation-of-isotopes-by-laser-excitation))
  <a id="_1127"></a>
  - [tx ef374dcc5b23f16ecb0b1b639ba577d2acda7ad32321b5866db2fa9e6807b9c5](https://www.blockchain.com/btc/tx/ef374dcc5b23f16ecb0b1b639ba577d2acda7ad32321b5866db2fa9e6807b9c5) block 155494 (2011-12-01) contains the intruction from the bitcoin.org website: [https://web.archive.org/web/20210129054851/https://bitcoin.org/en/](https://web.archive.org/web/20210129054851/https://bitcoin.org/en/)<a id="_1128"></a>

    ```
    11Bitcoin1sADecentra1izedXXWPM6Hs
    11PeertopeerNetworkoverXXXXUkyy3M
    11WhichUsersMakeXXXXXXXXXXXX4tQgN
    11TransactionsThatAreXXXXXXVdZfnJ
    ```
  <a id="_1129"></a>
  - [tx 05ee60dfb92795c79e46e106f52bbdbc1006eba0837ed9e4ad99d9b214eb5fcf](https://www.blockchain.com/explorer/transactions/btc/05ee60dfb92795c79e46e106f52bbdbc1006eba0837ed9e4ad99d9b214eb5fcf) block 155538 contains a tribute to Archimedes:<a id="_1130"></a>

    ```
    11ArchimedesWasANativeofXXXXJsj6W
    11SyracuseSici1y1t1sXXXXXXXaYF4CE
    11ReportedBySomeAuthorsThatXjFBcV
    11HeVisitedEgyptAndThereXXXYVzj58
    ```

    original text at: [https://mathshistory.st-andrews.ac.uk/Biographies/Archimedes/](https://mathshistory.st-andrews.ac.uk/Biographies/Archimedes/)<a id="_1131"></a>
    > Archimedes was a native of Syracuse, Sicily. It is reported by some authors that he visited Egypt and there invented a device now known as Archimedes' screw. This is a pump, still used in many parts of the world. It is highly likely that, when he was a young man, Archimedes studied with the successors of Euclid in Alexandria. Certainly he was completely familiar with the mathematics developed there, but what makes this conjecture much more certain, he knew personally the mathematicians working there and he sent his results to Alexandria with personal messages. He regarded Conon of Samos, one of the mathematicians at Alexandria, both very highly for his abilities as a mathematician and he also regarded him as a close friend.

    <a id="image-archimedes"></a>
    ![](https://upload.wikimedia.org/wikipedia/commons/thumb/e/e7/Domenico-Fetti_Archimedes_1620.jpg/500px-Domenico-Fetti_Archimedes_1620.jpg)

    **[Figure 94](#image-archimedes). Archimedes**. [Source](https://commons.wikimedia.org/wiki/File:Domenico-Fetti_Archimedes_1620.jpg). Off-chain image.
  <a id="_1132"></a>
  - [tx 237b50dac42af130171773b233954e62690182fd4901a453ad5d11d1d54a8ca3](https://www.blockchain.com/btc/tx/237b50dac42af130171773b233954e62690182fd4901a453ad5d11d1d54a8ca3) block 155545 (2012-01-01) contains an exceprt from [https://en.wikipedia.org/wiki/The_Glass_Menagerie](https://en.wikipedia.org/wiki/The_Glass_Menagerie)<a id="_1133"></a>

    ```
    11TomAppearsAtTheTopofTheXXWyM2Bt
    11A11eyAfterEachSo1emnBoomXaBp7oy
    11ofTheBe111nTheTowerHeXXXXVQaies
    11ShakesALitt1eNoisemakeroraeWTgK
    ...
    ```
  <a id="_1134"></a>
  - [tx 57bfd63000bbfa6e9a61f7285a4abf9aef91dfcfba4fe0f940b431653eb8068b](https://www.blockchain.com/btc/tx/57bfd63000bbfa6e9a61f7285a4abf9aef91dfcfba4fe0f940b431653eb8068b) block 155494 (2011-12-01) is a [Lorem ipsum](../lorem-ipsum.md) and [tx 7961b5ae2f053a16d5c589104f87edfabe80fcae185832ea185e7f0cf06c7747](https://www.blockchain.com/explorer/transactions/btc/7961b5ae2f053a16d5c589104f87edfabe80fcae185832ea185e7f0cf06c7747) (2011-12-05) is another one:<a id="_1135"></a>

    ```
    11Lorem1psumDo1orSitAmetXXXWAEZ6C
    11ConsecteturAdipiscingE1itYQHEPM
    ...
    ```
<a id="_1136"></a>
- [tx 8ffacbb18f63576fe323cbf2acc6c4c01c86aadf13d8352cfdd39d91916d98c8](https://www.blockchain.com/btc/tx/8ffacbb18f63576fe323cbf2acc6c4c01c86aadf13d8352cfdd39d91916d98c8) block 156164 (2011-12-05) advertises [etchablock.com](etchablock-com.md) by repeating the following 3 messages 80 times:<a id="_1137"></a>

  ```
  11EtchABLockDotComGivesYouXZHcYVz
  11BLockChain1mmortaLityXXXXYRZD5m
  11VisitEtchABLockDotComNowXTbeZZ9
  ```

  decoding to:<a id="_1138"></a>
  > etchablock.com gives you blockchain immortaility. Visit etchablock.com now.

  More ads can be seen at:<a id="_1139"></a>

  <a id="_1140"></a>
  - [tx 14bac1f94636c24ada613b1ccc5fe4fca35657683baac6cc861f0eb88fd33fbc](https://www.blockchain.com/btc/tx/14bac1f94636c24ada613b1ccc5fe4fca35657683baac6cc861f0eb88fd33fbc)
  <a id="_1141"></a>
  - [tx bfb41cbb857a8189bfacecfc3cd544ee9d14af4414ea95a7b4f86507eace8183](https://www.blockchain.com/btc/tx/bfb41cbb857a8189bfacecfc3cd544ee9d14af4414ea95a7b4f86507eace8183)
<a id="_1142"></a>
- [tx 12a8866ea85a8a6838d77cc67ce74ef190a074bc822572f4a82daad00fd980d6](https://www.blockchain.com/explorer/transactions/btc/12a8866ea85a8a6838d77cc67ce74ef190a074bc822572f4a82daad00fd980d6) block 156119 (2011-12-05) seems like an alphabet test:<a id="_1143"></a>

  ```
  111111111a11111111111b11dC8yHQ
  111111111c1111111111111dWctEU9
  111111111111e1111111111W7v25m
  111111f1111111111111111g11WfG2p8
  1111111111111h111111111WdQPXP
  11111i111111111111j1111111bL5SyF
  11111111k111111111111111XV7PT9D
  111L1111111111111111111m111YmYGPJ
  1111111111111111n11111U4Rs6D
  1111111111111o111111111cLV3wA
  11111111p11111111111111qW1RK1A
  1111111111111111r1111VRWJZs
  111111111111s1111111111VUeyXS
  11111111111t11111111111Vq1Wm3
  11111111u111111111111111bVpCYE
  111111111v11111111111111XoV17A
  11111111w1111111111111111YyEFv6
  111111111x11111111111111XvZPGp
  11111111111y11111111111Y1hDo5
  111111111111111zXXXXXXVSn6d5
  ```
<a id="_1144"></a>
- [tx 31331de21d321766fcac556d7233ad0e3918bc78c7af22b99373569c07d4f30c](https://www.blockchain.com/explorer/transactions/btc/31331de21d321766fcac556d7233ad0e3918bc78c7af22b99373569c07d4f30c) block 158772 (2011-12-23) has a quick love declaration by a Chinese dude to his Chinese dudess<a id="_1145"></a>

  ```
  11YechunnanLoveChenchenYeziSsezJQ
  11ForeverXXXXXXXXXXXXXXXXXXWcSE4Z
  ```

  presumably the man's name is "Ye Chunnan", possible profile: [https://github.com/finway-china](https://github.com/finway-china)
<a id="_1146"></a>
- [tx bf40e4a1c2546747bc800a085e7145d921a9f402aaf4040c155ff5d0df9cc999](https://www.blockchain.com/explorer/transactions/btc/bf40e4a1c2546747bc800a085e7145d921a9f402aaf4040c155ff5d0df9cc999) block 161202 (2012-01-08) encodes:<a id="_1147"></a>

  ```
  11When1DieBuryMeDeepLayTwoXVEY5jv
  11SpeakersAtMyFeetAPairofXXTyrHor
  11HeadphonesonMyHeadAndXXXXYUSvnd
  11ALwaysPLayTheGratefuLDeadWdq4Xo
  ```

  <a id="_1148"></a>
  > When I die, bury me deep, lay two speakers at my feet, a pair of headphones on my head. Always play the grateful dead.

  Related quote mention: [https://www.reddit.com/r/quotes/comments/w51yfg/comment/iwnxk9i/](https://www.reddit.com/r/quotes/comments/w51yfg/comment/iwnxk9i/)
<a id="_1149"></a>
- [tx 3a027fadac6ac2d9cf54480667465ba6ad88b7b3c1de62e1cb34cd06a44243ac](https://www.blockchain.com/explorer/transactions/btc/3a027fadac6ac2d9cf54480667465ba6ad88b7b3c1de62e1cb34cd06a44243ac) block 161267 (2012-01-08) has a birthday wish:<a id="_1150"></a>

  ```
  11HappyBirthdayStephenXXXXXZL6eQZ
  11HawkingXXXXXXXXXXXXXXXXXXRu9FPe
  ```

  <a id="_1151"></a>
  > Happy birthday Stephen Hawking

  <a id="image-stephen-hawking"></a>
  ![](https://upload.wikimedia.org/wikipedia/commons/e/eb/Stephen_Hawking.StarChild.jpg)

  **[Figure 95](#image-stephen-hawking). Stephen Hawking**. [Source](https://commons.wikimedia.org/wiki/File:Stephen_Hawking.StarChild.jpg). Off-chain image.
<a id="_1152"></a>
- [1BrianDeeryWasHereCaryNCUSAy1hRCCC](https://www.blockchain.com/explorer/addresses/btc/1BrianDeeryWasHereCaryNCUSAy1hRCCC) on [tx c584dd7d3e9ba9776d61ae91f801371e21e434b9d8dab3c81850301433a50fcb](https://www.blockchain.com/explorer/transactions/btc/c584dd7d3e9ba9776d61ae91f801371e21e434b9d8dab3c81850301433a50fcb) block 188657 (2012-06-12) is a check-in by a Brian Deery at Cary, NC, USA. Most likely:<a id="_1153"></a>

  <a id="_1154"></a>
  - [https://www.crunchbase.com/person/brian-deery](https://www.crunchbase.com/person/brian-deery)
  <a id="_1155"></a>
  - [https://x.com/deery_me](https://x.com/deery_me)
  <a id="_1156"></a>
  - [https://www.findinggeniuspodcast.com/podcasts/brian-deery-on-asic-boost-the-blockchain-and-the-history-and-future-of-bitcoin/](https://www.findinggeniuspodcast.com/podcasts/brian-deery-on-asic-boost-the-blockchain-and-the-history-and-future-of-bitcoin/)
<a id="_1157"></a>
- [tx 143a3d7e7599557f9d63e7f224f34d33e9251b2c23c38f95631b3a54de53f024](https://www.blockchain.com/explorer/transactions/btc/143a3d7e7599557f9d63e7f224f34d33e9251b2c23c38f95631b3a54de53f024) block 306,204 (2014-06-16) has a [Star Wars opening crawl](https://ourbigbook.com/go/topic/star-wars-opening-crawl):<a id="_1158"></a>

  ```
  1EpisodeiV111111111111111111wbq9i2
  1ANewHope1111111111111111111vnYm6D
  111111111111111111112xT3273
  1itisAPeriodofCiviLWarRebeLyzK2rV
  1SpaceshipsStrikingFromA111vh24Fi
  1HiddenBaseHaveWonTheirFirstVCugGV
  1VictoryAgainstTheEviL111123YSBKF
  1GaLacticEmpire1111111111111xsW5HG
  1111111111111111111141MmnWZ
  1DuringTheBattLeRebeLSpies11ybfhTP
  1ManagedToSteaLSecretPLansToxvKf4K
  1TheEmpiresULtimateWeapon11zoRcyn
  1TheDEATHSTARAnArmoredSpacezUyCHa
  1StationWithEnoughPowerTo11vFTWwP
  1DestroyAnEntirePLanet1111122KUcy5
  111111111111111111114ysyUW1
  1PursuedByTheEmpiresSinisterypjWrk
  1AgentsPrincessLeiaRacesHomewxuNTT
  1AboardHerStarshipCustodian1yhX6zg
  1ofTheStoLenPLansThatCan111zCJt3F
  1SaveHerPeopLeAndRestore111yULD1y
  1FreedomToTheGaLaxy1111111122roNk3
  ```

  <a id="image-star-wars-opening-crawl"></a>
  ![](https://web.archive.org/web/20250328114856im_/https://ew.com/thmb/eW1iuH6MfyudbBScg2O34cYe3Uw=/1500x0/filters:no_upscale():max_bytes(150000):strip_icc()/star-wars-crawl-02-d8ed15dbd1fe4127858c3e22593988be.jpg)

  **[Figure 96](#image-star-wars-opening-crawl). Star Wars Opening Crawl**. [Source](https://ew.com/article/2015/12/22/star-wars-crawl-creator/). Off-chain image.
<a id="_1159"></a>
- [1PavedWithGodAndSomeTeensionXudq5X](https://www.blockchain.com/explorer/addresses/btc/1PavedWithGodAndSomeTeensionXudq5X) on [tx 3e1572ca351d743d7bf627bc844da8f3bdc84eab4a9d27934a8dba30a2e05fe1](https://www.blockchain.com/explorer/transactions/btc/3e1572ca351d743d7bf627bc844da8f3bdc84eab4a9d27934a8dba30a2e05fe1) block 371894 (2015-08-28) is the largest likely burn that we know of with a single transaction, totalling 1.61803399 BTC<a id="_1160"></a>
  > Paved With God And Some Teension

  It is unclear what this means exactly and we can't find any pre-existing soruces, but it seems to be a variant of the well known:<a id="_1161"></a>
  > [The road to hell is paved with good intentions](https://ourbigbook.com/go/topic/the-road-to-hell-is-paved-with-good-intentions)
<a id="_1162"></a>
- [1NakamotoSatoshiCraigWright8RwLKB](https://www.blockchain.com/explorer/addresses/btc/1NakamotoSatoshiCraigWright8RwLKB) appears on two transactions mentioning our friend [Craig Steven Wright](../craig-steven-wright.md), the first being [tx 2e3207cc93844e2684bdc0bb856c32a6b703dab5b4ba19ed4f06b3fd581b61c3](https://www.blockchain.com/explorer/transactions/btc/2e3207cc93844e2684bdc0bb856c32a6b703dab5b4ba19ed4f06b3fd581b61c3) block 474472 (2016-06-13)<a id="_1163"></a>
  > Nakamoto Saoshi Craig Wright

  A few others include:<a id="_1164"></a>

  <a id="_1165"></a>
  - [1FuckRogerVerCraigWrightJihanBGMX3](https://www.blockchain.com/explorer/addresses/btc/1FuckRogerVerCraigWrightJihanBGMX3) (2018-02-08)<a id="_1166"></a>
    > Fuck [Roger Ver](https://ourbigbook.com/go/topic/roger-ver) [Craig Wright](https://ourbigbook.com/go/topic/craig-wright) [Jihan](https://ourbigbook.com/go/topic/jihan-wu)
  <a id="_1167"></a>
  - [1CraigWrightisAFrausterCuntwgASwJ](https://www.blockchain.com/explorer/addresses/btc/1CraigWrightisAFrausterCuntwgASwJ) (2019-06-02)<a id="_1168"></a>
    > [Craig Wright](../craig-steven-wright.md) is a fraudster cunt
  <a id="_1169"></a>
  - [1FuckYouGraigWrightxSatoshiXc6ppN](https://www.blockchain.com/explorer/addresses/btc/1FuckYouGraigWrightxSatoshiXc6ppN) (2020-06-24)<a id="_1170"></a>
    > Fuck [Craig Wright](../craig-steven-wright.md)

  <a id="image-craig-steven-wright"></a>
  ![](https://web.archive.org/web/20250124020342im_/https://i.guim.co.uk/img/media/a3e4de579a13e709b9705e1225804654b5e61e14/1009_1_2530_1518/master/2530.jpg?width=620&amp;dpr=1&amp;s=none&amp;crop=none)

  **[Figure 97](#image-craig-steven-wright). Craig Steven Wright**. [Source](https://www.theguardian.com/technology/2021/dec/07/australian-man-craig-wright-wins-us-court-battle-for-bitcoin-fortune-worth-billions). Off-chain image. The dude is so crooked that you can tell it just by looking at him for 2 seconds! Epic.

<a id="_1171"></a>
Related:<a id="_1172"></a>

<a id="_1173"></a>
- [https://www.reddit.com/r/Buttcoin/comments/3kqdjv/a_list_of_bitcoin_addresses_used_to_intentionally/](https://www.reddit.com/r/Buttcoin/comments/3kqdjv/a_list_of_bitcoin_addresses_used_to_intentionally/) A list of bitcoin addresses used to intentionally burn bitcoin (2015-09-13). Their list is not based solely on base58 images, e.g. [1A1zP1eP5QGefi2DMPTfTL5SLmv7DivfNa](../genesis-block-output-address.md) from the [Genesis block](../genesis-block.md) is present. Also their ordering is unclear, it's neither stricly chronological nor by value. But it is a good list however.
<a id="_1174"></a>
- [https://github.com/BranndonWork/bitcoin-bulk-balance-check/blob/master/burned.csv](https://github.com/BranndonWork/bitcoin-bulk-balance-check/blob/master/burned.csv)
<a id="_1175"></a>
- [https://bitcointalk.org/index.php?topic=84569](https://bitcointalk.org/index.php?topic=84569) Vanity Pool - vanity address generator pool
<a id="_1176"></a>
- [https://bitcointalk.org/index.php?topic=85935](https://bitcointalk.org/index.php?topic=85935) Coins sent to the great wallet in the sky (2012-06-07)
<a id="_1177"></a>
- [https://bitcointalk.org/index.php?topic=90982.285](https://bitcointalk.org/index.php?topic=90982.285) Rare address hall of fame (2015)
<a id="_1178"></a>
- [https://bitcointalk.org/index.php?topic=917913.0](https://bitcointalk.org/index.php?topic=917913.0) Burn Baby Burn! - Compiling all Bitcoin burn addresses by fairglu (2015)
<a id="_1179"></a>
- [https://bitcointalk.org/index.php?topic=553449.0](https://bitcointalk.org/index.php?topic=553449.0) Longest most impressive VANITY (2014)
<a id="_1180"></a>
- [https://bitcointalk.org/index.php?topic=558604.0](https://bitcointalk.org/index.php?topic=558604.0) Custom Bitcoin address? (2014)
<a id="_1181"></a>
- [https://medium.com/@westkate37/burned-bitcoins-d9b15b3699d6](https://medium.com/@westkate37/burned-bitcoins-d9b15b3699d6)
<a id="_1182"></a>
- [https://www.bitcoinwhoswho.com/blog/2018/12/29/2-btc-burned-in-2018/](https://www.bitcoinwhoswho.com/blog/2018/12/29/2-btc-burned-in-2018/)
<a id="_1183"></a>
- [https://bitcoin.stackexchange.com/questions/70241/whats-with-this-address-1111111111111111111114olvt2/125931#125931](https://bitcoin.stackexchange.com/questions/70241/whats-with-this-address-1111111111111111111114olvt2/125931#125931)
<a id="_1184"></a>
- [https://bitcoin.stackexchange.com/questions/49625/whats-the-point-of-bitcoin-eaters](https://bitcoin.stackexchange.com/questions/49625/whats-the-point-of-bitcoin-eaters) mentions in particular `1BitcoinEaterAddressDontSendf59kuE`
<a id="_1185"></a>
- [https://kf106.medium.com/interesting-addresses-on-the-bitcoin-blockchain-e0956f06ec01](https://kf106.medium.com/interesting-addresses-on-the-bitcoin-blockchain-e0956f06ec01) has some interesting monetary ones, not inscriptions
<a id="_1186"></a>
- [https://www.bitcoinwhoswho.com/blog/2016/06/01/the-7-most-incredible-bitcoin-addresses/](https://www.bitcoinwhoswho.com/blog/2016/06/01/the-7-most-incredible-bitcoin-addresses/) The 7 Most Incredible Bitcoin Addresses (2016)

**Table of contents**

- [etchablock.com](etchablock-com.md)

## ↑ Ancestors (13)

1. [Text](text.md)
2. [Media type](media-type.md)
3. [Cool data embedded in the Bitcoin blockchain](../cool-data-embedded-in-the-bitcoin-blockchain-split.md)
4. [Bitcoin inscription](../bitcoin-inscription.md)
5. [Bitcoin](../bitcoin.md)
6. [List of cryptocurrencies](../list-of-cryptocurrencies.md)
7. [Cryptocurrency](../cryptocurrency-split.md)
8. [Blockchain](../blockchain.md)
9. [Money](../money.md)
10. [Social technology](../social-technology-split.md)
11. [Area of technology](../area-of-technology.md)
12. [Technology](../technology-split.md)
13. [Ciro Santilli's Homepage](../split.md)

## ← Incoming links (4)

- [Bitcoin 2011 vanity address pool](../bitcoin-2011-vanity-address-pool.md)
- [etchablock.com](etchablock-com.md)
- [Themes](themes.md)
- [New Bitcoin Base58 messages found due to a new paper: Bitcoin Burn Addresses: Unveiling the Permanent Losses and Their Underlying Causes](../updates/new-bitcoin-base58-messages-found-due-to-a-new-paper-bitcoin-burn-addresses-unveiling-the-permanent-losses-and-their-underlying-causes.md)
