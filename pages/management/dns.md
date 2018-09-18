---
title: DNS
layout: docs
permalink: /management/dns/

sidenav: management
---

A Domain Name System (DNS) provider is an internet service that translates your domain name into an IP address. This makes it possible for people to access your website by typing in the domain name instead of the website’s IP address.

Your internet service provider or technical support team will give you DNS name server addresses for your .gov domain such as `ns1.example-name.com` and `ns2.example-name.com`.

### What are the DNS requirements for .gov domains?

You must provide at least one primary and secondary name server.

You will not be able to specify an IP address for your name servers unless they are child name servers of the domain you’re trying to register or update.

### How quickly will changes to my domain propagate throughout the internet?

Propagation depends on a variety of factors, such as caching and connectivity. The changes are usually effective within 24 hours.

If you’re planning to make critical changes to your name servers over the weekend, please [contact us]({{ site.baseurl }}/support/) before 5 p.m. on the prior Thursday to ensure the information propagates during weekend hours.

### Why can’t I access systems within my domain, but people outside can?

To speed up the entire DNS process, name servers will temporarily store IP addresses that they’re found. This means that if someone in the office next to you visits [dotgov.gov](https://domains.dotgov.gov) and you visit the site shortly afterwards, you will receive the IP address from local temporary storage instead of the root servers.

If your local name server is not expiring this temporary storage (or cache), you may get incorrect IP addresses while people connected through different ISPs get the correct information. Please contact your internet service provider or technical support team for assistance.

### When can I define my DS record?

You can define Delegation of Signing (DS) records during registration or after the domain name is active. Before your DS records are published in the .gov zone, they will be tested and verified.

### Where do I look for the authoritative .gov zone data?

The root servers (`[a-d].gov-servers.net`) are the authoritative source of .gov information that is "live" on the internet.
