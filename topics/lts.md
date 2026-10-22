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
# TCP Facts 2026-10-22: lts

- Log Tank Service (LTS) is a central cloud logging service that stores log data from many sources in one place and forwards it to Object Storage Service or Distributed Message Service for further processing or archiving. The documentation names real-time collection of host and cloud service logs, keyword and fuzzy log search, alarm reporting and a retention period the customer sets, after which logs are deleted unless transferred to OBS for long-term storage. The Regions and Endpoints page lists API endpoints for LTS in eu-de and eu-nl. (KB-3YYI, contract, checked 2026-10-14)
- GET /v2/{project_id}/groups on the LTS endpoint answers HTTP 200 with a log_groups array. Each entry carries log_group_id, log_group_name and ttl_in_days. (KB-CRKU, live, checked 2026-07-02)
- T Cloud Public (TCP) collects logs centrally in Log Tank Service (LTS): host and cloud service logs are gathered in real time into log groups and streams, searched by keyword, used for alarms, kept for a retention period of 1 to 365 days per log group (KB-XLF6) and transferred to OBS or DMS for longer storage. (KB-MZQU, docs, checked 2026-10-11)
- LTS log group retention is set per group through ttl_in_days and runs from 1 to 365 days, with 30 days as the default. (KB-XLF6, live, checked 2026-07-02)
