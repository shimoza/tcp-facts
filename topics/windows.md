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
# TCP Facts 2026-10-28: windows

- A restored Windows server answered RDP after 235 seconds on Server 2019 and 269 seconds on Server 2022 at first boot. A cold rebuild of the same shape took 152 seconds. (KB-2IE5, live, checked 2026-09-02)
- The attack surface reduction rule that blocks credential stealing from LSASS is documented as an equivalent of RunAsPPL LSA Protection rather than a layer added on top of it. (KB-4LLB, docs, checked 2026-06-11)
- Software can be installed on a Windows ECS from an ISO held in OBS: the ISO is pulled into the guest with rclone, mounted with the PowerShell cmdlet Mount-DiskImage -PassThru, installed from the mounted drive letter and released with Dismount-DiskImage. (KB-4VOL, live, checked 2026-06-17)
- LiDAR360 from GreenValley uses a node-locked license key with online activation through its License Manager. The key binds to the machine, and moving it requires a return or deactivation on the old machine before activation on the new one. (KB-7DW6, live, checked 2026-06-17)
- On Windows Server 2025 an ECS that is reachable only over RDP cannot complete a forced first-logon password change. The server requires NLA by default and the client stops with error 0x1207, password must be changed before logging on. (KB-EDZM, live, checked 2026-06-11)
- A restored Windows server brings its data disk up Offline because of the SAN policy OfflineShared. Setting san policy=OnlineAll before the full-ECS image is created fixes this once in the image instead of at each restore. (KB-F535, docs, checked 2026-09-02)
- Client Windows images such as Windows 10 and Windows 7 may only be used to create ECS on a Dedicated Host. The service description additionally limits bring-your-own Microsoft Windows and SQL Server licences to Physical and Dedicated Hosts. (KB-O4J5, contract, checked 2026-06-10)
