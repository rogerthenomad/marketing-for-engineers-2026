# 10. Outbound and Partnerships

> Most writing on cold outreach is either a compliance panic that tells you never to do it, or
> a tooling list that pretends the law doesn't exist. Both are unhelpful. The truth is narrower:
> targeted outbound is legitimate and still works. Mass automated outbound is now both
> ineffective and, in several jurisdictions, unlawful.

---

## 10.1 The state of cold outreach

Two things happened simultaneously. Automation made sending 10,000 personalised-looking emails
trivial, and consequently made receiving them worthless. Everyone's inbox now filters on the
signals that mass tooling produces. The result is a genuine inversion:

**Twenty carefully researched messages now outperform two thousand automated ones** — not
marginally, but by enough that the automated approach is often net-negative once you account for
domain reputation damage.

The mechanism is simple. Deliverability is now reputation-gated
([chapter 9](09-email-and-lifecycle.md#91-fix-deliverability-first)), complaint rates above 0.3%
get you rejected outright, and mass outbound reliably generates complaints. You are trading your
ability to reach anyone for a low-probability shot at reaching everyone.

---

## 10.2 The legal floor

Know this before you send anything:

- **US — CAN-SPAM.** Cold B2B email is permitted. You need accurate headers and sender identity, a physical postal address, a clear opt-out, and you must honour opt-outs within 10 business days.
- **Canada — CASL.** Considerably stricter. Generally requires express or implied consent, with significant penalties.
- **EU — GDPR.** The lawful basis for most B2B prospecting is **Article 6(1)(f) legitimate interest**, not consent — but you need a documented Legitimate Interest Assessment. And **Article 14 requires you to tell people where you got their data, on first contact**, when you didn't collect it from them directly.
- **"B2B is exempt" is false.** Several member states — Germany and Italy notably — apply consent-grade rules to B2B email.

**The Article 14 disclosure is the most useful compliance obligation you'll ever meet**, because
it's also good outreach. A sentence saying "I found you through your talk at KubeCon / your
GitHub profile / your company's engineering blog" is simultaneously the legal requirement and the
single best thing you can put in a cold email. It proves you did research, which is the only
thing that makes cold outreach work.

If you can't write that sentence honestly, you don't know enough about the person to be emailing
them.

Full detail in [chapter 15](15-privacy-and-compliance.md).

---

## 10.3 Outreach that actually works

**The structure:**

1. **Why you specifically.** A concrete, verifiable detail. Their talk, their issue comment, their blog post, the job posting that reveals the problem. Not "I saw your company is in the fintech space."
2. **Where you got their details.** See above.
3. **The problem you think they have**, stated as a hypothesis you might be wrong about — not as a diagnosis.
4. **One specific, small ask.** A fifteen-minute call is a big ask from a stranger. "Does this match your experience?" is a small one, and it gets answered.
5. **An easy exit.** "If this isn't relevant, no reply needed."

**What kills it:** fake personalisation tokens, invented mutual connections, false urgency,
flattery, "quick question," multi-paragraph feature lists, and any of the seven-touch sequences
that treat a human being as a state machine.

**On AI-assisted outreach:** the failure mode is specific and serious. An agent that invents a
prospect's headcount, funding round or mutual connection has made a factual misrepresentation
with your name on it. The mitigation is architectural: **pull facts from a system of record,
template the factual slots, and let the model choose only phrasing.** See
[chapter 16](16-ai-marketing-stack.md#162-agentic-marketing).

---

## 10.4 Partnerships and integrations

For a developer tool, this is usually higher-yield than outbound, and consistently underrated.

**Integrations are distribution.** Building an integration with a product your users already use
puts you in their marketplace, their docs, their changelog, and their users' mental model of the
category. It is a durable placement rather than a one-day spike, and it compounds. See
[chapter 13](13-pricing-and-business-model.md#138-business-models-for-shipping-something-small)
on marketplace distribution.

**The 2026 version of this:** MCP servers, agent tool registries and coding-agent skill formats
are the newest marketplace, with the lowest competition and the highest intent. See
[chapter 5](05-developer-marketing-and-devrel.md#54-the-agent-is-your-first-reader).

**Co-marketing that isn't a waste of time:**

- **Joint technical content** — a genuinely useful "how to use X with Y" guide that both parties link. Works because it's useful independent of either party's marketing.
- **Being in each other's docs.** More valuable than a joint webinar and a fraction of the effort.
- **Community cross-pollination** — showing up genuinely in a partner's community, not pitching in it.

**What doesn't work:** logo-swap "partnership" pages nobody visits, joint webinars with twelve
attendees, and press releases about partnerships that involve no product work.

**How to approach a potential partner:** lead with the thing you already built. An integration
that exists is a conversation; an integration you'd like to discuss building is a meeting request.
Engineers respond to working code.

---

## 10.5 Talking to influential people

Deliberately not called "influencer marketing," because for technical products that term
describes something that mostly doesn't work. Paid technical influencer campaigns are transparent
to the audience and generally counterproductive.

What does work has not changed in twenty years: **be genuinely useful to people whose work you
respect, without an immediate ask.** Cite their work. Fix their
bug. Answer their question. Send the thing you built because of their post.

Two rules:

- **Disclose material connections.** If you paid, gifted, or otherwise compensated someone for coverage, that has to be disclosed — this is FTC Endorsement Guides territory, and it applies to free product too. See [chapter 15](15-privacy-and-compliance.md#155-the-ftc-no-ai-exemption).
- **Never fabricate the relationship.** An AI-generated "testimonial" from someone who never used your product is a fabricated endorsement, and it's the bright line.

---

## 10.6 If you only do five things

1. Cut your outbound list by 95% and spend the saved time on research.
2. Put the "here's where I found you" sentence in every cold email. It's the law and it's the hook.
3. Never let a model generate a fact about a prospect.
4. Build the integration before you pitch the partnership.
5. Be useful to three people whose work you admire, with no ask attached.

---

**Related:** [Email and lifecycle](09-email-and-lifecycle.md) · [Privacy and compliance](15-privacy-and-compliance.md) · [Psychology and ethics](14-psychology-and-ethics.md)

*Last reviewed July 2026. Not legal advice. Corrections welcome — see [CONTRIBUTING.md](../CONTRIBUTING.md).*
