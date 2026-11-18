# Awesome GTM Engineering [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> Go-to-market built like software — scoring, routing, paid control, and a learning loop, as tested code instead of slide decks. Curated for **GTM engineers** and anyone learning **AI agents, agentic AI, and LLMs**.

GTM engineering is the discipline of turning the parts of go-to-market that usually live in someone's head — who to target, what to spend, which leads to route — into systems you can run, test, and improve. One operator, a five-person motion. This is the stack you build it from.

Maintained by [Kai](https://github.com/Kai8karma). **Links, not forks** — every resource is its own project; this is the map, and every entry is verified: the repo exists, and the licence shown is the one in its licence file. Last full check: 2026-11-18.

## Contents
- [Engines — GTM as code](#engines--gtm-as-code)
- [MCP servers and tooling](#mcp-servers-and-tooling)
- [GTM & marketing skills](#gtm--marketing-skills)
- [CRM and conversations](#crm-and-conversations)
- [Data quality and entity resolution](#data-quality-and-entity-resolution)
- [Enrichment, crawling and signals](#enrichment-crawling-and-signals)
- [Workflow and automation](#workflow-and-automation)
- [Outbound and deliverability](#outbound-and-deliverability)
- [Scheduling, analytics and attribution](#scheduling-analytics-and-attribution)
- [Measurement](#measurement)
- [AI agent frameworks](#ai-agent-frameworks)
- [Memory & brains](#memory--brains)
- [Evals & rigor](#evals--rigor)
- [Learn the foundations](#learn-the-foundations)
- [Related lists](#related-lists)

## Engines — GTM as code
The system layer: decisions as tested functions, not playbooks.
- **[kaikarma-gtm-engine](https://github.com/Kai8karma/kaikarma-gtm-engine)** `MIT` — ICP scoring, paid-spend control under hard caps, lead routing, and a backtested learning loop. 774 tests; nothing ships unless the gate is green.
- **[gtmos-mcp](https://github.com/Kai8karma/gtmos-mcp)** `MIT` — deterministic CRM audit for HubSpot over MCP: integrity score, duplicates, stalled revenue, ops health, and a policy-gated proposal queue. Zero dependencies, never writes to the CRM.
- [gtm-agency-os-starter](https://github.com/Kai8karma/gtm-agency-os-starter) `MIT` — 5-layer agency operating system: reference agents, per-client routines, eval + security gates.
- [postevent-engine](https://github.com/Kai8karma/postevent-engine) — post-event pipeline prototype: lead enrichment, segmented follow-up, content repurposing, and a lead dashboard, with every claim grounded against the transcript.

## MCP servers and tooling
How agents reach your GTM systems, and how you prove a server works.
- [MCP Python SDK](https://github.com/modelcontextprotocol/python-sdk) `MIT` — the official SDK; v2 speaks the stateless 2026-07-28 revision and still serves older clients.
- [MCP Inspector](https://github.com/modelcontextprotocol/inspector) `Apache-2.0 / MIT` — call a server's tools by hand before an agent does.
- [MCP conformance](https://github.com/modelcontextprotocol/conformance) `Apache-2.0 / MIT` — the official test framework for clients and servers.
- [MCP Registry](https://github.com/modelcontextprotocol/registry) `Apache-2.0 / MIT` — where a server gets listed; publish `server.json` from CI.

## GTM & marketing skills
Agent skills for the motion — outbound, ads, SEO, growth.
- [marketingskills](https://github.com/coreyhaines31/marketingskills) `MIT` — Corey Haines' growth-engineering skills: CRO, copy, analytics.
- [claude-seo](https://github.com/AgriciDaniel/claude-seo) `MIT` — sub-skills and agents across technical SEO, schema, GEO/AEO.
- [claude-ads](https://github.com/AgriciDaniel/claude-ads) `MIT` — paid-ads audit checks across Google, Meta, LinkedIn, TikTok.
- [ai-marketing-skills](https://github.com/ericosiu/ai-marketing-skills) `MIT` — Eric Siu: growth experiments, sales pipeline, content ops.
- [gtm-agents](https://github.com/gtmagents/gtm-agents) `Apache-2.0` — agent collection for sales, marketing and growth work. Quiet since April 2026.
- [marketing-team-eve-template](https://github.com/vercel-labs/marketing-team-eve-template) `MIT` — a lead agent that briefs five specialists, with approval gates before anything is sent or published.
- [Google Workspace CLI](https://github.com/googleworkspace/cli) `Apache-2.0` — Gmail, Sheets, Drive and Calendar for terminal agents, with bundled skills. Not an officially supported Google product.

## CRM and conversations
A system of record you can read, run and test against.
- [Twenty](https://github.com/twentyhq/twenty) `AGPL-3.0, parts commercial` — open CRM with an API; a free portal to develop and test audits against.
- [Chatwoot](https://github.com/chatwoot/chatwoot) `MIT, enterprise parts separate` — shared inbox across chat, email and messaging; the raw material for reply triage.

## Data quality and entity resolution
A CRM score is only as good as its matching rules.
- [Splink](https://github.com/moj-analytical-services/splink) `MIT` — probabilistic record linkage at scale; the step up from exact-key duplicate rules.
- [RapidFuzz](https://github.com/rapidfuzz/RapidFuzz) `MIT` — fast fuzzy string matching for names and companies.
- [disposable-email-domains](https://github.com/disposable-email-domains/disposable-email-domains) `CC0` — a maintained blocklist of throwaway email domains, as a plain file.
- [python-phonenumbers](https://github.com/daviddrysdale/python-phonenumbers) `Apache-2.0` — parse, validate and normalise phone numbers.

## Enrichment, crawling and signals
Turn the public web into inputs a scorer can use.
- [Crawl4AI](https://github.com/unclecode/crawl4ai) `Apache-2.0` — crawl sites into clean markdown for models.
- [Firecrawl](https://github.com/firecrawl/firecrawl) `AGPL-3.0` — crawl and extract as a service or self-hosted; mind the licence if you embed it.
- [Playwright](https://github.com/microsoft/playwright) `Apache-2.0` — browser automation for the places with no API.
- [changedetection.io](https://github.com/dgtlmoon/changedetection.io) `Apache-2.0` — watch pricing, careers and product pages; a change is a signal.

## Workflow and automation
The glue between systems. Check the licence before you build a business on one.
- [n8n](https://github.com/n8n-io/n8n) `Sustainable Use (fair-code, not OSI open source)` — the most widely used workflow builder, with AI nodes. Source-available; commercial hosting for others is restricted.
- [Activepieces](https://github.com/activepieces/activepieces) `MIT, enterprise parts separate` — the MIT-licensed alternative.
- [Windmill](https://github.com/windmill-labs/windmill) `AGPL-3.0, Apache-2.0 parts` — scripts as workflows; a natural home for Python engines.

## Outbound and deliverability
Getting to the inbox is an engineering problem.
- [checkdmarc](https://github.com/domainaware/checkdmarc) `Apache-2.0` — validate SPF and DMARC records for a sending domain.
- [parsedmarc](https://github.com/domainaware/parsedmarc) `Apache-2.0` — parse DMARC reports into something you can monitor.
- [Mautic](https://github.com/mautic/mautic) `GPL` — self-hosted marketing automation: campaigns, segments, lead scoring.

## Scheduling, analytics and attribution
Where intent shows up, and where you measure it.
- [cal.diy](https://github.com/calcom/cal.diy) `MIT` — scheduling infrastructure for inbound booking and round-robin routing.
- [PostHog](https://github.com/PostHog/posthog) `MIT, enterprise parts separate` — product analytics, replay and flags; product usage as an intent signal.
- [Plausible](https://github.com/plausible/analytics) `AGPL-3.0` — cookie-free web analytics for campaign and UTM tracking.
- [Dub](https://github.com/dubinc/dub) `AGPL-3.0, enterprise parts separate` — link management with conversion tracking.
- [Formbricks](https://github.com/formbricks/formbricks) `AGPL-3.0, enterprise parts separate` — in-app surveys triggered by events.

## Measurement
Whether the spend worked, beyond last-click.
- [Meridian](https://github.com/google/meridian) `Apache-2.0` — Google's marketing mix modelling framework.
- [PyMC-Marketing](https://github.com/pymc-labs/pymc-marketing) `Apache-2.0` — Bayesian mix models and customer lifetime value.

## AI agent frameworks
What you build the engine on.
- [Claude Agent SDK](https://github.com/anthropics/claude-agent-sdk-python) `MIT` — the agent loop behind Claude Code, with tools and MCP servers.
- [OpenAI Agents SDK](https://github.com/openai/openai-agents-python) `MIT` — agents, handoffs and guardrails; the successor to Swarm.
- [LangGraph](https://github.com/langchain-ai/langgraph) `MIT` — stateful, graph-based agent orchestration.
- [LangChain](https://github.com/langchain-ai/langchain) `MIT` — the standard LLM-app toolkit.
- [CrewAI](https://github.com/crewAIInc/crewAI) `MIT` — role-based multi-agent crews.
- [AutoGen](https://github.com/microsoft/autogen) `MIT code, CC-BY-4.0 docs` — Microsoft's multi-agent conversation framework.
- [LlamaIndex](https://github.com/run-llama/llama_index) `MIT` — data framework for LLM + agent apps.
- [PydanticAI](https://github.com/pydantic/pydantic-ai) `MIT` — typed, production-minded agents.
- [Agno](https://github.com/agno-agi/agno) `Apache-2.0` — fast multi-agent runtime (formerly phidata).
- [DSPy](https://github.com/stanfordnlp/dspy) `MIT` — program LLMs with optimizable modules, not prompt strings.
- [GPT Researcher](https://github.com/assafelovic/gpt-researcher) `Apache-2.0` — autonomous research agent.

## Memory & brains
The learning layer — institutional memory that compounds.
- [mem0](https://github.com/mem0ai/mem0) `Apache-2.0` — memory layer for AI apps and agents.
- [Letta](https://github.com/letta-ai/letta) `Apache-2.0` — stateful agents with long-term memory (formerly MemGPT).

## Evals & rigor
A method you can't measure is faith — and faith doesn't belong in a pipeline. Prove it before you ship it.
- [promptfoo](https://github.com/promptfoo/promptfoo) `MIT` — regression tests for prompts and agents, runnable in CI.
- [Inspect AI](https://github.com/UKGovernmentBEIS/inspect_ai) `MIT` — evaluation framework with first-class support for agents and tool use.
- [OpenAI Evals](https://github.com/openai/evals) `MIT` — framework + registry for evaluating LLMs.
- [Ragas](https://github.com/vibrantlabsai/ragas) `Apache-2.0` — evaluation for RAG pipelines.
- [DeepEval](https://github.com/confident-ai/deepeval) `Apache-2.0` — unit-testing for LLM outputs.

## Learn the foundations
From first principles to shipping.
- [Neural Networks: Zero to Hero](https://github.com/karpathy/nn-zero-to-hero) `MIT` — Karpathy: backprop → GPT, from scratch.
- [nanoGPT](https://github.com/karpathy/nanoGPT) `MIT` — the simplest fast GPT to train and read.
- [LLM Course](https://github.com/mlabonne/llm-course) `Apache-2.0` — roadmaps + notebooks, fundamentals → deployment.
- [Generative AI for Beginners](https://github.com/microsoft/generative-ai-for-beginners) `MIT` — Microsoft's 21-lesson course.
- [OpenAI Cookbook](https://github.com/openai/openai-cookbook) `MIT` — task-oriented recipes.
- [Claude Cookbooks](https://github.com/anthropics/claude-cookbooks) `MIT` — Anthropic recipes: tool use, RAG, agents.
- [Claude Quickstarts](https://github.com/anthropics/claude-quickstarts) `MIT` — deployable starter apps.
- [Anthropic Courses](https://github.com/anthropics/courses) — prompt engineering, tool use, evals.

## Related lists
- [awesome-marketing](https://github.com/marketingtoolslist/awesome-marketing) `MIT` — a broad index of marketing tools and reading, not limited to open source.
- [awesome-gtm-engineering](https://github.com/marketinguys/awesome-gtm-engineering) `MIT` — a list with the same name and a different scope: tagging, attribution and analytics. Last updated June 2025.

---

## Why this list
Most "awesome AI" lists are link dumps. This one is curated by a working GTM engineer around one question: *what do you actually build a go-to-market system out of?* Every entry is checked against the repository itself — it exists, and the licence tag is what its licence file says. No clones, no rebrands — just the map.

Three rules keep it honest:

- **The licence tag is the real one.** "Open source" is used loosely in this space. Where a project is source-available, or keeps part of the code under a commercial licence, the tag says so.
- **No star counts.** They are stale within weeks and say little about fit.
- **No profiling tools.** Research here means accounts and public company signals, not assembling a person's private accounts.

**Contributions welcome** — see [CONTRIBUTING.md](CONTRIBUTING.md).

## License
[MIT](LICENSE) — the curation is yours to reuse. Each linked project keeps its own license (shown inline).
