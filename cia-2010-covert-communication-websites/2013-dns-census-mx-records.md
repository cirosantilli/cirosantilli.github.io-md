# 2013 DNS census MX records

↑ **Parent:** [DNS Census 2013](dns-census-2013.md)

Let' see if there's anything in records/mx.xz.

mx.csv is 21GB.

They do have `"` in the files to escape commas so:

mx.py
```
import csv
import sys
writer = csv.writer(sys.stdout)
with open('mx.csv', 'r') as f:
    reader = csv.reader(f)
    for row in reader:
        writer.writerow([row[0], row[3]])
```
Would have been better with csvkit: [https://stackoverflow.com/questions/36287982/bash-parse-csv-with-quotes-commas-and-newlines](https://stackoverflow.com/questions/36287982/bash-parse-csv-with-quotes-commas-and-newlines)

then:

```
# uniq not amazing as there are often two or three slightly different records repeated on multiple timestamps, but down to 11 GB
python3 mx.py | uniq > mx-uniq.csv
sqlite3 mx.sqlite 'create table t(d text, m text)'
# 13 GB
time sqlite3 mx.sqlite ".import --csv --skip 1 'mx-uniq.csv' t"

# 41 GB
time sqlite3 mx.sqlite 'create index td on t(d)'
time sqlite3 mx.sqlite 'create index tm on t(m)'
time sqlite3 mx.sqlite 'create index tdm on t(d, m)'

# Remove dupes.
# Rows: 150m
time sqlite3 mx.sqlite <<EOF
delete from t
where rowid not in (
  select min(rowid)
  from t
  group by d, m
)
EOF

# 15 GB
time sqlite3 mx.sqlite vacuum
```

Let's see what the hits use:
```
awk -F, 'NR>1{ print $2 }' ../media/cia-2010-covert-communication-websites/hits.csv | xargs -I{} sqlite3 mx.sqlite "select distinct * from t where d = '{}'"
```

At around 267 total hits, only 84 have MX records, and from those that do, almost all of them have exactly:
```
smtp.secureserver.net
mailstore1.secureserver.net
```
with only three exceptions:
```
dailynewsandsports.com|dailynewsandsports.com
inews-today.com|mail.inews-today.com
just-kidding-news.com|just-kidding-news.com
```
We need to count out of the totals!
```
sqlite3 mx.sqlite "select count(*) from t where m = 'mailstore1.secureserver.net'"
```
which gives, ~18M, so nope, it is too much by itself...

Let's try to use that to reduce `av.sqlite` from [2013 DNS Census virtual host cleanup](2013-dns-census-virtual-host-cleanup.md) a bit further:
```
time sqlite3 mx.sqlite '.mode csv' "attach 'aiddcu.sqlite' as 'av'" '.load ./ip' "select ipi2s(av.t.i), av.t.d from av.t inner join t as mx on av.t.d = mx.d and mx.m = 'mailstore1.secureserver.net' order by av.t.i asc" > avm.csv
```
where `avm` stands for `av` with `mx` pruning. This leaves us with only ~500k entries left. With one more figerprint we could do a [Wayback Machine CDX scanning](wayback-machine-cdx-scanning.md) scan.

Let's check that we still have most our hits in there:
```
grep -f <(awk -F, 'NR>1{print $2}' /home/ciro/bak/git/media/cia-2010-covert-communication-websites/hits.csv) avm.csv
```
At 267 hits we got 81, so all are still present.

secureserver is a hosting provider, we can see their blank page e.g. at: [https://web.archive.org/web/20110128152204/http://emmano.com/](https://web.archive.org/web/20110128152204/http://emmano.com/). [https://security.stackexchange.com/questions/12610/why-did-secureserver-net-godaddy-access-my-gmail-account/12616#12616](https://security.stackexchange.com/questions/12610/why-did-secureserver-net-godaddy-access-my-gmail-account/12616#12616) comments:

> secureserver.net is the name GoDaddy use as the reverse DNS for IP addresses used for dedicated/virtual server hosting

## ↑ Ancestors (15)

1. [DNS Census 2013](dns-census-2013.md)
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

## ← Incoming links (1)

- [2013 DNS census secureserver.net MX records intersection 2013 DNS Census virtual host cleanup](2013-dns-census-secureserver-net-mx-records-intersection-2013-dns-census-virtual-host-cleanup.md)
