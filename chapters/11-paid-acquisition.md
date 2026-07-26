# 11. Paid Acquisition

> The original list had extensive chapters on Facebook and Twitter ads. Both platforms
> changed beyond recognition, the targeting they described no longer exists, and the
> measurement they assumed broke. This is a shorter chapter than that one, deliberately:
> for most readers of this list, paid acquisition is the wrong tool, and the honest advice
> is to say so before listing the tools.

---

## 11.1 Should you be doing this at all?

**Probably not yet.** Three conditions should be true before you spend money on ads:

1. **You know what converts organically.** Paid amplifies an existing motion; it doesn't discover one. If you don't know which message lands, you're buying expensive A/B tests with a stranger's attention.
2. **You can measure incrementality**, at least roughly. See [chapter 12](12-analytics-and-attribution.md). Without it you cannot distinguish "ads work" from "ads take credit for demand something else created" — and retargeting in particular always looks brilliant for exactly this reason.
3. **Your unit economics survive it.** With AI COGS compressing gross margins ([chapter 13](13-pricing-and-business-model.md#133-ai-changed-the-margin-structure-and-that-changes-everything-downstream)), CAC payback computed on revenue rather than gross profit will flatter you badly.

For a bootstrapped developer tool, the honest ranking of where a marginal dollar goes furthest is
usually: documentation, then original-data content, then sponsorships of things your audience
already reads, and only then performance ads.

---

## 11.2 What actually works for technical products

**Sponsoring what your audience already reads.** Consistently the best-performing paid channel
for developer tools, and the one most likely to be ignored because it doesn't have a dashboard.
A newsletter your buyers actually open, a podcast they actually finish, an open-source project
they actually depend on. You're buying trust by association rather than an impression.

- Developer-focused, privacy-respecting ad networks like [EthicalAds](https://www.ethicalads.io/) and Carbon Ads place contextual ads on documentation and developer sites without tracking. Modest volume, well-targeted, and they don't make your brand look like the reason people install ad blockers.
- **GitHub Sponsors and open-source sponsorship** — see [chapter 6](06-open-source-and-plg.md). Buys goodwill in a community that notices, and is frequently cheaper than the equivalent ad spend.

**Search ads on high-intent terms.** Google Ads on "your competitor alternative," "how to do
[the specific job]" and category terms is one of the few paid motions with genuinely
buyer-intent-shaped demand behind it. Small budgets, tight keyword lists, and check the search
terms report weekly — broad match will spend your budget on nonsense faster than you'd believe.

**LinkedIn for the economic buyer.** Expensive per click and worth it in narrow cases: developer
tools bought by engineering managers and platform leads, where the audience is precisely
targetable by role and company and the deal size justifies the CPC. Not for reaching individual
developers, who aren't there.

**Reddit Ads.** Genuinely differentiated by subreddit and conversation targeting — the closest
thing to intent targeting outside search. See [chapter 8](08-communities-and-social.md#reddit-ads).

**What generally doesn't work for dev tools:** broad Meta campaigns (wrong audience, wrong
intent), display retargeting at small scale (you're paying to reach people who were going to come
back anyway), and X ads (declining reach, historically poor advertiser tooling).

---

## 11.3 Measurement, in a world where it doesn't quite work

Everything in [chapter 12](12-analytics-and-attribution.md) applies, but the paid-specific points:

- **Consent Mode v2 has been required since March 2024** for EEA traffic if you want ad personalisation and remarketing in Google products. Implement it deliberately, understanding the legal-versus-measurement trade-off between basic and advanced modes.
- **Server-side tagging and conversion APIs** are the current standard for reliable conversion signal. More work, better data, and less dependent on the browser.
- **Apple's App Tracking Transparency** ended reliable cross-app mobile attribution in 2021. If your plan assumes mobile attribution works like it did, it doesn't.
- **The third-party cookie deprecation did not happen** — Google reversed course in 2024 and again in 2025. Don't panic-migrate, but don't rebuild dependence either. See [chapter 15](15-privacy-and-compliance.md#152-the-third-party-cookie-story-told-correctly).
- **Run a geo holdout before you scale anything.** Turn the channel off in some regions and compare. It is the only way to know whether you're buying incremental revenue, and the result is frequently sobering.

---

## 11.4 A sane way to start

1. **Set a budget you can afford to lose entirely**, and treat it as tuition.
2. **One channel, one audience, one message.** Multi-channel launches teach you nothing because you can't attribute the result.
3. **Send traffic to a page built for that traffic**, not your homepage.
4. **Run it long enough to reach significance**, which is longer than you think and usually longer than the budget allows — which is itself useful information about whether you should be doing this.
5. **Compute payback on gross profit.**
6. **Kill it quickly if it doesn't work.** The sunk-cost trap in paid acquisition is well documented and you are not immune to it.

---

## 11.5 If you only do five things

1. Delay paid until you know what converts organically.
2. Sponsor one newsletter your buyers actually read before you touch an ad platform.
3. If you run search ads, check the search terms report weekly and add negatives ruthlessly.
4. Implement Consent Mode properly if you serve EEA traffic.
5. Run one geo holdout before scaling spend.

---

**Related:** [Analytics and attribution](12-analytics-and-attribution.md) · [Pricing and business model](13-pricing-and-business-model.md) · [Privacy and compliance](15-privacy-and-compliance.md)

*Last reviewed July 2026. Ad platform features and pricing change constantly — verify at the
platform. Corrections welcome — see [CONTRIBUTING.md](../CONTRIBUTING.md).*
