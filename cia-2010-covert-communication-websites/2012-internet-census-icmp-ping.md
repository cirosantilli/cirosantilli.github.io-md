<h1 id="2012-internet-census-icmp-ping">2012 Internet Census icmp_ping</h1>

↑ **Parent:** [Internet Census 2012](internet-census-2012.md)

<a id="_6198"></a>
Let's check relevancy of known hits:<a id="_6199"></a>

```
grep -e '208.254.40' -e '208.254.42' 208 | tee 208hits
```
Output:<a id="_6200"></a>

```
208.254.40.95	1355564700	unreachable
208.254.40.95	1355622300	unreachable
208.254.40.96	1334537100	alive, 36342
208.254.40.96	1335269700	alive, 17586

..

208.254.40.127	1355562900	alive, 35023
208.254.40.127	1355593500	alive, 59866
208.254.40.128	1334609100	unreachable
208.254.40.128	1334708100	alive from 208.254.32.214, 43358
208.254.40.128	1336596300	unreachable
```

<a id="_6201"></a>
The rest of 208 is mostly unreachable.

<a id="_6202"></a>
```
208.254.42.191	1335294900	unreachable
...
208.254.42.191	1344737700	unreachable
208.254.42.191	1345574700	Icmp Error: 0,ICMP Network Unreachable, from 63.111.123.26
208.254.42.191	1346166900	unreachable
...
208.254.42.191	1355665500	unreachable
208.254.42.192	1334625300	alive, 6672
...
208.254.42.192	1355658300	alive, 57412
208.254.42.193	1334677500	alive, 28985
208.254.42.193	1336524300	unreachable
208.254.42.193	1344447900	alive, 8934
208.254.42.193	1344613500	alive, 24037
208.254.42.193	1344806100	alive, 20410
208.254.42.193	1345162500	alive, 10177
...
208.254.42.223	1336590900	alive, 23284
...
208.254.42.223	1355555700	alive, 58841
208.254.42.224	1334607300	Icmp Type: 11,ICMP Time Exceeded, from 65.214.56.142
208.254.42.224	1334681100	Icmp Type: 11,ICMP Time Exceeded, from 65.214.56.142
208.254.42.224	1336563900	Icmp Type: 11,ICMP Time Exceeded, from 65.214.56.142
208.254.42.224	1344451500	Icmp Type: 11,ICMP Time Exceeded, from 65.214.56.138
208.254.42.224	1344566700	unreachable
208.254.42.224	1344762900	unreachable
```

<a id="_6203"></a>
Let's try with 66. First there way too much data, 9 GB, let's cut it down:

<a id="_6204"></a>
```
n=66
time awk '$3~/^alive,/ { print $1 }' $n | uniq -c | sed -r 's/^ +//;s/ /,/' | tee $n-up-uniq-c
```

<a id="_6205"></a>
OK down to 45 MB, now we can work.

<a id="_6206"></a>
```
grep -e '66.45.179' -e '66.104.169' -e '66.104.173' -e '66.104.175' -e '66.175.106' '66-alive-uniq-c' | tee 66hits
```

<a id="_6207"></a>
Nah, it's full of holes:<a id="_6208"></a>

```
4,66.45.179.187
12,66.45.179.188
2,66.45.179.197
1,66.45.179.202
2,66.45.179.205
2,66.45.179.206
1,66.45.179.207
```
won't be able to find new ranges here.

## ↑ Ancestors (15)

1. [Internet Census 2012](internet-census-2012.md)
2. [Data sources](data-sources.md)
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
