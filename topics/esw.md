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
# TCP Facts 2026-10-28: esw

- Three vocabularies name the same three enterprise switch sizes: Basic, Standard and Enhanced on the console and spec page, small, medium and large in the quota table, and esw.small, esw.medium and esw.large as billing SKUs. (KB-4CG4, docs, checked 2026-08-26)
- Enterprise Switch (ES) is a preview service that provides layer 2 communication between the customer's on-premises data center and a VPC, so workloads can move to T Cloud Public (TCP) without changing subnets or IP addresses. It requires a layer 3 connection through Enterprise VPN or Direct Connect, and the documentation describes a layer 2 connection gateway that works with that connection, also where the cloud and on-premises address ranges overlap. (KB-IIT3, contract, checked 2026-10-14)
- The ESW documentation requires a service ticket to confirm that a Direct Connect or VPN connection supports VXLAN interconnection with an enterprise switch. The requirement is stated twice. (KB-J7GH, docs, checked 2026-08-26)
- Enterprise Switch (ESW) has no lifecycle API on TCP. Switches and L2 connections are created and changed in the console only. (KB-QDFH, docs, checked 2026-08-26)
- The user guides for enterprise-switch and secure-mail-gateway hold real content while both API references are placeholder pages. Secure Mail Gateway is an outbound mail anti-spam and anti-virus gateway documented as flat pages on intro, security mechanisms, setups and installation. (KB-RHSC, docs, checked 2026-06-08)
- Enterprise Switch is offered in eu-de only. (KB-TEXG, contract, checked 2026-10-14)
- Cloud Eye publishes the namespace SYS.ESW with 6 metrics per instance_id at 1 minute granularity. This is the programmatic read path for an enterprise switch. (KB-VZL5, docs, checked 2026-08-26)
- The ESW forwarding restriction is documented for one direction: untrusted unicast, broadcast and multicast packets (VRRP excepted) and IPv6 packets are not forwarded from the customer data center to the cloud. The cloud to data center direction is not covered by that sentence. (KB-YAWC, docs, checked 2026-08-26)
- The ESW permissions table assigns create, modify, delete and view of a switch or an L2 connection to the VPC Administrator role, and view to Tenant Guest. (KB-YM4F, docs, checked 2026-08-26)
