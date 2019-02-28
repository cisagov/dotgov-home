---
title: Domain security best practices
layout: docs
permalink: /management/security-best-practices/

sidenav: management
subnav:
  - text: Add a security contact
    href: '#add-a-security-contact'
  - text: Develop a VDP
    href: '#develop-a-vulnerability-disclosure-policy'
  - text: Preload your domain
    href: '#preload-your-domain'
  - text: Use DMARC
    href: '#use-dmarc'
  - text: Sign up for Cyber Hygiene
    href: '#sign-up-for-dhs-cyber-hygiene'
  - text: Join MS-ISAC
    href: '#join-ms-isac'
---
Domain management is about more than just [DNS]({{ site.baseurl }}/management#dns). It's also about ensuring a safe experience for your organization and your users.

## Add a security contact
Governments maintain legitimacy by keeping the trust of their citizens, and a security flaw found on a .gov host can erode that confidence. When government systems are exposed by weak configuration or technical vulnerability, the security of the information, the privacy of its citizen-owners, and the reputation of its custodians are at risk.

A _security contact_ can help you improve the resiliency of your digital services. Defining this contact is like **building a digital front door** for outsiders to report observed or suspected security issues at your domain. This could include notifications about compromised accounts, unsolicited email, routing problems, or reporting a potential vulnerability.

You can add a security contact at the [.gov registrar](https://domains.dotgov.gov), which will make it available in the [.gov WHOIS](https://domains.dotgov.gov/dotgov-web/registration/whois.xhtml) (including port 43) and our published [data]({{ site.baseurl }}/data/). You can change your security contact at any time; removing the contact withdraws it from WHOIS and our published data.

A security contact should be capable of evaluating or triaging security reports *for your entire domain*. We recommend using a team email address specifically for reports, and avoiding the use of an individual’s email address. A common address form is `security@<domain>` or `abuse@<domain>`.

We'd also recommend placing your security contact info on your website and in organizational communications. If people can’t find where to report something, having a security contact isn’t helpful!

## Develop a vulnerability disclosure policy
Consider having a vulnerability disclosure policy (VDP). A VDP outlines how your organization prefers to receive vulnerability reports and what you’ll do with them, the scope of systems covered by the policy, and legal authorization for those who follow the policy and report in good faith.

* The Department of Justice’s [Framework for a Vulnerability Disclosure Program for Online Systems](https://www.justice.gov/criminal-ccips/page/file/983996/download) provides helpful background for developing, instituting, and administering a policy.
* Model VDPs do exist in the government. VDPs from the [Department of Defense](https://hackerone.com/deptofdefense) and the [Technology Transformation Service at the General Services Administration](https://18f.gsa.gov/vulnerability-disclosure-policy/) are excellent examples.
* The National Telecommunications and Information Administration has [a VDP template](https://www.ntia.doc.gov/files/ntia/publications/ntia_vuln_disclosure_early_stage_template.pdf) which helps itemize key elements for a vulnerability disclosure program.

Once complete, put your vulnerability disclosure policy online. Some organizations include a link to their “security policy” near or with their privacy policy.

## Preload your domain
Web browsers allow domains to be "[preloaded](https://hstspreload.org)". This means that web browsers will always use HTTPS to connect with those websites. For example, [whitehouse.gov](https://whitehouse.gov) has been preloaded into all major web browsers. If you type `whitehouse.gov` into your browser and press **Enter** or click on a link without https in the protocol, your browser knows to connect to `https://whitehouse.gov` instead of `http://whitehouse.gov`, even though you didn't specifically tell it to. The same thing happens if you go to a subdomain of [whitehouse.gov](https://whitehouse.gov), like [petitions.whitehouse.gov](https://petitions.whitehouse.gov).

By preloading your domain, you can ensure your users will always make secure HTTPS connections to all of your websites. New domains can opt-in to preloading at registration.

See our [preloading page]({{ site.baseurl }}/management/preloading/) for more information.

## Use DMARC
It shouldn't be easy to impersonate the government. DMARC, "Domain-based Message Authentication, Reporting and Conformance", protects your reputation and good name by making it difficult for malicious actors to successfully spoof your domain in email.

Setting an enforced DMARC policy can take some effort, but once you do, email that *appears* to come from your domain but fails email authentication checks is rejected by the mail server and not delivered to users.

For domains that don't send mail, setting a strong DMARC policy ensures that no one receives mail that appears to come from your domain.

See the Department of Homeland Security's (DHS) guide to [DMARC and email authentication](https://cyber.dhs.gov/bod/18-01/#introduction-to-email-authentication).

## Sign up for DHS Cyber Hygiene
DHS operates a network and vulnerability scanning service for government organizations called "[Cyber Hygiene](https://www.us-cert.gov/resources/ncats)". Cyber Hygiene provides regular reports to help you secure your internet-facing systems from weak configuration and known vulnerabilities, and encourages the adoption of modern security best practices.

## Join MS-ISAC
For non-federal government organizations, consider joining the [Multi-State Information Sharing and Analysis Center](https://learn.cisecurity.org/ms-isac-registration). MS-ISAC has been [designated by DHS](https://www.dhs.gov/topic/cybersecurity-information-sharing) as the cybersecurity information sharing center for state, local, tribal, and territorial governments, and works to help ensure the resiliency of government systems.
