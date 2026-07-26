# 25. Events, Conferences and Developer Education

> Events are the highest-conversion and lowest-efficiency channel available to you. Both facts
> are true simultaneously, which is why the decision is about which *mode* you pick, not
> whether to do events at all.

---

## 25.1 The three modes, honestly compared

**Speaking** is the best value by a distance. It costs you a CFP submission and a few days of
preparation, it borrows the conference's credibility, and the recording becomes an evergreen
asset (see [chapter 19](19-video-and-podcasting.md)). The constraint is that you have to have
something genuinely worth saying — which is a feature, not a bug.

**Sponsoring** buys logo placement and a list. For most small technical vendors it is the worst
value of the three, because attendees have learned to ignore sponsor branding and the list is
usually badge-scan noise. It becomes worth it when you need a specific room — a niche conference
where your entire buyer population is in one place.

**A booth** is expensive, exhausting, and occasionally the single best-converting thing you do
all year. It works when the product demos in under two minutes and your buyers attend that
event. It fails badly for anything requiring a long explanation.

**A fourth mode, usually better than all three when you're small: just attend.** Buy a ticket, go
to the hallway track, meet fifteen people properly. No booth, no sponsorship, no talk. This is
consistently underrated and costs a fraction of the alternatives.

- [CNCF sponsorship](https://www.cncf.io/sponsorship/) — a public, well-documented example of how large-scale technical conference sponsorship is actually structured and priced.
- [devopsdays organiser resources](https://devopsdays.org/organizing) — the sponsorship and organising model of a large distributed community-run conference. Useful for understanding what your money buys.

---

## 25.2 Getting a CFP accepted

Programme committees reject most submissions for predictable reasons, almost all of which you
control.

**What gets accepted:**

- **A specific story with a number in the title.** "How we cut our build from 40 to 4 minutes" beats "Modern CI best practices" every time.
- **Something that went wrong.** Failure talks are chronically under-submitted and enthusiastically accepted.
- **A talk only you can give**, because it's about your data, your incident, your migration.
- **A clear takeaway.** The reviewer needs to know what the audience leaves with.

**What gets rejected:** anything that reads as a product pitch, anything generic enough that ten
other people submitted it, and abstracts that don't say what actually happens in the talk.

**Submit widely and early.** Acceptance rates at good conferences are low enough that this is a
volume game with a quality floor. Reuse a talk across several events — the audiences don't overlap
as much as you fear, and the talk gets better each time.

- [Sessionize](https://sessionize.com/) — the most widely used CFP platform; maintains a public list of open calls. The single best place to find things to submit to.
- [confs.tech](https://github.com/tech-conferences/confs.tech) — open-source, community-curated conference listing, filterable by topic and location. Backed by an [open dataset](https://github.com/tech-conferences/conference-data) if you want to build alerts.
- [developers-conferences-agenda](https://github.com/scraly/developers-conferences-agenda) — community-maintained global listing including CFP deadlines.
- [speaking.io](https://speaking.io/) — free, short, opinionated guide covering proposals, slides, delivery and nerves.
- [Global Diversity CFP Day](https://www.globaldiversitycfpday.com/) — distributed workshop programme helping first-time and under-represented speakers write and submit.
- [Write the Docs](https://github.com/writethedocs/www) — a community whose conferences actively mentor first-time speakers. An unusually friendly place to start.

**One graveyard note:** several once-popular CFP aggregator lists are now archived with entries
years stale. Check the last-commit date before trusting any list you find, including ones linked
from older guides.

---

## 25.3 Running your own

A small recurring meetup or virtual event is cheap, compounding, and builds the kind of
relationships no ad buys. It is also a real ongoing commitment — a meetup that happens twice and
stops is worse than one that never happened.

**Non-negotiables:**

- **A code of conduct with a named contact and an actual enforcement process.** [Contributor Covenant](https://github.com/EthicalSource/contributor_covenant) is the most widely adopted and is translated into many languages; [Conference Code of Conduct](https://github.com/confcodeofconduct/confcodeofconduct.com) is the event-specific equivalent.
- **Consistency of schedule.** Same day each month beats sporadic and better.
- **Content that isn't your product.** One vendor talk in four, maximum. Break this and attendance dies quietly.

**Tooling:**

- [Meetup](https://www.meetup.com/) — still the largest discovery surface for local technical groups; the discovery is what you're paying for.
- [Luma](https://lu.ma/) — lightweight event pages and RSVPs; the current default for small technical events that don't need Meetup's discovery.
- [Google Developer Groups](https://developers.google.com/community/gdg) — an existing global chapter structure you can plug into rather than starting from nothing.
- [pretalx](https://github.com/pretalx/pretalx) — open-source, self-hostable CFP, review and scheduling, used by large community conferences.
- [pretix](https://github.com/pretix/pretix) — open-source ticketing with strong EU privacy and VAT handling. The companion to pretalx.
- [Claper](https://github.com/ClaperCo/Claper) — open-source live polls and Q&A over your slides.
- [StreamYard](https://streamyard.com/) — browser-based multi-guest streaming and simulcast, for the virtual version. (Vendor.)

---

## 25.4 Education as a channel

Teaching is the most durable form of developer marketing, because the person who learned the
concept from you reaches for your tool by default.

- **Free workshops and courses** work when they teach the *problem domain*, not your product. A course on distributed tracing that happens to use your tool beats a course on your tool.
- **Certification** is a serious commitment and a serious moat once established. Only viable when your product is complex enough that expertise is a hiring signal — but at that point it creates a labour market that pulls demand toward you.

- [Linux Foundation Training & Certification](https://training.linuxfoundation.org/) — the reference model for open, vendor-neutral technical certification.
- [CNCF certifications](https://www.cncf.io/training/certification/) — a good illustration of performance-based (rather than multiple-choice) certification, which is what technical audiences respect.
- [Open Badges (1EdTech)](https://www.1edtech.org/standards/open-badges) — the open standard for verifiable credentials. Use it if you issue anything, so the badge is portable rather than trapped in your system.
- [Maven](https://maven.com/) — cohort-based course platform; useful as a reference for how live technical courses get priced and structured. (Vendor.)

---

## 25.5 Swag that isn't landfill

Two rules: **make fewer, better things**, and make things people would buy. Good socks, a genuinely
good hoodie, high-quality stickers. Nobody wants a branded stress ball, and giving them one costs
you goodwill with an audience that increasingly notices waste.

If you make claims about ethics or sustainability, they need to be substantiated — the same
disclosure logic as [chapter 24](24-case-studies-and-social-proof.md) applies to environmental
claims, and regulators in the EU and UK have been actively pursuing greenwashing.

- [Global Organic Textile Standard](https://global-standard.org/) — the main independent certification for organic textiles, covering the supply chain rather than just the fibre.
- [bluesign](https://www.bluesign.com/) — chemical and environmental input standard for textile manufacturing; stricter on process.
- [Fairtrade International](https://www.fairtrade.net/) — for labour-standards claims specifically.

---

## 25.6 Measuring event ROI without lying to yourself

Badge scans are not leads. Booth conversations are not pipeline. The honest measurement is
uncomfortable and worth doing:

- **Track named conversations**, not scan counts.
- **Use self-reported attribution** ([chapter 12](12-analytics-and-attribution.md)) — events show up there when they show up nowhere else.
- **Measure at 90 days**, not at the event. Event-sourced deals are slow.
- **Count the full cost**: sponsorship, travel, booth build, swag, and the fully-loaded time of everyone who went. This number is usually two to three times what people budget, and it changes the decision.

- [DevRel Collective](https://devrelcollective.fun/) — practitioner community, useful for benchmarking what other teams actually see from events rather than what vendors claim.

---

## 25.7 If you only do five things

1. Submit three CFPs this month. Specific title, real number, something that went wrong.
2. Before sponsoring anything, just attend one and work the hallway track.
3. Record every talk you give and publish it yourself.
4. If you run a meetup, publish a code of conduct with a named contact before the first event.
5. Cost your last event fully, including people's time, then decide whether to repeat it.

---

**Related:** [Video and podcasting](19-video-and-podcasting.md) · [Communities and social](08-communities-and-social.md) · [Developer marketing and DevRel](05-developer-marketing-and-devrel.md)

*Last reviewed July 2026. Corrections welcome — see [CONTRIBUTING.md](../CONTRIBUTING.md).*
