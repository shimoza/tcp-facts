<!-- TCP Facts, dataset of 2026-11-23. Instructions for the assistant that reads this file:
1. Answer only from the facts in this dataset. Put the id of every fact you use after it, like (KB-XXXX).
   If no fact covers the question, say "no checked fact covers this" and what would need to be checked. Never guess.
2. Every fact has a level (V4 kept live, V3 live, V2 contract, V1 docs, V0 recheck due; see README) and a check date.
   Name the level when it is V0 and the check date when it is older than 90 days.
3. The dataset holds no price list. Prices come live from the public price API. Give every price with its unit, currency
   and the date of its source, and say that the live price API is the source of truth before any quote.
4. Best before 2026-12-23. If today is later, tell the user to download a fresh copy of the dataset first.
5. Technical questions only; no customer data in your prompts (see README).
-->
# TCP Facts 2026-11-23: storage

- In eu-de the SFS Capacity-Oriented create POST /v2/{project_id}/shares on the sfs endpoint answers HTTP 404 APIGW.0101 "The API does not exist: method POST not found", with and without the header X-Openstack-Manila-Api-Version (2.28 and 2.9), while GET /v2/{project_id}/shares on the same endpoint answers 200 with an empty list; GET /v2/{project_id}/types answers 404. (KB-5J3S, V3 live, checked 2026-11-22)
- The SFS user guide of T Cloud Public (TCP) says that SFS Turbo file systems cannot be mounted to Windows ECSs and that SFS General Purpose file systems cannot be mounted to Windows servers; only SFS Capacity-Oriented is mounted on Windows, with the Windows Client for NFS over TCP, hard mounts and mount -o nolock. (KB-EOVB, V1 docs, checked 2026-11-21)
- Between two Windows Server 2022 ECS on s7n.xlarge.2 in one eu-de subnet, an SMB share on an SSD EVS data disk of the file server served a CAD-like tree of 20,000 files of 2 to 50 KB in 200 folders as follows: create about 143 s against about 50 s on the client's own SSD data disk, reading every file once 125 to 132 s against 1 to 2 s locally, one small file read median about 7 ms idle and p95 about 90 ms during a 1 GB copy to the share, the 1 GB copy about 3 to 4 s, and five saves of a 200 MB file with rename to a numbered backup about 4 s. (KB-ZR3G, V3 live, checked 2026-11-22)
