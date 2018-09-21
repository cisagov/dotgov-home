---
title: DNS
layout: docs
permalink: /management/dns/

sidenav: management
---

The Domain Name System (DNS) is an internet service that translates your domain name into an IP address. This makes it possible for people to access your website by typing in the domain name instead of the website’s IP address.

.gov is a top-level domain (TLD). Other recognizable top-level domains include .com and .org. While many TLDs are *generic*, meaning anyone can obtain a domain name, .gov is a "sponsored" TLD, where the US Government acts as the sponsor for other US-based government organizations. These organizations are the only ones that can obtain a .gov domain.

### Does the DotGov Program provide DNS services for .gov domains?

No. We manage the authoritative name servers for the .gov zone, and ensure `.gov` is propagated to the root name servers. We don't operate a for-government, managed DNS service.

Your internet service provider or technical support team can provide you with DNS name server addresses for your .gov domain, which often take the form of `ns1.example-name.com` and `ns2.example-name.com`.

### What are the DNS requirements for .gov domains?

You must provide at least one primary and secondary name server.

You will not be able to specify an IP address for your name servers unless they are child name servers of the domain you’re trying to register or update.

### How quickly will changes to my domain propagate throughout the internet?

Propagation depends on a variety of factors, such as caching and connectivity, but changes are usually effective within 24 hours.

If you’re planning to make critical changes to your name servers over the weekend, please [contact us]({{ site.baseurl }}/support/) before 5 p.m. on the prior Thursday to ensure the information propagates during weekend hours.

### Why can’t I access systems within my domain, but people outside can?

To speed up the entire DNS process, name servers will temporarily store IP addresses that they’re found. This means that if someone in the office next to you visits [dotgov.gov](https://dotgov.gov) and you visit the site shortly afterwards, you will receive the IP address from local temporary storage instead of the root servers.

If your local name server is not expiring this temporary storage (or cache), you may get incorrect IP addresses while others connected through different ISPs get the correct information. Please contact your internet service provider or technical support team for assistance.

### When can I define my DS record?

You can define Delegation of Signing (DS) records during registration or after the domain name is active. Before your DS records are published in the .gov zone, they will be tested and verified.

### Where do I look for the authoritative .gov zone data?

The root servers (`[a-d].gov-servers.net`) are the authoritative source of .gov information that is "live" on the internet.
