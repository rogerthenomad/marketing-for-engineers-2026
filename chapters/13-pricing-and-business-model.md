# 13. Pricing and Business Model

> Pricing is the highest-leverage marketing decision you will make, and the one engineers
> most consistently defer until it's expensive to change. The 2018 edition of this list
> treated it as a late-stage concern. In 2026, with inference costing real money on every
> request, **your billing unit is an architectural decision** — pick it before you build.

---

## 13.1 Start here

If you have never priced anything, read one book and steal one framework.

- **Monetizing Innovation** (Ramanujam & Tacke, 2016) — still the best first book on pricing for someone technical. The whole discipline compressed: *have the willingness-to-pay conversation before you write the code.* Its examples predate AI; its logic doesn't.
- **Scaling Innovation** (Ramanujam & Hartman, 2025) — the sequel, and where the AI-era monetisation framework lives. The single most useful new pricing book for this edition.

Ramanujam's AI-pricing framework is worth internalising even if you read nothing else. It's a
2×2 of **autonomy** (how independently your product works without a human) against
**attribution** (how cleanly you can tie its work to a business outcome). **High autonomy plus
high attribution is the only quadrant where outcome-based pricing actually works.** Everything
else should be a subscription or a hybrid. Most products that think they should charge per
outcome cannot measure the outcome, and discover this after signing the contract.

