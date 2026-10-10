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
# TCP Facts 2026-10-10: swr

- The SWR organisation quota is 5 per account and is read at GET /v2/manage/projects/{project_id}/quotas. (KB-7OJD, live, checked 2026-07-02)
- The SWR feature gates read on eu-de on 2026-09-25 returned enable_image_scan false, enable_hss_service false, enable_cci_service false and enable_image_sync false, so image vulnerability scanning and the SWR to CCI hookup were switched off for that account. (KB-MWNP, live, checked 2026-09-25)
- GET /v2/manage/projects/{project_id}/feature-gates on swr-api.eu-de.otc.t-systems.com returns per-domain service enablement flags, for example enable_hss_service, which show whether the API gateway lets a service through for that domain. (KB-OIJ5, live, checked 2026-09-02)
- SWR accepts two docker login forms. A temporary secret valid 24 hours comes from POST /v2/manage/utils/secret and arrives in the X-Swr-Dockerlogin response header. A long term login valid one year uses the region name plus the access key as user name and an HMAC-SHA256 of the access key, keyed with the secret key, as password. (KB-R2VK, live, checked 2026-07-02)
- SWR management calls run against the swr-api host on eu-de. GET /v2/manage/repos, GET /v2/manage/namespaces and GET /v2/manage/projects/{project_id}/feature-gates each answered HTTP 200. Image pull and push use the separate swr registry host. (KB-ZG4G, live, checked 2026-07-02)
