# 22. Brand, Naming and Visual Identity

> Engineers undervalue design because they've watched people spend money on logos instead of
> products. That instinct is half right. The half that's wrong is expensive: a name you have to
> abandon, and a site that looks untrustworthy to the people you most want to trust you.

---

## 22.1 What a brand actually is

A brand is not your logo. It is the expectation someone has before they use your product, and it
is owned by them, not by you. You influence it through everything you ship — including your error
messages, your changelog and how you answer issues.

For technical products this is good news, because the things that build it are things you're
already good at: consistency, clarity, and not lying.

- [Taste for Makers](https://www.paulgraham.com/taste.html) — Paul Graham's argument that taste is real, learnable and not decoration. The essay to read if design feels like superstition.

---

## 22.2 Choosing a name that survives

Naming failures are among the most expensive avoidable mistakes in a technical product, because
by the time you notice, the name is in package registries, import statements and other people's
code.

**Run all of these checks before you commit:**

1. **Package registry availability**, in every ecosystem you might ship to. This is the check people skip and regret. Registries differ in ways that matter: crates.io is a single flat first-come namespace, npm actively rejects names too similar to existing ones, PyPI normalises names so `Foo.Bar` and `foo-bar` collide, and in Go and Maven your *domain* is effectively your namespace.
2. **Trademark search** — see 22.3.
3. **Domain**, ideally `.com`. Alternative TLDs are fine but you will spend the rest of the product's life spelling it out.
4. **Search results.** If your name collides with something popular, you're buying a permanent SEO disadvantage.
5. **Say it out loud.** On a call, in a noisy room, to someone who doesn't share your first language.

- [npm package name guidelines](https://docs.npmjs.com/package-name-guidelines) and [npm disputes policy](https://docs.npmjs.com/policies/disputes) — including what actually happens when your trademark collides with a squatted package.
- [PyPA name normalization](https://packaging.python.org/en/latest/specifications/name-normalization/) — why apparently different names collide.
- [Cargo publishing reference](https://doc.rust-lang.org/cargo/reference/publishing.html) — crates.io's first-come flat namespace.
- [Go modules reference](https://go.dev/ref/mod) — module paths are URLs, so your domain choice is your namespace choice.
- [ICANN UDRP](https://www.icann.org/resources/pages/udrp-2012-02-25-en) — the mechanism for recovering a domain registered in bad faith against your trademark.

---

## 22.3 Trademark search, practically

**Not legal advice.** But a first-pass search is free, takes an hour, and catches most disasters.

- [USPTO Trademark Search](https://tmsearch.uspto.gov/) — the current US public search system. **Note:** this replaced TESS, so any guide telling you to use TESS is out of date.
- [USPTO Trademark basics](https://www.uspto.gov/trademarks/basics) — the official plain-language explainer.
- [TMview](https://www.tmdn.org/tmview/) — aggregated search across EUIPO, national EU offices, the USPTO and many others in one query. The best single first-pass tool.
- [WIPO Global Brand Database](https://branddb.wipo.int/) — free search across international registrations.
- [Nice Classification](https://www.wipo.int/classifications/nice/en/) — the 45-class system everything above is organised by. You need to know your class to search meaningfully.
- [USPTO: caution on misleading notices](https://www.uspto.gov/trademarks/protect/caution-misleading-notices) — after you file you *will* receive official-looking invoices from private companies. They are not from the USPTO. Read this before you pay one.

---

## 22.4 A minimal credible identity

You do not need a brand agency. You need to not look untrustworthy. That is achievable in a day
with constraints rather than creativity:

- **One typeface, two weights.** [Practical Typography](https://practicaltypography.com/) is a free, complete book on this and its "typography in ten minutes" section covers most of what matters.
- **A restrained palette.** One brand colour, one accent, a neutral ramp. More colours means more decisions and more inconsistency.
- **One consistent spacing scale.** This single choice does more for perceived quality than any logo.
- **One diagram style.** [Excalidraw](https://excalidraw.com/) is popular in developer marketing precisely because it produces a consistent house style with no effort.
- **Adequate contrast.** [WCAG 2.2](https://www.w3.org/TR/WCAG22/) is the actual standard, and in some jurisdictions a legal requirement — see [chapter 26](26-performance-and-accessibility.md).

**Steal structure from published design systems.** These are free, documented, and built by teams
with research budgets:

- [U.S. Web Design System](https://designsystem.digital.gov/) — public domain, accessibility-first, exceptionally well documented. The best free starting point.
- [GOV.UK Design System](https://design-system.service.gov.uk/) — publishes the user research behind each component, which is rare and instructive.
- [Primer](https://primer.style/) — GitHub's system; the most directly relevant if your audience is developers.
- [awesome-design-systems](https://github.com/alexpate/awesome-design-systems) — the large index of public systems.

**For implementation:** [Tailwind CSS](https://tailwindcss.com/) is valuable to a non-designer
mainly because its default scales are already coherent; [shadcn/ui](https://ui.shadcn.com/) gives
you components you own rather than a dependency; [Radix Primitives](https://www.radix-ui.com/primitives)
gives accessible behaviour without imposing a look.

**Fonts and icons:** [Google Fonts](https://fonts.google.com/) — self-host rather than hotlink,
which is faster and avoids a third-party request you'd have to disclose in a cookie banner. Read
the [SIL Open Font License](https://openfontlicense.org/) before embedding anything.
[Lucide](https://lucide.dev/), [Phosphor](https://phosphoricons.com/) and
[Heroicons](https://heroicons.com/) are all open and coherent — pick one and don't mix.

---

## 22.5 Designer or template?

**Use a template when** you're pre-revenue, the product is still moving, and your differentiation
is technical. A good template executed consistently beats a bespoke identity executed badly, which
is what a cheap designer produces.

**Hire a designer when** you have a repeatable sale and the visual gap is costing you credibility
with a buyer who isn't technical, or when you need a system rather than a picture. Ask for the
system — type scale, spacing, components, usage rules — not just a logo file.

**Red flags:** a logo with no accompanying usage guidance, a designer who won't show you the
reasoning, and anyone who starts with mood boards before asking who your customers are.

- [AIGA](https://www.aiga.org/) — the US professional design association; publishes standard-form client agreements and scoping guidance, useful if you've never contracted a designer.

---

## 22.6 If you only do five things

1. Check package registry availability in every ecosystem before you commit to a name.
2. Run a free TMview search in your Nice class.
3. Pick one typeface, one brand colour and one spacing scale, then never deviate.
4. Steal structure from USWDS or GOV.UK rather than inventing it.
5. Ignore any invoice that arrives after a trademark filing until you have verified who sent it.

---

**Related:** [Positioning and audience](01-positioning-and-audience.md) · [Landing pages and conversion](18-landing-pages-and-conversion.md) · [Performance and accessibility](26-performance-and-accessibility.md)

*Last reviewed July 2026. Not legal advice. Corrections welcome — see [CONTRIBUTING.md](../CONTRIBUTING.md).*
