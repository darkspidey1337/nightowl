# Contributing to Night Owl Art

This guide explains the site architecture and development workflow for contributors.

## Tech Stack

| Technology | Version | Source | Purpose |
|------------|---------|--------|---------|
| Tailwind CSS | v4 | CDN (`@tailwindcss/browser`) | Styling via utility classes |
| HTMX | v2.0.8 | CDN | Dynamic HTML loading (progressive enhancement) |
| Vanilla JS | ES6+ | Inline | Product rendering, filtering, URL handling |

**Key constraint:** This is a static site with **no build step**. All dependencies are loaded from CDN. There is no bundler, no PostCSS, no Node.js runtime required for the site itself.

## Quick Start

```bash
pnpm install
pnpm dev
```
