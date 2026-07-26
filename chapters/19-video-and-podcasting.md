# 19. Video, YouTube and Podcasting

> The most underused channel available to technical products, and the one engineers avoid
> hardest. A single good twenty-minute video has effectively unlimited half-life, ranks in both
> Google and AI answers, and demonstrates a technical product in a way text cannot.

---

## 19.1 Why this is underrated

Text has to *describe* what your tool does. Video *shows* it. For anything with a workflow — a
CLI, a debugger, an infrastructure tool, a UI — that difference is enormous, and it's why the
"how I built X" genre consistently outperforms the equivalent blog post.

Three structural advantages that compound:

- **Half-life.** A good tutorial keeps earning views for years. A social post is dead in 48 hours.
- **Search presence in two places.** YouTube is itself a major search engine, and video results surface in Google and increasingly in AI answers.
- **Trust transfer.** Watching someone competent use a tool is the closest thing to a reference from a colleague.

The reason engineers avoid it is almost always production anxiety, and that anxiety is
misdirected — see 19.3.

---

## 19.2 What actually works for technical audiences

In rough order of return:

1. **Build-alongs.** Start from nothing, ship something real, unedited enough to include the bits that go wrong. The failures are the credibility.
2. **Architecture walkthroughs.** How the thing actually works, with diagrams. This is the format that gets shared inside engineering teams.
3. **Conference talks, re-cut.** You already gave it. Record it properly and it becomes an evergreen asset. See [chapter 25](25-events-and-education.md).
4. **Debugging sessions.** Genuinely rare, genuinely compelling, and almost nobody does it.
5. **Short-form clips cut from the above.** Derivative, cheap, and useful for discovery — but only after the long-form asset exists.

**What doesn't work:** product-marketing sizzle reels, animated explainers with a voiceover artist,
and anything where nobody actually uses the product on screen.

Two channels worth studying as references for opposite ends of the format spectrum —
[Fireship](https://www.youtube.com/@Fireship) for extreme information density, and
[ThePrimeagen](https://www.youtube.com/@ThePrimeagen) for long-form, unedited, personality-led work.
Both prove the same point: the audience rewards competence, not polish.

---

## 19.3 The production floor

**What actually matters:** audio quality, legible text on screen, and getting to the point in the
first fifteen seconds.

**What doesn't:** your camera, your lighting, your face being on screen at all, and your editing
software.

Audio is the one place to spend money — viewers forgive bad video and leave immediately on bad
audio. A decent USB microphone in a room with soft furnishings beats an expensive microphone in a
bare room.

For screen recordings, **increase your font size far beyond what feels natural.** Most developer
video is unwatchable on a phone because the author recorded at their normal editor settings.

- [OBS Studio](https://github.com/obsproject/obs-studio) — free, open source, the standard for screen recording and streaming. Learn scenes and you have a studio.
- [Kdenlive](https://kdenlive.org/) — free, open-source, cross-platform video editor. Sufficient for everything in 19.2.
- [DaVinci Resolve](https://www.blackmagicdesign.com/products/davinciresolve) — professional-grade with a genuinely capable free tier. Overkill until it isn't.
- [Audacity](https://github.com/audacity/audacity) — free audio editing; enough to clean up a recording.
- [Descript](https://www.descript.com/) — edit video by editing the transcript. A step change if you think in text rather than timelines.

---

## 19.4 YouTube mechanics, honestly

The title and thumbnail do most of the work, and the first fifteen seconds do the rest. That's
not a hack, it's just what the platform optimises for: whether people click, and whether they stay.

- **Title for the search someone actually types**, not for cleverness. "How to X in Y" outperforms wordplay for technical content, permanently.
- **Thumbnail should be legible at phone size.** Three or four words maximum.
- **Say what the video delivers immediately.** No intro sequence, no "hey guys, before we get started."
- **Put the timestamps in the description.** They generate chapter markers, which improve retention *and* get surfaced in search.
- **Ignore subscriber count.** Watch time and retention are what the system optimises, and what actually correlates with reach.

- [YouTube Creators](https://www.youtube.com/creators/) — the official resource hub. Dry, free, and more accurate than the guru ecosystem around it.
- [How YouTube's recommendation system works](https://blog.youtube/inside-youtube/on-youtubes-recommendation-system/) — YouTube's own explanation, which is a useful counterweight to speculation about "the algorithm."

---

## 19.5 Podcasting

Podcasting is a **relationship channel, not a reach channel** — and for B2B that's often the more
valuable of the two.

**Guesting beats hosting**, at least at first. It borrows an existing audience, costs an hour, and
carries none of the production burden. Twenty good guest appearances will do more for a small
company than twenty episodes of a show nobody has found yet.

**If you do host**, the strongest format for a technical company is the one where you interview
your own users about problems in their world, not about your product. It produces genuine
research, deepens the relationship, and generates content as a side effect.

Be realistic about measurement: podcast attribution is famously poor. Use the self-reported
attribution field from [chapter 12](12-analytics-and-attribution.md), because it is frequently
the only place a podcast will ever show up.

- [IAB Podcast Measurement Technical Guidelines](https://iabtechlab.com/standards/podcast-measurement-guidelines/) — the standard that defines what a "download" legitimately means. Worth knowing before you compare two hosts' numbers.
- [Transistor](https://transistor.fm/) — podcast hosting with good analytics and unlimited shows on one account.
- [Podcast Index](https://podcastindex.org/) — an open, free directory and API, built as an alternative to closed platform control.

---

## 19.6 Repurposing

One recording should become many artefacts. The pipeline from
[chapter 16](16-ai-marketing-stack.md#165-content-operations) applies directly: transcript first,
then everything else derives from it.

- [Whisper](https://github.com/openai/whisper) — MIT-licensed, self-hostable transcription; the foundation of the pipeline.
- [faster-whisper](https://github.com/SYSTRAN/faster-whisper) — substantially faster reimplementation; the practical choice for batch work.
- [WhisperX](https://github.com/m-bain/whisperX) — adds word-level timestamps and speaker diarisation, which is what you need for clean clip cutting and multi-speaker transcripts.
- [whisper.cpp](https://github.com/ggml-org/whisper.cpp) — plain C/C++ port with no Python dependency. The easiest thing to put in a build pipeline.

**Always publish the transcript.** It's an accessibility requirement, an SEO asset, and the thing
that makes your video quotable by an AI answer engine — which, per
[chapter 4](04-seo-and-ai-search.md), is increasingly how people find anything.

---

## 19.7 If you only do five things

1. Record one twenty-minute build-along of your own product. Publish it unpolished.
2. Buy a decent microphone. Ignore the camera.
3. Double your editor font size before recording anything.
4. Get on five podcasts before you start one.
5. Publish the transcript with every video.

---

**Related:** [Content marketing](03-content-marketing.md) · [Communities and social](08-communities-and-social.md) · [Events and education](25-events-and-education.md)

*Last reviewed July 2026. Corrections welcome — see [CONTRIBUTING.md](../CONTRIBUTING.md).*
