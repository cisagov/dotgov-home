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

## Cloud Signing Service

#### What is the Cloud Signing Service?

The Cloud Signing Service eliminates many of the administrative burdens of the technical DNSSEC signing and management process. The service performs the initial cryptographic signing, the regular re-signing of zone resource records and the ongoing management of key rollover schedules and the associated zone re-signing.

#### How do I get started with the Cloud Signing Service?

* Existing unsigned .gov zone:  You have an existing, active domain name, and your zone is not DNSSEC enabled (or in other words, your zone is not signed by you or any external DNSSEC provider).  If you are not currently signed with any DNSSEC provider, you are eligible to enroll with the Cloud Signing Service.
* Existing signed zone with Algorithm 8: You or your provider is signing your zone with Algorithm 8 (RSA/SHA-256) and you want to switch to Cloud Signing Service.  Automatic enrollment for transferring DNSSEC providers is not supported at this time.  This process can be done manually.  For additional details, please contact the Helpdesk at [registrar@dotgov.gov](mailto:registrar@dotgov.gov).
* Existing signed zone with other Algorithm: You or your provider is signing your zone with an Algorithm other than Algorithm 8 and you want to switch to Cloud Signing Service. Automatic enrollment for transferring DNSSEC providers is not supported at this time.  This process can be done manually.  For additional details, please contact the Helpdesk at [registrar@dotgov.gov](mailto:registrar@dotgov.gov).

#### If I am currently enrolled in the Key Monitoring Service, do I still need to enroll in the Cloud Signing Service?

The Cloud Signing Service and Key Monitoring Service are different services. Enrolling in Key Monitoring will not automatically enroll you in the Cloud Signing Service. The Key Monitoring Service enables monitoring of a child zone for any new KSKs and automatically adds the DS corresponding to the new KSK. This will also send notifications when the ROLLOVER is successfully completed, when an RRSIG expiry is within certain thresholds, and also when there is a Child Key Error. The Cloud Signing Service will perform the initial signing and ongoing key management for your zone. If you do not need a DNSSEC signing service, you do not need to enroll into Cloud Signing Service. However, if you do need a DNSSEC signing service for your zone, and wish to take advantage of the Cloud Signing Service, you will need to explicitly enroll into Cloud Signing Service. The Key Monitoring enrollment alone will not provide the initial and ongoing signing that is required for a DNSSEC enabled zone.

If your domain is enrolled in the Key Monitoring Service, it will stay enrolled into that service even after you enroll into the Cloud Signing Service.

If your domain is not already enrolled into the Key Monitoring Service and you choose to enroll in the Cloud Signing Service, the system will automatically enroll you into the Key Monitoring Service. Customers have the option to de-enroll from Key Monitoring if they want, however, this is not recommended. Please note that if you choose to remove your domain from the Key Monitoring Service, it will be your responsibility to submit the appropriate DS information into the .gov UI.

#### What is a TSIG?

The Cloud Signing Service requires the use of TSIG (Transaction Signature) to provide the secure transfer of zone data by allowing your designated nameservers to authenticate to our nameservers. It also allows our   nameservers to check the integrity of the zone data transferred. Please note that TSIG requires that you run BIND version 8.2 or later.

Where do I enter my TSIG key?

Enter your TSIG key information along with the nameserver information. You will also need to do the following:

* Add a key statement to your 'named.conf' file
* Add an "allow-transfers" sub-statement to your zone's statement.

Please note that this requires BIND version 8.2 or later.

#### What do I do if I don't have a TSIG key?

If you do not have a TSIG key, you may generate a TSIG key through the "Customer Nameservers" tab. You will then need to add a key statement to your 'named.conf' file and an "allow-transfers" sub-statement to your zone's zone statement.

#### Why do I need to configure my nameservers for the Cloud Signing Service?

The new zone added to the service will not be signed until your source nameserver and destination nameserver have been configured to allow zone transfer out and in respectively from the Cloud Signing Service source and destination nameservers.

The following steps are what may be followed in a typical set up for the Cloud Signing Service:

* Identify your Source and Destination nameservers. (The Source nameserver should be able to serve your UNSIGNED zone. Your Destination nameserver may or may not be your Active nameserver)
* Set up a TSIG for them (you can generate one or ask Cloud Signing Service to generate it for you when adding your nameservers)
* Make sure your nameservers support zone transfer using AXFR.
* Make sure your firewall for both source and destination nameservers allow the following IPs on port 53:

    72.13.32.91<br/>
    69.58.186.91<br/>
    72.13.32.92<br/>
    69.58.186.92<br/>
    72.13.32.93<br/>
    69.58.186.93<br/>
    72.13.32.94<br/>
    69.58.186.94

