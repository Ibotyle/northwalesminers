# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Static website for North Wales Miners Association Trust - recovered from Wayback Machine archives. Hosted on Cloudflare.

**Domain:** https://northwalesminers.com (no www)

## Architecture

- Pure static HTML/CSS site (no build step)
- `index.html` - main homepage (served at `/`)
- `index.htm` - duplicate with canonical to `/` (backward compatibility)
- `style.css` - shared styles across all pages
- `favicon.svg` - site icon

### Directory Structure

```
/                       # Homepage + global assets
/trust/                 # Trust info pages (why.htm, contactus.htm)
/sites.htm              # Mine sites index
/sites/minecoal/        # Coal mine pages
/sites/minemetal/       # Metal mine pages (lead)
/minecoal/              # Legacy path (crossfoxes duplicate)
```

## Deployment

- Hosted on Cloudflare Pages
- GitHub repo: `Ibotyle/northwalesminers`
- Push to `master` triggers deploy

## SEO

- All pages have Open Graph and Twitter card meta tags
- Canonical URLs point to `https://northwalesminers.com/` (no www)
- `sitemap.xml` and `robots.txt` in root
- `.htm` pages have canonical pointing to preferred URL

## Content Source

Original content recovered from Wayback Machine (web.archive.org) snapshots from 2011-2013. Priority URLs for future recovery listed in `prompt.md`.
