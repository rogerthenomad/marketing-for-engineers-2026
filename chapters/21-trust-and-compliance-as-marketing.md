# 21. Trust, Security and Compliance as Marketing

> Every enterprise deal has a security review in it, and for a small vendor that review is
> usually the longest part of the sale. Treating it as paperwork loses deals. Treating it as a
> marketing surface wins them, because the companies that make it easy to say yes get bought.

---

## 21.1 The unblocker framing

SOC 2 and ISO 27001 don't win deals. They *stop losing* them. The distinction matters, because it
tells you when to spend the money: not to differentiate, but at the point where a real deal is
blocked and the buyer has said so.

Do not pursue certification speculatively because a blog told you enterprises need it. Do pursue
it the moment a deal you want is stuck behind it — and say so on the call, because "we're in the
audit window, here's our timeline" often unblocks a procurement conversation on its own.

**The practical distinction:**

- **SOC 2** — a US attestation report from an auditor about controls over a period. Type I is a point in time; Type II covers a window and is what buyers actually want.
- **ISO 27001** — an international certification of an information security management system. More common as a requirement outside the US.
- **NIST CSF** — a free framework, not a certification. The best no-cost way to structure your security programme before you're ready to pay anyone.

- [AICPA — SOC for Service Organizations](https://www.aicpa-cima.com/topic/audit-assurance/audit-and-assurance-greater-than-soc-2) — the authoritative description of what SOC 2 actually is, from the body that defines it.
- [ISO/IEC 27001](https://www.iso.org/standard/27001) — the standard's official page.
- [NIST Cybersecurity Framework](https://www.nist.gov/cyberframework) — free, credible, and enough structure to start.
- [CSA STAR Registry](https://cloudsecurityalliance.org/star/registry) — a free public registry where you can self-assess and publish. A genuinely cheap credibility signal that most small vendors overlook.

---

## 21.2 The trust page

Long before you have certifications, you can have a page that answers the questions a security
reviewer will ask. This is pure marketing work and it costs nothing.

**What belongs on it:**

- Where data is stored, and in which regions
- Encryption in transit and at rest, stated plainly
- Your **subprocessor list**, published and dated — required under GDPR Article 28 for processors, and a strong trust signal regardless
- Authentication options (SSO, MFA, SCIM if you have it)
- Data retention and deletion, with the actual mechanism
- Your security contact and disclosure policy
- Certifications, or an honest statement of where you are

- [GDPR Article 28](https://gdpr-info.eu/art-28-gdpr/) — why your subprocessor list is a legal artefact and not a nicety.
- [Vanta Trust Center](https://www.vanta.com/products/trust-center) and [SafeBase](https://safebase.io/) — hosted trust-centre products that gate documents behind NDA and automate the questionnaire dance. (Vendors.) Useful at scale; a plain HTML page is fine before then.

**The disproportionate win:** publishing this page means a reviewer can self-serve the first
eighty percent of their questionnaire. That can take a week out of your sales cycle.

---

## 21.3 Status pages and incident communication

How you behave during an outage is the most credible marketing you will ever do, and the only kind
your competitors cannot copy.

- **Have a status page on separate infrastructure.** A status page hosted on the thing that's down is a punchline.
- **Post before you have answers.** "We're aware and investigating" within minutes beats a polished update in an hour.
- **Publish real post-mortems.** Blameless, specific, with the actual timeline and what you changed. The engineering community rewards this enormously, and post-mortems are among the most-shared technical writing there is.
- **Never quietly delete an incident.**

- [Google SRE Books](https://sre.google/books/) — free full text; the postmortem culture chapter is the reference.
- [PagerDuty Incident Response documentation](https://response.pagerduty.com/) — PagerDuty's internal process, published openly. The best free operational template available.
- [Uptime Kuma](https://github.com/louislam/uptime-kuma) — self-hosted uptime monitoring with a status page. Popular, actively maintained.
- [Gatus](https://github.com/TwiN/gatus) — health dashboard and status page as configuration-as-code.
- [Cachet](https://github.com/cachethq/cachet) — long-running open-source status page system.

---

## 21.4 Vulnerability disclosure

Having a documented way for someone to report a vulnerability is a trust signal, a security
control and a way to avoid a researcher going public because they couldn't find your email.

- [RFC 9116](https://www.rfc-editor.org/rfc/rfc9116.html) — the `security.txt` standard. A single file at `/.well-known/security.txt`. Fifteen minutes of work.
- [securitytxt.org](https://securitytxt.org/) — generator and explainer.
- [disclose.io](https://disclose.io/) — open-source policy templates and safe-harbour language, so researchers know they won't be sued for helping you.
- [Adding a security policy to your repository](https://docs.github.com/en/code-security/getting-started/adding-a-security-policy-to-your-repository) — the `SECURITY.md` convention; GitHub surfaces it prominently.

---

## 21.5 How procurement actually evaluates a small vendor

Worth understanding because it explains behaviour that otherwise looks irrational.

The reviewer's job is not to assess your security. It is to **not be the person who approved the
vendor that caused the breach.** Everything follows from that: they want documentation they can
file, answers that match the questionnaire's categories, and evidence that someone else has
already checked you.

What this means practically:

- **Being small is the risk, not your architecture.** Bus factor, financial stability and support continuity come up more than cryptography.
- **A completed questionnaire you can send instantly is worth more than a better answer sent in two weeks.** Keep a maintained master document.
- **Cyber insurance** is frequently asked for and rarely mentioned in marketing advice.
- **Name a security contact who is a human.** Not `security@` with no owner.

---

## 21.6 Tooling, with honest notes

Compliance automation genuinely reduces the work, and it is genuinely expensive relative to a
small company's budget. Get quotes before you assume.

- [Vanta](https://www.vanta.com/) — the market leader in compliance automation, broad framework coverage. (Vendor.)
- [Drata](https://drata.com/) — the closest direct competitor, comparable scope. (Vendor.)
- [Oneleet](https://www.oneleet.com/) — differentiates by bundling penetration testing with the audit. (Vendor.)
- [Comp AI](https://github.com/trycompai/comp) — the credible open-source alternative in this category.
- [Prowler](https://github.com/prowler-cloud/prowler) — open-source cloud security assessment across AWS, Azure, GCP and Kubernetes. Free, and it will find things.
- [ScoutSuite](https://github.com/nccgroup/ScoutSuite) — multi-cloud security auditing from NCC Group.
- [OpenSCAP](https://github.com/OpenSCAP/openscap) — the mature open-source SCAP implementation.

**One licence warning**, because this tool is widely miscategorised: **Gapps** is AGPLv3 *plus
Commons Clause*, which makes it source-available rather than OSI open source. It is frequently
listed as "the open-source Vanta alternative." Read the licence before you build on it.

---

## 21.7 If you only do five things

1. Publish a trust page this week, even without certifications.
2. Add `security.txt` and `SECURITY.md`. Fifteen minutes.
3. Put your status page on infrastructure that isn't yours.
4. Keep a maintained master security questionnaire so you can answer instantly.
5. Don't buy certification until a real deal is blocked on it — then move fast and say so.

---

**Related:** [Privacy and compliance](15-privacy-and-compliance.md) · [Founder-led sales](20-founder-led-sales.md) · [Case studies and social proof](24-case-studies-and-social-proof.md)

*Last reviewed July 2026. Not legal or security advice. Corrections welcome — see
[CONTRIBUTING.md](../CONTRIBUTING.md).*
