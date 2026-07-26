# 5. Developer Marketing and DevRel

> **Most marketing guides have no chapter like this**, which is why so much of their advice
> bounces off technical audiences. If your buyer is an engineer, almost every tactic in the
> classic playbook either doesn't work on them or actively repels them — and since roughly 2024
> your first reader often isn't a human at all.

---

## 5.1 Why marketing to engineers is different

Developers self-educate, evaluate by building, distrust anything that smells like a funnel, and
route around gated content and sales calls. They will read your source before they read your
homepage. They will ask a colleague, a subreddit, or a model before they ask your sales team.

The consequence is not "don't do marketing." It is that the marketing surface *is the product
surface*: docs, quickstarts, error messages, the README, the free tier, the SDK. Anything that
makes a developer succeed faster is marketing. Anything that makes them fill in a form to find
out whether your product does the thing is anti-marketing.

- [Developer Marketing Does Not Exist: The Authentic Guide to Reach a Technical Audience](https://everydeveloper.com/developer-marketing/book/) — the canonical short book on the thesis, by someone who ran developer content at SendGrid and Zapier. Put the conventional toolbox away and engage honestly. (2021, Adam DuVander / EveryDeveloper)
- [Developer Marketing and Relations: The Essential Guide](https://www.slashdata.co/resources/developer-marketing-book) — the multi-author reference volume; broader and drier than DuVander, useful as a lookup. (SlashData; eds. Caroline Lewko, Nicolas Sauvage, Andreas Constantinou)
- [SlashData](https://www.slashdata.co/) and [Developer Nation](https://www.developernation.net/) — the long-running quantitative surveys on developer population, tool adoption and channel preference. The best available answer to "how do developers actually discover tools."
- [Draft.dev Learn](https://draft.dev/learn/) — free library on technical content operations, from an agency that only does technical content.
- [Developer Markepear](https://www.developermarkepear.com/) — dev-tool positioning and messaging teardowns. Good for calibrating your own homepage against the field.

---

## 5.2 The state of DevRel

Be clear-eyed about this if you're deciding whether to hire for it. DevRel was hit
disproportionately in the 2023–2025 tech layoffs, and the pattern was consistent: **teams that
could not connect their activity to a business outcome were cut first.** Conference talks and
community vibes were not a defence. Teams that had instrumented their contribution — pipeline
influenced, activation lifted, support burden reduced — largely survived.

The counter-trend is institutional. The Linux Foundation formed a **Developer Relations
Foundation** in 2025, which is the biggest structural change the discipline has seen, publishing
open persona libraries, tool catalogues and strategy frameworks rather than leaving every team to
reinvent them.

- [developerrelations.com](https://developerrelations.com/) — Hoopy's hub: the talks archive, the annual [State of Developer Relations report](https://developerrelations.com/reports/), and [DevRelCon](https://developerrelations.com/devrelcon/). The primary source for how the field is actually doing.
- [Developer Relations Foundation](https://www.linuxfoundation.org/press/linux-foundation-announces-the-formation-of-the-developer-relations-foundation) — the Linux Foundation's DevRel project, formed 2025. Open frameworks instead of folklore.
- [DevRel Roadmap](https://roadmap.sh/devrel) — community skills map; a decent onboarding artefact for someone new to the role.
- [DevRel Scribbles](https://scribbles.devrel.page/) — community-maintained notes wiki. Unusually practical.

### Measurement, which is now the whole job

- [Measuring Developer Relations](https://swyx.io/measuring-devrel) — still the most-linked practical essay on the problem. Start here. (swyx / Shawn Wang)
- [DevRel Qualified Leads](https://www.marythengvall.com/blog/2019/12/14/devrel-qualified-leads-repurposing-a-common-business-metrics-to-prove-value) — the origin of the DQL. Crucially, a DQL is a *connection passed to the right internal team*, deliberately **not** a sales metric. Misusing it as one is how DevRel teams get restructured into SDRs. (2019, Mary Thengvall)
- Mary Thengvall's *The Business Value of Developer Relations* (Apress, 2018) remains the standard text on justifying the function internally.

**Metrics that survive scrutiny:** time to first successful API call, activation rate, package
downloads and version-adoption curves, non-employee PR and issue velocity, support-ticket
deflection, pipeline where a DQL was the first touch.

**Metrics that don't:** talk count, follower count, event attendance, "impressions," and GitHub
stars (see [chapter 6](06-open-source-and-plg.md)).

### Communities aren't funnels

- [The Orbit Model](https://github.com/orbit-love/orbit-model) — concentric orbits (advocates → contributors → participants → observers) instead of a funnel, on the reasoning that community members *pull themselves inward* rather than being pushed toward one conversion goal. `Gravity = Love × Reach`.
- [Communities aren't funnels — try the Orbit Model instead](https://speakerdeck.com/dzello/communities-arent-funnels-try-the-orbit-model-instead) — the canonical talk. (Josh Dzielak)

**Status note worth knowing:** the *company* Orbit was acquired by Postman and shut down in 2024,
and the model repo is no longer actively developed. The framework is still the clearest way to
think about community measurement; just don't go looking for the product. [Common Room](https://www.commonroom.io/) was the obvious successor, but it pivoted toward
go-to-market intelligence and was acquired by Zoom in July 2026 — and its entry pricing is well
beyond a small team. There is currently **no cheap, obvious community-CRM for a small dev tool**,
which is worth knowing before you go shopping for one.

---

## 5.3 Docs are the marketing

For a developer tool, documentation is simultaneously the landing page, the sales demo, the
onboarding flow, the support deflection layer, and — since about 2024 — the thing an AI agent
reads on the buyer's behalf. It is almost always the highest-leverage marketing surface the
company owns, and it is almost always owned by nobody in particular.

### Structure

- [Diátaxis](https://diataxis.fr/) — the dominant documentation architecture: four modes (tutorials, how-to guides, reference, explanation) separated along two axes. Adopted by Python, Django, Canonical/Ubuntu, Cloudflare and many others. If your docs feel bad and you can't say why, it's usually because these four are blended into one.
- [Diátaxis, a new foundation for Canonical documentation](https://ubuntu.com/blog/diataxis-a-new-foundation-for-canonical-documentation) — the best "we adopted this at scale and here's what happened" case study.
- [What is Diátaxis and should you be using it?](https://idratherbewriting.com/blog/what-is-diataxis-documentation-framework) — a critical read rather than a fan post. (Tom Johnson)
- [I'd Rather Be Writing](https://idratherbewriting.com/) — the best long-running blog on API documentation, and since 2024 the most thoughtful place on what AI does to it.

### The activation metric that matters

**Time to first Hello World (TTFHW)** — how long from landing on your docs to a developer getting
a real response back. It is the single number most predictive of whether a dev tool converts, and
it is measurable in a way that "brand awareness" is not.

- [What is TTFHW?](https://www.moesif.com/blog/technical/api-product-management/What-is-TTFHW/) — definition and how to instrument it.
- [What Comes After Hello World?](https://everydeveloper.com/after-hello-world/) — the second-step problem: most docs win the first five minutes and lose the next fifty. (Adam DuVander)

Instrument the drop-off between "signed up" and "first successful call," then fix the biggest
step. That work outperforms almost any campaign you could run with the same hours.

### Tooling

- [Docusaurus](https://docusaurus.io/) — Meta's open-source React docs framework. Free, endlessly customisable, still the default for OSS projects.
- [Starlight](https://starlight.astro.build/) — Astro's docs theme. Very fast, low-JS, increasingly the choice for OSS docs that care about Core Web Vitals.
- [Mintlify](https://www.mintlify.com/) — AI-first hosted docs: MDX, OpenAPI ingestion, an assistant trained on your docs, `llms.txt` output. Common default for new commercial dev-tool docs.
- [Fern](https://buildwithfern.com/) — spec-first: one OpenAPI file generates docs *and* type-safe SDKs. Best fit if you're genuinely API-first. Acquired by Postman in January 2026, which broadened its input formats and is worth factoring into a long-term bet.
- [ReadMe](https://readme.com/) — interactive reference with a try-it explorer and per-user usage analytics. Strongest on onboarding telemetry.
- [Redocly](https://redocly.com/) and [GitBook](https://www.gitbook.com/) — the other two serious contenders.
- [OpenAPI Initiative](https://www.openapis.org/) — your spec is now a marketing asset, not just an engineering one. It generates the reference docs, the SDKs, the Postman collection, the `llms.txt`, and increasingly the MCP server.

Also read [4.8 on documentation SEO](04-seo-and-ai-search.md#48-the-dev-tool-playbook) — the
technical failure modes there (unversioned canonicals, client-side-only rendering, templated
titles) quietly cost more traffic than most content strategies gain.

---

## 5.4 The agent is your first reader

This is the genuinely new thing, and it is not a small adjustment.

A coding agent increasingly reads your docs, resolves your package name, chooses your library over
a competitor's, and writes the integration — often before a human has looked at your homepage.
That makes machine-readable surfaces a **distribution channel**, not a technical nicety, and it
makes several long-standing dev-marketing habits actively harmful.

- [Introducing AX: Why Agent Experience Matters](https://biilmann.blog/articles/introducing-ax/) — coined "Agent Experience": the experience AI agents have as users of your product. The best conceptual anchor for this whole shift. (2025, Matt Biilmann, Netlify)
- [agentexperience.ax](https://agentexperience.ax/) — the community site that followed.
- [Beyond DX: Developers Must Now Learn Agent Experience (AX)](https://thenewstack.io/beyond-dx-developers-must-now-learn-agent-experience-ax/) — independent coverage. (The New Stack)

### The surfaces

- [`AGENTS.md`](https://agents.md/) — the open format for instructing coding agents inside a repository. Emerged from OpenAI's Codex work in 2025, formalised with Google, Cursor, Factory and Sourcegraph, and since donated to the Linux Foundation's Agentic AI Foundation. Read by Claude Code, Codex CLI, Cursor, Copilot, Gemini CLI, Windsurf, Zed, Aider and others. **Shipping a good `AGENTS.md` in your examples and templates is marketing**, because it determines how well an agent succeeds with your product on the first try.
- [`llms.txt`](https://llmstxt.org/) — a curated Markdown index at `/llms.txt` plus `/llms-full.txt`, proposed by Jeremy Howard in 2024. Still a community proposal, not a standard, and — as [chapter 4](04-seo-and-ai-search.md#45-llmstxt-the-honest-status) says at length — **not a search-visibility lever.** It is a docs-delivery feature for AI coding assistants, and worth shipping on exactly those grounds.
- [Context7](https://github.com/upstash/context7) — MIT-licensed MCP server that feeds up-to-date, version-specific library docs into coding agents, specifically to stop hallucinated APIs. Getting your library indexed here is a real distribution act. (Upstash)
- [Model Context Protocol](https://modelcontextprotocol.io/) — the spec. An official MCP server puts your product inside the agent's tool list, which is roughly the 2026 equivalent of being in the IDE's plugin marketplace. Stripe, Cloudflare, GitHub, Supabase, Sentry, Vercel, Figma and Notion all ship one.
- [DeepWiki](https://deepwiki.com/) — auto-generated agent-readable wikis for public repos. Your project gets explained to agents whether you participate or not, which is a good reason to make the source explain itself well.
- **Agent Skills (`SKILL.md`)** — the newer, lighter sibling of an MCP server: a folder of instructions and scripts that teaches an agent to use your product, with no server to run. Stewarded under the same Linux Foundation umbrella as `AGENTS.md` and supported across a growing set of tools. For most small dev-tool teams this is now a **cheaper first step than shipping an MCP server**, and it is the surface moving fastest.

### The honest counterweight

**Discovery is the bottleneck, not publication.** There are thousands of public MCP servers and
most are experimental or abandoned. Shipping one gets you into a registry; it does not get you
adopted. The same will be true of every agent-facing surface within a year of it existing. Build
these because they make your product genuinely easier to succeed with, and treat any distribution
benefit as upside.

### What this makes obsolete

- **Gated content and "book a demo" walls.** An agent cannot fill in your form, and the developer who delegated the evaluation to it will simply pick the tool that documented itself in public.
- **Docs metrics based on human attention.** Sessions and time-on-page degrade as signals once agents read your docs at machine scale. Move to TTFHW, API-key activation and package downloads.
- **Depending on community Q&A for discovery.** Stack Overflow's role as a discovery channel has collapsed as developers ask models instead. Whatever share of your inbound used to arrive via someone else's answer to a question about your tool, assume it is shrinking.

---

## 5.5 Newsletters, podcasts and people

**Newsletters**

- [Growth Unhinged](https://www.growthunhinged.com/) — Kyle Poyar on PLG, pricing and benchmarks. The best free successor to the research OpenView used to publish.
- [Elena Verna](https://www.elenaverna.com/) — the sharpest writer on where product-led growth stops working.
- [Github20K](https://www.github20k.com/) — Nevo David on growing an open-source project's audience. Directly on-topic for [chapter 6](06-open-source-and-plg.md).
- [DevFirst](https://devfirst.substack.com/) — Francesca Krihely (ex-MongoDB, Snyk) on developer-first go-to-market.
- [daily.dev](https://daily.dev/) — where a meaningful share of developer content distribution actually happens now.
- [DevRel Weekly](https://devrelweekly.com/) — the long-running curated DevRel newsletter. **Now wound down** after roughly six years; the archive is still worth mining, but don't expect new issues.

**Podcasts**

- [Scaling DevTools](https://podcast.bitreach.io/) — Jack Bridger interviewing devtool founders. Consistently the most useful one in this space.
- [Open Source Ready](https://www.heavybit.com/library/podcasts/open-source-ready) — Heavybit, on open-source business models.
- [Community Pulse](https://www.communitypulse.io/) — the long-running DevRel and community show.
- [DevRel podcasts directory](https://developerrelations.com/podcasts/) — better maintained than any listicle.

**People worth following**

Adam DuVander (developer content and docs-as-marketing) · Mary Thengvall (DevRel business value)
· swyx (measurement, and now AI) · Kyle Poyar (PLG and pricing) · Elena Verna (PLG's limits) ·
Matt Biilmann (agent experience) · Daniele Procida (Diátaxis) · Tom Johnson (API docs and AI) ·
Chad Whitacre (fair source) · Josh Dzielak (community measurement) · Jack Bridger (devtool GTM).

**Hubs and other lists**

- [Heavybit Library](https://www.heavybit.com/library) — the deepest free archive of developer-first go-to-market talks and articles anywhere.
- [Nordic APIs](https://nordicapis.com/) — long-running blog and conference on API business and developer experience.
- [The New Stack](https://thenewstack.io/) — the best mainstream trade press on this beat.
- [awesome-developer-marketing](https://github.com/ronakganatra/awesome-developer-marketing) — the closest neighbouring awesome-list. Some links are stale, but it's a useful cross-check.

---

## 5.6 If you only do five things

1. Measure time to first Hello World. Fix the biggest drop-off step. Repeat.
2. Restructure your docs along Diátaxis lines — most "our docs are bad" complaints are structural, not editorial.
3. Ship an `AGENTS.md` and an `llms-full.txt`, because an agent is increasingly your first reader.
4. Delete a gate. Any gate. The one in front of the thing people need to evaluate you.
5. Pick one DevRel metric that connects to a business outcome and report it monthly, before someone asks you to justify the function.

---

**Related:** [SEO and AI search](04-seo-and-ai-search.md) · [Open source and PLG](06-open-source-and-plg.md) · [Communities and social](08-communities-and-social.md)

*Last reviewed July 2026. This area moves quickly; verify status and pricing at the source before
acting on anything here. Corrections welcome — see [CONTRIBUTING.md](../CONTRIBUTING.md).*
