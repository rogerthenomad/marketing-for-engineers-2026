# 18. Landing Pages and Conversion

> You do not have a traffic problem. You have a page that does not explain what the thing is.
> This chapter is about the highest-leverage surface you control completely — and about why
> most of the A/B testing advice you will read does not apply to you yet.

---

## 18.1 The job of the page

A landing page has exactly one job: let a stranger decide, quickly, whether this is for them.
Not persuade. **Decide.** A fast "no" is a good outcome; it costs you nothing and saves them time.

The failure mode in technical products is almost never insufficient enthusiasm. It's that the page
never says plainly what the thing *is*. Ask five people who don't work with you to read your hero
section and tell you what you sell. If they can't, no amount of testing will save the page.

**What has to be visible without scrolling:**

1. **What it is**, in a sentence a stranger can repeat accurately.
2. **Who it's for** — specific enough that the wrong people leave.
3. **Proof it's real** — a terminal cast, a screenshot, a code sample. For technical products this outperforms any headline.
4. **One primary action.** Not five.

Everything below the fold is for people who have already decided they're interested. That's what
it's for, and it's fine that most people never reach it.

- [Nielsen Norman Group article library](https://www.nngroup.com/articles/) — the most reliable free usability research anywhere, and refreshingly resistant to fashion. Their work on how people actually read on the web is the antidote to writing pages for people who read every word.
- [Marketing Examples](https://marketingexamples.com/) — Harry Dry's library of annotated real pages. The fastest way to develop taste, because it shows the before and after rather than the theory.
- [Julian Shapiro's Growth Handbook](https://www.julian.com/guide/growth/landing-pages) — the clearest free writing on landing page structure specifically.

---

## 18.2 Forms are where conversion goes to die

Every field you add costs you signups. This is one of the most consistently replicated findings in
the field, and one of the most consistently ignored.

- **Ask for the minimum that lets you deliver value.** For most developer tools that is an email, or nothing at all.
- **Do not ask for a phone number** unless a human genuinely calls. Technical buyers read it as a threat.
- **Do not ask for company size** on the first form. Enrich it later; see [chapter 16](16-ai-marketing-stack.md#164-crm-and-gtm-data).
- **Kill the "confirm password" field.** Show the password instead.
- **Offer SSO and GitHub OAuth.** For a developer product, "sign in with GitHub" is often the single highest-impact conversion change available.

- [Baymard Institute research](https://baymard.com/research) — large-scale usability research on forms and checkout. E-commerce-focused, but the form findings transfer directly.

---

## 18.3 Pricing pages

Your pricing page is a landing page and usually gets more qualified traffic than your homepage.
Treat it accordingly. The details are in [chapter 13](13-pricing-and-business-model.md); the page
mechanics:

- **Publish a price.** "Contact us" for a self-serve product means "we will waste your time." A meaningful share of technical buyers will leave rather than fill in a form to learn a number.
- **Three tiers, one recommended.** More than four is a decision problem you have offloaded onto the customer.
- **Name tiers by who they're for**, not by metal.
- **Put the annual/monthly toggle where it's visible**, and show the actual saving.
- **Answer the objections on the page.** What happens when I exceed the limit? Can I cancel? Do you delete my data? An FAQ under the tiers converts better than a support ticket.

---

## 18.4 Social proof, placed where the doubt is

Social proof works when it appears at the moment of hesitation, not in a logo carousel nobody
looks at. Put the testimonial about migration difficulty next to the migration CTA. Put the
security quote next to the enterprise tier.

Two rules from [chapter 14](14-psychology-and-ethics.md): the proof must be **real**, and if you
have a material connection to the person providing it you must disclose it. Fabricated
testimonials are a federal enforcement matter in the US, not a grey area.

For technical audiences, the strongest proof in rough order: **public usage you can point at**
(download counts, a well-known project depending on you), **a named engineer at a named company
saying something specific**, **a detailed case study**, and only then logos.

---

## 18.5 A/B testing, and why you probably can't

This is the section most CRO content omits, because it undercuts the product being sold.

To detect a relative lift of about 10% on a baseline conversion rate of about 5%, at conventional
significance and power, you need roughly **20,000 visitors per variant**. The rough sizing is
`n ≈ 16p(1−p)/δ²`, and you can run the arithmetic for your own numbers in a minute.

If you get 2,000 visitors a month, a single conclusive test takes you about **twenty months**. In
that time the product, the market and the page will all have changed. **You cannot A/B test your
way to a good page at low traffic.** Anyone selling you testing tooling at that volume is selling
you a random number generator with a dashboard.

**What to do instead, at low traffic:**

- **Talk to five users** while they use the page. Recorded, silent, no prompting. You will learn more in an hour than a year of underpowered tests.
- **Make big changes, not small ones.** A rewritten page can produce an effect large enough to see without statistics. Button colours cannot.
- **Watch session replays** for rage clicks and dead ends.
- **Read your own support inbox.** Every repeated question is a page that failed.

When you do have the traffic:

- [How Not To Run An A/B Test](https://www.evanmiller.org/how-not-to-run-an-ab-test.html) — Evan Miller on why checking results early and stopping when you like them invalidates the whole exercise. This one essay prevents the single most common testing error.
- [Evan Miller's sample size calculator](https://www.evanmiller.org/ab-testing/sample-size.html) — run this *before* the test, not after.
- [ExP Platform](https://exp-platform.com/) — Kohavi's archive of the underlying research on controlled experiments at scale. The real literature, free.
- [GoodUI](https://goodui.org/) — UI patterns with associated test evidence attached.

---

## 18.6 Tooling

Free tiers and self-hostable options, with licences checked:

- [PostHog](https://github.com/PostHog/posthog) — product analytics, session replay, feature flags and experiments in one. MIT-licensed apart from named enterprise directories. For most engineering-led teams this is the whole stack.
- [GrowthBook](https://github.com/growthbook/growthbook) — the strongest choice if you want experimentation that runs off your warehouse rather than a vendor's pipeline. MIT with enterprise carve-outs.
- [Unleash](https://github.com/Unleash/unleash) — mature open-source feature flagging with good SDK coverage.
- [Flagsmith](https://github.com/Flagsmith/flagsmith) — open-source flags and remote config, BSD-3-Clause.
- [OpenFeature](https://github.com/open-feature/spec) — a CNCF vendor-neutral specification for feature flagging. Worth adopting early so you can change vendors later without rewriting.

Note that "open source" in this category frequently means "open core with the interesting parts
licensed separately." Read the licence before you build on it — see
[chapter 16](16-ai-marketing-stack.md#163-automation-and-reading-the-licence).

---

## 18.7 If you only do five things

1. Show your hero section to five strangers and ask what you sell. Fix it until they get it right.
2. Put a real price on the pricing page.
3. Delete every form field that isn't required to deliver value.
4. Add "sign in with GitHub" if your users have GitHub accounts.
5. Compute your required sample size before you plan a single test. Then, most likely, go talk to users instead.

---

**Related:** [Positioning and audience](01-positioning-and-audience.md) · [Pricing and business model](13-pricing-and-business-model.md) · [Psychology and ethics](14-psychology-and-ethics.md)

*Last reviewed July 2026. Corrections welcome — see [CONTRIBUTING.md](../CONTRIBUTING.md).*
