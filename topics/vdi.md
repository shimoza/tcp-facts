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
# TCP Facts 2026-11-23: vdi

- In the oneclick console the group OC Deployment is described as opening RDP for the vendor addresses, but on TCP the group allowed all protocols and ports from its four /32 addresses; the session from oneclick reaches the VM by RDP on the VM's public address, so a VM taken over needs an EIP and inbound access from those addresses. (KB-2RGP, V3 live, checked 2026-11-16)
- The onboarding of a tenant to the oneclick VDI platform starts in IAM on the customer side: a console user creates an IAM user, a user group, two role assignments to the group and the membership, about 5 minutes before the platform's first API call; no IAM change came from the platform itself. (KB-CV5P, V3 live, checked 2026-11-16)
- The oneclick VDI platform reaches existing VMs from its own public IPs through a firewall rule it adds and runs processes over WinRM; VMs without a public IP need a jump host, its gateway or its Mesh client on UDP 4242. It supports Windows Server 2019 to 2025 multi-session with FSLogix, own load balancing without a Connection Broker, scheduled start and stop and load-based scaling from a golden image; NVIDIA vGPU on TCP is not described in its public documentation. (KB-MU7R, V1 docs, checked 2026-11-16)
- Right after a tenant was attached to the oneclick VDI platform, a security group OC_Deployment_<id> without VPC appeared in the project with ingress of all protocols and ports from four public /32 addresses of the vendor and egress to 0.0.0.0/0; it was not yet bound to existing servers. (KB-NEBL, V3 live, checked 2026-11-16)
- When a tenant is attached to the oneclick VDI platform, the platform adds its own security group OC_Deployment_<id> to the ports of existing servers it takes over (VPC modifyPort, one call per server) and keeps the groups they already carry; the group allows all protocols and ports from four vendor /32 addresses, and the platform also adds explicit TCP 3389 rules from the same four addresses, about 5 minutes after its first API call. (KB-VCLX, V3 live, checked 2026-11-16)
- The API calls of the oneclick VDI platform on TCP appear in Cloud Trace Service under its IAM user with TCP-internal source addresses from the 100.64.0.0/10 range, not with the vendor's public addresses; it began with about 40 IMS listImages calls within one minute before it changed any port. (KB-XCPZ, V3 live, checked 2026-11-16)
- The oneclick VDI platform runs on TCP as a SaaS of its vendor, a TCP partner: the customer's tenant is attached with an IAM user with programmatic access and the roles IAM ReadOnlyAccess and Tenant Administrator, and the platform then creates VMs and its own security groups and removes the default security group from a VM; no TCP marketplace image and no self-installation. (KB-XHM4, V1 docs, checked 2026-11-16)
