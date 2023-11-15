---
redirect_to: /
title: HSTS preloading
layout: docs
permalink: /management/preloading/
sidenav: support
subnav:
  - text: Introduction
    href: '#introduction'
  - text: Certificates
    href: '#certificates'
---

## Introduction

The DotGov Program has begun automatically implementing the preloading of HTTP Strict Transport Security records ("HSTS Preloading") for newly issued **federal executive branch** .gov domains.

Newly registered domains from outside the federal executive branch can also **opt-in** to preloading.

### What is HTTPS and why is it important?

HTTPS (Hypertext Transfer Protocol Secure) is a protocol that gives users a level of security and privacy when connecting to websites and web services.

The internet's fundamental design means that both visitors and website owners have very little control over where communications will travel, or whose devices will carry that communication. To ensure secure communication across the internet, traffic must be encrypted all the way from visitors' devices to the website owners' devices -- and that's exactly what HTTPS does. Without HTTPS, hostile networks can inject malware or tracking beacons, or otherwise monitor or change visitor interactions online.

Without HTTPS, website visitors have no guarantees about what happens as they browse the web. Without HTTPS, a visitor's communication with a website can be modified or monitored by anyone or anything "between" them and the website they're visiting. The attacker could be someone using that coffee shop WiFi (or the coffee shop itself), or it could be someone who's hacked an old, out-of-date load balancer which website traffic is flowing through on its way around the internet.

### What is HSTS/HTTPS preloading?

