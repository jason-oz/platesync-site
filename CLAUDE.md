# PlateSync Marketing Site — Project Instructions

## Overview

Marketing/landing site for **PlateSync** — a family meal planning web app that calculates per-person portions based on each family member's health profile, generates smart shopping lists, and provides a mobile cooking guide. The app lives at **https://app.getplatesync.com**.

This is the public-facing marketing site. Domain: **https://getplatesync.com** (not yet connected).

## Tech Stack

| Layer | Technology |
|---|---|
| Framework | Eleventy (11ty) v3 — static HTML, zero client JS by default |
| Styling | Tailwind CSS v4 (via @tailwindcss/cli, not PostCSS) |
| Templating | Nunjucks (.njk) for layouts and partials, Markdown for content pages |
| Fonts | DM Sans (body, Google Fonts), DM Mono (accent labels, Google Fonts) |
| Hosting | Vercel |
| Version control | GitHub (repo TBD) |

## Commands

```bash
npm run dev    # Dev server (Eleventy --serve + Tailwind --watch via concurrently)
npm run build  # Production build (Eleventy then Tailwind --minify)
```

## Brand & Design

**Primary colour:** Emerald-600 (`#059669`) — used for CTAs, links, accents, section labels
**Background:** White (`bg-white`) for content sections, Neutral-50 (`bg-neutral-50`) for alternating sections
**Text:** Neutral-900 for headings, Neutral-600 for body, Neutral-400 for subtle/footer text
**Border:** Neutral-200 for card borders and section dividers

**Typography:**
- Body: DM Sans, 400/500/600/700/800 weights
- Accent labels (section eyebrows): DM Mono, uppercase, tracking-widest, text-xs, text-emerald-600
- Headings: DM Sans, font-extrabold for hero, font-bold for section heads

**Design principles:**
- Clean, modern, generous whitespace
- Mobile-first responsive (Tailwind breakpoints: `sm:`, `md:`, `lg:`)
- No animations or JS unless absolutely required
- Card-based feature layout with subtle borders
- Sticky nav with backdrop blur
- Sections alternate white / neutral-50 backgrounds

**This is NOT the HCD brand.** PlateSync has its own identity — emerald green, clean, health-focused. Do not apply HCD's dark premium styling.

## File Structure

```
src/
  _data/
    site.js                # Global site data: name, url, appUrl, description, author, abn
  _includes/
    base.njk               # HTML shell — meta, OG, schema, fonts, speculation rules, nav+footer
    legal.njk              # Layout for privacy/terms (wraps content in prose container)
    partials/
      nav.njk              # Sticky header: logo, section links, "Get Started" CTA
      footer.njk           # 3-column footer: product links, legal links, credits + ABN
  assets/
    css/main.css           # Tailwind @import + DM Sans/Mono font-family overrides
    images/                # OG image, app screenshots (TODO — currently empty)
    fonts/                 # Local font files if needed (currently using Google Fonts CDN)
    favicon.svg            # Placeholder emerald "P" favicon
  index.njk                # Homepage — 6 sections: hero, problem, how it works, features, FAQ, CTA
  privacy.md               # Privacy policy (Markdown, legal.njk layout)
  terms.md                 # Terms of service (Markdown, legal.njk layout)
  404.njk                  # 404 page
  robots.txt               # Allows all, references sitemap
  sitemap.njk              # Auto-generated XML sitemap from collections.all
  llms.txt                 # Short LLM-readable summary (GEO)
  llms-full.txt            # Full LLM-readable documentation (GEO)

eleventy.config.js         # Eleventy config — passthrough copies, isoDate filter, Nunjucks options
vercel.json                # Vercel build config, security headers, cache rules
package.json               # Dependencies: @11ty/eleventy, tailwindcss, @tailwindcss/cli, concurrently
```

## Homepage Sections (index.njk)

1. **Hero** — Eyebrow label + H1 headline + subtitle + "Get Started Free" CTA + "See how it works" anchor
2. **Problem** — Short empathy section describing the family meal planning pain
3. **How It Works** — 6-step numbered grid (setup → recipes → plan → shop → cook → leftovers)
4. **Features** — 9 feature cards in a 3-column grid
5. **FAQ** — 6 common questions with direct answers
6. **CTA** — Emerald background, headline + "Get Started Free" button

## SEO / AEO / GEO

All pages must follow the standards from the global CLAUDE.md:

