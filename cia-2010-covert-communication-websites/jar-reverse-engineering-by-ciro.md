# [JAR](../jar-file-format.md) reverse engineering by Ciro

↑ **Parent:** [JAR reverse engineering](jar-reverse-engineering.md)  
🏷️ **Tags:** [JAR](../jar-file-format.md)

[https://web.archive.org/web/20110208072027/http://newsupdatesite.com/update.jar](https://web.archive.org/web/20110208072027/http://newsupdatesite.com/update.jar) unzips to:


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

`./META-INF/MANIFEST.MF`
```
Manifest-Version: 1.0
Ant-Version: Apache Ant 1.7.1
Created-By: 1.5.0_17-b04 (Sun Microsystems Inc.)
```

Other files whose existence might help to fingerprint include:
- `a/a/a/applet.configs`
- empty `a/cre`

A quick:
```
find . -type f | xargs strings | sort -u
```
does not reveal any obvious cryptography calls.

[https://web.archive.org/web/20110207204640/http://flyingtimeline.com/aircraft.jar](https://web.archive.org/web/20110207204640/http://flyingtimeline.com/aircraft.jar) is very similar looking. `META-INF/MANIFEST.MF` is identical:
```
Manifest-Version: 1.0
Ant-Version: Apache Ant 1.7.1
Created-By: 1.5.0_17-b04 (Sun Microsystems Inc.)
```

[https://web.archive.org/web/20110202185659/http://differentviewtoday.com/bwm.jar](https://web.archive.org/web/20110202185659/http://differentviewtoday.com/bwm.jar) is a bit different with tree:
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
and:
```
META-INF/MANIFEST.MF
Manifest-Version: 1.0
Ant-Version: Apache Ant 1.6.5
Created-By: 1.5.0_12-b04 (Sun Microsystems Inc.)
```

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
