# 14. Psychology and Ethics

> The original list had a psychology chapter full of genuinely good material on persuasion.
> It had no ethics chapter. In 2018 you could treat that as a matter of taste. In 2026 the
> gap between "persuasion" and "manipulation" is the subject of active enforcement in
> multiple jurisdictions, and the techniques that cross it are trivially easy to implement
> by accident.
>
> This chapter merges the two on purpose. They're the same subject.

---

## 14.1 The principles, and the one rule that governs them

Cialdini's seven principles of influence — reciprocity, commitment and consistency, social proof,
authority, liking, scarcity, and unity — remain the best-validated framework in marketing, and
the original list was right to include them.

The rule that makes them safe to use is simple: **the principle has to be genuinely present.**

Your job is to be a detective who *finds* the real principle and reveals it clearly — not a
smuggler who invents one. This isn't only ethics; it's strategy. Manufactured persuasion buys a
short-term lift and a long-term trust collapse, and in engineering markets, where people talk to
each other constantly and screenshot everything, the collapse arrives faster than in any other
industry.

| Principle | The honest version | The version that gets you in trouble |
|---|---|---|
| **Social proof** | Real users, real numbers, real logos you have permission to use | Fake reviews, invented testimonials, borrowed logos, purchased stars |
| **Scarcity** | A cohort that genuinely has limited places; a price that genuinely rises | Countdown timers that reset on reload; "3 spots left" forever |
| **Authority** | Credentials you hold, work you did, data you gathered | Implied endorsements, misrepresented press mentions, "as seen in" for a directory listing |
| **Reciprocity** | Genuinely useful free tools and content, given without strings | Value-gated behind a form you'll immediately sell to a data broker |
| **Commitment** | A small real first step that leads somewhere | Dark-pattern onboarding you can't exit |
| **Unity** | A community you actually built and participate in | Astroturfed "community" of employees posing as users |

---

## 14.2 What's now actually illegal

The right column above is no longer just distasteful. See
[chapter 15](15-privacy-and-compliance.md) for detail; the summary:

- **Fake reviews and testimonials** — including AI-generated ones and reviews from people who don't exist — are prohibited under the FTC's consumer reviews rule, effective October 2024, with civil penalties. This explicitly covers insider reviews from employees or founders without clear disclosure.
- **Undisclosed material connections** with anyone endorsing you breach the FTC Endorsement Guides.
- **Unlabelled synthetic media depicting people** falls under EU AI Act Article 50 transparency obligations from August 2026 — and the deepfake labelling duty applies *even with no intent to deceive*.
- **Vote manipulation and astroturfing** breach every relevant platform's terms, and where a product endorsement is involved may fall within the FTC rule's scope. See [chapter 7](07-launching.md#76-astroturfing-is-now-a-legal-exposure-not-a-growth-tactic).

**The practical test:** if the tactic only works because the audience doesn't know you're doing
it, it's manipulation. That test predates all the regulation and still catches more cases than
the regulation does.

---

## 14.3 Dark patterns, and why engineers ship them by accident

Almost nobody sets out to build a dark pattern. They arrive through a series of individually
defensible optimisations: the cancel flow gets one more "are you sure," the decline button gets
a little quieter, the pre-checked box saves a click, the trial-end email gets sent a bit later.

Each step tests well. The aggregate is a product people feel tricked by.

**The ones that show up most often in technical products:**

- **Roach motel** — signup is one click, cancellation is an email to support. Increasingly regulated, and always resented.
- **Confirmshaming** — "No thanks, I don't care about performance."
- **Hidden costs** — per-seat minimums, overage rates, or annual-only pricing revealed at checkout.
- **Forced continuity** — a trial that converts to paid without a clear reminder.
- **Obscured comparison** — a pricing page engineered so you can't tell what tier you need.

**The counter-practice** is straightforward and cheap: make cancellation as easy as signup, put
the real price on the pricing page, send the trial-ending email early enough to act on, and
default every checkbox to off. These cost you a measurable amount of short-term revenue and buy
you the thing that actually compounds, which is people recommending you without reservation.

---

## 14.4 Persuasion that's worth studying

The genuinely useful reading, most of which is unchanged since 2018 because good psychology
research ages well:

- **Cialdini, *Influence*** and **Cialdini, *Pre-Suasion*** — the second is the more underrated: the frame you establish *before* a message determines how it lands. What you show first changes how everything after it is experienced.
- **Kahneman, *Thinking, Fast and Slow*** — for understanding why your users' decisions don't match their stated preferences. Note that some of the priming research it cites has replicated poorly; the core two-system framing has held up better than some of its examples.
- [Cognitive bias cheat sheet](https://betterhumans.pub/cognitive-bias-cheat-sheet-55a472476b18) — Buster Benson's organisation of the full bias list into four underlying problems. Still the most useful single reference on the topic.
- **Nick Kolenda's** work on pricing and copywriting psychology — tactical, specific, and directly applicable to a pricing page. His site is now at [kolenda.io](https://www.kolenda.io/).

**A note on the replication crisis.** A meaningful share of the popular psychology cited in
marketing content — ego depletion, many priming effects, some social-proof studies — has failed
to replicate. Be sceptical of any tactic justified by a single striking study, especially one
from before 2015. The principles in 14.1 are among the better-supported, and even they are
context-dependent.

---

## 14.5 An ethical floor you can actually hold to

Not aspirational. These are cheap, and each one prevents a specific, common failure:

1. **Never fabricate a person, a review, a customer, a result, or a logo.** The bright line. Everything else is judgment; this isn't.
2. **Make cancellation as easy as signup.**
3. **Put the real price on the pricing page.**
4. **Disclose material connections** — paid, gifted, or employed.
5. **Don't use scarcity or urgency you can't substantiate.**
6. **Don't pretend to be a user** in a community. Not on Reddit, not on Hacker News, not in a competitor's Discord.
7. **Let people leave with their data.**
8. **Say what your product doesn't do.** This is the single most underrated trust-building move available, it costs nothing, and engineers respond to it more strongly than to any feature claim.

The commercial argument for all of this, if you need one: technical audiences are unusually good
at detecting manipulation, unusually well-connected, and unusually willing to say so publicly and
permanently. In a market where a single Hacker News comment can define your reputation for years,
honesty is the cheapest growth strategy available.

---

## 14.6 If you only do five things

1. Audit your own funnel for the five dark patterns in 14.3. You will find at least one.
2. Make cancellation self-serve this week.
3. Delete any urgency claim you can't substantiate.
4. Add a "what this isn't for" section to your homepage or README.
5. Check that every testimonial on your site came from a real person who agreed to it.

---

**Related:** [Privacy and compliance](15-privacy-and-compliance.md) · [Launching](07-launching.md) · [Pricing and business model](13-pricing-and-business-model.md)

*Last reviewed July 2026. Corrections welcome — see [CONTRIBUTING.md](../CONTRIBUTING.md).*
