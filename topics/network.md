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
# TCP Facts 2026-10-14: network

- The Meraki vMX 26.1.4 KVM image does not ask a metadata service at 169.254.169.254 for user data: under QEMU with a network it sent no request in 15 minutes, while a control guest did. (KB-3H4S, live, checked 2026-10-01)
- With the MTU raised on one side only, a path MTU bisect returned 1276 bytes, which is not a tunnel limit. It is the far end veth still at 1300 plus the bridge allowance of mtu plus hard_header_len plus VLAN_HLEN, 18 bytes. (KB-3UAP, live, checked 2026-08-26)
- At boot the Meraki vMX 26.1.4 KVM image mounts /dev/sr0 on /mnt/cd. With an ISO labelled cidata on a CD-ROM it logs 'Successfully mounted CDROM for VMX platform', without one 'Failed to mount CDROM for VMX platform'. (KB-D3EJ, live, checked 2026-10-01)
- On 2026-10-07 the public Cisco Meraki documentation and product pages describe the vMX only as a virtual machine (AWS, Azure, GCP, Alibaba Cloud, KVM, ESXi, Private Cloud on UCS). A container or Kubernetes edition of the vMX is not described there; ask Cisco for its name and status. (KB-D6SI, docs, checked 2026-10-07)
- The Meraki vMX 26.1.4 KVM image reads its token only from the CD-ROM device /dev/sr0. The same cidata ISO on a hard disk is not used. (KB-EEL6, live, checked 2026-10-01)
- The managed Secure Mail Gateway service relays outbound mail through the operator's smarthost, requires an SPF entry for the sending domain, and its documentation states that mailing per customer can be limited to 100 mails per minute. (KB-HFAR, docs, checked 2026-09-16)
- The Meraki vMX 26.1.4 KVM image runs a virtio-net NIC as wan0, takes its address by DHCP on it and boots with virtio_net.gso=0 on its kernel command line. (KB-IU6Q, live, checked 2026-10-01)
- The Cisco Meraki vMX on AWS takes its authentication token from EC2 user data: the setup guide has the token entered in the user data field under Advanced Details when the instance is launched. The same guide says the vMX on Azure, GCP and Alibaba Cloud also gets the token from a user-data field in the VM configuration. (KB-JQLW, docs, checked 2026-09-30)
- The Content Delivery Network service of the platform is built on Akamai. Its user guide index carries the title "Content Delivery Network (Akamai)" and the API reference in the mirror is a TODO placeholder. (KB-KXZ7, docs, checked 2026-06-08)
- ARP traverses a VXLAN tunnel between Linux VTEPs by flood and learn. The remote MAC appears in bridge fdb show for the remote VTEP destination, so a stretched subnet works with no L3 route anywhere. (KB-M3JN, live, checked 2026-08-26)
- The Meraki vMX 26.1.4 KVM image boots only with its disk on an AHCI (SATA) controller. Under QEMU it boots on q35 with SATA and on i440FX with an added AHCI controller, but not from IDE or virtio-blk. (KB-NAOF, live, checked 2026-10-01)
- Section 6.5.1 of the TCP service description prices network traffic under exactly three items: VPN, internet inbound and internet outbound. (KB-TJXA, contract, checked 2026-09-11)
- Jumbo frames on the underlay are only needed to keep a guest MTU of 1500, which requires 1550 on the wire. A guest clamped to 1450 runs over a normal 1500 underlay. Over IPsec subtract about 62 bytes of ESP overhead, about 78 bytes with NAT-T. (KB-TZV7, docs, checked 2026-08-26)
- A SonicWall SMA 8200v virtual appliance (firmware 12.5.0-02002, KVM qcow2 build) running as an ECS in eu-de terminated a Connect Tunnel SSL VPN session from a Linux client in another tenant over the internet. The client got an address from a pool inside the VPC subnet and reached RDP on another ECS in that subnet. (KB-VDM3, live, checked 2026-04-15)
- With Linux VTEPs over VPC peering in eu-de a 1500 byte underlay carries an inner IP MTU of 1450. The largest payload passing with DF set is 1422 bytes, which is exactly 1500 on the wire, because the VXLAN headers take 50 bytes. (KB-XUSG, live, checked 2026-08-26)
