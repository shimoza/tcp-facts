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
# TCP Facts 2026-10-14: dcs

- After an online migration between DCS Redis 4.0 or later instances, DCS can swap the IP addresses of source and target so clients keep their address, with a rollback of the swap possible. It works for single-node, master/standby, read/write splitting and Proxy Cluster instances with the same port, password and whitelist, while the instances turn read-only for one minute during the swap. (KB-2XZS, docs, checked 2026-09-25)
- The Redis major version of a DCS instance cannot be changed after creation, for example from 5.0 to 6.0. The documented path is a new instance with the higher version and a data migration into it. (KB-5XW5, docs, checked 2026-09-25)
- Distributed Cache Service (DCS) is a managed in-memory NoSQL database based on Redis, with tools for automatic provisioning, maintenance, monitoring, backup and recovery. Instances are single node, primary/standby with 2 to 5 replicas, or cluster, plus read/write splitting and proxy cluster types; new instances run Redis 4.x, 5.x, 6.x or 7.x, and the documentation states that primary/standby and cluster instances can be deployed across availability zones. The Regions and Endpoints page lists API endpoints for DCS in eu-de and eu-nl. (KB-AS3U, contract, checked 2026-10-11)
- New Redis 3.x instances of DCS can no longer be booked, while existing Redis 3.x instances can still be used as usual. (KB-P4WZ, contract, checked 2026-09-25)
- DCS migrates data between instances either online (in full or incrementally, when the source allows SYNC and PSYNC) or by importing AOF or RDB backup files. Every DCS instance type can be the source for every DCS target type. (KB-QQFN, docs, checked 2026-09-25)
- On 2026-09-25 the DCS flavor list in eu-de and eu-nl tagged the single-node, master/standby and Redis Cluster flavors with Redis 4.0, 5.0, 6.0 and 7.0. Proxy Cluster and read/write splitting flavors carried 4.0, 5.0 and 6.0, so a Redis 6.0 target exists in all five instance types. (KB-TUIU, live, checked 2026-09-25)
- In place, DCS upgrades only the minor or proxy version of Redis 4.0 and later instances, always to the latest one, without rollback and with connection address, password, whitelist and alarms unchanged. During the upgrade a migrating shard turns read-only for one minute and clients are intermittently disconnected. (KB-VP4J, docs, checked 2026-09-25)
