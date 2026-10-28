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
# TCP Facts 2026-10-28: swr

- Software Repository for Containers (SWR) is a managed private container image registry: container images are uploaded, downloaded and removed through the console or the Docker CLI. The documentation adds private repositories with read, write and edit permissions per user, use together with Cloud Container Engine or on its own, and faster image pulls for CCE clusters. The Regions and Endpoints page lists API endpoints for SWR in eu-de and eu-nl. (KB-6MXP, contract, checked 2026-10-14)
- The SWR organisation quota is 5 per account and is read at GET /v2/manage/projects/{project_id}/quotas. (KB-7OJD, live, checked 2026-07-02)
- The SWR user manual returns zero hits for vulnerability, CVE and image scanning, so SWR itself performs no container image scanning. (KB-FJ2L, docs, checked 2026-10-14)
- The SWR feature gates read on eu-de on 2026-09-25 returned enable_image_scan false, enable_hss_service false, enable_cci_service false and enable_image_sync false, so image vulnerability scanning and the SWR to CCI hookup were switched off for that account. (KB-MWNP, live, checked 2026-09-25, recheck due)
- GET /v2/manage/projects/{project_id}/feature-gates on swr-api.eu-de.otc.t-systems.com returns per-domain service enablement flags, for example enable_hss_service, which show whether the API gateway lets a service through for that domain. (KB-OIJ5, live, checked 2026-09-02)
- SWR accepts two docker login forms. A temporary secret valid 24 hours comes from POST /v2/manage/utils/secret and arrives in the X-Swr-Dockerlogin response header. A long term login valid one year uses the region name plus the access key as user name and an HMAC-SHA256 of the access key, keyed with the secret key, as password. (KB-R2VK, live, checked 2026-07-02)
- T Cloud Public (TCP) offers a private container registry in Software Repository for Containers (SWR): container images are pushed, pulled and deleted with the Docker CLI or the console in the customer's own namespaces and repositories. Docker login with a temporary secret or a long-term login derived from an access key was tested live in eu-de (KB-R2VK). (KB-U7YD, contract, checked 2026-10-14)
- SWR management calls run against the swr-api host on eu-de. GET /v2/manage/repos, GET /v2/manage/namespaces and GET /v2/manage/projects/{project_id}/feature-gates each answered HTTP 200. Image pull and push use the separate swr registry host. (KB-ZG4G, live, checked 2026-07-02)
