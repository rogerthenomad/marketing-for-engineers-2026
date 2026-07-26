# 1. Positioning and Audience

> Everything downstream depends on this chapter. Buyer personas built from demographics have
> been largely replaced by job-based and alternatives-based thinking, the free research tooling
> has almost entirely turned over in the last few years, and there's a new failure mode worth
> naming early: asking a language model what your customers want instead of asking your
> customers.

---

## 1.1 Positioning comes before everything

Almost every marketing problem an engineer describes to me is actually a positioning problem
wearing a costume. "Our conversion rate is bad." "People don't get it." "We keep losing to a
worse product." "We can't figure out what to write." All of these are downstream of not being
able to finish this sentence:

> **We are the only ___ that ___, for ___, who want ___.**

If you can't complete it honestly, no amount of content, SEO or paid spend will rescue you.
You'll just distribute a confusing message more efficiently.

- **Obviously Awesome** (April Dunford, 2019) — the standard text, and the right first read for a technical founder. The method is refreshingly mechanical: list the competitive alternatives, isolate what's genuinely unique about you, translate those attributes into the value they enable, work out who cares disproportionately about that value, and then deliberately choose the market category you want to be evaluated inside.
- [April Dunford's site](https://www.aprildunford.com/) — hosts a free Positioning Canvas workbook. Do the exercise before you read anything else in this list.
- **Sales Pitch** (April Dunford, 2023) — how to say it out loud, structured around presenting the buyer's alternatives honestly rather than parading features.

**The insight engineers usually find surprising:** your positioning is defined by the
*alternatives*, not by your feature list. If your prospect's realistic alternative is a Python
script and a cron job, you are competing with a Python script and a cron job — not with the
funded company you benchmark against. Price, message and roadmap all change once you get this
right.

---

## 1.2 Jobs to be done

The complementary lens, and the one that survives contact with reality better than personas.
Instead of asking who your customer is, ask **what progress they were trying to make when they
hired your product** — and what they fired to do it.

- [Know Your Customers' "Jobs to Be Done"](https://hbr.org/2016/09/know-your-customers-jobs-to-be-done) — the canonical short version. (2016, Christensen, Hall, Dillon & Duncan / HBR)
- **Demand-Side Sales 101** (Bob Moesta, 2020) — JTBD applied to selling, from one of the framework's architects. The best sales book for people who dislike selling.

The most useful JTBD question for a technical product, and the one almost nobody asks:
**"What were you doing about this before?"** The answer is your real competitor and usually your
best positioning material. The second most useful: **"What finally made you look for something
else?"** That's your inbound trigger, and it belongs at the top of your homepage.

---

## 1.3 Talking to actual users

There is no substitute for this: **you must talk to real people.** What's changed is that it's
now trivially easy to *simulate* the research instead — ask a model to generate a persona, produce a plausible interview transcript,
and skip the uncomfortable part. Don't. A model can tell you what people *generally* say about
problems like yours. It cannot tell you what your specific prospect actually did last Tuesday
when the thing broke.

Use models for what they're genuinely good at here: **synthesising research you actually
collected.** Twenty interview transcripts, a year of support tickets, or every mention of your
category in a community — an LLM is excellent at finding the patterns across those and terrible
at inventing them.

**How to run the interviews:**

- Ask about specific past behaviour, not hypothetical future behaviour. "Walk me through the last time this happened" beats "would you use a tool that…" every time.
- Never pitch during a research call. The moment you start selling, they start being polite.
- Ask what they tried and abandoned. Abandoned solutions are the richest positioning data you'll get.
- Ask what they'd have to stop doing to adopt you. Switching costs kill more deals than feature gaps.
- Ten good conversations beat a hundred survey responses. This is genuinely true and consistently ignored.

**Where to find people to talk to**, in rough order of yield for a technical product: your own
issue tracker and support inbox; the communities in [chapter 8](08-communities-and-social.md);
people who churned (the single most underused source); people who evaluated you and chose
something else; and — for cold outreach — a small, well-researched, honest ask rather than a
templated blast. See [chapter 10](10-outbound-and-partnerships.md).

---

## 1.4 The research tooling actually turned over

Nearly every free research tool that older marketing guides recommend is now gone. Amazon's Alexa web-analytics
service shut down in 2022. Social Mention, Nuzzel, Klout and a long tail of free social-listening
tools are dead. Followerwonk and Twitonomy lost most of their value when X's API pricing changed.
Pipl became enterprise-only. Siftery is gone.

**What works in 2026:**

**Understanding demand**
- [Google Search Console](https://search.google.com/search-console/about) — free, and the only source of truth for what people actually search to reach you. Start here, not with a keyword tool.
- [Google Trends](https://trends.google.com/) — free; good for direction and seasonality, bad for absolute volume.
- [Ahrefs Webmaster Tools](https://ahrefs.com/webmaster-tools) — free for domains you own and verify.
- **Ask a model what it recommends in your category.** Genuinely useful competitive research now: run the prompts your buyers would run, across several assistants, and see who gets named. That *is* your AI-visibility baseline. See [chapter 4](04-seo-and-ai-search.md).

**Understanding competitors**
- [AlternativeTo](https://alternativeto.net/) — still alive, still the fastest way to see how the market frames your category.
- **Your competitors' own comparison pages, changelogs and pricing pages.** Underrated and free. Their changelog tells you their roadmap; their comparison pages tell you who they think they're losing to.
- **Reddit and Hacker News search.** Where people say what they actually think about the tools in your space, in public, at length. Frequently more useful than any paid tool.
- **Review sites** (G2, Capterra for business software) — read the three-star reviews, which are the only honest ones.

**Talking to people**
- [Typeform](https://www.typeform.com/), Google Forms, or [Tally](https://tally.so/) for surveys — the tool doesn't matter, the questions do.
- Anything that records and transcribes calls. Transcripts are the raw material for the synthesis work above.

---

## 1.5 The "how did you hear about us" field

One tactic, promoted out of the analytics chapter because it belongs in research too: **ask every
new signup, in free text, how they found you.**

With roughly two-thirds of searches ending without a click, meaningful discovery happening inside
AI assistants, and dark-social sharing invisible to every analytics tool, self-reported
attribution has gone from a soft supplement to one of the most reliable signals you have. It is
also nearly free to implement.

Do it as an optional open text field, not a dropdown — dropdowns tell you what you already
guessed. Read the answers monthly. See [chapter 12](12-analytics-and-attribution.md).

---

## 1.6 Anti-patterns

- **Demographic personas.** "Marketing Mary, 34, likes yoga" tells you nothing about whether she'll adopt your CLI. Job-based and alternatives-based thinking has largely replaced this, correctly.
- **Asking an LLM to be your customer.** It will confidently produce plausible, average, useless answers. Use it to synthesise real data, not to substitute for it.
- **Positioning against the market leader by default.** Most of your losses are to "do nothing," a spreadsheet, or an internal script. Position against the real alternative.
- **Researching until you're certain.** You won't be. Ten conversations and a decision beats forty conversations and a document.
- **Confusing what people say they want with what they've paid for.** Only the second one is data.

---

## 1.7 If you only do five things

1. Complete the Onliness sentence. Show it to five people who don't work with you and see if they repeat it back correctly.
2. Interview ten users about the last time the problem happened — past behaviour, not hypotheticals.
3. Ask five churned users what they went back to.
4. Run your buyers' likely prompts through three AI assistants and write down who gets recommended.
5. Add the "how did you hear about us?" free-text field today.

---

**Related:** [Content marketing](03-content-marketing.md) · [Pricing and business model](13-pricing-and-business-model.md) · [Analytics and attribution](12-analytics-and-attribution.md)

*Last reviewed July 2026. Corrections welcome — see [CONTRIBUTING.md](../CONTRIBUTING.md).*
