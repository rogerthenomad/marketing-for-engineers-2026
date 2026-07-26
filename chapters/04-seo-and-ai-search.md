# 4. SEO and AI Search (GEO / AEO)

> **The one-paragraph version.** Search stopped being a list of ten links you try to get into,
> and became an answer layer that quotes passages. The engineering work barely changed —
> crawlable, fast, well-structured pages written by people who know the subject — but the
> *measurement* changed completely, and roughly two-thirds of searches now end without a click
> to the open web. Do the boring technical work, be genuinely quotable, get mentioned in the
> places models read, and ignore almost everything being sold as "GEO."

---

## 4.1 What actually changed since 2018

The 2018 edition of this list assumed search meant ten blue links and the job was to be one of
them. Five things broke that assumption:

**1. The click is no longer the default outcome of a search.**
The most trustworthy public measurement is from Pew, not from an SEO vendor: across the real
browsing data of 900 US adults in March 2025, users clicked a traditional search result on **8%**
of page-visits where an AI summary appeared, versus **15%** where it did not. They clicked a
source *cited inside* the AI summary on just **1%** of visits, and ended their browsing session
entirely on 26% of AI-summary pages versus 16% otherwise.

- [Do people click on links in Google AI summaries?](https://www.pewresearch.org/short-reads/2025/07/22/google-users-are-less-likely-to-click-on-links-when-an-ai-summary-appears-in-the-results/) — the single best-sourced data point in this entire field: real browsing data, transparent method, no product to sell. (2025-07-22, Pew Research Center)

**2. Answers are assembled from passages, not pages.**
Google's AI surfaces use *query fan-out*: one prompt is decomposed into many parallel sub-queries,
and candidate passages are scored somewhat independently of your blue-link position. The practical
consequence is disorienting the first time you see it — **a page can rank #1 and never be cited,
and a page that ranks nowhere can be quoted** because one of its sections was the cleanest answer
to a sub-question.

At I/O in May 2026 Google merged AI Overviews and AI Mode into a single unified search experience
rather than two distinct surfaces, and made the AI mode core to the product. Anything written
before then that treats them as separate things to optimise for separately is describing a
structure that no longer exists. The passage-level mechanic is what carried over, and it's the
part that matters.

**3. A second, smaller discovery channel appeared.**
ChatGPT, Perplexity, Gemini, Claude and Copilot collectively refer roughly **1% of web referral
traffic** as of early 2026 — growing fast, still small, and consistently reported to convert better
than generic organic because the visitor arrives after a recommendation. Treat it as a *quality*
channel, not a volume replacement, and instrument it before you invest in it (see 4.7).

**4. Off-site mentions matter more than links for AI visibility.**
Every large-N 2026 study lands in the same place: being *talked about* in the sources models read
predicts AI visibility better than your backlink profile does. Ahrefs' study of 75,000 brands put
branded web mentions at 0.664 correlation against backlinks at 0.218. Read that as correlation on
big brands, not a causal recipe — Ahrefs also sells the tool that measures it — but the practical
implication matches what good marketers already did.

**5. Publishing volume stopped being a strategy.**
It died twice: first with Google's helpful-content guidance, then again when generative AI made
thin content free to produce and Google named **scaled content abuse** in its spam policies.

### What did *not* change

Crawlability. Internal linking. Covering a subject properly instead of chasing scattered keywords.
Real named authors who know the thing they're writing about. Fast, stable pages. One canonical URL
per thing. Every credible 2026 study lands back on these, which is why this chapter spends more
words on `robots.txt` than on prompt engineering.

---

## 4.2 Start here: the primary sources

Read Google's own documentation rather than a blog's paraphrase of it. It is short, free, updated,
and consistently less breathless than the industry writing about it.

- [Google Search Essentials](https://developers.google.com/search/docs/essentials) — the replacement for the old Webmaster Guidelines. Technical requirements, spam policies, key practices. Start here.
- [Creating helpful, reliable, people-first content](https://developers.google.com/search/docs/fundamentals/creating-helpful-content) — the "Who / How / Why" self-assessment questions. The closest thing to a content spec Google publishes.
- [SEO Starter Guide](https://developers.google.com/search/docs/fundamentals/seo-starter-guide) — deliberately short. Google's own position is that most sites need less technical SEO than vendors imply.
- [Spam Policies for Google Web Search](https://developers.google.com/search/docs/essentials/spam-policies) — read *scaled content abuse* and *site reputation abuse* before any programmatic SEO project.
- [AI Features and Your Website](https://developers.google.com/search/docs/appearance/ai-features) — how AI surfaces source content, and which controls you actually have (`nosnippet`, `max-snippet`, `data-nosnippet`, `Google-Extended`).
- [Optimizing your website for generative AI features on Google Search](https://developers.google.com/search/docs/fundamentals/ai-optimization-guide) — added by Google in 2026 and now the most authoritative single page on this topic. It explicitly mythbusts `llms.txt`, content "chunking" and AI-specific rewriting. If you only read one link in this chapter, read this one — it settles most arguments before they start.
- [Overview of Google crawlers and fetchers](https://developers.google.com/search/docs/crawling-indexing/overview-google-crawlers) — the authoritative user-agent list.
- [Search Quality Rater Guidelines (PDF)](https://static.googleusercontent.com/media/guidelines.raterhub.com/en//searchqualityevaluatorguidelines.pdf) — the E-E-A-T source document. Not a ranking factor; it's the spec human raters are graded against, which makes it the best public description of what Google is *trying* to reward.
- [Google Search Status Dashboard](https://status.search.google.com/summary) — authoritative start/end dates for ranking and spam updates. Use this instead of trusting a blog's timeline.
- [Core Web Vitals](https://web.dev/articles/vitals) — LCP, INP, CLS. **INP replaced FID in March 2024**; any guide still saying "FID" is stale.

---

## 4.3 GEO and AEO: what the evidence actually supports

There is exactly one piece of peer-reviewed work at the root of this entire discipline, and almost
nobody selling "GEO services" has read past its abstract.

- [GEO: Generative Engine Optimization](https://arxiv.org/abs/2311.09735) — Aggarwal, Murahari, Rajpurohit, Kalyan, Narasimhan and Deshpande (IIT Delhi / Princeton), published at **KDD 2024**. Black-box-tested nine content tactics against a generative-engine benchmark. The methods that won were **adding quotations, adding statistics, and citing sources** — worth roughly a 30–40% relative visibility lift on their metric. Keyword stuffing did not win.

**Read the caveat that practitioners skip:** those results come from a 2023–24 research harness
(Google top-5 retrieval feeding GPT-3.5 synthesis), not from today's Google AI Mode or ChatGPT
search. The "+40%" gets quoted as a 2026 guarantee. It is not one. **Cite the method, distrust the
number.**

What the method tells you is genuinely useful, and it is not exotic: *write passages a machine can
lift and a reader can trust.* Named statistics with their sources. Direct quotes from named people.
Self-contained sections that answer one question without requiring the four paragraphs above them.
This is what good editors have always asked for.

### Supported by evidence

- **Being quotable.** Self-contained factual passages, statistics with attribution, quotes from named experts.
- **Being mentioned off-site** — Reddit, YouTube, review sites, industry press, Wikipedia/Wikidata. Unlinked brand mentions outrank backlinks as an AI-visibility correlate in every large 2026 study.
- **Being crawlable by the right bots** — see 4.4. This is the single most common real cause of "we don't appear in AI answers."
- **Being unambiguous about entity identity** — one consistent name and description everywhere, `Organization` schema with `sameAs`, an accurate Wikidata entry if you qualify for one.

### Not supported, and widely sold anyway

- **`llms.txt` as a ranking or citation lever.** See 4.5.
- **"Chunking" your pages for AI**, or maintaining a separate AI-only version of a page. Google has said rewriting for AI isn't required, and cloaking an AI-only variant is a spam violation.
- **Schema markup as a citation lever.** It's a rich-result eligibility lever. Different thing (4.6).
- **FAQ-block stuffing and "brand density" writing.**
- **Anyone guaranteeing AI citations.** Nobody controls model outputs. A guarantee is a promise to sell you sampling noise.

Useful counterweights when someone sends you a GEO deck:

- [GEO isn't a fad — but most GEO tactics won't survive](https://martech.org/geo-isnt-a-fad-but-most-geo-tactics-wont-survive/) — the sane middle position. (MarTech)
- Search the arXiv listings for recent critical surveys of the GEO literature before believing a vendor's causal claim — the academic work is consistently more skeptical than the commercial work.

---

## 4.4 The highest-leverage 30 minutes: bot control

Most "we're invisible in AI answers" problems are not content problems. They are a line in
`robots.txt` or a checkbox in a CDN dashboard. Several CDNs shipped AI-bot blocking as a
default-on feature, so this is frequently something nobody on your team chose.

**The distinction almost everyone gets wrong: training crawlers and search-time fetchers are
different bots.** Blocking the training bot does not remove you from that product's search
results. Blocking the search-time fetcher does.

| Vendor | Training crawler | Search-time / user fetch |
|---|---|---|
| OpenAI | `GPTBot` | `OAI-SearchBot` (index), `ChatGPT-User` (live fetch) |
| Anthropic | `ClaudeBot` | `Claude-SearchBot`, `Claude-User` |
| Google | `Google-Extended` (Gemini/Vertex training opt-out) | `Googlebot` — **includes AI Overviews and AI Mode** |
| Perplexity | `PerplexityBot` | `Perplexity-User` |

Two things worth knowing:

- **This changed in mid-2026: you can now opt out of Google's AI surfaces and stay in Search.** For most of the AI-search era the honest answer was that you couldn't — `Google-Extended` governs model training, not AI Overviews, and your only lever was snippet control (`nosnippet`, `max-snippet`, `data-nosnippet`), which cost you ordinary snippets too. In June 2026 Google began rolling out a Search Console control that excludes a site from AI Overviews and AI Mode while leaving classic Search and Discover intact, and states it is not a ranking signal elsewhere. The change was forced by a legally binding UK CMA conduct requirement under Google's Strategic Market Status designation rather than offered voluntarily, and Google has a nine-month implementation window from June 2026 — so **check whether the control is available for your property before assuming it is.** If you find older guidance saying opt-out is impossible, that guidance predates this.
- The common 2026 posture is **block training, allow search-time.** That's a business decision, not a technical default. Make it deliberately — and note that opting out of AI surfaces means opting out of a channel, not just a risk.

**Checklist:**

1. Read your live `robots.txt` — the one being served, not the one in your repo.
2. Check your CDN/WAF bot rules separately. Cloudflare's managed robots feature can override your origin file.
3. Confirm the search-time fetchers are allowed if you want to appear in AI answers.
4. Verify server-side rendering: several AI fetchers do not execute JavaScript. If your content only exists after hydration, they see an empty page.

---

## 4.5 `llms.txt`: the honest status

**Short version: not used by Google Search, not a standard, and not a search-visibility lever — but
it found a real second life as a documentation-delivery format for AI coding tools.**

Google's position has been consistent and public since John Mueller's June 2025 comparison of
`llms.txt` to the meta keywords tag: no AI search system has been shown to use it for ranking or
citation, and Google's own AI-features guidance says you don't need to create new machine-readable
files, AI text files, or Markdown to appear in Google Search including its generative features.
Measured adoption remains in the single-digit percentages of top sites.

**Where it genuinely helps — the dev-tools exception.** AI coding assistants (Cursor, Claude Code,
Copilot, Cline, Aider and friends) *will* read `/llms.txt` and `/llms-full.txt` when a user points
them at your docs. Anthropic, Stripe, Vercel and Cloudflare all ship one. If you sell a developer
product, `llms-full.txt` makes your API materially easier to code against, which is a real
distribution win in an era where an agent is often the first thing to read your documentation.

**So: ship it as a docs feature, not as an SEO tactic.** Anyone selling it as the latter is either
behind or hoping you are. See [chapter 5](05-developer-marketing-and-devrel.md) for why agent-readable
docs are becoming a genuine channel.

---

## 4.6 Structured data: still useful, for the other thing

Structured data is **not** required for, and is not a special lever for, AI Overviews or AI Mode.
Google has said there is no AI-specific markup. What it still does is earn **rich results** in
classic SERPs and help machines resolve *entity identity* — which is an indirect but real input to
being described correctly.

- [Intro to how structured data works](https://developers.google.com/search/docs/appearance/structured-data/intro-structured-data) — start here.
- [Search gallery / rich result types](https://developers.google.com/search/docs/appearance/structured-data/search-gallery) — the only authoritative list of markup that actually produces a SERP feature.
- [Structured data general guidelines](https://developers.google.com/search/docs/appearance/structured-data/sd-policies) — eligibility, quality and spam rules.
- [Rich Results Test](https://search.google.com/test/rich-results) and [Schema Markup Validator](https://validator.schema.org/) — the two validators worth bookmarking.

**Worth marking up for a dev tool, in priority order:**

1. `Organization` with `sameAs` pointing at your GitHub, LinkedIn, X and Wikidata. Cheap, permanent, and the highest-value entity-disambiguation move you can make.
2. `SoftwareApplication` / `SoftwareSourceCode` on product and docs pages.
3. `Article` / `BlogPosting` with a real `author` that resolves to a real person page. This is the schema half of E-E-A-T.
4. `BreadcrumbList`.
5. `Product` + `Offer` + `AggregateRating` **only if you have genuine reviews.** Fabricating these is an explicit spam-policy violation and, in the US, now also an FTC matter (see [chapter 15](15-privacy-and-compliance.md)).

**Stop building:** `FAQPage` rich results have been restricted to government and health sites since
2023, and `HowTo` rich results were dropped. Marking up an FAQ for SERP display is close to
zero-value now.

**Ignore** the widely circulated vendor claims that structured data produces a "+73% AI Overview
selection rate" or "2.5x higher chance of appearing in AI answers." Neither has a published
methodology.

---

## 4.7 Measurement, and the free stack that covers most of it

Rank tracking is now a partial view of a partial channel. What to watch instead: impressions in
generative surfaces, branded search volume, referral hosts, self-reported attribution, and assisted
conversions.

**The free stack, which genuinely covers ~80% of what a small team needs:**

- [Google Search Console](https://search.google.com/search-console/about) — free, non-negotiable, and the only source of your own Google impression and position data. In June 2026 Google began adding generative-AI performance reporting that breaks out AI-surface impressions from ordinary Search. **Two catches:** it is **impressions only** — no clicks, no CTR, no query data, with click data promised but undated — and it is a **staged rollout** that started with a subset of site owners rather than launching globally. Check whether your property has it before building a process around it. You can finally see AI-surface visibility; you still can't price it.
- [Bing Webmaster Tools](https://www.bing.com/webmasters/) — free, and matters more than it used to because Copilot leans on Bing's index.
- [Ahrefs Webmaster Tools](https://ahrefs.com/webmaster-tools) — genuinely free, no card, for domains you verify and own. Site audit plus your own backlinks and ranking keywords. No competitor data — that's the paid upsell.
- [Screaming Frog SEO Spider](https://www.screamingfrog.co.uk/seo-spider/) — free up to 500 URLs with no JS rendering. For a docs site under 500 pages that is often genuinely enough.
- [PageSpeed Insights](https://pagespeed.web.dev/) and [Lighthouse](https://developer.chrome.com/docs/lighthouse/overview) — free Core Web Vitals. INP is the one JS-heavy dev-tool sites usually fail.
- **A referrer report in your analytics.** Costs nothing and ends the arguing. Segment on `chatgpt.com`, `perplexity.ai`, `gemini.google.com`, `claude.ai`, `copilot.microsoft.com`. Build this before you buy anything in the next section.

**Paid, when you've outgrown the above:** Ahrefs and Semrush both run laddered plans from roughly
$100/month into the high hundreds; Sitebulb is the friendliest technical crawler for engineers who
don't do SEO daily. Check current pricing directly — every vendor in this space repriced during
2025–26 and any number printed in a list like this is stale on arrival.

**AI-visibility trackers** (Profound, Peec, Otterly, Scrunch, plus Ahrefs Brand Radar and Semrush's
AI toolkit) measure how often a model mentions or cites you across a prompt set. That is a
legitimate metric. It is **not** a ranking system, prompt sets are small and hand-chosen, and
sampling noise is large. If you already pay for Ahrefs or Semrush, their bundled version is the
cheaper first step. **Do not buy one until you have written down the question it will answer.**

---

## 4.8 The dev-tool playbook

### Documentation SEO

Docs are usually the largest and highest-intent organic surface a developer tool owns, and where
the ugliest technical-SEO bugs live.

- [How to do SEO for documentation projects](https://docs.readthedocs.com/platform/latest/guides/technical-docs-seo-guide.html) — the best free vendor-neutral guide, written by people who host docs rather than by an SEO agency. (Read the Docs)

The failure modes, in the order they usually bite:

1. **Versioned docs without canonicals.** `/v1/`, `/v2/`, `/latest/`, `/next/` all indexed means you compete with yourself. Index current stable, `rel=canonical` the rest to it, `noindex` pre-release.
2. **Client-side-only rendering.** Several AI fetchers don't run JS. SSR or SSG your docs.
3. **Every page titled `Docs | Product`.** Kills both SERP CTR and passage identification.
4. **API reference as one giant page.** One page per endpoint — descriptive H1, parameters, runnable example — is both better docs and a better retrieval unit.
5. **Unstable heading anchors.** AI answers cite deep links; unstable IDs break them permanently.
6. **Changelogs unindexed.** They're strong long-tail magnets for "does X support Y."
7. **Docs-search pages indexed.** Classic infinite-URL crawl trap.

### Comparison and "alternatives to X" pages

Still the highest-converting organic page type a dev tool can own, and now doubly valuable because
"what are the alternatives to X" is one of the most common things people ask an assistant.

Rules that keep them working and out of trouble:

- **Date them and state the version compared.** Competitors change pricing, and a stale claim gets quoted back at you by a model long after you've corrected the page.
- **Be fair enough to be believable.** Say where the competitor is genuinely better. Reviewers, Reddit and LLMs all reward this; pure hit pieces rarely get cited.
- **Never fabricate ratings markup.**
- **Use competitor names nominatively** — referring to their product, not in your own branding, with no implied affiliation. Get counsel if you plan to be aggressive here; this is not legal advice.

### Programmatic SEO

Not dead — but the risk is now explicit policy rather than folklore. Google's **scaled content
abuse** rules cover generating many pages "whether through automation, humans, or a combination"
primarily to manipulate rankings.

The line Google draws is **unique value per page**, not "was a template involved":

- **Safe:** pages built on data you actually have and nobody else does. Per-integration pages backed by a real integration. Per-error-code pages backed by real error semantics. Benchmark pages with your own measurements.
- **Unsafe:** `{keyword}` swap-ins over boilerplate. "Best X for Y" with no first-hand testing. Auto-generated comparisons of competitors you've never used. Thin per-city pages for a product with no local component.
- **The test:** if you can't say what a human learns on page 400 that they couldn't get on page 1, don't ship pages 2–400.

This is one of the few areas where being an engineering-led company is a structural advantage —
you have real data and can generate genuinely differentiated pages from it. Most of your
competitors are swapping keywords into a template.

---

## 4.9 Myths worth naming

- **"Add `llms.txt` and AI will prioritise you."** No AI search system has been shown to use it for ranking. Ship it for AI *coding* assistants; that's a different, real use case.
- **"There's special schema for AI Overviews."** There isn't, and Google says so.
- **"GEO is a new discipline that replaces SEO."** The winning tactics in the only peer-reviewed GEO study are quotes, statistics, cited sources and clear writing. Most "GEO" offerings are technical SEO plus digital PR with new packaging.
- **"Ahrefs proved YouTube causes AI citations, so start a channel."** Correlation, measured on big brands, by the company selling the measurement tool.
- **"Rank tracking is the KPI."** With roughly two-thirds of searches ending click-free and answers assembled from passages, position is a weak proxy for anything.
- **"Blocking GPTBot is free protection."** Only if you know which bot does which job. Block the wrong one and you remove yourself from a discovery surface.
- **Keyword density, LSI keywords, meta keywords, submitting your site to search engines, PageRank sculpting, AMP, and "domain authority is a Google metric."** All still dead. DA and DR are vendor metrics; Google has never used them.

---

## 4.10 If you only do five things

1. Check `robots.txt` **and** your CDN bot rules. Decide training vs. search-time deliberately.
2. Verify your docs are server-rendered, canonicalised across versions, and have stable anchors.
3. Add `Organization` schema with `sameAs`, and put real named authors on real author pages.
4. Build the AI-referrer report in your analytics. It's free and it ends the speculation.
5. Write two or three genuinely fair, dated comparison pages for the competitors you actually lose deals to.

Everything else in this chapter is optimisation on top of those.

---

**Related:** [Content marketing](03-content-marketing.md) · [Developer marketing and DevRel](05-developer-marketing-and-devrel.md) · [Analytics and attribution](12-analytics-and-attribution.md)

*Sources in this chapter were last reviewed in July 2026. Platform mechanics, pricing and policy
in this area change faster than any list can track — treat every specific number as "as reported"
and re-check the primary source before making a decision on it. Corrections welcome; see
[CONTRIBUTING.md](../CONTRIBUTING.md).*
