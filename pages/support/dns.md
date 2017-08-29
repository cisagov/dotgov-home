---
title: Domain name system (DNS)
layout: docs
permalink: /support/dns/

sidenav: support
---

A Domain Name System (DNS) provider is an internet service that translates your domain name into an IP address. Your provider will give you a DNS name server to.


To learn more about the federal DNS policy, review the memorandum [M-08-23: Securing the Federal Government’s Domain Name System Infrastructure Memorandum](https://www.whitehouse.gov/sites/whitehouse.gov/files/omb/memoranda/2008/m08-23.pdf) or [download the PDF](https://www.dotgov.gov/dotgov-web/files/get_file?uuid=0d2b7be9-1c4d-423e-b3fa-6c9cd6310613&groupId=12665&action=get_file).

### How quickly will changes to my domain propagate throughout the internet?

Propagation depends on a variety of factors, such as caching and connectivity. The changes are usually effective by the next morning.

### Why can’t I access systems within my domain, but people outside can?

To speed up the entire DNS process, name servers will temporarily store IP addresses that they have found. This means that if someone in the office next to you visits [dotgov.gov](https://www.dotgov.gov) and you visit the site shortly afterwards, you receive the IP address from the local, temporary storage rather than through the root servers.

If your local name server is not expiring this temporary storage (called a cache), you could be getting incorrect IP addresses while people connected through different ISPs are getting the correct information. Please contact your ISP or local technical support for assistance.

### Where do I look for the authoritative .gov zone data?

The root servers (e.g., `a.root-server.net` - `j.root-server.net`) are the authoritative source of .gov information that is "live" on the internet.
