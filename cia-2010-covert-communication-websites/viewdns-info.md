<h1 id="viewdns-info">viewdns.info</h1>

↑ **Parent:** [Data sources](data-sources.md)  
🏷️ **Tags:** [Data as a service](../data-as-a-service.md)

<a id="_6015"></a>
Accounts used so far: 6 (1500 reverse IP checks).

<a id="_6016"></a>
Their historic DNS and reverse DNS info was very valuable, and served as Ciro's the initial entry point to finding hits in the IP ranges given by Reuters.

<a id="_6017"></a>
Generic information about the website not specific on this project will be stored at: [Section "viewdns.info"](../viewdns-info.md).

<a id="_6018"></a>
Since this source is so scarce and valuable, we have been quite careful to note down all the domain and IP ranges that have been explored.

<a id="_6019"></a>
At [https://news.ycombinator.com/item?id=38496244](https://news.ycombinator.com/item?id=38496244), the creator of the viewdns.info, "Hughesey", also stated that he'd able to give some free credits for public research projects such as this one. This would have saved up going to quite a few Cafes to get those sweet extra IPs! But it was more fun in hardmode, no doubt.

<a id="_6020"></a>
We do API access to IP ranges with this simple helper: [cia-2010-covert-communication-websites/viewdns-info.sh](cia-2010-covert-communication-websites/viewdns-info.sh), usage:<a id="_6021"></a>

```
./viewdns-info.sh <apikey> <start-ipv-address> <end-ipv-address>
```
e.g.:<a id="_6022"></a>

```
./viewdns-info.sh 8b890b00b17ed2d66bbed878d51200b58d43d014 66.45.179.187 66.45.179.210
```

<a id="_6023"></a>
For domain to IP queries from the API you should use "iphistory" [https://viewdns.info/api/docs/ip-history.php](https://viewdns.info/api/docs/ip-history.php):<a id="_6024"></a>

```
curl 'https://api.viewdns.info/iphistory/?domain=todaysengineering.com&apikey=$APIKEY&output=json'
```

<a id="_6025"></a>
Just beware of the [viewdns.info reverse IP bug](../viewdns-info-reverse-ip-bug.md), that really sucks and led to us missing a ton of domains.

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

## ← Incoming links (8)

- [2013 DNS Census virtual host cleanup](2013-dns-census-virtual-host-cleanup.md)
- [Hits with nearby IP hits](hits-with-nearby-ip-hits.md)
- [Hits without nearby IP hits](hits-without-nearby-ip-hits.md)
- [Ipinf.ru](ipinf-ru.md)
- [Overview of Ciro Santilli's investigation](overview-of-ciro-santilli-s-investigation.md)
- [Possible hits](possible-hits.md)
- [Securitytrails.com](securitytrails-com.md)
- [Viewdns.info](viewdns-info.md)
