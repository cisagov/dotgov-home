---
title: Common registration questions
layout: docs
permalink: /registration/common-questions/

sidenav: registration
subnav:

  - text: Domain authorization FAQ
    href: '#domain-authorization-faq'
  - text: DNS FAQ
    href: '#dns-faq'
---


## Domain requirements and authorization
* [What are the requirements for a domain's points of contact?](#what-are-the-requirements-for-a-domains-points-of-contact)
* [How do I request an exception to the naming requirements?](#how-do-i-request-an-exception-to-the-naming-requirements)
* [My authorizing authority won’t sign an authorization letter. What do I do now?](#my-authorizing-authority-wont-sign-an-authorization-letter-what-do-i-do-now)
* [How often do I need to renew my domain name?](#how-often-do-i-need-to-renew-my-domain-name)
* [What happens if I do not renew my domain name?](#what-happens-if-i-do-not-renew-my-domain-name)

## DNS
* [What are the valid characters for a domain name and how long can it be?](#what-are-the-valid-characters-for-a-domain-name-and-how-long-can-it-be)
* [Why won’t my domain work after updating the registration with actual name servers?](#why-wont-my-domain-work-after-updating-the-registration-with-actual-name-servers)

***

### Domain authorization FAQ
#### What are the requirements for a domain's points of contact?

1. **Administrative contact**: someone from the signatory’s office that will approve the content. This person must be a government employee.

2. **Technical contact**: a developer or administrator, often responsible for managing [DNS]({{ site.baseurl }}/management/dns/) and securing the infrastructure.

3. **Security contact**: a [security contact]({{ site.baseurl }}/management/security-best-practices/#add-a-security-contact) is a recommended practice, and can be added to allow outsiders to report observed or suspected security issues at your domain. *Security contact details are made public.*

We don't currently allow a single point of contact to be re-used for more than one role. An exception is made should you choose to use a personal email address for a security contact. We recommend using an alias, like `security@<domain>`.

Administrative and technical contacts have the ability to access the .gov registrar or make changes to DNS.

#### How do I request an exception to the naming requirements?

Exceptions to the [naming requirements]({{ site.baseurl }}/registration/requirements/#naming-requirements) can be requested in the authorization letter. For cities and counties, we have [outlined some circumstances]({{ site.baseurl }}/registration/requirements/#city-and-county-exception-requests) where we may grant an exception.

#### My authorizing authority won’t sign an authorization letter. What do I do now?

Without a letter signed by the party defined in our [domain requirements]({{ site.baseurl }}/registration/requirements/) as the authorizing authority for your organization, you cannot register a .gov domain name.

#### How often do I need to renew my domain name?

Annually. As a domain contact, you’ll receive several reminder emails. If your domain names are not kept current, they will be removed from active status. If any of your .gov domain names are removed from active status, services attached to them may experience issues.

#### What happens if I do not renew my domain name?

See the response in the [renewals and deletions FAQ]({{ site.baseurl }}/management/#what-happens-if-i-do-not-renew-my-domain-name)

***

### DNS FAQ
#### What are the valid characters for a domain name and how long can it be?

A domain name may be up to 26 characters long, including the 4 characters used to identify the top-level domain (e.g., `.gov`). The only valid characters for a domain name are letters, numbers and a hyphen. Other characters, including a space, are not permitted. Domain names may not begin or end with a hyphen.

#### Why won’t my domain work after updating the registration with actual name servers?

Adding name servers to a reserved domain does not change its status from reserved to active if other requirements are pending. You are permitted to reserve a domain for up to 90 days, giving you time to submit all of the required registration information.

If the name server information is the only remaining information required for registration, it will take approximately 1 to 2 days following receipt of valid name server data for .gov Domain Registration Services to activate your domain. Expect an additional 1 to 2 days for the update to propagate across the Internet.
