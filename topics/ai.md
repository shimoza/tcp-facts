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
# TCP Facts 2026-10-28: ai

- A 400 validation error is a FastAPI error list that echoes the submitted request body, so the prompt can end up in client error logs. (KB-234F, live, checked 2026-09-21)
- Visual RAG runs under /v1 (files and vector stores) with text-embedding-bge-m3 for text and tsi-embedding-colqwen2-2b-v1 for page images. GET /v1/vector_stores answered on a Category 1 key. (KB-2PS3, live, checked 2026-09-21)
- The Whisper prompt parameter had no effect. verbose_json returns only text and usage, so there are no timestamps, and there is no diarization. (KB-2ZQZ, live, checked 2026-09-08)
- AI Foundation Services (AIFS) is a T-Systems product, also called LLM Hub. Its service description names it LLM-Serving-Service. (KB-3QGT, docs, checked 2026-10-08)
- Category 1 metadata in the API says deployment_region "otc-germany" and deployment_country "Germany, EU", but the service description commits only to EU/EEA or an adequacy country. (KB-3VHO, live, checked 2026-09-17)
- The API showed end-of-life dates (for example 2026-10-01 on two Qwen3 models) while the docs retirement page listed nothing as scheduled. Read EOL dates from the API. (KB-52IK, live, checked 2026-09-17)
- The meta_data of /v2/models carries end_of_life_date, replacement_exact_model_name, model_lifecycle_stage, input_modalities, output_modalities, max_sequence_length, max_output_length, is_externally_hosted, deployment_region, deployment_country, parameter_mappings and license. is_externally_hosted tells Category 1 from Category 2. (KB-5HKP, live, checked 2026-09-17)
- The Category 1 backend is vLLM; system_fingerprint starts with "vllm-". (KB-7PHA, live, checked 2026-09-21)
- In v1.24 the service description removed the section on the chat frontend (Playground), so the Playground is no longer a contracted feature. (KB-B5UT, docs, checked 2026-10-08)
- A customer who sends personal data must sign a data processing agreement (Telekom template), available on request. (KB-BVS7, docs, checked 2026-06-12)
- Category 2 models in v1.24 (20): on Azure Sweden GPT-5.6 Sol, Terra and Luna, GPT-6.1 Sol and GPT-6 Luna; on Azure GPT-Image-2; Ada-Text (Azure France); on GCP Mistral Medium 3; on GCP and Azure Mistral Medium 3.5, Claude Opus 5, Opus 5.5, Sonnet 5, Sonnet 5.5, Fable 5 and Fable 5.1; on GCP Gemini 3 Flash, 3.1 Pro, 3.5 Flash, 3.8 Flash and 3 Pro Image. (KB-CN3H, docs, checked 2026-10-08)
- Category 1 models are operated by Telekom on T Cloud Public / Industrial AI Cloud. Data is processed in the EU/EEA and/or in countries with an EU adequacy decision. (KB-EZ6O, docs, checked 2026-10-08)
- A stream always ends with a usage chunk whose choices list is empty, even without stream_options.include_usage. A client that reads choices[0] on every chunk fails on it. (KB-FTZX, live, checked 2026-09-21)
- Tool calling works on every Category 1 chat model except Qwen3.6-35B-A3B-FP8. response_format json_object is not honoured on GLM-5.2, Nemotron 3 Super and Qwen3.6. (KB-GGYA, live, checked 2026-09-17)
- The /queue/... endpoints return a finished completion with no job id. They answer synchronously and do not work as a batch API. (KB-GMCD, live, checked 2026-09-21)
- Requests and answers are by default not stored permanently and not used for training. A cache keeps processed requests for a limited time; it is on by default and the customer can switch it off. (KB-GWKA, docs, checked 2026-10-08)
- Category 2 models are not operated by Telekom. Requests go directly to the third-party provider, processing can take place outside the EU/EEA, the provider can use sub-processors worldwide and the customer accepts the provider's terms and data protection rules. (KB-HC2L, docs, checked 2026-10-08)
- There is no latency or time-to-first-token target; the docs say the SLA covers API availability only. (KB-J2X4, docs, checked 2026-08-21)
- A wrong key returns 401 "Incorrect API key was provided". A deactivated key returns 401 "Your API Key is deactivated...". A request without an Authorization header returns 403 "Missing authentication". (KB-JLYF, live, checked 2026-09-26)
- Every request authenticates with the header "Authorization: Bearer <API key>". The OpenAI SDK works when OPENAI_API_KEY and OPENAI_BASE_URL are set. (KB-JNV5, docs, checked 2026-06-12)
- Whisper has a 448-token context per request. Audio longer than about 2.5 minutes came back with duplicated text or a lost final segment, so long audio must be split. (KB-JWXS, live, checked 2026-09-08)
- Prefix caching matches exact token prefixes only. T Cloud models use the request fields save_cache and cache_salt; Anthropic models use cache_control. The docs call cache counters diagnostics, not a billing statement. (KB-K6QW, docs, checked 2026-08-21)
- Published Category 1 rate limits (Essential / Professional / Agentic): GPT-OSS-120B 400k / 1M / 2M TPM and 100 / 200 / 300 RPM; Gemma 4, Mistral Small 4, Qwen3.6 and Nemotron 3 Super 50k / 100k / 300k TPM and 50 / 100 / 150 RPM; GLM 5.2 400k / 1M / 2M TPM and 100 / 200 / 300 RPM; Whisper large-v3 218 TPM, turbo 345 TPM, 300 RPM in every plan. (KB-LT6G, docs, checked 2026-10-08)
- The API base URL is https://llm-server.llmhub.t-systems.net/v2 (path /v2, not /v1) and it is OpenAI-compatible. (KB-MAIA, live, checked 2026-09-21)
- The service description names only public internet access: HTTPS requests or the Python package openai, with the handover point at the API endpoint in the Telekom data centre. It names no VPN, Direct Connect, peering or private endpoint. (KB-NF43, docs, checked 2026-10-10)
- Chat completions accept n, logprobs with top_logprobs, seed, stop, the penalty parameters and a strict json_schema. (KB-PHSS, live, checked 2026-09-21)
- AIFS is not a service in the T Cloud Public service description. It has its own service description and its own contract. (KB-PKO4, docs, checked 2026-09-01)
- Silence in the audio produced invented, billed text (a known Whisper effect); trim silence before sending. (KB-QEGN, live, checked 2026-09-08)
- Since v1.22 the service description no longer says Category 1 data is "not visible to Telekom or third parties"; the v1.20 text said that. (KB-SXWH, docs, checked 2026-08-21)
- Rate limits apply per contract and are shared by all keys under it. They are maximum ceilings on a best-effort basis and not part of the SLA. (KB-VA7X, docs, checked 2026-10-08)
- On a Category 1 key, /v2/chat/completions, /v2/completions, /v2/audio/transcriptions, /v2/coding/chat/completions and /v2/responses (tested with gpt-oss-120b) work. (KB-VBP2, live, checked 2026-09-21)
- Models hosted on T Cloud Public send no rate-limit headers; clients must count usage themselves. (KB-VCL5, live, checked 2026-08-25)
- Category 1 models in v1.24 (12): Gemma 4 31B, Mistral Small 4, Qwen3.6 35B, NVIDIA Nemotron 3 Super, GLM 5.2, GLM 5.3 Flash, Qwen 3.8 27B, GPT-OSS-120B, jina-embeddings-v2-base-de, text-embedding-bge-m3, Whisper Large v3 and Whisper Large v3 Turbo. (KB-VOCY, docs, checked 2026-10-08)
- Whisper is billed by transcript tokens, all in completion_tokens, with prompt_tokens 0. Dense German speech produced about 152.6 tokens per audio minute. (KB-W2D6, live, checked 2026-09-08)
- GET /v2/models lists the models of the key. GET /v2/models/{id} returns 405. (KB-WKNA, live, checked 2026-09-17)
- The self-service portal https://apikey.llmhub.t-systems.net shows the keys and their models, creates and manages keys and shows token use per key and model. The customer admin gets a login and adds users, who create their own keys. (KB-WMLW, docs, checked 2026-10-08)
- The SLA is 99.5 % monthly availability in the minimum-spend plans, measured only Monday to Friday 09:00 to 17:00 without German public holidays. Service credits are 5 %, 10 % or 25 % of the minimum spend. Outages of third-party LLM providers are excluded. (KB-XVXB, docs, checked 2026-10-10)
- gpt-oss-120b spends max_tokens on reasoning first. With a small limit the answer has content null, the text sits in message.reasoning and finish_reason is "length". (KB-XXO6, live, checked 2026-09-21)
- Input TPM is enforced, sometimes below the published figure (Gemma 4 and Mistral Small 4 throttled at 35,000 against 50,000). Output TPM and Whisper TPM were not enforced. An unenforced limit can be switched on without notice. (KB-Z3AO, live, checked 2026-09-17)
