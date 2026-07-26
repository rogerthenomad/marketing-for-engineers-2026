# 7. Launching

> **The headline change since 2018: launch day stopped being a growth event and became a
> credibility event.** Product Hunt, Hacker News and the rest still matter — but as proof,
> press and social capital, not as a customer-acquisition plan. The launches that produce
> durable revenue are the ones where the founder already had an audience before launch day.
> Which means the real launch work happens in the three months *before* it.

---

## 7.1 What a launch is actually for

Be honest with yourself about which of these you're buying, because they need different plans:

- **Credibility** — a badge, a rank, a link you can put in a fundraising deck or a cold email.
- **Press and investor visibility** — journalists and VCs genuinely still monitor these surfaces.
- **A feedback burst** — a few hundred technical people stress-testing your positioning in public, which is worth more than most user research.
- **Customers** — the least reliable outcome, and the one every guide promises.

A launch converts an existing audience into users. It does not create the audience. If you have
no audience, the highest-value thing you can do is not "launch better" — it's spend the next
quarter building one, and then launch. See [chapter 3](03-content-marketing.md) and
[chapter 8](08-communities-and-social.md).

---

## 7.2 Hacker News

Still the highest-quality-per-visitor free launch surface for developer tools, still un-gameable
in any way that survives, and still brutally low-yield: the median Show HN scores in the low
single digits. Front page is a small percentage of submissions.

**The canonical rules — read these, not a blog's summary:**

