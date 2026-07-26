# 16. The AI Marketing Stack

> Marketing automation used to mean an email tool and a spreadsheet. This chapter is what it
> means now. The single most useful principle in it: **LLMs are excellent at transformation and terrible
> at origination.** Every genuinely valuable AI marketing workflow reshapes material you
> already have. Every slop workflow invents material you don't.

---

## 16.1 Where LLMs actually earn their keep

**Ship these:**

- **Extraction and structuring.** Pull objections, feature requests and exact customer phrasing out of support tickets, call transcripts and review sites into a schema. This is the highest-value marketing use of an LLM and almost nobody does it. The output is verifiable against the source, which is what makes it safe.
- **Repurposing.** One substantial artefact — a talk, an RFC, an incident post-mortem, a customer call — becomes a thread, a newsletter section, a changelog entry, five clip captions. The facts already exist; the model only reframes them.
- **Variant generation for testing.** Twenty subject lines, ten headline angles. The model's job is to widen the search space; yours is to judge.
- **Research synthesis with sources in context.** Give it the material and ask for synthesis. **Never ask it to recall.**
- **Editorial QA.** "Which claims here are unsupported?" "List every number that needs a source." LLMs are better critics than authors, and a false positive costs a human ten seconds.
- **Plumbing.** Rewriting four hundred alt texts, normalising UTM taxonomies, converting a CSV into a tracking plan.

**Don't:**

- Net-new "thought leadership" with no input material. The model has no opinions, only an average of everyone else's.
- Programmatic content at volume with no unique data behind it — now an explicit Google spam-policy violation, not a grey area.
- Anything containing a number, date, price, customer name or legal claim, unreviewed.
- Persona and ICP invention. An LLM-invented persona is a plausible-sounding average that will misroute your entire funnel. See [chapter 1](01-positioning-and-audience.md).
- Anything where the value *is* the human voice: founder posts, customer stories, apologies, incident communications.

### What Google actually says, since almost everyone gets this wrong

Google's **scaled content abuse** policy replaced the older "spammy automatically generated
content" policy in March 2024. The definition covers generating many pages primarily to
manipulate rankings, producing large amounts of unoriginal low-value content — **"no matter how
it's created."**

That clause is load-bearing and deliberately method-agnostic. **AI authorship is not the
violation.** Scale plus unoriginality plus no user value is the violation, and a human content
farm breaches it identically.

