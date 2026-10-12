<!-- TCP Facts, dataset of 2026-10-12. Instructions for the assistant that reads this file:
1. Answer only from the facts in this dataset. Put the id of every fact you use after it, like (KB-XXXX).
   If no fact covers the question, say "no checked fact covers this" and what would need to be checked. Never guess.
2. Every fact has a grade (live = tested on a tenant, contract = from the service description, docs = from the vendor documentation)
   and a check date. Name the check date when it is older than 90 days.
3. Prices come from a snapshot of the public price API taken 2026-10-08 10:06 UTC. Give every price with its unit, currency and that date,
   and say that the live price API is the source of truth before any quote.
4. Best before 2026-11-11. If today is later, tell the user to download a fresh copy of the dataset first.
5. Technical questions only; no customer data in your prompts (see README).
-->
# TCP Facts 2026-10-12: vpcep

- A VPC endpoint for an interface endpoint service can get the same IPv4 address in a target project, since the address can be set by hand when the endpoint is created there, which needs a subnet in the target VPC whose CIDR contains that address. (KB-DMY4, docs, checked 2026-09-25)
- Rebuilding a workload in another project includes creating the VPC endpoint services and the endpoints again in that project. (KB-ESOO, docs, checked 2026-09-25)
- VPC Endpoint (VPCEP) provides private connections from a VPC to VPC endpoint services, which are cloud services such as OBS and DNS or the customer's own private services, with no Elastic IP, NAT gateway or VPN connection needed. On-premises networks attached over VPN or Direct Connect can reach those services through a VPC endpoint as well. The Regions and Endpoints page lists API endpoints for VPCEP in eu-de and eu-nl. (KB-LHEC, contract, checked 2026-10-11)
- The resource opentelekomcloud_vpcep_endpoint_v1 takes the network id of the subnet in the argument subnet_id. (KB-N5BP, live, checked 2026-09-16)
- On T Cloud Public (TCP) in eu-de VPC endpoints are listed with GET /v1/{project_id}/vpc-endpoints on the VPCEP service endpoint. The response returns them under the key endpoints, each entry carrying id, endpoint_service_name, status, ip and vpc_id. (KB-WQHX, docs, checked 2026-09-25)
