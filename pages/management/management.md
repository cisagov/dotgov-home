---
title: Domain management
layout: docs
permalink: /management/

sidenav: management
subnav:
  - text: DNS FAQ
    href: '#dns-faq'
  - text: Points of contact FAQ
    href: '#points-of-contact-faq'
  - text: Renewals and deletions FAQ
    href: '#renewals-and-deletions-faq'
---
This section provides answers to questions about the domain management lifecycle.

We recommend you also review our [domain security best practices]({{ site.baseurl }}/management/security-best-practices/) page.

## DNS
The Domain Name System (DNS) is an internet service that translates your domain name into an IP address. This makes it possible for people to access your website by typing in the domain name instead of the website’s IP address.

.gov is a top-level domain (TLD). Other recognizable top-level domains include .com and .org. While many TLDs are *generic*, meaning anyone can obtain a domain name, .gov is a "sponsored" TLD, where the US Government acts as the sponsor for other US-based government organizations. These organizations are the only ones that can obtain a .gov domain.

* [Does the .gov TLD provide DNS services for .gov domains?](#does-the-gov-tld-provide-dns-services-for-gov-domains)
* [What are the DNS requirements for .gov domains?](#what-are-the-dns-requirements-for-gov-domains)
* [How quickly will changes to my domain propagate throughout the internet?](#how-quickly-will-changes-to-my-domain-propagate-throughout-the-internet)
* [How do I transfer my domain to a different agency?](#how-do-i-transfer-my-domain-to-a-different-agency)
* [Why can’t I access systems within my domain, but people outside can?](#why-cant-i-access-systems-within-my-domain-but-people-outside-can)
* [When can I define my DS record?](#when-can-i-define-my-ds-record)
* [Where do I look for the authoritative .gov zone data?](#where-do-i-look-for-the-authoritative-gov-zone-data)

## Points of contact
Keeping point of contact (POC) information from going stale ensures that only the appropriate people can make changes to your domain. It also makes it possible for DotGov to reach your organization when there's an issue.

* [How do I set up a new point of contact?](#how-do-i-set-up-a-new-point-of-contact)
* [How do I change a point of contact on the account?](#how-do-i-change-a-point-of-contact-on-the-account)
* [One of our contacts is no longer the right person to help manage our domain. How do I remove them from the account?](#one-of-our-contacts-is-no-longer-the-right-person-to-help-manage-our-domain-how-do-i-remove-them-from-the-account)
* [Can one person serve as multiple POCs on a single domain?](#can-one-person-serve-as-multiple-pocs-on-a-single-domain)
* [Can one person serve as a POC on multiple domains?](#can-one-person-serve-as-a-poc-on-multiple-domains)

## Renewals and deletions
Some surprises are wonderful. Discovering your domain is no longer on the internet won't be one of them.

* [How long is a .gov domain registered for?](#how-long-is-a-gov-domain-registered-for)
* [How much is the renewal fee for a .gov domain?](#how-much-is-the-renewal-fee-for-a-gov-domain)
* [Where can I get a list of my domains that are up for renewal?](#where-can-i-get-a-list-of-my-domains-that-are-up-for-renewal)
* [How do I delete my domain?](#how-do-i-delete-my-domain)
* [What happens if I do not renew my domain name?](#what-happens-if-i-do-not-renew-my-domain-name)

***

### DNS FAQ
#### Does the .gov TLD provide DNS services for .gov domains?

No. We manage the authoritative name servers for the .gov zone, and ensure `.gov` is propagated to the root name servers. We don't operate a for-government, managed DNS service.

Your internet service provider or technical support team can provide you with DNS name server addresses for your .gov domain, which often take the form of `ns1.example-name.com` and `ns2.example-name.com`.

#### What are the DNS requirements for .gov domains?

You must provide at least one primary and secondary name server.

You will not be able to specify an IP address for your name servers unless they are child name servers of the domain you’re trying to register or update.

#### How quickly will changes to my domain propagate throughout the internet?

Propagation depends on a variety of factors, such as caching and connectivity, but changes are usually effective within 24 hours.

If you’re planning to make critical changes to your name servers over the weekend, please [contact us]({{ site.baseurl }}/support/) before 5 p.m. on the prior Thursday to ensure the information propagates during weekend hours.

#### How do I transfer my domain to a different agency?

To transfer ownership of a domain name from one federal agency to another agency, two letters must be submitted to us: one from the *transferring* agency and one from the *accepting* agency.

##### Transferring agency letter

Start by copying and pasting the [Domain Transfer Letter Template]({{ site.baseurl }}/management/authorization-templates/transfers/) into a word processor.

The letter from the transferring agency must be on official agency letterhead and signed by the transferring agency CIO. The letter should formally request that the domain name be transferred to the new agency and should include the following information:

* Domain name to be transferred
* Both agency names (transferring agency and accepting agency)
* Current contacts and phone numbers (for the transferring agency)
* New contacts and phone numbers (for the accepting agency)

##### Accepting agency letter

Start by copying and pasting the [Domain Transfer Letter Template]({{ site.baseurl }}/management/authorization-templates/transfers/) into a word processor.

The letter from the accepting agency must be on official agency letterhead and must be signed by the accepting agency CIO.

This letter must specify the request for ownership of the domain name and should include the following information:

* Domain name to be transferred
* Both agency names (transferring agency and accepting agency)
* Current contacts and phone numbers (for the transferring agency)
* New contacts and phone numbers (for the accepting agency)
* New [domain name server]({{ site.baseurl }}/management#dns) addresses

##### Submit your request

Email your authorization letter to <registrar@dotgov.gov>, or fax a copy to 540-301-0160.

After we receive and verify both letters, the registry will be updated to reflect the transfer.

#### Why can’t I access systems within my domain, but people outside can?

To speed up the entire DNS process, name servers will temporarily store IP addresses that they’re found. This means that if someone in the office next to you visits [dotgov.gov](https://dotgov.gov) and you visit the site shortly afterwards, you will receive the IP address from local temporary storage instead of the root servers.

If your local name server is not expiring this temporary storage (or cache), you may get incorrect IP addresses while others connected through different ISPs get the correct information. Please contact your internet service provider or technical support team for assistance.

#### When can I define my DS record?

You can define Delegation of Signing (DS) records during registration or after the domain name is active. Before your DS records are published in the .gov zone, they will be tested and verified.

#### Where do I look for the authoritative .gov zone data?

The root servers (`[a-d].gov-servers.net`) are the authoritative source of .gov information that is "live" on the internet.

***

### Points of contact FAQ
#### How do I set up a new point of contact?

Request an account by sending an email to [registrar@dotgov.gov](mailto:registrar@dotgov.gov).

For a new domain request, the [authorization letter]({{ site.baseurl }}/registration/authorization-templates/) must also list the person’s name as a valid contact.

#### How do I change a point of contact on the account?

**If the point of contact is new** and doesn't have a account of the .gov registrar, they can create one in the [Account section of domains.dotgov.gov](https://domains.dotgov.gov/dotgov-web/user/register_registrant.xhtml?_m=2). We will then verity with another POC that they should have access.

**If the point of contact already has an account** on the .gov registrar, please provide the username for the account and which point of contact the user will replace. If the new point of contact does not currently have an account, please send the name and contact information so an account can be set up for them. For federal level domains the email must come from a government employee.

**If all three points of contact have left the domain**, the Authorizing Authority must sign a new authorization letter and assign 3 more points of contact.

Review our [account information guidelines]({{ site.baseurl }}/registration/requirements/#account-information) for more details.

#### One of our contacts is no longer the right person to help manage our domain. How do I remove them from the account?

If you are a contact on a domain that is undergoing the request process, you can update the POC with another. However, please ensure that you’re selecting an existing user.

If you are unable to update a point of contact with an existing user, please [contact us]({{ site.baseurl }}/support/).

#### Can one person serve as multiple POCs on a single domain?

No. All POCs on a domain must be **_unique_** to prevent a single point of failure. Each domain will require three (3) distinct POCs before submitting a request for approval or before submitting a renewal payment.

#### Can one person serve as a POC on multiple domains?

Yes.

***

### Renewals and deletions FAQ
#### How long is a .gov domain registered for?

Domains are registered for a one year period and can be renewed annually.

#### How much is the renewal fee for a .gov domain?

The cost of a .gov domain name is $400 per year. For more information, see our [Fees page]({{ site.baseurl }}/registration/fees/).

#### Where can I get a list of my domains that are up for renewal?

On [domains.dotgov.gov](https://domains.dotgov.gov), from the Home tab, click Fees**.

#### How do I delete my domain?

If you'd like to delete a domain name, [contact us](mailto:registrar@dotgov.gov) from an account registered to the domain. Also, you should ask your DNS provider to remove your domain's resource records.

Warning: once a domain is deleted, the entire [registration process]({{ site.baseurl }}/registration/) must be initiated to recover the domain. Be certain you want to delete a domain name before contacting us.

#### What happens if I do not renew my domain name?

Failure to submit payment does not result in the deletion of your domain. However, it may be placed in a hold status. When a domain name is held, it ceases resolving in DNS, making all services attached to the domain inaccessible by name resolution.

Your agency will be held financially responsible for all accrued registration fees under [Final Rule 41 CFR Part 102-173.35 and 102-173.40](https://www.ecfr.gov/cgi-bin/text-idx?mc=true&node=pt41.3.102_6173&rgn=div5#se41.3.102_6173_150), and you will not be able to register new domains until your account is up to date.

If you do not wish to renew, please contact us to [delete your domain]({{ site.baseurl }}/management/#what-happens-if-i-do-not-renew-my-domain-name).
