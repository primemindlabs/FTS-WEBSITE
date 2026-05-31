# Fortis Talent & Solutions — Website

Marketing website for Fortis Talent & Solutions, a staffing agency serving Atlanta, Charlotte, Dallas, Houston, and Nashville. Static HTML/CSS site with location pages, blog articles, and lead-capture forms.

## Tech stack

- Plain static **HTML + CSS** — no build step, no framework, no backend.
- **Netlify Forms** for lead capture (forms post to `/` with `data-netlify="true"`).
- **Google Tag Manager** (`GTM-KSFTSVZV`) for analytics.
- Google Fonts (Plus Jakarta Sans, Lora) loaded via CSS `@import`.

## Run locally

No dependencies to install. Serve the directory with any static file server:

```bash
# Python 3
python3 -m http.server 8000

# or Node (if installed)
npx serve .
```

Then open http://localhost:8000. You can also just open `index.html` directly in a browser, though a local server is recommended so root-relative paths and form posts behave correctly.

## Environment variables

None. This is a fully static site with no secrets or server-side configuration. The only third-party IDs (the GTM container ID and the `fortistalentsolutions.com` form endpoints) are public client-side values committed in the HTML by design.

## Deployment

Deployed on **Netlify**. Push to the default branch and Netlify publishes the repo root as-is (no build command required). The contact/quote/application forms rely on Netlify's built-in form handling, so form submissions only work on a Netlify deployment, not when serving the files locally.

## Pages

- `index.html` — homepage
- `staffing.html`, `direct-hire.html`, `temp-to-hire.html` — service pages
- `staffing-{atlanta,charlotte,dallas,houston,nashville}.html` — city landing pages
- `jobs.html`, `contact.html` — job listings and contact forms
- `blog.html` plus individual article pages — content marketing
