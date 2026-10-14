<!-- TCP Facts, dataset of 2026-10-14. Instructions for the assistant that reads this file:
1. Answer only from the facts in this dataset. Put the id of every fact you use after it, like (KB-XXXX).
   If no fact covers the question, say "no checked fact covers this" and what would need to be checked. Never guess.
2. Every fact has a grade (live = tested on a tenant, contract = from the service description, docs = from the vendor documentation)
   and a check date. Name the check date when it is older than 90 days.
3. Prices come from a snapshot of the public price API taken 2026-10-14 13:11 UTC. Give every price with its unit, currency and that date,
   and say that the live price API is the source of truth before any quote.
4. Best before 2026-11-13. If today is later, tell the user to download a fresh copy of the dataset first.
5. Technical questions only; no customer data in your prompts (see README).
-->
# TCP Facts 2026-10-14: deh

- In eu-de the Dedicated Host listing GET /v1.0/{project_id}/dedicated-hosts answers HTTP 200 on a tenant that owns no host, returning an empty dedicated_hosts array and total 0. (KB-26NM, live, checked 2026-07-20)
- Host types per availability zone are read with GET /v1.0/{project_id}/availability-zone/{az}/dedicated-host-types. The response carries the type names only, so vCPU and memory sizes have to come from another source such as the price API. (KB-5GCH, live, checked 2026-07-20)
- Dedicated host (DeH) provides isolated physical servers that are fully dedicated to one customer and run that customer's Elastic Cloud Servers. Dedicated hosts come in general purpose, dedicated general purpose, memory optimized and ultra-high I/O types and are provisioned, monitored and managed in the console. Customer-owned Microsoft Windows Server and SQL Server licenses (bring your own license) may be used on physical and dedicated hosts. The Regions and Endpoints page lists API endpoints for DeH in eu-de and eu-nl. (KB-6VVI, contract, checked 2026-10-14)
- On 2026-07-20 the Dedicated Host type listing returned for eu-de-01: s2, s2-medium, c3, c4, c7n, m3, m4, m7n; for eu-de-02: s2, s2-medium, c3, c4, c7n, m3; for eu-de-03: s2, s2-medium, s7n, c4, c7n. (KB-ESW2, live, checked 2026-09-25)
- The per-VM OS license rows of the eu-de DeH listing (productSection=licence, key prefix deh.lic) covered Open Linux, Oracle Linux, RedHat, Suse, SUSE-SAP and Windows. (KB-FJ6E, live, checked 2026-09-25)
- For a Dedicated Host deployment the billed items are the host itself, attached EVS, EIP and the per-VM OS license row. ECS instances placed on the host are covered by the host charge, which makes the model usable with customer-owned OS licenses. (KB-PEKS, docs, checked 2026-07-20)
- The public price API accepts sn=deh and returns Dedicated Host records under response.result.deh, split into productSection=main host rows and productSection=licence per-VM license rows. priceAmount is an hourly value, R12 and R24 are flat monthly values, and the 36-month reserved fields carried no rate on any DeH row of the eu-de listing. (KB-T5E6, live, checked 2026-07-20)
- As of 2026-07-20 no GPU host type was offered for Dedicated Host in eu-de. The per-AZ host-type listings returned only s, c and m families, and the service description lists only s, c, m and i families. (KB-TXBP, contract, checked 2026-10-14)
- The eu-de DeH listing read on 2026-07-20 held 9 host-type rows: s2, s2-medium, s7n, c3, c7n, c4, m3, m4 and m7n. The listing records what the price API carried on that date, which is separate from whether each host type can be ordered. (KB-UB44, live, checked 2026-09-25)
- The Dedicated Host service description (section 3.1.2, revision 09.10.2026) lists more host types than the eu-de API returned on 2026-09-25: s3, c9, c9 Pro, m9, i3, i3 Pro and i3m. Its section 6.2.2 shows s3 and the i3 types for EU-NL only and says the c9 and m9 hosts are offered only on request. (KB-WQWT, contract, checked 2026-10-14)
- The TCP service description (section 3.1.2, revision 09.10.2026) lists the Dedicated Host types s2-medium, s2, s3, s7n, c3, c4, c7n, c9, c9 Pro, m3, m4, m7n, m9, i3, i3 Pro and i3m, all of them CPU host types. (KB-ZLGK, contract, checked 2026-10-14)
