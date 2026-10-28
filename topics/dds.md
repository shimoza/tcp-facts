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
# TCP Facts 2026-10-28: dds

- DDS 4.2, 4.4 and 5.0 run the RocksDB storage engine, while DDS 4.0 runs WiredTiger. (KB-JP6W, docs, checked 2026-09-25)
- DDS is reached with a client driver compatible with MongoDB 3.0 or later. For the distributed transactions of DDS 4.2 and later the version table notes that the MongoDB drivers must be updated for MongoDB 4.2. (KB-ML3K, docs, checked 2026-09-25)
- DDS is a MongoDB-compatible service, not the MongoDB community engine itself: DDS 4.0 (since 16 October 2018) and DDS 4.2 and later use community version 4.0.3 as their baseline and add independently developed features. A DDS version number states compatibility and does not correspond to a community release. (KB-MNLG, docs, checked 2026-09-25)
- Document Database Service (DDS) is a managed document-oriented NoSQL database compatible with MongoDB, with a high availability architecture, disaster recovery failover, online scaling, backup and restore. It is deployed as a single node, as a three-node replica set with automatic failover, or as a sharded cluster with config nodes, shards and mongos nodes. The Regions and Endpoints page lists API endpoints for DDS in eu-de and eu-nl. (KB-OUE6, contract, checked 2026-10-14)
