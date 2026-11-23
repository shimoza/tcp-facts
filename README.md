<h1 align="center">TCP Facts</h1>

<p align="center"><b>Checked facts about T Cloud Public (TCP) for any AI assistant, dataset of 2026-11-23</b><br>A product of the <a href="https://github.com/shimoza/tcp-awb">Architect Workbench</a>, the open source TCP harness that builds and checks these facts</p>

> **Unofficial and independent.** Not a product of, and not endorsed by, T-Systems or Deutsche Telekom; it speaks for nobody but its author. Built only from public sources (the public documentation, the public service description, the public price API), with respect for robots.txt and the terms of those sources. No customer data and no confidential information. No warranty: the provider's contract documents are binding.

<p align="center">Claude Desktop, one click: <a href="https://github.com/shimoza/tcp-facts/releases/latest/download/tcp-facts.mcpb">tcp-facts.mcpb</a> (needs Python 3.10 or newer)</p>

<p align="center">
  <img alt="Unofficial" src="https://img.shields.io/badge/Status-Unofficial-c64a3d">
  <img alt="Facts: 2177" src="https://img.shields.io/badge/Facts-2177-2f6fd1">
  <img alt="Best before: 2026-12-23" src="https://img.shields.io/badge/Best_before-2026--12--23-e0b43a">
  <img alt="License: CC BY 4.0" src="https://img.shields.io/badge/License-CC_BY_4.0-3f9d5a">
  <a href="#mcp-clients"><img alt="MCP server" src="https://img.shields.io/badge/MCP-server-8a63b8"></a>
</p>

Build of 2026-11-23 06:01 UTC. A later build of the same day replaces this one under the same name; the manifest carries the build time.

2177 checked facts about T Cloud Public (TCP) with the list of orderable services. Made to be dropped into any AI assistant. Prices are not part of the dataset: they come live from the public price API with --live.

1493 facts were tested live on a TCP tenant, 515 come from the vendor documentation and 169 from the service description (revision 18.11.2026). No fact from hearsay, no customer, no project, no credential.

398 of the 515 documentation facts come from the open source repositories of the GitHub organisation opentelekomcloud-docs, published under the Apache License 2.0. The public source of each of the others is in facts.jsonl. The documentation website is not crawled, its robots.txt disallows all robots. Sources whose terms forbid automated analysis are not used, so the community portal and internal documentation are left out. The live checks ran on the compiler's own TCP test tenants.


## Use

Attach facts.md and type:

```
Use the attached TCP Facts. Answer: <your question>
```

PROMPT.md has the rest.


## What the facts cover

76 of the 76 services orderable per the service description of 18.11.2026 have at least one plain fact that says what the service is and does: a statement that opens with the name of the service. By section of the service description:

- Computing: 5 of 5

- Databases: 9 of 9

- Storage: 5 of 5

- Network: 10 of 10

- Application: 5 of 5

- Management & Deployment: 9 of 9

- Container: 4 of 4

- Data analysis: 6 of 6

- Security: 9 of 9

- Optional services: 8 of 8

- Preview and beta versions: 6 of 6

17 facts state what the platform covers for a requirement area. Each opens with "T Cloud Public (TCP)" and names the services that cover it:

- collects logs centrally (KB-MZQU)

- connects on-premises networks by site-to-site VPN and by dedicated lines (KB-XSZD)

- keeps audit logs of management actions (KB-MF3H)

- manages users, user groups and federation (KB-D64T)

- monitors resources and raises alarms (KB-L4FW)

- offers a private container registry (KB-U7YD)

- offers a web application firewall (KB-KIAP)

- offers key management with customer-managed and customer-supplied keys (KB-KUZK)

- offers load balancing at layer 4 and layer 7 (KB-HZXL)

- offers managed Kubernetes (KB-OOVV)

- offers managed relational databases (KB-33UY)

- offers object storage for archive use (KB-JMBA)

- offers shared file storage over NFS (KB-TX7A)

- provides virtual machines (KB-EPEA)

- runs scheduled backups with a set retention period (KB-ITGL)

- supports infrastructure as code (KB-V42N)

- supports multi-factor authentication (KB-TFIN)

Example: to check whether TCP covers a requirement, attach facts.md and ask:

```
Use the attached TCP Facts. Answer: is this requirement covered: "TCP collects logs centrally"? Cite the id of every fact that backs the answer.
```

A good answer quotes the fact and its id, for example (KB-MZQU) for this one, so a reader finds it in facts.md. When no fact covers the requirement it says "no checked fact covers this".

What the dataset does not hold and never will: commitments on certificates and attestations, SLA values, support hours and response times, prices and subcontractors. These are contract matters: check them in the contract. A fact that touches one of them is background from a public source, not a commitment.


## Validation levels

Every fact carries one level, after its id in facts.md and as "level" in facts.jsonl. The level follows from the grade, the check block and the check date of the fact, nothing else.

