<h1 id="dns-configuration-of-ciro-santilli-s-website">DNS configuration of Ciro Santilli's website</h1>

↑ **Parent:** [cirosantilli.com](cirosantilli-com-split.md)

AKA how this [GitHub page](https://github.com/cirosantilli/cirosantilli.github.io) gets served under the domain: [https://cirosantilli.com](https://cirosantilli.com)

Ciro only touches this very rarely, and always forgets and go into great pain whenever a change needs to done, so it is important to document it.

The last change was of 2019-07-07, when Ciro moved from the www subdomain [https://www.cirosantilli.com](https://www.cirosantilli.com) to the APEX [https://cirosantilli.com](https://cirosantilli.com). A redirect is setup from the www subdomain to APEX.

[GoDaddy](https://en.wikipedia.org/wiki/GoDaddy) DNS entries:

```
Type    Name    Value                   TTL
A       @       185.199.108.153         1 Hour
A       @       185.199.109.153         1 Hour
A       @       185.199.110.153         1 Hour
A       @       185.199.111.153         1 Hour
CNAME   www     cirosantilli.github.io  1 Hour
```

Moved cirosantilli.com to Porkbun 2022-02, unfortunatly records were not automatically updated and domain went down for a bit, upadded to new entries for IPv6 as well which are not documented by GitHub:

```
TYPE 	HOST	ANSWER	TTL	PRIORITY	OPTIONS
A	cirosantilli.com	185.199.108.153	600
A	cirosantilli.com	185.199.109.153	600
A	cirosantilli.com	185.199.110.153	600
A	cirosantilli.com	185.199.111.153	600
AAAA	cirosantilli.com	2606:50c0:8000::153	600
AAAA	cirosantilli.com	2606:50c0:8001::153	600
AAAA	cirosantilli.com	2606:50c0:8002::153	600
AAAA	cirosantilli.com	2606:50c0:8003::153	600
CNAME	www.cirosantilli.com	cirosantilli.github.io	600
```

where the IPs are obtained from: [https://help.github.com/en/articles/setting-up-an-apex-domain#configuring-a-records-with-your-dns-provider](https://help.github.com/en/articles/setting-up-an-apex-domain#configuring-a-records-with-your-dns-provider) ([archive](http://web.archive.org/web/20190707085154/https://help.github.com/en/articles/setting-up-an-apex-domain#configuring-a-records-with-your-dns-provider)).

Under [https://github.com/cirosantilli/cirosantilli.github.io/settings](https://github.com/cirosantilli/cirosantilli.github.io/settings)

- Custom domain: `cirosantilli.com`
- Enforce HTTPS: checked

And the CNAME file is tracked in this repository: [CNAME](CNAME).

## ↑ Ancestors (3)

1. [cirosantilli.com](cirosantilli-com-split.md)
2. [Ciro Santilli](ciro-santilli-split.md)
3. [Ciro Santilli's Homepage](split.md)