* Login to dotGOV UI and go to the Domain Update page for your domain.
* Enroll your domain into Cloud Signing Service from here.
* Cloud Signing Service will sign your zone and then the signed zone will be transferred back to your destination name server
* Make sure the signed zone is published to your active name servers (if different from Destination)
* The DS record will be automatically added to the .GOV zone within 24 hours from signing.

#### When does the Cloud Signing Service communicate with my source/destination nameservers?

* The service shall query the customer primary/ backup nameservers under the following scenarios:
* When your source nameserver(s) issues NOTIFY, the Cloud Signing Service requests AXFR from that source nameserver(s) ONLY.
* When the Cloud Signing Service initiates a SOA query/ AXFR request for a new zone or expiry of refresh interval, then the service fails over to the backup customer nameserver if communication to the first server fails
* When the signed zone is ready the Cloud Signing Service, we will notify your destination nameservers.
* When your destination nameserver(s) initiates a query, the Cloud Signing Service will respond to your server

#### How does a zone transfer occur?

For both of these processes the common DNS AXFR protocol is utilized. There are no custom APIs or protocols that are needed in order to transfer zone data into and out of the Cloud Signing Service.

#### What happens when a zone is added?

The Cloud Signing Service first requests a DNS transfer (AXFR) from your nameserver. The service signs the zone and informs the customer systematically that the zone is ready to be picked up and processed.

#### What are the keys that are generated to sign the zone?

Once a zone is added to the service and the transfer is successful the first step in the signing process involves generating the necessary keys to sign the zone. This includes a KSK and a ZSK. The public key of the KSK and ZSK are stored in DNSKEY RRs in the zone file and the private key is stored within our secure infrastructure.

#### What is a KSK?

The Key Signing Key (KSK) is an authentication key that corresponds to a private key used to sign one or more other keys for a given zone. With this service the private key corresponding to a KSK will sign the ZSK, which in turn has a corresponding private key that will sign other data in your zone.

#### What is a ZSK?

Zone Signing Key (ZSK) is an authentication key that corresponds to a private key used by this service to sign data in your zone.

#### What is the key pre-publish period?

Keys are required to be pre-published before the active key expires to allow time for the DS record to be updated in the parent zone (for a KSK) and to accommodate resolvers that may have cached the prior signed zone and are still referencing the signatures created by the previously active keys.

* The Pre-publish period for the KSK will be for a period of 2 months.
* The Pre-publish period for the ZSK will be for a period of 1 week.

#### What is the key active period?

The active period is the time during which the keys (KSK or ZSK) will be active. Following this period the keys will be rolled over and the pre published key will become the active key.

* Active period for KSK is 2 years and for ZSK is 3 months.
* The active period for the KSK will be for a period of 2 years.
* The active period for the ZSK will be for a period of 3 months.

#### What is the key post-publish period?

The keys will be published in the zone for a predetermined post-publish period after the active end date. This is to accommodate resolvers that may have cached the prior signed zone and are still referencing the signatures created by the previously active keys.

* The post-publish period for the KSK will be for a period of 2 months.
* The post-publish period for the ZSK will be for a period of 1 week.

#### What is the signature validity period?

The Signature validity period is the periods through which the signature is valid.

It starts at the time specified in the signature inception field of the RRSIG RR and ends at the time specified in the expiration field of the RRSIG RR. The Cloud Signing Service currently assigns a signature validity period of 14 days for all zones and all signatures in zones. It will attempt to re-sign each zone again in about 7 days to ensure that a published zone never has invalid signatures.

#### How often is the zone signed?

The zone is signed every time your zone file is updated, or every 7 days, whichever comes first.

#### How often are the keys rolled?

The Cloud Signing Service will support a fixed schedule for all KSKs and ZSKs. The fixed schedule will include the following: Key pre publish period; Key Active period; and Key post publish period for all KSKs and ZSKs. Key Rollovers will occur on the following schedules:

* The KSK will be available for a fixed interval of two (2) years
* The ZSK will be available for a fixed interval of three (3) months

