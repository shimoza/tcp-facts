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
# TCP Facts 2026-10-22: dws

- In DWS, CREATE EXTERNAL SCHEMA and ALTER EXTERNAL SCHEMA point at a metastore: source_type accepts dli, lakeformation or hive. The syntax is available from DWS 8.3.0. (KB-DB4T, docs, checked 2026-07-29)
- A DWS foreign table on OBS reads ORC, TEXT, JSON, CSV, CarbonData, Parquet and Hudi, and writes ORC and Parquet. Iceberg appears in neither list. (KB-JZIX, docs, checked 2026-07-29)
- Data Warehouse Service (DWS) is a managed online analytical database for searching and analyzing large data sets on a distributed architecture. The documentation states that it supports ANSI/ISO SQL-92, SQL-99 and SQL:2003 syntax and is interoperable with the PostgreSQL, Oracle, Teradata and MySQL ecosystems. The Regions and Endpoints page lists the DWS API endpoint in eu-de. (KB-MQCW, contract, checked 2026-10-14)
- The DWS flavor dws.m3.xlarge in eu-de carries minAmount 3 in the price API, so the smallest cluster of that flavor is three nodes that run whether or not a query is issued. (KB-TP5W, live, checked 2026-09-25)
- The TCP service description, revision 09.10.2026, section 6.9.2, prices DWS nodes for EU-DE only and marks every EU-NL price column n.a., so DWS is not offered in eu-nl under that contract revision. (KB-XFT6, contract, checked 2026-10-14)
