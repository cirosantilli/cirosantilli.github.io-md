# [JAR](../jar-file-format.md) reverse engineering

↑ **Parent:** [Communication mechanism](communication-mechanism.md)

<a id="_6569"></a>
TODO it would be cool to have a look at the JARs and see if they have anything in common that makes for a good fringerprint. Would not help find new ones, but would help to confirm possible hits.

<a id="_6570"></a>
The most advanced reverse engineering effort so far has been by [GitHub user quat1024](https://github.com/quat1024), an undergratuate student at Ohio State University, [Minecraft modding extraordinaire](https://modrinth.com/user/quat) and [furry afficionado](https://highlysuspect.agency/photos/). Minecraft is written in Java, which may partly explains his Java skills.<a id="_6571"></a>

<a id="_6572"></a>
- [https://github.com/cirosantilli/cirosantilli.github.io/issues/203](https://github.com/cirosantilli/cirosantilli.github.io/issues/203)
<a id="_6573"></a>
- [https://notes.highlysuspect.agency/cia-jars.html](https://notes.highlysuspect.agency/cia-jars.html)
He managed to deobfuscate the strings present inthe JARs using Enigma, possibly [https://github.com/FabricMC/Enigma](https://github.com/FabricMC/Enigma), a Java reverse engineering tool. Cool findings on [https://web.archive.org/web/20110208072027/http://newsupdatesite.com/update.jar](https://web.archive.org/web/20110208072027/http://newsupdatesite.com/update.jar) include:<a id="_6574"></a>

<a id="_6575"></a>
- `applet.configs1` deobfuscated contains a date:<a id="_6576"></a>

  ```
   Fri Feb 05 12:04:29 EST 2010
  ```

  Also cool is the present of a timeszone, "EST" unsurprisingly.

<a id="_6577"></a>
[https://web.archive.org/web/20110208072027/http://newsupdatesite.com/update.jar](https://web.archive.org/web/20110208072027/http://newsupdatesite.com/update.jar) unzips to:

<a id="_6578"></a>
<a id="_6579"></a>

```
.
./c
./c/b
./c/b/b.class
./c/b/c.class
./c/b/d.class
./c/b/a
./c/b/a/a.class
./c/b/a/b.class
./c/b/a/c.class
./c/b/a/d.class
./c/a
./c/a/a.class
./c/a/b.class
./c/a/c.class
./b
./b/a
./b/a/a
./b/a/a/e.class
./b/a/a/f.class
./b/a/a/a.class
./b/a/a/b.class
./b/a/a/g.class
./b/a/a/c.class
./b/a/a/d.class
./META-INF
./META-INF/MANIFEST.MF
./a
./a/cre
./a/a
./a/a/b
./a/a/b/a.class
./a/a/a
./a/a/a/e.class
./a/a/a/applet.configs
./a/a/a/b
./a/a/a/b/e.class
./a/a/a/b/f.class
./a/a/a/b/b.class
./a/a/a/b/g.class
./a/a/a/b/c.class
./a/a/a/b/d.class
./a/a/a/b/a
./a/a/a/b/a/a.class
./a/a/a/b/a/b.class
./a/a/a/b/a/c.class
./a/a/a/c.class
./a/a/a/d.class
./a/a/a/a
./a/a/a/a/a.class
```
so it is fully obfuscated.

<a id="_6580"></a>
`./META-INF/MANIFEST.MF`<a id="_6581"></a>

```
Manifest-Version: 1.0
Ant-Version: Apache Ant 1.7.1
Created-By: 1.5.0_17-b04 (Sun Microsystems Inc.)
```

<a id="_6582"></a>
Other files whose existence might help to fingerprint include:<a id="_6583"></a>

<a id="_6584"></a>
- `a/a/a/applet.configs`
<a id="_6585"></a>
- empty `a/cre`

<a id="_6586"></a>
A quick:<a id="_6587"></a>

```
find . -type f | xargs strings | sort -u
```
does not reveal any obvious cryptography calls.

<a id="_6588"></a>
[https://web.archive.org/web/20110207204640/http://flyingtimeline.com/aircraft.jar](https://web.archive.org/web/20110207204640/http://flyingtimeline.com/aircraft.jar) is very similar looking. `META-INF/MANIFEST.MF` is identical:<a id="_6589"></a>

```
Manifest-Version: 1.0
Ant-Version: Apache Ant 1.7.1
Created-By: 1.5.0_17-b04 (Sun Microsystems Inc.)
```

<a id="_6590"></a>
[https://web.archive.org/web/20110202185659/http://differentviewtoday.com/bwm.jar](https://web.archive.org/web/20110202185659/http://differentviewtoday.com/bwm.jar) is a bit different with tree:<a id="_6591"></a>

```
META-INF/MANIFEST.MF
a/a.class
b/a/a/a.class
b/a/a/b.class
b/a/a/c.class
b/a/b/a.class
b/a/b/b.class
b/a/b/c.class
b/a/b/d.class
b/a/b/e.class
b/a/bw.properties
b/a/c.class
c/a/a/a.class
c/a/a/b.class
c/a/a/c.class
c/a/a/d.class
c/a/b.class
c/a/c.class
c/a/d.class
c/a/e.class
c/b/a.class
c/b/b.class
c/b/c.class
```
and:<a id="_6592"></a>

```
META-INF/MANIFEST.MF
Manifest-Version: 1.0
Ant-Version: Apache Ant 1.6.5
Created-By: 1.5.0_12-b04 (Sun Microsystems Inc.)
```

## ↑ Ancestors (15)

1. [Communication mechanism](communication-mechanism.md)
2. [Reverse engineering](reverse-engineering.md)
3. [Methodology](methodology.md)
4. [CIA 2010 covert communication websites](../cia-2010-covert-communication-websites-split.md)
5. [Central Intelligence Agency](../central-intelligence-agency.md)
6. [American intelligence agency](../american-intelligence-agency.md)
7. [United States Intelligence Community](../united-states-intelligence-community.md)
8. [Intelligence community](../intelligence-community.md)
9. [Secret service](../secret-service.md)
10. [Espionage](../espionage.md)
11. [War](../war.md)
12. [Social science](../social-science.md)
13. [Scientific method](../scientific-method.md)
14. [Science](../science-split.md)
15. [Ciro Santilli's Homepage](../split.md)
