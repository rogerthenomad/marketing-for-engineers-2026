# 15. Privacy and Compliance

> The 2018 list mentioned GDPR once, in a note advising against cold email. Since then the
> ground under digital marketing has moved more than in any other area covered here. This
> chapter is the minimum an engineer running their own marketing needs to know.
>
> **This is not legal advice.** It's a map of what exists so you know when to get some.

---

## 15.1 A timeline of what changed

| When | What | Why it matters |
|---|---|---|
| May 2018 | **GDPR** applies | Consent, lawful basis, and the first real penalties |
| Apr 2021 | **Apple App Tracking Transparency** (iOS 14.5) | Opt-in rates settled far below what advertisers assumed; mobile attribution broke |
| Jul 2023 | **Universal Analytics stops processing data** | GA4 or nothing |
| Feb 2024 | **Google + Yahoo bulk sender requirements** | Authentication became mandatory, not best practice |
| Mar 2024 | **Google Consent Mode v2** required for EEA traffic | No consent signal, no ad personalisation or remarketing in Google products |
| Mar 2024 | **Scaled content abuse** named in Google's spam policies | Programmatic content risk became explicit policy |
| Jul 2024 | **UA interface and API removed; data deleted** | No migration path; historical data gone if you didn't export |
| Aug/Oct 2024 | **FTC rule on consumer reviews and testimonials** | Fake and AI-generated reviews became a federal enforcement matter |
| Jul 2024 → Apr 2025 | **Google reverses third-party cookie deprecation** | The thing everyone spent five years preparing for did not happen |
| May 2025 | **Microsoft matches bulk sender rules** for Outlook consumer domains | Non-compliant mail rejected outright |
| Nov 2025 | **Google/Yahoo enforcement tightened** | Rejections rather than junk-foldering |
| Aug 2026 | **EU AI Act Article 50 transparency obligations apply** | Deepfake labelling and chatbot disclosure become law |

---

## 15.2 The third-party cookie story, told correctly

This is the single most misreported item in marketing, and a lot of 2026 content still describes
a world that never arrived.

**What actually happened:** Google announced the deprecation of third-party cookies in Chrome in
2020 and repeatedly delayed it. In **July 2024** it announced it would not deprecate them at all,
proposing instead a user-choice experience in Chrome. In **April 2025** it confirmed it would not
ship even that standalone prompt. Third-party cookies remain enabled by default in Chrome, with
no removal timeline. Google then formally ended the Privacy Sandbox in October 2025, retiring most
of its APIs; only a few survive, including CHIPS, FedCM and Private State Tokens.

**What this means practically:**

- **Don't panic-migrate.** A large consulting industry sold cookie-apocalypse readiness for five years. The apocalypse was cancelled.
- **But don't rebuild dependence on them either.** Safari's Intelligent Tracking Prevention and Firefox's protections have blocked third-party cookies for years regardless of Chrome, so a meaningful share of your traffic was never trackable that way.
- **First-party data and server-side measurement remain the right architecture** — not because Chrome forced it, but because they're more reliable, more durable, and less dependent on any one vendor's roadmap.

---

## 15.3 Consent, and the US state patchwork

**EU/EEA.** Google **Consent Mode v2** has been required since March 2024 for EEA traffic if you
want ad personalisation, remarketing and full measurement in Google products. Basic mode fires no
tags without consent; advanced mode loads tags before the banner and sends cookieless pings on
denial, which is what enables Google's conversion modelling. Which you choose is a genuine
legal-versus-measurement trade-off — get advice rather than picking the one with better numbers.

