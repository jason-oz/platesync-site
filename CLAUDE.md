# PlateSync Marketing Site — Project Instructions

## Overview

Marketing/landing site for PlateSync (the family meal planning app at app.getplatesync.com). Static site built with Eleventy + Tailwind CSS, deployed to Vercel. Domain: **getplatesync.com**.

## Tech Stack

- **Framework:** Eleventy (11ty) v3
- **Styling:** Tailwind CSS v4 (via @tailwindcss/cli)
- **Templating:** Nunjucks (.njk) for layouts, Markdown for content pages
- **Fonts:** DM Sans (body), DM Mono (accent labels)
- **Hosting:** Vercel
- **Brand colour:** Emerald-600 (#059669) as primary

## Commands

```bash
npm run dev    # Dev server (Eleventy --serve + Tailwind --watch)
npm run build  # Production build (Eleventy + Tailwind minified)
```

## File Structure

```
src/
  _data/site.js          # Site name, URL, description, author
  _includes/
    base.njk             # HTML shell — meta, schema, fonts, nav+footer includes
    legal.njk            # Layout for privacy/terms pages
    partials/
      nav.njk            # Sticky header nav
      footer.njk         # Footer with links and ABN
  assets/
    css/main.css         # Tailwind entry point + brand font overrides
    images/              # OG image, screenshots (TODO)
    fonts/               # Custom fonts if needed
    favicon.svg          # Placeholder favicon
  index.njk              # Homepage — hero, problem, how it works, features, FAQ, CTA
  privacy.md             # Privacy policy
  terms.md               # Terms of service
  404.njk                # 404 page
  robots.txt             # Robots directive + sitemap reference
  sitemap.njk            # Auto-generated XML sitemap
  llms.txt               # Short LLM-readable product summary
  llms-full.txt          # Full LLM-readable documentation
```

## Related Projects

- **PlateSync app:** `C:\Users\jason\Claude Dev Projects\platesync` — the React app
- **Marketing assets:** `C:\Users\jason\Claude Dev Projects\platesync\marketing\` — explainer, outreach, FAQ
- **Features guide:** `C:\Users\jason\Claude Dev Projects\platesync\documentation\features-guide.md`

## TODO

- [ ] Replace placeholder favicon with proper brand mark
- [ ] Add OG image (screenshot or designed graphic)
- [ ] Add app screenshots to homepage
- [ ] Set up Vercel project and connect getplatesync.com domain
- [ ] Add Google Analytics tag
- [ ] Pricing section (once pricing is decided)
