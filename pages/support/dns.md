---
title: DNS
layout: docs
permalink: /support/dns/

sidenav: support
---

A Domain Name System (DNS) provider is an internet service that translates your domain name into an IP address. This makes it possible for people to access your website by typing in the domain name instead of the website’s IP address.

Your internet service provider or technical support team will give you DNS name server addresses for your .gov domain such as `ns1.company-name.com` and `ns2.company-name.com`.

### What are the DNS requirements for .gov domains?

You must provide at least one primary and secondary name server.

You will not be able to specify an IP address for your name servers unless they are child name servers of the domain you’re trying to register or update.

To learn more about the federal DNS policy, review the memorandum [M-08-23: Securing the Federal Government’s Domain Name System Infrastructure Memorandum](https://www.whitehouse.gov/sites/whitehouse.gov/files/omb/memoranda/2008/m08-23.pdf) or [download the PDF](https://www.dotgov.gov/dotgov-web/files/get_file?uuid=0d2b7be9-1c4d-423e-b3fa-6c9cd6310613&groupId=12665&action=get_file).

### How quickly will changes to my domain propagate throughout the internet?

Propagation depends on a variety of factors, such as caching and connectivity. The changes are usually effective within 24 hours.

If you’re planning to make critical changes to your name servers over the weekend, please [contact us]({{ site.baseurl }}/support/) before 5 p.m. on the prior Thursday to ensure the information propagates during weekend hours.

### Why can’t I access systems within my domain, but people outside can?

To speed up the entire DNS process, name servers will temporarily store IP addresses that they’re found. This means that if someone in the office next to you visits [dotgov.gov](https://www.dotgov.gov) and you visit the site shortly afterwards, you will receive the IP address from local temporary storage instead of the root servers.

If your local name server is not expiring this temporary storage (or cache), you may get incorrect IP addresses while people connected through different ISPs get the correct information. Please contact your internet service provider or technical support team for assistance.

### Where do I look for the authoritative .gov zone data?

The root servers (e.g., `a.root-server.net` - `j.root-server.net`) are the authoritative source of .gov information that is "live" on the internet.
