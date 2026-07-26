# 27. International and Localisation

> Most technical products get international users long before they do anything international.
> This chapter is about the order of operations — because localising too early is one of the
> more expensive ways to waste a quarter, and doing nothing is leaving money on the table.

---

## 27.1 The order of operations

Do these in order. Skipping ahead is the mistake:

1. **Look at where your traffic and signups already come from.** You almost certainly have a country that over-indexes and nobody has noticed.
2. **Fix pricing and payments for those markets.** Usually a bigger win than translation, and far cheaper.
3. **Localise support and documentation** before marketing pages. People who already use you feel it first.
4. **Translate the marketing site** only when a specific market justifies the ongoing maintenance cost.
5. **Localise the product** last, and only if the market demands it.

The trap is doing step 4 first because it's the visible one. A translated homepage that leads to
an English product with US-only payment methods converts worse than the English homepage did.

---

## 27.2 International SEO and hreflang

`hreflang` is where most international SEO effort goes and where most of it is wasted, because
the implementation is fiddly and the failure is silent.

- [Google Search Central: localized versions of your pages](https://developers.google.com/search/docs/specialty/international/localized-versions) — the authoritative implementation guide. Read this rather than a blog summary; the return-link requirement in particular trips people up.
- [Managing multi-regional and multilingual sites](https://developers.google.com/search/docs/specialty/international/managing-multi-regional-sites) — the URL-structure decision (subdomain, subdirectory or ccTLD) and its consequences.
- [RFC 5646 / BCP 47](https://www.rfc-editor.org/rfc/rfc5646) — the actual specification for language tags. Worth skimming because a surprising number of `hreflang` bugs are malformed tags.
- [IANA Language Subtag Registry](https://www.iana.org/assignments/language-subtag-registry) — the authoritative list of valid subtags.
- [W3C Internationalization Checker](https://validator.w3.org/i18n-checker/) — checks a page's language declarations and encoding. Free, fast, catches the basics.
- [W3C Internationalization Activity](https://www.w3.org/International/) — the hub for i18n techniques and articles.

**The rules that prevent most problems:**

- `hreflang` annotations must be **reciprocal**. If A points to B, B must point back to A. Non-reciprocal annotations are ignored, silently.
- Include a **self-referential** tag on every page.
- Use `x-default` for your fallback.
- **Subdirectories (`/de/`) are usually the right default** for a small company: they inherit domain authority and are far cheaper to operate than country domains.
- **Do not auto-redirect by IP.** It breaks crawling and infuriates travellers and VPN users. Offer a banner instead.

---

## 27.3 Translation quality

Machine translation is now good enough to be a starting point for most European language pairs and
genuinely risky for others. The professional model is **MTPE** — machine translation plus human
post-editing — and it's the right default: cheaper than human-from-scratch, far better than raw
output.

**Never machine-translate without review:** legal terms, pricing, security claims, error messages,
or anything where a mistranslation creates liability.

- [ISO 18587](https://www.iso.org/standard/62970.html) — the standard for post-editing of machine translation output. Useful mainly for knowing what to ask a vendor for.
- [MQM (Multidimensional Quality Metrics)](https://themqm.org/) — the open framework for scoring translation quality by error type, rather than by vibes.
- [COMET](https://github.com/Unbabel/COMET) — neural framework for automatic MT evaluation; the current state of the art for scoring output quality.
- [FLORES](https://github.com/facebookresearch/flores) — evaluation benchmark spanning many low-resource languages. Useful for calibrating how much you should trust MT for a given pair.
- [Argos Translate](https://github.com/argosopentech/argos-translate) — offline, open-source translation. Relevant when you can't send content to a third party.

---

## 27.4 The engineering

Get the data layer right and everything else is easier. Get it wrong and you'll rebuild.

- [Unicode CLDR](https://cldr.unicode.org/) — the Common Locale Data Repository: the underlying data for dates, times, numbers, currencies and plural rules in essentially every platform. [Source repo here](https://github.com/unicode-org/cldr).
- [ICU4X](https://github.com/unicode-org/icu4x) — modular, memory-safe Unicode and i18n components. The modern choice where you control the stack.
- [MessageFormat Working Group](https://github.com/unicode-org/message-format-wg) — the standards work on message formatting. Relevant because plural and gender handling is where naive i18n breaks first.
- [Fluent](https://github.com/projectfluent/fluent) — Mozilla's localisation system, designed around the reality that translations aren't one-to-one string swaps. Conceptually the strongest model here.
- [i18next](https://github.com/i18next/i18next) — the most widely deployed JS i18n framework, with the largest ecosystem.
- [FormatJS](https://github.com/formatjs/formatjs) — React Intl and ICU MessageFormat done properly.
- [Lingui](https://github.com/lingui/js-lingui) — compile-time message extraction with a small runtime.
- [next-intl](https://github.com/amannn/next-intl) — i18n for Next.js including locale-aware routing.

**Translation management**, all open source and self-hostable:

- [Weblate](https://github.com/WeblateOrg/weblate) — continuous localisation with git integration. The strongest general choice.
- [Pontoon](https://github.com/mozilla/pontoon) — Mozilla's own system, battle-tested at scale with volunteer communities.
- [Tolgee](https://github.com/tolgee/tolgee-platform) — includes in-context editing, which materially improves translation quality because translators can see where the string lands.

---

## 27.5 Pricing and payments

Frequently a larger lever than translation, and almost always cheaper to implement.

- **Local payment methods matter more than local language** in many markets. A German buyer who can't use SEPA or a Dutch buyer without iDEAL simply doesn't convert, regardless of what language your page is in.
- **Purchasing power parity pricing** — charging less in lower-income markets — expands your reachable market but creates arbitrage risk. Enforce it with something (billing address, card country), accept some leakage, and decide in advance whether you care.
- **Display prices in local currency** even if you settle in one. The mental-conversion tax is a real conversion cost.
- **Know your tax obligations before you sell.** Digital services tax and VAT rules bite quickly, and merchant-of-record providers exist precisely because this is genuinely hard.

- [World Bank International Comparison Program](https://www.worldbank.org/en/programs/icp) — the authoritative source for purchasing power parity data if you want to set PPP tiers on something defensible.
- [The Economist's Big Mac Index data](https://github.com/TheEconomist/big-mac-data) — the actual open dataset. A rough but transparent PPP proxy, and easier to explain internally than ICP.
- [Stripe payment method support by country](https://docs.stripe.com/payments/payment-methods/payment-method-support) — the clearest public reference for which methods matter where.
- [EU VAT One Stop Shop](https://taxation-customs.ec.europa.eu/) — the EU's own tax portal.

---

## 27.6 Cultural and channel differences

The channel map in [chapter 8](08-communities-and-social.md) is US and Europe centric, and that
matters. Some things that consistently surprise teams expanding:

- **Messaging apps are primary business channels** in much of Asia and Latin America in a way they are not in the US.
- **Search engine share varies**: assuming Google everywhere is wrong in several large markets.
- **Directness norms differ sharply.** Copy that reads as confident in the US can read as arrogant elsewhere, and vice versa.
- **Formality in address** — the formal/informal pronoun distinction in many languages is a positioning decision you must make explicitly, not a translation detail.

- [The Culture Map](https://erinmeyer.com/books/the-culture-map/) — Erin Meyer. The standard reference on cross-cultural business communication, and genuinely useful rather than a listicle of stereotypes.
- [Nielsen Norman Group on international users](https://www.nngroup.com/topic/international-users/) — research-based, and unusually free of hand-waving.

**On the widely quoted "can't read, won't buy" statistic** about people preferring to buy in their
own language: it comes from a commercial research firm's own survey. The direction is almost
certainly right; treat the specific percentage as marketing rather than fact, and don't build a
business case on the number alone.

---

## 27.7 If you only do five things

1. Look at which countries already over-index in your signups. Start there, not where you'd like to be.
2. Add the local payment methods for your top non-domestic market before translating anything.
3. If you do use `hreflang`, make every annotation reciprocal and self-referential, then validate it.
4. Never auto-redirect by IP.
5. Use MT plus human post-editing, and keep humans on anything legal, priced or security-related.

---

**Related:** [SEO and AI search](04-seo-and-ai-search.md) · [Pricing and business model](13-pricing-and-business-model.md) · [Communities and social](08-communities-and-social.md)

*Last reviewed July 2026. Not tax or legal advice. Corrections welcome — see
[CONTRIBUTING.md](../CONTRIBUTING.md).*
