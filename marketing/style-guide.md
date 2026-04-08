# PlateSync — Brand Style Guide

---

## Brand Identity

**Product name:** PlateSync
**URL:** https://getplatesync.com
**App URL:** https://app.getplatesync.com
**Built by:** High Country Digital (Jason Townsend)
**Tagline:** Everyone at the table gets exactly what they need
**One-liner:** The AI does the maths. You do the cooking.
**Positioning:** A meal planning tool for families who want to eat well, waste less food, and stop guessing at portions every night. Not a diet app. Not a calorie counter. A practical planning tool that happens to be very good at maths.

**Brand voice:**
- **Direct** — Say it plainly. No hedging, no jargon, no AI hype.
- **Confident** — Know what the product does and say it. Avoid "we aim to" and "we try to".
- **Relatable** — Write like a mate explaining something useful, not a brand talking at a customer.
- **Outcome-focused** — Lead with what the user gets, not what the feature does.

**Words and phrases to avoid:**
- "game-changer", "revolutionary", "cutting-edge", "seamlessly", "leverage"
- "AI-powered" as a headline or main selling point
- "diet app", "calorie counter" (positioning away from these)
- "we aim to", "we try to", "we hope to"
- Anything that treats the user as though they can't cook or don't know their own family

**Words and phrases to use:**
- "portions", "per person", "family", "household"
- "exactly what they need", "right amount"
- "plan", "shop", "cook", "leftovers"
- "waste less", "buy less", "no guessing"

---

## Logo

**Logo files:** `src/assets/brand/`

| File | Description |
|---|---|
| `logo-full.svg` | Mark + wordmark "PlateSync" — default for nav and footer |
| `logo-mark.svg` | Icon only (48×48px) — favicon, small spaces |
| `logo-white.svg` | Full logo reversed for dark/emerald backgrounds |
| `favicon.svg` | 32×32px mark — site favicon |

**Wordmark style:** "Plate" in neutral-900, "Sync" in emerald-600.

### Logo usage by context

| Context | File | Size |
|---|---|---|
| Nav / header | `logo-full.svg` | h-8 (32px height, width auto) |
| Footer | `logo-full.svg` | h-7 (28px height, width auto) |
| Emerald CTA section | `logo-white.svg` | h-8 |
| Favicon | `favicon.svg` | 32×32px |

### Logo rules

- Never stretch, recolour, or add effects to the logo
- Always use `logo-white.svg` on dark or emerald backgrounds — never the dark version
- Maintain clear space of at least the height of the mark on all sides
- Do not place the logo on busy photographic backgrounds

---

## Colours

*(See DESIGN.md for full token definitions and Tailwind implementation.)*

| Role | Hex | Brand meaning |
|---|---|---|
| Primary (emerald-600) | `#059669` | Action, energy, health. Used only for CTAs, links, active states, and eyebrow labels. Not for decoration. |
| Primary dark (emerald-700) | `#047857` | Hover states. Slightly richer, signals interactivity. |
| Primary light (emerald-50) | `#ecfdf5` | Subtle tint for badges and hover backgrounds. Not for large fills. |
| Background | `#ffffff` | Clean, open, airy. |
| Foreground | `#171717` | Near-black — avoids harshness of pure black. |
| Muted background | `#fafafa` | Section alternation — creates rhythm without hard breaks. |
| Body text | `#525252` | Readable, not competing with headings. |
| Subtle / footer | `#a3a3a3` | Tertiary information — credits, timestamps. |
| Border | `#e5e5e5` | Quiet structure. Cards and dividers. |

**Colour rule:** Emerald is used to direct attention, not to decorate. If in doubt, use neutral.

---

## Typography

*(See DESIGN.md for full scale and implementation.)*

| Role | Font | Why |
|---|---|---|
| Body / headings | DM Sans | Geometric sans — modern, clean, and approachable without being clinical |
| Accent / labels | DM Mono | Adds technical precision to section eyebrows, step numbers, and data labels |

**Section eyebrow pattern:** DM Mono · uppercase · tracking-widest · text-xs · emerald-600. Used above every section heading. Never skip it — it creates the visual rhythm that ties the page together.

---

## Tone of Voice

### Principles

