# SmileCraft Dental & Lab

A modern single-page brochure website for a combined dental clinic and dental lab. Zero build tooling — open `index.html` and it works. Designed to deploy directly to GitHub Pages.

**Live demo:** `https://<your-username>.github.io/<repo-name>/`

---

## Stack

| Layer | Tech |
|-------|------|
| Markup | HTML5 (semantic) |
| Styling | [Tailwind CSS](https://tailwindcss.com/) via Play CDN |
| Animations | [AOS.js](https://michalsnik.github.io/aos/) |
| Fonts | Google Fonts — Playfair Display + Inter |
| Forms | [Formspree](https://formspree.io/) (free tier) |
| Hosting | GitHub Pages |

No `node_modules`, no build step, no CI required.

---

## Sections

1. **Navbar** — sticky, mobile hamburger, smooth-scroll links
2. **Hero** — full-viewport with gradient overlay and CTAs
3. **Clinic Services** — 6-card grid (Implants, Whitening, Orthodontics, Root Canal, Veneers, General)
4. **Lab Services** — 6-card grid on dark background with turnaround times
5. **About** — story + animated stat counters + team photo
6. **Team** — 3 circular photo cards
7. **Gallery** — CSS grid with keyboard-navigable lightbox (←/→/Esc)
8. **Contact** — form + Google Maps embed + contact details
9. **Footer** — social icons, quick links, copyright

---

## File Structure

```
Website-Testing/
  index.html          # entire site
  assets/
    favicon.svg       # tooth icon
    images/           # drop local images here if needed
  README.md
```

---

## Setup & Deploy

### Local preview
Just open the file — no server needed:
```bash
open index.html
```

### GitHub Pages deployment
```bash
git init
git add .
git commit -m "init: SmileCraft dental website"
git branch -M main
git remote add origin https://github.com/<username>/<repo>.git
git push -u origin main
```
Then: **GitHub repo → Settings → Pages → Source: `main` branch / `/ (root)`**

Site goes live at `https://<username>.github.io/<repo>/` within ~60 seconds.

---

## Configuration

### Contact form (Formspree)
1. Create a free account at [formspree.io](https://formspree.io/)
2. Create a new form and copy the endpoint ID
3. In `index.html`, replace the form action:
```html
<!-- find this line -->
<form action="https://formspree.io/f/YOUR_FORM_ID" ...>

<!-- replace YOUR_FORM_ID with your real ID, e.g. -->
<form action="https://formspree.io/f/xpwzabcd" ...>
```

### Branding
All colors are Tailwind CSS custom properties defined in the `<script>` config block at the top of `index.html`:
```js
colors: {
  primary: '#0e7490',       // deep teal — buttons, headings, icons
  'primary-dark': '#0c5f73', // hover state
  accent: '#22d3ee',         // bright cyan — highlights
  surface: '#f0f9ff',        // ice white — section backgrounds
}
```

### Images
Placeholder images use Unsplash CDN URLs. Replace the `src` attributes in the hero, about, team, and gallery sections with your own images. Drop them in `assets/images/` and update paths accordingly.

---

## Customisation Checklist

- [ ] Replace business name (`SmileCraft Dental & Lab`) throughout `index.html`
- [ ] Swap Unsplash placeholder images with real photos
- [ ] Update address, phone, and email in Contact section and Footer
- [ ] Update Google Maps embed URL with your actual location
- [ ] Replace `YOUR_FORM_ID` with real Formspree endpoint
- [ ] Update team names, titles, and bios
- [ ] Add your real social media profile links in Footer
