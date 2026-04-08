# DESIGN.md — PlateSync

## Overview

A clean, confident, health-focused marketing site for a family meal planning app. The design should feel trustworthy and approachable — like a well-organised kitchen, not a hospital. Generous whitespace, clear hierarchy, and an emphasis on readability. The interface communicates competence without being clinical.

**Aesthetic keywords:** clean, spacious, confident, health-focused, modern
**Target feel:** "A trusted tool that makes your life easier — not another thing to learn"

---

## Colors

### Brand

| Token | Hex | Role |
|---|---|---|
| `primary` | `#059669` | Main brand colour (emerald-600). CTAs, links, active states, section eyebrow labels, icon accents. |
| `primary-foreground` | `#ffffff` | Text and icons on primary backgrounds. |
| `primary-hover` | `#047857` | Hover state for primary buttons (emerald-700). |
| `primary-light` | `#ecfdf5` | Light tint for subtle backgrounds, badges (emerald-50). |

### Neutrals

| Token | Hex | Role |
|---|---|---|
| `background` | `#ffffff` | Page background. Primary content sections. |
| `foreground` | `#171717` | Primary text colour (neutral-900). Headlines, strong labels. |
| `muted` | `#fafafa` | Alternating section backgrounds, card fills (neutral-50). |
| `muted-foreground` | `#525252` | Secondary text, descriptions, body copy (neutral-600). |
| `subtle` | `#a3a3a3` | Tertiary text, footer, timestamps (neutral-400). |
| `border` | `#e5e5e5` | Card borders, section dividers, input borders (neutral-200). |

### Status / Feedback

| Token | Hex | Role |
|---|---|---|
| `success` | `#16a34a` | Positive states, confirmations (green-600). |
| `warning` | `#d97706` | Caution states, expiring items (amber-600). |
| `error` | `#dc2626` | Errors, destructive actions (red-600). |
| `info` | `#2563eb` | Informational highlights, tips (blue-600). |

---

## Typography

### Font Stack

| Role | Font | Fallback | Source |
|---|---|---|---|
| Body / UI | DM Sans | system-ui, sans-serif | Google Fonts |
| Headings | DM Sans | system-ui, sans-serif | Google Fonts (same family, heavier weights) |
| Mono / Labels | DM Mono | monospace | Google Fonts |

### Scale

| Level | Size | Weight | Line Height | Tracking | Usage |
|---|---|---|---|---|---|
| Display | 3.5rem (56px) | 800 | 1.1 | -0.02em | Hero headline only |
| H1 | 2.5rem (40px) | 700 | 1.2 | -0.01em | Page titles |
| H2 | 1.875rem (30px) | 700 | 1.3 | -0.01em | Section headings |
| H3 | 1.125rem (18px) | 600 | 1.4 | 0 | Card titles, feature names |
| Body | 1rem (16px) | 400 | 1.6 | 0 | Paragraphs, descriptions |
| Small | 0.875rem (14px) | 400 | 1.5 | 0 | Captions, helper text |
| Label | 0.75rem (12px) | 500 | 1.3 | 0.05em | Section eyebrows, badges (uppercase) |

### Patterns

- **Section eyebrow:** DM Mono, uppercase, tracking-widest, 12px, emerald-600. Appears above every section heading.
- **Hero heading:** Display size, font-extrabold (800), tight tracking, neutral-900. Max-width constrained for readability.
- **Section heading:** H2 size, font-bold (700). May highlight one word in emerald-600 via `<span>`.
- **Card title:** H3 size, font-bold (700), neutral-900.
- **Body text:** 16px, regular weight, neutral-600, relaxed leading (1.6).
- **Caption/footer:** 14px or 12px, neutral-400.

---

## Components

### Buttons

| Variant | Background | Text | Border | Radius | Padding | Hover |
|---|---|---|---|---|---|---|
| Primary CTA | `#059669` | white | none | 0.5rem (8px) | px-6 py-3 | bg emerald-700, optional subtle glow shadow |
| Secondary | transparent | neutral-600 | 1px neutral-200 | 0.5rem | px-6 py-3 | bg neutral-50 |
| Ghost/link | transparent | neutral-600 | none | 0.5rem | px-4 py-2 | text neutral-900 |
| CTA (inverted) | white | emerald-700 | none | 0.5rem | px-6 py-3 | bg emerald-50 (used on emerald backgrounds) |

All buttons: `transition-colors` with 150ms duration. Font-semibold (600). Minimum height 44px for touch targets.

### Cards

| Property | Value |
|---|---|
| Background | white |
| Border | 1px `#e5e5e5` (neutral-200) |
| Radius | 0.75rem (12px) |
| Padding | 1.25rem (20px) |
| Shadow | None (border-only design) |
| Hover | Optional subtle shadow or primary-tinted border |

### Inputs

| Property | Value |
|---|---|
| Height | 2.75rem (44px) minimum |
| Border | 1px neutral-200 |
| Radius | 0.5rem (8px) |
| Padding | 0.75rem horizontal |
| Focus | Emerald-600 border, subtle emerald ring |
| Background | white |

---

## Elevation

| Level | Usage | Implementation |
|---|---|---|
| None | Cards, content sections | Border contrast only (1px neutral-200) |
| Subtle | Hover states | `shadow-sm` or slightly more visible border |
| Medium | Sticky nav | `shadow-sm` + `backdrop-blur-sm` + `bg-white/90` |
| Strong | Modals, toasts (if added later) | `shadow-xl` + backdrop overlay |

---

## Spacing & Layout

| Token | Value | Usage |
|---|---|---|
| Section padding | `py-20 md:py-24` | Vertical space between major page sections |
| Container | `max-w-6xl mx-auto px-6` | Standard content width (1152px) |
| Narrow container | `max-w-4xl` | How It Works, problem sections |
| Text container | `max-w-3xl` | Legal pages, FAQ, hero subtitle |
| Card grid | `grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6` | Feature cards |
| 2-col grid | `grid-cols-1 md:grid-cols-2 gap-8` | How It Works steps |
| Section internal | `gap-12` (mb-12) | Between section heading block and content |

---

## Do's and Don'ts

### Do

- Use emerald-600 only for actionable elements: CTAs, links, eyebrow labels, icon accents
- Maintain WCAG AA contrast (4.5:1 for body text, 3:1 for large headings)
- Use the section pattern consistently: eyebrow label (mono, uppercase, emerald) → heading (bold, neutral-900) → body (neutral-600)
- Keep sections alternating white / neutral-50 backgrounds for visual rhythm
- Use generous whitespace — py-20+ between sections, gap-6+ between cards
- Keep all border-radius consistent: 8px for buttons/inputs, 12px for cards

### Don't

- Don't use emerald-600 for decorative backgrounds or large surface fills (except the final CTA section)
- Don't mix rounded and sharp corners — everything is rounded in this design
- Don't use more than two font weights on a single screen (regular + bold is the default pair)
- Don't put text smaller than 12px anywhere
- Don't skip the eyebrow label on section headings — it creates the visual rhythm that ties the page together
- Don't use shadows on cards — this is a border-only design (shadows reserved for nav and overlays)
