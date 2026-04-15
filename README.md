# Launchkit

Launch platform and documentation site for Wherewithal ventures.

## Overview

Launchkit is a Cloudflare Pages static site project hosted at `launchkit.wherewithal.studio`.

## Getting Started

```bash
npm install
npm run build
```

## Deployment

This project uses GitHub Actions for continuous deployment to Cloudflare Pages. Every push to `main` triggers an automatic deployment.

### Secrets Required

Add these secrets to GitHub repository settings (Settings → Secrets and variables → Actions):

- `CLOUDFLARE_ACCOUNT_ID` — Your Cloudflare account ID
- `CLOUDFLARE_API_TOKEN` — Cloudflare API token with Pages Deploy scope

See `.github/DEPLOYMENT.md` for troubleshooting and manual deployment procedures.

## Project Structure

```
launchkit/
├── public/          # Static site root
│   └── index.html   # Home page
├── package.json     # Node dependencies
├── wrangler.json    # Cloudflare Pages config
└── README.md        # This file
```

## License

All rights reserved. Wherewithal Ventures.
