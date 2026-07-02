# AGENTS.md

## Project overview

Two self-contained HTML games. No build step, no package manager, no test framework. All CSS and JS are inline — each file is fully runnable by itself.

## Structure

- `linkgame.html` (932 lines) — 水果連連看 (Fruit Link, match-2 tile game)
- `galaga.html` (~1076 lines) — 小蜜蜂射擊遊戲 (Galaga-style shooter)
- `linkgame.html:Zone.Identifier` — Windows download metadata, ignore

## How to run

Open either `linkgame.html` or `galaga.html` directly in a browser. No server required.

Note: `linkgame.html` links to `/static/shared/style.css` (a shared stylesheet from the parent site). If it's unavailable, the game still works — the inline styles cover everything needed.

## Key facts

- Language: Traditional Chinese (`zh-Hant` / `zh-TW`)
- `linkgame.html` uses two `localStorage` keys: `sage-linkgame-save` (game state) and `sage-linkgame-audio` (music/sfx toggle prefs)
- `galaga.html` uses one `localStorage` key: `sage-galaga-audio` (music/sfx toggle prefs)
- Both games use Web Audio API oscillators for audio — no audio files
- `galaga.html`: 5 levels with increasing difficulty (enemy count, speed, queen count/HP, fire rate)
- `galaga.html`: Player starts with 3 planes; each plane lost triggers explosion SFX
- `galaga.html`: Level transition screen (2s) between stages; "全部關卡通過" on final win

## Commands

None. Open a file in a browser — that's it.
