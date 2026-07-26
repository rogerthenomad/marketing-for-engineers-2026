# 6. Open Source and Product-Led Growth

> Open source is the most powerful distribution mechanism available to an engineer with no
> budget, and the most reliable way to build a business you don't own. Both statements are
> true. This chapter is about choosing deliberately rather than discovering the trade-off
> after you've made it.

---

## 6.1 Open source as go-to-market

When it works, open source solves the two hardest problems a technical product has: **trust**
(they can read the code) and **distribution** (they can try it without asking anyone). No amount
of content marketing buys either.

What it does not solve is revenue. The gap between "widely used" and "paid for" is where most
commercial open-source companies live, and every strategy below is an answer to that gap.

- [Roadmap: Open Source](https://www.bvp.com/atlas/roadmap-open-source) — Bessemer's open-source investment thesis and maturity framework, built on analysis of the largest public GitHub repositories. The most rigorous free overview of how OSS companies actually monetise.
- [Open Source: From Community to Commercialization](https://a16z.com/open-source-from-community-to-commercialization/) — a16z's four-stage open-source go-to-market model and which internal function owns each stage.
- [Heavybit Library](https://www.heavybit.com/library) — including [Open Source Go-To-Market and Enterprise Readiness](https://www.heavybit.com/library/video/open-source-go-to-market-and-enterprise-readiness) and [How to Start an Open-Source Project](https://www.heavybit.com/library/article/how-to-start-an-open-source-project). The deepest free archive on this topic.
- [Measuring the engagement of an open source software community](https://www.bvp.com/atlas/measuring-the-engagement-of-an-open-source-software-community) — a framework for community health that isn't star-counting.

---

## 6.2 Licensing is a go-to-market decision

Between 2018 and 2026 a series of companies discovered that a permissive licence plus a
hyperscaler is a difficult business model, relicensed to something source-available, and got
forked. The pattern is now well enough established that you can plan around it.

The short history, because it's the most useful thing to know before you pick a licence:

- **MongoDB moved to SSPL in 2018**, setting the template.
- **Elastic moved to SSPL / the Elastic License in 2021** and was forked by AWS into **OpenSearch**.
- **HashiCorp moved Terraform to BUSL 1.1 in August 2023** and was forked within weeks into **OpenTofu**, which was donated to the Linux Foundation. IBM subsequently acquired HashiCorp; Terraform did not return to its original licence.
- **Redis moved to RSALv2/SSPL in March 2024** and was forked into **Valkey** under the Linux Foundation.
- **Elastic added AGPLv3 back in August 2024**, and **Redis added AGPLv3 back with Redis 8 in May 2025** — the first reversals of the trend.

**The lesson is not "never relicense."** It is that the community's counter-move — fork, and put
the fork under a neutral foundation — is now fast and reliable, and the forks retain substantial
adoption even after the original relicenses back. Relicensing is a strategy with a known,
non-refundable cost. Price it in advance.

### Fair source: the third way

Since 2024 there's been a serious attempt to name the middle ground honestly rather than stretch
the definition of "open source" to cover it.

- [fair.io](https://fair.io/) — publicly readable source, minimal use restrictions to protect the producer's business model, and **Delayed Open Source Publication**: the code becomes properly open on a timer. Stewarded by Chad Whitacre (Sentry) and Zeke Gabrielse (Keygen).
- [Functional Source License](https://fsl.software/) — Sentry's simpler BUSL alternative; converts to Apache-2.0 or MIT after two years rather than four.
- [Sentry is now Fair Source](https://blog.sentry.io/sentry-is-now-fair-source) — the announcement and, more usefully, the reasoning.
- [Some startups are going 'fair source' to avoid the pitfalls of open source licensing](https://techcrunch.com/2024/09/22/some-startups-are-going-fair-source-to-avoid-the-pitfalls-of-open-source-licensing/) — the best neutral explainer. (2024, TechCrunch)

The honest framing for a solo engineer: **fair source is a good answer if your fear is a
hyperscaler, and an unnecessary complication if it isn't.** Most side projects are not at risk of
being resold by AWS, and a permissive licence buys adoption that a source-available one doesn't.

---

## 6.3 GitHub stars are a compromised metric

This deserves its own section now, because the situation changed materially.

Stars were always a weak proxy. They are now actively gamed at scale. The definitive work is
academic, not a blog post:

- [Six Million (Suspected) Fake Stars in GitHub: A Growing Spiral of Popularity Contests, Spams, and Malware](https://arxiv.org/abs/2412.13459) — He, Yang, Burckhardt, Kapravelos, Vasilescu and Kästner (CMU / NC State). Built a detector for low-activity and lockstep starring across GitHub's full metadata. Fake-star activity surged from 2024; most fake stars promote short-lived malware repositories; and — the finding that matters commercially — **fake stars only help for under about two months, and become a liability afterwards.** (2024, revised)

- [ROSS Index](https://runacap.com/ross-index/) — Runa Capital's quarterly ranking of fastest-growing open-source startups by star growth, with [published methodology](https://runacap.com/ross-index/methodology/) and an [open dataset](https://github.com/RunaCapital/ROSS-Index). Useful as a landscape view; read it knowing the metric it ranks on is gameable.

**Signals that are harder to fake, and correlate better with a business:**

- Package-manager download counts, and the shape of the version-adoption curve
- Fork-to-star ratio
- Non-employee pull requests and issue velocity
- Docker pulls, or equivalent runtime-distribution telemetry
- Inbound questions that reference internals — the mark of real users, not browsers

If you're raising money, the star count will get asked about. Have the other numbers ready, and
be the person in the room who explains why they're better.

---

## 6.4 README as the landing page

Most open-source projects have exactly one high-traffic marketing page and treat it as a
technical afterthought. The README is where the decision gets made, usually in under a minute,
frequently by someone who arrived from a search result or a model's recommendation.

What consistently works:

1. **One line that says what it is and who it's for.** Not a tagline. A sentence a stranger can repeat accurately.
2. **Proof it runs, above the fold.** A terminal cast or short GIF beats three paragraphs.
3. **Install in one copyable command.**
4. **A quickstart that produces a real result in under five minutes** — the open-source form of [time to first Hello World](05-developer-marketing-and-devrel.md#the-activation-metric-that-matters).
5. **Then links out.** Full docs, architecture, contributing guide. The README's job is to earn the second click, not to be complete.
6. **An honest scope statement.** "This does not do X" prevents the issues that consume maintainer time and generate public frustration.

Two things that are marketing even though they don't look like it: a clear `CONTRIBUTING.md`, and
fast, kind responses to first-time issues. Both are cheaper than any campaign and compound
similarly.

- [GitHub Sponsors](https://github.com/sponsors) — relevant here as a credibility and relationship channel more than a revenue model.
- [Open Source Pledge](https://opensourcepledge.com/) — companies committing to pay maintainers. Worth knowing about whether you're on the giving or receiving end.

---

## 6.5 Product-led growth

PLG means the product does the work of acquiring, converting and expanding customers — trial,
use, upgrade, all without talking to anyone. It fits developer tools better than almost any other
category, because engineers *prefer* it.

### A status note, since it affects where the good material lives

**OpenView Venture Partners — the firm that popularised the term "product-led growth" — halted new
investments and dismissed most staff in December 2023, and wound down through 2024.** Its research
output was the field's reference material, so a lot of links in older articles now rot. Two things
survived usefully:

- The **SaaS Benchmarks Report** passed to [High Alpha](https://www.highalpha.com/saas-benchmarks), which continues to publish it annually.
- The people dispersed and kept writing, which is where the best current material is.

- [Growth Unhinged](https://www.growthunhinged.com/) — Kyle Poyar, formerly of OpenView. The single best free successor to that research.
- [Elena Verna](https://www.elenaverna.com/) — start with [Product-led growth is many things. But here is what it's NOT.](https://www.elenaverna.com/p/product-led-growth-is-many-things) and her [B2B Product-Led Sales Guide](https://www.elenaverna.com/p/b2b-product-led-sales-guide). The most rigorous writing on where PLG breaks down and sales has to start.
- [Product-Led Growth: How to Build a Product That Sells Itself](https://productled.com/book/product-led-growth) — the canonical book. (Wes Bush)

### Free tier, free trial, or reverse trial

The decision that determines most of your funnel economics:

- **Free tier** when the product has network or collaboration effects, or when the free user is themselves distribution — an OSS CLI, a widget with your name on it, a shared artefact other people see. The cost of a free user is a marketing cost.
- **Free trial** when the value genuinely requires the whole product and a crippled version demonstrates nothing.
- **Reverse trial** — start everyone on premium, downgrade to free at day N — when you want freemium's top-of-funnel *and* a trial's urgency. Increasingly the default for dev tools with a clean free/paid split. [Kyle Poyar's guide to reverse trials](https://www.growthunhinged.com/p/your-guide-to-reverse-trials) is the definitive write-up.

**The AI-era complication:** "free forever" is much harder when every free user costs you
inference. Free tiers built on near-zero marginal cost don't transfer to products where marginal
cost is real. Model your free tier as a marketing budget with a per-user burn rate, decide what
you're buying with it, and cap it. See [chapter 13](13-pricing-and-business-model.md).

### Activation and PQLs

**Activation is not signup.** For a developer tool it is almost never "created an account" — it's
first successful API call, first deploy, first green CI run. Find the action that predicts
retention, instrument it, and treat everything before it as funnel.

A **product-qualified lead** is a usage-signal-triggered handoff, not a form fill. Product-led
sales layers a human on top of self-serve *at the account level* — when the team using you free
has grown to the point where a conversation creates value. Elena Verna's product-led sales guide
above is the best single reference.

Benchmark numbers for activation and trial conversion circulate widely and are mostly
uncited aggregations. **Instrument your own baseline and improve against it** rather than
optimising toward someone else's median.

---

## 6.6 If you only do five things

1. Pick your licence deliberately, knowing the fork is a real and fast counter-move.
2. Rewrite your README as a landing page: one clear line, proof it runs, one-command install, five-minute win.
3. Stop reporting stars. Report downloads, non-employee contributions and adoption curves.
4. Define your activation event, instrument it, and find the biggest drop-off before it.
5. If you have a free tier, know its per-user cost and what you're buying with it.

---

**Related:** [Developer marketing and DevRel](05-developer-marketing-and-devrel.md) · [Pricing and business model](13-pricing-and-business-model.md) · [Launching](07-launching.md)

*Last reviewed July 2026. Licence status and company situations change; verify at the source
before acting. Corrections welcome — see [CONTRIBUTING.md](../CONTRIBUTING.md).*
