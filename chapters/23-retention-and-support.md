# 23. Retention, Churn and Support

> The cheapest growth is the customer you already have. This chapter is also where this
> handbook is most careful about numbers, because retention is the topic with the highest
> density of confidently repeated statistics that nobody can source.

---

## 23.1 Where the famous numbers come from, and which one to stop repeating

The entire "retention is worth more than acquisition" literature traces back to one paper:
Reichheld and Sasser's *Zero Defections: Quality Comes to Services*, Harvard Business Review,
1990. It's worth reading the original, because the finding has drifted considerably in retelling.

- [Zero Defections: Quality Comes to Services](https://hbr.org/1990/09/zero-defections-quality-comes-to-services) — the primary source. (1990, Reichheld & Sasser / HBR)

**The claim to stop repeating: "it costs 5× more to acquire a customer than retain one."** This
number is everywhere and has no credible primary source. It gets attributed to several places,
none of which contain it. Drop it from your deck. The underlying argument — that retention
compounds and acquisition doesn't — stands perfectly well without a fake statistic.

For benchmarks you can actually cite:

- [SaaS Capital research](https://www.saas-capital.com/research/) — annual retention benchmarks with an unusually useful skew toward *bootstrapped* companies.
- [Bessemer State of the Cloud](https://www.bvp.com/atlas/state-of-the-cloud) — NDR benchmarks by segment. (VC content.)
- [ChartMogul reports](https://chartmogul.com/reports/) — drawn from real aggregated subscription data rather than survey self-report. (Vendor.)

---

## 23.2 Diagnose before you treat: involuntary churn is not churn

A large share of what teams call churn is **failed payments** — expired cards, insufficient
funds, issuer declines, and in Europe, strong customer authentication failures. This is not a
product problem or a marketing problem. It's a billing configuration problem, and it's the
cheapest revenue you will ever recover.

Fix this before you run a single retention campaign:

- Card-updater services so expiring cards refresh automatically
- Smart retry schedules rather than fixed daily retries
- Dunning emails that actually reach the inbox (see [chapter 9](09-email-and-lifecycle.md))
- Grace periods before you cut off access

- [Stripe revenue recovery documentation](https://docs.stripe.com/billing/revenue-recovery) — the clearest public documentation of how retry logic, card updaters and dunning actually work. Useful even if you don't use Stripe.
- [Strong customer authentication overview](https://stripe.com/guides/strong-customer-authentication) — why European card failure rates behave differently, which surprises US-based teams.
- [Recurly Research](https://recurly.com/research/) — churn benchmarks split by voluntary versus involuntary. (Vendor.)

**Then** look at voluntary churn — and segment it. Churn in the first 30 days is an onboarding
failure. Churn at month 12 is a value failure. They need opposite responses.

---

## 23.3 Onboarding is retention

The strongest predictor of whether someone is still a customer in six months is usually whether
they reached the activation moment in the first session. This is the same activation event from
[chapter 6](06-open-source-and-plg.md#activation-and-pqls) — first successful API call, first
deploy, first green run.

Instrument it, find the biggest drop-off before it, and fix that. Then repeat. This work
outperforms almost any retention campaign you could run with the same hours.

- [UserOnboard teardowns](https://www.useronboard.com/) — Samuel Hulick's annotated screen-by-screen teardowns of real onboarding flows. The archive documents interfaces that no longer exist, but the analytical method is the value and it transfers directly.
- [Sean Ellis product/market-fit survey](https://pmfsurvey.com/) — the "how would you feel if you could no longer use this product?" instrument. Cheap, fast, and the single most useful survey in this chapter.

---

## 23.4 NPS, CSAT and CES, honestly

- **NPS** measures relationship sentiment and is easy to game, easy to misread, and enormously popular. Its usefulness is almost entirely in the **free-text follow-up**, not the score. Track the verbatims; treat the number as a rough trend.
- **CSAT** measures satisfaction with a specific interaction. Better for support quality than for relationship health.
- **CES** measures effort. For technical products this is frequently the most predictive of the three, because friction is the thing that actually drives your users away.

- [The One Number You Need to Grow](https://hbr.org/2003/12/the-one-number-you-need-to-grow) — the NPS primary source. Worth reading precisely because the original claim is narrower than the industry built on it.
- [Net Promoter 3.0](https://hbr.org/2021/11/net-promoter-3-0) — Reichheld's own substantial revision, introducing earned growth rate. An unusual example of an author correcting his own framework.
- [Stop Trying to Delight Your Customers](https://hbr.org/2010/07/stop-trying-to-delight-your-customers) — the origin of CES, and the argument that reducing effort beats exceeding expectations.
- [American Customer Satisfaction Index](https://theacsi.org/) — the long-running academically grounded index, and the one genuinely independent benchmark here.

**At small scale, none of these beat reading every support ticket yourself.**

---

## 23.5 Support as a marketing channel

For a technical product, support quality *is* your reputation, because your users talk to each
other in public and screenshot everything.

- **Answer publicly where you can.** A well-answered GitHub issue is documentation, SEO, and proof of responsiveness in one artefact.
- **Fast beats perfect.** An acknowledgement in an hour outperforms a complete answer in two days.
- **Every repeated question is a documentation bug.** Track the repeats; fix the docs; measure the deflection.
- **Let engineers do support.** The classic 37signals argument, and it holds: it produces better answers and a much shorter feedback loop to the people who can fix the cause.

- [Help Scout blog](https://www.helpscout.com/blog/) — the most substantial free body of writing on support-as-growth. (Vendor, but genuinely good.)
- [37signals](https://37signals.com/) — publishes its support philosophy openly; a useful counterweight to enterprise support orthodoxy.

---

## 23.6 Community as support, and how it fails

Community support scales your team and is not free. The failure mode is predictable: questions get
answered in a walled garden, the same answers are regenerated forever, and nothing compounds. See
the platform decision in [chapter 8](08-communities-and-social.md#83-choosing-a-community-platform).

- [Discourse](https://www.discourse.org/) — the default open-source forum for technical communities. Self-hostable and indexed by default, which is the whole point.
- [CHAOSS](https://github.com/chaoss/community) — Linux Foundation project defining open, peer-reviewed community health metrics. The credible alternative to vanity member counts.
- [Open Source Guides](https://github.com/github/opensource.guide) — the "Building Welcoming Communities" and "Best Practices for Maintainers" chapters are directly applicable.
- [crowd.dev](https://github.com/CrowdDotDev/crowd.dev) — open-source community data platform, and a live successor now that most commercial community CRMs have been acquired upmarket.

---

## 23.7 Changelogs as retention

The most underrated retention artefact. A good changelog reminds people you're alive, gives
lapsed users a reason to return, and is one of the few marketing emails people genuinely want.

- [Keep a Changelog](https://github.com/olivierlacan/keep-a-changelog) — the convention: human-first, grouped by Added/Changed/Deprecated/Removed/Fixed. Written for people, not from `git log`.
- [Semantic Versioning](https://github.com/semver/semver) — relevant to marketing because your version numbers are a promise about breakage.
- [Stripe API changelog](https://docs.stripe.com/changelog) — the reference for doing this at scale with dated, versioned, migration-aware entries.
- [Linear changelog](https://linear.app/changelog) — the reference for a changelog treated as a marketing surface.

---

## 23.8 If you only do five things

1. Separate involuntary from voluntary churn before doing anything else. Fix the billing first.
2. Stop repeating the "5× cheaper to retain" statistic.
3. Instrument your activation event and fix the biggest drop-off before it.
4. Read the NPS free-text answers and ignore the score.
5. Write a human changelog and email it.

---

**Related:** [Open source and PLG](06-open-source-and-plg.md) · [Email and lifecycle](09-email-and-lifecycle.md) · [Pricing and business model](13-pricing-and-business-model.md)

*Last reviewed July 2026. Corrections welcome — see [CONTRIBUTING.md](../CONTRIBUTING.md).*
