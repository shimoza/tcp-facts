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
# TCP Facts 2026-10-10: lts

- GET /v2/{project_id}/groups on the LTS endpoint answers HTTP 200 with a log_groups array. Each entry carries log_group_id, log_group_name and ttl_in_days. (KB-CRKU, live, checked 2026-07-02)
- LTS log group retention is set per group through ttl_in_days and runs from 1 to 365 days, with 30 days as the default. (KB-XLF6, live, checked 2026-07-02)
