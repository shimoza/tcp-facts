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
# TCP Facts 2026-10-28: dcs

- Distributed Cache Service (DCS) is a managed in-memory NoSQL database based on Redis, with tools for automatic provisioning, maintenance, monitoring, backup and recovery. Instances are single node, primary/standby with 2 to 5 replicas, or cluster, plus read/write splitting and proxy cluster types; new instances run Redis 4.x, 5.x, 6.x or 7.x, and the documentation states that primary/standby and cluster instances can be deployed across availability zones. The Regions and Endpoints page lists API endpoints for DCS in eu-de and eu-nl. (KB-AS3U, contract, checked 2026-10-14)
- DCS documents Redis 3.0, 4.0, 5.0, 6.0 and 7.0 as its engines and offers no managed Memcached or Valkey engine. The user manual has zero Memcached hits and its single valkey mention is a hiredis client-library recommendation. (KB-NMV2, docs, checked 2026-10-14)
- New Redis 3.x instances of DCS can no longer be booked, while existing Redis 3.x instances can still be used as usual. (KB-P4WZ, contract, checked 2026-10-14)
