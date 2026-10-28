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
# TCP Facts 2026-10-28: dli

- On POST /v3/{project_id}/elastic-resource-pools, DLI requires max_cu to equal min_cu. A pool with min 16 and max 64 returned DLI.0035 about insufficient CU quota, while 16/16 with the basic spec label returned HTTP 200 and reached AVAILABLE in roughly ten minutes. (KB-2NIV, live, checked 2026-07-28)
- Creating a DLI elastic resource pool requires max_cu equal to min_cu: 16/64 returns DLI.0035 while 16/16 returns HTTP 200. The pool reaches AVAILABLE in roughly ten minutes. (KB-3XJB, live, checked 2026-07-28)
- GET /v1.0/{project_id}/queues on DLI in eu-de showed the default queue reporting support_spark_versions of 2.4.5 on the date of the check. Queues are created with POST /v1.0/{project_id}/queues, and DELETE /v1.0/{project_id}/queues/{name} returned HTTP 200. (KB-4XEJ, live, checked 2026-07-28)
- In eu-de a general DLI queue listed support_spark_versions 2.4.5 and 3.1.1 with default_spark_version 2.4.5, while the default sql queue listed 2.4.5 only. A submit using Spark 3.3.1 was refused, so these fields report a default rather than everything a submit accepts. (KB-5ENU, live, checked 2026-07-29)
- On the shared default DLI queue statements sit in LAUNCHING for 15 minutes and longer, and the submit call gives up with DLI.0019 "Get sync job result timeout". The job id remains recoverable from that error text. (KB-7NI7, live, checked 2026-07-28)
- On a dedicated DLI queue in eu-de, an Iceberg table creation is rejected with "DLI.0007: Only support 'USING' PARQUET/ORC/JSON/CSV/HUDI/DELTA for create non dli table", while Parquet and ORC controls pass in the same run. HUDI and DELTA are accepted although the documentation lists only CSV, Parquet, ORC, JSON and Avro. (KB-D554, live, checked 2026-07-28)
- Data Lake Insight (DLI) is a serverless big data query and analysis service compatible with Apache Spark and Apache Flink that runs SQL statements and Spark applications on heterogeneous data sources. Jobs run on non-dedicated queues, which take resources only while a job runs, or on dedicated queues that run around the clock until deleted. The Regions and Endpoints page lists the DLI API endpoint in eu-de. (KB-D6ZP, contract, checked 2026-10-14)
- A DLI elastic resource pool needs a minimum CU strictly greater than the sum of the minimum CU of the queues registered in it. A 16 CU pool therefore rejects a 16 CU queue while another queue is still registered. (KB-HNQS, live, checked 2026-07-29)
- GET /v1.0/{pid}/queues without a filter returned only the default sql queue in eu-de. General queues appeared through GET /v1.0/{pid}/queues?queue_type=general, GET /v3/{pid}/elastic-resource-pools/{pool}/queues or GET /v1.0/{pid}/queues/{name}. (KB-JYDX, live, checked 2026-07-29)
- PUT /v3/{pid}/elastic-resource-pools/{name} resizing a DLI elastic resource pool to 64 CU returned DLI.0035, insufficient resources, in eu-de. (KB-MLOK, live, checked 2026-07-29)
- POST /v1.0/{project_id}/jobs/submit-job on DLI is synchronous. On a congested queue it gives up with HTTP 408 and DLI.0019 "Get sync job result timeout with id", but the job id in that message is a real job that can still be polled at /jobs/{id}/status. (KB-NXZH, live, checked 2026-07-28)
- On DLI, POST /v1.0/{project_id}/databases returns HTTP 200 on a tenant that has not used the service before, while GET /v1.0/{project_id}/databases can return HTTP 400 with DLI.0999 on such an unprovisioned tenant. (KB-PTKT, live, checked 2026-07-28)
- GET /v1.0/{project_id}/jobs with limit and sort=start_time_desc returns DLI job outcomes, including a message field that carries the SQL error text. It is the reliable way to read a job result after a synchronous submit times out. (KB-PXT2, live, checked 2026-07-28)
- A DLI job reads Iceberg tables when the Iceberg jar is supplied with the job itself. (KB-WBCZ, live, checked 2026-07-30)
