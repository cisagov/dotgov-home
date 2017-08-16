---
title: Support
layout: docs
permalink: /technical-support/
top: true
---

## Technical support

#### Why can't I access systems within my domain, but people outside can?

To speed up the entire DNS process, name servers will temporarily store IP addresses that they have found. This means that if someone in the office next to you visits [www.dotgov.gov](https://www.dotgov.gov) and then you visit the site shortly afterwards, you receive the IP address from the local, temporary storage rather than through the root servers. If you or your ISP's local name server is not "expiring" this temporary storage (called a cache), you could be getting incorrect IP addresses while people connected through different ISPs are getting the correct information. Please contact your ISP or local technical support for assistance.

#### Where do I look for the authoritative .gov zone data?

The root servers (e.g., a.root-server.net - j.root-server.net) are the authoritative source of .gov information that is "live" on the Internet.
