# bibnor.com

Company site for **Bibnor** — custom school management software, built with AI.

Live at **https://www.bibnor.com** via GitHub Pages. Contact: **info@bibnor.com**

## What's here

| Path | Purpose |
| --- | --- |
| `index.html` | The whole site — markup, styles and script in one self-contained file. No build step, no dependencies. |
| `CNAME` | Custom domain for GitHub Pages (`www.bibnor.com`). |
| `.nojekyll` | Serves files as-is instead of running them through Jekyll. |
| `assets/icon.svg` | App icon / favicon. |
| `assets/icon-monochrome.svg` | Single-colour mark (`currentColor`) for stamps, print and watermarks. |
| `assets/logo-horizontal-light.svg` | Full lockup for light backgrounds. |
| `assets/logo-horizontal-dark.svg` | Full lockup for dark backgrounds. |
| `assets/og.svg` → `assets/og.png` | Social share card. The SVG is the source; the PNG is what gets shared. |

## The mark

A 5×7 dot grid — an attendance roster — with the letter **B** picked out in solid amber
nodes and traced with connectors. It is a picture of what the product does: find the
pattern inside rows of school data. The hero canvas is the same idea in motion, resolving
the grid into the mark, a timetable, an attendance chart and a trend line.

## Brand

| Token | Value |
| --- | --- |
| Chalkboard (hero ground) | `#0E1F17` |
| Ink | `#1F3D2E` |
| Amber | `#E8A33D` |
| Amber deep | `#B5731F` |
| Chalk | `#F1EEDD` |
| Paper | `#EFF0E6` |

Type is a geometric grotesk (Avenir Next / Century Gothic) for display, and a monospace
for labels and data. No web fonts are loaded, so the page never waits on a font CDN.

## Editing

Open `index.html` and edit it. There is nothing to install or compile — push to `main`
and GitHub Pages redeploys within a minute or two.

Regenerating the social card after editing `assets/og.svg` (macOS):

```bash
cd assets
qlmanage -t -s 1200 -o . og.svg && sips -c 630 1200 og.svg.png --out og.png && rm og.svg.png
```

## DNS

The `CNAME` file only tells GitHub which domain to answer for — the domain's DNS still has
to point at GitHub:

| Record | Host | Value |
| --- | --- | --- |
| CNAME | `www` | `bmns1.github.io` |

To serve the apex `bibnor.com` too, add `A` records for `185.199.108.153`,
`185.199.109.153`, `185.199.110.153` and `185.199.111.153`, then set the redirect in the
registrar or in the repository's Pages settings.
