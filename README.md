# TCP Facts 2026-10-10

Build of 2026-10-10 11:08 UTC. A later build of the same day replaces this one under the same name; the manifest carries the build time.

1531 checked facts about T Cloud Public (TCP) with the list of orderable services and the public price list of two regions. Made to be dropped into any AI assistant.

1035 facts were tested live on a TCP tenant, 425 come from the vendor documentation and 71 from the service description (revision 17.08.2026). No fact from hearsay, no expired fact, no customer, no project, no credential.


## Use

Attach facts.md and type:

```
Use the attached TCP Facts. Answer: <your question>
```

PROMPT.md has the rest.


## Before you use it with a public model

The facts are public and carry no customer data. Your questions are another matter. When you use this dataset with a public model (ChatGPT, Claude, Gemini, Copilot or any hosted service), what you type goes to that provider under its terms, not under the terms of this dataset. So:

- Ask technical questions only: can TCP do this, what does it cost, how does this service behave.

- Never paste customer data: no names, no mail addresses, no documents, no tenant ids, no prices from an offer.

- A described setup can identify a customer too. A region, a sector, a number of sites, a named application and a go-live date together are often enough for a capable model to guess who the customer is, even when you named nobody. Keep the setup generic or run the model where the data may go.

How you use it is your responsibility as the user. The dataset gives you checked facts and nothing else.


## Files

facts.md: all facts, grouped by topic. facts.jsonl: the same facts with source, tags, class, expiry and the evidence of negatives, for RAG and tools. topics/<topic>.md: one file per topic. services.md: the 76 services orderable per the service description of 17.08.2026. prices/<region>.csv: eu-de 3315 records, eu-nl 2637 records. tcp_facts_mcp.py: a read-only MCP server over these files for Claude, VS Code or any MCP client; its first lines say how to add it. MANIFEST.json: counts, dates and the sha256 of every file.


## MCP clients

tcp_facts_mcp.py is a read-only MCP server over the files beside it: one Python file, standard library only, Python 3.10 or newer, JSON-RPC 2.0 over stdio. It has four tools: tcp_facts_search (facts by words, tag or grade), tcp_service_check (offered or not, from services.md), tcp_price_find (price rows of eu-de or eu-nl from the snapshot) and tcp_calculate (exact arithmetic in hours, a month is 720 h). It reads no file outside its folder, opens no connection without --live and writes nothing.

Unpack the zip of the latest release or clone this repository, then add the server to your client. Replace /path/to/tcp-facts with that folder.

Claude Desktop, in claude_desktop_config.json:

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

Add "--live" to the arguments for live prices from the public price API (no credentials). On Windows the command is python or py. The rules of "Before you use it with a public model" apply here too: the client sends your questions to its model provider.


## Dates and licence

Built 2026-10-10. Best before 2026-11-09: facts about availability are re-checked every 30 days. Prices are a snapshot; the live price API is the source of truth before any quote.

Dataset: TCP Facts, github.com/shimoza/tcp-facts.

Compiled from public sources and live checks. Licence CC BY 4.0: name the dataset and its address when you reuse it. No warranty: the service description and the price list of the provider are the binding documents.

The full licence text is in [LICENSE](LICENSE).
