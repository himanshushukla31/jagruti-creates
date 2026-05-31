# jagruti.creates — website

A single-file website for Jagruti's handmade mandala art. Everything lives in **`index.html`**
(HTML + CSS + JS together), so there's nothing to install or build.

## View it locally
Double-click `index.html` — it opens in your browser.

## Put it online (so you get a link for your Instagram bio)

Easiest, free, no account-juggling:

1. Go to **https://app.netlify.com/drop**
2. Drag the whole **`jagruti-creates` folder** onto the page.
3. You'll instantly get a live URL like `https://jagruti-creates.netlify.app`.
4. Open the **Instagram mobile app** → Edit profile → **Website** → paste that URL.
   (Web can't edit the Website field — it's app-only, as the edit page noted.)

To update later: drag the folder onto Netlify Drop again, or connect the folder to a free
Netlify/GitHub account for auto-updates.

Other free hosts that work the same way: **Vercel**, **Cloudflare Pages**, **GitHub Pages**.

## Customising (all edits are in `index.html`)

### Swap in your real art photos (gallery)
Find the `mandala(...)` tiles built in the `<script>` near the bottom (the `palettes.forEach`
block). To use a real photo instead of a generated mandala, replace a tile's inner SVG with an
image. The simplest approach: put your photos in this folder and edit the gallery loop so each
tile uses `<img src="my-photo.jpg" alt="Lotus Bloom">` instead of `mandala({...})`.

### Add your portrait (About section)
In the `.portrait` div, replace the `<div id="portraitMandala">` with:
`<img src="me.jpg" alt="Jagruti in her studio" style="width:100%;height:100%;object-fit:cover">`

### Link your real reels (Watch section)
In the `<script>`, the `vlabels` array drives the three video cards. Point each card's `href`
at a specific reel URL, or embed the reels directly.

### Email
In the footer there's a `mailto:hello@jagruticreates.com` link — change it to your real address.

### Text / colours
- All copy is plain text in the HTML — edit it directly.
- Colours live at the very top of the `<style>` block in the `:root { ... }` variables
  (`--terracotta`, `--teal`, `--gold`, etc.). Change them in one place and the whole site updates.

## What still needs the Instagram mobile app
- **Website link** in your bio (web is read-only for this)
- **Profile photo** change
- **Posting reels/videos**
