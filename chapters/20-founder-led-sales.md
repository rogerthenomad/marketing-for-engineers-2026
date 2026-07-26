# 20. Founder-Led Sales

> Nobody can sell your product before you have. Not because you're better at selling — you
> almost certainly aren't — but because the first hundred sales conversations are product
> research wearing a sales costume, and you're the only one who can act on what they teach.

---

## 20.1 Why you have to do this yourself first

Hiring a salesperson to solve "we don't know how to sell this" fails reliably, and it fails
expensively. A salesperson can execute a known motion. They cannot discover one. Until you know
who buys, why, what they compare you to, what objection kills the deal and what price clears,
there is no motion to execute.

The signals that you're ready to hire are concrete: you can predict roughly how many conversations
produce a deal, you know the two or three objections that actually matter, and you've said the
same words and won more than once. Before that, a sales hire is an expensive way to keep not
knowing.

- [Y Combinator Library](https://www.ycombinator.com/library) — free archive of YC's startup advice, including a lot of the canonical founder-sales material.
- [First Round Review](https://review.firstround.com/) — long-form operator interviews with a deep archive on early sales.
- [Close resources](https://www.close.com/resources) — Steli Efti's material on founder-led sales is unusually direct and unusually free of theatre. (Vendor, but the content stands alone.)
- [SaaStr](https://www.saastr.com/) — the standard reference archive on SaaS go-to-market. Skew enterprise; adjust down.

---

## 20.2 Discovery: shut up and take notes

The single most common failure in a founder's first sales calls is talking. You built the thing,
you're excited, and you demo for forty minutes to someone who needed three of those minutes.

**The structure that works:**

1. **Ask what they're doing today.** Not what they want — what they currently do. In detail.
2. **Ask what it costs them.** Time, money, headcount, incidents, sleep.
3. **Ask what they've already tried.** This is your real competitive set, and it's usually a script and a cron job rather than a funded competitor.
4. **Ask what happens if they do nothing.** If the answer is "nothing much," you have no deal, and finding that out in ten minutes is a win.
5. **Only then, show the two things that address what they just said.**

Talk under 40% of the time. Write down their exact words — that phrasing is your homepage copy,
and it will be better than anything you'd write yourself.

**The Mom Test** by Rob Fitzpatrick is the standard short book on asking questions that produce
truth rather than politeness. It's the best few hours you can spend before your first calls.

---

## 20.3 Qualification, honestly

Frameworks like BANT and MEDDIC exist to help large sales teams forecast consistently. At your
stage they are mostly ritual, and applying them early makes you sound like a call centre.

What you actually need to know, in plain terms:

- **Is this a real problem they're already spending on?** (Budget exists somewhere, even if it's someone's time.)
- **Can this person get it bought, or do they need someone else?**
- **Is there a reason to do it now?** No trigger, no deal — just a pleasant conversation.

That's it. Learn the formal frameworks when you have a team who needs shared vocabulary.

- [MEDDIC Academy](https://meddic.academy/) — the framework from its commercial custodians, for when you get there. (Vendor.)

---

## 20.4 Demos for technical buyers

A technical buyer is evaluating whether *they* can succeed with your product, not whether it looks
impressive. So:

- **Let them drive if at all possible.** A trial account beats a guided tour.
- **Start from their use case**, not your feature tour. Ask before the call what they want to see.
- **Show the failure modes.** What happens when it breaks, how you debug it, what the error looks like. This builds more trust than any success path.
- **Never fake anything.** Not a mock, not a "this is coming next month" shown as though it exists. Technical buyers find out, and they tell people.
- **Answer "no" cleanly.** "We don't do that, and here's what people usually do instead" wins more deals than a hedge.

---

## 20.5 "We'll just build it ourselves"

The default objection for technical buyers, and the one most founders handle badly by arguing.

Don't argue. They probably *can* build it — that's why they're technical. The question is whether
they should, and that's a conversation about opportunity cost, not capability.

What works:

- **Concede the point immediately.** "You definitely could. Most of our customers could."
- **Move to maintenance, not construction.** Building version one is a weekend. The ongoing cost is edge cases, on-call, the migration when the upstream API changes, and the person who owns it leaving.
- **Ask what they'd stop doing to build it.** This is the real trade and they usually haven't priced it.
- **Sometimes agree that they should build it.** If it's genuinely core to their business, say so. You'll lose the deal and gain a reputation that closes three others.

---

## 20.6 Pricing conversations

Covered properly in [chapter 13](13-pricing-and-business-model.md). The conversational mechanics:

- **Say the number without flinching**, then stop talking. The silence is uncomfortable and it is not your job to fill it.
- **Never discount without getting something** — an annual commitment, a case study, a reference call. An unconditional discount teaches the buyer your price is fiction.
- **Discount the term, not the value.** Cutting scope to hit a price is better than cutting price for full scope.
- **If you keep winning instantly on price, you're too cheap.** A healthy price loses some deals.

---

## 20.7 Tooling for tiny teams

You need to know who you talked to and what they said. That's it. Do not buy a sales stack.

- [HubSpot CRM](https://www.hubspot.com/products/crm) — genuinely usable free tier with a contact cap; the most common starting point.
- [Attio](https://attio.com/) — flexible relational data model, popular with technical teams who'd otherwise build one in Postgres.
- [Close](https://www.close.com/) — built for small teams doing high-volume calling, with calling built in. (Vendor.)
- [Twenty](https://github.com/twentyhq/twenty) — the most actively developed modern open-source CRM. AGPLv3 with enterprise file carve-outs.
- [EspoCRM](https://github.com/espocrm/espocrm) — mature, stable, unfashionable, works.

A spreadsheet is a completely legitimate CRM for your first fifty conversations, and switching
later costs you an afternoon.

---

## 20.8 If you only do five things

1. Do fifty sales calls yourself before you consider hiring anyone.
2. Talk less than 40% of the time and write down their exact words.
3. Show the failure modes in every demo.
4. Concede "you could build this" instantly, then talk about maintenance.
5. Say your price, then stop talking.

---

**Related:** [Positioning and audience](01-positioning-and-audience.md) · [Pricing and business model](13-pricing-and-business-model.md) · [Outbound and partnerships](10-outbound-and-partnerships.md)

*Last reviewed July 2026. Corrections welcome — see [CONTRIBUTING.md](../CONTRIBUTING.md).*
