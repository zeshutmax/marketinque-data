# marketinque data

Two open datasets from [marketinque](https://marketinque.com), the launch plan and marketing library agents work through over MCP. Both are free to reuse with credit under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). The write-up that uses them: [SaaS marketing in 2027: what to start, change and stop](https://marketinque.com/blog/saas-marketing-2027).

| File | What it is | Rows |
| --- | --- | --- |
| [`data/ai-citation-study-2026-11.csv`](data/ai-citation-study-2026-11.csv) | Every link four AI engines cited when asked for the best tools in 50 SaaS categories, 17 November 2026 | 3,054 |
| [`data/mcp-census-2026-11.csv`](data/mcp-census-2026-11.csv) | Which of 163 leading cloud companies publish an MCP server, with an evidence link per company | 163 |

## AI citation study (November 2026)

On 17 November 2026 we asked "What are the best [category] tools for a small team?" in 50 SaaS categories. Google AI Mode and ChatGPT (signed out, with search) answered all 50 in a browser; Claude (with web search) answered 20; Gemini 2.5 Flash answered all 50 through its API with Google Search grounding. Every cited link was recorded and sorted by URL into articles, vendor pages, Reddit, YouTube, review sites and other. The file also holds Gemini's answers to "alternatives" and "how to choose" prompts.

Columns: `date, engine, category, prompt, position, cited_url, domain, source_type`.

On the main prompt (1,660 links): 54% were article lists; Google AI Mode cited Reddit in 42 of 50 answers and YouTube in 35, while ChatGPT, Gemini and Claude cited Reddit in none; G2 or Capterra appeared in 2 of 50 AI Mode, 6 of 50 ChatGPT and 8 of 50 Gemini answers.

Limits: one day, one prompt per category on the main question, answers from a browser in Europe and some localised. A hand check of 40 random links found 37 sorted correctly. Perplexity was left out because it asked for a human check.

## MCP census (November 2026)

The 2025 Forbes Cloud 100 plus the 64 companies of the BVP Nasdaq Emerging Cloud Index, 163 in all. For each we searched the official MCP registry and the company's own documentation, and counted a server only when the company publishes it. `status` is `product` (works on a customer's own account), `docs_only`, `none` or `unclear`; `in_official_registry` says whether it is listed there.

Result: 125 publish a product server, 6 a docs-only server, 27 none, 5 unclear; 28 of the 125 are in the official registry. It counts who publishes a server, not who uses one.

## Cite as

> The Marketinque Team (2026). *AI citation study* and *MCP census*, November 2026. marketinque. https://marketinque.com/blog/saas-marketing-2027. CC BY 4.0.

The same files are served at [marketinque.com/data/](https://marketinque.com/data/ai-citation-study-2026-11.csv), which stays the canonical copy. We plan to re-run the citation study around February 2027 and publish the new file beside this one.
