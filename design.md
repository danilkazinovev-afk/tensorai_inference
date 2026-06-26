---
version: 1.0
name: TENSORAI-design-system
description: |
  A documentation-first marketing surface for an inference-reselling startup —
  paper-white canvas, near-black ink, and a tight neutral-gray ramp carrying all
  the prose. The page reads like a well-set README: one continuous white sheet,
  generous 88px air between sections, thin hairline borders, and zero shadows or
  gradients on structure. Personality is concentrated in three places only: a
  geometric Clash Display heading face, a single animated multi-color gradient on
  one hero word, and exactly one inverted dark surface (the bottom CTA strip).
  Buttons are squared (6px) while inputs and snippets stay fully pill-rounded; the
  type system pairs Clash Display (headings) with DM Sans (body + pricing numbers)
  and Space Mono (uppercase structural labels + code).

colors:
  primary: "#000000"
  on-primary: "#ffffff"
  ink: "#000000"
  ink-deep: "#090909"
  charcoal: "#525252"
  body: "#737373"
  mute: "#a3a3a3"
  canvas: "#ffffff"
  surface-soft: "#fafafa"
  surface-dark: "#171717"
  hairline: "#e5e5e5"
  hairline-strong: "#d4d4d4"
  on-dark: "#ffffff"
  on-dark-mute: "rgba(255,255,255,0.7)"
  focus-ring: "rgba(59,130,246,0.5)"
  term-red: "#ff5f56"
  term-yellow: "#ffbd2e"
  term-green: "#27c93f"
  gradient-blue: "#3B82F6"
  gradient-green: "#10B981"
  gradient-orange: "#F97316"
  gradient-pink: "#EC4899"

typography:
  display-xl:
    fontFamily: Clash Display
    fontSize: clamp(28px, 6vw, 36px)
    fontWeight: 700
    lineHeight: 1.12
    letterSpacing: -0.01em
  display-lg:
    fontFamily: Clash Display
    fontSize: clamp(24px, 4.5vw, 30px)
    fontWeight: 600
    lineHeight: 1.2
    letterSpacing: -0.01em
  heading-lg:
    fontFamily: Clash Display
    fontSize: 24px
    fontWeight: 600
    lineHeight: 1.33
    letterSpacing: -0.01em
  heading-md:
    fontFamily: Clash Display
    fontSize: 20px
    fontWeight: 600
    lineHeight: 1.4
  heading-sm:
    fontFamily: Clash Display
    fontSize: 18px
    fontWeight: 600
    lineHeight: 1.56
  body-md:
    fontFamily: DM Sans
    fontSize: 16px
    fontWeight: 400
    lineHeight: 1.5
  body-strong:
    fontFamily: DM Sans
    fontSize: 16px
    fontWeight: 500
    lineHeight: 1.5
  body-sm:
    fontFamily: DM Sans
    fontSize: 14px
    fontWeight: 400
    lineHeight: 1.43
  caption:
    fontFamily: DM Sans
    fontSize: 12px
    fontWeight: 400
    lineHeight: 1.33
  label:
    fontFamily: Space Mono
    fontSize: 12px
    fontWeight: 700
    lineHeight: 1.33
    letterSpacing: 0.06em
    textTransform: uppercase
  code-md:
    fontFamily: Space Mono
    fontSize: 16px
    fontWeight: 400
    lineHeight: 1.5
  code-sm:
    fontFamily: Space Mono
    fontSize: 14px
    fontWeight: 400
    lineHeight: 1.6
  button:
    fontFamily: DM Sans
    fontSize: 14px
    fontWeight: 500
    lineHeight: 1

rounded:
  sm: 6px
  md: 8px
  lg: 12px
  full: 9999px

spacing:
  xxs: 2px
  xs: 4px
  sm: 8px
  md: 12px
  lg: 16px
  xl: 24px
  xxl: 32px
  section: 88px

layout:
  container: { width: 86%, maxWidth: 1100px }
  container-wide: { width: 90%, maxWidth: 1240px }
  nav-height: 56px
  breakpoints: { stack: 850px, mobile-nav: 768px, phone: 640px }

