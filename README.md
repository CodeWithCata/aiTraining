# AI Business Challenge UPB – team prep guide (single-file web app)

READ THIS FIRST, then `docs/01_CONTEXT.md`, `docs/02_MVP_SPEC.md`, `docs/03_DESIGN_AND_USER_PREFERENCES.md`, `docs/04_STATUS_AND_TODO.md`.

## What this is
`index.html` is ONE self-contained file (HTML + CSS + JS, ~95 KB, no build step, no framework) that works as a **preparation guide and contest-day cockpit** for a 3-person high-school team entering the *AI-Powered Business Challenge* (Start Your StartUP 2026, POLITEHNICA București, **21 Nov 2026**, 3-hour on-site contest).

It is NOT the contest application. The team will build the real app on contest day, after the theme is revealed. This page helps them prepare during the 6 days before and organize themselves during the 3 hours.

## Language
- UI and content: **Romanian** (`lang="ro"`).
- Conversation with the user: Romanian, short and direct. The user reads on a phone (Claude mobile app).
- Docs in this folder (except `HANDOFF_original_RO.md`): English.

## Run it
Open `index.html` in a browser. No server needed. Google Fonts (IBM Plex) load from the internet; offline it falls back to system fonts.

## Files
- `index.html` – the app
- `exemplu/` – assets for the Exemplu tab (example app, Excel model, poster/post images). Keep next to index.html
- `docs/01_CONTEXT.md` – the contest, the team, the rules, what is unverified
- `docs/02_MVP_SPEC.md` – features, code structure, data, storage keys
- `docs/03_DESIGN_AND_USER_PREFERENCES.md` – design system and what the user explicitly likes/hates
- `docs/04_STATUS_AND_TODO.md` – what was tested, known gaps, next steps
- `docs/HANDOFF_original_RO.md` – earlier handoff written in Romanian (contest facts, 6-day plan)