- [Spam policies for Google Web Search](https://developers.google.com/search/docs/essentials/spam-policies) — the canonical source. Read it before any programmatic project.
- [AI-generated content does not hurt your Google rankings](https://ahrefs.com/blog/ai-generated-content-does-not-hurt-your-google-rankings/) — analysis of roughly 600,000 pages: the overwhelming majority of top-ranking pages contain *some* AI-generated content, very few are purely AI, and the correlation between AI share and ranking is statistically indistinguishable from noise. The best-performing pattern is AI-assisted and human-edited. (2025, Ahrefs — who sell SEO software; read accordingly, but the methodology is stated.)

**The real risk in 2026 is not a penalty.** It's that you publish two hundred indistinguishable
pages, they rank adequately, nobody cares, and you've spent a year building an asset with no
distribution moat and no reason for anyone to cite it. Ranking is no longer the constraint;
being worth citing is.

A useful cultural marker: **Merriam-Webster's 2025 word of the year was "slop"** — "digital
content of low quality that is produced usually in quantity by means of artificial
intelligence." The audience now has a name for your content strategy's failure mode. Volume
plays carry negative brand equity in a way they didn't in 2023.

---

## 16.2 Agentic marketing

- [Model Context Protocol](https://modelcontextprotocol.io) — the open protocol connecting LLM clients to tools and data. This is the thing that genuinely changed marketing tooling: your CRM, analytics and CMS become callable by an agent without writing an integration.
- [modelcontextprotocol/servers](https://github.com/modelcontextprotocol/servers) — the official reference server collection. Start here rather than at a "best MCP servers for marketers" listicle — several of those assert official servers that are actually community forks. MCP governance moved to the Linux Foundation's Agentic AI Foundation, and the official registry is still in preview, so a listing there is not yet meaningful distribution.

**What agents are genuinely good at right now** is the read-heavy, low-blast-radius half:
research and reporting. "Pull last month's organic performance, cross-reference it against the
content calendar, and tell me which posts underperformed and why" works today and is a real step
change. Anything that *writes* — sends an email, posts publicly, updates a CRM record — is a
different risk class entirely.

### The risk list, stated bluntly

- **Hallucinated facts in outbound.** An agent that invents a prospect's headcount or a mutual connection has made a factual misrepresentation with your name on it. **The mitigation is architectural, not prompt-level:** pull facts from a system of record, template the factual slots, and let the model choose only phrasing.
- **Blast radius.** Marketing agents get credentials to the CRM, the ESP and the social accounts — write access to your customer relationships and your public voice. A bad support reply is one bad interaction; a bad ESP-connected agent is forty thousand of them in ninety seconds. **Rate-limit and dry-run every write path, and require human approval on anything that fans out.**
- **Prompt injection via untrusted marketing data.** Your agent reads inbound leads, form submissions, review sites and social replies — all attacker-controlled text. An agent with CRM write access reading a lead-form "company description" field is a live injection surface. Treat every scraped or user-submitted string as hostile.
- **Brand drift.** Agents erode tone and claims over hundreds of generations in a way no single review catches. Keep a golden set of on-brand outputs and run it like a test suite.

**Vendor-hype flag:** "agentic" is 2026's "AI-powered." Most products described as agentic
marketing platforms are a workflow builder with an LLM node. That's often useful — but it is n8n
with better branding, and you should price it accordingly.

---

## 16.3 Automation, and reading the licence

This is where awesome-lists get embarrassed, so these were verified directly against each
project's licence file:

| Tool | Licence | Honest description |
|---|---|---|
| [n8n](https://github.com/n8n-io/n8n) | **Sustainable Use License** | **Not OSI open source.** n8n's own term is *fair-code*. Internal business or non-commercial use only; redistribution only free of charge and non-commercially. `.ee.` files are separately licensed. Self-hosting for your company is fine; building a product on it needs a licence read. |
| [RudderStack](https://github.com/rudderlabs/rudder-server) | **Elastic License 2.0** | **Not OSI open source.** Forbids offering it as a hosted service. The widely repeated "RudderStack is the open-source Segment alternative" line is wrong. |
| [Jitsu](https://github.com/jitsucom/jitsu) | **MIT** | The actually-open-source event pipeline. Smaller ecosystem, no licence landmines. |
| [Windmill](https://github.com/windmill-labs/windmill) | **AGPLv3 + Apache-2.0**, enterprise carve-out | Open source with an EE carve-out. Turns scripts into workflows, UIs and cron jobs. |
| [Temporal](https://github.com/temporalio/temporal) | **MIT** | Durable execution. Overkill for "post to Slack on form submit"; exactly right when a lifecycle workflow must survive crashes and run for ninety days. Underused in marketing. |
| [Postiz](https://github.com/gitroomhq/postiz-app) | **AGPL-3.0** | Genuinely open-source social scheduling. |
| [Listmonk](https://github.com/knadh/listmonk) | **AGPL-3.0** | Genuinely open-source newsletter manager. |
| [Mixpost](https://github.com/inovector/mixpost) | **MIT core** | MIT core (Lite); Pro and Enterprise are separately sold. Say "MIT core, commercial Pro." |
| [Whisper](https://github.com/openai/whisper) | **MIT** | Free, accurate, self-hostable transcription. |

**Commercial options:** [Zapier](https://zapier.com) has the widest catalogue, the highest
per-task cost and the lowest engineering effort — correct for the long tail of one-off glue, and
it stops making sense the moment a workflow runs at volume. [Make](https://www.make.com) offers
real branching, iterators and error handlers at meaningfully lower cost, with a steeper learning
curve — note it now bills in credits rather than per operation, so old cost comparisons mislead.

**Reality check on self-hosting to save money:** an n8n or Listmonk instance is a production
service with a database, a queue, secrets, an upgrade path and an on-call rotation. It's cheaper
in dollars and more expensive in attention. Be honest about which one you're short of.

**On CDPs:** most teams under roughly $10M ARR don't need one. They need one tracking plan, one
warehouse, and dbt. Buying a CDP early mostly buys you a second place for your event schema to rot.

---

## 16.4 CRM and GTM data

- [HubSpot free CRM](https://www.hubspot.com/products/crm) — the free tier is usable but capped (notably at 1,000 contacts), and the on-ramp is the point: pricing escalates steeply and migration out is real work. Now also the most agent-accessible CRM, with official MCP servers for both CRM access and development.
- [Attio](https://attio.com) — CRM as a relational database: custom objects, real API, webhooks, workflow builder. The right pick for a technical team that would otherwise build a CRM in Postgres.
- [Folk](https://www.folk.app) — deliberately lightweight and spreadsheet-shaped. Right for 0–10 people wanting same-day setup; wrong if you plan to automate against it.
- [Clay](https://clay.com) — the data-orchestration layer that defined the category: many enrichment providers behind one waterfall, plus LLM research agents for fields no provider has. Powerful, and extremely easy to spend money on — credit consumption is what people underestimate.

**Clearbit is not an independent product.** It was acquired by HubSpot in December 2023 and
folded into Breeze Intelligence. Any 2026 list still saying "Clearbit — enrichment API" is
copying a list that stopped being updated years ago.

**Is "GTM engineering" real?** Yes as a *practice* — treating pipeline generation as a
data-and-automation engineering problem rather than a headcount problem. Inflated as a *title*:
the term was popularised largely by Clay and its agency ecosystem, and many postings describe
someone who can operate Clay, Apollo and a scraper. The practice is worth learning; the title is
marketing.

---

## 16.5 Content operations

**The pipeline that works:** one substantial source artefact per week → transcript → structured
extraction of claims, quotes and hooks → derivative formats → human edit → publish.

Note the direction: **one thing becomes many.** Every failing content operation runs the
opposite way, starting from a calendar of topics and manufacturing filler to fit it.

- [Whisper](https://github.com/openai/whisper) — MIT-licensed, self-hostable, and still the pragmatic default for a repurposing pipeline because of its licence and ecosystem rather than raw accuracy: several newer open models now beat it on benchmarks. Transcripts are the highest-leverage artefact in content ops — searchable, diffable, and the input to everything downstream.
- [Descript](https://www.descript.com) — edit video and audio by editing the transcript. A genuine step change for people who think in text rather than timelines.

**Editorial QA with AI is the one AI content workflow with no downside.** Run every draft
through a checker for unsupported claims, numbers without sources, voice drift, broken internal
links and accessibility. It's classification and extraction — exactly what LLMs are reliable at.
Wire it into CI on your content repo.

---

## 16.6 Social scheduling, and a lesson about platform risk

- [Buffer](https://buffer.com) — durable, unexciting, multi-channel, with approvals and reporting.
- [Typefully](https://typefully.com) — writing-first. Best when the bottleneck is the writing rather than the workflow.
- [Postiz](https://github.com/gitroomhq/postiz-app) — the genuinely open-source, self-hostable option.

**X's API has been repriced four times in three years** — the 2023 removal of free access
killed an entire generation of Twitter tools, and the model changed again in 2026 toward
pay-per-use for new developers. Check [the official pricing page](https://docs.x.com/x-api/getting-started/pricing)
rather than trusting any number printed in a list like this one.

**The durable lesson is not the prices.** Any distribution strategy built on a single platform's
API is one pricing announcement away from zero. Own the email list.

---

## 16.7 If you only do five things

1. Build the extraction workflow: support tickets and call transcripts into structured customer language. Highest-value AI use in marketing, and almost nobody does it.
2. Wire an editorial-QA pass into CI for anything you publish.
3. Ship the reporting agent; gate every write path behind dry runs and human approval.
4. Read the licence before you call something open source in public.
5. Prefer boring, durable infrastructure. Postgres plus a workflow engine plus a decent ESP will outlive most vendors in this chapter.

---

**Related:** [Email and lifecycle](09-email-and-lifecycle.md) · [Privacy and compliance](15-privacy-and-compliance.md) · [Content marketing](03-content-marketing.md)

*Licence claims above were verified against each project's licence file in July 2026; licences
change, so re-check before relying on one. Corrections welcome — see
[CONTRIBUTING.md](../CONTRIBUTING.md).*
