# SSL certificate

↑ **Parent:** [CGI comms](cgi-comms.md)

The [CGI comms](cgi-comms.md) websites contain the only occurrence of HTTPS, so it might open up the door for a certificate fingerprint as proposed by user joelcollinsdc at: [https://news.ycombinator.com/item?id=36280801](https://news.ycombinator.com/item?id=36280801)!

[https://crt.sh](https://crt.sh) appears to be a good way to look into this:
- backstage.musical-fortune.net:
  - [https://crt.sh/?q=backstage.musical-fortune.net](https://crt.sh/?q=backstage.musical-fortune.net)
  - [https://crt.sh/?id=1412501](https://crt.sh/?id=1412501)
- clients.smart-travel-consultant.com
  - [https://crt.sh/?q=clients.smart-travel-consultant.com](https://crt.sh/?q=clients.smart-travel-consultant.com)
  - [https://crt.sh/?id=34910476](https://crt.sh/?id=34910476)
- members.it-proonline.com
  - [https://crt.sh/?q=members.it-proonline.com](https://crt.sh/?q=members.it-proonline.com)
  - [https://crt.sh/?id=34166798](https://crt.sh/?id=34166798)
- members.metanewsdaily.com
  - [https://crt.sh/?q=members.metanewsdaily.com](https://crt.sh/?q=members.metanewsdaily.com)
  - [https://crt.sh/?id=38512637](https://crt.sh/?id=38512637)
- miembros.todosperuahora.com
  - [https://crt.sh/?q=miembros.todosperuahora.com](https://crt.sh/?q=miembros.todosperuahora.com)
  - [https://crt.sh/?id=34584314](https://crt.sh/?id=34584314)
- secure.altworldnews.com
  - [https://crt.sh/?q=secure.altworldnews.com](https://crt.sh/?q=secure.altworldnews.com)
  - [https://crt.sh/?id=1326989](https://crt.sh/?id=1326989)
- secure.driversinternationalgolf.com
  - [https://crt.sh/?id=1855125](https://crt.sh/?id=1855125)
  - [https://crt.sh/?id=34240083](https://crt.sh/?id=34240083)
- secure.freshtechonline.com
  - [https://crt.sh/?q=secure.freshtechonline.com](https://crt.sh/?q=secure.freshtechonline.com)
  - [https://crt.sh/?id=34560115](https://crt.sh/?id=34560115)
- secure.globalnewsbulletin.com
  - [https://crt.sh/?q=secure.globalnewsbulletin.com](https://crt.sh/?q=secure.globalnewsbulletin.com)
  - [https://crt.sh/?id=774803](https://crt.sh/?id=774803)
- secure.negativeaperture.com
  - [https://crt.sh/?q=secure.negativeaperture.com](https://crt.sh/?q=secure.negativeaperture.com)
  - [https://crt.sh/?id=34547778](https://crt.sh/?id=34547778)
- secure.riskandrewardnews.com
  - [https://crt.sh/?id=33737677](https://crt.sh/?id=33737677)
  - [https://crt.sh/?id=1140907](https://crt.sh/?id=1140907)
- secure.theworld-news.net
- secure.topbillingsite.com
- secure.worldnewsandent.com
- ssl.beyondnetworknews.com
- ssl.newtechfrontier.com
- www.businessexchangetoday.com
- heal.conquermstoday.com
They all appear to use either of:
- Go Daddy
- Thawte DV SSL CA
- Starfield Technologies, Inc.

[https://crt.sh/?q=globalnewsbulletin.com](https://crt.sh/?q=globalnewsbulletin.com) has a hit to: [https://crt.sh/?id=774803](https://crt.sh/?id=774803). With login we can see: [https://search.censys.io/certificates/5078bce356a8f8590205ae45350b27f58f4ac04478ed47a389a55b539065cee8](https://search.censys.io/certificates/5078bce356a8f8590205ae45350b27f58f4ac04478ed47a389a55b539065cee8). Issued by [https://www.thawte.com/repository/index.html](https://www.thawte.com/repository/index.html). No hits for certificates with same public key: [https://search.censys.io/search?resource=certificates&q=parsed.subject_key_info.fingerprint_sha256%3A+714b4a3e8b2f555d230a92c943ced4f34b709b39ed590a6a230e520c273705af](https://search.censys.io/search?resource=certificates&q=parsed.subject_key_info.fingerprint_sha256%3A+714b4a3e8b2f555d230a92c943ced4f34b709b39ed590a6a230e520c273705af) or any other "same" queries though.

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
