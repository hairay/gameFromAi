# AGENTS.md

## Project overview

Single-file HTML game ("水果連連看" / Fruit Link). Self-contained — all CSS and JS are inline in `linkgame.html`. No build step, no package manager, no test framework.

## How to run

Open `linkgame.html` in a browser. No server required, though the page expects a shared stylesheet at `/static/shared/style.css` (part of a parent site, not included here).

## Structure

- `linkgame.html` — entire game (markup + CSS + JS, ~800 lines)
- `linkgame.html:Zone.Identifier` — Windows download metadata, not relevant

## Key facts

- Language: Traditional Chinese (`zh-Hant`)
- Save/load uses `localStorage` (key: `sage-linkgame-save`)
- 5 levels with grids from 3x4 to 7x8
- Path-finding algorithm attributed to `eden-chen-ehen/link-game` (line 262)
- Responsive layout via `@media (max-width: 980px)` breakpoint
- Cloudflare analytics beacon is included at page bottom

## Commands

No lint, test, typecheck, or build commands exist. There is nothing to install.
