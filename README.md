# Xencore Global AG — Website

Three-page static website built for Cloudflare Pages deployment.

## File structure

```
/
├── index.html          Home page
├── what-we-build.html  Products & services
├── about.html          About & contact
├── style.css           Shared stylesheet
└── README.md           This file
```

## Deployment — Cloudflare Pages (recommended)

1. Push this folder to a GitHub repository
2. Log in to Cloudflare Dashboard → Pages → Create a project
3. Connect your GitHub repository
4. Build settings:
   - Framework preset: **None**
   - Build command: *(leave blank)*
   - Build output directory: `/` (root)
5. Click **Save and Deploy**

Every push to `main` deploys automatically. No build step required.

## Custom domain

In Cloudflare Pages → your project → Custom domains:
- Add `xencoreglobal.com` and `www.xencoreglobal.com`
- Cloudflare manages the SSL certificate automatically

## Contact form

The contact form in `about.html` uses Formspree by default.

1. Create a free account at https://formspree.io
2. Create a new form and copy your form ID
3. In `about.html`, replace `YOUR_FORM_ID` in the form action:
   ```html
   action="https://formspree.io/f/YOUR_FORM_ID"
   ```

**Alternative — Cloudflare Pages Functions:**
Create `/functions/api/contact.js` to handle form submissions
serverlessly via Cloudflare Workers. See:
https://developers.cloudflare.com/pages/functions/

## Logo

Replace the placeholder SVG in all three nav `<div class="xc-nav__logo-mark">` 
elements with the actual Xencore Global SVG logo mark.

## Environmental Technology

should be replaced with the actual product name once confirmed.

## Forge link

The Forge product links to `https://forge.projectcoachai.com` throughout.
Update this URL if the domain changes.

## Tech stack

- Hosting: Cloudflare Pages
- DNS & CDN: Cloudflare
- Version control: GitHub
- Deployment: Git push → auto-deploy (no CI/CD pipeline needed)
- No build tools, no npm, no dependencies — pure HTML/CSS/JS
