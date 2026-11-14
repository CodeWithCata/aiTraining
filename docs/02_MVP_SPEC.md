# 02 – MVP spec (what the app does and how it is built)

## Pages (sections inside one HTML file; one visible at a time, switched by URL hash)
`#start` · `#concurs` · `#livrabile` · `#punctaj` · `#reguli` · `#roadmap` · `#prompturi` · `#glosar` · `#ziua` · `#checklist` · `#video` · `#aplicatii` · `#resurse`
Order and pager (Back/Next buttons) come from the `ORDER` array. Unknown hash falls back to `start`.

## Features
- **Start:** days-until-contest countdown (target `2026-11-20T10:00+02:00`), core idea note, start-time warning (10:00 vs 11:00), four link cards. Deliberately NO hero headline.
- **Aplicații:** team tools shown as a one-column logo list, each with a one-line Romanian description of what the tool is used for (`#appLogos`, `LOGOS` array = name, domain, link, description, 9 tools: 4 AI + Sheets, Docs, Slides, Drive, Vercel; icons for the Google apps and Vercel come from the inline `ICONS` object, the AI tools use favicons; favicon images with letter fallback), then the role-filtered app list.
- **Concursul pe scurt / Reguli / Punctaj:** static facts; Punctaj has a Preselecție/Finală toggle with bars.
- **Livrabile:** the 6 deliverables with owner role; filterable by role.
- **Roadmap pe zile:** 6 day tabs, panel per day (exercise, keep, done-when), "mark done" with progress meter, auto-selects today.
- **Constructor de prompturi:** pick the target AI (Claude / ChatGPT / Gemini / Google Flow), write one free request in any language → live output is a meta-prompt to paste into Gemini, which returns a full English prompt (ROLE, CONTEXT, TASK, CONSTRAINTS, FORMAT, ACCEPTANCE CRITERIA) for the chosen AI. Google Flow = image prompt only. Copy, example, clear. (The old 6-field form and the "save to library" button were removed.)
- **Glosar:** searchable, category chips. **Tap-a-word:** first mention of each glossary term in a section gets a dotted underline and opens an inline popover (static text only; text re-rendered by JS, e.g. roadmap panel, is not linked).
- **Cele 180 de minute:** phase list, colour bar, stopwatch (start/pause/reset) highlighting the current phase.
- **Checklist-uri:** grouped, checkable, filter chips, reset.
- **Videoclipuri / Aplicații / Linkuri:** curated lists with honesty tags (direct link / verified / YouTube search).
- **Role switch (sidebar):** collapsible "Rolul tău" (Toți / Tech Lead / Produs & UX / Business & QA). Filters Livrabile and Aplicații, dims roadmap days led by someone else, and marks menu items with a dot (relevant) or dims them (less relevant) via `MENU_ROLES`.
- **Theme** light/dark (persisted; applied before paint), mobile drawer menu, keyboard-accessible, `prefers-reduced-motion` respected.

## Code structure (all inside `index.html`)
1. `<head>`: theme bootstrap script, Google Fonts link, one `<style>` block (tokens first, then layout, components, mobile, motion).
2. `<body>`: inline SVG icon sprite (`<symbol id="i-…">`, 24px grid, 1.75 stroke), `<nav class="side">`, `<main>` with one `<section id="…">` per page.
3. One IIFE `<script>`: data arrays → renderers → handlers → navigation.
   Data arrays you will edit most: `PHASES`, `DAYS`, `GLOSS`, `DELIV` + `DELIV_ROLES`, `APPS` + `APP_ROLES`, `CHECK`, `VIDEOS`, `RES`, `ORDER`, `MENU_ROLES`, `ROLES`/`SHORT`.
4. Adding a page: add `<section id="x">`, a menu `<li><a href="#x">`, an entry in `ORDER`, optionally in `MENU_ROLES`.

## Persistence (localStorage, per device, never shared between teammates)
`theme`, `role`, `names`, `days` (done days), `checks`. (Old keys `strat`, `fin`, `journal`, `plib`, `tplTab` from the removed Șabloane page may still sit in a browser; nothing reads them.)
All reads/writes are wrapped in try/catch (`store.get/set`). Sharing between teammates would need an export/import button or a backend (not built).

## Constraints
- Single file, no dependencies, no build. External: Google Fonts only.
- Do not use inline event attributes for new code; follow the existing `$`/`$$` helpers and ES5-style where the file already uses it.
