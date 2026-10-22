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
# TCP Facts 2026-10-22: gaussdb

- TaurusDB is not available in eu-nl: on 2026-09-25 its API answered HTTP 404 APIGW.0101 on the eu-nl endpoint, while the endpoint list names TaurusDB for eu-de only. (KB-7Y6M, live, checked 2026-09-25)
- GeminiDB is a managed cloud-native NoSQL database with decoupled compute and storage that is compatible with Apache Cassandra, InfluxDB and DynamoDB. GeminiDB for Cassandra supports the Cassandra Query Language (CQL) and the InfluxDB-compatible variant serves time-series data; the service description of 09.10.2026 announces the DynamoDB-compatible flavors as expected to be available from 1 November 2026. The documentation describes deployment of nodes across three availability zones, backup and restore, and monitoring with alarms. The Regions and Endpoints page lists the GeminiDB API endpoint in eu-de. (KB-FJQ6, contract, checked 2026-10-14)
- TaurusDB is compatible with MySQL 8.0 and decouples compute from storage: one instance holds up to 128 TB and consists of one primary node and up to 15 read replicas on the same shared storage. No storage size is set when an instance is created. (KB-MNIA, docs, checked 2026-09-25)
- TaurusDB is a managed distributed relational database for enterprise requirements that is compatible with MySQL (MySQL 8.0 per the engine table) and decouples compute from storage for high scalability and storage capacity. An instance has one primary (write) node and several read replicas on shared storage, and the documentation gives up to 128 TB of storage per instance. The Regions and Endpoints page lists the TaurusDB API endpoint in eu-de. (KB-RVSG, contract, checked 2026-10-14)
- In eu-de TaurusDB offered engine version 8.0 (MySQL 8.0.22) on 2026-09-25 with six x86 flavors from 2 vCPU and 8 GB to 64 vCPU and 512 GB RAM. The flavors were on sale in eu-de-01 and eu-de-03 and unsupported in eu-de-02. (KB-UN55, live, checked 2026-09-25)
- DRS migrates MySQL 5.5, 5.6, 5.7 and 8.0 databases from RDS for MySQL, ECS, on-premises or other clouds to TaurusDB cluster instances in real time. (KB-YL3W, docs, checked 2026-09-25)