components:
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.on-primary}"
    typography: "{typography.button}"
    rounded: "{rounded.sm}"
    padding: 8px 20px
    height: 36px
    activeBackground: "{colors.ink-deep}"
  button-secondary:
    backgroundColor: "{colors.canvas}"
    textColor: "{colors.ink}"
    border: 1px solid {colors.hairline-strong}
    typography: "{typography.button}"
    rounded: "{rounded.sm}"
    padding: 8px 20px
    height: 36px
    activeBorder: "{colors.ink}"
  button-on-dark:
    backgroundColor: "{colors.canvas}"
    textColor: "{colors.ink}"
    typography: "{typography.button}"
    rounded: "{rounded.sm}"
    padding: 8px 20px
    height: 36px
  search-pill:
    backgroundColor: "{colors.surface-soft}"
    textColor: "{colors.ink}"
    placeholderColor: "{colors.mute}"
    typography: "{typography.body-sm}"
    rounded: "{rounded.full}"
    padding: 8px 16px
    height: 36px
  install-snippet:
    backgroundColor: "{colors.surface-soft}"
    textColor: "{colors.ink}"
    typography: "{typography.code-md}"
    rounded: "{rounded.full}"
    padding: 12px 20px
    height: 48px
  command-tag:
    backgroundColor: "{colors.surface-soft}"
    textColor: "{colors.ink}"
    typography: "{typography.code-sm}"
    rounded: "{rounded.full}"
    padding: 6px 12px
  terminal-card:
    backgroundColor: "{colors.canvas}"
    border: 1px solid {colors.hairline}
    typography: "{typography.code-sm}"
    rounded: "{rounded.lg}"
    padding: 16px
  terminal-traffic-lights:
    rounded: "{rounded.full}"
    size: 12px
    gap: "{spacing.xs}"
  pricing-table:
    headerType: "{typography.label}"
    headerColor: "{colors.mute}"
    headerRule: 1px solid {colors.hairline-strong}
    rowRule: 1px solid {colors.hairline}
    numberType: DM Sans 500 tabular-nums
    rowPadding: 16px 0
  faq-row:
    backgroundColor: "{colors.canvas}"
    questionType: "{typography.heading-sm}"
    answerType: "{typography.body-md}"
    answerColor: "{colors.body}"
    border: 1px solid {colors.hairline} (bottom)
    padding: 16px 0
  cta-strip-dark:
    backgroundColor: "{colors.surface-dark}"
    textColor: "{colors.on-dark}"
    secondaryColor: "{colors.on-dark-mute}"
    typography: "{typography.heading-lg}"
    rounded: "{rounded.lg}"
    padding: 24px 32px
    cta: "{components.button-on-dark}"
  primary-nav:
    backgroundColor: "{colors.canvas}"
    border: 1px solid {colors.hairline} (bottom)
    height: 56px
    sticky: true
  mobile-menu:
    backgroundColor: "{colors.canvas}"
    border: 1px solid {colors.hairline} (bottom)
    itemType: "{typography.body-strong}"
    visibleBelow: 768px
  footer:
    backgroundColor: "{colors.canvas}"
    border: 1px solid {colors.hairline} (top)
    linkType: "{typography.label}"
    linkColor: "{colors.body}"
    padding: 32px 24px
  gradient-word:
    backgroundImage: linear-gradient(115deg, blue, green, orange, pink, blue)
    backgroundSize: 320% 320%
    clip: text
    animation: gradient-drift 9s ease-in-out infinite
    reducedMotion: animation none
---

## Overview

TENSORAI's landing page is built on a single design conviction: the page should
read like documentation, not a brochure. The whole surface is one continuous
sheet of `{colors.canvas}` (pure white) with no banded backgrounds, no hero
imagery, and no decorative dividers — sections are separated only by `{spacing.section}`
(88px) of plain air, the visual equivalent of a blank line in a Markdown source
file. The prose is carried almost entirely by a tight neutral-gray ramp
(`{colors.ink}` → `{colors.charcoal}` → `{colors.body}` → `{colors.mute}`), and
the only true color in the entire system is concentrated in a single animated word.

The system makes three deliberate, scarce "personality" investments and otherwise
stays studiously flat:

1. **A geometric display face.** Headings are set in Clash Display (600/700), whose
   rounded geometric forms give the page its only typographic character. Everything
   below heading size collapses into DM Sans, and every structural label collapses
   into uppercase Space Mono.