| level | what it means | how it stays true | facts |
|---|---|---|---|
| V4 kept live | Tested live on a TCP tenant and inside its check period. | A check block repeats the test every week by itself. | 67 |
| V3 live | Tested live on a TCP tenant and inside its check period. | No check block yet: it is tested again when it expires. | 1239 |
| V2 contract | Stated by the current service description and inside its check period. | Checked again when the service description gets a new revision. | 1 |
| V1 docs | Taken from the vendor documentation and inside its check period. | Checked again when its documentation page changes or when it expires. | 437 |
| V0 recheck due | Past its check date, or a recheck contradicted it. | Use it only with its check date and say that it waits for a recheck. | 433 |


## Facts with a recheck due

433 facts are past their expiry date and wait for their weekly recheck. They stay in the dataset until something invalidates them: a recheck that refutes them, a newer fact that replaces them or a change of the service description. Name the check date when you use one.

| fact | grade | checked | state |
|---|---|---|---|
| KB-2ZZR | live | 2026-02-04 | recheck due |
| KB-37RS | live | 2026-02-04 | recheck due |
| KB-46C6 | live | 2026-02-04 | recheck due |
| KB-6FEI | live | 2026-02-04 | recheck due |
| KB-BS7A | live | 2026-02-04 | recheck due |
| KB-CGCI | live | 2026-02-04 | recheck due |
| KB-DOPL | live | 2026-02-04 | recheck due |
| KB-E5HH | live | 2026-02-04 | recheck due |
| KB-GBEV | live | 2026-02-04 | recheck due |
| KB-LWS5 | live | 2026-02-04 | recheck due |
| KB-N72X | live | 2026-02-04 | recheck due |
| KB-P6FC | live | 2026-02-04 | recheck due |
| KB-PAUD | live | 2026-02-04 | recheck due |
| KB-RGV4 | live | 2026-02-04 | recheck due |
| KB-RY24 | live | 2026-02-04 | recheck due |
| KB-XKBA | live | 2026-02-04 | recheck due |
| KB-XXAD | live | 2026-02-04 | recheck due |
| KB-YPPS | live | 2026-03-04 | recheck due |
| KB-LJFS | live | 2026-03-07 | recheck due |
| KB-H7UG | live | 2026-03-10 | recheck due |
| KB-4V7Z | live | 2026-05-01 | recheck due |
| KB-6IAO | live | 2026-05-01 | recheck due |
| KB-7AIC | live | 2026-05-01 | recheck due |
| KB-CZH3 | live | 2026-05-01 | recheck due |
| KB-DDGQ | live | 2026-05-01 | recheck due |
| KB-DWRX | live | 2026-05-01 | recheck due |
| KB-E3O4 | live | 2026-05-01 | recheck due |
| KB-FSXW | live | 2026-05-01 | recheck due |
| KB-QDQE | live | 2026-05-01 | recheck due |
| KB-SD7O | live | 2026-05-01 | recheck due |
| KB-TTWD | live | 2026-05-01 | recheck due |
| KB-EDXJ | live | 2026-05-06 | recheck due |
| KB-5GI3 | live | 2026-05-07 | recheck due |
| KB-65QI | live | 2026-05-07 | recheck due |
| KB-5VMM | docs | 2026-05-20 | recheck due |
| KB-BETZ | docs | 2026-05-20 | recheck due |
| KB-LE6N | docs | 2026-05-20 | recheck due |
| KB-MEQU | live | 2026-05-20 | recheck due |
| KB-NGJR | docs | 2026-05-20 | recheck due |
| KB-NKEB | docs | 2026-05-20 | recheck due |
| KB-SDB5 | docs | 2026-05-20 | recheck due |
| KB-W72N | docs | 2026-05-20 | recheck due |
| KB-475G | live | 2026-05-22 | recheck due |
| KB-6ELY | live | 2026-05-22 | recheck due |
| KB-7IPK | live | 2026-05-22 | recheck due |
| KB-NEKR | live | 2026-05-22 | recheck due |
| KB-OI2G | live | 2026-05-22 | recheck due |
| KB-SCS5 | live | 2026-05-22 | recheck due |
| KB-5A7O | live | 2026-05-26 | recheck due |
| KB-FA4K | live | 2026-05-26 | recheck due |
| KB-KG3S | live | 2026-05-26 | recheck due |
| KB-KYXU | live | 2026-05-26 | recheck due |
| KB-NQ7B | live | 2026-05-26 | recheck due |
| KB-PJVB | live | 2026-05-26 | recheck due |
| KB-ZT4C | live | 2026-05-26 | recheck due |
| KB-O4J5 | contract | 2026-06-10 | recheck due |
| KB-MJ5A | docs | 2026-06-12 | recheck due |
| KB-OTPK | contract | 2026-06-29 | recheck due |
| KB-FZRN | contract | 2026-07-01 | recheck due |
| KB-IDKJ | contract | 2026-07-01 | recheck due |
| KB-ZJ4B | contract | 2026-07-01 | recheck due |
| KB-FBVR | contract | 2026-07-05 | recheck due |
| KB-HOSK | contract | 2026-07-05 | recheck due |
| KB-SUE5 | contract | 2026-07-05 | recheck due |
| KB-DFXG | contract | 2026-07-15 | recheck due |
| KB-HT72 | live | 2026-07-17 | recheck due |
| KB-MQ2H | live | 2026-07-17 | recheck due |
| KB-BUI2 | live | 2026-07-21 | recheck due |
| KB-22JC | live | 2026-07-28 | recheck due |
| KB-2X6J | live | 2026-07-28 | recheck due |
| KB-BJMP | live | 2026-07-28 | recheck due |
| KB-ECWX | live | 2026-07-28 | recheck due |
| KB-HQC7 | live | 2026-07-28 | recheck due |
| KB-NSFM | live | 2026-07-28 | recheck due |
| KB-XIWQ | live | 2026-07-28 | recheck due |
| KB-Z3UG | live | 2026-07-28 | recheck due |
| KB-2XCG | live | 2026-07-30 | recheck due |
| KB-46JJ | live | 2026-07-30 | recheck due |
| KB-GA5U | live | 2026-07-30 | recheck due |
| KB-HYY7 | live | 2026-07-30 | recheck due |
| KB-5IOB | live | 2026-08-18 | recheck due |
| KB-62LJ | docs | 2026-08-19 | recheck due |
| KB-T7WI | docs | 2026-08-21 | recheck due |
| KB-WTCR | docs | 2026-08-21 | recheck due |
| KB-L5JU | docs | 2026-08-25 | recheck due |
| KB-PASA | docs | 2026-08-25 | recheck due |
| KB-QMAT | docs | 2026-08-25 | recheck due |
| KB-W6A3 | docs | 2026-08-25 | recheck due |
| KB-3CKT | contract | 2026-08-27 | recheck due |
| KB-EI4V | contract | 2026-08-27 | recheck due |
| KB-TPA7 | contract | 2026-08-27 | recheck due |
| KB-VUL6 | live | 2026-08-27 | recheck due |
| KB-DIDW | live | 2026-09-01 | recheck due |
| KB-QIV4 | contract | 2026-09-01 | recheck due |
| KB-IP74 | live | 2026-09-02 | recheck due |
| KB-T4MF | contract | 2026-09-02 | recheck due |
| KB-ZPJG | contract | 2026-09-08 | recheck due |
| KB-JN3T | contract | 2026-09-09 | recheck due |
| KB-UWKH | contract | 2026-09-09 | recheck due |
| KB-XQFT | contract | 2026-09-09 | recheck due |
| KB-6HHT | contract | 2026-09-11 | recheck due |
| KB-6JVL | contract | 2026-09-11 | recheck due |
| KB-AH5P | contract | 2026-09-11 | recheck due |
| KB-TJXA | contract | 2026-09-11 | recheck due |
| KB-MQND | contract | 2026-09-15 | recheck due |
| KB-SRKV | contract | 2026-09-15 | recheck due |
| KB-HVJS | docs | 2026-09-16 | recheck due |
| KB-J2C5 | docs | 2026-09-16 | recheck due |
| KB-MC6B | contract | 2026-09-16 | recheck due |
| KB-YHSH | contract | 2026-09-16 | recheck due |
| KB-356T | live | 2026-09-17 | recheck due |
| KB-75DH | live | 2026-09-17 | recheck due |
| KB-BHHR | live | 2026-09-17 | recheck due |
| KB-NX4L | live | 2026-09-17 | recheck due |
| KB-QYGN | live | 2026-09-17 | recheck due |
| KB-3UFL | live | 2026-09-24 | recheck due |
| KB-FIBF | live | 2026-09-24 | recheck due |
| KB-SJJV | live | 2026-09-24 | recheck due |
| KB-WFB7 | live | 2026-09-24 | recheck due |
| KB-XELM | live | 2026-09-24 | recheck due |
| KB-2FA3 | docs | 2026-09-25 | recheck due |
| KB-2HZA | docs | 2026-09-25 | recheck due |
| KB-2MGI | docs | 2026-09-25 | recheck due |
| KB-2MWY | live | 2026-09-25 | recheck due |
| KB-2XZS | docs | 2026-09-25 | recheck due |
| KB-3744 | live | 2026-09-25 | recheck due |
| KB-3EX6 | contract | 2026-09-25 | recheck due |
| KB-3JIJ | live | 2026-09-25 | recheck due |
| KB-3TBJ | live | 2026-09-25 | recheck due |
| KB-4MR7 | live | 2026-09-25 | recheck due |
| KB-4V3I | docs | 2026-09-25 | recheck due |
| KB-4WDK | docs | 2026-09-25 | recheck due |
| KB-5BJH | live | 2026-09-25 | recheck due |
| KB-5RPQ | live | 2026-09-25 | recheck due |
| KB-5TID | docs | 2026-09-25 | recheck due |
| KB-5TJI | live | 2026-09-25 | recheck due |
| KB-5VPL | live | 2026-09-25 | recheck due |
| KB-5XW5 | docs | 2026-09-25 | recheck due |
| KB-66D6 | docs | 2026-09-25 | recheck due |
| KB-6EFK | docs | 2026-09-25 | recheck due |
| KB-74US | docs | 2026-09-25 | recheck due |
| KB-7QD4 | live | 2026-09-25 | recheck due |
| KB-7Y6M | live | 2026-09-25 | recheck due |
| KB-AGQK | docs | 2026-09-25 | recheck due |
| KB-B4SW | live | 2026-09-25 | recheck due |
| KB-BB4E | live | 2026-09-25 | recheck due |
| KB-BCY3 | live | 2026-09-25 | recheck due |
| KB-BGBR | live | 2026-09-25 | recheck due |
| KB-BICR | docs | 2026-09-25 | recheck due |
| KB-C2YH | live | 2026-09-25 | recheck due |
| KB-CKVZ | docs | 2026-09-25 | recheck due |
| KB-COAJ | live | 2026-09-25 | recheck due |
| KB-CQ2S | live | 2026-09-25 | recheck due |
| KB-DBAV | live | 2026-09-25 | recheck due |
| KB-ESW2 | live | 2026-09-25 | recheck due |
| KB-F7NF | docs | 2026-09-25 | recheck due |
| KB-FJ6E | live | 2026-09-25 | recheck due |
| KB-FVXP | live | 2026-09-25 | recheck due |
| KB-G6SH | live | 2026-09-25 | recheck due |
| KB-GEDK | docs | 2026-09-25 | recheck due |
| KB-GMRI | docs | 2026-09-25 | recheck due |
| KB-GP36 | live | 2026-09-25 | recheck due |
| KB-H34Q | docs | 2026-09-25 | recheck due |
| KB-HGAP | docs | 2026-09-25 | recheck due |
| KB-HIYO | live | 2026-09-25 | recheck due |
| KB-HSTO | live | 2026-09-25 | recheck due |
| KB-HULX | docs | 2026-09-25 | recheck due |
| KB-I4YA | live | 2026-09-25 | recheck due |
| KB-IWD5 | live | 2026-09-25 | recheck due |
| KB-J3DZ | live | 2026-09-25 | recheck due |
| KB-JM53 | live | 2026-09-25 | recheck due |
| KB-JYO7 | live | 2026-09-25 | recheck due |
| KB-KFC4 | docs | 2026-09-25 | recheck due |
| KB-KUBY | docs | 2026-09-25 | recheck due |
| KB-KVBP | live | 2026-09-25 | recheck due |
| KB-L4MM | docs | 2026-09-25 | recheck due |
| KB-LD5O | docs | 2026-09-25 | recheck due |
| KB-M3JR | live | 2026-09-25 | recheck due |
| KB-M42H | live | 2026-09-25 | recheck due |
| KB-MNIA | docs | 2026-09-25 | recheck due |
| KB-MWNP | live | 2026-09-25 | recheck due |
| KB-NIV7 | live | 2026-09-25 | recheck due |
| KB-NU75 | docs | 2026-09-25 | recheck due |
| KB-NZRC | docs | 2026-09-25 | recheck due |
| KB-OK4D | live | 2026-09-25 | recheck due |
| KB-OKUT | live | 2026-09-25 | recheck due |
| KB-OVOE | live | 2026-09-25 | recheck due |
| KB-P2MX | docs | 2026-09-25 | recheck due |
| KB-PBIU | live | 2026-09-25 | recheck due |
| KB-PWSD | docs | 2026-09-25 | recheck due |
| KB-PYYO | live | 2026-09-25 | recheck due |
| KB-QLJ5 | live | 2026-09-25 | recheck due |
| KB-QQFN | docs | 2026-09-25 | recheck due |
| KB-R3TV | docs | 2026-09-25 | recheck due |
| KB-RUHF | live | 2026-09-25 | recheck due |
| KB-RY3G | docs | 2026-09-25 | recheck due |
| KB-SBUW | live | 2026-09-25 | recheck due |
| KB-SOBS | live | 2026-09-25 | recheck due |
| KB-SWZZ | docs | 2026-09-25 | recheck due |
| KB-SZLC | live | 2026-09-25 | recheck due |
| KB-TOS5 | live | 2026-09-25 | recheck due |
| KB-TP5W | live | 2026-09-25 | recheck due |
| KB-TUIU | live | 2026-09-25 | recheck due |
| KB-UB44 | live | 2026-09-25 | recheck due |
| KB-UGZC | live | 2026-09-25 | recheck due |
| KB-ULTQ | docs | 2026-09-25 | recheck due |
| KB-UN55 | live | 2026-09-25 | recheck due |
| KB-USSN | live | 2026-09-25 | recheck due |
| KB-VOUX | docs | 2026-09-25 | recheck due |
| KB-VP4J | docs | 2026-09-25 | recheck due |
| KB-VZW3 | live | 2026-09-25 | recheck due |
| KB-W2R3 | docs | 2026-09-25 | recheck due |
| KB-WCSR | live | 2026-09-25 | recheck due |
| KB-WESI | live | 2026-09-25 | recheck due |
| KB-WMZT | live | 2026-09-25 | recheck due |
| KB-WYFA | docs | 2026-09-25 | recheck due |
| KB-X52S | live | 2026-09-25 | recheck due |
| KB-XC4T | docs | 2026-09-25 | recheck due |
| KB-XI6O | live | 2026-09-25 | recheck due |
| KB-XRV5 | docs | 2026-09-25 | recheck due |
| KB-XVNK | docs | 2026-09-25 | recheck due |
| KB-YL3W | docs | 2026-09-25 | recheck due |
| KB-ZABN | live | 2026-09-25 | recheck due |
| KB-ZD3W | docs | 2026-09-25 | recheck due |
| KB-ZD4H | live | 2026-09-25 | recheck due |
| KB-ZH7A | live | 2026-09-25 | recheck due |
| KB-ZHA4 | live | 2026-09-25 | recheck due |
| KB-B4YD | live | 2026-10-04 | recheck due |
| KB-PA4Y | live | 2026-10-04 | recheck due |
| KB-RFLA | live | 2026-10-04 | recheck due |
| KB-5FFD | live | 2026-10-05 | recheck due |
| KB-E2KU | live | 2026-10-05 | recheck due |
| KB-HTPH | live | 2026-10-05 | recheck due |
| KB-I7J7 | live | 2026-10-05 | recheck due |
| KB-QKU4 | live | 2026-10-05 | recheck due |
| KB-QQBS | live | 2026-10-05 | recheck due |
| KB-SQ4W | live | 2026-10-05 | recheck due |
| KB-TN3S | docs | 2026-10-05 | recheck due |
| KB-WP5X | live | 2026-10-06 | recheck due |
| KB-D6SI | docs | 2026-10-07 | recheck due |
| KB-4FW6 | docs | 2026-10-08 | recheck due |
| KB-CN3H | docs | 2026-10-08 | recheck due |
| KB-EZ6O | docs | 2026-10-08 | recheck due |
| KB-LT6G | docs | 2026-10-08 | recheck due |
| KB-PRGT | live | 2026-10-08 | recheck due |
| KB-QWED | live | 2026-10-08 | recheck due |
| KB-TQFH | docs | 2026-10-08 | recheck due |
| KB-VOCY | docs | 2026-10-08 | recheck due |
| KB-2IMZ | docs | 2026-10-09 | recheck due |
| KB-C7WI | docs | 2026-10-09 | recheck due |
| KB-XVXB | docs | 2026-10-10 | recheck due |
| KB-OOVV | docs | 2026-10-11 | recheck due |
| KB-KYR6 | live | 2026-10-12 | recheck due |
| KB-PLHK | live | 2026-10-12 | recheck due |
| KB-22XD | contract | 2026-10-14 | recheck due |
| KB-22YR | contract | 2026-10-14 | recheck due |
| KB-23F7 | contract | 2026-10-14 | recheck due |
| KB-2DY5 | contract | 2026-10-14 | recheck due |
| KB-2GNH | docs | 2026-10-14 | recheck due |
| KB-2SIL | contract | 2026-10-14 | recheck due |
| KB-2U4K | contract | 2026-10-14 | recheck due |
| KB-33UY | contract | 2026-10-14 | recheck due |
| KB-35HK | contract | 2026-10-14 | recheck due |
| KB-3CST | contract | 2026-10-14 | recheck due |
| KB-3L75 | contract | 2026-10-14 | recheck due |
| KB-3YYI | contract | 2026-10-14 | recheck due |
| KB-424Q | contract | 2026-10-14 | recheck due |
| KB-4COH | contract | 2026-10-14 | recheck due |
| KB-4I6S | contract | 2026-10-14 | recheck due |
| KB-4N6Q | contract | 2026-10-14 | recheck due |
| KB-4SRI | contract | 2026-10-14 | recheck due |
| KB-5RCL | live | 2026-10-14 | recheck due |
| KB-6AR3 | contract | 2026-10-14 | recheck due |
| KB-6LWE | contract | 2026-10-14 | recheck due |
| KB-6MXP | contract | 2026-10-14 | recheck due |
| KB-6VVI | contract | 2026-10-14 | recheck due |
| KB-752O | contract | 2026-10-14 | recheck due |
| KB-75AL | contract | 2026-10-14 | recheck due |
| KB-7IGI | contract | 2026-10-14 | recheck due |
| KB-7KEU | docs | 2026-10-14 | recheck due |
| KB-7U4I | contract | 2026-10-14 | recheck due |
| KB-AB67 | contract | 2026-10-14 | recheck due |
| KB-ABGI | contract | 2026-10-14 | recheck due |
| KB-ABSZ | contract | 2026-10-14 | recheck due |
| KB-APXI | contract | 2026-10-14 | recheck due |
| KB-AS3U | contract | 2026-10-14 | recheck due |
| KB-BFOA | contract | 2026-10-14 | recheck due |
| KB-BGAJ | contract | 2026-10-14 | recheck due |
| KB-BJGL | contract | 2026-10-14 | recheck due |
| KB-BKQH | contract | 2026-10-14 | recheck due |
| KB-BLS4 | contract | 2026-10-14 | recheck due |
| KB-BOS5 | contract | 2026-10-14 | recheck due |
| KB-BTIB | contract | 2026-10-14 | recheck due |
| KB-BXH5 | contract | 2026-10-14 | recheck due |
| KB-C27P | docs | 2026-10-14 | recheck due |
| KB-CE5J | contract | 2026-10-14 | recheck due |
| KB-CVCM | contract | 2026-10-14 | recheck due |
| KB-CXIW | contract | 2026-10-14 | recheck due |
| KB-D6ZP | contract | 2026-10-14 | recheck due |
| KB-EPEA | contract | 2026-10-14 | recheck due |
| KB-F3A4 | contract | 2026-10-14 | recheck due |
| KB-FEC6 | contract | 2026-10-14 | recheck due |
| KB-FFRB | contract | 2026-10-14 | recheck due |
| KB-FIKE | contract | 2026-10-14 | recheck due |
| KB-FJ2L | docs | 2026-10-14 | recheck due |
| KB-FJQ6 | contract | 2026-10-14 | recheck due |
| KB-FK5P | contract | 2026-10-14 | recheck due |
| KB-FQSW | contract | 2026-10-14 | recheck due |
| KB-HFN2 | contract | 2026-10-14 | recheck due |
| KB-HQFZ | contract | 2026-10-14 | recheck due |
| KB-HUHI | contract | 2026-10-14 | recheck due |
| KB-HWFP | contract | 2026-10-14 | recheck due |
| KB-HWYV | contract | 2026-10-14 | recheck due |
| KB-HYWV | contract | 2026-10-14 | recheck due |
| KB-I4EH | contract | 2026-10-14 | recheck due |
| KB-I4TR | live | 2026-10-14 | recheck due |
| KB-IIT3 | contract | 2026-10-14 | recheck due |
| KB-IXZ3 | contract | 2026-10-14 | recheck due |
| KB-JJEO | contract | 2026-10-14 | recheck due |
| KB-JQJN | contract | 2026-10-14 | recheck due |
| KB-K346 | contract | 2026-10-14 | recheck due |
| KB-K5D2 | live | 2026-10-14 | recheck due |
| KB-KA35 | contract | 2026-10-14 | recheck due |
| KB-KD7R | contract | 2026-10-14 | recheck due |
| KB-KHDV | contract | 2026-10-14 | recheck due |
| KB-KIAP | contract | 2026-10-14 | recheck due |
| KB-KOA3 | contract | 2026-10-14 | recheck due |
| KB-KSMV | contract | 2026-10-14 | recheck due |
| KB-KT7I | contract | 2026-10-14 | recheck due |
| KB-KUZK | contract | 2026-10-14 | recheck due |
| KB-KWII | contract | 2026-10-14 | recheck due |
| KB-LC4V | contract | 2026-10-14 | recheck due |
| KB-LHEC | contract | 2026-10-14 | recheck due |
| KB-LQBE | contract | 2026-10-14 | recheck due |
| KB-LSZV | contract | 2026-10-14 | recheck due |
| KB-LU3H | contract | 2026-10-14 | recheck due |
| KB-M6UB | contract | 2026-10-14 | recheck due |
| KB-MHO7 | live | 2026-10-14 | recheck due |
| KB-MIJ4 | contract | 2026-10-14 | recheck due |
| KB-MM3J | contract | 2026-10-14 | recheck due |
| KB-MQCW | contract | 2026-10-14 | recheck due |
| KB-MV5K | live | 2026-10-14 | recheck due |
| KB-MZEP | contract | 2026-10-14 | recheck due |
| KB-N7ZV | contract | 2026-10-14 | recheck due |
| KB-NHAY | contract | 2026-10-14 | recheck due |
| KB-NHCM | live | 2026-10-14 | recheck due |
| KB-NMSH | contract | 2026-10-14 | recheck due |
| KB-NMV2 | docs | 2026-10-14 | recheck due |
| KB-NZSQ | contract | 2026-10-14 | recheck due |
| KB-O2UG | contract | 2026-10-14 | recheck due |
| KB-OBHQ | contract | 2026-10-14 | recheck due |
| KB-ORQX | contract | 2026-10-14 | recheck due |
| KB-OUE6 | contract | 2026-10-14 | recheck due |
| KB-P3JV | contract | 2026-10-14 | recheck due |
| KB-P3X6 | contract | 2026-10-14 | recheck due |
| KB-P4WZ | contract | 2026-10-14 | recheck due |
| KB-PMPA | contract | 2026-10-14 | recheck due |
| KB-PWIV | contract | 2026-10-14 | recheck due |
| KB-QAFU | contract | 2026-10-14 | recheck due |
| KB-QJ3S | contract | 2026-10-14 | recheck due |
| KB-QLMG | contract | 2026-10-14 | recheck due |
| KB-R52P | contract | 2026-10-14 | recheck due |
| KB-RNFZ | contract | 2026-10-14 | recheck due |
| KB-RVSG | contract | 2026-10-14 | recheck due |
| KB-S22V | live | 2026-10-14 | recheck due |
| KB-SA7V | contract | 2026-10-14 | recheck due |
| KB-SNAP | contract | 2026-10-14 | recheck due |
| KB-SOBG | contract | 2026-10-14 | recheck due |
| KB-SWH2 | live | 2026-10-14 | recheck due |
| KB-T6NU | live | 2026-10-14 | recheck due |
| KB-TAXN | live | 2026-10-14 | recheck due |
| KB-TEXG | contract | 2026-10-14 | recheck due |
| KB-TKYD | contract | 2026-10-14 | recheck due |
| KB-TNVA | live | 2026-10-14 | recheck due |
| KB-TUGV | contract | 2026-10-14 | recheck due |
| KB-TX7A | contract | 2026-10-14 | recheck due |
| KB-TXBP | contract | 2026-10-14 | recheck due |
| KB-U7RP | contract | 2026-10-14 | recheck due |
| KB-U7YD | contract | 2026-10-14 | recheck due |
| KB-UEVJ | contract | 2026-10-14 | recheck due |
| KB-UFQA | contract | 2026-10-14 | recheck due |
| KB-UJSI | contract | 2026-10-14 | recheck due |
| KB-UTUP | contract | 2026-10-14 | recheck due |
| KB-UUV3 | contract | 2026-10-14 | recheck due |
| KB-UUZF | contract | 2026-10-14 | recheck due |
| KB-UVSS | live | 2026-10-14 | recheck due |
| KB-VBBT | contract | 2026-10-14 | recheck due |
| KB-VEDO | contract | 2026-10-14 | recheck due |
| KB-VNL6 | contract | 2026-10-14 | recheck due |
| KB-VYRW | contract | 2026-10-14 | recheck due |
| KB-WD2H | contract | 2026-10-14 | recheck due |
| KB-WKYI | live | 2026-10-14 | recheck due |
| KB-WNNJ | contract | 2026-10-14 | recheck due |
| KB-WQA4 | live | 2026-10-14 | recheck due |
| KB-WQWT | contract | 2026-10-14 | recheck due |
| KB-WVTD | contract | 2026-10-14 | recheck due |
| KB-X3HG | contract | 2026-10-14 | recheck due |
| KB-X6WM | contract | 2026-10-14 | recheck due |
| KB-XFT6 | contract | 2026-10-14 | recheck due |
| KB-XKXQ | contract | 2026-10-14 | recheck due |
| KB-XQQY | contract | 2026-10-14 | recheck due |
| KB-XSZD | contract | 2026-10-14 | recheck due |
| KB-Y4LS | contract | 2026-10-14 | recheck due |
| KB-Z3MG | live | 2026-10-14 | recheck due |
| KB-ZLGK | contract | 2026-10-14 | recheck due |
| KB-ZMQL | contract | 2026-10-14 | recheck due |
| KB-ZYJM | contract | 2026-10-14 | recheck due |
| KB-2NF7 | live | 2026-10-19 | recheck due |
| KB-6SR2 | live | 2026-10-19 | recheck due |
| KB-FBFG | live | 2026-10-19 | recheck due |
| KB-TMQ5 | live | 2026-10-19 | recheck due |
| KB-BJTC | live | 2026-10-20 | recheck due |
| KB-GURS | live | 2026-10-20 | recheck due |
| KB-H76B | live | 2026-10-20 | recheck due |
| KB-JQ76 | live | 2026-10-20 | recheck due |
| KB-Q6XQ | live | 2026-10-20 | recheck due |
| KB-RBLP | live | 2026-10-20 | recheck due |
| KB-T7LO | live | 2026-10-20 | recheck due |
| KB-3VXF | live | 2026-10-21 | recheck due |
| KB-6Z4Y | live | 2026-10-21 | recheck due |
| KB-AX36 | contract | 2026-10-21 | recheck due |
| KB-DUTE | live | 2026-10-21 | recheck due |
| KB-EPOM | live | 2026-10-21 | recheck due |
| KB-LGNR | live | 2026-10-21 | recheck due |
| KB-VCXP | contract | 2026-10-21 | recheck due |
| KB-77QY | docs | 2026-10-22 | recheck due |
| KB-P2OZ | live | 2026-10-22 | recheck due |
| KB-SHDM | contract | 2026-10-22 | recheck due |
| KB-B2JD | contract | 2026-11-07 | recheck due |
| KB-KM2G | contract | 2026-11-07 | recheck due |
| KB-DXKH | contract | 2026-11-12 | recheck due |
| KB-6EWX | contract | 2026-11-16 | recheck due |
| KB-PLV4 | contract | 2026-11-19 | recheck due |


