# Contributing

This is a curated list, not a directory. The value is in what gets left out.

## The bar

A link gets in if it clears all five:

1. **It solves a problem an engineer actually has.** Not "here is a thing that exists" —
   "here is the thing to read when you are stuck on X."
2. **It is current, or it is timeless.** Anything describing platform mechanics, ad
   products, pricing, or law must reflect 2025–2026 reality. Anything older has to be a
   genuine classic whose logic still holds (Paul Graham on doing things that don't scale
   is fine; a 2017 guide to Facebook Page organic reach is not).
3. **It is free to read, or the paywall is stated.** No surprise registration walls.
   Mark paid resources explicitly.
4. **It is not primarily an ad.** Vendor content is allowed when it contains real,
   reusable methodology or original data. It is not allowed when it is a product pitch
   with a blog-post costume on. When we link vendor research, we say who paid for it.
5. **The link resolves.** Check it before you submit.

## The annotation

Every entry needs a one-line annotation that answers *why would I click this*. Format:

```markdown
- [Title of the thing](https://example.com) — what it gives you, and when to reach for it. (2025, Author/Org)
```

Include the year and the author or organisation. If a number is cited, the annotation says
where the number came from and when it was measured.

## Things that will get a PR closed

- Affiliate links, referral codes, or UTM parameters pointing at your own tracking.
- Your own product, unless it is genuinely best-in-class for a gap the list has, and you
  disclose that it's yours in the PR description. Disclosed self-submissions are welcome
  and get judged on merit; undisclosed ones are not.
- AI-generated filler. Volume is not the goal. A PR that adds forty mediocre links is
  worse than one that adds two good ones or removes ten dead ones.
- Unverifiable statistics. If you cannot link the primary source, don't cite the number.
- Growth tactics that require deceiving people: fake reviews, undisclosed paid endorsement,
  astroturfed community posts, fabricated scarcity, scraped-contact cold outreach into
  jurisdictions where it is illegal. This list has a chapter on why those are also bad
  business; see [`chapters/14-psychology-and-ethics.md`](chapters/14-psychology-and-ethics.md).

## Especially welcome

**Removals.** Link rot is the enemy of a list like this. A PR that says "these nine links
are dead, here are the replacements" is the single most valuable contribution you can make.

**Corrections.** If a fact here is wrong — a date, a regulation, a pricing tier, a claim
about how a platform behaves — open an issue with the primary source. Anything about law,
privacy rules, or deliverability requirements gets fixed at high priority, because people
make real decisions on it.

**Non-US perspective.** The list currently leans US/EU. Guidance on marketing to and from
other regions is a real gap.

## How to submit

1. Fork, branch, edit the relevant file in `chapters/`.
2. Keep the existing section structure and annotation format.
3. In the PR description, say what you added or removed and why it clears the bar.
4. One theme per PR. Easier to review, faster to merge.

## A note on the tone of the list

The prose is meant to be blunt about what does not work. If a channel has decayed, the
chapter says so rather than burying a dead tactic in an otherwise cheerful paragraph.
Please write your additions the same way. Telling an engineer that a tactic used to work
and now doesn't is more useful than pretending it still does.