2. **One animated gradient word.** The word "easiest" in the hero headline carries
   a continuously looping blue→green→orange→pink gradient that drifts across a 2D
   field. It is the single moment of color in an otherwise black-on-white system.
3. **One inverted surface.** The dark `{colors.surface-dark}` CTA strip near the
   foot of the page is the only non-white surface and the only "look here" cue. It
   is used exactly once.

The shape language is split on purpose: **buttons are squared** to `{rounded.sm}`
(6px), while **inputs, snippets, and pills stay fully rounded** to `{rounded.full}`.
Cards and the dark strip use `{rounded.lg}` (12px). There are no drop shadows
anywhere — depth is expressed only by a 1px hairline border or by the single dark
inversion.

**Key characteristics:**
- Paper-white `{colors.canvas}` end to end; no surface alternation, no gradients on structure
- Center-aligned hero with a fluid `{typography.display-xl}` Clash Display headline and one animated `{components.gradient-word}`
- Signature pill `{components.install-snippet}` sitting directly under the hero subhead
- Squared buttons (`{rounded.sm}`) against fully-rounded inputs/snippets (`{rounded.full}`)
- A `{components.terminal-card}` as the only "product preview," complete with macOS traffic-light dots
- A flat, hairline-ruled `{components.pricing-table}` — uppercase Space Mono headers, DM Sans tabular numbers
- One inverted `{components.cta-strip-dark}` — the system's single non-white surface
- Fully responsive: fluid type, a real toggled `{components.mobile-menu}`, wrapping snippet, full-width tap targets

## Colors

The palette is black + white + four grays, plus a quarantined four-stop gradient
and three macOS terminal dots. There is no brand hue carrying CTAs — the brand is
black on white.

### Ink & surface
- **Primary / Ink** (`{colors.primary}`, `{colors.ink}` — `#000000`): headlines, nav wordmark, every button label on light surfaces, primary table text.
- **Ink Deep** (`{colors.ink-deep}` — `#090909`): the pressed/active state of `{components.button-primary}`, one notch below pure black.
- **Charcoal** (`{colors.charcoal}` — `#525252`): list/feature copy and lower-emphasis text.
- **Body** (`{colors.body}` — `#737373`): the workhorse — default paragraph copy, FAQ answers, footer links.
- **Mute** (`{colors.mute}` — `#a3a3a3`): captions, table header labels, terminal comments, lowest-emphasis text.
- **Canvas** (`{colors.canvas}` — `#ffffff`): the page itself and nearly every surface.
- **Surface Soft** (`{colors.surface-soft}` — `#fafafa`): the fill behind the install snippet, search pill, and command tags.
- **Surface Dark** (`{colors.surface-dark}` — `#171717`): the single inverted CTA strip.
- **Hairline** (`{colors.hairline}` — `#e5e5e5`): all 1px borders and row dividers.
- **Hairline Strong** (`{colors.hairline-strong}` — `#d4d4d4`): the pricing table's header rule and the secondary button border.

### On-dark
- **On Dark** (`{colors.on-dark}` — `#ffffff`): text on `{colors.surface-dark}`.
- **On Dark Mute** (`{colors.on-dark-mute}` — `rgba(255,255,255,0.7)`): secondary copy inside the dark CTA strip.

### Accent — the gradient word (the only real color)
A four-stop gradient, mirrored so the loop is seamless (it starts and ends on blue):
- **Blue** `{colors.gradient-blue}` `#3B82F6` → **Green** `{colors.gradient-green}` `#10B981` → **Orange** `{colors.gradient-orange}` `#F97316` → **Pink** `{colors.gradient-pink}` `#EC4899` → back to **Blue**.

This palette appears only inside `{components.gradient-word}`. It has no other use.

### Semantic
The system has no error/success/warning palette — there are no forms, validation,
or destructive flows on the marketing surface. The only "semantic" colors are the
three macOS terminal dots, used only inside `{components.terminal-card}`:
- **Red** `{colors.term-red}` `#ff5f56` · **Yellow** `{colors.term-yellow}` `#ffbd2e` · **Green** `{colors.term-green}` `#27c93f`