- [Show HN guidelines](https://news.ycombinator.com/showhn.html) — Show HN is for "something you've made that other people can play with." It must be your own work, you must be around to discuss it, and if it isn't ready, don't post.
- [Hacker News Guidelines](https://news.ycombinator.com/newsguidelines.html) — site-wide rules, including editorialised titles and the prohibition on vote manipulation.
- [Hacker News FAQ](https://news.ycombinator.com/newsfaq.html) — flags, penalties, and the second-chance pool.

**The five things that actually decide how it goes:**

1. **Never ask anyone to upvote.** This is the number one way founders self-destruct on HN. Vote rings are detected, and the punishment is silent — your post simply stops ranking, and your domain can be penalised for future submissions. There is no recovery process worth relying on.
2. **Don't editorialise the title.** Superlatives read as marketing and get flagged. Plain and descriptive beats clever every time.
3. **Make it trivially easy to try.** A signup wall in front of a Show HN converts curiosity into a closed tab. If people can't play with it, you get less feedback, which is the entire point of the exercise.
4. **Show up in the comments and stay there.** The thread *is* the product of a Show HN. Founders who answer critical comments substantively — including "you're right, that's a real limitation" — do dramatically better than founders who post and leave.
5. **Velocity matters more than volume**, because of the time-decay in HN's ranking. But you cannot manufacture velocity without breaking rule 1, so the only legitimate lever is posting when your genuine audience is awake.

Useful practitioner reading:

- [How to launch a dev tool on Hacker News](https://www.markepear.dev/blog/dev-tool-hacker-news-launch) — strongest on tone: talk to HN as fellow engineers, skip the superlatives, go deep on technical detail.

**A note on the statistics you'll see quoted.** Front-page rates, median scores and "best time to
post" figures circulate widely and almost all trace back to marketing blogs rather than published
datasets. HN's data is fully public through its Firebase and Algolia APIs. If the number matters
to your decision, compute it yourself — it's an afternoon of work and you'll be one of the few
people citing something real.

---

## 7.3 Product Hunt

**Verdict: launch, but budget it as PR and social proof.** The 2018 framing — get to #1 and
receive a traffic firehose — no longer holds. Retrospectives consistently find that final rank
correlates weakly or not at all with paid conversion, and that the launches producing real
revenue were backed by a pre-existing audience.

- [Product Hunt Launch Guide](https://www.producthunt.com/launch) — the official hub: timing, submission, the content checklist, the first comment. Start here rather than with a third-party guide.

**What's changed structurally:**

- **AI saturation.** AI is now the most contested category on the site by a wide margin, and the bar for a top placement there is far higher than in a normal category. If you're an AI product, you are launching into the hardest possible bracket.
- **Fast decay.** The overwhelming majority of launch traffic arrives in the first 24 hours and falls away sharply within the month. Plan for what you do with a one-day spike, not for a sustained lift.
- **A polluted advice ecosystem.** Search results for "Product Hunt launch strategy" are now dominated by AI-written content marketing from launch-services vendors. Treat any specific upvote threshold or traffic figure from those sources as fiction until proven otherwise.

**Do not buy upvotes.** See 7.6 — this is no longer just a ToS problem.

---

## 7.4 The surfaces that are actually underrated

Ranked by honest expected value for a developer tool.

### Your package registry listing

Deeply underrated, almost never discussed as marketing. The README that renders on your
npm / PyPI / crates.io / Docker Hub page is frequently the **only** page a developer reads before
deciding. Treat registry metadata as launch collateral: description, keywords, a hero line and a
copyable install command inside the first screen.

Getting into **homebrew-core** is a durable distribution asset rather than a one-day spike — a
permanent, trusted install path.

### GitHub Trending

- [GitHub Trending](https://github.com/trending) — for an open-source dev tool, hitting daily trending in your language is comparable to a good Hacker News day.

The caveat matters: it ranks on raw star velocity, which is a popularity vote and not an adoption
signal. See [chapter 6 on why stars are compromised](06-open-source-and-plg.md#63-github-stars-are-a-compromised-metric).
Enjoy it if it happens; don't build a strategy around farming it.

### Awesome-lists in your category

Getting merged into the relevant `awesome-*` repository is a permanent, compounding placement
that also feeds retrieval corpora that models read. Very high value per hour of effort, and
almost nobody talks about it. (Yes, including this one — see [CONTRIBUTING.md](../CONTRIBUTING.md).)

### The smaller, more technical surfaces

- [Indie Hackers](https://www.indiehackers.com) — still the best place for build-in-public updates and revenue transparency. Lower traffic than its peak, higher intent, and an audience that understands engineering trade-offs.
- [DevHunt](https://devhunt.org) — weekly launch cycle specifically for developer tools, SDKs and IDE extensions. Far less competition than Product Hunt and a genuinely developer audience. Small absolute numbers.
- [Peerlist](https://peerlist.io) — professional network for builders with a launch surface; technical, engaged, small.
- [Lobsters](https://lobste.rs) — small, invite-only, extremely high signal-to-noise, and considerably more hostile to marketing than HN. **Do not join Lobsters in order to promote something.** Participate for real or skip it entirely.

### AI tool directories

Two are worth the form-filling because they rank for "best AI tool for X" queries:
[There's An AI For That](https://theresanaiforthat.com) and [Futurepedia](https://www.futurepedia.io).
Note that TAAFT's links are nofollow and Futurepedia typically charges for placement.

Almost everything else in this space is a paid-listing business dressed as a directory. **Five or
six directories done properly beats mass submission**, and the "we'll submit you to 100+
directories" services generate low-quality links to pages nobody visits.

---

## 7.5 A launch sequence that reflects how this actually works

**T-minus 8–12 weeks.** Build the audience. Ship in public, write the technical posts, answer
questions in the communities where your users already are. This is the part that determines the
outcome, and it's the part every launch guide skips.

**T-minus 2 weeks.** Get the assets right: a demo that works without signup, a README/landing
page that passes the five-second test, and a genuinely honest scope statement. Line up the people
who would *want* to know about this — not to ask for upvotes, but so the news reaches them.

**T-minus 1 week.** Write the first comment. On both HN and PH this is the most-read text you'll
publish that day. Say what it is, why you built it, what it deliberately doesn't do, and what
you'd like feedback on. Vulnerability outperforms polish on both platforms.

**Launch day.** Post once, early in your audience's morning. Then spend the day *in the comments*.
Answer every substantive criticism. Do not post the link in seven Slack groups asking for support.

**T-plus 1 week.** The follow-through is where the value is: convert the feedback into a public
changelog, reply to everyone who tried it, and write the retrospective. A good "what I learned
launching X" post frequently outperforms the launch itself.

**T-plus 1 month.** Ask what actually converted. Usually it is not the platform you optimised for.

---

## 7.6 Astroturfing is now a legal exposure, not a growth tactic

The old wink about "seeding some discussion" needs replacing with something blunt.

The FTC's **Rule on the Use of Consumer Reviews and Testimonials** was finalised in August 2024
and took effect in October 2024. It bans, among other things:

- Fake or AI-generated reviews and testimonials from people who never used the product
- Incentivising reviews conditioned on expressing a particular sentiment
- **Insider reviews** — from employees, founders or their relatives — without clear and conspicuous disclosure of the connection

- [FTC Rule on Consumer Reviews and Testimonials — Questions and Answers](https://www.ftc.gov/business-guidance/resources/consumer-reviews-testimonials-rule-questions-answers) — the official business guidance. Read the primary source; it's short and readable.

Civil penalties run to tens of thousands of dollars per violation, and the FTC has been sending
warning letters under it.

**So, plainly:** buying upvotes, running sockpuppet accounts, paying agencies to seed Reddit or
Product Hunt threads, and having employees post as neutral users are all (a) against every
platform's terms, (b) plausibly within the scope of a federal rule where a product endorsement is
involved, and (c) reputationally fatal in engineering communities, which are unusually good at
detecting them and unusually unforgiving afterwards.

The entire "buy upvotes" vendor ecosystem that now dominates search results for launch advice
belongs on a don't-bother list, not in a toolkit.

---

## 7.7 Don't bother

1. **Buying upvotes, karma or "launch boosts."** See 7.6.
2. **Agency "Reddit seeding" and sockpuppets.** Same, plus engineers are very good at spotting it.
3. **Mass directory submission services.** Links from pages with no traffic.
4. **Asking friends to upvote your Show HN.** Explicitly against the rules; silently kills the post and can permanently penalise your domain.
5. **Treating Product Hunt as your distribution plan.** It's one day. Build the audience that makes the day work.
6. **Any "2026 launch study" from a launch-services vendor.** This entire content niche is now lead-gen. Cite the platforms' own documentation instead.

---

## 7.8 If you only do five things

1. Spend the pre-launch quarter building an audience; treat launch day as the conversion event it actually is.
2. Read the Show HN guidelines properly, and never ask for a vote.
3. Write the first comment as if the criticism is the point — because it is.
4. Fix your package-registry README, which more people will read than your launch post.
5. Publish the honest retrospective a week later. It usually outperforms the launch.

---

**Related:** [Communities and social](08-communities-and-social.md) · [Open source and PLG](06-open-source-and-plg.md) · [Psychology and ethics](14-psychology-and-ethics.md)

*Last reviewed July 2026. Platform rules change; read the live guidelines before you post.
Corrections welcome — see [CONTRIBUTING.md](../CONTRIBUTING.md).*
