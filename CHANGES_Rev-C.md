# Dua & Zikr — Rev-C (Bismillah open, English/Urdu, Simple mode)

Validator + logic tests + JS syntax all pass. 175 items, content_version 2.3.0.

## 1. Brief Bismillah on open
The launch splash now leads with the full Basmala
(بِسْمِ اللَّهِ الرَّحْمَٰنِ الرَّحِيمِ) in calligraphic Scheherazade, with the
name "Dua & Zikr" quiet beneath it, and holds ~1.7s with a gentle fade.

## 2. English / Urdu language selection
- New **Language** selector at the top of Display settings: English / اردو.
- Selecting Urdu switches the interface to **RTL**, localizes the chrome
  (now-reading, view picker, sheet titles, nav, prayer label, verification chip,
  settings group titles, Location & Simple-mode rows), and shows each dua's
  **Urdu translation** in proper **Nastaliq** where available.
- Transliteration and source references stay left-to-right for legibility.
- Mechanism: items carry optional `title_ur` / `translation_ur`; the reader uses
  them when Urdu is selected and **falls back to English** when an item isn't
  translated yet.

### Urdu content status — IMPORTANT
- Seeded so far (12 items, draft): the 5 new additions + the full **After-Salah**
  set (a core daily routine).
- These are **AI-drafted and flagged `urdu_status: draft_pending_review`** — they
  need an Urdu-literate reviewer before being treated as final.
- The remaining ~163 items show English until translated. Say the word and I'll
  do the next Urdu batch (suggest: Morning, Evening, Before-Sleep, Kalimas — her
  daily routine) in the same review-flagged way, or plug in an Urdu source you trust.

## 3. Simple mode (elderly-friendly) — strengthened
The existing "Easy View" is now **Simple mode (large text & buttons)**, localized,
and stronger: larger Arabic line-height, taller navigation with always-visible
Previous/Next labels, bigger title, a more prominent prayer ribbon, and reduced
clutter (type/flow tags hidden) so it is easy for your mother to operate.

## 4. Name
Stays **Dua and Zikr** (launcher, title, splash, About). Package id unchanged
(`com.ahmed.azkartv`) to keep your signing/release pipeline intact. If you want a
different exact name, tell me the text and I'll change it everywhere.

## Notes / still pending
- Run a build before publishing; `dom_smoke.mjs` needs `jsdom` (your CI has it).
- `color-mix` styling degrades gracefully on older WebViews.
- All new dua content and all Urdu translations remain pending scholarly review.
