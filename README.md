# Gill Makes Stuff

The website for **Gill Makes Stuff** (GMS) — a maker's channel and craft hub from a self-built studio in the Scottish Highlands. Static, hand-built, no framework, no build step.

🔗 **Live site:** https://gillmakesstuff.co.uk
📺 **Channel:** *(add YouTube link)*

---

## What's in here

| File | What it is |
|------|------------|
| `index.html` | Homepage — hero, what-I-make, latest videos, downloads teaser, about |
| `downloads.html` | The free downloads library, filterable by craft |
| `CNAME` | Tells GitHub Pages which domain to serve *(created automatically when you set the custom domain — leave it alone)* |
| `assets/` *(suggested)* | Your actual files: SVG cut files, STL print files, PDF printables, and images |

Both pages are completely self-contained — all CSS and JavaScript live inside each HTML file, so there's nothing to install or compile. Edit a file, push, and the change is live within a minute or two.

---

## Previewing locally

The quickest check is to double-click `index.html` to open it in a browser.

To test it exactly as it'll behave when hosted (so `index.html` is served as the root and the page-to-page links resolve properly), run a tiny local server from the repo folder:

```bash
python3 -m http.server 8000
```

Then visit **http://localhost:8000** in your browser. Stop it with `Ctrl+C`.

---

## Updating the content

Everything below is plain text inside the HTML — no special tooling needed. Search for the bit you want and edit it.

**Latest videos** (`index.html`)
Find the three `vcard` blocks in the *Watch* section. Replace the titles, the `· duration · craft` line, and point each card's `href="#"` at the real YouTube URL.

**Free downloads** (`downloads.html`)
Each download is an `<article class="dl">` block. To add one, copy an existing block and edit the title, description, craft tag, and meta line. Two things to keep in sync:
- `data-cat="..."` on the `<article>` controls which filter chip it appears under (e.g. `sewing`, `bookbinding`, `printing`, `knitting`, `leatherwork`). A file can belong to several — just separate them with spaces.
- The badge class (`svg` / `stl` / `pdf`) sets the colour-coded file-type label.
Then point the download link's `href="#"` at your actual file (e.g. `assets/zip-pouch.svg`).

**The crow mark**
The crow is a hand-drawn placeholder SVG. If you have your own crow artwork from the journal covers, swap the `<svg>` inside `.gms` (header) and `.foot-head` (footer) for it, or drop in an image.

**About / bio** (`index.html`)
The *About* section copy is deliberately plain — rewrite it in your own voice. There's a mauve note in there reminding you it's placeholder; delete that line when you're done.

**Social & contact links**
Footer links (`YouTube`, `Instagram`, `Email`) are `href="#"` placeholders on both pages — point them at the real destinations.

---

## Brand reference

Keep these consistent if you add pages or graphics.

| Role | Colour | Hex |
|------|--------|-----|
| Highland Green (primary ink) | 🟩 | `#3a5a40` |
| Deep Green (fine text) | 🟩 | `#2c4531` |
| Cream / Paper (background) | ⬜ | `#f3eee2` |
| Warm Stone (secondary surface) | 🟫 | `#cabfa6` |
| Terra (accent — SVG badges, links) | 🟧 | `#c4714f` |
| Mauve (secondary accent — STL badges) | 🟪 | `#9d7e9b` |

**Type:** Poppins for headings, labels and UI · Fraunces for body and reading text *(both loaded from Google Fonts)*.
**Motifs:** the saddle-stitch seam divider and the crow mark — nods to bookbinding and the journal covers.

---

## How it's hosted

The site runs on **GitHub Pages** with the custom domain `gillmakesstuff.co.uk`. Pushing to the `main` branch redeploys automatically — there's no separate publish step. DNS (the A records pointing the domain at GitHub, plus the `www` CNAME) is configured at the domain registrar, not in this repo.

---

## A note on reuse

The **downloads** — cut files, print files and printables — are free for anyone to use. A credit back to the channel is always welcome but not required. The site's own code and design are here for GMS; if you'd like to reuse a chunk of it, just ask.
