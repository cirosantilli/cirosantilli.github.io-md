<h1 id="overview-of-ciro-santilli-s-investigation">Overview of Ciro Santilli's investigation</h1>

↑ **Parent:** [Background](background.md)

<a id="_125"></a>
[Ciro Santilli](../ciro-santilli-split.md) hard heard about the 2018 Yahoo article around 2020 while [studying for his China campaign](../ciro-santilli-s-campaign-for-freedom-of-speech-in-china.md) because the websites had been used to take down the Chinese CIA network in China. He [even asked on Quora about it](https://www.quora.com/What-were-some-examples-of-the-websites-that-the-CIA-used-around-2010-as-a-communication-mechanism-for-its-spies-in-China-and-Iran-but-were-later-found-and-used-to-take-down-their-spy-networks), but there were no publicly known domains at the time to serve as a starting point. [Chris, Electrical Engineer and former Avionics Tech in the US Navy](https://www.quora.com/profile/Chris-2110), even replied suggesting that obviously the [CIA](../central-intelligence-agency.md) is so competent that it would never ever have its sites leaked like that:<a id="_126"></a>


> Seriously a dumb question.

<a id="image-seriously-a-dumb-question-quora-answer-by-chris-from-the-us-navy"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/CIA_2010_site_Quora_question_and_Chris_answer.png" alt="" height="550">

**[Figure 8](#image-seriously-a-dumb-question-quora-answer-by-chris-from-the-us-navy). "Seriously a dumb question" Quora answer by Chris from the US Navy**. [Source](https://www.quora.com/What-were-some-examples-of-the-websites-that-the-CIA-used-around-2010-as-a-communication-mechanism-for-its-spies-in-China-and-Iran-but-were-later-found-and-used-to-take-down-their-spy-networks/answer/Chris-2110).

<a id="_127"></a>
In 2023, one year after the Reuters article had been published, [Ciro Santilli](../ciro-santilli-split.md) was killing some time on [YouTube](../youtube.md) when he saw a curious video: [Video 3. "Compromised Comms by Darknet Diaries (2023)"](#video-compromised-comms-by-darknet-diaries-2023). As soon as he understood what it was about and that it was likely related to the previously undisclosed websites that he was interested in, he went on to read the [Reuters article](reuters-article.md) that the podcast pointed him to.

<a id="_128"></a>
Being a [half-arsed web developer himself](../ourbigbook-com-split.md), Ciro knows that the [attack surface](../attack-surface.md) of a website is about the [size of Texas](../size-of-texas-meme.md), and the potential for [fingerprinting](../fingerprinting-cybersecurity.md) is off the charts with so many bits and pieces sticking out. And given that there were at least 885 of them, surely we should be able to find a few more than nine, right?

<a id="_129"></a>
In particular, it is fun how these websites provide to anyone "live" examples of the [USA spying on its own allies](usa-spying-on-its-own-allies.md) in the form of [Wayback Machine](wayback-machine.md) archives.

<a id="_130"></a>
Given all of this, [Ciro knew he had to try](../ciro-santilli-s-naughty-projects.md) and find some of the domains himself using the newly available information! It was an irresistible real-life [capture the flag](../capture-the-flag-cybersecurity.md).

<a id="_131"></a>
Chris, get fucked.

<a id="video-compromised-comms-by-darknet-diaries-2023"></a>
**[Video 3](#video-compromised-comms-by-darknet-diaries-2023). Compromised Comms by Darknet Diaries (2023)** [Source](https://www.youtube.com/watch?v=uh_q02eefFM). <a id="_132"></a>
It was the [YouTube](../youtube.md) suggestion for this video that made [Ciro Santilli](../ciro-santilli-split.md) aware of the [Reuters article](reuters-article.md) almost one year after its publication, which kickstarted his research on the topic.

<a id="_133"></a>
Full podcast transcript: [https://darknetdiaries.com/transcript/75/](https://darknetdiaries.com/transcript/75/)

<a id="_134"></a>
[Ciro Santilli pinged the Podcast's host Jack Rhysider on Twitter](https://x.com/cirosantilli/status/1900278353065894324) and he ACK'ed which is cool, though he was skeptical about the strength of the fingerprints found, and didn't reply when clarification was offered. Perhaps the material is just not impactful enough for him to produce any new content based on it. Or also perhaps it comes too close to [sources and methods](../sources-and-methods.md) for his own good as a presumably American citizen.

---

<a id="_135"></a>
The first step was to try and obtain the domain names of [all nine websites that Reuters had highlighted](the-reuters-websites.md) as they had only given two domains explicitly.

<a id="_136"></a>
Thankfully however, either by carelessness or intentionally, this was easy to do by inspecting the address of the screenshots provided. For example, one of the URLs was:<a id="_137"></a>

```
https://www.reuters.com/investigates/special-report/assets/usa-spies-iran/screencap-activegaminginfo.com.jpg?v=192516290922
```
which corresponds to `activegaminginfo.com`.

<a id="image-inspecting-the-reuters-article-html-source-code"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/Reuters_CIA_website_article_image_urls_arrow.jpg" alt="" height="600">

**[Figure 9](#image-inspecting-the-reuters-article-html-source-code). Inspecting the Reuters article HTML source code**. [Source](https://www.reuters.com/investigates/special-report/usa-spies-iran/). The [Reuters article](reuters-article.md) only gave one URL explicitly: [iraniangoals.com](iraniangoals-com.md). But most others could be found by inspecting the HTML of the screenshots provided, except for [the Carson website](searching-for-carson.md).

<a id="_138"></a>
Once we had this, we were then able to inspect the websites on the [Wayback Machine](wayback-machine.md) to better understand possible [fingerprints](fingerprints.md) such as their [communication mechanism](communication-mechanism.md).

<a id="_139"></a>
The next step was to use our knowledge of the sequential IP flaw to look for more neighbor websites to the nine we knew of.

<a id="_140"></a>
This was not so easy to do because the websites are down and so it requires historical data. But for our luck we found [viewdns.info](viewdns-info.md) which allowed for 200 free historical queries (and they seem to have since removed this hard limit and moved to only throttling), leading to the discovery or some or our own new domains!

<a id="_141"></a>
This gave us a larger website sample size in the order of the tens, which allowed us to better grasp more of the possible different styles of website and have a much better idea of what a good [fingerprint](fingerprints.md) would look like.

<a id="image-viewdns-info-activegameinfo-com-domain-to-ip"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/viewdns.info_activegameinfo.com_domain_to_IP_arrow.png" alt="" height="550">

**[Figure 10](#image-viewdns-info-activegameinfo-com-domain-to-ip). viewdns.info `activegameinfo.com` domain to IP**. [Source](https://viewdns.info/iphistory/?domain=activegaminginfo.com).

<a id="image-viewdns-info-aroundthemiddleeast-com-ip-to-domain"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/viewdns.info_aroundthemiddleeast.com_IP_to_domain_arrow.png" alt="" height="550">

**[Figure 11](#image-viewdns-info-aroundthemiddleeast-com-ip-to-domain). viewdns.info `aroundthemiddleeast.com` IP to domain**. [Source](https://viewdns.info/reverseip/?host=66.175.106.140&t=1).

<a id="_142"></a>
The next major and difficult step would be to find new IP ranges.

<a id="_143"></a>
This was and still is a hacky heuristic process for us, but we've had the most success with the following methods:<a id="_144"></a>

<a id="_145"></a>
- step 1) get huge lists of historic domain names. The two most valuable sources so far have been:<a id="_146"></a>

  <a id="_147"></a>
  - [2013 DNS Census](dns-census-2013.md)
  <a id="_148"></a>
  - scraping [expired domain trackers](expired-domain-trackers.md)
<a id="_149"></a>
- step 2) filter the domain lists down somehow to a more manageable number of domains. The most successful heuristics have been:<a id="_150"></a>

  <a id="_151"></a>
  - for [2013 DNS Census](dns-census-2013.md) which has IPs, check that they are the only domain in a given IP, which was the case for the majority of CIA websites, but was already not so common for legitimate websites
  <a id="_152"></a>
  - they have the word `news` on the domain name, given that so many of the websites were fake news aggregators
<a id="_153"></a>
- step 3) search on Wayback machine if any of those filtered domains contain URL's that could be those of a [communication mechanism](communication-mechanism.md). In particular, we've used [a small army of Tor bots](wayback-machine-cdx-scanning-with-tor-parallelization.md) to overcome the Wayback Machine's IP throttling and greatly increase our checking capacity

<a id="image-dns-census-2013-website"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/dnscensus2013.neocities.org.png" alt="" height="574">

**[Figure 12](#image-dns-census-2013-website). DNS Census 2013 website**. [Source](https://dnscensus2013.neocities.org/). This source provided valuable historical domain to IP data. It was likely extracted with an illegal [botnet](../botnet.md). Data excerpt from the CSVs:<a id="_154"></a>

```
amazon.com,2012-02-01T21:33:36,72.21.194.1
amazon.com,2012-02-01T21:33:36,72.21.211.176
amazon.com,2013-10-02T19:03:39,72.21.194.212
amazon.com,2013-10-02T19:03:39,72.21.215.232
amazon.com.au,2012-02-10T08:03:38,207.171.166.22
amazon.com.au,2012-02-10T08:03:38,72.21.206.80
google.com,2012-01-28T05:33:40,74.125.159.103
google.com,2012-01-28T05:33:40,74.125.159.104
google.com,2013-10-02T19:02:35,74.125.239.41
google.com,2013-10-02T19:02:35,74.125.239.46
```

---

<a id="image-the-four-communication-mechanisms-used-by-the-cia-websites"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/cia-website-comms-methods.png" alt="" height="800">

**[Figure 13](#image-the-four-communication-mechanisms-used-by-the-cia-websites). The four communication mechanisms used by the CIA websites**. [Java](../java-programming-language.md) Applets, [Adobe Flash](../adobe-flash.md), [JavaScript](../javascript.md) and [HTTPS](../https.md)

<a id="image-expired-domain-names-by-day-2011"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/github.com_cirosantilli_expired-domain-names-by-day-2011.png" alt="" height="850">

**[Figure 14](#image-expired-domain-names-by-day-2011). Expired domain names by day 2011**. [Source](https://github.com/cirosantilli/expired-domain-names-by-day-2011). The scraping of [expired domain trackers](expired-domain-trackers.md) to Github was one of the positive outcomes of this project.

<a id="_155"></a>
Finally, at the very end of our pipeline, we were left with a a few hundred domains, and we just manually inspected them one by one as far as patience would allow it to confirm or discard them.

<a id="image-you-can-never-have-enough-wayback-machine-tabs-open"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/cia-2010-covert-communication-websites/archive-tabs.png" alt="" height="200">

**[Figure 15](#image-you-can-never-have-enough-wayback-machine-tabs-open). You can never have enough Wayback Machine tabs open**. This is how the end of the fingerprint pipeline looks like: as many tabs as you have the patience to go through one by one!

## ↑ Ancestors (13)

1. [Background](background.md)
2. [CIA 2010 covert communication websites](../cia-2010-covert-communication-websites-split.md)
3. [Central Intelligence Agency](../central-intelligence-agency.md)
4. [American intelligence agency](../american-intelligence-agency.md)
5. [United States Intelligence Community](../united-states-intelligence-community.md)
6. [Intelligence community](../intelligence-community.md)
7. [Secret service](../secret-service.md)
8. [Espionage](../espionage.md)
9. [War](../war.md)
10. [Social science](../social-science.md)
11. [Scientific method](../scientific-method.md)
12. [Science](../science-split.md)
13. [Ciro Santilli's Homepage](../split.md)
