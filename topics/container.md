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
# TCP Facts 2026-10-28: container

- The Neutron port API on TCP deviates from upstream OpenStack, so the OpenShift Machine API fails to create network ports when a MachineSet scales workers. The documented workaround replaces machine-api-provider-openstack with a patched image published in SWR. The deviation affects OpenStack-native tooling in general. (KB-5ZKF, docs, checked 2026-06-08)
- OpenShift is orderable on TCP through the Cloud Create self-service catalogue as self-managed Red Hat OpenShift Container Platform, bring your own subscription, installed UPI on the OpenStack-compatible API. Template versions 4.16.19 and 4.18.30 are offered, further versions on request. (KB-6EFK, docs, checked 2026-09-25, recheck due)
- The paths /v1/clusters, /v1/fleets, /v1/permissions and /v1/ccechecks were recorded on the eu-de UCS endpoint ucs.eu-de.otc.t-systems.com. Only /v1/clusters was confirmed by a live call, the other three were noted and not called. (KB-DIDW, live, checked 2026-09-01, recheck due)
- UCS on T Cloud Public (TCP) is domain-scoped. GET /v1/clusters on the eu-de UCS endpoint answered HTTP 200 with an empty item list when signed with a domain-scoped IAM token, and answered HTTP 401 UCS.01000003 when signed with project-scoped AK/SK. (KB-L6UF, live, checked 2026-09-01)
- A Cloud Create OpenShift deployment builds 3 master nodes, at least 2 workers, a bootstrap node that is deleted after installation and a bastion. It needs about 30 minutes or more until the cluster is ready. (KB-UE2E, docs, checked 2026-06-08)
- UCS carries a stated availability date of 01.09.2026 on T Cloud Public (TCP). A signed call reached its eu-de API, while ordering and consumption of the service were not tested. (KB-X3HG, contract, checked 2026-10-14)