Today, web browsers allow websites to be "preloaded" as HSTS-only. This means that web browsers will always use HTTPS to connect with those websites. For example, [whitehouse.gov](https://whitehouse.gov) has been preloaded into all major web browsers. If you type `whitehouse.gov` into your browser and press **Enter** or click on a link without https in the protocol, your browser knows to connect to `https://whitehouse.gov` instead of `http://whitehouse.gov`, even though you didn't specifically tell it to. The same thing happens if you go to a subdomain of [whitehouse.gov](https://whitehouse.gov), like [petitions.whitehouse.gov](https://petitions.whitehouse.gov).

By preloading [whitehouse.gov](https://whitehouse.gov), the site owners have ensured that browsers will always make secure HTTPS connections to all of its websites.

### Will automatic preloading affect all .gov domains?

**No.** All the following criteria must be met for domains (and associated websites) to be affected:

* The .gov domain belongs to an agency of the **federal government’s executive branch**; and
* The .gov domain was **registered for the first time on a date after May 15, 2017**; and
* The .gov domain is **on the preload list.**

### Will automatic preloading affect non-executive branch federal domains and websites?

**No.** If a .gov domain belongs to the federal government's legislative or judicial branches, it will not be affected by HTTPS preloading. However, new domains from these branches can opt-in to preloading at the time of registration.

### Will automatic preloading affect state or local government, or Native tribe domains and websites?

**No.** If a .gov domain belongs to a native tribe, state, or local government entity, it will not be affected by HTTPS preloading. However, new domains from these government entities can opt-in to preloading at the time of registration.

### Will automatic preloading affect domains registered before May 15, 2017?

**No.** If a .gov domain was registered before May 15, 2017, it will not be affected by automatic HTTPS preloading.

Note: It's possible for any .gov domain owner to preload their own domain. Some domains not meeting the above criteria have been preloaded through the domain owner's direct action, and could be affected. This service only applies to identifying domains preloaded through the DotGov Program's action, rather than the domain owner's action.

### How will HSTS preloading affect .gov domain visitors?

If a .gov domain is affected and preloaded, any websites hosted on that domain or any of its subdomains will be affected in the following two ways:

1. Supporting web browsers will automatically redirect HTTP requests to the HTTPS version of the same URL, for any URL on that domain or its subdomains.

    * To illustrate, if [example.gov](https://example.gov) is preloaded, then attempting to visit `http://example.gov/about/` will redirect the user to `https://example.gov/about/`.
    * Similarly, attempting to visit `http://history.example.gov/faq/` will redirect the user to `https://history.example.gov/faq/`.
    * This will happen no matter how the domain owner has configured their web server. In fact, this will happen even if the domain owner has no web server configured at all.

2. Supporting web browsers **will not** allow website visitors to click through any certificate warnings a user might encounter on a website on the affected .gov domain or any of its subdomains. This means that affected domain owners must treat a certificate configuration issue as equivalent to downtime. Visitors cannot be asked to click through certificate warnings to use the website.

### How can I verify whether a .gov domain is preloaded?

To verify whether a domain is affected by HSTS preloading:

1. Check Chrome's HSTS Preload list form at [https://hstspreload.org](https://hstspreload.org). Enter the domain and click **Check status and eligibility**. For example, if you enter `whitehouse.gov` you'll get a message saying "Status: whitehouse.gov is currently preloaded."

2. View the [Chrome source code](https://chromium.googlesource.com/chromium/src/net/+/refs/heads/master/http/transport_security_state_static.json). This is a large file and is in JSON format, but is the authoritative source of whether the domain is preloaded in Chrome. Other browsers pull from this list, so it should be valid for browsers other than Chrome.

## Certificates

### Where can I obtain a web certificate for my .gov website?

To obtain new certificates, agencies should make use of any publicly trusted certificate authority. In general, these are commercial or non-profit entities, as the U.S. government does not operate a certificate authority trusted by all modern browsers.

GSA encourages .gov domain owners to obtain [low cost or free certificates](https://https.cio.gov/certificates/#what-kind-of-certificate-should-i-get-for-my-domain). More expensive certificates generally do not offer more security value to service owners, and automatic deployment of free certificates can significantly improve service owners' security posture. For more information, see: [https.cio.gov/certificates/](https://https.cio.gov/certificates/).

### How do SSL providers verify a certificate for a .gov domain?

SSL certificate providers can contact us at 1-877-734-4688 to verify administrative contact information before issuing an SSL Certificate for a .gov domain name.

Due to security reasons, this can only be provided verbally. The information cannot be provided in writing.

### How should I address web certificate issues that could prevent visitors from viewing web content?

If visitors experience certificate issues on a website the agency intends for public use, and that domain is affected by preloading, then **the federal agency must take action** to fix the issue. Visitors will not be able to click through the certificate warning.

Common certificate issues include:

#### The certificate has expired.

Certificates are valid for a certain length of time from issuance, and once they expire they will no longer be trusted by web browsers.

**Solution:** Renew and redeploy the certificate.

#### The certificate is served with an incomplete certificate chain.

This issue can be difficult for non-technical visitors to diagnose, and may appear to affected visitors as if the certificate is not issued by a trusted authority (Note: only some visitors may be affected -- for example, this commonly affects mobile visitors but not desktop visitors).

**Solution:** Update the server configuration to also include the intermediate certificate used by the certificate authority from which the original certificate was issued. For more information, see [https://https.cio.gov/technical-guidelines/#a-complete-certificate-chain](https://https.cio.gov/technical-guidelines/#a-complete-certificate-chain)

#### The certificate is not valid for the given domain name.

Certificates are only valid for the exact specific domain name shown in the URL bar.

**Solution:** The agency must issue a new certificate valid for that domain name, or reissue an existing certificate to add the domain name to its list of valid domain names. Examples of this include:

* A certificate valid for [example.gov](https://example.gov) **will not** work for [history.example.gov](https://history.example.gov).
* A certificate valid for [example.gov](https://example.gov) **will not** work for [www.example.gov](https://www.example.gov).
* A certificate valid for [www.example.gov](https://www.example.gov) **will not** work for [example.gov](https://example.gov).
* A certificate valid for `*.example.gov` **will not** work for [example.gov](https://example.gov). (This certificate **will** be valid for [www.example.gov](https://www.example.gov)).

#### The certificate is not issued by a trusted authority.

Visitors use browsers and operating systems that only trust a certain set of "certificate authorities," and many visitors from the general public use browsers and operating systems that do not trust government-issued certificates. For websites that serve a public audience, agencies must use commercially issued certificates.

**Solution:** Replace the certificate with one from a widely trusted certificate authority. For more information, see [https.cio.gov/certificates/](https://https.cio.gov/certificates/).
