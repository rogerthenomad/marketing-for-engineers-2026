# 3. Content Marketing

> The strategy half of content marketing has aged well. The distribution half has not:
> publishing volume stopped being a strategy, the platforms that used to hand out reach have
> stopped, and the point of a post shifted from "get the click" to "be the thing that gets
> quoted."

---

## 3.1 What changed

**Volume stopped working.** When competent generic content became free to produce, competent
generic content stopped differentiating anything. Google named *scaled content abuse* in its spam
policies in 2024, and — more importantly than the policy — readers developed an allergy. The 2025
word of the year across multiple dictionaries was *slop*. Your audience now has a name for the
failure mode.

**The click stopped being the goal.** With roughly two-thirds of searches ending without a visit,
and answers assembled from passages, a post's job has changed. It now has to be *quotable* —
useful even when read as an extract inside somebody else's answer, and attributable enough that
you get named.

**Which means the winning format changed.** The generic explainer is worthless; a model writes
that instantly and better. What can't be generated is the thing with your data, your incident,
your benchmark, your opinion, and your name on it.

---

## 3.2 Strategy before output

Before writing anything, answer these. If you can't, the writing won't help.

1. **Who is this for, specifically?** Not "developers." "Platform engineers at 50–500 person companies who have just been handed a Kubernetes migration."
2. **What do they already believe that's wrong?** The most-shared technical content usually corrects a widely held misconception.
3. **What can you say that nobody else can?** Your data, your production experience, your failure. If the answer is nothing, don't publish yet — go get the data.
4. **What happens after they read it?** Not "they buy." What is the single next step, and is it on the page?

- [Growing From 0-12k Organic Visitors by Mapping Content to the Sales Funnel](https://growandconvert.com/content-marketing/grew-organic-visitors-suggested-search-hack/) — Grow & Convert's approach of writing for the bottom of the funnel first is more right now than when it was written. Start with the pages that convert, not the ones that get traffic.

---

## 3.3 Formats that work for technical audiences

**Ranked by return on effort:**

1. **Original data and benchmarks.** You ran the test, you have the numbers, nobody else does. This is the single most linkable, most citable, most AI-quotable format available, and engineers are uniquely positioned to produce it.
2. **Incident and post-mortem write-ups.** Enormously popular, deeply trusted, and almost impossible to fake. Publishing yours builds more credibility than any amount of thought leadership.
3. **"How we built X" with real architecture.** Diagrams, trade-offs, the thing you'd do differently.
4. **Genuinely fair comparison content.** "X vs Y" and "alternatives to X" pages convert better than anything else and are increasingly what models read when someone asks for options. Be honest about where you lose. See [chapter 4](04-seo-and-ai-search.md#comparison-and-alternatives-to-x-pages).
5. **Deep documentation.** Frequently the highest-traffic content a dev tool has. See [chapter 5](05-developer-marketing-and-devrel.md#53-docs-are-the-marketing).
6. **Long-form video.** The most underused format for technical products, with effectively unlimited half-life. See [chapter 8](08-communities-and-social.md#84-social-platforms-honestly-ranked).

**What to stop writing:** listicles, "ultimate guides" to topics already covered a thousand
times, keyword-shaped explainers with no first-hand experience, and anything whose main claim to
existence is that a keyword tool showed volume for it.

---

## 3.4 Writing so it gets quoted

The only peer-reviewed research on optimising for generative answers found that the tactics which
actually worked were **adding quotations, adding statistics, and citing sources** — see
[chapter 4](04-seo-and-ai-search.md#43-geo-and-aeo-what-the-evidence-actually-supports). That's
not an exotic new discipline; it's what good editors have always asked for.

Practically:

- **Make each section self-contained.** A reader — or a retrieval system — should be able to lift one section and have it make sense without the four paragraphs above it.
- **Put the answer first, then the reasoning.** Inverted pyramid. The 800-word runway before the answer is a habit from a different era of SEO.
- **Attribute every number.** "Latency dropped 40%" is unusable. "p99 latency dropped from 340ms to 205ms on our staging cluster, measured over two weeks in March 2026" is citable.
- **Use real names.** Named authors with real credentials and their own pages. This is the operational form of E-E-A-T and it's also just honest.
- **Date everything**, and update rather than republish.

---

## 3.5 Own your domain

A lot of older advice recommends Medium as a primary channel. Don't. It's paywalled, its distribution to
non-subscribers is a fraction of what that advice assumed, and you're building an asset on
someone else's balance sheet.

**Publish on your own domain first.** Syndicate afterwards — [dev.to](https://dev.to) is worth
cross-posting to, and cross-posting with a canonical link back is fine and always has been.

The general principle is the one from [chapter 16](16-ai-marketing-stack.md#166-social-scheduling-and-a-lesson-about-platform-risk):
any strategy built on a platform you don't control is one policy announcement away from zero.

---

## 3.6 Using AI without producing slop

Covered in depth in [chapter 16](16-ai-marketing-stack.md#161-where-llms-actually-earn-their-keep).
The short version for writers:

**Use it for:** turning your messy transcript into a structured draft, generating headline
variants for you to choose between, checking which claims in your draft lack sources, and finding
the patterns across forty customer interviews.

**Don't use it for:** the opinion, the story, the data, or the voice. If there's no source
artefact, you're generating slop with extra steps.

The reliable pattern is **AI-assisted, human-edited, human-owned** — which is also, not
coincidentally, what keeps you inside the EU AI Act's editorial-responsibility carve-out. See
[chapter 15](15-privacy-and-compliance.md#156-the-eu-ai-act-for-marketers).

---

## 3.7 Distribution

Writing it is half the job, and the half engineers prefer. A realistic distribution routine:

- **Publish on your domain.** Canonical, dated, named author.
- **Send it to your list.** Your highest-converting channel by a distance. See [chapter 9](09-email-and-lifecycle.md).
- **Post it where the audience actually is**, respecting each community's rules — see [chapter 8](08-communities-and-social.md). One thoughtful post in the right subreddit beats broadcasting to five platforms.
- **Tell the people you cited.** Not a request for a share — just a note that you referenced their work. This is how the relationships in [chapter 10](10-outbound-and-partnerships.md) start.
- **Update it in six months.** Refreshing a piece that already ranks is consistently better value than writing a new one.

---

## 3.8 If you only do five things

1. Publish one piece built on data only you have. Then do it again next quarter.
2. Put the answer at the top of every post.
3. Attribute every number with a method and a date.
4. Move your blog to your own domain if it isn't there.
5. Refresh your best-performing post instead of writing a new mediocre one.

---

**Related:** [SEO and AI search](04-seo-and-ai-search.md) · [Zero-budget growth](02-zero-budget-growth.md) · [AI marketing stack](16-ai-marketing-stack.md)

*Last reviewed July 2026. Corrections welcome — see [CONTRIBUTING.md](../CONTRIBUTING.md).*
