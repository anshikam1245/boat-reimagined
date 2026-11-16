# boAt, reimagined

A working concept store built from my UX audit of boat-lifestyle.com. The audit logged 13 problems across desktop and mobile, and this concept fixes all 13. Turn on **Audit view** (top right) and a red tag appears on every fix. Tap one to see what the live site did before and what changed.

It opens in dark mode; the sun/moon button switches to light, and the choice is remembered.

- Live concept: https://anshikam1245.github.io/boat-reimagined/
- Full case study: https://www.behance.net/gallery/258539387

> Unofficial portfolio project by Anshika Mittal. Not affiliated with or endorsed by boAt / Imagine Marketing Limited. Nothing on the site can be bought, and it collects no data. Prices, ratings and features are as listed on boat-lifestyle.com on 16 Nov 2026. Product photos belong to boAt and its retailers and are used for portfolio purposes.

## What's fixed where

| Fix | Where to see it |
| --- | --- |
| D1 · FAQ named other products | Any product page. The FAQ is generated from the product's own spec record, and each answer shows its source. |
| D2 · Sign-up wall on arrival | Gifting page (no modal) and checkout (sign-in asked for there). |
| D3 / M5 · Search hint looked like a search | Header search. The hint is static and muted, and results match what you type. |
| D4 · Broken image | Product gallery. Open the D4 note and press "Break the product photo". |
| D5 · "Resonates" grammar slip | Gifting headline. |
| D6 · Three coupon systems | Product price box and cart. One computed price, and the cart applies the single best offer. |
| D7 · 90+ link footer | Footer. Popular links first, the full inventory in collapsible groups. |
| D8 / M2 · Duplicate spec rows | Spec table. One row per feature, legal details shown once. |
| M1 · Two stacked sticky bars | Product pages on mobile. The buy bar replaces the tab bar. |
| M3 · Unlabelled countdown | Removed from the product gallery. |
| M4 · Floating chip over content | "Similar products" lives in the gallery controls. |

## Links that open a fix directly

Each link turns on audit view and opens the note for that fix:

- D1: `https://anshikam1245.github.io/boat-reimagined/#/p/rockerz-412?fix=D1`
- D6: `https://anshikam1245.github.io/boat-reimagined/#/p/rockerz-412?fix=D6`
- M1 (best on a phone): `https://anshikam1245.github.io/boat-reimagined/#/p/rockerz-110?fix=M1`
- All 13: `https://anshikam1245.github.io/boat-reimagined/#/audit`

Add `?audit=1` before the `#` to open any page with audit view already on.

## Put it online (GitHub Pages, about 5 minutes)

1. On GitHub, create a new public repository named `boat-reimagined`.
2. Choose **Add file > Upload files**, drop in `index.html`, `og-image.png` and this `README.md`, then commit.
3. Go to **Settings > Pages**. Under **Build and deployment**, pick **Deploy from a branch**, choose `main` and `/ (root)`, then **Save**.
4. After a minute or two the site is live at `https://anshikam1245.github.io/boat-reimagined/`.

If you name the repository something else, change the `og:image` line near the top of `index.html` to match, so link previews show the image.

## Updating prices or photos

Open `index.html` and search for `PRODUCT DATA`. Each product is one line of data.

- To change a price, edit `price` (selling price) or `mrp`, and update `LISTED_ON` at the top.
- Product photos are embedded in the file, so the site works with no image hosting. To swap one, add `img: "https://..."` to that product and it takes priority.
- If a photo ever fails to load, a drawn version of the product appears instead of a broken icon (that's fix D4).

## Built with

One self-contained HTML file: no framework, no database, no tracking. Archivo is embedded as a variable font (OFL) and the product photos are embedded as WebP. Cart, theme and audit-view state live in the visitor's own browser.

Research, design and build by Anshika Mittal, with Claude.