- [Pricing and scaling your AI product: lessons from 400+ companies](https://www.lennysnewsletter.com/p/pricing-and-scaling-your-ai-product-madhavan-ramanujam) — the free long-form version of that framework. (Lenny's Newsletter)

---

## 13.2 The 2026 shift: from selling access to selling work

The structural change is simple to state. **Per-seat pricing is in decline because agents do
work that used to require a seat.** If your software replaces the user, you cannot bill the
user.

What replaced it is not pure usage-based pricing — it's **hybrid**: a subscription or platform
floor plus a consumption layer on top, usually denominated in credits. That's now the most
common shape in B2B software, and the default recommendation for an AI-inflected product.

The four models, and when each is right:

| Model | Bill on | Use when |
|---|---|---|
| **Subscription / seat** | Access | Your COGS per user is bounded and predictable, and humans are the ones doing the work |
| **Consumption** | Tokens, API calls, runs | Costs scale with usage and you want clean margins |
| **Workflow** | Tasks completed | Closer to how work actually happens; cost variability is higher |
| **Outcome** | Results delivered | Only when you can *measure* the result cheaply and cap your downside |

The canonical outcome-pricing example is **Intercom Fin**, which charges per resolved
conversation — a model that held up and got widely copied across customer-support AI. Note what
makes it work: the outcome is unambiguous, cheap to verify, and directly valuable. If yours
isn't all three, don't copy the model.

- [The AI pricing playbook for founders](https://www.bvp.com/atlas) — Bessemer's founder-facing framing of consumption vs. workflow vs. outcome. Their Atlas library is the best free VC publication on this topic.
- [Growth Unhinged](https://www.growthunhinged.com/) — Kyle Poyar's annual monetisation survey and the [pricing](https://www.growthunhinged.com/t/pricing) archive. The single best free source on SaaS and AI pricing.
- [The Pricing Conundrum](https://thepricingconundrum.substack.com/) — narrower, pricing-only, good on outcome models.

**A warning about the statistics in this space.** Specific figures for the seat-to-hybrid shift
circulate constantly and mostly originate in billing-vendor content marketing with no traceable
primary study. The direction of travel is well-supported. The precise percentages usually
aren't. Don't quote them.

---

## 13.3 AI changed the margin structure, and that changes everything downstream

This is the most important economic shift since the last edition of this list, and it's easy to
miss because it shows up in accounting rather than in product.

Classic SaaS is built once and served to the next customer at near-zero marginal cost. That's
where 80–90% gross margins came from, and *every* piece of standard SaaS advice — free tiers,
generous trials, land-and-expand, unlimited plans — is downstream of that fact.

**An AI product spends real inference on every query.** COGS scales *with* usage instead of
amortising across it. AI-native gross margins have run substantially below classic SaaS,
improving as companies optimise but not converging to 90%.

Three consequences you have to design around:

1. **Gross margin is a pricing input, not an afterthought.** Compute CAC payback on gross profit, not revenue. With materially lower margins, the answer changes.
2. **"Unlimited" is a balance-sheet risk**, not a marketing flourish. Never ship unlimited on top of a metered model.
3. **The margin levers are engineering decisions.** Model routing (cheap model by default, escalate rarely), prompt caching, batching where latency permits, and retrieval instead of stuffing context. Collectively these move the number a lot — which means **your pricing team and your inference architecture are the same conversation.**

- [The New Business of AI (and How It's Different From Traditional Software)](https://a16z.com/the-new-business-of-ai-and-how-its-different-from-traditional-software/) — the origin text of the "AI margins are structurally worse" argument. Written in 2020, before the LLM boom, and largely vindicated by it. The concepts hold; the numbers are dated.

---

## 13.4 Free tiers in the AI era

Freemium made sense when a free user cost approximately nothing. Now the free tier is a metered
liability that scales with adoption — and the users who consume most are disproportionately the
ones least likely to convert. The squeeze is that you have to throttle the free experience
*before* the user has felt enough value to pay, which is exactly backwards from how freemium is
supposed to work.

Across 2025–26 the industry repriced accordingly: providers raised prices, some killed free
tiers outright, and others fell back on the oldest answer to "who pays for the free users" —
advertising.

**What to actually do:**

1. **Meter in the unit that costs you money** — tokens, generations, runs — not in time or seats. A 14-day unlimited trial on an inference-heavy product is an uncapped liability.
2. **Give away the cheap model, sell the expensive one.** Model routing is a pricing decision.
3. **Prefer a credit grant to "unlimited with fair use."** Credits are legible to the user and bounded for you.
4. **Consider a trial instead of a free tier.** Free-forever made sense when storage was the only marginal cost.
5. **Price high enough that you want the usage.**

Cross-reference [chapter 6 on free tier vs. free trial vs. reverse trial](06-open-source-and-plg.md#free-tier-free-trial-or-reverse-trial) for the acquisition side of the same decision.

---

## 13.5 Positioning: the work that has to happen before pricing

You cannot price something you can't position. If prospects don't know what category you're in,
they have no reference price, and every conversation becomes an education project.

- **Obviously Awesome** (April Dunford, 2019) — the default answer for engineers who built something good and can't explain it. The method: list the competitive alternatives, isolate your genuinely unique attributes, map those to the value they enable, identify who cares disproportionately, then deliberately choose the market frame you want to be judged in.
- **Sales Pitch** (April Dunford, 2023) — the sequel, on saying it out loud. Builds the pitch around presenting the buyer's alternatives honestly rather than parading features, which makes it unusually compatible with how engineers prefer to sell.
- [April Dunford's site](https://www.aprildunford.com/) — hosts a free workbook with the Positioning Canvas and Sales Pitch Storyboard. The highest-value free artefact in this chapter.
- [A step-by-step guide to crafting a sales pitch that wins](https://www.lennysnewsletter.com/p/a-step-by-step-guide-to-crafting) — the best free long-form version of the framework.

**Jobs to Be Done** — the complementary lens. Instead of asking who your customer is
demographically, ask what progress they were trying to make when they hired your product.

- [Know Your Customers' "Jobs to Be Done"](https://hbr.org/2016/09/know-your-customers-jobs-to-be-done) — the canonical short version. (2016, Christensen, Hall, Dillon & Duncan / HBR)
- **Demand-Side Sales 101** (Bob Moesta, 2020) — JTBD applied to selling. The best sales book for people who hate selling.

**Category design** — *Play Bigger* (2016) argues that the company which defines a category
captures the overwhelming majority of the value created in it. Worth reading, with a caveat this
list will state plainly: **it is the most survivorship-biased idea in this chapter.** It
describes winners well and predicts them badly. For a solo engineer it's almost always the wrong
first move; Dunford's positioning is.

---

## 13.6 Finding the actual number

Ranked by how much you should trust the answer:

1. **Charge someone real money.** Nothing else is evidence. A signed invoice beats a hundred survey responses.
2. **Gabor-Granger** — walk a real prospect up and down concrete price points and record acceptance.
3. **[Van Westendorp Price Sensitivity Meter](https://en.wikipedia.org/wiki/Van_Westendorp%27s_Price_Sensitivity_Meter)** — four questions (too cheap / cheap / expensive / too expensive) that yield a defensible range from around fifty responses. Cheap to run, easy to abuse: it measures *stated*, not revealed, willingness to pay.
4. **Surveys about feelings.** Don't.

For the tactical layer — anchoring, tier structure, how many plans, where to put the annual
toggle — Nick Kolenda's pricing work is the highest-ROI reading for someone about to design a
pricing page. His site moved to [kolenda.io](https://www.kolenda.io/); older lists still point at
the previous domain.

---

## 13.7 The metrics, and which ones apply to you

Definitions worth spelling out, because they get used loosely:

- **NRR / NDR** — revenue from an existing cohort a year later, including expansion, minus contraction and churn. Above 100% means you grow with zero new customers.
- **GRR** — the same, without expansion. **GRR is the honest churn number**; NRR can hide a leaky bucket behind upsells.
- **CAC payback** — months of *gross-profit-adjusted* revenue to repay acquisition cost. Use gross profit. With AI COGS this materially changes the answer.
- **Burn multiple** — net burn divided by net new ARR. Coined by David Sacks in [The Burn Multiple](https://medium.com/craft-ventures/the-burn-multiple-51a7e43cb200) (2020). Under 1× is excellent; over 2× is a problem.
- **Rule of 40** — growth rate plus profit margin ≥ 40. A late-stage heuristic that is close to meaningless below roughly $5M ARR. If you're pre-$1M and someone asks about your Rule of 40, they're pattern-matching, not thinking.

### The AI-native divergence

The single most important benchmarking finding for anyone shipping an AI product: **growth is
faster and retention is worse, simultaneously.** AI-native companies routinely traverse
$1M to $10M ARR in well under a year — far quicker than the old breakout-SaaS standards — while
retention benchmarks for AI-native products have come in dramatically below classic SaaS norms.

The variable that rescues it appears to be **price point**: enterprise-priced AI products retain
far better than cheap self-serve ones, which churn ferociously.

**Read those retention figures carefully before applying them to yourself.** The published
cohorts are likely dominated by inexpensive self-serve products, and may not describe your
business at all. The practical implication for an engineer shipping something small: your growth
chart will look spectacular and your cohort chart will look alarming. Budget for it, price
higher, sell annual, and **do not raise money against a three-month revenue curve.**

**Benchmark sources worth your time:**

- [SaaS Capital research](https://www.saas-capital.com/research/) — **the most relevant benchmarks for this audience**, because they survey bootstrapped companies rather than venture-backed ones.
- [ChartMogul Insights](https://chartmogul.com/insights/) — free reports built on real aggregated subscription data rather than survey self-report.
- [Bessemer Atlas](https://www.bvp.com/atlas) — highest signal-per-word VC publication on cloud and AI business models.

---

## 13.8 Business models for shipping something small

**Incorporation and money plumbing**

- [Stripe Atlas](https://stripe.com/atlas) — US entity, EIN, founder stock, 83(b), template legal pack in one flow. The default for a non-US founder who needs a standard US entity quickly.
- [Stripe Atlas guides](https://stripe.com/guides/atlas-guides) — **the free library is the real value**, independent of whether you incorporate through them. Note the URL moved; older lists point at the wrong path.

**Communities and canonical texts**

- [Indie Hackers](https://www.indiehackers.com/) — the interview archive of real revenue numbers remains the draw. Acquired by Stripe in 2017 and bought back by its founders in 2023; independent again.
- [MicroConf](https://microconf.com/) — the conference and community for bootstrapped B2B SaaS, with a large free talk archive.
- [MAKE: The Indie Maker Handbook](https://readmake.com/) — Pieter Levels. Continuously updated since 2018. Opinionated, occasionally dogmatic, still the most honest account of shipping many small products fast. (The old `makebook.io` domain has been superseded.)

**Model choices**

- [open-business-models](https://github.com/protontypes/open-business-models) — a curated list of open-source business models. The best starting point for "how do I make money from something I open-sourced."
- **Open core** — free core, paid enterprise edge (SSO, RBAC, audit logs, compliance). The reliably paid feature set is boring and enterprise-shaped, which is the point. Caveat: foundation-governed projects generally *can't* do open core; it requires single-vendor control.
- **Sponsorware** — ship privately to sponsors first, open-source at a threshold. GitHub Sponsors, Open Collective and Polar are the rails.
- **Marketplace and plugin distribution** — the highest-leverage channel available to a solo engineer, because *the marketplace supplies the demand*. VS Code, JetBrains, Shopify, Figma, Chrome Web Store, Raycast, Obsidian — and, new since the last edition, **MCP server and agent-tool registries**, which are roughly where app stores were early on: low competition, high intent. The trade-off is a platform take rate, policy risk, and no direct customer relationship.
- **Micro-SaaS** — one narrow job, one narrow audience, $20–200/month, run by one or two people. Realistic ceiling is low-six-figure ARR at far lower effort than a venture path. Benchmark against bootstrapped data, not VC data.

---

## 13.9 If you only do five things

1. Write your Onliness sentence — "we are the only X that Y for Z" — before you touch a pricing page.
2. Pick your billing unit before you build, and make sure it's the unit that costs you money.
3. Compute CAC payback on gross profit, not revenue.
4. Replace "unlimited" with a credit grant everywhere it appears.
5. Charge someone real money as early as possible. It's the only pricing research that counts.

---

**Related:** [Positioning and audience](01-positioning-and-audience.md) · [Open source and PLG](06-open-source-and-plg.md) · [Analytics and attribution](12-analytics-and-attribution.md)

*Last reviewed July 2026. Pricing pages and benchmark reports change constantly — verify any
specific figure at the source. Corrections welcome — see [CONTRIBUTING.md](../CONTRIBUTING.md).*
