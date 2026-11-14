# 04 – Status and next steps (as of Sat 14 Nov 2026)

## Tested
- JavaScript parses (`new Function` check on every inline script).
- Smoke-tested in **jsdom** (simulated browser): no runtime errors; template tabs render; journal add; role switch; menu highlighting; glossary popover; saved-name sanitising.

## NOT tested
- Not opened in a real browser or on a real phone by the assistant. Visual quality, scrolling, animation feel, popover placement on small screens, the mobile drawer and iOS behaviour are unverified. The user has been sending screenshots; fix what they show with small edits, do not rewrite.
- "Copy for Sheets/Excel" (tab-separated formulas) not pasted into Sheets/Excel yet. Check Romanian-locale Excel behaviour.
- Print layout does not exist.

## Known gaps
- Checklists and the 180-minute phases are not filtered by role.
- Tap-a-word does not cover JS re-rendered text (roadmap panel). Only first mention per section.
- `MENU_ROLES` (which page matters for which role) is the assistant's own assumption; ask the user.
- Progress is per device; teammates do not see each other's ticks or entries.
- Fonts need internet on first load (no offline caching/PWA).
- Names prompt uses `window.prompt` (clunky); an inline editor would be nicer.

## Suggested next steps (ask the user which)
1. Real-device pass (phone + desktop), fix visual issues from screenshots.
2. Export/import of saved data (JSON) so teammates can share progress.
3. Role filter for checklists and contest-day phases.
4. Print view of the 180-minute plan + checklists on one A4 page.
5. Offline support (service worker / inlined fonts) for bad venue wifi.
6. Practice material: an invented theme and fake data for the day-5 simulation; 3-minute pitch rehearsal and likely jury questions.
7. Confirm open questions with organizers (start time, registration, submission format).

## Update 14 Nov 2026 (later)
- Contest date changed to **21 Nov 2026** (high-school section); countdown, texts and docs updated. Start time still unconfirmed.
- The old "Exemple" tab is now **"Exemplu"** (`#exemplu`): a full invented project "Socoteala" - brief, working app, one-page strategy, financial model (interactive + Excel), poster + social post, AI log, 5-slide pitch with speaker notes.
- New folder `exemplu/`: `app.html` (the real example app, standalone), `model-financiar.xlsx` (formulas, checked by recalculation), `afis.png/.svg`, `postare.png/.svg`, `ecran-app.png`.
- Public link of the example app is a private Claude artifact; it opens for others only after the owner shares it. QR codes in the poster/post/slide 5 point to it.
- Tested in headless Chromium (logic of the app, model, slides, no console errors at 400 px and 1100 px). Not tested on a real phone.

## Update 14 Nov 2026 (latest)
- **Aplicatii page:** team tools (Claude, ChatGPT, Gemini, Google Flow) are shown as a **single column** of logo + name links, each with a one-line Romanian "used for" description (4th item in each `LOGOS` entry), above the filtered app list (`<ul class="logos" id="appLogos">`, filled from the `LOGOS` array). Logos are site favicons from `google.com/s2/favicons`; if one fails to load, a letter fallback shows (`.lg.off`). Needs internet. Not checked on a real phone.
- **Prompt builder reworked (`#prompturi`):** instead of 6 fields it now has a target picker (Claude / ChatGPT / Gemini / Google Flow, `#pTarget`, `P_TARGET`, `P_HINT`) and ONE free-text request field. The output is a meta-prompt to paste into Gemini, which turns it into a full English prompt (ROLE, CONTEXT, TASK, CONSTRAINTS, FORMAT, ACCEPTANCE CRITERIA) for the chosen AI. Google Flow gets an image-prompt variant (images only). `PROMPT_EX` now holds one `REQUEST` example.
- Scripts parse (`node --check`). Not re-tested in a browser after these changes.
- "Model financiar" apps list now shows only **Google Sheets** (the user has no paid Excel). The .xlsx download still exists and opens in Google Sheets via Drive.
- Aplicatii logo column now lists **all tools the team needs** (9): Claude, ChatGPT, Gemini, Google Flow, Google Sheets, Google Docs, Google Slides, Google Drive, Netlify Drop, each with a one-line Romanian description. PowerPoint removed from the "Slide-uri" row (paid; Google Slides is enough). The "Planul echipei" text now says "patru unelte AI".
- Logos: Google Docs/Sheets/Slides/Drive and Vercel are **inline SVG icons** (`ICONS` object in the script, simplified own drawings, not the official files) because the favicon service returned the generic Google "G" for all Google apps. The AI tools still use favicons. Publishing tool is now **Vercel** (user's decision): "Netlify Drop" removed from the logo list and from the "Publicat linkul" row (GitHub Pages removed there too). Note: Vercel has no drag-and-drop deploy like Netlify Drop; it needs a GitHub repo import or the CLI. Test the publish flow before contest day.
- Renamed in the UI: Livrabile -> **Lucruri de predat** (menu, page title, texts, "(de predat nr. N)" in lessons, role counter) and Glosar -> **Dicționar** (menu, title, search label, Învață card, pager). Checked in headless Chromium at 400 and 1100 px: no console errors, menu fits. The SVG label "Construiți livrabilele" became "Construiți ce predăm".
- **Removed the "Șabloane" page** (user: "cam inutila"): menu item, section, all its code (strategy template, financial-model table + .xlsx/JSON export, AI-log journal, saved-prompt library) and the "Salvează în bibliotecă" button of the prompt builder. Texts that pointed to it now point to Google Docs / Google Sheets. Old `#sabloane` links fall back to Start. The finished example model stays on the Exemplu page (`exemplu/model-financiar.xlsx`). Some template-only CSS may remain unused. Tested in headless Chromium at 400 and 1100 px: no console errors, every remaining page opens, prompt builder works.
