# 26. Performance and Accessibility

> Your marketing site is almost certainly the slowest, least accessible thing your company
> ships. It's built by whoever had time, on a page builder nobody owns, loaded with tracking
> scripts nobody audits — and it's the first thing a prospect touches.

---

## 26.1 Why the marketing site is the worst thing you own

The product gets code review, performance budgets and a CI pipeline. The marketing site gets a
tag manager and four analytics vendors, and nobody's name is on it.

The result is predictable: the page that must load fast for a stranger on mobile data is the one
carrying the most third-party JavaScript. Meanwhile the product, which loads for people already
committed to waiting, is fine.

**The single highest-leverage audit:** open your marketing site's network tab and count the
third-party requests. Then ask, for each one, who asked for it and whether anyone still looks at
its data. Most sites can delete half.

---

## 26.2 Core Web Vitals, and what they actually buy you

- [Core Web Vitals](https://web.dev/articles/vitals) — the canonical definition of LCP, INP and CLS with thresholds. **INP replaced FID in March 2024**; any guide still saying FID is stale.
- [Chrome UX Report](https://developer.chrome.com/docs/crux) — the public dataset of real Chrome user measurements. This is *field* data, which is what Google actually uses, as opposed to the lab data your local Lighthouse run produces. The gap between the two surprises people.
- [HTTP Archive Web Almanac](https://almanac.httparchive.org/) — annual, methodologically transparent, crawl-based analysis of how the web is actually built. Free and unusually rigorous.

**Be honest about the ranking benefit: it is small.** Core Web Vitals are a tiebreaker, not a
lever. The reason to care is conversion, not ranking — a slow page loses people before they read
your positioning, and that cost is immediate and much larger than any SEO effect.

---

## 26.3 Tooling

All open source and free unless noted:

- [Lighthouse](https://github.com/GoogleChrome/lighthouse) — already in your browser's dev tools. Lab data; good for catching regressions, bad for representing real users.
- [WebPageTest](https://www.webpagetest.org/) — real devices, real network conditions, filmstrips and request waterfalls. Deeper than Lighthouse when you need to know *why*. The [agent is open source](https://github.com/catchpoint/WebPageTest) if you want to self-host.
- [sitespeed.io](https://github.com/sitespeedio/sitespeed.io) — fully open-source, self-hostable performance monitoring. The right answer if you want continuous measurement without a vendor.
- [Lighthouse CI](https://github.com/GoogleChrome/lighthouse-ci) and the [GitHub Action wrapper](https://github.com/treosh/lighthouse-ci-action) — run Lighthouse on every commit and fail the build on regression. This is how performance stops rotting.
- [Unlighthouse](https://github.com/harlan-zw/unlighthouse) — scans **every page on a site** rather than one URL at a time. Enormously useful for finding the one terrible page you forgot about.
- [web-vitals](https://github.com/GoogleChrome/web-vitals) — the official library for measuring the metrics from real users, so you can send field data to your own analytics.

**Fonts are usually the biggest single win** on a marketing site:

- [fontaine](https://github.com/unjs/fontaine) — automatic fallback-font metric overrides, which kills the layout shift when your webfont loads. Close to free CLS improvement.
- [fonttools](https://github.com/fonttools/fonttools) — `pyftsubset` strips a font to the characters you actually use. Often an order-of-magnitude size reduction.
- **Self-host your fonts.** Faster, and it removes a third-party request you'd otherwise have to declare in a cookie banner.

---

## 26.4 Rendering, decided honestly

Static or server-rendered, unless you have a specific reason otherwise. The reasons compound:

- **Some AI fetchers do not execute JavaScript.** If your content only exists after hydration, you are invisible to them — see [chapter 4](04-seo-and-ai-search.md#44-the-highest-leverage-30-minutes-bot-control).
- Googlebot renders JS, but rendering is queued and can lag.
- Static is faster, cheaper and harder to break.

- [Google Search Central: JavaScript SEO basics](https://developers.google.com/search/docs/crawling-indexing/javascript/javascript-seo-basics) — the authoritative description of how Google handles JS, and the mistakes that break it.

**Note:** dynamic rendering (serving a prerendered version to bots) is now deprecated as a
recommended approach — Google explicitly treats it as a workaround rather than a solution. Don't
build new systems on it.

---

## 26.5 Accessibility

Two reasons to care, and you should be honest that only one of them motivates most teams:
**it's right**, and **it's increasingly a legal and procurement requirement**.

The procurement angle is the one that gets budget: enterprise and public-sector buyers ask for
accessibility conformance documentation, and not having it stalls deals the same way missing SOC 2
does ([chapter 21](21-trust-and-compliance-as-marketing.md)).

- [WCAG 2.2](https://www.w3.org/TR/WCAG22/) — the normative standard. You will not read it end to end and you shouldn't.
- [How to Meet WCAG 2.2 (Quick Reference)](https://www.w3.org/WAI/WCAG22/quickref/) — the filterable version. Start here instead.
- [Understanding WCAG 2.2](https://www.w3.org/WAI/WCAG22/Understanding/) — per-criterion explanation of intent, which is what you need when a checker flags something and you don't know why it matters.
- [ARIA Authoring Practices Guide](https://www.w3.org/WAI/ARIA/apg/) — patterns for accessible components. The most practically useful W3C resource here, and the one to consult *before* building a custom dropdown.
- [WebAIM WCAG 2 Checklist](https://webaim.org/standards/wcag/checklist) — WCAG restated in plain language. The version to give a designer.
- [WebAIM Million](https://webaim.org/projects/million/) — annual automated survey of the top million homepages. Sobering, and useful for calibrating how bad the baseline is.

**Tooling:**

- [axe-core](https://github.com/dequelabs/axe-core) — the rules engine underneath most accessibility tooling, including your browser's. [axe-core-npm](https://github.com/dequelabs/axe-core-npm) provides Playwright, Puppeteer and CLI integrations, so this belongs in CI.
- [Pa11y](https://github.com/pa11y/pa11y) — command-line accessibility testing; simpler to adopt than axe. [pa11y-ci](https://github.com/pa11y/pa11y-ci) adds sitemap support for whole-site runs.
- [WAVE](https://wave.webaim.org/) — browser-based with a visual overlay. The tool to hand a designer who doesn't read test output.

**The honest limit: automated tools catch roughly a third of issues.** They cannot tell you
whether your alt text is meaningful, your focus order is logical, or your error messages make
sense to a screen reader user. Automated testing is the floor, not the ceiling.

**On accessibility overlays** — the JavaScript widgets that promise instant compliance: the
accessibility community is close to unanimous that they do not work and sometimes make things
worse. [The Overlay Fact Sheet](https://overlayfactsheet.com/) is the community statement, signed
by a large number of practitioners including people who use assistive technology daily. Read it
before buying one.

---

## 26.6 The legal landscape

**Not legal advice, and verify current status before acting** — this area moves and the details
determine whether it applies to you at all.

- [ADA.gov Web Accessibility](https://www.ada.gov/topics/web-accessibility/) — the US Department of Justice's own page. Web accessibility litigation in the US is substantial and ongoing.
- [Section 508 / ICT Accessibility Standards](https://www.access-board.gov/ict/) — the US federal procurement standard. Matters the moment you sell to government, and often flows down through contractors.
- [Directive (EU) 2019/882 — the European Accessibility Act](https://eur-lex.europa.eu/eli/dir/2019/882/oj) — the EU directive covering accessibility of certain products and services. **Check scope carefully before assuming it applies to you:** it covers a defined list of products and services rather than all websites, and there are exemptions for the smallest enterprises. A B2B developer-tools marketing site may well fall outside it. Confirm with the current official guidance and, if it matters commercially, with counsel.
- [Web Accessibility Directive (EU) 2016/2102](https://eur-lex.europa.eu/eli/dir/2016/2102/oj) — the *other* EU accessibility directive, covering public sector bodies. Relevant if you sell to them.
- [EN 301 549](https://www.etsi.org/standards) — the harmonised European standard that EU procurement references.

---

## 26.7 If you only do five things

1. Count the third-party requests on your marketing site and delete half.
2. Self-host and subset your fonts.
3. Put Lighthouse CI and axe in your pipeline so neither can rot silently.
4. Run one keyboard-only pass through your signup flow. You will find something.
5. Do not buy an accessibility overlay.

---

**Related:** [SEO and AI search](04-seo-and-ai-search.md) · [Landing pages and conversion](18-landing-pages-and-conversion.md) · [Brand and identity](22-brand-naming-and-identity.md)

*Last reviewed July 2026. Not legal advice; regulatory scope in this area is genuinely
complicated and worth checking properly. Corrections welcome — see
[CONTRIBUTING.md](../CONTRIBUTING.md).*
