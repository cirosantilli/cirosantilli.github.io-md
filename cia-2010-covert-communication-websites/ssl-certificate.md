# SSL certificate

↑ **Parent:** [CGI comms](cgi-comms.md)

<a id="_6509"></a>
The [CGI comms](cgi-comms.md) websites contain the only occurrence of HTTPS, so it might open up the door for a certificate fingerprint as proposed by user joelcollinsdc at: [https://news.ycombinator.com/item?id=36280801](https://news.ycombinator.com/item?id=36280801)!

<a id="_6510"></a>
[https://crt.sh](https://crt.sh) appears to be a good way to look into this:<a id="_6511"></a>

<a id="_6512"></a>
- backstage.musical-fortune.net:<a id="_6513"></a>

  <a id="_6514"></a>
  - [https://crt.sh/?q=backstage.musical-fortune.net](https://crt.sh/?q=backstage.musical-fortune.net)
  <a id="_6515"></a>
  - [https://crt.sh/?id=1412501](https://crt.sh/?id=1412501)
<a id="_6516"></a>
- clients.smart-travel-consultant.com<a id="_6517"></a>

  <a id="_6518"></a>
  - [https://crt.sh/?q=clients.smart-travel-consultant.com](https://crt.sh/?q=clients.smart-travel-consultant.com)
  <a id="_6519"></a>
  - [https://crt.sh/?id=34910476](https://crt.sh/?id=34910476)
<a id="_6520"></a>
- members.it-proonline.com<a id="_6521"></a>

  <a id="_6522"></a>
  - [https://crt.sh/?q=members.it-proonline.com](https://crt.sh/?q=members.it-proonline.com)
  <a id="_6523"></a>
  - [https://crt.sh/?id=34166798](https://crt.sh/?id=34166798)
<a id="_6524"></a>
- members.metanewsdaily.com<a id="_6525"></a>

  <a id="_6526"></a>
  - [https://crt.sh/?q=members.metanewsdaily.com](https://crt.sh/?q=members.metanewsdaily.com)
  <a id="_6527"></a>
  - [https://crt.sh/?id=38512637](https://crt.sh/?id=38512637)
<a id="_6528"></a>
- miembros.todosperuahora.com<a id="_6529"></a>

  <a id="_6530"></a>
  - [https://crt.sh/?q=miembros.todosperuahora.com](https://crt.sh/?q=miembros.todosperuahora.com)
  <a id="_6531"></a>
  - [https://crt.sh/?id=34584314](https://crt.sh/?id=34584314)
<a id="_6532"></a>
- secure.altworldnews.com<a id="_6533"></a>

  <a id="_6534"></a>
  - [https://crt.sh/?q=secure.altworldnews.com](https://crt.sh/?q=secure.altworldnews.com)
  <a id="_6535"></a>
  - [https://crt.sh/?id=1326989](https://crt.sh/?id=1326989)
<a id="_6536"></a>
- secure.driversinternationalgolf.com<a id="_6537"></a>

  <a id="_6538"></a>
  - [https://crt.sh/?id=1855125](https://crt.sh/?id=1855125)
  <a id="_6539"></a>
  - [https://crt.sh/?id=34240083](https://crt.sh/?id=34240083)
<a id="_6540"></a>
- secure.freshtechonline.com<a id="_6541"></a>

  <a id="_6542"></a>
  - [https://crt.sh/?q=secure.freshtechonline.com](https://crt.sh/?q=secure.freshtechonline.com)
  <a id="_6543"></a>
  - [https://crt.sh/?id=34560115](https://crt.sh/?id=34560115)
<a id="_6544"></a>
- secure.globalnewsbulletin.com<a id="_6545"></a>

  <a id="_6546"></a>
  - [https://crt.sh/?q=secure.globalnewsbulletin.com](https://crt.sh/?q=secure.globalnewsbulletin.com)
  <a id="_6547"></a>
  - [https://crt.sh/?id=774803](https://crt.sh/?id=774803)
<a id="_6548"></a>
- secure.negativeaperture.com<a id="_6549"></a>

  <a id="_6550"></a>
  - [https://crt.sh/?q=secure.negativeaperture.com](https://crt.sh/?q=secure.negativeaperture.com)
  <a id="_6551"></a>
  - [https://crt.sh/?id=34547778](https://crt.sh/?id=34547778)
<a id="_6552"></a>
- secure.riskandrewardnews.com<a id="_6553"></a>

  <a id="_6554"></a>
  - [https://crt.sh/?id=33737677](https://crt.sh/?id=33737677)
  <a id="_6555"></a>
  - [https://crt.sh/?id=1140907](https://crt.sh/?id=1140907)
<a id="_6556"></a>
- secure.theworld-news.net
<a id="_6557"></a>
- secure.topbillingsite.com
<a id="_6558"></a>
- secure.worldnewsandent.com
<a id="_6559"></a>
- ssl.beyondnetworknews.com
<a id="_6560"></a>
- ssl.newtechfrontier.com
<a id="_6561"></a>
- www.businessexchangetoday.com
<a id="_6562"></a>
- heal.conquermstoday.com
They all appear to use either of:<a id="_6563"></a>

<a id="_6564"></a>
- Go Daddy
<a id="_6565"></a>
- Thawte DV SSL CA
<a id="_6566"></a>
- Starfield Technologies, Inc.

<a id="_6567"></a>
[https://crt.sh/?q=globalnewsbulletin.com](https://crt.sh/?q=globalnewsbulletin.com) has a hit to: [https://crt.sh/?id=774803](https://crt.sh/?id=774803). With login we can see: [https://search.censys.io/certificates/5078bce356a8f8590205ae45350b27f58f4ac04478ed47a389a55b539065cee8](https://search.censys.io/certificates/5078bce356a8f8590205ae45350b27f58f4ac04478ed47a389a55b539065cee8). Issued by [https://www.thawte.com/repository/index.html](https://www.thawte.com/repository/index.html). No hits for certificates with same public key: [https://search.censys.io/search?resource=certificates&q=parsed.subject_key_info.fingerprint_sha256%3A+714b4a3e8b2f555d230a92c943ced4f34b709b39ed590a6a230e520c273705af](https://search.censys.io/search?resource=certificates&q=parsed.subject_key_info.fingerprint_sha256%3A+714b4a3e8b2f555d230a92c943ced4f34b709b39ed590a6a230e520c273705af) or any other "same" queries though.

<a id="_6568"></a>
Let's try another one for secure.altworldnews.com: [https://search.censys.io/certificates/e88f8db87414401fd00728db39a7698d874dbe1ae9d88b01c675105fabf69b94](https://search.censys.io/certificates/e88f8db87414401fd00728db39a7698d874dbe1ae9d88b01c675105fabf69b94). Nope, no direct mega hits here either.

## ↑ Ancestors (16)

1. [CGI comms](cgi-comms.md)
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
