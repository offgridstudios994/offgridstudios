# OFFGRD STUDIO — website mockup

A single-page, self-contained marketing-site mockup for a Beirut music conservatory.
Built with the blkprint pipeline. **This is a demo:** the name, images, phone number and
stats are all placeholders, flagged in the page.

## Files
- `index.html` — the whole site (HTML + CSS + JS inlined). Nothing to build.
- `logo.svg` — the logo mark (simple equalizer bars).
- `DESIGN.md` — the design spec (palette, type, the signature scroll concept).

## View it
Open `index.html` in a browser, or serve the folder:
```
python3 -m http.server 4599
# then visit http://localhost:4599
```

## Change the name
The brand name is plain text — search-and-replace **`OFFGRD STUDIO`** in `index.html`
(it appears in the header, footer, page title, contact email and the WhatsApp message).

## Change the logo
Replace **`logo.svg`** with your own SVG (keep the filename), or edit it — it's four
`<rect>` bars; change the `fill` colour or each bar's height. It's used in the header,
the footer and as the browser-tab icon.

## Change the accent colour
Edit the CSS variables at the top of `index.html` (`:root { --brass: … }`). `--brass` is
the main accent; the logo uses the same value (`#d59a4e`).

## Connect the "Book a trial" button
The form opens WhatsApp with a pre-filled message, sent to the studio's number
(+961 71 610 379). To change it, search for `wa.me/96171610379` in `index.html` (and the
displayed `+961 71 610 379` in the contact section) and replace with your WhatsApp number
(country code, no `+`).
