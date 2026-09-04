# Custom Domain Brand Kit

The logo, wordmark and colour tokens behind customdomain.ai, and the rules for using them.

> [!NOTE]
> New repository, opened 2026-09-04. This README is the specification and it is complete and
> current. The vector sources are not committed here yet, so the inventory below says where
> each asset lives today.

**Status:** Specification committed · vector sources pending · public

|  |  |
|---|---|
| **What it is** | The canonical brand reference for Custom Domain: mark, wordmark, colour and type |
| **Who it's for** | Anyone putting the Custom Domain name or mark on a surface, inside the company or out |
| **Live at** | [customdomain.ai](https://customdomain.ai) · [github.com/CUSTOM-DOMAIN-APP](https://github.com/CUSTOM-DOMAIN-APP) |
| **Stack** | Markdown spec · CSS custom properties · Inter · PNG masters, no SVG yet |
| **Status** | Tokens transcribed from the shipped site theme and re-verified 2026-09-04 |

Custom Domain is the product that lets a platform's users connect a domain they own. Its
identity is a dark one: near-black ink, a single purple, and Inter set tight. Everything on
this page is what actually ships today, not an aspiration, which is the only way a brand
reference stays worth opening.

## Why it exists

The identity was captured from a Framer build and rebuilt in React, and the tokens landed in a
theme file inside the marketing site. That made the site correct and left everything else
guessing. A slide deck, a GitHub badge, a partner one-pager and an in-product empty state were
each picking their own purple, and two different greys were both being called "the background".

One page that a person can read in ninety seconds settles that. Everything below is a value you
can copy or a rule short enough to remember, and every one of them was read off something that
is live rather than out of a deck.

A brand kit earns its keep in the moments nobody plans for: a partner asks for a logo an hour
before their launch post, a conference wants a mark for the sponsor wall, an engineer needs the
right green for a status pill at eleven at night. Each of those is a small decision that gets
made either from this page or from a screenshot. This page is cheaper and it is right.

## What it covers

- **The name.** *Custom Domain*, two words, title case. Never "Connect Domain", never one word in prose. The domain is `customdomain.ai` and stays one word because it is a hostname.
- **The lockup.** The mark, then a `2.5` gap, then the wordmark at 15px / 600 weight with `-0.01em` tracking, in white.
- **Colour.** Four brand values, four primitives, and the surface and border alphas that build every card.
- **Type.** Inter for everything, with a monospace treatment reserved for values a developer types.
- **Contrast and focus.** The one accessibility fact worth memorising and the focus ring that depends on it.
- **Asset inventory.** Where each file lives right now, and which ones do not exist yet.

## Quickstart

Paste the tokens. They are declared on `[data-theme="cd"]` in the shipped site and work as
plain custom properties anywhere:

```css
:root {
  /* Brand */
  --cd-purple:    #6d3fea;  /* buttons, active nav, ambient glow */
  --cd-lavender:  #a492ed;  /* eyebrow rules, links, focus ring, gradient terminus */
  --cd-green:     #34d399;  /* live and verified states */
  --cd-orange:    #f6821f;  /* warning, and the provider accent */

  /* Primitives */
  --ink:          #020010;  /* page background, near-black and blue-shifted */
  --snow:         #f7f7fa;
  --white:        #ffffff;  /* primary text */
  --danger:       #f2555a;

  /* Surfaces are white at low alpha over ink, never a lighter grey */
  --surface:      rgba(255, 255, 255, 0.04);
  --border:       rgba(255, 255, 255, 0.10);
  --separator:    rgba(255, 255, 255, 0.08);
  --muted:        rgba(255, 255, 255, 0.55);

  /* Geometry */
  --radius:       1rem;     /* cards */
  --field-radius: 999px;    /* inputs, chips, pills */
}
```

The public product imagery is committed in the organisation profile repo and can be pulled
directly:

```bash
curl -O https://raw.githubusercontent.com/CUSTOM-DOMAIN-APP/.github/main/assets/provider-logos.png
curl -O https://raw.githubusercontent.com/CUSTOM-DOMAIN-APP/.github/main/assets/connect-flow-demo.gif
```

## Design tokens

**Type.** Inter, one family, bound to `--font-sans`. The monospace stack is
`ui-monospace, SFMono-Regular, Menlo, monospace`, used only for values a developer types or
receives: domains, record types, endpoints, statuses. Shipped scale: hero 60 to 72px / 500,
section heading 30px / 500, card title 17px / 600, body 16px / 400 to 500, meta 14px / 400,
eyebrow 12px / 500 uppercase with wide tracking.

**Depth.** The design reads flat. Depth comes from a radial purple glow, not a drop shadow.
Surface shadows are explicitly zero; only floating overlays carry one.

**Contrast.** Lavender measures 7.83:1 against ink, which is why it carries the focus ring:
`2px solid var(--cd-lavender)` with a `2px` offset. Do not swap the focus ring to purple, which
does not clear the same bar.

**Gradients.** Three recur: an eyebrow rule,
`linear-gradient(90deg, transparent 0%, #a492ed 100%)`; an ambient glow,
`radial-gradient(50% 50%, #6d3fea 0%, transparent 100%)`; and a headline sheen,
`linear-gradient(128deg, #ffffff 4%, #a492ed 46%)`, clipped to text.

## Asset inventory and layout

| Asset | Where it lives today | State |
|---|---|---|
| `logo-glyph.png` | Marketing site, `public/brand/` (private repo in this org) | White on transparent, 256px tall. Crisp at lockup sizes, not for display sizes |
| `logo-mark.png` | Marketing site, `public/brand/` (private repo in this org) | The mark with its plate |
| Logo lockup component | Marketing site, `components/ui/logo.tsx` (private repo in this org) | The reference implementation of the spacing above |
| `provider-logos.png` | `.github` repo, `assets/` (public) | The supported provider wall |
| `connect-flow-demo.gif` | `.github` repo, `assets/` (public) | 3.5 MB. Copy it, never hotlink it |
| Product screenshots | `.github` repo, `assets/` (public) | `app-connect-domain.jpg`, `app-domain-live.jpg` |
| Vector masters | Nowhere | No SVG exists for the mark or the wordmark |

## Usage rules

- Set the mark on ink or on a dark photograph. There is no approved light-background lockup because there is no dark version of the mark.
- Do not recolour, rotate, outline or add effects to the mark, and do not rebuild the wordmark in another face.
- Shields.io badges across this organisation use ink `1c1917`, which is a GitHub-surface convention rather than a brand colour. It is deliberate and it stays.
- Product names in this family are written on their own terms: **Custom Domain**, **Custom Agents**, **CustomPortal**, **JustMail**.

## Limitations

- **No SVG master.** Every mark in circulation descends from a 256px PNG, which caps the largest clean rendering at roughly lockup size. Anything larger than a nav bar needs a redraw first.
- **No build script.** Derived assets are produced by hand today. A generator is the reason this repo exists, and it is not written.
- **Two palettes are live.** The product ships the dark ink and purple theme; GitHub surfaces and the App registration page ship a warm stone palette (`#faf9f7`, `#1c1917`, `#57534e`). Both are intentional today. Reconciling them is an open decision, not a bug to fix quietly.

## License

The Custom Domain name, wordmark and logo mark are trademarks of CustomDomain.ai. No open
source licence applies to the assets: all rights reserved. The colour values, type scale and
usage rules on this page are published so that partners and press can represent the product
correctly, and may be quoted for that purpose. For anything else, ask first.
