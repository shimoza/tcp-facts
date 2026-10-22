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
# TCP Facts 2026-10-22: monitoring

- GET /v2/{project_id}/fgs/functions/{urn}/statistics/{period} returns arrays for count, fail_count, duration, max_duration, min_duration, concurrency_num, instance_num and reject_count. The accepted periods are 5, 15 and 60. (KB-DE5J, live, checked 2026-07-30)
