# Contributing to Night Owl Art

This guide explains the site architecture and development workflow for contributors.

## Tech Stack

| Technology | Version | Source | Purpose |
|------------|---------|--------|---------|
| Tailwind CSS | v4 | CDN (`@tailwindcss/browser`) | Styling via utility classes |
| HTMX | v2.0.8 | CDN | Dynamic HTML loading (progressive enhancement) |
| Vanilla JS | ES6+ | Inline | Product rendering, filtering, URL handling |

**Key constraint:** This is a static site with **no build step**. All dependencies are loaded from CDN. There is no bundler, no PostCSS, no Node.js runtime required for the site itself.

## Code Organisation

- Data should be stored using the JSONL format in the `art.jsonl` file under the `data` subdirectory.
- Images should be stored in the `images` subdirectory.
- To the extent that html partials are needed, put them in the `partials` subdirectory.

## Quick Start

Local development uses the `live-server` Node package, installed and invoked with PNPM.

```bash
pnpm install
pnpm dev
```
