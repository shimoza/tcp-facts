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
# TCP Facts 2026-10-22: ms-licensing

- The Microsoft clause of the T Cloud Public (TCP) service description names Windows Server 2016, 2019 and 2022 as the sublicensed versions. (KB-6EWX, contract, checked 2026-10-14)
- A full-text search of the T Cloud Public (TCP) service description, revision 09.10.2026, for remote desktop, terminal, multi-session and session host returned zero hits. The platform documentation mentions the Remote Desktop Session Host role only in RDP troubleshooting FAQs for Windows ECS, for example removing the role when the 120-day licensing grace period ends. (KB-DXKH, contract, checked 2026-10-14)
- Self-managed SQL Server under bring-your-own-license runs on Dedicated Host or physical servers. (KB-PWIV, contract, checked 2026-10-14)
- Remote Desktop Services client access licences (RDS CAL) and SAL subscriptions are not price-list items on T Cloud Public (TCP) in eu-de and have to be brought from outside the platform. (KB-RBRL, live, checked 2026-09-25)
- The service description, section 3.1.4.2 in revision 09.10.2026, limits customer-owned Microsoft Windows Server and Microsoft SQL Server licences to Physical and Dedicated Hosts. (KB-SOBG, contract, checked 2026-10-14)
- The ECS price listing (sn=ecs) of eu-de carried six operating system tiers on each of its 66 flavors on 2026-09-24: Open Linux, Oracle Linux, RedHat Linux, SUSE Linux, SUSE for SAP and Windows. None of the six ECS service names carried a SQL Server line; SQL Server appears under rds and ms-man-db. (KB-WFB7, live, checked 2026-09-24)
- Bring-your-own Microsoft SQL Server licenses are accepted only on Dedicated Hosts (DeH) or physical servers, so a self-managed SQL Server on ECS under BYOL needs one of those. (KB-XQQY, contract, checked 2026-10-14)
