# Wayback Machine CDX scanning

↑ **Parent:** [Wayback Machine](wayback-machine.md)

<a id="_5984"></a>
The Wayback Machine has an endpoint to query cralwed pages called the CDX server. It is documented at: [https://github.com/internetarchive/wayback/blob/master/wayback-cdx-server/README.md](https://github.com/internetarchive/wayback/blob/master/wayback-cdx-server/README.md).

<a id="_5985"></a>
This allows to filter down 10 thousands of possible domains in a few hours. But 100s of thousands would be too much. This is because you have to query exactly one URL at a time, and they possibly rate limit IPs. But no IP blacklisting so far after several hours, so it's not that bad.

<a id="_5986"></a>
Once you have a heuristic to narrow down some domains, you can use this helper: [cia-2010-covert-communication-websites/cdx.sh](cia-2010-covert-communication-websites/cdx.sh) to drill them down from 10s of thousands down to hundreds or thousands.

<a id="_5987"></a>
We then post process the results of cdx.sh with [cia-2010-covert-communication-websites/cdx-post.sh](cia-2010-covert-communication-websites/cdx-post.sh) to drill them down from from thousands to dozens, and manually inspect everything.

<a id="_5988"></a>
From then on, you can just manually inspect for hist on your browser.

**Table of contents**

- [Wayback Machine CDX scanning with Tor parallelization](wayback-machine-cdx-scanning-with-tor-parallelization.md)
- [JS CDX scanning](js-cdx-scanning.md)

## ↑ Ancestors (15)

1. [Wayback Machine](wayback-machine.md)
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

## ← Incoming links (7)

- [2013 DNS census MX records](2013-dns-census-mx-records.md)
- [2013 DNS census NS records](2013-dns-census-ns-records.md)
- [2013 DNS census secureserver.net MX records intersection 2013 DNS Census virtual host cleanup](2013-dns-census-secureserver-net-mx-records-intersection-2013-dns-census-virtual-host-cleanup.md)
- [2013 DNS Census virtual host cleanup heuristic keyword searches](2013-dns-census-virtual-host-cleanup-heuristic-keyword-searches.md)
- [Non .com .net TLDs](non-com-net-tlds.md)
- [Secure subdomain search on 2013 DNS Census](secure-subdomain-search-on-2013-dns-census.md)
- [Wayback Machine](wayback-machine.md)
