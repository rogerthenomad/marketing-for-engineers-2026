# 8. Communities and Social

> A few years ago the answer here was Twitter, Facebook, Reddit, LinkedIn and Quora. Two of
> those are no longer meaningful channels for a technical product, one has transformed beyond
> recognition, and the single most important surface in 2026 — Reddit — used to be described
> mainly as a place you get banned from.

---

## 8.1 Where engineers actually are now

**The honest summary: nowhere, together.** The unified dev-Twitter of 2018 is gone and nothing
replaced it. You multi-home or you accept reduced reach. Anyone telling you "everyone moved to
platform X" is selling something.

### Stack Overflow: say the quiet part loudly

This is the clearest death in this entire handbook. The standard advice — build reputation by
answering questions in your problem space — describes a channel that no longer exists.

Monthly question volume peaked around 200,000 in the mid-2010s and fell off a cliff after
ChatGPT's release, reaching levels last seen around 2008 and erasing roughly fifteen years of
growth. Reported year-over-year declines through 2025–2026 are in the high tens of percent.

- [Dramatic drop in Stack Overflow questions as devs look elsewhere for help](https://www.devclass.com/ai-ml/2026/01/05/dramatic-drop-in-stack-overflow-questions-as-devs-look-elsewhere-for-help/4079575) — (2026, DevClass)
- [Stack Overflow in freefall: 78 percent drop in number of questions](https://www.techzine.eu/news/devops/137686/stack-overflow-in-freefall-78-percent-drop-in-number-of-questions/) — (2026, Techzine)

Unusually for a statistic in this field, **this one is independently checkable**: Stack Exchange
publishes a public Data Explorer, and the widely-circulated charts were produced from it. Verify
it yourself rather than taking anyone's word.

**Implication:** the legacy corpus still has SEO value, and being present is free. But delete any
strategy that involves reaching developers there.

### The rest of the map

- **Hacker News** — still the centre of gravity for launches and serious technical discussion. Highest-quality traffic per visitor of any free channel. See [chapter 7](07-launching.md).
- **Reddit** — now the most strategically important surface on the open web for technical products. See 8.2.
- **Discord** — where day-to-day developer conversation actually happens, spread across thousands of project and language servers. Invisible to search, which is exactly why it's undervalued as a channel and overvalued as an asset.
- [dev.to](https://dev.to) — survived the AI-content wave better than expected and is worth cross-posting to. Not worth making primary.
- [Lobsters](https://lobste.rs) — small, technical, invite-only, promotion-hostile. High read value, low write value unless you're genuinely part of it.
- **Hashnode** — showing consistent signals of abandonment (long-dormant changelog and communications). Don't build your blog there. Verify current status before relying on this either way.

---

## 8.2 Reddit is the biggest change since 2018

Reddit used to be a place engineers hung out and marketers got banned from. It is now arguably
the most valuable single distribution surface on the open web — and the most rule-bound.

**Why it matters now:** Reddit is consistently among the most-cited domains across AI answer
engines. When a developer asks a model "what should I use for X," a credible Reddit thread is
frequently the mechanism by which your product becomes the answer.

- [The Most-Cited Domains in AI](https://www.semrush.com/blog/most-cited-domains-ai/) — the best-sourced measurement of this. (Semrush; they have the panel to measure it, and they also sell tools — read accordingly.)
- [Reddit Is Winning the AI Game](https://www.cjr.org/analysis/reddit-winning-ai-licensing-deals-openai-google-gemini-answers-rsl.php) — Columbia Journalism Review on Reddit's licensing leverage. The highest-credibility source in this area.

**Two caveats that most 2026 advice omits:**

1. **This channel is volatile.** Reddit's citation share in major assistants has swung dramatically over periods of weeks. It can be turned down by someone else's ranking change, with no notice.
2. **The commercial arrangements are not permanent.** Reddit's content-licensing deal with Google, signed in 2024, has been publicly reported as uncertain in mid-2026. Build your reasoning on the community and citation dynamics, which are structural — not on a contract that may lapse.

### The self-promotion rules, corrected

**The most-repeated piece of Reddit advice on the internet is out of date.** Reddit retired the
formal site-wide 9:1 self-promotion ratio. What replaced it is a qualitative spam policy enforced
almost entirely by individual subreddit moderators and AutoModerator — which is precisely why the
rules feel arbitrary and vary enormously between communities.

- [Reddit Content Policy](https://redditinc.com/policies/content-policy) — the actual site-wide policy. Spam and manipulation are covered here; a numeric ratio is not.

**The only rule that works:** read the sidebar and the wiki of each individual subreddit before
posting, and participate genuinely for weeks before you ever link your own thing. Subreddits
broadly split into ones with designated promo days or megathreads, ones that permit promotion
under a local ratio, and ones that ban it outright — and the large general programming subs are
mostly in the last group.

Post a genuinely useful library to a language-specific subreddit without marketing language and
you'll often do fine. Post a launch announcement to r/programming and you won't.

### Reddit Ads

A real, functional performance channel, genuinely differentiated by **subreddit targeting** and
**conversation targeting** — placing ads against posts containing specific terms, which is the
closest thing to intent targeting outside search.

- [Reddit Ads](https://ads.reddit.com)

The CPC and ROAS benchmarks you'll find are almost entirely published by agencies selling Reddit
Ads management. Ignore them and measure your own. The one structural claim worth testing: the
handful of mega-subreddits are bid up, while long-tail subreddits often clear well below median
CPM at equal or better intent.

---

## 8.3 Choosing a community platform

This is a **one-way door**. Picking wrong costs you a migration that loses most of your members.
The axis that matters most is the one comparison posts bury: **does the content become a public,
indexable, retrievable asset, or does it evaporate?**

| | Discord | Slack | Discourse | GitHub Discussions |
|---|---|---|---|---|
| Cost at 100–5,000 members | Free | Expensive per seat | Self-host free / hosted paid | Free |
| Public and indexable | No | No | **Yes** | **Yes** |
| Feeds AI answer engines | No | No | **Yes** | **Yes** |
| Answers stay findable | Poor | **Worst** (history limits) | **Best** | **Best** |
| Real-time culture | **Best** | Good | Poor | Poor |
| User already has an account | Mostly | At work, not for you | No | **Yes** |

**The recommendation for a developer tool: GitHub Discussions + Discord.**

Discussions carries the durable, searchable, indexed Q&A right next to the code, with near-zero
friction because your users already have GitHub accounts. Discord carries the real-time culture,
early-adopter energy and support triage. This pairing is where most successful dev tools
converged.

**Discourse** if knowledge accumulation is the entire point — large user base, complex product,
long-lived answers. Best long-term search and AI-visibility asset of the four; slowest to feel
alive.

**Do not start a public community on Slack in 2026.** Free-tier history limits destroy your
community's knowledge on a rolling basis, none of it is indexable, and paid seats scale
punishingly. Slack communities from the 2018–2021 era are the single most common "we have to
migrate" story in developer relations.

**Discord's structural weakness** is that it's a walled garden. Every answered question is
invisible to search and to model retrieval, which means you regenerate the same answers forever
and get zero compounding value. Mitigate deliberately: promote recurring questions into docs or
Discussions on a schedule. Treat it as a process, not an intention.

### Metrics

**Vanity:** total members, total messages, server joins. These are what community tools sell you,
and they measure nothing.

**Real:** weekly active *contributors* (posted, not lurked) · question-to-answer rate and
time-to-first-response · **percentage of answers given by community members rather than staff**,
which is the only true measure of a self-sustaining community · 30- and 90-day member retention ·
progression from lurker to asker to answerer to contributor.

- [Common Room](https://www.commonroom.io/) — aggregates GitHub, Discord, LinkedIn and other signals into a person-level view. The useful insight behind the category: community engagement precedes purchase intent, so a repository star or a Discord question is a warmer signal than any cold outbound.

---

## 8.4 Social platforms, honestly ranked

For a technical product with limited time, the realistic 2026 stack is **X + LinkedIn + YouTube**.

**YouTube is the most underrated channel for developer tools**, and almost every
engineering-founder guide omits it. Long-form tutorials and conference-talk-style content have
effectively unlimited half-life, rank in both Google and AI answers, and demonstrate a technical
product in a way text cannot. One good twenty-minute "how I built X" video routinely outperforms a
year of posting.

**X** still has the largest dev-adjacent audience in absolute terms, but reach is unreliable and
link posts are suppressed. High ceiling, high variance, and increasingly dependent on an existing
following.

**LinkedIn** is the surprise entry. Developers themselves spend little time there, but the
**buyers** of developer tools do — engineering managers, directors, platform leads. Two structural
facts worth acting on: educational "here's what I learned" content substantially outperforms other
formats, and **posts from individual people travel far further than company-page posts**, whose
organic reach has fallen sharply. Post from humans. Always.

**Bluesky and Mastodon** are cheap insurance rather than growth. Both are small, but they contain
a disproportionate share of the open-source, infrastructure, security and standards people — which
is a valuable slice if that's your product's world. Bluesky's reach is roughly chronological, so
good posts can travel without an algorithmic gatekeeper. Mastodon has zero tolerance for anything
that reads as marketing: post as a human or don't post.

**Threads and TikTok are not developer channels.** Both are enormous and almost entirely
non-technical. Fine for recruiting; skip otherwise.

**What's genuinely dead for technical products:** Facebook Pages (organic reach for brand pages
has been negligible for years), and Quora, which has declined severely as both a traffic source
and a community.

---

## 8.5 If you only do five things

1. Delete Stack Overflow outreach from your plan; it's no longer a channel.
2. Pick GitHub Discussions + Discord, and set a recurring process for promoting Discord answers into indexed docs.
3. Participate genuinely in two or three subreddits where your users already are, for months, before you ever link your own work.
4. Post from your personal account, not the company page — everywhere, but especially LinkedIn.
5. Make one twenty-minute YouTube video properly. It will still be working for you in three years.

---

**Related:** [Launching](07-launching.md) · [Content marketing](03-content-marketing.md) · [SEO and AI search](04-seo-and-ai-search.md)

*Last reviewed July 2026. Platform rules and subreddit policies change constantly — verify before
you post. Corrections welcome — see [CONTRIBUTING.md](../CONTRIBUTING.md).*