### Focus
- **Focus Ring** (`{colors.focus-ring}` — `rgba(59,130,246,0.5)`): a 3px translucent-blue outline (offset 2px) on `:focus-visible` for links, buttons, and inputs. The only blue in the chrome.

## Typography

### Font families
- **Clash Display** (display, 600/700) — all headings: hero title, section headers,
  card titles, FAQ questions, the nav wordmark. Loaded from **Fontshare**
  (`api.fontshare.com`), not Google Fonts. Falls back to `Space Grotesk` → `system-ui`.
  Clash ships no 500 weight, so headings that read as "medium" are rendered at 600.
- **DM Sans** (body, 400–700) — paragraph copy, UI text, button labels, and the
  pricing-table numbers (500, `tabular-nums`). From Google Fonts; falls back to `system-ui`.
- **Space Mono** (labels + code, 400/700) — at **700, uppercase** it carries every
  small structural label (table headers, hero meta tag, footer links, copyright);
  at **400** it carries code in the install snippet and terminal mockup. From Google
  Fonts; falls back to `ui-monospace` → SFMono/Menlo/Consolas.

The pairing is intentional: Clash supplies geometric personality up top, DM Sans
keeps the body neutral and legible, and Space Mono's monospaced labels reinforce
the "this is documentation / this is a developer tool" register.

### Hierarchy

| Token | Family | Size | Weight | Line | Use |
|---|---|---|---|---|---|
| `{typography.display-xl}` | Clash Display | clamp(28–36px) | 700 | 1.12 | Hero headline (fluid) |
| `{typography.display-lg}` | Clash Display | clamp(24–30px) | 600 | 1.2 | Section headlines ("Pricing", "FAQ") |
| `{typography.heading-lg}` | Clash Display | 24px | 600 | 1.33 | In-body subheads, dark CTA title |
| `{typography.heading-md}` | Clash Display | 20px | 600 | 1.4 | "Why us" card titles |
| `{typography.heading-sm}` | Clash Display | 18px | 600 | 1.56 | FAQ questions |
| `{typography.body-md}` | DM Sans | 16px | 400 | 1.5 | Default body, FAQ answers |
| `{typography.body-strong}` | DM Sans | 16px | 500 | 1.5 | Mobile-menu links, inline emphasis |
| `{typography.body-sm}` | DM Sans | 14px | 400 | 1.43 | Feature bullets, search placeholder |
| `{typography.caption}` | DM Sans | 12px | 400 | 1.33 | "one endpoint, one key" caption |
| `{typography.label}` | Space Mono | 12px | 700 | 1.33 | Table headers, hero tag, footer — UPPERCASE, `+0.06em` |
| `{typography.code-md}` | Space Mono | 16px | 400 | 1.5 | Install-snippet command |
| `{typography.code-sm}` | Space Mono | 14px | 400 | 1.6 | Terminal output, command tags |
| `{typography.button}` | DM Sans | 14px | 500 | 1 | Every button label |

### Principles
The ramp is tight and compresses fast (36 → 30 → 24 → 20 → 16) so the page reads as
a single readable column rather than a marketing pyramid. Headings carry a slight
`-0.01em` negative tracking to keep Clash's geometric forms from feeling loose; the
only positive tracking in the system is the `+0.06em` on uppercase Space Mono labels.
No italics, no display-only weights beyond 700.

## Layout

### Spacing
- **Base unit:** 8px, with finer 2/4/6px steps for inline gaps.
- **Tokens:** `{spacing.xxs}` 2 · `{spacing.xs}` 4 · `{spacing.sm}` 8 · `{spacing.md}` 12 · `{spacing.lg}` 16 · `{spacing.xl}` 24 · `{spacing.xxl}` 32 · `{spacing.section}` 88.
- **Section rhythm:** `{spacing.section}` (88px) vertical padding between every major block. This is the single most important spacing decision — the air *is* the layout.
- **Card padding:** terminal card at `{spacing.lg}` (16px); the dark CTA strip at `24px 32px`; pricing/FAQ rows at `16px 0`.

