# Facebook profile face dump

↑ **Parent:** [Ciro Santilli's naughty projects](ciro-santilli-s-naughty-projects.md)  
🏷️ **Tags:** [Ciro Santilli's data projects](ciro-santilli-s-data-projects.md)

In 2016 Ciro made a script downloaded [Facebook](facebook.md) profile pictures.

This was possible at the time without any login by using a 2010 profile ID dump from originally announced at: [https://blog.skullsecurity.org/2010/return-of-the-facebook-snatchers](https://blog.skullsecurity.org/2010/return-of-the-facebook-snatchers) since profile picture access was not authenticated.

The profile ID dump was downloadable through a [BitTorrent](bittorrent.md) named `fbdata.torrent` of about 2.8GB, mostly compressed. Doing:
```
find . -type f | xargs sha256sum | sha256sum
```
on Ubuntu 20.04 gives:
```
2c9a739c9c5495e38ebab81fc67411b7c6562f139dcb8619901a3f01230efdd5
```
This dump widely reported e.g. on [Hacker News](hacker-news.md) at: [https://news.ycombinator.com/item?id=1554558](https://news.ycombinator.com/item?id=1554558).

At some point however, Facebook finally started to require tokens to view public profile pictures, thus making such further collection impossible, e.g. as of 2021: [https://developers.facebook.com/docs/graph-api/reference/v9.0/user/picture](https://developers.facebook.com/docs/graph-api/reference/v9.0/user/picture) mentions:

> Querying a User ID (UID) now requires an access token.

This is also mentioned e.g. at: [https://stackoverflow.com/questions/11442442/get-user-profile-picture-by-id](https://stackoverflow.com/questions/11442442/get-user-profile-picture-by-id). This major privacy flaw was therefore finally addressed at some point, making it impossible to reproduce this project.

Ciro downloaded 10 thousand of those pictures, and did facial extraction with: [https://stackoverflow.com/questions/13211745/detect-face-then-autocrop-pictures/37501314#37501314](https://stackoverflow.com/questions/13211745/detect-face-then-autocrop-pictures/37501314#37501314)

He then created single a video by joining 10 thousand of those cropped faces which can be uploaded e.g. to [YouTube](youtube.md). Ciro later decided it was better to make those videos private however, as sooner later he'd lose his account for it.

[Companies](company-split.md) like [YouTube](youtube.md) blocking this kind of content is the type of thing that makes companies take longer to fix such gaping privacy issues, and is a bit like [security through obscurity](security-through-obscurity.md). A video makes it clear to everyone that there is a privacy issue very effectively. But people prefer to hide and look away, and then 99% of people who know nothing about tech get their privacy busted by actual criminals/government spies and never learn about it.

But now that Facebook finally fixed it, it's fine, no need for the video anymore.

## ↑ Ancestors (4)

1. [Ciro Santilli's naughty projects](ciro-santilli-s-naughty-projects.md)
2. [Ciro Santilli's projects](ciro-santilli-s-projects-split.md)
3. [Ciro Santilli](ciro-santilli-split.md)
4. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (1)

- [WhatsApp profile information is public by default](whatsapp-profile-information-is-public-by-default.md)
