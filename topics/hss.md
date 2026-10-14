<!-- TCP Facts, dataset of 2026-10-14. Instructions for the assistant that reads this file:
1. Answer only from the facts in this dataset. Put the id of every fact you use after it, like (KB-XXXX).
   If no fact covers the question, say "no checked fact covers this" and what would need to be checked. Never guess.
2. Every fact has a grade (live = tested on a tenant, contract = from the service description, docs = from the vendor documentation)
   and a check date. Name the check date when it is older than 90 days.
3. Prices come from a snapshot of the public price API taken 2026-10-08 10:06 UTC. Give every price with its unit, currency and that date,
   and say that the live price API is the source of truth before any quote.
4. Best before 2026-11-13. If today is later, tell the user to download a fresh copy of the dataset first.
5. Technical questions only; no customer data in your prompts (see README).
-->
# TCP Facts 2026-10-14: hss

- On a CCE worker node the HSS host agent runs three processes: hostguard at about 311 MB RSS, containerserver at about 42 MB and hostwatch at about 12 MB, roughly 365 MB RSS together, about 563 MB on disk and about 1.5 percent CPU at idle. Measured on EulerOS 2.9. (KB-2ZZR, live, checked 2026-02-04)
- Host Security Service (HSS) protects server workloads: it identifies and manages the assets on servers, reduces risks and defends against intrusions and web page tampering. It includes Container Guard Service (CGS), which scans container images for vulnerabilities and configuration issues, and Web Tamper Protection (WTP), which monitors website directories in real time and restores tampered files from backups. The Regions and Endpoints page lists the HSS API endpoint in eu-de. (KB-3CST, contract, checked 2026-10-11)
- The HSS user manual documents an HSS Administrator role and an HSSFullAccess policy for HSS permissions. Whether a subscribed domain needs them in addition to the subscription was not tested. (KB-AVCB, docs, checked 2026-09-02)
- On 2026-09-25 the documented HSS v5 API was not published in eu-nl: four GET paths answered 404 APIGW.0101 there, while in eu-de they reached the service (403 for a user without HSS rights). The public price API listed only the HSS Premium Edition for eu-nl, although section 6.10.7 of the service description lists four editions for EU-NL. (KB-OVOE, live, checked 2026-09-25)
- On 2026-09-25 in eu-de, GET under hss.eu-de.otc.t-systems.com/v5/{project_id} with the test key answered HTTP 403 APIGW.0302 (IAM user not authorized) for host-management/hosts, vulnerability/hosts, baseline/risk-configs, event/events and billing/quotas-detail, and HTTP 404 APIGW.0101 for asset/processes, asset/ports, asset/softwares, asset/accounts, asset/users and policy/groups. The HTTP 200 answers seen on 2026-02-04 on a premium-edition tenant were not reproduced. (KB-T4OL, live, checked 2026-09-25)
- On 2026-02-04 on a premium-edition HSS tenant, GET on the HSS v5 paths antivirus, webtamper/static/policy and image/build-history returned HTTP 404. (KB-UX32, live, checked 2026-09-25)
- On 2026-09-02 in eu-de, GET /v5/{project_id}/host-management/hosts returned 403 APIGW.0302, and billing/quotas-detail, policy/groups, asset/users and host-management/groups returned 404 APIGW.0101, with AK/SK signing and with a project-scoped token. The same access key received 200 from ECS. (KB-UXVH, live, checked 2026-09-02)