### Container
Two centered, fluid-width columns rather than a fixed grid:
- **`{layout.container}`** — `width: 86%`, `max-width: 1100px`. Holds the hero, why-us, pricing, privacy, and FAQ.
- **`{layout.container-wide}`** — `width: 90%`, `max-width: 1240px`. Holds the two-column split and the dark CTA strip.
- Inner reading measures are capped per element (e.g. hero subhead ~64ch, FAQ ~880px) so line lengths stay readable even as the container widens.

### Section grids
- **Why-us:** 3-up equal columns → 1-up centered below 850px.
- **Split (text + terminal):** 50/50 → stacks vertical below 850px (text above terminal).
- **Pricing:** a single flat table inside a horizontal-scroll container.
- **FAQ:** single stacked column, max 880px.
- **Footer:** centered single row of small links, wrapping on narrow screens.

### Whitespace philosophy
Whitespace carries the entire structure. No colored bands, no callout boxes, no
lifted cards between sections — just 88px of white. Inside a section, content sits
in a tight reading column. The page is a long-form document and the gaps are its
paragraph breaks.

## Elevation & depth

| Level | Treatment | Use |
|---|---|---|
| 0 — Flat | No border, no shadow | Hero, why-us, privacy, footer — the dominant treatment |
| 1 — Hairline | 1px solid `{colors.hairline}` | Terminal card, pricing/FAQ dividers, nav & footer rules |
| 2 — Inverted | `{colors.surface-dark}` fill | The single dark CTA strip — depth via color, never shadow |

There are **no drop shadows** in the system. Nothing floats or lifts. The only
non-flat moment is the one dark CTA strip.

### Decorative depth
The system is nearly ornament-free. Its only non-text visual devices are:
- **The animated gradient word** — the hero's "easiest" (see Motion).
- **A stroke-only lock icon** — line-drawn in `{colors.ink}` in the "Your data stays yours" section.
- **macOS traffic-light dots** — three 12px filled circles in the terminal card header.

(Earlier iterations carried a hand-drawn llama mascot in the nav and hero; both have
been removed. The brand mark is now the plain "TENSORAI" wordmark.)

## Shapes

### Border-radius scale

| Token | Value | Use |
|---|---|---|
| `{rounded.sm}` | 6px | **Buttons** (squared), inline code chips |
| `{rounded.md}` | 8px | Reserved / rare medium surfaces |
| `{rounded.lg}` | 12px | Cards — terminal card, dark CTA strip |
| `{rounded.full}` | 9999px | **Inputs & snippets** — search pill, install snippet, command tag, traffic-light dots |

The defining shape decision is the **split**: buttons are squared to 6px while
inputs/snippets are fully pill-rounded. This is the inverse of the typical "pill
buttons" pattern and is load-bearing for the brand's feel — keep it.

### Imagery geometry
There is no photography. Image-like elements are vector only: the lock icon
(single stroke), the search/copy/hamburger icons (2px stroke, round caps), and the
three filled terminal dots.

## Components

> Specs cover Default and Active/Pressed. Hover is limited to quiet color/border shifts.

### Buttons (squared, `{rounded.sm}`)

**`{components.button-primary}`** — the universal CTA
- Background `{colors.primary}`, text `{colors.on-primary}`, `{typography.button}`, `8px 20px`, height 36px, radius `{rounded.sm}`.
- Active: background drops to `{colors.ink-deep}`.
- Used for "Get an API key" (nav + hero), "Get started" is the on-dark variant.

**`{components.button-secondary}`** — outline on canvas
- Background `{colors.canvas}`, text `{colors.ink}`, 1px `{colors.hairline-strong}` border, radius `{rounded.sm}`.
- Active: border darkens to `{colors.ink}`. Used for "View pricing" in the hero.

**`{components.button-on-dark}`** — white pill-square on the dark strip
- Background `{colors.canvas}`, text `{colors.ink}`. Sits inside `{components.cta-strip-dark}` as "Get started" so the dark surface anchors and the light button reads as the action.

### Inputs & snippets (pill, `{rounded.full}`)

**`{components.search-pill}`** — nav search (decorative placeholder)
- Background `{colors.surface-soft}`, magnifier icon + "Search models" placeholder in `{colors.mute}`, height 36px. Hidden below the mobile-nav breakpoint.

