<!-- TCP Facts, dataset of 2026-10-28. Instructions for the assistant that reads this file:
1. Answer only from the facts in this dataset. Put the id of every fact you use after it, like (KB-XXXX).
   If no fact covers the question, say "no checked fact covers this" and what would need to be checked. Never guess.
2. Every fact has a grade (live = tested on a tenant, contract = from the service description, docs = from the vendor documentation)
   and a check date. Name the check date when it is older than 90 days.
3. The dataset holds no price list. Prices come live from the public price API. Give every price with its unit, currency
   and the date of its source, and say that the live price API is the source of truth before any quote.
4. Best before 2026-11-27. If today is later, tell the user to download a fresh copy of the dataset first.
5. Technical questions only; no customer data in your prompts (see README).
-->
# TCP Facts 2026-10-28: dns

- A signed parent zone's denial of DS stays in resolver caches after a DS is published. Measured caps on the public resolvers: Google 1800 s, Quad9 about 3600 s, Cloudflare honours the parent SOA MINIMUM in full. (KB-34BU, live, checked 2026-09-10)
- Private DNS zones on TCP resolve the cloud-internal namespace. (KB-3DUD, docs, checked 2026-07-17)
- GET /v2/zones/{zone_id}/dnssec on the eu-de DNS endpoint returns 200 with status DISABLE, or the key object with flag 257, key_tag, digest, digest_algorithm SHA256, digest_type 2, signature ECDSAP256SHA256, signature_type 13, ksk_public_key, ds_record, created_at, updated_at and status ENABLE. (KB-4KAY, live, checked 2026-09-10)
- In eu-de on 2026-09-25, GET /v2/zones/{zone_id}/nameservers returned ns1.open-telekom-cloud.com and ns2.open-telekom-cloud.com for all four public zones of a test project, and a domain hosted in the TCP DNS service is delegated to these two name servers at its registrar. An NS lookup of such a domain names the platform. (KB-5KZD, live, checked 2026-09-25)
- DNSSEC is absent from the DNS api-ref, and the opentelekomcloud Terraform provider 1.37.8 ships no DNSSEC resource. (KB-5SWB, docs, checked 2026-09-10)
- On a TCP public zone with DNSSEC enabled, the parent side returns no authenticated denial of DS for a delegated child zone, so validating resolvers cannot resolve names below such a delegation, wherever the child is hosted. Keep child names in the parent zone, or leave DNSSEC off while a delegation is needed. (KB-5T6U, live, checked 2026-09-10)
- Enabling DNSSEC works on a subdomain public zone on TCP, although the console banner says DNSSEC can be enabled only for top-level domains and the UMN says DNSSEC supports only primary domain names. (KB-6PPX, live, checked 2026-09-10)
- Domain Name Service (DNS) is an authoritative DNS service in which the customer configures DNS zones and records for internal and external communication. It provides public zones that resolve domain names on the internet, private zones that resolve names to private IP addresses inside VPCs, and reverse resolution of IP addresses to domain names. The Regions and Endpoints page lists API endpoints for DNS in eu-de and eu-nl. (KB-ABGI, contract, checked 2026-10-14)
- TCP DNS rejects DNSKEY as a record set type and refuses both AXFR and IXFR, so a second provider's ZSK cannot be published and a signing secondary cannot be fed. RFC 8901 multi-signer is not possible with TCP DNS as a participant. (KB-CWDY, live, checked 2026-09-10)
- CTS logs DNSSEC switching as the operations enableDnssecConfig and disableDnssecConfig with resource_type dnssec and trace_type ConsoleAction, while a scripted record-set create appears with trace_type ApiCall. (KB-DR5A, live, checked 2026-09-10)
- A DNS zone object carries no dnssec field, and a dnssec key in the zone-create body is accepted and ignored. (KB-H2BV, live, checked 2026-09-10)
- A zone delegated to TCP DNS validates end to end when its parent is hosted off-platform and publishes the DS: the child is signed by TCP DNS and resolvers report it fully validated. (KB-IGAE, live, checked 2026-09-10)
- Re-keying a signed TCP public zone is a disable and re-enable of DNSSEC, which mints a brand new KSK with a different key tag and no overlap with the old one. The documented order is to remove the DS at the parent first, then disable, otherwise the zone goes bogus instead of dropping to unsigned. (KB-LS5E, live, checked 2026-09-10)
- On T Cloud Public (TCP) in eu-de the DNS v2 call GET /v2/zones?type=private returns HTTP 200. The response carries the keys zones, links and metadata.total_count, so private zones come from the same v2 zones path as public ones, selected by the type query parameter. (KB-MRFV, live, checked 2026-07-02)
- Each of the nine EIPs of a test project in eu-de answered a reverse DNS lookup on 2026-09-25 with a default name that starts with ecs-, carries the address with dashes and ends in reverse.open-telekom-cloud.com, while the DNS user guide shows the pattern ecs-xx-xx-xx-xx under a compute domain. The guide says a PTR record created in the DNS service replaces this default and deleting it brings the default back. (KB-NIB4, live, checked 2026-09-25)
- A signed TCP public zone that delegates nothing beneath it works. The platform does not insert a child DS automatically when parent and child are both public zones in the same tenant. (KB-POVU, live, checked 2026-09-10)
- The TCP DNS signer is online and signs per RRset at write time, separately on each nameserver. The RRSIG validity window runs from 30 days before signing to 730 days after, so a published window reads 760 days wide and one zone carries several windows at once. (KB-RCXE, live, checked 2026-09-10)
- Default DNS quota on TCP is 50 public zones and 500 record sets. (KB-TWRY, docs, checked 2026-09-10)
- The DNS DNSSEC resource is registered read-only. POST, PUT, PATCH and DELETE on /v2/zones/{id}/dnssec return 404 APIGW.0101 with the text "method POST not found", both with AK/SK signing and with IAM tokens. (KB-W7XD, live, checked 2026-09-10)
- The DNS fine-grained action list on TCP has no action for the DNSSEC operation, so it cannot be separated from zone administration in an IAM policy. The audit service records the operation. (KB-XFW6, docs, checked 2026-09-10)
- Wildcard records and underscore-prefixed names resolve and validate on a DNSSEC-signed TCP public zone. A wildcard answer carries an RRSIG with the correct label count plus the NSEC proving the queried name does not exist. (KB-XWFC, live, checked 2026-09-10)
