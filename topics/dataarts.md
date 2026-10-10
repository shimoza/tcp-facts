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
# TCP Facts 2026-10-10: dataarts

- The CDM API is rate limited to 5 requests per minute and answers APIGW.0308 above that rate. (KB-22H2, live, checked 2026-07-30)
- Incremental file migration in CDM is the destination option toJobConfig.duplicateFileOpType set to SKIP, not a separate incremental flag. In an OBS to OBS test an empty target copied 28 files, an unchanged rerun copied 0 and a run after one new file copied 1. REPLACE recopies everything. (KB-5HTE, live, checked 2026-07-30)
- In eu-de the DataArts Studio endpoint prefixes dayu, dayu-dlf and cdm all resolve to the same address. (KB-6IFY, live, checked 2026-07-30)
- DataArts Factory calls honour only the header named workspace, and it must be inside the AK/SK signature. The variants workspaceId, instance-id and dayu-workspace are ignored and the call answers 200 with an empty job list, while a wrong workspace id answers 400 DLF.0819 Workspace does not exists. (KB-6IM3, live, checked 2026-07-30)
- The endpoint prefixes dataartsstudio, dataarts, dgc, dlf and dayu-cdm have no DNS record in eu-de. (KB-D4PF, live, checked 2026-07-30)
- The service description, revision 17.08.2026, offers DataArts Studio in eu-de as a Starter version without data governance and as an Enterprise version with Data Architecture, Data Quality, Data Catalog, Data Security and Data Service, while its table lists the Data Service (DLM) flavors as n.a. for EU-DE. On the test tenant on 2026-09-25 only the Factory and Migration APIs answered; the documented paths of the other modules returned APIGW.0101. (KB-FEC6, contract, checked 2026-09-25)
- The DataArts Factory error DLF.3025 "The schedule parameter is invalid" is commonly caused by a missing processType field, which is a different field from the schedule parameters. (KB-GBHW, live, checked 2026-07-30)
- DataArts Factory in eu-de rejects the node types MRSHetuEngine and PRESTO with DLF.2013 The processor type parameter is invalid, and HetuEngineSQL as a node with DLF.2014 The job object type is invalid, so a HetuEngine script can be authored but not scheduled natively. (KB-KAFE, live, checked 2026-07-30)
- A DataArts Factory job schedule needs cron.startTime with an ISO 8601 offset, and cron.expressionTimeZone in the GMT+2 form rather than an IANA zone name such as Europe/Berlin. (KB-LGPE, live, checked 2026-07-30)
- A DataArts Studio instance, a workspace and a Migration (CDM) cluster have to be created in the console in eu-de. Everything below those three objects is API-driven. (KB-LONI, live, checked 2026-07-30)
- A DataArts Factory job body requires processType with value BATCH or REAL_TIME. Omitting it returns DLF.3025 The schedule parameter is invalid, which points at the wrong field. (KB-MZN5, live, checked 2026-07-30)
- DataArts Migration skips files that were already transferred when toJobConfig.duplicateFileOpType is set to SKIP, which covers incremental file loads. (KB-O5QK, live, checked 2026-07-30)
- DataArts Factory job listing honours only the workspace request header. With workspaceId, instance-id or dayu-workspace instead, the call answers HTTP 200 with {"jobs":[],"total":0} for the default scope. (KB-PNCE, live, checked 2026-07-30)
- DataArts Studio in eu-de is torn down in the console only: read, delete and stop on a single Factory job answer 404 APIGW.0101, and the deletion is a console chain of jobs, data connection, migration clusters and instance. A service the service description lists can have functions without an API, while an API can still answer for a service no longer offered (BMS). (KB-QSZB, live, checked 2026-07-31)
- DataArts Studio provides CDM for batch data movement and Factory for orchestration, and MRS provides Kafka and Flink for streaming pipelines. (KB-SWZZ, docs, checked 2026-09-25)
- The DataArts CDM job failure "Run fail.Execute rest api job fail." after about 135 seconds points to a missing network route between the CDM agent and the target, for example when the two sit in different VPCs. (KB-TL3G, live, checked 2026-07-30)
- A minute-level cron in a DataArts Factory job needs both a range and an interval. The expression 0 0-59/2 * * * ? is accepted, 0 0/10 * * * ? returns DLF.1006 and 0 */10 * * * ? returns DLF.3025. (KB-TML3, live, checked 2026-07-30)
- On eu-de, HetuEngine is scheduled from DataArts Factory with a generic RESTAPI node that calls the Trino statement API. (KB-UCCW, live, checked 2026-07-30)
- Once a CDM cluster exists, its links and jobs are API-driven in eu-de: GET /v1.1/{project_id}/clusters and /datastores, POST /v1.1/{project_id}/clusters/{cluster_id}/cdm/link (connector-name obs-connector) and /cdm/job, PUT /cdm/job/{name}/start, GET /cdm/job/{name}/status. (KB-V65H, live, checked 2026-07-30)
- In eu-de the DataArts Factory node types HiveSQL, SMN and RESTAPI ran successfully, HiveSQL verified against an MRS cluster. (KB-XHDJ, live, checked 2026-07-30)
- On 2026-09-25 the CDM flavor listing in eu-de (GET /v1.1/{project_id}/datastores/{datastore_id}/flavors) returned five flavors for the current cluster version 2.10.0.300: cdm.small (2 vCPU / 4 GB), cdm.medium (4/8), cdm.large (8/16), cdm.xlarge (16/32) and cdm.4xlarge (64/128). (KB-XI6O, live, checked 2026-09-25)
- A DataArts Factory job in eu-de has no run-on-demand API. A job runs when its schedule fires, or it is started from the console. (KB-XXDO, live, checked 2026-07-30)
