# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Night Owl is a static art portfolio site for digital artwork. It has **no build step** — all dependencies load from CDN. Deployed via GitHub Pages.

## Development Commands

```bash
pnpm install        # Install dependencies (requires pnpm v10.28.1)
pnpm dev            # Start live-server with hot reload
```

No test framework is configured yet.

## Tech Stack

- **Tailwind CSS v4** via CDN (`@tailwindcss/browser`) — no PostCSS, no build
- **HTMX v2.0.8** via CDN — dynamic HTML loading / progressive enhancement
- **Vanilla JavaScript (ES6+)** — inline, no bundler

## Architecture

This is a zero-build static site. The only Node.js dependency is `live-server` for local development. The site itself runs entirely in the browser with CDN-loaded libraries.

### File Organization

- `index.html` — Main entry point
- `data/art.jsonl` — Art metadata in JSONL format
- `images/` — Artwork image files
- `partials/` — HTML partials for HTMX (create as needed)

### Key Constraints

- No bundler, no transpilation, no server-side runtime
- All third-party code must come from CDN
- Keep JavaScript vanilla ES6+ (no frameworks)
