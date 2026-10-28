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
# TCP Facts 2026-10-28: bms

- BMS bare metal is not orderable in eu-de. The service description revision 09.10.2026 carries no BMS entry and offers bare metal as Physical ECS c7t, with physical c9 and m9 announced from 01.10.2026 on request; on 2026-09-25 the BMS flavor listing marked every AZ of the three returned flavors as abandon or sellout. (KB-UEVJ, contract, checked 2026-10-14)
- The service description revision 09.10.2026 offers bare metal as Physical ECS: BM General Purpose c7t.28xl, EU-DE only (section 3.1.1.2 and section 6.2.1.19), and the ECS flavor c7t.28xlarge.4.physical reported eu-de-03(normal) on 2026-09-25. Physical c9 and m9 flavors are announced from 01.10.2026 and offered only on request. (KB-WD2H, contract, checked 2026-10-14)
- The opentelekomcloud provider 1.37.8 ships 330 resources. Compared with 1.36.64 it adds 15 resources and drops the two BMS resources compute_bms_server_v2 and compute_bms_tags_v2. (KB-WMZI, live, checked 2026-09-16)
