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
# TCP Facts 2026-10-10: cci

- A CCI API that answers on eu-de is not proof that CCI can be ordered for production use. The service description, revision 17.08.2026, lists CCI in section 3.12 among the preview and beta versions for testing purposes only, and the CCI user manual still marks it as beta. (KB-KA35, contract, checked 2026-09-25)
- On the CCI endpoint the paths / and /healthz answered HTTP 404 with error code APIGW.0101, so only the published API paths are reachable through the gateway. (KB-XNOI, live, checked 2026-07-02)
