# Internet Census 2012

↑ **Parent:** [Data sources](data-sources.md)

<a id="_6160"></a>
Does not appear to have any reverse IP hits unfortunately: [https://opendata.stackexchange.com/questions/1951/dataset-of-domain-names/21077#21077](https://opendata.stackexchange.com/questions/1951/dataset-of-domain-names/21077#21077). Likely only has domains that were explicitly advertised.

<a id="_6161"></a>
We could not find anything useful in it so far, but there is great potential to use this tool to find new IP ranges based on properties of existing IP ranges. Part of the problem is that the dataset is huge, and is split by top 256 bytes. But it would be reasonable to at least explore ranges with pre-existing known hits...

<a id="_6162"></a>
We have started looking for patterns on `66.*` and `208.*`, both selected as two relatively far away ranges that have a number of pre-existing hits. 208 should likely have been 212 considering later finds that put several ranges in 212.

<a id="_6163"></a>
tcpip\_fp:<a id="_6164"></a>

<a id="_6165"></a>
- 66.104.<a id="_6166"></a>

  <a id="_6167"></a>
  - 66.104.175.41: grubbersworldrugbynews.com: 1346397300 SCAN(V=6.01%E=4%D=1/12%OT=22%CT=443%CU=%PV=N%G=N%TM=387CAB9E%P=mipsel-openwrt-linux-gnu),ECN(R=N),T1(R=N),T2(R=N),T3(R=N),T4(R=N),T5(R=N),T6(R=N),T7(R=N),U1(R=N),IE(R=N)
  <a id="_6168"></a>
  - 66.104.175.48: worlddispatch.net:          1346816700 SCAN(V=6.01%E=4%D=1/2%OT=22%CT=443%CU=%PV=N%DC=I%G=N%TM=1D5EA%P=mipsel-openwrt-linux-gnu),SEQ(SP=F8%GCD=3%ISR=109%TI=Z%TS=A),ECN(R=N),T1(R=Y%DF=Y%TG=40%S=O%A=S+%F=AS%RD=0%Q=),T1(R=N),T2(R=N),T3(R=N),T4(R=N),T5(R=Y%DF=Y%TG=40%W=0%S=Z%A=S+%F=AR%O=%RD=0%Q=),T6(R=N),T7(R=N),U1(R=N),IE(R=N)
  <a id="_6169"></a>
  - 66.104.175.49: webworldsports.com:         1346692500 SCAN(V=6.01%E=4%D=9/3%OT=22%CT=443%CU=%PV=N%DC=I%G=N%TM=5044E96E%P=mipsel-openwrt-linux-gnu),SEQ(SP=105%GCD=1%ISR=108%TI=Z%TS=A),OPS(O1=M550ST11NW6%O2=M550ST11NW6%O3=M550NNT11NW6%O4=M550ST11NW6%O5=M550ST11NW6%O6=M550ST11),WIN(W1=1510%W2=1510%W3=1510%W4=1510%W5=1510%W6=1510),ECN(R=N),T1(R=Y%DF=Y%TG=40%S=O%A=S+%F=AS%RD=0%Q=),T1(R=N),T2(R=N),T3(R=N),T4(R=N),T5(R=Y%DF=Y%TG=40%W=0%S=Z%A=S+%F=AR%O=%RD=0%Q=),T6(R=N),T7(R=N),U1(R=N),IE(R=N)
  <a id="_6170"></a>
  - 66.104.175.50: fly-bybirdies.com:          1346822100 SCAN(V=6.01%E=4%D=1/1%OT=22%CT=443%CU=%PV=N%DC=I%G=N%TM=14655%P=mipsel-openwrt-linux-gnu),SEQ(TI=Z%TS=A),ECN(R=N),T1(R=Y%DF=Y%TG=40%S=O%A=S+%F=AS%RD=0%Q=),T1(R=N),T2(R=N),T3(R=N),T4(R=N),T5(R=Y%DF=Y%TG=40%W=0%S=Z%A=S+%F=AR%O=%RD=0%Q=),T6(R=N),T7(R=N),U1(R=N),IE(R=N)
  <a id="_6171"></a>
  - 66.104.175.53: info-ology.net:             1346712300 SCAN(V=6.01%E=4%D=9/4%OT=22%CT=443%CU=%PV=N%DC=I%G=N%TM=50453230%P=mipsel-openwrt-linux-gnu),SEQ(SP=FB%GCD=1%ISR=FF%TI=Z%TS=A),ECN(R=N),T1(R=Y%DF=Y%TG=40%S=O%A=S+%F=AS%RD=0%Q=),T1(R=N),T2(R=N),T3(R=N),T4(R=N),T5(R=Y%DF=Y%TG=40%W=0%S=Z%A=S+%F=AR%O=%RD=0%Q=),T6(R=N),T7(R=N),U1(R=N),IE(R=N)
<a id="_6172"></a>
- 66.175.106<a id="_6173"></a>

  <a id="_6174"></a>
  - 66.175.106.150: noticiasmusica.net:        1340077500 SCAN(V=5.51%D=1/3%OT=22%CT=443%CU=%PV=N%G=N%TM=38707542%P=mipsel-openwrt-linux-gnu),ECN(R=N),T1(R=N),T2(R=N),T3(R=N),T4(R=N),T5(R=Y%DF=Y%TG=40%W=0%S=Z%A=S+%F=AR%O=%RD=0%Q=),T6(R=N),T7(R=N),U1(R=N),IE(R=N)
  <a id="_6175"></a>
  - 66.175.106.155: atomworldnews.com:         1345562100 SCAN(V=5.51%D=8/21%OT=22%CT=443%CU=%PV=N%DC=I%G=N%TM=5033A5F2%P=mips-openwrt-linux-gnu),SEQ(SP=FB%GCD=1%ISR=FC%TI=Z%TS=A),ECN(R=Y%DF=Y%TG=40%W=1540%O=M550NNSNW6%CC=N%Q=),T1(R=Y%DF=Y%TG=40%S=O%A=S+%F=AS%RD=0%Q=),T2(R=N),T3(R=N),T4(R=N),T5(R=Y%DF=Y%TG=40%W=0%S=Z%A=S+%F=AR%O=%RD=0%Q=),T6(R=N),T7(R=N),U1(R=N),IE(R=N)

**Table of contents**

- [2012 Internet Census hostprobes](2012-internet-census-hostprobes.md)
- [2012 Internet Census icmp\_ping](2012-internet-census-icmp-ping.md)

## ↑ Ancestors (14)

1. [Data sources](data-sources.md)
2. [Methodology](methodology.md)
3. [CIA 2010 covert communication websites](../cia-2010-covert-communication-websites-split.md)
4. [Central Intelligence Agency](../central-intelligence-agency.md)
5. [American intelligence agency](../american-intelligence-agency.md)
6. [United States Intelligence Community](../united-states-intelligence-community.md)
7. [Intelligence community](../intelligence-community.md)
8. [Secret service](../secret-service.md)
9. [Espionage](../espionage.md)
10. [War](../war.md)
11. [Social science](../social-science.md)
12. [Scientific method](../scientific-method.md)
13. [Science](../science-split.md)
14. [Ciro Santilli's Homepage](../split.md)
