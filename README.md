# Ember Jade Realty — Site Files

Vanilla HTML/CSS/JS, no build step. Push these files as-is to a GitHub repo and connect it to Netlify for auto-deploy on push — same workflow as your other site.

## Before going live, replace these placeholders:

**Rent** — in `index.html`, search for `rent-placeholder` (two spots, one per property) and swap `$&mdash; / month` for the real amount.

**Contact info** — in `index.html`, in the `#contact` section:
- Phone: replace `tel:+10000000000` and the displayed `(—) ———-————` with the real number.
- Email: replace `leasing@emberjaderealty.com` in both the `mailto:` link and the visible text.

**Photos** — each property currently shows a "Photos coming soon" placeholder tile. To swap in real photos:
1. Drop image files into `assets/` (e.g. `assets/1907-exterior.jpg`).
2. In `index.html`, replace the `<div class="property-photo placeholder-photo">...</div>` block for that property with:
   ```html
   <div class="property-photo">
     <img src="assets/1907-exterior.jpg" alt="1907 Spindletop Dr exterior">
   </div>
   ```
   You can add more than one photo per property if you want a small gallery — ask Claude to build that out once you have the images.

## Structure
```
index.html    — page content
styles.css    — all styling (brand colors/type defined at the top as CSS variables)
app.js        — just sets the footer copyright year
assets/logo.png — your logo
```
