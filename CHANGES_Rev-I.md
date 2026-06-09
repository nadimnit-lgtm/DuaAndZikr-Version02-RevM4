# Dua & Zikr — Rev-I (find-by-name search + Qunut/Istikhara fix)

Validator + logic tests + JS syntax pass. Total items: 185 (content_version 2.6.0).

## Why this revision
You couldn't find specific du'as (Qunut, Istikhara) by name. They were already
in the app but buried in the generic "Dua" section with no search, and Istikhara
was duplicated. Fixed both.

## 1. Content fixes
- Removed a duplicate Istikhara entry (186 -> 185).
- Renamed for clarity/searchability:
  - "Qunoot al-Witr" -> "Dua al-Qunut (Witr)"
  - "Complete Dua al-Istikhara" -> "Salat al-Istikhara (Prayer for Guidance)"

## 2. New: search any du'a by name
- A search box now sits at the top of the "What to read" sheet.
- Type a name (e.g. "qunut", "istikhara", "wudu", "travel") and it lists every
  matching du'a by title + category; tap one to jump straight to it.
- Matches title, Urdu title, category, and transliteration. Localised
  placeholder (English / Urdu). Works with Simple mode (larger box) and RTL.

## Note on discoverability
The generic "Dua" (18) and "Azkar" (11) buckets are still broad. The search box
solves finding any specific item now. If you'd like, the next structural step is
to split those buckets into clearer named sections (e.g. In-Prayer, Witr/Qunut,
Istikhara, Wudu) so they're browsable too.

## Still pending review
New content and all Urdu remain pending scholarly / Urdu-literate sign-off.
