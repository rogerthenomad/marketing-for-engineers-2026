# 24. Case Studies and Social Proof

> Technical buyers discount your claims about yourself to approximately zero and weight other
> engineers' experience heavily. That's the whole chapter. Everything else is mechanics — and
> the mechanics now include real legal exposure.

---

## 24.1 What technical buyers accept as proof

In descending order of weight:

1. **A colleague's direct recommendation.** Unbeatable, and mostly outside your control — except that everything in [chapter 23](23-retention-and-support.md) produces it.
2. **Public usage you can verify.** A named project depending on you, download counts, real deployments.
3. **A named engineer at a named company saying something specific.** "Cut our p99 from 340ms to 205ms" beats "great product, great team" by an enormous margin.
4. **A detailed case study with numbers and architecture.**
5. **Logos.** Weakest, and they still matter for procurement — a buyer needs to justify the choice internally.

**What carries no weight:** unattributed testimonials, five-star ratings with no substance,
"trusted by thousands," and anything a competitor could paste onto their own site unchanged.

- [Nielsen Norman Group](https://www.nngroup.com/articles/) — independent research on how users actually evaluate credibility signals.

---

## 24.2 Getting a customer to say yes

The ask fails when it sounds like work. Make it small and reciprocal:

- **Ask right after a win.** They shipped, the migration worked, you fixed something fast. Not at renewal.
- **Ask for 30 minutes of conversation, not a written case study.** You write it; they approve it. This changes the answer more than anything else you can do.
- **Offer them the spotlight.** Their engineer gets a byline, their company gets exposure to your audience, their team gets a public artefact about work they're proud of.
- **Have the approval path ready.** Legal and comms will need to see it. Ask who that is at the start, not after you've written it.
- **Accept anonymity.** "A Fortune 500 financial services company" with real numbers beats no case study at all.

**When they say no**, the usual reason is that their security or legal team prohibits naming
vendors. That's a policy, not a judgement on you. Ask if you can use the numbers without the name.

---

## 24.3 The structure that converts

Technical buyers read case studies to answer one question: *is this like us, and did it work?*

1. **The situation** — company, scale, stack, and the constraint they were under. Enough that a reader can pattern-match to themselves.
2. **What they tried first.** This is the most-skipped and most-valuable section, because it's where the reader recognises their own current approach.
3. **What they implemented**, with enough architectural detail to be credible. Diagrams help.
4. **What changed, with numbers and a method.** "40% faster" is marketing. "p99 from 340ms to 205ms, measured over two weeks in March" is evidence.
5. **What was hard.** Include the friction. A case study with no difficulty in it reads as fiction and gets discounted entirely.
6. **A quote from the engineer**, not the CMO.

Date every case study and state the version compared. See
[chapter 4](04-seo-and-ai-search.md#comparison-and-alternatives-to-x-pages) — a stale claim gets
quoted back at you by an AI answer engine long after you've corrected the page.

---

## 24.4 The rules you are actually subject to

Not legal advice, but this is now enforcement territory rather than etiquette. Covered in
[chapter 15](15-privacy-and-compliance.md); the specifics for this chapter:

- [FTC Endorsement Guides — what people are asking](https://www.ftc.gov/business-guidance/resources/ftcs-endorsement-guides-what-people-are-asking) — the plain-language version, and the one to actually read.
- [16 CFR Part 255](https://www.ecfr.gov/current/title-16/chapter-I/subchapter-B/part-255) — the Guides themselves.
- [Rule on the Use of Consumer Reviews and Testimonials](https://www.ftc.gov/legal-library/browse/rules/rule-consumer-reviews-testimonials) — the 2024 rule, with civil penalties, covering fake and AI-generated reviews and undisclosed insider reviews.
- [Soliciting and Paying for Online Reviews: A Guide for Marketers](https://www.ftc.gov/business-guidance/resources/soliciting-paying-online-reviews-guide-marketers) — what you may and may not offer in exchange for a review.
- [Directive (EU) 2019/2161 (Omnibus Directive)](https://eur-lex.europa.eu/eli/dir/2019/2161/oj) — the EU equivalent, requiring you to say how you verify reviews.
- [Digital Markets, Competition and Consumers Act 2024](https://www.legislation.gov.uk/ukpga/2024/13) — the UK regime for fake and concealed incentivised reviews.

**The short version:** if you gave someone anything of value for their endorsement — money, free
service, a discount, swag — disclose it clearly. If they work for you or you're an investor,
disclose it. Never publish a testimonial from someone who didn't say it, and never generate one.

---

## 24.5 Logos and permission

Using a customer's logo generally requires permission, and "they're a customer" is not permission.
Get it in writing, and check whether your contract already grants it — many enterprise agreements
explicitly *forbid* it, which is a common and avoidable embarrassment.

Keep a record of who approved what and when. Companies get acquired, contacts leave, and policies
change; a logo you were cleared to use in 2024 may need re-clearing.

- [International Trademark Association](https://www.inta.org/) — free plain-language explainers on trademark use and nominative fair use.

---

## 24.6 Review sites, and how they really work

Be clear-eyed: most of these are advertising businesses with a review layer, not neutral arbiters.

- [G2](https://www.g2.com/) — the largest B2B software review platform and the one with real weight in evaluations. Reviews are moderated and verified; **grid placement is influenced by review volume and recency**, which is why vendors run review drives. Paid profiles buy presentation and lead access, not review outcomes.
- [Gartner Peer Insights](https://www.gartner.com/reviews/) — heavily moderated, slower, and the most credible of the large platforms. Feeds Gartner's Voice of the Customer reports.
- [Capterra](https://www.capterra.com/), [GetApp](https://www.getapp.com/) and [Software Advice](https://www.softwareadvice.com/) — all three are Gartner-owned properties. **Placement in their listings is substantially pay-per-click**, which is not obvious from the interface. Treat rankings there as ad inventory.
- [TrustRadius](https://www.trustradius.com/) — historically the most methodologically strict of the mid-size platforms, with long-form reviews and heavy verification.

**Honest recommendation for a small technical vendor:** G2 is usually the only one worth deliberate
effort, and only if your buyers actually consult it — which for pure developer tools they often
don't. Ask five customers where they looked before buying. If nobody says G2, don't spend the
quarter on it.

**Running a review drive is legitimate.** Asking customers to leave an honest review, with no
condition on sentiment, is fine everywhere. Offering an incentive contingent on a *positive*
review is illegal in the US, EU and UK.

- [Testimonial.to](https://testimonial.to/) and [Senja](https://senja.io/) — tooling for collecting and embedding written and video testimonials. (Vendors.)
- [UserEvidence](https://www.userevidence.com/) — generates verifiable, attributable proof points from customer surveys, which sidesteps much of the case-study approval problem. (Vendor.)

---

## 24.7 If you only do five things

1. Ask for 30 minutes of conversation, not a written case study. Write it yourself.
2. Put a real number with a measurement method in every case study.
3. Include what was hard.
4. Disclose every material connection, every time.
5. Ask five customers where they looked before buying, and only then decide whether review sites deserve your quarter.

---

**Related:** [Retention and support](23-retention-and-support.md) · [Psychology and ethics](14-psychology-and-ethics.md) · [Privacy and compliance](15-privacy-and-compliance.md)

*Last reviewed July 2026. Not legal advice. Corrections welcome — see [CONTRIBUTING.md](../CONTRIBUTING.md).*
