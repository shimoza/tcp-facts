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
# TCP Facts 2026-10-14: smn

- An SMN subscription is added with POST /v2/{project_id}/notifications/topics/{topic_urn}/subscriptions on smn.eu-de.otc.t-systems.com, taking protocol, endpoint and remark. The recorded call used protocol email. (KB-2KS5, live, checked 2026-09-23)
- An SMN email subscription answers 201 and lists status 0 until the recipient clicks the link in the confirmation mail; after the click the subscription list shows status 1. (KB-2UVH, live, checked 2026-09-23)
- An SMN topic can invoke a FunctionGraph function, either as a subscription with the FunctionGraph protocol or through an SMN trigger on the function. A function with VPC access reaches the resources in the VPC bound to it. (KB-4WDK, docs, checked 2026-09-25)
- SMN creates a topic with POST /v2/{project_id}/notifications/topics on smn.eu-de.otc.t-systems.com, taking name and display_name. The response carries the key topic_urn, which the subscription call then uses in its path. (KB-6ZWH, live, checked 2026-09-23)
- SMN HTTP and HTTPS subscriptions accept only public network URLs and public IP addresses, so SMN cannot call a webhook on a private VPC address directly. Besides HTTP and HTTPS the user guide lists email, SMS and FunctionGraph (function) as protocols. (KB-ACTM, docs, checked 2026-09-25)
- Deleting an SMN subscription and creating it again sets its confirmation state back to unconfirmed. (KB-D6RJ, docs, checked 2026-09-25)
- SMN delivers asynchronously without a timeliness guarantee: for an unreachable endpoint it queues the message and tries six more times, at intervals that depend on the queue length, then drops it without telling the publisher. The publish call only returns a message_id and a request_id. (KB-F6ZA, docs, checked 2026-09-25)
- An SMN subscription confirmation token stays valid for 48 hours. (KB-FRLE, docs, checked 2026-09-25)
- According to the SMN user guide, Cloud Eye and Anti-DDoS may publish to the topics of all users by default, while other services such as OBS have to be selected in the topic policy, and the services on offer there vary by region. (KB-LSZZ, docs, checked 2026-09-25)
- Simple Message Notification (SMN) is a scalable, event-driven notification service: the customer defines topics and sends messages to their subscribers manually or automatically by email, text message (SMS) or HTTP/HTTPS. It is used on its own or together with Cloud Eye, Cloud Trace Service and Anti-DDoS. The Regions and Endpoints page lists API endpoints for SMN in eu-de and eu-nl. (KB-M6UB, contract, checked 2026-10-11)
- Per the SMN user guide, an HTTP or HTTPS subscription is confirmed when the subscriber visits the subscribe_url that SMN sends in a SubscriptionConfirmation message, valid for 48 hours. An email subscription is confirmed by opening the link in the confirmation mail, which is also valid for 48 hours. (KB-PPUL, docs, checked 2026-09-25)
- GET /v2/{project_id}/notifications/topics on the SMN endpoint answers HTTP 200 and returns topic_count together with the topic list. (KB-QE47, live, checked 2026-07-02)
- SMN sends email notifications from one fixed no-reply address of the platform domain (noreply at otc.t-systems.com), and a topic display name only sets the sender name shown in front of that address. (KB-SS56, docs, checked 2026-09-25)
- In eu-de on 2026-09-25, GET /v2/{project_id}/notifications/topics/{topic_urn}/attributes?name=access_policy returned an empty access_policy for all three topics of a test project, which matches the documented default, so a topic grants OBS nothing until such a policy is set. (KB-V6YD, live, checked 2026-09-25)
- Through the SMN API the authorization is a topic policy set with PUT /v2/{project_id}/notifications/topics/{topic_urn}/attributes/access_policy, policy version 2016-09-07, with a statement whose Principal is Service obs in lower case and whose Action includes SMN:Publish. The documented sample also grants SMN:QueryTopicDetail. (KB-YRKR, docs, checked 2026-09-25)
