---
title: Common registration questions
layout: docs
permalink: /registration/common-questions/

sidenav: registration
subnav:
  - text: Fees FAQ
    href: '#fees-faq'
  - text: Domain authorization FAQ
    href: '#domain-authorization-faq'
  - text: DNS FAQ
    hret: '#dns-faq'
---

## Fees
A .gov domain name is $400 per year.

* [What payment methods do you accept?](#what-payment-methods-do-you-accept)
* [How often do I need to renew my domain name?](#how-often-do-i-need-to-renew-my-domain-name)
* [What happens if I fail to submit a payment?](#what-happens-if-i-fail-to-submit-a-payment)

## Domain requirements and authorization
* [What are the requirements for a domain's points of contact?](#what-are-the-requirements-for-a-domains-points-of-contact)
* [How do I request an exception to the naming conventions?](#how-do-i-request-an-exception-to-the-naming-conventions)
* [My authorizing authority won’t sign an authorization letter. What do I do now?](#my-authorizing-authority-wont-sign-an-authorization-letter-what-do-i-do-now)
* [My request was denied. What is the appeal process?](#my-request-was-denied-what-is-the-appeal-process)

## DNS
* [What are the valid characters for a domain name and how long can it be?](#what-are-the-valid-characters-for-a-domain-name-and-how-long-can-it-be)
* [Why won’t my domain work after updating the registration with actual name servers?](#why-wont-my-domain-work-after-updating-the-registration-with-actual-name-servers)

***

### Fees FAQ

A .gov domain name is $400 per year.

#### What payment methods do you accept?

We can only accept credit card payments.

#### How often do I need to renew my domain name?

Annually. As a point of contact, you’ll receive several reminder emails. Please note that if your domain names are not kept current, they will be removed from active status. If any of your .gov domain names are removed from active status, services attached to them may experience issues.

#### What happens if I do not renew my domain name?

See the response in the [renewals and deletions FAQ]({{ site.baseurl }}/management/#what-happens-if-i-do-not-renew-my-domain-name)

***

### Domain authorization FAQ
#### What are the requirements for a domain's points of contact?

Each domain is to have unique points of contact, which your authorization letter must define. There cannot be a single point of contact or one duplicated across more than one role, unless you select a named person's email address for a security contact (which is **not recommended**).

1. **Administrative contact**: someone from the signatory’s office that will approve the content. This person must be a government employee.

2. **Billing contact**: a person with access to a government credit card and the ability to pay registration fees.

3. **Technical contact**: a developer or administrator, often responsible for managing [DNS]({{ site.baseurl }}/management/dns/) and securing the infrastructure.

4. **Security contact**: a [security contact]({{ site.baseurl }}/management/security-best-practices/#add-a-security-contact) is a recommended practice, and can be added to allow outsiders to report observed or suspected security issues at your domain. *Security contact details are made public.*

Each contact will have the ability to access the .gov registrar, make changes to DNS, or make payments.

#### How do I request an exception to the naming conventions?

Exceptions to the [naming conventions]({{ site.baseurl }}/registration/requirements/#naming-conventions) can be requested in the authorization letter. For cities and counties, we have [outlined some circumstances]({{ site.baseurl }}/registration/requirements/#city-and-county-exception-requests) where we may grant an exception.

#### My authorizing authority won’t sign an authorization letter. What do I do now?

Without a letter signed by the party defined in our [domain requirements]({{ site.baseurl }}/registration/requirements/) as the authorizing authority for your organization, you cannot register a .gov domain name.

#### My request was denied. What is the appeal process?

In October 1997, the Federal Networking Council delegated full responsibility for .gov domain registration to the [General Services Administration](https://www.gsa.gov). Please [contact us]({{ site.baseurl }}/support/) with any questions you may have.

***

### DNS FAQ
#### What are the valid characters for a domain name and how long can it be?

A domain name may be up to 26 characters long, including the 4 characters used to identify the top-level domain (e.g., `.gov`). The only valid characters for a domain name are letters, numbers and a hyphen. Other characters, including a space, are not permitted. Domain names may not begin or end with a hyphen.

#### Why won’t my domain work after updating the registration with actual name servers?

Adding name servers to a reserved domain does not change its status from reserved to active if other requirements are pending. You are permitted to reserve a domain for up to 90 days, giving you time to submit all of the required registration information.

If the name server information is the only remaining information required for registration, it will take approximately 1 to 2 days following receipt of valid name server data for .gov Domain Registration Services to activate your domain. Expect an additional 1 to 2 days for the update to propagate across the Internet.
