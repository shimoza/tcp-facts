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
# TCP Facts 2026-10-10: sfs

- Scalable File Service on T Cloud Public (TCP) offers NFSv3 access only. SFS Capacity-Oriented, SFS Turbo and General Purpose file systems expose no SMB or CIFS share, and general purpose file systems cannot be mounted to Windows servers. (KB-7TPW, docs, checked 2026-08-24)
