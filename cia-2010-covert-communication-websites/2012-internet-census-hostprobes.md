# 2012 Internet Census hostprobes

↑ **Parent:** [Internet Census 2012](internet-census-2012.md)

<a id="_6176"></a>
Hostprobes quick look on two ranges:

<a id="_6177"></a>
208.254.40:<a id="_6178"></a>

```
... similar down

208.254.40.95	1334668500	down	no-response
208.254.40.95	1338270300	down	no-response
208.254.40.95	1338839100	down	no-response
208.254.40.95	1339361100	down	no-response
208.254.40.95	1346391900	down	no-response
208.254.40.96	1335806100	up	unknown
208.254.40.96	1336979700	up	unknown
208.254.40.96	1338840900	up	unknown
208.254.40.96	1339454700	up	unknown
208.254.40.96	1346778900	up	echo-reply (0.34s latency).
208.254.40.96	1346838300	up	echo-reply (0.30s latency).
208.254.40.97	1335840300	up	unknown
208.254.40.97	1338446700	up	unknown
208.254.40.97	1339334100	up	unknown
208.254.40.97	1346658300	up	echo-reply (0.26s latency).

... similar up

208.254.40.126	1335708900	up	unknown
208.254.40.126	1338446700	up	unknown
208.254.40.126	1339330500	up	unknown
208.254.40.126	1346494500	up	echo-reply (0.24s latency).
208.254.40.127	1335840300	up	unknown
208.254.40.127	1337793300	up	unknown
208.254.40.127	1338853500	up	unknown
208.254.40.127	1346454900	up	echo-reply (0.23s latency).

208.254.40.128	1335856500	up	unknown
208.254.40.128	1338200100	down	no-response
208.254.40.128	1338749100	down	no-response
208.254.40.128	1339334100	down	no-response
208.254.40.128	1346607900	down	net-unreach
208.254.40.129	1335699900	up	unknown

... similar down
```

<a id="_6179"></a>
Suggests exactly 127 - 96 + 1 = 31 IPs.

<a id="_6180"></a>
208.254.42:<a id="_6181"></a>

```
... similar down

208.254.42.191	1334522700	down	no-response
208.254.42.191	1335276900	down	no-response
208.254.42.191	1335784500	down	no-response
208.254.42.191	1337845500	down	no-response
208.254.42.191	1338752700	down	no-response
208.254.42.191	1339332300	down	no-response
208.254.42.191	1346499900	down	net-unreach

208.254.42.192	1334668500	up	unknown
208.254.42.192	1336808700	up	unknown
208.254.42.192	1339334100	up	unknown
208.254.42.192	1346766300	up	echo-reply (0.40s latency).
208.254.42.193	1335770100	up	unknown
208.254.42.193	1338444900	up	unknown
208.254.42.193	1339334100	up	unknown

... similar up

208.254.42.221	1346517900	up	echo-reply (0.19s latency).
208.254.42.222	1335708900	up	unknown
208.254.42.222	1335708900	up	unknown
208.254.42.222	1338066900	up	unknown
208.254.42.222	1338747300	up	unknown
208.254.42.222	1346872500	up	echo-reply (0.27s latency).
208.254.42.223	1335773700	up	unknown
208.254.42.223	1336949100	up	unknown
208.254.42.223	1338750900	up	unknown
208.254.42.223	1339334100	up	unknown
208.254.42.223	1346854500	up	echo-reply (0.13s latency).

208.254.42.224	1335665700	down	no-response
208.254.42.224	1336567500	down	no-response
208.254.42.224	1338840900	down	no-response
208.254.42.224	1339425900	down	no-response
208.254.42.224	1346494500	down	time-exceeded

... similar down
```

<a id="_6182"></a>
Suggests exactly 223 - 192 + 1 = 31 IPs.

<a id="_6183"></a>
Let's have a look at the file `68`: outcome: no clear hits like on 208. One wonders why.

<a id="_6184"></a>
It does appears that long sequences of ranges are a sort of fingerprint. The question is how unique it would be.

<a id="_6185"></a>
First:<a id="_6186"></a>

```
n=208
time awk '$3=="up"{ print $1 }' $n | uniq -c | sed -r 's/^ +//;s/ /,/' | tee $n-up-uniq
t=$n-up-uniq.sqlite
rm -f $t
time sqlite3 $t 'create table tmp(cnt text, i text)'
time sqlite3 $t ".import --csv $n-up-uniq tmp"
time sqlite3 $t 'create table t (i integer)'
time sqlite3 $t '.load ./ip' 'insert into t select str2ipv4(i) from tmp'
time sqlite3 $t 'drop table tmp'
time sqlite3 $t 'create index ti on t(i)'
```
This reduces us to 2 million IP rows from the total possible 16 million IPs.

<a id="_6187"></a>
OK now just counting hits on fixed windows has way too many results:<a id="_6188"></a>

```
sqlite3 208-up-uniq.sqlite "\
SELECT * FROM (
  SELECT min(i), COUNT(*) OVER (
    ORDER BY i RANGE BETWEEN 15 PRECEDING AND 15 FOLLOWING
  ) as c FROM t
) WHERE c > 20 and c < 30
"
```

<a id="_6189"></a>
Let's try instead consecutive ranges of length exactly 31 instead then:<a id="_6190"></a>

```
sqlite3 208-up-uniq.sqlite <<EOF
SELECT f, t - f as c FROM (
  SELECT min(i) as f, max(i) as t
  FROM (SELECT i, ROW_NUMBER() OVER (ORDER BY i) - i as grp FROM t)
  GROUP BY grp
  ORDER BY i
) where c = 31
EOF
```
271. Hmm. A bit more than we'd like...

<a id="_6191"></a>
Another route is to also count the ups:<a id="_6192"></a>

```
n=208
time awk '$3=="up"{ print $1 }' $n | uniq -c | sed -r 's/^ +//;s/ /,/' | tee $n-up-uniq-cnt
t=$n-up-uniq-cnt.sqlite
rm -f $t
time sqlite3 $t 'create table tmp(cnt text, i text)'
time sqlite3 $t ".import --csv $n-up-uniq-cnt tmp"
time sqlite3 $t 'create table t (cnt integer, i integer)'
time sqlite3 $t '.load ./ip' 'insert into t select cnt as integer, str2ipv4(i) from tmp'
time sqlite3 $t 'drop table tmp'
time sqlite3 $t 'create index ti on t(i)'
```

<a id="_6193"></a>
Let's see how many consecutives with counts:<a id="_6194"></a>

```
sqlite3 208-up-uniq-cnt.sqlite <<EOF
SELECT f, t - f as c FROM (
  SELECT min(i) as f, max(i) as t
  FROM (SELECT i, ROW_NUMBER() OVER (ORDER BY i) - i as grp FROM t WHERE cnt >= 3)
  GROUP BY grp
  ORDER BY i
) where c > 28 and c < 32
EOF
```

<a id="_6195"></a>
Let's check on 66:<a id="_6196"></a>

```
grep -e '66.45.179' -e '66.45.179' 66
```
not representative at all... e.g. several convfirmed hits are down:<a id="_6197"></a>

```
66.45.179.215   1335305700      down    no-response
66.45.179.215   1337579100      down    no-response
66.45.179.215   1338765300      down    no-response
66.45.179.215   1340271900      down    no-response
66.45.179.215   1346813100      down    no-response
```

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
