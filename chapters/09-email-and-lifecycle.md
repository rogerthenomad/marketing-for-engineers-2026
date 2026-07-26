# 9. Email and Lifecycle

> Email is the only channel you own. Every platform in [chapter 8](08-communities-and-social.md)
> has repriced, throttled or deprecated its API in the last three years. Your list is the one
> asset nobody can take away by changing a policy — which is exactly why the deliverability
> section below matters more than the vendor comparison.

---

## 9.1 Fix deliverability first

This is the highest-return item in this entire list for an engineer, because it is a DNS and
headers problem — fully within your control, roughly a day of work, and it gates everything
downstream. It is also the thing most teams discover only after a campaign lands in spam.

**The bulk-sender floor.** Google and Yahoo introduced requirements in February 2024 and
tightened enforcement from November 2025, moving from junk-foldering to outright rejections.
Microsoft matched them in May 2025 for Outlook.com, Hotmail.com and Live.com — non-compliant
mail gets rejected with `550 5.7.15 Access denied`, not delivered to spam.

At **5,000+ messages per day to personal accounts** you must have:

- **SPF and DKIM** both passing
- **DMARC** published, at minimum `p=none`
- **Alignment** — SPF or DKIM must align with the visible `From:` domain
- **RFC 8058 one-click unsubscribe** on marketing mail, honoured promptly
- **Spam complaint rate below 0.3%** — competent senders target below 0.1%

- [Outlook's requirements for high-volume senders](https://techcommunity.microsoft.com/blog/microsoftdefenderforoffice365blog/strengthening-email-ecosystem-outlook%E2%80%99s-new-requirements-for-high%E2%80%90volume-senders/4399730) — Microsoft's own announcement. (2025, Microsoft)

**The engineer's checklist, in order:**

1. **Dedicated sending subdomain.** Never your apex domain. A bad campaign should not be able to damage your primary domain's reputation.
2. **SPF + DKIM (2048-bit) + DMARC `p=none`** with an `rua` address you actually read.
3. **Move to `p=quarantine`, then `p=reject`** once the reports are clean.
4. **`List-Unsubscribe` and `List-Unsubscribe-Post` headers** on every marketing send.
5. **Bounce and complaint webhooks wired to automatic suppression.** Not a manual process.
6. **Separate transactional and marketing streams.** This is the mistake engineering teams make most often: a bad marketing campaign takes down your password reset delivery.

---

## 9.2 Choosing the stack

### Transactional sending

- [Resend](https://resend.com) — the developer-experience winner. Clean API, React Email templating, good docs, generous free tier. Worth knowing it's a well-designed layer over an underlying MTA rather than an MTA itself, which matters when you're reasoning about reputation isolation.
- [Postmark](https://postmarkapp.com) — the deliverability purist. Separate message streams for transactional and broadcast, aggressive reputation defence, and correspondingly opinionated about what you're allowed to send. **If password resets landing in spam would be an incident, use this.**
- [Amazon SES](https://aws.amazon.com/ses/) — cheapest raw sending by a wide margin and the most work. No templating, no analytics worth the name; you build suppression and reputation tooling yourself.
- [SendGrid](https://sendgrid.com) (Twilio) — enormous scale and a mature API, but the shared-IP reputation pool is a genuine liability on lower tiers. Fine at volume with dedicated IPs.

### Newsletters and creator lists

- [Kit](https://kit.com) — **formerly ConvertKit**; the rebrand completed in October 2024, so any list still saying "ConvertKit" is out of date. Tag-and-automation model that maps cleanly onto how developers think, decent API, free tier for early lists. The default if your list is your product.
- [beehiiv](https://beehiiv.com) — built around growth and monetisation (ad network, referrals, paid subscriptions). Better than Kit if the newsletter *is* the business; worse if email is one channel inside a product.
- [Substack](https://substack.com) — you are renting an audience on a social network that happens to send email. Best-in-class discovery, near-zero technical control, a cut of paid revenue, and periodic moderation controversies that become your problem. Good for reach, bad as infrastructure. **Export your list regularly.**
- [Listmonk](https://github.com/knadh/listmonk) — self-hosted, single Go binary plus Postgres, **AGPL-3.0 and genuinely open source**. You bring your own SMTP or SES and own the deliverability problem entirely — which for a technical team with a large list is often an order of magnitude cheaper and strictly more controllable.

### Product and lifecycle messaging

- [Customer.io](https://customer.io) — the serious choice for behavioural, event-driven messaging across email, push and in-app. Assumes a clean event stream and punishes you if you don't have one. Pick it when journey logic is genuinely complex, not because you might need it later.
- [Loops](https://loops.so) — modern, deliberately simple lifecycle email for SaaS, priced per contact rather than per send. **Resend for transactional plus Loops for lifecycle** is a reasonable default for a small product team.
- [Userlist](https://userlist.com) — B2B-specific, and genuinely differentiated: it models the **company** as the lifecycle entity with users nested inside, which is how multi-seat B2B actually works.

---

## 9.3 The sequences that matter

**Onboarding.** The rule that matters more than any template: **branch on activation events, not
elapsed days.** A drip still saying "here's how to get started" to someone who activated on day
one is a public admission you aren't reading your own telemetry. Tie this to your activation
metric from [chapter 6](06-open-source-and-plg.md#activation-and-pqls).

**Trial expiry.** Tell people what happens to their data. The most common trial-end email is a
discount; the most effective one is usually reassurance plus a single clear next step.

**Win-back.** The counterintuitive and well-supported point: **don't lead with a discount.**
Opening a win-back with an incentive teaches your list to churn deliberately and wait for the
offer. Reintroduce value first; escalate to incentives only after softer messages fail.

**Product updates and changelogs.** Chronically underused. A well-written changelog email is one
of the few marketing sends people genuinely want, and it doubles as a re-activation trigger.

- [Really Good Emails](https://reallygoodemails.com/) — still the best library of real examples, and still free.

---

## 9.4 Cold outreach — the legal reality

Covered fully in [chapter 10](10-outbound-and-partnerships.md), but the short version belongs
here because it's an email problem:

- **US:** CAN-SPAM permits cold B2B email, but requires accurate headers, a physical address, and honouring opt-outs within 10 business days.
- **EU:** the lawful basis for most B2B prospecting is GDPR Article 6(1)(f) legitimate interest — **not** consent — but it requires a documented Legitimate Interest Assessment. And **Article 14 requires you to tell people where you got their data on first contact** when you didn't collect it from them directly. Almost nobody using enrichment tooling does this; it's the cheapest compliance win available and it measurably improves reply rates because it reads as honest.
- **"B2B is exempt" is false.** Several member states, notably Germany and Italy, apply consent-grade rules to B2B email.

**The blunt version:** enrichment vendors sell you data whose lawful basis is your problem, not
theirs. The indemnity in their contract is not what you think it is.

---

## 9.5 If you only do five things

1. Set up SPF, DKIM and DMARC on a dedicated sending subdomain today.
2. Separate your transactional and marketing streams so one can't take down the other.
3. Wire complaint and bounce webhooks to automatic suppression.
4. Branch your onboarding sequence on activation events instead of days.
5. Export your list from whatever platform holds it, on a schedule, to somewhere you control.

---

**Related:** [Outbound and partnerships](10-outbound-and-partnerships.md) · [AI marketing stack](16-ai-marketing-stack.md) · [Privacy and compliance](15-privacy-and-compliance.md)

*Last reviewed July 2026. Sender requirements and pricing change — verify at the provider's own
documentation. Corrections welcome — see [CONTRIBUTING.md](../CONTRIBUTING.md).*
