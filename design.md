# Design System — dr.gorska

## Color Palette

| Token | Hex | Usage |
|-------|-----|-------|
| `--color-primary` | `#53161D` | Burgundy — main accent, borders, highlights |
| `--color-deep` | `#30050E` | Dark background (hero, dark sections) |
| `--color-black` | `#1E100F` | Near-black — text on light backgrounds |
| `--color-cream` | `#FFFBF0` | Light background / text on dark |
| `--color-warm` | `#AA9F95` | Warm grey — secondary text, captions |
| `--color-light` | `#F5F0E8` | Light secondary background (alternating sections) |

Dark sections: `--color-deep` bg + `--color-cream` text  
Light sections: `--color-light` bg + `--color-black` text  
Accent always: `--color-primary` (#53161D)

---

## Typography

### Headlines / Display
- **Family:** Cormorant Garamond
- **Weights:** 300 (light), 400 (regular), 600 (semibold)
- **Style:** Italic for emotional phrases and key words
- **Size:** `clamp(3rem, 8vw, 7rem)` for hero; scale down proportionally per section
- **Line-height:** 1.05–1.1 for display, 1.3–1.4 for section titles

### Body / UI
- **Family:** Montserrat
- **Weights:** 300 (primary), 400 (emphasis only)
- **Size:** `clamp(0.9rem, 2vw, 1.1rem)` for body text
- **Line-height:** 1.6–1.8
- **Letter-spacing:** `0.02em` body, `0.2–0.25em` for uppercase labels

### Labels / Eyebrows
- Montserrat 300
- `font-size: 0.75rem`
- `letter-spacing: 0.25em`
- `text-transform: uppercase`
- Color: `--color-warm`

---

## Visual References

- **buly1803.com** — primary reference: dark, ornamental, antique luxury aesthetic
- **violetgrey.com** — editorial layout, long text strips, magazine feel

---

## Section Layout Rules

- Alternating dark / light sections — never all dark, never all light
- Minimum section padding: `80px 24px` (vertical / horizontal)
- Max content width: `1100px`, centered
- Generous whitespace — don't fill space, let it breathe
- Large oversized typography dominates; photography is full-width when used
- Ornamental dividers between sections: thin `1px` lines, vertical drops, or decorative glyphs

### Section Order
1. Hero — dark (`--color-deep`)
2. For Whom — light (`--color-light`)
3. What's Inside — dark (`--color-deep`)
4. About Author — light (`--color-light`)
5. Results / Testimonials — dark (`--color-deep`)
6. Pricing — light (`--color-light`)
7. FAQ — dark (`--color-deep`)

---

## Buttons

```css
/* Base button */
display: inline-block;
font-family: Montserrat, sans-serif;
font-weight: 300;
font-size: 0.75rem;
letter-spacing: 0.2em;
text-transform: uppercase;
text-decoration: none;
border: 1px solid var(--color-primary);
padding: 16px 48px;
border-radius: 0;           /* no rounding */
background: transparent;
color: var(--color-cream);
transition: background 0.3s ease, color 0.3s ease;

/* Hover */
background: var(--color-primary);
color: var(--color-cream);
```

Rules:
- NO rounded corners (`border-radius: 0` always)
- NO filled background on default state
- NO gradients, NO shadows
- Primary CTA: burgundy border on dark bg, fills burgundy on hover
- Secondary variant: `--color-warm` border for less prominent actions

---

## Spacing System

| Token | Value | Use |
|-------|-------|-----|
| `xs` | `8px` | Gap between inline elements |
| `sm` | `16px` | Internal component padding |
| `md` | `32px` | Between related elements |
| `lg` | `56px` | Between sections within a block |
| `xl` | `80px` | Section vertical padding |
| `2xl` | `120px` | Hero / large feature padding |

---

## What NOT to Use

- NO pink, pastel, or generic beauty-salon colors
- NO gradients
- NO neon
- NO rounded "bubble" buttons
- NO drop shadows on text
- NO decorative icons from icon packs (use text ornaments or CSS lines instead)
