# PlateSync Brand Assets — Checklist

## Required Assets

### Favicon
- [ ] `favicon.svg` — SVG mark, works at 32x32. Currently a placeholder "P" on emerald background.
- [ ] `favicon-192.png` — 192x192 PNG for Android/PWA
- [ ] `favicon-512.png` — 512x512 PNG for PWA splash
- [ ] `apple-touch-icon.png` — 180x180 PNG for iOS

### Logo
- [ ] `logo-full.svg` — Full logo (mark + wordmark "PlateSync"), horizontal layout
- [ ] `logo-mark.svg` — Icon/mark only (for nav, small spaces)
- [ ] `logo-white.svg` — White version for dark/emerald backgrounds (CTA section, footer if dark)

### Open Graph / Social
- [ ] `og-image.jpg` — 1200x630px, used for link previews on social media, Slack, etc. Should include: logo, tagline, app screenshot or illustration. Referenced in base.njk `<meta property="og:image">`.

### App Screenshots (for homepage)
- [ ] Desktop screenshot — meal plan view or cooking mode
- [ ] Mobile screenshot — cooking mode on phone (the hero use case)
- [ ] Optional: family setup, recipe picker, shopping list

## Brand Specs

| Property | Value |
|---|---|
| Primary colour | `#059669` (emerald-600) |
| Primary dark | `#047857` (emerald-700) |
| Primary light | `#ecfdf5` (emerald-50) |
| Body font | DM Sans |
| Accent font | DM Mono |
| Background | White (#ffffff) |
| Text | Neutral-900 (#171717) |

## Where Assets Are Used

| Asset | Location |
|---|---|
| `favicon.svg` | `src/assets/favicon.svg` → copied to site root |
| `og-image.jpg` | `src/assets/images/og-image.jpg` → referenced in base.njk |
| `logo-full.svg` | Nav bar (nav.njk) — replaces the current text "PlateSync" |
| `logo-mark.svg` | Mobile nav, favicon alternative |
| Screenshots | Homepage feature sections, hero area |

## Notes

- All images should be optimised (SVG for logos, WebP/AVIF for screenshots, JPEG for OG image)
- Logo should work on both white and emerald backgrounds
- OG image is critical — it's what people see when the link is shared on social/Slack/WhatsApp
- The app (platesync) also needs the favicon updated — currently using a Lucide utensils icon at `public/favicon.svg`