**United States.** There is no federal privacy law. Instead there are around **twenty states with
comprehensive privacy laws in effect during 2026**, with more enacted and pending. Counts differ
between trackers because "enacted" and "in effect" are different things — the
[IAPP US State Privacy Legislation Tracker](https://iapp.org/resources/article/us-state-privacy-legislation-tracker/)
is the reference to check rather than any blog post.

The practical consequence for a small team: **build for the strictest regime you serve.**
Maintaining twenty state-specific flows is not viable for a company your size, and the strictest
requirements are broadly a superset.

**Universal minimums worth implementing regardless of jurisdiction:**

- A real privacy policy that describes what you actually collect
- A working data-deletion path that a human can trigger without emailing you
- Honest cookie consent, where "reject" genuinely rejects
- Do not collect what you don't use — the cheapest compliance strategy is a smaller data footprint

---

## 15.4 Email law

Covered operationally in [chapter 9](09-email-and-lifecycle.md); the legal layer:

- **CAN-SPAM (US)** — permits cold B2B email. Requires accurate headers and sender identity, a physical postal address, clear opt-out, and honouring opt-outs within 10 business days.
- **CASL (Canada)** — considerably stricter, generally requiring express or implied consent, with meaningful penalties.
- **GDPR (EU)** — the lawful basis for most B2B prospecting is **Article 6(1)(f) legitimate interest**, not consent. But it requires a documented **Legitimate Interest Assessment**, and **Article 14 requires you to tell people where you obtained their data on first contact** when you didn't collect it from them directly. Almost nobody using enrichment tooling does this. It is the cheapest compliance win available, and it improves reply rates because it reads as honest.
- **"B2B is exempt" is false.** Several member states, notably Germany and Italy, apply consent-grade rules to B2B email under national ePrivacy implementations.

**On enrichment vendors:** they sell you data whose lawful basis is *your* problem to defend. The
indemnity in their contract is rarely what you assume.

---

## 15.5 The FTC: no AI exemption

Two instruments matter, and the difference between them is the most commonly botched point in
marketing-compliance writing.

- [FTC Rule on the Use of Consumer Reviews and Testimonials](https://www.ftc.gov/business-guidance/resources/consumer-reviews-testimonials-rule-questions-answers) — final rule effective October 2024, and **no longer theoretical**: the FTC sent warning letters to companies under it in late 2025 and brought its first actions in 2026. Bans creating, buying or disseminating fake reviews and testimonials **whether generated by humans or artificial intelligence**, including reviews from people who don't exist; bans incentives conditioned on expressing a particular sentiment; bans company-controlled "independent" review sites; and requires clear disclosure of insider reviews from employees, founders or their relatives. Carries civil penalties.
- **Endorsement Guides (16 CFR Part 255)**, substantially revised in 2023 — the rules on disclosing material connections with anyone endorsing you.

**What the FTC actually requires — and does not:**

It does **not** require you to label AI-written blog posts or ad copy. It requires:

1. **Substantiation** for any "AI-powered" claim about your product. If the AI is a regex, don't call it AI.
2. **Disclosure of material connections** with endorsers.
3. **No fake or synthetic endorsers, reviews or testimonials.** An AI-generated "customer" is a fabricated endorsement, full stop.

Confusing "the FTC requires AI disclosure" with "the FTC prohibits deceptive AI claims and fake
endorsements" is the single most common error in this space.

---

## 15.6 The EU AI Act, for marketers

**Article 50 transparency obligations apply from 2 August 2026**, with a transitional period into
December 2026 for generative systems already on the market before that date.

The EU's "Digital Omnibus" package was adopted in June 2026 and, importantly for marketers,
**left Article 50 untouched** — the 2 August 2026 date stands. What it did defer was the
high-risk-system regime, which moved out to late 2027 and 2028. So if you read that the AI Act
"was delayed," check which part: the transparency duties that apply to marketing were not.
Penalties for Article 50 breaches run to the order of millions of euros or a percentage of global
turnover, and are live from the same date.

- [Article 50 — transparency obligations](https://artificialintelligenceact.eu/article/50/) — the text.
- [European Commission: guidelines on transparency of AI-generated content](https://digital-strategy.ec.europa.eu/en/policies/guidelines-transparency-ai-generated-content) — the official guidance.

**If you're only *using* generative tools rather than providing them**, you are a *deployer*, and
you owe three things:

1. **Label deepfakes.** This applies **even with no intent to deceive**, and even where no real person is depicted. If your ad features an AI-generated spokesperson, label it.
2. **Disclose AI-generated or AI-manipulated text published to inform the public on matters of public interest** — *unless* the text underwent **genuine human review and a natural or legal person assumes editorial responsibility for it.**
3. **Disclose that a chatbot is a bot** where it isn't obvious.

**That carve-out in (2) is the most important sentence in this chapter for a marketing team.**
Human-reviewed, editorially-owned, AI-assisted copy is not unlabelled synthetic text. The Act
targets unattributed synthetic material passed off as reportage — not your AI-drafted,
human-edited product page. Most "you must now label all AI content" posts get this wrong.

---

## 15.7 A disclosure policy you can actually adopt

1. **Always disclose** where a human is depicted or voiced synthetically — AI spokesperson, cloned voice, generated testimonial. Required in the EU, ethically required everywhere, and reputationally catastrophic when discovered rather than declared.
2. **Always disclose** that a chatbot is a bot.
3. **Never fabricate** a person, review, case study, result or customer logo. This is the bright line; everything else is judgment.
4. **Take editorial responsibility** — a named human who reviewed it and stands behind it. This satisfies the AI Act's text carve-out and is simply what publishing means.
5. **Don't label routine AI assistance.** A badge on every post is noise that trains readers to ignore it on the one page where it matters. Disclosure is a scarce signal — spend it where deception is actually possible.
6. **Substantiate every "AI-powered" claim** about your own product.

---

## 15.8 If you only do five things

1. Publish a privacy policy that matches what you actually collect, and build a working deletion path.
2. Get SPF, DKIM and DMARC right — it's compliance and deliverability in one job.
3. Add the Article 14 sentence to cold outreach: say where you got their details.
4. Never fabricate a review, testimonial, customer or result. Not once, not for a launch.
5. Bookmark the IAPP tracker instead of trusting any blog's count of state laws.

---

**Related:** [Email and lifecycle](09-email-and-lifecycle.md) · [Analytics and attribution](12-analytics-and-attribution.md) · [Psychology and ethics](14-psychology-and-ethics.md)

*Last reviewed July 2026. Regulatory dates and implementation detail move — verify against the
primary source before making a decision. This is a map, not legal advice. Corrections are
especially welcome here; see [CONTRIBUTING.md](../CONTRIBUTING.md).*
