# AGENTS.md

## Project overview

Single-file HTML game ("水果連連看" / Fruit Link). Self-contained — all CSS and JS are inline in `linkgame.html` (~930 lines). No build step, no package manager, no test framework.

## How to run

Open `linkgame.html` in a browser. No server required, though the page expects a shared stylesheet at `/static/shared/style.css` (part of a parent site, not included here).

## Structure

- `linkgame.html` — entire game (markup + CSS + JS)
- `linkgame.html:Zone.Identifier` — Windows download metadata, not relevant

## Key facts

- Language: Traditional Chinese (`zh-Hant`)
- Two `localStorage` keys: `sage-linkgame-save` (game state) and `sage-linkgame-audio` (music/sfx toggle prefs)
- 5 levels with grids from 3×4 to 7×8; 8 emoji patterns (水果 + 動物)
- Path-finding algorithm (`canConnect` / `getConnectionPath`) attributed to `eden-chen-ehen/link-game`
- All audio via Web Audio API oscillators — no audio files
- Canvas overlay for connection-line animation and particle effects
- Auto-shuffles on deadlock (up to 80 attempts); game-over if still unsolvable
- Combo system: matches within 3 seconds stack multiplier
- Cloudflare analytics beacon at page bottom
- Responsive layout via `@media (max-width: 980px)` breakpoint

## Commands

No lint, test, typecheck, or build commands exist. There is nothing to install.
