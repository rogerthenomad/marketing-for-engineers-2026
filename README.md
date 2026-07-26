<p align="center">
  <a href="https://www.capturethatmedia.com">
    <img src="assets/logo-full.png" alt="Capture That Media" width="320">
  </a>
</p>

<p align="center">
  <em>Maintained by <a href="https://www.capturethatmedia.com">Capture That Media</a> — San Antonio's AI visibility agency.<br>
  Visibility, everywhere your customers actually search.</em>
</p>

---

# Marketing for Engineers — 2026 Edition

**A practical, opinionated marketing collection for engineers who have to market the thing they
built.** Organised by the problem you're actually trying to solve, honest about what no longer
works, and written so you can act on it today.

Inspired by [Marketing for Engineers](https://github.com/goabstract/Marketing-for-Engineers) by
Lisa Dziuba and Ahmed Sulaiman — one of the best resources of its era, last meaningfully updated
around 2018. This is a rewrite, not a fork: every chapter was written from scratch for 2026.
See [CREDITS.md](CREDITS.md).

> **New here?** Start with [What Changed for 2026](WHATS-NEW-2026.md), especially
> [the graveyard](WHATS-NEW-2026.md#the-graveyard) — the list of tools and tactics that are dead,
> and what replaced them. If you've been following 2018-era advice, that's the fastest way to
> stop wasting your time.

---

## Who this is for

**You, if you can build the thing but not sell it.**

- **The solo developer or indie hacker** who shipped something good six months ago and has eleven users, three of whom are your friends.
- **The technical founder** who can explain the architecture in ten minutes and the value proposition in never.
- **The open-source maintainer** with fifteen thousand stars, four thousand weekly downloads, and no idea how any of that becomes a living.
- **The first marketing hire at a dev-tools company**, trying to work out why the playbook that worked at your last B2C job is bouncing off engineers.
- **The DevRel person** who is being asked, for the first time, to prove the function pays for itself.
- **The agency or consultant** whose clients are technical and who is tired of decks that assume the buyer can be reached on Facebook.

**Who it is not for.** This assumes a technical or B2B buyer throughout. If you're marketing
consumer goods, local services, or e-commerce, most of the mechanics here will be wrong for you —
the chapters on developer marketing, open source and agent-readable documentation simply won't
apply. Go find a list built for your channel.

**What you don't need.** A budget, a marketing background, a team, or permission. Most of what
follows is either free or something you can do yourself in an afternoon. Where something costs
real money, the chapter says so, and usually says not to buy it yet.

## Why this matters now

Marketing used to be the thing you could postpone. Build something good, the reasoning went, and
distribution would sort itself out. That was never quite true, and in 2026 it is actively false —
for reasons that are specific, recent, and mostly invisible from inside an editor.

**Being good is no longer sufficient to be found.** Roughly two-thirds of searches now end without
a click to the open web. Answers are assembled from passages by systems that may never send you a
visitor. You can rank first and be quoted nowhere.

**Your first reader is increasingly not a person.** A coding agent reads your docs, resolves your
package name, and picks your library before a human sees your homepage. If your documentation is
gated, unrendered, or ambiguous about what your product is called, you lose that evaluation
without ever knowing it happened.

**The cost of being generic went to zero, and so did the value.** Anyone can now generate a
competent blog post, a plausible landing page, and forty variations of an email. Which means none
of those differentiate anything. The things that still work are the things a model can't produce:
your data, your incident, your benchmark, your opinion, your name on it. That is *good* news for
engineers — you have the raw material and most of your competitors don't.

**Several tactics from the last era are now enforcement matters.** Fake reviews, undisclosed
endorsements, bought upvotes and astroturfed threads moved from distasteful to regulated, with
civil penalties attached. The 2018 advice on some of this will get you in genuine trouble.

**And the old advice is still the top search result.** That's the real reason this exists. The
list this one rebuilds was excellent, is nearly a decade old, and is still being found and
followed by people who then waste months on channels that closed years ago. Half the value here is
the [graveyard](WHATS-NEW-2026.md#the-graveyard).

Marketing is a learnable skill with a literature, the same as distributed systems or type theory.
This is the reading list, minus the parts that stopped being true.

---

## Start with your actual problem

| If you're… | Read |
|---|---|
| Unable to explain what you built | [1. Positioning and audience](chapters/01-positioning-and-audience.md) |
| At zero users with no budget | [2. Zero-budget growth](chapters/02-zero-budget-growth.md) |
| Wondering what to write | [3. Content marketing](chapters/03-content-marketing.md) |
| Invisible in Google *and* in ChatGPT | [4. SEO and AI search](chapters/04-seo-and-ai-search.md) |
| Selling to developers | [5. Developer marketing and DevRel](chapters/05-developer-marketing-and-devrel.md) |
| Trying to monetise an open-source project | [6. Open source and PLG](chapters/06-open-source-and-plg.md) |
| About to launch | [7. Launching](chapters/07-launching.md) |
| Deciding where to build a community | [8. Communities and social](chapters/08-communities-and-social.md) |
| Setting up email that lands in inboxes | [9. Email and lifecycle](chapters/09-email-and-lifecycle.md) |
| Doing cold outreach or partnerships | [10. Outbound and partnerships](chapters/10-outbound-and-partnerships.md) |
| Considering spending money on ads | [11. Paid acquisition](chapters/11-paid-acquisition.md) |
| Unable to tell what's working | [12. Analytics and attribution](chapters/12-analytics-and-attribution.md) |
| Guessing at your price | [13. Pricing and business model](chapters/13-pricing-and-business-model.md) |
| Unsure where persuasion becomes manipulation | [14. Psychology and ethics](chapters/14-psychology-and-ethics.md) |
| Worried about GDPR, the FTC, or the EU AI Act | [15. Privacy and compliance](chapters/15-privacy-and-compliance.md) |
| Building an AI-assisted marketing workflow | [16. The AI marketing stack](chapters/16-ai-marketing-stack.md) |
| Looking for what to read next | [17. Reading list](chapters/17-reading-list.md) |

---

## The short version

If you read nothing else, this is most of the value:

1. **Positioning first.** Almost every marketing problem an engineer describes is a positioning problem wearing a costume. If you can't finish "we are the only ___ that ___, for ___," fix that before anything else.
2. **Your first hundred users come one at a time, by hand.** There is no version of this that scales, and the manual phase is where the product gets good.
3. **Publish what only you could publish.** Your data, your incident, your benchmark. Generic competent content is now free to produce and therefore worth nothing.
4. **Docs are the marketing** — and since about 2024, an AI agent is often the first thing to read them.
5. **Fix deliverability before anything else in email.** SPF, DKIM, DMARC on a dedicated subdomain. It's a day of work and it gates every downstream channel.
6. **Check your `robots.txt` and your CDN's bot rules.** The most common cause of "we don't appear in AI answers" isn't content — it's a blocked crawler.
7. **Pick your billing unit before you build.** With inference costing real money per request, gross margin is a pricing input, not an afterthought.
8. **Ask people how they found you**, in a free-text field. With two-thirds of searches ending click-free, this is now one of your most reliable signals.
9. **Never fabricate a person, review, customer or result.** It's the bright line, it's now federally enforceable in the US, and technical audiences catch it.
10. **Own your domain and your email list.** Every platform in this list has repriced, throttled or deprecated something in the last three years.

---

## How this list is built

**Curated, not comprehensive.** The value is in what's left out. Link rot taught the awesome-list
ecosystem that breadth is a liability, so this edition prefers canonical, stable URLs — official
docs, primary research, project repositories — over deep links that 404 in two years.

**Every number is attributed and dated.** Where a study comes from a vendor selling the thing it
measures, the chapter says so. Where no primary source could be traced, the number was cut rather
than repeated.

**It tells you when things don't work.** A chapter that quietly omits a dead tactic isn't helping —
someone will find the 2018 advice and follow it. So the dead things are named.

**Every chapter ends with "if you only do five things."** Curated lists are easy to admire and
hard to act on.

**Known limitations** are documented in [What Changed for 2026](WHATS-NEW-2026.md#known-gaps)
rather than hidden. The most significant one: link verification was partial, because the research
environment blocked direct HTTP fetches to most hosts.

---

## Contributing

**Removals and corrections are the most valuable contributions**, more than additions. If a link
is dead, a fact is wrong, or a tactic stopped working, please open an issue or PR — anything
about law, privacy rules, or deliverability requirements gets fixed at high priority, because
people make real decisions on it.

See [CONTRIBUTING.md](CONTRIBUTING.md) for the bar a link has to clear.

---

## Licence

The original text of this collection — chapter prose, annotations, structure and curation — is
licensed [CC BY 4.0](LICENSE). Every linked resource belongs to its own author and is governed by
their terms.

---

## About

<img src="assets/logo-full.png" alt="Capture That Media" width="220">

### 🌐 [www.capturethatmedia.com](https://www.capturethatmedia.com)

**Capture That Media** is an AI visibility marketing agency in San Antonio, Texas, founded in 2020
by [Roger Wong Won](https://github.com/rogerthenomad). Gold ADDY winner, and named Best of San
Antonio in 2023.

*Visibility, everywhere your customers actually search.*

We work on branding, social, SEO/AEO/GEO, web development, e-commerce and full-stack marketing —
which is to say we spend our working days on most of the problems in this list. That's the honest
reason it exists. We kept reaching for the 2018 original, kept finding its links dead, and
eventually concluded that rewriting it was less work than explaining it away.

The chapters on [AI search](chapters/04-seo-and-ai-search.md),
[analytics](chapters/12-analytics-and-attribution.md) and
[compliance](chapters/15-privacy-and-compliance.md) are the ones we get asked about most, and the
ones where the 2018 advice is most likely to actively hurt you.

**Where to find us**

- Website — [www.capturethatmedia.com](https://www.capturethatmedia.com)
- Location — San Antonio, Texas
- Maintainer — [@rogerthenomad](https://github.com/rogerthenomad)

**Disclosure.** Capture That Media sells marketing services that overlap the subject matter of
this list. **Nothing here is a paid placement.** No vendor was compensated for inclusion, there are
no affiliate links, and we don't recommend our own services in the chapters. Where our commercial
interest touches a recommendation, the text says so. See [CONTRIBUTING.md](CONTRIBUTING.md) for the
bar a link has to clear, and [CREDITS.md](CREDITS.md) for the full disclosure.

**Found something wrong?** [Open an issue](../../issues). Corrections — especially about law,
privacy rules and deliverability — get fixed fast, because people make real decisions on them.

---

*Compiled July 2026. Standing on the shoulders of [Lisa Dziuba and Ahmed Sulaiman](CREDITS.md),
who wrote the original and taught a generation of engineers that marketing is a learnable skill.*
