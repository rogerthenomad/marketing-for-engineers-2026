# 12. Analytics and Attribution

> Marketing guides used to be able to skip this, because attribution mostly worked: cookies
> tracked people across sites, last-click was good enough, and the dashboard roughly matched
> reality. None of those three things is true now, and the honest response is not a better
> tool — it's a different relationship with certainty.

---

## 12.1 Why attribution broke

Four independent forces, none of which is reversing:

1. **Platform privacy changes.** Apple's App Tracking Transparency (2021) collapsed mobile attribution. Safari and Firefox have blocked third-party cookies for years. Even though [Chrome ultimately did not deprecate them](15-privacy-and-compliance.md#152-the-third-party-cookie-story-told-correctly), a large share of your traffic was never cookie-trackable.
2. **Zero-click search.** Roughly two-thirds of searches now end without a click to the open web. The influence happened; the visit didn't.
3. **AI assistants as an intermediary.** Someone asks a model, gets a recommendation, and types your name into the address bar. Your analytics records "direct."
4. **Dark social.** The Slack DM, the private Discord, the group chat, the conference conversation. Always invisible; now a larger share of a smaller measurable whole.

The net effect: **your dashboard systematically under-credits the channels that actually create
demand and over-credits the ones that capture it.** Branded search and direct traffic look like
heroes. Whatever caused someone to know your name looks like nothing.

---

## 12.2 The tooling

**Web analytics**

- [Google Analytics 4](https://analytics.google.com/) — free, ubiquitous, and the one most people end up on. Universal Analytics stopped processing data in July 2023 and its interface and data were removed in July 2024, with no migration path — so if you're reading an older guide, everything it says about UA is dead.
- [Plausible](https://plausible.io/) — open source, self-hostable, cookieless, and genuinely simple. Often removes the need for a consent banner at all, which is a real advantage.
- [Umami](https://umami.is/) — open source and self-hostable, similar niche, MIT-licensed.
- [Fathom](https://usefathom.com/) and [Matomo](https://matomo.org/) — the other credible privacy-first options; Matomo is the most full-featured and the heaviest.

**Product analytics**

- [PostHog](https://posthog.com/) — product analytics, session replay, feature flags and experiments in one, with a generous free tier and a self-hostable option. For most engineering-led teams this is the single highest-value tool in this chapter.
- [Mixpanel](https://mixpanel.com/) and [Amplitude](https://amplitude.com/) — the incumbents. Both have free tiers; both are more product-manager-shaped than PostHog.

**The recommendation for a small technical team:** a privacy-friendly web analytics tool for
traffic, PostHog for product behaviour, and your database for revenue. You do not need a customer
data platform — see [chapter 16](16-ai-marketing-stack.md#163-automation-and-reading-the-licence).

---

## 12.3 Triangulation instead of attribution

The 2026 practice is to stop looking for one true number and instead take three independent
readings that fail in different ways.

**1. Self-reported attribution — do this first, it's nearly free.**

Ask every new signup, in an **optional free-text field**, how they heard about you. Not a
dropdown: dropdowns only confirm what you already guessed. Read the answers monthly.

This has gone from a soft supplement to one of the most reliable signals available, precisely
because it captures the things no tracking can see — the podcast, the colleague, the model that
recommended you. It is the highest-value-per-hour item in this entire chapter.

**2. Incrementality testing — the only causal evidence you'll get.**

Turn a channel off in some geographies and not others. Hold back a randomised segment. Measure
the difference. This is the only method that answers "would this revenue have happened anyway,"
which is the actual question and the one no attribution model can answer.

Geo-based holdout tests are within reach of a small team and worth far more than a better
dashboard.

**3. Marketing mix modelling — the strategic view.**

MMM had a genuine renaissance because it needs no cookies or device IDs — it regresses aggregate
outcomes against aggregate spend and external factors. It used to require a consultancy; open
tooling collapsed the cost:

- [Meridian](https://developers.google.com/meridian) — Google's Bayesian MMM, open source, Python.
- [Robyn](https://github.com/facebookexperimental/Robyn) — Meta's MMM, open source, R.
- [PyMC-Marketing](https://www.pymc-marketing.io/) — Bayesian MMM and CLV built on PyMC.

**Honest caveat:** MMM wants a lot of data across a lot of time periods. Below a few million in
revenue, or with under two years of history, it will produce confident nonsense. Most readers of
this list should do (1) and (2) and read about (3).

Much of the practitioner writing recommending MMM comes from vendors selling MMM services.
The technique is sound; the urgency is marketed.

---

## 12.4 Measuring the AI channel

New in this edition, and cheap to implement.

**Build a referrer report** segmenting on `chatgpt.com`, `perplexity.ai`, `gemini.google.com`,
`claude.ai` and `copilot.microsoft.com`. This costs nothing and ends most internal arguments
about whether AI traffic matters.

What you'll typically find: **small volume, better conversion.** Visitors arrive after a
recommendation rather than a search, which means they're pre-qualified. Treat it as a quality
channel, not a volume replacement.

**On the impressions side**, Google Search Console added generative-AI performance reporting in
2026 that separates AI Overviews and AI Mode impressions from ordinary search. The catch is that
it reports **impressions only** — no clicks, no CTR, no query data. You can now see AI-surface
visibility; you still can't price it.

Also track **branded search volume** over time. When demand creation is working and attribution
can't see it, branded search is usually where it shows up first.

---

## 12.5 Metrics discipline

- **If a metric can't change a decision, it doesn't belong on the dashboard.** Most dashboards are decorative.
- **Pick one number per funnel stage** and let the rest be diagnostic.
- **Track cohorts, not totals.** Totals hide churn behind growth.
- **Instrument activation, not signup.** See [chapter 6](06-open-source-and-plg.md#activation-and-pqls).
- **Beware the attribution mirage.** The channel that looks most efficient is usually the one closest to the purchase, which is not the same as the one that caused it. Retargeting always looks brilliant; it is frequently taking credit for demand something else created.
- **Accept a confidence interval.** The correct 2026 posture is "we believe this channel is working, here's our evidence from three independent methods" — not a number with two decimal places that nobody can reproduce.

---

## 12.6 If you only do five things

1. Add the "how did you hear about us?" free-text field today. Read it monthly.
2. Build the AI-referrer segment in your analytics.
3. Instrument your activation event properly, and stop optimising signups.
4. Run one geo holdout on your largest paid channel. You will probably be unpleasantly surprised.
5. Delete half your dashboard. Keep only what changes a decision.

---

**Related:** [SEO and AI search](04-seo-and-ai-search.md) · [Paid acquisition](11-paid-acquisition.md) · [Privacy and compliance](15-privacy-and-compliance.md)

*Last reviewed July 2026. Corrections welcome — see [CONTRIBUTING.md](../CONTRIBUTING.md).*