- Unique `<title>` and `<meta description>` per page (set via front matter)
- One `h1` per page, logical heading hierarchy
- JSON-LD schema in base.njk: `Organization`, `WebSite`, `SoftwareApplication`
- Open Graph + Twitter Card meta tags
- XML sitemap auto-generated
- `robots.txt` with sitemap reference
- `llms.txt` and `llms-full.txt` for LLM crawlers (GEO)
- Canonical URLs via `<link rel="canonical">`
- Speculation rules for prefetch/prerender (instant page transitions in Chrome)
- Direct-answer lead sentences in FAQ for AEO snippet targeting

## Schema Markup

**base.njk** includes:
- `Organization` — PlateSync, linked to High Country Digital
- `WebSite` — site URL, name, description
- `SoftwareApplication` — category HealthApplication

**Homepage should add** (TODO):
- `FAQPage` schema wrapping the FAQ section
- `HowTo` schema wrapping the "How It Works" steps

## Coding Conventions

- Nunjucks for all layouts and reusable partials (`_includes/`)
- Markdown for content pages (privacy, terms) with front matter
- Tailwind utility classes only — no custom CSS unless unavoidable
- Clean semantic HTML — no div soup
- Mobile-first, no inline styles
- Keep layouts under 100 lines — extract partials if longer
- Comment only when the *why* is non-obvious
- Section IDs for anchor links: `id="features"`, `id="how-it-works"`, `id="faq"`

## Related Projects

| Project | Path | What |
|---|---|---|
| PlateSync app | `C:\Users\jason\Claude Dev Projects\platesync` | React SPA — the actual product |
| PlateSync app CLAUDE.md | `C:\Users\jason\Claude Dev Projects\platesync\CLAUDE.md` | Full app architecture docs |
| Marketing assets | `C:\Users\jason\Claude Dev Projects\platesync\marketing\` | explainer.md, outreach.md, faq.md |
| Features guide | `C:\Users\jason\Claude Dev Projects\platesync\documentation\features-guide.md` | Full feature breakdown for copy |
| Pricing doc | `C:\Users\jason\Claude Dev Projects\platesync\documentation\pricing-and-gating.md` | Pricing placeholder + questions |
| WebMap site (template) | `C:\Users\jason\Claude Dev Projects\WebMap-site` | Reference for structure and patterns |

## Product Context (for writing copy)

**What PlateSync does:**
- Builds weekly meal plans with per-person portions based on health profiles
- Calculates nutrition using Mifflin-St Jeor BMR + protein targets (0.9–2.2 g/kg)
- Adjusts targets per day based on training schedule (rest/light/training/intense)
- Cooks the full recipe — portions are capped to serving count, never fractional
- Tracks leftovers (fridge/freeze/discard) and offers them for future meals
- Generates shopping lists with full-batch ingredient amounts minus pantry stock
- Provides mobile cooking mode with checkable ingredients and step-by-step instructions
- Detects allergens across family members
- Supports household sharing (multiple users, one household)

**Who it's for:**
- Families with 2+ people eating together
- Parents managing different nutritional needs (adults training, kids growing, dietary restrictions)
- Anyone tracking protein/macros who's tired of calculating portions manually
- Households that waste food from over-buying or forgotten ingredients

**What it is NOT:**
- Not a diet app or calorie counter
- Not for individual meal preppers (it's family-focused)
- Not a recipe blog — it's a planning tool

**Tone:** Clean, confident, outcome-focused. Approachable but not cutesy. Similar to Thryvia's tone — "a mate telling you about something that'll save you time." Never lead with AI. Sell outcomes: right portions, less waste, easier cooking nights.

**Banned words:** "game-changer," "revolutionary," "cutting-edge," "seamlessly," "leverage," "AI-powered" as a headline.

## TODO

- [ ] Replace placeholder favicon with proper brand mark
- [ ] Add OG image (screenshot or designed graphic)
- [ ] Add app screenshots to feature sections
- [x] Create GitHub repo and push
- [ ] Set up Vercel project and connect getplatesync.com domain
- [x] Add Google Analytics tag (G-ZMSHM5NXH0) — conversion events not yet configured
- [x] Add FAQPage + HowTo JSON-LD schema to homepage
- [ ] Pricing section (once pricing model is decided)
- [ ] Add testimonials/social proof section (once beta feedback comes in)
- [ ] Consider adding a /features page for deeper feature breakdowns
