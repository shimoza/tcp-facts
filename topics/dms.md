<!-- TCP Facts, dataset of 2026-10-22. Instructions for the assistant that reads this file:
1. Answer only from the facts in this dataset. Put the id of every fact you use after it, like (KB-XXXX).
   If no fact covers the question, say "no checked fact covers this" and what would need to be checked. Never guess.
2. Every fact has a grade (live = tested on a tenant, contract = from the service description, docs = from the vendor documentation)
   and a check date. Name the check date when it is older than 90 days.
3. The dataset holds no price list. Prices come live from the public price API. Give every price with its unit, currency
   and the date of its source, and say that the live price API is the source of truth before any quote.
4. Best before 2026-11-21. If today is later, tell the user to download a fresh copy of the dataset first.
5. Technical questions only; no customer data in your prompts (see README).
-->
# TCP Facts 2026-10-22: dms

- The DMS documentation handles the move from a single-AZ Kafka instance to a cross-AZ one as a migration to a new instance: create the target with specifications not lower than the original, create the topics with the same settings, then move producers and consumers (production first, production later, or consumption first with a Smart Connect replication task). (KB-5EBZ, docs, checked 2026-09-25)
- A DMS for Kafka instance is deployed in one AZ or in at least three AZs. Two AZs cannot be selected. (KB-DB6R, docs, checked 2026-09-25)
- A DMS for Kafka instance cannot be upgraded to a higher Kafka version after it is created. The documentation says to create another Kafka instance with the higher version instead. (KB-FK4Y, docs, checked 2026-09-25)
- Distributed Message Service (DMS) is a managed message queuing service: DMS for Kafka provides Kafka instances that are compatible with open-source Apache Kafka and are reached with open-source Kafka clients, with a configurable number of partitions and replicas, as single-broker or cluster flavors of 3 to 50 brokers. Since May 2026 DMS also offers RocketMQ instances as single instance or cluster. The Regions and Endpoints page lists API endpoints for DMS in eu-de and eu-nl. (KB-IXZ3, contract, checked 2026-10-14)
- On 2026-09-25 the DMS Kafka product catalog (GET /v2/kafka/products) listed Kafka versions 2.7 and 3.x for new instances in eu-de and eu-nl, and GET /v2/available-zones returned three AZs in each region. The FAQ page of the docs mirror still names v2.3.0 as well. (KB-PBIU, live, checked 2026-09-25)
- The AZs of a DMS for Kafka instance cannot be changed after creation, so a single-AZ instance cannot become a multi-AZ instance. To use several AZs you create another instance. (KB-PEZB, docs, checked 2026-09-25)
- Smart Connect, the DMS function that replicates data between two Kafka instances, is not available for single-node Kafka instances, only for cluster instances. (KB-Q7ZJ, docs, checked 2026-09-25)
- In TCP eu-de on 2026-09-25 the classic DMS queue path GET /v1.0/{project_id}/queues returns HTTP 404 and the Kafka instance paths respond normally. The quota paths GET /v2/{project_id}/quotas, documented in the RocketMQ API reference, and GET /v1.0/{project_id}/quotas/dms answer 200 with Kafka and RocketMQ instance quotas. (KB-ZFRE, live, checked 2026-09-25)
