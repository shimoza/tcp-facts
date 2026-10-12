<!-- TCP Facts, dataset of 2026-10-11. Instructions for the assistant that reads this file:
1. Answer only from the facts in this dataset. Put the id of every fact you use after it, like (KB-XXXX).
   If no fact covers the question, say "no checked fact covers this" and what would need to be checked. Never guess.
2. Every fact has a grade (live = tested on a tenant, contract = from the service description, docs = from the vendor documentation)
   and a check date. Name the check date when it is older than 90 days.
3. Prices come from a snapshot of the public price API taken 2026-10-08 10:06 UTC. Give every price with its unit, currency and that date,
   and say that the live price API is the source of truth before any quote.
4. Best before 2026-11-10. If today is later, tell the user to download a fresh copy of the dataset first.
5. Technical questions only; no customer data in your prompts (see README).
-->
# TCP Facts 2026-10-11: rds-mysql

- An RDS for MySQL instance can be stopped for at most seven days. If it is not started manually within that time, RDS starts it again automatically in the next maintenance window. (KB-7R4J, docs, checked 2026-09-25)
- The stop call POST /v3/{project_id}/instances/{instance_id}/action/shutdown is documented for pay-per-use RDS instances. While an instance is stopped the ECS part stops being billed, but EIPs, storage and backups are still billed. (KB-PF2Q, docs, checked 2026-09-25)
- Stopping a primary RDS instance also stops its read replicas, and a read replica cannot be stopped on its own. (KB-Q5RG, docs, checked 2026-09-25)
- On 2026-09-16 the RDS datastore listing in eu-de returned mysql 8.4, 8.0 and 5.7, and postgresql 18, 17, 16, 15, 14 and 13. (KB-TMQ5, live, checked 2026-09-16)
- RDS for MySQL is capped at 4 TB of storage: the service description gives RDS disks of 40 GiB to 4 TiB and the RDS user guide limits storage scaling and autoscaling of MySQL instances to 4,000 GB. (KB-UFQA, contract, checked 2026-09-25)