## Before you use it with a public model

The facts are public and carry no customer data. Your questions are another matter. When you use this dataset with a public model (ChatGPT, Claude, Gemini, Copilot or any hosted service), what you type goes to that provider under its terms, not under the terms of this dataset. So:

- Ask technical questions only: can TCP do this, what does it cost, how does this service behave.

- Never paste customer data: no names, no mail addresses, no documents, no tenant ids, no prices from an offer.

- A described setup can identify a customer too. A region, a sector, a number of sites, a named application and a go-live date together are often enough for a capable model to guess who the customer is, even when you named nobody. Identifying a customer through such details can break data protection law, so give the model technical tasks only and keep them simple. Keep the setup generic or run the model where the data may go.

How you use it is your responsibility as the user. The dataset gives you checked facts and nothing else.


## MCP clients

tcp_facts_mcp.py is a read-only MCP server over the files beside it: one Python file, standard library only, Python 3.10 or newer, JSON-RPC 2.0 over stdio. It has four tools: tcp_facts_search (facts by words, tag or grade), tcp_service_check (offered or not, from services.md), tcp_price_find (live price rows of eu-de or eu-nl, only with --live) and tcp_calculate (exact arithmetic in hours, a month is 720 h). It reads no file outside its folder, opens no connection without --live and writes nothing.

