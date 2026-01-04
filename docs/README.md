# Nagstamon Documentation Site (Hugo)

This site has been migrated from Jekyll to Hugo while maintaining backward-compatible URLs.

## Building the Site

### Prerequisites
- Hugo Extended v0.128.0 or later

### Local Development
```bash
cd docs
hugo server -D
```

### Production Build
```bash
cd docs
hugo --minify
```

The output will be in `docs/public/`.

## Site Structure

- `content/` - Page content and blog posts
- `content/news/` - News/blog posts (rendered at root by slug)
- `layouts/` - Hugo templates
- `static/` - Static assets (CSS, images, CNAME, favicon)
- `data/` - Data files
- `hugo.toml` - Hugo configuration

## URL Structure

All URLs are backward-compatible with the previous Jekyll site:

- Pages: `/features/`, `/download/`, `/documentation/`, `/legal/`
- Posts: `/:slug/` (e.g., `/nagstamon-3-0-finally-out/`)
- RSS Feed: `/feed.xml` (with redirect from `/feed`)

## GitHub Actions Deployment

The site is automatically deployed to GitHub Pages via `.github/workflows/pages.yml` on pushes to the main branch.
