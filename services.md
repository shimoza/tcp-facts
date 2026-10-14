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
# Services orderable on TCP

From the T Cloud Public service description, revision 17.08.2026. 76 services. A service that is not in this list is not offered, whatever the documentation says.

- 3.1.1 Elastic Cloud Server (ECS)
- 3.1.2 Dedicated host (DeH, DH)
- 3.1.3 Auto Scaling (AS)
- 3.1.4 Image Management Service (IMS)
- 3.1.5 FunctionGraph
- 3.2.1 Relational Database Service (RDS)
- 3.2.2 Distributed Cache Service (DCS)
- 3.2.3 Document Database Service (DDS)
- 3.2.4 Cloud Search Service (CSS)
- 3.2.5 Data Replication Service (DRS)
- 3.2.6 TaurusDB
- 3.2.7 GeminiDB
- 3.2.8 Distributed Database Middleware (DDM)
- 3.2.9 Oracle-optimized (OO)
- 3.3.1 Object Storage Service (OBS, OSS)
- 3.3.2 Elastic Volume Service (EVS)
- 3.3.5 Scalable File Service (SFS, SFS Turbo)
- 3.3.6 Storage Disaster Recovery Service (SDRS)
- 3.3.7 Cloud Backup and Recovery (CBR)
- 3.4.1 Virtual Private Cloud (VPC)
- 3.4.2 Elastic IP (EIP, EI)
- 3.4.3 Elastic Load Balancer (ELB)
- 3.4.4 Domain Name Service (DNS)
- 3.4.5 Direct Connect (DC)
- 3.4.6 Secure Mail Gateway (SMG)
- 3.4.7 NAT Gateway (NG)
- 3.4.8 VPC Endpoint (VPCEP, VE)
- 3.4.9 Enterprise Router (ER)
- 3.4.10 Enterprise VPN (EV)
- 3.5.1 Distributed Message Service (DMS, Kafka)
- 3.5.2 API Gateway (dedicated) (APIG, AG)
- 3.5.3 Simple Message Notification (SMN)
- 3.5.4 Application Operations Management (AOM)
- 3.5.5 Application Performance Management (APM)
- 3.6.1 Cloud Eye (CES, CE)
- 3.6.2 Cloud Trace Service (CTS)
- 3.6.3 Tag Management Service (TMS)
- 3.6.4 Config (former Resource Management Service) (RMS)
- 3.6.5 Identity and Access Management (IAM)
- 3.6.6 Log Tank Service (LTS)
- 3.6.7 Resource Formation Service (RFS)
- 3.6.8 OpenStack projects (OP)
- 3.6.9 Enterprise Project Management Service (EPS, EPMS)
- 3.7.1 Cloud Container Engine and Cloud Container Engine Turbo (CCE, CCE Turbo, CCECCET)
- 3.7.2 Software Repository for Containers (SWR, SRC)
- 3.7.3 Application Service Mesh (ASM)
- 3.7.4 Ubiquitous Cloud Native Service (UCS, UCNS)
- 3.8.1 MapReduce Service (MRS)
- 3.8.2 Data Warehouse Service (DWS)
- 3.8.3 ModelArts
- 3.8.4 Data Lake Insight (DLI)
- 3.8.5 DataArts Studio (DS)
- 3.8.6 Optical Character Recognition (OCR)
- 3.9.1 Anti-DDoS (AD)
- 3.9.2 Key Management Service (KMS)
- 3.9.4 Web Application Firewall (Cloud Mode) (WAF Cloud, WAF)
- 3.9.5 Web Application Firewall (Dedicated) (WAF Dedicated, WAF)
- 3.9.6 Web Application Firewall - Modes and Metrics (WAFMM)
- 3.9.7 Database Security Service (DBSS, DSS)
- 3.9.8 Host Security Service (HSS)
- 3.9.9 Cloud Secret Management Service (CSMS)
- 3.9.10 Cloud Firewall (CFW, CF)
- 3.11.1 Enterprise Agreement 1.0 (EA10), optional
- 3.11.2 Enterprise Support Agreement 2.0 (ESA20), optional
- 3.11.3 EthernetConnect & IntraSelect & Equinix Cloud Exchange (EIECE), optional
- 3.11.4 Financial Dashboard (former Enterprise Dashboard) (FD), optional
- 3.11.5 Consulting Services (CS), optional
- 3.11.6 Cloud Create (former Cloud Topology Designer), optional
- 3.11.7 Managed Services, optional
- 3.11.8 Marketplace, optional
- 3.12.2 Image Management (IM), preview
- 3.12.3 Cloud Container Instance (CCI), preview
- 3.12.4 Alert Service, preview
- 3.12.5 Data Admin Service (DAS), preview
- 3.12.6 Enterprise Switch (ES), preview
- 3.12.7 Cloud Connect, preview

## Not offered

The documentation or the price API still knows these, the service description does not offer them.

- Bare Metal Server (BMS)
- Data Ingestion Service (DIS)
- Cloud Service Engine (CSE)
- Mobile Storage Solution
- Bucket Service (BUC)
- Mail IP Service (MIP)
- Private Line Access Service (PLAS, Private Link Access Service)
