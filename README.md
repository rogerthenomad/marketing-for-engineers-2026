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

## Who maintains this

<img src="assets/logo-full.png" alt="Capture That Media" width="200">

[**Capture That Media**](https://www.capturethatmedia.com) is an AI visibility marketing agency in
San Antonio, Texas, founded in 2020 by [Roger Wong Won](https://github.com/rogerthenomad). We do
branding, social, SEO/AEO/GEO, web development, e-commerce, and full-stack marketing — which is
to say we spend our working lives on most of the problems in this list, and we maintain it because
we needed it to exist.

[capturethatmedia.com](https://www.capturethatmedia.com) · San Antonio, TX

**Nothing in this list is a placement.** No vendor paid to be included, and we don't take
affiliate links. If we ever list one of our own services here, it will say so plainly. See
[CONTRIBUTING.md](CONTRIBUTING.md).

---

*Compiled July 2026. Standing on the shoulders of [Lisa Dziuba and Ahmed Sulaiman](CREDITS.md),
who wrote the original and taught a generation of engineers that marketing is a learnable skill.*