Claude Desktop, one click: download https://github.com/shimoza/tcp-facts/releases/latest/download/tcp-facts.mcpb (the newest release, the same bytes as its tcp-facts-<date>.mcpb) and open it (double click, or drag it into Settings, Extensions). Claude Desktop shows the extension and its four tools; press Install. The file carries the server and the data of that build. It needs Python 3.10 or newer on the machine.

Any other client: unpack the zip of the latest release or clone github.com/shimoza/tcp-facts, then add the server by hand. Replace /path/to/tcp-facts with that folder, the one that holds facts.jsonl and tcp_facts_mcp.py.

Claude Desktop by hand, in claude_desktop_config.json:

```json
{"mcpServers": {"tcp-facts": {"command": "python3", "args": ["/path/to/tcp-facts/tcp_facts_mcp.py"]}}}
```

Claude Code:

```bash
claude mcp add tcp-facts -- python3 /path/to/tcp-facts/tcp_facts_mcp.py
```

VS Code (and GitHub Copilot in it), in .vscode/mcp.json:

```json
{"servers": {"tcp-facts": {"type": "stdio", "command": "python3", "args": ["/path/to/tcp-facts/tcp_facts_mcp.py"]}}}
```

Add "--live" to the arguments for prices: they come live from the public price API (no credentials) and are not part of the dataset; without it tcp_price_find says so. Claude Desktop opens its file under Settings, Developer, Edit Config and loads a change only after a full quit and start. Give the path in full, never relative to a folder. On Windows the command is python or py. In the JSON every backslash of a path is written twice. The rules of "Before you use it with a public model" apply here too: the client sends your questions to its model provider.


## Files

facts.md: all facts, grouped by topic. facts.jsonl: the same facts with source, tags, class, expiry and the evidence of negatives, for RAG and tools. topics/<topic>.md: one file per topic. services.md: the 76 services orderable per the service description of 18.11.2026. tcp_facts_mcp.py: a read-only MCP server over these files for Claude, VS Code or any MCP client; its first lines say how to add it. MANIFEST.json: counts, dates and the sha256 of every file.


## Dates and licence

Built 2026-11-23. Best before 2026-12-23: facts about availability are re-checked every 30 days. Prices are not part of the dataset: the live price API is the source of truth before any quote.

Dataset: TCP Facts, github.com/shimoza/tcp-facts.

Compiled from public sources and live checks. Licence CC BY 4.0: name the dataset and its address when you reuse it. No warranty: the service description and the price list of the provider are the binding documents.

The documentation facts draw on the repositories of github.com/opentelekomcloud-docs, licensed under the Apache License 2.0 (www.apache.org/licenses/LICENSE-2.0).

The full licence text is in LICENSE at github.com/shimoza/tcp-facts.