**`{components.install-snippet}`** — the signature element
- A `{colors.surface-soft}` pill in `{typography.code-md}` with a `$` prompt in `{colors.mute}`, the install command, and a copy-icon button at the right edge. Sits directly under the hero subhead. Wraps (rather than truncates) on phones.

**`{components.command-tag}`** — small inline command chip
- `{colors.surface-soft}` pill, `{typography.code-sm}`, `6px 12px`. Used for the `base_url = …` chip in the split section.

### Cards & containers (`{rounded.lg}`)

**`{components.terminal-card}`** — the only product preview
- `{colors.canvas}` fill, 1px `{colors.hairline}`, 16px padding. Header is a row of three `{components.terminal-traffic-lights}` (12px red/yellow/green, `{spacing.xs}` gaps). Body is `{typography.code-sm}` with comments in `{colors.mute}` and active text in `{colors.ink}`; scrolls horizontally on overflow.

**`{components.pricing-table}`** — flat, hairline-ruled
- Header cells: `{typography.label}` (uppercase Space Mono) in `{colors.mute}`, over a 1px `{colors.hairline-strong}` rule. Right-aligned numeric headers ("Input / Output / Cached").
- Body rows: `16px 0` padding, separated by 1px `{colors.hairline}`. Model name in `{colors.ink}` 500 (variant qualifiers in `{colors.mute}`); numbers in **DM Sans 500 with `tabular-nums`**, right-aligned. "Contact" rows render an inline underlined link instead of a price.
- Lives in a horizontal-scroll wrapper (`min-width: 560px`) so it scrolls rather than cramping on small screens.

**`{components.cta-strip-dark}`** — the single inverted surface
- `{colors.surface-dark}` fill, `{colors.on-dark}` title in `{typography.heading-lg}`, `{colors.on-dark-mute}` subcopy, a `{components.button-on-dark}` CTA, radius `{rounded.lg}`, `24px 32px`. Stacks vertically on phones. Use **once per page**.

### Content rows

**`{components.faq-row}`** — always-expanded Q&A
- Question in `{typography.heading-sm}` (`{colors.ink}`), answer directly below in `{typography.body-md}` (`{colors.body}`), with `4px` gap. 1px `{colors.hairline}` bottom divider, `16px 0` padding. No accordion — answers are always visible. Inline `<code>` chips use Space Mono.

**Feature bullets / why-us items**
- A heading in `{typography.heading-md}` over `{typography.body-sm}` body in `{colors.body}`. No border, no card chrome — flat stacked text that centers when the grid collapses.

### Navigation

**`{components.primary-nav}`** — sticky, 56px
- `{colors.canvas}` background, 1px `{colors.hairline}` bottom border, sticky to top. Layout: "TENSORAI" wordmark (left) · text links Models/Docs/Pricing · centered `{components.search-pill}` · right cluster of "Sign in" + black "Get an API key".

**`{components.mobile-menu}`** — toggled dropdown (≤768px)
- Below 768px the links, search, and sign-in collapse; the hamburger toggles a full-width `{colors.canvas}` dropdown (1px `{colors.hairline}` bottom) listing Models · Docs · Pricing · Sign in · Get an API key. Items are `{typography.body-strong}` with hairline dividers; the CTA renders as a full-width 44px button. JS manages `aria-expanded`/`aria-label`, closes on link tap, and resets on resize above 768px.

### Footer

**`{components.footer}`**
- `{colors.canvas}`, 1px `{colors.hairline}` top border, `32px 24px`. A centered wrapping row of `{typography.label}` (uppercase Space Mono) links in `{colors.body}` — Get an API key · Docs · Pricing · GitHub · Discord · Contact · Privacy · Terms — with a `© 2026 TENSORAI · San Francisco` label pushed to the right edge (wraps to its own row on mobile).

## Motion

The system is almost entirely static. Transitions are limited to quiet ~120ms
color/border shifts on buttons. There is exactly **one** continuous animation:

**`{components.gradient-word}`** — the hero word "easiest"
- A `linear-gradient(115deg, …)` of blue→green→orange→pink→blue, clipped to the
  text (`background-clip: text`, transparent fill) on a `320% 320%` background.
- The `gradient-drift` keyframes move `background-position` through five offset
  points across a 2D field (vertical + diagonal sweeps), `9s ease-in-out infinite`.
  The path returns to its origin and the palette is mirrored, so the loop is seamless.
