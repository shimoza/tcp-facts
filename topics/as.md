<!-- TCP Facts, dataset of 2026-11-16. Instructions for the assistant that reads this file:
1. Answer only from the facts in this dataset. Put the id of every fact you use after it, like (KB-XXXX).
   If no fact covers the question, say "no checked fact covers this" and what would need to be checked. Never guess.
2. Every fact has a level (V4 kept live, V3 live, V2 contract, V1 docs, V0 recheck due; see README) and a check date.
   Name the level when it is V0 and the check date when it is older than 90 days.
3. The dataset holds no price list. Prices come live from the public price API. Give every price with its unit, currency
   and the date of its source, and say that the live price API is the source of truth before any quote.
4. Best before 2026-12-16. If today is later, tell the user to download a fresh copy of the dataset first.
5. Technical questions only; no customer data in your prompts (see README).
-->
# TCP Facts 2026-11-16: as

- Auto Scaling (AS) is a service that automatically scales Elastic Cloud Server instances and bandwidth out and in by conditions the customer sets. Scaling is triggered by alarm-based policies on Cloud Eye metrics such as vCPU, memory, disk or inbound traffic, by scheduled policies or by periodic policies, and AS works together with Elastic Load Balancer, Elastic Volume Service and Elastic IP. The Regions and Endpoints page lists API endpoints for AS in eu-de and eu-nl. (KB-4COH, V2 contract, checked 2026-10-14)
- The Auto Scaling API of T Cloud Public (TCP) sets instance protection with POST /autoscaling-api/v1/{project_id}/scaling_group_instance/{scaling_group_id}/action and the actions PROTECT and UNPROTECT, and removes instances with REMOVE and instance_delete yes or no; only INSERVICE instances can be protected or removed, and a removal works only while no scaling action is in progress and the group stays at or above its minimum number. (KB-5BHI, V1 docs, checked 2026-11-12)
- Instance protection in TCP Auto Scaling keeps a protected instance from being removed by an automatic scale-in. It does not protect against manual removal or health check replacement, it is off by default on new instances and it is lost when the instance leaves the group. (KB-ABMF, V1 docs, checked 2026-11-12)
- An Auto Scaling group on T Cloud Public (TCP) takes up to five lifecycle hooks of the types Instance adding and Instance removal. A hook holds the instance in a wait state for a timeout of 60 to 86,400 seconds or until a callback (Continue or Abandon), and it can send a Simple Message Notification message with a token. (KB-C5JC, V1 docs, checked 2026-11-12)
- An Auto Scaling alarm policy on T Cloud Public (TCP) is created with scaling_policy_type ALARM and the alarm_id of an existing Cloud Eye alarm rule; AS then adds an autoscaling action to that alarm rule. The page does not say whether the alarm rule may be one on a custom metric. (KB-NJB7, V1 docs, checked 2026-11-12)
- The user_data field of an Auto Scaling configuration on T Cloud Public (TCP) is base64 encoded and limited to 32 KB before encoding; when key_name and user_data are both set, user_data only injects user data. (KB-UBP3, V1 docs, checked 2026-11-12)
- On 2026-11-12 the Auto Scaling quota call on a TCP test tenant in eu-de returned 1250 AS groups and 1250 AS configurations (1 used each), 50 policies and 200 instances per group, which differs from the 25 groups and 100 configurations of the Auto Scaling constraints page. (KB-WWOA, V3 live, checked 2026-11-12)
- The instance removal policies of TCP Auto Scaling choose by age and by AS configuration (oldest instance, newest instance, oldest or newest instance created from the oldest AS configuration). None of them chooses by a load or session metric, so a scale-in that must take an empty session host needs instance protection or a manual removal of the named instance. (KB-XJYB, V1 docs, checked 2026-11-12)
