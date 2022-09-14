---
title: What to Think About When You're <i>Thinking About</i> Moving to .gov
layout: docs
permalink: /help/what-to-think-about-thinking-about-moving-to-gov/
sidenav: help
subnav:
  - text: Technological tasks
    href: '#technological-tasks'
  - text: Branding
    href: '#branding'
  - text: Public communication
    href: '#public-communication'
---

Most government organizations that want to register a .gov domain name have already established an online home -- a website or email address -- at a non-.gov domain like .org or .us. We have other documentation to help you [request a .gov domain]({{ site.baseurl }}/registration/), but the goal of this page is to help your organization think about what steps are necessary to *actually transition* to a .gov domain.

Moving to .gov is not solely a technical task, although there are some important technological considerations. Given the diversity of organizational types, authorities held, constituents, and underlying IT infrastructure of governments across the nation, the outline below is somewhat generic. This content is best used as a conversation piece between your government organization's *IT professionals* (e.g., folks responsible for DNS, web, network, information security), *public affairs team* (people responsible for public communication online, in print, or elsewhere), and *staff or executives responsible for administration*. It should generate ideas so you can develop a transition plan.

## Technological tasks

Many organizations take advantage of a domain update to upgrade certain infrastructure and/or move it to the cloud. Review what your needs and opportunities are.

### Domains and Domain Name System (DNS)

  - Plan to maintain your current non-.gov domain registration(s) in perpetuity: you don\'t want your old domains to ever fall to other hands.

  - .gov [doesn't provide hosted DNS services]({{ site.baseurl }}/help/#do-you-provide-dns-hosting-for-gov-domains), so you will need to operate or manage authoritative DNS for your domain. If you're coming from a non-.gov domain, this may be a new requirement. You can manage your own DNS servers or host your domain with a third-party; "DNS hosting" is a good search term to find providers. Options range in price but are typically only a few dollars per month. Some local internet service providers (ISPs) or technology service providers may also offer DNS hosting.

### Web redirects and URLs

  - Review your site for documents that link to your prior domain name. You may also have images where the domain is embedded.

  - Use HTTP redirects from your old domain to your new domain. This lets people with bookmarks or legacy links be directed to your new online home. Use [HTTP 302s](https://en.wikipedia.org/wiki/HTTP_302) for testing, and [HTTP 301s](https://en.wikipedia.org/wiki/HTTP_301) to signal to search engines a permanent move.

    - If you're using your old domain for web redirects, plan to keep the TLS certificate current for your older domain, too.

    - You may want to use this time to archive content that is no longer relevant or update it to make it current.

### Email

  - Moving to .gov in your email depends on your current infrastructure or provider, but most mail services support aliases so that mail sent to a prior domain name is still delivered. Search for the documentation of your mail server/provider along with "custom domain".

  - If you're currently using a free email address (@gmail.com, @outlook.com, @icloud.com, @yahoo.com), you'll need to pay for an email service or manage your own email servers in order to use a .gov domain for email.

### Identity

  - Organizations often use email addresses (which include a domain name) as unique identifiers for accounts. This can occur on internal systems (like a directory service) or with external services (like software-as-a-service accounts). If you bind user identity into a token that uses a domain name, review the documentation for your software to evaluate the steps needed to use a different address.

### Security

  - Each of the above topics has its own security impact. As an enterprise, you can improve security by reviewing our [domain security best practices]({{ site.baseurl }}/help/security-best-practices/).

Keep in mind that you don't need to transition everything at once! Many have found success doing the simple (or most pressing) things first and tackling more complicated tasks in time.

## Branding

Domain names show up in more places than just online. They're printed on paper products (like letterhead or business cards), vehicles (painted on or included on license plates), or public signage (advertising, road signs). These products typically have their own refresh period. Consider the right time to update each.

## Public communication

Many government organizations share the fact that they\'ve transitioned to a .gov domain name via press release or social media, sometimes before and after the change. These events regularly get picked up online or in traditional media outlets, amplifying your ability to tell the public.

Here are some examples of government organizations communicating publicly about their .gov move:

### Press release

- [Dallas, TX](https://www.dallascitynews.net/new-dallas-gov-domain-name) – dallas.gov
- [Colorado Secretary of State](https://www.sos.state.co.us/pubs/newsRoom/pressReleases/2021/PR20210825Domain.html) – coloradosos.gov
- [Larimer County, CO](https://www.larimer.gov/spotlights/2022/04/27/why-we-are-moving-larimergov) – larimer.gov
- [Hillsborough County, FL](https://www.votehillsborough.gov/Portals/Hillsborough/Documents/Press%20Releases/2021%20Press%20Releases/New%20VoteHillsborough%20Web%20Address.pdf?ver=GXgWNkiPHgjV51lfuXIb2Q%3d%3d) - votehillsborough.gov

### Social media

- [@COSecofState](https://twitter.com/COSecofState/status/1430583619865616385) – coloradosos.gov
- [@ArlingtonVotes](https://twitter.com/ArlingtonVotes/status/1554158281135898625) – vote.arlingtonva.gov
- [@bouldercounty](https://twitter.com/bouldercounty/status/1545070920452096001) – bouldercounty.gov
- [@Carrboro, NC](https://twitter.com/CarrboroGov/status/1483845242071752711) – carrboronc.gov

### Print and radio

- [Abilene Reflector-Chronicle](https://www.abilene-rc.com/news/county-website-and-emails-change-from-org-to-gov/article_cc417aaa-5ceb-11ec-80db-3b467491a717.html) – dickinsontexas.gov
- [Missourian](https://www.emissourian.com/local_news/union-moving-to-gov-domain-name/article_4bc2bf98-62b2-11ec-bde9-e70c55cd93c4.html) – on UnionMissouri.gov
- [WJBC, AM 1230](https://www.wjbc.com/2022/04/29/bloomington-normal-to-update-website-domains/) on bloomingtonil.gov

If you announce your transition on social media, tag us at [@cisagov](https://twitter.com/cisagov). We'd love to help you get the word out!

---

Is there anything we've missed? Something you've found work well in your organization? You can let us know at <dotgov@cisa.dhs.gov> or suggest an edit on this page.
