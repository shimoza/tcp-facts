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
# TCP Facts 2026-10-28: llm-gateway

- SmartChat is the managed RAG product built on the LLM Hub: hosted document knowledge bases queried by browser UI or API with over 50 retrieval settings, isolated spaces per tenant, audit logging, role-based access and enterprise SSO, operated by T-Systems in Germany at a monthly flat rate. Access credentials come from the AIFS team on request. (KB-2BED, docs, checked 2026-10-22)
- The LLM Hub (AI Foundation Services) lists 48 models. The open-source models run on T-Cloud in Germany with data processing in Germany. The proprietary models run on Azure (Sweden, France) or GCP (Europe) with data processing in the EU, except the Gemini models and GPT-6.1 Sol, whose server location and data processing are worldwide. (KB-77QY, docs, checked 2026-10-22)
- On T Cloud Public (TCP) the LLM Hub is a subscription product of the Marketplace: the customer subscribes after accepting the seller EULA and the platform terms, creates any number of API keys, each shown once, and sees the token consumption per key in the Marketplace dashboard. The Marketplace guide describes it as model inference hosted in Germany and the EU with open-source and proprietary LLMs behind an OpenAI-compatible API. (KB-GIOM, docs, checked 2026-10-20)
- AI Foundation Services, also called LLM Hub, does not appear in the T Cloud Public (TCP) service description of 09.10.2026, while ModelArts, UCS, Cloud Firewall and KMS do appear. It is contracted as a separate product and is not orderable from the TCP catalog. (KB-KSMV, contract, checked 2026-10-14)
- Fine-tuning of LLM Hub models is an optional service on separate order, against additional payment and after a feasibility check: Telekom provides the fine-tuning function with its documentation and supports building and integrating the fine-tuned model. Dedicated model instances, installation in a customer-owned environment and models outside the catalog are optional services of the same kind. (KB-WTDS, docs, checked 2026-10-22)
- The LLM Hub API is OpenAI-compatible at https://llm-server.llmhub.t-systems.net/v2 and covers chat completions, streaming, embeddings, function calling with structured JSON output, speech-to-text models (Whisper) and image models. Its documentation names integrations with LangChain and LlamaIndex. (KB-ZAIQ, docs, checked 2026-10-22)