The KSK and ZSK will be active until the scheduled rollover date or until an emergency key rollover is requested. The service will not generate a new KSK or ZSK key every time the zone is signed. The same KSK and ZSK keys will be used until it is no longer active.

#### What is an emergency roll over?

In the unlikely event you feel that a key may have been compromised (KSK, ZSK or both), the Point of Contact for your domain may contact the Helpdesk at registrar@dotgov.gov to request an unscheduled/ emergency key rollover. After the Helpdesk completes the emergency key rollover request, the zone will be signed with the new keys.

#### What happens when an emergency KSK rollover is requested?

When an emergency KSK is requested the zone will be resigned with the compromised KSK and with either a

* new KSK, or
* if a KSK was already being pre-published, then that key will be made active
* Compromised KSK: The compromised KSK will be active for 1 week from rollover date, and post-published for 1 week.
* New KSK: The new KSK will be active following the rollover date. The new KSK will be valid for a period of 2 years from the emergency rollover date and will be post-published per usual post-publish period.

#### What happens when an emergency ZSK rollover is requested?

When an emergency ZSK is requested, the zone will be signed with the compromised ZSK for an additional 2 days from date of rollover request. After 2 days, the zone will be resigned with either a

* new ZSK, or
* If a ZSK was already being pre-published, then that key will be made active
* Compromised ZSK: The compromised ZSK is inactivated 2 days after the emergency rollover request and post-published for 2 days
* New ZSK: The new ZSK will be active starting 2 days from the rollover request date until 3 months from active date and will be post-published for the usual post-publish period

#### What happens when my zone is updated?

The Cloud Signing Service requires that you set up your source nameserver to use NOTIFY to alert our service's   nameservers of any zone data changes. If you are running BIND version 8 or later and use the NOTIFY function, your nameserver will alert our nameservers to provide automatic zone updates when they occur.

#### What is a DS record?

The DS (Delegation Signer) Resource Record (stored in the parent zone) refers to specific zones KSK DNSKEY RR (in the child zone) and is used in the DNSSEC authentication process (see RFC4035 section 5 for details on the authentication process). A DS RR refers to the KSKs DNSKEY RR by storing the key tag, algorithm number, and a digest of the DNSKEY RR. By authenticating the DS record, a resolver can authenticate the KSK DNSKEY RR to which the DS record points.

#### What are the notifications that will be sent to the domain's technical POC?

* KSK Rollover scheduled (2 month, 1 month, 2 weeks prior to KSK expiration)
* KSK Rollover successful
* KSK Post-Publish Period Complete
* Emergency KSK Rollover
* Emergency ZSK Rollover
* Signing Status Change Alert (to SOURCE-FAILED-XFER)
* Signing Status Change Alert (to SOURCE-SOA-QUERY-FAILED)
* Signing Status Change Alert (to DESTINATION-FAILED-XFER)

#### What are the different statuses in the service a zone can have once it is added?

The following are the possible statuses while transferring a Zone from the customer nameserver to our nameservers.

* SOURCE_PENDING_XFER – This status is shown when a new Zone is added and is pending transfer.
* SOURCE_OK – This status is shown when the transfer from the source nameserver succeeded.
* SOURCE_FAILED_XFER – This status is shown when the transfer from the source nameserver failed.
* SOA_QUERY_FAILED – This status is shown when the SOA record query failed.

#### What are some of the reasons of a failure of a source SOA query?

The source SOA query can fail for the following reasons:

* No connectivity to source nameserver
* Customer nameserver is not running.
* Customer nameserver does not have the zone yet
* Customer nameserver has the zone but does not recognize our virtual IP address (VIP) as slave yet
* ACL for source nameserver has not reached the Cloud Signing Service

Please note, that the service will retry the connectivity every 1 hour after each one of these failures.

#### What are some of the reasons when the source_failed_xfer status occurs?

The source transfer could fail because of one of the reasons listed above in 2.28 or when your nameserver has not properly configured the TSIG.

#### What resource records are supported in the Cloud Signing Service?

The DNSSEC Signing Service is has been tested been tested to ensure support of the following DNS Resource Record Types: A, AAAA, CNAME, DNAME, DNSKEY, DS, LOC, MX, NAPTR, NS, NSEC, NSEC3, PTR, RRSIG, SOA, SPI, SRV, SSHFP, TXT. Other record types may be supported but have not been validated in our testing.

#### What method is used authenticate the zone transfer?

The Cloud Signing Service uses DNS TSIG/TKEY for the transfer of Zones.
