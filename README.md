# YOURCOMPANY — marketing site

A single-page, static marketing site for an LLM inference reselling startup,
built on an Ollama-style **documentation-first** design system: paper-white
canvas, pure-black pill CTAs, rounded display headings, and a flat reading
column. Plain HTML + CSS, no build step, no backend.

## Stack

- One file: `index.html` (all CSS is inline in a `<style>` block; a tiny inline
  `<script>` only wires the install-snippet copy button).
- Webfonts (require a network connection on first load; they fall back to
  `system-ui` / monospace offline):
  - **Clash Display** (600/700) — all headings: hero title, section headers,
    card titles, FAQ questions. Loaded from **Fontshare** (`api.fontshare.com`),
    not Google Fonts.
  - **DM Sans** (400–700) — body copy and the pricing numbers. From Google Fonts.
  - **Space Mono** (700) — small uppercase structural labels: table column
    headers, the hero meta tag, footer links + copyright, and the running
    nav/footer chrome. Also carries the code in the install snippet and terminal
    mockup (at weight 400). From Google Fonts.

## Run it

It's static — just open the file:

```bash
open index.html          # macOS
```

Or serve it locally (any static server works):

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Customize

The brand name is the placeholder **`YOURCOMPANY`** everywhere. Find-and-replace it:

```bash
# macOS / BSD sed
sed -i '' 's/YOURCOMPANY/Acme/g' index.html README.md
```

Other things you'll likely want to change:

- **Endpoint** — `https://api.YOURCOMPANY.com/v1` in the terminal mockup, FAQ, and command tag.
- **Install command** — the `pip install ...` line in the hero install-snippet pill (`#install-cmd`).
- **Contact email** — `hello@YOURCOMPANY.com` in the footer.
- **CTAs** — the `Get an API key` / `Get started` buttons point to `#` placeholders.
- **Pricing** — edit the rows in `<table class="pricing">`. Numbers live in
  `<td class="num">` cells; "Contact" rows use an inline `<a>` to `#contact`.
- **Llama mascot** — inline `<svg class="llama">` in the nav and hero. Swap in your
  own brand mark; it's the only illustration in the system.

## Design system

Documentation-first, geometric, single-surface. The full token set lives in the
CSS `:root` block. Highlights:

### Palette (black + white + grays only — no brand color)

| Token            | Hex                   | Use                                   |
|------------------|-----------------------|---------------------------------------|
| primary / ink    | `#000000`             | Headlines, every pill CTA, nav links  |
| ink-deep         | `#090909`             | Pressed-state black                   |
| charcoal         | `#525252`             | List/feature text                     |
| body             | `#737373`             | Default paragraph + FAQ prose         |
| mute             | `#a3a3a3`             | Captions, terminal comments           |
| canvas           | `#ffffff`             | The whole page                        |
| surface-soft     | `#fafafa`             | Install snippet, search pill          |
| surface-dark     | `#171717`             | The one inverted CTA strip            |
| hairline         | `#e5e5e5`             | 1px borders + row dividers            |
| hairline-strong  | `#d4d4d4`             | Table header rule, secondary buttons  |
| terminal r/y/g   | `#ff5f56 #ffbd2e #27c93f` | macOS traffic-light dots only     |

### Shape & type

- **Squared buttons, pill inputs:** buttons use a small `6px` structural radius
  (squared, not pill). The install snippet, search pill, and traffic-light dots
  stay fully rounded; cards use `12px`.
- **No depth:** no shadows, no gradients. Surfaces are flat, or a 1px hairline
  border, or the single `surface-dark` inversion — that's the entire elevation scale.
- **Type ramp:** 36px Clash Display headline → 30/24px Clash section heads → 16px
  DM Sans body → 12px Space Mono uppercase labels. Tight, no marketing pyramid.
- **Section rhythm:** 88px of plain white air between blocks, no decorative dividers.

## Sections (single page)

Nav → Hero (mascot + headline + install-snippet pill + CTAs) → Drop-in split
(text + terminal mockup) → Why us (3 flat cards) → Pricing (flat hairline table) →
Your data stays yours → FAQ wall → dark CTA strip → footer.

## Notes

- Fully responsive: the why-us cards and the split stack on tablet; the pricing
  table scrolls horizontally; the nav collapses to a hamburger at 768px; the hero
  headline scales 36px → 28px on mobile.
- The only JavaScript is the ~8-line copy-to-clipboard handler for the install pill.
