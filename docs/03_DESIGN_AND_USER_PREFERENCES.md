# 03 – Design system and what the user wants

## Direction: "field manual"
Warm tinted paper, ink text, ONE accent (vermilion). Plain, editorial, no decoration.
- **Type:** IBM Plex Sans (all text, bold headings) + IBM Plex Mono (times, labels, numbers). Weights 400/500/600 and mono 400/500, `font-display: swap`.
- **Tokens (CSS variables on `:root`, dark override on `[data-theme="dark"]`):** `--paper --surface --ink --muted --line --accent --accent-soft --on-accent --thumb`; spacing `--s1…--s9` on a 4/8 grid; radii `--r1:2px --r2:4px`; type scale ratio 1.25; `--ease`.
- Light: paper `#f3efe6`, ink `#1d1b16`, accent `#a83c0c`. Dark: paper `#141210`, ink `#eee9de`, accent `#f0955f`.
- No shadows (borders + tonal fills), except the glossary popover. Icons: one inline SVG set, never emoji.
- Motion: 0.2–0.35 s ease-out, short staggered entrance on section change, press feedback; all disabled under `prefers-reduced-motion`.
- Tap targets ≥ 44 px, visible `:focus-visible` rings, thin themed scrollbars.

## Explicit user preferences (learned the hard way – respect them)
- **Mobile first.** The user reads on a phone. Check every change at ~360 px.
- **No useless words.** They removed: the hero headline and intro paragraph, the "AI Business Challenge" brand text, "Meniu"/"Temă" button labels (icon-only now), decorative accent bars above headings, the colour bar + legend on the start page. Everyone on the team already knows what the contest is.
- **Do not over-remove.** When told to remove "the hero" the whole start page was deleted by mistake; the user was upset. Remove exactly what was named, nothing more. Ask only if truly ambiguous.
- **No "vibecoded slop".** No gradient text, glow blobs, generic hero, emoji icons, fake stats, decorative animation.
- **Labels must mean something.** "Persoana 1/2/3" was rejected; roles describe what the person does (Tech Lead, Produs & UX, Business & QA).
- Wants quick, premium-feeling micro-animations, better fonts, real icons, a collapsible role picker, and menu hints by role.
- Replies: short, concrete, no long intros. Say plainly what was and was not tested.
- **Wording:** the user said "livrabil" and "glosar" sound odd in Romanian. Visible text now says **"Lucruri de predat"** (was Livrabile) and **"Dicționar"** (was Glosar). Internal ids/hashes (`#livrabile`, `#glosar`, `MENU_ROLES` keys, `ORDER` keys) are unchanged on purpose so links and code keep working. Do not bring the old words back in new text. The English docs still say "deliverables" and "glossary".
