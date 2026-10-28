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
# TCP Facts 2026-10-28: cfw

- A standard postPaid Cloud Firewall protecting the EIP of a hub NAT gateway filters spoke egress at the internet border. A top-priority deny rule on one destination address and port blocked exactly that flow while traffic to other destinations still left through the NAT EIP. (KB-437B, live, checked 2026-07-17)
- POST /v1/{project_id}/acl-rule needs a top-level type field, 0 for the internet border, beside the per-rule fields. Without it the call returns common.00000400, '[type] must not be null'. (KB-75P6, live, checked 2026-07-17)
- A Cloud Firewall instance is created with POST /v2/{project_id}/firewall carrying name, enterprise_project_id, flavor.version standard and charge_info.charge_mode postPaid, and removed with DELETE /v2/{project_id}/firewall/{firewall_id}. (KB-BOFP, live, checked 2026-07-17)
- CFW firewalls are listed with POST /v1/{project_id}/firewalls/list on cfw.eu-de.otc.t-systems.com carrying limit and offset, not with GET. The call returned HTTP 200 and the listed firewall showed is_support_postpaid true. (KB-HJNP, live, checked 2026-07-17)
- Cloud Firewall (CFW) is a cloud-native next-generation firewall that protects the internet border and the VPC borders with real-time intrusion detection and prevention, unified access control, traffic analysis, log audit and tracing. The documentation names access control by 5-tuple, by domain name, by IPS rules in observe or block mode and by IP address groups with blacklists and whitelists, and an HA cluster deployment. Its API answered in eu-de and eu-nl on 2026-09-25 (KB-4MR7). (KB-N7ZV, contract, checked 2026-10-14)
- GET /v1/{project_id}/eips/protect?object_id=..&sync=1 must be called once to sync tenant EIPs before POST /v1/{project_id}/eip/protect, otherwise the protect call returns CFW.00200111. Protected objects are listed under .protect_objects in the firewall/exist records, where type 0 is the internet border. (KB-OY5B, live, checked 2026-07-17)
- Cloud Firewall (CFW) protects NAT gateway traffic by protecting the VPC where the NAT gateway resides. CFW professional edition with Enterprise Router (ER) traffic diversion inspects inter-VPC east-west traffic and Direct Connect traffic. (KB-UWHB, docs, checked 2026-07-17)