- **Only the color moves — the word itself does not.** (An earlier `word-float`
  transform was removed by design.)
- `@media (prefers-reduced-motion: reduce)` sets `animation: none`, holding the
  gradient still.

## Do's and don'ts

### Do
- Treat the page as a Markdown document: one reading column, 88px of `{spacing.section}` air between blocks, no decorative dividers.
- Use `{components.button-primary}` (black, squared) for every primary action. There is no colored CTA.
- Keep the shape split: **buttons squared (`{rounded.sm}`)**, **inputs/snippets pill (`{rounded.full}`)**, **cards `{rounded.lg}`**.
- Set headings in Clash Display at 600/700 and everything else in DM Sans; use Space Mono **only** for uppercase labels and code.
- Reserve `{components.cta-strip-dark}` for exactly one "look here" moment per page.
- Keep `{components.gradient-word}` the only color and the only animation. One word, once.
- Render commands inside `{components.install-snippet}` / `{components.terminal-card}` / `{components.command-tag}` — code is a first-class component.

### Don't
- Don't add shadows, structural gradients, or atmospheric backgrounds. The canvas is pure `{colors.canvas}`.
- Don't introduce a brand hue for CTAs — the system is black on white with gray prose.
- Don't round the buttons into pills or square the inputs — the inverse split is intentional.
- Don't animate the word's position, add a second gradient, or color a second word.
- Don't use a second dark surface or lift cards with shadow — hairline border or the one inversion only.
- Don't swap DM Sans for a branded body face; the neutral body is what makes the headings and gradient read as the accents.

## Responsive behavior

### Breakpoints

| Name | Width | Key changes |
|---|---|---|
| desktop | 1100px+ | Default — fluid container to 1100/1240px max, 3-up why-us, 50/50 split |
| stack | ≤850px | Why-us → 1-up centered; split stacks (text above terminal) |
| mobile-nav | ≤768px | Nav links/search/sign-in collapse into the toggled `{components.mobile-menu}`; section padding 64px |
| phone | ≤640px | Container → 92% width; install snippet wraps; hero buttons + dark-strip button go full-width 44px; CTA strip stacks; footer gaps tighten |

### Type & targets
- Hero and section headings scale fluidly via `clamp()` (no hard jump at one breakpoint).
- Primary touch targets are 36px on desktop and grow to **44px full-width** on phones (hero actions, dark CTA, mobile-menu CTA) for comfortable tapping.
- `:focus-visible` shows the `{colors.focus-ring}` outline on all interactive elements.

### Collapsing strategy
- **Nav:** horizontal → hamburger dropdown at 768px; the desktop "Get an API key" pill moves into the menu (the menu carries its own full-width CTA).
- **Install snippet:** single-line with ellipsis on desktop → wraps to multiple lines with `word-break` on phones; copy icon stays anchored.
- **Pricing table:** always a horizontal-scroll container (min-width 560px) so long model names never cramp; a right hairline hints the scroll on phones.
- **Split:** 50/50 → vertical stack at 850px.
- **Section spacing:** 88px → 64px (≤768px) → 48px (≤640px).

## Implementation notes

- **Single file.** Everything lives in `index.html`: all CSS in one `<style>` block
  (tokens as CSS custom properties on `:root`), plus a ~25-line `<script>` for the
  install-snippet copy button and the mobile-menu toggle. No build step, no backend.
- **Tokens.** The front-matter mirrors the `:root` variables 1:1 (`--primary`,
  `--surface-dark`, `--r-sm`, `--s-section`, `--font-display`, etc.). Change a token
  once and it propagates.
- **Fonts.** Clash Display loads from `api.fontshare.com`; DM Sans + Space Mono from
  Google Fonts. All three degrade to system fonts offline. Self-host the woff2 files
  if you need offline/air-gapped reliability.
- **Brand placeholder.** "TENSORAI" is the wordmark; endpoints use `api.tensorai.com`
  and the contact email is `hello@tensorai.com`. These are easy find-and-replace targets.
- **Accessibility.** `prefers-reduced-motion` is honored for the gradient; the mobile
  menu manages ARIA state; focus is always visible. The nav search input is currently
  decorative (not wired to anything).
