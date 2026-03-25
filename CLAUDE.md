# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Commands

```bash
npm run dev       # Start dev server (http://localhost:4321)
npm run build     # Build production site to ./dist/
npm run preview   # Preview production build locally
```

No lint or test commands are configured.

## Project Overview

This is an Astro 4.x static site for **FightCoffee** — a hybrid combat sports & lifestyle concept in Pleurtuit, Bretagne. The current goal is building an investor deck/presentation. Business documents (business plan, operational annex, HTML deck) live in the `fightcoffee/` directory and serve as content reference.

## Architecture

**Framework:** Astro with no integrations — vanilla HTML/CSS output, no React/Vue/Svelte.

**Structure:**
- `src/layouts/Layout.astro` — base HTML shell; accepts optional `title` prop; lang is `fr`
- `src/pages/` — file-based routing (currently empty; pages need to be created)
- `src/styles/global.css` — the entire design system (see below)
- `public/images/` — static image assets

## Design System (`global.css`)

All styling is done via the CSS custom properties and utility classes defined in `global.css`. Do not introduce a CSS framework.

**Colors:**
- Neutrals: `--bg`, `--bg2`, `--bg3`, `--ink`, `--ink2`, `--ink3`
- Brand: `--red` (#c8241a), `--gold` (#9a7a2e)
- Tints: `--red-pale`, `--gold-pale`

**Typography:**
- `Bebas Neue` — headings/display
- `DM Sans` — body
- `DM Mono` — labels/monospace
- Classes: `.display.xl/lg/md/sm`, `.eyebrow`, `.body-text`, `.caption`

**Layout classes:**
- `.slide` — full-viewport section with nav padding
- `.cols-2`, `.cols-3`, `.cols-4`, `.cols-12`, `.cols-21` — CSS Grid layouts
- `.cell` — bordered grid cell
- `.fighter-block` — dark-themed profile block
- `.kpi-row`, `.stat-num`, `.tag` — data/KPI display elements
- `.photo-strip` — multi-image gallery

**Responsive breakpoints:** 1024px and 768px (mobile gets hamburger nav).
