# Sangam Sharma — Personal Portfolio

A responsive personal portfolio built with plain HTML, CSS and vanilla JavaScript. There is no framework, package installation, build step or backend.

## Run locally

Open `index.html` in a browser, or run a local server from this folder:

```bash
python -m http.server 8000
```

Then visit `http://localhost:8000`.

## Project structure

```text
portfolio-website/
├── index.html
├── favicon.svg
├── robots.txt
├── sitemap.xml
├── security.txt
├── _headers
├── .well-known/
│   └── security.txt
└── assets/
    ├── css/
    │   ├── style.css
    │   └── responsive.css
    ├── js/
    │   └── script.js
    ├── images/
    └── icons/
```

## Updating content

The site is a single-page portfolio. Visible content is in `index.html`, arranged in sections:

- Navigation and introduction
- Current focus and about
- Featured projects and additional academic work
- Skills and technologies
- Education and experience
- Certifications and training
- Contact details

Keep project descriptions accurate. Add repository, demo or write-up links only after those resources are published and checked. The current restaurant ordering system is marked as in progress.

## Contact

The contact section uses direct links to the email address, LinkedIn profile and GitHub profile. There is no contact form or backend.

## Deploy with Cloudflare Pages

This repository is a static website. For a Git-connected Cloudflare Pages project, use:

- Framework preset: `None`
- Build command: leave blank
- Build output directory: `.`
- Production branch: `main`

Make sure `index.html` is at the repository root. Connect the GitHub repository to Cloudflare Pages, deploy the `main` branch, and test the generated `pages.dev` address. Then add the custom domain from the Pages project's **Custom domains** settings. Follow the DNS instructions shown by Cloudflare; do not add guessed DNS records manually.

## Before publishing changes

- Check the page at desktop and mobile widths.
- Confirm email, LinkedIn and GitHub links.
- Check that every project description reflects completed work accurately.
- Add screenshots or public repository links only when the real assets are ready.
- Do not add a resume download link until a real resume PDF is available.


## Security configuration

Cloudflare Pages reads the root-level `_headers` file and applies the listed response headers to static assets. This project includes a restrictive Content Security Policy, clickjacking protection, MIME-sniffing protection, a referrer policy, a limited permissions policy and HSTS. The CSP permits only this site's assets plus Google Fonts stylesheets/fonts; the JSON-LD metadata block is allowlisted by its SHA-256 hash. Inline style attributes and JavaScript style mutations were removed so the policy does not need `unsafe-inline`.

After deployment, verify the live response headers and test the page in a browser. If you add analytics, embedded media, external images, scripts or other third-party services later, review and deliberately update the CSP rather than weakening it broadly. HSTS is enabled with a one-year max-age and without `includeSubDomains` or `preload`; keep HTTPS working before publishing and do not enable broader HSTS settings until every relevant subdomain is confirmed HTTPS-ready.

The files in this repository cannot guarantee security of the hosting account, GitHub account, DNS configuration or Cloudflare account. Protect those accounts with unique passwords and multi-factor authentication.
