# CustomDomain™ Brand Kit

The name rule, mark, color tokens and type behind customdomain.ai, and the rules for using them.

**Status:** Specification committed (README and IDENTITY.md) · asset files not committed yet · public

[![docs](https://img.shields.io/badge/docs-docs.customdomain.ai-1c1917?style=flat)](https://docs.customdomain.ai/docs)
[![license](https://img.shields.io/badge/license-all%20rights%20reserved-1c1917?style=flat)](#license)

[Website](https://customdomain.ai) · [Docs](https://docs.customdomain.ai/docs) · [Console](https://app.customdomain.ai) · [Brand page](https://customdomain.ai/brand) · [IDENTITY.md](./IDENTITY.md)

|  |  |
|---|---|
| **What it is** | The canonical brand reference for CustomDomain™: name, mark, color and type |
| **Who it's for** | Anyone putting the CustomDomain™ name or mark on a surface, inside the company or out |
| **Live at** | [customdomain.ai/brand](https://customdomain.ai/brand) · [github.com/CUSTOM-DOMAIN-APP](https://github.com/CUSTOM-DOMAIN-APP) |
| **Stack** | Markdown spec · CSS custom properties · Instrument Serif, Inter, Geist Mono · SVG and PNG masters in the design source, not committed yet |
| **Status** | Values checked against the live brand page and its tokens on 2026-09-26 |

CustomDomain™ is the product that lets a platform's users connect a domain they own. Its identity is a quiet,
warm one: near-black ink on paper, stone neutrals, an oak for a mark, one green kept for status, and three
typefaces. Everything on this page is what ships today on the brand page, the console and the hosted widget,
not an aspiration, which is the only way a brand reference stays worth opening.

## Why it exists

The identity has one written source of record, [IDENTITY.md](./IDENTITY.md), and one public page that renders
it, [customdomain.ai/brand](https://customdomain.ai/brand). Everything else (a slide deck, a GitHub badge, a
partner one-pager, an in-product empty state) ends up picking its own values unless something short and
current tells it what to use. An earlier version of this kit described a dark purple theme that no longer
ships anywhere; this version describes the stone palette that does.

One page that a person can read in ninety seconds settles that. Everything below is a value you can copy or a
rule short enough to remember, and every one of them was read off something that is live rather than out of a
deck.

A brand kit earns its keep in the moments nobody plans for: a partner asks for a logo an hour before their
launch post, a conference wants a mark for the sponsor wall, an engineer needs the right green for a status
pill at eleven at night. Each of those is a small decision that gets made either from this page or from a
screenshot. This page is cheaper and it is right.

## What it covers

- **The name.** *CustomDomain™*: one word, capital C and D, with the ™. The generic concept stays lowercase ("a custom domain"), and `customdomain.ai` stays lowercase because it is a hostname. Never "Connect Domain".
- **The mark.** An oak, in two constructions: flat for lockups and favicons, grounded for app icons and BIMI.
- **Color.** Ink on paper, stone neutrals for text and surfaces, and one green that means "live" and nothing else.
- **Type.** Instrument Serif for headlines, Inter for interface text and the wordmark, Geist Mono for facts and values.
- **Usage rules.** What not to do with the name and the mark.
- **Asset inventory.** Where each file lives today, and why none are committed here yet.

## Quickstart

Paste the tokens. They are published at
[customdomain.ai/brand/tokens.css](https://customdomain.ai/brand/tokens.css) and work as plain custom
properties anywhere:

```css
:root {
  --cd-ink: #1c1917;
  --cd-ink-soft: #44403c;
  --cd-muted: #6f6862;
  --cd-faint: #a8a29e;
  --cd-paper: #faf8f5;
  --cd-paper-2: #f4f1ec;
  --cd-card: #ffffff;
  --cd-line: #e7e5e4;
  --cd-line-soft: #efece7;
  --cd-live: #15803d;
  --cd-live-bg: #f0f7f1;
  --cd-accent: #0f6b33;
  --cd-warn: #b91c1c;
  --cd-warn-bg: #fbf2f1;
  --cd-btn: #1c1917;
  --cd-btn-ink: #faf8f5;
  --cd-serif: "Instrument Serif", Georgia, "Times New Roman", serif;
  --cd-sans: "Inter", system-ui, -apple-system, "Segoe UI", sans-serif;
  --cd-mono: "Geist Mono", ui-monospace, SFMono-Regular, Menlo, monospace;
  --cd-wrap: 1120px;
  --cd-radius: 14px;
  --cd-shadow: 0 1px 2px rgba(28,25,23,.04), 0 12px 40px -18px rgba(28,25,23,.22);
}
```

The same values as JSON, and the mark itself, straight from the brand page:

```bash
curl -O https://customdomain.ai/brand/tokens.json
curl -O https://customdomain.ai/brand/cd-mark-ink.svg     # the flat oak, ink, 512×512
```

## Design tokens

**Color.** Ink `#1c1917` carries body text, the logo on light surfaces, and buttons. Ink soft `#44403c` is
secondary body text, Muted `#6f6862` is eyebrows and captions, and Faint `#a8a29e` is placeholders only. Pages
sit on Paper `#faf8f5`, alternating bands on Paper 2 `#f4f1ec`, raised surfaces on Card `#ffffff`, and rules
are Line `#e7e5e4`. Live `#15803d` is for status only, with Accent `#0f6b33` as its hover. Warn `#b91c1c` means
failure. The full table, with roles, is section 3 of [IDENTITY.md](./IDENTITY.md).

**Type.** Three faces, all loaded from Google Fonts on the live site:

| Use | Face | Stack |
|---|---|---|
| Headlines only | Instrument Serif Regular | `"Instrument Serif", Georgia, "Times New Roman", serif` |
| Interface and body | Inter | `"Inter", system-ui, -apple-system, "Segoe UI", sans-serif` |
| Facts, hex values, domains, records | Geist Mono | `"Geist Mono", ui-monospace, SFMono-Regular, Menlo, monospace` |
| Wordmark | Inter SemiBold 600, all caps, +0.18em tracking | |

**The mark.** An oak. The flat construction (lockups, favicon) is a six-circle canopy, a rounded trunk 36×150
with rx 18, and two-stroke roots on a 512×512 artboard. The grounded construction (app icon, BIMI) keeps the
canopy language and adds a horizon stroke at y=302 and a three-root flare. The mark is `#1c1917` on paper and
`#fafaf9` on ink.

**Geometry.** Content width 1120px, radius 14px, and one soft shadow for raised surfaces (`--cd-shadow` above).

## Asset inventory and layout

The masters exist in the design source and the public set is downloadable from the brand page. None are
committed here yet, because the wordmark and lockup files still carry the retired two-word name; they will be
committed once they are redrawn, so this repository never ships the old name.

| Asset | Where it lives today | State |
|---|---|---|
| Oak mark, flat and grounded (SVG, PNG 128 to 1024) | Design source; public on [customdomain.ai/brand](https://customdomain.ai/brand) | Current |
| App icon (ink and paper), favicon (SVG, PNG 16 and 32), BIMI | Design source; public on the brand page | Current |
| Wordmarks (caps, serif), horizontal and stacked lockups, endorsement line | Design source; public on the brand page | Set the retired two-word name; being redrawn |
| Tokens, `tokens.css` and `tokens.json` | [customdomain.ai/brand/tokens.css](https://customdomain.ai/brand/tokens.css), [tokens.json](https://customdomain.ai/brand/tokens.json) | Current; transcribed above |
| Written spec | [IDENTITY.md](./IDENTITY.md) in this repository | Current; the copy on the brand page still has the old name rule |
| Social covers, avatars, product shots | Design source; some public on the brand page | Not committed here |
| Provider wall, demo capture, console screenshots | [`.github` repo, `assets/`](https://github.com/CUSTOM-DOMAIN-APP/.github/tree/main/assets) (public) | `connect-flow-demo.gif` is 3.5 MB: copy it, never hotlink it |

The design source also holds a green variant of the mark (`cd-mark-live.svg`, `#15803d`). It is not on the brand
page and it contradicts the "never green" rule, so do not use it as the logo.

## Usage rules

- Write the name as **CustomDomain™** every time the product is meant: one word, capital C and D, with the ™. Never "Custom Domain", "Customdomain" or "CUSTOM DOMAIN" as the name.
- Until the wordmark is redrawn, do not use the current wordmark, lockup or endorsement files to write the product name; they set the retired two-word name.
- The oak is ink on paper or `#fafaf9` on ink. Never green, never a second color, never an outline.
- Do not recolor, rotate, outline or add effects to the mark, and do not redraw it.
- Green `#15803d` means live status and nothing else. It is not a brand accent for decoration.
- Instrument Serif is for headlines. It is not the wordmark and not body text.
- The brand page files may be used for accurate reference to CustomDomain™. Do not redraw them, and do not imply a partnership that has not been announced.
- Shields.io badges across this organization use ink `1c1917` in the flat style, which is also the brand ink.
- Product names in this family are written on their own terms: **CustomDomain™**, **Custom Agents**, **CustomPortal**, **JustMail**.

## Limitations

- **The wordmark carries the retired name.** Every drawn wordmark and lockup still sets "CUSTOM DOMAIN" or "Custom Domain". They are being redrawn; until then this kit publishes the name rule and the mark, not a wordmark for the new name.
- **No assets committed yet.** The SVG and PNG masters live in the design source and on the brand page. They arrive here with the redrawn wordmark.
- **No build script in this repository.** The script that renders the PNG sizes and the download bundle from the SVG masters lives with the design source and is not committed.
- **The brand page lags this repository on the name.** customdomain.ai/brand and the IDENTITY.md it serves still state the two-word name rule. Until the page is updated, the rule in this repository is the current one.

## Related

- [.github](https://github.com/CUSTOM-DOMAIN-APP/.github): the organization profile and the public product imagery in `assets/`
- [docs](https://github.com/CUSTOM-DOMAIN-APP/docs): the CustomDomain™ documentation source, rendered at [docs.customdomain.ai](https://docs.customdomain.ai/docs)
- [customdomain-sdk](https://github.com/CUSTOM-DOMAIN-APP/customdomain-sdk): the browser SDK and the embeddable widget it opens

## Support

- **Docs:** [docs.customdomain.ai](https://docs.customdomain.ai/docs)
- **Questions and ideas:** [GitHub Discussions](https://github.com/CUSTOM-DOMAIN-APP/docs/discussions)
- **Bugs and corrections:** [open an issue](https://github.com/CUSTOM-DOMAIN-APP/customdomain-brand-kit/issues) on this repository
- **Service status:** [status.customdomain.ai](https://status.customdomain.ai)
- **Account and billing:** connect@customdomain.ai
- **Security:** report privately to security@customdomain.ai, never in a public issue. Policy: [app.customdomain.ai/security](https://app.customdomain.ai/security)

## License

No open source license applies to the assets or to this specification: all rights reserved. The CustomDomain™
name, the oak mark and the wordmark are trademarks of EverJust Company. The color values, type scale and usage
rules on this page are published so that partners and press can represent the product correctly, and may be
quoted for that purpose. For anything else, ask first. CustomDomain™ is a product of EverJust Company.
