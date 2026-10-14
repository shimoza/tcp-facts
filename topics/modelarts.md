<!-- TCP Facts, dataset of 2026-10-14. Instructions for the assistant that reads this file:
1. Answer only from the facts in this dataset. Put the id of every fact you use after it, like (KB-XXXX).
   If no fact covers the question, say "no checked fact covers this" and what would need to be checked. Never guess.
2. Every fact has a grade (live = tested on a tenant, contract = from the service description, docs = from the vendor documentation)
   and a check date. Name the check date when it is older than 90 days.
3. Prices come from a snapshot of the public price API taken 2026-10-14 13:11 UTC. Give every price with its unit, currency and that date,
   and say that the live price API is the source of truth before any quote.
4. Best before 2026-11-13. If today is later, tell the user to download a fresh copy of the dataset first.
5. Technical questions only; no customer data in your prompts (see README).
-->
# TCP Facts 2026-10-14: modelarts

- The ModelArts v2 training job listing is POST /v2/{project_id}/training-job-searches, not a GET. GET /v1/{project_id}/services answers HTTP 200 with a count field and serves, like the flavor and engine GETs, as a cheap liveness probe. (KB-FFU5, live, checked 2026-07-02)
- ModelArts is an end-to-end AI development platform that covers data preprocessing and semi-automatic labeling, distributed training, automated model building and deployment of models on T Cloud Public (TCP). The documentation names the open-source frameworks TensorFlow, PyTorch and MindSpore, dedicated resources and custom images for custom frameworks. The Regions and Endpoints page lists the ModelArts API endpoint in eu-de. (KB-O2UG, contract, checked 2026-10-14)
- GET /v1/{project_id}/services/specifications returns 5 inference specifications in eu-de: cpu.2u, high.p3 without a GPU, bm.gpu.v100 with one V100 32GB, high.p2 with an 8GB GPU and gpu.t4u8 with a T4 16GB. Their state moves between normal and sellout: on 2026-09-25 two checks disagreed on cpu.2u and high.p3, while high.p2 and gpu.t4u8 were sellout in every read. Sellout marks a specification the listing returns while no capacity is on offer. (KB-Q6XQ, live, checked 2026-09-25)
- The ModelArts endpoint on eu-de resolves and answers AK/SK signed calls. GET /v2/{project_id}/training-job-flavors returned 3 training flavors on 2026-07-02: modelarts.vm.cpu.2u, modelarts.vm.gpu.v100 with one V100 32GB and modelarts.vm.gpu.4v100 with four V100 32GB, each with max_num 1, so single node training. (KB-TOS5, live, checked 2026-09-25)
- GET /v2/{project_id}/training-job-engines returned 2 preset engines on eu-de on 2026-09-25: pytorch_1.8.0-cuda_10.2-py_3.7-ubuntu_18.04-x86_64 and tensorflow_2.1.0-cuda_10.1-py_3.7-ubuntu_18.04-x86_64. (KB-WMZT, live, checked 2026-09-25)
