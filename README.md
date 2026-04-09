# Monse's Taste of El Salvador — Website

Complete static website for Monse's Taste of El Salvador Pupuseria.
115 S. 25th Street, Colorado Springs, CO 80904 · (719) 473-0877

---

## File Structure

```
monses-website/
├── index.html            ← Home page
├── menu.html             ← Full menu
├── about.html            ← About us / story
├── events.html           ← Private events (call to inquire)
├── gallery.html          ← Photo gallery with lightbox
├── privacy-policy.html   ← Full privacy policy (GA4 compliant)
├── css/
│   └── styles.css        ← All shared styles + design tokens
├── js/
│   └── main.js           ← Shared JavaScript (nav, animations, etc.)
├── images/
│   └── README.txt        ← Instructions for adding photos
└── README.md             ← This file
```

---

## How to Open the Site

Double-click `index.html` to open in your browser. All links between
pages are relative, so everything works locally without a server.

To host online: upload the entire `monses-website/` folder to any
static web host (Netlify, GitHub Pages, Squarespace Developer Mode, etc.).

---

## Adding Google Analytics (GA4)

1. Create a GA4 property at [analytics.google.com](https://analytics.google.com)
2. Get your Measurement ID (format: `G-XXXXXXXXXX`)
3. In **every HTML file**, find this comment in the `<head>`:
   ```html
   <!-- PASTE YOUR GOOGLE ANALYTICS GA4 SCRIPT TAG HERE -->
   ```
4. Replace that comment with your GA4 script tag:
   ```html
   <script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
   <script>
     window.dataLayer = window.dataLayer || [];
     function gtag(){dataLayer.push(arguments);}
     gtag('js', new Date());
     gtag('config', 'G-XXXXXXXXXX');
   </script>
   ```
5. Replace `G-XXXXXXXXXX` with your actual Measurement ID in both places

The Privacy Policy already discloses Google Analytics data collection as required.

---

## Adding Your Favicon

1. Create a 64×64px PNG of your logo (transparent background recommended)
2. Save it as `images/favicon.png`
3. In each HTML file, find this comment in `<head>`:
   ```html
   <!-- <link rel="icon" type="image/png" href="images/favicon.png" /> -->
   ```
4. Remove the `<!--` and `-->` to uncomment it

---

## Swapping Placeholder Content

### Hero Background Image
The home page hero background is set in `css/styles.css`:
```css
.hero-bg {
  background: ..., url('../images/hero-bg.jpg') center/cover no-repeat;
}
```
Add your photo to the `images/` folder named `hero-bg.jpg`.

### About / Events Page Photos
Look for `<div class="img-placeholder">` blocks. Replace with:
```html
<img src="images/your-photo.jpg" alt="Description of photo"
     class="about-img-main" width="600" height="480" loading="lazy" />
```

### Gallery Photos
In `gallery.html`, additional placeholder slots are marked with:
```html
<!-- REPLACE: restaurant exterior photo -->
```
Replace `<div class="gallery-placeholder">` blocks with `<img>` tags
pointing to your photos in the `images/` folder.

### Owner / Story Text
In `about.html`, look for:
```html
<!-- REPLACE: Personalize this story ... -->
```
These are clearly marked placeholder paragraphs for the owner to customize.

---

## Menu Prices & Items

All menu items and prices have been verified from the restaurant's
live menu as of early 2026:

- **Pupusas:** $6.00 each (14 filling options)
- **Pupusa Plate (1):** $9.00 · **(2):** $14.00 · **(3):** $16.75
- **Pupusas Colorado (2):** $17.25
- **Chalchuapa (5 pupusas):** $34.50
- **Tazumal (8 pupusas):** $50.00
- **Tostadas Salvadorenos:** $13.50
- **Chilaquillas Salvadorenos:** $15.00
- **Plato Amigos:** $16.00
- **Dos Tamales:** $15.00
- **Brunch items:** $8.99–$11.75

> **Note:** Prices may change. Update `menu.html` whenever prices change.
> Online ordering and current pricing: https://order.toasttab.com/online/monsess-old-colorado-city-115-south-25th-street

---

## Design System

Colors, fonts, and spacing tokens are defined at the top of `css/styles.css`
as CSS custom properties (`:root { ... }`). Change values there to update
the entire site's appearance at once.

| Token | Value | Use |
|---|---|---|
| `--red` | `#8C1F11` | Primary brand red |
| `--red-dark` | `#5E1209` | Nav, dark backgrounds |
| `--gold` | `#C4860A` | Accents, CTAs |
| `--cream` | `#FDF6E3` | Section backgrounds |
| `--font-heading` | Playfair Display SC | All headings |
| `--font-body` | Karla | Body text |

---

## Navigation Active States

Each page sets the active nav link with `class="active"` on the
corresponding `<a>` tag in both the desktop nav and mobile menu.
No JavaScript required — it's purely CSS-driven.

---

## Browser Support

Works in all modern browsers: Chrome, Firefox, Safari, Edge.
No build tools, no dependencies, no frameworks. Pure HTML/CSS/JS.