1. **Sell outcomes, not features** — The user doesn't care that we use Mifflin-St Jeor. They care that everyone gets the right amount on their plate.
2. **Be specific** — "4-day fridge expiry" beats "short-term storage". Specific details build trust.
3. **Don't lead with AI** — AI is the engine, not the selling point. The outcome is the selling point.
4. **One idea per sentence** — Don't stack multiple claims. Let each point land.
5. **Relatable over polished** — "same five dinners on repeat" is better than "repetitive meal selection". Write how people talk.

### Writing patterns

- **Lead with the outcome:** "Only buy what you need" not "shopping list generation with pantry deduction"
- **Name the person:** "Dad needs 150g of protein" not "users have different nutritional requirements"
- **Use active voice:** "PlateSync calculates your portions" not "portions are calculated by PlateSync"
- **Short over long:** If it can be said in 8 words, don't use 14
- **Never hedge:** "Portions adjust based on your training schedule" not "portions may adjust based on your training schedule where applicable"

### Sample copy

**Hero headline (good):** Everyone at the table gets exactly what they need
**Hero headline (bad):** AI-powered personalised meal planning for the whole family

**Feature name (good):** Cooking mode — No ads, no life story. Just the recipe.
**Feature name (bad):** Intelligent recipe viewer with step-by-step guidance

**CTA (good):** Get Started Free
**CTA (bad):** Begin Your Meal Planning Journey

**Problem statement (good):** You're cooking one meal and somehow everyone needs a different plate — so you default to the same five dinners on repeat.
**Problem statement (bad):** Meal planning is challenging when family members have diverse nutritional requirements.

**FAQ answer (good):** Yes. After cooking, you choose what to do with surplus servings: keep in the fridge (4-day expiry), freeze (no expiry), or discard.
**FAQ answer (bad):** Our leftovers management system provides flexible options for handling surplus meal servings.

---

## Product Positioning

### What PlateSync is

- A weekly meal planner for families with different nutritional needs
- A shopping list generator that only includes what you actually need to buy
- A cooking guide designed for phone use in the kitchen
- A leftovers tracker that reduces food waste

### What PlateSync is NOT

- Not a diet app or calorie counter
- Not for individual meal preppers (it's family-focused)
- Not a recipe blog or recipe discovery platform
- Not a substitute for medical/dietary advice

### Who it's for

- Families with 2+ people eating together regularly
- Parents managing mixed needs — adults training, kids growing, dietary restrictions
- Anyone tracking protein or macros who's tired of calculating portions manually
- Households that waste food from over-buying or forgotten ingredients

### What makes it different

Most meal planners treat the whole family as one person. PlateSync calculates per-person portions based on each individual's age, weight, goals, and training schedule — then tells you exactly what to put on each plate. The AI does the maths; you do the cooking.

---

## Photography & Imagery

*(No images in place yet — placeholder guidance for when assets are available.)*

- **Style:** Real situations — a phone on a kitchen bench, ingredients on a chopping board, a family at a table. Not staged stock photography.
- **Mood:** Warm, practical, everyday. This is a Tuesday night dinner, not a Sunday brunch photoshoot.
- **App screenshots:** Prioritise cooking mode (phone in hand), meal plan calendar, and shopping list. These are the hero use cases.
- **What to avoid:** Perfect kitchens, model families, food styled for editorial. PlateSync is for real households.

---

## Do's and Don'ts (Brand)

**Do:**
- Use the full brand name "PlateSync" (one word, capital P and S) in all contexts
- Lead with the specific family scenario — name the people, name the problem
- Pair every feature claim with the concrete benefit: "Allergy detection — scanned automatically, so you don't have to check every ingredient"
- Mention "early access" / "free during beta" when referencing pricing — don't imply the product is permanently free
- Refer to the household as a "household" or "family" — not "team", "group", or "users"

**Don't:**
- Don't write "AI-powered" in headlines or feature names — the AI is the method, not the message
- Don't use vague superlatives: "best", "most powerful", "easiest"
- Don't reference specific competitors by name
- Don't promise medical outcomes — portions are estimates based on input data, not clinical advice
- Don't use "we" extensively — write from the product's perspective: "PlateSync calculates..." not "we calculate..."
