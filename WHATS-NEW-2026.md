# What Changed for 2026

A chapter-by-chapter account of what was added, rewritten, and removed relative to the
[2018 original](https://github.com/goabstract/Marketing-for-Engineers). Written so you can see
the reasoning, disagree with it, and correct it.

If you only read one section, make it [The graveyard](#the-graveyard).

---

## The five things that changed the most

**1. Search stopped being ten blue links.**
Roughly two-thirds of searches now end without a click to the open web. Answers are assembled
from *passages* via query fan-out, so a page can rank first and never be cited, or rank nowhere
and be quoted. The 2018 list's entire model of SEO — rank, get the click, convert — describes a
minority case now. → [Chapter 4](chapters/04-seo-and-ai-search.md)

**2. Your first reader is often not a person.**
A coding agent reads your docs, resolves your package name, and picks your library before a human
sees your homepage. Machine-readable surfaces (`AGENTS.md`, `llms-full.txt`, MCP servers) became a
distribution channel. Gated content and "book a demo" walls became actively hostile, because an
agent can't fill in your form. → [Chapter 5](chapters/05-developer-marketing-and-devrel.md)

**3. Publishing volume stopped working.**
When competent generic content became free to produce, it stopped differentiating anything.
Google named *scaled content abuse* in policy; readers coined "slop." What survives is what a
model can't generate: your data, your incident, your benchmark, your name.
→ [Chapter 3](chapters/03-content-marketing.md)

**4. Attribution broke, and no tool fixes it.**
ATT, zero-click search, AI intermediation and dark social mean your dashboard systematically
under-credits demand *creation* and over-credits demand *capture*. The 2026 answer is
triangulation — self-reported attribution, incrementality tests, and mix modelling — not a better
dashboard. → [Chapter 12](chapters/12-analytics-and-attribution.md)

**5. Several 2018 growth tactics are now enforcement matters.**
Fake reviews (including AI-generated ones), undisclosed insider endorsements, bought upvotes and
astroturfed threads moved from "distasteful" to "regulated," with civil penalties.
→ [Chapter 14](chapters/14-psychology-and-ethics.md) and [Chapter 15](chapters/15-privacy-and-compliance.md)

---

## New chapters that didn't exist in 2018

| Chapter | Why it's here |
|---|---|
| [5. Developer marketing and DevRel](chapters/05-developer-marketing-and-devrel.md) | The original had no coverage of marketing to engineers, despite being written for engineers. Its single biggest gap. |
| [6. Open source and PLG](chapters/06-open-source-and-plg.md) | Licensing as a go-to-market decision, the 2018–2025 relicensing wars, and why GitHub stars became a compromised metric. |
| [12. Analytics and attribution](chapters/12-analytics-and-attribution.md) | The original had no analytics chapter. It could get away with that; we can't. |
| [15. Privacy and compliance](chapters/15-privacy-and-compliance.md) | GDPR got one line in 2018. Since then: ATT, Consent Mode v2, twenty-odd US state laws, the FTC reviews rule, and the EU AI Act. |
| [16. The AI marketing stack](chapters/16-ai-marketing-stack.md) | The original's "Marketing Automation" chapter had two entries. |
| [14. Psychology **and ethics**](chapters/14-psychology-and-ethics.md) | The psychology chapter survived; the ethics half is new, and they belong together. |

---

## Chapter-by-chapter

**User Research + Market Research → [1. Positioning and audience](chapters/01-positioning-and-audience.md)**
Demographic buyer personas replaced with positioning (Dunford) and jobs-to-be-done. Nearly every
free research tool from the original is dead — see the graveyard. New failure mode named: asking
an LLM to *be* your customer instead of talking to one.

**Marketing without Budget → [2. Zero-budget growth](chapters/02-zero-budget-growth.md)**
The chapter that aged best. Paul Graham's *Do Things that Don't Scale* survives intact. Rebuilt
around what differentiates now that generic content is free to produce, plus an honest timeline
of how slow this actually is.

**Content Marketing (3 sub-chapters) → [3. Content marketing](chapters/03-content-marketing.md)**
The Medium sub-chapter is gone entirely (see graveyard). Reframed from "get the click" to "be
quotable," which is what the only peer-reviewed research on generative-answer optimisation
actually supports.

**Product Hunt → [7. Launching](chapters/07-launching.md)**
Reframed from growth event to credibility event. Adds Hacker News properly, the underrated
surfaces (package registries, `homebrew-core`, awesome-lists), and replaces the original's
tolerance of "seeding discussions" with the FTC rule.

**Social Media (Twitter/Facebook/Reddit/LinkedIn/Quora) → [8. Communities and social](chapters/08-communities-and-social.md)**
The most heavily rewritten chapter. Reddit went from "place you get banned" to the most-cited
domain in AI answers. Stack Overflow died as a channel. Quora and Facebook Pages dropped. Added
Bluesky, Mastodon, Discord, and a community-platform decision table. YouTube promoted to "most
underrated channel for dev tools."

**Lifecycle + Cold Email → [9. Email](chapters/09-email-and-lifecycle.md) and [10. Outbound](chapters/10-outbound-and-partnerships.md)**
Resolves the original's contradiction — it disavowed cold email post-GDPR and then listed eleven
cold-email tools. Deliverability promoted to the front, because Google/Yahoo (2024, tightened
2025) and Microsoft (2025) made authentication mandatory and now *reject* non-compliant mail.

**Facebook/Twitter Ads → [11. Paid acquisition](chapters/11-paid-acquisition.md)**
Substantially shorter, and opens by telling most readers not to run ads yet. The targeting the
original described no longer exists.

**Business Model and Pricing → [13. Pricing and business model](chapters/13-pricing-and-business-model.md)**
Heavily expanded. Per-seat decline, hybrid pricing, outcome pricing and when it actually works,
and the big one: **AI COGS made gross margin a pricing input**, which invalidates a lot of
inherited SaaS advice about free tiers.

**Moving to SaaS + Marketing Automation → [16. AI marketing stack](chapters/16-ai-marketing-stack.md)**
Complete rebuild, including a licence table verified against each project's licence file.

---

## The graveyard

Removed, with reasons. This is the most useful part of the document.

### Dead outright

| Thing | What happened |
|---|---|
| **Alexa.com** web analytics | Amazon retired it in May 2022. Alexa Rank no longer exists. |
| **Social Mention** | Long unmaintained, and the domain now resolves to an unrelated follower-selling "SMM panel." Linking it would send readers to a service that sells fake engagement. |
| **Nuzzel** | Went dark in 2021 after Twitter acquired its parent. |
| **Siftery** | Acquired by G2 in 2018; standalone product shut down. |
| **Pablo by Buffer** | Sunset in November 2024. Buffer points users to Canva. |
| **Hashtagify, Twitonomy, Scoutzen** | Killed by X's 2023 API repricing, along with the whole free-Twitter-analytics category. |
| **Attach.io** | Absorbed into Cirrus Insight. |
| **Ginger** | Acquired by Grammarly in 2020 and folded in. |
| **The Startup Chat podcast** | Last episode December 2020. |
| **500hunters, productrunt, phlics, tophuntsdaily, makertools.xyz** | The 2018 cohort of one-person Product Hunt directories has near-total mortality. The "get a big hunter to hunt you" dynamic they served no longer exists. |
| **lisearcher.com** | Offline for years, and LinkedIn X-ray scraping is ToS-adjacent regardless. |
| **SnoopSnoo** | Original site gone; a community revival exists at a different domain. |

### Removed on principle

- **The BAMF Bible** — a 2017 growth-hack compendium built almost entirely on LinkedIn/Facebook automation and engagement pods. Every one of those channels is now closed or a ban risk. Historical curiosity, not advice.
- **Salesfolk** — the agency is not a going concern and its founder pleaded guilty in a multi-billion-dollar money-laundering case. Removed entirely rather than relinked.
- **Every "buy upvotes" and mass-directory-submission service** that now dominates search results for launch advice. See [chapter 7](chapters/07-launching.md#76-astroturfing-is-now-a-legal-exposure-not-a-growth-tactic).
- **Follow/unfollow scripts, auto-DM tools, and the LinkedIn automation category** — ToS violations with real account-loss risk, and they stopped working anyway.

### Platforms whose value collapsed

- **Medium** — the original devoted a whole sub-chapter to it as a distribution engine. It's now paywalled with a fraction of the reach that advice assumed. Own your domain.
- **Quora** — audience largely evaporated into AI chat.
- **Stack Overflow** — question volume fell to levels last seen around 2008 after ChatGPT. The clearest death in the list, and unusually, one you can verify yourself through Stack Exchange's public Data Explorer.
- **Facebook Pages** — organic reach for brand pages has been negligible for years.
- **X for link distribution** — link posts are suppressed; reach is unreliable without an existing following.
- **Product Hunt as an acquisition channel** — still valuable for credibility and press; no longer a traffic firehose, and the AI category is saturated.

### Alive but no longer what the original described

- **Typeform** — cut its free tier drastically in 2026. No longer honest to recommend as a free tool. Tally and Formbricks are the replacements.
- **Hootsuite** — removed its permanent free plan. Buffer, which kept one, is now the better recommendation.
- **BuzzSumo** — moved upmarket after acquisition; the free tier is too thin for the original's use case.
- **Appcues** — now effectively sales-led pricing; no longer plausible for a bootstrapped engineer.
- **Sumo.com** — acquired and rebuilt under a new name; the old free growth-app store is gone.
- **Followerwonk** — changed hands twice, and structurally degraded by X's API pricing regardless of owner.
- **Copyscape** — still works for verbatim duplication, but can't detect paraphrased or AI-rewritten text, which is now the dominant case.
- **Moz** — acquired by Ziff Davis in 2021; Rand Fishkin left in 2018 and founded SparkToro. Still useful, no longer category-defining.
- **UserOnboard teardowns** — the archive is still instructive, but it documents interfaces that no longer exist. Linked as an archive.
- **Drift** — acquired, and a gradual sunset of the standalone product was announced. Not recommended for new builds.
- **Segment** — alive under Twilio, with a far more restrictive free tier than in 2018.

### Kept, because they're still the best thing available

Paul Graham on doing things that don't scale · Really Good Emails · AlternativeTo · Buffer ·
Canva · Crisp · Customer.io · Mixpanel · Vero · World Time Buddy · Jon Loomer on Meta ads ·
Grow and Convert (which has itself repositioned around generative-engine optimisation) ·
Awesome-Indie · Stripe Atlas guides.

---

## Editorial decisions worth stating

**Fewer links, better links.** The original's value was breadth. Link rot has taught the whole
awesome-list ecosystem that breadth is a liability. This edition prefers canonical, stable URLs —
official documentation, primary research, project repositories — over deep links to blog posts
that will 404 within two years.

**Every number is attributed and dated.** Where a figure comes from a vendor who sells the thing
it measures, the chapter says so. Where no primary source could be traced, the number was cut
rather than repeated — this removed a lot of widely circulated statistics about Product Hunt
upvote thresholds, Hacker News front-page rates, Reddit ad performance, and SaaS pricing shifts.

**The list tells you when something doesn't work.** Naming a dead tactic is more useful than
quietly omitting it, because someone is otherwise going to find the 2018 advice and follow it.

**Chapters say what to do if you only do five things.** Curated lists are easy to admire and hard
to act on.

---

## Known gaps

Stated plainly, because a list that hides its weaknesses isn't useful:

- **Link verification was partial.** The research environment blocked direct fetches to most hosts, so links were verified through search indexing rather than HTTP response codes. A full link check from an unrestricted network is the highest-priority next task. See [issue-worthy work](CONTRIBUTING.md).
- **US/EU bias.** Guidance on marketing to and from other regions is thin.
- **No B2C depth.** The list assumes a technical or B2B buyer throughout.
- **Conference and event marketing** is barely covered.
- **Some fast-moving facts will already be stale**, particularly pricing, AI-search mechanics, and the EU AI Act's implementation detail, parts of which were still in flux in mid-2026.

Corrections are the most valuable contribution you can make. See [CONTRIBUTING.md](CONTRIBUTING.md).

---

*Compiled July 2026. See [CREDITS.md](CREDITS.md) for the original's authors, who deserve them.*
