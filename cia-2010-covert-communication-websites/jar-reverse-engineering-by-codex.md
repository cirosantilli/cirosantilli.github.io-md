# [JAR](../jar-file-format.md) reverse engineering by Codex

↑ **Parent:** [JAR reverse engineering](jar-reverse-engineering.md)  
🏷️ **Tags:** [JAR](../jar-file-format.md)

This project was originally done before [Ciro Santilli](../ciro-santilli-split.md) knew how to use [Codex](../codex.md) and before Codex was so incredibly strong. Codex 6 Astra High can now just disassemble, deobfuscate and datamine the fuck out of such binaries, so we asked it to. Unfortunately it couldn't really find anything mind blowing, but here are the results anyways.

The analysis scripts is: [jar.py](https://github.com/cirosantilli/media/blob/master/cia-2010-covert-communication-websites/jar.py) and it should be pointed to a dump directory of the websites such as [CIA 2010 websites dump](cia-2010-websites-dump.md). The analysis below was done as of commit b9eb31618c36421133e4875bc1cd7d7ac7763a32.

These scripts produce TODO directories.

The JARs are obfuscated, and Codex believes that they have a strong match to the [Zelix KlassMaster](https://www.zelix.com/) commercial obfuscator, and points to this analysis from 2006: [https://www.exploit-db.com/docs/english/13132-cracking-string-encryption-in-java-obfuscated-bytecode.pdf](https://www.exploit-db.com/docs/english/13132-cracking-string-encryption-in-java-obfuscated-bytecode.pdf). Zelix appears to have the exact same string obfucation mechanism [quat1024](jar-reverse-engineering-by-quat1024.md) had already previously manually discovered. It stores all string literals XOR'ed with 5 consecutive key bytes along:
```
switch (character_index % 5):
    case 0: key = 47
    case 1: key = 41
    case 2: key = 84
    case 3: key = 35
    default: key = 14
```
It then injects an encoder/decoder for this which transforms the strings as neede at runtime. The bytes are present in each class file itself.

Zelix is made by an [Australian company](https://www.zelix.com/klassmaster/contactUs.html) based in Narraweena and its website proudly sates:

> Leading Java Obfuscator since 1997

Shame they failed to list the [CIA](../central-intelligence-agency.md) in their users list! I'm goign to ping them actually.

Here are the best small finds:
- some of the `resource/resources.bin` files contain the string:
  ```
  #Auto-generated Starbuck client config file
  ```
  Codex could not find any clear public reference to what `Starbuck` is, which leads to the tentalizing possibility that could be an internal project codename. Though the possibility that it is just some internal of some public tool so obscure that even the web has lost track of it is also too strong to refute entirely.

  This string is part of a more complete key/value pair, e.g. `dryterrainnews.com` contains:
  - key: `Config.properties.old.1277148810409`
  - value:

    ```
    #Auto-generated Starbuck client config file: Mon Jun 21 14:32:02 ACT 2010
    #Mon Jun 21 14:32:02 ACT 2010
    ServerURL=http\\://www.dryterrainnews.com/cgi-bin/nigeria.cgi
    EncSharedSecret=7A948986EF08B9DDF800E5AF229EC118D4F8AD9609C5080CBF2AB92397C2A9B8
    KeyE=1F7D7
    KeyN=67D8EA7BF935232E55863DCED7A279F701B7492316FE96F15D00C983CBFDB93B97D35898FA8928FA13D4F320E2B62D1B92F08FA8692F7D043EC197E2857D2A540E01A2529AEB232EB386917992B80D5CADE283D2C4E8DCBF682704F419E29D013FFCF33D9A1BC94E4AA469058BB508EEE1D654CF9FC4B89977A13FA33CDEDAED
    ```
  which would be present insie the `resource/resources.bin` file present inside the [JAR](../jar-file-format.md).

  `resource/resources.bin` file is encrypted with [International Data Encryption Algorithm](../international-data-encryption-algorithm.md), a public [symmetric encryption](../symmetric-encryption.md) standard. However the key is itself present inside the JAR as an XOR obfuscated string.

  The decrypted form of `resource/resources.bin` is a custom key value format which Codex could not identify the source of for the life in it. The JAR contains a decoder for it in its code.

  There are different alternative filenames for this file all with the same format, each one with a single key used across all JARs, and each JAR having at most one of them:
  - `Applet.properties`: key: `7A5DAEC4029C91ED`, occurances: 76. Exmaple: `aryannews.net/20101229122727/headlines.jar` path `c/b/b/Applet.properties`.
  - `Client.properties`: key: `60A514D96C19F93C`, occurances: 33. Example: `activegaminginfo.com/20110202130304/gaming.jar` path  `a/b/f/Client.properties`
  - `resource/resources.bin`: key: `0C5C45F2EC3C2A63`, occurances: 45. Example: `all-sport-headlines.com/20110207144821/birdie.jar` path `resource/resources.bin`

  The remaining JARs use other arrangements:
  - `applet.configs`, XOR-obfuscated as a single string: 35. Example: `aeronet-news.com/20110202122601/aeronet.jar` path `a/a/b/applet.configs`. Deobfuscated content might look like:

    ```
    #Applet Properties
    #Thu Aug 19 08:19:00 AMT 2010
    RequestKey.UserData.1.IsQuery=set
    Applet.BundleSize=1
    ResponseKey.UserData.0.Size=85
    ```
  - `bw.properties`, ZIP-packed: 30. Example: `casanewsnow.com/20110201184918/casanews.jar` path `b/a/bw.properties`
  - none of these configuration resources: 9. Example: `factorforcenews.com/20110202125321/factorspeed.jar`

  These files contain a wide variety of resources, including server paths, images, user strings and various settings.
- there's a certain number of timestamps present in the Jars. Although these could have been faked, it feels unlikey that they were. The sources of those include:
  - ZIP modification time of each file
    - present in: all [JAR](../jar-file-format.md), since JARs are ZIPs
    - timezone: no
    - visible with: `zipinfo -v travelxtreme.net/20101226193020/xtreme.jar`
  - Certificate validity dates: 
    - present in 37 JARs. Example: `latinamericanewsbeat.com/20100513191045/today.jar` file `META-INF/INLINE.DSA`
    - timezone: yes
    - format: Standard binary `PKCS#7/X.509` encoding unencrypted, readable with OpenSSL
    - usage: these are part of a standard JAR public key signatures scheme, which if a key trusted would have given greater execution priviledges to the JAR. They are validly signed but self signed as you might expect...
  - `applet.configs`: comment timestamp as shown above
  - `Starbuck` client comment as shown above:
    ```
    #Auto-generated Starbuck client config file: Mon Jun 21 14:32:02 ACT 2010
    ```
  - config key backup Unix epoch milliseconds key, e.g. the `1277148810409` in `Config.properties.old.1277148810409`. So their editing tool kept backups as they were editing it, which is a small OPSEC defect.

We've dumped timestamp data to: [https://github.com/cirosantilli/media/blob/master/cia-2010-covert-communication-websites/jar/dates.csv](https://github.com/cirosantilli/media/blob/master/cia-2010-covert-communication-websites/jar/dates.csv) No dates of interest was found in the [SWF](swf-reverse-engineering.md).

Many of the timestamps present are much older than the earliest archive we have for each website, suggesting that they were around for much longer. E.g. 2005-06-02.

The operators worked exclusively on weekdays, and much less on Friday than other days of the week, lol they're only human:
```
   Day          Configuration timestamps    Distinct configuration calendar dates    ZIP timestamps¹
   Monday                             21                                       11                 72
   Tuesday                            12                                       10                 78
   Wednesday                          16                                       13                 72
   Thursday                           12                                       11                 72
   Friday                              5                                        5                 60
   Saturday                            0                                        0                  0
   Sunday                              0                                        0                  0
```
92% of timestamps fall in conventional work hours between 08:00 and 18:00, so it was not a James Bond work through the clock to save the world business.

The timezones are:
```
Timezone label    applet.configs    Backups in resources.bin    Total    Possible locations / interpretations
  EST                          9                           4       13    Eastern United States, eastern Canada, parts of the Caribbean
  EDT                          8                          11       19    Eastern United States, eastern Canada, parts of the Caribbean
  AMT                         18                           0       18    Western Brazil (Amazon Time), Armenia
  ACT                          0                          16       16    Acre in Brazil (Acre Time), Northern Territory in Australia if interpreted as Java’s short timezone ID
```

There are a few plausible timestamp trigram documentations with slightly different possibilities among them:
- [https://code.googlesource.com/edge/openjdk/+/refs/heads/master/jdk/src/share/classes/java/time/ZoneId.java](https://code.googlesource.com/edge/openjdk/+/refs/heads/master/jdk/src/share/classes/java/time/ZoneId.java)
- [https://docs.oracle.com/cd/E98457_01/opera_5_6_core_help/PDFs/Time_Zones.pdf](https://docs.oracle.com/cd/E98457_01/opera_5_6_core_help/PDFs/Time_Zones.pdf)
- [https:////android.googlesource.com/platform/libcore/+/9f08ee8977750b228382eaf9a081f4847a1e0377/jdk/src/share/classes/sun/util/resources/TimeZoneNames.java](https:////android.googlesource.com/platform/libcore/+/9f08ee8977750b228382eaf9a081f4847a1e0377/jdk/src/share/classes/sun/util/resources/TimeZoneNames.java)

EST an EDT are obvious, [Langley](../langley.md). ACT is understandable, Australia, a [Five Eyes](../five-eyes.md) country and center of US espionage is East Asia. But AMT? That one is weird.

A few sites have timestamps from multiple locations e.g.:
```
Site                               Labels and counts
internationalnewsworthiness.com    EDT ×2, ACT ×2
intlnewsdaily.com                  EDT ×2, ACT ×1
www.myhealthlibrary.net            EDT ×1, ACT ×5
www.todaysnewsreports.net          EDT ×1, ACT ×3
```

Codex also spots the interesting case of myhealthlibrary on April 11, 2011 backup sequence, configuration comments go:
```
09:18:19 ACT
13:59:13 EDT
13:34:14 ACT
13:43:20 ACT
14:17:18 ACT
```
which in UTC would jump backwards in time if ACT actually means Australia...
```
09:18:19 ACT    April 10, 23:48:19
13:59:13 EDT    April 11, 17:59:13
13:34:14 ACT    April 11, 04:04:14
13:43:20 ACT    April 11, 04:13:20
14:17:18 ACT    April 11, 04:47:18
```
but would work neatly if ACT is actualy Acre Standard time at UTC-4. Damn, Brazilian operators???
```
14:18:19 UTC
17:59:13 UTC
18:34:14 UTC
18:43:20 UTC
19:17:18 UTC
```
Codex also comments:

> One historical wrinkle: Acre’s official clocks used UTC−4 during 2008–2013, including April 2011. An older Java timezone database could still apply UTC−5, so the label alone doesn’t establish the offset actually used.

Too strong. Too strong.

About the backups Codex analyses:

> 
> - 31 backups across 11 sites; eight sites have multiple backups.
> - Of 20 successive intervals, 11 are under an hour, 15 under a day.
> - Four intervals exceed a month; the longest is about 560 days.
> 
> This fits bursts of configuration work followed by occasional maintenance.

## ↑ Ancestors (16)

1. [JAR reverse engineering](jar-reverse-engineering.md)
2. [Communication mechanism](communication-mechanism.md)
3. [Reverse engineering](reverse-engineering.md)
4. [Methodology](methodology.md)
5. [CIA 2010 covert communication websites](../cia-2010-covert-communication-websites-split.md)
6. [Central Intelligence Agency](../central-intelligence-agency.md)
7. [American intelligence agency](../american-intelligence-agency.md)
8. [United States Intelligence Community](../united-states-intelligence-community.md)
9. [Intelligence community](../intelligence-community.md)
10. [Secret service](../secret-service.md)
11. [Espionage](../espionage.md)
12. [War](../war.md)
13. [Social science](../social-science.md)
14. [Scientific method](../scientific-method.md)
15. [Science](../science-split.md)
16. [Ciro Santilli's Homepage](../split.md)
