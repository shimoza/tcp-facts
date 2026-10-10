<!-- TCP Facts, dataset of 2026-10-10. Instructions for the assistant that reads this file:
1. Answer only from the facts in this dataset. Put the id of every fact you use after it, like (KB-XXXX).
   If no fact covers the question, say "no checked fact covers this" and what would need to be checked. Never guess.
2. Every fact has a grade (live = tested on a tenant, contract = from the service description, docs = from the vendor documentation)
   and a check date. Name the check date when it is older than 90 days.
3. Prices come from a snapshot of the public price API taken 2026-10-08 10:06 UTC. Give every price with its unit, currency and that date,
   and say that the live price API is the source of truth before any quote.
4. Best before 2026-11-09. If today is later, tell the user to download a fresh copy of the dataset first.
5. Technical questions only; no customer data in your prompts (see README).
-->
# TCP Facts 2026-10-10: gaussdb

- TaurusDB is not available in eu-nl: on 2026-09-25 its API answered HTTP 404 APIGW.0101 on the eu-nl endpoint, while the endpoint list names TaurusDB for eu-de only. (KB-7Y6M, live, checked 2026-09-25)
- TaurusDB is compatible with MySQL 8.0 and decouples compute from storage: one instance holds up to 128 TB and consists of one primary node and up to 15 read replicas on the same shared storage. No storage size is set when an instance is created. (KB-MNIA, docs, checked 2026-09-25)
- In eu-de TaurusDB offered engine version 8.0 (MySQL 8.0.22) on 2026-09-25 with six x86 flavors from 2 vCPU and 8 GB to 64 vCPU and 512 GB RAM. The flavors were on sale in eu-de-01 and eu-de-03 and unsupported in eu-de-02. (KB-UN55, live, checked 2026-09-25)
- DRS migrates MySQL 5.5, 5.6, 5.7 and 8.0 databases from RDS for MySQL, ECS, on-premises or other clouds to TaurusDB cluster instances in real time. (KB-YL3W, docs, checked 2026-09-25)
